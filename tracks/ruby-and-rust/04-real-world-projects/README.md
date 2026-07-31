# Real-World / Capstone Projects

These projects sit **above** the per-language mini projects. Do them after finishing at least one full curriculum (ideally both).

Each project lists:

- Suggested language(s)
- Skills exercised
- Stretch goals
- Links back to chapters

---

## Project catalog

### 1. Polyglot URL shortener

| | |
|--|--|
| **Languages** | Ruby (API) + optional Rust (hashing / redirect hot path) |
| **Skills** | HTTP APIs, persistence, error handling, deployment basics |
| **Ruby chapters** | Web, errors/testing, collections |
| **Rust chapters** | Result, structs, optional async |

**MVP:** `POST /shorten` → code; `GET /:code` → redirect. Store in SQLite or Redis.

**Stretch:** rate limits, analytics events, Rust microservice for redirects.

---

### 2. Log analysis CLI

| | |
|--|--|
| **Languages** | Prefer **Rust**; Ruby OK for prototype |
| **Skills** | Parsing, iterators/Enumerable, performance awareness |
| **Chapters** | Collections, error handling, ownership (Rust) |

**MVP:** read nginx/combined logs from stdin; print top paths and status code histogram.

**Stretch:** streaming large files, `--json` output, parallel shard processing.

---

### 3. Markdown notes SaaS (mini)

| | |
|--|--|
| **Languages** | **Ruby** (Sinatra or Rails) |
| **Skills** | CRUD, sessions/auth lite, testing |
| **Chapters** | Sinatra, RSpec, OOP |

**MVP:** signup-less notes with a secret token URL; markdown → HTML.

**Stretch:** full Rails, ActiveRecord, background jobs for link previews.

---

### 4. Concurrent link checker

| | |
|--|--|
| **Languages** | **Rust** (async) primary; Ruby Typhoeus/async comparison |
| **Skills** | Concurrency, timeouts, Result aggregation |
| **Chapters** | Async, errors, collections |

**MVP:** given a file of URLs, print status codes with a concurrency limit.

**Stretch:** compare wall-clock Ruby vs Rust; respect `robots.txt`.

---

### 5. Toy JSON config language

| | |
|--|--|
| **Languages** | Implement twice: Ruby then Rust |
| **Skills** | Parsing, enums/ADTs vs objects, good errors |
| **Chapters** | Metaprogramming (Ruby DSL), enums/match (Rust) |

**MVP:** support nested maps, arrays, comments, and line-numbered errors.

**Stretch:** format-preserving rewrite; WASM build of the Rust parser.

---

### 6. Team pick — production clone (scoped)

Pick a thin slice of a tool you use:

- Subset of `jq`  
- Subset of `make`  
- Subset of feature flags service  
- Subset of chat ops bot  

**Rule:** ship an MVP in two weeks max. Write a short ADR: why Ruby, Rust, or both.

---

## Capstone write-up template

When you finish, add `WRITEUP.md` to your fork:

```markdown
# Project: <name>
## Goal
## Language choice and why
## Architecture
## What was harder than expected
## What I'd do in production next
## Chapter skills used
```

---

## Learning path position

```text
Curriculum chapters → language projects/ → HERE → your production work
```

Return to comparison essays if you waffle on language choice:

- [Memory models](../03-comparing-ruby-and-rust/01-memory-models.md)  
- [When to choose which](../03-comparing-ruby-and-rust/04-when-to-choose-which.md)  

---

## Key takeaways

- Capstones test **judgment**, not just syntax.  
- Prefer a finished small system over an infinite framework.  
- Document tradeoffs — that's what seniors do.
