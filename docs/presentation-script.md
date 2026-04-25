# Short Presentation Script

Use this as a simple structure for explaining the project.

1. This project solves a small portfolio optimization problem.
2. Each asset is represented by one bit.
3. A bit value of `1` means the asset is selected.
4. The objective balances expected return against risk.
5. The binary objective is converted into an Ising Hamiltonian.
6. QAOA builds a quantum circuit using cost and mixer layers.
7. A classical optimizer tunes the circuit angles.
8. The final probabilities show which portfolios the circuit prefers.

Closing line:

```text
This notebook is mainly a learning example that connects finance, binary optimization, and QAOA in one readable workflow.
```
