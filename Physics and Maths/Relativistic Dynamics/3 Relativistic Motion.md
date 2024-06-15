Tags: [[Special Relativity]]
___
## The New Notion of Time
Now that time has been absorbed into a spatial coordinate, it is no longer useful in the context of dynamics over spacetime. We need a new notion of time against which motion over spacetime can be measured. This is the **proper time $\tau$**. It is the time experienced by the moving frame whose motion we wish to quantify. 

Revisit the Lorentz transformation of the time coordinate:
$$ct^\prime=\gamma\left(ct-\beta x\right)$$
The $t^\prime$ is the time of the moving frame measured in the world frame. The $t$ is the time measured if the observer is in the moving frame, hence the proper time $\tau$. From this we see the relationship between the regular time and the proper time:
$$\frac{dt}{d\tau}=\gamma$$
## 4-Velocity
We can now define the rate of change of the spacetime coordinate 4-vector with respect to proper time. This is the 4-velocity, $U^\mu$, also called proper velocity. It is the answer to the question within the moving frame "how fast am I moving through space and time with respect to my own time passing?"
$$U=\frac{d}{d\tau} X=\frac{dt}{d\tau}\frac{d}{dt}X=\gamma(c, v_x, v_y, v_z)$$
Notice a few things:
1. When $\gamma=1$ i.e. there is no spatial motion, frames move through time at the speed of light. 
2. The proper velocity is simply the regular velocity multiplied by $\gamma$.
3. When $\gamma\rightarrow\infty$, as $v\rightarrow c$, the frame moves through space and time time infinitely fast. In this sense, light speed is really infinite. 
4. The length of the proper velocity is $\sqrt{U_\mu U^\mu} = \gamma\sqrt{c^2-v^2}=\frac{1}{\sqrt{1-\left(\frac{v}{c}\right)^2}}c\sqrt{1-\left(\frac{v}{c}\right)^2}=c$, where $v=\sqrt{v_x^2+v_y^2+v_z^2}$. This means that all objects regardless of any other properties, travel through spacetime with lightspeed. Acceleration through space is a [[hyperbolic rotation]] of this 4-velocity away from the time axis.  