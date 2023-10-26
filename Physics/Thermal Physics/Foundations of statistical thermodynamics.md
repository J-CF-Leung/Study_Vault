- [[Classical Thermodynamics]] is a _phenomenological_ study of systems with a large number of particles
- Statistical thermodynamics provides an _explanation_, by linking _microscopic behaviour_ with _observable quantities_

# Describing a system

## Microstates and macrostates
- For a system with an enormous number of particles, and thus, degrees of freedom, there is an immeasurable number of __microstates__

- In _classical mechanics_, this _specifies position and velocity of every constituent particle_
- In _quantum mechanics_, it is the _multi-particle wave function_
- _Microstates_ can evolve _reversibly and deterministically with time_

- For thermodynamics to work, 2 fundamental suppositions must be made:
1. After a sufficiently long time, the _initial conditions become irrelevant_, as particles redistribute energy and momentum until equilibrium is reached
2. For a system _in equilibrium_, all possible microstates are equally likely
	- [[Principles of statistical mechanics#The equal probabilities postulate]]
	- This means eventually, the system will have _explored all possible microstates_

- A __macrostate__ is defined by the _bulk properties_ of the system, and _incorporates many microstates_
- Macrostates are described by [[Chemical thermodynamics#State variables and reversibility|state variables]] such as $U, N, V, S, T, p, \mu$
	- _Extensive variables_ $U,N,V,S$ will _scale with_ the system
	- _Intensive variables_ $T,p,\mu$ will _remain constant_ when scaling the system
- Macrostates with energy more or less _equally shared_ among particles become way more likely (way _more available microstates_)
	- Consequence of equal probabilities
	- From the _central limit theorem_, the _mean_ of a quantity (such as energy) is close to its _median_ (value for the _most common microstate_)

## Statistics, density of states, and ensembles
- The _number of microstates_ with energy $E$, _given a macrostate_ is given by a function $\Omega(E)$
	- It is _purely a function of energy_
	- Sometimes called the [[Principles of statistical mechanics#The statistical distribution function|statistical distribution function]]

- For a system with _discrete energy levels_, $\Omega$ is simply the _number of microstates_ with energy $E$

- For a system with a _continuous spectrum of energy_, define the _density of states_ $g(E)$, where $\Omega(E)$ gives the number of microstates in the _range_ of energies $E$ to $E+\delta E$:
$$\Omega(E)=g(E) \delta E$$
- The _spread_ in energy is often estimated from the [[Fundamental concepts of quantum mechanics#Energy-time uncertainty principle|energy-time uncertainty principle]], and is typically in the order of $10^{-24}\,\text{J}$

- The probability of being in a microstate is obtained from _sampling the system at various times_, with the _collection_ of samples being titled the _ensemble_

- The ___microcanonical ensemble___: a system is _isolated_, with _fixed energy_
	- Discrete energy levels: $\rho(E)=1$ for $E=E_0$, 0 everywhere else
	- Continuous energy levels: $\rho(E)=\delta(E-E_0)$

- The ___canonical ensemble___: a _small subsystem_, with a _fixed number of particles_, within a _much larger_ system of _constant temperature_
	- In other words, a system is _connected to a temperature "bath"_, with which it can _exchange energy but not particles_
	- For a given energy of the _subsystem_, $E$, the number of _microstates_ available is not uniform, hence $\rho(E)$ is _not constant_
	- $\rho(E)$ is given by the [[#Boltzmann Distribution]]

- The ___grand canonical ensemble___: a _small subsystem_, within a _much larger_ system of _constant temperature_
	- A system is connected to a _temperature bath_, with which it can _exchange both energy and particles_

## Irreversibility
- As time goes on, a _macrostate irreversibly tends to its mean_, which defines _statistical equilibrium_
	- This is characterised by the state variable of _entropy_
- The _final_ macrostate will tend to be one with _the most number of microstates_
	- Consequence of equal probabilities (the system spends the most time in that macrostate)
	- There will be [[Principles of statistical mechanics#Fluctuations|fluctuations]] in that macrostate that reduce as the _number of particles_ grows

- If a sudden _change_ occurs to the system, the _set of available microstates_ changes
	- If there are _significantly more microstates_ than before, then the change is _irreversible_, as it becomes incredibly _unlikely_ for the previous microstates to be occupied

# Statistical view of temperature
- When two bodies are in _thermal equilibrium_, they must have the _same temperature_
- [[Classical Thermodynamics#The zeroth law and equations of state|Zeroth law]]: if $A$  is in thermal equilibrium with $B$ and $C$, $B$ and $C$ are in thermal equilibrium with each other
	- i.e. The thermodynamic concept of temperature _"makes sense"_
- To understand temperature _from the P.O.V. of statistics_, let there be 2 bodies in _thermal contact_ with small fluctuations
	- Can exchange $U$, but $N$ and $V$ remain fixed
	- Total microstates = $\Omega_1\Omega_2$
- The _most probable macrostate_ has a _maximum number of microstates_
- One can write:
$$\frac{d}{dU_1}(\Omega_1\Omega_2)=0$$
- From energy conservation $dU_1=-dU_2$:
$$\displaylines{\frac{1}{\Omega_1}\frac{d\Omega_1}{dU_1}-\frac{1}{\Omega_2}\frac{d\Omega_2}{dU_2}=0 \\\frac{d(\ln\Omega)}{dU}=\beta\equiv \frac{1}{k_BT}}$$
- This quantity is _the same across two objects_. and $T$ is defined as the _temperature_
- Temperature scales can often be _arbitrary_

- This also defines another _state variable_: _Entropy_
	$$S=k_B\ln\Omega$$
	- $k_B=$ Boltzmann's constant
- A _macrostate of maximum number of microstates_ has _maximum entropy_
- This is applicable for a _macrostate of fixed energy_ or in the [[#Statistics, density of states, and ensembles|microcanonical ensemble]]
- This forms a "bridge" to [[Classical Thermodynamics#State variables|Classical Thermodynamics]] as it matches the definition of $S$ via the Master Equation:
$$\frac{1}{T}=\left(\pd{S}{U}\right)_{V,N}$$
- This is most applicable to _large systems_, with a _large density of states_ as the system is allowed to exchange _infinitesimal_ energy
	- For smaller systems, use [[#Definition of Gibbs Entropy|Gibbs entropy]]

# Boltzmann Distribution

- Consider the _canonical ensemble_
- Given that the _system plus reservoir_ are in the _macrostate of fixed energy_ $E$, find the probability that the _system is in a microstate_ with energy $\epsilon$
![[Canonical ensemble.png]]

## The Boltzmann Factor
- The _probability_ of the system having energy $\epsilon$ is _proportional to the number of microstates of the reservoir_ $\Omega(E-\epsilon)$
- Then, using a _Taylor expansion_ of $\ln\Omega(E)$:
$$\ln\Omega(E-\epsilon)\approx \ln\Omega(E)-\epsilon\frac{d\,\ln\Omega}{dE}=\ln\Omega(E)-\beta\epsilon$$
- The _first order_ approximation is only valid for $\ln\Omega$, for a _large reservoir_ where $E>>\epsilon$

- Hence, the _probability_ of the system being at energy $\epsilon$ is proportional to:
$$P(\epsilon)\propto\exp(-\beta\epsilon)=\exp\left(-\frac{\epsilon}{k_BT}\right)$$
- The exponential is known as the _Boltzmann factor_

- As more energy is transferred _out of the reservoir_, the number of microstates _shrinks_
- The _most likely microstate_ is where the system is in the _ground state_

## The Partition Function
- Then, one needs to _normalise_ the distribution:
$$P(E_i)=\frac{\exp(-\beta E_i)}{\sum_j \exp(-\beta E_j)}\equiv\frac{\exp(-\beta E_i)}{Z}$$
- $Z$ is known as the _partition function_ of the system:
$$Z=\sum_i \exp\left(-\frac{E_i}{k_BT}\right)$$

- If a particular energy level is _degenerate_, with degeneracy $g_i$:
$$\displaylines{P(E_i)=\frac{g_i\exp(-\beta E_i)}{\sum_j g_j\exp(-\beta E_j)}\equiv g_i\frac{\exp(-\beta E_i)}{Z} \\ Z=\sum_i g_i \exp\left(-\frac{E_i}{k_BT}\right)}$$

- Example: A _two-state_ system with energies $0$ and $\epsilon$, occupied by _one particle_:
$$Z=1+\exp\left(-\frac{\epsilon}{k_BT}\right)$$

## Energy and heat capacity
- The _internal energy_ of a macroscopic body is the _statistical average_ over the microstates:
$$U=\sum_\text{states} p_i E_i=\frac{1}{Z}\sum_i E_i\exp\left(-\frac{E_i}{k_BT}\right)=\frac{\sum_i E_i\exp(-\beta E_i)}{\sum_j \exp(-\beta E_j)}$$
- This can be written as:
$$U=-\frac{1}{Z}\frac{dZ}{d\beta}=-\frac{d\ln Z}{d\beta}$$

- Then, one can write the _heat capacity_ as:
$$C_V=\left(\pd{U}{T}\right)_V$$

### Example: Harmonic oscillator
- Example: A single particle modelled by the _harmonic oscillator_:
$$E_n=\left(n+\frac{1}{2}\right)\hbar\omega$$
- Taking the _ground state_ as zero energy:
$$Z=1+\exp(-\beta\hbar\omega)+\exp(-2\beta\hbar\omega)+\dots=\frac{1}{1-\exp(-\beta\hbar\omega)}$$
- Then, calculating the internal energy:
$$U=-\frac{1}{Z}\frac{dZ}{d\beta}=\frac{\hbar\omega}{\exp(\beta\hbar\omega)-1}$$
- At _low temperatures_, $\hbar\omega>>kT$, then $U\approx \hbar\omega\exp(-\beta\hbar\omega)$
	- The _energy spacing_ is much larger than $kT$
	- The _first excited state_ is rarely occupied
- At _high temperatures_, $\hbar\omega<<kT$, then $U\approx kT$
	- This is the _equipartition value_

- The _heat capacity_ tends to _zero_ for low temperartues
	- There is only a _slight chance_ that the particle gets up to the first excited state
- The _heat capacity_ tends to $k$ for high temperatures

## The classical limit: equipartition
- Consider classical dynamics, where some _continuous variable_ $u_i$ contributes a _quadratic term_ to energy:
$$E_i=\alpha u_i^2$$
- Their contributions to internal energy are _additive_
- Assuming states are _evenly spaced_ in $u_i$, then each _contribution_ is:
	$$U_i=\frac{\int \alpha u_i^2 \exp(-\beta \alpha u_i^2)\,du_i}{\int \exp(-\beta \alpha u_i^2)\,du_i}=\frac{1}{2\beta}=\frac{kT}{2}$$
	- If evaluating _total energy_, integrating over $du_1du_2\dots du_N$, the integrals separate

- Hence, if energy has $N_t$ _quadratic terms_ in any coordinate or velocity, then:
$$U_\text{tot}=\frac{N_tkT}{2}$$
- For a system with _quantised energy levels_, at _high temperatures_ (where $kT$ is much larger than the _spacing_), the internal energy reaches the _equipartition limit_

### Heat capacity of a diatomic gas
- The _translational energy levels_ can be obtained from the particle in a box, and are often _very small compared to $kT$_
- Hence, at _low temperatures_, $U\approx 3kT/2$ per particle
	- For a _monoatomic gas_, this is true for _all temperatures_

- At _higher temperatures_, the _rotational modes_ start being "activated", and $U\approx 5kT/2$
	- Typical value for _diatomics at room temperature_

- At _even higher temperatures_, the _vibrational modes_ are involved, and $U\approx 7kT/2$

# Entropy
- For a system of energy $U$, the _entropy associated with the number of microstates_ $\Omega$ is:
$$S=k_B\ln\Omega(U)$$
- For actual systems, like the [[#Boltzmann Distribution|canonical ensemble]], the system can be in _macrostates of different energy and entropy_

- The _total entropy_ of the system is associated with the _total number of microstates_ $N$:
$$S_\text{tot}=k_B\ln N$$
- It can be broken into _two parts_:
	- Entropy associated with the _freedom to choose macrostates_
	- Entropy associated with the _freedom to choose microstates within the macrostates_
$$S_\text{tot}=S+S_\text{micro}$$

## Gibbs formula for Entropy
- For each _macrostate_ $i$, let there be $n_i$ _microstates_
$$\sum_i n_i=N$$
- Then since _all microstates are equally probable_, define the _probability_ of finding the system in the $i$th macrostate as:
	$$P_i=\frac{n_i}{N}$$
	- It is often an _unmeasurable quantity_
	- Formally, it is the probability of finding the state within a _statistical ensemble_ of $N$ systems
- The entropy _associated with the microstates_ is then:
$$S_\text{micro}=\sum_i P_iS_i=k_B\sum_i P_i\ln n_i$$
- Carrying out the subtraction, one finds the _Gibbs formula_ for $S$:
$$S=-k_B\sum_i P_i\ln P_i$$

### In the microcanonical ensemble
- In the [[#Statistics, density of states, and ensembles|microcanonical ensemble]] with $\Omega$ states, they are _equally probable_, hence $P_i=1/\Omega$
- The entropy _associated with choosing between these states_ is then:
$$S=-k_B\sum_i\frac{1}{\Omega}\ln\frac{1}{\Omega}=k_B\ln\Omega$$

## Connection to classical thermodynamics
- In [[Classical Thermodynamics#The second law and entropy|classical thermodynamics]], a _change in entropy_ is defined as:
$$dS=\frac{\dbar Q_\text{rev}}{T}$$
- Considering the [[Classical Thermodynamics#The first law, internal energy, and heat|first law]], and the formula for $U$ in terms of the _energies and probabilities of the constituent states_:
$$dU=\dbar Q+\dbar W=d\left(\sum_i P_iE_i\right)$$
- Consider _reversible processes_ with either _no work done_, or _no heat transfer_
![[Heat and work for states.png]]
- Heat can be seen as _increasing occupancy_ of higher states _without changing their energies_
- Work can be seen as _changing energies of each state_ while _not changing occupancy_

- As entropy is _purely associated with microstate probabilities_, only _heat transfer_ can increase it

## Deriving the Boltzmann Distribution
- In the _canonical ensemble_, the system, connected to a reservoir of temperature $T$, has freedom to be in _many macrostates of different energies_ $E_i$
	- Each macrostate has a _different number of total microstates_ for the combined system of the reservoir and the system
- There is some _statistical distribution_ of macrostates, which gives the _maximum entropy_
- There is a _statistical average_ of energy, $\mean{E}=U$

- Given a state of energy $E_i$ has probability $P_i$, the system is subject to _constraints_:
$$\sum_i P_i=1 \hspace{1cm} \sum_i P_iE_i=U$$
- Using the technique of [[Calculus of variations#Constrained variation|Lagrange multipliers]], define the Lagrangian:
$$\Lagr=\sum_i -P_i\ln P_i-\alpha\sum_i P_i-\beta\sum P_iE_i$$
- Then, optimise by:
$$\pd{\Lagr}{P_j}=\pd{\Lagr}{\alpha}=\pd{\Lagr}{\beta}=0$$
- This then gives the _distribution_:
$$P_j=\frac{\exp(-\beta E_j)}{\exp(1+\alpha)}\equiv\frac{\exp(-\beta E_j)}{Z}$$
- This is then simply the Boltzmann distribution