Category: [[Fourier Analysis]]
___
Prerequisites: [[1 Fourier Transform and Frequency Domain]] [[2 Discrete Fourier Transform]]
___
Related: 
___
## Aliasing
There is the original continuous signal in time domain. Then there is the discretisation - the sampling. If the sampling rate is too low, information about the original signal is lost. Think of high frequency characteristics that would not be captured by a sampling rate that is low. 
## The Nyquist-Shannon Sampling Theorem
The theorem says:
	For loss-less sampling, the sampling frequency $f_s$ (or $1/\Delta T$) must be at least twice the highest frequency $B$ of the original signal. 

To understand this theorem, we only need to establish that when the sampling frequency falls below the Nyquist frequency ($2B$), the signal will be distorted. 
## Cause of Aliasing when $f_s<2B$
First see [[2 Discrete Fourier Transform]].

When the time domain signal has a discrete step size $\Delta T$, the frequency domain representation is periodic with a size $f_s$. To recover the true signal, we only need to pass it through a low pass filter cutting off at $f_s$. 

Suppose the signal's baseband (the frequency profile of the original signal) is thinner than $f_s/2$, then the periodic overlay of the signal in frequency domain does not interfere with the baseband, because the baseband is not made to overlap with copies of itself at higher frequencies. However, as soon as $B>f_s/2$, the periodic overlay of the signal in frequency domain causes the edges of the profile in frequency domain to change. This is distortion. This effect is easiest seen with a diagram. 
![[aliasing.png]]
In other words, aliasing occurs whenever $f_s<2B$. 

The Nyquist sampling theorem is hereby justified. 