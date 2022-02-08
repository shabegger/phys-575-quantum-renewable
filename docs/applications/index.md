# Applications for Renewable Energy

By 2019, 29 states and DC had “renewable portfolio standards”. The transition to renewable energy sources presents a variety of challenges for energy systems, and some of these may be aided by the use of quantum computers. [[Giani 2021](https://doi.org/10.1007/s42979-021-00786-3)]

In some cases, as with the increase in rooftop solar, the transition to renewables involves moving away from large, centralized generators to a distributed system, and dispatch of these generators is complex. The natural processes that provide renewable energy like wind and solar are variable and difficult to predict, which is a challenge for the electrical grid. [[Giani 2021](https://doi.org/10.1007/s42979-021-00786-3)]

Furthermore, the increasing variety of energy sources are subject to a slate of complex constraints. Conflicting objectives may exist, such as use of resources for water vs. food vs. energy. Renewable resources must be compared, taking into account factors such as the price of generated energy, greenhouse gas emissions, availability of resources (such as wind and solar), energy conversion efficiency and social impacts. Proper allocation requires energy planning models, supply-demand models, renewable energy models, emissions models and optimization models. Planning and scheduling, location and transportation, resource allocation, engineering design and network planning are all areas that may benefit from optimization methods. While classical deterministic optimization methods have been used, in addition to heuristic approaches such as simulated annealing (see [quantum annealing](../quantum/architectures/annealing.md)), genetic algorithms and artificial neural networks (machine learning), some of these problems may benefit from the use of quantum methods. [[Ajagekar 2019](https://doi.org/10.1016/j.energy.2019.04.186)]

Current solutions use methods like process integration and superstructure optimization, which are computationally expensive, requiring exponential time with problem size. Futhermore, there is not always a guarantee of a solution. Classical general-purpose optimization methods often are unable to provide feasible solutions for large-scale multi-objective optimization problems, though sometimes specialized methods are available. Even when classical methods converge, real-world problems may require days or weeks to reach an optimal solution, and most existing studies are limited to local and regional scales as a result. [[Ajagekar 2019](https://doi.org/10.1016/j.energy.2019.04.186)]

Since [quantum computing](../quantum/index.md) algorithms that are superior to classical are only known for a small number of problems, we must weigh the known impact of quantum solutions versus the difficulty to solve using classical methods. The figure below shows that problems in chemistry, linear systems and optimization are prime candidates for quantum computing solutions, since they are classically difficult and quantum algorithms seem to provide a substantial speedup. 

<figure>
  <img src="../images/QC_Opp_Fig2.png"
       alt="Quantum computing potential">
  <figcaption>
    Relative potential for applications of quantum computing.
    [<a href="https://doi.org/10.1007/s42979-021-00786-3">Giani 2021</a>]
  </figcaption>
</figure>

<script>MathJax.typeset();</script>
