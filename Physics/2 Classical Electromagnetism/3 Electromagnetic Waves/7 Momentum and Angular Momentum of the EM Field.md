Tags: [[Electromagnetism]] [[Electromagnetic Waves]] [[6 Energy Flow of the EM Field]] [[5 Polarisation of EM Waves]] [[9 Magnetic Forces and Fields, Lorentz Force]]
___
Consider a plane wave washing over a charge in free space. Whenever the electric field pushes the charge in one direction, the magnetic field acts on that velocity to product a force in the same direction of the wave propagation. This happens regardless of the electric field orientation. Over time, the charge obtains momentum. Let's consider this. 
## Derivation of Linear Momentum Transfer Rate
Assume a unit charge is stationary at $t=0$. $F_\perp$ is the force transverse to wave propagation, $F_\parallel$ is the force parallel to wave propagation. Using the lorentz force law, we have: 
$$F_{\parallel}(t)=v_\perp(t)B(t)q=v_\perp(t)\frac{E(t)}{c}q=v_\perp(t)\frac{F_\perp(t)}{c}=\frac{P}{c}$$
Where $P$ is the power delivering to the charge. We need not continue to obtain an explicit expression for the momentum, but simply recognise that both sides involve a time rate of change: 
$$\frac{dp}{dt}=\frac{1}{c}\frac{dE}{dt}$$
Thus: 
$$\boxed{p=\frac{E}{c}}$$
So the momentum density of the electromagnetic wave is its energy density divided by $c$. 

Now we shall obtain the full expression for momentum. Start from poynting vector $\vec S=c^2\epsilon_0\vec E \times\vec B$ which is an energy density current, we divide by the velocity dimension once to get to the energy density, and we divide by $c$ again to reach the momentum density $\vec g$:
$$\boxed{\vec g=\epsilon_0\vec E\times\vec B}$$
## Angular Momentum
##### Angular Momentum Due to Frame Offset
Simply take the positional cross product to obtain the angular momentum density with respect to the frame origin: 
$$\boxed{\vec l=\epsilon_0(\vec r\times(\vec E\times\vec B))}$$
##### Angular Momentum Due to Circular Polarisation
A circularly polarised EM wave causes a charge to orbit the axis of incidence. The circularly polarised EM wave therefore must carry angular momentum. The classical treatment is far more complex than the quantum treatment, so we shall revisit this point during particle physics. 