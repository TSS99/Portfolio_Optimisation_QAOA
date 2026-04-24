# QUBO To Ising

QUBO stands for Quadratic Unconstrained Binary Optimization.

In this project, the QUBO variable is:

```text
x_i in {0, 1}
```

Quantum Hamiltonians are easier to write with Pauli-Z values:

```text
Z_i in {+1, -1}
```

The bridge between them is:

```text
x_i = (1 - Z_i) / 2
```

This mapping works because:

| Z value | x value | Meaning |
| --- | --- | --- |
| `+1` | `0` | Asset is not selected |
| `-1` | `1` | Asset is selected |

After this substitution, the portfolio cost becomes an Ising Hamiltonian that can be encoded into QAOA circuit rotations.
