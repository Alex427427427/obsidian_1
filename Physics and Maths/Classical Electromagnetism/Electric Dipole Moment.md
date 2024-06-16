Tags: [[Electromagnetism]] [[Magnetic Dipole Moment]]
___
## The Electric Dipole
The simplest **electric dipole** is a **net-zero charge** system that has **equal and opposite charges separated by a distance** sitting on what we call its two opposing poles. Other configurations that give rise to the same far field pattern will be discussed later. 
## Electric Fields on Electric Dipoles
##### Uniform Field
The dipole experiences **no net force** in a **uniform** electric field $\vec E$, but a torque $\tau$. 
$$\boxed{\vec \tau=\vec p \times\vec E}$$
where $\vec p$ is what we would like to define as the dipole moment. To derive it, let's consider a picture of the dipole in a field:
![[Electric Dipole in Electric Field.png|500]]
1. Since we want the directions in the torque equation to work out, we need $\vec p$ to point from the negative charge to the positive charge. Let's prepare for this by defining $\vec d$ to be the vector pointing from the negative charge to the positive charge. This is the **displacement vector**.
2. Now examine the torque strength. Take the negative charge as the pivot (which we are free to do), the force on the negative charge is no longer relevant. The torque is then $q|\vec E||\vec d| \sin{\theta}=q\vec d \times \vec E$.
Therefore the electric dipole moment is:
$$\boxed{\vec p = q\vec d}$$
##### Non-Uniform Field
When there is a field gradient, the dipole no longer experiences net-zero force. Consider the same image as above, but this time the field gets stronger the further we go to the right. Let right be the positive $x$ direction. The net force that the dipole experiences then becomes:
$$\vec F_x=\vec F_+-\vec F_-$$
Where $\vec F_+$ and $\vec F_-$ are the forces acting on the positive and negative poles respectively. Then:
$$\vec F_x=q|\vec E_x(x_+)|-q|\vec E_x(x_-)|$$
where $x_+$ and $x_-$ are the $x$ locations of the positive and negative poles respectively. Putting the displacement vector in:
$$\vec F_x=q|\vec E_x(x_-+|\vec d|\cos{\theta})|-q|\vec E_x(x_-)|$$
$$=q|\vec d|\cos{\theta}\frac{|\vec E_x(x_-+|\vec d|\cos{\theta})|-|\vec E_x(x_-)|}{|\vec d|\cos{\theta}}$$
$$=|\vec p|\cos{\theta}\frac{|\vec E_x(x_-+|\vec d|\cos{\theta})|-|\vec E_x(x_-)|}{|\vec d|\cos{\theta}}$$
Now let's consider the infinitesimal local limit of the same dipole moment. In this idealisation, the poles are so close to each other that they may as well exist at the same location. So the force becomes:
$$\vec F_x=\lim_{|\vec d|\rightarrow0}|\vec p|\cos{\theta}\frac{|\vec E_x(x_-+|\vec d|\cos{\theta})|-|\vec E_x(x_-)|}{|\vec d|\cos{\theta}}$$
The term $=\lim_{|\vec d|\rightarrow0}\frac{|\vec E_x(x_-+|\vec d|\cos{\theta})|-|\vec E_x(x_-)|}{|\vec d|\cos{\theta}}$ is the definition of the field strength gradient in first principles. Thus:
$$\vec F_x=|\vec p|\cos{\theta}\left|\frac{\partial \vec E_x}{\partial x}\right|=\vec p_x\frac{\partial\vec E_x}{\partial x}$$
Generalising to 3D:
$$\vec F=\begin{pmatrix}
\vec p_x\frac{\partial\vec E_x}{\partial x}
&\vec p_y\frac{\partial\vec E_y}{\partial y}
&\vec p_z\frac{\partial\vec E_z}{\partial z}
\end{pmatrix}
=\nabla
\left(
\vec p_x\vec E_x
+\vec p_y\vec E_y
+\vec p_z\vec E_z
\right)
=
\nabla(\vec p\cdot\vec E)
$$
Therefore, 
$$\boxed{\vec F=
\nabla(\vec p\cdot\vec E)}$$
**This happens all the while the torque makes the dipole oscillate back and forth, if the dipole is free to move**. 
##### The Interaction Energy between the field and the dipole
It is now useful to define the potential energy $U$ of the interaction between the field and the dipole, from which the force can be found with a simple negative gradient operation.
$$\vec F=
\nabla(\vec p\cdot\vec E)=-\nabla(-\vec p\cdot\vec E)=-\nabla U$$
$$\boxed{\therefore U=-\vec p\cdot\vec E}$$
Notice that this matches the behaviour even when there is a uniform field - the dipole prefers to align with the electric field for a lower energy state. Without internal drag, the dipole would oscillate indefinitely about the alignment direction. Notice that the energy encodes enough information to describe both the torque and force behaviour of the dipole. 
## Alternative Dipole Configurations

![[Different Dipole Configurations.png]]
Top left is the idealised infinitesimal dipole. Top right is the standard dipole arrangement, and the one typically found in matter. Bottom left is a polarised disc. Bottom right is a capacitor. Notice that for all four configurations, the field far away from the source looks the same. This is the dipole field pattern. 