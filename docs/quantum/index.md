# Overview of Quantum Computing

It’s important to recognize that quantum computers can not solve every problem
exponentially faster than classical computers
[[Giani 2021](https://doi.org/10.1007/s42979-021-00786-3)]. Many problems exist
in the same complexity class for quantum computers as they do for classical
computers, and given the expense of quantum hardware and typically
longer-running elementary operations, it is important to judiciously select the
problems on which quantum computing is brought to bear.

Quantum complexity theory is not yet developed enough to know for certain whether any exponential quantum speedups exist [[Giani 2021](https://doi.org/10.1007/s42979-021-00786-3)]. (Note: Is that really true? Or is it just that we don’t know for sure that P != NP) For instance, it was once thought that a recommendation algorithm had a large quantum speedup over classical, but in 2018 an undergraduate student discovered a classical algorithm that eliminates the quantum advantage [[Giani 2021](https://doi.org/10.1007/s42979-021-00786-3)].

Shor’s algorithm is a method of factoring large numbers and is part of a family of algorithms for solving “hidden subgroup” problems. It would be capable of breaking some modern cryptographic schemes, like RSA. [[Giani 2021](https://doi.org/10.1007/s42979-021-00786-3)]

Specifying a classical state of N bits requires N classical bits, but specifying the quantum state of N qubits requires 2^N numbers. [[Giani 2021](https://doi.org/10.1007/s42979-021-00786-3)]

Polynomial speedup vs. exponential speedup

While classical computer information is entirely binary, quantum information can take advantage of superposition, entanglement and interference. Quantum computing is only likely to have an advantage over classical computing for algorithms that can make use of these properties. [[Giani 2021](https://doi.org/10.1007/s42979-021-00786-3)]
