Tags: [[Electromagnetism]] [[1 Charges and Currents]]
___
We shall now quantify forces. Once we do, the evolution of any system can be carried out with $\vec F=m\vec a$. 
## Electric Force
Place two point charges $Q_1$ and $Q_2$ a distance of $r$ apart. Their electrostatic attraction or repulsion should be proportional to each charge quantity individually. Furthermore, through experiment, we know that the force is inversely proportional to distance squared. to summarise this, and the force they experience will be:
$$F=K\frac{Q_1Q_2}{r^2}$$
Which is Coulomb's law with the coulomb constant of proportionality $K$. Upon writing down the Maxwell's equations in the future we will discover that $K$ should be more meaningfully expressed as $\frac{1}{4\pi\epsilon_0}$. Where $\epsilon_0$ is another constant of proportionality we will learn later, having replaced $K$. Expressing this way provides geometric insight to the nature of the electric force. 
$$\boxed{F=\frac{1}{4\pi\epsilon_0}\frac{Q_1Q_2}{r^2}}$$
##### The Factor of $4\pi$, and Solid Angles
Spherical geometry tells us that all the possible directions pointing out from an origin, can be characterised by an angular unit much like the radian, a square-radian if you will, also known as the **solid angle** $\Omega$. One solid angle results in a field of view of 1 unit area on a surface of 1 unit length away from the observer. 
$$\Omega=\frac{A}{r^2}$$
if there is a field of view of area $A$ at a distance $r$ away. See more in [[Spherical Geometry - Solid Angle]].

**There are $4\pi$ total solid angles to form the totality of all directions.** The factor of $4\pi$ in the formula tells us that the **solid angle density** is proportional to the force that the point charges experience. The same charge can be smeared out over a region occupying more solid angles, and the reduction in the angular charge density cancels out the effect, maintaining the same overall force. 
## Electric Field
The combination of the solid angle density insight along with the inverse square scaling of the force, suggests that there is behaviour similar to a **fluid like substance emanating** from $Q_1$, carrying the force to $Q_2$, and vice versa. This is the electric field. We say that an electric field emerges from $Q_1$, that must be agnostic to the second charge. We define the field to be the force that will be delivered, per charge. And the realisation of this force will be multiplication of the field strength with whatever second charge happens to be there. Thus the electric field around a charge $Q$ is: 
$$\boxed{\vec E=\frac{1}{4\pi\epsilon_0}\frac{Q}{|\vec r|^2}\hat r}$$
and a second charge $q$ will experience a force:
$$\boxed{\vec F=q\vec E}$$
Of course, the sign of the charge conveniently encodes the force direction. 

The force realised is symmetric between the charges. 

Note that field sources **do not feel their own field**. 
## Electric Field Lines
Like an incompressible fluid, electric fields can be characterised by field lines. The density of the lines indicates field strength. The lines flow out of a positive charge, and flow into a negative charge to maintain the force definitions. 
![[electric field lines.png]]
These fields linearly superimpose, creating fantastic and complex patterns:
![[more elec fields.png]]
The local effect of these field lines on charges remains the same: to push positive charges along the field direction, and push negative charges in the opposite field direction. In a way, the field is a **separation** field, motivating the **charge displacement field** that will be defined much later. [[5 Electric Displacement Field]]
##### Is There Really Something Flowing? 
Uncertain. It makes no difference for the rest of physics and the field has always been thought of as mathematical accounting tools. See [[Speculation]] [[Energy is Flowing Between Charges]]. 
