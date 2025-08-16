Category: [[Classical Mechanics]]
___
### Continuous symmetry and conservation laws
1. Express the continuous symmetry as a one-parameter $s$ infinitesimal transformation on the coordinates. This results in some function $f_i$ for each coordinate $q_i$, as a function of all coordinates $q$: 
$$\delta{q_i}=f_i(q)s$$
		where $f_i=\partial {q_i}^{'}/\partial s$, and ${q_i}^{'}=q_i + \delta q_i$
2. Expand infinitesimal change in (a time invariant) Lagrangian $\mathcal L$:
$$\delta\mathcal L=\sum_i \frac{\partial\mathcal L}{\partial q_i}\delta q_i+\frac{\partial\mathcal L}{\partial \dot q_i}\delta \dot q_i$$
3. Substitute:
$$\delta\mathcal L=\sum_i \frac{\partial\mathcal L}{\partial q_i}f_is+\frac{\partial\mathcal L}{\partial \dot q_i}\delta \dot f_i s$$
4. Use Euler Lagrange ([[2 Euler Lagrange Equation]]) and canonical momentum $p_i=\frac{\partial\mathcal L}{\partial \dot q_i}$:
$$\delta\mathcal L=\sum_i \dot p_i f_is+p_i \dot f_i s$$
5. Use product rule:
$$\delta\mathcal L/s=\frac{d}{dt}\sum_i (p_if_i)$$
6. Suppose the transformation leaves the lagrangian invariant:
$$\frac{d}{dt}\sum_i (p_if_i)=0$$
7. Thus the sum 
$$\sum_i p_if_i$$
is a constant of motion. A conserved quantity. More explicitly:
$$\boxed{\sum_i \frac{\partial\mathcal L}{\partial\dot q_i}\frac{\partial{q_i}^{'}}{\partial s}=\vec p \cdot\vec v}$$
where $\vec v$ is the velocity of the system in configuration space, under the continuous transformation. 
### Hamiltonian 
Expand time derivative of Lagrangian. Substitute momenta. Rearrange to find a quantity that doesn't change with time. That quantity is: 
$$\sum_ip_i\dot q_i-\mathcal L:=\mathcal H$$
The equations of motion are obtained by taking partial derivative of $\mathcal H$ with respect of the coordinates. This involves expanding the $\mathcal L$ as well. When the terms cancel, we have: 
$$
\frac{\partial\mathcal H}{\partial p_i}=\dot q_i
$$
$$-\frac{\partial \mathcal H}{\partial q_i}=\dot p_i$$
Which for a simple harmonic oscillator ($\mathcal H=p^2+q^2$) results in a clockwise circular flow on the phase space. 

The Hamiltonian defines a **vector field** over phase space. This field describes the flow of systems over this phase space. 
### Liouville's Theorem: Phase space flow conserves volume; phase space fluid is incompressible; phase space vector field has divergence zero
The divergence of the vector field described by the Hamiltonian (calculate it) is always zero. 

$$\nabla\cdot (\dot q_i, \dot p_i)=\frac{\partial \dot q_i}{\partial q_i}+\frac{\partial \dot p_i}{\partial p_i}
=\frac{\partial}{\partial q_i} \frac{\partial\mathcal H}{\partial p_i}-
\frac{\partial}{\partial p_i} \frac{\partial\mathcal H}{\partial q_i}=0
$$
One line proof of Liouville's theorem. 
### Non-fundamental Laws
Damped oscillator. This is NOT a physical law. It is a statistical law. That viscous damping term is a statistical average force. The diff eqn does NOT have a corresponding Lagrangian nor Hamiltonian. The phase space flow is not conserved. 

