Tags: [[Unit Systems]] [[Electromagnetism]] 
___
## History
The **SI (standard international) system** has 4 base units: length(m), time(s), mass(kg), current(A). All mechanical measurements can be expressed with a combination of these 4.

The unit for current is actually unnecessary. When experimentalists first observed two current carrying wires exerting a force on each other, they decided to define a unit to quantify current. The Ampere is the amount of current that produces $2\times 10^{-7} N$ of force per unit length, when the current carrying wires are spaced 1m apart. The charge unit Coulomb was then defined using As.

### Consequences on the Electric field
Such a definition of unit charge results in a proportionality constant between the charge density and the divergence of the electric field, which is $\epsilon_0$ - the permittivity of free space, in the Maxwell equation:
$$\nabla\cdot\vec{E}=\frac{\rho}{\epsilon_0}$$
The electric force magnitude between 2 charges becomes: 
$$F=k\frac{q_1 q_2}{r^2}$$
where $k=\frac{1}{4\pi \epsilon_0}$, so
$$F=\frac{1}{4\pi \epsilon_0}\frac{q_1 q_2}{r^2}$$
and the electric field near a charge becomes
$$\vec{E}=\frac{1}{4\pi\epsilon_0}\frac{q}{|\vec{r}|^2}\hat{r}$$
### Consequences on the Magnetic field
The definition of unit current also results in a proportionality constant between the current density and the curl of the magnetic field, which is $\mu_0$ - the permeability of free space, in the Maxwell equation: 
$$\nabla\times\vec{B}=\mu_0\vec{J}$$
The magnetic field near a current carrying wire then becomes:
$$\vec{B}=\frac{\mu_0}{4\pi}\int  \frac{Id\vec{l}\times \hat{r}}{|\vec{r}|^2}$$
___
## Gaussian Units Definition
The **Gaussian system** has 3 base units: length(cm), time(s), mass(g). All mechanical measurements will b expressed with a combination of these 3. 

Charge is defined such that $k = 1$ in the electric force law:
$$\boxed{F=\frac{q_1q_2}{r^2}}$$
Which means that 1 unit of charge - statCoulomb - is the amount of charge that results in a force of 1 g cm $s^{-2}$ (one "dyne"), when separated by 1cm. The unit of current is statCoulomb / sec, passing through some plane. 

### Consequences
#### Factors of $4\pi$ and $\epsilon_0$
In any unit system, the laws of electromagnetism will have a factor of $4\pi$ somewhere, whether in the Maxwell equations or the force laws. The SI system has it appear in the force laws and absent in the Maxwell equations. The Gaussian system has the factor of $4\pi$ appear in the Maxwell equations and absent in the force laws. Let's understand why this happens. 

Consider the force law. The factor disappears from the force law, meaning it must have been absorbed into the charges. **The charge unit has changed in such a way that $\epsilon_0$ is $\frac{1}{4\pi}$**. How was this done? Since the charge unit is squared in the force law, the charge quantities must have obtained a factor of $\frac{1}{\sqrt{4\pi\epsilon_0}}$ each. **The same physical amount of charge, will appear smaller in Gaussian unit by a factor of $\sqrt{4\pi\epsilon_0}$**. 

Now consider the field strength law. The charge absorbs a factor of $\frac{1}{\sqrt{4\pi\epsilon_0}}$, leaving behind a factor of $\frac{1}{\sqrt{4\pi\epsilon_0}}$. Moving this to the left hand side, we see that the field strength must absorb a factor of $\sqrt{4\pi\epsilon_0}$. **The same physical field will have a value in the Gaussian system that is larger than what would have been in the SI system, by a factor of $\sqrt{4\pi\epsilon_0}$.

#### Applying to the force laws
The Electric force law in SI unit, when involving the electric field, is:
$$\vec{F}=q_{SI}\vec{E}_{SI}$$
Substitute the SI system E being $\sqrt{4\pi\epsilon_0}$ smaller than the Gaussian system E, and the SI system charge being $\sqrt{4\pi\epsilon_0}$ larger than the Gaussian system charge, we get:
$$\vec{F}=\sqrt{4\pi\epsilon_0}\cdot q_G\cdot\frac{1}{\sqrt{4\pi\epsilon_0}}\vec{E}_G$$
$$\therefore\vec{F}=q_G\vec{E}_G$$
We see that the force law is unchanged. 

Now consider the magnetic force law:
$$\vec{F}=q_{SI}\cdot\vec{v}\times\vec{B}_{SI}$$
In order for the force law to be invariant, the magnetic field strength must also pick up a factor of $\frac{1}{\sqrt{4\pi\epsilon_0}}$ like the electric field strength. Additionally, we shall perform another unit shift. We will redefine the magnetic field strength such that it has the same dimensions as the electric field. This is done in a similar way to convert time coordinates into the same dimension as space coordinates: 
$$t^\prime=ct$$
similarly:
$$\vec{B}^\prime = c\vec{B}$$
So altogether:
$$\boxed{\vec{F}=q_G\left(\vec{E}_G+\frac{1}{c}\vec{v}\times\vec{B}_G\right)}$$
or
$$\boxed{\vec{F}=q_G\left(\vec{E}_G+\vec{\beta}\times\vec{B}_G\right)}$$
in Gaussian units.
#### Applying to the Maxwell Equations
**The Gauss Law for Electric field** in SI units is:
$$\nabla\cdot\vec{E}_{SI}=\frac{\rho_{SI}}{\epsilon_0}$$
Substitute the SI system E being $\sqrt{4\pi\epsilon_0}$ smaller than the Gaussian system E, and the SI system charge being $\sqrt{4\pi\epsilon_0}$ larger than the Gaussian system charge, we get:
$$\frac{1}{\sqrt{4\pi\epsilon_0}}\nabla\cdot\vec{E}_G=\sqrt{4\pi\epsilon_0}\frac{\rho_G}{\epsilon_0}$$
$$\boxed{\therefore\nabla\cdot\vec{E}_G=4\pi\rho_G}$$
The full **Ampere Law** in SI units is: 
$$\nabla\times\vec{B}_{SI}=\mu_0\left(\vec{J}_{SI}+\epsilon_0\frac{\partial\vec{E}}{\partial t}\right)$$
Substitute the SI system field strengths being $\sqrt{4\pi\epsilon_0}$ smaller than the Gaussian system field strengths, and the SI system sources being $\sqrt{4\pi\epsilon_0}$ larger than the Gaussian system sources, and that the SI magnetic field is a factor of c weaker than the Gaussian magnetic field, we get:
$$\frac{1}{\sqrt{4\pi\epsilon_0}}\nabla\times\frac{1}{c}\vec{B}_{G}=\mu_0\left(\sqrt{4\pi\epsilon_0}\vec{J}_{G}+\epsilon_0 \frac{1}{\sqrt{4\pi\epsilon_0}}\frac{\partial \vec{E}_G}{\partial t}\right)$$
$$\frac{1}{c}\nabla\times\vec{B}_G=4\pi\mu_0\epsilon_0\vec{J}_G+\mu_0\epsilon_0\frac{\partial\vec{E}_G}{\partial t}$$
$$\frac{1}{c}\nabla\times\vec{B}_G=\frac{4\pi}{c^2}\vec{J}_G + \frac{1}{c^2}\frac{\partial\vec{E}_G}{\partial t}$$
$$\boxed{\therefore\nabla\times\vec{B}_G=\frac{4\pi}{c}\vec{J}_G + \frac{1}{c}\frac{\partial\vec{E}_G}{\partial t}}$$
The **Faraday Law** in SI units is:
$$\nabla\times\vec{E}_{SI}=-\frac{\partial\vec{B}_{SI}}{\partial t}$$
Both fields will cause a factor of $\frac{1}{\sqrt{4\pi\epsilon_0}}$ to appear in the Gaussian version of the equation, which cancel out. Additionally, the magnetic field will gain a factor of $\frac{1}{c}$. Therefore:
$$\boxed{\nabla\times\vec{E}_G=-\frac{1}{c}\frac{\partial\vec{B}_G}{\partial t}}$$
The **Gauss' Law for magnetic field** remains unchanged:
$$\boxed{\nabla\cdot\vec{B}_G=0}$$
# Rules to convert SI equation into Gaussian equation

From all the reasoning above, here is the procedure to convert an SI equation into the correct form in Gaussian units. 
1. Multiply all sources by $\sqrt{4\pi\epsilon_0}$
2. Divide all fields by $\sqrt{4\pi\epsilon_0}$
3. Further divide the magnetic field by c
4. Where there is free $\mu_0$, replace with $\frac{4\pi}{c^2}$
5. Where there is free $\epsilon_0$, replace with $\frac{1}{4\pi}$

# HL units

[[2 Heaviside-Lorentz Units]]
Use the same steps above except remove all factors of $4\pi$
