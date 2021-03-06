# The Jordan-Wigner Representation

There are a number of models used to describe quantum chemistry systems, but the Jordan-Wigner representation is one of the simplest and most common. It is well suited for mapping onto the [circuit model](../architectures/circuit.md) of quantum computing. [[MSFT Azure Docs](https://docs.microsoft.com/en-us/azure/quantum/user-guide/libraries/chemistry/concepts/jordan-wigner)]

The Jordan-Wigner representation is an example of second quantization. In first quantization, an electron is described as being in a particular orbital about one or several atomic nuclei and as having a particular spin, or in a superposition of any of these basis states. In second quantization, we instead choose a basis such that each spin-orbital combination has but two states, occupied or unoccupied. This situation works well when studying fermions, like electrons, since each spin-orbital has maximum occupancy of one. This representation is also well suited to studying chemistry systems on a quantum computer, since the unoccupied/occupied states may be mapped to the <math><mo>|</mo><mn>0</mn><mo>&rang;</mo></math> and <math><mo>|</mo><mn>1</mn><mo>&rang;</mo></math> states of a qubit.

<script>MathJax.typeset();</script>
