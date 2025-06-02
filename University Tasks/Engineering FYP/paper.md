We consider a uniform linear array (ULA) consisting of N=8N = 8N=8 isotropic antenna elements arranged along the xxx-axis with half-wavelength spacing d=λ/2d = \lambda/2d=λ/2. Each element is equipped with a 4-bit digital phase shifter, allowing for 24=162^4 = 1624=16 discrete phase states uniformly distributed over the interval [0,2π)[0, 2\pi)[0,2π). The ideal phase shift resolution is thus Δϕ=2π16=π8\Delta\phi = \frac{2\pi}{16} = \frac{\pi}{8}Δϕ=162π​=8π​.

Let θ\thetaθ denote the angle of departure (or arrival) measured from broadside, and let the desired beam steering direction be θ0\theta_0θ0​. The ideal progressive phase shift across elements is given by:

ϕnideal=−kdnsin⁡θ0=−πnsin⁡θ0,n=0,1,…,N−1\phi_n^{\text{ideal}} = -k d n \sin\theta_0 = -\pi n \sin\theta_0, \quad n = 0, 1, \ldots, N-1ϕnideal​=−kdnsinθ0​=−πnsinθ0​,n=0,1,…,N−1

where k=2πλk = \frac{2\pi}{\lambda}k=λ2π​ is the wavenumber. The ideal array factor can be expressed as:

AFideal(θ)=∑n=0N−1wnej(ϕnideal+kdnsin⁡θ)AF_{\text{ideal}}(\theta) = \sum_{n=0}^{N-1} w_n e^{j(\phi_n^{\text{ideal}} + k d n \sin\theta)}AFideal​(θ)=n=0∑N−1​wn​ej(ϕnideal​+kdnsinθ)

where wnw_nwn​ is the complex excitation weight, assumed to be uniform and of unit magnitude for all elements (i.e., wn=1w_n = 1wn​=1).

### A. Phase Shifter Quantization and Fault Model

Each ideal phase ϕnideal\phi_n^{\text{ideal}}ϕnideal​ must be quantized to the nearest representable value given the 4-bit resolution. The set of quantized phase values is:

Q={0,π8,2π8,…,15π8}\mathcal{Q} = \left\{ 0, \frac{\pi}{8}, \frac{2\pi}{8}, \ldots, \frac{15\pi}{8} \right\}Q={0,8π​,82π​,…,815π​}

We represent each 4-bit phase setting as a binary word [b3 b2 b1 b0][b_3\, b_2\, b_1\, b_0][b3​b2​b1​b0​], with b3b_3b3​ as the most significant bit (MSB). The actual quantized phase applied to the nnn-th element is:

ϕn=2π16⋅∑i=03bi(n)⋅2i\phi_n = \frac{2\pi}{16} \cdot \sum_{i=0}^{3} b_i^{(n)} \cdot 2^iϕn​=162π​⋅i=0∑3​bi(n)​⋅2i

We consider two types of hardware faults in the digital phase shifters:

1. **MSB Failures**: In this common failure mode, one or more of the most significant bits (e.g., b3b_3b3​, b2b_2b2​) are stuck at either 0 or 1 due to diode malfunction. This constrains the phase shifter to a subset of possible output values.
    
2. **Random Bit Failures**: A more general fault model in which any subset of bits (not necessarily contiguous or most significant) may be stuck, and the failure pattern is randomly assigned across the array.
    

Given the fault state, each element nnn has a constrained set of achievable phase values:

Qnfaulty⊆Q\mathcal{Q}_n^{\text{faulty}} \subseteq \mathcal{Q}Qnfaulty​⊆Q

The beamforming task is then to select, for each element, the best achievable phase ϕn∈Qnfaulty\phi_n \in \mathcal{Q}_n^{\text{faulty}}ϕn​∈Qnfaulty​ that approximates ϕnideal\phi_n^{\text{ideal}}ϕnideal​, subject to the constraints imposed by the faulty bits.