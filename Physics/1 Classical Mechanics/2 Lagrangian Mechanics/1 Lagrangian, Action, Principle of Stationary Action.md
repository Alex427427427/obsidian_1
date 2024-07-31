Category: [[Classical Mechanics]] [[Lagrangian Mechanics]]
___
Prerequisites: 
___
Related: 
___
## Configuration Space
The space where each dimension is the available values for a degree of freedom of a system. For example, the position of every particle in an N particle system forms a 3N dimensional configuration space. 
## Generalised Coordinates
Part of the power of Lagrangian mechanics is that it does away with vectors in space in favour of general coordinates. If a configuration can be parameterised by a set of variables $q$, then those can form the configuration space, instead of the positions of all particles. Suddenly, constraints are put in the background and don't have to be explicitly treated. 
## Lagrangian
A property of a system at a point in time, $L$. Defined to be the kinetic energy $T$ within the system take away the potential energy $V$.
$$\boxed{L(q^a,\dot q^a)=T(\dot q^a)-V(q^a)}$$
Note that in most cases this equation does not explicitly depend on time, but only depends on time indirectly when $q$ and $\dot q$ depend on time. 

Also note that we adopt the einstein notation ([[3 Einstein's Summation Notation]]), where indices are enough to denote an entire set. 
## Action
A property $S$ of a path that a system takes in configuration space over time. Defined to be the integral of the Lagrangian over the path. 
$$\boxed{S[q^a(t)]=\int_{t_1}^{t_2}L(q^a(t),\dot q^a(t))\ dt}$$
## Principle of Stationary Action
We now encounter the one law that is the closest to a theory of everything that we have. All modern fields of physics are described in terms of this principle -

**A system evolves through the configuration space along a path that makes the action an extremum with respect to the choice of path**. (Mostly, minimises)
$$\boxed{\delta S[q^a_{real}(t)]=0}$$
**This principle remains invariant if the Lagrangian is scaled or shifted by a constant.**
## Interpretation
##### Background
It is commonly believed that there is no intuition for what the Lagrangian represents, other than that it produces another quantity when integrated along a path in configuration space, which follows an axiomatic optimisation principle that happens to describe reality. 

This is an unfortunate result of the historical choice of the definition of the Lagrangian. Kinetic energy minus potential energy, while the simplest choice to satisfy the stationary action principle, obscures the underlying idea which the Lagrangian represents. 

There is also a rumor that the principle of least action represents the least amount of energy transfer from potential to kinetic and vice versa, by inspecting the form of the Lagrangian $T-V$. Unfortunately this view breaks apart upon scrutiny, but it gets closer to the truth - that the action is *some* kind of measure of *change*. 
##### Action = Phase Change, Lagrangian = Rate of Phase Change
The Lagrangian is a measure of **action rate** - how much action is occuring per unit time. 

And what is action? A full understanding will have to wait for quantum mechanics ([[Quantum Mechanics]]) and relativity ([[Relativity]]). See [[0 Discrete Action Relationships]]. But the short answer is here - **the action is a measure of phase change in the rest frame of a particle** - consider a harmonic de broglie wave in spacetime. So the principle of least action is the **principle of least phase change**. And the **Lagrangian is a measure of the rate at which phase is changing**. 
