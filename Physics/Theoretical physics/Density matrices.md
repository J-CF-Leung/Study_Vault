- The _most general_ description of a quantum system
- A _pure state_ is simply described by a _single vector_

- The _density matrix_ formalism encodes _classical probabilities_
# The density operator
- A _mixed state_ has some _statistical distribution_ of states
	- Typically a _subsystem_ of some _ensemble_
	- This is different to the statistical distribution of _physical quantities_ with average value $\left<A\right>=\braket{ \psi|A | \psi }$
	- The source of uncertainty is more "classical"
	- It is an _incoherent_ combination of states, unlike the linear superposition
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
$$\displaylines{\rho=\alpha^{2}\ket{\uparrow}\bra{\uparrow}+\beta^{2} \ket{\downarrow}\bra{\downarrow} +\dots  \\ \rho =\begin{pmatrix}
\alpha^{2} & \alpha\beta^{*} \\ \alpha^{*}\beta & \beta^{2}
\end{pmatrix}}   $$
- There are _off-diagonal terms_

- The _general_ spin-1/2 density matrix
	- $0<r<1$
$$\rho=\frac{1}{2}(\mathbb{I}+r \,\boldsymbol{n}\cdot \boldsymbol{\sigma})$$
- Example: 
	- A _classical_ equal mixture of up and down (no off-diagonal terms) $$\rho= \frac{1}{2}\begin{pmatrix} 1&0\\ 0&1\end{pmatrix}$$
	- A _pure state_ with equal probabilities
	- The _off-diagonal_ terms indicate _coherence_ between the states

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
	- _Different_ to the [[Quantum Dynamics#Dynamics in the Heisenberg picture|Heisenberg equation of motion]], as it is the _state_ that is evolving
$$ \frac{d\rho}{dt}=-\frac{i}{\hbar} [H,\rho]$$

- In general, there can be _damping_

## Quantum statistical mechanics
- Let a system be in _thermal equilibrium_
- Energy eigenstates:
$$H\ket{\psi_{n}}=E_{n}\ket{\psi_{n}}  $$
- Let there be an _ensemble_ of states characterised by distribution $P_{n}$

- In the [[Advanced statistical mechanics#Canonical ensemble and the partition function|canonical ensemble]] of temperature $T$:
$$\displaylines{P_{n}= \frac{1}{Z} \exp(-\beta E_{n}) \hspace{1.5cm} Z=\sum_{n}\exp(-\beta E_{n}) \\ \rho=\sum_{n} \frac{1}{Z}\exp(-\beta E_{n}) \ket{\psi_{n}}\bra{\psi_{n}}=\frac{1}{Z}\exp(-\beta H) \\ Z=\mathrm{Tr}[\exp(-\beta H)] \\ \frac{d\rho}{dt}=0}$$

- Thermodynamic variables:
$$\displaylines{E=\overline{\langle H \rangle }=\mathrm{Tr}(H\rho) \\ S=-k_{B}\sum_{\alpha}P_{\alpha}\ln P_{\alpha}=-k_{B}\mathrm{Tr}(\rho \ln \rho)}$$
- The latter is the _von Neumann entropy_
- For _pure states_, $S=0$
- For eigenvalues of $\lambda_{i}$ of $\rho _\text{red}$, the entropy is $-k_{B}\sum_{i} \lambda_{i}\ln\lambda_{i}$

- _Without_ any damping or entanglement (the system is _isolated_), $dS/dt=0$
	- The latter equality is obtained using the von Neumann equation and the _cyclic property_ of the trace
$$\frac{dS}{dt}=-k_{B}\mathrm{Tr}[\dot{\rho}\ln \rho+\dot{\rho}]=0$$

### Free particle
- Consider a _single particle_ of an [[Advanced statistical mechanics#The ideal gas in the canonical ensemble|ideal gas]] at temperature $T$
$$Z_{1}=\mathrm{Tr}[\exp(-\beta H)]\hspace{1.5cm} H=\frac{p^{2}}{2m}$$
- With volume normalisation, introducing the thermal wavelength $\lambda _\text{dB}$:
$$\displaylines{Z_{1}=\int  \, \frac{d^{3}k}{(2\pi)^{3}/V} \exp\left( -\frac{\hbar^{2}k^{2}}{2m} \right)= \frac{V}{\lambda^{3}_{dB}} \\ \lambda _\text{dB}=\sqrt{ \frac{2\pi\beta \hbar^{2}}{m} }}$$

- As _momentum eigenstates_ are also _energy eigenstates_, express the density matrix in _momentum representation_:
$$\rho=\sum_{k}\exp(-\beta E_{k}) \frac{\lambda _\text{dB}^{3}}{V} \ket{\varphi_{k}}\bra{\varphi_{k}}  $$

- Position space representation
$$\rho(\boldsymbol{r},\boldsymbol{r}')=\sum_{k,k'} \braket{ \boldsymbol{r} | \varphi_{k} } \braket{ \varphi_{k}|\rho | \varphi_{k'} } \braket{ \varphi_{k'} | \boldsymbol{r}' } $$
- Summing over $k$ to obtain:
$$\rho _\text{free}(\boldsymbol{r},\boldsymbol{r}')=\frac{1}{V} \exp\left( -\pi\frac{|\boldsymbol{r}-\boldsymbol{r}'|^{2}}{\lambda _\text{dB}^{2}} \right)$$
- Particles have a _width_ of $\sim\lambda _\text{dB}$
- At $\boldsymbol{r}=\boldsymbol{r}'$, this returns the _particle density_

- The exponential factor measures _quantum coherence_ between the wave packets

### Quantum corrections to the ideal gas law
- Consider the $N-$body wave function for _indistinguishable particles_

# Density operators for subsystems
- The simplest case: some subsystem $A$ surrounded by an _environment_ $B$
- Represent them with kets $\ket{i}$ and $\ket{\alpha}$
- The _state_ of the system can be written as:
$$\ket{\psi}=\sum_{i,\alpha}C_{i\alpha}\ket{i}\otimes \ket{\alpha}   $$

- Consider the _expectation value_ of an operator $O$ acting on only system $A$, being the _identity_ for system $B$:
$$\begin{align}
\overline{\langle O \rangle }&=\sum_{i,j,\alpha,\beta}C_{\beta j}^{*}C_{i\alpha}\braket{ \beta |\alpha  } \braket{ j|O |i  } \\ &=\sum_{i,j,\alpha} C_{\alpha j}^{*}C_{i\alpha} \braket{ j|O |i  } 
\end{align} $$

- This leads to the _reduced density operator_, from summing over the _environment_ states:
$$\rho_{A,\text{red}}=\mathrm{Tr}_{B}[\rho_{AB}]$$
- This describes the _mixed state_ for $A$, despite the fact that it _starts from pure states_

- When $B$ is not known, $A$ can _appear to be in a mixed state_ (already _thermalised_)
	- A reflection of _entanglement_
	- The _eigenstate thermalisation hypothesis_

- One can quantify entanglement using an _entanglement entropy_:
$$S_\text{ent}=-k_{B}\mathrm{Tr}[\rho _\text{red}\ln \rho _\text{red}]$$

## Spin-1/2 particles
- The _Bell state_ (a pure state):
$$\displaylines{\ket{\psi}=\frac{1}{\sqrt{ 2 }}(\ket{\uparrow}_{A}\ket{\uparrow}_{B} + \ket{\downarrow}_{A}\ket{\downarrow}_{B}    )  \\ \rho=\ket{\psi}\bra{\psi}  }$$
- The _reduced density operator_:
$$\rho _\text{red}=\frac{1}{2}(\ket{\uparrow}\bra{\uparrow} +\ket{\downarrow}\bra{\downarrow}    )$$

- It describes a _mixed state_ for $A$
	- $A$ and $B$ are _entangled_
$$S_\text{ent}=k_{B}\ln2$$

# Quantum damping
- The entropy for a _coupled system_ can vary
	- The _arrow of time_
	- For an _isolated system_, $dS/dt=0$
- When a system is _coupled_ to an environment, there can be _transitions_
- States start to _decohere_ (pure state to "classical" mixed state)
	- Indicated by the _disappearance of off-diagonal terms_ in $\rho$

## Two-level system coupled to a field
- The Hamiltonian of both the _two-level system_, and the _field_ (second quantised)
$$H_{0}=\frac{\hbar\omega}{2}\sigma_{z}+\sum_{\boldsymbol{k}} \hbar\omega_{\boldsymbol{k}}a_{\boldsymbol{k}}^{\dagger}a_{\boldsymbol{k}}$$
- Let the environment be in _thermal equilibrium_ at temperature $T$

- The _coupling_ between the system and the field, accounting for _absorption_ and _emission_ of photons:
$$V=\sum_{\boldsymbol{k}}\hbar g_{\boldsymbol{k}}(\sigma_{+}a_{\boldsymbol{k}}+\sigma_{-}a_{\boldsymbol{k}}^{\dagger})$$
- Write the _reduced density matrix_ as:
$$\rho _\text{red}=\pmatrix{\rho_{uu}&\rho_{ud} \\ \rho_{ud}^{*} &\rho_{dd}}$$

- The field in thermal equilibrium:
$$\bar{n}_{\omega}=\frac{1}{\exp(\beta \hbar\omega)+1}$$
- Rate constant:
$$\Gamma=\frac{\omega^{3}d^{2}}{3\pi\epsilon_{0}\hbar c^{3}}$$

- Final results:
$$\begin{align}
\dot{\rho}_{uu}&=-(\bar{n}_{\omega}+1)\Gamma \rho_{uu}+\bar{n}_{\omega}\Gamma \rho_{dd} \\ \dot{\rho}_{ud}&=\dot{\rho}^{*}_{du}=-\left( \bar{n}_{\omega}+\frac{1}{2} \right) \Gamma \rho_{ud} \\ \dot{\rho}_{dd}&=-\bar{n}_{\omega}\Gamma \rho_{dd}+(\bar{n}_{\omega}+1)\Gamma \rho_{uu}
\end{align}$$
- The up state can _decay_, _emitting_ a photon with _spontaneous_ and _stimulated_ components
- The down state can also _absorb_ photons to _promote_ particles
- $\dot{\rho}_{uu}=-\dot{\rho}_{dd}$ to _preserve_ the trace

- The off-diagonal terms _decay_ with rate $\Gamma(\bar{n}_{\omega}+1/2)$
	- _Decoherence_ between the up and down states

- At $T=0$, $\bar{n}_{\omega}=0$ and there is only _spontaneous decay_

- At _long times_ (in steady state)
$$\rho=\frac{1}{1+\exp(\beta \hbar\omega)}\pmatrix{e^{-\beta \hbar\omega}&0 \\ 0&1}$$

- In real system, damping can also occur due to _phonons_
- The coupling _modulates_ the energy splitting
$$V=\sum_{\boldsymbol{k}}g_{\boldsymbol{k}}\sigma^{z}(\boldsymbol{k})a_{\boldsymbol{k}}^{\dagger}a_{\boldsymbol{k}}$$
