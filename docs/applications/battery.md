# Energy Storage and Battery Technology

Quantum computing may be applied to computational materials design for batteries. [[Ho 2018](https://doi.org/10.1016/j.joule.2018.04.021)] Properties and integration of a battery's materials (determined by chemical behavior) determine performance and cost. Prediction of materials and designs may be determined by solutions to Schrodinger's equation for the electrons involved in the chemistry. It may help to create safer or lighter batteries, or to find replacements for rare and expensive materials.

Reliable and cheap energy storage will be required at an increasing pace as renewables come online.

Density Functional Theory (DFT) has given accurate predictions in the development of materials for Li-Ion batteries, hydrogen production, superconductors, photovoltaics and thermoelectrics. For Li-Ion batteries, it has been used to calculate cell voltages, ionic mobility and thermo and chemical stability, allowing predicions of energy density, charging/discharging time, safety and cycle life.

DFT is an approximation and requires the choice of a set of exchange-correlation functionals, but this choice affects accuracy and requires highly specialized knowledge. DFT and other methods, such as quantum Monte Carlo and tensor networks are reaching their technical limits, and quantum computing algorithms are expected to scale similarly to DFT methods but provide a method for computing exact solutions without worrying about [the sign problem](https://en.wikipedia.org/wiki/Numerical_sign_problem) explicitly storing the wave function. These algorithms are also fairly general, so do not require the same level of specialized knowledge to implement as DFT.

Quantum algorithms can simulate strongly correlated states and complex interfacial systems like those in a battery.

Some quantum algorithms may require a fully fault-tolerant quantum computer, but great progress has been made toward algorithms that are robust to errors, and the complexity of state-of-the art algorithms improved from O(n^11) in 2013 to O(n^3) in 2017, with n the number of electron orbitals involved in the system.

[[Ho 2018](https://doi.org/10.1016/j.joule.2018.04.021)] estimate that quantum
algorithms may become more useful than classical approaches when around 128 or more orbitals are involved. While current quantum algorithms would require a circuit depth of around 1 million to solve these systems, current hardware may be capable of a circuit depth of around 100-1,000.