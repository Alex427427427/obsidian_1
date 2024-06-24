Tags: [[Classical Mechanics]] [[Newtonian Mechanics]] [[1 Review of Newton - Single Particle Mechanics]]
___
## Total Force
The second law gives us how force affects motion. We turn our attention briefly to the source of the force in a multi-particle system. First we look at all possible forces acting on one particle in the system:
$$\vec F_i=\sum_{j\neq i}\vec F_{ij}+\vec F_{ext\ on\ i}$$
Where the summation term are the internal forces on the $i$th particle. The forces experienced by all particles in the system are: 
$$\sum_i\vec F_i=\sum_i\left(\sum_{j\neq i}\vec F_{ij}+\vec F_{ext\ on\ i}\right)=\sum_{i<j}(\vec F_{ij}+\vec F_{ji})+\vec F_{ext}=\vec F_{ext}$$
Where we have used newton's third law to cancel reciprocating forces. We see that the total force experienced by a system is equivalent to the forces that come from sources external to the system. 
## Center of Mass, Macroscopic Newton's Second Law
The total mass is:
$$M=\sum_i m_i$$
The center of mass is the first moment (weighted sum): 
$$\vec R=\frac{\sum_i m_i\vec r_i}{M}$$
The newton's second law then becomes: 
$$\vec F_{ext}=\sum_i\vec F_i=\sum_i\dot{\vec p_i}=\sum_im_i\ddot{\vec r_i}=M\frac{\sum_im_i\ddot{\vec r_i}}{M}=M\ddot{\vec R}$$
This is an important result. The center of mass of a system of particles acts as if all the mass is concentrated there. It is this law that makes classical physics so powerful. Doesn't matter if you throw a tennis ball or a cat, the center of mass traces the same path. It is thanks to the smoothing out of smaller scale phenomena, that humanity is able to conquer the monumental task of understanding the natural world. 
## Momenta
Momentum and angular momentum are the same
$$\vec P=\sum_i\vec p_i=\sum_im_i\dot{\vec r_i}=M\frac{\sum_im_i\dot{\vec r_i}}{M}=M\dot{\vec R}\ \ \ \ \ \ \ and\ \ \ \ \ \ \ \vec L=\vec r\times\vec P$$
The angular momentum second law has a subtlety:
$$\dot{\vec L}=\sum_i\vec r_i\times\dot{\vec p_i}=\sum_i\vec r_i\times\vec F_i=\sum_i\vec r_i\times\left(\sum_{j\neq i}\vec F_{ij}+\vec F_{ext\ on\ i}\right)
$$
$$=\sum_{i<j}(\vec r_i\times\vec F_{ij}+\vec r_j\times\vec F_{ji})+\vec r_i\times\vec F_{ext}=\sum_{i<j}(\vec r_i-\vec r_j)\times\vec F_{ij}+\vec\tau_{ext}$$
The **strong form** of Newton's 3rd law is that the equal and opposite forces act in line to the dispacement vector between 2 bodies. Thus the cross product vanishes, and the second law form is preserved: 
$$\dot{\vec L}=\vec \tau_{ext}$$
Lorentz forces do not follow the strong form of Newton's 3rd law, but fields themselves carry the momenta to conserve them. [[9 Magnetic Forces and Fields, Lorentz Force]] [[7 Momentum and Angular Momentum of the EM Field]]
## Energy
##### Kinetic Energy
To turn the multi-particle kinetic energy into a more illuminating form, we break the location of a particle to the vector pointing to the center of mass added by the particle's location relative to the center of mass, $\tilde r_i$:
$$T=\frac{1}{2}\sum_im_i\dot{\vec r_i}^2=\frac{1}{2}\sum_im_i\dot{(\vec R+\tilde r_i)}^2$$
$$=\frac{1}{2}\sum_im_i(\dot{\vec R}\cdot\dot{\vec R}+2\dot{\vec R}\cdot\dot{\tilde r_i}+\dot{\tilde r_i}\cdot\dot{\tilde r_i})=\frac{1}{2}\sum_im_i\dot{\vec R}^2+\sum_im_i\dot{\vec R}\cdot\dot{\tilde r_i}+\frac{1}{2}\sum_im_i\dot{\tilde r_i}^2$$
The second term contains the time rate of change of the weighted sum of all particle displacements relative to the center of mass, which by definition of the center of mass, remains 0. Thus: 
$$T=\frac{1}{2}\sum_im_i\dot{\vec R}^2+\frac{1}{2}\sum_im_i\dot{\tilde r_i}^2$$
Where the first term is energy due to the linear motion of the object's center of mass, and the second term is the internal kinetic energy describing how the particles are moving around the center of mass. 
##### Potential Energy and Conservation
$$T(t_2)-T(t_1)=\sum_i\int_{\vec r_{i1}}^{\vec r_{i2}}\left(\vec F_{ext\ on\ i}+\sum_{j\neq i}\vec F_{ij}\right)\cdot d\vec r_i$$
$$=\sum_i\int_{\vec r_{i1}}^{\vec r_{i2}}\vec F_{ext\ on\ i}\cdot d\vec r_i+\sum_{i<j}\int\vec F_{ij}\cdot d(\vec r_i-\vec r_j)$$
Let $\vec F_{ext\ on\ i}=-\nabla_i V_i$ where $\nabla_i=\frac{\partial}{\partial\vec r_i}$ and $V_i$ is the external potential that particle $i$ experiences. Let $\vec F_{ij}=-\nabla_i V_{ij}$ where $V_{ij}$ is the internal potential that particle $j$ exerts on particle $i$. In order for newton's 3rd law to hold ($\vec F_{ij}=-\vec F_{ji}$ and $\vec F_{ij}\parallel (\vec r_i-\vec r_j)$) then the potentials must satisfy $V_{ij}=V_{ji}$ and that they are only functions on the relative distance between the two particles. Thus: 
$$V=\sum_iV_i+\sum_{i<j}V_{ij}$$
Substitution into the energy change yields:
$$T(t_1)+V(t_1)=T(t_2)+V(t_2)=E$$
##### Example
Gravity between 2 particles. $T=\frac{1}{2}m_1\dot{\vec r_1}^2+\frac{1}{2}m_2\dot{\vec r_2}^2$ and $V=-\frac{Gm_1m_2}{|\vec r_1-\vec r_2|}$
This system has total linear momentum and angular momentum and energy conserved. 