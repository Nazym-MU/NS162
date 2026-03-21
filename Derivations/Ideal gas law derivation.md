$$P= \frac{F}{A} = \frac{\Delta p}{\Delta t \cdot A} = \frac{2mv_x}{\Delta t \cdot A}$$
Given a small increment in time $\Delta t$, the particles need to be $\Delta x \leq v_x\Delta t$ close to the wall to hit it.
The probability that a small particle traveling at $v_x$ is within the small volume defined by the area we focus on is: $\frac{Av_x\Delta t}{V}$
Pressure:
$$P =\frac{1}{2}\int \frac{2mv_x}{\Delta t \cdot A}\cdot \frac{Av_x\Delta t}{V}\cdot N p(v_x) dv_x = \frac{mN}{V}\int v_x^2p(v_x)dv_x$$
- 1/2 comes from the fact that only half the particles are heading towards the wall
- $p(v_x)$ is the probability that a particle is traveling at $v_x$
- there are $N$ particles we're observing
- multiply the pressure by the probability of being in that region and the probability of having that velocity
- integrate over all possible velocities
That integral gives the expectation value (definition: probability * the velocity)
$$\int v_x^2 p(v_x)dv_x = 
\langle v_x^2 \rangle$$
Isotropy of the gas: $$E = \frac{1}{2}m\langle v^2 \rangle = \frac{1}{2}m\langle v^2_x + v^2_y + v^2_z \rangle = \frac{3}{2}m\langle v_x^2\rangle$$
$$m\langle v_x^2 \rangle = \frac{2}{3} E$$
Pressure: $$P = \frac{2NE}{3V}$$
 $$PV = \frac{2NE}{3} = Nk_BT$$
 $$E = \frac{3}{2}k_BT$$