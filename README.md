# atpg-python-tool

> A Python **Automatic Test Pattern Generation** tool for combinational logic.
> Roadmap repo — grows the working fault simulator from `dft-fundamentals` into a
> standalone, packaged ATPG tool.

![Status](https://img.shields.io/badge/status-planned-blue)
![Focus](https://img.shields.io/badge/focus-ATPG-1f6feb)
![Python](https://img.shields.io/badge/Python-3-3776ab?logo=python&logoColor=white)
![Prototype](https://img.shields.io/badge/prototype-in%20dft--fundamentals-2ea043)

> **Status: planned.** A working stuck-at fault simulator + coverage tool already
> exists in [`dft-fundamentals/atpg`](https://github.com/SaroshGabriel/dft-fundamentals);
> this repo will package and extend it into a real ATPG tool.

---

## Goal

Take a gate-level circuit and automatically generate a compact set of test
patterns that detect manufacturing faults — then report the fault coverage.

## Planned Scope

- Stuck-at fault model (SA0/SA1) with structural fault collapsing
- Test-pattern generation (D-algorithm / PODEM)
- Fault simulation + **fault-coverage** grading
- Minimal test-set derivation
- Read a simple gate-level netlist; emit a pattern set

## Already Working (in dft-fundamentals)

The prototype this builds on:
[`dft-fundamentals/atpg/fault_simulator.py`](https://github.com/SaroshGabriel/dft-fundamentals/blob/main/atpg/fault_simulator.py)
— SA0/SA1 modeling, fault detection by propagation to a primary output, coverage
computation, and minimal detecting set on a small AND→OR circuit (currently by
exhaustive search; PODEM is the upgrade this repo targets).

## Roadmap

| Stage | Status |
|-------|--------|
| Fault model + coverage (prototype) | ✅ in `dft-fundamentals` |
| Netlist parser | ⬜ |
| Pattern generation (PODEM) | ⬜ |
| Packaging / CLI | ⬜ |

## Related

- [`dft-fundamentals`](https://github.com/SaroshGabriel/dft-fundamentals) — the foundations + working prototype
- [`dft-readiness-checker`](https://github.com/SaroshGabriel/dft-readiness-checker) — pre-scan netlist checks
- [`openroad-dft-flow`](https://github.com/SaroshGabriel/openroad-dft-flow) — where generated patterns plug into a real flow

## Author

**Sarosh (KJ)** · [github.com/SaroshGabriel](https://github.com/SaroshGabriel) · saroshjibreel@gmail.com
