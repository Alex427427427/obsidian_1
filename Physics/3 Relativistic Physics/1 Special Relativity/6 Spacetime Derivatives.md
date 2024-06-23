Tags: [[Tensors]] [[6 Tensor Calculus]] [[Relativity]]
___
## Derivative
The spacetime derivative:
$$\partial_\mu=\frac{\partial}{\partial X^\mu}=\left(\frac{\partial}{\partial(ct)},\frac{\partial}{\partial x},\frac{\partial}{\partial y},\frac{\partial}{\partial z}\right)=\left(\frac{1}{c}\frac{\partial}{\partial t},\frac{\partial}{\partial x},\frac{\partial}{\partial y},\frac{\partial}{\partial z}\right)$$
And its contravariant form:
$$\partial^\mu=\partial_\nu\tilde\eta^{\nu\mu}=\left(\frac{1}{c}\frac{\partial}{\partial t},-\frac{\partial}{\partial x},-\frac{\partial}{\partial y},-\frac{\partial}{\partial z}\right)^T$$

## Divergence
The spacetime divergence of a 4-vector field $J$:
$$\partial_\mu J^\mu=\frac{1}{c}\frac{\partial J^0}{\partial t}+\frac{\partial J^x}{\partial x}+\frac{\partial J^y}{\partial y}+\frac{\partial J^z}{\partial z}$$
## Curl
In spacetime, curl is replaced by a more generalisable representation, as an antisymmetric rotation [[Generator]] tensor field $F$. For a 4-vector field $A$, it is:
$$F_{\mu\nu}=\partial_\mu A_\nu-\partial_\nu A_\mu$$
If you must extract a curl in 3D, use:
$$(\nabla\times\vec A)^i=\epsilon^{ijk}\partial_jA_k$$
## Laplacian
The spacetime laplacian, when expanded, is:
$$\partial_\mu\partial^\mu=\frac{1}{c^2}\frac{\partial^2}{\partial t^2}-\frac{\partial^2}{\partial x^2}-\frac{\partial^2}{\partial y^2}-\frac{\partial^2}{\partial z^2}=\frac{1}{c^2}\frac{\partial^2}{\partial t^2}-\nabla^2=\square^2$$
