Tags: [[10 Magnetic Dipole]] [[Electromagnetism]] [[8 Permeability and Magnetic Susceptibility]] [[1 Electric Polarisation and the Polarisation Field]]
___
Materials respond to magnetic fields. Usually this is an alignment of the internal dipoles of the material, leading to a stronger overall field. 
## Magnetisation Field
When all the magnetic moments align, there is a large overall magnetic moment. The small circulations of the current loops add up to form one giant circulation, with current $I$ around the surface of the material. 
$$\sum\vec m=IA\hat n$$
Like how the electric polarisation field is the electric dipole density, the magnetisation field $\vec M$ is the magnetic dipole density. Dividing the above by volume, we get:
$$M=\frac{I}{d}=nI$$
Where $\frac{I}{d}$ is the density of current along the sheet enveloping the material. This is equivalent to $NI/d$ in a muti-winding inductor configuration, i.e. $nI$ where $n=N/d$ is the winding density. 
## Paramagnetism
When a magnetic field envelops certain materials, the material itself produces a very weak magnetic field, in line with the external one, making the total magnetic field slightly larger. The material is weakly magnetised. When taken away the external field, the material does not retain the magnetisation. 

If a magnet is placed near a paramagnetic material, the material will magnetise weakly and become attracted to the magnet. 
#### Explanation
The material is full of microscopic magnetic dipoles, but oriented randomly. This happens when the atoms with magnetic dipole field are not tightly coupled. When the external field is applied, the dipoles align with the field after some drag, making the total field stronger. When the field is taken away, the dipoles return to random orientation. 
## Ferromagnetism
When a magnetic field envelops certain materials, the material produces a strong magnetic field, in line with the external one, making the total magnetic field much stronger. The material is strongly magnetised. When taken away the external field, the material retains the magnetisation. It takes an opposing field to reverse this effect, leading to hysteresis. **Iron** is the most ubiquitous example, giving the name "ferro" to ferromagnetism. 

When a magnet is placed near a ferromagnetic material, the material will magnetise strongly and be attracted to the magnet. 
##### Explanation
Not only are there microscopic magnetic dipoles, but they are also very strongly influenced by one another. They group together to form regions in the material that have the same dipole direction, called **magnetic domains**. When an external magnetic field is applied, these domains align with the field, creating a much stronger field. When the external field is taken away, the domains all force one another to maintain their orientation. Upon heating, the dipoles are given enough energy to reorient into random domains. Alternatively, a negative magnetic field must be applied to reverse the magnetisation
![[magnetic domain magnetisation.png]]
##### Hysteresis, Coercivity and Relentivity
The fact that the magnetisation is retained and doesn't follow a simple linear dependence is hysteresis. Depending on the point in the cycle, the same external field could correspond to two different magnetisations. Hysteresis can be represented on a graph. 
![[magnetic hysteresis.png]]
The horizontal axis is the magnetic induction field ([[6 Magnetic Induction Field]]) - equivalent to the external magnetic field strength, while the vertical axis is the magnetisation field. The vertical axis intercept is the **retentivity $M_R$**, which is how much magnetisation field will remain when the external field is turned off. The horizontal axis intercept is the **coercivity** $H_C$, which is how much magnetic induction field is required to erase the magnetisation. 
## Diamagnetism
When a magnetic field is applied to certain materials, the material creates a magnetic field that is anti-aligned with the applied field. 

When a magnet is placed near a diamagnetic material, the material will be weakly repelled. 
##### Explanation
This kind of material usually has no net magnetic moment even on the microscopic scale. Every orbitting electron is paired with another one orbitting in the opposite direction. In other words, magnetic moments come in opposite pairs on the microscopic scale. 
![[paired moment.png]]
Upon application of a magnetic field, the change causes the moment facing opposite the external field to get stronger due to Faraday's Law ([[14 Maxwell Equation - Faraday's Law of Induction]]), while the same law predicts that the moment facing along the external field will get weaker. This results in a net moment facing against the external field, leading to repulsion. 
![[altered paired moment.png]]
If materials aren't paramagnetic or ferromagnetic, they are diamagnetic. 