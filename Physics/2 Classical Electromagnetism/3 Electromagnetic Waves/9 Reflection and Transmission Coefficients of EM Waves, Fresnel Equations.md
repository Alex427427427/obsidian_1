Category: [[Electromagnetism]] [[Electromagnetic Waves]]
___
Prerequisites: [[8 EM Field Interface Conditions at Media Boundary]] [[4 EM Waves in Media]]
___
Related: 
___
Note: All following derivations only care about the normal incidence component of the total wave, because the parallel travelling components to the interface do not have any non-trivial effects. Thus there will be cosines scaling all the field components. 
## History of Fresnel Equations
Augustin-Jean Fresnel was a French civil engineer and physicist whose research in optics led to the unanimous acceptance of the wave theory of light. He was the first to realise that light was a transverse wave, before the understanding of its electromagnetic origins. It was by him that polarisation of light was first understood, and he developed a set of equations describing how light would be reflected and transmitted. Now, we use the EM field interface conditions to derive these equations. 
## Plane of Incidence, S and P Polarisations
We must first understand incident light as decomposable into s and p polarisations, each with a different set of Fresnel equations. 

The S polarisation comes from the German work for perpendicular, and represents the polarisation in which the incident electric field is **perpendicular** to the **plane of incidence** - the plane formed by the incident, reflected and refracted ray. 

The P polarisation refers to the parallel component of the electric field to the plane of incidence. 
## The Equations
##### S Polarisation of Oblique Incidence
These can be derived using the optical boundary conditions derived in [[8 EM Field Interface Conditions at Media Boundary]]:
$$E_i+E_r=E_t$$
$$\frac{E_i}{\eta_1}\cos(\theta_1)-\frac{E_r}{\eta_1}\cos(\theta_1)=\frac{E_t}{\eta_2}\cos(\theta_2)$$
Note that for the S polarisation, the magnetising field needs cosine scaling to be reduced to the tangential component. 

Solving these two equations yields a relationship between the incident and reflected fields - the reflection coefficient: 
$$\boxed{\frac{E_r}{E_i}=\frac{\eta_2\cos(\theta_1)-\eta_1\cos(\theta_2)}{\eta_2\cos(\theta_1)+\eta_1\cos(\theta_2)}:=\Gamma_s:=r_s}$$
And the transmitted and incident fields - the transmission coefficient: 
$$\boxed{\frac{E_t}{E_i}=\frac{2\eta_2\cos(\theta_1)}{\eta_2\cos(\theta_1)+\eta_1\cos(\theta_2)}:=t_s}$$
##### P Polarisation of Oblique Incidence
These can be derived using the optical boundary conditions derived in [[8 EM Field Interface Conditions at Media Boundary]]:
$$E_i\cos(\theta_1)+E_r\cos(\theta_1)=E_t\cos(\theta_2)$$
$$\frac{E_i}{\eta_1}-\frac{E_r}{\eta_1}=\frac{E_t}{\eta_2}$$
Note that for the P polarisation, the electric field needs cosine scaling to be reduced to the tangential component. 

Solving these two equations yields a relationship between the incident and reflected fields: 
$$\boxed{\frac{E_r}{E_i}=\frac{\eta_2\cos(\theta_2)-\eta_1\cos(\theta_1)}{\eta_2\cos(\theta_2)+\eta_1\cos(\theta_1)}:=\Gamma_p:=r_p}$$
And the transmitted and incident fields: 
$$\boxed{\frac{E_t}{E_i}=\frac{2\eta_2\cos(\theta_1)}{\eta_2\cos(\theta_2)+\eta_1\cos(\theta_1)}:=t_p}$$
##### Special Case of Normal Incidence 
If you understand the general oblique case, you understand the special case. 
$$\boxed{\Gamma_n=\frac{\eta_2-\eta_1}{\eta_2+\eta_1}}$$
In this case, we can also consider what the reflection coefficient would look like in the other direction. It must be the negative. Thus there is an additional phase shift of half cycle. 
$$\boxed{\Gamma_{1\rightarrow2}=-\Gamma_{2\rightarrow1}}$$
##### The Total Coefficients 
Combining the coefficients is not trivial. It is in general best to start with the absolute electric field intensities. 

In the special case of unpolarised light - light whose polarisation rapidly changes, it can be assumed that power is evenly distributed in the s and p polarisations. Thus $R_{effective}=(R_s+R_p)/2$.
##### Reflectance $R$
The reflectance R is the ratio of reflected and incident power, which, by logic of [[6 Energy Flow of the EM Field]], is the square magnitude of the reflection coefficient. 
$$\boxed{R=|\Gamma|^2}$$
##### Transmittance T
The transmittance T is the ratio of transmitted and incident power, which by conservation of energy flow, must be: 
$$\boxed{T=1-R}$$
You may wrongly assume it is also the case that: 
$$T=|t|^2$$
But the transmitted power must be scaled appropriately according to the wave impedance of both materials which was not a concern in reflection. Furthermore, both wave components must be scaled to only look at the normal direction, which is the direction in which energy is being transported across the boundary. This results in: 
$$\boxed{T=\frac{\eta_1cos(\theta_2)}{\eta_2\cos(\theta_1)}|t|^2}$$
##### Replacing the impedances with refractive indices
You can see from the contents regarding wave impedances in [[4 EM Waves in Media]], that in non-conductive, non-magnetising media, the ratio of refractive indices is the **reciprocal** of the ratio of impedances. You may replace those parameters in the equations as you please. 