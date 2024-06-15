Tags: [[Tensors]]
___
The Metric tensor has two simple interpretations that basically mean the same thing.
##### 1 - They define inner products
To calculate the inner product between $X^\mu$ and $Y^\mu$, simply sandwich the metric tensor between them. 
$$X\cdot Y=X^\mu \eta_{\mu\nu}Y^\nu$$
Now the indices match, and after the contractions of $\mu$ and $\nu$, results in a scalar. 
The metric tensor, by defining an inner product, assigns a notion of distance and angle on the space. It defines the geometry of the space.

The simplest example of the metric tensor is the Identity, in euclidean space:
$$\eta=\begin{bmatrix}1&0&0\\0&1&0\\0&0&1\end{bmatrix}$$
Which defines the standard euclidean inner product. 

Another example is the Minkowski metric tensor, which defines how distances are measured over spacetime:
$$\eta=diag(+1,-1,-1,-1)=\begin{bmatrix}1&0&0&0\\0&-1&0&0\\0&0&-1&0\\0&0&0&-1\end{bmatrix}$$
Which results in the inner product ${X^0}^2-{X^1}^2-{X^2}^2-{X^3}^2$.
##### 2 - They convert a vector into its dual space object (so that it can later used in an inner product)
The metric tensor converts a vector into a co-vector, which can also be seen as an index lowering operation. We can define 
$$X_\mu=X^\nu\eta_{\nu\mu}$$
and use it in the inner product with $Y$. The inner product then looks exactly like a contraction:
$$X_\mu Y^\mu$$
