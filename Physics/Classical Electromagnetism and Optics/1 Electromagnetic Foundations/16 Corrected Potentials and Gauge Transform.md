Tags: [[Electromagnetism]] [[4 Electric Scalar Potential and Voltage]] [[12 Magnetic Vector Potential]] [[14 Maxwell Equation - Faraday's Law of Induction]] 
___
The Maxwell's Equations suggest that the electric potential must be altered. We also find that there is a degree of freedom in choosing the vector potential and the scalar potential. 
## Faraday's Law In Terms of Potentials 
Examine the local form. We can replace the magnetic field with the curl of its vector potential $\vec A$.
$$\nabla\times\vec E=-\frac{\partial}{\partial t}\nabla\times\vec A$$
Which suggests 
$$\vec E=-\frac{\partial\vec A}{\partial t}$$
## New Electric Field Understanding
So there are two sources of the electric field. 
1. It comes from the gradient of the scalar potential
2. In the absence of scalar potential gradient, it can come as the time rate of change of the magnetic vector potential. 
Thus:
$$\vec E=-\nabla \phi-\frac{\partial \vec A}{\partial t}$$
Which is the corrected version of $\vec E=-\nabla \phi$.
## A Degree of Freedom in the Potentials
We know that the magnetic potential is defined such that:
$$\vec B=\nabla\times\vec A$$
But similar to the electric scalar potential being free to choose any reference level as 0, the magnetic vector potential is not unique. 

We can overlay the vector potential field with any gradient field $\nabla\chi$ i.e. $\vec A^\prime=\vec A+\nabla\chi$, and the resultant magnetic field is unaffected. Substitute the original potential as the new potential *minus* the gradient field gives:
$$\vec B=\nabla\times(\vec A^\prime-\nabla \chi)=\vec B=\nabla\times\vec A^\prime-\nabla\times\nabla\chi=\nabla\times\vec A^\prime$$
Where we used our understanding that gradient fields are irrotational. What we have just performed is a **gauge transformation**. 

If the magnetic vector potential is free to take on a gradient field, how would that affect the electric field? 
$$\vec E=-\nabla\phi-\frac{\partial(\vec A^\prime-\nabla\chi)}{\partial t}=
-\nabla\phi+\nabla\frac{\partial\chi}{\partial t}-\frac{\partial\vec A^\prime}{\partial t}=
-\nabla\left(\phi-\frac{\partial \chi}{\partial t}\right)-\frac{\partial\vec A^\prime}{\partial t}$$
But the electric field must remain the same, which means the scalar potential must be corrected in tandem. The correction is $\phi^\prime=\phi-\frac{\partial\chi}{\partial t}$. 
## Summary
The gauge transformations of the electric scalar potential and the magnetic vector potential that would leave the electric and magnetic fields invariant is:
$$\boxed{\vec A^\prime=\vec A+\nabla\chi}\ \ \ \ \ \ and\ \ \ \\ \ \ \boxed{\phi^\prime=\phi-\frac{\partial\chi}{\partial t}}$$
While the fields can be obtained by:
$$\boxed{\vec B=\nabla\times\vec A}\ \ \ \ \ \ \ and\ \  \ \ \ \ \boxed{\vec E=-\nabla \phi-\frac{\partial \vec A}{\partial t}}$$
