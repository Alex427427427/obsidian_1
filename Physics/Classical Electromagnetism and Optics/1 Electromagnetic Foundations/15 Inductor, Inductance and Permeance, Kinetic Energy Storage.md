Tags: [[Electromagnetism]] [[13 Maxwell Equation - Ampere's Law]]
___
A current loop produces a magnet dipole field. A long helical current - equivalent to many current loops stacked together - creates a nice uniform magnetic field pattern within the cylinder of space in the middle of the helix, while the field outside nearly cancels out everywhere. This configuration of current is an **inductor**. 
![[Inductor Field.png]]
## Inductance
A small rectangular Amperian loop that pinches the edge of the inductor, would pick up no field on the outside, and all the magnetic field $B$ is on the inside, uniformly distributed. Thus ampere's law tells us:
$$Bl=\mu_0NI$$
where $N$ is the number of windings and $NI$ is the total current enclosed. 

With inductors, the primary entity of interest is the **magnetic flux linkage** $N\Phi_B$. According to Faraday's law, as the magnetic flux collapses, each loop winding will experience a forward pushing potential. It's as if the flux stored kinetic energy or contains inertia, and will dispense it to the current as it tries to slow down. The total forward pushing potential across the inductor is $N$ times more than the one experienced by the single winding. 
$$N\Phi_B=NAB=\frac{\mu_0A}{l}N^2I$$
Thus we can characterise the inductor's effectiveness at producing flux linkage:
$$\boxed{N\Phi_B=LI}\ \ \ \ \ \ \ where\ \ \ \ \\ \boxed{L=N^2\frac{\mu_0A}{l}}$$
$L$ is called **inductance**. 
## Permeance
Removing the effect of the winding number, we can turn our attention to the material itself:
$$\Phi_B=\frac{\mu_0A}{l}NI$$
If we then recognise that $NI$ is simply the total enveloping current, we could group it into a new concept called the $magnetomotive force$ $\mathcal F$. Thus
$$\boxed{\Phi_B=\mathcal P\mathcal F}\ \ \ \ \\ \ \ where \ \ \ \ \ \ \ 
\boxed{\mathcal P=\frac{\mu_0 A}{l}}\ \ \ \ \ \ \ \ and\ \ \ \ \ \ \ 
\boxed{\mathcal F=NI}$$
The quantity $\mathcal P$ is the **permeance** of a material. It reveals how much magnetic flux will pass through a material, given a unit magnetomotive force - an enveloping current. In this sense, we can think of permeance as the **magnetic conductance**. Indeed, we can construct entire **magnetic circuits** that work not with electromotive forces and currents, but magnetomotive forces and magnetic flux. 


The reduced permeance agnostic to material dimensions is $\mu_0$ - permeability of free space. In time, we will see that this is different in different media. 
## Inductor's Dynamical Properties
Suppose there is a changing current - which is the source of the inductor's magnetic flux. This will apply a time differential on both sides of the inductance equation:
$$\frac{dN\Phi_B}{dt}=L\frac{dI}{dt}$$
We can substitute the left hand side with electric properties via Faraday's law:
$$-\int_C\vec E\cdot d\vec l=L\frac{dI}{dt}$$
Thus 
$$\boxed{V=L\frac{dI}{dt}}$$
##### Electromechanical Analogues
In the electromechanical systems unification, $V$ is the electric analogue of force, while $I$ is the electric analogue of velocity. (Charge is displacement). This suggests that $L$ is the mass, and that the inductor is an inertial element. The inductor dynamics equation is Newton's 2nd law. Furthermore, the quantity $LI$ is the electric analogue of $mv$, which is momentum. *Flux linkage is momentum*. 
$$\boxed{L\leftrightarrow m}\ \ \ \ \ \ \ and\ \ \ \ \ \ \ \boxed{N\Phi_B\leftrightarrow p=mv}$$
Indeed, if the current was forcefully stopped, then depending on the deceleration, a large amount of electromotive force will be created, pushing on whatever is trying to stop the current. This creates sparks and arcs where the voltage is strong enough to push charges into air. 
##### Kinetic Energy Stored in the Inductor
The electromechanical analogies are more literal than you may think. If we copy over the equations of dynamics, we obtain the correct energies for the electric and mechanical systems. Indeed the analogies were constructed to make this work. 
$$E_k=\frac{1}{2}mv^2=\frac{p^2}{2m}$$
$$\boxed{E_k=\frac{1}{2}LI^2=\frac{N^2\Phi_B^2}{2L}}$$
The fact that the inductor is an inertial element means that its energy is kinetic. 