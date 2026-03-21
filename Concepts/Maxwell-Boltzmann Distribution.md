Describes the distribution of speeds of particles in an ideal gas at temperature $T$.

The energy of a single particle moving in 3D:
$$E = \frac{1}{2}m(v_x^2 + v_y^2 + v_z^2)$$

From the canonical ensemble, the probability of a microstate is $p \propto e^{-E/k_BT}$. Since the three velocity components are independent, the joint distribution factorizes:
$$p(v_x, v_y, v_z) \propto e^{-m(v_x^2+v_y^2+v_z^2)/2k_BT}$$

Normalizing each Gaussian component:
$$p(v_x) = \sqrt{\frac{m}{2\pi k_BT}} \exp\!\left(-\frac{mv_x^2}{2k_BT}\right)$$

### Speed distribution
Converting to spherical coordinates and integrating over all directions (the $4\pi v^2$ factor comes from the surface area of a sphere of radius $v$):
$$f(v) = 4\pi v^2 \left(\frac{m}{2\pi k_BT}\right)^{3/2} \exp\!\left(-\frac{mv^2}{2k_BT}\right)$$

This is the Maxwell-Boltzmann speed distribution.

### Key speeds
- **Most probable speed** (peak of $f(v)$): $v_p = \sqrt{\dfrac{2k_BT}{m}}$
- **Mean speed**: $\langle v \rangle = \sqrt{\dfrac{8k_BT}{\pi m}}$
- **RMS speed**: $v_\text{rms} = \sqrt{\dfrac{3k_BT}{m}}$

### Mean kinetic energy
$$\langle E \rangle = \frac{1}{2}m\langle v^2 \rangle = \frac{3}{2}k_BT$$

Each velocity component contributes $\frac{1}{2}k_BT$ — this is equipartition.