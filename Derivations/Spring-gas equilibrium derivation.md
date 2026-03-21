---
dg-publish: true
---
**Setup:** Spring (force constant $k$) + gas in heat bath. Piston at displacement $x$ from equilibrium; gas volume $V = V_1 + Ax$ where $A$ is piston area.

Equilibrium condition: $\frac{\partial F}{\partial x} = 0$

$$\frac{\partial F}{\partial x} = \frac{\partial E}{\partial x} - T\frac{\partial S}{\partial x}$$

**Energy term** — gas is at constant $T$, so its energy doesn't change with $x$. Only the spring contributes:
$$\frac{\partial E}{\partial x} = \mathcal{F}_\text{piston} = -kx$$

**Entropy term** — piston has no entropy; only the gas contributes:
$$\frac{\partial S}{\partial x} = \frac{\partial S}{\partial V}\frac{\partial V}{\partial x} = \frac{P}{T}\cdot A = \frac{\mathcal{F}_\text{gas}}{T}$$

Substituting:
$$\frac{\partial F}{\partial x} = \mathcal{F}_\text{piston} - \mathcal{F}_\text{gas} = 0 \implies \mathcal{F}_\text{piston} = \mathcal{F}_\text{gas}$$

**Result:** Minimising free energy is equivalent to balancing forces.