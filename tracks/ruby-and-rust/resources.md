# Resources

Curated for engineers who already know Java, Python, or Go. Prefer primary docs and a few battle-tested books over infinite blog hopping.

---

## Official docs

| Resource | Link |
|----------|------|
| Ruby language docs | https://www.ruby-lang.org/en/documentation/ |
| Ruby core API | https://docs.ruby-lang.org/en/ |
| Ruby style guide | https://rubystyle.guide/ |
| Rust book (official) | https://doc.rust-lang.org/book/ |
| Rust by Example | https://doc.rust-lang.org/rust-by-example/ |
| Rust std docs | https://doc.rust-lang.org/std/ |
| Cargo book | https://doc.rust-lang.org/cargo/ |
| Tokio tutorial | https://tokio.rs/tokio/tutorial |

---

## Books worth buying

### Ruby

- **Practical Object-Oriented Design in Ruby (POODR)** — Sandi Metz  
- **Metaprogramming Ruby 2** — Paolo Perrotta  
- **Eloquent Ruby** — Russ Olsen  

### Rust

- **The Rust Programming Language** (free online, also print)  
- **Programming Rust** (O'Reilly) — Blandy, Orendorff, Tindall  
- **Rust for Rustaceans** — Jon Gjengset (after intermediate)  
- **Async Rust** materials via Tokio + *Asynchronous Programming in Rust* (evolving)

---

## Practice & community

| Place | Why |
|-------|-----|
| https://exercism.org/tracks/ruby | Mentored exercises |
| https://exercism.org/tracks/rust | Mentored exercises |
| https://www.ruby-lang.org/en/community/ | Mailing lists, Discord links |
| https://users.rust-lang.org/ | Official users forum |
| r/ruby, r/rust | Casual Q&A (verify advice) |
| This Week in Rust | Weekly ecosystem digest |

---

## From your language → here

| Background | Helpful bridge |
|------------|----------------|
| Java | Ruby: think "Smalltalk + Perl practicality." Rust: think "C++ correctness without the footguns + ADTs." |
| Python | Ruby: similar dynamism, different object model & blocks. Rust: iterators feel like generators on steroids; ownership is new. |
| Go | Ruby: richer OOP, less "one way." Rust: `Result`/`?` ≈ err checks; no GC; traits ≈ interfaces with superpowers. |

---

## Related repos in this learning path

- Website: [www.onenova.in](http://www.onenova.in)  
- [learning-path](https://github.com/saurabhahuja71/learning-path) — main hub  
- [tracks/ruby-and-rust](./README.md) — this track map  
- [ruby-from-scratch](https://github.com/saurabhahuja71/ruby-from-scratch) — Ruby curriculum  
- [Rust-learning](https://github.com/saurabhahuja71/Rust-learning) — Rust curriculum  

---

## Staying current

- Ruby: follow Ruby core release notes (3.2 → 3.3 → 3.4 features like YJIT defaults, Prism parser)  
- Rust: follow edition guides; prefer stable over nightly unless a chapter says otherwise  
- Re-run `rustup update` and `gem update --system` periodically  

When in doubt, **official docs > random Medium posts**.
