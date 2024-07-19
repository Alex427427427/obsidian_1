Tags: [[Electromagnetism]] [[Electromagnetic Waves]] [[3 Macroscopic EM Wave Equations]] [[2 Electromagnetic Waves]] [[10 Maxwell's Equations in Frequency Domain]] 
___
A medium is characterised by 3 properties that contain all macroscopic information of its optical behaviour - its conductivity $\sigma$ (that dissipates energy), permittivity $\epsilon$ (that stores elastic energy), and permeability $\mu$ (that stores kinetic energy in inertia). This is the electrical analogue of the 3 primary mechanical properties friction, (reciprocal of) elasticity, and inertia. 

The macroscopic wave equations in general media is: 
$$\nabla^2\vec E=\mu\sigma\frac{\partial\vec E}{\partial t}+\mu\epsilon\frac{\partial^2\vec E}{\partial t^2}\ \ \ \ \ \ \ and\ \ \ \ \ \ \ \nabla^2\vec H=\mu\sigma\frac{\partial\vec H}{\partial t}+\mu\epsilon\frac{\partial^2\vec H}{\partial t^2}$$
Only caring about the propagating components, we can collapse the spatial dimensions according to this simplification discussed in [[3 Macroscopic EM Wave Equations]]:
$$\frac{\partial^2 E_x}{\partial z^2}=\mu\sigma\frac{\partial E_x}{\partial t}+\mu\epsilon\frac{\partial^2 E_x}{\partial t^2}\ \ \ \ \ \ \ and\ \ \ \ \ \ \ \frac{\partial^2 H_y}{\partial z^2}=\mu\sigma\frac{\partial H_y}{\partial t}+\mu\epsilon\frac{\partial^2 H_y}{\partial t^2}$$
In the frequency domain: 
$$\frac{\partial^2E_x}{\partial z^2}=i\mu\omega(\sigma+i\epsilon\omega)E_x\ \ \ \ \ \ \ and\ \ \ \ \ \ \ \frac{\partial^2H_y}{\partial z^2}=i\mu\omega(\sigma+i\epsilon\omega)H_y$$
## Solutions
We understand immediately that the coefficient of $E_x$ shall be the square of the complex exponent $\gamma$ that will form our basis solutions over space $e^{\lambda z}$. 
$$\boxed{\gamma=\sqrt{i\mu\omega(\sigma+i\epsilon\omega)}=\alpha+ik}$$
With a sign ambiguity. 

Thus the solutions for the fields are:
$$\boxed{E_x(z,t)=E_{+}e^{i\omega t-\gamma z}+E_-e^{i\omega t+\gamma z}}$$
$$\boxed{H_y(z,t)=H_+e^{i\omega t-\gamma z}+H_-e^{i\omega t+\gamma z}}$$

The negative traveling waves are physically unrealisable due to the spatial growth of the wave amplitude along that negative direction of travel. 
## Geometric Properties
##### Attenuation, Oscillation, Phase Speed
**$\alpha$ is the spatial exponential scaling of the (propagating component of the) fields, and $\beta$ is the spatial oscillation frequency of the fields**. (The physically realisable solution has a $-\alpha$ in the exponent). 

The speed of phase is:
$$\boxed{v=\frac{\omega}{k}}$$
This speed is the **phase velocity**, the speed of propagation of an ABSTRACTION. The speed at which surfaces of constant phase are moving. The actual physical influence is still propagating at the speed of light. 

The **cause** of this change in phase velocity, is that as the surface of constant phase passes through infinitesimally thin slices of the medium, the polarisation and conductivity and magnetisation of the medium shifts the phase backward or forward infinitesimally. In reality all phase shifts are backward, but a shift backward beyond a half cycle $\pi$ appears to be a shift forward. Later, differing phase shifts along different principal axes of the medium can be used to create circularly polarised light. [[5 Polarisation of EM Waves]]
##### Relative Amplitudes Between $E$ and $H$
To find this, we return to the maxwell equations in frequency domain in general media, expressed in $E$ and $H$, and only the nonzero components of the curl have been picked out:
$$\frac{\partial E_x}{\partial z}=-i\omega \mu H_y\ \ \ \ \ \ \ and\ \ \ \ \ \ \ -\frac{\partial H_y}{\partial z}=(\sigma+i\omega\epsilon)E_x$$
The spatial partial derivative of the harmonic $E_x$ produces a factor of $-\gamma$:
$$-\gamma E_x=-i\omega \mu H_y\implies E_x=\frac{i\omega\mu}{\gamma}H_y=\frac{i\omega\mu}{\sqrt{i\omega\mu(\sigma+i\omega\epsilon)}}H_y=\sqrt\frac{i\omega\mu}{\sigma+i\omega\epsilon}H_y$$
Note that the reason we get a negative sign from the spatial derivative, is due to the frequency domain formulation of the solutions. We have chosen the phase to advance positively over time at a fixed location, by $i\omega t$, so a positive travelling wave solution must have $-\gamma z$ as the spatial exponent. This is in contrast to the usual choice of $e^{\gamma z-\omega t}$. 
##### Intrinsic Impedance
The coefficient of the magnetising field can be thought of as the intrinsic impedance $\eta$ (to energy propagation). It is in fact the impedance between dimensionally reduced properties of voltage and current. (The electric field is a voltage line density, the magnetising field is a current line density). The intrinsic impedance indeed has the unit of Ohms. 
$$\boxed{\eta=\sqrt\frac{i\omega\mu}{\sigma+i\omega\epsilon}}$$
Such that $\boxed{H_y=E_x/\eta}$. **In the case that $\eta$ is real, the electric and magnetising fields are in phase. In the case that it is complex, the electric and magnetising fields are out of phase**. By considering what happens to the angle of $\eta$ as we increase conductivity, we can see that the more conductivity, the more phase offset, and this phase offset is always $H$ lagging $E$. 

In vacuum, the wave impedance is:
$$\boxed{\eta_0=\sqrt\frac{\mu_0}{\epsilon_0}}$$
The meaning of the impedance has a direct parallel in transmission line - it is that complex parameter which relates the voltage and current in the transmission line. Thus different transmission line impedances can be thought of changing optical media. 
## Waves Through Lossless (Non-Conductive) Media
In lossless i.e. non-conductive i.e. dielectric i.e. insulating media, $\sigma=0$, which means the equations reduce to the usual wave equation, and $\gamma$ reduces: 
$$\gamma=\sqrt{i\mu\omega(\sigma+i\epsilon\omega)}=\sqrt{-\mu\epsilon\omega^2}=i\omega\sqrt{\mu\epsilon}=ik$$
Thus 
$$k=\omega\sqrt{\mu\epsilon}\ \ \ \ \ \ \ \ and\ \ \ \ \ \ \ \boxed{v=\frac{1}{\sqrt{\mu\epsilon}}}$$
Additionally, we define a factor that captures the change of speed. It is in fact the reciprocal of the relative speed of the phase compared to the speed of light in vacuum. 
$$\boxed{n=\frac{c}{v}=\frac{\sqrt{\mu\epsilon}}{\sqrt{\mu_0\epsilon_0}}=\sqrt{\mu_r\epsilon_r}\approx\sqrt{\epsilon_r}}$$
Where we have used the empirical observation that non magnetisable media usually have a relative permeability very close to 1. 

All this is on an attenuation-less wave, propagating with wave number $k$. 

The wave impedance is: 
$$\boxed{\eta=\sqrt{\frac{\mu}{\epsilon}}=\eta_0\sqrt\frac{\mu_r}{\epsilon_r}}$$
## Waves Through Lossy Media
Lossy, is when the medium has some conductivity that is not total, such that the first order term doesn't overpower the second order term in the differential equation, so that there are still propagating components. Conductivity is like a shield that prevents the incoming energy from penetrating the inside of the medium, but as a result generates and radiates heat. 

The case of lossy propagation is simply the general case derived above. An analytical solution is not necessary as these values can be calculated numerically in practice. 
## Waves in Conductive Media
In conductive media, $\sigma\rightarrow\infty$ compared to $\omega\epsilon$. This the spatial complex exponent into:
$$\gamma=\sqrt{i\mu\omega\sigma}=\sqrt{i} \sqrt{\mu\omega\sigma}=\left(\frac{1}{\sqrt2}+\frac{1}{\sqrt2}i\right)\sqrt{\mu\omega\sigma}=\alpha+ik$$
Thus:
$$\boxed{\gamma=\sqrt{\frac{\mu\omega\sigma}{2}}+\sqrt{\frac{\mu\omega\sigma}{2}}i=\alpha+ik}$$
And the wave impedance: 
$$\boxed{\eta=\sqrt\frac{i\omega\mu}{\sigma+i\omega\epsilon}=\sqrt{\frac{i\omega\mu}{\sigma}}=\sqrt{\frac{\omega\mu}{\sigma}}e^{45\degree}}$$
Meaning the magnetising field lags the electric field by 45 degrees. 
##### Skin Effect
[[Skin Effect]]
At high frequencies the ideal conductor properties no longer hold, because charge distribution can never reach equilibrium. Potential can be different over it, and propagate along it, so can electric fields point along the conductor surface. A changing potential results in waves of charge being pushed back and forth while the energy change travels along the conductor at the speed of light. 

AC current conduction over wires can be thought of as this propagation of charge density pressure waves, carried out by the sinusoidal electric field pointing **along** the wires. Such a process must follow the wave and energy propagation laws derived above. Namely, the electric field must distribute itself with exponential decay away from the conductor surface, where it will be most pronounced. This means current is also distributed that way. Additionally, EM waves radiate away from the wires, carrying small energy into space. 

This effect can be parameterised with a **skin depth** - the depth at which the current distribution decays to $1/e$ as strong as the surface current. Thus $\alpha$ is the skin depth. If all current is uniform and constrained to above the skin depth, it would result in the same total current. Thus the skin depth reveals the effective conducting cross section. The approximation fails when the exponential decay doesn't happen much before reaching the center axis of the conductor. 
