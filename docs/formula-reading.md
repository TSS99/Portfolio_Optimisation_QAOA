# How To Read The Objective Formula

The objective is:

```text
(q / 2) * x^T Sigma x - mu^T x
```

Break it into two parts:

1. `(q / 2) * x^T Sigma x`
   This is the risk penalty. It gets larger when the selected portfolio is riskier.
2. `mu^T x`
   This is the expected return. It gets larger when selected assets have better expected returns.

Because the return term is subtracted, high return reduces the final cost.

The optimizer minimizes the full expression, so it searches for a balance between low risk and high expected return.
