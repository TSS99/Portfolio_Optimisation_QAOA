# Possible Extensions

After understanding the current notebook, students can extend the project in several directions.

## Add a budget constraint

Require the portfolio to select only assets that fit inside a fixed budget.

## Select exactly k assets

Add a penalty term so the optimizer prefers bitstrings with exactly `k` selected assets.

## Use real market data

Replace the mock `mu` and `Sigma` values with returns and covariance estimated from historical prices.

## Compare with brute force

For small asset counts, calculate the objective for every bitstring and compare QAOA with the exact best answer.
