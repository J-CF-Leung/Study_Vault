- Ideas _emerge_ from [[Classical Thermodynamics|Thermodynamics]]
- It deals with _energy_ in _large, (non-)interacting systems_

# Thermodynamics 
- _Energy_ is a _conserved quantity_, given by the _first law_:
>[!info] First Law of Thermodynamics
>Energy is conserved, and both heat and work are forms of energy
>Put mathematically: $$\Delta U=Q+W$$
- $U$ is the _internal energy_ of the system
- $Q$ is the _heat supplied_ to the system
- $W$ is the _work done on_ the system

- _Detailed recap_:
	![[Classical Thermodynamics#The first law, internal energy, and heat]]

- A _large system_ is one where there are _many particles_, and it becomes _impossible to solve for motion of all particles_
- Hence, one must deal with _statistical properties_

- Both _interacting_ and _non-interacting_ systems give _emergent statistical properties_

>[!info] Second Law of Thermodynamics
>For a thermally isolated system, entropy cannot **decrease**

>[!info] Third Law of Thermodynamics
>The entropy of all systems in _internal equilibrium_ at absolute zero may be _taken at zero_

# Thermodynamic variables
- One describes a system at _equilibrium_ using _thermodynamic variables_
- If there is some _generalised force_ acting on some system, characterised by some _displacement_, one can define its form of _energy_:
$$d(\text{Energy})=(\text{Force})\cdot d(\text{Displacement})$$
- The "force" and "displacement" are _conjugate variables_
	- Example: _Torque_ $\tau$ and _angular displacement_ $\theta$
	- Magnetic _field_ $B$ and _magnetisation_ $M$
	- _Surface tension_ $\gamma$ and _area_ $A$
	- _Temperature_ $T$ and _entropy_ $S$, where $dQ=TdS$
- The former entries are _intensive variables_, which remain _constant with scaling_
- The latter entries are _extensive variables_, which _scale with the system_

- To perform _changes of variables_, one uses the _Legendre transform_:
$$\displaylines{\Pi=\Pi(x)\hspace{1cm}\frac{d\Pi}{dx}=Y \\ \Pi'=\Pi-Yx\hspace{1.5cm}\frac{d\Pi'}{dY}=-x}$$

- The _mean internal energy_ of the system is a _function of all extensive variables_:
$$U=U(S,V,N)$$
- A _state function_ is one that _does not depend on the "history" of the system_, but _only its current parameters_

## Equilibrium
- A system at _equilibrium_ is one where there is no _"force"_, and hence _no change in any thermodynamic variable_
- The _total entropy_ of the system $S$ is _unchanged_, or $\Delta S=0$

### The closed system
- Let there be a _closed system at equilibrium_
- _Divide_ the system into two subsystems
- From the fact that $dS=0$, $dS_1+dS_2=0$
- For _any change_ in $1$, $2$ must have the _opposite_ $(dX_1=-dX_2)$
- Using the _Master Equation_:
$$\displaylines{dS=\frac{dU}{T}+\frac{p}{T}dV-\frac{\mu}{T}dN \\ dS_1+dS_2=\left(\frac{1}{T_1}+\frac{1}{T_2}\right)dU+\left(\frac{p_1}{T_1}+\frac{p_2}{T_2}\right)dV-\left(\frac{\mu_1}{T_1}+\frac{\mu_2}{T_2}\right)dN=0}$$

- As the division is _arbitrary_, _all intensive variables_ must be _uniform_ throughout the system

### Reservoir and availability
- Let there be an _open system_, which is connected to a _reservoir_:
$$dS_\text{tot}=dS+dS_R=dS+\frac{dU_R}{T}+\frac{p_R}{T_R}dV_R-\frac{\mu_R}{T_R}dN_R$$
- Converting the _differentials_ to that of the system:
$$-T_R\,dS_\text{tot}=dU-T_R\,dS+p_R\,dV-\mu_R\,dN$$
- Define the _availability_ $A$:
$$dA=dU-T_R\,dS+p_R\,dV-\mu_R\,dN$$
- All the "forces" are that of the _reservoir_ while the "displacements" are that of the _system_
- The availability quantifies how the reservoir can _influence the system_
	- Therefore, it is a function of _both_ the system and the reservoir
- One can rewrite $dA$:
$$dA=(T-T_R)\,dS-(p-p_R)\,dV+(\mu-\mu_R)\,dN$$
- Any _difference in force/intensive variables_ between the _system_ and _reservoir_ will produce some _change in the system_
- At _equilibrium_, $A$ is at a _minimum_, or $dA=0$, and the intensive variables are _equal_

- Availability is linked to the _probability_ of a system to have some value $x$ of a variable
$$\displaylines{S_\text{tot}(x)=k_B\ln\Omega(x) \\ P(x)\propto\exp\left(\frac{S_\text{tot}}{k_B}\right)=\exp\left(-\frac{S_\text{tot}}{k_BT}\right)}$$
### Thermodynamic potentials
- Consider a body with _constant $V$_ and $N$ 

### Minimising potentials

# Statistics
- The "state" of a system specifies its _configuration_

- The _probability_ of a state having energy $E_i$, at _temperature_ $T$ is given by the _Boltzmann distribution_:
$$p_i\propto\exp\left(-\frac{E_i}{kT}\right)$$

## Microstates and macrostates
- _Detailed recap_:
	![[Foundations of statistical thermodynamics#Microstates and macrostates]]

- The __microstates__ of a system is a collection of _states_ (specifying _configuration_, a point in _phase space_), all with the _same energy_ $E_i$
	- They _cannot be distinguished_
- A __macrostate__ is defined by the _bulk properties_ of the system, and _incorporates many microstates_
- Macrostates are described by [[Chemical thermodynamics#State variables and reversibility|state variables]] such as $U, N, V, S, T, p, \mu$
	- _Extensive variables_ $U,N,V,S$ will _scale with_ the system
	- _Intensive variables_ $T,p,\mu$ will _remain constant_ when scaling the system
- Macrostates with energy more or less _equally shared_ among particles become way more likely (way _more available microstates_)
	- Consequence of equal probabilities
	- From the _central limit theorem_, the _mean_ of a quantity (such as energy) is close to its _median_ (value for the _most common microstate_)

### Microstates and macrostates in the canonical ensemble
- Let a system be part of the [[Foundations of statistical thermodynamics#Boltzmann Distribution|canonical ensemble]]
- If a microstate has _degeneracy_ $\Omega_i$:
$$p_i\propto\Omega_i\exp\left(-\frac{E_i}{kT}\right)=\exp\left(-\frac{E_i-kT\ln\Omega_i}{kT}\right)\equiv\exp\left(-\frac{E_i-TS_i}{T}\right)$$
- Defining the _entropy_ as:
$$S_i=k\ln\Omega_i$$
- The microstate of _maximum probability_ is the one with _minimum_ $E_i-TS_i$
- _Temperature_ determines the _relative significance_ of $E$ and $S$ in determining probability

- The quantity $E_i-TS_i$ is _a property of the microstate_, and is _NOT_ free energy

- The _Helmholtz free energy_ $F=U-TS$ is a property of the system at _equilibrium_, in the most probable _macrostate_
- The _minimum_ of $E_i-TS_i$ is $F$
	- The corresponding values of $E_i$ and $S_i$ are then the _thermodynamic variables_ of the _macrostate_

## Temperature
- Consider a _closed_ system which is in two _partitions_
- The _total energy_ is constant $E=E_1+E_2=\text{const.}$
	- Hence, $dE_1=-dE_2$
- The _total number of states_ is $\Omega=\Omega_1\Omega_2$

- While $\Omega$ is _not extensive_, $\ln\Omega$ is:
$$\ln\Omega=\ln\Omega_1+\ln\Omega_2$$
- For a _given_ $E_1$, the system will try to _maximise_ the number of states:
$$\pd{\Omega}{E_1}=\Omega_2\pd{\Omega_1}{E_1}-\Omega_1\pd{\Omega_2}{E_2}=0$$
- Dividing _both sides_ by $\Omega$:
$$\pd{}{E_1}\ln\Omega_1=\pd{}{E_2}\ln\Omega_2$$

- Using the above definition of _entropy_, define _temperature_:
$$\displaylines{\frac{1}{T}=\pd{S}{E} \\ T_1=T_2}$$

## Gibbs Entropy
- Consider an _open_ system, which is connected to a _reservoir_
- It has _no fixed energy_
- Consider an _ensemble_ of $N$ replicas of the system, each with _different configurations and energies_
	- The replicas are _not time-dependent_
- A _subset_ of these replicas has energy $E_i$
- Define the proportion of this subset as $p_i(E_i)$

- The _total number of states_, taking into account the _indistinguishability_ of replicas with the same energy:
$$\Omega=\frac{N!}{N_1!N_2!\dots N_i!\dots}$$
- Using _Stirling's approximation_ $\ln N!=N\ln N-N$:
$$S=k\ln\Omega=k[N\ln N-N-\sum_i(N_i\ln N_i-N_i)]$$
- Rearranging the expression, one gets:
$$S=-Nk\sum_i\frac{N_i}{N}\ln\frac{N_i}{N}=-Nk\sum_i p_i\ln p_i$$
- This is the _Gibbs entropy_

## Ensembles
- As mentioned above, a _statistical ensemble_ is a set of _replicas_ of the system, covering _all possible configurations_

### Microcanonical ensemble
- The _microcanonical ensemble_ is one with _isolated systems_, where the _energy $E$ is constant_
- There are _states_ $\Omega(E)$, each with probability $p_i$
	- These are not microstates
	- They are fundamentally indistinguishable
- With the _normalisation_:
$$\sum_i p_i=1$$
- One wishes to _maximise entropy_ with the constraint of normalisation
- Using [[Calculus of variations#Lagrange multipliers|Lagrange multipliers]], maximise the function:
$$\pd{}{p_i}\left[-k_B\sum_k p_k\ln p_k-\lambda\sum_k p_k\right]=0$$
- One then gets:
$$p_i=\exp\left(-\frac{\lambda}{k_B}-1\right)$$
- This is _constant_
	- Reinforcing the fact that _the states are indistinguishable_
- Hence, the probability can simply be written as:
$$p_i=\frac{1}{\Omega}$$

### Canonical ensemble and the partition function
- A _canonical ensemble_ contains systems _connected to energy reservoirs_, such that _microstates can have any energy $E_i$_
- There must still be some _average energy of the system_ $U$
- Alongside normalisation, this gives the _constraints_:
$$\sum_i p_iE_i=U \hspace{1.5cm} \sum_i p_i=1$$
- Maximising $S/k_B$ with the constraints:
$$\pd{}{p_i}\left(-\sum_i p_k\ln p_k-\lambda\sum_k p_k-\beta\sum_k p_kE_k\right)=0$$
- One then gets:
$$p_i=\exp[-(\lambda+1)-\beta E_i]$$
- Ignoring the _constant prefactor_, then _normalising_:
$$\displaylines{\sum_\text{states} \exp(-\beta E_i)=\sum_\text{microstates}\Omega_i \exp(-\beta E_i)=Z \\ p_i=\frac{\exp(-\beta E_i)}{Z}}$$
- $Z$ is the _partition function_ of the system
- From the definition of _entropy_, one can get that:
$$\beta=\frac{1}{kT}$$
- From the _partition function_, one can get the _internal energy_ and the _free energy_:
$$U=-\pd{}{\beta}\ln Z\hspace{1.5cm} F=-kT\ln Z$$

- One can express the partition function as:
$$Z=\sum_\text{microstates} \exp\left(-\frac{E_i-TS_i}{kT}\right)$$
- This sum has the _largest contribution_ from the _minimum_ of $E_i-TS_i$
- One can then make an _approximation_ of the _equilibrium values_ using the minimum:
$$\text{min}(E_i-TS_i)\approx U-TS$$

- The above expressions give $U$ and $F$ as _functions of $T$_
- $T$ is only the _proper variable for the latter_
- However, $\partial U/\partial T$ still gives _heat capacity_
- One must perform _transformations_ to get _other useful quantities_ from $U$

### Grand canonical ensemble
- A set of _open systems_, able to _exchange energy and number of particles_ with a _reservoir_
- _Microstates_ can have _any energy $E_i$ or number of particles_ $N_i$
- There must be some _average_ $N$

- Constrained minimisation of $S/k_B$:
$$\pd{}{p_i}\left(-\sum_k p_k\ln p_k-\lambda \sum_k p_k-\beta\sum_k p_kE_k-\kappa \sum_k p_kN_k\right)=0$$
- One then gets:
$$p_i=\exp[-(\lambda+1)-\beta E_i-\kappa N_i]$$
- Defining $\kappa$ as $-\mu/kT$:
$$p_i=\frac{1}{\Xi}\exp(-\beta E_i+\beta\mu N_i)$$
- Define the _grand partition function_:
$$\Xi=\sum_i\sum_{N_i}\exp[-\beta(E_i[N_i]-\mu N_i)]$$
- One must sum over both _energy microstates_, as well as _all possible numbers of particles_

- Taking into account the _degeneracy_ of each microstate:
$$\Xi=\sum_\text{microstates}\exp[-\beta(E_i-TS_i)]\exp(\beta\mu N_i)=\sum_{N_i}Z(N_i)\exp(\beta\mu N_i)$$
- Using the definition of entropy:
$$-kT\ln\Xi=F-\mu N=\Phi(T,V,\mu)$$
- $\Phi$ is known as the _grand potential_

### Gibbs ensemble
- For this ensemble, let the systems be able to _expand/contract_, and also be able to _exchange energy_ with the reservoir
- Constrained minimisation:
$$\pd{}{p_i}\left(-\sum_k p_k\ln p_k-\lambda \sum_k p_k-\beta\sum_k p_kE_k-\gamma \sum_k p_kV_k\right)=0$$
- Defining $\gamma\equiv-\beta p$:
$$p_i=\frac{1}{Y}\exp[-\beta (E_i-pV_i)]$$
- From the partition function $Y$, one can derive _thermodynamic potential_ $G(T,p,N)$

### Conclusions
- For each ensemble, one can derive some _partition function_, and the corresponding _thermodynamic potential_
- Each potential must depend on both _intensive and extensive variables_
	- One would not be able to define a partition function or potential for _fixed_ $(T,p,\mu)$

## Examples
### The two-level system
- At _high temperature_, the particles are _evenly distributed across both levels_
	- _Entropy_ is maximised in this distribution

### Point defect in a lattice
- Let there be a lattice with $N$ atoms and $n$ _vacancies_
	- $N+n$ _total sites_
- _Occupying_ a vacancy has _energetic cost_ $\varepsilon$
- The energy of a microstate is then $n\varepsilon$, and the _number of states_ is then:
$$\Omega=\frac{(N+n)!}{N!n!}$$
- _Minimising_ $E_n-TS_n$:
$$n_\text{eq}=\frac{N}{\exp(\beta\varepsilon)-1}$$
- There is _no upper limit_ on $n_\text{eq}$ as temperature gets _high_
- Hence, this is an _unphysical_ model

### The paramagnet
- Magnetic moments can be _spin up or down_, under the influence of an _external magnetic field_ $B$
- If it is _aligned_, the energy is $-mB<0$, and the _antiparallel_ energy is $mB>0$
- The spins _do not interact with each other_

- For a _single spin_:
$$Z_1=\exp\left(-\frac{mB}{kT}\right)+\exp\left(\frac{mB}{kT}\right)=2\text{cosh}\left(\frac{mB}{kT}\right)$$
- For $N$ sites:
$$Z_N=Z_1^N$$
- The _free energy_:
$$F=-NkT\ln\left(2\text{cosh}\left(\frac{mB}{kT}\right)\right)$$
- As expected, it is _extensive_
- The _magnetisation_, or _magnetic moment per spin_:
$$M=-\pd{F}{B}=m\tanh\left(\frac{mB}{kT}\right)$$

- There is an _alternative approach_ using _minimisation_
- The _internal energy_ for each _microstate_:
$$E=mB(N_--N_+)$$
- The _number of states_ for each _microstate_:
$$\Omega=\frac{N!}{N_+!N_-!}$$
- _Defining_ the magnetisation:
$$M=m\frac{N_+-N_-}{N}\hspace{1.5cm} E=-NMB$$
- By _minimising_ $F=E-TS$ w.r.t. $M$, one gets the magnetisation:
$$M=m\tanh\left(\frac{mB}{kT}\right)$$

- There is _another alternative approach_ by defining $\sigma_i=\pm1$ for each site, writing out the _energy_, then the _partition function_ by summing _all configurations_

![[Paramagnet variables.png]]
## The many-level system
- For the [[Quantum Harmonic Oscillator]], there are _many equally spaced, singly degenerate levels_:
$$E_n=\hbar\omega\left(n+\frac{1}{2}\right)$$
- Then write the partition function $Z$:
$$Z=\sum_{n=0}^\infty \exp\left[-\frac{\hbar\omega}{kT}\left(n+\frac{1}{2}\right)\right]=\frac{\exp(-\hbar\omega/2kT)}{1-\exp(-\hbar\omega/kT)}=\frac{1}{2\sinh(\hbar\omega/2kT)}$$
- For _low temperature_, $Z\approx \exp(-\hbar\omega/2kT)$

- Doing the required derivative, one gets the _internal energy_:
$$U=\frac{\hbar\omega}{2}\coth\left(\frac{\hbar\omega}{2kT}\right)$$
- One can also get that at _high temperature_, the _heat capacity_ is _constant_



# The ideal gas in the canonical ensemble
- Let there be a gas of _volume_ $V$, _temperature_ $T$, with _number of particles_ $N$
	- Still free to _exchange energy_ with a reservoir
- Each particle only has _kinetic energy_ $p^2/2m$
- A system with _continuous energy levels_

## Single particle partition function (in phase space)
- The partition function is coverted to an _integral over phase space_
- As _phase space volume_ has dimensionality, and $Z$ is dimensionless, introduce the _normalising factor_:
$$\Delta x\Delta p\sim 2\pi\hbar$$
	- Another approach is from considering _particle in a box_ wave-functions, with _periodic boundary conditions_, and considering some _shell_ in $k-$space

- A _factor_ in $Z$ only adds a _constant_ to entropy or energy4
	- Aside from the $1/2\pi\hbar$, the partition function is still _entirely classical_
	- The factor _embeds "quantumness"_
- Therefore, the partition function is:
$$Z=\int\frac{d^3x\,d^3p}{(2\pi\hbar)^3}\exp\left(-\frac{p_x^2+p_y^2+p_z^2}{2mkT}\right)$$
- Evaluating the integral:
$$Z=\int d^3x\left(\int\exp\left(-\frac{p^2}{2mkT}\right)\frac{dp}{2\pi\hbar}\right)^3=\left(\frac{kTm}{2\pi\hbar^2}\right)^{3/2}V\equiv\frac{V}{\lambda^3}$$
- Similarly, for a 1D or 2D gas, the corresponding $Z$ are $L/\lambda$ and $A/\lambda^2$

- $\lambda$ is the _thermal wavelength_:
$$\lambda\equiv\sqrt{\frac{2\pi\hbar^2}{mkT}}=\left(\frac{2\pi\hbar^2}{m}\beta\right)^{1/2}$$
- It can also be recognised as the _de Broglie wavelength_ when $\mean{p}=\sqrt{mkT}$ (when the _mean momentum_ corresponds to _thermal motion_)

- This gives _energy_:
$$U=-\pd{}{\beta}\ln Z=\frac{3}{2}kT$$

### Single particle partition function (in configuration space)
- In _configuration space_, as _potential energy_ $V(x)=0$, the _Boltzmann factors_ are $1$
- Therefore, $Z$ is the _number of possible configurations of the particle in a box_
- The above result means that this is given by the number of _packets_ of size $\lambda^3$ in $V$

## Internal degrees of freedom
- The gas can have _internal degrees of freedom_
- This gives the _partition function_:
$$Z=Z_1Z_\text{int}=\left(\frac{V}{\lambda^3}\right)^NZ_\text{int}$$

### External potential
- There can be some _external potential_:
$$\displaylines{E=\frac{p^2}{2m}+\phi\Longrightarrow Z=\frac{V}{\lambda^3}\exp\left(-\frac{\phi}{kT}\right) \\ U=-\pd{}{\beta}\ln Z=\frac{3}{2}kT+\phi}$$
- It can be _electrical_, or _gravitational_

### Diatomic
- For a _diatomic molecule_, there are [[#The many-level system|vibrational]] and _rotational_ degrees of freedom
	- Vibrational: [[#The many-level system|quantum harmonic oscillator]] (many-level system)
	- Rotationa;: _Rigid rotor_, characterised by quantum number $J$ with _degeneracy_ $2J+1$
$$\displaylines{Z_\text{osc}=\frac{1}{2\sinh(\beta\hbar\omega/2)} \\ Z_\text{rot}=\sum_{J}(2J+1)\exp\left(-\frac{\beta\hbar^2J(J+1)}{2I}\right)}$$
- One can take a _low and high temperature limits_ for $Z_\text{rot}$:
$$\displaylines{Z_\text{rot}(T\to 0)=1 \\ Z_\text{rot}(T\to\infty)\approx \int_0^\infty(2J+1)\exp\left(-\frac{\beta\hbar^2J(J+1)}{2I}\right)\,dJ=\frac{I}{\hbar^2\beta}}$$
- The internal energy is then:
$$\displaylines{U(T\to0)=\frac{3}{2}kT+\coth\frac{\beta\hbar\omega}{2}+\frac{3\hbar^2}{I}\exp\left(\frac{\beta\hbar^2}{I}\right) \\ U(T\to\infty)=\frac{3}{2}kT+\coth\frac{\beta\hbar\omega}{2}+kT}$$
- At _high temperature_, as there are _2 rotational degrees of freedom_, $U_\text{rot}\approx kT$

## N particles in a box
- For a gas of $N$ _indistinguishable particles_, one must add a factor:
$$Z_N=\frac{Z_1^N}{N!}=\frac{1}{N!}\left(\frac{V}{\lambda^3}\right)^NZ_\text{int}^N$$
- The _internal energy_:
$$U=-\pd{}{\beta}\ln Z=-N\pd{}{\beta}\ln Z_1=\frac{3}{2}NkT+NU_\text{int}$$

- The _free energy_:
$$\begin{aligned}F =-kT\ln Z &= -NkT\ln Z_1+kT(N\ln N-N) \\ &=NkT\ln\left(\frac{N\lambda^3}{eVZ_\text{int}}\right)\end{aligned}$$
- One can then get _pressure_:
$$F=-\pd{F}{V}=\frac{NkT}{V}$$
- As for _entropy_:
$$\begin{aligned}S=-\pd{F}{T}&=-Nk\ln\left(\frac{N}{V}\frac{\lambda^3}{eZ_\text{int}}\right)+\frac{3}{2}Nk \\ &=\frac{3}{2}Nk+\frac{5}{2}Nk\ln T-Nk\ln p+S_0\end{aligned}$$
- $S_0$ takes care of the _internal degrees of freedom and extra factors_

- The _Sackur-Tetrode formula_:
$$\begin{aligned}S&=C_p\ln T-Nk\ln p+S_0 \\ &=C_V\ln T+Nk\ln V+\tilde{S}_0\end{aligned}$$
- The _chemical potential_:
$$\mu=\pd{F}{N}=kT\ln\left(\frac{N\lambda^3}{V}\right)+\mu_0$$
- Like above, $\mu_0$ takes care of the _internal degrees of freedom_ and _extra factors_
- Example: with the external potential
$$\mu=kT\ln\left(\frac{N\lambda^3}{V}\right)+\phi$$
- $N\lambda^3$ can be interpreted as the _volume fraction_ in the box, hence:
$$\mu=kT\ln c+\phi$$
- $c$ can be interpreted as a _concentration_

- For $N\lambda^3/V\ll1$, it is the _classical limit_ where the particles can be interpreted as _"pointlike"_, and the _wave-functions do not overlap_
	- Can be reached by _low temperature_ or _low $N$_
- For $N\lambda^3/V\gg1$, _quantum effects_ start to interfere

# The ideal gas in the grand canonical ensemble
- Consider the _ideal gas_, with _variable energy and particle number_, and _fixed_ $T$ and $\mu$
- The [[#Grand canonical ensemble|grand partition function]]:
$$\Xi=\sum_{N_i=0}^\infty\sum_\text{states}\exp[-\beta(E_i-\mu N_i)]=\sum_{N_i=0}^\infty \frac{1}{N_i!}Z_1^{N_i}\exp(\beta\mu N_i)$$
- This can then be rewritten as:
$$\Xi=\exp\left(Z_1e^{\beta\mu}\right)=\exp\left(\frac{V}{\lambda^3}Z_\text{int}e^{\beta\mu}\right)$$
- One then gets the _grand potential_:
$$\Phi=-kT\ln\Xi=-kT\frac{V}{\lambda^3}Z_\text{int}e^{\beta\mu}$$

- Assume $Z_\text{int}=1$
- The _pressure_ of the gas:
$$p=-\pd{\Phi}{V}=\frac{kT}{\lambda^3}e^{\beta\mu}\hspace{1.5cm}N=-\pd{\Phi}{\mu}=\frac{V}{\lambda^3}e^{\beta\mu}$$
- From this, one can get the _ideal gas law_ $pV=NkT$
- One can also _invert_ the relation for $N$ above to get:
$$\mu=kT\ln\left(\frac{N\lambda^3}{V}\right)$$

## Langmuir isotherm
- Let the _3D gas_ at temperature $T$ be able to be _adsorbed_ onto a _2D surface_
- There is some _energy change_ $-\Delta<0$ when _adsorbed_

- One can consider it as a _single system_ in _equilibrium_, where $T_1=T_2$, $\mu_1=\mu_2$, and $p_1=p_2$
- One can also consider the _adsorbing layer_ as a system _connected to a reservoir_

# Mixtures of an ideal gas
- Let there be a _total particle number_ $N$ and _total pressure_ $p$
- $N_i$ and $p_i$ of each _subsystem_ are _additive_:
$$\sum_i N_i=N\hspace{1.5cm}\sum_i p_i=p$$
- The entropy of _each contribution_:
$$S_i=C_{p_i}\ln T-N_ik\ln p_i+S_{0i}$$
- Calculate an _entropy of mixing_:
$$\Delta S_\text{mix}=S_\text{mixed}-S_\text{pure}=-k\sum_i N_i\ln p_i+kN\ln p_0=-k\sum_i N_i\ln\frac{p_i}{p_0}$$
- Given they are in the _same volume_, with the _same temperature_:
$$\Delta S_\text{mix}=-Nk\sum_i \frac{N_i}{N}\ln\frac{N_i}{N}\equiv-Nk\sum_i c_i\ln c_i$$
- $c_i$ is some _number fraction_ in the mixture

- If there are only _two species_, $A$ and $B$:
$$\displaylines{c_B=1-c_A\equiv 1-c \\ \Delta S_\text{mix}=Nk[c\ln c+(1-c)\ln(1-c)]}$$
- This has a _maximum_ at $c=0.5$
- At $c=0$ or $c=1$, $d(\Delta S_\text{mix})/dc=\pm\infty$

# Chemical reactions
- Let a _chemical reaction_ happen at _constant_ $T$ and $p$
- The _total change in Gibbs Free Energy_ $G$:
$$dG(p,T)=\sum_\text{species}\mu_i dN_i$$
- Incorporating _reaction coefficients_ $\nu_i$ such that:
$$\sum_i \nu_i c_i=0$$
- At _equilibrium_:
$$dG=\sum_i \nu_i\mu_i\,dN_0=0\Longrightarrow \sum_i\nu_i\mu_i=0$$
- Then writing the _chemical potential_ in the [[#The ideal gas in the grand canonical ensemble|grand canonical ensemble]]:
$$\mu_i=kT\ln\left(\frac{N_i}{Z_1(i)}\right)$$
- Substituting this formula, define the _equilibrium constant_ $K$:
$$K=\prod_i N_i^{\nu_i}=\prod_iZ_1^{\nu_i}(i)$$
- The constant is _dimensionless_

- For a _bimolecular_ reaction:
$$\displaylines{A+B\longrightarrow C \\ K_N=\frac{N_AN_B}{N_C}=\frac{Z_1(A)Z_1(B)}{Z_1(C)}}$$
- If the species all have _no internal degrees of freedom_:
$$K_N=\frac{V^2}{\lambda_A^3\lambda_B^3}\frac{\lambda_C^3}{V}\sim\frac{V}{\lambda^3}\gg1$$
- Therefore, the reaction does not occur _unless the reaction has some potential energy advantage_

# The high-temperature limit
- For the [[#The many-level system|quantum harmonic oscillator]], at _high temperatures_:
$$Z=\frac{1}{2\sinh(\beta\hbar\omega/2)}\approx\frac{kT}{\hbar\omega}$$
- However, treating it as a _continuous system_:
$$Z=\int\frac{dx\,dp}{2\pi\hbar}\exp\left(-\frac{p^2}{2mkT}-\frac{\kappa x^2}{2kT}\right)=\frac{1}{\lambda}\sqrt{\frac{2\pi kT}{\kappa}}$$
- This can only be true if the _size of the system_ $L$ is such that $\kappa L^2\gg kT$
- However, at the _high temperature limit_ where $\kappa L^2\ll kT$:
$$Z\approx\frac{L}{\lambda}$$

# Classical to quantum
- Consider the ratio:
$$\frac{N\lambda^3}{V}$$
- If this quantity $\gg1$, the _wave functions of the particles_ start to _overlap_
- The _classical particle_ becomes a _bad approximation_, and one can only speak of _states_

- For a system with _energy levels_ $\varepsilon_i$ each with occupation number $n_i$, with _total number of particles_ $N$ and _total energy_ $E$, denote some _microstate_ by $(N,E)$:
$$Z(N)=\sum_{n_1,n_2,\dots}\exp[-\beta(n_1\varepsilon_1+n_2\varepsilon_2+\dots)]$$
- If there is _no fixed particle number_:
$$\Xi=\sum_{n_1,n_2,\dots}\exp[-\beta(n_1\varepsilon_1+n_2\varepsilon_2+\dots)]\exp(\beta\mu N)$$

# Grand canonical ensemble
- Characterise a system by _energy levels_ $\varepsilon_k$, each with _occupation number_ $n_k$
- The _total energy_ of the system:
$$E=\sum_k n_k\varepsilon_k$$
- Mathematics
- Then the _total grand partition function_ is:
$$\Xi=\prod_k\Xi_k$$
- The _grand potential_ is then:
$$\Phi=\sum_k\Phi_k$$
- _Classical limit_, where $\beta(\varepsilon_k-\mu)\gg1$
$$\Xi_k\approx 1+\exp[-\beta(\varepsilon_k-\mu)]$$

- Below the _quantum threshold_, where $N\lambda^3/V\gg1$, the effects of particles being _bosons_ and _fermions_ emerge
- For _bosons_:
$$\displaylines{\Xi_k=\sum_{n=0}^\infty\exp[-\beta(\varepsilon_k-\mu)n]=\frac{1}{1-\exp[-\beta(\varepsilon_k-\mu)]} \\ \Phi_k=kT\ln[1-\exp(-\beta\varepsilon_k+\beta\mu)] \\ \mean{n_k}=\pd{\Phi_k}{\mu}=\frac{1}{1-\exp[\beta(\varepsilon_k-\mu)]}}$$
- For _fermions_:
$$\displaylines{\Xi_k=\sum_{n=0}^1\exp[-\beta)(\varepsilon_k-\mu)n]=1-\exp[-\beta(\varepsilon_k-\mu)] \\ \Phi_k= \\ \mean{n_k}=\frac{1}{1+\exp[\beta(\varepsilon_k-\mu)]}}$$

- For _bosons_ at _low temperatures_, $\mean{n_k}$ can start to _diverge_
	- This gives rise to the _Bose-Einstein condensate_

- For _fermions_ at _low temperatures_, $\mean{n_k}$ becomes _constant_ at _lower levels_ until the _Fermi energy_ $\varepsilon_F$ where it _drops off quickly_
	- The _chemical potential_ can be _approximated_ by $\varepsilon_F$ as it is the _energy gained by adding one particle_

# The Fermi gas
- Given the _energy distribution_:
$$\mean{n_k}=\frac{1}{1+\exp[\beta(\varepsilon_k-\mu)]}$$
- The _total number of particles_:
$$N=\sum_k\mean{n_k}=\int\frac{d^3x\,d^3p}{(2\pi\hbar)^3}\frac{1}{1+\exp[\beta(\varepsilon_k-\mu)]}$$
- Writing the _density of states_ $g(\varepsilon)$:
$$N=V\int_0^\infty g(\varepsilon)n(\varepsilon)\,d\varepsilon$$
- One can then use the _distribution at absolute zero_:
$$N=V\int_0^{\varepsilon_F}$$
- One then finds that the _Fermi energy_ is:
$$\varepsilon_F=\left[\left(\frac{}{}\right)\frac{N}{V}\right]^{2/3}$$

- The _internal energy_ of the gas:
$$U=\sum_k\varepsilon_k\mean{n_k}=V\int_0^\infty g(\varepsilon)\,d\varepsilon\frac{\epsilon}{1+\exp[]}$$
- At _absolute zero_:
$$U|_{T=0}=V\left(\frac{}{}\right)\left(\frac{N}{V}\right)^{5/3}$$
- This is _not a function of temperature_, as it is _evaulated_ at $T=0$

- When one _compresses_ the gas, due to the _Pauli principle_, the energies are _raised_, giving the _Fermi pressure_:
$$p_F=-\pd{U}{V}=(\dots)\frac{\hbar^2}{m}\left(\frac{N}{V}\right)^{5/3}$$
- This is _not the actual pressure_, as $U|_{T=0}$ is _not a thermodynamic variable_