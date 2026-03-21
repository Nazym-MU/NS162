---
dg-publish: true
---
Two results that follow directly from extensivity of entropy. See [[Euler equation derivation]].

### Euler equation

$$E = TS - PV + \mu N$$

Derived by differentiating $S(cE, cV, cN) = cS(E,V,N)$ with respect to $c$ and setting $c=1$.

### Gibbs-Duhem equation

$$S\,dT - V\,dP + N\,d\mu = 0$$

Derived by taking $d(E = TS - PV + \mu N)$ and subtracting $dE = T\,dS - P\,dV + \mu\,dN$.

Implies $T, P, \mu$ are **not independent** — only two can be varied freely for a one-component system. Breaks down for systems with long-range interactions (gravity, black holes where $S \propto A$ not $V$).

Partial derivative identities from Gibbs-Duhem:
$$\left(\frac{dP}{dT}\right)_\mu = \frac{S}{V}, \qquad \left(\frac{dT}{d\mu}\right)_P = -\frac{N}{S}$$