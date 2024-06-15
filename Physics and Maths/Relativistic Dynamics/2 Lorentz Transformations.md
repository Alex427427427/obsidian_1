Tags: [[Special Relativity]] [[Tensors]] [[5 How Tensors Transform]]
___
## Lorentz Transformations
What kind of transformations preserve the metric tensor? Such transformations are Lorentz transformations, and correspond to switching between reference frames in spacetime. These transformations denoted $\Lambda$ are defined by: 
$$\Lambda^{-1} \eta \Lambda=\eta\ \ \ \ \ \ \ \ \ \ \ \ $$
Let's unpack this and find out what $\Lambda^{-1}$ must be. 
$${\left(\Lambda^{-1}\right)^\rho}_\mu\eta_{\rho\sigma}{\Lambda^\sigma}_\nu=\eta_{\mu\nu}={\Lambda_\mu}^\rho\eta_{\rho\sigma}{\Lambda^\sigma}_\nu={\left(\Lambda^T\right)^\rho}_\mu\eta_{\rho\sigma}{\Lambda^\sigma}_\nu$$
$$\boxed{\therefore\Lambda^{-1}=\Lambda^T}$$
This is a familiar identity and defines rotations in Minkowski spacetime. All Lorentz transformations can be composed from two classes of rotations, whose rotational planes intersect at right angle:
1. Rotation in space $$\begin{bmatrix}1&0&0&0\\0&R_{11}&R_{12}&R_{13}\\0&R_{21}&R_{22}&R_{23}\\0&R_{31}&R_{32}&R_{33}\\\end{bmatrix}$$
2. Lorentz boost - [[hyperbolic rotation]] away from the time axis - change of velocity through space: $$\begin{bmatrix}\gamma &-\beta&0&0\\-\beta &\gamma &0&0\\0&0&1&0\\0&0&0&1\\\end{bmatrix}$$ and other cyclic permutations of $x,y,z$.
	This matches the Lorentz transformation of changing into a frame moving at velocity v along an axis: $$ct^\prime=\gamma\left(ct-\beta x\right)\ \ \ \ \ \ \ \ \  
x^\prime = \gamma\left(x-\beta ct\right)\ \ \ \ \ \ \ \ \  
y^\prime=y\ \ \ \ \ \ \ \ \  
z^\prime=z$$where $\gamma=\frac{1}{\sqrt{1-\beta^2}}$, and $\beta = v/c$
	Lorentz boosts along an arbitrary direction can be calculated by first rotating so that the boosted direction aligns with an axis, performing the boost, then rotating back. 

### How various objects transform
#### 4-Vector
With the Lorentz transformation defined, we see how 4-vectors transform:
$$X^{\prime\mu}={\Lambda^{\mu}}_{\nu}X^\nu$$
For Lorentz boosts, this results in the tip of the $X$ vector tracing out a hyperbola. This preserves the volume of the **causal diamond** which is the intersection between the future light-cone of the origin and the past light-cone of $X$, meaning the totality of the events that can connect the origin to $X$ have a fixed volume.
#### co-vector
Now let's find out how co-vectors transform. Consider inserting an identity between the inner product between a co-vector and a vector:
$$X_\mu X^\mu=X_\nu\left(\Lambda^T \Lambda\right)X^\nu$$
Which should be the same as the inner product between the transformed co-vector and vector $X^\prime_\mu X^{\prime\mu}$, because it is Lorentz invariant. Note that whenever a general transformation is introduced, the index of objects being transformed ought to change to an arbitrary new index. 

Since $\Lambda X^\nu$ gives us $X^{\prime\mu}$, the remaining must give $X^\prime_\mu$:
$$X^\prime_\mu = {\left(\Lambda^T\right)^\nu}_\mu X_\nu ={\Lambda_\mu}^\nu X_\nu$$
#### Tensor
We see that a transformation needs to be applied per index, with the appropriate transposition depending whether the object being transformed has a co-vector or a vector for the immediate index of interest. Therefore, a tensor $F$ of rank $(2,0)$ ought to transform as:
$$
F^\prime=\Lambda F\Lambda^T
$$