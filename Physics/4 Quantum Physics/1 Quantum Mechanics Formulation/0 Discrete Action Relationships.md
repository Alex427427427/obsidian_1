Category: [[Quantum Mechanics]] [[Relativity]]
___
Prerequisites: [[1 Lagrangian, Action, Principle of Stationary Action]]
___
Related: [[5 Noether's Theorem - Symmetries of the Lagrangian]] [[Path Integral Formulation]]
___
While the birth of quantum formalism was forced upon by strange experiments, arguably the most important idea is the discovery of *discrete action*. 
## Discrete Action
##### Energy and Time
The photoelectric effect ([[Photoelectric Effect]]) and the ultraviolet catastrophe ([[Ultraviolet Catastrophe in Black Body Radiation]]) both imply that the electromagnetic wave performs discrete actions. While Einstein framed this as light being particles, they need not be - they just need to interact discretely, and as for the geometrical shape, they may as well be fully distributed entities. This discrete action was discovered to have a value of $h$ - which they named Planck's constant. And here comes the first important discovery: 
$$\boxed{E=hf}$$
What does this imply? It implies that **action** (more precisely, action per cycle) is that which is the product of energy and 1 period of an electromagnetic wave: 
$$h=ET$$
So a full cycle of an electromagnetic wave performs an action of $h$ with energy $E$, whatever that means. For convenience of not having to write $2\pi$ in certain places, the reduced Planck's constant was introduced, which is the **action performed per radian**. 
$$\boxed{\hbar:=\frac{h}{2\pi}}$$
Under which the energy equation becomes: 
$$\boxed{E=\hbar\omega}$$
**Let's assign the notion of action to be measured in this very unit $\hbar$.** All action can be measured against *the action performed by a 1-radian time evolution of an electromagnetic wave, $\hbar$*. Notice that it has the units of energy-time, consistent with the classical action. 
##### Momentum and Space
Light has momentum ([[7 Momentum and Angular Momentum of the EM Field]]). By using the equation $c=\omega/k$ (a statement of wave kinematics) and the energy-time action relation $E=\hbar\omega$, and the classical result $E=pc$, we can write down the momentum-space action relation. 
$$E=\hbar\omega=\hbar kc=pc$$
Thus
$$\boxed{p=\hbar k}\implies p\lambda=h$$
So the action unit $h$ is the action performed by an EM wave, over 1 cycle of spatial evolution, which must have momentum $p$. This matches with the energy-time result - the EM wave performs and action of $h$ over a full cycle, whether you measure that cycle in space or time. And the reduced action unit $\hbar$ is the action performed over 1-radian of spatial evolution. Notice that action also has the unit of momentum-space. 
##### Phase Evolution
The phase of an EM wave is: 
$$e^{i(kx-\omega t)}$$
Substituting the above results, we discover:
$$\boxed{Phase=e^{i(\frac{p}{\hbar}x-\frac{E}{\hbar}t)}}$$
What if we use this phase to encode the configuration changes (in $x$ and $t$) for arbitrary systems? Then the index of the exponential will contain the generator, and the total phase is the exponential map. 

Which fits with the classical Lie Algebraic result that: 
- Momentum is the generator of spatial evolution (here in quantum mechanics, the generator is $-i\frac{p}{\hbar}$)
- Energy is the generator of time evolution (here in quantum mechanics, the generator is $-i\frac{E}{\hbar}$)
Notice the unfortunate choice of negative sign convention for the spatial generator, indicating a wave travelling in the negative direction. 
##### Angular Momentum and Spatial Rotation
The above discoveries motivate a third action relation that is begging to be put into formula. The phase may change over spatial translation and time evolution. Can it also change over spatial rotation $\phi$? It can. 
$$e^{i\frac{L}{\hbar}\phi}$$
Notice that if $L=\frac{\hbar}{2}$, it immediately implies that it requires a spatial rotation of $\phi$ to evolve a full phase cycle, which is quite strange, and happens to be what most elementary matter particles obey. We call objects with such spatial rotation behaviour, **spinors**. 
## Matter Ensemble Waves and Quantum Dynamics
One leap of faith by Louis De Broglie resulted in the postulate that all matter that have momentum, may also have associated wavelengths according to the momentum-space action relation $p\lambda=h$. This was experimentally demonstrated by the double slit experiment ([[Single Particle Double Slit]]). Schrodinger later spent much time trying to derive a wave equation. Unfortunately for him, at the time, humanity did not yet have the Lie Algebraic insight drawn from the action relations above. 

If all **matter ensembles** - we shall denote these objects $\ket\Psi$ - contain a **phase** that makes them capable of producing the interference pattern in the double slit experiment, and that phase obeys the boxed exponential equation above, then these matter ensembles must obey the Lie Generator equations under any configuration change. For now, let's focus on coherent waves. 

For spatial translation: 
$$\boxed{\frac{\partial}{\partial x}\ket\Psi=-i\frac{p}{\hbar}\ket\Psi}$$
For time evolution:
$$\boxed{\frac{\partial}{\partial t}\ket\Psi=-i\frac{E}{\hbar}\ket\Psi}$$
For spatial rotation:
$$\boxed{\frac{\partial}{\partial\phi}\ket\Psi=-i\frac{L}{\hbar}\ket\Psi}$$
Note that these relationships are only valid for **coherent states** - those states that behave like a coherent wave. We also call these pure states. For treatment of composite states, which themselves have a ghostly linear superposition structure, the observables $p$, $E$, $L$, must be replaced by operators which are equipped to act on those linear structures. 
## The Rest of the Journey
If everything - absolutely everything - behaved as waves all the time, there would arguably be nothing unintuitive about quantum mechanics. Yet this is not the case. It is the *discrete action* that remains the central unsolved mystery to this day - from this, all difficulties emerge. The non-local collapse of the quantum state, the measurement problem, entanglement, quantisation of angular momentum... 

So we cast these action relationships aside for a while, and look at the formalism developed to deal with this most perplexing phenomenon of discrete action - we will examine Matrix Mechanics. In time, these action relationships will return, when we need them to map the matrix formalism to our particular physical universe. 
## Connections to Noether's Theorem
Notice that the action pairs: energy-time, momentum-space, also form a noether pair. Symmetry of time translation leads to constant energy. Symmetry of spatial translation leads to constant momentum. These all correspond to coherent wave intensities. They arise naturally out of wave mechanics. 
