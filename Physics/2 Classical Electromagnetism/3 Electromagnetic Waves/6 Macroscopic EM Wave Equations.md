Tags: [[Electromagnetism]] [[Electromagnetic Waves]] [[7 Maxwell's Equations in Frequency Domain]] [[3 Energy Flow of the Electromagnetic Field]]
___
We have previously dealt with vacuum. Now we must turn our eye to media.

This material deals with linear (external electric fields produce polarisation field that has a linear relationship between input and output) isotropic (degree of polarisability is equal in all directions, such that external electric fields produce polarisation field along the same direction) material. 
## Derivation of the wave equation
First, under the isotropic assumption, we can convert the Faraday's law:
$$\nabla\times\vec E=-\mu\frac{\partial}{\partial t}\vec H$$
And with no current source, but in general partially conductive media, the magnetising field equation becomes:
$$\nabla\times \vec H=\sigma\vec E+\epsilon\frac{\partial\vec E}{\partial t}$$
In other words: 
$$\nabla\times\vec H=\left(\sigma+\epsilon\frac{\partial}{\partial t}\right)\vec E$$
Now take the curl of both equations. 
$$\nabla\times\nabla\times\vec E=-\mu\frac{\partial}{\partial t}\nabla\times\vec H$$
$$\nabla\times\nabla\times\vec H=\left(\sigma+\epsilon\frac{\partial}{\partial t}\right)\nabla\times\vec E$$
Substitute the original equations.
$$\nabla\times\nabla\times\vec E=-\mu\frac{\partial}{\partial t}\left(\sigma+\epsilon\frac{\partial}{\partial t}\right)\vec E$$
$$\nabla\times\nabla\times\vec H=-\left(\sigma+\epsilon\frac{\partial}{\partial t}\right)\mu\frac{\partial}{\partial t}\vec H$$
$$\boxed{\nabla^2\vec E=\mu\epsilon\frac{\partial \vec E}{\partial t}}$$
$$\boxed{\nabla^2\vec H=\mu\epsilon\frac{\partial\vec H}{\partial t}}$$
