Category: [[Electromagnetism]] [[Electromagnetic Waves]]
___
Prerequisites: 
___
Related: 
___
In our continued pursuit to understand the behaviour of EM waves through matter, we must organise our knowledge about their behaviour at the interface between media. 
## Interface Conditions in General
##### Parallel component of Electric Field $\vec E$ Continuous
The parallel component of the electric field $\vec E$ at an interface must be continuous. 
$$\boxed{\vec E_{1\parallel}=\vec E_{2\parallel}}$$
This can be proven by considering an infinitesimally thin rectangle centered at the interface. As the area is zero, there can be no magnetic flux through it, thus the electric field circulation around that rectangle must be net zero. 
##### Normal component of Displacement Field $\vec D$ Steps by Free Surface Charge Density
Consider an infinitesimally short cylinder whose axis is normal to the interface, centered at the interface. By Gauss' Law the normal component of the displacement field must step by the surface charge density. 
$$\boxed{|\vec D_{1\perp}|+\sigma=|\vec D_{2\perp}|}$$
In the case of zero free charge: 
$$\boxed{\vec D_{1\perp}=\vec D_{2\perp}}$$
Thus the tangential electric fields are related by the permittivity in each medium: 
$$\boxed{\epsilon_1\vec E_{1\perp}=\epsilon_2\vec E_{2\perp}}$$
##### Normal Component of Magnetic Flux Density $\vec B$ Continuous
Gauss' Law for magnetism shows that the normal component of the magnetic flux density must be continuous, by considering an infinitesimally short cylinder whose axis is normal to the interface, crossing the interface. 
$$\boxed{\vec B_{1\perp}=\vec B_{2\perp}}$$
##### Parallel Component of Magnetising Field $\vec H$ 
By the integral Ampere's Law and considering an infinitesimally thin rectangle whose plane is normal to the interface, we know that the tangential component of the magnetising field is continuous by the surface current density. Note that the displacement field will have zero flux in that region. 
$$\boxed{|\vec H_{1\parallel}|+j=|\vec H_{2\parallel}|}$$
In the case that there are no free charges and currents: 
$$\boxed{\vec H_{1\parallel}=\vec H_{2\parallel}}$$
Thus the tangential magnetic fields are related by the permeability in each medium: 
$$\boxed{\mu_1\vec B_{1\parallel}=\mu_2\vec B_{2\parallel}}$$
## Boundary Conditions When the Second Medium is Metal
Then the tangential electric field is zero, and normal magnetic field is zero, if conductivity is infinite (but this would mean instantaneous charge rearrangement on the surface, which is impossible). Keep in mind in real metals the conductivity is not infinite and it will take time for charge to move on the surface, thus the EM field is able to penetrate a little. ([[Skin Effect]] and [[4 EM Waves in Media]])
## Optical Boundary Conditions
The conditions above can further imply relationships between the incident, reflected and transmitted (refracted) EM waves. (**only the tangential component!)

The parallel electric field being continuous condition implies that: 
$$\boxed{\vec E_i+\vec E_r=\vec E_t}$$
Since the transmitted power must be no more than the incident power, the reflected field must be opposing to the incident field. i.e. **the reflected wave is phase shifted by half cycle**. 

The magnetising field of the reflected wave must remain in the same direction while the electric field flips, because only then will the direction of power transfer be flipped. Thus, the parallel magnetising field being continuous implies that: 
$$\boxed{\vec H_i+\vec H_r=\vec H_t}$$
$$\boxed{\frac{\vec E_i}{\eta_1}-\frac{\vec E_r}{\eta_1}=\frac{\vec E_t}{\eta_2}}$$
Where we have used the fact that $H_r=-E_r/\eta$ in the coordinate system shared by the incident and transmitted waves. 