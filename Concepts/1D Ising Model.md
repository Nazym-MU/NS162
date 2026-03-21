---
dg-publish: true
---
$N$ spins $s_1, s_2, \ldots, s_N$, each $= \pm 1$ on a regular grid; only neighbors interact. 1D = chain, 2D = grid.

### Energy

$$E(s_1, s_2, \ldots) = -h\sum_{i=1}^{N} s_i - J\sum_{i=1}^{N-1} s_i s_{i+1}$$

- $-h\sum s_i$: coupling to external field. Energy decreases when spins align with $h$.
- $-J\sum s_i s_{i+1}$: neighbor coupling. $J > 0$ → ferromagnetic; $J < 0$ → anti-ferromagnetic.

Studied in the canonical ensemble. Define $\hat{h} = h/kT$, $\hat{J} = J/kT$. Boltzmann factor:

$$e^{-E/kT} = e^{\hat{h}\sum s_i + \hat{J}\sum s_i s_{i+1}}$$

Partition function:

$$Z(	\hat{h}, \hat{J}) = \sum_{s_1=\pm1,\, s_2=\pm1,\ldots} e^{\hat{h}\sum s_i + 	\hat{J}\sum s_i s_{i+1}}$$

---
### Single spin ($J=0$, $N=1$)

$$Z_0(	\hat{h}) = \sum_{s_1=\pm1} e^{-\hat{h}s_1} = e^{-\hat{h}} + e^{\hat{h}} = \cosh(\hat{h})$$
Average spin:
$$\langle s_1 \rangle = \frac{1}{Z_0(\hat{h})}\sum_{s_1=\pm1} s_1\, e^{-\hat{h}s_1} = \frac{1}{2\cosh	\hat{h}}\!\left(-e^{-	\hat{h}} + e^{\hat{h}}\right) = \frac{\sinh \hat{h}}{\cosh	\hat{h}} = \tanh(\hat{h})$$
Response saturates at $\langle s \rangle = \pm 1$ for large $|\hat{h}|$.

---
### Non-interacting spins ($J=0$, $N$ spins)
Boltzmann factor factorizes → partition function factorizes:
$$Z(	\hat{h}, N) = Z_0(\hat{h})^N = \cosh(	\hat{h})^N$$
Magnetization density $m = \frac{1}{N}\sum_i s_i$, and by the same argument per spin:
$$\langle m \rangle = \tanh	\hat{h}$$

---

### Strong coupling limit ($J \to \infty$)

$\hat{J} \to \infty$ locks spins into alignment; anti-aligned configurations have Boltzmann factor $\to 0$. System behaves as a single dipole of strength $N$:

$$\langle m \rangle_{J	\to\infty} = 	\tanh(N	\hat{h})$$

As $N \to \infty$: sharp step — any nonzero $h$ fully magnetizes the system. ($J \to \infty$ equivalent to $T \to 0$ at fixed $J$.)

---
### $h = 0$, general $J$ — link variable
Define $l_i = s_i s_{i+1} = \pm 1$ (aligned vs. anti-aligned). Energy becomes:

$$E = -J\sum_{i=1}^{N-1} s_i s_{i+1} = -J\sum_{i=1}^{N-1} l_i$$

The $N-1$ link variables are independent — this is just a non-interacting Ising model for the links with external field $J$. This is a **duality**: the interacting spin model maps exactly onto a non-interacting link model.

---

### General result ($N \to \infty$, transfer matrix)

$$\langle m \rangle = \frac{\sinh	\hat{h}}{\sqrt{\sinh^2	\hat{h} + e^{-4	\hat{J}}}}$$

Recovers $\tanh	\hat{h}$ at $\hat{J}=0$ and sharp step as $\hat{J} 	\to \infty$. No finite-$T$ phase transition in 1D for any $J > 0$. The 2D Ising model does have a finite critical $T_c > 0$.