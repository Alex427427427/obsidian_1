Tags: [[Geometry]]
___
Spherical geometry tells us that all the possible directions pointing out from an origin, can be characterised by an angular unit much like the radian, a square-radian if you will, also known as the **solid angle** $\Omega$. One solid angle results in a field of view of 1 unit area on a surface of 1 unit length away from the observer. 
$$\Omega=\frac{A}{r^2}$$
if there is a field of view of area $A$ at a distance $r$ away. 

**There are $4\pi$ total solid angles to form the totality of all directions.** in other words:
$$\boxed{4\pi=\int d\Omega}$$
## Spherical Volume Integral
The definition of the solid angle makes the spherical volume integral amazingly simple. It is the integration of infinitesimally thin spherical sheets of area $r^2 d\Omega$ , across all $r$ in the region of interest. Therefore:
$$\boxed{\int_VdV=\int_r\int_\Omega r^2d\Omega dr}$$
Where there is spherical symmetry i.e. no angular dependence, the solid angle integral becomes $4\pi$ immediately. 
