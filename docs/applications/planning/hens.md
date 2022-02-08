# Heat Exchanger Network Synthesis

One way industrial plants can help to minimize energy costs and maximize efficiency of energy conversion is to use heat exchangers, allowing hot utilities or streams to heat cold streams, or vice versa. Optimizing a network of heat exchangers, known as Heat Exchanger Network Synthesis, or HENS, is often accomplished using a heuristic that decomposes the problem into separate parts, but aquiring an exact solution is an NP-hard problem. [[Ajagekar 2019](https://doi.org/10.1016/j.energy.2019.04.186)]

The cost function we minimize in HENS is given by

<math display="block"><mrow><mi>C</mi><mo>(</mo><mi>x</mi><mo>)</mo></mrow><mo>=</mo><munder><mo>&sum;</mo><mi>i</mi></munder><munder><mo>&sum;</mo><mi>j</mi></munder><msub><mi>c</mi><mrow><mi>i</mi><mi>j</mi></mrow></msub><msub><mi>w</mi><mrow><mi>i</mi><mi>j</mi></mrow></math>

where <math><msub><mi>c</mi><mrow><mi>i</mi><mi>j</mi></mrow></msub></math> gives the cost for placing a heat exhanger between source <math><mi>i</mi></math> and sink <math><mi>j</mi></math> and <math><msub><mi>w</mi><mrow><mi>i</mi><mi>j</mi></mrow></msub></math> is a boolean variable that indicates whether such a heat exchanger is used. A number of constraints are also involved, such as the requirement that the total heat flowing into all sinks from a particular source must equal the heat flowing from that source, <math><munder><mo>&sum;</mo><mi>j</mi></munder><msub><mi>q</mi><mrow><mi>i</mi><mi>j</mi></mrow></msub><mo>=</mo><msub><mi>S</mi><mi>i</mi></math>. [[Ajagekar 2019](https://doi.org/10.1016/j.energy.2019.04.186)]

[Ajagekar 2019](https://doi.org/10.1016/j.energy.2019.04.186) mapped a series of HENS instances onto [QUBO](../../quantum/models/qubo.md) and solved the same instances using a classical optimizer. While the heat <math><msub><mi>q</mi><mrow><mi>i</mi><mi>j</mi></mrow></msub></math> flowing between source and sink is a continuous variable, it must be discretized by partitioning into a range of values to solve on a quantum computer. For this problem, the quantum solver was able to find the optimal solution in nearly all cases, but performance scaled no better than for the classical implementation, with a substantial overall performance gap. However, much more research is required to determine whether a quantum computer will eventually beat the classical solution.

<script>MathJax.typeset();</script>
