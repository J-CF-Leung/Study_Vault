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

## Temperature
- Temperature is a variable _only defined at thermal equilibrium_
- A _statistical definition_: [[Statistical thermodynamics#Statistical view of temperature]]
$$\begin{aligned}\frac{1}{k_BT}&=\frac{d(\ln\Omega)}{dU} \\ T&=\left(\pd{U}{S}\right)_V\end{aligned}$$

## The Boltzmann distribution
- In chemistry, one usually considers a system _in thermal equilibrium with surroundings_
- This can be considered a small system _able to exchange energy with a much larger reservoir at constant temperature_

- Let the _energy including the reservoir_ be $E_\text{tot}$, and energy _of the system_ be $E_i<<E_\text{tot}$
- The _probability_ that the system has energy $\varepsilon$ is _proportional to the number of microstates of the reservoir_
- Using this fact, and doing a Taylor expansion:
$$\displaylines{\ln\Omega(E_\text{tot}-E_i)\approx\ln\Omega(E_\text{tot}) -E_i\frac{d\ln\Omega}{dE_\text{tot}}=\ln\Omega(E_\text{tot})-\frac{E_i}{k_BT} \\ P(E_i)\propto\exp\left(-\frac{E_i}{k_BT}\right)}$$
- The exponential $\exp(-E_i/k_BT)$ is known as the _Boltzmann factor_

- Using the fact that the probability is _normalised_:
$$\displaylines{P(E_i)=\frac{1}{Q_N}\exp\left(-\frac{E_i}{k_BT}\right) \\ Q_N=\sum_i\exp\left(-\frac{E_i}{k_BT}\right)}$$
- $Q_N$ is known as the _partition function_ of the system

- This expression for probability applies to the _microstate_ of the _entire system_
- It applies to _molecular energy levels if and only if_ the particles _do not interact_ (the energies are _independent_ of each other) 

# The partition function
- For a system with energy levels $\{E_i\}$, the _partition function_ $Q_N$ is:
$$Q_N=\sum_i\exp\left(-\frac{E_i}{k_BT}\right)$$

## Thermodynamic functions in terms of partition function
- The _internal energy_ $U$ is written as:
$$U=\sum_i P_iE_i=\frac{1}{Q_N}\sum_iE_i\exp\left(-\frac{E_i}{k_BT}\right)=k_BT^2\left(\pd{\ln Q_N}{T}\right)_V$$
- Thus, internal energy _can be derived from the partition function_

- Meanwhile, _entropy_ $S$ can be written as:
$$S=\frac{U}{T}+k_B\ln{Q_N}=k_BT\left(\pd{\ln Q_N}{T}\right)_V+k_B\ln Q_N$$
- This is proven from _another definition of entropy_, given [[Statistical thermodynamics|here]]
- From this, one can derive the expression for _Helmholtz Free Energy_ $A$:
$$A=-k_BT\ln{Q_N}$$
## Multi-particle systems
- In almost all cases, the system considered is one with _many particles_, each with _their own degrees of freedom and energy levels_

### Non-interacting, distinguishable particles
- If the energies of the particles are _independent of each other_:
$$E_\text{sys}=\varepsilon_i^{(A)}+\varepsilon_j^{(B)}+\varepsilon_k^{(C)}+\dots$$
- The _subscript_ is the _state of the particle_, while the _superscript_ is the _particle index_
- This is generally _only applicable to gases_

- Then, the _partition function_ becomes:
$$Q_N=\sum_{i,j,k,\dots}\exp\left(-\frac{E_{\text{sys},i,j,k\dots}}{k_BT}\right)=\prod_\text{particles}\sum_i\exp\left(-\frac{\varepsilon_i}{k_BT}\right)=\prod_\text{particles}q$$
- Here, $q$ is the _molecular partition function_:
$$q=\sum_i\exp\left(-\frac{\varepsilon_i}{k_BT}\right)$$
- If there are $N$ _molecules with identical energy levels_:
$$Q_N=q^N$$

### Indistinguishable particles
- If the particles are _identical_, then for _every microstate with identical populations of each energy level_ will be the _same_
- For this reason, the partition function in this case is the one for _distinguishable particles_, _divided_ by the number of permutations:
$$Q_N=\frac{q^N}{N!}$$
- This generally applies to _molecules and atoms of the same type_
- This _does not apply to solids_, as the _lattice sites_ are distinguishable

## Effect of temperature and accessible states
- Express the energy levels in terms of difference from the _ground state_ energy $\varepsilon_0$:
$$\displaylines{\varepsilon_i=\varepsilon_0+\Delta_i \\ \begin{aligned}q&=\exp\left(-\frac{\varepsilon_0}{kT}\right)\left[1+\exp\left(-\frac{\varepsilon_1}{kT}\right)+\exp\left(-\frac{\varepsilon_2}{kT}\right)+\dots\right]\\&=\exp\left(-\frac{\varepsilon_0}{kT}\right)q' \\ q'&=1+\exp\left(-\frac{\varepsilon_1}{kT}\right)+\exp\left(-\frac{\varepsilon_2}{kT}\right)+\dots\end{aligned} \\ }$$
- For _high temperatures_, where $\Delta_i<<kT$, the _Boltzmann factors are nearly all $1$_
	- _All levels_ are roughly _equally populated_
	- Therefore, $q'\approx N$
- For _low temperatures_, where $\Delta_i>>kT$, the _Boltzmann factors nearly vanish_
	- Only the _ground state_ contributes significantly
	- Therefore, $q'\approx 1$

- Therefore, $q'$ is known as _the number of accessible states_
	- It is _roughly equal_ to the number of states that are _significantly populated_

### Approximation via integration
- Let the energy levels be some _function of a variable_ $i$:
$$\displaylines{\epsilon(i)=\epsilon_0+\Delta(i) \\ \\ q'=\sum_{i=0}^\infty \exp\left(-\frac{\Delta(i)}{k_BT}\right)}$$
- If the _temperature is high_, $k_BT>>\Delta(i)$, then the error from converting from a sum to integration becomes _less significant_:
$$q'\approx\int_0^\infty \exp\left(-\frac{\Delta(i)}{k_BT}\right)\,di \hspace{0.5cm}\text{ assuming } k_BT>>\Delta(i)$$
- This necessitates that $q'>>1$

## Thermodynamic quantities for multiple particles

### Distinguishable particles
- Using the expressions above:
$$\displaylines{\begin{aligned}Q_N&=q^N \\ \\ A&=-kT\ln Q_N \\ &=-NkT\ln q \\ \\ S&=-\left(\pd{A}{T}\right)_V \\ &=Nk\ln q+NkT\left(\pd{\ln q}{T}\right)_V \\ \\ U&=kT^2\left(\pd{\ln Q_N}{T}\right)_V \\ &=NkT^2\left(\pd{\ln q}{T}\right)_V\end{aligned}}$$
- This verifies the fact that $A,S,U$ are _extensive properties_, as they _scale with the number of particles_

### Indistinguishable particles
- For this, one needs to use _Stirling's approximation_:
$$\ln N!\approx N\ln N-N$$
- Using the expressions above:
$$\begin{aligned}Q_N&=\frac{q^N}{N!} \\ \\ A&=-kT\ln Q_N \\ &=-NkT\ln q+kT(N\ln N-N) \\ \\ S&=-\left(\pd{A}{T}\right)_V \\ &=Nk\ln q-Nk\ln N+Nk+NkT\left(\pd{\ln q}{T}\right)_V \\ \\ U&=kT^2\left(\pd{\ln Q_N}{T}\right)_V \\ &=NkT^2\left(\pd{\ln q}{T}\right)_V\end{aligned}$$
- Only _internal energy_ remains the same
- The additional terms in $A$ and $S$ represent a _loss in configurational entropy_ as there are _fewer microstates_

## Choice of energy zero
- Sometimes, one may want to express energies _relative to a ground state_, with energy $\varepsilon^0$:
$$\varepsilon_i'=\varepsilon_i-\varepsilon^0$$
- In this case, the partition function _gains a multiplicative factor_:
$$q=q'\exp\left(-\frac{\varepsilon^0}{k_BT}\right)$$
- The effect on _internal energy_ is:
$$U=NkT^2\left(\pd{\ln q}{T}\right)_V=NkT^2\left(\pd{\ln q'}{T}\right)_V+N\varepsilon^0$$
- The internal energy is simply _shifted_ by $N\epsilon^0$, since _nothing about the system itself has changed_, only the _reference energy_
- $N\epsilon^0$ can be identified as _the energy of the system at absolute zero_

- The _Helmholtz free energy_ has the same _corrective term_:
$$A=-NkT\ln q'+kT(N\ln N-N)+N\varepsilon^0$$

- Meanwhile, _entropy is unchanged_:
$$S=Nk\ln q'-Nk\ln N+Nk+NkT\left(\pd{\ln q'}{T}\right)_V$$
- This is expected as _choice of reference energy does not influence disorder_

## Degeneracy
- Many systems show _degeneracy_, where _distinct wave functions have the same energy_
	- Example: _multi-dimensional_ particle in a box, or harmonic oscillator

- The previous expression for partition function is a _sum over states_, so it still holds

- However, it is often evaluated as a _sum over energies_
- In this case, if energy $\varepsilon_j$ has _degeneracy_ $g_j$:
$$q=\sum_{\text{states }i} \exp\left(-\frac{\varepsilon_i}{k_BT}\right)=\sum_{\text{energies }j}g_j\exp\left(-\frac{\varepsilon_j}{k_BT}\right)$$
- In this case, the _number of accessible levels_ is still valid, as _degenerate levels are still distinct_

# Calculating the partition function

## Multiple degrees of freedom


# Internal energy and heat capacity

# Entropy

# Nuclear spin statistics

# Chemical equilibrium

# Kinetics
