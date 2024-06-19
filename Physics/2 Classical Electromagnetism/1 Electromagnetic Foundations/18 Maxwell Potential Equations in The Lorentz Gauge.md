Tags: [[17 Maxwell Equations in Potential Form]] [[16 Corrected Potentials and Gauge Transform]] [[Electromagnetism]] [[2 The Continuity Equation - Conservation of Any Flowing Substance]]
___
The maxwell's equations in potential form reduce to two, and the two potentials are mixed together. They appear in a quite complex and asymmetric form:
**The charge source law:**
$$-\nabla^2\phi-\frac{\partial}{\partial t}(\nabla\cdot\vec A)=+\frac{\rho}{\epsilon_0}$$
**The current source law:**
$$\left(\mu_0\epsilon_0\frac{\partial^2}{\partial t^2}-\nabla^2\right)\vec A+\nabla\left(\nabla\cdot\vec A+\mu_0\epsilon_0\frac{\partial\phi}{\partial t}\right)=\mu_0\vec J$$
## Gauge Fixing
Through choosing the appropriate gauge, which we are free to do ([[16 Corrected Potentials and Gauge Transform]]), we can simplify these equations. 
##### Lorentz Gauge
The lorentz gauge treats the **scalar potential like an energy density**, while **the vector potential is an energy current density** (with appropriate scaling). Thus, they satisfy the continuity equation ([[2 The Continuity Equation - Conservation of Any Flowing Substance]]): 
$$\boxed{\mu_0\epsilon_0\frac{\partial\phi}{\partial t}+\nabla\cdot\vec A=0}$$
Which is the definition of the **Lorentz gauge**. 

Thus the Maxwell's equations become much simpler:
**charge source law**:
$$\boxed{\left(\mu_0\epsilon_0\frac{\partial^2}{\partial t^2}-\nabla^2\right)\phi=\frac{\rho}{\epsilon_0}}$$
**current source law:**
$$\boxed{\left(\mu_0\epsilon_0\frac{\partial^2}{\partial t^2}-\nabla^2\right)\vec A=\mu_0\vec J}$$
Which is painfully elegant. The above equations are in fact spacetime laplacian equations, which suggest that charges and currents impose a potential over space-time like a hyperbolic harmonic drum. Alternatively, you can see this as they broadcast their potentials through space over time at the speed of $\frac{1}{\sqrt{\mu_0\epsilon_0}}=c$. 
## Potentials are Physically More Real Than Force Fields
The elegance and naturalness of the potentials is no accident. They are closer to reality than force fields are. See Aharonov-Bohm effect that proves it. ([[Aharonov-Bohm Effect]]) 