# Portfolio Bitstrings

QAOA outputs bitstrings. In this project, each bit represents one asset.

For three assets:

| Bitstring | Meaning |
| --- | --- |
| `000` | Select no assets |
| `001` | Select asset 1 |
| `010` | Select asset 2 |
| `011` | Select assets 1 and 2 |
| `100` | Select asset 3 |
| `101` | Select assets 1 and 3 |
| `110` | Select assets 2 and 3 |
| `111` | Select all three assets |

Qiskit displays bitstrings with qubit 0 on the right. This notebook maps qubit 0 to asset 1, so the rightmost bit corresponds to the first asset.
