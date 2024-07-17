Category: [[Fourier Analysis]]
___
Prerequisites: [[Fourier Transform and Frequency Domain]] [[Discrete Fourier Transform]]
___
Related: 
___
The most important algorithm of all time. A fast algorithm to perform the Discrete Fourier Transforms:
$$X(k)=\sum_{n=0}^{N-1}x(n)e^{-i2\pi\frac{kn}{N}}$$
$$x(n)=\sum_{n=0}^{N-1}X(k)e^{i2\pi\frac{kn}{N}}$$
Where $x(n)$ is the $n$th sample of the original signal, $X(k)$ is the $k$th sample of the signal in the reciprocal space. 
## The Algorithm
To the filled in. 