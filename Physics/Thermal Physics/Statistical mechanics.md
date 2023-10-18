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

- A _large system_ is one where there are _many particles_, and it becomes _impossible to solve for motion of all particles_
- Hence, one must deal with _statistical properties_

- Both _interacting_ and _non-interacting_ systems give _emergent statistical properties_

>[!info] Second Law of Thermodynamics
>For a thermally isolated system, entropy cannot **decrease**

>[!info] Third Law of Thermodynamics
>The entropy of all systems in _internal equilibrium_ at absolute zero may be _taken at zero_

# Thermodynamic variables
- One describes the system using _thermodynamic variables_
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
- For _any change_ in $1$, $2$ must 
- Using the _Master Equation_:
$$\displaylines{dS=\frac{dU}{T}+\frac{p}{T}dV-\frac{\mu}{T}dN \\ dS_1+dS_2=}$$
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

### Minimising potentials and availability

# Statistics
- The "state" of a system specifies its _configuration_

- The _probability_ of a state having energy $E_i$, at _temperature_ $T$ is given by the _Boltzmann distribution_:
$$p_i\propto\exp\left(-\frac{E_i}{kT}\right)$$

## Microstates and macrostates
- The _microstate_ of a system is a collection of states, all with the _same energy_ $E_i$
	- They _cannot be distinguished_
- If a microstate has _degeneracy_ $\Omega_i$:
$$p_i\propto\Omega_i\exp\left(-\frac{E_i}{kT}\right)=\exp\left(-\frac{E_i-kT\ln\Omega_i}{kT}\right)\equiv\exp\left(-\frac{E_i-TS_i}{T}\right)$$
- Defining the _entropy_ as:
$$S_i=k\ln\Omega_i$$
- The microstate of _maximum probability_ is the one with _minimum_ $E_i-TS_i$
- _Temperature_ determines the _relative significance_ of $E$ and $S$ in determining probability

- The quantity $E_i-TS_i$ is _a property of the microstate_, and is _NOT_ free energy

- The _Helmholtz free energy_ $F=U-TS$ is a property of the system at _equilibrium_, in the most probably _macrostate_
- The _minimum_ of $E_i-TS_i$ is $F$
	- The corresponding values of $E_i$ and $S_i$ are then the _macrostate_ thermodynamic variables

## Temperature
- Consider a _closed_ system which is in two _partitions_
- The _total energy_ is constant $E=E_1+E_2=\text{const.}$
	- Hence, $dE_1=-dE_2$
- The _total number of states_ is $\Omega=\Omega_1\Omega_2$

- While $\Omega$ is _not extensive_, $\ln\Omega$ is:
$$\ln\Omega=\ln\Omega_1+\ln\Omega_2$$
- For a _given_ $E_1$, the system will try to _maximise_ the number of states:
$$\pd{\Omega}{E_1}=\Omega_2\pd{\Omega_1}{E_1}-\Omega_1\pd{\Omega_2}{E_1}=0$$
- Dividing _both sides_ by $\Omega$:
$$\pd{}{E_1}\ln\Omega_1=\pd{}{E_1}\ln\Omega_2$$

- Using the above definition of _entropy_:
$$T_1=T_2$$

## Gibbs Entropy
- Consider an _open_ system, which is connected to a _reservoir_
- It has _no fixed energy_
- Consider an _ensemble_ of $N$ replicas of the system, each with _different configurations_
	- The replicas are _not time-dependent_
- A subset of these replicas has energy $E_i$
- Define the proportion of this subset as $p_i(E_i)$

- The _total number of states_, taking into account the _indistinguishability_ of replicas with the same energy:
$$\Omega=\frac{N!}{N_1!N_2!\dots N_i!\dots}$$
- Using _Stirling's approximation_ $\ln N!=N\ln N-N$:
$$S=k\ln\Omega=k[N\ln N-N-\sum_i(N_i\ln N_i-N_i)]$$
- Rearranging the expression, one gets:
$$S=-Nk\sum_i\frac{N_i}{N}\ln\frac{N_i}{N}=-Nk\sum_i p_i\ln p_i$$
- This is the _Gibbs entropy_

## Ensembles
- The _microcanonical ensemble_ is one with _closed systems_, where the _energy $E$ is constant_
- There are _states_ $\Omega(E)$, each with probability $p_i$
	- These are not microstates
	- They are fundamentally indistinguishable
- With the _normalisation_:
$$\sum_i p_i=1$$
- One wishes to _maximise entropy_ with the constraint of normalisation
- Using [[Calculus of variations#Lagrange multipliers|Lagrange multipliers]], maximise the function:
$$\pd{}{p_i}\left[-k_B\sum_i p_i\ln p_i-\lambda\sum_i p_i\right]=0$$
- One then gets:
$$p_i=\exp\left(-\frac{\lambda}{k_B}-1\right)$$
- This is _constant_
- Hence, the probability can simply be written as:
$$p_i=\frac{1}{\Omega}$$
