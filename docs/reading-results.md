# Reading Results

The notebook prints portfolio probabilities after optimization.

Example:

```text
Portfolio 101 : 32.50%
```

This means the optimized QAOA circuit would output the bitstring `101` about 32.50 percent of the time.

For this notebook, `101` means:

- asset 1 is selected;
- asset 2 is not selected;
- asset 3 is selected.

The most likely bitstring is the portfolio the trained circuit favors most. It should be treated as a candidate answer. For a small example, students can also calculate the cost of all bitstrings and compare them directly.
