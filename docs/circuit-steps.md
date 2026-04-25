# Circuit Steps

The QAOA circuit is easier to understand if you read it in stages.

1. Apply Hadamard gates to all qubits.
   This creates a starting superposition over all possible portfolios.
2. Apply cost rotations.
   These use the cost Hamiltonian so better and worse portfolios receive different phases.
3. Apply mixer rotations.
   These help move probability between portfolio bitstrings.
4. Repeat for each QAOA layer.
   More layers mean more chances to reshape the probability distribution.
5. Simulate the final state.
   The final state gives probabilities for each portfolio bitstring.

The optimizer changes the rotation angles, not the structure of the circuit.
