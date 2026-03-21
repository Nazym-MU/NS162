---
dg-publish: true
---
Derive the partition function for an ideal gas and extract thermodynamic quantities from it.
## Single Particle in a Box
Energy levels for a particle in a 3D box of side $L$:
$$E_{n_x, n_y, n_z} = \frac{\hbar^2 \pi^2}{2mL^2}(n_x^2 + n_y^2 + n_z^2)$$
Single-particle partition function — convert sum to integral (valid when $k_BT \gg$ level spacing):
$$z = \int_0^\infty dn_x\, dn_y\, dn_z\, e^{-\beta \frac{\hbar^2\pi^2}{2mL^2}(n_x^2+n_y^2+n_z^2)} = \left(\frac{L}{\lambda}\right)^3 = \frac{V}{\lambda^3}$$
where $\lambda = \sqrt{\frac{2\pi\hbar^2}{mk_BT}}$ is the thermal de Broglie wavelength.
## N-Particle Partition Function
Particles are indistinguishable, so divide by $N!$:
$$Z = \frac{z^N}{N!} = \frac{1}{N!}\left(\frac{V}{\lambda^3}\right)^N$$
$$\ln Z = N\ln V - 3N\ln\lambda - \ln N!$$
## Thermodynamic Quantities
Using Stirling's approximation ($\ln N! \approx N\ln N - N$):
$$\langle E \rangle = -\frac{\partial \ln Z}{\partial \beta} = \frac{3}{2}Nk_BT$$
$$P = k_BT\frac{\partial \ln Z}{\partial V} = \frac{Nk_BT}{V} \quad \Rightarrow \quad PV = Nk_BT$$
$$S = k_B(\ln Z + \beta\langle E\rangle) = Nk_B\left[\ln\frac{V}{N\lambda^3} + \frac{5}{2}\right] \quad 	ext{(Sackur-Tetrode)}$$
## Classical Limit
The classical partition function arrives at the same result via phase space integration:
$$Z = \frac{1}{N! h^{3N}}\int d^{3N}p\, d^{3N}q\, e^{-\beta H}$$
The $h^{3N}$ factor sets the fundamental phase space cell size — needed to make $Z$ dimensionless and $S$ extensive.