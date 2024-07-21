Category: [[Fourier Analysis]]
___
Related: [[Frequency Domain]] [[2 Discrete Fourier Transform]]
___
A mathematical operation that transforms functions in one space to functions in the reciprocal space. Most commonly applied to the time domain and its reciprocal frequency domain, but can be applied to any reciprocal pairs of spaces. They are formally known as conjugate spaces. 
## From Frequency Domain to Original Domain
It is best to start by understanding that functions on some domain can be constructed via its components from the frequency domain. These components are harmonic oscillations. 

Indeed, it is a fact that all functions on some space can be constructed from harmonic basis functions on that same space via linear combination. Thus the function has an associated plot of how much of the various frequencies make it up across the frequency spectrum. This distribution in the frequency domain is its Fourier Transform. To construct the original function, simply sum up all the harmonic functions with frequencies that appear in the frequency domain, with the appropriate amplitude and phase. 

Since the frequency domain is a continuous distribution, the above sum shall be an integral over frequencies. Thus we have the **synthesis function** that constructs the original function $f(t)$ from the frequency domain profile $\hat f(\xi)$:
$$f(t)=\int_{-\infty}^{+\infty}\hat f(\xi)e^{i2\pi\xi t}d\xi$$
But how do we go the other way? In other words, construct the frequency domain distribution $\hat f(\xi)$ given the original function $f(t)$? 
## From Original Domain to Frequency Domain
Every value of $\hat f$ at a $\xi$ is a complex number representing the amplitude and phase of the harmonic oscillation with frequency $\xi$. We detect the presence of each $\xi$ with resonance. We multiply the original function with that particular harmonic oscillation, essentially wrapping the original function around the unit circle on the complex plane at a certain period and seeing where the totality of the function's center of mass is. This is done by the **analysis function**:
$$\hat f(\xi)=\int_{-\infty}^{+\infty}f(t)e^{-i2\pi\xi t}dt$$
Another easy way to understand this function is to see that the negative harmonic function $e^{-i2\pi\xi t}$ takes away that component of the oscillation away from the original function, while all other frequency components remain oscillatory with some shifted frequency. The oscillatory components all integrate to 0 over the entire domain. Only the component with frequency $\xi$ will remain present as a single amplitude and be integrated to infinity. This results in a dirac delta distribution on the frequency domain. In general, this results in a distribution on the frequency domain. 
## The Transform
The synthesis and analysis functions introduced above are in fact the Inverse Fourier Transform and the Fourier Transform respectively. 
##### In terms of Frequency $\xi$
$$\boxed{\hat f(\xi)=\int_{-\infty}^{+\infty}f(t)e^{-i2\pi\xi t}dt:=\mathcal F[f(t)]}$$
$$\boxed{f(t)=\int_{-\infty}^{+\infty}\hat f(\xi)e^{i2\pi\xi t}d\xi:=\mathcal F^{-1}[\hat f(\xi)]}$$
The integral operations that are the Fourier Transforms are denoted $\mathcal F$ and $\mathcal F^{-1}$. Notice the symmetry of the processes.
##### In terms of Angular Frequency $\omega=2\pi\xi$
The same formulae from above can have $\xi$ substituted with $\omega$. 
$$\hat f(\omega/2\pi)=\int_{-\infty}^{+\infty}f(t)e^{-i\omega t}dt$$
$$f(t)=\int_{-\infty}^{+\infty}\hat f(\omega/2\pi)e^{i\omega t}d\omega/2\pi$$
If we wish to redefine a frequency domain function that directly uses the formula on the top line, we would simply denote a new function $\hat f_1(\omega)=\hat f(\omega/2\pi)$. We can then discard $\hat f$ and relabel $\hat f_1$ as $\hat f$. Thus:
$$\boxed{\hat f(\omega)=\int_{-\infty}^{+\infty}f(t)e^{-i\omega t}dt}$$
$$\boxed{f(t)=\frac{1}{2\pi}\int_{-\infty}^{+\infty}\hat f(\omega)e^{i\omega t}d\omega}$$
Under this definition, there is less symmetry in the transforms. 
##### Angular Frequency Forms made Symmetric
We can make the above formulae symmetric by absorbing a factor of $\frac{1}{\sqrt{2\pi}}$ into $\hat f$.
$$\boxed{\hat f(\omega)=\frac{1}{\sqrt{2\pi}}\int_{-\infty}^{+\infty}f(t)e^{-i\omega t}dt}$$
$$\boxed{f(t)=\frac{1}{\sqrt{2\pi}}\int_{-\infty}^{+\infty}\hat f(\omega)e^{i\omega t}d\omega}$$
##### Most Common Conventions
The symmetric convention is most popular in physics. In electrical engineering, it is yet another one, placing the factor in the fourier transform and have it absent from the inverse transform. This convention maintains that the inverse fourier transform is a direct integration of frequency components. 
$$\boxed{\hat f(\omega)=\frac{1}{2\pi}\int_{-\infty}^{+\infty}f(t)e^{-i\omega t}dt}$$
$$\boxed{f(t)=\int_{-\infty}^{+\infty}\hat f(\omega)e^{i\omega t}d\omega}$$
**The existence of all these conventions introduce factors of $2\pi$ in many of the transform identities. Fortunately, for analytical purposes the absolute values of functions in the frequency domain is not important - all that's important is their distribution i.e. the form of the functions.**
## Alternate Derivation from Functional Analysis
The space of all square integrable functions $L^2$ over an interval $[-T/2, T/2]$ is a vector space. We may see functions in this space as infinite dimensional vectors, where the values of such functions at every $x$ are their components along each dimension. We can tame this space by defining a new basis. Each basis vector itself will be an infinite dimensional vector - a function itself - that pierces through the space with its infinite dimensional reach. Every function then, can be seen as a linear combination of these basis functions. The linear coefficients are the components. One such way to choose a basis is to use harmonic functions of the form $e^{i\omega t}$. Thus the Fourier Transform should take us from the original function to the linear coefficients of the harmonic basis functions. 

To find linear coefficients, we need a dot product - a projection of some total vector onto a normalised basis vector. For this to work we also require the basis to be orthogonal. We need an orthonormal basis. But to find the orthonormal basis, we need a dot product. We can redefine a dot product between vectors (which are functions) by extending the usual definition. The usual sum of components multiplied becomes an integral of the function values multiplied. Note the complex conjugate applied to complex spaces. 
$$\left<{f, g}\right>:=\int_{-T/2}^{T/2} f(t)g^*(t)\ dt$$
If we apply this dot product to basis functions of the form $e^{i\omega t}$, we need to do some scaling, either to the dot product formula or to the basis functions, in order for them to be unit "length". 

The Fourier Transformed space is in fact the **dual vector space** to the hilbert space of functions. 

Now we face a choice that leads us to produce two types of analysis. 
##### Discrete Dimensions - Fourier Series
If we want to decompose the space into discrete dimensions, we need the restriction that the function space is restricted to periodic functions on some interval. In this case, the functions can still go on forever, but we can analyse all its properties by focusing on one cycle. In this case, the set of basis functions become a set of $e^{i\omega t}$ where $\omega$ advances discretely. 

In such a choice, the dot product as defined above always returns $2\pi$ when applied to the basis functions and themselves, and $0$ when applied between basis functions. We see that orthogonality is obtained. Unit length can be obtained by either defining the basis to be $e^{i\omega t}/2\pi$, or the dot product to be $\frac{1}{2\pi}\int_{-T/2}^{T/2} f(t)g^*(t)\ dt$. The production of the total function is done with a sum, not an integral. This is the discrete **Fourier Series**. 

The Fourier Transform is a projection onto a basis vector: 
$$\boxed{\hat f(\omega)=\left<f(t),e^{i\omega t}\right>=\frac{1}{2\pi}\int_{-T/2}^{T/2} f(t)e^{-i\omega t}\ dt}$$
While the Inverse Fourier Transform is a linear combination: 
$$\boxed{f(t)=\sum_{\omega=0}^{\infty}\hat f(\omega)e^{i\omega t}}$$
Again, the factor of $2\pi$ can be pushed around. 
##### Continuous Dimensions - Fourier Transform
If we decompose the space into continuous dimensions where $\omega$ advances continuously, we must redefine the notion of linear combination. It will no longer be a sum over the basis vectors, but an integral, and the basis vectors shall be seen as possible values for a distribution. The space also no longer has to be within an interval, but can extend indefinitely. We can simply carry over the definitions in the discrete case, extend the interval to all space, turn the sum into an integral.
$$\boxed{\hat f(\omega)=\left<f(t),e^{i\omega t}\right>=\frac{1}{2\pi}\int_{-\infty}^{\infty} f(t)e^{-i\omega t}\ dt}$$
$$\boxed{f(t)=\int_{-\infty}^{\infty}\hat f(\omega)e^{i\omega t}d\omega}$$
In this case, the dot product of a basis function with itself will in fact return infinity. But this infinity must be such that when integrated over a distribution, returns the original harmonic oscillation, i.e. the harmonic oscillation has a component of 1. Thus the dot product has the following identity: 
$$\boxed{\left<e^{i\omega_1 t}, e^{i\omega_2 t}\right>=\delta(\omega_1-\omega_2)}$$
Which will be useful in quantum mechanics when defining positional basis states.  
## Graphs
The frequency domain graphs are often only plotted with their magnitude. 
## Elementary Facts
1. Harmonic oscillations have dirac delta spikes in the frequency domain. 
2. A cosine function has symmetric delta spikes in the frequency domain at $\pm\omega$. This is apparent from the exponential form of the function, $\cos(x)=\frac{1}{2}e^{ix}+\frac{1}{2}e^{-ix}$
3. A sine function has antisymmetric delta spikes in the frequency domain at $\pm\omega$. This is apparent from the exponential form of the function, $\sin(x)=\frac{1}{2i}e^{ix}-\frac{1}{2i}e^{-ix}$
4. All odd functions consist solely of sine functions. All even functions consist solely of cosine functions.
5. From 2,3,4, we see that all odd functions remain odd and all even functions remain even under the Fourier Transform. 
6. Intuitions about functions being transformed into their frequency domain, hold in the other direction. 
## Common Identities 
1. $\mathcal F[e^{i\omega_0 t}]=\delta(\omega-\omega_0)$ in EE convenction 
2. $\mathcal F[\cos(\omega_0 t)]=\frac{1}{2}\delta({\omega+\omega_0})+\frac{1}{2}\delta({\omega-\omega_0})$ in EE convention
3. $\mathcal F[\sin(\omega_0 t)]=\frac{1}{2}\delta({\omega+\omega_0})-\frac{1}{2}\delta({\omega-\omega_0})$ in EE convention
4. $\mathcal F[sinc(t)]=rect(\xi)$ in frequency convention
## Theorems
##### Shifting Theorem
$$\boxed{\mathcal F[f(t-t_0)](\xi)=e^{-i2\pi \xi t_0}\hat f(\xi)}$$
The Fourier Transform of a domain shifted signal is the same as the Fourier Transform of the original signal but multiplied by an imaginary exponential factor for each frequency. This is easy to see because shifting a signal along means every harmonic component picks up a corresponding phase shift. Since the shift is towards the right of the axis, the phase has been rotated backwards, hence the negative sign. 

In the other direction:
 $$\boxed{\mathcal F^{-1}[\hat f(\xi-\xi_0)](t)=e^{i2\pi\xi_0 t}f(t)}$$
 This statement means that shifting the signal in frequency domain will introduce an oscillation in the time domain with that frequency, while the original function will serve as its envelope. 

This theorem has the same mathematical form regardless of the convention chosen. 
##### Convolution Theorem
A convolution defines a process that takes in two functions and returns a new function by the following formula:
$$(f*g)\ (t)=\int_{-\infty}^{+\infty}f(\tau)g(t-\tau)\ d\tau$$
The convolution theorem is:
$$\boxed{\mathcal F[f*g](\xi)=\hat f(\xi)\hat g(\xi)}$$
This theorem says that convolution in one domain is equivalent to multiplication in the reciprocal domain. The proof is simple, just apply convolution and the shifting theorem. The same holds in the other direction. 
$$\boxed{\mathcal F^{-1}[\hat f*\hat g](t)=f(t)\cdot g(t)}$$
##### Similarity Theorem
$$\boxed{\mathcal F[f(at)](\xi)=\frac{1}{|a|}\hat f(\frac{\xi}{a})}$$
Inspect the form. When the time domain signal is squashed by a factor of $a$, we should expect the frequencies present to be multiplied by a factor of $a$, hence the dilation $\hat f(\frac{\xi}{a})$ seen on the right hand side. Additionally, the area under the distribution should be conserved, hence the attenuation of $1/|a|$ across all frequencies. Since squashing in the time domain does not introduce any phase shifts, the attenuation must also preserve the phase, so we take the magnitude only. 
##### Rayleigh's Theorem
$$\boxed{\int_{-\infty}^\infty|f(t)|^2dt=\int_{-\infty}^\infty|\hat f(\xi)|^2d\xi}$$
This is proven simply by expanding the fourier transform definitions. What is more important is that this theorem is a statement about energy conservation. In electrical engineering, $f$ is often a voltage, the square of which is proportional to power. Integrating all over all time gives the total energy contained in the signal. In the frequency domain, the value squared at each frequency tells the energy contained in that frequency. Integrating over all frequencies should return the total energy. 
##### Differentiation Theorem
$$\boxed{\mathcal F\left[\frac{df(t)}{dt}\right](\xi)=i2\pi\xi\hat f(\xi)}$$
This is trivial considering the behaviour of harmonic functions in calculus. A similar integral theorem can be made, where the extra factor on the RHS is divided instead of multiplied. 

In the other direction, we inspect the form of the synthesis equation but apply the analysis equation's logic, and can think of the frequency domain function as consisting of negative phase advancement harmonic functions *on the frequency domain*, where t is the "frequency". Thus:
$$\boxed{\mathcal F^{-1}\left[\frac{d\hat f (\xi)}{d\xi}\right](t)=-i2\pi t f(t)}$$
##### Final and Initial Value
Special case of the Laplace Transform theorems.
$$\boxed{\lim_{\xi\rightarrow0}i2\pi\xi\hat f(\xi)=f(\infty)}$$
$$\boxed{\lim_{\xi\rightarrow\infty}i2\pi\xi\hat f(\xi)=f(0)}$$
