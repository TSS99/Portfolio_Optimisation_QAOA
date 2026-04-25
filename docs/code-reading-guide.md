# Code Reading Guide

When reading the notebook code, follow the variables in this order.

1. `n_assets`
   Defines how many qubits and binary decisions are needed.
2. `mu`
   Gives the expected return for each asset.
3. `Sigma`
   Gives the covariance matrix for risk.
4. `cost_hamiltonian`
   Stores the quantum cost model.
5. `qaoa_circ`
   Stores the parameterized QAOA circuit.
6. `initial_params`
   Gives the optimizer its starting angles.
7. `optimal_params`
   Stores the best angles found by COBYLA.
8. `sorted_probs`
   Shows portfolio bitstrings ordered by probability.

This path follows the same logic as the project: data, model, circuit, optimization, result.
