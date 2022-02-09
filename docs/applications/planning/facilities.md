# Facility Location-Allocation

Facility location-allocation is a category of well-defined optimization problems of great importance to design and planning for energy systems, into which several infrastructure development optimization problems for renewables can be cast. As an example, we would like to determine where to develop a wind farm for maximum energy capture, while also adhering to the constraints of the electrical grid. [[Ajagekar 2019](https://doi.org/10.1016/j.energy.2019.04.186)]

The quadratic assignment problem is an example of a facility location-allocation problem which is known to be in the NP-hard complexity class. An example instance of this problem is the assignment of <math><mi>n</mi></math> power plants to <math><mi>n</mi></math> regions. It is defined by two <math><mi>n</mi><mo>&times;</mo><mi>n</mi></math> matrices, <math><mi>C</mi></math> and <math><mi>T</mi></math>, where the elements <math><msub><mi>C</mi><mrow><mi>i</mi><mi>j</mi></mrow></msub></math> and <math><msub><mi>T</mi><mrow><mi>p</mi><mi>q</mi></mrow></msub></math> represent the cost of moving a unit of energy from location <math><mi>i</mi></math> to location <math><mi>j</mi></math> and the number of units of energy that will need to be transported from plant <math><mi>p</mi></math> to plant <math><mi>q</mi></math>, respectively. [[Ajagekar 2019](https://doi.org/10.1016/j.energy.2019.04.186)]

Subject to the constraint that the solution gives a one-to-one mapping between locations and plants, the cost function to optimize is given by

<math display="block"><mrow><mi>C</mi><mo>(</mo><mi>x</mi><mo>)</mo></mrow><mo>=</mo><munderover><mo>&sum;</mo><mrow><mi>q</mi><mo>=</mo><mn>1</mn></mrow><mi>n</mi></munderover><munderover><mo>&sum;</mo><mrow><mi>p</mi><mo>=</mo><mn>1</mn></mrow><mi>n</mi></munderover><munderover><mo>&sum;</mo><mrow><mi>j</mi><mo>=</mo><mn>1</mn></mrow><mi>n</mi></munderover><munderover><mo>&sum;</mo><mrow><mi>i</mi><mo>=</mo><mn>1</mn></mrow><mi>n</mi></munderover><msub><mi>C</mi><mrow><mi>i</mi><mi>j</mi></mrow></msub><msub><mi>T</mi><mrow><mi>p</mi><mi>q</mi></mrow></msub><msub><mi>x</mi><mrow><mi>p</mi><mi>i</mi></mrow></msub><msub><mi>x</mi><mrow><mi>q</mi><mi>j</mi></mrow></math>

where <math><msub><mi>x</mi><mrow><mi>p</mi><mi>i</mi></mrow></msub></math> is a boolean variable that indicates whether plant <math><mi>p</mi></math> is to be built at location <math><mi>i</mi></math>. [[Ajagekar 2019](https://doi.org/10.1016/j.energy.2019.04.186)]

[Ajagekar 2019](https://doi.org/10.1016/j.energy.2019.04.186) cast this problem into the [Ising model](../../quantum/models/ising.md), the Hamiltonian of which can easily be represented as operations in a [quantum circuit](../../quantum/architectures/circuit.md), and solved a small <math><mi>n</mi><mo>=</mo><mn>4</mn></math> instance on [IBM Q](https://quantum-computing.ibm.com/)'s quantum computer using the [VQE](../../quantum/algorithms/vqe.md) algorithm.

Since the constraint of a one-to-one map from power plant to location can't be made explicitly in a quantum algorithm, one instead encodes that constraint as a large cost, <math><mi>A</mi></math>, when the constraint is not met. The cost function can then be updated as

<math display="block"><mrow><mi>C</mi><mo>(</mo><mi>x</mi><mo>)</mo></mrow><mo>=</mo><munderover><mo>&sum;</mo><mrow><mi>q</mi><mo>=</mo><mn>1</mn></mrow><mi>n</mi></munderover><munderover><mo>&sum;</mo><mrow><mi>p</mi><mo>=</mo><mn>1</mn></mrow><mi>n</mi></munderover><munderover><mo>&sum;</mo><mrow><mi>j</mi><mo>=</mo><mn>1</mn></mrow><mi>n</mi></munderover><munderover><mo>&sum;</mo><mrow><mi>i</mi><mo>=</mo><mn>1</mn></mrow><mi>n</mi></munderover><msub><mi>C</mi><mrow><mi>i</mi><mi>j</mi></mrow></msub><msub><mi>T</mi><mrow><mi>p</mi><mi>q</mi></mrow></msub><msub><mi>x</mi><mrow><mi>p</mi><mi>i</mi></mrow></msub><msub><mi>x</mi><mrow><mi>q</mi><mi>j</mi></mrow></msub><mo>+</mo><mi>A</mi><munderover><mo>&sum;</mo><mrow><mi>i</mi><mo>=</mo><mn>1</mn></mrow><mi>n</mi></munderover><msup><mrow><mo>(</mo><mn>1</mn><mo>-</mo><munderover><mo>&sum;</mo><mrow><mi>p</mi><mo>=</mo><mn>1</mn></mrow><mi>n</mi></munderover><msub><mi>x</mi><mrow><mi>p</mi><mi>i</mi></mrow></msub><mo>)</mo></mrow><mn>2</mn></msup><mo>+</mo><mi>A</mi><munderover><mo>&sum;</mo><mrow><mi>p</mi><mo>=</mo><mn>1</mn></mrow><mi>n</mi></munderover><msup><mrow><mo>(</mo><mn>1</mn><mo>-</mo><munderover><mo>&sum;</mo><mrow><mi>i</mi><mo>=</mo><mn>1</mn></mrow><mi>n</mi></munderover><msub><mi>x</mi><mrow><mi>p</mi><mi>i</mi></mrow></msub><mo>)</mo></mrow><mn>2</mn></msup></math>

To encode the binary variables, <math><msub><mi>x</mi><mrow><mi>p</mi><mi>i</mi></mrow></msub></math>, onto measurements in the computational basis, <math><mi>Z</mi></math>, which give values <math><mn>1</mn></math> and <math><mn>-1</mn></math>, we set

<math display="block"><msub><mi>x</mi><mrow><mi>p</mi><mi>i</mi></mrow></msub><mo>=</mo><mfrac><mrow><mn>1</mn><mo>-</mo><msub><mi>Z</mi><mrow><mi>p</mi><mi>i</mi></mrow></msub></mrow><mn>2</mn></mfrac></math>

This [Google Colab](https://colab.research.google.com/drive/1imY5xEJ9VOmJxiLQTY2vll793MXWxxy8?usp=sharing) notebook illustrates how this problem can be mapped onto a quantum circuit and solved using VQE. The notebook contains the complete code for a random <math><mi>n</mi><mo>=</mo><mn>3</mn></math> problem using Google's open source quantum framework, [Cirq](https://quantumai.google/cirq). In this example, the resulting quantum circuit is run in the Cirq simulator, but it can also be run on real quantum hardware. [Tensorflow](https://www.tensorflow.org/) and [Tensorflow Quantum](https://www.tensorflow.org/quantum) are used for the classical outer optimization loop. The Hamiltonian can be described with the following code

```python
# Large penalty for breaking constraints
A = 50

# Build up the Hamiltonian for our Ising model
h = []
for q in range(N):
  for p in range(N):
    for j in range(N):
      for i in range(N):
        h.append(costs[i][j] * transport[p][q] * (1 - cirq.Z(cirq.GridQubit(p, i))) / 2 * (1 - cirq.Z(cirq.GridQubit(q, j))) / 2)
for i in range(N):
  h_i = [1]
  for p in range(N):
    h_i.append((cirq.Z(cirq.GridQubit(p, i)) - 1) / 2)
  h.append(A * sum(h_i) * sum(h_i))
for p in range(N):
  h_p = [1]
  for i in range(N):
    h_p.append((cirq.Z(cirq.GridQubit(p, i)) - 1) / 2)
  h.append(A * sum(h_p) * sum(h_p))
```

[Ajagekar 2019](https://doi.org/10.1016/j.energy.2019.04.186) additionally mapped this problem onto [QUBO](../../quantum/models/qubo.md) and ran it on a [D-Wave](https://www.dwavesys.com/) annealer for several differently sized instances. They found the D-Wave solver produced nearly optimal results with much better scaling than running a classical optimizer on a single CPU core.

<script>MathJax.typeset();</script>
