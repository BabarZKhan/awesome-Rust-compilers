# awesome-Rust-SSA-IRs

A curated list of Rust compiler infrastructure, SSA-based intermediate representations (IR), and code-generation backends. This list collects projects relevant to building compilers in Rust: native IR frameworks, MLIR/LLVM bindings, register allocators, GPU, and formal verification tooling.

## Rust Compiler Internals (rustc ecosystem)

- [rust](https://github.com/rust-lang/rust): The Rust language compiler and standard library itself.
- [project-stable-mir](https://github.com/rust-lang/project-stable-mir):Effort to provide a stable API to rustc's MIR for external tools.
- [rustc_codegen_cranelift](https://github.com/rust-lang/rustc_codegen_cranelift):Alternative rustc backend using Cranelift instead of LLVM (faster debug builds).
- [chalk](https://github.com/rust-lang/chalk): Trait-solving engine (logic/Prolog-style) for Rust's type system.
- [polonius](https://github.com/rust-lang/polonius): Next-gen borrow checker based on datalog-style analysis.
- [a-mir-formality](https://github.com/rust-lang/a-mir-formality): Formal model/specification of Rust's type system and MIR.
- [miri](https://github.com/rust-lang/miri/): Interpreter for MIR; detects UB and runs Rust without native codegen.

## MLIR / LLVM Bindings

- [melior](https://github.com/mlir-rs/melior): Safe, idiomatic Rust bindings to MLIR.
- [mlir-sys](https://github.com/mlir-rs/mlir-sys): Raw FFI (unsafe C) bindings to MLIR.
- [mlir-rs](https://github.com/conradludgate/mlir-rs): Another Rust MLIR binding effort.
- [inkwell](https://github.com/TheDan64/inkwell): Safe, idiomatic Rust wrapper over the LLVM C API.
- [llvm-ir](https://github.com/cdisselkoen/llvm-ir): Library for parsing/analyzing LLVM IR in pure Rust (read-only).

## Native Rust IR Frameworks

- [pliron](https://github.com/pliron-org/pliron): Rust-native, MLIR-style extensible IR framework with custom dialects.
- [sonatina](https://github.com/fe-lang/sonatina): SSA-based IR and optimizing backend (from the Fe language project).
- [lift](https://github.com/rustnew/lift): Rust IR/compiler infrastructure project.
- [llhd](https://github.com/fabianschuiki/llhd): Low-level hardware description IR (multi-level IR for hardware).
- [roto](https://github.com/NLnetLabs/roto): Scripting language compiler/runtime from NLnet Labs.

## Code-Generation Backends

- [wasmtime](https://github.com/bytecodealliance/wasmtime): WebAssembly runtime; home of the Cranelift codegen backend.
- [regalloc2](https://github.com/bytecodealliance/regalloc2): Standalone SSA-based register allocator (used by Cranelift).
- [isle](https://github.com/cfallin/isle): DSL for writing instruction-selection/lowering rules (used in Cranelift).
- [rustc_codegen_clr](https://github.com/FractalFir/rustc_codegen_clr): rustc backend targeting .NET CLR / CIL bytecode.

## GPU / SPIR-V / CUDA

- [rust-gpu](https://github.com/Rust-GPU/rust-gpu): Compile Rust directly to SPIR-V shaders.
- [spirt](https://github.com/EmbarkStudios/spirt): SPIR-V intermediate/transformation IR (Embark original; also mirrored under [rust-gpu/spirt](https://github.com/rust-gpu/spirt)).
- [Rust-CUDA](https://github.com/Rust-GPU/Rust-CUDA): Toolchain for writing/running CUDA GPU code in Rust.
- [cuda-oxide](https://github.com/NVlabs/cuda-oxide): Safe Rust wrapper over the CUDA driver API.

## HLS / Hardware Synthesis

- [calyx](https://github.com/calyxir/calyx): Intermediate language and infrastructure for hardware accelerator (HLS) compilers.
- [rust_hls](https://github.com/zebreus/rust_hls): High-level synthesis from Rust to hardware.

## Formal Verification & Model Checking

- [CompCert](https://github.com/AbsInt/CompCert): Formally verified C compiler (proven correct in Coq).
- [charon](https://github.com/AeneasVerif/charon). Extracts Rust (via MIR) into a format for formal verification (Aeneas project).
- [kani](https://github.com/model-checking/kani): Bit-precise model checker for Rust (verifies properties, finds UB).

## E-Graphs / Optimization

- [egg](https://github.com/egraphs-good/egg): E-graph library for equality saturation and term rewriting/optimization.

## Language Compilers (built in/with Rust)

- [gleam](https://github.com/gleam-lang/gleam): Statically-typed language for the BEAM (Erlang VM) and JS.
- [move](https://github.com/move-language/move): Smart-contract language (originally Diem/Libra).
- [SEMAPRAX](https://wavect.io/semaprax/): Experimental pre-alpha systems language and compiler built in Rust around stable semantic identities and a versioned program graph ([source](https://github.com/wavect/semaprax)).
- [sway](https://github.com/FuelLabs/sway): Smart-contract language for the Fuel blockchain.
- [noir](https://github.com/noir-lang/noir): Domain-specific language for zero-knowledge proofs.
- [fe](https://github.com/argotorg/fe) — Smart-contract language for the EVM (uses sonatina as backend).
- [solang](https://github.com/hyperledger-solang/solang) — Solidity compiler built on LLVM (Hyperledger).
- [cairo_native](https://github.com/starkware-libs/cairo_native) — Compiles StarkNet's Cairo language to native code via MLIR.
