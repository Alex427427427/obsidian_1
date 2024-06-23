Tags: [[Electromagnetism]] [[Electromagnetic Waves]] [[10 Maxwell's Equations in Frequency Domain]] [[6 Energy Flow of the EM Field]] [[10 Maxwell's Equations in Frequency Domain]]
___
We have previously dealt with vacuum. Now we must turn our eye to media.

This material deals with linear (external electric fields produce polarisation field that has a linear relationship between input and output) isotropic (degree of polarisability is equal in all directions, such that external electric fields produce polarisation field along the same direction) material. **Anisotropic media can be considered along the principal axes, and the results linearly combined**. 
## Derivation of the wave equation
##### The General Case
First, under the isotropic assumption, we can convert the Faraday's law:
$$\nabla\times\vec E=-\mu\frac{\partial}{\partial t}\vec H$$
And with no current source, but in general partially conductive media, the magnetising field equation becomes:
$$\nabla\times \vec H=\sigma\vec E+\epsilon\frac{\partial\vec E}{\partial t}$$
In other words: 
$$\nabla\times\vec H=\left(\sigma+\epsilon\frac{\partial}{\partial t}\right)\vec E$$
Now take the curl of both equations. 
$$\nabla\times\nabla\times\vec E=-\mu\frac{\partial}{\partial t}\nabla\times\vec H$$
$$\nabla\times\nabla\times\vec H=\left(\sigma+\epsilon\frac{\partial}{\partial t}\right)\nabla\times\vec E$$
Substitute the original equations.
$$\nabla\times\nabla\times\vec E=-\mu\frac{\partial}{\partial t}\left(\sigma+\epsilon\frac{\partial}{\partial t}\right)\vec E$$
$$\nabla\times\nabla\times\vec H=-\left(\sigma+\epsilon\frac{\partial}{\partial t}\right)\mu\frac{\partial}{\partial t}\vec H$$
Apply the vector calc ids on LHS:
$$\nabla(\nabla\cdot\vec E)-\nabla^2\vec E=-\mu\frac{\partial}{\partial t}\left(\sigma+\epsilon\frac{\partial}{\partial t}\right)\vec E$$
$$\nabla(\nabla\cdot\vec H)-\nabla^2\vec H=-\left(\sigma+\epsilon\frac{\partial}{\partial t}\right)\mu\frac{\partial}{\partial t}\vec H$$
With the lack of sources (free charge and free current), the divergence of either field is 0. thus:
$$\nabla^2\vec E=\mu\frac{\partial}{\partial t}\left(\sigma+\epsilon\frac{\partial}{\partial t}\right)\vec E$$
$$\nabla^2\vec H=\left(\sigma+\epsilon\frac{\partial}{\partial t}\right)\mu\frac{\partial}{\partial t}\vec H$$
Expanding:
$$\boxed{\nabla^2\vec E=\mu\sigma\frac{\partial\vec E}{\partial t}+\mu\epsilon\frac{\partial^2\vec E}{\partial t^2}}$$
$$\boxed{\nabla^2\vec H=\mu\sigma\frac{\partial\vec H}{\partial t}+\mu\epsilon\frac{\partial^2\vec H}{\partial t^2}}$$
Which contains a diffusion (heat) term and a wave term. We see that energy dissipates in a conductive medium. The remaining term is the travelling component. 

To solve this we can employ green's functions, but that's more cumbersome than needed. We can bring all this into the frequency domain to solve them. 
##### Simplification
Macroscopically what is readily measured and usually of more interest, is the non-dispersive component of the field, propagating orthogonally to the plane of constant phase. To find out how this component behaves, we make some simplifications. 
1. The plane wave propagates along $z$.
2. The electric field oscillates in the $x$ direction.
3. The magnetising field oscillates in the $y$ direction. 
These relationships are consequences of the maxwell equation conditions discussed in [[2 Electromagnetic Waves]]. 
$$\boxed{\frac{\partial^2 E_x}{\partial z^2}=\mu\sigma\frac{\partial E_x}{\partial t}+\mu\epsilon\frac{\partial^2 E_x}{\partial t^2}}$$
$$\boxed{\frac{\partial^2 H_y}{\partial z^2}=\mu\sigma\frac{\partial H_y}{\partial t}+\mu\epsilon\frac{\partial^2 H_y}{\partial t^2}}$$
## The Wave Component In Frequency Domain
To solve the equations easily in this case, we bring this to the frequency domain. [[10 Maxwell's Equations in Frequency Domain]]. 

In the frequency domain, all fields are time harmonic - we only consider the harmonically oscillating component at every location in space, with a constant angular frequency variable $\omega$. The time derivative operator becomes $i\omega$. 
$$\frac{\partial^2 E_x}{\partial z^2}=i\mu\sigma\omega E_x+\mu\epsilon i^2\omega^2E_x\implies
\boxed{\frac{\partial^2E_x}{\partial z^2}=i\mu\omega(\sigma+i\epsilon\omega)E_x}$$
Similarly
$$\boxed{\frac{\partial^2H_y}{\partial z^2}=i\mu\omega(\sigma+i\epsilon\omega)H_y}$$
