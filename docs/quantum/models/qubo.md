# Quadratic Unconstrained Binary Optimization

Quadratic Unconstrained Binary Optimization (QUBO) is actually an optimization problem, rather than an algorithm. It is defined by the cost function, <math><mi>C</mi><mo>(</mo><mi>x</mi><mo>)</mo><mo>=</mo><munderover><mo>&sum;</mo><mrow><mi>i</mi><mo>=</mo><mn>1</mn></mrow><mi>n</mi></munderover><munderover><mo>&sum;</mo><mrow><mi>j</mi><mo>=</mo><mn>1</mn></mrow><mi>i</mi></munderover><msub><mi>q</mi><mrow><mi>i</mi><mi>j</mi></mrow></msub><msub><mi>x</mi><mi>i</mi></msub><msub><mi>x</mi><mi>j</mi></msub></math>, with <math><mi>x</mi></math> a vector of boolean (<math><mn>0</mn></math> or <math><mn>1</mn></math>) values and real coefficients <math><msub><mi>q</mi><mrow><mi>i</mi><mi>j</mi></mrow></msub></math>.

QUBO is of interest because the [quantum annealers](../architectures/annealing.md) provided by the Canadian company D-Wave are capable of optimizing QUBO, so problems that can be cast as QUBO may be solved in this way. [[Gianai 2021](https://doi.org/10.1007/s42979-021-00786-3)]

<script>MathJax.typeset();</script>