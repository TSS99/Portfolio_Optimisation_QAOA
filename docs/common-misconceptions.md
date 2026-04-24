# Common Misconceptions

## QAOA does not magically guarantee the best answer

QAOA is a heuristic algorithm. It searches for good answers, but the highest-probability bitstring is still a candidate solution.

## A high return asset is not always selected

The objective also includes risk. A high-return asset can be avoided if it adds too much risk to the portfolio.

## More QAOA layers are not always easier

More layers give the circuit more flexibility, but they also add more parameters. The classical optimizer may need more iterations.

## The example is intentionally small

Three assets are used so the full workflow is easy to inspect. Larger portfolios require more qubits and more careful optimization.
