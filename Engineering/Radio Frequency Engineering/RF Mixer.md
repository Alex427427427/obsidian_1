Category: [[Radio Frequency Engineering]]
___
Related: [[Amplitude Modulation and Demodulation]]
___
The primary way of implementing amplitude modulation. **Multiplies 2 signals in time domain, convolves 2 signals in frequency domain**. Usually one of the inputs is the signal carrying information, often called "RF (Radio Frequency)", the other a pure oscillation, often called "LO (Local Oscillator)". It is usually denoted with a circle encasing a multiply sign on a diagram. The process of multiplying an input signal with an oscillation to create a frequency shifted signal is called **heterodyning**.
## Effect on Signals
See [[Amplitude Modulation and Demodulation]]. 

An ideal mixer is a 3 port system that multiplies 2 input signals in real time and outputs the product. Usually, one of the input is the baseband signal $f(t)$, the other a local oscillator at the carrier frequency $\omega$. 
$$f(t)\cos(\omega t)$$
As derived in the AM document, this results in the baseband signal beign shifted up to center about the carrier frequency. 
##### Mixing Pure Oscillations
What is not mentioned in that document is a special case - when the baseband is itself a pure oscillation. Then by inspecting the convolution in frequency domain (or by doing some opaque trig algebra), we see that the resultant signal will have 2 frequencies, **one at the sum of the 2 frequencies, the other at the difference**. 
## Implementation
##### General Principle: Non-linearity
We say that we want to multiply 2 signals, thereby convolving them in the frequency domain, and shifting one up to center about the other. It may seem that we need a very specific process or type of system to achieve this. Yet amazingly, *any* non-linear system will do. 

So to do signal multiplication we need to feed the 2 signals into any non-linear process, and the output side of that process will contain a signal component that is the product of the 2 signals. This may seem baffling, but consider the fact that a general function can be represented with a Taylor Series. If we simply feed the sum of the 2 inputs $x$ and $y$ into that non-linear function $f$, then in that Taylor Series, there are powers of the sum of the inputs. The higher orders become insignificant when the signals are small, thus:
$$f(x+y)\approx k_1(x+y)+k_2(x+y)^2=k_1x+k_1y+k_2x^2+2k_2\boxed{xy}+k_2y^2$$
As long as that $xy$ component exists, and is in its own frequency band from the other components, then we can use a band-pass filter to extract that. 

*In summary, non-linearity makes inputs interact among themselves. Multiplication is interaction. With this insight, we know in principle what is required to make an RF mixer.*
##### Example 1: Single diode
Attach the 2 voltage signals in series, and connect a diode and resistor across it. The voltage drop across the diode will perform the mixing via its exponential relationship between current and voltage, within which a product component can be found by band filtering. 

Since this results in a bunch of other signal components, we say this mixer is *unbalanced*.
##### Example 2: Switching baseband on and off
A switch that turns on and off at a regular frequency is like multiplying the other signal by a square wave. Now, the square wave itself is made of myriad frequency harmonics at discrete frequencies (periodic signals in time domain result in discrete frequencies in frequency domain). What's important is that the fundamental frequency of the square wave is sufficiently spaced from the rest, and that the product signal can be filtered through. 
##### Example 3: Switching baseband from positive to negative
A slightly more complex way to switch is done with a diode ring circuit and center tapped transformers. In the following diagram, "IF" is intermediate frequency, which is the baseband signal shifted up to some frequency already. For the purposes of understanding mixers, you may very well take this to mean the baseband signal. For more information about IF, see [[Superheterodyne Receiver]].
![[diode ring.png|300]]
If you follow the logic of the circuit, you will notice that the output, RF, is the baseband signal but every half cycle of LO causes it to flip sign. This is equivalent to multiplying by a square wave that goes not from 0 to 1, but -1 to 1. This is also equivalent to phase shifting the signal by 180 degrees. Again, the most important idea here is that the fundamental frequency associated with the square wave will shift the baseband up to the desired frequency. 
##### Example 3: Voltage Controlled Amplifier
Consider the local oscillator being the input to some variable gain amplifier. If the control of the gain is done by a voltage signal, and we use the baseband signal to do that, then we have exactly caused the baseband signal to form the envelope of the output signal, while the local oscillator forms the oscillations in the output signal. This is the best performing kind of mixer, but has complex circuit topology. 
##### Example 4: Inductors near saturation
Near saturation, inductors have non-linear behaviour. 
## Terminology
Let's now summarise some terms used to categorise mixers. 
##### Unbalanced
Mixers that produce the frequency of original signals (along with higher order products), in addition to the mixed frequencies, at the output. 
##### Balanced 
Mixers that suppress 
##### Passive and Active
Passive mixers, as with all notions of passivity in EE, are mixers that require no external power other than the input signals. Active mixers are not those. 