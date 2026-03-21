---
dg-publish: true
---
**Starting point:** $S(E, V, N)$ is extensive: $S(cE, cV, cN) = cS(E, V, N)$

Differentiate both sides with respect to $c$:
$$\frac{\partial S}{\partial cE}\cdot E + \frac{\partial S}{\partial cV}\cdot V + \frac{\partial S}{\partial cN}\cdot N = S(E,V,N)$$

Set $c = 1$ and substitute the definitions $\frac{\partial S}{\partial E} = \frac{1}{T}$, $\frac{\partial S}{\partial V} = \frac{P}{T}$, $\frac{\partial S}{\partial N} = -\frac{\mu}{T}$:

$$\frac{E}{T} + \frac{P}{T}V - \frac{\mu}{T}N = S$$

**Result:**
$$\boxed{E = TS - PV + \mu N}$$

---

**Gibbs-Duhem** — take total derivative of the Euler equation:
$$dE = T\,dS + S\,dT - P\,dV - V\,dP + \mu\,dN + N\,d\mu$$

Subtract the fundamental relation $dE = T\,dS - P\,dV + \mu\,dN$:

$$\boxed{S\,dT - V\,dP + N\,d\mu = 0}$$