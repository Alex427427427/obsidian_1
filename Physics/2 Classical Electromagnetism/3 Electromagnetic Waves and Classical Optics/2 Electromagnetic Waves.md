Tags: [[Electromagnetism]] [[Electromagnetic Waves]] [[1 Electromagnetic Wave Equations]] [[14 Maxwell Equation - Faraday's Law of Induction]] [[18 Maxwell Potential Equations in The Lorentz Gauge]] [[9 Macroscopic Maxwell Equations]]
___
The wave equations of electromagnetism produce travelling wave solutions, moving at $\frac{1}{\sqrt{\mu_0\epsilon_0}}$, which turned out to be the same as the speed of light $c$. These are the electromagnetic waves. Electromagnetic waves are light. Let's examine the simplest solutions from which linear superpositions can form all travelling wave shapes. These are harmonic solutions. 
## Plane Waves
##### Potentials
$$\phi(\vec r, t)=\phi_0e^{i(\vec k\cdot\vec r-\omega t+\theta_0)}$$
$$\vec A(\vec r,t)=\vec A_oe^{i(\vec k\cdot\vec r-\omega t+\theta_0)}$$
##### Vector Fields
$$\vec E(\vec r,t)=\vec E_oe^{i(\vec k\cdot\vec r-\omega t+\theta_0)}$$
$$\vec B(\vec r,t)=\vec B_oe^{i(\vec k\cdot\vec r-\omega t+\theta_0)}$$
##### Macroscopic Fields
$$\vec D(\vec r,t)=\vec D_oe^{i( k\cdot r-\omega t+\theta_0)}$$
$$\vec H(\vec r,t)=\vec H_oe^{i( k\cdot r-\omega t+\theta_0)}$$
## Spherical Waves (Only the Radial Dependence)
##### Potentials
$$\phi(r, t)=\frac{\phi_0}{r}e^{i(kr-\omega t+\theta_0)}$$$$\vec A(r,t)=\frac{\vec A_o}{r}e^{i( kr-\omega t+\theta_0)}$$
##### Vector Fields
$$\vec E(r,t)=\frac{\vec E_o}{r}e^{i(k r-\omega t+\theta_0)}$$
$$\vec B(r,t)=\frac{\vec B_o}{r}e^{i(k r-\omega t+\theta_0)}$$
##### Macroscopic Fields
$$\vec D(r,t)=\frac{\vec D_o}{r}e^{i( kr-\omega t+\theta_0)}$$
$$\vec H(r,t)=\frac{\vec H_o}{r}e^{i( k r-\omega t+\theta_0)}$$
## Properties
##### Oscillation Direction
1. The oscillation direction of the scalar case is trivial. 
2. For the vector case, all fields must oscillate **orthogonal to the direction of travel**, because in source-less space they must all be divergence-less. Note there may still be components of the field that point along the direction of travel, but those components must be constant. If we focus only on the components that are travelling, they are all orthogonal. 
3. For the electric and magnetic vector fields including the macroscopic ones, Faraday's law relates the changing components with a curl, which means the changing components of each field must be orthogonal to one another. **The electric and magnetic vector fields in a wave are orthogonal to each other**. 
##### Oscillation Phase
1. Faraday's law relates the magnitude of the changing components of each field. They are proportional to each other. **The electric and magnetic vector fields in a wave are in phase.**
##### Oscillation Amplitude
1. Faraday's law when applied to the harmonic solutions requires a spatial derivative for the electric field, and a temporal derivative for the magnetic field. This produces a factor of $\omega$ and $k$ such that the amplitudes of the electric and magnetic fields are related by a factor of $c$. **Magnetic vectors are $c$ times smaller than the electric vectors**. The same relationship holds for the potentials. 
2. If the medium is conductive, energy of the wave would distribute into the atoms that conduct while the fields pass through them. Deeper into the medium, the wave loses more and more energy until the amplitude is insignificant. **Conductive media are lossy, giving the fields additional exponential attenuation during propagation**. The exponential profile will be derived later. 
##### Wave Speed
For all solutions, $\vec k$ is the directed spatial frequency of the wave, $\omega$ is the temporal frequency, $\theta_0$ is the phase offset, which is a degree of freedom. Due to the speed of light constraining how the phase moves through spacetime, $\vec k$ and $\omega$ are constrained. 

In vacuum:
$$\frac{\omega}{|\vec k|}=c\ \ \ \ \ \ \ where\ \ \ \ \ \ \ c=\frac{1}{\sqrt{\mu_0\epsilon_0}}$$
In polarisable and magnetisable (and insulating) media:
$$\frac{\omega}{|\vec k|}=v\ \ \ \ \ \ \ where\ \ \ \ \ \ \ v=\frac{1}{\sqrt{\mu\epsilon}}$$
Leading us to define the relative speed (actually, the reciprocal of the relative speed, $n$) compared to vacuum:
$$n=\frac{c}{v}=\frac{\sqrt{\mu\epsilon}}{\sqrt{\mu_0\epsilon_0}}=\sqrt{\mu_r\epsilon_r}\approx\sqrt{\epsilon_r}$$
Where we have used the empirically observed fact that most media's relative permeability is extremely close to 1.
