- Superconductivity: _vanishing resistivity_
- Superfluidity: _zero viscosity_ flow

- First superconductor: Mercury
- BCS theory: electron pairing
- Bosonic superfluid: $\ce{ ^{4}He }$
	- $T_{c}=2.17\text{ K}$ under its own vapour pressure
- Superfluidity due to non-$s$-wave pairing: $\ce{ ^{3}He }$
	- $T_{c}=0.9\text{ mK}$
	- Between $T_{c}$ and $\sim 0.1 \text{ K}$: normal _Fermi liquid_
- High-temp superconductors: cuprates

# Overview
## Phenomenology
- Superconducting/superfluid phase: a _thermodynamically ordered phase_
	- Phase transition: a _specific heat anomaly_ due to loss in entropy

- Superfluid flow at _finite temperature_: a _two-component model_
	- Superfluid density $n_s$ is non-zero for $T<T_{c}$
	- $n_{s}\leq n$ (total density), equality for $T=0$

- Superconductors act as _diamagnets_, producing _surface currents_ when exposed to an _external magnetic field_, such that the field is _expelled_
- This is the _Meissner effect_
- For some $H<H_{c}(T)$ (critical external field), the superconductor is a _perfect diamagnet_, so there is _no internal field_
- For $H>H_{c}(T)$, the superconductor may then become a _normal solid_
	- Known as a _type-I superconductor_

- In some superconductors, there is a _lower critical field_ $H_{c1}(T)$ such that for $H>H_{c1}(T)$, the field _only partially penetrates_
	- It is a _vortex lattice state_
- Then above some $H_{c2}(T)$, the material goes back to a _normal state_

- For a type-I superconductor with a _cavity_, the _flux in the cavity is quantised_ in terms of _flux quanta_
$$\phi_{0}=\frac{hc}{2e}=\frac{h}{2e}$$
- As the _external field goes to zero_, the _flux is still trapped_ to give a _persistent current_
- In a type-II superconductor, the _vortices_ each trap _one flux quantum_

## Bosonic systems
- At low temperatures, $N$ bosons in a volume $V$ will undergo [[Advanced statistical mechanics#Bose-Einstein condensation at low temperatures|Bose-Einstein condensation]] at some temperature:
$$k_{B}T_\text{0}=\frac{2\pi \hbar^{2}}{m}\left( \frac{N}{2.6V} \right)^{2/3}$$
- Below this temperature, the _lowest energy eigenstate_ $\varphi_{0}$ has a _temperature-dependent macroscopic occupation_, known as the _condensate_
	- Lowest energy eigenstate: $p=0$ for an ideal gas system
$$N_{0}(T)=N\left[ 1-\left( \frac{T}{T_{0}} \right)^{3/2} \right]$$
- The _entropy_ of the system comes from the _thermally excited particles_, giving the distinction of _normal fluid_ and _superfluid_ (the condensate)

#### Long range order: check newer refs
- Occupation of the _lowest energy state_ indicates some _macroscopic long-range order_
- Can be seen using [[Theories of Quantum Matter#Single particle density operator|single-particle density operator]], averaged:
	- Also known as _off-diagonal long range order_
$$\rho(\boldsymbol{x},\boldsymbol{x}')\equiv \langle \psi(\boldsymbol{x})\psi ^{\dagger}(\boldsymbol{x}) \rangle = N_{0}\varphi_{0}(\boldsymbol{x})\varphi_{0}(\boldsymbol{x}')+g(\boldsymbol{x}-\boldsymbol{x}')$$
- The second term represents the contribution of _short-ranged order_, as it contains terms from _excited states_
	- Short range: typically within de Broglie wavelength at temperature $T$
- As the lowest energy state, $\varphi_{0}(\boldsymbol{x})$ has a _long length-scale_, such that $\rho(\boldsymbol{x},\boldsymbol{x}')$ is _finite_ even for large $|\boldsymbol{x}-\boldsymbol{x}'|$

- One example is the case of an _dilute Bose gas_ with Hamiltonian:
$$\begin{align}
H-\mu N=&\int d\boldsymbol{x}\, \left\{ \frac{\hbar^{2}}{2m}\nabla \psi ^{\dagger}\cdot \nabla \psi-\mu \psi ^{\dagger}\psi \right\} \\
&+\frac{1}{2}\int d\boldsymbol{x}\,d\boldsymbol{x}'\, U(\boldsymbol{x}-\boldsymbol{x}')\psi ^{\dagger}(\boldsymbol{x})\psi ^{\dagger}(\boldsymbol{x}')\psi(\boldsymbol{x}')\psi(\boldsymbol{x})
\end{align}$$
- For _weak, contact interactions_ this gives the [[Theories of Quantum Matter#Gross-Pitaevskii approximation|Gross-Pitaevskii approximation]]
- It gives a _ground state_ of the form:
$$\psi(\boldsymbol{x})=\sqrt{ n_{s}(\boldsymbol{x}) }\exp[i\phi(\boldsymbol{x})]$$
- There is a _superfluid density_ $n_{s}(\boldsymbol{x})$ and a corresponding _phase_ $\phi(\boldsymbol{x})$

### Ginzburg-Landau theory for superfluids????

# Macroscopic electrodynamics
- The two London equations, and the resulting equation for _magnetic field decay_
	- _Phenomenological_ in origin, with no proof on microscopic scale without Ginzburg-Landau or BCS theory
	- Classical origins for first: Drude equation with $\tau\to \infty$
	- Second equation: from Maxwell's equation with _flux expulsion conditions_
$$\displaylines{\Lambda \frac{\partial}{\partial t}\boldsymbol{j}=\boldsymbol{E} \\ \boldsymbol{B}=-\Lambda \nabla\times \boldsymbol{j} \\ \Lambda= (ne^{2}/m)^{-1}\\ \nabla^{2}\boldsymbol{B}=\frac{\mu_{0}}{\Lambda}\boldsymbol{B}=\frac{1}{\lambda^2}\boldsymbol{B} }$$
- $\lambda$ is the _penetration depth_ of the magnetic field, where one solution is:
$$\boldsymbol{B}=\boldsymbol{B}_{0}\exp\left( -\frac{x}{\lambda} \right)$$
- This represents _screening_ by the electrons in the supercoductor

- There is typically some _discrepancy_ between $\lambda$ predicted by the above, and the _experimentally measured_ value, due to _non-local electrodynamics_ at the scale of the _wavefunction coherence length_


# Mean field theory of pairing

# BCS theory

# Strong coupling
