# Cost Hamiltonian

The cost Hamiltonian is the quantum version of the portfolio objective.

In simple terms:

```text
low Hamiltonian energy = better portfolio cost
```

The notebook builds two kinds of terms:

- `Z_i` terms, which describe the individual effect of each asset;
- `Z_i Z_j` terms, which describe pairwise risk relationships between assets.

The QAOA circuit uses this Hamiltonian to make better portfolio bitstrings more likely after optimization.

Constant terms are skipped because they shift every portfolio score by the same amount and do not change the best answer.
