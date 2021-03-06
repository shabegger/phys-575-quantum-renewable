# Quantum Approximate Optimization Algorithm

The quantum approximate optimization algorithm (QAOA) is a combinatorial optimization algorithm that provides approximate solutions using a classical optimization outer loop [[Giani 2021](https://doi.org/10.1007/s42979-021-00786-3)]. It is designed to minimize the cost function

<math display="block"><mrow><mi>C</mi><mo>(</mo><mi>z</mi><mo>)</mo></mrow><mo>=</mo><munderover><mo>&sum;</mo><mrow><mi>a</mi><mo>=</mo><mn>1</mn></mrow><mi>m</mi></munderover><mrow><msub><mi>C</mi><mi>a</mi></msub><mo>(</mo><mi>z</mi><mo>)</mo></mrow></math>

where the function <math><msub><mi>C</mi><mi>a</mi></msub><mo>(</mo><mi>z</mi><mo>)</mo></math> takes as input all measured qubits and returns a boolean <math><mn>0</mn></math> or <math><mn>1</mn></math>.

In the quantum component of this algorithm, a set of operators are applied to an initial state in an equal superposition of all states. After the operators are applied, the state of the system is measured, and the cost function, <math><mi>C</mi><mo>(</mo><mi>z</mi><mo>)</mo></math>, is calculated. A classical outer loop adjusts the parameters on the operators until <math><mi>C</mi><mo>(</mo><mi>z</mi><mo>)</mo></math> is minimized.

<script>MathJax.typeset();</script>
