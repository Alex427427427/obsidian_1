Category: [[Classical Mechanics]] [[Lagrangian Mechanics]]
___
Prerequisites: [[3 Change of Coordinates for Lagrangian]] [[2 Euler Lagrange Equation]] [[1 Lagrangian, Action, Principle of Stationary Action]]
___
Related: 
___
## Constraints
Constraints are relationships between the coordinates that restrict how they can change. Every constraint is expressible in an equation that involves the coordinates, and every constraint kills a degree of freedom. 
##### Holonomic Constraints
Of particular interest are **holonomic constraints** - constraints on the coordinates (which may be time dependent), but not on the velocities. 
$$f_\alpha (x^j,t)=0$$
A generalised coordinate $q^i$ can be assigned to every degree of freedom. After the constraints, suppose there are $n$ degrees of freedom left. 
## Explicitly Working with Constraints - using Lagrange Multipliers
We can extend the Lagrangian with *Lagrange Multipliers* $\lambda_\alpha$ as additional coordinates: 
$$\boxed{L^\prime=L(x^j,\dot x^j)+\lambda_\alpha f_\alpha (x^j,t)}$$
Treating these multipliers as genuine coordinates, gives the following equations: 
$$\boxed{\frac{\partial L^\prime}{\partial\lambda_\alpha}=f_\alpha(x^j, t)=\frac{d}{dt}\frac{\partial L^\prime}{\partial\dot\lambda_\alpha}=0}$$
From which we recover the constraints. 

Furthermore, the original coordinates gain new equations of motion that has the constraints built in: 
$$\frac{\partial L^\prime}{\partial x^j}-\frac{d}{dt}\frac{\partial L^\prime}{\partial\dot x^j}=0$$
$$\frac{\partial L}{\partial x^j}+\lambda_\alpha\frac{\partial L}{\partial x^j}-\frac{d}{dt}\frac{\partial L}{\partial\dot x^j}=0$$
$$\boxed{\frac{d}{dt}\frac{\partial L}{\partial\dot x^j}-\frac{\partial L}{\partial x^j}=\lambda_\alpha\frac{\partial L}{\partial x^j}}$$
Of course, choosing the right generalised coordinates $q$ will remove the need to deal with these constraints explicitly. 
## General Optimisation Problems
Outside of physics, this approach is also applicable to constrained optimisation problems - where the action $S$ is the variable that needs to be optimized, expressible as an integral of some lagrangian $L$ over a parameter $t$. The constraints can then be added in, expressible in the same integral over $t$, along with a multiplier. This creates a new action $S^\prime$ that, under the euler lagrange equation, spits out the equations that optimise $S$ under the constraints. 
