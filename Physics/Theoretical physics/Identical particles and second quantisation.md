- For $N$ particles, one uses a _multi-particle wave function_ $\Psi(\boldsymbol{r}_{1},\boldsymbol{r}_{2},\dots,\boldsymbol{r}_{N})$ to describe the system

# Identical particles
- If the particles are [[Identical Particles|identical]], the _probability density_ must be _same under exchange_:
$$|\Psi(\boldsymbol{r}_{1,},\boldsymbol{r}_{2})|^{2}=|\Psi(\boldsymbol{r}_{2,}\boldsymbol{r}_{1})|^{2}$$
- The wave function must then only change by a _phase factor_:
$$\hat{P}_{12}\Psi(\boldsymbol{r}_{1},\boldsymbol{r}_{2})=\Psi(\boldsymbol{r}_{2},\boldsymbol{r}_{1})=\exp(i\theta)\Psi(\boldsymbol{r}_{1},\boldsymbol{r}_{2})$$
- In 3D, if particles are _exchanged twice_:
$$P_{12}^{2}=1$$
- The system is also _exchange symmetric_:
$$\left[ \hat{P}_{12},\hat{H} \right]=0$$
- In 2D, there can be an _arbitrary phase_
## Fermions and bosons
- In 3D, if $P_{12}=+1$, the particles are _bosons_, if $P_{12}=-1$, they are _fermions_

- As long as the Hamiltonian is _separable_, the system can be described using _product states_
- The individual particle _eigenstates_ ($i,j$ label the _eigenstates_, coordinates label particles)
$$\braket{ \phi_{i} | \phi_{j} }=\delta_{ij} $$
- For two particles:
$$\psi(\boldsymbol{r}_{1},\boldsymbol{r}_{2})=\frac{1}{\sqrt{ 2 }}[\phi_{1}(\boldsymbol{r}_{1})\phi_{2}(\boldsymbol{r}_{2})\pm \phi_{1}(\boldsymbol{r}_{2})\phi_{2}(\boldsymbol{r}_{1})] $$
- The sign depends on whether the particles are _fermions_ or _bosons_
- For a product state:
$$\braket{ \psi | \psi } \neq \braket{ \phi_{1} | \phi_{1} }+\braket{ \phi_{2} | \phi_{2} }  $$
- For _fermions_, $\psi(\boldsymbol{r},\boldsymbol{r})=0$
- This is the _Pauli exclusion principle_

- For _bosons_, $|\psi(\boldsymbol{r},\boldsymbol{r})|^{2}=2|\phi_{1}(\boldsymbol{r})|^{2}|\phi(\boldsymbol{r})|^{2}$
- Bosons like to _occupy the same state_

## Hong-Ou-Mandel effect
- Identical particles _do not have independent probabilities_
- Hong-Ou-Mandel effect: two photons approach a _beam splitter_
- The _channels_ are labelled $A,B$

- Let the beam splitter be 50:50
$$\displaylines{\begin{pmatrix}
a_\text{out} \\ b_\text{out}\end{pmatrix}=S \begin{pmatrix}
a_\text{in}\\b_\text{in}
\end{pmatrix} \\ \ket{A,\text{in}} \to \frac{1}{\sqrt{ 2 }}[\ket{A,\text{out}} +\ket{B,\text{out}} ] \\ \ket{B, \text{in}} \to \frac{1}{\sqrt{ 2 }} [\ket{A, \text{out}} -\ket{B,\text{out}} ]} $$
- The _out_ states are _orthogonal_ due to the [[Quantum scattering theory#Scattering matrix|unitarity of the scattering matrix]]
$$S=\frac{1}{\sqrt{ 2 }}\begin{pmatrix}1&1\\1&-1\end{pmatrix}$$
- Let the photons be _indistinguishable_
- Then form _product states_:
$$\displaylines{\ket{\Psi _\text{in}}= \frac{1}{\sqrt{ 2 }}[\ket{A,\text{in} }_{1}\ket{B,\text{in}}_{2} + \ket{A,\text{in} }_{2}\ket{B,\text{in}}_{1}  ] \\ \downarrow\\\ket{\Psi _\text{out}}=\frac{1}{\sqrt{ 2 } } [\ket{A,\text{out}}_{1}\ket{A,\text{out}}_{2} - \ket{B,\text{out}}_{1}\ket{B,\text{out}}_{2}]}$$
- The photons must _both come out of the same channel_
	- The _choice_ of channel is still _random_

## More particles
- For many particles, a swap between _any two particles_ must still maintain probability density
- Following the same arguments as above:
$$\hat{P}_{ij}\Psi(\boldsymbol{r}_{1},\dots \boldsymbol{r}_{i},\dots\boldsymbol{r}_{j},\dots \boldsymbol{r}_{N})=\pm \Psi(\boldsymbol{r}_{1},\dots \boldsymbol{r}_{j},\dots\boldsymbol{r}_{i},\dots \boldsymbol{r}_{N})$$
- The _product states_ are formed as long as:
$$\hat{H}=\sum_{i=1}^{N}\left[ -\frac{\hbar^{2}}{2m}\nabla_{i}^{2}+V_{i}(\boldsymbol{r}_{i}) \right]$$
- Label the _states_ by _quantum numbers_ $\{\alpha_{i}\}$
- Given each state may have some _occupation number_ $N_{\alpha}$
	- Significant for _bosons_
$$E=\sum_{\alpha} N_{\alpha}E_{\alpha}$$
- Let the _symmetrising_ operator $\mathcal{S}$ and the _antisymmetrising_ operator $\mathcal{P}$ be:
$$\mathcal{S}= \frac{1}{N!}\sum_{P} P\hspace{1.5cm}\mathcal{A}=\frac{1}{N!}\sum_{P}\mathrm{sgn}(P)P$$
- The _product states_ for fermions and bosons:
$$\displaylines{\ket{\Psi^{S}_{\alpha_{1}\alpha_{2}\dots\alpha_{N}}}=\sqrt{ \frac{N!}{\prod_{\alpha}N_{\alpha}!}}\mathcal{S}[\phi_{\alpha_{1}}(\boldsymbol{r}_{1})\phi_{\alpha_{2}}(\boldsymbol{r}_{2})\dots \phi_{\alpha_{N}}(\boldsymbol{r}_{N})] \\ \ket{\Psi^{A}_{\alpha_{1}\alpha_{2}\dots\alpha_{N}}}=\sqrt{ N! }\mathcal{A}[\phi_{\alpha_{1}}(\boldsymbol{r}_{1})\phi_{\alpha_{2}}(\boldsymbol{r}_{2})\dots \phi_{\alpha_{N}}(\boldsymbol{r}_{N})]  } $$
- The _denominator_ for the bosonic state takes into account states $\alpha$ that are _occupied by multiple particles_

- The fermion state can be written as a _Slater determinant_:
$$\ket{\Psi^{A}_{\alpha_{1}\alpha_{2}\dots\alpha_{N}}}=\begin{vmatrix}
\phi _{\alpha_{1}}(\boldsymbol{r}_{1})& \phi _{\alpha_{1}}(\boldsymbol{r}_{2}) &\dots & \phi_{\alpha_{1}}(\boldsymbol{r}_{N}) \\ \phi_{\alpha_{2}}(\boldsymbol{r}_{1}) & \phi_{\alpha_{2}}(\boldsymbol{r}_{2})& \dots & \phi_{\alpha_{2}}(\boldsymbol{r}_{N}) \\ \vdots & \vdots& \ddots & \vdots \\ \phi_{\alpha_{N}}(\boldsymbol{r}_{1}) & \phi_{\alpha_{N}}(\boldsymbol{r}_{2}) & \dots & \phi_{\alpha_{N}}(\boldsymbol{r}_{N})
\end{vmatrix} $$
# Second quantisation
- Represent states by their _occupation number_ instead of some quantum number
- An $N-$particle state is written as:
$$\ket{\{N_{\alpha}\}} $$
- The set $\{N_{\alpha}\}$ are the _occupation numbers_ of states

- The _space_ of states with _all possible particle numbers_ is known as _Fock space_
	- The _direct sum_ of spaces of zero particles, one particle, ...
- For two states of _arbitrary particle numbers_:
$$\braket{ N_{1}N_{2}\dots | N_{1}'N_{2}'\dots }=\delta_{N_{1}N_{1}'}\delta_{N_{2}N_{2}'}\dots $$
## Creation and annihilation operators
- Introduce _creation and annihilation operators_, which _add and subtract quanta_
$$\displaylines{a_{\alpha}^{\dagger}\ket{\Psi_{\alpha_{1}\alpha_{2}\dots\alpha_{N}}}=\sqrt{ N+1 }\ket{\phi_{\alpha}}\ket{\Psi_{\alpha_{1}\alpha_{2}\dots\alpha_{N}}}  }$$

### Bosons
- For _bosons_:
$$a_{\alpha}^{\dagger}\ket{\Psi^{S}_{\alpha_{1}\alpha_{2}\dots\alpha_{N}}}=\sqrt{ N+1 }\mathcal{S}\left\{\ket{\phi_{\alpha}}\ket{\Psi^{S}_{\alpha_{1}\alpha_{2}\dots\alpha_{N}}}\right\}$$
- Labelling by _occupation number_, the above becomes:
$$\displaylines{a^{\dagger}_{\alpha}\ket{N_{1}N_{2}\dots N_{\alpha}\dots N_{N}}=\sqrt{ N_{\alpha}+1 }\ket{N_{1}N_{2}\dots N_{\alpha}+1\dots N_{N}}\\a_{\alpha}\ket{N_{1}N_{2}\dots N_{\alpha}\dots N_{N}}=\sqrt{ N_{\alpha} }\ket{N_{1}N_{2}\dots N_{\alpha}-1\dots N_{N}}  }$$
- From this, one can show:
$$\left[ a_{\alpha},a_{\beta}^{\dagger} \right]=\delta_{\alpha\beta} \hspace{1cm}\left[ a_{\alpha},a_{\beta} \right]=\left[ a_{\alpha}^{\dagger}, a_{\beta}^{\dagger} \right]=0$$
- Then define the _number operator_:
$$\displaylines{\hat{N}_{\alpha}=a^{\dagger}_{\alpha}a_{\alpha} \\ \left[ a_{\alpha},\hat{N}_{\alpha} \right]=a_{\alpha}\hspace{1.5cm}\left[ a_{\alpha}^{\dagger} ,\hat{N}_{\alpha}\right]=-a_{\alpha}^{\dagger}}$$
- The _normalised state_ can then be written as:
$$\ket{N_{1}N_{2},\dots N_{N}} =\prod_{\alpha} \frac{\left( a^{\dagger}_{\alpha} \right)^{N_{\alpha}}}{\sqrt{ N_{\alpha}! }}\ket{00\dots0} $$
- $\ket{00\dots{0}}$ is the _vacuum state_, and represents _no quanta in any state_:
$$\ket{\text{VAC}}=\ket{00\dots0}  $$

- This is an _identical algebra_ to the [[Quantum Harmonic Oscillator]]
- Example: _photons_ and the [[Quantum electrodynamics|EM field]]

### Fermions
$$a_{\alpha}^{\dagger}\ket{\Psi^{A}_{\alpha_{1}\alpha_{2}\dots\alpha_{N}}}=\sqrt{ N+1 }\mathcal{A}\left\{\ket{\phi_{\alpha}}\ket{\Psi^{A}_{\alpha_{1}\alpha_{2}\dots\alpha_{N}}}\right\}$$
- They obey _anticommutation relations_
$$\left\{ a_{\alpha},a_{\beta}^{\dagger} \right\}=\delta_{\alpha\beta} \hspace{1cm}\left\{ a_{\alpha},a_{\beta} \right\}=\left\{ a_{\alpha}^{\dagger},a_{\beta}^{\dagger} \right\}=0$$
- One _cannot create two fermions in the same state_

- Building up a general state:
$$\ket{N_{0}N_{1}\dots N_{N}}=\prod_{\alpha} \left( a^{\dagger}_{\alpha} \right)^{N_{\alpha}}\ket{\text{VAC}} $$
- The occupation numbers $N_{\alpha}$ are _either_ $0$ or $1$
- The _ordering_ of operators is significant due to the anticommutation relations

- Due to the limitation of occupation numbers (and from the anticommutators):
$$\left( a_{\alpha} \right)^{2}=\left( a_{\alpha}^{\dagger} \right)^{2}=0$$
- The _commutation relation_ with the number operator still holds:
$$\displaylines{\hat{N}_{\alpha}=a^{\dagger}_{\alpha}a_{\alpha} \\ \left[ a_{\alpha},\hat{N}_{\alpha} \right]=a_{\alpha}\hspace{1.5cm}\left[ a_{\alpha}^{\dagger} ,\hat{N}_{\alpha}\right]=-a_{\alpha}^{\dagger}}$$
### Common commutation relations
- The above relations have _commutators_ for _both fermions and bosons_
- Similarly, the more general relations are:
$$\left[ a_{\alpha}, a_{\beta}^{\dagger}a_{\gamma}\right]=\delta_{\alpha\beta}a_{\gamma}\hspace{1.5cm}[a_{\alpha}^{\dagger},a_{\beta}^{\dagger}a_{\gamma}]=-\delta_{\alpha\gamma}a_{\beta}^{\dagger}$$

### Field operators
- The _unitary change of basis_:
$$\{\phi_{\alpha}\}\to \{\tilde{\phi}_{\alpha}\}$$
$$\ket{\tilde{\phi}_{\alpha}}=\sum_{\beta} \ket{\phi_{\beta}}\braket{ \phi_{\beta} | \tilde{\phi}_{\alpha} }  =\sum_{\beta} \braket{ \phi_{\beta} | \tilde{\phi}_{\alpha} }a_{\beta}^{\dagger}\ket{\text{VAC}}  $$
- Therefore, the transformation _for the operator_:
$$\hat{\tilde{a}}_{\alpha}^{\dagger} =\sum_{\beta} \braket{ \phi_{\beta} | \tilde{\phi}_{\alpha} }a_{\beta}^{\dagger}  $$
- Transforming to _position eigenstates_ $\ket{\tilde{\phi}_{\alpha}}=\ket{\boldsymbol{r}}$
$$\displaylines{\braket{ \phi_{\beta} | \boldsymbol{r} }=\phi_{\beta}^{*} \\ \sum_{\beta}\phi_{\beta}^{*}(\boldsymbol{r})\phi_{\beta}(\boldsymbol{r}')=\delta(\boldsymbol{r}-\boldsymbol{r}')}$$
- Define the _field operator_, the _creation_ operator in _position space_:
$$\psi^{\dagger}(\boldsymbol{r})\equiv \sum_{\beta}\phi_{\beta}^{*}(\boldsymbol{r})a^{\dagger}_{\beta}$$
- The corresponding _annihilation operator_:
$$\psi(\boldsymbol{r})\equiv \sum_{\beta} \phi_\beta(\boldsymbol{r})a_{\beta}$$
- They _change occupation of position eigenstates_

- (Anti-)commutation, depending on _bosons/fermions_
	- Same relations as those for $a,a^{\dagger}$ in energy eigenspace
$$\displaylines{\left[ \psi(\boldsymbol{r}),\psi^{\dagger}(\boldsymbol{r}') \right]_{\mp}=\delta(\boldsymbol{r}-\boldsymbol{r}') \\ \left[ \psi(\boldsymbol{r}), \psi(\boldsymbol{r}') \right]_{\mp}=\left[ \psi^{\dagger}(\boldsymbol{r}), \psi^{\dagger}(\boldsymbol{r}') \right]_{\mp}=0}$$
### Example: free particle
- The free particle Hamiltonian:
$$H=\frac{p^{2}}{2m}$$
- Let there be particles _for each wavenumber_ $\boldsymbol{k}$, with corresponding operators $a_{\boldsymbol{k}}, a_{\boldsymbol{k}}^{\dagger}$
- Position eigenstates:
$$\braket{ \boldsymbol{k} | \boldsymbol{r} }=\exp(-i\boldsymbol{k}\cdot \boldsymbol{r}) $$
- The field operators:
$$\psi^{\dagger}(\boldsymbol{r})=\sum_{\boldsymbol{k}} \exp(-i\boldsymbol{k}\cdot \boldsymbol{r}) a_{\boldsymbol{k}}^{\dagger}\hspace{1cm}\psi(\boldsymbol{r})=\sum_{\boldsymbol{k}} \exp(i\boldsymbol{k}\cdot \boldsymbol{r}) a_{\boldsymbol{k}}$$
## Representation of operators

### One particle operators
- A _one particle operator_ consists of a _sum_ of terms, _one for each particle_
- As the particles are _indistinguishable_, each term must be the _same_

- Operator $A$ acting on a single particle of state $\ket{\varphi_{\beta}}$:
$$A\ket{\varphi_{\beta}}=\sum_{\alpha} \ket{\varphi_{\alpha}} \braket{ \varphi_{\alpha}|A |\varphi_{\beta}  } \equiv\sum_{\alpha}A_{\alpha\beta}\ket{\varphi_{\alpha}}   $$
- $A_{\alpha\beta}\equiv \braket{ \varphi_{\alpha} |A|\varphi_{\beta}  }$ are the _matrix elements_:
$$A=\sum_{\alpha,\beta}A_{\alpha\beta}\ket{\varphi_{\alpha}}\bra{\varphi_{\beta}}  $$

- For a _second quantised operator_:
$$\hat{A}=\sum_{\alpha,\beta} A_{\alpha\beta} a_{\alpha}^{\dagger}a_{\beta}$$
- Proof: [[#Common commutation relations|commutation relations]], $a\ket{\text{VAC}}=0$, replicate action on $\ket{\varphi_{\beta}}$

- _Looks_ like the _expectation value_ for the _single particle_, with wavefunction:
$$\ket{\psi}=\sum_{\alpha} a_{\alpha} \ket{\varphi_{\alpha}} \implies \left<a\right>= \sum_{\alpha,\beta} A_{\alpha\beta} a_{\alpha}^{*}a_{\beta}  $$
- As it is a multiplication of _operators_ instead of coefficients, the _order matters_
	- Origin of "second quantisation"

- _Every_ single particle operator $A$ has a _second quantised counterpart_ $\hat{A}$, which is _formally identical_ to the _expectation value_ of $A$

### Hamiltonian
- Example: the _Hamiltonian_
$$\hat{H}\equiv \sum_{\alpha,\beta}H_{\alpha\beta} a_{\alpha}^{\dagger}a_{\beta} $$
- In the _energy eigenbasis_, this becomes:
$$\hat{H}= \sum_{\alpha} E_{\alpha}a_{\alpha}^{\dagger}a_{\alpha}=\sum_{\alpha}E_{\alpha}\hat{N}_{\alpha}$$
- In the _position eigenbasis_:
$$\begin{align}
\hat{H}&=\int  \, d\boldsymbol{r}\left[ -\frac{\hbar^{2}}{2m}\psi ^{\dagger}(\boldsymbol{r})\nabla^{2}\psi(\boldsymbol{r})+V(\boldsymbol{r})\psi ^{\dagger}(\boldsymbol{r})\psi(\boldsymbol{r}) \right] \\ &= \int  \, d\boldsymbol{r}\left[ \frac{\hbar^{2}}{2m}\nabla\psi ^{\dagger}(\boldsymbol{r})\cdot\nabla\psi(\boldsymbol{r})+V(\boldsymbol{r})\psi ^{\dagger}(\boldsymbol{r})\psi(\boldsymbol{r}) \right]
\end{align}$$
- From the [[Quantum Dynamics#Dynamics in the Heisenberg picture|Heisenberg equation of motion]]:
$$i\hbar \frac{\partial }{\partial t}\psi(\boldsymbol{r},t)=-\left[ \hat{H} ,\psi(\boldsymbol{r},t)\right]=-\frac{\hbar^{2}}{2m}\nabla^{2}\psi(\boldsymbol{r},t)+V(\boldsymbol{r})\psi(\boldsymbol{r},t)$$
- This is the _time-dependent Schrodinger equation_ for the _field operator_

### Probability current
- Similarly, one can define the _probability current_:
$$\hat{j}(\boldsymbol{r})=-\frac{i\hbar}{2m}[\psi ^{\dagger}(\boldsymbol{r})\nabla \psi(\boldsymbol{r})-\psi(\boldsymbol{r})\nabla \psi ^{\dagger}(\boldsymbol{r})]$$
### Single particle density
- The _density_ of particles:
$$\rho(\boldsymbol{x})=\sum_{i} \delta(\boldsymbol{x}-\boldsymbol{r}_{i})$$
- It is _diagonal_ in the position basis
- Single particle: the _expectation value_ is simply the _probability density_ in position space

- The corresponding _second quantised form_:
$$\hat{\rho}(\boldsymbol{x})=\int  \, d\boldsymbol{r}\,\psi^{\dagger}(\boldsymbol{r})\psi(\boldsymbol{r})\delta(\boldsymbol{x}-\boldsymbol{r}) =\psi^{\dagger}(\boldsymbol{x})\psi(\boldsymbol{x})$$

- Using the [[#Field operators|definition of the field operator]], integrating _over position_:
$$\int  \, d\boldsymbol{x} \,\psi^{\dagger}(\boldsymbol{x}) \psi(\boldsymbol{x})=\sum_{\alpha} a_{\alpha}^{\dagger}a_{\alpha}=\sum_{\alpha}N_{\alpha} $$
- This gives the _total number_ of particles, as expected

- _Expectation value_ for some state:
$$\left\langle  \hat{\rho}(\boldsymbol{x})  \right\rangle = \braket{ N_{0}N_{1}\dots |\hat{\rho}(\boldsymbol{x}) |N_{0}N_{1}\dots  }=\sum_{\alpha}N_{\alpha} \left| \varphi_{\alpha}(\boldsymbol{x}) \right|^{2} $$
- The _number of particles_ in each state is _weighted_ by the probability density
### Single particle density matrix
- Define the _single particle density matrix_
	- _Generalisation_ of the single particle density, involving two positions
$$g(\boldsymbol{r},\boldsymbol{r}')=\left<\psi^{\dagger}(\boldsymbol{r})\psi(\boldsymbol{r}')\right>$$
- To check:
$$g(\boldsymbol{r},\boldsymbol{r})=\left<\psi^{\dagger}(\boldsymbol{r})\psi(\boldsymbol{r})\right>=\left<\hat{\rho}(\boldsymbol{r})\right>$$
- For the state $\ket{N_{0}N_{1}\dots}$:
$$g(\boldsymbol{r},\boldsymbol{r}')=\sum_{\alpha}N_{\alpha}\varphi_{\alpha}^{*}(\boldsymbol{r})\varphi_{\alpha}(\boldsymbol{r}')$$

- For the _Fermi gas_, in its _ground state_:
$$\begin{align}
g(\boldsymbol{r},\boldsymbol{r}')&=\frac{1}{V} \sum_{|\boldsymbol{k}|<k_{F}}\exp[-i\boldsymbol{k}\cdot(\boldsymbol{r}-\boldsymbol{r}')] \\ &= \frac{k_{F}^{3}}{2\pi^{2}} \left[ \frac{\sin(k_{F}|\boldsymbol{r}-\boldsymbol{r}'|)}{(k_{F}|\boldsymbol{r}-\boldsymbol{r}'|)^{3}} -  \frac{\cos(k_{F}|\boldsymbol{r}-\boldsymbol{r}'|)}{(k_{F}|\boldsymbol{r}-\boldsymbol{r}'|)^{2}} \right]
\end{align}$$
- Calculating the correlation _at the same position_ simply gives the _number density_:
$$g(\boldsymbol{r},\boldsymbol{r})=\frac{k_{F}^{3}}{6\pi^{2}}=n$$

- $g(\boldsymbol{r},\boldsymbol{r})$ to number density
![[Fermi gas single particle density.png]]

- For the _non-degenerate Bose gas_:
$$g(\boldsymbol{r},\boldsymbol{r}')=\sum_{\boldsymbol{k}} \frac{\exp(-E_{k}/k_{B}T)}{Z} \exp[i\boldsymbol{k}\cdot(\boldsymbol{r}'-\boldsymbol{r})]$$
- Similarly falls off with a _characteristic length scale_

### Density-density correlations and Wick's Theorem
- Consider the _density-density correlation_:
$$\left<\rho(\boldsymbol{r})\rho(\boldsymbol{r}')\right> = \left<\psi^{\dagger}(\boldsymbol{r})\psi(\boldsymbol{r})\psi^{\dagger}(\boldsymbol{r}') \psi(\boldsymbol{r}')\right>$$
- Qualitatively, one expects different behaviour for _fermions and bosons_
- They have _different_ [[#Field operators|commutation relations]]
	- For _bosons/fermions_, field operators of different positions _commute/anticommute_
- It describes the _probability_ that $\boldsymbol{r}$ and $\boldsymbol{r}'$ are _both occupied_ by a particle

- _Expanding_ (with $+$ for bosons and $-$ for fermions)
$$\left<\rho(\boldsymbol{r})\rho(\boldsymbol{r}')\right>=\left<\psi^{\dagger}(\boldsymbol{r})\psi^{\dagger}(\boldsymbol{r}')\psi(\boldsymbol{r}) \psi(\boldsymbol{r}')\right> \pm\delta(\boldsymbol{r}-\boldsymbol{r}')\left<\psi^{\dagger}(\boldsymbol{r})\psi(\boldsymbol{r}')\right>$$
- There is a _self-correlation term_ $\delta(\boldsymbol{r}-\boldsymbol{r}')\left<\rho(\boldsymbol{r})\right>$
	- Given by the _mean density_

- Use _normal ordering_: all _creation operators_ to the _left_, annihilation operators on the right, including the _signature_ of the permutation:
	- To maintain the _sign_, it must be an _even permutation_
$$\displaylines{a_{\alpha}a_{\beta}^{\dagger}=\delta_{\alpha\beta}\pm a_{\beta}^{\dagger}a_{\alpha}\hspace{1.5cm} :a_{\alpha}^{\dagger}a_{\beta}:=\pm a_{\beta}^{\dagger}a_{\alpha} \\ \left<\rho(\boldsymbol{r})\rho(\boldsymbol{r}')\right>= \left<:\rho(\boldsymbol{r})\rho(\boldsymbol{r}'):\right>+\delta(\boldsymbol{r}-\boldsymbol{r}')\langle \rho(\boldsymbol{r}) \rangle }$$
- The proper _density-density correlation_:
$$C_{\rho}(\boldsymbol{r},\boldsymbol{r}')=\left<:\rho(\boldsymbol{r})\rho(\boldsymbol{r}'):\right>$$
- It describes a _joint_ probability density of finding particles at $\boldsymbol{r}$ and $\boldsymbol{r}'$, but _removing_ the _mean density_
	- _Normal ordering_ effectively _removes_ particles at $\boldsymbol{r}$ and $\boldsymbol{r}'$ by applying $\psi(\boldsymbol{r})\psi(\boldsymbol{r}')$

- Go to the _energy representation_:
$$\left<\rho(\boldsymbol{r})\rho(\boldsymbol{r}')\right>=\sum_{\alpha,\beta,\gamma,\delta} \varphi_{\alpha}^{*}(\boldsymbol{r})\varphi_{\beta}(\boldsymbol{r})\varphi_{\gamma}^{*}(\boldsymbol{r}')\varphi_{\delta}(\boldsymbol{r}') \left\langle a_{\alpha}^{\dagger}a_{\beta}a_{\gamma}^{\dagger}a_{\delta} \right\rangle  $$
- For a state of form $\ket{N_{0}N_{1}\dots}$, the sum is _non-zero_ for:
$$\alpha=\beta,\gamma=\delta \hspace{1cm}\text{ or }\hspace{1cm}\alpha=\delta,\beta=\gamma$$
- _Ignore_ the case $\alpha=\beta=\gamma=\delta$ (does not matter for _large particle number_)

- _Wick's Theorem_:
$$\begin{align}
\left<\rho(\boldsymbol{r})\rho(\boldsymbol{r})'\right> &= \sum_{\alpha,\gamma} |\varphi_{\alpha}(\boldsymbol{r})|^{2}|\varphi_{\gamma}(\boldsymbol{r}')|^{2} N_{\alpha}N_{\gamma} \\ &+ \sum_{\alpha,\gamma} \left(\varphi_{\alpha}^{*}(\boldsymbol{r})\varphi_{\alpha}(\boldsymbol{r}')\right)\left(\varphi_{\gamma}(\boldsymbol{r})\varphi_{\gamma}^{*}(\boldsymbol{r}')\right) N_{\alpha}(1\pm N_{\gamma})
\end{align}$$
- The $N_{\alpha}$ term originates from the _self-correlation_
- Using the completeness relation for the _position eigenstates_:
$$C_{\rho}(\boldsymbol{r},\boldsymbol{r}')= \left<\rho(\boldsymbol{r})\right>\left<\rho(\boldsymbol{r}')\right> \pm g(\boldsymbol{r},\boldsymbol{r}')g(\boldsymbol{r}',\boldsymbol{r})$$

- For _fermions_, as $\boldsymbol{r}\to \boldsymbol{r}'$, the density correlation tends to _zero_
- This is an _anti-bunching effect_
![[Fermion density correlation.png]]
- For _bosons_, there is a _bunching effect_
	- Starts at a finite value, then drops off and plateaus to _half_ the value

### Two body operators
- A _two-particle_ operator consists of a _sum of terms_ that act between _pairs of particles_

- In _general_, it can be written as:
$$\hat{A}_{2}=\frac{1}{2}\sum_{i,j,k,l}A_{ijkl}a^{\dagger}_{i}a^{\dagger}_{j}a_{k}a_{l}$$
- $A_{ijkl}$ is some _two-body matrix element_

- Example: the _interaction Hamiltonian_, summing over potential energy of _pairs_
$$H_\text{int}=\frac{1}{2}\sum_{i\neq j} U(\boldsymbol{r}_{i}-\boldsymbol{r}_{j})=\sum_{i<j}U(\boldsymbol{r}_{i}-\boldsymbol{r}_{j})$$
- To count _pairs_ of particles, consider:
$$\frac{1}{2}\int  \, d\boldsymbol{r} d\boldsymbol{r}' \rho(\boldsymbol{r}) U(\boldsymbol{r}-\boldsymbol{r}') \rho(\boldsymbol{r}') $$
- This contains _self-interaction terms_

- Therefore, use [[#Density-density correlations|normal ordering]]:
	- To preserve _sign_, have it be an _even permutation_
$$\begin{align}
H_\text{int}&= \frac{1}{2} \int  \, d\boldsymbol{r}\,d\boldsymbol{r}' :\rho(\boldsymbol{r})U(\boldsymbol{r}-\boldsymbol{r}')\rho(\boldsymbol{r}'):\\&=\frac{1}{2}\int  \, d\boldsymbol{r}\,d\boldsymbol{r}' \psi ^{\dagger}(\boldsymbol{r})\psi ^{\dagger}(\boldsymbol{r}')U(\boldsymbol{r}-\boldsymbol{r}')\psi(\boldsymbol{r}')\psi(\boldsymbol{r}) 
\end{align} $$
- The _expectation value_, using [[#Density-density correlations and Wick's Theorem|Wick's Theorem]]:
$$\left<H_\text{int}\right>= \frac{1}{2} \int d\boldsymbol{r} \, d\boldsymbol{r}' \left<\rho(\boldsymbol{r})\right>U(\boldsymbol{r}-\boldsymbol{r}') \left<\rho(\boldsymbol{r}')\right> \pm \frac{1}{2}\int d\boldsymbol{r}  \, d\boldsymbol{r}' U(\boldsymbol{r}-\boldsymbol{r}')g(\boldsymbol{r},\boldsymbol{r}')g(\boldsymbol{r}',\boldsymbol{r})  $$
- The first term is the _Hartree_ term
- The second term is the _Fock term_, accounting for _exchange energy_

- With _pairwise interactions_, the _full second quantised Hamiltonian_:
$$\begin{align}
H= &\int  \, d\boldsymbol{r}\left[ \frac{\hbar^{2}}{2m}\nabla\psi ^{\dagger}(\boldsymbol{r})\cdot\nabla\psi(\boldsymbol{r})+V(\boldsymbol{r})\psi ^{\dagger}(\boldsymbol{r})\psi(\boldsymbol{r}) \right] \\ &+ \frac{1}{2}\int  \, d\boldsymbol{r}\,d\boldsymbol{r}' \psi ^{\dagger}(\boldsymbol{r})\psi ^{\dagger}(\boldsymbol{r}')U(\boldsymbol{r}-\boldsymbol{r}')\psi(\boldsymbol{r}')\psi(\boldsymbol{r})
\end{align}$$
## Bose-Hubbard model
- Model for a _lattice_, where a particle can _hop_ along the lattice
$$\hat{H}=-J \sum_{<i,j>} \left( a^{\dagger} _{i}a_{j}+a_{j}^{\dagger}a_{i}\right) +\frac{U}{2} \sum_{i} \hat{n}_{i}\left( \hat{n}_{i}-1 \right)$$
- There is a _hopping kinetic energy_ and an _interaction term_ depending on _number of particles_ $\hat{n}_{i}=a_{i}^{\dagger}a_{i}$ at the site
- In the _tight binding_ approximation, kinetic energies are _summed over nearest neighbours_

- The operators $a_{i}$ _create/annihilate_ particles at _site_ $i$, then _another particle_ at site $j$ is created, indicating the particle _hoppinh_
	- Wave functions: _Wannier state_ orbitals $\varphi_{i}(\boldsymbol{x})$
$$a_{i}^{\dagger}=\int \varphi_{i}(x)\psi ^{\dagger}(x) \, dx \hspace{1.5cm}[a_{i},a_{j}^{\dagger}]=\delta_{ij}$$

- The limit $J\gg U$ has the _kinetic energy_ dominate
- The states are effectively _plane waves_ (momentum eigenstates)

- The limit $J\ll U$ has the particles _localised_, with one particle per site
- They are _position_ eigenstates

- The _phase transition_ is a function of the _ratio_ $J/U$

### Bose-Einstein condensation
- Go to the limit $J\gg U$, the states are approximately _plane waves_ 
	- _Delocalised_ in real space, localised in momentum space
- _Plane wave basis_ (from [[#Field operators|change of basis]])
$$\hat{\tilde{a}}_{k}=\frac{1}{\sqrt{ N }} \sum_{j=1}^{N} \exp(ika_{j}) a_{j}$$
- Inserting a _delta function_

- The Hamiltonian becomes:
$$\hat{H}=\sum_{k}\varepsilon_{k}\hat{\tilde{a}}_{k}^{\dagger}\hat{\tilde{a}}_{k}$$
- The _dispersion relation_ has a _minimum_
- There is a _Bose-Einstein condensate_ formed at that minimum energy
$$\ket{\psi _\text{BEC}}=\frac{1}{\sqrt{ N! }} \left( \hat{\tilde{a}}^{\dagger}_{k=0} \right)^{N}\ket{\text{VAC}}  $$
- Consider the [[#Single particle density matrix]]
- It _plateaus_ into a finite value at $|\boldsymbol{r}-\boldsymbol{r}'| \to \infty$
- It has _long range order_

$$g(i,j)=\left<a_{i}^{\dagger}a_{j}\right> = \frac{1}{N!} \braket{  |  } $$
- Commutation relations:
$$\left[ \hat{\tilde{a}}_{i},\hat{\tilde{a}}_{i}^{\dagger} \right]=\frac{1}{\sqrt{ N }} \implies \left[ a_{i} \right]$$
- This gives $g$ as _constant_ in the limit

### Mott insulator
- Go to the limit $J\ll U$
- Particles are _localised_ in position space

$$\ket{\text{Mott}}= \prod_{i=1}^{N} a_{i}^{\dagger} \ket{\text{VAC}}  $$
$$g(i,j)=\delta_{ij}=n_{0}$$
## Bogoliubov Theory
- Take the $J\gg U$ limit, then use _perturbation theory_ using the momentum eigenstates

- The Hamiltonian:
$$\hat{H}=\sum_{k}\varepsilon_{k}a_{k}^{\dagger}a_{k} + \frac{U}{2N}\sum_{p,q}$$
- Make a _coherent state_ from the Bose-Einstein condensate:
$$\ket{\text{BEC}} \propto \exp\left( \sqrt{ N }\hat{\tilde{a}}_{0}^{\dagger} \right)\ket{\text{VAC}}  $$
- The _particle number_ is _indefinite_, but with an _expectation value_ of $N$

- The Hamiltonian has $U(1)$ _gauge symmetry_

- To make it a _mean field theory_, take an average:
$$\hat{H}=$$
- The _Bogoliubov transformation_:
$$\alpha_{k}=$$
- Gauge symmetry
	- Goldstone mode

## Interference of Bose-Einstein condensates
- The wave-function for a _Bose condensate_ of ground state $\varphi_{0}(\boldsymbol{r})$
$$\ket{\Psi}=\frac{1}{\sqrt{ N! }} \left( a_{0}^{\dagger} \right)^{N} \ket{\text{VAC}}  $$


- Let there be a Bose-Einstein condensate initially in a _trap_
- Let the trap be _released_

- Dispersion: Gaussian

- Long times: linearly growing width
### Double well