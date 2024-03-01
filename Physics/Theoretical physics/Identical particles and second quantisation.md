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
$$\displaylines{\ket{\Psi _\text{in}}= \frac{1}{\sqrt{ 2 }}[\ket{A,\text{in} }_{1}\ket{B,\text{in}}_{2} + \ket{A,\text{in} }_{2}\ket{B,\text{in}}_{1}  ] \\ \downarrow\\\ket{\Psi _\text{out}}= } $$
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
$$\displaylines{\hat{a}_{\alpha}^{\dagger}\ket{\Psi_{\alpha_{1}\alpha_{2}\dots\alpha_{N}}}=\sqrt{ N+1 }\ket{\phi_{\alpha}}\ket{\Psi_{\alpha_{1}\alpha_{2}\dots\alpha_{N}}}  }$$

### Bosons
- For _bosons_:
$$\hat{a}_{\alpha}^{\dagger}\ket{\Psi^{S}_{\alpha_{1}\alpha_{2}\dots\alpha_{N}}}=\sqrt{ N+1 }\mathcal{S}\left\{\ket{\phi_{\alpha}}\ket{\Psi^{S}_{\alpha_{1}\alpha_{2}\dots\alpha_{N}}}\right\}$$
- Labelling by _occupation number_:
$$\displaylines{\hat{a}^{\dagger}_{\alpha}\ket{N_{1}N_{2}\dots N_{\alpha}\dots N_{N}}=\sqrt{ N_{\alpha}+1 }\ket{N_{1}N_{2}\dots N_{\alpha}+1\dots N_{N}}\\\hat{a}_{\alpha}\ket{N_{1}N_{2}\dots N_{\alpha}\dots N_{N}}=\sqrt{ N_{\alpha} }\ket{N_{1}N_{2}\dots N_{\alpha}-1\dots N_{N}}  }$$
- From this, one can show:
$$\left[ \hat{a}_{\alpha},\hat{a}_{\beta}^{\dagger} \right]=\delta_{\alpha\beta} \hspace{1cm}\left[ \hat{a}_{\alpha},\hat{a}_{\beta} \right]=\left[ \hat{a}_{\alpha}^{\dagger}, \hat{a}_{\beta}^{\dagger} \right]=0$$
- Then define the _number operator_:
$$\hat{N}_{\alpha}=\hat{a}^{\dagger}_{\alpha}\hat{a}_{\alpha}$$
- The _normalised state_ can then be written as:
$$\ket{N_{1}N_{2},\dots N_{N}} =\prod_{\alpha} \frac{\left( \hat{a}^{\dagger}_{\alpha} \right)^{N_{\alpha}}}{\sqrt{ N_{\alpha}! }}\ket{00\dots0} $$
- $\ket{00\dots{0}}$ is the _vacuum state_, and represents _no quanta in any state_:
$$\ket{\text{VAC}}=\ket{00\dots0}  $$

- This is an _identical algebra_ to the [[Quantum Harmonic Oscillator]]
- Example: _photons_ and the [[Quantum electrodynamics|EM field]]

### Fermions
$$\hat{a}_{\alpha}^{\dagger}\ket{\Psi^{A}_{\alpha_{1}\alpha_{2}\dots\alpha_{N}}}=\sqrt{ N+1 }\mathcal{A}\left\{\ket{\phi_{\alpha}}\ket{\Psi^{A}_{\alpha_{1}\alpha_{2}\dots\alpha_{N}}}\right\}$$
- They obey _anticommutation relations_
$$\left\{ \hat{a}_{\alpha},\hat{a}_{\beta}^{\dagger} \right\}=\delta_{\alpha\beta} \hspace{1cm}\left\{ \hat{a}_{\alpha},\hat{a}_{\beta} \right\}=\left\{ \hat{a}_{\alpha}^{\dagger},\hat{a}_{\beta} \right\}=0$$
- One _cannot create two fermions in the same state_

- Building up a general state:
$$\ket{N_{0}N_{1}\dots N_{N}}=\prod_{\alpha} \left( \hat{a}^{\dagger}_{\alpha} \right)^{N_{\alpha}}\ket{\text{VAC}} $$
- The occupation numbers $N_{\alpha}$ are _either_ $0$ or $1$
- The _ordering_ of operators is significant due to the anticommutation relations

### Field operators
- The _unitary change of basis_:
$$\{\phi_{\alpha}\}\to \{\tilde{\phi}_{\alpha}\}$$
$$\ket{\tilde{\phi}_{\alpha}}=\sum_{\beta} =\sum_{\beta} \braket{ \phi_{\beta} | \tilde{\phi}_{\alpha} }\hat{a}_{\beta}\ket{\text{VAC}}  $$
- Therefore, the transformation _for the operator_:
$$\hat{\tilde{a}}_{\alpha} =\sum_{\beta} \braket{ \phi_{\beta} | \tilde{\phi}_{\alpha} }\hat{a}_{\beta}  $$
- Transforming to _position eigenstates_ $\ket{\tilde{\phi}_{\alpha}}=\ket{\boldsymbol{r}}$
$$\displaylines{\braket{ \phi_{\beta} | \boldsymbol{r} }=\phi_{\beta}^{*} \\ \sum_{\beta}\phi_{\beta}^{*}(\boldsymbol{r})\phi_{\beta}(\boldsymbol{r}')=\delta(\boldsymbol{r}-\boldsymbol{r}')}$$
- Define the _field operator_, the _creation_ operator in _position space_:
$$\hat{\psi}^{\dagger}(\boldsymbol{r})\equiv \sum_{\beta}\phi_{\beta}^{*}(\boldsymbol{r})\hat{a}^{\dagger}_{\beta}$$
- The corresponding _annihilation operator_:
$$\hat{\psi}(\boldsymbol{r})\equiv \sum_{\beta} \phi_\beta(\boldsymbol{r})\hat{a}_{\beta}$$

- (Anti-)commutation, depending on _bosons/fermions_
	- Same relations as those for $\hat{a},\hat{a}^{\dagger}$ in energy eigenspace
$$\displaylines{\left[ \hat{\psi}(\boldsymbol{r}),\hat{\psi}^{\dagger}(\boldsymbol{r}') \right]_{\mp}=\delta(\boldsymbol{r}-\boldsymbol{r}') \\ \left[ \hat{\psi}(\boldsymbol{r}), \hat{\psi}(\boldsymbol{r}') \right]_{\mp}=\left[ \hat{\psi}^{\dagger}(\boldsymbol{r}), \hat{\psi}^{\dagger}(\boldsymbol{r}') \right]_{\mp}=0}$$
### Example: free particle
- The free particle Hamiltonian:
$$H=\frac{p^{2}}{2m}$$
- Let there be particles _for each wavenumber_ $\boldsymbol{k}$, with corresponding operators $\hat{a}_{\boldsymbol{k}}, \hat{a}_{\boldsymbol{k}}^{\dagger}$
- Position eigenstates:
$$\braket{ \boldsymbol{k} | \boldsymbol{r} }=\exp(-i\boldsymbol{k}\cdot \boldsymbol{r}) $$
- The field operators:
$$\hat{\psi}^{\dagger}(\boldsymbol{r})=\sum_{\boldsymbol{k}} \exp(-i\boldsymbol{k}\cdot \boldsymbol{r}) \hat{a}_{\boldsymbol{k}}^{\dagger}\hspace{1cm}\hat{\psi}(\boldsymbol{r})=\sum_{\boldsymbol{k}} \exp(i\boldsymbol{k}\cdot \boldsymbol{r}) \hat{a}_{\boldsymbol{k}}$$
## Representation of operators

### One particle operators
- A _one particle operator_ consists of a _sum_ of terms, _one for each particle_
- As the particles are _indistinguishable_, each term must be the _same_

- Operator $A$ acting on a single particle of state $\ket{\varphi_{\beta}}$:
$$A\ket{\varphi_{\beta}}=\sum_{\alpha} \ket{\varphi_{\alpha}} \braket{ \varphi_{\alpha}|A |\varphi_{\beta}  } \equiv\sum_{\alpha}A_{\alpha\beta}\ket{\varphi_{\alpha}}   $$
- $A_{\alpha\beta}\equiv \braket{ \varphi_{\alpha} |A|\varphi_{\beta}  }$ are the _matrix elements_:
$$A=\sum_{\alpha,\beta}A_{\alpha\beta}\ket{\varphi_{\alpha}}\bra{\varphi_{\beta}}  $$

- For a _second quantised operator_:
$$\hat{A}_{\alpha\beta}=\sum_{\alpha,\beta} A_{\alpha\beta} \hat{a}_{\alpha}^{\dagger}\hat{a}_{\beta}$$
- Proof: commutation relations, $\hat{A}\ket{\text{VAC}}=0$, replicate action on $\ket{\varphi_{\beta}}$

- _Looks_ like the _expectation value_ for the _single particle_, with wavefunction:
$$\ket{\psi}=\sum_{\alpha} a_{\alpha} \ket{\varphi_{\alpha}} \implies \left<\hat{A}\right>= \sum_{\alpha,\beta} A_{\alpha\beta} a_{\alpha}^{*}a_{\beta}  $$
- As it is a multiplication of _operators_ instead of coefficients, the _order matters_
	- Origin of "second quantisation"

- _Every_ single particle operator $A$ has a _second quantised counterpart_ $\hat{A}$, which is _formally identical_ to the _expectation value_ of $A$

- Example: the _Hamiltonian_
$$\hat{H}\equiv \sum_{\alpha,\beta}H_{\alpha\beta} \hat{a}_{\alpha}^{\dagger}\hat{a}_{\beta} $$
- In the _energy eigenbasis_, this becomes:
$$\hat{H}= \sum_{\alpha} E_{\alpha}\hat{a}_{\alpha}^{\dagger}\hat{a}_{\alpha}=\sum_{\alpha}E_{\alpha}\hat{N}_{\alpha}$$

### Single particle density
- The _density_ of particles:
$$\rho(\boldsymbol{x})=\sum_{i} \delta(\boldsymbol{x}-\boldsymbol{r}_{i})$$
- It is _diagonal_ in the position basis
- Single particle: the _expectation value_ is simply the _probability density_ in position space

- The corresponding _second quantised form_:
$$\hat{\rho}(\boldsymbol{x})=\int  \, d\boldsymbol{r}\,\hat{\psi}^{\dagger}(\boldsymbol{r})\hat{\psi}(\boldsymbol{r})\delta(\boldsymbol{x}-\boldsymbol{r}) =\hat{\psi}^{\dagger}(\boldsymbol{x})\hat{\psi}(\boldsymbol{x})$$
- Using the [[#Change of basis|definition of the field operator]], integrating _over position_:
$$\int  \, d\boldsymbol{x} \,\hat{\psi}^{\dagger}(\boldsymbol{x}) \hat{\psi}(\boldsymbol{x})=\sum_{\alpha} \hat{a}_{\alpha}^{\dagger}\hat{a}_{\alpha}=\sum_{\alpha}N_{\alpha} $$
- Similar to the _number operator_, counting particles at each _position_

- _Expectation value_ for some state:
$$\braket{ N_{0}N_{1}\dots |\hat{\rho}(\boldsymbol{x}) |N_{0}N_{1}\dots  }=\sum_{\alpha}N_{\alpha} \left| \varphi_{\alpha}(\boldsymbol{x}) \right|^{2} $$
### Single particle density matrix
- Define the _single particle density matrix_
	- _Generalisation_ of the single particle density, involving two positions
$$g(\boldsymbol{r},\boldsymbol{r}')=\left<\hat{\psi}^{\dagger}(\boldsymbol{r})\hat{\psi}(\boldsymbol{r}')\right>$$
- To check:
$$g(\boldsymbol{r},\boldsymbol{r})=\left<\hat{\psi}^{\dagger}(\boldsymbol{r})\hat{\psi}(\boldsymbol{r})\right>=\left<\hat{\rho}(\boldsymbol{r})\right>$$
- For the state $\ket{N_{0}N_{1}\dots}$:
$$g(\boldsymbol{r},\boldsymbol{r}')=\sum_{\alpha}N_{\alpha}\varphi_{\alpha}^{*}(\boldsymbol{r})\varphi_{\alpha}(\boldsymbol{r}')$$

- For the _Fermi gas_:
$$g(\boldsymbol{r},\boldsymbol{r}')=\frac{1}{V} \sum_{|\boldsymbol{k}|<k_{F}}\exp[-i\boldsymbol{k}\cdot(\boldsymbol{r}-\boldsymbol{r}')]$$

- $g(\boldsymbol{r},\boldsymbol{r})$ to number density
![[Fermi gas single particle density.png]]

- For the _non-degenerate Bose gas_:
$$g(\boldsymbol{r},\boldsymbol{r}')=\sum_{\boldsymbol{k}} \frac{\exp(-E_{k}/k_{B}T)}{Z} \exp[i\boldsymbol{k}\cdot(\boldsymbol{r}'-\boldsymbol{r})]$$
- Similarly falls off with a _characteristic length scale_

### Density-density correlations
- Consider the _density-density correlation_:
$$\left<\rho(\boldsymbol{r})\rho(\boldsymbol{r}')\right> = \left<\hat{\psi}^{\dagger}(\boldsymbol{r})\hat{\psi}(\boldsymbol{r})\hat{\psi}^{\dagger}(\boldsymbol{r}') \hat{\psi}(\boldsymbol{r}')\right>$$
- Qualitatively, one expects different behaviour for _fermions and bosons_
- They have _different_ [[#Field operators|commutation relations]]
	- For _bosons/fermions_, field operators of different positions _commute/anticommute_
- It describes the _probability_ that $\boldsymbol{r}$ and $\boldsymbol{r}'$ are both _occupied_ by a particle

- Expanding:
$$\left<\rho(\boldsymbol{r})\rho(\boldsymbol{r}')\right>=\left<\hat{\psi}^{\dagger}(\boldsymbol{r})\hat{\psi}^{\dagger}(\boldsymbol{r}')\hat{\psi}(\boldsymbol{r}) \hat{\psi}(\boldsymbol{r}')\right> +\delta(\boldsymbol{r}-\boldsymbol{r}')\left<\hat{\psi}^{\dagger}(\boldsymbol{r})\hat{\psi}(\boldsymbol{r}')\right>$$
- There is a _self-correlation term_ $\delta(\boldsymbol{r}-\boldsymbol{r}')\left<\rho(\boldsymbol{r})\right>$
	- Given by the _mean density_

- Use _normal ordering_: all _creation operators_ to the _left_, annihilation operators on the right
$$\left<:\rho(\boldsymbol{r})\rho(\boldsymbol{r}'):\right>= \left<\rho(\boldsymbol{r})\rho(\boldsymbol{r}')\right>+\text{self correlation term}$$
- The proper _density-density correlation_:
$$C_{\rho}(\boldsymbol{r},\boldsymbol{r}')=\left<:\rho(\boldsymbol{r})\rho(\boldsymbol{r}'):\right> =\left<\hat{\psi}^{\dagger}(\boldsymbol{r})\hat{\psi}^{\dagger}(\boldsymbol{r}')\hat{\psi}(\boldsymbol{r}) \hat{\psi}(\boldsymbol{r}')\right>$$

- Go to the _energy representation_:
$$\left<\rho(\boldsymbol{r})\rho(\boldsymbol{r}')\right>=\sum_{\alpha,\beta,\gamma,\delta} $$
- For a state of form $\ket{N_{0}N_{1}\dots}$
- Sum over possible correlations

- _Wick's Theorem_:
$$\begin{align}
\left<\rho(\boldsymbol{r})\rho(\boldsymbol{r})'\right> &= \sum_{\alpha,\gamma} \dots N_{\alpha}N_{\gamma} \\ &+ \sum_{\alpha,\gamma} \dots N_{\alpha}(1\pm N_{\gamma})
\end{align}$$
- The $N_{\alpha}$ term originates from the _self-correlation_
- Reading off the formula for normal ordering:
$$\begin{align}
C_{\rho}(\boldsymbol{r},\boldsymbol{r}')&= \left<\rho(\boldsymbol{r})\right>\left<\rho(\boldsymbol{r}')\right> \pm g(\boldsymbol{r},\boldsymbol{r}')g(\boldsymbol{r}',\boldsymbol{r}) \\ &= n^{2} \pm |g(\boldsymbol{r},\boldsymbol{r}')|^{2}
\end{align}$$

- For _fermions_, as $\boldsymbol{r}\to \boldsymbol{r}'$, the density correlation tends to _zero_
- This is an _anti-bunching effect_
![[Fermion density correlation.png]]
- For _bosons_, there is a _bunching effect_
	- Starts at a finite value, then drops off and plateaus to _half_ the value

### Two body operators
$$\sum_{i,j=1}^{N} A_{ij}$$
- The _interaction Hamiltonian_:
$$H_\text{int}=\frac{1}{2}\sum_{i\neq j} U(\boldsymbol{r}_{i}-\boldsymbol{r}_{j})=\sum_{i<j}U(\boldsymbol{r}_{i}-\boldsymbol{r}_{j})$$
- Summing over particles, consider the expression:
$$\frac{1}{2}\int  \, d\boldsymbol{r} d\boldsymbol{r}' \rho H \rho $$
- This contains _self-interaction terms_

- Use _normal ordering_:
$$H_\text{int}= \frac{1}{2} \int  \, d\boldsymbol{r}\,d\boldsymbol{r}' :\rho(\boldsymbol{r})U(\boldsymbol{r}-\boldsymbol{r}')\rho(\boldsymbol{r}'): $$
- The _expectation value_:
$$\left<H_\text{int}\right>= \frac{1}{2} \int d\boldsymbol{r} \, d\boldsymbol{r}' \left<\rho(\boldsymbol{r})\right>U(\boldsymbol{r}-\boldsymbol{r}') \left<\rho(\boldsymbol{r}')\right> \pm \frac{1}{2}\int d\boldsymbol{r}  \, d\boldsymbol{r}' U(\boldsymbol{r}-\boldsymbol{r}')g(\boldsymbol{r},\boldsymbol{r}')g(\boldsymbol{r}',\boldsymbol{r})  $$
- The first term is the _Hartree_ term
- The second term is the _Fock term_, accounting for _exchange energy_

## Bose-Hubbard model
- Fermions: the _Hubbard model_

- Bosons: modelled by _Bose-Hubbard model_

- Model for a _lattice_, where a particle can _hop_ along the lattice
$$\hat{H}=-J \sum_{<i,j>} \left( \hat{a}^{\dagger} _{i}\hat{a}_{j}+\hat{a}_{j}^{\dagger}\hat{a}_{i}\right) +\frac{U}{2} \sum_{i} \hat{n}_{i}\left( \hat{n}_{i}-1 \right)$$
- There is a _hopping kinetic energy_ (sum over _all neighbouring sites_) and an _interaction term_

- The operators $\hat{a}_{i}$ _create/annihilate_ particles at _site_ $i$
	- Positions: _Wannier states_

- The limit $J\gg U$ has the _kinetic energy_ dominate
- The states are effectively _plane waves_ (momentum eigenstates)

- The limit $J\ll U$ has the particles _localised_, with one particle per site
- They are _position_ eigenstates

### Bose-Einstein condensation
- Go to the limit $J\gg U$, the states are approximately _plane waves_ 
	- _Delocalised_ in real space, localised in momentum space
- Plane wave basis (from [[#Field operators|change of basis]])
$$\hat{\tilde{a}}_{k}=\frac{1}{\sqrt{ N }} \sum_{j=1}^{N} \exp(ika_{j}) \hat{a}_{j}$$
- Inserting a _delta function_

- The Hamiltonian becomes:
$$\hat{H}=\sum_{k}\varepsilon_{k}\hat{\tilde{a}}_{k}^{\dagger}\hat{\tilde{a}}_{k}$$
- The _dispersion relation_ has a _minimum_
- There is a _Bose-Einstein condensate_ formed at that minimum energy
$$\ket{\psi _\text{BEC}}=\frac{1}{\sqrt{ N! }} \left( \hat{\tilde{a}}^{\dagger}_{k=0} \right)^{N}\ket{\text{VAC}}  $$
- Consider the [[#Single particle density matrix]]
- It _plateaus_ into a finite value at $|\boldsymbol{r}-\boldsymbol{r}'| \to \infty$
- It has _long range order_

$$g(i,j)=\left<\hat{a}_{i}^{\dagger}\hat{a}_{j}\right> = \frac{1}{N!} \braket{  |  } $$
- Commutation relations:
$$\left[ \hat{\tilde{a}}_{i},\hat{\tilde{a}}_{i}^{\dagger} \right]=\frac{1}{\sqrt{ N }} \implies \left[ \hat{a}_{i} \right]$$
- This gives $g$ as _constant_ in the limit

### Mott insulator
- Go to the limit $J\ll U$
- Particles are _localised_ in position space

$$\ket{\text{Mott}}= \prod_{i=1}^{N} \hat{a}_{i}^{\dagger} \ket{\text{VAC}}  $$
$$g(i,j)=\delta_{ij}=n_{0}$$
## Bogoliubov Theory
- Take the $J\gg U$ limit, then use _perturbation theory_ using the momentum eigenstates

- The Hamiltonian:
$$\hat{H}=\sum_{k}\varepsilon_{k}\hat{a}_{k}^{\dagger}\hat{a}_{k} + \frac{U}{2N}\sum_{p,q}$$
- Make a _coherent state_ from the Bose-Einstein condensate:
$$\ket{\text{BEC}} \propto \exp\left( \sqrt{ N }\hat{\tilde{a}}_{0}^{\dagger} \right)\ket{\text{VAC}}  $$
- The _particle number_ is _indefinite_, but with an _expectation value_ of $N$

- The Hamiltonian has $U(1)$ _gauge symmetry_

- To make it a _mean field theory_, take an average:
$$\hat{H}=$$
- The _Bogoliubov transformation_:
$$\alpha_{k}=$$
- Gauge symmetry

## Interference of Bose-Einstein condensates
- Let there be a Bose-Einstein condensate initially in a _trap_
- Let the trap be _released_

- Dispersion: Gaussian

- Long times: linearly growing width
### Double well