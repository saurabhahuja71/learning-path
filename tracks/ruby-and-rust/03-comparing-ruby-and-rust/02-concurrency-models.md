# Concurrency Models

## Learning objectives

- Contrast Ruby's threading/GVL with Rust's fearless concurrency story
- Know when to use threads, processes, fibers, or async in each ecosystem
- Map models to Java executors, Python asyncio/GIL, and Go goroutines

---

## Concept

**Concurrency** = structure work so many tasks make progress.  
**Parallelism** = tasks actually run at the same time on multiple cores.

| Language | Default story |
|----------|----------------|
| **Ruby (MRI)** | Threads exist, but **GVL** means only one thread runs Ruby bytecode at a time; I/O can release GVL. For CPU parallelism: processes (or JRuby/TruffleRuby). Fibers + async gems for structured concurrency. |
| **Rust** | Threads are OS threads; **data races rejected at compile time**. Async (Tokio) for high-concurrency I/O with cooperative tasks. Channels, `Mutex`, `RwLock`, `Arc` are explicit. |

---

## Comparison table

| Model | Java | Python | Go | Ruby MRI | Rust |
|-------|------|--------|-----|----------|------|
| Lightweight tasks | Virtual threads (21+) | asyncio tasks | goroutines | Fibers / async | `async` tasks (Tokio) |
| OS threads | Yes | Yes (GIL) | Yes | Yes (GVL) | Yes |
| Shared memory | Common | Common | Common | Common | Controlled |
| Message passing | Queues | Queues | channels (idiomatic) | Queues / Ractors | `mpsc` / channels (idiomatic) |
| Data-race prevention | Discipline + tools | GIL papering | Discipline | GVL papering | Compiler |

---

## Mental model for Go engineers

Go: "share memory by communicating."  
Rust: same slogan, **enforced** — if you share, you wrap (`Arc`) and synchronize (`Mutex`) or you don't mutate.

```rust
use std::sync::mpsc;
use std::thread;

let (tx, rx) = mpsc::channel();
thread::spawn(move || {
    tx.send(42).unwrap();
});
assert_eq!(rx.recv().unwrap(), 42);
```

Ruby equivalent (threads + Queue):

```ruby
require "thread"
q = Queue.new
Thread.new { q << 42 }
puts q.pop  # => 42
```

---

## Mental model for Python engineers

Python asyncio ≈ Rust async **in shape** (event loop, await points), but Rust:

- Requires `Send`/`Sync` bounds for cross-thread tasks  
- Has no GIL — true multi-threaded async runtimes are normal  
- Color problem exists (`async` vs sync) but is explicit in types  

---

## When to pick what

| Workload | Ruby lean | Rust lean |
|----------|-----------|-----------|
| CRUD web, I/O bound | Puma threads / Fibers / Sidekiq processes | Tokio + hyper/axum |
| CPU-heavy parallel | Multi-process, native ext, or don't | `rayon`, threads |
| Huge connection count | Possible with right stack | Async shines |
| Simple scripts | Threads rarely needed | Threads rarely needed |

---

## Common pitfalls

1. **Assuming Ruby threads = parallel CPU** on MRI — usually not.  
2. **`async` everywhere in Rust** without need — threads are fine for many CLIs.  
3. **Holding a `Mutex` across `.await`** — deadlock risk; use care / `tokio::sync`.  
4. **Sharing Ruby objects across Ractors** without understanding isolation.  

---

## Exercises

1. Explain why a CPU-bound Fibonacci on 8 Ruby threads may not use 8 cores on MRI.  
2. Write a one-sentence rule for choosing `std::thread` vs `tokio::spawn`.  
3. Compare Go's goroutine scheduling to Tokio's work-stealing scheduler at a high level.

---

## Try it yourself

- Ruby: spawn 4 threads doing CPU work; time vs 4 processes.  
- Rust: same with threads; then with `rayon::join` if you add the crate later.

---

## Key takeaways

- Ruby concurrency is pragmatic and GC-friendly; true parallel Ruby often means multi-process.  
- Rust concurrency is explicit and compiler-checked; async is for scale of I/O, not mandatory for everything.  
- Message passing is idiomatic in both; Rust enforces the rules Go recommends.

**Next:** [03-error-handling-philosophies.md](./03-error-handling-philosophies.md)
