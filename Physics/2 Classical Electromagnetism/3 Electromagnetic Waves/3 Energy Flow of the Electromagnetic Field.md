Tags: [[Electromagnetism]] [[Electromagnetic Waves]] [[19 Energy is the Fluid Emerging from Charges]] [[20 The Electric Field Holds Energy Density]] [[21 The Magnetic Field Holds Energy Density]]
___
We are now ready to fully understand the dynamics of energy transfer in an electromagnetic field. 
## Energy Density in General
The electric field holds energy density $u$. [[20 The Electric Field Holds Energy Density]] It holds it with magnitude
$$u=\frac{1}{2}\epsilon_0|\vec E|^2$$
The magnetic field holds energy density. [[21 The Magnetic Field Holds Energy Density]]. It holts it with magnitude
$$u=\frac{1}{2\mu_0}|\vec B|^2$$
Therefore the total energy held at a location in space that contains both fields is: 
$$\boxed{u=\frac{1}{2}\epsilon_0 |\vec E|^2+\frac{1}{2\mu_0}|\vec B|^2}$$
## Energy Density in a Wave
Since the magnetic component can be directly related to the electric components in an electromagnetic wave, where $|\vec B|=|\vec E|/c$ thus $|\vec B|^2=\mu_0\epsilon_0|\vec E|^2$. Thus, the total energy density (the PROPAGATING COMPONENT OF...) is:
$$\boxed{u=\epsilon_0|\vec E|^2}$$
We can also define the **energy density current** $\vec S=u\vec v$. This is the energy surface density delivered per unit time. For EM waves $|\vec v|=c$. Since $|\vec E|^2$ can be thought of as $|\vec E||c\vec B|$, and we know that it's only the orthogonal components of the electric and magnetic field that give the propagating energy, the general case must also hold true given a cross product. 
$$\boxed{\vec S=c^2\epsilon_0\vec E\times\vec B=\frac{1}{\mu_0}\vec E\times\vec B}$$
This is known as the poynting vector. 

The **intensity** - surface power density - of an electromagnetic wave, is simply the magnitude of the energy density multiplied by the speed of light, which is the definition of energy density current, and indeed the magnitude of the poynting vector. In light, this is proportional to brightness. 
$$\boxed{I=c\epsilon_0|\vec E|^2=\sqrt{\frac{\epsilon_0}{\mu_0}}|\vec E|^2}$$
The constant $\sqrt{\frac{\epsilon_0}{\mu_0}}$ is the reciprocal of another concept, the **intrinsic impedance of free space** $\eta_0=\sqrt{\frac{\mu_0}{\epsilon_0}}$.

Notice the square proportionality between power and field. **Indeed, the relationship between the field amplitudes and energy density is the same between the quantum wavefunction amplitudes and probability density**. See [[Speculation]] [[Electric Fields can Model Quantum Wavefunction]]. 

The square proportionality also illuminates the $1/r$ scaling of the spherical field. Thanks to the inverse scaling, the power flux has an inverse square scaling, which conserves energy as the shell of energy expands. 
## Yet Another Continuity Equation
Considering the outflow of energy from a location, and energy delivered to a current in that location from the electic field at that location (magnetic fields do no work), we have a continuity equation for energy density:
$$\boxed{\frac{\partial u}{\partial t}=-\nabla\cdot\vec S-\vec J\cdot\vec E}$$
Note that $\vec J\cdot\vec E$ is power delivered to the current via simple dimensional analysis. This is Poynting's theorem. 

Via complicated detailed derivation from first principles, we can see that the aforementioned poynting vector formula for the EM wave holds in general. This is a bit surprising because in general the electric and magnetic fields do not have a scaling of $c$, which they do in EM waves. The technicality lies in that the propagating component of the electric field and the magnetic field **will** in general be the correct relationship. The poynting vector formula abstracts that away and reveals that the net electric and magnetic field components contains all that information. 
