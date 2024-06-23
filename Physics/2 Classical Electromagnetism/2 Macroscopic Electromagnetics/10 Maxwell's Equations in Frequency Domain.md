Tags: [[6 Magnetic Induction Field (or Magnetising Field)]] [[17 Maxwell Equations in Potential Form]] [[Electromagnetism]] [[9 Macroscopic Maxwell Equations]]
___
We define yet another set of maxwell's equations for the time harmonic quantities in frequency domain, in order to deal with harmonic phenomena (such as wave propagation) in media later. This simplifies matters significantly. 
## Derivation
In the frequency domain, the fields at every point in space are oscillating with some angular frequency $\omega$. The time differential operator simply becomes a multiplication:
$$\frac{\partial}{\partial t}\rightarrow i\omega$$
##### Macroscopic
$$\nabla\cdot\vec D=\rho_f$$
$$\nabla\cdot\vec B=0$$
$$\boxed{\nabla\times\vec E=-i\omega\vec B}$$
$$\boxed{\nabla\times\vec H=\vec J_f+i\omega\vec D}$$
In dissipative (coductive media), the free current term can be replaced by $\sigma\vec E$.
##### Microscopic
Though the motivation for these equations is complex macroscopic phenomena, we can still define the microscopic parts which provides yet another alternate path to derive equations simply. 
$$\nabla\cdot\vec E=\frac{\rho}{\epsilon_0}$$
$$\nabla\cdot\vec B=0$$
$$\nabla\times\vec E=-i\omega\vec B$$
$$\boxed{\nabla\times\vec B=\mu_0\vec J+i\omega\mu_0\epsilon_0\vec E}$$
##### Harmonic Sources
Note that the sources are now time harmonic too. 