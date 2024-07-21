Category: [[Tags/RF Engineering]]
___
Prerequisite: [[Fourier Analysis]] [[Fourier Transform and Frequency Domain]]
___
Related: [[Phase Locked Loop (PLL)]] [[Phase Modulation (PM)]]
___
## Introduction
![[AMFM.png]]
See image above for what FM looks like. Frequency Modulation is complementary to Phase Modulation, which together form angle modulation. Amplitude modulation is its own thing. 
## Comparison with AM
##### Advantages
It has a larger signal to noise ratio - rejects RFI better than an equal power AM signal. For this reason, most music is broadcast over FM. 
##### Disadvantages
Under multipath conditions, FM performs much worse and has high frequency artefacts not present with AM. 
## Theory
We start with a pure sine wave $A_c\cos(2\pi f_c t)$. In AM, the amplitude term is replaced by the signal. If we apply this logic to FM, that we replace the frequency term with the signal, we would get the wrong idea:
$$y(t)=A_c\cos(2\pi x_m(t))$$
where $y$ is the modulated signal and $x$ is the original signal. This is wrong, because instantaneously shifting the frequency like this would produce spurious local extrema. To get the smooth variation, we actually need to reinterpret FM as an integral:
$$y(t)=A_c\cos(2\pi\int_0^t f(\tau)d\tau)$$
Where $f(\tau)$ is a time varying frequency. In the case of the carrier, this equation reduces to the pure cosine equation. We then add a frequency deviation, scaled by the original signal, into this integral:
$$y(t)=A_c\cos(2\pi\int_0^tf_c+\Delta fx_m(\tau)d\tau)$$
$$\boxed{y(t)=A_c\cos(2\pi f_c t+2\pi\Delta f\int_0^tx_m(\tau)d\tau)}$$
This produces the expected FM curve. It is actually a special case of the general form of **angle modulation**: 
$$y(t)=A_c\cos(2\pi f_c t+\phi(t))$$
##### Interpretation
The change in the signal happens at the phase level, hence why FM is part of angle modulation. Consider the boxed FM equation, in which the bracketed terms describe the angle advancement of the signal. We must add to our repertoire of intuitions and see frequency as the rate of angle advancement - as a velocity. $f_c t$ is a constant angle advancement - a straight line - which corresponds to an unaltered oscillation. Frequency modulation then can only be properly done by changing the instantaneous velocity of that angle advancement - with an auxiliary time integral over $\tau$. The signal provides that change in velocity. 

If we did not do the integral, but naively multiply the frequency with the signal, we would be trying to dictate the *final* angle displacement to reflect that change in average speed, swinging the straight line curve up and down, instead of instantaneously steering it up and down. 

For the above reasons, frequency modulation is usually properly defined as varying the "instantaneous" frequency of the wave. 
## Frequency Domain Characteristics
As expected, most of the energy of the signal is contained within $f_c \pm\Delta f$. However, not all. Via Fourier analysis ([[Fourier Analysis]]), we can see that the actual frequency spectrum extends infinitely. Higher order components are often neglected in practical design problems. 
## Implementation
##### Modulation
FM can be generated directly by feeding the signal into a VCO ([[Voltage Controlled Oscillator (VCO)]]). Another way is to first integrate the signal and then feed into phase modulation ([[Phase Modulation (PM)]]). Then the frequency components are all multiplied to enter the FM frequency range. This second way is said to be indirect. 
##### Demodulation
This can be done in many ways, such as the Foster-Seeley discriminator, or PLLs ([[Phase Locked Loop (PLL)]]). The exact mechanism requires further study by the note taker. 

Alternatively, software defined radios can digitally demodulate. 
