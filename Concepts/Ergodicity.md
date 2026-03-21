---
dg-publish: true
---
$$\langle J \rangle = \lim_{T\to\infty}\left( \frac{1}{T} \int^T_0 J(u(t))dt \right)$$
The time average of a function along a trajectory starting from almost everywhere equals the ensemble average.
$X(t)$ is ergodic if $\bar{X} = \langle X \rangle$. In other words, when the average along a single trajectory and the average over many different trajectories at a fixed time are equivalent.

Hypothesis: $w[t]$ eventually visits all of $\Omega$ regardless of $w[0]$. If true, then Birkhoff's equality holds: $$\lim_{T\to\infty} \frac{1}{T}\int_0^T f(w[t])dt = \int_\Omega f(w)P(w)dw$$
$$\text{average along a long trajectory} = \text{average over all possible states}$$
---
- The ergodic theorem states that for typical Hamiltonian systems with finite dynamics, the time average is equal to the ensemble average.
- Mixing (self-correlation of a well-behaved function) means that correlation decays in time.
	- Weak mixing is when the time average of the *squared* correlation decays
- Chaos means the phase space orbits exhibit local instability, namely that phase space trajectories exiting from nearby points diverge exponentially.
	- Trajectories in an ergodic flow diverge algebraically, in contrast to the exponential divergence of chaos. Thus, 'chaos' is stronger than 'ergodicity'. A chaotic flow is definitely mixing.
---
## Importance of all three
- Ergodicity links time and ensemble averages.
- Mixing and chaos justify certain key assumptions in the derivation of the Boltzmann equation and the proof of the H-Theorem.
---
Microcanonical ensemble is the largest region of the phase space. Given that entropy only increases ($d\Omega_{eq}/dt \geq 0$), $\Omega_{eq}$ grows until it reaches $\Omega_{eq}(E, V, N)$. The only constraints to how much it can grow are the conserved quantities like energy, volume, and number of particles.
Symmetry creates conservation laws, and conservation laws prevent ergodicity