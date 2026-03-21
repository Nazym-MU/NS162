---
dg-publish: true
---
## First Law of Thermodynamics
$$\Delta U = Q - W$$
- $\Delta U$: change in internal energy
- $Q$: heat absorbed by system (+) / lost by system (−)
- $W$: work done by system (+) / done on system (−)

## Thermodynamic Processes

| Process | Condition | Simplification |
|---|---|---|
| Isovolumetric | $\Delta V = 0$ | $W = 0$, so $\Delta U = Q$ |
| Isothermal | $\Delta T = 0$ | $\Delta U = 0$, so $Q = W$ |
| Adiabatic | $Q = 0$ | $\Delta U = -W$ |
| Isolated | $Q = 0$, $W = 0$ | $\Delta U = 0$ |

## Sign Conventions
- $Q > 0$: heat flows **into** system
- $W > 0$: work done **by** system (expansion)
- $W < 0$: work done **on** system (compression)

## Microscopic Picture
Internal energy as a sum over microstates: $U = \sum_i p_i E_i$

Total differential:
$$dU = \sum_i E_i \, dp_i + \sum_i p_i \, dE_i$$
$$dU = \mathit{đ q} + \mathit{đ w}$$

- $đq = \sum_i E_i \, dp_i$ — **heat**: change probabilities $p_i$, keep energy levels $E_i$ fixed
- $đ w = \sum_i p_i \, dE_i$ — **work**: change energy levels $E_i$ (e.g. by compression), keep $p_i$ fixed

$đq$ and $đw$ are **inexact differentials** — unlike $dU$, their integrals depend on the path taken between states, not just the endpoints. Heat and work are not state functions; only their sum is.