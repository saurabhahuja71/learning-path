# Track: Ruby & Rust From Scratch

> For software engineers who already know **Java, Python, or Go**.  
> Full curricula live in dedicated repos; this folder is the **map + comparisons**.

Hub: **[learning-path](https://github.com/saurabhahuja71/learning-path)**

---

## Sister repositories

| Repository | What it teaches | GitHub |
|------------|-----------------|--------|
| **ruby-from-scratch** | Modern Ruby 3.2+: syntax, OOP, blocks, Enumerable, metaprogramming, RSpec, Sinatra | [saurabhahuja71/ruby-from-scratch](https://github.com/saurabhahuja71/ruby-from-scratch) |
| **Rust-learning** | Rust (edition 2021+): ownership, traits, Result/Option, iterators, async, smart pointers | [saurabhahuja71/Rust-learning](https://github.com/saurabhahuja71/Rust-learning) |

```bash
git clone https://github.com/saurabhahuja71/ruby-from-scratch.git
git clone https://github.com/saurabhahuja71/Rust-learning.git
```

---

## Suggested order

### Option A — Ruby first (most app engineers)

1. [00-setup/overview.md](./00-setup/overview.md) + [how-to-study.md](./00-setup/how-to-study.md)  
2. **[ruby-from-scratch](https://github.com/saurabhahuja71/ruby-from-scratch)** chapters 01–07 + projects  
3. Comparison essays below  
4. **[Rust-learning](https://github.com/saurabhahuja71/Rust-learning)** chapters 01–07 + projects  
5. [Capstones](./04-real-world-projects/README.md)

### Option B — Rust first (systems / performance)

1. Setup → **Rust-learning** through ownership + Result  
2. Finish Rust curriculum  
3. **ruby-from-scratch** for contrast  
4. Comparisons + capstones  

### Option C — Parallel (~10–12 weeks)

| Week | Ruby | Rust | Hub |
|------|------|------|-----|
| 1–2 | Basics + OOP | Ownership | Memory models |
| 3–4 | Blocks + Enumerable | Structs, traits | — |
| 5–6 | Testing + meta | Result + iterators | Errors |
| 7–8 | Sinatra + projects | Async + smart pointers | Concurrency |
| 9–12 | Capstone | Capstone | Choose Ruby vs Rust |

---

## Comparison essays (this folder)

| Doc | Topic |
|-----|--------|
| [01-memory-models.md](./03-comparing-ruby-and-rust/01-memory-models.md) | GC vs ownership |
| [02-concurrency-models.md](./03-comparing-ruby-and-rust/02-concurrency-models.md) | Threads, GVL, async, Tokio |
| [03-error-handling-philosophies.md](./03-comparing-ruby-and-rust/03-error-handling-philosophies.md) | Exceptions vs Result |
| [04-when-to-choose-which.md](./03-comparing-ruby-and-rust/04-when-to-choose-which.md) | Decision framework |
| [05-syntax-and-idioms-cheatsheet.md](./03-comparing-ruby-and-rust/05-syntax-and-idioms-cheatsheet.md) | Side-by-side syntax |
| [resources.md](./resources.md) | Books, docs, communities |
| [04-real-world-projects](./04-real-world-projects/README.md) | Capstone ideas |

---

## How to run examples

### Ruby

```bash
cd ruby-from-scratch
ruby 01-basics/examples/01_hello.rb
cd projects/cli-todo && bundle install && bundle exec ruby bin/todo.rb help
```

### Rust

```bash
cd Rust-learning
cd 01-ownership-and-borrowing/examples && cargo run --bin move_semantics
cd projects/cli-todo && cargo run -- list
```

---

## Key takeaways

- Ruby optimizes for **human time** and expressive APIs.  
- Rust optimizes for **correctness + performance** without a GC.  
- Learning both makes tradeoffs obvious — pick the tool for the job.

**Back to hub:** [learning-path README](../../README.md)

---

## Author

**Saurabh Ahuja** ([@saurabhahuja71](https://github.com/saurabhahuja71)) · Website: [www.onenova.in](http://www.onenova.in)
