Tags: [[1 The Quantum State]] [[Quantum Mechanics]]
___
The constructions stated in [[1 The Quantum State]] is neatly represented in linear algebra. The formulation of all quantum phenomena into linear algebra is matrix mechanics, developed by Werner Heisenberg, Max Born and a few others. 
## States
In a given basis, $\ket\Psi$ is written as a column vector 
$$\vec{\Psi}=\begin{pmatrix}c_1\\c_2\\\vdots\end{pmatrix}$$
where $c_i=\vec{e_i}\cdot\vec{\Psi}$, the projection of $\vec{\Psi}$ onto the $i$th basis vector $\vec{e}_i$. 
## Inner Products
Since the components of $\ket\Psi$ are complex, we use the complex inner product. For 2 complex numbers $v$ and $w$, the inner product is $v^*w$. The result is a complex number having a magnitude equal to the product of the operand magnitudes, and a phase equal to the phase difference between the operand phases. Therefore, for 2 vectors $\vec \Psi_1=\sum_i a_i\vec e_i$ and $\vec\Psi_2=\sum_i b_i\vec e_i$, the dot product is:
$${\vec\Psi_1}^\dagger\vec\Psi_2=\begin{pmatrix}a_1^*&a_2^*&\dots\end{pmatrix}\begin{pmatrix}b_1\\b_2\\\vdots\end{pmatrix}$$
Where ${\vec\Psi}^\dagger$ is the hermitian conjugate of $\vec\Psi$ - its complex conjugate transpose. 
## Dual of States
$\vec\Psi^\dagger$, the hermitian conjugate of $\vec\Psi$, is the covector ([[1 What Tensors Are]]) of $\vec\Psi$ and lives in its dual space. It is that object which we use in inner products - to measure a space, and endow it with a notion of length and angle.  
$$\vec{\Psi}^\dagger=\begin{pmatrix}c_1^*&c_2^*&\dots\end{pmatrix}$$
where $c_i=\vec{e_i}\cdot\vec{\Psi}$, the projection of $\vec{\Psi}$ onto the $i$th basis vector $\vec{e}_i$. 
## Operators
These objects linearly transform states and duals of states via matrix multiplication. Measurement, projection, spatial translation, time evolution, rotation, can all be written as matrices. An operator $\hat A$ is written as $A$ in matrix form.

The usual definition of matrix elements using basis vector inner products works here:
$$A_{ij}=\vec e_i^\dagger A\vec e_j$$
So that the operator looks like:
$$A=\begin{pmatrix}\vec e_1^\dagger A\vec e_1&\vec e_1^\dagger A\vec e_2&\dots\\
\vec e_2^\dagger A\vec e_1&\vec e_2^\dagger A\vec e_2&\dots\\
\vdots&\vdots&\ddots
\end{pmatrix}$$
This allows us to work out the details of an operator using knowledge of only the effects of the operator on the basis states. 
## Outer Products
If we take the inner product and swap the places of the state and the state dual, we get a matrix:
$$\vec\Psi_1{\vec\Psi_2}^\dagger=
\begin{pmatrix}a_1^*\\a_2*\\\vdots\end{pmatrix}
\begin{pmatrix}b_1&b_2&\dots\end{pmatrix}
=\begin{pmatrix}
a_1^*b_1&a_1^*b_2&\dots\\
a_2^*b_1&a_2^*b_2&\dots\\
\vdots&\vdots&\ddots\\
\end{pmatrix}
$$
We see that the outer product is an operator. 
## How Operators Transform States, State Duals, and other Operators
An operator $A$ transforms a state $\vec\Psi$ by matrix multiplication on the left:
$$\vec\Psi^\prime=A\vec\Psi$$
The same operator must transform a state dual $\vec\Psi^\dagger$ by right multiplication of the inverse operator:
$$\vec\Psi^{\dagger\prime}=\vec\Psi^\dagger A^\dagger$$
This is simply a result of [[5 How Tensors Transform]]. Alternatively, algebraically:
$$\vec\Psi^{\dagger\prime}=\left(\vec\Psi^{\prime}\right)^\dagger
=\left(A\vec\Psi\right)^\dagger
=\vec\Psi^\dagger A^\dagger$$
Following the rules of [[5 How Tensors Transform]], a measurement operator $O$ must be transformed as:
$$O^\prime=A^\dagger OA$$
Note that the placement of the conjugated $A$ is different to what would be expected from the note about tensors, because here $O$ represents a measurement - a rank (0,2) tensor. Note that a transformation operator $A$ is a rank (1,1) tensor. 