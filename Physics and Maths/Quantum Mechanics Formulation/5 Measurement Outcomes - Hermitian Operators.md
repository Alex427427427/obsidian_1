Tags: [[Quantum Mechanics]] [[1 The Quantum State]] [[2 Matrix Mechanics]] [[4 Measurement Event, the Projection and Identity Operator]]
___
As introduced in [[1 The Quantum State]]:
1. Every measurable property of the system is characterised by a linear operator $\hat A$ - a matrix. When measured, the quantum state of the system probabilistically snaps into one of the **eigenvectors** of $\hat A$, called **eigenstates**. The **eigenvalue** is the value of the measured property. 
2. The probability of $\ket \Psi$ becoming each eigenstate is distributed according to the square magnitude of the projection of $\ket\Psi$ onto every eigenstate. 
Let's describe how this plays out in practice. 

## The Measurement Result Operator 
The operator $\hat A$ associated with a measurement encodes the possible results of the measurement for every eigenstate. Assuming it is expressed in its eigenbasis, it will be a diagonal matrix $A$, with the eigenvalues on the diagonal, each being the result of the measurement on the corresponding eigenstate: 
$$A=\begin{pmatrix}
a_1 & 0 & 0 & \dots\\
0 & a_2 & 0 & \dots\\
0 & 0 & a_3 & \dots\\
\vdots & \vdots & \vdots & \ddots\\
\end{pmatrix}$$
Each entry is as usual characterised by $A_{ij}=\braket{a_i|\hat A|a_j}$. The fact that the off-diagonal terms are 0 means that there is no dependence between different basis states, which means we are in the eigenbasis. In time, we will use this insight to recognise when we are not in the eigenbasis, and know to transform towards it accordingly. 

Beware that this operator's matrix form will appear different in a different base. 
## If the quantum state was already an eigenstate prior to measurement
If the quantum state is already in an eigenstate $\ket {a_i}$ of the measurement operator $\hat A$, it will remain the same state upon measurement with a probability of 1. The measurement operator $\hat A$ then gives the result of the measurement as the $i$th eigenvalue $a_i$:
$$\hat A\ket{a_i}=a_i\ket{a_i}$$
## If the quantum state was a general state prior to measurement
Then the quantum state is a linear superposition of the eigenstates. The object described by the quantum state will no longer produce a definite value upon measurement. Instead, it will probabilistically snap to one of the eigenstates according to [[The Born Rule]] and *then* produce the associated eigenvalue. 

Upon many repetitions of the same measurement on a large number of such objects with the same quantum state, a statistical result will emerge. It will be a distribution of eigenvalues, each with probability equal to the squared magnitude of the wavefunction's projection onto the eigenstate. 

The expected value - the average - of the measurement outcome, denoted $\braket \hat A$, is the sum of the probabilities times the outcome. This is valid so long as the eigenstates are orthogonal, which they are in quantum mechanics. 
$$\braket \hat A=\sum_i |\braket{a_i|\Psi}|^2 a_i$$
$$=\sum_i \braket{a_i|\Psi}^*\braket{a_i|\Psi}a_i$$
$$=\sum_i \braket{\Psi|a_i}\braket{a_i|\Psi}a_i$$
$$=\sum_i \braket{\Psi|a_i|a_i}\braket{a_i|\Psi}$$
$$=\sum_i \braket{\Psi|\hat A|a_i}\braket{a_i|\Psi}$$
$$=\braket{\Psi|\hat A\sum_i |a_i}\braket{a_i|\Psi}$$
$$=\bra{\Psi} \hat A\hat I \ket{\Psi}$$
$$=\bra\Psi\hat A\ket\Psi$$
So $\boxed{\braket{\hat A}=\bra\Psi\hat A\ket\Psi}$. This equation is valid in any base, and holds because the eigenstates are orthogonal. 
## Measurement Outcome Operators are Hermitian
Consider $\hat A$ as a transformation on $\ket\Psi$. Then the expected outcome is the inner product between the transformed $\ket{\Psi^\prime}=\hat A\ket\Psi$ and its original dual $\bra\Psi$.
$$\braket \hat A=\braket{\Psi|\Psi^\prime}$$
Since **measurement outcomes are real-valued**, the complex conjugate of the expected outcome must equal to itself. 
$$\braket \hat A^*
=\braket{\Psi|\Psi^\prime}^*
=\braket{\Psi|\Psi^\prime}^\dagger
=\braket{\Psi^\prime|\Psi}=\braket{\Psi|\hat A^\dagger|\Psi}
$$
In the final equality above we invoked our understanding of how state duals - covectors ([[1 What Tensors Are]]) - transform ([[5 How Tensors Transform]]). Alternatively, recognise algebraically $\bra{\Psi^\prime}=\ket{\Psi^\prime}^\dagger=(\hat A\ket\Psi)^\dagger=\ket\Psi^\dagger \hat A^\dagger=\bra\Psi\hat A^\dagger$.

So we have shown that:
$$\braket \hat A=\braket \hat A^*\implies
\bra\Psi\hat A\ket\Psi=
\braket{\Psi|\hat A^\dagger|\Psi}\implies 
\boxed{\hat A = \hat A^\dagger}$$
Which is the same as saying $\hat A$ is **Hermitian**. Keep these in mind: 
Through the development of our formalism, asserting that **eigenstates must be orthogonal**, along with the assertion that **measurement outcomes are real-valued**, we are forced to conclude that **operators associated with measurement outcomes - observables - are Hermitian**. 

Conversely, if we know an operator is Hermitian, then we know that it has orthogonal eigenstates, and real eigenvalues. The operator is associated with an observable. 



