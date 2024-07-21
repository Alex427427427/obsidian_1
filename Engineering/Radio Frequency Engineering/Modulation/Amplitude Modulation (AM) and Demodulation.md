Category: [[Tags/RF Engineering]]
___
Related: [[RF Mixer]]
___
The most important way of shifting signals up and down along the frequency domain while preserving their shape. This is also known as **heterodyning**. This is very important because frequency bands have different properties and allow the transfer of information through any desired medium. 

There exists a concise and full explanation of how this process works, in addition to the explanations below. See the **shifting theorem** in [[Fourier Transform and Frequency Domain]].
## Terminology
**Baseband signal**: the original signal, with some upper bound in the frequency domain below which there is appreciable value, centered at 0 frequency. 
**Carrier frequency**: the frequency about which the baseband signal will be shifted up to. 
**Amplitude Modulation**: the act of shifting the baseband signal up to the carrier frequency while preserving its shape in the frequency domain.
**Amplitude Demodulation**: the act of recovering the baseband signal from the signal at carrier frequency, with no change to its profile in frequency domain. 
## Effect on Signals
##### Time Domain During Modulation
A signal $f(t)$ mixed with an oscillation $\cos(\omega t)$ gives:
$$f(t)\cos(\omega t)$$
This looks like the signal forms the envelope of a quickly oscillating **carrier wave**.
![[AM.png|300]]
##### Frequency Domain During Modulation
A signal $f(t)$ has some defined width in frequency domain, centered around 0. This is the **baseband** signal. It may take any arbitrary symmetric shape centered at 0 that attenuates to insignificance outside the bandwidth. The symmetry is an artefact of Fourier Transform. 

A pure oscillation $\cos(\omega t)$ is a delta spike (two, symmetric about 0, at $\pm\omega$) in the frequency domain. 

When the signal and the oscillation multiply in time domain, equivalently they get convolved in the frequency domain. This results in the original signal being reproduced (shifted) to center the 2 delta spikes in frequency domain. Their signal has been effectively shifted over to the carrier frequency. 
![[AM freq domain.png]]
##### Time Domain During Demodulation
Upon receiving, the signal may simply be multiplied again by the carrier oscillation to produce:
$$f(t)\cos^2(\omega t)$$
The meaning of this will be more apparent in the frequency domain, but even in the time domain, we can use algebra to get intuition. Trig identities tell us the above expression is equivalent to:
$$f(t)\left(\frac{1+\cos(2\omega t)}{2}\right)$$
Thus there is a component of the signal that is just the original baseband signal, while there is an additional copy centered about $2\omega$ frequency. 
##### Frequency Domain During Demodulation
Consider the same convolution picture from above. If the double-copied signal at the carrier frequency convolves with another pair of delta spikes at the carrier frequency, we get a signal at the baseband again. There will be 2 additional signals at twice the carrier frequency, which can be easily filtered out. 
![[AM demod.png]]
## Implementation
The multiply symbol in the above diagrams is responsible for amplitude modulation and demodulation. So we need a subsystem that performs multiplication on two signals. This is a **mixer circuit**. See [[RF Mixer]]
