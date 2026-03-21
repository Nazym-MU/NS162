---

---
- Free energy is to a constant $T$ system what $E$ is to a mechanical system.
- Helmholtz free energy is the available energy to do work at constant $T$ and $V$.
- In a system kept at constant $T$ and $V$, interacting with the surroundings only through an exchange of heat (i.e. no work), the Helmholtz free energy never increases.
- In an isolated system at constant $T$ and $V$, Helmholtz free energy is minimized in equilibrium.
- Free energy refers to the free energy of the system only $F = F_\text{system}$.
---
Four thermodynamic potentials, each natural for a different set of held-fixed variables:

| Potential | Definition | Natural variables |
|---|---|---|
| Helmholtz $F$ | $E - TS$ | $T, V, N$ |
| [[Enthalpy]] $H$ | $E + PV$ | $S, P, N$ |
| Gibbs $G$ | $E + PV - TS$ | $T, P, N$ |
| Grand $\Omega$ | $E - TS - \mu N$ | $T, V, \mu$ |

See [[Euler equation and Gibbs-Duhem]] for the underlying structure.

---

### Helmholtz free energy $F = E - TS$

Differential (using $dE = T\,dS - P\,dV + \mu\,dN$ and chain rule on $TS$):
$$dF = dE - T\,dS - S\,dT = -P\,dV + \mu\,dN - S\,dT$$

$dS$ drops out — $F = F(V, N, T)$. This is the Legendre transform replacing $S$ with $T$.

Maxwell relations:
$$\left(\frac{\partial F}{\partial V}\right)_{N,T} = -P, \qquad \left(\frac{\partial F}{\partial N}\right)_{V,T} = \mu, \qquad \left(\frac{\partial F}{\partial T}\right)_{V,N} = -S$$

**Why it's useful:** $V, N, T$ are easily measurable. Contrast with $E(S,V,N)$ and $S(E,V,N)$ where entropy is hard to measure directly.

#### Free energy and work

For an isolated system at constant $T$ and $V$, interacting with surroundings only by heat exchange — see [[Helmholtz work inequality derivation]]:
$$W \leq -\Delta F$$
equality iff reversible. Free energy is literally the energy *free* to do work.

When $W = 0$: $\Delta F \leq 0$ — Helmholtz free energy never increases at constant $T, V$.

**Equilibrium = state of minimum $F$** (for isolated system at constant $T, V$).

Example — two gases separated by a partition at constant $T$, minimising $F$:
$$dF = -P_1\,dV_1 - P_2\,d(V - V_1) = (P_2 - P_1)\,dV_1 = 0 \implies P_1 = P_2$$
Same result as maximising total entropy — the two are equivalent.

#### Connection to partition function

From the canonical ensemble, $S = \langle E\rangle/T + k_B \ln Z$, so:
$$\boxed{F = -k_B T \ln Z}$$

Equivalently: $e^{-\beta F} = Z = \sum e^{-\beta E}$ — free energy equals energy when there is only one microstate.

For monatomic ideal gas:
$$F = -Nk_BT\left(\ln\frac{V}{N} + \frac{3}{2}\ln\frac{2\pi mk_BT}{h^2} + 1\right)$$

Checks: $-\left(\frac{\partial F}{\partial T}\right)_{V,N} = S$ ✓ and $-\left(\frac{\partial F}{\partial V}\right)_{T,N} = \frac{Nk_BT}{V} = P$ ✓ (ideal gas law)

#### Spring and gas example

See [[Spring-gas equilibrium derivation]]. Piston+gas system in heat bath — equilibrium via $\frac{\partial F}{\partial x} = 0$:
$$\frac{\partial F}{\partial x} = \underbrace{\frac{\partial E}{\partial x}}_{= \mathcal{F}_\text{piston} = -kx} - T\frac{\partial S}{\partial x} = \mathcal{F}_\text{piston} - \mathcal{F}_\text{gas} = 0$$
Minimising $F$ is equivalent to balancing forces.

#### Energy (non)-minimisation

Total energy is conserved — it never minimises. What minimises is free energy:
$$F = -T\left[S_\text{sys} + \frac{-E}{T}\right] = -T\left[S_\text{sys} + S_\text{surr}\right]$$

Minimising $F$ = maximising total entropy = 2nd law. "Energy minimisation" (ball rolling downhill, spring with friction) is always free energy minimisation driven entirely by entropy.

Free energy is a property of the *ensemble*, not of a single microstate. $F = F_	ext{system}$ only — minimise the system's $F$, ignore the bath. Use $F$ for constant $T, V$; use $G$ for constant $T, P$.

---

### Gibbs free energy $G = E + PV - TS$

$$dG = dE + d(PV) - d(TS) = V\,dP - S\,dT + \mu\,dN$$

$G = G(P, N, T)$. Maxwell relations:
$$\left(\frac{\partial G}{\partial T}\right)_{P,N} = -S, \qquad \left(\frac{\partial G}{\partial P}\right)_{T,N} = V, \qquad \left(\frac{\partial G}{\partial N}\right)_{P,T} = \mu$$

Natural potential for chemistry and biology: reactions at constant $T, P$ are spontaneous iff $\Delta G \leq 0$.

---

### Grand free energy $\Omega = E - TS - \mu N$

Natural for the grand canonical ensemble (constant $T, V, \mu$; $N$ fluctuates).