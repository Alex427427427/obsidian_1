Tags: [[Relativity]] [[5 How Tensors Transform]]
___
## Derivative
The derivative operator $\frac{\partial}{\partial X^\mu}$ is a tensor. When acting on a scalar field, it returns the gradient. Is it contravariant or covariant? 

Consider a transformation of $X^\prime=\Lambda X$. What happens to the derivative in the new coordinates?
$$\frac{\partial}{\partial X^{\prime}}=\frac{\partial}{\partial X}\frac{\partial X}{\partial X^\prime}=\frac{\partial}{\partial X} \Lambda^T$$
In other words, the derivative operator transforms like a **covector**. It is covariant and has lower indices. From now on, the derivative operator will be written as:
$$\boxed{\partial_\mu:=\frac{\partial}{\partial X^\mu}}$$
The contravariant version of the operator can be obtained with the raising metric tensor ([[4 The Metric Tensor]]): 
$$\partial ^\mu=\partial _\nu\tilde\eta^{\nu\mu}$$
## Divergence
Divergence is the contraction of the derivative. It acts on a vector field $J$, and looks like:
$$\boxed{\partial_\mu J^\mu}$$
## Curl
Curl is defined using the **Levi-Civita tensor** $\epsilon$, also called the alternating tensor, which captures cyclic permutations and is useful for calculating rotation related properties. 

The full definition of the Levi-Civita tensor is:
$$\epsilon^{ijk\dots}=\begin{cases}
+1&(i,j,k,\dots)=even\ permutation\ of\ (0,1,2,3,\dots)\\
-1&(i,j,k,\dots)=odd\ permutation\ of\ (0,1,2,3,\dots)\\
0&otherwise
\end{cases}$$
And curl in 3D space is:
$$\boxed{(\nabla\times\vec F)^i=\epsilon^{ijk}\partial_j F_k}$$
## Laplacian
The Laplacian is the contraction of the derivative operator with itself. 
$$\boxed{\partial_\mu \partial^\mu}$$
