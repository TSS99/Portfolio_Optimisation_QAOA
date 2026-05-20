<div align="center">
  <h1>⚛️ Portfolio Optimisation using QAOA</h1>
  <p><strong>A beginner-friendly guide to solving financial portfolio optimization using the Quantum Approximate Optimization Algorithm (QAOA) via Qiskit.</strong></p>
  
  <p>
    <img src="https://img.shields.io/badge/Python-3.8+-blue.svg" alt="Python Version" />
    <img src="https://img.shields.io/badge/Qiskit-SDK-purple.svg" alt="Qiskit" />
    <img src="https://img.shields.io/badge/Algorithm-QAOA-success.svg" alt="QAOA" />
    <img src="https://img.shields.io/badge/Finance-Portfolio_Optimization-goldenrod.svg" alt="Finance" />
  </p>
</div>

---

## 🚀 Overview

This repository demonstrates how to approach a real-world financial problem—**Portfolio Optimization**—using Quantum Computing. We translate the financial goal of maximizing returns while minimizing risk into a **Quadratic Unconstrained Binary Optimization (QUBO)** model, map it to an **Ising Hamiltonian**, and optimize it using **QAOA**.

This is designed as an educational bridge between quantitative finance and quantum algorithms.

---

## 🧮 The Mathematical Foundation

### 1. The Portfolio Objective

We want to decide which assets to include in our portfolio. Let our decision be a binary vector $x \in \{0, 1\}^n$:
- $x_i = 1$ (Select asset $i$)
- $x_i = 0$ (Do not select asset $i$)

Given expected returns $\mu$, a covariance (risk) matrix $\Sigma$, and a risk-aversion factor $q$, we want to minimize our risk while maximizing our expected return. 

$$ \min_{x \in \{0,1\}^n} \frac{q}{2} x^T \Sigma x - \mu^T x $$

### 2. Ising Hamiltonian Mapping

Quantum computers operate on qubits, whose states can be measured as $+1$ or $-1$ (eigenvalues of the Pauli-Z operator). We convert our binary variables $x_i \in \{0, 1\}$ into spin variables $Z_i \in \{1, -1\}$ using the substitution:

$$ x_i = \frac{1 - Z_i}{2} $$

Substituting this into our QUBO gives us the **Cost Hamiltonian** ($H_C$). The lowest energy state (ground state) of this Hamiltonian corresponds to the optimal portfolio.

### 3. The QAOA Approach

**QAOA** (Quantum Approximate Optimization Algorithm) is a hybrid quantum-classical algorithm. It uses two Hamiltonians:

1. **Cost Hamiltonian ($H_C$)**: Encodes our portfolio optimization problem.
2. **Mixer Hamiltonian ($H_M$)**: Flips qubit states to allow the algorithm to explore the solution space.

$$ H_M = \sum_{i=1}^n X_i $$

The QAOA circuit alternates between applying $H_C$ and $H_M$ over $p$ layers, parameterized by angles $\gamma$ and $\beta$. A classical optimizer (like COBYLA) tweaks these angles until the expectation value $\langle \psi | H_C | \psi \rangle$ is minimized.

---

## 💻 Repository Structure

| File / Folder | Purpose |
| --- | --- |
| 📓 `Portfolio_Optimisation_QAOA.ipynb` | **Main Notebook:** The full step-by-step implementation. |
| 📄 `README.md` | Project overview and mathematical foundation. |
| 📦 `requirements.txt` | Python dependencies. |
| 📚 `docs/` | Supporting study notes and classroom resources. |

---

## 🛠️ Quick Start

**1. Create a virtual environment & install dependencies:**
```bash
python -m venv .venv
source .venv/bin/activate  # On Windows use: .venv\Scripts\activate
pip install -r requirements.txt
```

**2. Launch Jupyter Notebook:**
```bash
jupyter notebook Portfolio_Optimisation_QAOA.ipynb
```

**3. Experiment!**
Try modifying the mock data in the notebook:
- Change the `q` (risk aversion) factor. Higher $q$ means the algorithm prioritizes low risk. Lower $q$ means it chases higher returns.
- Change the expected returns vector $\mu$.
- Adjust the number of QAOA layers (`p_layers`).

---

## 📊 Interpreting Results

Once the classical optimizer finishes tuning the QAOA circuit, measuring the circuit produces a probability distribution over all possible portfolios (bitstrings).

```text
Top Portfolios by Probability:
Portfolio 101 : 32.50%
```

In this 3-asset example, the bitstring `101` means that **Asset 1 and Asset 3** were selected, offering the best mathematical balance of return and risk based on our inputs!

<div align="center">
  <i>"Quantum optimization isn't about finding the perfect answer immediately, it's about shifting the probability landscape so the best answers are the easiest to find."</i>
</div>
