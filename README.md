# QI26-20: QUBO–QAOA Benchmark for Generalized Bipartite Assignment

This repository contains the compact, executable artifact for **“A Reproducible QUBO–QAOA Benchmark for Generalized Bipartite Assignment on NISQ Hardware.”** The central artifact is one numbered Google Colab/Jupyter notebook that integrates the mathematical formulation, synthetic instances, constraint validation, classical baselines, standard QAOA, GM-QAOA, topology analysis, IBM Quantum execution, and scientific reporting.

## Repository contents

```text
QI26-20-QUBO-QAOA-Benchmark/
├── README.md
├── requirements.txt
├── QI26_20_QUBO_QAOA_GM_QAOA_Benchmark.ipynb
├── results/
│   ├── phase1_classical_baselines.csv
│   ├── phase1_standard_qaoa_depth_results.csv
│   ├── phase1_gm_qaoa_ideal_results.csv
│   ├── phase1_transpilation_metrics.csv
│   ├── phase1_hardware_summary.csv
│   ├── phase1_hardware_top_outcomes.csv
│   ├── phase1_claims_checklist.csv
│   └── phase1_compliance_matrix.csv
└── paper/
    └── README.md
```

The final compiled LaTeX manuscript is intentionally omitted. Before the public GitHub release, place it at:

```text
paper/QI26_20_preprint.pdf
```

## Notebook organization

The notebook contains **36 explicitly numbered cells** and should be executed sequentially. Its seven stages are:

1. mathematical formulation and QUBO derivation;
2. synthetic data and constraint validation;
3. classical baselines and evaluation metrics;
4. standard QAOA with Qiskit;
5. Grover-Mixer QAOA;
6. NISQ topology, transpilation, and IBM Quantum execution;
7. experiment tracking, compliance, and conclusions.

The notebook preserves the executed outputs used to produce the CSV files in `results/`.

## Installation

In a local Python environment:

```bash
python -m pip install -r requirements.txt
```

Google Colab users may run the dependency-installation cell included in the notebook.

## IBM Quantum authentication

No credential is stored in this repository. The public notebook sets:

```python
IBM_API_TOKEN = ""
```

For real-hardware execution, provide the token through either:

- a Colab Secret named `QISKIT_IBM_TOKEN`; or
- the environment variable `QISKIT_IBM_TOKEN`.

Without a token, the notebook's automatic execution mode uses a fake IBM backend. Never commit a real API token to GitHub.

## Result tables

| File | Content |
|---|---|
| `phase1_classical_baselines.csv` | Exact, Hungarian, greedy, and simulated-annealing results on the fixed instances. |
| `phase1_standard_qaoa_depth_results.csv` | Deterministic ideal standard-QAOA comparison for $p\in\{1,2,3\}$. |
| `phase1_gm_qaoa_ideal_results.csv` | Ideal GM-QAOA feasibility, optimality, fidelity, parameters, and circuit-depth summary. |
| `phase1_transpilation_metrics.csv` | Logical and transpiled depth, size, and two-qubit-gate counts. |
| `phase1_hardware_summary.csv` | Verifiable aggregate results from the recorded IBM Quantum execution. |
| `phase1_hardware_top_outcomes.csv` | The 15 most probable displayed outcomes per algorithm; this is not the complete distribution. |
| `phase1_claims_checklist.csv` | Explicit limits on the scientific claims supported by Phase 1. |
| `phase1_compliance_matrix.csv` | Mapping between project requirements and notebook evidence. |

## Scientific scope

The benchmark demonstrates reproducible small-instance formulations and comparisons. It does **not** establish quantum advantage or a general scalable state-preparation procedure for GM-QAOA. Hardware claims are tied to the backend, job identifier, transpilation metrics, and measurement results recorded in the executed notebook and exported tables.
