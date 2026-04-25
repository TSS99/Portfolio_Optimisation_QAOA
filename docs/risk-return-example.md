# Risk And Return Example

Imagine two assets:

- Asset A has high expected return but high risk.
- Asset B has lower expected return but lower risk.

If `q` is small, the optimizer may prefer Asset A because return matters more.

If `q` is large, the optimizer may prefer Asset B because risk is punished more strongly.

This is the main tradeoff in the notebook. QAOA is not simply looking for the highest return. It is looking for a bitstring with a good score under the chosen risk-return objective.

That is why changing `q` is one of the best first experiments for students.
