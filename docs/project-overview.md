# Project Overview

This project demonstrates a small portfolio optimization workflow using QAOA.

The full story is:

1. A portfolio is written as a bitstring.
2. A finance objective scores each bitstring.
3. The objective is converted into a Hamiltonian.
4. A QAOA circuit prepares a probability distribution over bitstrings.
5. A classical optimizer adjusts the circuit parameters.
6. The highest-probability bitstrings are interpreted as candidate portfolios.

The example uses only three assets so that every possible portfolio can be inspected by hand. That makes it easier to connect the math, the circuit, and the final plot.
