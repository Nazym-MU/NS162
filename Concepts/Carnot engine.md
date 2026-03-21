## Heat Engines
A **heat engine** converts thermal energy into mechanical work by cycling a working body between a hot bath ($T_H$) and cold bath ($T_C$).

**Carnot cycle** (4 steps):
1. Contact with hot bath → isothermal expansion at $T_H$, absorbs $Q_H$
2. Isolated → adiabatic expansion, temperature drops to $T_C$
3. Contact with cold bath → isothermal compression at $T_C$, expels $Q_C$
4. Isolated → adiabatic compression, temperature returns to $T_H$

Key quantities: $Q_H = T_H \Delta S_H$, $Q_C = T_C \Delta S_C$, net work $W = Q_H - Q_C$

## Efficiency & Carnot's Theorem
$$\eta \equiv \frac{W}{Q_H} = 1 - \frac{Q_C}{Q_H} = 1 - \frac{T_C \Delta S_C}{T_H \Delta S_H}$$

Second law requires $\Delta S_C \geq \Delta S_H$, so:
$$\boxed{\eta \leq 1 - \frac{T_C}{T_H}}$$

This is **Carnot's theorem** — an absolute upper bound on efficiency for *any* heat engine, regardless of design or working body. To be efficient: maximize $T_H$, minimize $T_C$.

Running the cycle in reverse → **heat pump** (refrigerator/AC): work is put in to move heat from cold to hot.

## Free Energy
Working body with energy $E$, entropy $S$, next to a single heat bath at $T$. Maximum extractable work:
$$W_	\text{max} = E - T(S - S_0)$$

Setting $S_0 = 0$ (conventional in thermodynamics):
$$W_	\text{max} = E - TS = F \quad \text{(Helmholtz free energy)}$$

$F$ is the energy "free" to do work — the rest is locked up as entropy. The colder the heat bath, the more work you can extract.
Ideally, we would like the maximum amount of work we can extract from the body to be E. We want to extract _all_ the energy as work. But the second law makes that impossible. As the body’s energy decreases, its entropy does too. We need to make up for that by adding heat (and entropy) to the heat bath.