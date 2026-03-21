---
dg-publish: true
---
A phase transition is an abrupt, discontinuous change in the properties of a system. The stable phase is always the one with lowest free energy $G = E + PV - TS$.
### Why phases exist
At low $T$: $G$ dominated by $E$ → solid preferred. As $T$ increases, $-TS$ grows → liquid, then gas. Each phase is a tradeoff between energy and entropy.
### Van der Waals equation
$$p = \frac{k_BT}{v - b} - \frac{a}{v^2}, \qquad v = V/N$$
Two corrections to ideal gas: $b$ is the minimum approach distance between atoms (v cannot go below $b$); $a/v^2$ captures attractive interactions that reduce pressure.
Isotherms for $T < T_c$ develop a wiggle with an unstable region ($dp/dv > 0$). Left branch ($v \sim b$): liquid — dense, nearly incompressible. Right branch: gas — compressible, low density.
### Critical point
The wiggle flattens into an inflection point at $T_c$. Condition: $dp/dv = 0$ and $d^2p/dv^2 = 0$. See [[Phase Transitions derivations]]:

$$k_BT_c = \frac{8a}{27b}, \qquad v_c = 3b$$
Above $T_c$: no phase transition, single fluid. At $T_c$: second order transition ($S_\text{liq} \to S_\text{gas}$ continuously). Below $T_c$: first order transition with latent heat.
### Phase equilibrium and Maxwell construction
Two phases coexist when $p$, $T$, and $\mu$ are equal. Since $G = \mu N$, this means $g_\text{liq} = g_\text{gas}$. Using $dG = V\,dP$ at constant $T$, integrating along the isotherm requires:
$$\int_\text{loop} v\,dp = 0$$
Graphically: the two areas enclosed between the flat line $p = p^*$ and the Van der Waals curve must be equal (**Maxwell construction**). This gives the coexistence pressure. Inside the coexistence curve, isotherms become flat — liquid and gas coexist in whatever proportions keep average density fixed.

### Metastable states
Between the spinodal curve (through stationary points of isotherms) and the coexistence curve: states with $dp/dv < 0$, locally stable but higher $G$ than equilibrium. Supercooled vapour (gas compressed past coexistence) and superheated liquid (liquid expanded past coexistence) — any disturbance triggers condensation/nucleation.

### Clausius-Clapeyron equation

On the $p$-$T$ diagram the coexistence region collapses to a line. Moving along it with $g_\text{liq} = g_\text{gas}$, see [[Phase Transitions derivations]]:

$$\frac{dp}{dT} = \frac{s_\text{gas} - s_\text{liq}}{v_\text{gas} - v_\text{liq}} = \frac{L}{T(v_\text{gas} - v_\text{liq})}$$

where specific latent heat $L = T(s_\text{gas} - s_\text{liq})$. Slope proportional to latent heat; large when volumes are similar (solid-liquid), small when volumes differ greatly (liquid-gas).

Liquid-gas is a **first order** transition: $V = \partial G/\partial p$ is discontinuous. At $T_c$ it becomes second order.

### Latent heat

At the transition $T$, phases have equal $G$. Extra heat at constant $T$ converts one phase to the other — temperature does not rise. From $dE = T\,dS$ at constant $T$: $E_2 - E_1 = T(S_2 - S_1)$.

### Symmetry and critical points

Solid-liquid coexistence curve has no critical point: solid has crystal symmetries (translational, rotational) that liquid lacks. Phases with different symmetry groups must always be separated by a transition (Landau symmetry principle). Liquid and gas share the same symmetry group, so one can continuously deform into the other — hence the liquid-gas curve ends at a critical point.
### Triple point
Unique $(P, T)$ where solid, liquid, gas all have equal $G$ and coexist. Below triple-point pressure: no liquid phase; solid goes directly to gas (sublimation).