# Syntax & Idioms Cheatsheet

Quick side-by-side reference. Details live in each curriculum repo.

---

## Hello & entry points

| | Ruby | Rust |
|--|------|------|
| Run file | `ruby app.rb` | `cargo run` |
| Entry | top-level script | `fn main()` |
| Print | `puts "hi"` | `println!("hi")` |

---

## Variables & mutability

```ruby
name = "Ada"       # reassignable by default
name = "Grace"
COUNT = 10         # constant (convention + warning)
```

```rust
let name = "Ada";           // immutable binding
let mut count = 0;          // explicit mut
count += 1;
const MAX: u32 = 10;        // compile-time constant
```

---

## Functions / methods

```ruby
def add(a, b) = a + b   # endless method (3.0+)
```

```rust
fn add(a: i32, b: i32) -> i32 { a + b }
```

---

## Collections

| Idea | Ruby | Rust |
|------|------|------|
| Growable list | `Array` | `Vec<T>` |
| Map | `Hash` | `HashMap<K,V>` |
| Iterate | `each`, `map` | `.iter()`, `.map()` |
| Chaining | Enumerable | Iterator adapters |

```ruby
[1, 2, 3].map { |x| x * 2 }.select(&:even?)
```

```rust
vec![1, 2, 3].into_iter().map(|x| x * 2).filter(|x| x % 2 == 0).collect::<Vec<_>>()
```

---

## Null / absence

| Ruby | Rust | Python | Go | Java |
|------|------|--------|-----|------|
| `nil` | `Option<T>` | `None` | zero / ok | `null` / `Optional` |

```ruby
user&.name || "guest"
```

```rust
user.as_ref().map(|u| u.name.as_str()).unwrap_or("guest");
```

---

## Errors

```ruby
begin
  risky!
rescue SomeError => e
  warn e.message
end
```

```rust
match risky() {
    Ok(v) => v,
    Err(e) => { eprintln!("{e}"); return; }
}
// or: let v = risky()?;
```

---

## OOP-ish shapes

| Idea | Ruby | Rust |
|------|------|------|
| Nominal type | `class` | `struct` + `impl` |
| Interface | `Module` as mixin / duck typing | `trait` |
| Inheritance | single + mixins | no inheritance of data; traits |
| Constructor | `initialize` | `::new` convention |

---

## Concurrency one-liners

```ruby
Thread.new { do_work }
```

```rust
std::thread::spawn(|| do_work());
```

---

## Project files

```ruby
# Gemfile
source "https://rubygems.org"
gem "sinatra"
```

```toml
# Cargo.toml
[package]
name = "demo"
edition = "2021"
```

---

## Idiom reminders

- Ruby: prefer **clarity and blocks**; monkey patch sparingly.  
- Rust: prefer **borrows over clones**; `unwrap` only when panic is correct.  
- Both: small pure functions + thin I/O boundaries age well.

For deep dives, return to the language repos:

- [ruby-from-scratch](https://github.com/saurabhahuja71/ruby-from-scratch)  
- [Rust-learning](https://github.com/saurabhahuja71/Rust-learning)
