Category: [[Radio Frequency Engineering]]
___
Prerequisites: [[RF Reflection Coefficient and VSWR]] [[Smith Chart]]
___
Related: [[RF Networks]] [[Scattering Parameters (S-Params)]]
___
## Reflectionless Impedance Matching
If we wish to waste no power to be reflected at the RF block back at the source, we would do reflectionless impedance matching - making the load impedance equal to the incident impedance. This is like making 2 media have the exact same optical characteristics. In this case, add matching networks such that the value of $\Gamma$ (reflection coefficient, output of the smith chart mapping) on the smith chart approaches 0. 
## Maximum Power Transfer Impedance Matching - Conjugate Impedance Matching
To deliver maximum power, the philosophy is different. We ought to make the load impedance the complex conjugate of the source impedance. It can be proven that this facilitates maximum power delivered to the load from the source, despite having some waste. In contrast, reflectionless impedance matching results in maximum efficiency. The two cases are equivalent when source impedance is purely resistive. 