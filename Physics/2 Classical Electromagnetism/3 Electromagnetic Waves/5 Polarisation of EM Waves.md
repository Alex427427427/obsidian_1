Tags: [[Electromagnetism]] [[Electromagnetic Waves]] [[2 Electromagnetic Waves]]
___
Polarisation of electromagnetic waves is the field behaviour over time at a location-fixed transverse plane to propagation. 

Electromagnetic waves can be polarised - given a direction of propagation and a fixture of overall initial phase, there remains **3** degrees of freedom of orientation for the electric field over time. 
1. The degree of orientation along an orthogonal direction to propagation.
2. The degree of orientation along a second orthogonal direction to propagation.
3. The degree of relative phase difference between those first two fields. This results in a cyclic orientation sweeping around the orthogonal plane to propagation, with differing eccentricity. 
This can be effectively captured with the mathematics of Jones vectors. 

For the remaining discussion, assume a plane wave propagating in the z direction. 
## Jones Vectors
2 degrees of complex freedom is enough to encompass the aforementioned 3 degrees of freedom. In fact, it gives us 4. Let the basis states of the wave be an oscillation in x and y respectively. 
$$\begin{pmatrix}1\\0\end{pmatrix}:=\hat x\cos(kz-\omega t)\ \ \ \ \ \ \ and\ \ \ \ \ \ \ \begin{pmatrix}0\\1\end{pmatrix}:=\hat y\cos(kz-\omega t)$$
In general: 
$$\boxed{\begin{pmatrix}xe^{i\theta_1}\\0\end{pmatrix}:=\vec x\cos(kz-\omega t+\theta_1)}\ \ \ \ \ \ \ and\ \ \ \ \ \ \ \boxed{\begin{pmatrix}0\\ye^{i\theta_2}\end{pmatrix}:=\vec y\cos(kz-\omega t+\theta_2)}$$
This gives us 4 degrees of freedom, but only the phase difference between the two basis states is observable (at optical frequencies). So to uniquely describe an observable polarisation state, we can fix the first basis state to have a phase of 0, while the second basis state's phase is in fact the relative phase between the two. So, in general, for real valued $x, y$ and $\theta$:
$$\boxed{\begin{pmatrix}x\\ ye^{i\theta}\end{pmatrix}:=\vec x\cos(kz-\omega t)+\vec y\cos(kz-\omega t+\theta)}$$
And all overall phase shifts of the state are said to be equivalent due to returning the same observables. 
##### Change of Basis - Diagonal States
The diagonal polarisations - where two equal magnitude linear polarisation states in sync are added - form a complete basis for the space of polarisations. 
**Diagonal:** 
$$\boxed{\frac{1}{\sqrt2}\begin{pmatrix}1\\ 1\end{pmatrix}:=\frac{1}{\sqrt2}\hat x\cos(kz-\omega t)+\frac{1}{\sqrt2}\hat y\cos(kz-\omega t)}$$
**Anti-Diagonal:** 
$$\boxed{\frac{1}{\sqrt2}\begin{pmatrix}1\\ -1\end{pmatrix}:=\frac{1}{\sqrt2}\hat x\cos(kz-\omega t)-\frac{1}{\sqrt2}\hat y\cos(kz-\omega t)}$$
Where we have applied appropriate scaling to ensure unit amplitude. 
##### Change of Basis - Circular States
The circular polarisations - where two equal magnitude linear polarisation states are offsetted by a quarter wavelength i.e. phase offset by $90\degree$ - also form a complete basis for the space of polarisations. 
**Right hand:** (at a fixed plane as the wave passes through, left hand spatial helicity)
$$\boxed{\frac{1}{\sqrt2}\begin{pmatrix}1\\ i\end{pmatrix}:=\frac{1}{\sqrt2}\hat x\cos(kz-\omega t)-\frac{1}{\sqrt2}\hat y\sin(kz-\omega t)}$$
**Left hand:** (at a fixed plane as the wave passes through, right hand spatial helicity)
$$\boxed{\frac{1}{\sqrt2}\begin{pmatrix}1\\ -i\end{pmatrix}:=\frac{1}{\sqrt2}\hat x\cos(kz-\omega t)+\frac{1}{\sqrt2}\hat y\sin(kz-\omega t)}$$
In quantum mechanics, it will become apparent that these circular polarisation states are the true basis for photon states. 
## Appearance
![[polarisation states.png]]
Above diagram describes the appearance of polarisation states. In the diagram, $\psi$ is the angle made on the orthogonal plane to propagation, by the magnitudes $x,y$. $\delta$ is the phase offset between the two linear degrees of polarisation. We see how the phase shift alters eccentricity. The sign of the phase offset results in which direction the field is rotating over the ellipse. This is its helicity. Light gray marks the polarisation when phase offset is none. 
## How each polarisation state is produced
To create linearly polarised light (phase offset 0), have a conductive grating that is only free to conduct along the direction of the gratings. This absorbs all energy in that direction, leaving only the orthogonal direction to pass through. 
![Sale > polarising filters > in stock](https://thecuriousastronomer.files.wordpress.com/2014/07/4.jpg)
Note that the slit shown is **NOT** what physical filters will look like. The slits in the diagram represent the orientation that will be let through, while slits in actual filters are orthogonal to that orientation. 

To create elliptically polarised light, pass a linearly polarised light through a medium where light polarised along different directions experience different infinitesimal phase changes. After passing through an appropriate length of the material, light will emerge on the other side where each linear polarisation component has been phase shifted to just the right phase difference. 
![[circular polarising plate.png]]
## Jones Matrices
Polarising media can be thought of as matrices acting on the Jones vector states. Deriving the form of those matrices is trivial. 