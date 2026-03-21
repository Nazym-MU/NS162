---
dg-publish: true
---
Generalizing from discrete to continuous variables in statistical mechanics requires moving from **counting microstates** to measuring **volumes in phase space**.

>**The process is:**
- Find Ω_p(E' < E) = volume of momentum space with energy less than E
- Take derivative: Ω_p'(E) = dΩ_p/dE = density at energy E
- This gives you states per unit energy
- Configuration space V^N just multiplies this result
---
### Calculating Density of States
**Step 1: Find cumulative volume** $$\Omega(s_{AB} < s_0) = \begin{cases} \frac{1}{2}s_0^2 & s_0 \leq 1 \\ 1 - \frac{1}{2}(1-s_0)^2 & s_0 > 1 \end{cases}$$
**Step 2: Take derivative to get density** $$\Omega'(s_0) = \frac{d\Omega(s_{AB} < s_0)}{ds_0}$$$$\Omega'(s_0) = \begin{cases} s_0 & s_0 \leq 1 \\ (1-s_0) & s_0 > 1 \end{cases}$$
### Probability Density
$$\rho(s_{AB}) = \frac{\Omega'(s_{AB})}{\Omega}$$
Result: $$\rho(s_{AB}) = \begin{cases} s_{AB} & s_{AB} \leq 1 \\ (1-s_{AB}) & s_{AB} \geq 1 \end{cases}$$
## Phase Space of Billiards Model
### Definition
**Phase space** = set of all possible positions $\vec{q}$ and momenta $\vec{p}$ of all particles
**Dimensions:**
- $N$ particles in $d$ dimensions → $2dN$-dimensional phase space
- 2D billiards with $N$ particles → $4N$ dimensions
- 3D gas with $N$ particles → $6N$ dimensions
### Density of States Formula
$$\Omega(E,V,N) = \omega_{d,N} \int_{H(\vec{p},\vec{q})=E} d^{dN}p , d^{dN}q$$
- $H(\vec{p},\vec{q})$ = Hamiltonian (total energy)
- $\omega_{d,N}$ = normalization constant
- Constraint: $H(\vec{p},\vec{q}) = E$ (energy shell)
### Factorization
For ideal gas (energy independent of position): $$\Omega(E,V,N) = \omega_{d,N} \Omega_p(E,N) \times \Omega_q(V,N)$$
**Configuration space** $\Omega_q$: $$\Omega_q(V,N) = V^N$$
- Each particle can be anywhere in volume $V$
- Probability all particles on left half: $(1/2)^N$
**Momentum space** $\Omega_p$:
- Energy constraint: $\sum_i \frac{|\vec{p}_i|^2}{2m} = E$
- This defines a hypersphere in momentum space
## Key Results
### 2D Billiards Model
$$\Omega(E, V=A, N) \approx \omega_{2,N}m\sqrt{2e}\left(\frac{2\pi e \times 2mE}{2N}\right)^{\frac{2N-2}{2}} A^N$$
### 3D Monatomic Ideal Gas
$$\Omega(E,V,N) \approx \omega_{3,N}m\sqrt{2e}\left(\frac{2\pi e \times 2mE}{3N}\right)^{\frac{3N-2}{2}} V^N$$
### Physical Interpretation
Energy spreads roughly evenly over all momentum components:
- Average energy per momentum component: $\sim E/2N$ (2D) or $E/3N$ (3D)
- $\Omega$ grows extremely rapidly with $E$ (scales as $E^{N}$)
## Important Concepts
### Volume vs Counting
- **Discrete systems**: Count individual microstates
- **Continuous systems**: Measure phase space volume
- Volume is proportional to number of states
### Energy Shell
- Constraint $H(\vec{p},\vec{q}) = E$ defines a surface in phase space
- Actually consider thin shell: $E < H < E + dE$
- Density: $\Omega'(E) = d\Omega/dE$
### Why This Matters
- Foundation for thermodynamics: $S = k\ln\Omega$
- Explains ideal gas law
- Shows how microscopic mechanics → macroscopic behavior