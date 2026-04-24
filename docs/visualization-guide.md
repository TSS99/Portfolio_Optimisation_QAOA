# Visualization Guide

The final bar chart shows the probability of each portfolio bitstring after QAOA optimization.

How to read it:

- The x-axis lists bitstrings.
- The y-axis shows probability.
- Taller bars are portfolios the optimized circuit favors more.

If one or two bars dominate, QAOA is concentrating probability on a small set of candidate solutions.

If all bars are similar, the result is less decisive. In that case, try increasing the optimizer iterations, changing the initial parameters, or testing a different number of QAOA layers.
