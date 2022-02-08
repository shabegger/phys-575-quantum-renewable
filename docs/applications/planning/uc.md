# Unit Commitment

Unit commitment addresses the problem of identifying the energy resources that should be used to meet a particular demand. It is subject to a large number of constraints, such as thermal line limits, voltage limits, node balancing and reserve requirements. Since demand forecasts may be innacurate, unit commitment must be solved in near real-time. [[Giani 2021](https://doi.org/10.1007/s42979-021-00786-3)]

Unit commitment is generally formulated as a mixed-integer nonlinear optimization problem and is NP-hard. A variety of heuristics have been used to solve unit commitment, but with the large and increasing number of power plants, this problem may become intractable. [[Ajagekar 2019](https://doi.org/10.1016/j.energy.2019.04.186)]

The goal of unit commitment is to minimize the cost of operating a number of energy sources while meeting demand, while obeying all system constraints. The cost function can be formulated as

<math display="block"><mrow><mi>C</mi><mo>(</mo><mi>x</mi><mo>)</mo></mrow><mo>=</mo><munder><mo>&sum;</mo><mi>i</mi></munder><msub><mi>A</mi><mi>i</mi></msub><msub><mi>y</mi><mi>i</mi></msub><mo>+</mo><msub><mi>B</mi><mi>i</mi></msub><msub><mi>p</mi><mi>i</mi></msub><mo>+</mo><msub><mi>C</mi><mi>i</mi></msub><msubsup><mi>p</mi><mi>i</mi><mn>2</mn></msubsup></math>

where <math><msub><mi>y</mi><mi>i</mi></msub></math> is a binary variable that indicates whether energy source <math><mi>i</mi></math> is online and <math><msub><mi>p</mi><mi>i</mi></msub></math> is the power output of the source. <math><msub><mi>A</mi><mi>i</mi></msub></math>, <math><msub><mi>B</mi><mi>i</mi></msub></math> and <math><msub><mi>C</mi><mi>i</mi></msub></math> are constants particular to each energy source.

[Ajagekar 2019](https://doi.org/10.1016/j.energy.2019.04.186) mapped a series of unit commitment instances with varying numbers of energy sources onto [QUBO](../../quantum/models/qubo.md) and solved the same instances using a classical optimizer. As the size of the problem grew, the solutions given by the D-Wave system decreased in quality compared to solutions from the classical optimizer with poor scaling. As a mixed-integer nonlinear optimization problem, unit commitment may not benefit from quantum computing until a fully fault-tolerant universal [circuit-based](../../quantum/architectures/circuit.md) quantum computer is built.

<script>MathJax.typeset();</script>
