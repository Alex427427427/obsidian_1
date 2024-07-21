Category: [[Tags/RF Engineering]]
___
Prerequisites: [[Spherical Geometry - Solid Angle]] [[6 Energy Flow of the EM Field]]
___
Related: 
___
## Definition
The Antenna Aperture is a function on the unit sphere - its value at each direction represents the effective (angular) area of an aperture facing that direction, controlling how much incident EM power can pass through. This concept is very similar to antenna gain. 

The fundamental definition of this effective area in one direction is such that the incident power density of a plane wave from that direction multiplied by the aperture function $A$ gives the actual total power received by the antenna, from that direction. 
$$\boxed{P_{received}(\theta,\phi)=I_{incident}(\theta, \phi)A(\theta, \phi)}$$
## Relationship to Gain
The gain compares the actual received power in one direction compared to the power received by an isotropic antenna. The incident irradiance must be the same. Thus: 
$$G=\frac{P_{actual}}{P_{iso}}=\frac{A_{actual}}{A_{iso}}$$
From complicated thermodynamics derivations, we know the aperture of an isotropic antenna is: 
$$\boxed{A_{iso}=\frac{\lambda^2}{4\pi}}$$
Which suggests that the effective total spherical area is $\lambda^2$, which is then divided by the total solid angles in a sphere, $4\pi$. 

Thus, in general,
$$\boxed{G=\frac{4\pi}{\lambda^2}A}$$
