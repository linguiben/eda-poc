# EDA Requirements Summary (v1)

Source: `docs/input/eda_requirements_v1.txt` (contains character-encoding corruption; items below reflect directly readable content plus constrained inference).

## 1) Scope and Objective
- Build an EDA PoC oriented to advanced-node CPU design workflows.
- Primary node focus: `3nm` with references to `GAA` and future `2nm` extensibility.
- Target domains explicitly mentioned: CPU, memory (DRAM/NAND/HBM), and AI-assisted optimization.

## 2) Core Functional Requirements
- End-to-end RTL-to-GDS flow support:
  - HDL handling: `Verilog`, `VHDL`.
  - Signoff/verification checks: `DRC`, `LVS`, `ERC`, `STA`, and `DFM`.
  - Data exchange/formats: `GDSII`, `SPICE`, `PDF` outputs (plus general report artifacts).
- CPU architecture coverage:
  - `RISC-V`, `ARMv8`, `x86-64` called out.
- Memory-related support:
  - `DRAM`/`DDR5`, `NAND Flash`/`3D NAND`, `HBM`/`HBM3` referenced.
- AI-enabled capabilities:
  - AI model-assisted optimization and analysis workflows.
  - References to model families/frameworks (e.g., `OpenAI GPT`, `NVIDIA Nemotron`, `CNN/GNN`) as exploratory support.

## 3) Performance and Quality Targets
- 3nm CPU flow efficiency/performance improvements are emphasized.
- Accuracy and signoff-quality constraints appear in timing/verification sections.
- Large design handling and runtime constraints are specified in benchmark-like terms.

### Clearly Labeled Estimates
- [Estimate] End-to-end runtime target for one full advanced-node flow: `~72 hours` (inferred from acceptance/performance sections).
- [Estimate] Improvement goals repeatedly implied: `~30%` runtime/efficiency gain in key steps.
- [Estimate] Additional quality uplift target from AI-assisted tuning: `~10%` class improvements in selected PPA/verification metrics.
- [Estimate] Timing analysis precision target: `~1 ps` granularity.
- [Estimate] DRC/LVS/ERC throughput target for `100 mm^2` class design: `<= 48 hours`.

## 4) Platform and Environment Requirements
- OS:
  - `Windows 10/11` (64-bit)
  - `Linux Ubuntu 20.04` (64-bit)
- Runtime/toolchain:
  - `Java 11+`, `Python 3.8+`
  - compiler/sim tools referenced: `GCC`, `Clang`, `ModelSim`, `VCS`
- Baseline hardware references in source:
  - CPU class around `Intel i7-12700H` / `AMD Ryzen 7 5800H`
  - memory and storage baselines/targets include `8GB` (min signal), `64GB` (higher-tier signal), and `2TB` storage.

### Clearly Labeled Estimates
- [Estimate] Practical PoC workstation for stable execution: `>=16 vCPU`, `>=64GB RAM`, `>=2TB NVMe`.
- [Estimate] GPU support likely needed for AI acceleration: `>=1 x NVIDIA RTX 3090 class` if local inference is required.

## 5) Interoperability and Ecosystem
- Integration references include major EDA ecosystems (`Synopsys`, `Cadence`) for compatibility context.
- Standards/protocol references include `IEEE 1076` and `IEEE 1364` (HDL-related).

## 6) Risk and Constraints
- Source quality risk: input document text is partially corrupted; some requirements are semantically ambiguous.
- Technical risk: advanced-node signoff fidelity and runtime targets are aggressive for a PoC.
- Dependency risk: external toolchain/licensing and PDK availability are likely critical path items.

### Clearly Labeled Estimates
- [Estimate] Requirement ambiguity risk impact: `medium-high` until cleaned source text and acceptance criteria are re-baselined.
- [Estimate] Delivery confidence before clarification: `~60%` for full-scope PoC, `~80%` for narrowed MVP.

## 7) Assumptions Used in This Summary
- Numeric values (`72h`, `48h`, `30%`, `10%`, `1ps`, `100mm^2`) are taken from legible fragments and mapped to nearby sections.
- Some section titles and sentence intent were reconstructed from mixed Chinese/garbled text and English technical terms.
- This summary prioritizes preserving explicit terms over speculative expansion.
