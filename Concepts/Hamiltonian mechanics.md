---
dg-publish: true
---
[[Phase space]] - space described by all these generalized positions and momenta.
Hamiltonian in terms of Lagrangian:
$$\frac{\partial L}{\partial \dot q} = p$$
Hamiltonian as a function of generalized positions q and generalized momenta p:
$$H(q, p), \quad q=\{ q_1, ..., q_n\}, \quad p = \{p_1, ..., p_n\}$$
Hamilton's equations give $2n$ coupled 1st order equations. Euler-Lagrange equations give $n$ 2nd order equations.
$$\dot q_i = \frac{\partial H}{\partial p_i} =f_i(q, p), \qquad \dot p_i = -\frac{\partial H}{\partial q_i} =g_i(q, p)$$
$z(q, p) = \{ q_1, ..., q_n, p_1, ..., p_n \}$ <- point in phase space
$$\dot z(q, p) = h(q, p) = \{f_1, ..., f_n, g_1, ..., g_n \}$$
apply the Hamiltonian.

Starting with initial conditions $z_0$, this trajectory is unique => no trajectories can cross.
**Proof:** Assume two trajectories do cross at point $z'$. Then if $z'$ were an initial condition, then it would have two or more trajectories. This violates uniqueness. This implies that orbits do not cross at any point in time.

Motion in phase space: Any point that starts in $A$, ends up in area $A(t)$ at a later time $t$. Neighborhoods in phase space will remain connected for all time. This means that we can simply look at the trajectory of $A$, rather than of each individual $z$.
**Proof:** Assume that point $b$ doesn't end up in $A(t)$ later. The trajectory of $b$ will cross the trajectory of at least one point in $A$. This violates unique.

It is true that the term $p\dot q = 2K$ (twice the kinetic energy, according to gemini) 
[[Liouville theorem]]
