# Quantum state preparation with multi-controlled R_Z gates and 1-qubit gates

## This project aims to construct a Quantum Computing circuit via Qiskit, that takes an input of any state vector $\psi\in\mathbb C^{2^n}$ such that $\left\lVert\psi\right\rVert=1$, then outputs the circuit $U$ that prepares the zero register to be agree with $\psi$.

### Initial Thoughts:
1. QSP is constructed by induction on register dimension.
2. Only Ry and X gates are involved.
3. Ry can be represented by Rz.

### Implementation ideas:
1. Induction is constructed via recursion.
2. Subproblem of preparing first k digits is conditioned on, thus by the rest n-k digits.
3. The k-th subproblem takes inputs from the first and the second half of a 2^(k+1) state vector, where both should be normalized.

## Please see QSPcirc.ipynb for detailed implementation, tests and comments.
