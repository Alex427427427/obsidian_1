Tags: [[Tensors]]
___
Upper indices enumerate a contravariant object $X^\mu$, while lower indices numerate a covariant object $X_\mu$. A combination of upper and lower indices enumerate a higher rank tensor ${T^\mu}_\nu$. The number of indices of a tensor is its **rank**. A tensor with $a$ contravariant indices and $b$ covariant indices has a rank of $(a,b)$.

A typical tensor equation in index form looks like:
$$X^{\prime\mu}=\sum_\nu {\Lambda^\mu}_\nu X^\nu$$
In the index notation, **the order of the terms doesn't matter**. The order only needs to be enforced when you wish to write out the equation using the rules of matrix multiplication without refering to the indices: 
$$X^\prime=\Lambda X$$

When converting to matrix notation, the ordering of the indices of one element does matter. ${\Lambda^\mu}_\nu$ and ${\Lambda_\nu}^\mu$ enumerate $\Lambda$ and $\Lambda^T$ respectively.