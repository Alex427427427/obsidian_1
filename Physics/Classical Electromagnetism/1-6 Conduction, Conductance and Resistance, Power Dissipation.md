Tags: [[Electromagnetism]] [[1-4 Electric Potential and Voltage]] [[1-1 Charges and Currents]]
___
## Conductor
A conductor is an object in which there are charges that are free to move about. Such objects can facilitate current flow. 
## Current Flow
we previously spoke of current flow as a result of repulsion from a source of like charge, and / or attraction towards a source of opposite charge. With the description of the electric potential, we have abstracted away. We no longer care what the source looks like so long as it produces the right potential. We shall now examine current as charges interacting with the potential. 

The electric potential can be thought of as a hilly landscape. Charges want to roll down the hill. The electric field is the negative slope of the landscape, delivering force to the charges. When charges travel down the hill, they lose the potential difference, and gain more kinetic energy. If the hill is dissipative, they may keep rolling down the hill and have a constant velocity. A constant current. 
## Ideal Conductor
In an ideal conductor, the flow of charges is unimpeded. They soon accelerate to crazy fast speeds. This will continue **so long as there exists an electric field i.e. uneven potential** throughout the conductor. Thus charges will flow until, **very quickly**, they distribute themselves throughout the conductor in such a way to have **no electric field anywhere** in the conductor, in other words, the **potential is equal everywhere** in a conductor. The conductor is always an **"equipotential"**. Since the electric field, the negative gradient of potentials, is orthogonal to equipotentials, **all electric field must be orthogonal to the conductor's surface**. Another way to look at this is that if the electric field had any component parallel to the surface, the surface charges would quickly move until there was no more parallel component. 

Since there can be no electric field in a conductor at steady state, there must be no charge distribution in the volume of the conductor. Because if there were, then by the first Maxwell Equation there must be electric field everywhere in the conductor, because we are free to choose gaussian surfaces to apply the law. **All free charges in a conductor reside on its surface**. 
##### Ideal Conductor with a Cavity
If a neutral conductor has a cavity, and we introduce a charge $Q$ inside that cavity, then immediately charge will flow to that inner cavity's surface, such that the total charge on that surface is $-Q$. This is to ensure that a gaussian surface fully in the conductor, enclosing the cavity, will have no electric flux through it. Taking another gaussian surface outside the conductor enveloping the whole conductor, we must find the same flux as would have emanated from a charge $Q$. Since the cavity surface cancelled with the $Q$ inside, the outer conductor surface must also have a charge of $Q$ to compensate. 

If the cavity contains no charge, then there must be no field within. This can be seen from the fact that the electric potential is a harmonic function in the absence of sources, meaning that its extreme values in some volume of space must lie on the boundary of that space. Since the cavity wall is an equipotential, the potential's value *everywhere* in the cavity must be the same. This makes an ideal conductor perfect for protecting whatever is inside it from external fields. 
## Current Flowing Through Resistor and Resistance
Now suppose there is a voltage applied at two ends of a conductor. The enforced field would accelerate free charges in the conductor until the current approaches $\infty$. This is not good and would cause meltdowns. If we instead have a material that impedes the flow of charges and dissipates energy, then we have what is analogous to a slope with friction. The charges would reach some steady state velocity, which corresponds to a steady state current. We shall capture this effect: 
$$\boxed{I=\frac{V}{R}}$$
Where we have assumed a linear relationship between the applied voltage and the current. $R$ is the **resistance** of the material, quantifying how much voltage is needed to result in a unit current. This is Ohm's law, originally an empirical observation. The unit for resistance is "Ohm ($\Omega$)".
## Power Dissipation
In the mechanical analogue of electrical systems, current is velocity, voltage is force, and resistance is drag. Since power is force times velocity, 
$$\boxed{P=VI=I^2R=V^2/R}$$
We see that power is proportional to current or velocity squared. 
## Resistivity
We can reduce resistance into its intrinsic form, agnostic to the geometric dimensions of the resistor. We know that the wider its cross section $A$, the lower the resistance because current flow is less restricted. We know that the longer the resistor's length $d$, the higher the resistance because there is more impeding material. Therefore, 
$$\boxed{R=\frac{\rho d}{A}}$$
Where $\rho$ is the resistivity, an intrinsic property of material. 
## Conductance and Conductivity
We can equally define the reciprocal of resistance, conductance $G$:
$$\boxed{G=\frac{1}{R}}$$
and
$$\boxed{I=GV}$$
In which case conductance represents how much current will result from a unit potential difference, i.e. how readily an object conducts current.

This too can be reduced into the intrinsic form:
$$\boxed{G=\frac{\sigma A}{d}}$$
where $\sigma$ is the conductivity of material. 
## Ohm's Law in Local Form
$$I=GV$$
We can reduce the cross sectional area dimension on both sides, and also see that the length dimension of the conductivity cancels out with the voltage, leaving behind the electric field:
$$\boxed{\vec J=\sigma\vec E}$$
Note that in the rare general case, the resultant current may not align with the electric field due to the material lattice. In those cases, conductivity is a tensor. [[1 What Tensors Are]]