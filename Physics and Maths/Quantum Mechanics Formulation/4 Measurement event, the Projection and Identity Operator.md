Tags: [[1 The Quantum State]] [[2 Matrix Mechanics]] [[3 Dirac's Braket Notation]] [[Quantum Mechanics]]
___
## Projection 
As explained in [[1 The Quantum State]], a quantum system snaps into one of the eigenstates of the measurement operator for a property of interest. This snapping is best described with a projection, followed by renormalisation. The matter of renormalisation is simply finding the length of the new vector and dividing the new vector with it. The matter of projection is carried out with an operator:
$$\hat P_\hat {e_i}=\ket {\hat e_i}\bra {\hat e_i}$$
Let's observe what happens to a state $\ket\Psi$ when acted on by this operator:
$$\hat P_{\hat e_i}\ket\Psi=\ket {\hat e_i}\braket {\hat e_i|\Psi}=\braket {\hat e_i|\Psi}\ket {\hat e_i}$$
The inner product is the projection amplitude, while the whole term is the projection amplitude multiplied by the directional unit vector. 

Notice that **the outer product of a vector with itself is a projection operator** onto the direction of the vector. This originates from linear algebra and is not specific to dirac notation. 
## Collapse of the Quantum State
A measurement event causes the most frustratingly opaque phenomenon on the quantum state - it probabilistically snaps onto an eigenstate of the measurement. In other words, the smeared out superposition of the quantum states collapses into one definitive state. The superposition itself is not perplexing, and superpositions may be eigenstates from the point of view of other measurements. The strange part is the snap. This is the quantum state collapse:
$$\ket\Psi\rightarrow\begin{cases}
\ket{a_1}&with\ probability\ |\braket{a_1|\Psi}|^2\\
\ket{a_2}&with\ probability\ |\braket{a_2|\Psi}|^2\\
\vdots
\end{cases}$$
where $\ket {a_i}$ is the $i$th eigenstate of the operator associated with the measurement operator $\hat A$. This is [[The Born Rule]]. 

In current understanding, this collapse of the quantum state happens instantaneously, leading to severe non-locality down the line when we consider [[Entanglement]]. Furthermore, in current understanding, there appears to be no inner mechanism behind the collapse, and provably so, by [[Bell's Theorem]] experiments. In future notes, we will come to understand extremely well how a quantum system evolves, and yet have no idea of why or how the collapse happens. It is also difficult to define and pinpoint what constitutes a measurement event, that would cause the collapse. This is [[The Measurement Problem]]. For Alex, to remember your [[Speculation]], see [[Non-Local Realism]]. 
## Identity 
With the projection defined, it is useful to define the identity operator $\hat I$. It is simply the sum of the projection operators along every dimension of the quantum state space. The identity operator makes the linear combination of basis states to form the quantum state, explicit. 
$$\hat I=\sum_i \ket {\hat e_i}\bra {\hat e_i}$$
