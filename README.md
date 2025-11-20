# Timeless Correlation Theory (TCT): Numerical Experiments

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![Python 3.8+](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.17145229.svg)](https://doi.org/10.5281/zenodo.17145229)

This repository contains the source code and numerical experiments validating **Timeless Correlation Theory (TCT)** — an operational extension of the Page–Wootters framework for relational time.

## Paper Abstract
*From the accompanying article [1]:*

Timeless Correlation Theory (TCT) introduces operational metrics for evaluating clock quality within a globally stationary state $|\Psi\rangle$. Unlike the original Page-Wootters formulation, TCT quantifies the impact of noise, detuning, and reparameterization on the emergence of time.

This codebase provides the **computational proof** for the theory's central claims, demonstrating that "time" is a measurable resource derived from correlations between a clock subsystem and a system.

## Experiments

The Jupyter Notebook (`experiments.ipynb`) implements the four canonical experiments described in **Section 4** of the paper:

| Experiment | Description | Key Metric | Result |
| :--- | :--- | :--- | :--- |
| **1. Ideal Correlations** | Reconstructing dynamics from a perfect stationary state. | Fidelity $F(\tau)$ | $F \approx 1.0$ (Recovering Schrödinger evolution). |
| **2. Noisy ("Dirty") Correlations** | Injecting orthogonal noise to simulate decoherence. | Average Fidelity $\bar{F}(\epsilon)$ | Demonstrates fidelity degradation as correlations weaken. |
| **3. Reparameterization** | Testing invariance under clock scaling/shifting ($\tau \to \tau + \delta$). | Fidelity Shift | Proves physical predictions are gauge-invariant if the shift is accounted for. |
| **4. Clock Detuning** | Modifying clock frequency ($\alpha \neq 1$) to simulate miscalibration. | Constraint Norm $\Delta_{constr}$ | Shows linear growth of Hamiltonian constraint violation. |

## Getting Started

### Prerequisites
The simulations rely on standard scientific Python stack:
* `numpy`
* `scipy` (specifically `linalg.expm`)
* `matplotlib`

### Installation
```bash
git clone [https://github.com/YuNeziat/Timeless-Correlation-Theory.git](https://github.com/YuNeziat/Timeless-Correlation-Theory.git)
cd Timeless-Correlation-Theory
pip install -r requirements.txt
