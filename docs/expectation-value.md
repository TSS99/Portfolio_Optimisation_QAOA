# Expectation Value

The expectation value is the average cost predicted by the quantum state.

In the notebook, the QAOA circuit creates a state called `sv`. That state assigns amplitudes to different portfolio bitstrings.

The code then evaluates:

```text
<psi | H_C | psi>
```

This number is useful because the classical optimizer needs a single score to improve. Lower expectation values mean the current QAOA parameters are producing a better average portfolio cost.

For beginners, it is enough to remember:

```text
expectation value = average cost of the current quantum trial solution
```
