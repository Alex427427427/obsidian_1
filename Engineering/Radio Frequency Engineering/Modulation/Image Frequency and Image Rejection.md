Category: [[Tags/RF Engineering|RF Engineering]] 
___
Prerequisites: [[Amplitude Modulation (AM) and Demodulation]] [[RF Mixer]]
___
Related:
___
Consider a frequency domain populated by the following signals that are about to be demodulated down to IF: 
- The main signal at RF frequency
- A local oscillator (LO) at $RF-IF$ frequency
- Other signals at $RF - 2 IF$ frequency

The LO is necessary to convert RF down to IF via mixing ([[RF Mixer]]) (essentially a convolution in frequency domain). But the mixing process also sends the $RF-2IF$ signals down to IF. This unwanted signal is the signal at the **image frequency** and the signal that will be filtered out via **image rejection filters**. 

