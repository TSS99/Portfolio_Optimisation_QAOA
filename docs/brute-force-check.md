# Brute Force Check

For only three assets, there are eight possible portfolios.

That means students can manually check every bitstring:

```text
000, 001, 010, 011, 100, 101, 110, 111
```

A useful extension is to compute the portfolio objective for all eight bitstrings and compare the lowest-cost bitstring with the most likely QAOA result.

This helps separate two ideas:

- the exact best answer for a tiny problem;
- the candidate answer produced by the QAOA heuristic.

For larger portfolios, brute force becomes expensive because the number of bitstrings grows as `2^n`.
