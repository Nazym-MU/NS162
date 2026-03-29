---
dg-publish: true
---
Extension of [[1D Ising Model]] to a 2D $L \times L$ grid. Energy:
$$H = -H\sum_{i=0}^{N} \sigma_i - J\sum_{\langle i,j \rangle} \sigma_i \sigma_j$$
where $\langle ij \rangle$ sums over all nearest-neighbor pairs. In $d$ dimensions each spin has $2d$ neighbors. Magnetization:
$$M = \langle \sigma_i \rangle = \frac{\sum_i \sigma_i}{N}, \qquad \Omega(m) = \frac{N!}{m!(N-m)!}, \qquad M = \frac{2m}{N} - 1$$
where $m$ is the number of spin-up atoms. Boltzmann factor:
$$e^{-H/kT} = e^{\frac{1}{\hat{T}}\sum_{\langle ij \rangle} s_i s_j + \frac{\hat{h}'}{\hat{T}}\sum_i s_i}, \qquad \hat{T} = kT/J,\quad \hat{h}' = h/J$$
Exact critical temperature ($h=0$): $\hat{T}_c = \dfrac{2}{\ln(1+\sqrt{2})} \approx 2.269$

---

### Cases: effect of $H$ and $J$

| Case          | Energy minimum                                 | Low-$T$ phase                                                  | Notes                                                                                                                |
| ------------- | ---------------------------------------------- | -------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------- |
| $H=0, J>0$    | all spins aligned, $\sigma_i\sigma_j = +1$     | $\langle M \rangle = \pm 1$ (either)                           | Spontaneous symmetry breaking; large barrier between $M=+1$ and $M=-1$; system freezes in one — ergodicity breaking  |
| $H=0, J<0$    | all spins alternating, $\sigma_i\sigma_j = -1$ | $\langle M \rangle = 0$ even at low $T$                        | Also spontaneous symmetry breaking; two ground states (checkerboard and its inverse); long-range order still present |
| $H\neq0, J=0$ | all spins parallel to $H$                      | $\langle M\rangle$ follows Maxwell-Boltzmann for a single spin | $N$ independent spins; no phase transition; $M$ changes smoothly with $T$                                            |
At high $T$ in all cases: entropy dominates, spins roughly equal up/down, $\langle M \rangle \approx 0$.

**Spontaneous symmetry breaking** ($H=0, J>0$): flipping all spins leaves energy unchanged — the system has a symmetry. But below $T_c$ it picks one of the two minima and stays. Ensemble average gives $\langle M \rangle = 0$ but time average gives $\langle M \rangle \neq 0$ — the two disagree, so the system is not ergodic.

**Negative temperature** ($H \neq 0, J=0$, special case): as spins flip from all-parallel-to-$H$ toward half-up/half-down, entropy *increases* with energy. Then past the halfway point, entropy *decreases* with energy — meaning $\frac{1}{T} = \frac{\partial S}{\partial E} < 0$, so $T < 0$. Only possible because the Ising model has no kinetic energy; in real systems kinetic degrees of freedom make $S$ always increasing with $E$.

---

### Phase transition in $\rho(m)$

The full distribution $\rho(m)$ (not just $\langle m \rangle$) characterises the phase:

- $T > T_c$: single peak at $m = 0$, width $\sim 1/\sqrt{N}$ — disordered
- $T = T_c$: width becomes **independent of $N$** — infinite correlation length; system cannot be decomposed into independent subsystems; self-similar (renormalization group)
- $T < T_c$: two peaks at $m = \pm m^*$ — two coexisting phases; as $N 	o \infty$ transitions between them vanish

Phase transition: as $h$ crosses 0 for $T < T_c$, magnetization jumps discontinuously (in the $N 	o \infty$ limit).

---

### Simulation: MCMC

Partition function $Z(T,J,h) = \sum_{\{s_i\}} e^{-H/kT}$ has $2^N$ terms — exact sum intractable. Use Markov Chain Monte Carlo to sample from the Boltzmann distribution instead.

Two algorithms:
- **Metropolis**: flips individual spins; can get trapped in metastable states near $T_c$ — good for visualising real-time-like dynamics
- **Wolff**: flips correlated clusters; escapes metastable states in one step — better for finding true equilibrium near $T_c$

MCMC "time steps" are not physical time — only guarantees convergence to Boltzmann distribution, not real dynamics.

---

### Ising model as a lattice gas (liquid-gas mapping)

Coarse-grain a 2D molecular gas to grid cells of size $\sim r_0$ (molecular diameter): each cell is either occupied ($s_i = +1$) or empty ($s_i = -1$). Nearest-neighbor interaction $J \sim U_0$ (attractive well depth).

Number of molecules: $n = \sum_i (1+s_i)/2$. The field $h$ term becomes:
$$-h\sum_i s_i = -2hn + \text{const} \implies e^{-h/kT\sum s_i} \to e^{-2h/kT \cdot n}$$

So $h$ plays the role of **chemical potential**: $\mu = g = 2h$. System is in the grand canonical ensemble — fixed $\mu$, not fixed $N$.

Density: $\rho = \frac{n}{N} \cdot \frac{1}{v_0}$, related to magnetization by $\rho = \frac{m+1}{2} \cdot \frac{1}{v_0}$.

Phase diagram in $(h, T)$ maps to $(\mu, T)$, and qualitatively to $(p, v)$ — isotherms below $T_c$ show the same discontinuous volume jump as Van der Waals. High-density phase ($\langle m \rangle > 0$) = liquid; low-density phase ($\langle m \rangle < 0$) = gas.

---

### Universality

Near $T_c$, many different microscopic models (Ising, Van der Waals, real fluids) become **quantitatively identical** at large length scales — they share the same critical exponents. This is universality. Explaining it requires renormalization group (beyond this course).
