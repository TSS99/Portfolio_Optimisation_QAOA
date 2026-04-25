# Parameter Guide

The notebook has a few values that students can safely change.

| Parameter | Where it appears | What it affects |
| --- | --- | --- |
| `mu` | Mock financial data | Expected return for each asset |
| `Sigma` | Mock financial data | Risk and asset co-movement |
| `q` | Mock financial data | How strongly risk is penalized |
| `p_layers` | QAOA circuit setup | Number of QAOA layers |
| `maxiter` | Optimizer call | How long COBYLA searches |

Suggested beginner workflow:

1. Change only one parameter.
2. Run the notebook from top to bottom.
3. Compare the final portfolio probabilities.
4. Write one sentence explaining what changed.
