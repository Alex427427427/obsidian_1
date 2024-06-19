Tags: [[Electromagnetism]] [[Electromagnetic Waves]] [[9 Macroscopic Maxwell Equations]] [[18 Maxwell Potential Equations in The Lorentz Gauge]] [[14 Maxwell Equation - Faraday's Law of Induction]] [[13 Maxwell Equation - Ampere's Law for Magnetic Field Creation]]
___
## Potential Form
The potential form equations in lorentz gauge are automatically wave equations in the source free regions of space. 
$$\boxed{\left(\mu_0\epsilon_0\frac{\partial^2}{\partial t^2}-\nabla^2\right)\phi=0}$$
$$\boxed{\left(\mu_0\epsilon_0\frac{\partial^2}{\partial t^2}-\nabla^2\right)\vec A=0}$$
## Usual Form
Take the curl of both curl equations:
$$\nabla\times\nabla\times\vec E=-\frac{\partial}{\partial t}\nabla\times\vec B$$
$$\nabla\times\nabla\times\vec B=\mu_0\epsilon_0\frac{\partial}{\partial t}\nabla\times\vec E$$
Substitute the sourceless field curls into the RHS equations, and convert the LHS using vector calculus identities:
$$\nabla(\nabla\cdot\vec E)-\nabla^2\vec E=-\mu_0\epsilon_0\frac{\partial \vec E}{\partial t}$$
$$\nabla(\nabla\cdot\vec B)-\nabla^2\vec B=-\mu_0\epsilon_0\frac{\partial \vec B}{\partial t}$$
In the source free region, the electric field is divergenless. The magnetic field is always divergenless. Thus: 
$$\boxed{\nabla^2\vec E=\mu_0\epsilon_0\frac{\partial \vec E}{\partial t}}$$
$$\boxed{\nabla^2\vec B=\mu_0\epsilon_0\frac{\partial\vec B}{\partial t}}$$
Which are wave equations. 
## Macroscopic Form
The same procedure as above returns
$$\boxed{\nabla^2\vec D=\mu_0\epsilon_0\frac{\partial \vec D}{\partial t}}$$
$$\boxed{\nabla^2\vec H=\mu_0\epsilon_0\frac{\partial\vec H}{\partial t}}$$
## Speed of Electromagnetic Waves is the Speed of Light
The form of the wave equation suggests that:
$$\boxed{\mu_0\epsilon_0=\frac{1}{c^2}}$$
Where $c$ is the speed of the wave. It turns out to be the speed of light. 