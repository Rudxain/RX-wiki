# Reduced Axiom Language
A **Reduced Axiom Set Language** or **Minimal Axiom System Lang**, is a lang that's specified in terms of a minimal (not necessarily the absolute minimum) amount of simple axioms. Such langs tend to define most of their core/standard libraries in the language itself, rather than being opaque implementations.

Another definition is that these langs have an axiom-to-construct ratio very close to 0, implying they have many features derived from a small set of axioms.

## Examples
- Rust: [Tris explains it better than me](https://github.com/0atman/noboilerplate/blob/main/scripts/32-rust-is-written-in-rust.md) ([video](https://youtu.be/v6RxJsk8otY))
- Gleam: [`Bool`](https://github.com/gleam-lang/gleam/discussions/1026#discussioncomment-598813)
- Ada: lookup its `Integer` def.

## Non-examples
- JavaScript/TypeScript and CoffeeScript
- Python
- Java (I guess?)

## Criticism
> But you're not talking about the specification! You're referring to the implementation!

The concept of RASL is fuzzy and context-sensitive, and thereby open to interpretation.
