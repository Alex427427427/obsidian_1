Tags: [[5 Maxwell Equation - Gauss' Law for Electric Field]] [[4 Electric Scalar Potential and Voltage]] [[1 Charges and Currents]] [[3 Electric Forces and Fields]] [[Electromagnetism]]
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
where $Q$ is the total charge displaced from the negative plate to the positive plate. Capacitance has the unit called **Farad** (F).
## Dynamical Properties of the Capacitor as an Electrical Spring
The above equation suggests a differential equation describing the electrical dynamics of the capacitor:
$$Q=CV\implies\frac{dQ}{dt}=C\frac{dV}{dt}\implies \boxed{I=C\frac{dV}{dt}}$$
Furthermore, when understanding electrical systems by their dynamical analogues in mechanical systems, we associate charge displacement $Q$ as displacement, current $I$ to be velocity, and voltage $V$ to be force. This means that the equation $V=\frac{1}{C}Q$ is the electrical analogue of $F=kx$ for ideal springs, with a spring constant of $k$. **The capacitor stores energy as potential energy like a spring**. This means the energy stored in the capacitor is:
$$U=\frac{1}{2C}Q^2=\boxed{\frac{1}{2}CV^2}$$
Analogous to $U=\frac{1}{2}kx^2=\frac{1}{2}\frac{1}{k}F^2$ for springs. 

Where exactly is all the energy stored? That will be later. See [[20 The Electric Field Holds Energy Density]]
## Capacitance in Terms of Capacitor Parameters
$C$ must be a function of the capacitor's properties, $A$ and $d$. To calculate $C$, we need the relationship between $Q$ and $V$, so let's first focus on those. 

Consider a cuboid Gaussian closed surface that envelops only the positive plate. All the electric flux is through the face in between the two plates, with the flux being $EA$, thanks to the uniformity of the electric field. [[5 Maxwell Equation - Gauss' Law for Electric Field]] $\oint_S \vec E\cdot d\vec A=\frac{Q}{\epsilon_0}$ tells us that this flux must be proportional to the charge enclosed. Thus
$$EA=\frac{Q}{\epsilon_0}\implies Q=\epsilon_0EA$$
Substituting into the capacitance equation yields the formula for capacitance in terms of the capacitor parameters:
$$C=\frac{\epsilon_0EA}{Ed}\implies \boxed{C=\frac{\epsilon_0A}{d}}$$
