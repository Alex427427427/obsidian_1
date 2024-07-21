Category: [[Tags/RF Engineering]] [[RF Modulation Schemes]]
___
Prerequisites: [[1 Fourier Transform and Frequency Domain]] [[Shannon's Information Theory]] [[Amplitude Modulation (AM) and Demodulation]]
___
Related: [[Amplitude Shift Keying (ASK)]] [[Phase Shift Keying (PSK)]]
___
## Introduction
The most popular encoding scheme used today. Modulates digital signal onto analog carrier. Identifies symbols with discrete chosen amplitude and phase combinations, spaced apart as a grid on the complex plane. 
![[16QAM.png]]
If the total number of symbols is $N$, then each symbol has $\log_2(N)$ bits. ([[Shannon's Information Theory]])
![[common qam.png]]
## Implementation
##### Modulation
The modulation is quite ingenious and simple. Every symbol in the QAM scheme can be reached by discretely amplitude modulating two orthogonal carrier waves, and adding their outputs together. One is called the $I$ signal for "In phase", the other $Q$ for "Quadrature". 
##### Demodulation
The received signal can be mixed ([[RF Mixer]]) with a sine and cosine function individually, to recover the two components. The mixing produces the original signal, and high frequency components that can be low pass filtered out. The phase must be recovered too, which requires a clock - sometimes included in the signal itself as a burst. 
## Noise
The maximum tolerable noise is one that brings the intended symbol to the edge of the circle centered at the symbol on the complex plane, that is tangent to neighbouring circles. 