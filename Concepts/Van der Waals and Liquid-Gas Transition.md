Van der Waals equation of state (Tong eq. 5.1), $v = V/N$:
$$p = \frac{k_BT}{v - b} - \frac{a}{v^2}$$

Two modifications from ideal gas:
- $v - b$: atoms cannot approach closer than $b$; $v$ cannot go below $b$
- $-a/v^2$: attractive interactions between atoms reduce the pressure

### Isotherms
Three regimes depending on $T$:
- $T > T_c$: monotonically decreasing — behaves like ideal gas
- $T = T_c$: inflection point where max and min merge
- $T < T_c$: wiggle develops with a region $dp/dv > 0$ — **unphysical/unstable**

The unstable middle branch ($dp/dv > 0$): compressing reduces pressure, expanding increases it — any perturbation causes explosive density change.

Left branch ($v \sim b$): very densely packed, nearly incompressible — this is the **liquid** state. Right branch ($v \gg b$): compressible, low density — this is the **gas** state.

### Critical temperature

The critical point is where $dp/dv = 0$ and $d^2p/dv^2 = 0$ simultaneously — the inflection point. See [[Van der Waals critical point derivation]].

$$k_BT_c = \frac{8a}{27b}, \qquad v_c = 3b$$

Above $T_c$: no phase transition. At $T_c$: second order transition ($S_	ext{liquid} 	o S_	ext{gas}$ continuously). Below $T_c$: first order liquid-gas transition with latent heat.

### Maxwell construction and phase equilibrium

For two phases to coexist, need thermal, mechanical, and chemical equilibrium:
$$p_\text{liq} = p_\text{gas}, \quad T_\text{liq} = T_\text{gas}, \quad \mu_\text{liq} = \mu_\text{gas}$$

Chemical equilibrium $\mu_\text{liq} = \mu_\text{gas}$ equivalently $g_	ext{liq} = g_	ext{gas}$ (Gibbs free energy per particle).

Using $dG = V\,dP$ at constant $T$ (from $dG = V\,dP - S\,dT$), integrating along the isotherm:
$$\mu(p) = \mu_\text{liq} + \int_{p_	\text{liq}}^{p} v(p', T)\,dp'$$

Equilibrium requires this integral to vanish when we return to $p = p_	ext{liq}$ after traversing the full loop — graphically, the **two areas** enclosed between the flat line $p = p^*$ and the Van der Waals curve must be **equal**. This determines the coexistence pressure $p^*$.

Inside the coexistence curve: system splits into liquid (density $1/v_	ext{liq}$) and gas (density $1/v_	ext{gas}$) in whatever proportions keep the average density fixed. Isotherms become flat lines there.

### Meta-stable states

Between the spinodal curve (through the stationary points of isotherms) and the coexistence curve: states with $dp/dv < 0$ that are locally stable but have higher $G$ than the liquid-gas equilibrium.
- **Supercooled vapour**: gas compressed beyond coexistence curve, metastable
- **Superheated liquid**: liquid expanded beyond coexistence curve, metastable

Any small disturbance causes condensation/nucleation.

### Clausius-Clapeyron (from Van der Waals perspective)

On the $p$-$T$ phase diagram the coexistence region collapses to a line. Moving along it with $g_	ext{liq} = g_	ext{gas}$:
$$s_	ext{liq}\,dT + v_	ext{liq}\,dp = s_	ext{gas}\,dT + v_	ext{gas}\,dp$$

$$\frac{dp}{dT} = \frac{s_	ext{gas} - s_	ext{liq}}{v_	ext{gas} - v_	ext{liq}} = \frac{L}{T(v_	ext{gas} - v_	ext{liq})}$$

where specific latent heat $L = T(s_	ext{gas} - s_	ext{liq})$. Liquid-gas transition is **first order**: $V = \partial G/\partial p$ is discontinuous across the transition.