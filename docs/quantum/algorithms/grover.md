# Grover's Algorithm

Grover’s algorithm uses a technique in quantum computing called amplitude amplification for database search [[Giani 2021](https://doi.org/10.1007/s42979-021-00786-3)]. Whereas the classical algorithm takes time proportional to the size of the database, <math><mi>N</mi></math> for a full search (i.e. without, say, indexing), Grover’s algorithm takes time proportional to the square root of <math><mi>N</mi></math>. The algorithm is given an oracle function capable of distinguishing the entry or entries it is searching for and a quantum state initialized with all elements in the database. Over a series of steps, the algorithm moves from a state with a constant probability over all entries to one that selects the desired entry with high probability.

Grover's algorithm assumes access to a large quantum RAM (random-access memory), which is currently unproven experimentally. [[Giani 2021](https://doi.org/10.1007/s42979-021-00786-3)]

<script>MathJax.typeset();</script>
