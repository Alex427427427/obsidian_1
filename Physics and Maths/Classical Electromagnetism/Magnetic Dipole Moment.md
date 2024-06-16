Tags: [[Electromagnetism]] [[Electric Dipole Moment]]
___
A magnet experiences a torque in a magnetic field, like how an electric dipole experiences a torque in an electric field. 
## Deriving The Magnetic Dipole Moment 
##### Magnetic Charge Model
At one point magnetic monopoles were thought to exist. Magnets were thought to be two poles separated by a distance, like electric dipoles. Under this model, the magnetic dipole moment $\vec\mu$ would be a product of the *hypothetical magnetic charge* $m$ and the displacement vector $\vec l$ pointing from the south charge to the north charge. 
$$\boxed{\vec \mu=m\vec l}$$
##### Current Loop Model
However, Ampere realised that current loops create the same field pattern of magnets, and hypothesised (correctly) that all known magnets were in fact current loops, and that magnetic charges did not exist. Now let's derive the formula of the magnetic moment of a current loop.

Consider a DC motor, that creates torque on a coil of current carrying wire by the Lorentz force. We know this phenomenon is the reverse of a generator which generates current by the rate of change of magnetic flux through the coil. The current generation mechanism doesn't care about the shape of the coil, but only the area. Running the generator in reverse, the same must also be true for the motor mechanism. Whatever distribution of the lorentz force on an arbitrarily shaped coil, will result in the same net torque, so long as the area of the loop is kept the same. Thus we are free to choose any shape convenient for our analysis. I will choose a rectangle. The above reasons also suggest that the only relevant properties to parameterise a magnetic moment with, is the area $a$ of the current loop, and the current $i$. 
![[Square Loop in Magnetic Field.png|300]]
Let the length of the rectangle (the edge perpendicular to the magnetic field) be $L$, and the width be $W$. Take the right edge to be the pivot, as we are free to do. The net torque $\vec \tau$ on the loop is then only the result of the lorentz force acting on the left edge:
$$\vec \tau=iLW\hat a\times\vec B$$
where $\hat a$ is the unit vector associated with the plane of the loop according to the right hand rule on the current. $LW\hat a$ is then simply $\vec a$, the vector associated with the plane of the loop, with a magnitude equal to the area. Thus
$$\vec\tau=i\vec a\times\vec B$$
$$\boxed{\vec\tau=\vec\mu\times\vec B \ \ \ \\ \ \ \ \ \ \ \ \ \ \ \ \  \vec\mu=i\vec a}$$
Which is summarised well in this diagram:
![[Magnetic Moment Current Loop.png|300]]
## Force and Interaction Energy of the Magnetic Moment in a Magnetic Field
##### Force
Like the electric dipole, 
$$\boxed{\vec F=\nabla(\vec\mu\cdot\vec B)}$$
##### Interaction Energy
Like the electric dipole,
$$\boxed{U=-\vec\mu\cdot\vec B}$$
## Behaviour
An electric dipole would **oscillate back and forth** in a uniform electric field, periodically changing its alignment to the electric field. 

A magnetic moment would instead **precess about the uniform magnetic field**, because an object with a magnetic moment is actually a rotating entity. 