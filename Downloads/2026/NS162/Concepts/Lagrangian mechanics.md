- describes the motion and dynamics of systems using **energies** rather than forces
- based on the **principle of stationary action**: the path a physical system takes is the one for which action is stationary. 
$$L = T - V$$
T – kinetic, V – potential
### Key concepts
- The Lagrangian ($L$):
	- unlike the total energy ($T + V$) used in Hamiltonian mechanics, the Lagrangian is the difference in energies.
- **Action ($A$):** a quantity that defines a specific trajectory through space and time
	- integral over time of the Lagrangian along a given path: $A = \int_{t_1}^{t_2} L dt$.
- Principle of Stationary Action: [[Principle of Least Action]]
	- the actual trajectory a system follows is the one where the action is stationary (functional differential is zero, $\delta A = 0$)
- Euler-Lagrange Equation (Lagrangian version of Newton’s second law ($F=ma$): $$\frac{d}{dt}\frac{\partial L}{\partial \dot x}=\frac{\partial L}{\partial x}$$

### Advantages Over Newtonian Mechanics
- scalar quantities (less directions to track)
- generalized coordinates: freedom in choosing coordinate systems
- forces of constraint, e.g., pendulum moving in a circle
- Look at the degrees of freedom: tells how many Euler-Lagrange equations there are
- step by step: find coordinates, define the Lagrangian, apply the EL equations, solve the differential equations
- Noether's theorem -> identify the conservation laws, symmetries of the system