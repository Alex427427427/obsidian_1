Tags: [[Quantum Mechanics]]
___
## The Quantum State $\ket\Psi$
Through myriad experiments in the 20th century, we postulate that everything an observer could know about a quantum system is fully described by the quantum state $\ket\Psi$ of the system. Here are the characteristics of the quantum state:
1. $\ket\Psi$ is a vector
2. Every measurable property of the system is characterised by a linear operator $\hat A$ - a matrix. When measured, the quantum state of the system probabilistically snaps into one of the **eigenvectors** of $\hat A$, called **eigenstates**. The **eigenvalue** is the value of the measured property. 
3. The probability of $\ket \Psi$ becoming each eigenstate is distributed according to the square magnitude of the projection of $\ket\Psi$ onto every eigenstate. 
4. The eigenstates form an orthogonal basis for the space containing $\ket\Psi$. i.e. $\ket\Psi=\sum_i c_i\ket i$. 
5. All $\ket\Psi$s pointing in the same direction represent the same quantum state, because the projection amplitudes remain at the same ratio to one another. 
6. It is convenient to always rescale $\ket\Psi$ such that $|\ket\Psi|^2=1$. In that case, since $|\ket\Psi|^2=\sum_i |c_i|^2=1$, $|c_i|^2$ is directly the probability of observing the eigenstate $\ket i$. This is renormalisation. When renormalised, the eigenstates form an orthonormal - not just orthogonal - basis for the space containing $\ket\Psi$. 
7. Due to the double slit experiment, where the distribution of a uniform flux of quantum particles end up interfering after passing through two close slits, it is unavoidable that the quantum state contains not only a magnitude but also a phase. This is encoded in a complex number. **Quantum states have complex coefficients**. This could have alternatively been captured with 2 real degrees of freedom, but the complex number conveniently packages it into one variable. 
8. A quantum system with a quantum state can undergo an overall phase shift and not affect the outcome of any experiment. 
9. When not observed, the quantum state also evolves by linear operators. The linearity of the operators ensures that component states do not interact with one another as they evolve in a ghostly superposition.  These operators are unitary - inner product preserving. 

The quantum state properties summarise the essence of what we understand of quantum mechanics. 