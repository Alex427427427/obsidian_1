Tags: [[Quantum Mechanics]] [[1 The Quantum State]] [[2 Matrix Mechanics]]
___
Paul Dirac introduced an elegant notation he called the "braket" notation, which we have in fact been using intermittently until now. 
## States - Kets
States are called "kets", and written as $$\ket\Psi$$ (If you're familiar with tensors, states are contravariant ([[5 How Tensors Transform]]), motivating their component representation as column vectors. )
## Dual of States - Bras
The dual of the state is called a "bra", and is written like $\bra\Psi$ in braket notation. i.e. 
$$\ket\Psi^\dagger=\bra\Psi$$(If you are familiar with tensors, bras are covariant ([[5 How Tensors Transform]]), motivating their component representation as row vectors). 
## Inner Products
Inner products, placing the bras to the left of kets, look like an angled bracket:
$$\braket{\Psi_1|\Psi_2}$$
The squared magnitude of a state is then:
$$|\Psi|^2=\braket{\Psi|\Psi}$$
## Operators
Remembering that unit vectors are (unfortunately) written with a hat, operators are also written with a hat: $$\hat A$$
They act on states $\ket\Psi$ by $\hat A\ket\Psi$, and state duals $\bra\Psi$ by $\bra\Psi\hat A^\dagger$.

Its matrix elements are found using the previously discussed ([[2 Matrix Mechanics]]) formula:
$$A_{ij}=\braket{\Psi_i|\hat A|\Psi_j}$$
where $\ket\Psi_i$ and $\ket\Psi_j$ are the $i$th and $j$th basis states. Altogether the matrix $A$ looks like:
$$A=\begin{pmatrix} \braket{\Psi_1|\hat A|\Psi_1}&\braket{\Psi_1|\hat A|\Psi_2}&\dots\\
\braket{\Psi_2|\hat A|\Psi_1}&\braket{\Psi_2|\hat A|\Psi_2}&\dots\\
\vdots&\vdots&\ddots
\end{pmatrix}$$
## Outer Products
In dirac notation, outer product looks like:
$$\ket{\Psi_1}\bra{\Psi_2}$$
