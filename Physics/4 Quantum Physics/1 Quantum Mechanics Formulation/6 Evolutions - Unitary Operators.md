Tags: [[Quantum Mechanics]] [[1 The Quantum State]] [[2 Matrix Mechanics]] 
___
Related: [[0 Discrete Action Relationships]]
___
When left to its own, a quantum state is free to evolve undisturbed. This could be a spatial translation, a time evolution, a rotation, and more. 

While all operators associated with observables are Hermitian, it turns out that all operators associated with undisturbed evolution are Unitary. Here we will understand this fact. 
## When a quantum state evolves
Suppose a quantum state $\ket\Psi$ evolves, and at some later stage of the evolution, it is a new state $\ket{\Psi^\prime}=\hat U(\theta)\ket\Psi$, for some operator $\hat U$ that describes the evolution parameterised by $\theta$, which could stand for space, time, angle, and more. How will the state dual evolve? According to [[5 How Tensors Transform]], or alternatively by doing simple matrix algebra, we know that:
$$\ket{\Psi^\prime}=\hat U(\theta)\ket\Psi\implies
\bra{\Psi^\prime}=\bra\Psi\hat U(\theta)^\dagger$$
Now consider the inner product of the state and its own dual. This represents the squared length of the state. Should it ever change? No. The total probability of the state having some eigenvalue is 1, so its squared length should always be 1:
$$\braket{\Psi|\Psi}=\braket{\Psi^\prime|\Psi^\prime}=
\bra\Psi\hat U(\theta)^\dagger\hat U(\theta)\ket\Psi$$
$$\boxed{\therefore\hat U^\dagger\hat U=\hat I}$$
Which is the same as saying $\hat U$ is **Unitary**, with a **squared determinant of 1**, and that it is **length preserving**, and its **column vectors are orthonormal**, as are its row vectors, and thus it is **like a rotation** (through configuration space). 