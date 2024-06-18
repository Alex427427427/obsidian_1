Tags: [[Electromagnetism]] [[1-3 Electric Forces and Fields]]
___
## Work and Potential Energy
Suppose an electric field pushes a charge along a path and delivers energy to it. As per classical dynamics, the work $W$ done by a force along a path from $\vec r_1$ to $\vec r_2$ is:
$$W=\int_{r_1}^{r_2}\vec F\cdot d\vec r$$
which is the losing of potential energy $\Delta U$:
$$\Delta U=U(\vec r_2)-U(\vec r_1)=-\int_{\vec r_1}^{\vec r_2}\vec F\cdot d\vec r$$
For a charge in an external electric field:
$$\Delta U=-\int_{\vec r_1}^{\vec r_2}q\vec E\cdot d\vec r=-q\int_{\vec r_1}^{\vec r_2}\vec E\cdot d\vec r$$
The negative sign is telling us that as the field does more work, the charge loses potential energy. Let's set the zero potential reference to be when the charge is at $\infty$. 
$$\boxed{U(\vec r)=-q\int_{\vec r}^{\infty}\vec E\cdot d\vec r}$$
##  A Potential Field Agnostic to the Charge Experiencing It
Everything outside the charge term, we can collect to form $\Phi$, the electric potential. This potential is agnostic to the charges that experience it. The potential energy is realised by multiplying a charge to it. 
$$\boxed{\phi(\vec r)=-\int_{\vec r}^{\infty}\vec E\cdot d\vec r}$$
This is valid regardless for *any system* producing the electric field. The same system produces the amount of potential at locations around it, according to the equation above. 

Furthermore, we know the electric field is **conservative** i.e. irrotational i.e. the energy delivered is the same for the same endpoints of the journey regardless of the exact path. Putting in the zero reference we see that:
$$\phi(\infty)-\phi(\vec r)=-\int_{\vec r}^{\infty}\vec E\cdot d\vec r$$
$$\phi(\vec r_2)-\phi(\vec r_1)=\int_{\vec r_1}^{\vec r_2}(-\vec E)\cdot d\vec r$$
From the fundamental theorem of calculus, we know that the bracketed term must be the gradient of the potential function. Therefore:
$$\boxed{\vec E=-\nabla\phi}$$
## Potential Difference
In most systems, we don't care about the absolute potential. It is the relative potential change that matters regarding energy delivery. Therefore we define the **potential difference** we call **voltage**:
$$\boxed{V(\vec r_1,\vec r_2)=\phi(\vec r_2)-\phi(\vec r_1)}$$
Which has unit of energy per charge, or called Volts (V).
## Visualisation
The electric potential can be thought of as a hilly landscape. The height is the potential, like the gravitational potential. The field is the negative slope of the landscape. When charges travel down the hill, they lose the potential difference, and gain more kinetic energy. If the hill is dissipative, they may keep rolling down the hill and have a constant velocity. 