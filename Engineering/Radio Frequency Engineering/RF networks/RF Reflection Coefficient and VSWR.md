Category: [[Radio Frequency Engineering]]
___
Prerequisites: [[9 Reflection and Transmission Coefficients of EM Waves, Fresnel Equations]]
___
Related: [[Scattering Parameters (S-Params)]]
___
## Reflection
The ports of RF blocks in a network can be seen as optical media boundary. RF energy can reflect and transmit. The reflection coefficient is equivalent to its notion in EM wave propagation. It is a complex number indicating the amplitude and phase shift of the reflected wave relative to the incident wave. This reflection coefficient will appear in the diagonal of the s-tensor describing an RF block, and is denoted $\Gamma$. 

In general oblique incidence of EM waves, the coefficient takes complicated forms derived in [[9 Reflection and Transmission Coefficients of EM Waves, Fresnel Equations]]. Since the RF energy is always normal incidence onto an RF block (because voltage is always transferred directly from source to load), we may use the simpler form of normal incidence: 
$$\boxed{\Gamma=\frac{Z_L-Z_S}{Z_L+Z_S}=\frac{V_r}{V_s}}$$
It is often useful to consider the ratio of load and source impedances, $z$. Thus:
$$\boxed{\Gamma=\frac{z-1}{z+1}}$$
Note that just like in the discussion of [[9 Reflection and Transmission Coefficients of EM Waves, Fresnel Equations]], the reflection coefficient in the other direction is the negative, or half cycle phase shifted version to the original reflection coefficient: 
$$\boxed{\Gamma_{2\rightarrow1}=-\Gamma_{1\rightarrow2}}$$
## Voltage Standing Wave Ratio (VSWR)
Two sinusoidal waves travelling in opposite directions produce a standing wave with nodes if the amplitudes are equal. If they are not equal, the standing wave is never decreases to 0: 
![[voltage standing waves.png]]
With phasor intuitions, we can find the maximum amplitude and minimum amplitude by adding and subtracting the magnitudes of the individual waves. Thus, the **ratio** of the maximum voltage and minimum voltage of this total waveform is:  
$$\boxed{VSWR:=\frac{V_{max}}{V_{min}}=\frac{1+|\Gamma|}{1-|\Gamma|}}$$
