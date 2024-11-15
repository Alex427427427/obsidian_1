Category: [[Classical Optics]]
___
Prerequisites: [[Fourier Analysis]] [[Fourier Optics - Wavelet Derivation]]
___
Related: 
___
## Prerequisites
- Fourier analysis; convention: $1/2\pi$ only in the synthesis function.
- Wavelet Derivation of fourier optics
- Plane wave propagation 
## Angular Plane Wave Decomposition
An incident plane wave, after passing through an aperture $A(x)$, will only have certain angular components retained - those plane waves that, *all* having a total wave vector $k$, whose spatial frequency along $x$ compose the aperture function itself. 

It suffices to first see how these plane waves propagate over $z$ along the optical axis, then sum over their patterns. 
## Terminology and Symbology
- $\vec k$ refers to the wave vector **in the transverse plane to the optical axis**. i.e. $(k_x, k_y)$.
- $\vec r$ refers to the spatial coordinate **in the transverse plane to the optical axis**. i.e. $(x, y)$
- $k_\omega$ refers to the total length of the wave vector, $2\pi/\lambda$. Therefore, $k_\omega^2=k_x^2+k_y^2+k_z^2=\vec k^2+k_z^2$
- Transfer function refers to the aperture distribution. It is that term which, multiplied to an incident wave in the frequency domain, produces the outgoing waves in the frequency domain. $\Psi(x, 0)=\Psi_0 t(x)$ for an incident wave amplitude $\Psi_0$ and aperture function $t(x)$
- A function with a tilde on top denotes that function in the frequency domain. 
## Propagator 
For a **single** plane wave $\tilde\Psi(\vec k)$ with transverse frequency $\vec k$, propagating along $z$, all that happens is it picks up a phase of $e^{ik_zz}$. 
$$\tilde\Psi(\vec k,z)=e^{ik_zz}\tilde\Psi(\vec k, 0)$$
$$\tilde\Psi(\vec k,z)=e^{iz\sqrt{k_\omega^2-\vec k^2}}\tilde\Psi(\vec k, 0):=\tilde P(\vec k, z)\tilde\Psi(\vec k, 0)$$
The phase term is the **propagator** $\tilde P(\vec k, z)$. 
## Fresnel Approximation
Assume $z\gg \vec r$. This means the angular distribution is very close to 0. This is the paraxial approximation. The propagator becomes: 
$$\boxed{\tilde P(\vec k, z)\approx e^{izk_\omega(1-\vec k^2/2k_\omega^2)}=e^{izk_\omega}e^{-iz\vec k^2/2k_\omega}}$$
Another common notation is to separate the constant phase term:
$$\tilde P(\vec k, z):=e^{ik_\omega z}\tilde P(\vec k)$$
where
$$\tilde P(\vec k)=e^{-iz\vec k^2/2k_\omega}$$
## Final Spatial Pattern
To find the spatial pattern, simply do the inverse Fourier Transform:
$$\boxed{\Psi(\vec r, z)=\mathcal F^{-1}\left[\tilde P(\vec k,z)\tilde\Psi(\vec k, 0)\right]=\mathcal F^{-1}\left[\tilde P(\vec k, z)\mathcal F\left[\Psi(\vec r, 0)\right]\right]}$$
So the procedure to calculate the pattern some distance away from the aperture is: 
1. Fourier transform the wave at the aperture
2. Multiply by the propagator up to distance $z$
3. Inverse Fourier transform
## Convolution
By the final equation above, and the **convolution theorem** in [[1 Fourier Transform and Frequency Domain]], we know that the final wave amplitude is the convolution of the wave amplitude at the aperture, and the propagator (expressed in space, rather than frequency)
$$\boxed{\Psi(\vec r, z)=conv(\Psi(\vec r, 0), P(\vec r, z))=\int\Psi(\vec r^\prime, 0)P(\vec r-\vec r^\prime,z)d\vec r^\prime}$$
Where:
$$P(\vec r, z)=\mathcal F^{-1}\left[\tilde P(\vec k, z)\right]$$
$$\boxed{P(\vec r, z)=\frac{e^{ik_\omega z}}{i\lambda z}e^{ik_\omega\vec r^2/2z}:=e^{ik_\omega z}P(\vec r)}$$
Where:
$$P(\vec r)=\frac{1}{i\lambda z}e^{ik_\omega\vec r^2/2z}$$
Note that the denominator is the normalisation volume of the gaussian in 2 dimensions $(x,y)$. In one dimension it would have been $\sqrt{i\lambda z}$. 
$$P(x)=\frac{1}{\sqrt{i\lambda z}}e^{ik_\omega x^2/2z}$$
$$P(y)=\frac{1}{\sqrt{i\lambda z}}e^{ik_\omega y^2/2z}$$
$$P(\vec r)=P(x)P(y)$$

The convolution becomes: 
$$\boxed{\Psi(\vec r, z)=\frac{e^{ik_\omega z}}{i\lambda z}\int_{-\infty}^{\infty}\Psi(\vec r^\prime, 0)e^{ik_\omega(\vec r-\vec r^\prime)^2/2z}d\vec r^\prime}$$
Notice that the previously unknown constant of proportionality is now found to be $1/i\lambda z$. Again, this is only true for the 2D case. In 1D, it would have been $1/\sqrt{i\lambda z}$.
## Far Field Approximation
In the far field, $z$ is so large that the tiny angular distribution from the optical axis results in a large $\vec r$. So $\vec r \gg\vec r^\prime$. Consider the exponent:
$$ik_\omega(\vec r^2-2\vec r\cdot\vec r^\prime+{\vec r^\prime}^2)/2z$$
We can get rid of ${\vec r^\prime}^2$ provided that it results in almost no change in the phase. In other words, 
$$\frac{k_\omega {\vec r^\prime}^2}{2z}\approx0$$
In engineering, it is often that the maximum phase allowed is $90\degree$ , so:
$$\frac{k_\omega{\vec r^\prime}^2}{2z}<\frac{\pi}{2}$$
$$\boxed{\frac{2D^2}{\lambda}<z}$$
Is the condition for the far field. We have simply rearranged the equation and replaced $\vec r^\prime$ with $D$ - the maximum dimension of the radiating element. 
## Fraunhofer Integral
Finally, let's put everything together to find the wave amplitude in the far field, known as the Fraunhofer integral. 
$$\boxed{\Psi(\vec r, z)=\frac{e^{ik_\omega z}}{i\lambda z}e^{ik_\omega\vec r^2/2z}\int_{-\infty}^{\infty}\Psi(\vec r^\prime, 0)e^{-ik_\omega\vec r\cdot\vec r^\prime/z}d\vec r^\prime}$$
For a one dimension distribution:
$$\boxed{\Psi(x, z)=\frac{e^{ik_\omega z}}{\sqrt{i\lambda z}}e^{ik_\omega x^2/2z}\int_{-\infty}^{\infty}\Psi(x^\prime, 0)e^{-ik_x x^\prime}dx^\prime}$$
The intensity for a one dimension distribution:
$$\boxed{I(x, z)=\frac{1}{\lambda z}|\tilde\Psi(k_x,0)|^2}$$
Notice that as $z$ increases, the pattern does not fundamentally change, and only gets scaled. This is characteristic of the far field.  

One final step of substituting $k_x = k_\omega x/z$ will recover actual wave pattern as a function of $x$. 