Tags: [[Tensors]]
___
The most ubiquitous example of a tensor is the stress tensor. 
## The Stress Tensor Field in Solid Material
The stress tensor $\sigma$ is a force function field at every location in a solid material. For an infinitesimal element, the stress tensor shows what stress (force per unit area) is exerted at every direction on the element. The stress tensor is a function that takes in a directional unit vector, and returns the stress vector. 
$$\sigma=\begin{bmatrix}
\sigma_{xx}&\sigma_{xy}&\sigma_{xz}\\
\sigma_{yx}&\sigma_{yy}&\sigma_{yz}\\
\sigma_{zx}&\sigma_{zy}&\sigma_{zz}
\end{bmatrix}$$
The stress vector applied in the direction $\hat r$ (i.e. the face orthogonal to $\hat r$):
$$\vec{\sigma}(\hat r)=\sigma \hat{r}$$
The interpretation of each element in the tensor:
$${\sigma^{i}}_{j}=\vec{e}_i^T\sigma\vec{e}_j$$
which is the $i$th component of the stress applied on the $j$th direction (the surface orthogonal to the $j$th basis vector).

If a non-unit vector is passed into the stress tensor, the vector's magnitude is the area of the orthogonal surface associated with the vector. The mapping would then return the total force exerted on the area. 
## The Stress Tensor is Symmetric
The diagonal elements $\sigma_{ii}$ are the axial stresses, while the off-diagonal elements $\sigma_{ij},i\neq j$ are the shear stresses. If the material is in stasis, all forces and moments must cancel. Axial stresses already represent symmetric opposing forces. The off-diagonal elements must match in such a way for net moment to be 0. This means the stress tensor is **symmetric**. 
## All Stress Tensors are Compressive/Expansive
Despite appearances that the stress tensor encodes shear stress, it is always possible to perform a coordinate transform into the eigenvector directions of the stress tensor, where the off-diagonal elements become 0. Along these principal directions, the stress tensor only applies axial stresses. If we were to visualise the stresses over a small ball centered at the location of interest, they would form an ellipsoid. These are the principal axes. 