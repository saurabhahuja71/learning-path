# How to Study (For People Who Already Code)

## Learning objectives

- Use an efficient study loop designed for experienced engineers
- Avoid the two failure modes: passive reading and premature optimization of notes
- Know when to peek at solutions vs struggle productively

---

## The 45-minute loop

Experienced engineers learn languages by **pattern mapping**, not by memorizing syntax tables.

1. **Skim the comparison table** (2 min) — map to Java/Python/Go  
2. **Read the concept section** (10 min) — focus on *why*  
3. **Type every example** (15 min) — do not copy-paste the first time  
4. **Break it** (5 min) — change a type, remove a borrow, call a missing method  
5. **Do one exercise** (10 min) — without the solution  
6. **Write a 3-bullet summary** in your own words (3 min)

If a concept still feels foggy after one loop, **sleep on it** and re-run step 3–5 the next day. Ownership and metaprogramming especially reward spaced repetition.

---

## What *not* to do

| Anti-pattern | Why it fails |
|--------------|--------------|
| Only reading | You already read well; you need muscle memory for new error messages |
| Porting an entire Java service on day 2 | Too much domain noise; learn the language kernel first |
| Skipping exercises | Exercises force the awkward edges into view |
| Fighting the Rust compiler angrily | The compiler is the curriculum. Read the full error. |
| Treating Ruby as "Python with `end`" | Blocks, objects-everywhere, and the object model are different |

---

## Mapping from your home language

When you see a new construct, fill this template:

```text
In <Java|Python|Go> I would write: ...
In <Ruby|Rust> the idiomatic form is: ...
The tradeoff is: ...
```

Example:

```text
In Go I would write: if err != nil { return err }
In Rust the idiomatic form is: let x = fallible()?;
The tradeoff is: Rust's ? needs a compatible error type; Go is more verbose but uniform.
```

---

## When to use the solution files

- **After 15–20 minutes** of genuine attempt  
- **After** you've written a failing test or a compiler error you understand  
- Always **diff** your solution vs the official one — idiomatic style matters

---

## Spaced project work

Every 2–3 chapters, pause for a **mini project** in that language's `projects/` folder. Projects consolidate syntax into judgment:

- Which API is ergonomic?  
- Where do I put error boundaries?  
- What would I never do in production?

---

## Key takeaways

- Map, don't memorize.  
- Type, break, fix — that loop beats highlight reels.  
- The Rust compiler and Ruby's stack traces are teachers, not enemies.  
- Projects lock in chapters; chapters alone fade.

**Next:** start [ruby-from-scratch](https://github.com/saurabhahuja71/ruby-from-scratch) or [Rust-learning](https://github.com/saurabhahuja71/Rust-learning).
