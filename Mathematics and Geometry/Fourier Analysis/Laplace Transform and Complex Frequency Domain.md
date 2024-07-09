Category: [[Fourier Analysis]]
___
Related: [[Fourier Transform and Frequency Domain]] [[Z-Transform or Discrete Laplace Transform]]
___
A generalisation of Fourier Transforms [[Fourier Transform and Frequency Domain]] to the complex frequency (exponential enveloping oscillation) domain. 
## Forward Transform
$$\boxed{\mathcal L[f(t)](s)=\int_0^{\infty}f(t)e^{-st}dt:=\hat f(s)}$$
Here $s$ is a complex number. 
## Graph on the Complex Frequency Domain
The Laplace Transform results in a function over the complex plane. This is in fact the complex frequency domain. The function itself is complex valued at every location, but plots usually only plot the magnitude. The Fourier Transform can be recovered with a slice at the imaginary axis. 
## Inverse Transform
The Inverse Laplace Transform is slightly more cumbersome compared to the Inverse Fourier Transform, though the spirit of being symmetric to the forward Laplace Transform is still there. 
$$\boxed{\mathcal L^{-1}[\hat f(s)](t)=\frac{1}{2\pi i}\lim_{T\rightarrow\infty}\int_{\gamma-iT}^{\gamma+iT}\hat f(s)e^{st}ds=f(t)}$$
This corresponds to a line integral along a vertical line $Re(s)=\gamma$ where $\gamma$ is to the right of all singularities. Any $\gamma$ will result in the same original signal! 

If all singularities are to the left of $Re(s)=0$, $\gamma$ can be chosen to be 0 and the Inverse Laplace Transform becomes the Inverse Fourier Transform. The extra factor of $i$ at the front of the formula can then be absorbed into the term $ds$ to return $d\omega$, where $s=i\omega$.
