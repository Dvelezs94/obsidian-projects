## Evolutionary Algorithm
EA's are essential to [[Evolutionary Computing]].

In essence, EA's try to mimic the game of life insructions.

There are many variants for EAs, but the common underlying idea is: given a population with individials in some environment that has limited resources, competition for those resources causes [[Natural selection]]. This in turn causes a rise in the fitness of the population. Given a quality function to be maximised, we can randomly create a set of candidate solutions, i.e., elements of the function’s domain. We then apply the quality function to these as an abstract fitness measure – the higher the better. On the basis of these fitness values some of the better candidates are chosen to seed the next generation. This is done by applying recombination and/or mutation to them. Recombination is an operator that is applied to two or more selected candidates (the so-called parents), producing one or more new candidates (the children). Mutation is applied to one candidate and results in one new candidate. Therefore executing the operations of recombination and mutation on the parents leads to the creation of a set of new candidates (the offspring). These have their fitness evaluated and then compete – based on their fitness (and possibly age) – with the old ones for a place in the next generation. This process can be iterated until a candidate with sufficient quality (a solution) is found or a previously set computational limit is reached.

![[Pasted image 20220930134003.png]]
EA pseudocode

- EAs are population based, i.e., they process a whole collection of candidate solutions simultaneously. 
- Most EAs use recombination, mixing information from two or more candidate solutions to create a new one. 
- EAs are stochastic.
![[Pasted image 20220930140203.png]]


Most EA's are petty much the same, most differences (not always) are in the data structure to represent the population characteristics. This is because depending on the problem it might be easier and faster to encode/decode the information at a candidate level. **Speed is key** in these kind of algorithms due to the fact that we can fast forward evolution if the program can handle it.
It is important to keep in mind that [[Fitness]] will always be the same, regardless of the strategy used to encode the DNA.

## Components
Certain components, procedures and operators need to be defined for an EA. These are:
1. Representation - Frame the problem
2. Evaluation function - Fitness on the environment
3. Population - Representation of possible solutions
4. Parent selection mechanism - Who gets to reproduce
5. Variation operators, recombination and mutation - For newborns
6. Survivor selection mechanism - Who dies

## Terms

### Representation
This is the first design step. Representation is basically mapping the original problem to a problem-solving space. It is how you represent the problem for the computer to hopefuly evolve and find the best solution.

It often involves simplifying or abstracting the problem you are attempting to solve into a well-defined and tangible problem context whithin which *possible solutions can exist and be evaluated* <- This forces the programmer to know the problem really well and frame it properly.

### Fitness Function
This function indicates what "improvement" means. From the problem-solving perspective, it represents the task to be solved in the evolutionary context.

Warning: in [[Evolutionary Computing]] the term Fitness Function and Objective function often are pretty close, but not always the same. We could have an Objective function which is a math function that could calculare the error rate for example, so the objective is to minimize that, while fitness is related to each candidate, and the higher, the better fit to its environment.

### Population
The role of population is to hold (the representation of) possible solutions.
Population forms the unit of evolution. Individuals are static objects that do not change or adapt; it is the population that does.

There are many ways to represent the population. It could simply be the collection of individuals. On some sophisticated EAs population can have spatial structures or a neightbothood relation.

The *diversity* of a population is the number of different present solutions in it (the population size in some cases)

 ### Parent Selection Mechanism
 This is the mechanism in charge of deciding who gets to be a parent for the future generation. Often this is often a probabilistic measure depdending on the phenotype and thus fitness where high-quality individuals are more likely to reproduce. It is important to mention that low-quality individuals also have a low positive probability to reproduce as well.

### Variation Operators
Variation operators role is to create new individuals from old ones. They are the rules that define the resulting genotype from evolution.
#### Mutation
It represents a very low random probability for an allele to be modified.

#### recombination
Recombination is the mechanism utilized to combine 2 genotypes into 1. This only happens when there is more than 1 parent involved in the reproduction of an offspring.

Both mutation and recombination can exist in EA's, however recombination is more often used than mutation.

The biology of the planet Earth, where, with very few exceptions, lower organisms reproduce asexually and higher organisms reproduce sexually, suggests that recombination is the superior form of reproduction.

### Survivor selection mechanism
This defines who will live the next generation. This runs after the offspring creation.
This decision is often assesed with the "Fitness function", favouring those with higuer values. Survivor selection is often deterministic

Survivor selection is often called *replacement strategy*.

