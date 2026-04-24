# Portfolio Optimisation using QAOA

This repository contains a beginner-friendly Jupyter Notebook that explains how to solve a small portfolio optimization problem using the Quantum Approximate Optimization Algorithm (QAOA).

Repository link: [TSS99/Portfolio_Optimisation_QAOA](https://github.com/TSS99/Portfolio_Optimisation_QAOA)

## What This Project Teaches

The notebook follows one clear chain of logic:

1. Start with a simple finance question: which assets should be selected?
2. Represent each asset decision as a binary value, where `1` means selected and `0` means not selected.
3. Build a cost function that rewards expected return and penalizes risk.
4. Convert the binary optimization problem into an Ising Hamiltonian.
5. Build a QAOA circuit in Qiskit.
6. Use a classical optimizer to tune the QAOA parameters.
7. Read the most likely bitstrings as candidate portfolios.

This is a learning project, not financial advice or a production trading system.

## Repository Contents

| File | Purpose |
| --- | --- |
| `Portfolio_Optimisation_QAOA.ipynb` | Main notebook with the full explanation and implementation |
| `README.md` | Project overview, setup instructions, and beginner notes |
| `requirements.txt` | Python packages needed to run the notebook |
| `docs/` | Short supporting notes for revision and presentation prep |
| `CONTRIBUTING.md` | Guidance for keeping future changes beginner-friendly |

## Supporting Notes

The `docs/` folder breaks the notebook into smaller study notes. Start with `docs/project-overview.md`, then read `docs/portfolio-bitstrings.md`, `docs/markowitz-intuition.md`, and `docs/qaoa-loop.md`.

## Key Idea

Portfolio optimization is about balancing return and risk.

In this notebook:

- `mu` stores the expected return of each asset.
- `Sigma` stores the covariance matrix, which describes risk and how assets move together.
- `q` controls risk aversion.
- A bitstring such as `101` represents a portfolio choice.

For a three-asset example:

- `000` means no assets are selected.
- `001` means only the first asset is selected.
- `101` means the first and third assets are selected.
- `111` means all assets are selected.

Qiskit prints bitstrings with qubit 0 on the right, and this notebook maps qubit 0 to asset 1.

QAOA searches over these bitstrings and tries to place higher probability on lower-cost portfolios.

## Setup

Create and activate a virtual environment:

```bash
python -m venv .venv
source .venv/bin/activate
```

Install the required packages:

```bash
python -m pip install -r requirements.txt
```

Start Jupyter Notebook:

```bash
jupyter notebook
```

Then open:

```text
Portfolio_Optimisation_QAOA.ipynb
```

## Quick Start For Students

If you are opening the project for the first time, run the notebook once without changing anything. After that, change only one variable, such as `q` or one value in `mu`, and run the notebook again. Comparing the two outputs is the easiest way to understand the model.

## Notebook Walkthrough

The notebook is organized as a step-by-step guide:

1. Mathematical formulation of the portfolio problem.
2. QUBO and Ising mapping.
3. Package imports.
4. Mock financial data generation.
5. Cost Hamiltonian construction.
6. QAOA concept introduction.
7. Mixer Hamiltonian construction.
8. Parameterized QAOA circuit creation.
9. Expectation value calculation.
10. Classical optimizer setup.
11. QAOA optimization loop.
12. Portfolio probability extraction.
13. Visualization and conclusion.

## How To Read The Output

After optimization, the notebook prints the most probable portfolios. Each portfolio is shown as a bitstring.

Example:

```text
Portfolio 101 : 32.50%
```

This means the optimized circuit outputs `101` with about `32.50%` probability. In a three-asset setup, that bitstring means selecting asset 1 and asset 3.

The bar chart at the end shows the same probabilities visually. Higher bars indicate portfolios that QAOA favors more strongly.

## Things To Experiment With

Students can modify these values to understand the algorithm better:

- Change `mu` to test different expected returns.
- Change `Sigma` to test different risk relationships.
- Change `q` to make the optimizer more or less risk-averse.
- Change `p_layers` to add or remove QAOA layers.
- Change `maxiter` to let the classical optimizer search longer.

## Important Limitations

This notebook intentionally keeps the problem small and readable.

- It uses only three mock assets.
- It uses a statevector simulator, not real quantum hardware.
- It does not include constraints such as budget, minimum return, or selecting exactly `k` assets.
- The highest-probability bitstring is a candidate solution, not a guaranteed global optimum.

These simplifications make the project easier to understand before moving to larger and more realistic portfolio optimization problems.
