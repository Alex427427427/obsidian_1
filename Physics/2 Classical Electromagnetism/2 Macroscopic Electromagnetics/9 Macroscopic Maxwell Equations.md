Tags: [[Electromagnetism]] [[5 Electric Displacement Field]] [[6 Magnetic Induction Field]] [[5 Maxwell Equation - Gauss' Law for Electric Field]] [[13 Maxwell Equation - Ampere's Law for Magnetic Field Creation]] [[11 Maxwell Equation - Gauss' Law for Magnetic Field]] [[14 Maxwell Equation - Faraday's Law of Induction]]
___
## The Charge Source Law
The displacement field's interpretation directly leads to a modified version of the first Maxwell's Equation:
$$\oint_S\vec E\cdot d\vec A=\frac{Q}{\epsilon_0}\rightarrow\oint_S\vec D\cdot d\vec A=Q_{free}$$
Which says the displacement field is the apparent charge density at the gaussian surface enclosing a displaced charge. This equation holds on the macroscopic scale, where the polarisation behaviour of media, and the complex microscopic field patterns, are abstracted away. 

In differential/local form:
$$\nabla\cdot\vec E=\frac{\rho}{\epsilon_0}\rightarrow\nabla\cdot\vec D=\rho_{free}$$
The equations can also be obtained by substituting the full definition of the displacement field, and using the bound charge expressions. 
## The Current Source Law
Starting from the Ampere Law
$$\nabla\times\vec B=\mu_0\vec J+\mu_0\epsilon_0\frac{\partial\vec E}{\partial t}$$
Substitute the macroscopic field definitions:
$$\nabla\times(\mu_0\vec H+\mu_0\vec M)=\mu_0\vec J+\mu_0\epsilon_0\frac{\partial}{\partial t}\frac{(\vec D-\vec P)}{\epsilon_0}$$
Move everything over:
$$\nabla\times\vec H=\vec J+\frac{\partial\vec D}{\partial t}-\frac{\partial\vec P}{\partial t}-\nabla\times\vec M$$
Realise that the negative terms equal to bound current:
$$\nabla\times\vec H=\vec J_{free}+\frac{\partial\vec D}{\partial t}$$
And we can create the corresponding integral form by inspection:
$$\oint_C\vec H\cdot d\vec l=I_{free}+\frac{\partial}{\partial t}\int_S\vec D\cdot d\vec A$$
## The Induction Law
Substitute the definitions into the faraday's law and we will obtain:
$$\nabla\times\vec D=-\mu_0\epsilon_0\frac{\partial\vec H}{\partial t}-\mu_0\epsilon_0\frac{\partial \vec M}{\partial t}+\nabla\times\vec P$$
Examine the magnetisation and polarisation terms. $\mu_0\vec M$ represents the response magnetic field $\vec B_{res}$ as a result of the magnetisation, while $-\vec P/\epsilon_0$ represents the response electric field $\vec E_{res}$. Thus these two terms actually form a Faraday's Law equation themselves, and cancel. Therefore: 
$$\nabla\times\vec D=-\mu_0\epsilon_0\frac{\partial\vec H}{\partial t}$$
With the integral form:
$$\oint_C\vec D\cdot d\vec l=-\mu_0\epsilon_0\frac{\partial}{\partial t}\int_S\vec H\cdot d\vec A$$
**The identity discussed above are not part of the canon. Please contact a supervisor for possibility of new insight.** 
**Update: This appears to be wrong at first glance, because it produces wave equations that have solutions that only propagate at the speed of light. Further argument about the non-physicality of phase velocity contained in the article [[Electromagnetic Waves]] should be examined before discarding it.**
## The Magnetic Gauss Law
Just like the magnetic field, the induction field has no direct source. 
$$\nabla\cdot\vec H=0$$
## Summary
##### Integral Forms
$$\boxed{\oint_S\vec D\cdot d\vec A=Q_{free}}$$
$$\boxed{\oint_S\vec H\cdot d\vec A=0}$$
$$\boxed{\oint_C\vec D\cdot d\vec l=-\mu_0\epsilon_0\frac{\partial}{\partial t}\int_S\vec H\cdot d\vec A}$$
$$\boxed{\oint_C\vec H\cdot d\vec l=I_{free}+\frac{\partial}{\partial t}\int_S\vec D\cdot d\vec A}$$
##### Differential / Local Forms
$$\boxed{\nabla\cdot\vec D=\rho_{free}}$$
$$\boxed{\nabla\cdot\vec H=0}$$
$$\boxed{\nabla\times\vec D=-\mu_0\epsilon_0\frac{\partial\vec H}{\partial t}}$$
$$\boxed{\nabla\times\vec H=\vec J_{free}+\frac{\partial\vec D}{\partial t}}$$
