### Clausius-Clapeyron

On the coexistence curve, $g_	ext{liq} = g_	ext{gas}$. Moving along it:
$$dg_\text{liq} = -s_\text{liq}\,dT + v_\text{liq}\,dp = dg_\text{gas} = -s_\text{gas}\,dT + v_\text{gas}\,dp$$

Rearranging:
$$\boxed{\frac{dp}{dT} = \frac{s_\text{gas} - s_\text{liq}}{v_\text{gas} - v_\text{liq}} = \frac{L}{T(v_\text{gas} - v_\text{liq})}}$$

where $L = T(s_\text{gas} - s_\text{liq})$ is the specific latent heat.

---

### Van der Waals critical point

$$p = \frac{k_BT}{v-b} - \frac{a}{v^2}$$

Set $dp/dv = 0$ and $d^2p/dv^2 = 0$:

$$\frac{dp}{dv} = -\frac{k_BT}{(v-b)^2} + \frac{2a}{v^3} = 0 \implies k_BT = \frac{2a(v-b)^2}{v^3}$$

$$\frac{d^2p}{dv^2} = \frac{2k_BT}{(v-b)^3} - \frac{6a}{v^4} = 0 \implies k_BT = \frac{3a(v-b)^3}{v^4}$$

Dividing:
$$\frac{3(v-b)}{2v} = 1 \implies \boxed{v_c = 3b}$$

Substituting back:
$$\boxed{k_BT_c = \frac{8a}{27b}}$$

Verification at $(v_c, T_c)$: substituting $v_c = 3b$, $v_c - b = 2b$, $k_BT_c = 8a/27b$:

$dp/dv = -\frac{2a}{27b^3} + \frac{2a}{27b^3} = 0$ ✓

$d^2p/dv^2 = \frac{2a}{27b^4} - \frac{2a}{27b^4} = 0$ ✓