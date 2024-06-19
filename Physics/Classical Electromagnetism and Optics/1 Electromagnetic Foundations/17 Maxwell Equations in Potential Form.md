Tags: [[13 Maxwell Equation - Ampere's Law]] [[11 Maxwell Equation - Gauss' Law for Magnetism]] [[5 Maxwell Equation - Gauss' Law for Electricity]] [[14 Maxwell Equation - Faraday's Law of Induction]] [[16 Corrected Potentials and Gauge Transform]]
___
## The Laws
##### Electric Gauss Law
$$\nabla\cdot\vec E=\frac{\rho}{\epsilon_0}$$
$$\nabla\cdot\left(-\nabla\phi-\frac{\partial\vec A}{\partial t}\right)=\frac{\rho}{\epsilon_0}$$
$$-\nabla^2\phi-\frac{\partial}{\partial t}(\nabla\cdot\vec A)=\frac{\rho}{\epsilon_0}$$
##### Magnetic Gauss Law
This law is eliminated due to the definition of the vector potential. [[12 Magnetic Vector Potential]]
##### Faraday's Induction Law (Electric Ampere Law)
$$\nabla\times\vec E=-\frac{\partial\vec B}{\partial t}$$
$$\nabla\times\left(-\nabla\phi-\frac{\partial\vec A}{\partial t}\right)=-\frac{\partial}{\partial t}(\nabla\times\vec A)$$
Which is a tautology due to gradient fields having no vorticity. Like the magnetic gauss law, this law is eliminated by virtue of defining the potentials. 
##### Magnetic Ampere Law
$$\nabla\times\vec B=\mu_0\vec J+\mu_0\epsilon_0\frac{\partial\vec E}{\partial t}$$
$$\nabla\times(\nabla\times\vec A)=\mu_0\vec J+\mu_0\epsilon_0\frac{\partial}{\partial t}\left(-\nabla\phi-\frac{\partial\vec A}{\partial t}\right)$$
$$\nabla(\nabla\cdot\vec A)-\nabla^2\vec A=\mu_0\vec J-\mu_0\epsilon_0\nabla\frac{\partial\phi}{\partial t}-\mu_0\epsilon_0\frac{\partial^2\vec A}{\partial t^2}$$
$$\left(\mu_0\epsilon_0\frac{\partial^2}{\partial t^2}-\nabla^2\right)\vec A+\nabla\left(\nabla\cdot\vec A+\mu_0\epsilon_0\frac{\partial\phi}{\partial t}\right)=\mu_0\vec J$$
##### Summary
We see now that the maxwell's equations in potential form have reduced to two, and the two potentials are mixed together. 

**The charge source law:**
$$\boxed{-\nabla^2\phi-\frac{\partial}{\partial t}(\nabla\cdot\vec A)=+\frac{\rho}{\epsilon_0}}$$
**The current source law:**
$$\boxed{\left(\mu_0\epsilon_0\frac{\partial^2}{\partial t^2}-\nabla^2\right)\vec A+\nabla\left(\nabla\cdot\vec A+\mu_0\epsilon_0\frac{\partial\phi}{\partial t}\right)=\mu_0\vec J}$$
