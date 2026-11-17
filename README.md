# Quantum Spectra and Arithmetic L-Functions

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Python 2.7](https://img.shields.io/badge/Python-2.7-green.svg)](https://www.python.org/)
[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.24296284.svg)](https://doi.org/10.5281/zenodo.24296284)

## Overview
A deterministic, zero-dependency Python 2.7 computational research suite modeling **Floquet-engineered trapped-ion realizations of Berry–Keating dilation dynamics** whose quasienergy spectra mirror the non-trivial zeros of the Riemann zeta function $\zeta(\frac{1}{2} + i\gamma_n)$ and higher arithmetic $L$-functions.

This repository accompanies the manuscript *"Analogue Quantum Spectra and Arithmetic L-Functions: Floquet-Engineered Trapped-Ion Realizations of Berry–Keating Dynamics with Deterministic Verification"*.

## Repository Structure
* `berry_keating_floquet_model.py` — Core Berry–Keating operator initialization and Floquet quasienergy spectral matcher.
* `step1_level_spacing_stats.py` — Unfolded nearest-neighbor level-spacing analyzer verifying Gaussian Unitary Ensemble (GUE) level repulsion.
* `step2_spectral_rigidity.py` — Long-range Dyson–Mehta $\Delta_3(L)$ spectral rigidity calculator.
* `step3_trapped_ion_noise.py` — Experimental ion-trap thermal heating and laser phase decoherence simulator.
* `quantum_spectra_floquet_riemann.tex` — Complete LaTeX research manuscript.
* `CITATION.cff` — Standard Citation File Format metadata.
* `.zenodo.json` — Archival metadata for automated Zenodo DOI minting.
* `LICENSE` — MIT Open Source License.

## Deterministic Software Engineering Standards
All Python modules adhere to strict safety-critical and deterministic design rules:
1. **Zero External Dependencies:** Uses only the Python 2.7 standard library (`__future__`, `os`, `math`).
2. **Static Memory Allocation:** All eigenvalue matrices and spectral history arrays are pre-allocated within fixed upper bounds (`MAX_ZEROS`, `MAX_LEVELS`, `MAX_INTERVALS`, `MAX_TIME_STEPS`).
3. **Fail-Safe Path Resolution:** Dynamically resolves output directories via `os.getcwd()` and `__file__` to prevent Windows backslash escape errors.
4. **Assertion-First Validation:** Every subroutine enforces dual mathematical invariants before state transitions.
5. **Automated Trace Auditing:** Each execution generates human-readable Input/Process/Output trace logs (`*.log`) and formal verification certificates (`*.txt`).

## Execution Instructions
Open any `.py` script in your Python 2.7 IDE (such as IDLE) and press **F5** to execute. Trace logs and verification output certificates will be written directly to the active working directory.

## Citation
If you use this software or manuscript in your research, please cite it using the metadata in `CITATION.cff` or via its Zenodo DOI.
