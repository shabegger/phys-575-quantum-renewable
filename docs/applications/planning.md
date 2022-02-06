# Planning and Dispatch

Planning on several time scales: immediate (daily operations), day-ahead planning, capital improvements over coming years. Given a particular demand, would like to find the cheapest way to meet that demand given constraints on, for example, transmission, safety and reliability and environmental policy. [[Giani 2021](https://doi.org/10.1007/s42979-021-00786-3)]

Optimal Power Flow (OPF) problems are highly constrained quadratic optimization problems, simultaneously balancing real (power dissipated by the resistances in a circuit) and reactive power (Volt-Amps Reactive, due to inductors and capacitors dropping voltage/drawing current). The power flow equations are nonlinear and difficult to solve and becomes more difficult when many nodes in the system are actively providing electrical energy, as with, for example, rooftop solar. [[Giani 2021](https://doi.org/10.1007/s42979-021-00786-3)]

On the scale of years, integrated resource planning tries to solve the problem of building transmission capabilities and generation capacity to meet future demand. However, the availability of highly dispersed resources is impossible to predict, and as a result more efficient and robust resource allocation algorithms are required. [[Giani 2021](https://doi.org/10.1007/s42979-021-00786-3)]

The electrical grid is becoming smarter, with more sensors and storage, as well as devices that can control demand in response to need or utility price (smart home?). New sources of demand, such as electric vehicles also factor in. All of this increases the complexity of the problem by adding new variables, and traditional computing strategies are having an increasingly difficult time with these issues. [[Giani 2021](https://doi.org/10.1007/s42979-021-00786-3)]

Scheduling and dispatch problems are known to be NP-hard (a system with N nodes can not be solved for in time polynomial in N). Approximations and heuristics are used. For instance, DC OPF is a linearization of AC OPF that assumes constant voltages. Assumptions may be made about impedance properties of the network to decouple some variables. These heuristics can solve the problems in a reasonable time, but inaccuracies could lead to inefficiencies or errors. [[Giani 2021](https://doi.org/10.1007/s42979-021-00786-3)]

Quantum annealing relies on directly encoding the problem into a quantum energy landscape. QAOA provides approximate solutions using a classical optimization loop. However, more research is needed to understand the potential benefits of quantum computing and to verify the benefit experimentally. [[Giani 2021](https://doi.org/10.1007/s42979-021-00786-3)]

Quantum optimization could be applied to scheduling and dispatch to provide energy reliably and efficiently. [[Giani 2021](https://doi.org/10.1007/s42979-021-00786-3)]
