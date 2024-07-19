Category: [[Radio Frequency Engineering]]
___
Prerequisites: [[Scattering Parameters (S-Params)]] [[RF Reflection Coefficient and VSWR]]
___
Related: 
___
A chart that shows a conformally mapped complex plane. The original plane is the normalised impedance of the load impedance, relative to the impedance of the incident medium. 
$$z:=\frac{Z_L}{Z_I}$$
## Derivation
The chart has the singular purpose to **show the reflection coefficient** between the reflected RF wave and the incident wave as a complex number. Thus the conformal map is simply the equation for reflection coefficient: 
$$\Gamma=\frac{z-1}{z+1}$$
Yielding the following pretty looking graph: 
![[smith chart.png]]
![[smith chart overlay.png]]
## Properties
Note that the gridlines show the original z plane. Via complex analysis we know that straight lines get mapped to circles under conformal mapping. 

All positive real z get mapped to inside this circle with radius 1. This matches the intuition that the reflection coefficient must be a fraction. By locating the z of interest on this plot, we can determine the exact reflection coefficient. 

Notice that short circuit results in a reflection coefficient of -1, which makes sense because the short circuit forces the end of the transmission line to be at ground voltage, thus the wave will undergo fixed end reflection - which flips the wave. 

Notice that open circuit results in a reflection coefficient of 1, which makes sense because the open circuit gives freedom to the end of the transmission line to exist at any voltage, thus the wave will undergo a free end reflection - which does not flip the wave. 
## A Caveat - Conjugate Matching
The above conformal map actually is only useful for reflectionless impedance matching, because the output of the map is 0 only when the relative impedance is 1. 

Now this would be equivalent to maximum power transfer impedance matching if the source impedance is purely resistive, which is often the case. 

In the general rare case that the incident impedance is also reactive, we must introduce a different mapping: 
$$\boxed{\Gamma^\prime=\frac{Z_L-Z_S^*}{Z_L+Z_S}}$$
This reflection coefficient actually represents the power wave ratios, and will reduce to 0 when the incident and load impedances are conjugately matched. 