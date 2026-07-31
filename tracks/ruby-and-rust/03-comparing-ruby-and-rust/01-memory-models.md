# Memory Models: GC vs Ownership

## Learning objectives

- Explain how Ruby manages memory (GC) vs how Rust does (ownership + drops)
- Map both models to Java, Python, and Go mental models
- Predict when each model helps or hurts latency, throughput, and safety

---

## Concept (plain English)

**Ruby** (like Java, Python, Go) uses a **garbage collector**. You allocate objects freely; a runtime periodically finds unreachable objects and reclaims them. You almost never free memory by hand.

**Rust** has **no GC**. Every value has exactly one **owner**. When the owner goes out of scope, Rust **drops** the value (runs destructors, frees heap memory). The compiler enforces rules so you cannot use freed memory, double-free, or data-race on shared mutable state.

```text
Ruby:  "I'll clean up later when nothing points at this object."
Rust:  "This variable owns the data. When the variable dies, the data dies. Borrow if you need temporary access."
```

---

## Comparison table

| Aspect | Java | Python | Go | Ruby | Rust |
|--------|------|--------|----|------|------|
| Primary strategy | GC (G1/ZGC…) | GC (ref count + cyclic) | GC (tricolor) | GC (mark-sweep / incremental) | Ownership + RAII drops |
| Manual free? | No (almost) | No | No | No | Rarely (`unsafe`, raw ptrs) |
| Use-after-free | Prevented by GC | Prevented by GC | Prevented by GC | Prevented by GC | Prevented by borrow checker |
| Pause risk | GC pauses (tunable) | GC pauses | GC pauses | GC pauses | No GC pauses (drops are local) |
| Shared mutability | Easy, racy without locks | Easy, GIL hides some pain | Easy with care | Easy, GVL limits true parallel Ruby threads | Hard by default — must opt in (`Mutex`, `Arc`) |
| Mental cost | Low day-to-day | Low | Low | Low | Higher compile-time cost |

---

## Side-by-side sketches

### Ruby — allocate freely

```ruby
def build_report
  rows = (1..10_000).map { |i| { id: i, body: "row-#{i}" } }
  rows.select { |r| r[:id].even? }
  # `rows` and intermediate arrays become garbage when nothing references them.
  # GC reclaims later — not necessarily when this method returns.
end
```

### Rust — ownership is explicit

```rust
fn build_report() -> Vec<(u32, String)> {
    let rows: Vec<(u32, String)> = (1..=10_000)
        .map(|i| (i, format!("row-{i}")))
        .collect();
    // `rows` is moved into the filter pipeline / new vec, or dropped at end of scope.
    rows.into_iter().filter(|(id, _)| id % 2 == 0).collect()
} // any locals still owned here are dropped now
```

### What Go engineers notice

Go: `make` + GC, escape analysis decides stack vs heap.  
Rust: you *feel* heap allocation (`Box`, `Vec`, `String`) and moves more directly. No GC, but also no "I forgot who owns this channel payload."

### What Java engineers notice

Java: references everywhere, finalizers discouraged, try-with-resources for non-memory resources.  
Rust: **Drop** is like a reliable, compiler-ordered destructor for *all* resources (memory, files, locks). `Drop` runs deterministically at scope end.

---

## Why Rust is strict (the "why")

GC languages solve memory safety by **runtime bookkeeping**. Rust solves it by **static proof**:

1. Each value has one owner.  
2. You may have many immutable borrows **or** one mutable borrow — not both.  
3. Borrows cannot outlive the owner (lifetimes).  

Cost: fight the compiler early. Benefit: no use-after-free, fewer data races, predictable latency.

---

## Common pitfalls for GC veterans

| Pitfall | Reality |
|---------|---------|
| "Rust will free when nothing references it" | No — ownership drops at scope end; cycles need `Weak` |
| "Clone everything to silence the compiler" | Compiles, but may be slow/wrong; prefer borrows |
| "Ruby has no memory issues" | Leaks via forgotten caches, unbounded queues, native extensions |
| "Rust is always faster" | Often, but naive clones or locks can lose to a tuned GC app |

---

## Exercises

1. In Ruby, create a large array inside a method and return only its length. When might the array be collected?  
2. In Rust, write a function that takes `&str` and returns a new `String`. Why doesn't the input need to be moved?  
3. Explain why `Arc<Mutex<T>>` appears in multi-threaded Rust but almost never in Ruby web apps.

<details>
<summary>Hints / solution pointers</summary>

1. After the method returns and no references remain; exact time is GC-dependent.  
2. `&str` is a borrow — caller keeps ownership; you only read.  
3. Rust allows true parallel mutable sharing only with synchronization + shared ownership; Ruby MRI's GVL and GC world make simpler sharing common (with different tradeoffs).

</details>

---

## Try it yourself

- Ruby: write a loop that allocates 1M short-lived strings; watch memory with a simple RSS print.  
- Rust: write the same with `String::from` in a loop vs reusing a buffer — feel the difference in intent.

---

## Key takeaways

- Ruby = GC comfort (like Java/Python/Go); think about *object graphs* and caches.  
- Rust = ownership + drops; think about *who owns this and for how long*.  
- Neither free lunch: GC pauses vs compile-time friction.  
- Resource management (files, sockets) is more uniform in Rust via `Drop`.

**Next:** [02-concurrency-models.md](./02-concurrency-models.md)
