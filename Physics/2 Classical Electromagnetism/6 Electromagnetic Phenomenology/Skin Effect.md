Tags: [[Electromagnetism]] [[Electromagnetic Phenomenology]] [[Eddy Currents]] [[4 EM Waves in Media]]
___
## Explanation from the Wave Viewpoint
At high frequencies the ideal conductor properties no longer hold, because charge distribution can never reach equilibrium. Potential can be different over it, and propagate along it, so can electric fields point along the conductor surface. A changing potential results in waves of charge being pushed back and forth while the energy change travels along the conductor at the speed of light. 

AC current conduction over wires can be thought of as this propagation of charge density pressure waves, carried out by the sinusoidal electric field pointing **along** the wires. Such a process must follow the wave and energy propagation laws within media. Namely, the electric field must distribute itself with exponential decay away from the conductor surface, where it will be most pronounced. 
$$E(z,t)=E_0e^{-\alpha z}e^{i(\omega t-k z)}$$
Where $E$ is the harmonic field extending into medium depth $z$, $\alpha=\sqrt{\frac{\mu\sigma\omega}{2}}$ is the attenuation factor, $k=\alpha$ is the spatial angular frequency, all derivable from first principles from Maxwell's equations in media. ([[4 EM Waves in Media]]) This means current is also distributed that way via ohm's law ([[6 Conduction, Conductance and Resistance, Energy Dissipation]]):
$$\vec J=\sigma\vec E$$
Additionally, EM waves radiate away from the wires, carrying small energy into space. 

This effect can be parameterised with a **skin depth** - the depth at which the current distribution decays to $1/e$ as strong as the surface current. Thus **$\alpha$ is the skin depth**. If all current is uniform and constrained to above the skin depth, it would result in the same total current. Thus the skin depth reveals the effective conducting cross section. The approximation fails when the exponential decay doesn't happen much before reaching the center axis of the conductor. 
## Explanation from Eddy Current Viewpoint
[[Eddy Currents]]
Alternatively, consider a harmonic current that is distributed uniformly over the cross section of a conductor. The change of the current creates magnetic field vorticity that is changing in time. This changing vorticity has an associated changing electric field vorticity, thus extra conduction. This is eddy current. The extra local currents, when imposed on the original uniform current, result in an exponential distribution. 