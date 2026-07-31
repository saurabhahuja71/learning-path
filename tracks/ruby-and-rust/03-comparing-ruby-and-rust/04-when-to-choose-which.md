# When to Choose Ruby vs Rust

## Learning objectives

- Apply a practical decision framework for real projects
- Recognize hybrid architectures (Ruby app + Rust extension/service)
- Avoid language fanaticism when shipping product

---

## The 30-second rule

| Choose **Ruby** when… | Choose **Rust** when… |
|------------------------|------------------------|
| You need features **this week** | You need **predictable latency** / low overhead |
| Domain is CRUD, admin, content, internal tools | Domain is systems, engines, parsers, data planes |
| Team velocity > raw CPU efficiency | Safety + performance are product requirements |
| Hiring generalists who love Rails | Hiring/training for systems discipline is OK |
| The bottleneck is product discovery | The bottleneck is CPU, memory, or concurrency correctness |

If both columns apply: **prototype in Ruby, extract hot paths to Rust**.

---

## Comparison to the languages you already use

| If you'd pick… | Also consider… |
|----------------|-----------------|
| **Rails / Django / Spring Boot** for a SaaS | Ruby (Rails) is a peer; Rust is rarely first for full SaaS |
| **Go** for a network service | Rust if you need richer types & no GC; Go if team speed + simplicity wins |
| **Java** for long-lived backend | Ruby for speed of change; Rust for native modules / edge services |
| **Python** for ML glue / scripts | Ruby for web/DSL joy; Rust for rewriting slow numeric/IO kernels |
| **C/C++** for embedded/hot path | Rust first for memory safety |

---

## Decision checklist

Score each 1–5 (higher = favors that side):

| Factor | Ruby | Rust |
|--------|------|------|
| Time-to-first-demo | ⭐⭐⭐⭐⭐ | ⭐⭐ |
| Runtime performance ceiling | ⭐⭐ | ⭐⭐⭐⭐⭐ |
| Memory predictability | ⭐⭐ | ⭐⭐⭐⭐⭐ |
| Fearless concurrency | ⭐⭐ | ⭐⭐⭐⭐⭐ |
| Metaprogramming / DSLs | ⭐⭐⭐⭐⭐ | ⭐⭐ |
| Ecosystem for HTML apps | ⭐⭐⭐⭐⭐ | ⭐⭐⭐ |
| WASM / embedded | ⭐ | ⭐⭐⭐⭐⭐ |
| Library for niche scientific ML | ⭐⭐ | ⭐⭐⭐ (growing) |

---

## Real architectures that work

1. **Rails monolith + Rust microservice** for PDF rendering, image pipelines, or policy engines  
2. **Ruby CLI** wrapping a **Rust core** via FFI or subprocess (great DX + speed)  
3. **Sinatra/Roda API** for orchestration; **Rust** for websocket fanout  
4. **All Rust** for CLIs (`ripgrep`-class tools)  
5. **All Ruby** for internal admin + Sidekiq — ship and sleep

---

## Anti-patterns

- Rewriting a stable Rails app into Rust "for performance" without a profile  
- Starting a vague startup MVP in pure Rust because HN said so  
- Using Ruby for a multiplayer simulation server expecting C++ speeds  
- Ignoring ops: a slow language well-cached beats a fast language poorly deployed  

---

## Exercises

1. Pick a system you know. Argue for Ruby *and* for Rust in one paragraph each.  
2. Identify one component that would benefit from a Rust rewrite and one that would not.  
3. Draft a hybrid boundary (API contract or gem/crate split).

---

## Try it yourself

Take the CLI todo projects from both curricula. Time implementing a new feature (e.g. tags) in each. Note which felt faster *for you* and which runtime would matter at 10M tasks.

---

## Key takeaways

- Language choice is **product + team + workload**, not tribal identity.  
- Ruby optimizes for **human time**. Rust optimizes for **machine constraints + correctness**.  
- Hybrids are professional, not impure.  
- Measure before you rewrite.

**Next:** [05-syntax-and-idioms-cheatsheet.md](./05-syntax-and-idioms-cheatsheet.md)
