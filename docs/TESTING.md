# Conformance, security and performance

Test each language rule with accepted and rejected programs, stable diagnostic identifiers and source-span checks. Add parser fuzzing, resource bounds for hostile inputs, path/import traversal tests and deterministic module resolution.

Test runtime integer boundaries, NaN/infinity, zero division, UTF-8, collection bounds, nested managed records/arrays, repeated allocations and all cleanup paths. Compare O0/O2 outputs. Run memory sanitizers and leak checks against supported native targets; record unsupported combinations honestly.

Benchmarks must publish complete source, compiler/runtime versions, flags, CPU/OS, warmup, repetitions, median and spread. Report compilation time, executable startup, runtime throughput, peak memory and binary size separately. Compare with optimized Rust/C and pinned JavaScript engines using equivalent work and observable results that prevent dead-code elimination. Report slower results as well as faster ones. A microbenchmark does not establish universal superiority.

Packaging requires named top-level directories, applicable licenses, normalized metadata, checksums, signed manifests and clean-checkout builds. Preserve source availability. Do not publish empty binaries or placeholders as stable compiler releases.
