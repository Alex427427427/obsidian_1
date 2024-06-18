Tags: [[1-1 Charges and Currents]] [[1-3 Electric Forces and Fields]]
___
## Magnetic Force between Currents
The previously mentioned force between parallel currents scales inversely with distance. In time, we will see that this force is the same phenomenon as magnetism. We shall discuss the force density along the wires of length $L$, $\frac{F}{L}$. 
$$\frac{F}{L}=k\frac{I_1I_2}{r}$$
This is the basis for defining the unit current Ampere as explained in [[1-1 Charges and Currents]]. Later, deriving from the Maxwell Equations, we will discover a more meaningful form of this equation, with a new constant $\mu_0$ having replaced $k$:
$$\boxed{\frac{F}{L}=\frac{\mu_0}{2\pi}\frac{I_1I_2}{r}}$$
##### The Factor of $2\pi$
Similar reasoning as before, the factor provides insight into the source of this magnetic force. There is a similar angular density dependence. This time however, one of the dimensions has been occupied by the infinitely long wires, leaving only 1 angular degree of freedom in the situation revolving about each of the wires, resulting in the $2\pi$, not $4\pi$. 
## Magnetic Field Around Current
We similarly characterise the magnetic field $B$ as an incompressible fluid like the electric field. This field will be responsible for delivering force density between currents. The field emerging from one current shall be agnostic to the second current strength, and the force density will be realised when multiplied by the second current. 
$$B=\frac{\mu_0}{2\pi}\frac{I_1}{r}$$
and 
$$\frac{F}{L}=I_2B$$
Now, the define the direction of the magnetic field is less simple than the electric field. For the electric field, we can simply take it to be radial. The magnetic field on the other hand must care about the axial current direction. Further experiment had shown that the force depends linearly on the component of alignment between the current directions. 

Smart dead people had done the work to design the following scheme. The magnetic field will envelope the current source with the right hand rule illustrated below, while the second current will experience a force according to the cross product, which is just the local version of the right hand rule. 
![[current magnetic field RHR.png|300]]
Thus
$$\boxed{\vec B =\frac{\mu_0}{2\pi}\frac{\vec I_1\times\hat r}{|\vec r|}}$$
$$\boxed{\frac{\vec F}{L}=\vec I_2\times\vec B}$$
## Magnetic Field Lines
Like an incompressible fluid, we can visually depict the flow of this fluid with field lines. The density of these flow lines is the strength of the magnetic field. Notice that the magnetic field lines form closed loops.
## Magnetic Force on Charge
We can convert the dimensions of the magnetic force law to work out how the magnetic field applies a force to an individual charge. 
$$\vec F=L\vec I_2\times\vec B=\vec L\frac{dq}{dt}\times\vec B=q\frac{d\vec L}{dt}\times\vec B=q\vec v\times\vec B$$
Where we have taken a unit vector out from the current vector and absorbed it into the distance vector along the length of the wire. 
## Summarising Electric and Magnetic Forces as Lorentz Force
When both electric and magnetic fields are present, a charge must experience both fields as a force. Thus: 
$$\boxed{\vec F=q(\vec E+\vec v\times\vec B)}$$
## Magnetic Field Produced by a Charge in Motion
To find the magnetic field produced by a moving charge, we need to begin from the magnetic field from a wire, and reduce a dimension via differentiation. 

It is a matter of geometric fact that the magnetic field at a distance $r$ away from a straight wire carrying current, is equivalent to the magnetic field at the center of a circular wire of radius $r$. Thus, the magnetic field from a small current element $Id\vec l$ is simply the total field reduced by $2\pi r$:
$$\vec B =\frac{\mu_0}{2\pi}\frac{\vec I\times\hat r}{|\vec r|}\rightarrow \boxed{d\vec B=\frac{\mu_0}{4\pi}\frac{Id\vec l\times\hat r}{|\vec r|^2}}$$
Which is the Biot-Savart law. We can associate the source element $Id\vec l$ with $q\vec v$ with a simple dimensional analysis. Thus, a moving charge produces a field:
$$\boxed{\vec B=\frac{\mu_0}{4\pi}\frac{q\vec v\times\hat r}{|\vec r|^2}}$$
![[mag field around moving charge.png]]
Notice the return of the $4\pi$ factor and the inverse square scaling law, further cementing the fluid notion. 
## Magnetic Field of a Ring Current is the Magnetic Field of a Magnet
Bending a current into a ring produces a donut-like field. 
![[ring current mag field pattern.png|300]]
![[bar magnet mag field.png]]
Prior, magnets were a separate phenomenon. Magnetic field lines indicated the direction that the north pole goes. Now it was clear that a ring current produces a pair of apparent north and south poles. 