## Heat and Entropy
At constant volume ($dW = 0$), $dQ = dE$. Using the definition of temperature:
$$dQ = dE = \left(\frac{\partial \log \Omega}{\partial E}\right)^{-1} d(\log \Omega) = T \, dS$$

So adding heat raises entropy; removing heat lowers it.

For heat $dQ$ flowing from A to B:
$$dS = dS_B + dS_A = \frac{dQ}{T_B} - \frac{dQ}{T_A}$$
- $T_A = T_B$: $dS = 0$, no heat flows (thermal equilibrium)
- $T_A < T_B$: $dS < 0$, forbidden by the second law
- $T_A > T_B$: $dS > 0$ ✓ — heat flows from hot to cold, total entropy increases

## Heat Capacity
Proportionality between heat added and temperature rise: $C \equiv \frac{dQ}{dT}$

**At constant volume** (no work done):
$$C_V = T\left(\frac{\partial S}{\partial T}\right)_V$$

**At constant pressure** (system can expand, $dE = TdS - PdV$):
$$C_P = T\left(\frac{\partial S}{\partial T}\right)_P + P\left(\frac{\partial V}{\partial T}\right)_P$$

$C_P > C_V$ for nearly all systems — at constant pressure, some heat goes into expansion work rather than raising temperature.

## Ideal Gas Law
Ideal gas: non-interacting particles, $\Omega \propto V^N$. From the definition of pressure:
$$P = kT \frac{\partial \log \Omega}{\partial V} = NkT \frac{\partial \log V}{\partial V} = \frac{NkT}{V}$$
$$\boxed{PV = NkT}$$

- Fix $V$: pressure scales with $T$
- Fix $P$: gas expands with $T$; expansion does work $W = P\Delta V$, so temperature tends to drop
- Good approximation for dilute, non-polar, non-reactive gases (e.g. air)