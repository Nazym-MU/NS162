#### From Feynman's lectures
Interesting note: The integral is a minimum if a velocity is constant (when there are no forces). If you deviate from the mean velocity too much, the mean square of that is always greater than the square of the mean. However, when we throw the ball upwards, it rises fast and then slows down. This is because we also incorporate the potential energy. You can't go up too fast because you will have too much kinetic energy. The solution is a balance between trying to get more potential energy with the least amount of extra kinetic energy.
$$\text{Action} = S = \int_{t_1}^{t_2} (\text{KE – PE})\space dt = \int \left[ \frac{m}{2} \left( \frac{dx}{dt} \right)^2 -V(x) \right] dt$$
Calculus of variations -> we can't just take the derivative and set it equal to zero because it's a path, not a variable.

The "True Path" taken by a particle is the one where the Action ($S$) is at a minimum. Therefore, if you take the True Path and distort it slightly (a first-order variation), the value of the Action should not change (to a first-order approximation). This is equivalent to setting the first derivative (or variation) to zero.

We call $\underline{x(t)}$ the true path that we are trying to find. We take some trial path $x(t)$ that differs from the true path by a small amount which we will call $\eta(t)$. If we calculate the action $S$ for the path $x(t)$, the difference between $S$ and the action we calculated for $\underline{x(t)}$ must be 0 in the first order (the difference in the second order can be nonzero).
Apply boundary conditions: $\eta(t_1)$ and $\eta(t_2)=0$ because these must be fixed, we must not deviate from the true path.
$$x(t) = \underline{x(t)} + \eta(t)$$
$$S = \int_{t_1}^{t_2} \left[ \frac{m}{2} \left( \frac{d\underline{x}}{dt} + \frac{d\eta}{dt} \right)^2 - V(\underline x + \eta) \right] dt =$$
$$= \int_{t_1}^{t_2} \left[ \frac{m}{2} \left( \left( \frac{d\underline{x}}{dt} \right)^2 + 2\frac{d\underline x}{dt} \frac{d\eta}{dt} +\left( \frac{d\underline{\eta}}{dt} \right)^2 \right)  - V(\underline x + \eta) \right] dt$$
Ignore the second order $\eta$ parts. As for the potential energy, we can expand it as Taylor series:
$$V(\underline x + \eta) = V(\underline x) + \eta V'(\underline x) + \frac{\eta^2}{2}V''(\underline x) +...$$ and ignore the second order $\eta$ parts. 
$$S = \int^{t_2}_{t_1} \left[\frac{m}{2}\left(\frac{d\underline x}{dt}\right)^2 - V(\underline x) + m\frac{d\underline x}{dt}\frac{d\eta}{dt} - \eta V'(\underline x) + O(\eta^2)\right]dt$$
The first two terms correspond to the action of $\underline S$. Let $\delta S$ (variation in $S$) be the difference between $S$ and $\underline S$, which corresponds to the other two terms. Leaving out the second and higher order terms as well, we get:
$$\delta S = \int^{t_2}_{t_1} \left[ m\frac{d\underline x}{dt}\frac{d\eta}{dt} - \eta V'(\underline x)\right]dt$$
Using integration by parts, we can write the variational derivative as:
$$\delta S = m\frac{d\underline x}{dt} \eta(t)\Big|_{t_1}^{t_2} - \int^{t_2}_{t_1} \frac{d}{dt} \left(m\frac{d\underline x}{dt}\right)  \eta(t)dt - \int^{t_2}_{t_1} V'(\underline x) \eta(t)dt$$
The first term disappears because $\eta(t_1) = 0$ and $\eta(t_2) = 0$.
$$\delta S = \int^{t_2}_{t_1} \left[ -m\frac{d^2\underline x}{dt^2} - V'(\underline x) \right] \eta(t)dt$$
If the action integral is zero for any $\eta$, then the coefficient of $\eta$ must be zero. The action integral will be a minimum for th epath that satisfies $$\left[-m \frac{d^2\underline x}{dt^2} - V'(\underline x) \right] = 0$$
This is just $F = ma$. Derivative of the potential energy is force. The principle of least action says that the path that has the minimum action is the one satisfying the Newton's law.

