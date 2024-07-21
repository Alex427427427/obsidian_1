Category: [[Classical Mechanics]] [[Lagrangian Mechanics]]
___
Prerequisites: [[3 Lagrangian, Action, Principle of Stationary Action]]
___
Related: 
___
## Local Version of the Stationary Action Principle - Euler-Lagrange Equation
The principle of stationary action is not explicitly local. But we like to pretend the universe necessarily has to be local. Regardless, it happens to be the case that here, the principle of stationary action has an equivalent local form that mechanistically drives systems to follow the principle of stationary action globally. It is the Euler-Lagrange Equation. 
$$\boxed{\frac{\partial L}{\partial q^a}-\frac{d}{dt}\frac{\partial L}{\partial\dot q^a}=0}$$
Which becomes Newton's Second Law in the case of a single particle. 
## Proof
To prove the Euler Lagrange equation, we need to show that if the stationary action principle is true, the euler lagrange equation must be true. 

Consider varying a given path slightly, but we fix the end points. (because the stationary principle says that between any two configurations, a system will take the path of least action)
$$q^a(t)\rightarrow q^a(t)+\delta q^a(t)$$
$$\delta q^a(t_1)=\delta q^a(t_2)=0$$
Thus 
$$\delta S=\delta\int_{t_1}^{t_2}L\ dt$$
$$=\int_{t_1}^{t_2}\delta L\ dt$$
Apply the total partial derivative: 
$$=\int_{t_1}^{t_2}\frac{\partial L}{\partial q^a}\delta q^a+\frac{\partial L}{\partial \dot q^a}\delta \dot q^a\ dt$$
We can see what this becomes when we try to make the second term in the integral also have $\delta q^a$, by integrating that term by parts:
$$\int_{t_1}^{t_2}\frac{\partial L}{\partial\dot q^a}\delta \dot q^a\ dt=\left[\frac{\partial L}{\partial\dot q^a}\delta q^a\right]_{t_1}^{t_2}-\int_{t_1}^{t_2}\left(\frac{d}{dt}\frac{\partial L}{\partial\dot q^a}\right)\delta q^a\ dt$$
The square bracket term will be 0 because the path change is 0 at the start and end time of the path. Substituting the rest in, we get: 
$$\delta S=\int_{t_1}^{t_2}\left(\frac{\partial L}{\partial q^a}-\frac{d}{dt}\frac{\partial L}{\partial\dot q^a}\right)\delta q^a\ dt=0$$
But the path change is arbitrary. The only way to guarantee this integral to always be 0, is that the bracketed term is zero. Therein lies the proof for the Euler Lagrange equation. 