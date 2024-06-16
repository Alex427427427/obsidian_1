Tags: [[Electromagnetism]] [[Maxwell Equation 1 - Gauss' Law for Electricity]] [[Electric Polarisation Of Insulators]]
___
Two conductive plates each carrying an equal and opposite charge, separated by a distance $d$ that is far too small compared to the area of the plates $A$, results in a very neat electric field pattern that is most useful in probing the properties of the electric field and free space. The parallel plate configuration is a capacitor. 
![[Capacitor.png]]
Most of the field is concentrated in-between the plates, and at the limit of $\frac{A}{d}\rightarrow\infty$, all the field is situated there. At the limit, this field is uniform in strength and direction all throughout the cylinder of free space between the capacitors. 
## Voltage across the capacitor
Integrating the electric field over the distance between the plates gives the potential difference, which is the voltage across the capacitor. Thanks to the uniformity of the field:
$$V=Ed$$
where $E=|\vec E|$. 
## Charge Storage and Capacitance
The capacitor stores charge. If connected to an external voltage source across the capacitor, charge will flow from one plate to another until the total charge displacement results in a voltage equal to the voltage source. Since we know that the electric field strength is linearly proportional to charge, and the voltage is proportional to the electric field strength, then the voltage must be proportional to charge. This motivates us to define a parameter called capacitance, $C$, that characterises the charge storing capability of the capacitor:
$$\boxed{C=\frac{Q}{V}}$$
where $Q$ is the total charge displaced from the negative plate to the positive plate. 
## Dynamical Properties of the Capacitor as an Electrical Spring
The above equation suggests a differential equation describing the electrical dynamics of the capacitor:
$$Q=CV\implies\frac{dQ}{dt}=C\frac{dV}{dt}\implies \boxed{I=C\frac{dV}{dt}}$$
Furthermore, when understanding electrical systems by their dynamical analogues in mechanical systems, we associate charge displacement $Q$ as displacement, current $I$ to be velocity, and voltage $V$ to be force. This means that the equation $V=\frac{1}{C}Q$ is the electrical analogue of $F=kx$ for ideal springs, with a spring constant of $k$. This means the energy stored in the capacitor is:
$$\boxed{U=\frac{1}{2C}Q^2}$$
Analogous to $U=\frac{1}{2}kx^2$ for springs. 
## Capacitance in Terms of Capacitor Parameters
$C$ must be a function of the capacitor's properties, $A$ and $d$. To calculate $C$, we need the relationship between $Q$ and $V$, so let's first focus on those. 

Consider a cuboid Gaussian closed surface that envelops only the positive plate. All the electric flux is through the face in between the two plates, with the flux being $EA$, thanks to the uniformity of the electric field. [[Maxwell Equation 1 - Gauss' Law for Electricity]] $\oint_S \vec E\cdot d\vec A=\frac{Q}{\epsilon_0}$ tells us that this flux must be proportional to the charge enclosed. Thus
$$EA=\frac{Q}{\epsilon_0}\implies Q=\epsilon_0EA$$
Substituting into the capacitance equation yields the formula for capacitance in terms of the capacitor parameters:
$$C=\frac{\epsilon_0EA}{Ed}\implies \boxed{C=\frac{\epsilon_0A}{d}}$$
This suggests there are 2 ways to improve a capacitor by changing its shape: to make the plates larger, and to make them closer. However, a simple calculation will reveal that the two parameters need to be extreme for the capacitance to be of any useful value. Is there another way to improve the capacitance? 
## Improving the Capacitance with Polarisable Dielectric
Suppose we want to store even more charge for the same voltage applied. The only remaining property to tweak is $\epsilon_0$, the permittivity of free space. But this cannot be changed, because it is a property of space. Namely, it is **the amount of charge permissible behind/within a closed surface given a unit electric flux through the surface**. Locally, it is **the amount of equivalent charge density smeared out on the closed surface, permitted for every unit electric field at that location**. It is the quantity that associates a surface charge density and the electric field that will emanate from it. 

We can in fact change this parameter. We simply have to swap out empty space with some other medium, within which the same external charge will result in a lower electric field within the medium. This effectively **raises the permittivity**. 

The medium of interest is a polarisable material - a dielectric. They are what precisely accomplish the goal. They have a higher permittivity than free space. For every external charge applied to the plates, the resultant electric field inside the dielectric is weaker than in free space, due to the induced dipoles partially cancelling out the electric field from the external charge. Since the electric field is smaller for the same charge displacement, the voltage is also smaller. This means that more charge is required to bring the voltage up to match the applied voltage. Hence the capacitance is higher.

The new capacitance is:
$$\boxed{C=\frac{\epsilon A}{d}}$$
and $\epsilon>\epsilon_0$. 
