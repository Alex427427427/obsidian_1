Category: [[Classical Optics]]
___
Prerequisites: [[1 Fourier Transform and Frequency Domain]] [[Antenna Aperture Function]]
___
Related: [[14 Diffraction and Interference of EM Waves]]
___
Fourier optics brings the understanding of light propagation to a new height. 
## Summary of Prerequisites
##### Fourier and Harmonic Analysis
The fourier transform brings functions from one domain to the conjugate domain, which is the reciprocal of the original domain. The conjugate domain contains the distribution function, each location in the conjugate domain representing a harmonic in the original domain. 
##### Aperture
A function over space - assigning a value to each location representing the effective aperture area density at that location - how much total power will be received by a plane wave arriving from that direction with a certain irradiance. 
## The Beginning - Diffraction
If a unit plane wave is incident on an aperture, a diffraction pattern is observed. 
![[fourier optics expl 1.png]]
This is the Fraunhofer diffraction. 
##### Qualitative Explanation
Before there was the notion of Fourier optics, it was intuited that every location of space serves as an infinitesimal radiator of optical energy, their collective radiations combining to form the propagating wavefronts. Thus every location inside the aperture where there is appreciable value, will have a spherical wave emerging from it. The interference of such waves produces the interference pattern on the screen. 
##### Analytical Description
(Note: the following derives the amplitude of the potential. To obtain the electric field, perform a spatial derivative and end up with an extra factor of $ik$ or $i2\pi/\lambda$ at front.)

Let's put the above idea to formulae. Let us restrict our view to one dimension. $x$ shall be the axis pointing up along the aperture plane, $z$ shall be the axis pointing perpendicular to it, towards the right, with the aperture plane at zero. Suppose the incident wave is restricted to a harmonic wave, with wavelength $\lambda$ and thus $k=2\pi/\lambda$. Then for a point source situated at $x_0$, the total wave pattern $\Psi$ at a distance $r$ away from the source is just the spherical wave $e^{ikr}/r$ integrated by the dirac delta distribution. 
$$\Psi(r)=\int_{-\infty}^\infty\delta(x^\prime-x_0)\frac{e^{ikr}}{r}dx^\prime$$
Note that $r$ is the distance from the specific source at $x_0$. If we express this term in $z$ and $(x-x^\prime)$ with pythagoras, we get:
$$\Psi(z,x)=\int_{-\infty}^\infty\delta(x^\prime-x_0)\frac{e^{ik\sqrt{z^2+(x-x^\prime)^2}}}{\sqrt{z^2+(x-x^\prime)^2}}dx^\prime$$
For a general aperture density distribution, or the aperture function $A(x)$, it is:
$$\Psi(z,x)=\int_{-\infty}^\infty A(x^\prime)\frac{e^{ik\sqrt{z^2+(x-x^\prime)^2}}}{\sqrt{z^2+(x-x^\prime)^2}}dx^\prime$$
##### Para-axial approximation - intermediate field
In the paraxial approximation, where $z\gg x$, the denominator reduces to $z$. However, the exponent of $e$ cannot be reduced as such, because the complex exponential map has the possibility of sending $kx$ to anywhere in the phase cycle. Thus we maintain the presence of $x$ to first order:
$$\Psi(z,x)=\int_{-\infty}^\infty A(x^\prime)\frac{e^{ikz(1+(x-x^\prime)^2/2z^2)}}{z}dx^\prime$$
$$\boxed{\Psi(z,x)=\frac{e^{ikz}}{z}\int_{-\infty}^\infty A(x^\prime)e^{ik(x-x^\prime)^2/2z}dx^\prime}$$
This is the **Fresnel integral** - where the only approximating assumption is the paraxial. This integral is valid in the intermediate field pattern. 
##### Far-field approximation - Fourier Transform Emerges
To proceed, we make the further assumption that the slit itself is very small compared to the distance along $x$ in which we measure the radiation pattern. In other words, $x^\prime\ll x$. Thus:
$$\Psi(z,x)=\frac{e^{ikz}}{z}\int_{-\infty}^\infty A(x^\prime)e^{ikx^2(1-2x^\prime/x)/2z}dx^\prime$$
$$\Psi(z,x)=\frac{e^{ikz}}{z}e^{ikx^2/2z}\int_{-\infty}^\infty A(x^\prime)e^{-ikxx^\prime/z}dx^\prime$$
Now, we make the observation that $kx/z$ is approximately $kx/r$, which is the $x$ component of the wave vector $\vec k$ with magnitude $k$. thus:
$$\boxed{\Psi(z,x)=\frac{e^{ikz}}{z}e^{ik_xx/2}\int_{-\infty}^\infty A(x^\prime)e^{-ik_xx^\prime}dx^\prime}$$
We now see the integral transform that is the Fourier Transform. **This is the foundation of Fourier optics**, also called the Fraunhofer diffraction equation. We should now interpret this result. 
## Interpretation
##### The terms outside integral
The complex exponential terms outside the integral do not affect the power distribution of the field that lands along $x$. For one, the term involving $z$ is fixed for all values of $x$, and two, the term involving $x$ only introduces a phase shift - an additional phase shift related to the fact that the wave has to travel longer to reach larger $x$. This term will disappear when we convert to the observable intensity. 
##### The Output of the Fourier Transform
We see a Fourier Transform, but from what domain to what domain? $x^\prime$, the position domain of the aperture distribution is converted to $k_x$, the wave vector component that points in the $x$ direction. 

Let's assume $z$ is fixed, because we consider the field pattern at a detector screen at fixed distance. Then the function $\Psi$ can be associated with a function of $k_x$, by a simple dilation along the $x$ direction by a factor of $z$ (i.e. substituting $x/z$ in place of $x$). Then, this new function, call it $G(k_x)$, upon appropriate scaling, can be directly related to the fourier transform of the aperture function. 
$$\boxed{G(k_x)=\int_{-\infty}^\infty A(x)e^{-ik_x x}dx}$$
*So what exactly is this function $G$?* 

Well, it is a distribution over $k_x$. A distribution of harmonic waves with $k_x$, such that these waves combine in the $x$ direction to form the aperture distribution. More aperture - more intensity let through. In constructing $G$, we have found all the harmonic modes with the right transverse frequency that the aperture lets through. The fourier transform of this distribution recreates something proportional to the aperture fuction (up to a projection factor):
$$\boxed{A(x)=\int_{-\infty}^\infty G(k_x)e^{ik_xx}dk_x}$$
##### Angular Spectrum
A distribution over $k_x$ is equivalent to a distribution over angles, in the far field approximation. So the distribution $G$ is also a distribution over the angular spectrum. 
## Applicable Intuitions
##### Visible objects are aperture functions
Now consider an object scattering monochromatic light. (See [[15 Scattering of EM Waves]]) Scattering makes every point on the surface act like a point spherical radiator. The locations on the surface that leads to more scattering, is like an effective aperture with higher density. Altogether, the appearance of the whole object's surface is an aperture function. (Here we consider the angular aperture distribution instead of a planar aperture distribution.) The behaviour of a totality of colours may be simply overlayed from the monochromatic scenarios of each colour. 
##### Light scattered from visible objects are the fourier transform of the object's appearance
Self evident from fourier optics. 
##### A Lens Performs Fourier Transform
A lens takes incoming faraway radiation patterns, and focuses each angular component onto a single point on the focal plane. This act reconstructs the aperture function that brought the radiation from far away. Lenses perform Inverse Fourier Transforms on faraway light to form an image on the focal plane. In the other direction, an aperture function placed at the focal plane will emit radiation that passes through the lens and become an angular distribution - the lens performs forward Fourier Transforms on images on the focal plane. 
