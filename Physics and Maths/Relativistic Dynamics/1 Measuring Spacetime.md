Tags: [[Special Relativity]] [[Tensors]] [[4 The Metric Tensor]] [[3 Einstein's Summation Notation]]
___
(This series uses the Einstein Summation Notation, where matching lower and upper indices are automatically summed - a contraction. )

## The Spacetime Coordinate
In order to speak of dynamics, spacetime ought to be measured. The 1 coordinate of time and 3 coordinates of space are put together to form a **4-vector** $(ct, x, y, z)$. The 4-vector is the location of an event or an object in spacetime. In order to measure time as a 4th dimension on near equal footing as space, its unit must be transformed to match that of space. This is done by multiplying it by $c$, the speed of light. The speed of light is the scaling ratio between space and time. So we have:
$$X^\mu=(ct, x, y, z)$$
## The Minkowski Metric Tensor
In order to have a notion of length in spacetime, we need a metric tensor - an object that encodes how length should be calculated in a space, sandwiched between 2 4-vectors in tensor multiplication. This length is invariant to all observers. The most significant invariant "length" is the proper time experienced by an inertial frame connecting two spacetime coordinates. The square of this length can be calculated by taking the squared temporal distance and subtracting the squared spatial distance. To achieve this, the metric must take the form:
$$\eta_{\mu\nu}=diag(+1,-1,-1,-1)$$
Which is numerically equivalent to the parity inversion tensor. 
## The Minkowski Inner Product
The Minkowski inner product of the 4-vector and itself is then defined to be:
$$ X^\mu\eta_{\mu\nu}X^\nu=c^2t^2-x^2-y^2-z^2$$
And the spacetime interval is its square root:
$$ds=\sqrt{c^2t^2-x^2-y^2-z^2}$$
The multiplication in the Minkowski inner product invites us to define a co-vector for the 4-vector:
$$X_\mu=\eta_{\mu\nu}X^\nu=(ct, -x, -y, -z)$$
such that the inner product looks like $X_\mu X^\mu$. In general, any inner product between 2 4-vectors - $X_\mu Y^\mu$ - is Lorentz invariant. 