Tags: [[Electromagnetism]] [[1-1 Charges and Currents]]
___
Like any other flowing substance, total charge is conserved. If charge appears to be disappearing at a location, it must have moved away from it as a current. 

Consider a volume that contains charge $Q$. If current $I$ is emitting from the closed surface $S$ of this volume, then the charge will decrease by $\frac{dQ}{dt}=I$. In integral form:
$$\frac{dQ}{dt}=\oint_S\vec J\cdot d\vec A$$
Where $\vec J$ is the current density through the surface. The divergence theorem - a property of geometry and differentials that tells us the total flux through a closed surface must equal to the total sources of the flux in the volume enclosed by the surface - allows us to convert the right hand side into a volume integral. 
$$\frac{dQ}{dt}=\int_V\nabla\cdot\vec JdV$$
The left hand side could also be converted into a volume integral of charge density $\rho$:
$$\int_V\frac{d\rho}{dt}dV=\int_V\nabla\cdot\vec JdV$$
Which contains the local form of the Continuity Equation:
$$\frac{d\rho}{dt}=\nabla\cdot\vec J$$
or
$$\boxed{\frac{d\rho}{dt}-\nabla\cdot\vec J=0}$$
This is the local conservation of charge spoken in the language of calculus. 