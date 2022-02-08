# Variational Quantum Eigensolver

Variational Quantum Eigensolvers (VQE) are a hybrid quantum/classical algorithm that can calculate the ground-state for a quantum system. They work on contemporary NISQ devices, but to solve new problems in, for instance, biochemistry, will require between 100 and 1000 fully-connected qubits with low error rates. [[Giani 2021](https://doi.org/10.1007/s42979-021-00786-3)]

VQE can also be extended to solve nonlinear problems with polynomial scaling, rather than the exponential scaling required by classical computers. [[Giani 2021](https://doi.org/10.1007/s42979-021-00786-3)]

In VQE, a physical system or optimization problem is encoded as an energy landscape defined by the Hamiltonian of the system. The system is prepared in a state known to be near to the optimal state, or ground state in the case of a physical system. At each iteration, an "ansatz" of parameterized operations is applied to this state and the energy expectation value is calculated by measuring the system. A classical optimization outer loop modifies the ansatz parameters until the energy expectation value converges near the minimum value.

<script>MathJax.typeset();</script>
