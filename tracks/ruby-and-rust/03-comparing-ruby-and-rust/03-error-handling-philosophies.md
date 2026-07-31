# Error Handling Philosophies

## Learning objectives

- Contrast Ruby exceptions with Rust's `Result` / `Option`
- Map to Java checked/unchecked, Python exceptions, Go's `error`
- Choose idiomatic patterns in each language

---

## Concept

**Ruby** (like Python/Java) treats many failures as **exceptions**: unwind the stack until `rescue` (or crash).

**Rust** splits the world:

- **Expected failures** → `Result<T, E>` (file not found, invalid input)  
- **Absence** → `Option<T>` (not an error, just nothing)  
- **Bugs** → `panic!` (index out of bounds, assertion)

Go sits between: multiple return values + `error`, rarely panics. Rust's `Result` is Go's idea with **type-forced handling** and the `?` operator.

---

## Comparison table

| Style | Java | Python | Go | Ruby | Rust |
|-------|------|--------|-----|------|------|
| Primary mechanism | Exceptions | Exceptions | `error` values | Exceptions | `Result` / `Option` |
| Absence | `null` / Optional | `None` | zero value / comma-ok | `nil` | `Option` |
| Must handle? | Checked exceptions try | No | By convention | No | Yes (or explicitly ignore) |
| Propagation sugar | — | — | `if err != nil` | raise | `?` |
| Catastrophic | Error / crash | SystemExit etc. | panic | raise / fail | `panic!` |

---

## Side-by-side

### Ruby

```ruby
def read_config(path)
  File.read(path)
rescue Errno::ENOENT
  raise "missing config: #{path}"
end
```

### Rust

```rust
use std::fs;
use std::io;

fn read_config(path: &str) -> Result<String, io::Error> {
    fs::read_to_string(path)
}

fn main() -> Result<(), Box<dyn std::error::Error>> {
    let cfg = read_config("app.toml")?;
    println!("{cfg}");
    Ok(())
}
```

### Go-shaped comparison

```go
// Go
b, err := os.ReadFile(path)
if err != nil {
    return err
}
```

```rust
// Rust
let b = std::fs::read(path)?;
```

---

## Why Rust avoids exceptions for normal errors

1. **Control flow is visible in types** — function signatures document failure.  
2. **No hidden unwind** across library boundaries for routine errors.  
3. **Composable** — `map_err`, `and_then`, `?` chain cleanly.  
4. **`Option` ≠ error** — forces you to distinguish "not found" from "disk failed."

Ruby prefers developer happiness and rapid iteration: exceptions + `rescue` keep call sites clean until you care.

---

## Common pitfalls

| From | Pitfall | Fix |
|------|---------|-----|
| Java | Wanting checked exceptions in Rust | Use `Result` in signatures |
| Python | Bare `rescue` / `except` everything | Rescue specific classes; in Rust avoid `unwrap` in libs |
| Go | Ignoring `Result` with `let _ = ...` | Handle or propagate with `?` |
| All | Using `unwrap()` in library code | Return `Result`; `unwrap`/`expect` for demos & invariants |
| Ruby | Rescuing `StandardError` too broadly | Narrow; log context |

---

## Exercises

1. Convert a Ruby method that raises on bad input into a Rust function returning `Result`.  
2. When would Ruby use `nil` return instead of raising — and what is the Rust analogue?  
3. Why is `panic!` in a library considered unfriendly?

<details>
<summary>Solution sketch</summary>

1. Signature `Result<T, E>`; map validation failures to `Err`.  
2. Soft absence → `nil` / `Option::None`; hard failure → exception / `Result::Err`.  
3. Panics abort or unwind across caller boundaries unexpectedly; libraries should return `Result`.

</details>

---

## Try it yourself

Implement "parse port number from string" in both languages: invalid input should not crash the process in library code.

---

## Key takeaways

- Ruby: exceptions are normal control for errors; `nil` for absence.  
- Rust: `Result`/`Option` are normal; `panic!` is for bugs.  
- Go developers usually love Rust errors; Python/Java developers need a week to adjust.  
- Prefer idioms of the language you're in — don't write Java in Rust.

**Next:** [04-when-to-choose-which.md](./04-when-to-choose-which.md)
