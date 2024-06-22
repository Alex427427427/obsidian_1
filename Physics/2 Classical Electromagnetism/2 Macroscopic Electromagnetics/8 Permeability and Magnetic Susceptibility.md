Tags: [[Electromagnetism]] [[4 Improving Inductance With Magnetisable Medium]] [[2 Magnetisation, its Field, and Phenomena]] [[6 Magnetic Induction Field (or Magnetising Field)]]
___
## Definition
Permeability $\mu$ is a property of a material, a medium. It is defined by the equation
$$\boxed{\vec B=\mu\vec H}$$
where $\vec H$ is the [[6 Magnetic Induction Field (or Magnetising Field)]] and $\vec B$ is the magnetic field. 
##### Interpretation
Permeability is the amount of sheet current density surrounding a solenoid that creates a unit magnetic field in the space inside the solenoid. 
## In Free Space
In free space, $\vec B=\mu_0 \vec H$. The permeability of free space is $\mu_0$. This is not a fundamental value, but an artefact of unit choice. Indeed, in [[3 Natural Units]], where the units are chosen appropriately, $\mu_0$ vanishes to $1$. 
## In Magnetisable Media
$\vec B=\mu \vec H$. More magnetic field lines can be pierced through the medium, for the same enveloping current sheet density. This is a higher permeability than free space. $\mu>\mu_0$. Note that for diamagnetic materials, where the magnetisation opposes the induction, $\mu < \mu_0$. 

We can always express $\mu$ in terms of $\mu_0$:
$$\boxed{\mu=\mu_0\mu_r}$$
where $\mu_r$ is the relative permeability of the medium. Note that in natural units, $\mu_0=1$, thus $\mu=\mu_r$. The relative permeability is what characterises magnetisability. Indeed, think of permeability as **magnetisability**. 

If the medium magnetisation is **anisotropic but still linear**, permeability is a general linear map - a **tensor** ([[1 What Tensors Are]]). 

If the medium magnetisation is **non-linear**, permeability is the linearised map - still a tensor - that is the **Jacobian** of the magnetic field function with respect to magnetisation field. 
## As the Intrinsic Permeance
The permeance of a material is: 
$$\mathcal P=\frac{\mu A}{l}$$
Notice the similarity to conductance and conductivity:
$$G=\frac{\sigma A}{l}$$
And capacitance and permittivity:
$$C=\frac{\epsilon A}{d}$$
Indeed, permeability is to permeance what conductivity is to conductance, and what permittivity is to capacitance. They are the reduced form of those macroscopic properties, made intrinsic and agnostic to the geometric dimensions of the materials. 
## Magnetic Susceptibility
This is a reformulation of the permeability. It characterises the magnetisability still. 
$$\vec B=\mu_0\vec B+\vec M=\mu_0\vec B+\mu_0\chi_m\vec B=\boxed{\mu_0(1+\chi_m)\vec B}$$
where we have used the idea that the magnetisation field is a linear map of the magnetic field. The parameter $\chi_m$ is the **magnetic susceptibility**. 

We see that $$\boxed{\mu_r=1+\chi_m}$$
The higher the susceptibility, the higher the magnetisability. Note that it is negative for diamagnetic materials.  