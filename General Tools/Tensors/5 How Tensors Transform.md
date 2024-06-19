Tags: [[Tensors]]
___
Suppose we are about to perform a coordinate transform on space. Coordinate transforms have a total rank of 2, specifically $(1,1)$. Let $\Lambda$ denote this transformation tensor. 
##### Vectors
A rank $(1,0)$ tensor $X^\mu$ transforms as:
$$X^{\prime\mu}= {\Lambda^\mu}_\nu X^\nu\implies X^\prime=\Lambda X$$
##### Covectors
A rank $(0,1)$ tensor $X_\mu$ transforms as:
$$X^\prime_\mu={\Lambda_\mu}^\nu X_\nu\implies X^\prime=X\Lambda^T$$
##### Tensors
A rank $(1,1)$ tensor ${F^\mu}_\nu$ transforms as:
$${F^{\prime\mu}}_\nu={\Lambda^\mu}_\rho{F^\rho}_\sigma{\Lambda^\sigma}_\nu\implies F^\prime=\Lambda F \Lambda$$
A rank (2,0) tensor $F^{\mu\nu}$ transforms as:
$$F^{\prime\mu\nu}={\Lambda^\mu}_\rho F^{\rho\sigma}{\Lambda_\sigma}^\nu\implies F^\prime=\Lambda F\Lambda^T$$
Note that whenever we introduce a new tensor multiplication, we must change the existing tensor indices to some free new indices, and match them accordingly. 