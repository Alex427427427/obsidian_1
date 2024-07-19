Category: [[Analogue Electronics]]
___
Prerequisites: [[Voltage Controlled Oscillator (VCO)]]
___
Related: 
___
## Definition
A system whose output is phase locked with the input. The specific waveforms need not be the same, but the periodicity will be. Thus, a phase locked loop also locks frequencies. 
## How to Make One
A simple PLL consists of some sort of phase offset detector, whose output varies according to the phase offset of its 2 inputs. If the output is fed into a low pass filter (to make the whole system more stable), which is then fed into a VCO ([[Voltage Controlled Oscillator (VCO)]]), the output of the VCO is the output of the whole PLL system. This output should be fed into the phase offset detector. If this feedback path has a frequency divider block (in the digital case this is easily implemented with cascading flip flops), the output of the PLL will be a certain multiple of the input frequency. 
![[PLL.png]]
Nowadays, PLLs can be found in single ICs. 
##### Phase Comparator Block
This is the most complex block in the analog case, there is also more freedom in the design than one might expect. The output simply ought to monotonically increase with the phase shift, up to 180 degrees. Mixers can be used to implement it, its validity proven using maths unnecessary to go into here. 

Digital phase comparators are much simpler and can be done with logic gates and rectifiers. 
##### Unexpected Examples
Weakly coupled pendulum clocks undergo spontaneous synchronisation, a well known fact since Dutch physicist Christiaan Huygens in 1673. It is in fact a PLL! 
## Uses
##### Distributing Clock Signals
A PLL can be situated at distant parts of an electronic system to receive a clock signal of a single origin, and generate a clean local clock signal completely synchronised in frequency and phase. One might think local amplifiers and filters can achieve the same end goal, but PLLs have the added benefit of frequency multiplication and division in its feedback block, reduces jitter, signal degradation (which amplifiers and filters have a hard time fully cleaning). 
##### Multiplying Clock Signals
From the frequency division feedback block. 
##### Frequency Modulation and Demodulation
See [[Frequency Modulation (FM) and Demodulation]]
