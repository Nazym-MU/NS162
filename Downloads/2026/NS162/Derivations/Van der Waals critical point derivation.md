**Starting point:** Van der Waals equation $p = \dfrac{k_BT}{v-b} - \dfrac{a}{v^2}$

Critical point satisfies $\dfrac{dp}{dv} = 0$ and $\dfrac{d^2p}{dv^2} = 0$ simultaneously.

**First derivative:**
$$\frac{dp}{dv} = -\frac{k_BT}{(v-b)^2} + \frac{2a}{v^3} = 0 \implies k_BT = \frac{2a(v-b)^2}{v^3}$$

**Second derivative:**
$$\frac{d^2p}{dv^2} = \frac{2k_BT}{(v-b)^3} - \frac{6a}{v^4} = 0 \implies k_BT = \frac{3a(v-b)^3}{v^4}$$

Divide the second equation by the first:
$$\frac{(v-b)}{v} = \frac{3}{2} \cdot \frac{(v-b)^3/v^4}{(v-b)^2/v^3} = \frac{3(v-b)}{2v}$$

Wait — divide first into second directly:
$$\frac{3a(v-b)^3/v^4}{2a(v-b)^2/v^3} = 1 \implies \frac{3(v-b)}{2v} = 1 \implies v_c = 3b$$

Substituting $v_c = 3b$ into the first equation:
$$k_BT_c = \frac{2a(2b)^2}{(3b)^3} = \frac{8ab^2}{27b^3} = \boxed{\frac{8a}{27b}}$$

**Verification at $(v_c, T_c)$:**

$dp/dv$: $-\dfrac{8a/27b}{4b^2} + \dfrac{2a}{27b^3} = -\dfrac{2a}{27b^3} + \dfrac{2a}{27b^3} = 0$ ✓

$d^2p/dv^2$: $\dfrac{2 \cdot 8a/27b}{8b^3} - \dfrac{6a}{81b^4} = \dfrac{2a}{27b^4} - \dfrac{2a}{27b^4} = 0$ ✓