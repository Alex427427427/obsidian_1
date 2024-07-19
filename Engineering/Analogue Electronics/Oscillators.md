Category: [[Analogue Electronics]]
___
Prerequisites: 
___
Related: 
___
## Fundamental Need
In many applications like clocks and radios, we need a circuit that, when powered, spontaneously produces an oscillating signal. This signal may or may not be sinusoidal. The most ubiquitous inertial-restorer system, though exhibits oscillation upon initial displacement, requires regular agitation to maintain the oscillations. Thus to design oscillators for our need, we need to consider something slightly different. 
## Feedback Oscillators
##### Criteria
An oscillator can be constructed with any system given *frequency dependent* positive feedback, and a non-attenuating loop gain. 
![[oscillator control diagram.png]]

The loop gain $A\beta$ need only fulfill the following 2 conditions at the desired oscillation frequency (remember, block diagram components are generally frequency dependent!):
1. $|A\beta|\geq 1$
2. $Arg(A\beta)=2\pi n$
This is the **Barkhausen criteria**. 
##### Mechanism
Due to the nature of the frequency dependent positive feedback, the input to the system need only be noise with microscopic origin. Noise contains power in all frequencies across the spectrum, and only those that experience zero phase shift will constructively interfere to appear at the output, overpowering the rest of the frequencies. For those frequencies such that there is any phase shift around the loop, or any loss around the loop, multiple copies of it will quickly overlap and either average to 0 (sum of all the phase shifts), or quickly attenuate to 0 (due to the loss), or both. 

In the case that the loop gain has magnitude greater than 1 and phase shift is zero, the oscillation quickly explodes. Usually this is clipped by the amplifier power supply, so the final signal could look distorted. However, if the loop gain is near 1, and the signal is not clipped, this type of oscillator can be approximated as **linear**. For this reason, these oscillators are often regarded as **linear and harmonic**.
##### Example: Microphone-Speaker Feedback
The microphone - speaker feedback system is actually an oscillator. The feedback is a physical distance to be travelled through space by the sound wave, thus the phase shift of this feedback path is frequency dependent. Only those frequencies and its harmonics that have full cycle phase shifts, will experience perpetual amplification, leading to oscillation at those frequencies. 
##### Example: Amplifier with Filtering Network as Feedback
The feedback network can be as simple as a bandpass filter. 
##### Example: Amplifier with Resonator Element as Feedback
The feedback network can also be an LC circuit, which only allows a certain resonant frequency to be maximally realised. Other resonant elements can be used, such as piezoelectric crystals. 
## Relaxation Oscillators
An oscillator can also be constructed with a storing element with a characteristic time behaviour, connected to a switch. The output is usually non-linear. 
##### Example: RC input to Schmitt Trigger
Inspect the circuit and use your knowledge of RC and Op Amp behaviour to understand how it works. 
