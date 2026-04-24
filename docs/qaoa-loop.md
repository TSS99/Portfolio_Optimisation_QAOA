# QAOA Loop

QAOA is a hybrid algorithm because it uses both a quantum circuit and a classical optimizer.

The loop works like this:

1. Choose starting values for `gamma` and `beta`.
2. Build a QAOA circuit using those values.
3. Simulate the circuit and compute the expected cost.
4. Give that cost to the classical optimizer.
5. Let the optimizer suggest new values.
6. Repeat until the optimizer stops.

The quantum side creates a probability distribution over portfolios. The classical side searches for parameters that make low-cost portfolios more likely.

In this notebook, the statevector simulator lets us compute the expectation value exactly for the small three-asset example.
