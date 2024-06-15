Tags: [[Tensors]]
___
The study of tensors brings linear algebra to the height of its descriptive power over physical phenomena. 

A vector is a member of a vector space. In the context of physics, the word "vector" is restricted to those that transform contravariantly - those that represent an idea similar to physical objects. If the basis vectors shrink, the coordinates must grow, because the physical object remained the same - that is contravariance. A vector in this sense must be written as a column: 
$$V=\begin{bmatrix}v_1\\v_2\\\vdots\end{bmatrix}$$

A co-vector is a linear function on a vector, identical to a dot product with some vector (which shall be what we identify the linear function with), and lives in the dual space of the vector space it acts on. A co-vector is best visualised with **equipotential maps** over the vector space it acts on, and each component of the co-vector represents how many equipotentials the corresponding basis vector will pierce through. They transform covariantly, because when the basis vectors shrink, the new basis vectors will pierce through fewer equipotentials. Co-vectors are written as rows:
$$\tilde V=\begin{bmatrix}\tilde v_1&\tilde v_2&\dots\end{bmatrix}$$

Tensors are the most general linear objects/maps. They are made using tensor products on a collection of vectors and co-vectors, which are its building blocks. Suring a tensor product, a new array is formed, where the left operand's elements are distributed to the right operand repeatedly. Thus, tensors can be rows of rows or rows of columns or columns of columns or columns of rows and any higher combination. Similar to vector fields, there can also be tensor fields. 

Just like how covectors are functions on vectors and returns a scalar, a tensor is a general function that transforms its inputs - whether vectors or covectors or tensors - via a multiplication reminiscent of matrix multiplication. What it returns depends on what is fed into it, and what it expects to be fed into it. 

Below are some examples of various tensor constructions. 
$$T_{(2,0)}=U\otimes V=\begin{bmatrix}
u_1\begin{bmatrix}v_1\\ v_2\\\vdots\end{bmatrix}\\
u_2\begin{bmatrix}v_1\\ v_2\\\vdots\end{bmatrix}\\
\vdots
\end{bmatrix}$$
$$T_{(0,2)}=\tilde U\otimes \tilde V=\begin{bmatrix}
u_1\begin{bmatrix}v_1& v_2&\dots\end{bmatrix}&
u_2\begin{bmatrix}v_1& v_2&\dots\end{bmatrix}&
\dots
\end{bmatrix}$$
$$T_{(1,1)}=U\otimes \tilde V=\begin{bmatrix}
u_1\begin{bmatrix}v_1& v_2&\dots\end{bmatrix}\\
u_2\begin{bmatrix}v_1& v_2&\dots\end{bmatrix}\\
\vdots
\end{bmatrix}$$
$$T_{(1,1)}=\tilde U\otimes V=\begin{bmatrix}
u_1\begin{bmatrix}v_1\\ v_2\\\vdots\end{bmatrix}&
u_2\begin{bmatrix}v_1\\ v_2\\\vdots\end{bmatrix}&
\dots
\end{bmatrix}$$
The bracket subscript is the tensor's rank, which will be explained later. 

