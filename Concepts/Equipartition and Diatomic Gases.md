Each quadratic degree of freedom in the energy contributes $\frac{1}{2}k_BT$ to the average energy.

For a monatomic ideal gas: 3 translational DOF $\rightarrow$ $\langle E \rangle = \frac{3}{2}k_BT$

### Diatomic molecules
A diatomic molecule has additional rotational modes. The principal axes of a diatomic molecule:
- 2 rotational DOF with $I > 0$ (axes perpendicular to the bond)
- 1 axis with $I = 0$ along the bond — does **not** contribute (quantum effect: energy spacing too large to excite at typical temperatures)

Total DOF: 3 translational + 2 rotational = 5
$$\langle E \rangle = \frac{5}{2}k_BT$$

### Molar heat capacity
At constant volume, $C_V = \frac{\partial \langle E \rangle}{\partial T}$ per mole. Using $k_B \rightarrow R$ (per mole):

- Monatomic: $C_V = \frac{3}{2}R$
- Diatomic (no vibration): $C_V = \frac{5}{2}R$
- Diatomic (with vibration): $C_V = \frac{7}{2}R$ — vibrational mode adds 2 DOF (kinetic + potential)

Vibration only activates at high temperatures. At room temperature, diatomic gases behave as if $C_V = \frac{5}{2}R$.

### Connection to partition function
For a diatomic gas, the partition function factorizes:
$$Z = Z_\mathrm{trans} \cdot Z_\mathrm{rot} \cdot Z_\mathrm{vib}$$

Average energy from partition function:
$$\langle E \rangle = -\frac{\partial \ln Z}{\partial \beta}, \quad \beta = \frac{1}{k_BT}$$

Each independent quadratic DOF contributes a factor of $\sqrt{\pi/\beta}$ to $Z$, and $\frac{1}{2}k_BT$ to $\langle E \rangle$ — recovering equipartition.

### Quantum reason for low-temperature disagreement
Equipartition is a classical result — it assumes energy is continuous. Quantum mechanics says each mode has discrete energy levels. For a vibrational mode:
$$E_k = \hbar\omega\left(k + \frac{1}{2}\right), \quad k = 0, 1, 2, \ldots$$

A mode contributes $\frac{1}{2}k_BT$ only if it can be thermally excited, i.e. $k_BT \gg \hbar\omega$. If $k_BT \ll \hbar\omega$, the system lacks enough energy to reach the first excited state — the mode is **frozen out** and contributes nothing.

This defines a characteristic temperature for each mode:
$$\Theta = \frac{\hbar\omega}{k_B}$$

- $T \ll \Theta$: mode frozen, no contribution to $C_V$
- $T \gg \Theta$: mode fully active, classical equipartition recovered

For diatomic molecules, $\Theta_\mathrm{vib} \gg \Theta_\mathrm{rot} \gg \Theta_\mathrm{trans}$, which is why modes activate at different temperatures. This is why $C_V$ is experimentally observed to rise in steps as $T$ increases, rather than being constant as classical equipartition predicts.