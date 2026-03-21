---
dg-publish: true
---
$$H \equiv E + PV$$

Differential (from $dE = T\,dS - P\,dV + \mu\,dN$):
$$dH = dE + P\,dV + V\,dP = T\,dS + V\,dP + \mu\,dN$$

$H = H(S, P, N)$. Maxwell relations:
$$\left(\frac{\partial H}{\partial S}\right)_{P,N} = T, \qquad \left(\frac{\partial H}{\partial P}\right)_{S,N} = V, \qquad \left(\frac{\partial H}{\partial N}\right)_{P,S} = \mu$$

Enthalpy is the constant-pressure analogue of energy: at constant $P$, $\Delta H = Q$.

---

### Heat capacities

$$C_V = \left(\frac{\partial Q}{\partial T}\right)_V = \left(\frac{\partial E}{\partial T}\right)_V \quad 	ext{(no work at constant }V	ext{)}$$

At constant $P$: gas must expand to maintain pressure, so work is done and energy goes down. Total energy change: $\Delta E = Q - P\Delta V$, so $\Delta H = Q$. Thus:
$$C_P = \left(\frac{\partial H}{\partial T}\right)_P$$

For monatomic ideal gas ($PV = Nk_BT$, $E = \frac{3}{2}Nk_BT$):
$$H = E + PV = \frac{5}{2}Nk_BT \implies C_P = \frac{5}{2}Nk_B$$

---

### Enthalpy in chemistry (constant $P$)

Chemistry and biology happen at constant $P$ (open containers, solutions, cells). Heat released in a reaction = $\Delta H$.

Three approaches to compute reaction enthalpy (best → worst):

1. **Standard enthalpy of reaction** $\Delta_r H^\circ$ — look it up directly (defined at reference conditions, e.g. 298 K, 1 atm)
2. **Enthalpies of formation + Hess's law** — $\Delta_r H^\circ = \sum \Delta_f H^\circ(	ext{products}) - \sum \Delta_f H^\circ(	ext{reactants})$; enthalpy of formation of an element in standard state = 0 by definition
3. **Bond enthalpies** — last resort; sum up enthalpies per bond type (tabulated for gases only, not reliable for liquids/solids)

Example — hydrogenation of ethene:
$$	ext{H}_2 + 	ext{C}_2	ext{H}_4 	o 	ext{C}_2	ext{H}_6, \qquad \Delta_r H^\circ = -136.3 	ext{ kJ/mol (exothermic)}$$
- Via formation enthalpies: $\Delta_r H^\circ = -84 - 52.4 = -136.4$ kJ/mol ✓
- Via bond enthalpies: $-124$ kJ/mol — close but not great (bonds aren't identical across molecules)

Hess's law: enthalpies are state functions, so they can be added and subtracted freely.

---

### Enthalpy vs energy: when does the difference matter?

$$\Delta H - \Delta E = \Delta(PV) \approx (\Delta n_	ext{gas})RT$$

where $\Delta n_	ext{gas}$ = change in moles of gas in the reaction.

- **Solids/liquids:** $\Delta(PV) \ll \Delta H$ (< 1%) — $H \approx E$
  - Example: aragonite → calcite, $\Delta(PV) \sim 10^{-4}$ kJ/mol vs $\Delta H = 0.21$ kJ/mol
- **Gases:** $\Delta(PV) \sim$ few % — can matter for reaction kinetics
  - Example: $3	ext{H}_2 + 	ext{N}_2 	o 2	ext{NH}_3$, $\Delta n = -2$, $\Delta(PV) = -4.9$ kJ/mol ≈ 5% of $\Delta H$
- Rule of thumb: $(\Delta n)RT \approx 2.48\,	ext{kJ/mol}$ per mole of gas change at room $T$