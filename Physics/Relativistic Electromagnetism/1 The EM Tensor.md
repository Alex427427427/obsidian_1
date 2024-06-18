Tags: [[Tensors]] [[Electromagnetism]] [[Relativity]] 
This series uses the [[1 Gaussian Units]] system
___
The study of electromagnetism is about charges and their motion. Through experiments, humanity constructed the mathematical entities $\vec E$ (the Electric field) and $\vec B$ (the Magnetic field) to describe forces that change the motion of charged objects, called the Lorentz force law:
$$\vec F=q\left(\vec E+\frac{1}{c}\vec v\times\vec B\right)$$
This law will soon be replaced by a simpler equation of motion, when we understand the effects of $\vec E$ and $\vec B$ on a charged object through spacetime. $\vec E$ and $\vec B$ shall be united into the Electromagnetic field strength tensor. 
## The EM Field Strength Tensor
The electromagnetic field strength tensor is a rotation [[Generator]] field emanating from current sources (how this field is created by current sources is the subject of the next note), experienced by other sources. It exists at every location in spacetime. It is antisymmetric, expected of an infinitesimal rotation tensor. Expressed in Gaussian units where the magnetic field is scaled up by a factor of $c$:
$$F^{\mu\nu}=\begin{bmatrix}
0 & -E_x & -E_y & -E_z \\
E_x & 0 & -B_z & B_y \\
E_y & B_z & 0 & -B_x \\
E_z & -B_y & B_x & 0 
\end{bmatrix}$$
What does this rotation generator field rotate? The 4-velocity ([[3 Relativistic Motion]]) of charged objects. The equation of motion is simply the lie algebraic equation for infinitesimal rotation:
$$\left(\frac{dU}{dt}\right)_\mu=\frac{q}{m}F_{\mu\nu}U^\nu$$
While the term $\frac{qF}{m}$ is the rotation generator, the term $qFU$ is also clearly a force. So the tensor may also be understood as a **function** that maps velocities to forces. 
#### Degrees of Freedom
Notice that there are 6 degrees of freedom in the EM tensor, which matches that of a general rotation in 4D. Later we will see that the Electric and Magnetic fields are further constrained such that there are only 4 true degrees of freedom. 
## The Role of $\vec E$ and $\vec B$
Thanks to the Minkowski metric ([[1 Measuring Spacetime]]), the types of rotation that $\vec E$ is responsible for is different to those of $\vec B$. 

The elements in the field tensor belonging to $\vec E$ are responsible for rotations in the plane formed by the time axis and the spatial direction of $\vec E$. This is a hyperbolic rotation away or towards the time axis, which looks like acceleration through space.

The elements in the field tensor belonging to $\vec B$ are responsible for regular rotations within space, in the plane orthogonal to $\vec B$. 