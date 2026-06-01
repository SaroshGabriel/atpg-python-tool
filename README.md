# atpg-python-tool

> **Status: planned / in progress.** This repo is a placeholder on the DFT
> roadmap. A working stuck-at fault simulator + coverage tool already exists in
> [`dft-fundamentals/atpg`](https://github.com/SaroshGabriel/dft-fundamentals);
> this repo will grow it into a standalone, packaged ATPG tool.

A Python **Automatic Test Pattern Generation** tool for combinational logic.

## Planned scope

- Stuck-at fault model (SA0/SA1) with structural fault collapsing
- Test-pattern generation (D-algorithm / PODEM)
- Fault simulation + **fault-coverage** grading
- Minimal test-set derivation
- Read a simple gate-level netlist; emit a pattern set

## Background already done

See [`dft-fundamentals/atpg/fault_simulator.py`](https://github.com/SaroshGabriel/dft-fundamentals/blob/main/atpg/fault_simulator.py)
— SA0/SA1 modeling, fault detection by propagation to a primary output,
coverage computation, and minimal detecting set on a small AND→OR circuit.

## Roadmap

| Stage | Status |
|-------|--------|
| Fault model + coverage (prototype) | ✅ in `dft-fundamentals` |
| Netlist parser | ⬜ |
| Pattern generation (PODEM) | ⬜ |
| Packaging / CLI | ⬜ |
