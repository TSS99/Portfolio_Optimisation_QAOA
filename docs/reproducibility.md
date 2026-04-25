# Reproducibility Notes

The notebook uses random initial QAOA parameters:

```python
initial_params = np.random.rand(2 * p_layers) * np.pi
```

Because of this, two runs may produce slightly different optimizer paths and final probabilities.

For a more reproducible classroom demo, students can set a seed before creating `initial_params`:

```python
np.random.seed(42)
```

This makes the random starting point the same across runs on the same environment.

Reproducibility is useful when comparing reports, screenshots, or presentation outputs.
