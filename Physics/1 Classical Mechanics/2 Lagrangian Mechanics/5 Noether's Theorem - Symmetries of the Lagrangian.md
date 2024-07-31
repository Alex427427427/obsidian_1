Category: [[Classical Mechanics]] [[Lagrangian Mechanics]]
___
Prerequisites: [[2 Euler Lagrange Equation]] [[3 Change of Coordinates for Lagrangian]]
___
Related: 
___
## Constant of Motion
Defined as $F$ for which: 
$$\boxed{\frac{dF}{dt}=\sum_i\left(\frac{\partial F}{\partial q^i}\dot q^i+\frac{\partial F}{\partial\dot q^i}\ddot q^i\right)+\frac{\partial F}{\partial t}=0}$$
## Symmetry
Consider a one-parameter transformation
$$\boxed{q^i(t)\rightarrow Q^i(s,t)}$$
such that $Q^i(0,t)=q^i(t)$. Then this transformation is a *symmetry* of the Lagrangian $L$ if 
$$\boxed{\frac{\partial}{\partial s}L(Q^i(s,t),\dot Q^i(s,t),t)=0}$$
## Noether's Theorem
**There exists a conserved quantity - constant of motion - for every continuous symmetry**. It has a particular functional form that will be derived along with the proof of the theorem. 
##### Proof
$$\frac{\partial L}{\partial s}=\frac{\partial L}{\partial Q^i}\frac{\partial Q^i}{\partial s}+\frac{\partial L}{\partial \dot Q^i}\frac{\partial \dot Q^i}{\partial s}=0$$
At $s=0$, above must still hold. 
$$0=\left.\frac{\partial L}{\partial Q^i}\frac{\partial Q^i}{\partial s}\right|_{s=0}+\left.\frac{\partial L}{\partial \dot Q^i}\frac{\partial \dot Q^i}{\partial s}\right|_{s=0}$$
$$=\left.\frac{\partial L}{\partial q^i}\frac{\partial q^i}{\partial Q^i}\frac{\partial Q^i}{\partial s}\right|_{s=0}+\left.\frac{\partial L}{\partial \dot q^i}\frac{\partial \dot q^i}{\partial \dot Q^i}\frac{\partial \dot Q^i}{\partial s}\right|_{s=0}$$
The only way to construct one parameter maps that start as the original coordinates, will lead to the rate of change between the new and old coordinates be 1 as the parameter goes to 0. Thus: 
$$0=\left.\frac{\partial L}{\partial q^i}\frac{\partial Q^i}{\partial s}\right|_{s=0}+\left.\frac{\partial L}{\partial \dot q^i}\frac{\partial \dot Q^i}{\partial s}\right|_{s=0}$$
Now use the Euler-Lagrange equation. 
$$0=\left.\left(\frac{d}{dt}\frac{\partial L}{\partial\dot q^i}\right)\frac{\partial Q^i}{\partial s}\right|_{s=0}+\left.\frac{\partial L}{\partial \dot q^i}\frac{\partial \dot Q^i}{\partial s}\right|_{s=0}$$
Commute the time and $s$ derivatives in the second term and combine the whole equation using the product rule. 
$$0=\left.\left(\frac{d}{dt}\frac{\partial L}{\partial\dot q^i}\right)\frac{\partial Q^i}{\partial s}\right|_{s=0}+\left.\frac{\partial L}{\partial \dot q^i}\left(\frac{d}{dt}\frac{\partial Q^i}{\partial s}\right)\right|_{s=0}$$
$$\boxed{0=\frac{d}{dt}\left(\frac{\partial L}{\partial\dot q^i}\left.\frac{\partial Q^i}{\partial s}\right|_{s=0}\right)}$$
The quantity $(\partial L/\partial\dot q^i)(\partial Q^i/\partial s)$ evaluated at $s=0$ is constant for all time. Of course, this implies the sum over all coordinates is also constant for all time. 
## Homogeneity of Space - Momentum Conservation
A translation in space means $Q=q+s$ and $q=x$, which, if leaves the Lagrangian unchanged, leads to the conserved quantity reducing to $\partial L/\partial\dot x$, the momentum. 

Note that this was already apparent in the Euler-Lagrange Equation. But here we can see it play out in a different way: 
$$\vec r \rightarrow\vec r+s\vec n$$
$$\frac{\partial L}{\partial\dot{\vec r}}\cdot\vec n=\vec p\cdot\vec n$$
So we see that if the Lagrangian is invariant under translation in one direction, then momentum will be conserved along that particular direction. 
## Isotropy of Space - Angular Momentum Conservation
Consider a single particle with spatial position $\vec r$ in 3D. An infinitesimal rotation to first order is:
$$\vec r\rightarrow\vec r+s\hat n\times\vec r$$
$$\dot{\vec r} \rightarrow\dot{\vec r}+s\hat n\times\dot{\vec r}$$
Thus the conserved quantity is: 
$$\frac{\partial L}{\partial\dot{\vec r}}\cdot(\hat n\times\vec r)=\vec p\cdot(\hat n\times\vec r)=\hat n\cdot(\vec r\times\vec p)=\hat n\times\vec L$$
Where we have used Noether's theorem, vector calculus, and the permutation of a parallelopiped's major axes. 

Note that rotational symmetry along an axis $\hat n$ leads to conservation of angular momentum along that axis. 
## Homogeneity of Time - Energy Conservation
This is harder to directly apply Noether's theorem, because the main formula for the conserved quantity is for the coordinate symmetries, not time. Nevertheless, there is a quantity that corresponds to energy. 

Let's first look at what $d L/d t$ usually is. 
$$\frac{d L}{d t}=\frac{\partial L}{\partial q^i}\dot q^i+\frac{\partial L}{\partial \dot q^i}\ddot q^i+\frac{\partial L}{\partial t}$$
Which, if there is no explicit time dependence in the Lagrangian, becomes
$$\frac{d L}{d t}=\frac{\partial L}{\partial q^i}\dot q^i+\frac{\partial L}{\partial \dot q^i}\ddot q^i$$
So if we discover another nontrivial quantity that returns this same time derivative, we can substract that with $L$ to reach an expression that is conserved. First, apply the Euler-Lagrange equation: 
$$\frac{d L}{d t}=\frac{d}{dt}\frac{\partial L}{\partial\dot q^i}\dot q^i+\frac{\partial L}{\partial \dot q^i}\ddot q^i$$
Now apply the product rule: 
$$\frac{d L}{d t}=\frac{d}{dt}\left(\frac{\partial L}{\partial\dot q^i}\dot q^i\right)$$
There we have it. If we now define a new quantity $H$, it will have a time derivative of 0 and be a conserved quantity:
$$H=\frac{\partial L}{\partial\dot q^i}\dot q^i-L$$
$$\boxed{H=p_i\dot q^i-L\ \ \ \ \ \ \ where\ \ \ \ \ \ \ p_i=\frac{\partial L}{\partial \dot q^i}}$$
It is called the Hamiltonian. A whole new mechanics can be built on this quantity, in place of the Lagrangian. Notice that according to the rule of tensors ([[6 Tensor Calculus]]), momentum is a co-vector. Note there is a hidden sum because of the Einstein summation notation ([[3 Einstein's Summation Notation]]). 

What could this quantity be? If we apply it to a system that is a single particle in space, we have: 
$$\boxed{H=T+V}$$
So it's the total energy. 