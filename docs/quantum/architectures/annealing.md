# Quantum Annealer Architecture

Quantum annealing is the quantum counterpart of simulated annealing, a classical optimization heuristic. Whereas simulated annealing relies an a "temperature" variable to add randomization and avoid settling into a local optimum, quantum annealing enables quantum tunneling to achieve the same effect. [D-Wave](https://www.dwavesys.com/), a Canadian company, has made quantum annealers commercially available via the cloud. These machines are able to solve problems formulated as either the [QUBO](../models/qubo.md) or [Ising](../models/ising.md) models. [[Ajagekar 2019](https://doi.org/10.1016/j.energy.2019.04.186)]

Quantum annealing relies on directly encoding the problem into a quantum energy landscape with large penalties for breaking constraints [[Giani 2021](https://doi.org/10.1007/s42979-021-00786-3)]. At the beginning of the algorithm, the system is put into a state with a uniform probability distribution. The system is allowed to evolve until it is in it's minimum energy state with high probability [[Ajagekar 2019](https://doi.org/10.1016/j.energy.2019.04.186)].

<figure>
  <img src="../../images/annealing.jpg"
       alt="Quantum annealing">
  <figcaption>
    Quantum annealing in a double well potential.
    [<a href="https://doi.org/10.1016/j.energy.2019.04.186">Ajagekar 2019</a>]
  </figcaption>
</figure>

Existing devices are limited in problem size, qubit connectivity and precision. Annealers are inherently more robust to environmental noise than [quantum circuit model](circuit.md) machines, but there are very few known problems for which quantum annealers are exponentially faster than classical algorithms, and often classical algorithms can often be tuned to work well for specific problem instances. [[Ajagekar 2019](https://doi.org/10.1016/j.energy.2019.04.186)]

<script>MathJax.typeset();</script>
