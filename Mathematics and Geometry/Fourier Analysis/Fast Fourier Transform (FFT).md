Category: [[Fourier Analysis]]
___
Prerequisites: [[1 Fourier Transform and Frequency Domain]] [[2 Discrete Fourier Transform]]
___
Related: 
___
The most important algorithm of all time. A fast algorithm to perform the Discrete Fourier Transforms:
$$X(k)=\sum_{n=0}^{N-1}x(n)e^{-i2\pi\frac{kn}{N}}$$
$$x(n)=\sum_{n=0}^{N-1}X(k)e^{i2\pi\frac{kn}{N}}$$
Where $x(n)$ is the $n$th sample of the original signal, $X(k)$ is the $k$th sample of the signal in the reciprocal space. 
## The Algorithm
Implementing the algorithm directly from the formulae, we see that we need to do $N$ multiplications for each frequency, and since there are $N$ total frequencies, the algorithm will be complete in $N^2$ multiplication operations. (Most likely, each complex multiplication involves multiplication by sine and cosine, when implemented on a computer.)

The key to optimising this algorithm is the realisation that in the case of cosine, all odd frequencies share the same midpoint, and all even frequencies share the same midpoint (plus end points). This is true for sine as well. All the same frequencies under modulo 4 will share the same quarter points (including end points). This implies that most individual multiplications can be reused many times. 

A recursive division of the problem can reduce the $N$ multiplications required for computing a single frequency into $\log_2(N)$ multiplications. Thus the total steps of the Fast Fourier Transform scales with $N\log_2(N)$ instead of $N^2$.
