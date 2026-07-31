# Setup Overview

## Learning objectives

- Know which tools you need for Ruby vs Rust
- Install (or verify) both toolchains
- Understand how the three repositories fit together
- Run a "hello world" in each language

---

## The three-repo layout

```text
your-workspace/
├── learning-path/            # Hub — tracks/ruby-and-rust (comparisons + map)
├── ruby-from-scratch/        # Full Ruby curriculum
└── Rust-learning/            # Full Rust curriculum
```

GitHub:
- https://github.com/saurabhahuja71/learning-path  
- https://github.com/saurabhahuja71/ruby-from-scratch  
- https://github.com/saurabhahuja71/Rust-learning

| Repo | Setup guide |
|------|-------------|
| Ruby curriculum | [ruby-from-scratch setup](https://github.com/saurabhahuja71/ruby-from-scratch/blob/main/00-setup/ruby-setup.md) |
| Rust curriculum | [Rust-learning setup](https://github.com/saurabhahuja71/Rust-learning/blob/main/00-setup/rust-setup.md) |

---

## Quick verification

### Ruby

```bash
ruby -v    # expect 3.2+ (3.3/3.4 fine)
gem -v
bundle -v
```

Hello:

```bash
ruby -e 'puts "Hello from #{RUBY_VERSION}"'
```

### Rust

```bash
rustc --version   # edition 2021+ toolchain (1.70+ recommended)
cargo --version
```

Hello:

```bash
cargo new /tmp/hello-rust && cd /tmp/hello-rust && cargo run
```

---

## Editor recommendations

| Tool | Why |
|------|-----|
| **VS Code** + Ruby LSP / rust-analyzer | Best free default |
| **JetBrains RubyMine / RustRover** | Deep inspections |
| **Zed / Neovim** | Fast; wire LSP yourself |

Install language servers:

- Ruby: [Shopify Ruby LSP](https://github.com/Shopify/ruby-lsp) or Solargraph  
- Rust: `rust-analyzer` (comes with rustup component or editor extension)

---

## Comparison with languages you know

| Concern | Java | Python | Go | Ruby | Rust |
|---------|------|--------|----|------|------|
| Install | JDK + Maven/Gradle | pyenv + pip | go toolchain | rbenv/asdf + gem/bundler | rustup + cargo |
| Project file | pom.xml / build.gradle | pyproject.toml | go.mod | Gemfile | Cargo.toml |
| Package manager | Maven Central | PyPI | modules proxy | RubyGems | crates.io |
| Version manager | SDKMAN | pyenv | goenv (optional) | rbenv / asdf / chruby | rustup (built-in) |

---

## Common pitfalls (from Java / Python / Go)

1. **System Ruby is ancient** — macOS/Linux package Ruby may be 2.x. Use a version manager.  
2. **`cargo` not on PATH** — restart the shell after rustup; source `~/.cargo/env`.  
3. **Mixing global gems with project gems** — always prefer `bundle exec` in projects.  
4. **Expecting `go build` simplicity in Ruby** — Ruby is interpreted; packaging is different.  
5. **Skipping `rustup update`** — the ecosystem moves; keep the toolchain current.

---

## Try it yourself

1. Clone both curriculum repos as siblings of this hub.  
2. Complete the Ruby setup guide until `ruby -v` shows 3.2+.  
3. Complete the Rust setup guide until `cargo new` works.  
4. Bookmark [how-to-study.md](./how-to-study.md).

---

## Key takeaways

- This hub does **not** replace the language repos — it navigates them.  
- Version managers prevent "works on my machine" for Ruby; rustup is the equivalent for Rust.  
- Get both `ruby` and `cargo` green before starting chapter content.

**Next:** [how-to-study.md](./how-to-study.md) → then pick [ruby-from-scratch](https://github.com/saurabhahuja71/ruby-from-scratch) or [Rust-learning](https://github.com/saurabhahuja71/Rust-learning).
