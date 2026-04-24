# Classical Optimizer

QAOA still needs a classical optimizer because the quantum circuit contains adjustable angles.

In this notebook:

- `gamma` angles control the cost part of QAOA.
- `beta` angles control the mixer part of QAOA.
- COBYLA searches for values that reduce the expectation value.

COBYLA is derivative-free, so it does not require the gradient of the objective function.

The optimizer does not directly choose a portfolio. It chooses circuit parameters. The optimized circuit then produces portfolio bitstrings with different probabilities.
