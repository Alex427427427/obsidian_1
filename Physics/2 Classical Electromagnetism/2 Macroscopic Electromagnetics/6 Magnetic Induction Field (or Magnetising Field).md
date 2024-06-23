Tags: [[Electromagnetism]] [[2 Magnetisation, its Field, and Phenomena]] [[4 Improving Inductance With Magnetisable Medium]] [[9 Magnetic Forces and Fields, Lorentz Force]]
___
## The Induction Field
When a medium is magnetised, the magnetic field can become very complicated on the microscopic scale, with the vast number of dipole field patterns superimposing on one another. Although this usually smears out to be a uniform magnetic field on the macroscopic scale, this still requires us to explicitly obtain the magnetisation field to do any further analysis. 

We can define another field that is basically the magnetic field, but is agnostic to the effects of magnetisation. We explicitly isolate out the fields emanating from the free current sources. 
## Induction Field in Free Space
Return to the inductor. We know that the current circulating the inductor has a relationship with the line integral of the magnetic field induced through the material: 
$$Bl=\mu_0NI\implies B=\mu_0nI$$
Where $nI$ is used to denote the surface current density applied and is trying to induct a magnetic field line through the material. We define a new field that only contains the information of this inducting surface current density, pointing in the same direction of the magnetic field. 
$$\boxed{\vec H=\frac{1}{\mu_0}\vec B}$$
This is the induction field in free space. It has the same value as $nI$. 
## Induction Field in Magnetised Medium
More generally, however, the magnetic field is altered within a polarisable medium, altering the relationship between the magnetic field and the induction field. The same induction current will result in a larger magnetic field in paramagnetic and ferromagnetic materials. It's as if there is something raising the total inducting current. 

The culprit is the surface current density caused by magnetisation. This current is also not free to move or be used elsewhere, so should not be accounted for by the induction field. It is a **bound current**. Since $\vec H$ results in an additional aligned induction current, we can find the total induction:
$$\vec H+\vec M$$
which is now equivalent to $\frac{1}{\mu_0}\vec B$. Thus,
$$\boxed{\vec H=\frac{1}{\mu_0}\vec B-\vec M}\ \ \ \ \ \ \ and\ \ \ \ \ \ \ \boxed{\vec B=\mu_0(\vec H+\vec M)}$$
If we wish to find a direct relationship between the true induction field and the magnetic field in a medium, we can absorb the magnetisation field into the coefficient of the induction field. 
$$\boxed{\vec B=\mu\vec H}$$
In an isotropic medium, magnetisation is able to occur in any direction equally, and will be aligned with the magnetic field. In such cases $\mu$ is a scalar. If magnetisation is constrained to occur at different extents along different directions, the magnetisation field will not align with the induction field and $\mu$ will be a general linear map - a tensor ([[Tensors]] [[1 What Tensors Are]]). 
## Bound Current
The current induced in a magnetised material. This usually appears at the surface as a sheet current. This current is bound, because it can never leave the material. By conceiving the geometry of the situation, we see that: 
1. The magnetisation field's circulation is the current density. $$\nabla\times\vec M=\vec J_{bound}$$
2. A time rate of change of polarisation field is also the current density. $$\frac{\partial \vec P}{\partial t}=\vec J_{bound}$$
Thus the total bound current in a material is:
$$\boxed{\vec J_{bound}=\nabla\times\vec M+\frac{\partial\vec P}{\partial t}}$$
Which is analogous to the ampere law for bound sources:
$$\nabla\times\vec M=\vec J_{bound}-\frac{\partial\vec P}{\partial t}$$
## Monopoles
With the magnetisation field defined, we can also define a ficticious source such that when separated onto the two surfaces at the ends of the magnetised material, gives rise to the magnetisation field much like the electric polarisation case. This is the bound magnetic charge density $m$. 
$$\boxed{m_{bound}=-\nabla\cdot\vec M}$$
The form of this equation is trivial by inspection of the magnetisation field pattern. The induction field can also be associated with the displacement field notion from electricity, by observing the similarity between the equations: 
$$\vec D=\epsilon_0\vec E+\vec P\ \ \ \ \ \ \ and\ \ \ \ \ \ \ \vec H=\frac{1}{\mu_0}\vec B-\vec M$$
The first term is the source field, the second a flux density, the third a response source field. The negative sign is an artefact of the difference in the pole model and loop model's internal field pattern of a dipole. 

Thus $\vec H$ can be associated with a charge law: 
$$\boxed{m_{source}=\nabla\cdot\vec H}$$
In practice the two charges must cancel, to make sure the magnetic field is divergence-less. 
$$\nabla\cdot\vec H+\nabla\cdot\vec M=0$$
## Field Patterns
In free space, $\vec M$ doesn't exist, and $\vec B$ and $\vec H$ look the same. In a magnet, both $\vec H$ and $\vec M$ become divergent from fake magnetic charges. These magnetic charges account the charge versions of the free and bound currents. 
![[macroscopic mag field patterns.png]]
Notice that the $\vec H$ and $\vec M$ fields super impose to form the closed loop $\vec B$ pattern. 