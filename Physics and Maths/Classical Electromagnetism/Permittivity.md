Tags: [[Capacitors]] [[Electromagnetism]] [[Electric Displacement Field]] [[Electric Polarisation Of Insulators]] [[Maxwell Equation 1 - Gauss' Law for Electricity]] 
___
## Definition
Permittivity $\epsilon$ is a property of a material, a medium. It is defined by the equation
$$\boxed{\vec D=\epsilon\vec E}$$
where $\vec D$ is the [[Electric Displacement Field]] and $\vec E$ is the electric field. 
##### Interpretation
Permittivity is the amount of charge density at an infinitesimal surface element that creates a unit electric field at that location. 
After performing a surface integral:
$$\oint_S \vec D\cdot d\vec A=\epsilon\oint_S\vec E\cdot d\vec A$$
The permittivity can be seen as the amount of charge displacement permitted within a gaussian surface, for a unit electric flux. 
## In Free Space
In free space, $\vec D=\epsilon_0 \vec E$. The permittivity of free space is $\epsilon_0$. This is not a fundamental value, but an artefact of unit choice. Indeed, in [[3 Natural Units]] and [[2 Heaviside-Lorentz Units]], where the units are chosen appropriately, $\epsilon_0$ vanishes to $1$. 
## In Polarisable Media
In polarisable media i.e. dielectric i.e. insulating, $\vec D=\epsilon \vec E$. More charge can be displaced sandwiching the medium, before the same electric field strength is reached in the medium. This is a higher permittivity than free space. $\epsilon>\epsilon_0$. 

We can always express $\epsilon$ in terms of $\epsilon_0$:
$$\boxed{\epsilon=\epsilon_0\epsilon_r}$$
where $\epsilon_r$ is the relative permittivity of the medium. Note that in natural units, $\epsilon_0=1$, thus $\epsilon=\epsilon_r$. The relative permittivity is what characterises polarisability. Indeed, **polarisability** is another name for permittivity. 
## As the Intrinsic Capacitance
The capacitance of a capacitor is: 
$$C=\frac{\epsilon A}{d}$$
Notice the similarity to conductance and conductivity:
$$G=\frac{\sigma A}{l}$$
Indeed, permittivity is to capacitance what conductivity is to conductance. They are the reduced form of those macroscopic properties, made intrinsic and agnostic to the geometric dimensions of the materials. 