- Rigorous discussion w/ _derivations_: [[Classical Thermodynamics]]

# State variables and reversibility

## The first and second laws
- The _Second Law_ states that _any spontaneous process carries an increase in entropy_
- For an _infinitesimal process_, the change in entropy is:
$$dS=\frac{dq_\text{rev}}{T}$$
- $\dbar q_\text{rev}$ is the _heat under reversible conditions_
- For a reaction, one can separate the universe into the _system_ and the _surroundings_:
$$dS_\text{univ}=dS_\text{sys}+dS_\text{surr}$$

- The _First Law_ defines a state function, _internal energy_ $U$
- The differential is given by:
$$dU=\dbar q+\dbar w$$
- Here, $\dbar w$ is the work done _on_ the system
- $\dbar$ indicates that they are _path variables_, not state variables

- Linking to other state variables gives the _Master equation_, given _only in terms of state variables_
$$dU=TdS-pdV$$
- The _heat capacity at constant volume_ is defined as a partial derivative of $U$ w.r.t. $T$:
$$C_V=\left(\pd{U}{T}\right)_V$$
- Likewise, at _constant energy_, one gets:
$$\left(\pd{S}{V}\right)_U=\frac{p}{T}$$

## Thermodynamic functions

### Enthalpy
- One can define a new function, _enthalpy_:
$$\displaylines{H=U+pV \\ dH=T\,dS+V\,dp}$$
- From this, one can get that _$dH$ at constant pressure is equivalent to heat exchanged_

### Gibbs Free Energy
- If one considers breaking the universe into _system_ and _surroundings_, then consider the fact that _the surroundings are infinitely large_, hence _all heat exchanges are irrversible w.r.t. the surroundings_, hence:
$$dS_\text{surr}=-\frac{\dbar q_\text{sys}}{T}$$
- From this, one can define another thermodynamic function, the _Gibbs Free Energy_:
$$\displaylines{G=H-TS \\ dG=dH-T\,dS-S\,dT=V\,dp-S\,dT}$$
- Then, at _constant pressure and temperature_:
$$-\frac{dG_\text{sys}}{T}=dS_\text{sys}-\frac{\dbar q_\text{sys}}{T}=dS_\text{univ}$$
- From this, for a _spontaneous process at constant pressure and temperature_, $G$ _decreases_
- At _equilibrium_, $S$ is at a maximum and $G$ is at a minimum

### Helmholtz Free Energy
- The _Helmholtz Free Energy_ is defined as:
$$\displaylines{A=U-TS \\ dA=dU-T\,dS-S\,dT=-p\,dV-S\,dT}$$
- Following similar logic to above, at _constant volume and temperature_:
$$-\frac{dA_\text{sys}}{T}=dS_\text{sys}-\frac{dU}{T}=dS_\text{univ}$$
- From this, for a _spontaneous process at constant volume and temperature_, $A$ _decreases_

# Statistics and the Boltzmann distribution
- Detail: [[Statistical thermodynamics]]

## Microstates and macrostates
- For a system with an enormous number of particles, and thus, degrees of freedom, there is an immeasurable number of _microstates_
	- The number of microstates is denoted $\Omega$

- A *macrostate* is defined by the _bulk properties_ of the system, and _incorporates many microstates_
- Macrostates are described by _thermodynamic variables_ such as $U, N, V, S, T, p, \mu$
- For a macrostate with a particular $U$, there is a _very large number of microstates_ with different _distributions_ of energy among particles
- _Macrostates_ with energy more or less _equally shared_ among particles become way more likely (have _more microstates_)
	- Consequence of the equal probabilities postulate

- For thermodynamics to work, 2 fundamental suppositions must be made:
1. After a sufficiently long time, the _initial conditions become irrelevant_ as particles redistribute energy and momentum until equilibrium is reached
2. For a system _in equilibrium_, all possible microstates are equally likely 

- _Microstates_ can evolve _reversibly and deterministically with time_
- As time goes on, a _macrostate irreversibly tends to its mean_, which defines _statistical equilibrium_
- The _final_ macrostate will tend to be one with _the most number of microstates_
	- Consequence of the equal probabilities postulate, as the system _spends much more time_ in that macrostate

## Entropy
- The Boltzmann definition of entropy is:
$$S=k_B\ln\Omega$$
- Here, $\Omega$ is the _number of microstates_

- If two sub-systems $A,B$ have $\Omega_A$ and $\Omega_B$ microstates respectively, then $\Omega_\text{tot}=\Omega_A\Omega_B$
- Then, the entropy is _additive_: $S=S_A+S_B$

- Consider a system going from an _initial macrostate_ with $\Omega_\text{i}$ to a _final macrostate_ with $\Omega_\text{f}$
- The _ratio of probabilities_ for finding the system in the corresponding microstates is:
$$\begin{aligned}\frac{P_f}{P_i}=\frac{\Omega_f}{\Omega_i} =\exp(-\Delta S/k)\end{aligned}$$
- For $\sim1$ moles of gas, this would be the order of $\exp(-N_A)$

## The Boltzmann distribution
- In chemistry, one usually considers a system _in thermal equilibrium with surroundings_
- This can be considered a small system _able to exchange energy with a much larger reservoir at constant temperature_

# The partition function

# Internal energy and heat capacity

# Entropy

# Nuclear spin statistics

# Chemical equilibrium

# Kinetics

