Tags: [[20 The Electric Field Holds Energy Density]] [[19 Energy is the Fluid Emerging from Charges]]
___
## Work Done to Assemble 2 Discrete Charges
Consider 2 charges $q_1$ and $q_2$. We wish to bring them together to form an arrangement where they have a distance of $r_{12}$ between them. The first charge just exists in space and need only to be pinned down. The second charge is brought close, and the energy required to do that is $V_1(r_{12})$ per unit charge of $q_2$. Thus:
$$W_2=q_2V_1(r_{12})=\frac{1}{4\pi\epsilon_0}\frac{q_1q_2}{r_{12}}$$
## Work Done to Assemble $n$ Discrete Charges
Now a third charge will need to fight against the combined potential of both $q_1$ and $q_2$. 
$$W_3=q_3V_1(r_{13})+q_3V_2(r_{23})=\frac{1}{4\pi\epsilon_0}\left(\frac{q_1q_3}{r_{13}}+\frac{q_2q_3}{r_{23}}\right)$$
The $i$th charge in the distribution will need (note $r_{ji}=r_{ij}$):
$$W_i=\frac{1}{4\pi\epsilon_0}\left(\frac{q_1q_i}{r_{1i}}+\frac{q_2q_i}{r_{2i}}+\dots\right)$$
Thus the total work done, summing over all pairs of charges exactly once, is:
$$W=\frac{1}{4\pi\epsilon_0}\sum_{j>i}\left(\frac{q_iq_j}{r_{ij}}\right)$$
To force that $j>i$ in the sum is to force we only count each pair once. We can alternatively count all of them twice, and divide the whole by 2:
$$W=\frac{1}{2}\frac{1}{4\pi\epsilon_0}\sum_{i=1,j\neq i}^n\left(\frac{q_iq_j}{r_{ij}}\right)=
\frac{1}{2}\frac{1}{4\pi\epsilon_0}\sum_{i=1}^nq_i\sum_{j\neq i}\left(\frac{q_j}{r_{ij}}\right)$$
Notice the terms forming the total potential $V$ experienced by $q_i$ at the location $\vec r_i$:
$$V(\vec r_i)=\frac{1}{4\pi\epsilon_0}\sum_{j\neq i}\frac{q_j}{r_{ij}}$$
Thus:
$$\boxed{W=\frac{1}{2}\sum_{i=1}^nq_iV(\vec r_i)}$$
## Work Done to Assemble Continuous Charge Distribution
$$\boxed{W=\frac{1}{2}\int \rho Vd\tau}$$
Where $d\tau$ is an infinitesimal volume element. Notice that $V$ no longer needs the caveat that it needs to exclude the potential generated by the charge at the location experiencing it, because now there is no charge at any infinitesimally small region. 

We will now derive the previously obtained energy density in the electric field, from [[20 The Electric Field Holds Energy Density]].
$$W=\frac{\epsilon_0}{2}\int (\nabla\cdot\vec E) Vd\tau$$
Invoking the vector calculus version of the product rule: 
$$\nabla\cdot(\phi\vec F)=\phi\nabla\cdot\vec F+\vec F\cdot\nabla \phi$$
when combined with the divergence theorem, leads to the vector calculus integration by parts: 
$$\int\nabla\cdot(\phi\vec F)d\tau=\int \phi\nabla\cdot\vec Fd\tau+\int \vec F\cdot\nabla \phi d\tau=\oint \phi\vec F\cdot d\vec A$$
$$\int \phi\nabla\cdot\vec Fd\tau=\oint \phi\vec F\cdot d\vec A-\int \vec F\cdot\nabla \phi d\tau$$
Note that the surface integral is at the boundary of the volume over which the original integral was meant to take. 

Thus: 
$$W=\frac{\epsilon_0}{2}\left(\oint V\vec E\cdot d\vec A-\int \vec E\cdot\nabla V d\tau\right)=\frac{\epsilon_0}{2}\left(\oint V\vec E\cdot d\vec A+\int \vec E\cdot\vec E d\tau\right)$$
The above integral was meant to be taken over the volume in which there is charge distribution, but since there are no charges outside the distribution, should hold at any volume. In fact, why not take the integral over all space? The volume term grows while the surface term decreases, until the volume integral over all space holds the answer. 
$$\boxed{W=\frac{\epsilon_0}{2}\int|\vec E|^2d\tau}$$
Which tells us the energy density: 
$$u=\frac{\epsilon_0}{2}|\vec E|^2$$
## Interpretation
We see that both the charge distribution integral and the energy density integral produce the total energy stored in the charge distribution, so is the energy stored in the charge embedded in potentials, or is the energy stored in the field? 

This is unanswerable for now, but in general relativity, we must treat the energy being stored in the field. 