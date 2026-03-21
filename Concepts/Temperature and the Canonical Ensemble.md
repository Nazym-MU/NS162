Microcanonical ensemble only deals with isolated systems, but a canonical ensemble deals will closed (energy exchange can happen).
A canonical ensemble is a collection of replicas of a system all having fixed number of particles ($N$), volume ($V$), and temperature ($T$).
Microcanonical ensemble has constant $NVE$. Grand canonical ensemble $\mu VT$, where $\mu$ is the chemical potential of the particle.
$$\Omega_i(E) = \Omega_R(E-E_i)$$
$$\Omega(E) = \sum_i \Omega_i(E) = \sum_i \Omega_i(E-E_i)$$
Boltzmann definition of entropy:
$$S_R = k_B\ln\Omega_R(E-E_i) \approx k_B\ln\Omega_R(E) - \frac{\partial}{\partial E}(k_B\ln\Omega_R(E))E_i$$
where in the last step I used Taylor expansion. We know that $\frac{1}{T} = \frac{\partial S}{\partial E}$
$$=k_B\ln\Omega_R(E) - \frac{E_i}{T}$$
Hence, 
$$\Omega_R (E-E_i) = \Omega_R(E)e^{-E_i/k_BT}$$
Total number of microstates is the sum over $i$:
$$\Omega(E) = \Omega_R(E)\sum_ie^{-E_i/k_BT}$$
$$\Rightarrow p_i \propto e^{-E_i/k_BT}$$ $$\Rightarrow p_i = \frac{e^{-E_i/k_BT}}{\sum_j e^{-E_j/k_BT}} = \frac{e^{-E_i/k_BT}}{Z}$$where $Z$ is called the partition function: $Z = \sum_j e^{-E_j/k_BT}$