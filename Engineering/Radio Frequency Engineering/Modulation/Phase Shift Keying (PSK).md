Category: [[Radio Frequency Engineering]] [[RF Modulation Schemes]]
___
Prerequisites: 
___
Related: [[Amplitude Shift Keying (ASK)]] [[Frequency Shift Keying (FSK)]]
___
A way to modulate digital signal onto analog carrier. 

Assigns discrete phase states to each symbol. 
![[BPSK.png]]
## Types
##### Binary Phase Shift Keying
Use only 2 phases spaced 180 degrees apart. 
##### Quadrature Phase Shift Keying
Use 4 phases spaced 90 degrees apart. 
![[QPSK.png]]
##### Others
Can take arbitrarily many phases, up till the noise makes it hard to identify them from one another. 
## Design Choice
Use Grey codes so that neighbouring symbols are a minimal Hamming distance away. Reduces information lost to a misidentification of symbol. 

