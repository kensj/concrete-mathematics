# Concrete Mathematics — Solutions, Notes & Rust Implementations

This repository is where I’m working through my solutions, proofs, and notes for **_Concrete Mathematics_** by Graham, Knuth, and Patashnik — alongside Rust implementations for many of the identities, recurrences, and algorithms the book throws at me. The book doesn’t guide you gently; it hands you a shovel, points at a combinatorial hillside, and waits to see what you do with it. For me, this has become equal parts discipline, curiosity, and a quiet sharpening of the mind God entrusted to me.

The goals here:
- Develop clear, correct, well-motivated solutions.
- Keep the reasoning visible instead of pretending answers appear by revelation.
- Collect algebraic tricks and asymptotic instincts that make the next chapter easier to survive.
- Translate theory into practice by implementing selected ideas in Rust.
- Build foundations that actually matter in real CS work, not just the margins of a textbook.

If I say I want deep foundations, then this is where I prove it to myself.

## Project Structure

The Rust code lives under `src/`, and mirrors the structure of the book:

```
src/
  solutions/
    chapter_01/
      mod.rs        # implementations for chapter 1 problems
    mod.rs          # exposes all chapters + run_all()
  main.rs           # entry point
```

Each chapter is its own Rust module:

- `solutions/chapter_01/mod.rs` contains:
  - `run()` — a single function that executes all implemented problems for that chapter.
  - Individual helpers per problem (`problem_1()`, `problem_2()`, etc.)

You can run a single chapter or everything at once:

```rust
// main.rs
mod solutions;

fn main() {
    solutions::run_all();               // run everything
    // or: solutions::chapter_01::run(); // run just one chapter
}
```

As new chapters are added, each gets a `chapter_xx/mod.rs` and a small entry in `solutions/mod.rs`.

This keeps the math clean, the code organized, and the entire project easy to expand as I move through the book.

## Notes

This is not an official solution manual.  
It’s a workshop. Some proofs will get corrected, refactored, or resurrected after I realize the version I wrote at 1am needed more prayer and less confidence. Rust will keep me honest either way.

## License

MIT.  
Steal ideas responsibly, and may your sums converge and your Rust modules compile on the first try.
