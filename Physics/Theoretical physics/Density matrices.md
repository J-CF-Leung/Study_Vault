- The _most general_ description of a quantum system
- A _pure state_ is simply described by a _single vector_

- The _density matrix_ formalism encodes _classical probabilities_
# The density operator
- A _mixed state_ has some _statistical distribution_ of states
	- Typically a _subsystem_ of some _ensemble_
	- This is different to the statistical distribution of _physical quantities_ with average value $\left<A\right>=\braket{ \psi|A | \psi }$
	- The source of uncertainty is more "classical"
- With some set of _probabilities_ $p_{j}$ of a _system_ being in state $\ket{\psi_{j}}$
$$\overline{\left<A\right>}=\sum_{j}p_{j} \braket{ \psi_{j}|A | \psi_{j} }  $$

- Define the _density operator_:
$$\rho=\sum_{i} p_{i}\ket{\psi_{i}} \bra{\psi_{i}} $$

- Consider the quantity:
	- Order is insignificant as the _trace_ is _cyclic_
$$\mathrm{Tr}(A\rho)=\sum_{i,j}p_{i}\braket{ \psi_{j} | A |\psi_{i}}\braket{ \psi_{i} |\psi_{j}  }=\sum_{j}p_{j}\braket{ \psi_{j}|A |\psi_{j}  }  =\overline{\left<A\right>} $$
- Therefore, the _classical average_ of a quantity $A$ is given by $\mathrm{Tr}(A\rho)$
## Properties
- From its definition, $\rho$ is _Hermitian_:
$$\rho=\rho ^{\dagger}$$
- Its _trace_:
$$\mathrm{Tr}(\rho)=1$$
- It is _positive-definite_:
$$\braket{ \Phi|\rho | \Phi } =\sum_{i} p_{i} |\braket{ \psi_{i} |\Phi  } |^{2} \geq 0$$
- As $\rho$ is _Hermitian_, one can use an _orthonormal basis_ to decompose it:
$$\rho=\sum_{\alpha} P_{\alpha} \ket{\psi_{\alpha}}\bra{\psi_{\alpha}}  $$
- The probabilities are the _eigenvalues_
	- Must be _real_, _positive_, and _bounded_ between 0 and 1
$$\sum_{\alpha}P_{\alpha}=1$$
- In general:
$$\mathrm{Tr}(\rho^{2})\leq 1$$
- The equality only holds for _pure states_
## Pure states
- A _pure state_ corresponds to one probability being $1$:
$$\rho=\ket{\psi}\bra{\psi}  $$
- It is a _projection operator_ to state $\ket{\psi}$
- In this case:
$$\rho^{2}=\rho \implies \mathrm{Tr}(\rho^{2})=1$$

## The spin-1/2 particle
- The general _pure state_ for a spin-1/2 particle
$$\ket{\psi}=\alpha \ket{\uparrow}+\beta \ket{\downarrow}   $$

- The _density operator_ for this pure state:
$$\displaylines{\rho=\alpha^{2}\ket{\uparrow}\bra{\uparrow}+\beta^{2} \ket{\downarrow}\bra{\downarrow} +\alpha^{*}\beta  \\ \rho =\begin{pmatrix}
\alpha^{2} & \alpha\beta^{*} \\ \alpha^{*}\beta & \beta^{2}
\end{pmatrix}}   $$


- The _general_ spin-1/2 density matrix
	- $0<r<1$
$$\rho=\frac{1}{2}(\mathbb{I}+r \,\boldsymbol{n}\cdot \boldsymbol{\sigma})$$
- Example: 
	- A _classical_ equal mixture of up and down $$\rho= \frac{1}{2}\begin{pmatrix} 1&0\\ 0&1\end{pmatrix}$$
	- A _pure state_ with equal probabilities
	- The _off-diagonal_ terms indicate _coherence_

## Position representation
$$\rho(\boldsymbol{r},\boldsymbol{r}')=\braket{ \boldsymbol{r}|\rho |\boldsymbol{r}'  } $$
- In terms of the _wave functions_:
$$\rho(\boldsymbol{r},\boldsymbol{r}')=\sum_{\alpha}P_{\alpha}\varphi_{\alpha}(\boldsymbol{r})\varphi_{\alpha}^{*}(\boldsymbol{r}')$$
- The _mean density_ is then:
$$\rho(\boldsymbol{r},\boldsymbol{r})=\sum_{\alpha} P_{\alpha} |\varphi_{\alpha}|^{2}$$

- Can be _generalised_ to many-body systems

## Time evolution
- Time-dependent Schrodinger equation:
$$i\hbar \frac{d}{dt}\ket{\psi}=H\ket{\psi}  $$
- The density matrix evolves with time:
$$\rho(t)=\sum_{\alpha} p_{\alpha} \ket{\varphi_{\alpha}(t)} \bra{\varphi_{\alpha}(t)}  $$
- Each state evolves _coherently_, such that the _probabilities_ (eigenvalues) remain _unchanged_
	- The _energy_ of the system is _conserved_

- Apply to density matrix, one gets the _von Neumann equation_:
	- _Different_ to the Heisenberg equation of motion, as it is the _state_ that is evolving
$$ \frac{d\rho}{dt}=-\frac{i}{\hbar} [H,\rho]$$

- In general, there can be _damping_

## Quantum statistical mechanics
- Let a system be in _thermal equilibrium_
- Energy eigenstates:
$$H\ket{\psi_{n}}=E_{n}\ket{\psi_{n}}  $$
- Let there be an _ensemble_ of states characterised by distribution $P_{n}$

- In the [[Advanced statistical mechanics#Canonical ensemble and the partition function|canonical ensemble]] of temperature $T$:
$$\displaylines{P_{n}= \frac{1}{Z} \exp(-\beta E_{n}) \hspace{1.5cm} Z=\sum_{n}\exp(-\beta E_{n} \\ \rho=\sum_{n} \frac{1}{Z}\exp(-\beta E_{n}) \ket{\psi_{n}}\bra{\psi_{n}}=\frac{1}{Z}\exp(-\beta H) \\ Z=\mathrm{Tr}[\exp(-\beta H)] \\ \frac{d\rho}{dt}=0}$$

- Thermodynamic variables:
$$\displaylines{E=\overline{\langle H \rangle }=\mathrm{Tr}(H\rho) \\ S=-k_{B}\sum_{\alpha}P_{\alpha}\ln P_{\alpha}=-k_{B}\mathrm{Tr}(\rho \ln \rho)}$$
- The latter is the _von Neumann entropy_

### Free particle
$$Z=\mathrm{Tr}[\exp(-\beta H)]\hspace{1.5cm} H=\frac{p^{2}}{2m}$$
- With volume normalisation:
$$Z=\frac{V}{\lambda^{3}_{dB}}$$
- Thermal wavelength $\lambda _\text{dB}$

- Momentum space representation
$$\rho=\sum_{k}\exp(-\beta E_{k}) \frac{\lambda^{3}}{V} \ket{\varphi_{k}}\bra{\varphi_{k}}  $$

- Position space representation
$$\rho(\boldsymbol{r},\boldsymbol{r}')=\sum_{k,k'} \braket{ \boldsymbol{r} | \varphi_{k} } \braket{ \varphi_{k}|\rho | \varphi_{k'} } \braket{ \varphi_{k'} | \boldsymbol{r}' } $$
- Expanding:
$$\rho _\text{free}(\boldsymbol{r},\boldsymbol{r}')=\frac{1}{V} \exp()$$

- The exponential factor measures _quantum coherence_

# Density operators for subsystems
- The simplest case: some subsystem $A$ surrounded by an _environment_ $B$
- Represent them with kets $\ket{i}$ and $\ket{\alpha}$
- The _state_ of the system can be written as:
$$\ket{\psi}=\sum_{i,\alpha}C_{i\alpha}\ket{i}\otimes \ket{\alpha}   $$

- Expectation value
- Of the _whole system_
- Of only system $A$:

- The _reduced density operator_: sum over the _environment_ states:
$$\rho_{A,\text{red}}=\mathrm{Tr}_{B}[\rho_{AB}]$$
- This describes the _mixed state_ for $A$, despite the fact that it _starts from pure states_

- When $B$ is not known, $A$ can _appear to be in a mixed state_ (thermalised)
	- A reflection of _entanglement_
- "Eigenstate thermalisation"

- One can define an _entanglement entropy_:
$$S=-k_{B}\mathrm{Tr}[\rho _\text{red}\ln \rho _\text{red}]$$

## Spin-1/2 particles
- The _Bell state_ (a pure state):
$$\displaylines{\ket{\psi}=\frac{1}{\sqrt{ 2 }}(\ket{\uparrow}_{A}\ket{\uparrow}_{B} + \ket{\downarrow}_{A}\ket{\downarrow}_{B}    )  \\ \rho=\ket{\psi}\bra{\psi}  }$$
- The _reduced density operator_:

- It describes a _mixed state_ for $A$
	- $A$ and $B$ are _entangled_

## Thermalisation
- For an _isolated system_, the _entropy_ is unchanged
- Time evolution:
$$\frac{d\rho}{dt}$$
- This gives:
$$\frac{dS}{dt}=$$

- The _entanglement entropy_:

# Quantum damping
- When a system is _coupled_ to an environment, there can be _transitions_
- States start to _decohere_

## Two-level system coupled to a field
- The Hamiltonian of both the _two-level system_, and the _field_ (second quantised)
$$H_{0}=\frac{\hbar\omega}{2}\sigma_{z}+\sum_{\boldsymbol{k}}$$
- The _coupling_ between the system and the field, accounting for _absorption_ and _emission_ of photons:
