# Quantum Annealer Model

Quantum annealing relies on directly encoding the problem into a quantum energy landscape. [[Giani 2021](https://doi.org/10.1007/s42979-021-00786-3)]

Quantum counterpart of simulated annealing, enables quantum tunneling. [[Ajagekar 2019](https://doi.org/10.1016/j.energy.2019.04.186)]

Quantum annealers are specifically designed for optimization. D-Wave, a Canadian company has made quantum annealers commercially available via the cloud. These machines are able to solve problems formulated as either the [QUBO](../models/qubo.md) or [Ising](../models/ising.md) models. [[Ajagekar 2019](https://doi.org/10.1016/j.energy.2019.04.186)]

At the beginning of the algorithm, the system is put into a state with a uniform probability distribution. After the annealing process, the system is found in the globally optimum state with high probability. These machines are inherently more robust to environmental noise than [quantum circuit model](circuit.md) machines, but there are very few known problems for which quantum annealers are exponentially faster than classical algorithms. [[Ajagekar 2019](https://doi.org/10.1016/j.energy.2019.04.186)]

 The quantum speedup isn’t well-known. Begin with a known state of the system and create an energy landscape that encodes the problem with large penalties for breaking constraints. Allow the system to evolve until it is in its minimum energy state (the optimal solution). Special-purpose quantum annealers (D-Wave) or general-purpose quantum computers can be used. D-Wave annealers are shown to improve on classical methods, including simulated annealing, on several NP-hard graph problems. [[Gianai 2021](https://doi.org/10.1007/s42979-021-00786-3)]

<figure>
  <img src="../../images/annealing.jpg"
       alt="Quantum annealing">
  <figcaption>
    Quantum annealing in a double well potential.
    [<a href="https://doi.org/10.1016/j.energy.2019.04.186">Ajagekar 2019</a>]
  </figcaption>
</figure>

D-Wave devices are currently limited in problem size, qubit connectivity and precision. Although quantum annealers have proven to perform better than classical optimizers for some problems, classical algorithms can often be tuned to work well for specific instances. [[Ajagekar 2019](https://doi.org/10.1016/j.energy.2019.04.186)]
