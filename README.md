# KagLang

A JavaScript-inspired, statically typed language planned for native compilation.

**Status: language-design preview.** This repository contains specifications, illustrative examples and an implementation roadmap. There is no working compiler release yet, and no performance results are claimed. Existing JavaScript compatibility is not a goal for the first version.

## Design goals

- Familiar braces, functions and expressions, with inferred static types and optional annotations.
- A compiler written in Rust, using LLVM for ahead-of-time native code generation.
- Initial Linux amd64 and arm64 targets.
- Explicit conversions, defined arithmetic and bounds-checked collection access.
- Reproducible performance measurements covering compilation, startup, throughput and memory.

## Specification and implementation map

- [Language specification](docs/LANGUAGE.md): proposed syntax and semantics.
- [Compiler architecture](docs/ARCHITECTURE.md): stages, runtime and command interfaces.
- [Roadmap](docs/ROADMAP.md): ordered milestones and acceptance gates.
- [Testing and benchmarks](docs/TESTING.md): conformance and measurement requirements.
- [Illustrative examples](examples): proposed `.kag` programs; not currently executable.

Source implementation will use `crates/` for Rust compiler/runtime tools, `tests/` for conformance cases, `benchmarks/` for reproducible workloads, and `packaging/` for release definitions. Generated executables, caches and secrets will not be committed.

## Contributing

Discuss specification changes through GitHub issues and pull requests. Mark proposals as such; do not describe unimplemented syntax as supported. Implementation begins only after the corresponding language contract is accepted. See [CONTRIBUTING.md](CONTRIBUTING.md).

## License

Apache-2.0. This compiler/tooling license does not impose a license on programs compiled with KagLang. Third-party components retain their own licenses and notices; LLVM integration must retain its applicable notices.
