Category: [[Classical Mechanics]] [[Lagrangian Mechanics]]
___
Prerequisites: [[1 Lagrangian, Action, Principle of Stationary Action]]
___
Related: [[5 How Tensors Transform]]
___
From the action principle it immediately follows that the Euler-Lagrange equation ([[2 Euler Lagrange Equation]]) holds in any coordinate system. The most basic coordinate system is one with $3N$ dimensions for $N$ particles, each dimension measuring one spatial coordinate for a particle. Let's introduce new coordinates $q^a$ which can be a function of all the basic coordinates, plus time:
$$q^i=q^i(x^1,...,x^{3N},t)$$
By the chain rule, (or alternatively, tangent space linearisation):
$$\boxed{\dot q^i=\frac{\partial q^i}{\partial x^j}\dot x^j+\frac{\partial q^i}{\partial t}}$$
The term $\frac{\partial q^i}{\partial x^j}$ is in fact the **Jacobian**, a rank (1,1) tensor that maps vectors to vectors. 
$$\boxed{{J^i}_j=\frac{\partial q^i}{\partial x^j}}$$
To replace the coordinates of an equation with new ones, we must *figure out the inverse transformation*, that allows us to substitute the original coordinate variables as the inverse transformation of the new coordinates. So
$$x^i=x^i(q^1,...,t)$$
$$\boxed{\dot x^i=\frac{\partial x^i}{\partial q^j}\dot q^j+\frac{\partial x^i}{\partial t}}$$
Another Jacobian can be defined for this inverse transform: 
$$\boxed{{J^i}_j=\frac{\partial x^i}{\partial q^j}}$$
And you will find that this jacobian is the transpose of the forward transform jacobian, along with inverting every entry. 

Also notice how, from the inverse transform equation, we can see that: 
$$\boxed{\frac{\partial \dot x^i}{\partial \dot q^j}=\frac{\partial x^i}{\partial q^j}}$$
## Demonstrate that Change of Coordinates Leaves Lagrangian Mechanics Invariant
We already know this to be true from principle, but let's see how it plays out in action. The generalised force term: 

$$\frac{\partial L}{\partial q^i}=\frac{\partial L}{\partial x^j}\frac{\partial x^j}{\partial q^i}+\frac{\partial L}{\partial \dot x^j}\frac{\partial}{\partial q^i}\dot x^j=\frac{\partial L}{\partial x^j}\frac{\partial x^j}{\partial q^i}+\frac{\partial L}{\partial \dot x^j}\left(\frac{\partial^2x^j}{\partial q^i\partial q^a}\dot q^a+\frac{\partial^2x^j}{\partial q^i\partial t}\right)$$
The time derivative of the generalised momentum term: 
$$\frac{d}{dt}\frac{\partial L}{\partial\dot q^i}=\frac{d}{dt}\left(\frac{\partial L}{\partial \dot x^j}\frac{\partial\dot x^j}{\partial \dot q^i}+\frac{\partial L}{\partial x^j}\frac{\partial x^j}{\partial\dot q^i}\right)=\frac{d}{dt}\left(\frac{\partial L}{\partial \dot x^j}\frac{\partial\dot x^j}{\partial \dot q^i}\right)$$
Since $x$ is independent of $\dot q$, the second term goes to 0. Then the first term can be exapnded with the product rule: 
$$\frac{d}{dt}\frac{\partial L}{\partial\dot q^i}=\left(\frac{d}{dt}\frac{\partial L}{\partial \dot x^j}\right)\frac{\partial\dot x^j}{\partial \dot q^i}+\frac{\partial L}{\partial \dot x^j}\left(\frac{d}{dt}\frac{\partial\dot x^j}{\partial \dot q^i}\right)$$
Since the partial derivative of the velocities is the same as the partial derivative of the coordinates,
$$\frac{d}{dt}\frac{\partial L}{\partial\dot q^i}=\left(\frac{d}{dt}\frac{\partial L}{\partial \dot x^j}\right)\frac{\partial x^j}{\partial q^i}+\frac{\partial L}{\partial \dot x^j}\left(\frac{d}{dt}\frac{\partial x^j}{\partial q^i}\right)$$
Since $\frac{d}{dt}\frac{\partial x^j}{\partial q^i}=\frac{\partial}{\partial q^i}{\dot x^j}$ because the derivatives commute, this bracketed term becomes the same as the bracketed term from the first equation in this section:
$$\frac{d}{dt}\frac{\partial L}{\partial\dot q^i}=\left(\frac{d}{dt}\frac{\partial L}{\partial \dot x^j}\right)\frac{\partial x^j}{\partial q^i}+\frac{\partial L}{\partial \dot x^j}\left(\frac{\partial^2x^j}{\partial q^i\partial q^a}\dot q^a+\frac{\partial^2x^j}{\partial q^i\partial t}\right)$$
Combining our results, we get: 
$$\boxed{\frac{\partial L}{\partial q^i}-\frac{d}{dt}\frac{\partial L}{\partial\dot q^i}=\left(\frac{\partial L}{\partial x^j}-\frac{d}{dt}\frac{\partial L}{\partial \dot x^j}\right)\frac{\partial x^j}{\partial q^i}}$$
Which means that if the euler lagrange equation is solved in the $x$ coordinate system, it is also solved in the $q$ coordinate system. 