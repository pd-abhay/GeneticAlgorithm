Genetic Algorithm (GA) is a metaheuristic optimization technique inspired by the principles of natural selection and evolution. It is commonly used to solve complex optimization and search problems where traditional methods may fail.

 Key Concepts:
* Population: A set of potential solutions (individuals).
* Chromosome: A representation of a solution (often as a string of bits or numbers).
* Fitness Function: Evaluates how good each solution is.
* Selection: Chooses the fittest individuals to pass on their genes.
* Crossover (Recombination): Combines parts of two parents to produce offspring.
* Mutation: Randomly alters genes to maintain diversity in the population.
* Generation: A new population formed after applying selection, crossover, and mutation.

How it Works:
* Initialize a random population of candidate solutions.
* Evaluate each solution using the fitness function.
* Select the best-performing individuals.
* Apply crossover and mutation to create a new generation.
* Repeat steps 2–4 for several generations or until a stopping criterion is met.

Signs of Premature Convergence:
* Loss of genetic diversity: If you track the average Hamming distance between individuals’ genomes and see it drop precipitously (say, below 5 % of the chromosome length), that suggests the population has become too uniform.
* Flat fitness over many generations: While GA plateaus more slowly than PSO, a flat line for 20+ generations with no improvement can also signal premature convergence—especially if mutation rate is low.

Effects of various Hyperparameters:
* Crossover rate (p_n): High p_c (>0.8) promotes mixing of good schemata—faster progress but can disrupt building blocks; low p_n (<0.5) slows search. Use crossover rate pₙ ≈ 0.7–0.9 for effective recombination.
* Mutation rate (p_m): Small p_m (≈0.01–0.05) maintains diversity; too low → premature convergence, too high → random search. Keep mutation rate pₘ ≈ 0.01–0.05 to maintain diversity.
* Critical: Mutation rate is paramount for avoiding genetic drift and maintaining long‑term progress.

In very high‑dimensional spaces, Genetic Algorithms often edge out the others because their population‑based crossover can recombine useful subspaces without getting trapped by the “curse of dimensionality” as quickly.
