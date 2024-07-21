Category: [[Fourier Analysis]]
___
Prerequisite: [[2 Discrete Fourier Transform]]
___
Related: [[5 Laplace Transform and Complex Frequency Domain]]
___
This is a version of the Laplace Transform that discretises the time domain, but keeps the complex frequency domain continuous. 
## The Transform
##### Forward Transform
$x(n)$ is the $n$th sample of the signal, while $X(z)$ is its distribution on the complex frequency domain. The forward transform is like the discrete Fourier Transform case:  
$$X(z)=\sum_{n=0}^{\infty}x(n)z^{-n}$$
Notice that $z$ is a general complex number, and plays the role akin to $e^{-s}$ in the original Laplace Transform. 
##### Z Domain
We must now pause and look at the Z domain. You may want to assume it looks the same as the complex frequency domain, but that is not exactly right. The domain is no longer the exponent of $e$, but the result of the exponentiation. Thus, **every vertical line in the complex frequency domain is a circle in the z domain**. Regions of convergence will now be defined by circular boundaries instead of vertical lines. 

Since the original signal is discrete, the function must be periodic in some sense on the z domain, which it will always be, angularly. Since the original signal has infinite length, the function is continuous on the z domain. 
##### Inverse Transform
The inverse transform is the same as the original Inverse Laplace Transform. 
$$\boxed{x(n)=\frac{1}{2\pi i}\oint_C X(z)z^{n-1}dz}$$
Where $C$ is any counter clockwise curve encircling the origin and entirely within the region of convergence. Again, this is simply aiming to capture the information of the poles, which themselves show presence of such complex harmonic elements that need to be added up. 

