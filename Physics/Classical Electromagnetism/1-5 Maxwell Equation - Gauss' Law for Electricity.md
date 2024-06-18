Tags: [[Electromagnetism]] [[1-3 Electric Forces and Fields]] [[1-1 Charges and Currents]]
___
## The Law
##### Integral Form
The First Law is a compact statement of geometry, that electric charges are the only source of electric fields, that the field lines flow outward without preference of direction, and that the amount of flow is proportional to charge. 
$$\boxed{\oint_S \vec E\cdot d\vec A=\frac{Q}{\epsilon_0}}$$
This says that the total electric flux through a closed surface is constant regardless of the surface, and that it is proportional to the charge that is enclosed. The enclosing surface whose shape or size we don't care, is called a **Gaussian surface**.
![[first Maxwell law.png]]
Though the field patterns can be complex, due to the linearity of the field lines, this law is always preserved. 
![[Complex elec field pattern.png]]
##### The Constant $\epsilon_0$
The constant of proportionality is $\epsilon_0$, the permittivity of free space. For now it can be thought of as the amount of charge permitted in a given volume, if the electric flux is fixed and of unit quantity. Its full nature will be revealed later when your understanding of electric phenomena is more mature. [[2-12 Permittivity and Electric Susceptibility]] 
##### Differential, Local Form
Through the divergence theorem, which is another statement of geometry, we can relate the flux through a closed surface to the divergence of the field inside the surface:
$$\oint_S \vec E\cdot d\vec A=\int_V\nabla\cdot\vec EdV=\frac{Q}{\epsilon_0}$$
$$\int_V\nabla\cdot\vec EdV=\frac{\int_V\rho dV}{\epsilon_0}$$
$$\boxed{\nabla\cdot\vec E=\frac{\rho}{\epsilon_0}}$$
## The Law in Terms of Potential
$$\nabla\cdot(-\nabla\phi)=\frac{\rho}{\epsilon_0}$$
$$\boxed{\nabla^2\phi=-\frac{\rho}{\epsilon_0}}$$
In the absence of sources, the equation becomes $\nabla^2\phi=0$ which is Laplace's equation. The solution to which must satisfy harmonic properties: at everywhere in space, the value of $\phi$ is the average of an infinitesimal local neighbourhood, and that for any region of space, the extremal values must lie on the boundary of that space. 