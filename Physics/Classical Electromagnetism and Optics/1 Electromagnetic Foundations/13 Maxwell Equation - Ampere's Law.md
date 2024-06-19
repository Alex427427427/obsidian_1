Tags: [[Electromagnetism]] [[9 Magnetic Forces and Fields, Lorentz Force]] [[1 Charges and Currents]] [[5 Maxwell Equation - Gauss' Law for Electricity]]
___
## Naive Integral Form
Ampere's law describes how current sources produce magnetic fields. With the analogy of an incompressible fluid, Ampere's law says that a current source imparts a rotation to the fluid whose effects propagate outwards, always maintaining a constant rotation. This is similar to the electric flux remaining constant over an expanding gaussian surface. 
$$\oint_C\vec B\cdot d\vec l=\mu_0I$$
Where $C$ is the closed path (called an Amperian loop) enclosing a current, $I$ is the enclosed current passing through the surface enclosed by the path, and $\mu_0$ is the permeability of free space. For now, this can be interpreted as a simple constant of proportionality. Its full meaning will be discussed later when your understanding of electromagnetic phenomena is more mature. 
## Naive Local Form
If we dimensionally reduce the equation over the cross sectional area and invoke Stoke's theorem - a statement about geometry and calculus, that the total circulation of a field around a loop is equal to the area integral of the local vorticity over any surface enclosed by the loop - we get the local form:
$$\int_S(\nabla\times\vec B)\cdot d\vec A=\int_S(\mu_0\vec J)\cdot d\vec A$$
$$\nabla\times\vec B=\mu_0\vec J$$
Which reveals that a current density is a source of local vorticity of the magnetic field lines. 
## Maxwell's Correction to Ampere's Law
Now consider the current carrying wire has a break, where a capacitor has been inserted. The naive Ampere law would now depend on where the surface is chosen, for the same amperian loop. If the surface passes through the current, then there is one answer for the magnetic field circulation; if the surface was chosen to bulge and pass through the empty gap between the plates of the capacitor, then the law would conclude there is no magnetic field at all! This is clearly wrong. 

Maxwell realised that across the gap of the capacitor, while the wire on either side of the capacitor carries current, the electric field is changing in the gap. Since
$$I=C\frac{dV}{dt}$$
$$I=\frac{\epsilon_0A}{d}\frac{d(Ed)}{dt}=A\epsilon_0\frac{dE}{dt}$$
This implies that
$$\boxed{\vec J=\epsilon_0\frac{\partial\vec E}{\partial t}}$$
via a dimensional reduction. 

The above suggests that a changing electric field also induces a magnetic field vorticity. Thus
$$\boxed{\nabla\times\vec B=\mu_0\left(\vec J+\epsilon_0\frac{\partial\vec E}{\partial t}\right)}$$
$$\boxed{\oint_C\vec B\cdot d\vec l=\mu_0I+\mu_0\epsilon_0\frac{\partial\Phi_E}{\partial t}}$$
where $\Phi_E$ is the electric flux, $\int_S\vec E\cdot d\vec A$.
