# Troubleshooting

## `ModuleNotFoundError: No module named 'qiskit'`

Install the dependencies again from the repository root:

```bash
python -m pip install -r requirements.txt
```

## Jupyter opens but the notebook kernel is missing

Make sure the virtual environment is activated before starting Jupyter.

## The final probabilities change between runs

The notebook starts the optimizer from random initial parameters. Different starting points can lead to slightly different optimization paths.

## The chart is blank

Run all notebook cells from top to bottom. The final plot depends on variables created in earlier cells.
