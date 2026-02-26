# Research Notes: EDA PoC Requirements v1

Source reviewed: `docs/input/eda_requirements_v1.txt`

## 1) Document Readability Notes
- The source text shows significant encoding/OCR corruption.
- Technical keywords remain recoverable and internally consistent across pages.
- Directly legible anchors include:
  - process nodes: `3nm`, `2nm`, `FinFET`, `GAA`
  - flow checks: `DRC/LVS/ERC/STA/DFM`
  - design artifacts: `Verilog`, `VHDL`, `GDSII`, `SPICE`
  - architecture/memory: `RISC-V`, `ARMv8`, `x86-64`, `DDR5`, `HBM3`, `3D NAND`

## 2) Interpreted Product Intent
- Primary intent appears to be an advanced-node CPU-centric EDA flow demonstrator.
- Scope is broader than pure CPU logic:
  - memory subsystem modeling/constraints are repeatedly mentioned.
  - AI methods are treated as integral optimization support, not optional tooling.
- Requirements blend classic deterministic signoff methods with AI-assisted exploration.

## 3) Recoverable Quantitative Signals
- Multiple numeric constraints/goals appear repeatedly and plausibly map to KPIs.

### Clearly Labeled Estimates
- [Estimate] Throughput goal: one complete run in `~72h` for a representative 3nm CPU-class case.
- [Estimate] Verification throughput: `100 mm^2` DRC/LVS/ERC turnaround in `<=48h`.
- [Estimate] Improvement targets: `~30%` efficiency gain and `~10%` incremental quality uplift.
- [Estimate] Timing precision objective: `1 ps` scale.

## 4) Capability Clusters Identified
- Signoff correctness cluster:
  - rule/consistency checks and timing/EM/IR-style closure concerns are explicitly implied.
- Platform compatibility cluster:
  - multi-OS operation and heterogeneous toolchain support.
- AI enablement cluster:
  - model-assisted search/optimization and prediction layers over classic EDA tasks.
- Interoperability cluster:
  - compatibility with incumbent EDA ecosystems and standard interchange formats.

## 5) Feasibility Observations (Preliminary)
- Technically feasible as a staged PoC if scope is constrained to:
  - one architecture (e.g., RISC-V)
  - one representative design size band
  - a small number of signoff metrics with measurable baselines.
- Full stated breadth (multi-architecture + full memory depth + AI + aggressive runtime targets) is likely beyond a single-phase PoC.

### Clearly Labeled Estimates
- [Estimate] MVP feasibility window (small team): `10-14 weeks`.
- [Estimate] Expanded v1 scope feasibility window: `6-9 months`.
- [Estimate] Clarification effort needed due to source corruption: `1-2 weeks` requirements clean-up.

## 6) Open Questions Blocking High-Confidence Planning
- What exact acceptance thresholds define PPA success per architecture?
- Which checks are mandatory in PoC signoff versus deferred to later phases?
- Is AI inference expected local/on-prem only, or hybrid with remote services?
- What PDK/legal constraints apply to any 3nm collateral in this PoC?
- Which external commercial tools are assumed available under license?

## 7) Recommended Next Data Collection
- Acquire clean-source version (or native editable file) of requirements.
- Build a KPI table with explicit formulas and pass/fail thresholds.
- Define one fixed benchmark design and dataset to anchor comparisons.
- Freeze dependency matrix (PDK, tool licenses, compute profile) before implementation.
