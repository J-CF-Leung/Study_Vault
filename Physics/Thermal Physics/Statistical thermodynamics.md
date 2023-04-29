- [[Classical Thermodynamics]] is a _phenomenological_ study of systems with a large number of particles
- Statistical thermodynamics provides an _explanation_, by linking _microscopic behaviour_ with _observable quantities_


- For a system with an enormous number of particles, and thus, degrees of freedom, there is an immeasurable number of _microstates_
	- The number is denoted $\Omega$
- In _classical mechanics_, this _specifies position and velocity of every constituent particle_
- In _quantum mechanics_, it is the _multi-particle wave function_

- For thermodynamics to work, 2 fundamental suppositions must be made:
1. After a sufficiently long time, the _initial conditions become irrelevant_ as particles redistribute energy and momentum until equilibrium is reached
2. For a system _in equilibrium_, all possible microstates are equally likely 
	- [[Fundamental principles of statistical mechanics#The equal probabilities postulate]]

- A *macrostate* is defined by the _bulk properties_ of the system, and _incorporates many microstates_
		- The probability of a particular microstate, _given a macrostate_ is governed by the [[Fundamental principles of statistical mechanics#The statistical distribution function|statistical distribution function]]
- Macrostates are described by _thermodynamic variables_ such as $U, N, V, S, T, p, \mu$
- Macrostates with energy more or less _equally shared_ among particles become way more likely (way _more available mcirostates_)
	- Consequence of equal probabilities

- _Microstates_ can evolve _reversibly and deterministically with time_
- As time goes on, a _macrostate irreversibly tends to its mean_, which defines _statistical equilibrium_
	- This will later be characterised by the state variable of _entropy_
- The _final_ macrostate will tend to be one with _the most number of microstates_
	- Consequence of equal probabilities (the system spends the most time in the macrostate)

- If a sudden _change_ occurs to the system, the _set of available microstates_ changes

## Statistical view of temperature
- When two bodies are in _thermal equilibrium_, they must have the _same temperature_
- _Zeroth law_: if $A$  is in thermal equilibrium with $B$ and $C$, $B$ and $C$ are in thermal equilibrium with each other
	- i.e. The thermodynamic concept of temperature _"makes sense"_
- To understand definition of temperature, let there be 2 bodies in _thermal contact_ with small fluctuations
	- Can exchange $U$, but $N$ and $V$ remain fixed
	- Total microstates = $\Omega_1\Omega_2$
- The _most probable macrostate_ has a _maximum number of microstates_
- One can write:
$$\frac{d}{dU_1}(\Omega_1\Omega_2)=0$$
- From energy conservation $dU_1=-dU_2$:
$$\displaylines{\frac{1}{\Omega_1}\frac{d\Omega_1}{dU_1}-\frac{1}{\Omega_2}\frac{d\Omega_2}{dU_2}=0 \\\frac{d(\ln\Omega)}{dU}=\frac{1}{k_BT}}$$
- This quantity is _the same across two objects_. and $T$ is defined as the _temperature_
- Temperature scales can often be _arbitrary_

- This also defines another _state variable_: _Entropy_
	$$S=k_B\ln\Omega$$
	- $k_B=$ Boltzmann's constant
- A state of _maximum number of microstates_ has _maximum entropy_
