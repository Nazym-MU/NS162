---
dg-publish: true
---
Derive pressure and chemical potential of the ideal gas from entropy.
Remember that for a three dimensional system of $N$ billiards of mass $m$ in a volume $V$, we have found $\Omega_q \propto V^N$ and $\Omega_p \propto m(2mE)^{\frac{3N-2}{2}}$.
## Entropy of the Billiards Model
$$S(E, V, N) = Nk_B \ln V - \frac{3}{2}Nk_B \ln N + \frac{3}{2}Nk_B \ln E + C(N)$$
Temperature:
$$T = -\frac{\partial S/\partial E}{\partial S / \partial \mu} \quad \Rightarrow \quad \frac{1}{T} = \frac{\partial S}{\partial E} = \frac{3Nk_B}{2E} \quad \Rightarrow \quad E = \frac{3}{2}Nk_BT$$
## Pressure
Moving a piston: $W = P\Delta V$, so $dE = -P\,dV$.
Setting $dS = 0$:
$$\frac{\partial S}{\partial E}(-P\,dV) + \frac{\partial S}{\partial V}dV = 0$$
$$\boxed{P_\text{eq} = T\frac{\partial S}{\partial V}}$$
For the Billiards model, $\frac{\partial S}{\partial V} = \frac{Nk_B}{V}$, so:
$$\boxed{PV = Nk_BT}$$
## Chemical Potential
Setting $dS = 0$, $dN = 1$:
$$dS = \frac{\partial S}{\partial E}(-\mu) + \frac{\partial S}{\partial N}dN = 0$$
$$\boxed{\mu_\text{eq} = T\frac{\partial S}{\partial N}}$$