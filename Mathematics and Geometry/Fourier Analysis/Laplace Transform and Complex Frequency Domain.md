Category: [[Fourier Analysis]]
___
Related: [[Fourier Transform and Frequency Domain]] [[Z-Transform or Discrete Laplace Transform]]
___
A generalisation of Fourier Transforms [[Fourier Transform and Frequency Domain]] to the complex frequency (exponential enveloping oscillation) domain. 
## Forward Transform
$$\boxed{\mathcal L[f(t)](s)=\int_0^{\infty}f(t)e^{-st}dt:=F(s)}$$
Here $s$ is a complex number. Note that the transform only exists if the function doesn't grow faster than exponential. 
## Graph on the Complex Frequency Domain
The Laplace Transform results in a function over the complex plane. This is in fact the complex frequency domain. The function itself is complex valued at every location, but plots usually only plot the magnitude. The Fourier Transform can be recovered with a slice at the imaginary axis. 
## Inverse Transform
The Inverse Laplace Transform is slightly more cumbersome compared to the Inverse Fourier Transform, though the spirit of being symmetric to the forward Laplace Transform is still there. 
$$\boxed{\mathcal L^{-1}[F(s)](t)=\frac{1}{2\pi i}\lim_{T\rightarrow\infty}\int_{\gamma-iT}^{\gamma+iT}F(s)e^{st}ds=f(t)}$$
This corresponds to a line integral along a vertical line $Re(s)=\gamma$ where $\gamma$ is to the right of all singularities. Any $\gamma$ will result in the same original signal! This is telling us the nature of the complex frequency domain. Every vertical strip is a distribution of the complex exponentials of that strip that will combine to form the original signal. Often, we can simply pluck the poles from the complex plane and directly write down a linear combination of the complex harmonics associated with them. This reveals an interesting property of smooth functions on the complex plane - **any contour on the plane enclosing poles contain all information about those enclosed poles**! 

If all singularities are to the left of $Re(s)=0$, $\gamma$ can be chosen to be 0 and the Inverse Laplace Transform becomes the Inverse Fourier Transform. The extra factor of $i$ at the front of the formula can then be absorbed into the term $ds$ to return $d\omega$, where $s=i\omega$.
## Theorems
##### Parity
Similar reasoning as Fourier Transform. 

All even functions in time domain will be symmetric about the real axis in the complex frequency domain. All odd functions in time domain will be anti-symmetric about the real axis in the complex frequency domain. 
##### Linearity
Trivial by linearity of integration. 
##### Shifting Theorem
$$\boxed{\mathcal L[f(t-t_0)](s)=e^{-s t_0}F(s)}$$
$$\boxed{\mathcal L^{-1}[F(s-s_0)](t)=e^{s_0 t}f(t)}$$
Easy to see by arguments from Fourier Transform. 
##### Convolution
$$\boxed{\mathcal L[f*g](s)=F(s)\cdot G(s)}$$
Carries over from Fourier Transform. 
##### Differentiation
$$\boxed{\mathcal L\left[\frac{df}{dt}\right](s)=sF(s)-f(0)}$$
Proven via integration by parts from the laplace transform definition. This theorem can be repeatedly applied to reach higher order derivatives. 

In the other direction:
$$\boxed{\mathcal L\left[\frac{dF}{ds}\right](t)=-tf(t)}$$
Which is a generalisation of the Fourier Transform version of the theorem. 
##### Integration
$$\boxed{\mathcal L\left[\int_0^tf(\tau)d\tau\right](s)=\frac{1}{s}F(s)}$$
Follows from the differentiation theorem. 
##### Initial Value 
$$\boxed{\lim_{s\rightarrow\infty}sF(s)=f(0)}$$
Can be derived from the derivative rule. 

The infinite edge of the laplace domain contains information about the initial value of the system. 
##### Final Value
$$\boxed{\lim_{s\rightarrow 0}sF(s)=f(\infty)}$$
The origin of the laplace transform contains information about the steady state value of the system. If there is a pole there, we know that the system is unbounded. If there is a root there, we know the system decays to inactivity. 
##### Time Scaling
$$\boxed{\mathcal L[f(at)](s)=\frac{1}{|a|}F(\frac{s}{a})}$$
Comes from the similarity theorem of Fourier Transforms. 
## Common Identities
The simplest identity is:
$$\mathcal L[\delta(t)](s)=1$$
Then, by integration:
$$\mathcal L[H(t)](s)=\mathcal L[1](s)=\frac{1}{s}$$
Note that all functions is equivalent when multiplied by the Heaviside step function under the Laplace Transform. 

By the integration theorem, all polynomials:
$$\mathcal L[t](s)=\frac{1}{s^2}$$
$$\mathcal L[t^n](s)=\frac{1}{s^{n+1}}$$
Then, arguably the most important one: 
$$\mathcal L[e^{s_0t}](s)=\frac{1}{s-s_0}$$
Which, along with the aid of partial fractions, help solve most common inverse laplace transforms. This is not a surprise, because all systems could be constructed with complex exponentials. This also defines the cosine and sine functions as special cases: 
$$\mathcal L[\sin(\omega t)](s)=\frac{1}{2i(s-i\omega)}-\frac{1}{2i(s+i\omega)}=\frac{2i\omega}{2i(s^2+\omega^2)}=\frac{\omega}{s^2+\omega^2}$$
$$\mathcal L[\cos(\omega t)](s)=\frac{1}{2(s-i\omega)}+\frac{1}{2(s+i\omega)}=\frac{2s}{2(s^2+\omega^2)}=\frac{s}{s^2+\omega^2}$$
Finally, by the differentiation theorem, polynomials of s result in the various derivatives of the delta function: 
$$\mathcal L[\delta^\prime(t)](s)=s$$
## Differential Equations
Aside from decomposing signals into complex exponentials, the Laplace Transform can be applied to differential equations - ones that are linear on the various derivatives and orders of the function to which the differential equation is applied. 

Such differential equations in time become **polynomials** of $s$ multiplied by the function. 

The best way to understand this section is with an example.
##### Example
Consider a mass-spring-damper system with mass $m$, damping constant $b$, spring elasticity $k$, and the quantity of interest for this system is the displacement of the spring $y$. Obviously, with no external force, the system is: 
$$m\ddot y(t)=-ky(t)-b\dot y(t)$$
$$m\ddot y(t)+b\dot y(t)+ky(t)=0$$
This is the **homogeneous** differential equation - the response of the system under no external influence. 

Now, it is clear that the right hand side of the first equation collects the total force on the spring. We can add an external force term $u$, that may change over time, with which we can **control** and influence the system. 
$$m\ddot y(t)+b\dot y(t)+ky(t)=u(t)$$
Do the Laplace Transform: 
$$(ms^2+bs+k)Y(s)=U(s)$$
$$Y(s)=\boxed{\frac{1}{ms^2+bs+k}}U(s)$$
The boxed term is the **transfer function** of the system. It is that which, when multiplied to the control function (in this example, an external force), gives the system's response. 

**Since it is always possible to use partial fractions to split the transfer function of above form into linear combination of first order terms in s, We know that all such systems have complex exponential responses as the building block of the total response.**
##### Poles
Observe the identity:
$$\mathcal L[e^{s_0t}](s)=\frac{1}{s-s_0}$$
Since this function diverges at $s=s_0$ on the complex frequency domain, there is a **pole** at that location. 

Poles allow us to predict the time domain response of systems by inspection - the complex exponentials that make up its response. Each pole corresponds to one complex exponential component in the total response. If all poles lie on the left half of the plane, we know the complex exponential decays and the system is stable. 
##### Zeroes
Zeroes are any terms of $s$ that appear on the numerator side of the transfer function. what they represent is best understood using the integration theorem and considering the differential equation example above. The presence of zeroes represent integral components of the system parameter $y$ in its response. While it is hard to find examples in physics, we can find it appear in the integral term of PID control. 
##### Impulse Response
If the system is fed a unit impulse $\delta(t)$, the transfer function is multiplied by $1$. Then the system's actual response will be identical to the Inverse Laplace Transform of the transfer function itself. This fact allows estimation of a system's transfer function in practice. 
##### Step Response
If the system is fed a step control, the transfer function is multiplied by $1/s$. There is an additional pole at the origin in the complex frequency domain. Do partial fraction and find out what the system's response will look like. 
##### Causal Systems
Often we restrict our focus to systems that are causal. The formal definition is a system whose impulse response is 0 before the time at which the impulse is applied. 