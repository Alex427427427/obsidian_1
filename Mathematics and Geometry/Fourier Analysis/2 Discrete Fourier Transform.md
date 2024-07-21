Category: [[Fourier Analysis]]
___
Prerequisites: [[1 Fourier Transform and Frequency Domain]]
___
Related: [[Fast Fourier Transform (FFT)]]
___
## Foundational Facts
A point in time domain is a harmonic function in frequency domain. A point in frequency domain is a harmonic function in time domain. The domains are reciprocal (frequency is the reciprocal over period) or called conjugate spaces. Each domain represents a distribution of harmonic functions that make up the function in the reciprocal domain. The Fourier Transform is a mathematical statement of the above facts and converts these distributions between each other. 

(Small technicality: for this formalism to work, the frequency domain points represent a positive phase evolution harmonic function in time domain, while the time domain points represent a negative phase evolution harmonic function in frequency domain. This fact is seen in the analysis (forward transform) and synthesis (inverse transform) formulae of the Fourier Transform. If we apply the forward transform twice, we get the same signal flipped in the domain.)

The forward transform brings a function in time domain, $f(t)$, to a distribution in frequency domain, $\hat f(\xi)$: 
$$\hat f(\xi)=\int_{-\infty}^\infty f(t)e^{-i2\pi\xi t}dt$$
The inverse transform brings a distribution in frequency domain, $\hat f(\xi)$, to a function in time domain, $f(t)$:
$$f(t)=\int_{-\infty}^\infty\hat f(\xi)e^{i2\pi\xi t}d\xi$$
Notice how the functions are both treated as distributions of harmonic elements in the other domain to be integrated over. 
## Discretising the Frequency Domain
A periodic function in time domain has a discrete frequency domain profile. The general Fourier Transform assumes the periodicity to be infinity, allowing the analysis of arbitrary functions. However, most practical signals happen over a finite time $T$. For harmonic analysis of any finite time signal, we can assume the signal is periodic with a period equal to that total signal time. This restricts the possible frequencies to integer multiples of $1/T$. This case reduces to the Fourier series. 

In summary, **a periodic function in time is discrete in the frequency domain, with step size $1/T$**. 
## Discretising the Time Domain
With the same argument as the previous section, to discretise the time domain, we must make the frequency domain periodic. We also see from the previous section that a finite domain is equivalent to a periodic one in the context of harmonic analysis. So to discretise the time domain, we just need an upper bound in the frequecy domain. Carrying over the previous argument, an upper bound of frequency $\xi_{max}$ results in a time domain of step size $1/\xi_{max}$. 
## Discretising both Domains
The above two sections can be summarised in one image. 
![[discrete FT.png]]
The top row has time domain functions, while the bottom row has frequency domain functions. The left most column is the regular continuous Fourier Transform. The second column from the left shows that a periodic signal in time domain turns the frequency domain discrete. The third column shows that a periodic signal in frequency domain turns the time domain discrete. The final column shows that periodic signals in both domains make both domains discrete. This is the only practical way to analyse the original signal in column 1 computationally. Note that the function used here, a Gaussian, is the Fourier Transform of itself. See [[Gaussian is FT of Itself]].
## The Discrete Fourier Transform
Now we are ready to define the transform. 

The Discrete Fourier Transform takes a finite discrete time signal $f(t)$ and returns the finite discrete frequency distribution $\hat f(\xi)$. The finitude of the signal in both domains, hence its periodicity, ensures that the signals are discrete in both domains. 

Let's first convert to a common notation for both signals. The time signal $f(t)$ shall be renamed $x(n)$, and the frequency domain function $\hat f(\xi)$ shall be renamed $X(k)$. Both sequences have length $N$. Here, $x(n):=f(nT/N)$ which is the $n$th sample with timestep $T/N$, and $X(k):=\hat f(k/T)$ which is the $k$th sample in frequency domain with frequency step $1/T$. 

To derive the discrete versions, we begin from the regular transforms, and turn the integral into a sum: 
$$\hat f(k\Delta\xi)=\sum_{n=0}^{N-1}f(n\Delta T)e^{-i2\pi k\Delta\xi n\Delta T}\Delta T$$
$$f(n\Delta T)=\sum_{n=0}^{N-1}\hat f(k\Delta\xi)e^{i2\pi k\Delta\xi n\Delta T}\Delta \xi$$
Now substitute $\Delta\xi=1/T$ and $\Delta T=T/N$ and $x(n):=f(nT/N)$ and $X(k):=\hat f(k/T)$:
$$X(k)=\sum_{n=0}^{N-1}x(n)e^{-i2\pi \frac{kn}{N}}\Delta T$$
$$x(n)=\sum_{n=0}^{N-1}X(k)e^{i2\pi \frac{kn}{N}}\Delta \xi$$
Now this would be the most conceptually direct way to define the transform, but we commonly move the factor of $\Delta T$ to the second formula: 
$$\boxed{X(k)=\sum_{n=0}^{N-1}x(n)e^{-i2\pi \frac{kn}{N}}}$$
$$\boxed{X(k)=\frac{1}{N}\sum_{n=0}^{N-1}x(n)e^{i2\pi \frac{kn}{N}}}$$
Note that the uncertainties form the following relationship:
$$\Delta\xi\Delta T=\frac{1}{N}$$
In general, as long as the normalisation constants multiply to form this product, the fourier formalism will work. 