---
dg-publish: true
---
Partition function encodes all thermodynamic properties of a system from its energy spectrum.
## Partition Function
For a system with energy states $E_i$:
$$Z = \sum_i e^{-E_i/k_BT}$$
Key quantities derived from $Z$:

| Quantity | Formula |
|---|---|
| Free energy | $F = -k_BT \ln Z$ |
| Average energy | $\langle E \rangle = -\frac{\partial \ln Z}{\partial \beta}$, where $\beta = \frac{1}{k_BT}$ |
| Heat capacity | $C_V = \frac{\partial \langle E \rangle}{\partial T}$ |
| Entropy | $S = k_B(\ln Z + \beta \langle E \rangle)$ |
If a system is composed of independent subsystems: $Z = Z_1 \cdot Z_2 \cdot \ldots$
## 1D Quantum Harmonic Oscillator (QHO)
Energy levels: $E_n = \hbar\omega(n + \frac{1}{2})$, $n = 0, 1, 2, \ldots$
$$Z = \sum_{n=0}^\infty e^{-\beta\hbar\omega(n+1/2)} = \frac{e^{-\beta\hbar\omega/2}}{1 - e^{-\beta\hbar\omega}}$$
$$\langle E \rangle = \frac{\hbar\omega}{2} + \frac{\hbar\omega}{e^{\beta\hbar\omega}-1}$$
- Low $T$: system freezes in ground state, $\langle E \rangle \to \frac{\hbar\omega}{2}$
- High $T$: $\langle E \rangle \to k_BT$ (classical equipartition)
## Statistical Mechanics of the Ideal Gas
For $N$ non-interacting particles in volume $V$, the partition function factorizes: $Z = z^N$ where $z$ is the single-particle partition function.
$$z = \frac{V}{\lambda^3}, \quad \lambda = \sqrt{\frac{2\pi\hbar^2}{mk_BT}}$$
($\lambda$ is the thermal de Broglie wavelength)
$$Z = \frac{1}{N!}\left(\frac{V}{\lambda^3}\right)^N$$
The $N!$ accounts for indistinguishability (fixes Gibbs paradox, see [[Gibbs Paradox]]).
Key results:
$$\langle E \rangle = \frac{3}{2}Nk_BT$$
$$P = \frac{Nk_BT}{V} \quad \Rightarrow \quad PV = Nk_BT$$
$$S = Nk_B\left[\ln\frac{V}{N\lambda^3} + \frac{5}{2}\right] \quad 	\text{(Sackur-Tetrode equation)}$$