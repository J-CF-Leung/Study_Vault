- Main ideas _emerge_ from [[Classical Thermodynamics|Thermodynamics]]
- It deals with _energy_ in _large, (non-)interacting systems_

# Thermodynamics 
- _Energy_ is a _conserved quantity_, given by the _first law_:
>[!info] First Law of Thermodynamics
>Energy is conserved, and both heat and work are forms of energy
>Put mathematically: $$\Delta U=Q+W$$
- $U$ is the _internal energy_ of the system
- $Q$ is the _heat supplied_ to the system
	- Typically due to _microscopic_ interactions
- $W$ is the _work done on_ the system
	- Typically due to _macroscopic_ interactions

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

## Internal energy
- For a _reversible change_, $dQ_\text{rev}=TdS$ and $dW_\text{rev}=-pdV$
- Accounting for the _addition of particles_, introduce the _chemical potential_ $\mu$
	- Adding while _fixing entropy and volume_
$$dU=T\,dS-p\,dV+\mu\,dN$$

## Scaling and Gibbs-Duhem relation
- $U,S,V,N$ are all _extensive quantities_, while $T,p,\mu$ are all _intensive_
- If one _scales_ $S,V,N$ by $\lambda$, while keeping $T,p,\mu$ _fixed_, $U$ also _scales_ by $\lambda$:
$$U(\lambda S,\lambda V,\lambda N)=\lambda U(S,V,N)$$
- One can write:
$$\begin{align}U(S,V,N)&=\frac{\partial(\lambda U(S,V,N))}{\partial\lambda}=\frac{\partial}{\partial\lambda}U(\lambda S,\lambda V,\lambda N) \\ &=\frac{\partial U(\lambda S,\lambda V,\lambda N)}{\partial(\lambda S)}S+\frac{\partial U(\lambda S,\lambda V,\lambda N)}{\partial(\lambda V)}V+\frac{\partial U(\lambda S,\lambda V,\lambda N)}{\partial(\lambda N)}N\end{align}$$
- As this is _true for all_ $\lambda$, set it to $1$ and using the definitions of $T,p,\mu$:
$$U=TS-pV+\mu N$$
- By examining the _total differential_, one obtains the _Gibbs-Duhem equation_:
$$S\,dT-V\,dp+N\,d\mu=0$$

## Equilibrium
- A system at _equilibrium_ is one where there is no _"force"_, and hence _no change in any thermodynamic variable_
- The _total entropy_ of the system $S$ is _unchanged_, or $\Delta S=0$

- All systems also have an _equation of state_ specifying _equilibrium behaviour_:
$$f(p,T,V,N\dots)=0$$
- Example: the [[Classical Thermodynamics#Ideal gases|ideal gas]]

### The closed system
- Let there be a _closed system at equilibrium_
- _Divide_ the system into two subsystems
- From the fact that $dS=0$, $dS_1+dS_2=0$
- For _any change_ in $1$, $2$ must have the _opposite_ $(dX_1=-dX_2)$
- Using the _Master Equation_:
$$\displaylines{dS=\frac{dU}{T}+\frac{p}{T}dV-\frac{\mu}{T}dN \\ dS_1+dS_2=\left(\frac{1}{T_1}-\frac{1}{T_2}\right)dU+\left(\frac{p_1}{T_1}-\frac{p_2}{T_2}\right)dV-\left(\frac{\mu_1}{T_1}-\frac{\mu_2}{T_2}\right)dN=0}$$
 
- As the division is _arbitrary_, _all intensive variables_ must be _uniform_ throughout the system

### Reservoir and availability
- Let there be an _open system_, which is connected to a _reservoir_:
$$dS_\text{tot}=dS+dS_R=dS+\frac{dU_R}{T}+\frac{p_R}{T_R}dV_R-\frac{\mu_R}{T_R}dN_R$$
- Converting the _differentials_ to that of the system:
$$-T_R\,dS_\text{tot}=dU-T_R\,dS+p_R\,dV-\mu_R\,dN$$
- Define the _availability_ $A$:
$$dA=dU-T_R\,dS+p_R\,dV-\mu_R\,dN$$
- As the parameters of the reservoir are _constant_, integrate to get:
$$A=U-T_{R}S+p_{R}V-\mu_{R}N$$

- All the "forces" are that of the _reservoir_ while the "displacements" are that of the _system_
- The availability quantifies how the reservoir can _influence the system_
	- Therefore, it is a function of _both_ the system and the reservoir
- One can rewrite $dA$:
$$dA=(T-T_R)\,dS-(p-p_R)\,dV+(\mu-\mu_R)\,dN$$
- Any _difference in force/intensive variables_ between the _system_ and _reservoir_ will produce some _change in the system_
- At _equilibrium_, $A$ is at a _minimum_, or $dA=0$, and the intensive variables are _equal_
	- It is at a minimum as this is where $dS_\text{tot}$ is at _maximum
$$dA\leq 0$$

- Availability is linked to the _probability_ of a system to have some value $x$ of a variable
$$\displaylines{S_\text{tot}(x)=k_B\ln\Omega(x) \\ P(x)\propto\exp\left(\frac{S_\text{tot}}{k_B}\right)=\exp\left(-\frac{A(x)}{k_BT}\right)}$$

- Consider the case where work is _extracted_ from the system and reservoir, such that $dU\neq dU_{R}$
	- The second equality is from writing $U$ in terms of $A$
$$-dW_\text{extr}=dU+dU_{R}=dA+T_{R}d(S+S_{R})$$
- From this, $W_\text{extr}$ matches a _decrease in availability_
$$\Delta W_\text{extr}=-\Delta A$$
- $-\Delta A$ is the _maximum useful work_ from a system

### Legendre transforms and availability
- At _equilibrium_, $T=T_{R},p=p_{R},\mu=\mu_{R}$
- For this to be true, $S,V,N$ (the _natural variables_) must have their _equilibrium values_ $S_\text{eq},V_\text{eq},N_\text{eq}$, as _dictated_ by $T_{R},\mu_{R},p_{R}$
- $T_{R},p_{R},\mu_{R}$ correspond to the _values at equilibrium_ ($S=S_\text{eq},V=V_\text{eq},N=N_\text{eq}$)
- They can be considered _variables_ to describe the combined system

- This is an application for _Legendre transformations_
- For a function $f(x)$, consider the function $g(x,y)=f(x)-yx$:
$$dg=f'dx-ydx-xdy$$
- The _minimum_ of $g$ w.r.t. has $f'=y$
- Define $g_{0}$ as the _value of $g$ at its minimum_ w.r.t. $x$, for a _given_ $y$:
$$g_{0}(y)=\text{min}_{x}g(x,y)=g(x_{0},y)\implies dg_{0}=-x_{0}\,dy$$
- This is useful for describing systems _in terms of other variables_

- Consider the internal energy $U(S,V,N)$, and do a Legendre transform w.r.t. $S$:
$$\displaylines{F(S,V,N,T_{R})=U(S,V,N)-T_{R}S \\ dF=(T-T_{R})dS-S\,dT_{R}-p\,dV+\mu\,dN}$$
- The _minimum_ w.r.t. $S$ has $T=T_{R}$, _fixing_ the equilibrium entropy at $S=S_\text{eq}$
- Redefining all properties as their _equilibrium values_, one gets the expression for _Helmholtz free energy_
$$\displaylines{F(T,V,N)=U-TS\\dF=-S\,dT-p\,dV+\mu\,dN}$$

- When the Legendre transform is performed on all three variables, one gets _availability_
$$A=U-T_{R}S+p_{R}V-\mu_{R}N$$
- At _equilibrium_, the differential is:
$$dA=-S_\text{eq}\,dT_{R}+V_\text{eq}\,dp_{R}-N_\text{eq}\,d\mu_{R}$$
- In equilibrium, $A=0$, simply because _one cannot obtain any more work_
	- Also from $U-TS+pV-\mu N=0$
- However, there _are not always so many constrained variables_ as $T,p,\mu$
- This generates _other thermodynamic potentials_
### Thermodynamic potentials
- For a _system_ connected to some _reservoir_, $U_\text{sys}$ is _insufficient_ to determine the _equilibrium state_
- Energy must be _conserved for both the system and the reservoir_
- This is dependent on what _restrictions_ the reservoir places
	- _Only_ exchanging _energy_: constant $T$ due to reservoir, constant $V,N$ as properties of the system

- When work is _done_ on the system, energy is _stored in/removed from_ the reservoir
- Consider the _reversible work done_ on an _isothermal system_:
$$dW=dU-TdS=d(U-TS)_{T}\equiv(dF)_{T}$$
- Here, $F$ is the _Helmholtz free energy_:
$$F=U-TS$$
- In this case, for a system with a _fixed temperature_ $T$, $dF=0$ in _equilibrium_
	- No more work can be extracted for the _combined_ system 

- It is an example of a _thermodynamic potential_
	- It is a property which takes _global energy conservation_ into account
	- For given _external conditions_, there is a potential to be _minimised at equilibrium_
	- Also given as a _Legendre transform_ w.r.t. $S$

- Depending on the nature of the _reservoir_, and constraints in consideration, the other _thermodynamic potentials_ are:

| Name                  | Potential       | Differential         |
| --------------------- | --------------- | -------------------- |
| Internal energy       | $U=TS-pV+\mu N$ | $dU=TdS-pdV+\mu dN$  |
| Enthalpy              | $H=U+pV$        | $dH=TdS+Vdp+\mu dN$  |
| Helmholtz free energy | $F=U-TS$        | $dF=-SdT-pdV+\mu dN$ |
| Gibbs free energy     | $G=U-TS+pV$     | $dG=-SdT+Vdp+\mu dN$ |
| Grand/Landau potential                      | $\Phi=F-\mu N$                | $d\Phi=-SdT-pdV-Nd\mu$                     |
- If one knows a potential as a _function of its natural variables_, one has _complete thermodynamic information_ about the system
	- e.g. knowing $F(T,V,N)$ is sufficient, $F(T,V,p)$ is not

### Minimising potentials
- For a completely _isolated_ system, it must have _constant_ $S,V,N$
- Any _work extracted_ will _decrease_ $U$
	- $(dA)_{S,V,N}=(dU)_{S,V,N}$
- At equilibrium, $U$ is _minimised_

- For a system held at _constant pressure_, $S,p.N$ are fixed:
$$(dA)_{S,p,N}=d(U+pV)_{S,p,N}=d(H)_{S,p,N}$$
- $H=U+pV$, the _enthalpy_, is _minimised in equilibrium_ 
- The _heat_ transferred in constant pressure is equal to the _change in enthalpy_
$$(d\hspace{-0.04em}\bar{}\hspace{0.1em}Q)_{p}=(dH)_{p}$$
- This is important for _flow processes_ (e.g. fluids), and _phase transitions_


- For a system held at _constant temperature_, $T,V,N$ are fixed:
$$(dA)_{T,V,N}=d(U-TS)_{T,V,N}=d(F)_{T,V,N}$$
- $F=U-TS$, the _Helmholtz free energy_, is _minimised in equilibrium_
- $\Delta F$ is the _work done_ for a system at _constant temperature_


- For a system held at _constant temperature and pressure_, $T,p,N$ are fixed:
$$(dA)_{T,p,N}=d(U-TS+pV)_{T,p,N}=d(H-TS)_{T,p,N}=d(G)_{T,p,N}$$
- $G=U+pV-TS$, the _Gibbs free energy_, is _minimised in equilibrium_
- Useful for _chemical and phase equilibria_
- In a _pure phase_, $G=\mu N$, and $\mu$ is the _Gibbs energy per particle_
	- Can also be used to derive the [[#Scaling and Gibbs-Duhem relation|Gibbs-Duhem relation]]


- For a system held at _constant temperature and chemical potential_, $T,V,\mu$ are fixed:
$$(dA)_{T,V,\mu}=d(U-TS-\mu N)_{T,V,\mu}=d(\Phi)_{T,V,\mu}$$
- $\Phi=F-\mu N$, the _grand potential_, is _minimised in equilibrium_

### Summary
- For _fixed temperature_:

| Name                      | Helmholtz Free Energy  | Gibbs Free Energy | Grand potential    |
| ------------------------- | ---------------------- | ----------------- | ------------------ |
| Formula                   | $F=U-TS$               | $G=U+pV-TS=\mu N$ | $\Phi=F-\mu N=-pV$ |
| Differential              | $-SdT-pdV+\mu dN$      | $-SdT+Vdp+\mu dN$ | $-SdT-pdV-Nd\mu$   |
| Minimised for constraints | $T,V,N$                | $T,p,N$           | $T,V,\mu$          |
| Significance              | Mechanical equilibrium | Phase equilibrium | Fermions, bosons   |

- For _thermally isolated_ systems:

| Name                      | Internal Energy  | Enthalpy         |
| ------------------------- | ---------------- | ---------------- |
| Formula                   | $U=TS-pV+\mu N$  | $H=U+pV$         |
| Differential              | $TdS-pdV+\mu dN$ | $TdS+Vdp+\mu dN$ |
| Minimised for constraints | $V,N$            | $p,N$            |
| Significance              | Isolated systems | Flow processes   |

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

### Microscopic effect of heat and work
- From considering Gibbs entropy, and the _Boltzmann distribution_, using $\sum_{i} dP_{i}=0$ as the sum of $P_{i}$ is fixed:
$$dS=-k_{B}\sum_{i} d(P_{i}\ln P_{i})=k_{B}\sum_{i} \frac{E_{i}\,dP_{i}}{k_{B}T}$$
- One gets:
$$T\,dS=\sum_{i}E_{i}\,dP_{i}$$
- This is the _reversible heat flow_
- Then using the first law:
$$d\hspace{-0.04em}\bar{}\hspace{0.1em}W_\text{rev}=\sum_{i} P_{i}\,dE_{i}$$
- Heat _changes the probability distribution_ (but not the energies)
- Work _changes the energy levels_ (but not the probabilities)

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
	- Derived from definitions of $U$, and the [[#Gibbs Entropy]]
$$U=-\pd{}{\beta}\ln Z\hspace{1.5cm} F=-kT\ln Z$$

- One can express the partition function as:
$$Z=\sum_\text{microstates} \exp\left(-\frac{E_i-TS_i}{kT}\right)$$
- This sum has the _largest contribution_ from the _minimum_ of $E_i-TS_i$
- One can then make an _approximation_ of the _equilibrium values_ using the minimum:
$$\text{min}(E_i-TS_i)\approx U-TS=F$$
- This is one method to obtain the _expression_ for $F$
- $F$ is only defined for the _equilibrium macrostate_
- From there, one obtains $S$ and $p$ as _functions_ of $T$ and $V$
 
- The above expressions give $U$ and $F$ as _functions of $T$_
- $T$ is only the _proper variable for the latter_
- However, $\partial U/\partial T$ still gives _heat capacity_
- One must perform [[#Thermodynamic potentials|transformations]] to get _other useful quantities_ from $U$

- One can also check the _probability for a microstate of energy_ $E$:
$$P(E_{i})\propto \Omega(E)\exp(-\beta E)=\exp[-\beta(E-k_{B}T\ln\Omega(E))]$$
- As expected, this is _maximised_ for $E-TS(E)$ is minimised
	- Minimised at _equilibrium_

### Grand canonical ensemble
- A set of _open systems_, able to _exchange energy and number of particles_ with a _reservoir_
- _Microstates_ can have _any energy $E_i$ or number of particles_ $N_i$
- There must be some _average_ $N$

- Constrained minimisation of $S/k_B$:
$$\pd{}{p_i}\left(-\sum_k p_k\ln p_k-\lambda \sum_k p_k-\beta\sum_k p_kE_k-\kappa \sum_k p_kN_k\right)=0$$
- One then gets:
$$p_i=\exp[-(\lambda+1)-\beta E_i-\kappa N_i]$$
- Defining $\kappa$ as $-\mu/kT$:
$$p_i=\frac{1}{\Xi}\exp[-\beta (E_i-\mu N_i)]$$
- Define the _grand partition function_:
$$\Xi=\sum_i\sum_{N_i}\exp[-\beta(E_i[N_i]-\mu N_i)]$$
- One must sum over both _energy microstates_, as well as _all possible numbers of particles_
	- Exponential term known as the _Gibbs factor_
	- Energy eigenstates are, in general, _different for each particle number_

- Taking into account the _degeneracy_ $\Omega(E_{i})$ of each microstate, $\Xi$ can be written as:
$$\Xi=\sum_\text{microstates}\exp[-\beta(E_i-TS_i)]\exp(\beta\mu N_i)=\sum_{N_i}Z(N_i)\exp(\beta\mu N_i)$$

- Using the definition of [[#Gibbs Entropy]]
	- Or deduce that the _maximum probability_ is when $E-TS(E,N)-\mu N$ is _minimised_, and in equilibrium, $\Xi \approx \exp(-\beta \Phi)$
$$-kT\ln\Xi=F-\mu N=\Phi(T,V,\mu)$$
- $\Phi$ is known as the _grand potential_

### Gibbs ensemble
- For this ensemble, let the systems be able to _expand/contract_, and also be able to _exchange energy_ with the reservoir
- Constrained minimisation:
$$\pd{}{p_i}\left(-\sum_k p_k\ln p_k-\lambda \sum_k p_k-\beta\sum_k p_kE_k-\gamma \sum_k p_kV_k\right)=0$$
- Defining $\gamma\equiv-\beta p$:
$$p_i=\frac{1}{Y}\exp[-\beta (E_i-pV_i)]$$
- From the partition function $Y$, one can derive _thermodynamic potential_ $G(T,p,N)$

### Conclusions and summary
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

- A _factor_ in $Z$ only adds a _constant_ to entropy or energy
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

## Internal degrees of freedom and external potentials
- The gas can have _internal degrees of freedom_
- This gives the _partition function_:
$$Z=Z_1Z_\text{int}=\left(\frac{V}{\lambda^3}\right)Z_\text{int}$$

### External potential
- There can be some _external potential_:
$$\displaylines{E=\frac{p^2}{2m}+\phi\Longrightarrow Z=\frac{V}{\lambda^3}\exp\left(-\frac{\phi}{kT}\right) \\ U=-\pd{}{\beta}\ln Z=\frac{3}{2}kT+\phi}$$
- It can be _electrical_, or _gravitational_

### Diatomic
- For a _diatomic molecule_, there are [[#The many-level system|vibrational]] and _rotational_ degrees of freedom
	- Vibrational: [[#The many-level system|quantum harmonic oscillator]] (many-level system)
	- Rotational: _Rigid rotor_, characterised by quantum number $J$ with _degeneracy_ $2J+1$
$$\displaylines{Z_\text{osc}=\frac{1}{2\sinh(\beta\hbar\omega/2)} \\ Z_\text{rot}=\sum_{J}(2J+1)\exp\left(-\frac{\beta\hbar^2J(J+1)}{2I}\right)}$$
- One can take a _low and high temperature limits_ for $Z_\text{rot}$:
$$\displaylines{Z_\text{rot}(T\to 0)=1 \\ Z_\text{rot}(T\to\infty)\approx \int_0^\infty(2J+1)\exp\left(-\frac{\beta\hbar^2J(J+1)}{2I}\right)\,dJ=\frac{I}{\hbar^2\beta}}$$
- The internal energy is then:
$$\displaylines{U(T\to0)=\frac{3}{2}kT+\coth\frac{\beta\hbar\omega}{2}+\frac{3\hbar^2}{I}\exp\left(\frac{\beta\hbar^2}{I}\right) \\ U(T\to\infty)=\frac{3}{2}kT+\coth\frac{\beta\hbar\omega}{2}+kT}$$
- At _high temperature_, as there are _2 rotational degrees of freedom_, $U_\text{rot}\approx kT$
![[Diatomic heat capacities.png]]

## Thermodynamics of N particles in a box
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
	- the _Sackur-Tetrode formula_
$$\begin{aligned}S&=C_p\ln T-Nk\ln p+S_0 \\ &=C_V\ln T+Nk\ln V+\tilde{S}_0\end{aligned}$$
- For the _ideal gas_ with _no internal degrees of freedom_, the Sackur-Tetrode formula gives:
$$S=-\frac{\partial F_\text{ideal}}{\partial T}=\frac{5}{2}Nk_{B}+Nk_{B}\ln\left( \frac{V}{N\lambda^{3}} \right)$$

- The _chemical potential_:
$$\mu=\pd{F}{N}=kT\ln\left(\frac{N\lambda^3}{V}\right)+\mu_0$$
- Like above, $\mu_0$ takes care of the _internal degrees of freedom_ and _extra factors_
- Example: with the external potential,
$$\mu=kT\ln\left(\frac{N\lambda^3}{V}\right)+\phi$$
- $N\lambda^3$ can be interpreted as the _volume fraction_ in the box, hence:
$$\mu=kT\ln c+\phi$$
- $c$ can be interpreted as a _concentration_

## Classical to quantum crossover
- For $N\lambda^3/V\ll1$, it is the _classical limit_ where the particles can be interpreted as _"pointlike"_, and the _wave-functions do not overlap_
	- Can be reached by _low temperature_ or _low $N$_
	- Here, one gets $\mu\ll0$
- For $N\lambda^3/V\gg1$, _quantum effects_ start to interfere (wave-functions overlap)
- The _classical particle_ becomes a _bad approximation_, and one can only speak of _states_

## Equipartition
- The classical gas displays _equipartition_
- For any system with a _separable, quadratic Hamiltonian_, it is trivial to show that the _probability distributions for each coordinate are independent of other coordinates_

- Then for each coordinate $q$:
$$\displaylines{H(q)=Aq^{2} \\ \langle Aq^{2} \rangle = \frac{\int Aq^{2}\exp(-\beta Aq^{2}) \, dq}{\int \exp(-\beta Aq^{2}) \, dq } = \frac{1}{2}k_{B}T  }$$
- For each _degree of freedom present in_ $H$, there is $k_{B}T/2$ of energy
- In the _ideal gas_, the DoF are $p_{x},p_{y},p_{z}$

- Valid for the _classical limit_
# Grand partition function and grand potential
- Characterise a system by _energy levels_ $\varepsilon_k$, each with _occupation number_ $n_k$
- The _total energy_ of the system:
$$E=\sum_k n_k\varepsilon_k$$
- With _total number of particles_ $N$ and _total energy_ $E$, denote some _microstate_ by $(N,E)$, with _partition function_:
$$\displaylines{Z(T,V,N)=\sum_{n_1,n_2,\dots}\exp[-\beta(n_1\varepsilon_1+n_2\varepsilon_2+\dots)] \\ \text{satisfying }\, N=n_{1}+n_{2}+\dots}$$
- For _fermions_, the occupation number of each level must be $0$ or $1$

- If there is _no fixed particle number_, consider the _grand partition function_:
$$\begin{align}
\Xi(T,V,\mu)&=\sum_{N=0}^{\infty}Z(T,V,N)\exp(\beta\mu N) \\ &=\sum_{N=0}^{\infty}\sum_{n_{1},n_{2},\dots}^{N} \exp[-\beta(n_{1}\varepsilon_{1}+n_{2}\varepsilon_{2}+\dots)+\beta\mu(n_{1}+n_{2}+\dots)]
\end{align}$$
- The second sum has the _constraint_ that $n_{1}+n_{2}+\dots=N$
- However, as $N$ is _summed over_, the total sum is:
$$\begin{align}
\Xi(T,V,\mu)&=\sum_{n_{1},n_{2},\dots} \exp[-\beta(n_{1}\varepsilon_{1}+n_{2}\varepsilon_{2}+\dots)+\beta\mu(n_{1}+n_{2}+\dots)] \\ &=\sum_{n_{1},n_{2},\dots} \exp[-\beta(\varepsilon_{1}-\mu)n_{1}]\exp[-\beta(\varepsilon_{2}-\mu)n_{2}]\dots \\ &= \left[ \sum_{n_{1}} \exp[-\beta(\varepsilon_{1}-\mu)n_{1}] \right]\left[ \sum_{n_{2}} \exp[-\beta(\varepsilon_{2}-\mu)n_{2}] \right]\dots
\end{align}$$

- Then the _total grand partition function_ is:
$$\Xi=\prod_k\Xi_k$$
- The total grand partition function $\Xi$ is a _product_ of grand partition functions _of the individual energy levels_ $\Xi_{k}$

- The [[#Grand canonical ensemble|grand potential]] is then:
$$\Phi=\sum_k\Phi_k$$

## Classical limit
- For a _single energy level_ of energy $\varepsilon_{k}$:
$$\Xi_k=\sum_{n}\exp[-\beta(n\varepsilon_{k}-n\mu)]=\sum_{n}\left[\exp[-\beta(\varepsilon_{k}-\mu)]\right]^{n}$$
- For _fermions_, the occupation number of each level must be $0$ or $1$

- Let $\beta(\varepsilon_k-\mu)\gg1$
	- Different from the _high energy/low temperature limit_
$$\Xi_k=\sum_{n}(\exp[-\beta(\varepsilon_{k}-\mu)])^{n}\approx 1+\exp[-\beta(\varepsilon_k-\mu)]\equiv \Xi_{k}^{\text{cl}}$$
- If this is _valid for all energy levels_, then one gets a _classical gas_, as _fermionic/bosonic nature is irrelevant_
- This can only be valid for a _large, negative_ $\mu$, also corresponding to the [[#Classical to quantum crossover|classical limit]]
	- In the _ideal classical gas_, $\beta \mu=\ln(N\lambda^{3}/V)$

- Take the _grand potential_, expanding the logarithm to the _lowest order_:
$$\Phi_{k}^{\text{cl}}=-k_{B}T\ln \Xi_{k}^{\text{cl}}\approx -k_{B}T\exp[-\beta(\varepsilon_{k}-\mu)]$$
- The _average occupancy_ is then:
$$\langle n_{k} \rangle =-\left( \frac{\partial \Phi_{k}}{\partial \mu} \right)_{T,V}\approx \exp[-\beta(\varepsilon_{k}-\mu)] $$
- This is simply the _Maxwell-Boltzmann distribution_
	- For the _classical gas_, $\langle n_{k} \rangle$ is _always small_, including for $k=0$
## Quantum particles
- Below the _quantum threshold_, where $N\lambda^3/V\gg1$, the effects of particles being _bosons_ and _fermions_ emerge
- For _bosons_:
$$\displaylines{\Xi_k=\sum_{n=0}^\infty\exp[-\beta(\varepsilon_k-\mu)n]=\frac{1}{1-\exp[-\beta(\varepsilon_k-\mu)]} \\ \Phi_k=kT\ln[1-\exp(-\beta\varepsilon_k+\beta\mu)] \\ \mean{n_k}=\pd{\Phi_k}{\mu}=\frac{1}{\exp[\beta(\varepsilon_k-\mu)]-1}}$$
- The _Bose-Einstein distribution_

- For _fermions_:
$$\displaylines{\Xi_k=\sum_{n=0}^1\exp[-\beta(\varepsilon_k-\mu)n]=1+\exp[-\beta(\varepsilon_k-\mu)] \\ \Phi_k=kT\ln[1+\exp(-\beta\varepsilon_{k}+\beta \mu)] \\ \mean{n_k}=\frac{1}{\exp[\beta(\varepsilon_k-\mu)]+1}}$$
- The _Fermi-Dirac distribution_

- For _bosons_ at _low temperatures_, $\mean{n_k}$ can start to _diverge_
	- This gives rise to the _Bose-Einstein condensate_

- For _fermions_ at _low temperatures_, $\mean{n_k}$ becomes _constant_ at _lower levels_ until the _Fermi energy_ $\varepsilon_F$ where it _drops off quickly_
	- The _chemical potential_ can be _approximated_ by $\varepsilon_F$ as it is the _energy gained by adding one particle_

## Accounting for spin
- Quantum particles all have _spin_ $s$
- _Without external field_, spin _does not affect energy_, and there is a _degeneracy_:
$$\sigma\equiv 2s+1$$
# The ideal gas in the grand canonical ensemble
- Consider the _ideal gas_, with _variable energy and particle number_, and _fixed_ $T$ and $\mu$
- Let the particles also have _spin degeneracy_ $\sigma$
- The single particle partition function:
$$Z_{1}=\frac{\sigma V}{\lambda^{3}}$$
## Evaluating the grand partition function
- The [[#Grand canonical ensemble|grand partition function]]:
$$\Xi=\sum_{N_i=0}^\infty\sum_\text{states}\exp[-\beta(E_i[N_{i}]-\mu N_i)]=\sum_{N_i=0}^\infty \frac{1}{N_i!}Z_1^{N_i}\exp(\beta\mu N_i)$$
- This can then be rewritten as:
$$\Xi=\exp\left(Z_1e^{\beta\mu}\right)=\exp\left(\frac{\sigma V}{\lambda^3}e^{\beta\mu}\right)$$
### Thermodynamic quantities
- One then gets the _grand potential_:
$$\Phi=-kT\ln\Xi=-kT\frac{\sigma V}{\lambda^3}e^{\beta\mu}$$

- The _pressure_ of the gas, and the _equilibrium number of particles_ given $\mu$:
$$p=-\pd{\Phi}{V}=\frac{k_{B}T\sigma}{\lambda^3}e^{\beta\mu}\hspace{1.5cm}N=-\pd{\Phi}{\mu}=\frac{\sigma V}{\lambda^3}e^{\beta\mu}$$
- From this, one can get the _ideal gas law_ $pV=NkT$
- One can also _invert_ the relation for $N$ above to get:
$$\beta\mu=\ln\left(\frac{N\lambda^3}{\sigma V}\right)=\ln\left( \frac{N}{Z_{1}} \right)$$
- Once again, one can define a [[#Classical to quantum crossover|classical limit]] where $\mu\ll0$

- The entropy is given by:
$$S=-\left( \frac{\partial \Phi}{\partial T} \right)_{\mu,V}=k_{B} \frac{\sigma V}{\lambda^{3}}\exp(\beta \mu )\left[ \frac{5}{2}-\frac{\mu}{k_{B}T} \right]$$
- This gives the [[#Thermodynamics of N particles in a box|Sackur-Tetrode formula]]:
$$S=Nk_{B}\ln\left[ e^{5/2} \frac{\sigma V}{N}\left( \frac{mk_{B}T}{2\pi \hbar^{2}} \right)^{3/2} \right]$$

### Alternative: direct integration
- The _grand potential_ is:
$$\Phi=\sum\Phi_{k}=-k_{B}T \int  \, \Phi (\varepsilon) \frac{\sigma\,d^{3}x\,d^{3}p}{(2\pi \hbar)^{3}} $$

- Expression for $\Phi_{k}$ in the _classical limit_:
$$\Phi_{k}^{\text{cl}}=-k_{B}T\ln \Xi_{k}^{\text{cl}}\approx -k_{B}T\exp[-\beta(\varepsilon_{k}-\mu)]$$
- One can _sum over all states_, either in _phase space_ or using the _density of states_ in $\varepsilon$
	- The latter expression can be obtained via _quantisation_, or using $d^{3}p=4\pi p^{2}\,dp$
	- The density of states is for _single particles_
$$\displaylines{\int  \, \frac{\sigma\,d^{3}x\,d^{3}p}{(2\pi \hbar)^{3}} \longrightarrow \int_{0}^{\infty} g(\varepsilon) \, d\varepsilon  \\ g(\varepsilon)=\frac{\sigma V}{4\pi^{2}} \left( \frac{2m}{\hbar^{2}} \right)^{3/2}\sqrt{ \varepsilon }}$$
- Final expression for the grand potential, same as considering $Z$:
$$\Phi=-k_{B}T \frac{\sigma V}{\lambda^{3}}\exp(\beta \mu)$$
### Maxwell-Boltzmann distribution
- The number of _energy levels_ within $\varepsilon\to\varepsilon+d\varepsilon$ is $g(\varepsilon)\,d\varepsilon$
- The probability of _finding_ a particle in that energy interval is $\langle n_{k} \rangle/N$
- Then, the _probability of finding a particle in the box with energy_ $\varepsilon$ is $P(\varepsilon)$
$$P(\varepsilon)\,d\varepsilon=\frac{\langle n_{k} \rangle}{N}g(\varepsilon)\,d\varepsilon$$
- Substituting expressions for $\langle n_{k} \rangle$, $\mu$, and $g(\varepsilon)$, and using $\varepsilon=mv^{2}/2$, one obtains the _Maxwell distribution of speeds_:
$$P(v)\,dv=\left( \frac{m}{2\pi k_{B}T} \right)^{3/2}\exp(-\beta mv^{2}/2)\,4\pi v^{2}\,dv$$

## Internal degrees of freedom and external potentials
- Extend to particles with _internal degrees of freedom_, or subject to an _external potential_
- Let energy be in the form:
$$\varepsilon=\varepsilon_{\boldsymbol{k}}+\varepsilon _\text{int}+\varepsilon _\text{ext}$$
- For a _diatomic molecule_, with _vibrational_ and _rotational_ energy:
$$\varepsilon _\text{int}=\left( n+\frac{1}{2} \right)\hbar\omega_{0}+\frac{\hbar^{2}J(J+1)}{2I}$$
- External energy: can be _gravitational_ or _electrical_
- The _grand partition function/potential_ for a _single energy level_ $\varepsilon_{\boldsymbol{k}}$, in the [[#Classical limit]]
$$\displaylines{\Xi_{\boldsymbol{k}}=1+\sum_\text{int}\exp[-\beta(\varepsilon_{\boldsymbol{k}}+\varepsilon _\text{int}+\varepsilon _\text{ext}-\mu)]=1+Z_\text{int}Z_\text{ext}\exp[-\beta(\varepsilon_{\boldsymbol{k}}-\mu)] \\ \Phi_{\boldsymbol{k}}\approx -k_{B}TZ_\text{int}Z_\text{ext}\exp[-\beta(\varepsilon_{\boldsymbol{k}}-\mu)]}$$
- For a _particle number_ $N$, the chemical potential is then:
$$\mu=k_{B}T\left[ \ln\left( \frac{N\lambda^{3}}{\sigma V} \right)-\ln Z_\text{int}-\ln Z_\text{ext} \right]$$

- Example: _gravitational potential energy_:
$$\varepsilon=mgh \implies -k_{B}T\ln Z_\text{ext}=mgh$$
- $Z_\text{int}$ and $\mu$ must _both be independent of height_
$$N(h)=N(0)\exp\left( -\frac{mgh}{k_{B}T} \right)$$

## Langmuir isotherm
- Let the _3D gas_ at temperature $T$ be able to be _adsorbed_ onto a _2D surface_ with $N_{s}$ sites
- There is some _energy change_ $-\epsilon<0$ when _adsorbed_
- Consider _no internal degrees of freedom_ in the _vapour_
- On the _surface_, it can _vibrate_ against the surface, with _partition function_ $z_{s}(T)$

- For a given _vapour pressure_ $p$, there is a _fraction of surface sites occupied_ $\theta=N_{s}/N$

- In _equilibrium_, the _chemical potentials_ of the sites $(\mu_{s})$ and the _vapour_ $\mu_{v}$ are the same
$$\mu_{s}=\mu_{v}$$
### Chemical potential of surface
- Use the _canonical ensemble_ to obtain $\mu$ for a _fixed_ $N$
$$\displaylines{Z_{N}=\frac{N_{s}!}{(N_{s}-N)!N!}z_{s}^{N}\exp\left( \frac{N\epsilon}{k_{B}T} \right) \\ F=-k_{B}T\ln Z_{N} \\ \mu=\frac{\partial F}{\partial N}=-\varepsilon+k_{B}T\ln \frac{N}{(N_{s}-N)z_{s}}=-\varepsilon+k_{B}T\ln\left( \frac{\theta}{(1-\theta)z_{s}} \right)}$$
- Alternatively, consider the _grand canonical ensemble for a single site_
	- All sites are _independent_, consider one site as the system with _average occupation number_ $\theta$
	- Sites have _two states_, with occupancy $0$ or $1$
$$\displaylines{\Xi=\sum_\text{states}\exp[-\beta(E_{i}-\mu_{s}N_{i})]Z_\text{int}^{(i)}=1+z_{s}\exp[\beta(\epsilon+\mu_{s})] \\ \theta=-\left( \frac{\partial \Phi}{\partial \mu_{s}} \right)_{T,V}=\frac{z_{s}\exp[\beta(\epsilon+\mu_{s})]}{1+z_{s}\exp[\beta(\epsilon+\mu_{s})]}\\ \mu_{s}=-\varepsilon+k_{B}T\ln\left( \frac{\theta}{(1-\theta)z_{s}}\right)}$$
### The adsorption isotherm
- Chemical potential of an [[#Thermodynamic quantities|ideal gas]]
$$\mu_{v}=k_{B}T\ln\left( \frac{N\lambda^{3}}{V} \right)=k_{B}T\ln\left( \frac{p}{k_{B}T}\lambda^{3} \right)$$
- _Equating_ the chemical potentials:
$$p=\frac{\theta}{1-\theta} \frac{k_{B}T}{z_{s}\lambda^{3}}\exp(-\beta\epsilon)$$
### Kinetic argument
- Consider the _rates_ of _adsorption_ and _desorption_:
$$r_\text{ads}=k_{a}p(1-\theta)\hspace{1.5cm}r_\text{des}=-k_{d}\theta$$
- Equating:
$$p=\frac{\theta}{1-\theta} \frac{k_{d}}{k_{a}}$$
![[Langmuir isotherm.png]]
## Mixtures of an ideal gas
- Let there be a _total particle number_ $N$ and _total pressure_ $p$
- $N_i$ and $p_i$ of each _subsystem_ are _additive_:
$$\sum_i N_i=N\hspace{1.5cm}\sum_i p_i=p$$
- The [[#Thermodynamics of N particles in a box|ideal gas entropy]] of _each contribution_:
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

## Chemical reactions
- Let a _chemical reaction_ happen at _constant_ $T$ and $p$
- The _total change in Gibbs Free Energy_ $G$:
$$dG(p,T)=\sum_\text{species}\mu_i dN_i$$
- Incorporate _reaction coefficients_ $\nu_i$ 
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

## The high-temperature limit
- For the [[#The many-level system|quantum harmonic oscillator]], at _high temperatures_:
$$Z=\frac{1}{2\sinh(\beta\hbar\omega/2)}\approx\frac{kT}{\hbar\omega}$$
- However, treating it as a _continuous system_:
$$Z=\int\frac{dx\,dp}{2\pi\hbar}\exp\left(-\frac{p^2}{2mkT}-\frac{\kappa x^2}{2kT}\right)=\frac{1}{\lambda}\sqrt{\frac{2\pi kT}{\kappa}}$$
- This can only be true if the _size of the system_ $L$ is such that $\kappa L^2\gg kT$
- However, at the _high temperature limit_ where $\kappa L^2\ll kT$:
$$Z\approx\frac{L}{\lambda}$$

# The Fermi gas
- Given the _energy distribution_ $\varepsilon_k$:
$$\displaylines{\Xi_k=\sum_{n=0}^1\exp[-\beta(\varepsilon_k-\mu)n]=1+\exp[-\beta(\varepsilon_k-\mu)] \\ \Phi_k=kT\ln[1+\exp(-\beta\varepsilon_{k}+\beta \mu)] \\ \mean{n_k}=\frac{1}{\exp[\beta(\varepsilon_k-\mu)]+1}}$$
- At _absolute zero_:
$$\langle n_{\boldsymbol{k}} \rangle = \begin{cases}
1 &\varepsilon_{\boldsymbol{k}}<\mu \\ 0&\varepsilon_{\boldsymbol{k}}>\mu
\end{cases} $$

- The _entropy_ at _each level_:
$$S_{\boldsymbol{k}}(T,\mu)=-\left( \frac{\partial \Phi_{\boldsymbol{k}}}{\partial T} \right)_{V,\mu}=-k_{B}[\langle n_{k} \rangle \ln \langle n_{k} \rangle +(1-\langle n_{k} \rangle )\ln(1-\langle n_{k} \rangle ) ]$$
- It comes from _partially filled levels_
![[Fermi Dirac distribution.png|400]]

- The _total number of particles_:
$$N=\sum_k\mean{n_k}=\int\frac{\sigma\,d^3x\,d^3p}{(2\pi\hbar)^3}\frac{1}{1+\exp[\beta(\varepsilon_k-\mu)]}=\int  \, \frac{\sigma\, g(\varepsilon)\,d\varepsilon}{1+\exp[\beta(\varepsilon_{k}-\mu)]} $$
## At absolute zero

### Chemical potential
- There is often _no closed-form expression_ for $\mu$
- Its value must be _adjusted_ so the integral _always_ gives $N$
- At $T=0$, $\mu$ is defined as the _Fermi energy_

- Writing the _density of states_ $g(\varepsilon)$:
$$N=V\int_0^\infty g(\varepsilon)n(\varepsilon)\,d\varepsilon$$
- One can then use the _distribution at absolute zero_, up to the _Fermi energy_:
$$N=\frac{\sigma V}{4\pi^{2}} \left( \frac{2m}{\hbar^{2}} \right)^{3/2}\int_0^{\varepsilon_F} \sqrt{ \varepsilon}\,d\varepsilon=\frac{\sigma V}{4\pi^{2}} \left( \frac{2m}{\hbar^{2}} \right)^{3/2} \frac{2\varepsilon_{F}^{3/2}}{3}$$
- One then finds that the _Fermi energy_ is:
$$\mu(T\to 0)\equiv\varepsilon_F=\frac{\hbar^{2}}{2m}\left[ \left(\frac{6\pi^{2}}{\sigma}\right)\frac{N}{V} \right]^{2/3}$$
- As _temperature_ increases, and _higher energy_ states have higher $g(\varepsilon)$, $\mu$ _shifts to be lower_, eventually becoming _negative_
- Then in the [[#Classical limit]], it tends to the _Maxwell-Boltzmann_ distribution
$$n(\varepsilon)=\frac{1}{\exp[\beta(\varepsilon-\mu)]-1 }\longrightarrow \exp[-\beta(\varepsilon-\mu)]$$
![[Quantum gas mu.png]]

### Internal energy
- The _internal energy_ of the gas:
$$\begin{align}
U=\sum_k\varepsilon_k\mean{n_k}&=\sigma\int_0^\infty g(\varepsilon)\,d\varepsilon\frac{\varepsilon}{1+\exp[\beta(\varepsilon-\mu)]} \\ &= \frac{\sigma V}{4\pi^{2}} \left( \frac{2m}{\hbar^{2}} \right)^{3/2} \int _{0}^{\infty} \frac{\varepsilon^{3/2}\, d\varepsilon}{1+\exp[\beta(\varepsilon-\mu)]} 
\end{align}$$
- At _absolute zero_, evaluating the integral:
$$U|_{T=0}\propto V\left(\frac{N}{V}\right)^{5/3}$$
- This is _not a function of temperature_, as it is _evaulated_ at $T=0$
	- The _zero-temperature limit_ is _purely quantum_ as $N\lambda^3/V\to\infty$

### Fermi pressure
- When one _compresses_ the gas, due to the _Pauli principle_, the energies are _raised_, giving the _Fermi pressure_:
$$p_F=-\pd{U}{V}=(\text{const.} \sim 1)\frac{\hbar^2}{2m}\left(\frac{N}{V}\right)^{5/3}=-\frac{2}{3} \frac{U}{V}$$
- This is _not the actual pressure_, as $U|_{T=0}$ is _not a thermodynamic variable_
### Momentum representation
- Rewrite integrals in terms of _momentum_
$$N=\sigma V\int_0^{\varepsilon_F}\frac{p^2\,dp}{2\pi^2\hbar^3}=\sigma V\frac{k_F^3}{6\pi^2}$$
$$U=\sigma V\int_0^{\varepsilon_F}\frac{p^4\,dp}{2\pi^2(2m)\hbar^3}=$$
- One then also gets that the _momentum at the Fermi level_:
$$\hbar k_F=()^{1/3}\left(\frac{}{}\right)^{1/3}$$
- The _Fermi pressure_:
$$p_F=\frac{2}{5}\frac{N}{V}\varepsilon_F$$
## Away from absolute zero
- At $T>0$, the _chemical potential_ is _not equal_ to $\varepsilon_F$

### Grand potential and equation of state
- The _grand potential_ of the Fermi gas, using _integration by parts_ for the second equality:
$$\begin{aligned}\Phi&=V\int_0^\infty -k_{B}T\ln(1+\exp[-\beta(\varepsilon_k-\mu)])\,g(\varepsilon)\,d\varepsilon \\ &= -\frac{2}{3} \frac{\sigma V}{4\pi^{2}} \left( \frac{2m}{\hbar^{2}} \right)^{3/2} \int _{0}^{\infty} \frac{\varepsilon^{3/2}\, d\varepsilon}{1+\exp[\beta(\varepsilon-\mu)]}  \\ &=-\frac{2}{3}U\end{aligned}$$
- Using the formula $\Phi=-pV$
$$p= \frac{2}{3} \frac{\sigma }{4\pi^{2}} \left( \frac{2m}{\hbar^{2}} \right)^{3/2} \int _{0}^{\infty} \frac{\varepsilon^{3/2}\, d\varepsilon}{1+\exp[\beta(\varepsilon-\mu)]}$$
- This gives the _equation of state_ for the Fermi gas
### Sommerfeld expansion
- One can do _Taylor expansions_ with $1/(\beta\varepsilon_F)$
	- This is known as the _Sommerfeld expansion_
- For the integral:
$$\int_0^\infty \frac{A(\varepsilon)\,d\varepsilon}{\exp[\beta(\varepsilon-\mu)]+1}=\int_0^\mu A(\varepsilon)\,d\varepsilon+\frac{\pi^2}{6}(kT)^2A'(\mu)+\dots$$

- Applying this to _internal energy_:
$$\int_0^\infty\frac{\varepsilon\,g(\varepsilon)\,d\varepsilon}{\exp[\beta(\varepsilon-\mu)]+1}=\int_0^\mu\,\varepsilon g(\varepsilon)\,d\varepsilon+\frac{\pi^2}{6}(kT)^2[g(\mu)+\mu g'(\mu)]$$
- The _first term_ can be _expanded_:
$$\int_0^{\varepsilon_F}\varepsilon g(\varepsilon)\,d\varepsilon+(\mu-\varepsilon_F)\varepsilon_F\,g(\varepsilon_F)+\dots$$
- Expand $U$ with _correction terms_:
$$U=U(T=0)+\mathcal{O}(T)^{2}$$

### Correction terms
- Looking at _total number of particles_:
$$\displaylines{N=\int_0^\infty \frac{g(\varepsilon)}{\exp[\beta(\varepsilon-\mu )]+1}\,d\varepsilon \\ \frac{dN}{dT}=0=\frac{d\mu}{dT}g(\mu)+\frac{\pi^2}{3}k^2Tg'(\mu)=0}$$
- One then gets an _expression_ for $\mu$:
$$\mu(T)=\varepsilon_F-\frac{\pi^2}{6}(k_{B}T)^2\frac{g'(\varepsilon_{F})}{g(\varepsilon_{F})}$$
- Substituting in the corrections:
$$U(T)=U(T=0)+\frac{\pi^2}{6}(kT)^2g(\varepsilon_F)+\mathcal{O}(T^{4})$$
- This then gives the _heat capacity_:
$$C=\pd{U}{T}=\frac{\pi^2}{3}k^2g(\varepsilon_F)T$$

- Alternatively, consider the _grand potential_:
$$\Phi=-\frac{2}{3}U=\Phi(0)-\frac{\sigma V}{24}(k_{B}T)^{2} \left( \frac{2m}{\hbar^{2}} \right)^{3/2}\varepsilon_{F}^{1/2}$$
- The _entropy_ is then:
$$S=-\left( \frac{\partial \Phi}{\partial T} \right)_{\mu,V}=\frac{k_{B}^{2}T}{3} \frac{V}{2} \left( \frac{2m}{\hbar^{2}} \right)^{3/2} \sqrt{ \varepsilon_{F} }=\frac{\pi^{2}}{3}g(\varepsilon_{F})k_{B}^{2}T$$
- The heat capacity formula can also be obtained from $T(\partial S/\partial T)$
- Application: [[Solids#Heat capacity|heat capacity of electrons in metals]]

## At high temperatures
- [[#Classical limit]]:
$$\frac{N\lambda^3}{V}\ll1 \hspace{1.5cm}\mu=kT\ln\frac{N\lambda^3}{V}$$
- The _grand potential_:
$$\Phi=-\frac{2}{3}U=-\frac{2}{3}\sigma\int _{0}^{\infty} \frac{\varepsilon g(\varepsilon)\, d\varepsilon}{\exp(\beta\varepsilon)+\exp(\beta \mu)}\exp(\beta \mu) $$
- _Ignore_ the $\exp(\beta \mu)$ in the denominator (leading order term)
- Making the substitution $x=\beta\varepsilon$
$$\Phi=-\frac{2\sigma}{3}V\exp(\beta\mu) \frac{\sqrt{ 2 }m^{3/2}}{\pi^{2}\hbar^{3}}I \hspace{1cm}I=\int _{0}^{\infty} \frac{x^{3/2} \, dx}{e^{x}} =\frac{3\sqrt{ \pi }}{4}$$
- This leads to the result for the [[#The ideal gas in the grand canonical ensemble|classical ideal gas]]:
$$\Phi=-kT \frac{V}{\lambda^{3}} \exp(\beta \mu) \hspace{1.5cm}pV=NkT$$

- Considering the _first order term_ as well
$$\Phi=\Phi_\text{ideal}(1-0.2\exp(\beta\mu)+\dots)$$
- There is a _quantum correction_ to the ideal gas law
	- Derived from the [[Density matrices#Quantum corrections to the ideal gas law|density matrix formalism]]
	- Correction $\sim N\lambda^{3}/V$
$$p=\frac{NkT}{V}\left( 1+\frac{\pi^{3/2}}{4} \frac{N\hbar^{3}}{V(mk_{B}T)^{3/2}} \right)$$
# The Bose gas
$$\displaylines{\Xi_k=\sum_{n=0}^\infty\exp[-\beta(\varepsilon_k-\mu)n]=\frac{1}{1-\exp[-\beta(\varepsilon_k-\mu)]} \\ \Phi_k=kT\ln[1-\exp(-\beta\varepsilon_k+\beta\mu)] \\ \mean{n_k}=\pd{\Phi_k}{\mu}=\frac{1}{\exp[\beta(\varepsilon_k-\mu)]-1}}$$
- Number of particles in a _real gas_:
	- For some _elementary excitations_, $\mu(T)=0$ and $N$ can vary
$$N=\int _{0}^{\infty} n(\varepsilon)g(\varepsilon) \, d\varepsilon =\frac{\sigma V}{4\pi^{2}} \left( \frac{2m}{\hbar^{2}} \right)^{3/2} \int _{0}^{\infty}  \frac{\sqrt{ \varepsilon }\, d\varepsilon}{\exp[\beta(\varepsilon-\mu)]-1} $$

- The _total grand potential_, similar to the _Fermi gas_:
$$\begin{aligned}\Phi&=-\int\frac{d^3x\,d^3p}{(2\pi\hbar)^3}k_{B}T\ln[1-\exp[-\beta(\varepsilon_k-\mu)]] \\ &=-\frac{2}{3}U\end{aligned}$$

- Entropy for each level:
$$S_{\boldsymbol{k}}=-\left( \frac{\partial \Phi_{\boldsymbol{k}}}{\partial T} \right)_{\mu,V}=-k_{B}[\langle n_{\boldsymbol{k}} \rangle \ln \langle n_{\boldsymbol{k}} \rangle -(1+\langle n_{\boldsymbol{k}} \rangle )\ln(1+\langle n_{\boldsymbol{k}} \rangle ) ]$$

- Compare with the Fermi gas:
	- They both _tend to_ the Maxwell-Boltzmann distribution at high energies
![[Fermi and Bose distributions.png]]
- The Bose gas occupation number will always _diverge_ at $\varepsilon=\mu$
- For $N$ to be _well-defined and finite_, $\mu$ must always _remain negative_
	- _Classical limit_: $\beta \mu$ is large and _negative_
- As temperature _decreases_, $\mu$ must then be _less negative_ to preserve $N$

## Bose-Einstein condensation at low temperatures
- Take the quantum limit:
$$\frac{N\lambda^3}{V}\sim1$$
- For _bosons_, multiple particles can _occupy the same quantum state_
- Therefore there are _many particles in the $\varepsilon=0$ state_, where they can form a _condensate_
	- The rest of the particles are said to be _excited_
	- For a _isolated system of bosons_, $T,p,\mu$ are _uniform

- At some _low temperature_, even if $\mu$ is _adjusted_, the _area_ under $\langle n_{\boldsymbol{k}} \rangle$ _cannot be conserved_, so _particles_ must then be _condensing_ into the _ground state_
	- Cannot be conserved without making $\mu$ _positive_

- At $T=0$, all particles must be in the ground state:
$$\lim_{ T \to 0} n_{\varepsilon=0}=\lim_{ T \to 0 } \frac{1}{\exp(-\beta \mu)-1}=N $$
- In the _low temperature limit_, one gets:
$$\mu\approx-\frac{kT}{N}$$
- As expected, $\mu\approx 0$ for low temperatures, then becomes _large and negative at high temperatures_ (Classical limit)
![[Bose chemical potential.png|250]]
- _Separate_ the system into the condensate and the excited levels, it takes _zero energy_ to move particles _between_ the subsystems
- Hence $\mu=0$ throughout the gas _when there is a condensate_

- If the _dispersion relation_ goes to _negative energies_, it is _unphysical_, so particles _pile up_ at $\varepsilon=0$ instead

- The _number of particles_ in the excited gas (_not the condensate_), setting $\mu=0$:
$$N-N_c=\frac{\sigma V}{4\pi^{2}} \left( \frac{2mk_{B}T}{\hbar^{2}} \right)^{3/2} \int _{0}^{\infty}\frac{\sqrt{ x } \, dx}{e^{x}-1}=2.612 \frac{\sigma V}{\lambda^{3}}\equiv N\left( \frac{T}{T_{0}} \right)^{3/2} $$
- There is a _critical temperature_ $T_{0}$, above which there is _no condensation_
![[Condensation.png|400]]
- The condensation is a _second-order phase transition_

### In two dimensions
- In _two dimensions_, $g(\varepsilon)$ is _constant_
$$N-N_{c}=\frac{Am}{2\pi \hbar^{2}} \int _{0}^{\infty} \, \frac{d\varepsilon}{\exp(\beta\varepsilon)-1} $$
- The integrand _diverges_ as $\varepsilon\to 0$
- The _critical temperature_ $T_c=0$

- One _can only have Bose-Einstein condensates for_ dimensions $d\geq3$
- There _cannot be an ordered phase_
	- The _Landau-Peierls instability_

- In 2D, the gas is also _sensitive to perturbations_
- One can have _potential traps_ of depth $\Delta$ in a 2D gas, which form a _condensate_ with $T_c\neq0$ and $\mu=-\Delta$

## Experimental signatures of Bose-Einstein condensation
### Energy and heat capacity
- Only the _excited atoms_ will contribute to energy
$$U=\int _{0}^{\infty} \frac{\varepsilon g(\varepsilon)\, d\varepsilon}{\exp[\beta(\varepsilon-\mu)]-1} = \frac{\sigma V}{4\pi^{2}}  \left( \frac{2m}{\hbar^{2}} \right)^{3/2} \int_{0}^{\infty} \frac{\varepsilon^{3/2}  \, d\varepsilon}{\exp[\beta(\varepsilon-\mu)]-1}  $$
- _Below_ the critical temperature, $\mu=0$ and substituting for a dimensionless integral:
$$U\approx \frac{2\sigma V}{\lambda^{3}} k_{B}T\propto T^{5/2} \hspace{1.5cm}C_{V}\propto T^{3/2}$$
- At $T\gg T_{0}$, it approaches the _classical regime_ of $C_{V}=3Nk_{B}/2$
- Example: $\ce{ ^4He }$
	- Also has _inter-atomic_ forces not accounted for in this model
![[4-He heat capacity.png]]

### Momentum distribution
- The _ground state_ atoms have $k=0$
- There is a _sharp peak_ in the _momentum distribution_ where $k=0$
## Blackbody radiation
- Photons have _integer angular momentum_, hence will obey _Bose statistics_

- Photons are _non-interacting_, and can be _absorbed/emitted_ by a reservoir, changing $N$
- Absorption/emission takes place _until thermal equilibrium is reached_, where $F$ is _minimised_ at some value of $N$:
$$\left( \frac{\partial F}{\partial N} \right)_{T,V}=0$$
- Hence, $\mu=0$ for photons

- The Bose-Einstein distribution becomes the _Planck distribution_
$$\langle n_{\boldsymbol{k}} \rangle = \frac{1}{\exp(\beta \hbar\omega_{\boldsymbol{k}})-1} $$
- Photons obey the _dispersion relation_ $\omega=ck$
- The _phase space element_, accounting for $2$ available _polarisations_:
$$g(\varepsilon)\,d\varepsilon=\frac{2V}{8\pi^{3}} 4\pi k^{2}\,dk=\frac{V}{\pi^{2}c^{3}}\omega^{2}\,d\omega$$
- Differs from real gas due to $m=0$
	- Makes it so that _classical limit is impossible_ since $\lambda \to 0$

- The _energy distribution_ of black-body radiation:
$$E_{\omega}\,d\omega=\frac{V}{\pi^{2}c^{3}} \frac{\hbar\omega^{3}\,d\omega}{\exp(\beta \hbar\omega)-1}$$
- The _Planck distribution law_:
![[Planck distribution.png|400]]
- The _total energy density_ is then:
$$u=\frac{U}{V}=\frac{1}{V}\int _{0}^{\infty}E_{\omega} \, d\omega=\frac{\pi^{2}k_{B}^{4}}{15\hbar^{3}c^{3}}T^{4} $$
- The _Stefan-Boltzmann law_
- As $T\to 0$, the _number of photons_ in the cavity also goes to zero

- The _mean number of photons_ in a frequency interval:
$$N(\omega)\,d\omega=\frac{V}{\pi^{2}c^{3}} \frac{\omega^{2}\,d\omega}{\exp(\beta \hbar\omega)-1}$$

## Elementary excitations
- For _interacting systems_, one can describe _excitations_ from the ground state as some _non-interacting quasi-particles_, arising as _collective behaviour_
	- Example: [[Solids#Fermi liquid theory|Fermi liquids]]

- _Elementary excitations_ are characterised by _zero rest mass_
	- Hence $\lambda\to 0$, always in quantum regime

### Phonons
- _Interatomic interactions_ can be approximated as _harmonic_ for small displacements
- _Eigenstates_ of a lattice are _plane waves_ called [[Solids#One-dimensional models|phonons]]
	- Dispersion relation: _linear_ for small wave-number, _flattens off_ at the edge of the BZ

- The _Debye model_ assumes a _linear dispersion_:
$$\omega=ck$$
- The "average" speed of sound:
$$\frac{3}{c^{2}}=\frac{1}{c_{L}^{2}}+\frac{2}{c_{T}^{2}}$$
- Up to some _cut-off_ such that there are $3N$ modes for $N$ atoms
### Spin waves
- Dispersion relation:
$$\varepsilon_{\boldsymbol{k}}=\alpha k^{2}$$
- Similar to the _classical gas_, but following the _Bose distribution_
# Non-ideal gases and liquids
- Stay purely in the _classical regime_

## Pair interactions
- For each _pair of particles_, let there be some _potential_ between them
- A typical inter-particle potential:
![[Pair interaction potential.png|400]]

- The _Hamiltonian_ is:
$$H=\sum_i\frac{p_i^2}{2m}+\sum_{j>i}\phi(r_{ij})$$
- The _partition function_ can be _broken_ into the _ideal_ part and the _configurational_ part:
$$\begin{aligned}Z_N&=\frac{1}{N!}\left[\prod_{i=1}^N\int\frac{d^3p_i}{(2\pi\hbar)^3}\exp\left(-\frac{\beta p_i^2}{2m}\right)\right]\left[\prod_i\int d^3r_i\exp\left(\sum_{j>i}-\beta\phi(r_{ij})\right)\right] \\ &=\frac{1}{N!}\left(\frac{1}{\lambda^3}\right)^NZ_\phi\end{aligned}$$

- Define some _two-particle probability_, or the probability of finding 2 particles at $\bm{r}_1$ and $\bm{r}_2$
	- Single particle $p_i=\exp(-\beta E_i)$
$$P_2(\bm{r}_1,\bm{r}_2)=\frac{N(N-1)}{Z_\phi}\int\exp\left(\sum_{j>i}-\beta\phi(r_{ij})\right)\,d^3r_3\dots d^3r_N$$
- $N(N-1)$ is a _normalisation factor_ to account for the _number of possible pairs_
- It must _only depend on_ $r_{12}=|\bm{r}_1-\bm{r}_2|$ (translational invariance)

- The probability has a _dimensionality_ $n^2=(N/V)^2$, where $n$ is _number density_

- For _low densities_, due to _long range of interactions_:
	- Numerator integral: particles $3\dots N$ are _far away_ from each other, and $1,2$ such that $\phi \approx 0$ apart from $\phi(r_{12})$
	- $Z_{\phi}$: all particles are _far away_ from each other
$$P_2(\bm{r}_1,\bm{r}_2)\approx\frac{N^2}{V^2}\exp[-\beta\phi(r_{12})]$$

- Define the _radial distribution function_ (which is _dimensionless_)
$$g(r_{12})=\frac{V^2}{N^2}P_2(\bm{r}_1,\bm{r}_2)\approx\exp[-\beta\phi(r_{12})]$$
- _Forms_ of $g(r)$ in different substances:
	- Example: _Lennard-Jones potential_
![[Radial distribution functions.png|400]]
- For all materials, $g(r\ll\sigma)$ will be zero due to _hard core repulsion_
- For _liquids and gases_, there will be an _initial peak_ due to _nearest neighbours_
	- Gases: then _evens out_ as there is _no correlation_ between far-away particles
	- Liquids: also a _second peak_ due to a _second shell_ of particles
## Internal energy with pair interactions
- $T,V,N$ are _not natural variables_ of $U$
- Hence, one _does not have enough thermodynamic information_ from the above
	- One can still get _heat capacity_

- One can still get:
$$U=\frac{3}{2}NkT-\pd{}{\beta}\ln Z_\phi$$
- The _kinetic energy contribution_ remains _unchanged_

- By _summing over all pairs_:
$$-\pd{}{\beta}\ln Z_\phi=\frac{N(N-1)}{2Z_\phi}\int\phi(r_{12})\exp[-\beta\phi(r_{12})]\,d^3r_1\,d^3r_2\dots d^3r_N$$
- Writing $d^3r_1\,d^3r_2$ as $d^3(r_1-r_2)\,d^3r_2$, one can substitute the _pair distribution function_ to find:
$$U=\frac{3}{2}NkT+\frac{1}{2}\frac{N^2}{V}\int_0^\infty\phi(r)g(r)\,4\pi r^2\,dr$$
- This is an _expansion_ of $U$ in _powers of density_ $N/V$, accounting for _pair interactions_
	- _Higher order terms_ will need to account for _more interactions_

- Any expansion in powers of density is known as a _virial expansion_
## Virial Theorem
- Given particles of position $\bm{r}_i$ and forces $\bm{f}_i$, the _virial_ of the system is defined as:
$$\mathcal{V}=\sum_i-\frac{1}{2}\bm{r}_i\cdot\bm{f}_i$$
- Writing out the force with Newton's second law:
$$\mathcal{V}=\sum_i-\frac{1}{2}\bm{r}_i\cdot \left(m_i\frac{d\bm{v}_i}{dt}\right)=-\frac{1}{2}\sum_im
_i\frac{d}{dt}(\bm{r}_i\cdot\bm{v}_i)+\frac{1}{2}\sum_im_iv_i^2$$
- By _averaging_ the virial, one gets rid of the time derivative due to _fluctuations_:
$$\mean{\mathcal{V}}=\frac{1}{2}\sum_im_i\mean{v_i^2}=\frac{3}{2}NkT=\langle \mathcal{T} \rangle $$
- This is the _virial theorem_

- The virial can be due to _external forces_, which could be the _forces from a wall_:
$$\mean{\mathcal{V}_\text{ext}}=-\frac{1}{2}\sum_i\mean{\bm{r}_i\cdot\bm{f}_i}=\frac{1}{2}\oint \bm{r}\cdot\,(p\,d\bm{A})=\frac{p}{2}\int\div\bm{r}\,dV=\frac{3}{2}pV$$
- For an _ideal gas_, by equating the virials, one recovers the _ideal gas law_

### Accounting for pair interactions
- The _internal virial_ from pair $i,j$, using the fact that $f_{ij}=-f_{ji}$
$$\mean{\mathcal{V}_\text{int}}_{ij}=-\frac{1}{2}\mean{r_if_{ij}+r_jf_{ji}}=\frac{1}{2}(r_i-r_j)\pd{\phi_{ij}}{(r_i-r_j)}$$
- The _average_ contribution from _particle_ $i$ is then written as:
$$\mean{\mathcal{V}_\text{i}}=\frac{1}{2}\sum_{i\neq j}\mean{r_{ij}\pd{\phi}{r_{ij}}}=\frac{1}{2}\int r \frac{\partial \phi}{\partial r}ng(r)\,4\pi r^{2}\,dr$$
- For the _whole_ gas, it is multiplied by $N/2$ to avoid _double counting_
- The final result:
$$\mean{\mathcal{V}_\text{int}}=\frac{N^2}{4V}\int_0^\infty g(r)\,r\pd{\phi}{r}\,4\pi r^2\,dr$$
- Adding back the _external virial_ from the _container_:
$$\mean{\mathcal{V}}=\frac{3}{2}NkT=\frac{3}{2}pV+\frac{N^2}{4V}\int_0^\infty g(r)\,r\pd{\phi}{r}\,4\pi r^2\,dr$$
### Virial equation of state
- One then gets the _virial equation of state_:
$$p=\frac{NkT}{V}-\frac{N^2}{6V^2}\int g(r)\pd{\phi}{r}\,4\pi r^3\,dr$$
- This _cannot be obtained from_ $U$, and must be derived _independently_

- This is another _virial expansion_, only taking _pair interactions_ into account and hence only going into _second order_

## Virial expansion
- The general virial expansion:
$$p=B_1(T)n+B_2(T)n^2+\dots$$
- From the expansion above:
$$\displaylines{B_1=kT \\ B_2=-\frac{1}{6}\int_0^\infty r\,g(r)\pd{\phi}{r}\,4\pi r^2\,dr}$$
- Substituting $g=\exp(-\beta\phi)$, and integrating _by parts_
	- By parts: convert interval term to integral over $r$ from $0$ to $\infty$
$$B_2=\frac{1}{2}\int_0^\infty [1-\exp(-\beta\phi)]4\pi r^2\,dr$$

- Modelling $\phi$ as a _hard sphere_:
$$\displaylines{\phi(r)=\begin{cases}\infty&r<R \\ 0&r>R\end{cases}\\ B_2=\frac{1}{2}\left(\frac{4\pi}{3}R^{3} \right)}$$
- If the potential is a _well_
	- In the _repulsive part_, there is a _positive contribution_ to $B_2$
	- In the _attractive part_, there is a _negative contribution_ to $B_2$
- Example: Lennard-Jones
![[B2(T).png|400]]
- At _low temperatures_, the gas is _easier_ to compress due to _long-range attractions_
- At _high temperatures_, the gas is _harder_ to compress due to _short-range repulsion_

- At the _Boyle temperature_ $T_b$, $B_2(T=T_b)=0$
- The gas resembles an _ideal gas_ as the _attractions and repulsions cancel out_

### (Poor) approximation of pair interaction energy
- Simply _sum over_ interacting pairs, using an _average pair potential_
$$U_\text{pair}=\sum_{i>j}\phi(r_{ij})\approx \frac{N^{2}}{2}\left[ \frac{1}{V}\int \phi(r) \, d^{3}r  \right]$$
- In the _limit_ $\beta \phi\ll 1$:
$$U_\text{pair}\approx \frac{N^{2}}{V}k_{B}TB_{2}(T)$$
## Van der Waals gas
- Due to _fluctuations_ in the _dipole moments_ of each particle, the pair interaction is:
$$\phi\sim-\frac{A}{r^6}$$
- The _total potential energy_:
$$\sum_{i,j}\frac{1}{2}\phi(r_{ij})=\frac{N(N-1)}{2}\frac{1}{V}\int_R^\infty \phi(r)\,d^3r\sim -\frac{\varepsilon N^2}{V}$$

- The _excluded volume effect_:
$$Z(N)=\frac{1}{N!}\left(\frac{1}{\lambda^3}\right)^N\prod_i\int d^3r_i\exp\left(-\beta\sum\phi_{ij}\right)$$
- Extracting the _total potential energy_, and taking into account the _excluded volume_ $b$ for each particle:
$$Z(N)=\frac{1}{N!}\left(\frac{1}{\lambda^3}\right)^N\exp\left(\beta\frac{\varepsilon N^2}{V}\right)(V-Nb)^N$$
- The _free energy_:
$$F=-k_{B}T\ln\left[ \frac{1}{N!} \frac{1}{\lambda^{3N}} \right]-Nk_{B}T\ln(V-Nb)-\frac{N^{2}}{V}\varepsilon$$
- This gives the pressure:
$$p=-\pd{F}{V}=\frac{NkT}{V-Nb}-\varepsilon\frac{N^2}{V^2}$$
- This is the _Van der Waals equation of state_

- As a _virial expansion_:
$$p\approx\frac{NkT}{V}+\frac{N^2}{V^2}(bkT-\varepsilon)$$
- The second virial coefficient:
$$B_2=bkT-\varepsilon$$

# Phase equilibria and transitions
- In a _van der Waals gas_, one can find _phase behaviour_ between _liquid and gas_
	- One can draw a _phase diagram_
	- Phase boundaries given by _Clausius-Clapeyron relation_

- In Bose gases, there can be a _condensate phase_

- One can characterise phases with an _order parameter_

- _Scalar_ order parameters
	- Liquid-gas: _difference in density_
	- Binary mixture: _difference in concentration_
- _Vector_ order parameter
	- Array of magnetic dipoles: _magnetisation_
- _Quadrupolar_ order parameter
	- Liquid crystal: _degree of alignment_ $\mean{3\cos^2\theta-1}/2$

## The binary mixture
- Let there be two species, $A$ and $B$:
$$\displaylines{N=N_A+N_B \\ \phi_A=\frac{N_A}{N}\hspace{1.5cm}\phi_B=\frac{N_B}{N}=1-\phi_A}$$
- The [[#Mixtures of an ideal gas|entropy of mixing]]:
$$\Delta S_\text{mix}=-Nk_B[\phi\ln\phi+(1-\phi)\ln(1-\phi)]$$
- Account for _pair interactions_, using the [[#(Poor) approximation of pair interaction energy|second virial coefficient]]
	- Same particle: they are _indistinguishable_, giving factor of $1/2$
	- The $\varepsilon$ parameter accounts for _coordination number_ as well
$$\displaylines{U_{AA}\approx \frac{N_{A}^{2}}{V}k_{B}TB_{2}(AA)\approx N\varepsilon_{AA}\phi^{2} \\ U_{BB}\approx N\varepsilon_{BB}(1-\phi)^{2} \\ U_{AB}=2N\varepsilon_{AB}\phi(1-\phi)}$$
- The _difference in internal energy from mixing_:
	- First collection of terms: pair interaction in _mixed state_
	- Second collection of terms: pair interactions in the _phase-separated state_ (number of neighbours of $A$ does not depend on $\phi$ anymore)
	- Factor of 2 accounted for in _interaction energy_
	- Use a _mean-field_ approximation for a uniform value of $\phi$
$$\begin{aligned}\Delta U_\text{mix}&=N[\varepsilon_{AA}\phi^2+\varepsilon_{BB}(1-\phi)^2+2\varepsilon_{AB}\phi(1-\phi)] -N[\varepsilon_{AA}\phi+\varepsilon_{BB}(1-\phi)] \\ &=Nk_BT\chi\phi(1-\phi)\end{aligned}$$
- Define the _Flory parameter_ $\chi$ quantifying the _differences in interaction energy_
$$\chi=\frac{1}{k_BT}[2\varepsilon_{AB}-\varepsilon_{AA}-\varepsilon_{BB}]$$
- A _positive_ parameter means $A$ and $B$ are likely to _repel_ each other and _de-mix/phase separate_

- The _difference in free energy_:
$$\begin{aligned}\Delta F_\text{mix}&=\Delta U_\text{mix}-T\Delta S_\text{mix} \\ &=NkT[\phi\ln\phi+(1-\phi)\ln(1-\phi)+\chi\phi(1-\phi)]\end{aligned}$$
![[Phase separation.png]]
- As expected, for _small or negative_ $\chi$, it is favourable to _mix_

- For _large_ $\chi$, the mixture tends to _phase-separate_ as there are _multiple minima in free energy_

### The binodal and spinodal
- Number of _extrema in free energy_:
$$\pd{F}{\phi}=\chi(1-2\phi)-\ln\left(\frac{1-\phi}{\phi}\right)=0$$
- For _large_ $\chi$, there is a _maximum_ at $\phi=1/2$, and _two minima_
- For _small_ $\chi$, there is only a _minimum_ at $\phi=1/2$
- The _locus_ of _minima_ $\phi^{*}(\chi)$ form the _binodal line_ (often plotted as $\chi(\phi^{*})$)

- The _stability_ of the extrema:
$$\pd{^2F}{\phi^2}=-2\chi+\frac{1}{\phi(1-\phi)}$$
- For _large enough_ $\chi$, the extremum at $\phi=0.5$ will become _unstable_
- At some point, it transitions to some _stable region_ near the minima
![[Phase stability.png]]

- The _line of inflection points_:
$$\chi=\frac{1}{2\phi(1-\phi)}$$
- This forms the _spinodal_

- The binodal and spinodal:
![[Binodal and spinodal 1.png]]
- They _touch_ at a _critical point_ at $\phi=1/2, \chi=2$

- The region _below the binodal_ is _stable_
- The region _above the spinodal_ is _unstable_ and tends to phase separate
	- The _final concentrations of phases_ are on the _binodal_
	- The region _between_ is _metastable_ due to an _energy barrier_

### The T-c phase diagram
- Use the fact that $T\sim 1/\chi$
![[Phase separation T-c.png]]
- The region _below the spinodal_ is _unstable_ and will phase-separate
	- The _final concentrations of phases_ are on the _binodal_
- One can _change stability of the mixture_ by simply _raising/lowering the temperature_
	- By _lowering temperature_, the entropy of mixing makes it _less favourable_

- _Critical temperature_

### Expansion of free energy from equilibrium
- For a small perturbation in $\phi$, _expand_ the free energy from some _initial_ concentration $\phi_X$, where the system is in _equilibrium_
$$\displaylines{F(\phi)=NkT[\phi\ln\phi+(1-\phi)\ln(1-\phi)+\chi\phi(1-\phi)] 
\\ \rho=\phi-\phi_X \\ \frac{F(\phi)-F(\phi_X)}{NkT}\approx-\frac{1-2\chi\phi_X(1-\phi_X)}{2\phi_X(1-\phi_X)}\rho^2-\frac{1-2\phi_X}{6\phi_X^2(1-\phi_X)^2}\rho^3+\frac{1-3\phi_X+3\phi_X^2}{12\phi_X^3(1-\phi_X)^2}\rho^4}$$

- There is _no linear term_
	- At $F(\phi_X)$, the system is in _equilibrium_

- For $\phi_X=1/2$, the _cubic term disappears_
	- Determines the _symmetry_ of the expansion

- The _sign and magnitude_ of the _quadratic term_ can _change with $\chi$
- Its sign determines _stability_
	- For a _positive_ term, it is _stable_
	- For a _negative term_, the perturbation _grows_

- The _quartic term_ is _always positive_
	- Makes sure the perturbation _does not go to infinity_

### From the critical point
- At this _critical point_ $\phi_X=1/2$:
$$\frac{F(\phi)-F(\phi_X)}{NkT}=(2-\chi)\rho^2+\frac{1}{6}\rho^4$$
- Point where the system again reaches _equilibrium_ after the perturbation:
$$\rho_\text{eq}=\sqrt{3(\chi-2)}$$
- This _only exists for $\chi>2$_
	- Phase separation _from the critical point_ is _possible_
	- A _negative quadratic term_
- There is a _continuous change in the equilibrium_
	- Said to be _second order_

- _Away_ from the critical point, there is a _discontinuous change_ in the equilibrium value
	- Said to be _first order_

## Landau theory
- For any system, identify an _order parameter_, a _macroscopic quantity_ which will _change value_ at a phase transition
	- Scalar: _density_
	- Vector: _magnetisation_
- Assume that _near a critical point_, the order parameter is _small_
- One can then do a _Taylor expansion_ of free energy
	- The coefficients are then dependent on _temperature_

$$F=F_0+A\rho^2+B\rho^3+C\rho^4$$
- In _equilibrium_, $F$ is a minimum, hence there is _no linear term_
	- Unless there is some _external field_ (e.g. magnetic)

- $A,B,C$ are _functions of temperature_
- Considering the behaviour _near the critical point_, write the coefficients as:
$$F=F_0+a(T-T_c)\rho^2-b\rho^3+c\rho^4$$

### Second-order phase transitions
- When there is _no cubic term_, the free energy describes a _second-order phase transition_ as the equilibrium values evolve _continuously across the transition_
$$\Delta F=a(T-T_c)\rho^2+c\rho^4$$

- At equilibrium, $\partial F/\partial \rho=0$:
$$\rho_\text{eq}=\pm\sqrt{-\frac{a(T-T_c)}{2c}}$$
- At $T<T_c$, it _branches into separate values_
- At $T>T_c$, it _remains at zero_

- One can find $F_\text{eq}$ and $S_\text{eq}$ as a function of $T<T_c$:
$$F_\text{eq}=-\frac{a^2(T-T_c)^2}{4c}\hspace{1.5cm}S_\text{eq}=$$

- There is a _discontinuity in heat capacity_ at $T=T_c$
- The discontinuity in _second derivative of free energy_ classifies this as _second-order_

### First-order phase transitions
$$\Delta F=a(T-T_c)\rho^2-b\rho^3+c\rho^4$$
- At some temperature $T_1>T_c$, separate _minima and maxima_ will develop for $F>F_0$ at some $\rho>0$
- This minimum will then move _lower_, until $T=T^*$, where $\Delta F=0$ at that minmum
- Then at $T=T_c$, the curve _flattens at $\rho=0$_
- Then the "external" minimum becomes the _only stable equilibrium_ for $T<T_c$

- Extrema of the free energy, for _non-zero_ $\rho$:
$$\displaylines{4c\rho^2-3b\rho+2a(T-T_c)=0 \\ \rho_\pm=\frac{3b}{8c}\pm\frac{\sqrt{9b^2-32ac(T-T_c)}}{8c}}$$
- This gives the _non-zero extrema_ as long as:
$$T<T_1\hspace{1.5cm}9b^2=32ac(T_1-T_c)$$
- At $T=T_c$, $\rho_-=0$, meaning the _maximum is at $\rho=0$_

- At $T^*$, where $T_c<T^*<T_1$, $\Delta F(\rho_+)=0$
- There is a _discontinuous jump in equilibrium order parameter_ at $T=T^*$
- There is still a _metastable state_, as there is a _barrier_ to the new equilibrium
	- The system is _supercooled_ for $T^*\leq T<T_c$

- Plot the _most stable free energy_ as a function of $T$
- There is a _jump in entropy_ (the first derivative)
- Hence, it is a _first-order phase transition_
	- Also features the _jump in order parameter_
	- There is a _latent heat_ $L=T\Delta S$

- The _accuracy_ of the expansion depends on the _magnitude of the jump_

### Variations on the expansion
- With an _external field_ (e.g. a _magnetic field_)
$$\Delta F=-h\rho+a(T-T_c)\rho^2-b\rho^3+c\rho^4$$

- A _negative quartic term_:
$$\Delta F=a(T-T_c)\rho^2-c\rho^4+d\rho^6$$
- This also creates a _first-order phase transition_ but with only _even powers_

## Ising model

### Mean-field approximation
$$H=-m_{0}B\sum_{i}\sigma_{i}-J\sum_{<ij>}\sigma_{i}\sigma_{j}$$
- Mean field:
$$H=-m_{0}B\sum_{i}\sigma_{i}-J\sum_{<ij>}(\braket{ \sigma } +\delta\sigma_{i})(\braket{ \sigma } +\delta\sigma_{j})$$
### Critical behaviour

# Fluctuations
- Theories such as _Landau theory_ are based on some _order parameter_, which applies _throughout the medium_
- It is a _mean field theory_, which neglects _fluctuations_ in equilibrium
- Near a _critical point_, fluctuations should _grow_

- In equilibrium, the system is presumed to be in the _most probable microstate_
- Equilibrium is achieved by _fluctuations_, which _eventually tend toward equilibrium_ due to the energy landscape
	- A _metastable state_ will need many fluctuations to achieve _true equilibrium_

## From the Boltzmann distribution
- Given some _thermodynamic variable_ $x$, $\mean{\Delta x}=0$
- The _magnitude_ of fluctuations is measured by:
$$\mean{\Delta x^2}=\mean{x^2}-\mean{x}^2=\frac{1}{Z}\sum_i x_i^2\exp\left(-\beta E_i\right)-\left[\frac{1}{Z}\sum_i x_i\exp\left(-\beta E_i\right)\right]^2$$
- Let the [[#Thermodynamic variables|conjugate variable]] to $x$ be $f$:
$$\Delta E_i=-f\cdot \Delta x_i$$
- Writing the terms above as derivatives w.r.t. $f$:
$$\displaylines{\langle x \rangle =\frac{1}{\beta Z}\left( \frac{\partial Z}{\partial f} \right) \\ \langle x^{2} \rangle =\frac{1}{Z\beta^{2}} \frac{\partial^{2}Z}{\partial f^{2}} \\ \mean{\Delta x^2}=kT\pd{\mean{x}}{f}}$$

## As curvature of availability
- Consider the _total entropy_ of a _system_ connected to a _reservoir_:
$$\displaylines{S_\text{tot}(x,U_\text{tot})=k\ln\Omega(x,U_\text{tot}) \\ P(x)\propto\exp[S_\text{tot}/k]}$$
- Using the definition of [[#Reservoir and availability|availability]]:
$$\displaylines{dA=-T\,dS_\text{tot} \\ P(x)\propto\exp\left[-\frac{A(x)-A(\mean{x})}{kT}\right]}$$
- By _Taylor expanding_ the availability:
$$P(x)\propto\exp\left[-\frac{1}{2kT}\pd{^2A}{x^2}\Delta x^2\right]$$
- The _variance_ is then:
$$\mean{\Delta x^2}=\frac{kT}{|\partial
^2 A/\partial x^2|_{x=\mean{x}}}$$
- $A$ can be _replaced_ by some _thermodynamic potential_
	- For _volume fluctuations_, use $A=F(T,V)$
- For _thermodynamic potential_ $\Pi(x)$, where $d\Pi=f\,dx+\dots$
$$\mean{\Delta x^2}=kT\left(\pd{x}{f}\right)_\mean{x}$$
- Near a _critical point_, this _diverges_
	- Gives rise to phase transition


- Define some _linear response_ function where $x=\alpha f$:
$$\mean{\Delta x^2}=kT\alpha$$
- Example of the _fluctuation-dissipation theorem_

## Example: Ising model
- From [[#Ising model]]:
$$\mean{M}=Nm\tanh\frac{mB}{kT}$$
- Calculating the magnitude of fluctuations:
$$\mean{\Delta M^2}=kT\pd{\mean{M}}{B}=Nm^2\frac{1}{\cosh^2(mB/k
T)}$$
- The _ratio_ of magnitude to the mean:
$$\frac{\sqrt{\mean{\Delta M^2}}}{\mean{M}}\sim\frac{1}{\sqrt{N}}$$

# Stochastic physics
- If one considers the _particle motion_ in a medium, one must account for _random thermal motion_
- Introduce the _Langevin equation_:
$$m\frac{d\bm{v}}{dt}=-\gamma\bm{v}+\xi(t)$$
- The $-\gamma\bm{v}$ term is a _kinetic friction_
- $\xi(t)$ is a _stochastic force_:
$$\displaylines{\mean{\xi(t)}=0 \\ \mean{\xi^2(t)}=\Gamma \\ \mean{\xi(t_1)\xi(t_2)}=\Gamma\delta(t_1-t_2)}$$
- $\Gamma$ quantifies the _intensity_ of the force
- It represents _thermal/white noise_

- _Multiplying_ the equation by $v_0=v(t=0)$, and taking an _ensemble average_:
$$\begin{aligned}\frac{d}{dt}\mean{v(t)v(0)}&=-\frac{\gamma}{m}\mean{v(t)v(0)} \\ \mean{v(t)v(0)}&=\mean{v(0)^2}\exp\left(-\frac{\gamma}{m}t\right)\end{aligned}$$
- There is a _correlation decay time_ $\tau=m/\gamma$
	- In a _fluid_, $\gamma$ is related to the [[Soft Condensed Matter#Langevin equation|viscosity]] (e.g. _Stokes drag_)

## Formal solution and fluctuation-dissipation theorem
- Add the _homogenous_ and _inhomogeneous_ terms:
$$v(t)=v_0\exp\left(-\frac{t}{\tau}\right)+\int_0^t\exp\left(-\frac{t-t'}{\tau}\right)\frac{\xi(t')}{m}\,dt'$$
- The _mean-square value_:
$$\mean{v^2}=\mean{v_0^2}\exp\left(-\frac{2t}{\tau}\right)+\frac{\Gamma}{2m\gamma}\left[1-\exp\left(-\frac{2t}{\tau}\right)\right]$$
- As the _relaxation time_ is _fast_, and using _equipartition_:
$$\mean{\frac{mv^2}{2}}=\frac{\Gamma}{4\gamma}=\frac{1}{2}kT$$
- This is the _fluctuation-dissipation theorem_:
$$\Gamma=2\gamma kT$$
- The _magnitude_ of the _stochastic force_ is related to _temperature_, and the _friction constant_

## Diffusion
- For $t\gg\tau$, the _inertial effects_ are _irrelevant_, and $\dot{v}$ is _averaged out_:
$$0=-\gamma v+\xi(t)$$
- This is the _overdamped_ limit

- The _motion_ of the particle:
$$\begin{aligned}x&=\int_0^t\frac{1}{\gamma}\xi(t')\,dt' \\ \mean{x^2}&=\frac{1}{\gamma^2}\int_0^t\int_0^t\mean{\xi(t_1)\xi(t_2)}\,dt_1\,dt_2 \\ \mean{x^2}&=\frac{\Gamma}{\gamma^2}t\end{aligned}$$
- Define the _diffusion coefficient_ $D$:
$$\displaylines{D=\frac{kT}{\gamma} \\ \mean{x^2}\equiv2Dt}$$
- This is the _Einstein diffusion relation_
- It _grows_, as there is _no energy restriction_

- In 3 dimensions:
$$\mean{r^2}=6Dt$$
## Brownian particle in a potential well
- Let the particle be in a _potential_:
$$V(x)=\frac{1}{2}ax^2$$
- The _overdamped Langevin equation_:
$$\gamma\dot{x}=-ax+\xi(t)$$
- Using a similar strategy as the [[#Formal solution of Langevin equation|above]]:
$$\mean{x^2}=\frac{\Gamma}{2\gamma a}=\frac{kT}{a}$$
- This matches the result from [[#As curvature of availability|thermodynamic fluctuations]]

## Spectral analysis of the Langevin force
- The _damped harmonic oscillator_:
$$m\ddot{x}=-\gamma\dot{x}-\alpha x+f(t)$$
- Using the Fourier transform:
$$x_\omega=\frac{f_\omega}{-m\omega^2-i\gamma\omega+\alpha}\equiv\chi_\omega f_\omega$$
- Here, $\chi_\omega$ is the _linear response function_
- In general, it is _complex:
$$\chi_\omega=\chi_\omega'+i\chi_\omega''$$
- From the fluctuation-dissipation theorem:
$$\mean{x_\omega^2}=\frac{kT}{\alpha}=\chi'(\omega=0)kT$$
- One can derive:
$$\mean{\Delta x_\omega^2}=\frac{2kT}{\omega}\chi_\omega''=\frac{2kT\gamma}{(\alpha-m\omega^2)^2+\gamma^2\omega^2}$$
- This can show _resonant behaviour_ (for light damping)

- The _spectral content_ of the _Langevin force_ $(f_{\omega}=\xi_{\omega})$:
$$\mean{x_\omega^2}=|\chi_\omega|^2\mean{\xi_\omega^2}$$
- Substituting in the results above:
$$\mean{\xi_\omega^2}=2kT\gamma$$
- This shows that it has a _flat power spectrum_, with intensity related to damping constant

## Probability distributions
- Finding probabilities $P(x,t)$ _of stochastic variables_
- One can treat it as a _discrete random walk_

### Kramers-Moyal expansion and Fokker-Planck equation
- The _over-damped limit_, with force $f(x)$:
$$\dot{x}=\frac{f(x)}{\gamma}+\frac{1}{\gamma}\xi(t)$$
- The _infinitesimal_:
$$dx=\frac{f(x)}{\gamma}\,dt+\sigma\,dW$$
- Define $dW$ such that $\mean{dW^2}=1$, hence, $\sigma=\sqrt{2kT/\gamma}$
- $\sigma\,dW$ is the _diffusion term_

- Define the _propagator_ $G$, which _links_ probabilities between two positions:
$$P(x,t+\Delta t)=\int G(x,t+\Delta t\big|y,t)P(y,t)\,dy$$
- Changing variables to $\Delta x\equiv x-y$, and _shifting_ by $\Delta x$ such that $\tilde{x}=x-\Delta x$:
$$P(x,t+\Delta t)=\int G(\tilde{x}+\Delta x,t+\Delta t\big|\tilde{x},t)P(\tilde{x},t)\,d(-\Delta x)$$
- Using a _Taylor expansion_:
$$\begin{aligned}P(x,t+\Delta t)&=\int d(\Delta x)\sum_{n=0}^\infty\frac{(-\Delta x)^n}{n!}\pd{}{\tilde{x}^n}G(\tilde{x}+\Delta x,t+\Delta t|\tilde{x},t)P(\tilde{x},t) \\ &\approx P(x,t)-\pd{}{x}(\mean{dx}P(x,t))+\frac{1}{2}\pd{^2}{x^2}\left(\mean{dx}^2P(x,t)\right)\end{aligned}$$

- Substituting results _from the Langevin equation_:
$$\pd{P(x,t)}{t}=-\pd{}{x}\left(\frac{f(x)}{\gamma}P(x,t)\right)+\frac{\sigma^2}{2}\pd{^2P}{x^2}$$
- This is the _Fokker-Planck equation_

- This separates influences from an _external force_, and from _diffusion_:
$$\frac{\sigma^2}{2}=\frac{kT}{\gamma}\equiv D$$
$$\frac{\partial P(x,t)}{\partial t}=-\frac{\partial }{\partial x}\left( \frac{1}{\gamma}f(x)P(x,t) \right)+D \frac{\partial^{2}P(x,t)}{\partial x^{2}}$$
### Free diffusion
$$\pd{P}{t}=D\pd{^2P}{x^2}$$
- This gives:
$$P(x,t)=\frac{1}{\sqrt{ 4\pi Dt }}\exp\left( -\frac{x^{2}}{4Dt} \right)$$

- Replicates the result:
$$\langle x^{2} \rangle = 2Dt $$

### Equilibrium
- A _steady state_:
$$\pd{}{x}\left[ - \frac{f(x)}{\gamma}P+D \frac{\partial P}{\partial x}\right]=0$$

- This gives:
$$P_\text{eq}\sim\exp\left(-\frac{V(x)}{kT}\right)$$
### Probability current
- The probability is a _conserved quantity_:
$$\pd{P}{t}=-\text{div }J(x,t)$$
- The _probability flux_:
$$J=\frac{f(x)}{\gamma}P(x,t)-D\pd{P}{x}$$
- This replicates _Fick's law_ for diffusion if $f(x)=0$

- One can rewrite $J$ as:
$$J=-D\exp(-\beta V(x))\pd{}{x}\left[\exp(\beta V(x))P(x,t)\right]$$

### Kramers' Problem
- Let there be a _metastable state_ $A$, with a _barrier_ of height $\Delta V$ to the truly stable state $B$
- Find the _rate of escape_ in equilibrium, or the _mean first passage time_ to escape
$$J=\text{const.}$$
- By _integrating_:
$$\frac{1}{D}\int_A^B\exp(\beta V(x))J\,dx=-\left[\exp(\beta V(x))P(x,t)\right]_A^B$$
- By _approximating_ the potential as _parabolic_, paramatrised by $\kappa_C$
$$\frac{J}{D}\exp(\beta\Delta V)\sqrt{\frac{\pi}{\kappa_C}kT}=P(x=A)$$
- The term at $B$ is _approximated_ as zero if it is _deep_ enough
$$J=D\sqrt{\frac{\kappa_C}{\pi kT}}P(x=A)\exp(-\beta\Delta V)$$
- This gives the _Arrhenius law of thermal activation_
- The _prefactor_ depends on the _rate of attempts_, and the _barrier shape_

- The _number of particles around $A$_:
$$dN_A=P(x_A)\exp(-\beta V(x))\,dx$$
- Integrating _around_ $A$:
$$N_A=P(x_A)\sqrt{\frac{\pi kT}{\kappa_A}}$$
- The _rate of escape_:
$$r=\frac{J}{N_A}=D\frac{\sqrt{\kappa_C\kappa_A}}{\pi kT}\exp(-\beta\Delta V)$$

## Discrete random walks and Markov chains
- Consider a system evolving in _discrete steps_
- The behaviour at each step depends on the _local probability distribution_, but _not on the system's history_ (previous steps)
### 1D Random walk
- Let there be a particle along _1 dimension_, which can go to the _left or right_ by length $a$
- Within $N$ _steps_, it has $N_{-}$ to the _left_ and $N_{+}$ to the _right_
$$x=a(N_{+}-N_{-})=a(N-2N_{-})=a(2N_{+}-N)$$
- The _probability_ for finding a value of $N_{+}$ _given_ $N$
$$P(N_{+}|N)=\pmatrix{N_{+}\\N}\left( \frac{1}{2} \right)^{N}=\frac{N!}{N_{+}!(N-N_{+})!}\left( \frac{1}{2} \right)^{N}$$
- Using _Stirling's approximation_ $N!\approx \sqrt{ 2\pi N }N^{N}\exp(-N)$, keeping terms _up to the second order_:
$$P(N_{+},N)=\sqrt{ \frac{2}{\pi N} }\sqrt{ \frac{1}{1-(x/aN)^{2}} }\exp\left( -\frac{x^{2}}{2a^{2}N} \right)$$
- Going into the _continuous description_, let each step take _time_ $\tau$, and letting $D=a^{2}/2\tau$
$$P(x,t)=\frac{P(N_{+},N)}{2a}=\sqrt{ \frac{1}{4\pi Dt} }\exp\left( -\frac{x^{2}}{4Dt} \right)$$
- This recreates _diffusion_
### Fokker-Planck from random walks
- Let the _probability_ of the particle being in _position_ $m$ after $N+1$ steps be $P(m,N+1)$
- It can arrive from either the _left_ or _right_, with separate _probabilities_:
$$P(m,N+1)=w(m,m-1)P(m-1,N)+w(m,m+1)P(m+1,N)$$
- Let there be some _bias_ provided by an _external force_:
	- Biased to move _downwards_
$$w(m,m-1)=\frac{1}{2}-\epsilon \hspace{1.5cm}w(m,m+1)=\frac{1}{2}+\epsilon$$
- From this:
$$\begin{align}
\frac{P(m,N+1)-P(m,N)}{\tau}&=\frac{1}{2\tau}[(1-2\epsilon)P(m-1,N)+(1+2\epsilon)P(m+1,N)-2P(m,N)] \\ &=\frac{1}{2\tau}\left[ \frac{\partial^{2}P}{\partial m^{2}}+2\epsilon \frac{\partial P}{\partial m} \right]
\end{align}$$
- Converting to position, using $D=a^{2}/2\tau$, and letting $C=\epsilon a/\tau$
$$\frac{\partial P(x,t)}{\partial t}=D\frac{\partial^{2}P(x,t)}{\partial x^{2}}+C\frac{\partial P(x,t)}{\partial x}$$
- At _equilibrium_, recalling the _Boltzmann distribution_:
$$P(t\to \infty)\propto \exp\left( -\frac{Cx}{D} \right)=\exp\left( -\frac{V(x)}{k_{B}T} \right)$$
- Using the [[#Diffusion|Einstein relation]] $D=k_{B}T/\gamma$, and for a _linear potential_:
$$C=\frac{1}{\gamma }\left( \frac{dV}{dx} \right)\equiv-\frac{f(x)}{\gamma}$$
- Then, one re-derives the [[#Kramers-Moyal expansion and Fokker-Planck equation|Fokker-Planck equation]]:
$$\frac{\partial P(x,t)}{\partial t}=-\frac{\partial }{\partial x}\left( \frac{1}{\gamma}f(x)P(x,t) \right)+D \frac{\partial^{2}P(x,t)}{\partial x^{2}}$$
