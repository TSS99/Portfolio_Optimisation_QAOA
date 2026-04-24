# Mixer Hamiltonian

The mixer Hamiltonian helps QAOA explore possible answers.

This notebook uses:

```text
H_M = X_1 + X_2 + ... + X_n
```

The Pauli-X operation flips a qubit between 0 and 1. In portfolio language, that means it helps move between selecting and not selecting an asset.

Without a mixer, the circuit would mainly apply the cost information but would not explore the solution space in the standard QAOA way.

The mixer is controlled by the `beta` parameters in the circuit.
