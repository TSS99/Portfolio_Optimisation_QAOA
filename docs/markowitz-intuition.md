# Markowitz Intuition

The notebook uses the Markowitz mean-variance idea: a portfolio should be judged by both expected return and risk.

The return part is:

```text
mu^T x
```

This becomes larger when the selected assets have higher expected returns.

The risk part is:

```text
x^T Sigma x
```

This becomes larger when the selected assets are risky or move together strongly.

The objective minimizes:

```text
risk penalty - expected return
```

So the optimizer prefers portfolios that keep risk low while still earning enough expected return.
