Tags: [[Classical Mechanics]] [[Newtonian Mechanics]]
___
## Particles
A particle is a localised object whose size and shape is insignificant to the problem. This obscures spin phenomena, which forces us to treat objects as extended. 
## Force is the source of motion change
The motion of a particle at position $\vec r$ and velocity $\dot{\vec r}$ is governed by:
$$\vec F(\vec r, \dot{\vec r})=\dot{\vec p}$$
This is Newton's second law. The left hand side concerns with the source of the force $\vec F$ which is an accounting tool that allows us to predict the effects on motion. All future theories of reality may vary simply on how the force comes about. 

As long as $\vec F$ remains finite or a delta distribution over time, this equation is always integrable to give $\vec r$ and $\dot{\vec r}$ at all later times. This is the goal of classical mechanics. 
## Inertial Frames
This equation is not fully correct; it holds only in an inertial frame, else unphysical forces show up. In an inertial frame, a free particle with $\dot m=0$ travels in a straight line. 
$$\vec r=\vec r_0+\vec vt$$
Newton's first law is the statement that such frames exist. 
##### Galilean Group
Inertial frames are not unique. In fact, there are an infinite number of inertial frames. Let S be an inertial frame, there there are 10 linearly independent transformations $S\rightarrow S^\prime$ such that $S^\prime$ is also an inertial frame. These are:
1. 3 rotations $\vec r^\prime=O\vec r,\ \ \ \ \ \ \ O\in O(3)$
2. 3 translations $\vec r^\prime=\vec r+\vec c,\ \ \ \ \ \ \ \vec c\in\mathbb{R}^3$ 
3. 3 boosts $\vec r^\prime=\vec r+\vec vt,\ \ \ \ \ \ \ \vec v\in\mathbb{R}^3$
4. 1 time translation $t^\prime=t+c,\ \ \ \ \ \ \ c\in\mathbb{R}$
If motion is uniform in $S$, it will remain uniform in $S^\prime$. These transformations form the Galilean Group under which Newton's laws are invariant. These symmetries in spacetime are the underlying reason for conservation laws. These are generalised to Poincare Groups in relativity, where rotations and boosts have been unified into Lorentz transformations. The Galilean Group can be recovered from the Poincare Group by taking speed of light to infinity. 
## Angular Momentum
$\vec L=\vec r\times\vec p,\ \ \ \ \ \ \ \vec\tau=\vec r\times\vec p$
The angular momentum $\vec L$ and torque $\vec \tau$ depend on where the origin is taken. If we take $\vec r\times$ to Newton's 2nd law:
$$\vec F=\dot{\vec p}\implies\vec r\times\vec F=\vec r\times\dot{\vec p}\implies\vec\tau=\dot{\vec L}$$
$\tau=0$ doesn't imply $\vec F=0$, but only that it is a central force - it acts through the center of mass. 
## Energy
The nature of energy as a flowing substance that is the generator of time evolution will come later, for now it is a magical accounting tool. Kinetic energy: 
$$T=\frac{1}{2}m\dot{\vec r}\cdot\dot{\vec r}$$
Power delivered, using product rule:
$$P=\frac{dT}{dt}=m\dot{\vec r}\cdot\ddot{\vec r}=\vec F\cdot\dot{\vec r}$$
Thus the work done on the particle:
$$T(t_2)-T(t_1)=\int_{t_1}^{t_2}\frac{dT}{dt}dt=\int_{t_1}^{t_2}\vec F\cdot\dot{\vec r}dt=\int_{\vec r_1}^{\vec r_2}\vec F\cdot d\vec r$$
For now we focus on conservative forces, which means it is only a function of space, and the work done is independent from the path taken. Equivalently, there is some potential $V$ such that:
$$\vec F(\vec r)=-\nabla V(\vec r)$$
Systems which admit a potential of this form include gravitational, electrostatic and inter-atomic forces. When we have a conservative force, we necessarily have a conservation law for energy:
$$T(t_2)-T(t_1)=\int_{\vec r_1}^{\vec r_2}-\nabla V\cdot d\vec r=-(V(\vec r_2)-V(\vec r_1))=V(\vec r_1)-V(\vec r_2)$$
$$T(\vec r_1)+V(\vec r_1)=T(\vec r_2)+V(\vec r_2):=E$$
So $E=T+V$ is a constant of motion. When it is expressed as a function of momentum and position, it is called the hamiltonian $H$.
## Conservation Laws
Already we see conservation laws appear. For a system, Newton's second law says that if $\vec F=0$, $\vec p$ is conserved. If $\vec \tau=0$, $\vec L$ is conserved. If $\vec F=-\nabla V$, $E$ is conserved. 

Note that many systems will appear to have these quantities non-conserved. This means that it is not an inertial frame. 
##### Examples
1. Simple harmonic oscillator: 1D system, $\vec F=-k\vec x$, $V=\frac{1}{2}kx^2$. We are fixed at the oscillator's base. Since force is non-zero, momentum is not conserved. Since it is a 1D world, angular momentum is not defined. Since force is conservative, energy is conserved. 
2. Damped harmonic oscillator: $\vec F(x,\dot x)=-kx-\beta\dot x$. Since force is not conservative, energy is not conserved. The system will lose energy until it comes to rest. 
3. Particle moving under gravity: $\vec F=-\frac{GMm}{r^2}\hat r$, $V=-\frac{GMm}{r}$. We are at the center of the object whose gravity the particle is experiencing. Since force is nonzero, momentum is not conserved. Since force is central and conservative, angular momentum is conserved and so is energy. 
