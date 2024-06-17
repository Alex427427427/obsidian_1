Tags: [[Electromagnetism]] [[Electric Polarisation Of Insulators]] [[Capacitors]]
___
Please understand [[Electric Polarisation Of Insulators]] and [[Capacitors]] before attempting to understand this page. 
## The Displacement Field
When a medium is polarised, the electric field can become very complicated on the microscopic scale, with the vast number of dipole field patterns superimposing on one another. Although this usually smears out to be a uniform electric field on the macroscopic scale, this still requires us to explicitly obtain the polarisation field to do any further analysis. 

We can define another field that is basically the electric field, but is agnostic to the effects of polarisation. We explicitly isolate out the fields emanating from the free charges. 

## Displacement Field in Free Space
Return to the capacitor. We know that the charge stored on the plates has a relationship with the electric flux between the plates:
$$EA=\frac{Q}{\epsilon_0}\implies Q=\epsilon_0EA\implies\sigma_{free}=\epsilon_0E$$
Where $\sigma_{free}$ is used to denote the surface charge density that was free to move and hence was displaced across the capacitor plates. We define a new field that contains information about the electric field emerging from a surface charge density, pointing in the same direction as the electric field. 
$$\boxed{\vec D=\epsilon_0\vec E}$$
This is the displacement field in free space. Notice that it has the same value as the displaced charge density. 
## Meaning of the Displacement Field
In a capacitor arrangement, the displacement field at a location of interest, is the amount of **surface charge density** that's been **displaced** across the two plate elements situated on **either side of the location of interest**, whose field lines connect to pierce the location of interest.

**Integrating over a gaussian surface, the displacement field tells us precisely how much total free charge has been separated into either side of the gaussian surface**, earning its name. (Should there only be a charge on the inside of the gaussian surface and none outside, the charge displacement still returns the same value. This is because the situation is equivalent to having the opposite charge outside the surface, situated infinitely far away.) Since this field only describes charge displacement, it is uncaring to the details of the alterations to the electric field due to polarisation. 

An alternative interpretation is that this is also a field that describes the **equivalent presence of free charges, distributed over a gaussian surface, expanding and extending through space**. In a point charge arrangement, as we consider the influence of the charge on an expanding gaussian surface, it's as if the charge is smeared out over the gaussian surface as the surface expands, thus the equivalent charge density decreases as does the displacement field, and so does the resultant electric field at that surface. 

Note that the displacement field's whole purpose is to be **integrated over a surface** and return the charge enclosed \ displaced. This makes it more directly a **flux density**. On the other hand, the electric field is more suited to be integrated over lines, returning the electromotive force. This situation is the opposite to the magnetic phenomena, where the magnetic field is a flux density to be integrated over a surface, and the induction field is to be integrated over lines. 
## Displacement Field in Polarised Medium
More generally, however, the electric field is altered within a polarisable medium, altering the relationship between the electric field and the displacement field. The same charge displacement will result in a smaller electric field. It's as if there is something lowering the total charge displacement. 
![[Polarisation in material.png]]
The culprit is the surface charge displaced by the polarisation itself. This displacement is opposite to the external free charge displacement, responsible for the electric field. This displacement is also not free to move, so should not be accounted for by the displacement field. Since $\vec P$ results in an opposite displacement, we can find the total displacement:
$$\vec D-\vec P$$
which is now equivalent to $\epsilon_0\vec E$. Thus,
$$\boxed{\vec D=\epsilon_0\vec E+\vec P}$$
If we wish to find a direct relationship between the displacement field and the true electric field in a medium, we can absorb the polarisation field into the coefficient of the electric field. 
$$\boxed{\vec D=\epsilon\vec E}$$
In an isotropic medium, polarisation is able to occur in any direction equally, and will be aligned with the electric field. In such cases $\epsilon$ is a scalar. If polarisation is constrained to occur at different extents along different directions, the polarisation field will not align with the electric field and $\epsilon$ will be a general linear map - a tensor ([[Tensors]] [[1 What Tensors Are]]). 
## Macroscopic Version of the First Maxwell's Equation 
The displacement field's interpretation directly leads to a modified version of the first Maxwell's Equation:
$$\oint_S\vec E\cdot d\vec A=\frac{Q}{\epsilon_0}\rightarrow\boxed{\oint_S\vec D\cdot d\vec A=Q_{free}}$$
Which says the displacement field is the apparent charge density at the gaussian surface enclosing a displaced charge. This equation holds on the macroscopic scale, where the polarisation behaviour of media, and the complex microscopic field patterns, are abstracted away. 

In differential/local form:
$$\nabla\cdot\vec E=\frac{\rho}{\epsilon_0}\rightarrow\boxed{\nabla\cdot\vec D=\rho_{free}}$$
