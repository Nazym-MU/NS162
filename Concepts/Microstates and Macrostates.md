- The microstates are a **micro**scopic description of the possible **states** of the world.
	- always well defined
	- in an equilibrium, each microstate is equally likely
- The macrostates are the states of the world that are still distinguishable on the basis of the information we retain.
	- only well defined when the system is in the equilibrium
- Phase space – a set of all possibly physical states of the system described by a given parametrization

Microstates map onto macrostates

Rolling a dice gives us 36 microstates, but only 11 macrostates, corresponding to sums of 2 through 12.

Using binomial distribution:
```python
successes = list(range(n+1))
combinations = [comb(n,k) for k in successes]
```

Entropy: the universe is more likely to move towards more likely states.

There are too many atoms, so we think on logarithmic scales: $$S = k_B\ln \Omega$$$k_B = 1.38 \times 10^{-23} J/K, \Omega - \text{the number of microstates}, S - \text{entropy}$

The equilibrium probability distribution describing how energy is spread between the two systems is given by:
$$P_{eq}(E_A) \propto \Omega_A (E_A) \Omega_B(E_{AB} - E_A)$$
Or in terms of the entropy:
$$P_{eq}(E_A) \propto e^{S_A(E_A)/k_B}e^{S_B(E_{AB} - E_B)/k_B}$$
