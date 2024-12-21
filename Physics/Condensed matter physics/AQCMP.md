- Electron-ion Hamiltonian:
$$H=-\sum_{i}\frac{p_{i}^{2}}{2m}+\sum_{i}\frac{P_{i}^{2}}{2M_{i}}-\sum_{i,j} \frac{Z_{i}e^{2}}{4\pi\epsilon_{0}} \frac{1}{|\boldsymbol{R}_{j}-\boldsymbol{r}_{i}|}+\sum_{j<i} \frac{e^{2}}{4\pi\epsilon_{0}} \frac{1}{|\boldsymbol{r}_{i}-\boldsymbol{r}_{j}|}+\sum_{j<i}\frac{Z_{i}Z_{j}e^{2}}{4\pi\epsilon_{0}} \frac{1}{|\boldsymbol{R}_{i}-\boldsymbol{R}_{j}|}$$

- _Approximations_ used:
	- Independent electron approximation
	- Hartree-Fock
	- Density Functional Theory
	- Fermi Liquid Theory

- _Phenomenological_ models are useful for reproducing physical behaviour
	- Ising model/Heisenberg Hamiltonian (ferromagnetism)
	- BCS Hamiltonian (super-conductivity)

- Complex phenomena often _emerge_ from a few simple rules

- _Elementary excitations_: excitations of a many-particle system that _cannot be thought of as combinations of lower energy excitations_
- Can be described using _linear response theory_
- Types: _quasi-particles_, and _collective excitations_

- _Quasi-particle_: Elementary excitation thought of as a _non-interacting particle with modified dispersion relation_
	- Map non-interacting particle + Fermi sphere into an _interacting system_, still end up with Fermi sphere + quasiparticle
	- Examples: interacting electrons, heavy fermions, Cooper pairs

- _Collective excitations_: not easily described in a particle picture, often have _macroscopic_ degrees of freedom
	- Example: _phonons_, the general vibrational state of _atoms_ is a superposition of phonons
	- Example: _magonons_ (spin waves)
	- Example: _plasmons_ (electron density oscillations)

- Collective excitations result from _symmetry breaking_
- The _ground state_ often _breaks_ the symmetry of the Hamiltonian
	- Example: aligned spins in ferromagnet is _not isotropic_, while the Hamiltonian should have $SU(2)$ symmetry
	- Example: _solids_ can have crystal structures that break the symmetry of the Hamiltonian
- Symmetry-breaking ground states are _meta-stable_
	- True ground state is a _coherent superposition_

- The _presence_ of _broken symmetry states_ implies _phase transitions_ at temperature $T_c$
	- Symmetries _cannot change continuously_
	- At $T>T_c$, increase in _entropy_ drives transition to a disordered state
	- At $T<T_c$, the broken symmetry state is _weakened by elementary excitations_
	- States characterised by _order parameter_
- For a _broken continuous symmetry_, there must be _long wavelength elementary excitations_ in the system, with _vanishing energy_
	- Massless [[Classical Field Theory#Goldstone's Theorem|Goldstone bosons]]

- Characteristic _energy scales_:
	- $1\text{ eV}$ per atom - Optical absorption energies, Bonding energies, Plasmon energies
	- $10-100\text{ meV}$ per atom - Optical phonon energies, Exchange energy in ferromagnets, Activation energy for dopants in semiconductors
	- $1-10\text{ meV}$ per atom - Acoustic phonons, Exchange energies in more weakly coupled magnetic systems, Energy of the excitation gap in high $T_c$ superconductors
	- $<1\text{ meV}$ per atom - Energy gap in conventional superconductors

- Room temperature: $k_{B}T \sim 25\text{ meV}$
- At $4\text{ K}$: $k_{B}T \sim 0.3\text{ meV}$

- Interactions:
![[All interactions Hamiltonian.png]]

# Independent Electron Theory

## Lattices
- Bravais lattice vectors: $\boldsymbol{a}_{1},\boldsymbol{a}_{2},\boldsymbol{a}_{3}$
- _Basis_ vectors: $\boldsymbol{\beta}_{i}$

- _Translational_ symmetries define the _Bravais lattice_
![[Bravais lattices 1.png]]
- Crystals also have _point group_ symmetries associated with _rotations, inversions and reflections_, that keep the translational symmetry

- The crystal _space group_ is the _combination_ of all symmetries
	- Lattices are not necessarily _compatible_ with all point groups
	- There are 230 space groups

## Reciprocal lattice
- For a lattice vector $\boldsymbol{R}$, any _reciprocal lattice vector_ $\boldsymbol{G}$ must satisfy:
$$\exp(i\boldsymbol{G}\cdot \boldsymbol{R})=1$$
- Reciprocal lattice vectors:
$$\boldsymbol{b}_{1}=2\pi  \frac{\boldsymbol{a}_{2}\times \boldsymbol{a}_{3}}{\boldsymbol{a}_{1}\cdot(\boldsymbol{a}_{2}\times \boldsymbol{a}_{3})}$$

- The _Wigner-Seitz cell_ is a _primitive cell_ resulting from _Voronoi decomposition_

- The Wigner-Seitz cell of the reciprocal lattice is the _first Brillouin zone_

## Independent electrons
- With the _Born-Oppenheimer approximation_, assuming _no ionic motion_:
$$H_\text{el}=\sum_{i=1}^{N} \left[ \frac{p_{i}^{2}}{2m}-\sum_{k=1}^{M} \frac{Z_{k}e^{2}}{4\pi\epsilon_{0}|\boldsymbol{r}_{i}-\boldsymbol{R}_{k}|} \right] + \sum_{i<j} \frac{e^{2}}{4\pi\epsilon_{0} |\boldsymbol{r}_{i}-\boldsymbol{r}_{j}|}$$
- The _independent electron approximation_ is a _mean field approximation_
- It assumes that each electron moves in the _average effective potential_ created by both nuclei and other electrons
- Each electron is in a _single particle Hamiltonian_:
$$H_\text{I-el}=\frac{p^{2}}{2m}+V(\boldsymbol{r})$$

- From fixing the nuclei, one also gets that the _effective potential has the periodicity of the lattice_:
$$V(\boldsymbol{r}+\boldsymbol{R}_{i})=V(\boldsymbol{r})$$

## Bloch's Theorem
- Time-independent Schrodinger equation:
$$\left( -\frac{\hbar^{2}}{2m} \nabla^{2}+V(\boldsymbol{r}) \right)\Psi_{n,\boldsymbol{k}}(\boldsymbol{r})=E_{n}(\boldsymbol{k})\Psi_{n,\boldsymbol{k}}(\boldsymbol{r})$$
- $n,\boldsymbol{k}$ are _labels_ for the eigenstates

- _Bloch's Theorem_ dictates that the wave function reflects _translational symmetry_:
$$\Psi_{\boldsymbol{k}}(\boldsymbol{r}+\boldsymbol{R}_{i})=\exp(i\boldsymbol{k}\cdot \boldsymbol{R}_{i})\Psi(\boldsymbol{r})$$
- The wave-function can then be cast into the form:
$$\Psi_{\boldsymbol{k}}(\boldsymbol{r})=\exp(i\boldsymbol{k}\cdot \boldsymbol{r})u(\boldsymbol{r})$$
- $u(\boldsymbol{r})$ is the _Bloch function_, and must have the _same periodicity as the lattice_:
$$u_{\boldsymbol{k}}(\boldsymbol{r}+\boldsymbol{R}_{i})=u_{\boldsymbol{k}}(\boldsymbol{r}) \implies u_{\boldsymbol{k}}(\boldsymbol{r})=\sum_{\boldsymbol{G}}c_{\boldsymbol{k}}(\boldsymbol{G})\exp(i\boldsymbol{G}\cdot \boldsymbol{r})$$
- Similarly, the _potential_ also has a Fourier expansion:
$$V(\boldsymbol{r})=\sum_{\boldsymbol{G}}V_{\boldsymbol{G}}\exp(i\boldsymbol{G}\cdot \boldsymbol{r})$$

### Crystal momentum and band index
- The Hamiltonian _does not commute_ with $\boldsymbol{p}$, as translational symmetry is _only for lattice vectors_ instead of arbitrary displacements as $[\boldsymbol{p},H]$ requires
$$-i\hbar \nabla \Psi_{n\boldsymbol{k}}(\boldsymbol{r})=\hbar \boldsymbol{k}\Psi_{n\boldsymbol{k}}(\boldsymbol{r})-i\hbar \exp(i\boldsymbol{k}\cdot \boldsymbol{r})\nabla u_{n\boldsymbol{k}}(\boldsymbol{r})$$

- $\hbar \boldsymbol{k}$ is the _crystal momentum_, not physical momentum
	- Conserved within a _recriprocal lattice vector_
	- Useful for [[Solids#Semiclassical electron dynamics|semiclassical electron dynamics]]

- $n$ is the _band index_, as $\boldsymbol{k}$ may label multiple eigenstates

## Band structures
- From Bloch's Theorem, Schrodinger's equation becomes:
$$\left[ \frac{1}{2m}(\boldsymbol{p}+\hbar \boldsymbol{k})^{2}+V(\boldsymbol{r}) \right]u_{n\boldsymbol{k}}(\boldsymbol{r})=E_{n\boldsymbol{k}}u_{n\boldsymbol{k}}(\boldsymbol{r})$$
- The _periodic boundary conditions_ for $u_{n\boldsymbol{k}}$ produce _discrete eigenvalues_ known as _bands_
	- Analagous to _particle in a box_

- $\boldsymbol{k}$ is always _confine_ to the first BZ:
$$\psi_{n\boldsymbol{k}}(\boldsymbol{r}+\boldsymbol{R})=\psi_{n\boldsymbol{k}}(\boldsymbol{r}) \qquad E_{n,\boldsymbol{k}+\boldsymbol{G}}=E_{n\boldsymbol{k}}$$
- Band structure of Germanium:
![[Ge bands.png|500]]
- At $T=0$, electrons are filled up to the _Fermi level_
- For $N$ unit cells, each _band_ accommodates $2N$ electrons due to spin degeneracy

- If the Fermi level is in a _gap_ with no energy levels near it, the material is a _semiconductor_ or _insulator_
	- If the band _gap_ is within $k_{B}T$, it is a _semiconductor_
- If the Fermi level is in a _band_, the material is a _metal_

- Types of electronic states:
![[Electronics types.png]]

- For a _metal_, the _Fermi surface_ in $\boldsymbol{k}-$space is defined as all $\boldsymbol{k}_{F}$ such that:
$$E_{n}(\boldsymbol{k}_F)=E_{F}$$
- Parts of the Fermi surface belonging to _different bands_ are known as _branches_
## Breakdown of approximation
- Experimental evidence
	- _Hund's rule_ results from repulsive interaction between electrons
	- _Magnetism_ results from coupling of electrons and parallel spins
	- _Plasmons_ are collective _longitudinal electron density fluctuations_
	- _Friedel oscillations_ from screening of charges
	- _Heavy fermions_ in Fermi liquids
	- _One dimensional_ systems with interacting fermions form _Luttinger liquids_, with both _spin and charge density waves_

## Many-fermion states
- The many-electron Schrodinger equation, taking _spin_ into account:
$$H_\text{el}\Psi(\boldsymbol{r}_{1},\sigma_{1},\dots \boldsymbol{r}_{N}\sigma_{N})=E\Psi(\boldsymbol{r}_{1},\sigma_{1},\dots \boldsymbol{r}_{N}\sigma_{N})$$
- $N$ coupled 2nd order PDEs with $3N$ variables

- Pauli Principle for Fermions:
$$\Psi(\boldsymbol{r}_{1},\sigma_{1},\dots \boldsymbol{r}_{i},\sigma_{i},\dots \boldsymbol{r}_{j},\sigma_{j}\dots \boldsymbol{r}_{N}\sigma_{N})=-\Psi(\boldsymbol{r}_{1},\sigma_{1},\dots \boldsymbol{r}_{j},\sigma_{j},\dots \boldsymbol{r}_{i},\sigma_{i}\dots \boldsymbol{r}_{N}\sigma_{N})$$

- The resulting wave-fuction is _not separable_
	- A separable wave-function would not obey the Pauli Principle

### Example: Origin of Hund's Rule
- Let there be a _two-electron_, _two-site_ system
![[Two-site system.png|400]]
$$H=\sum_{i=1}^{2}\left(  \frac{p_{i}^{2}}{2m}+V_{L}(\boldsymbol{r}_{i})+V_{R}(\boldsymbol{r}_{i}) \right)+\frac{e^{2}}{4\pi\epsilon_{0}} \frac{1}{|\boldsymbol{r}_{1}-\boldsymbol{r}_{2}|}$$
- Spin can be _decoupled_ from other degrees of freedom
- Position and spin basis states:
$$\ket{\phi_{L}}, \ket{\phi_{R}} \qquad \ket{\uparrow} ,\ket{ \downarrow}    $$
- There are _four_ possible _spin-orbital states_

- Assume the orbitals are _orthogonal_ $(\braket{ \phi_{L} |\phi_{R}  }=0)$

- Then, construct [[Angular momentum in quantum mechanics#Addition of angular momenta|singlet and triplet]] spin states, pairing them with _symmetric/anti-symmetric_ combinations of $\ket{\phi_{L}}$ and $\ket{\phi _{R}}$

- The singlet and triplet energies are then a combination of _orbital energies_, the _Hartree energy_ $U_{H}$, and the _exchange energy_ $U_{E}$
$$\displaylines{E_{S}=\varepsilon_{L}+\varepsilon_{R}+U_{H}+U_{E} \\ E_{T}=\varepsilon_{L}+\varepsilon_{R}+U_{H}-U_{E} \\ U_{H}=\iint  d^{3}r_{1}\,d^{3}r_{2} |\phi_{L}(\boldsymbol{r}_{1})|^{2}V(\boldsymbol{r}_{1}-\boldsymbol{r}_{2})|\phi_{R}(\boldsymbol{r}_{2})|^{2} \\ U_{E}=\iint  d^{3}r_{1} \,d^{3}r_{2}\, \phi_{L}^{*}(\boldsymbol{r}_{1})\phi_{R}^{*}(\boldsymbol{r}_{2})V(\boldsymbol{r}_{1}-\boldsymbol{r}_{2})\phi_{R}(\boldsymbol{r}_{1})\phi_{L}(\boldsymbol{r}_{2}) }$$
- $U_{E}>0$, hence the _triplet state has lower energy_
- It has _lower Coulomb energy_, as _on average_, the electrons are further away:
$$\Psi_{T}(\boldsymbol{r}_{1}=\boldsymbol{r}_{2})=0$$
- A _spin-independent Hamiltonian_ can produce a _spin-dependent energy_

### General case
- An $N-$electron state can be written as a _linear combination of Slater determinants_

- Describe _position and spin_ degrees of freedom with $\boldsymbol{x}_{i}=(\boldsymbol{r}_{i},\sigma_{i})$
- Example: $m$ electrons in $n$ _spin-orbitals_, where $m<n$
	- Each _site_ for the electron has _two spin-orbitals_ 
$$\Psi(\boldsymbol{r}_{1},\sigma_{1},\dots \boldsymbol{r}_{m},\sigma_{m})=\sum_{P}a_{P}\Phi_{P}(\boldsymbol{r}_{1},\sigma_{1},\dots \boldsymbol{r}_{m},\sigma_{m})$$
- Here, $P$ are _all possible combinations_ of $m$ particles in the $n$ sites
- $\Phi_{P}$ is the Slater determinant, where $P_{i}$ indexes sites from $1$ to $n$
$$\displaylines{\Psi_{i}(\boldsymbol{x}_{i})=\varphi_{i}(\boldsymbol{r}_{i})\chi(\delta_{i})  \\\Phi_{P}=\frac{1}{\sqrt{ m! }} \begin{vmatrix}
\Psi_{P(1)}(\boldsymbol{x}_{1}) & \Psi_{P(2)}(\boldsymbol{x}_{1})&\dots& \Psi_{P(m)}(\boldsymbol{x}_{1}) \\
\Psi_{P(1)}(\boldsymbol{x}_{2}) &\dots&\dots& \Psi_{P(m)}(\boldsymbol{x}_{2})  \\
\vdots & \ddots & \ddots&\vdots \\ 
\Psi_{P(1)}(\boldsymbol{x}_{m}) &\dots&\dots&\Psi_{P(m)}(\boldsymbol{x}_{m})
\end{vmatrix}}$$
- The final wave-function will have $\pmatrix{n\\m}$ Slater determinants

- Typically, states with _parallel spins_ are _kept apart_ and have _lower energy_ (Hund's rule)

# Hartree-Fock Theory
- In the _Hartree-Fock_ approximation, instead of the above, _assume_ the ground state is a single _Slater determinant_:
$$\begin{align}
\Psi_{0}(\boldsymbol{x}_{1}\dots \boldsymbol{x}_{N})&=A\{\Psi_{1}(\boldsymbol{x}_{1})\Psi_{2}(\boldsymbol{x}_{2})\dots \Psi_{N}(\boldsymbol{x}_{N})\} \\ &= \frac{1}{\sqrt{ N! }} \sum_{i=1}^{N!} P_{i}\{\Psi_{1}(\boldsymbol{x}_{P(1)})\Psi_{2}(\boldsymbol{x}_{P(2)})\dots \Psi_{N}(\boldsymbol{x}_{P(N)})\}
\end{align}$$

- Then, use _variational calculus_ to find the _best fit spin-orbital wave functions_, by _minimising_ the estimated ground state energy:
$$E_{0}=\braket{ \Psi_{0} |H|\Psi_{0}  } $$

## The ground state energy
- The Hamiltonian can be written as:
$$H=\sum_{i=1}^{N}h_{i}+\sum_{i<j} g(|\boldsymbol{r}_{i}-\boldsymbol{r}_{j}|)$$
- $h_{i}$ is the _single-particle operator_:
$$h_{i}=\frac{p_{i}^{2}}{2m}+U_\text{e-ion}(\boldsymbol{r}_{i})$$
- $g$ is the _two-particle operator_:
$$g(|\boldsymbol{r}_{i}-\boldsymbol{r}_{j}|)=\frac{e^{2}}{4\pi\epsilon_{0}} \frac{1}{|\boldsymbol{r}_{i}-\boldsymbol{r}_{j}|}$$
### Single particle energy
- Consider:
$$\Braket{ \Psi_{0}|\sum_{i=1}^{N} h_{i}(\boldsymbol{x}_{i})| \Psi_{0} } $$
- The integral is _only non-zero_ when the _permutations match_, therefore one gets:
$$\Braket{ \Psi_{0}|\sum_{i=1}^{N} h_{i}(\boldsymbol{x}_{i})| \Psi_{0} } =\sum_{n=1}^{\infty} \int  d^{3}\boldsymbol{x} \,\Psi_{n}^{*}(\boldsymbol{x})h(\boldsymbol{x})\Psi_{n}(\boldsymbol{x}):= \sum_{n=1}^{N} [\Psi_{n}^{\dagger}\Psi_{n}|h]$$

### Interaction energy
- The _two-particle_ energy:
$$\frac{1}{2}\sum_{i\neq j=1}^{N} \braket{ \Psi_{0}|g(|\boldsymbol{r}_{i}-\boldsymbol{r}_{j}|) |\Psi_{0}  } $$
- Writing out:
$$\frac{1}{2}\sum_{i\neq j}\sum_{m,l} \frac{1}{N!}\int  d\boldsymbol{x}_{1}\dots d\boldsymbol{x}_{N}  (-1)^{P_{m}+P_{l}}P_{l}\{\Psi_{1}(\boldsymbol{x}_{P(1)})\dots \} g(|\boldsymbol{x}_{i}-\boldsymbol{x}_{j} |) P_{m}\{\Psi_{1}(\boldsymbol{x}_{P(1)})\dots\}$$
- Two integrals are non-zero:
$$P_{m}=P_{l}\quad \text{or} \quad P_{m}=P_{l}P_{i \leftrightarrow  j}$$
- They give the _Hartree energy_ and the _exchange energy_ respectively:
$$\displaylines{U_{H}=\frac{1}{2} \sum_{n\neq m}^{N}[\Psi_{n}^{\dagger}\Psi_{n}|g|\Psi_{m}^{\dagger}\Psi_{m}]=\frac{1}{2} \sum_{n\neq m}\int  d\boldsymbol{x} \,d\boldsymbol{y}\, \Psi_{n}^{*}(\boldsymbol{x})\Psi_{n}(\boldsymbol{x})g(|\boldsymbol{x}-\boldsymbol{y}|) \Psi_{m}^{*}(\boldsymbol{y})\Psi_{m}(\boldsymbol{y}) \\ U_{E}=-\frac{1}{2} \sum_{n\neq m}^{N}[\Psi_{n}^{\dagger}\Psi_{m}|g|\Psi_{m}^{\dagger}\Psi_{n}]=-\frac{1}{2} \sum_{n\neq m}\int  d\boldsymbol{x} \,d\boldsymbol{y}\, \Psi_{n}^{*}(\boldsymbol{x})\Psi_{n}(\boldsymbol{x})g(|\boldsymbol{x}-\boldsymbol{y}|) \Psi_{m}^{*}(\boldsymbol{y})\Psi_{m}(\boldsymbol{y}) }$$

- The total energy:
$$E_{0}=\sum_{n} [\Psi_{n}^{\dagger}\Psi_{n}|h]+ \frac{1}{2}\sum_{n,m}\{[\Psi_{n}^{\dagger}\Psi_{n}|g|\Psi_{m}^{\dagger}\Psi_{m}]-[\Psi_{n}^{\dagger}\Psi_{m}|g|\Psi_{m}^{\dagger}\Psi_{n}]\}$$
- For the $n=m$ case, the Hartree and exchange terms _cancel_
- The Coulomb term is _always positive_

- By separating $\Psi_{n}$ into orbital and spin parts, one gets that the _Hartree term is spin-independent_
	- The $n=m$ case is known as the _Hubbard_ $U$\
	- Analagous to the _classical Coulomb repulsion_
$$[\Psi_{n}^{\dagger}\Psi_{n}|g|\Psi_{m}^{\dagger}\Psi_{m}]= \iint  d^{3}\boldsymbol{r}\,d^{3}\boldsymbol{r}' \frac{\rho_{n}(\boldsymbol{r})\rho_{m}(\boldsymbol{r}')}{4\pi\epsilon_{0} |\boldsymbol{r}-\boldsymbol{r}'|} $$

- Exchange energy: _spin-dependent_
	- Opposite spin: zero
	- Identical spin: positive

- Typically, $E_{H}$ is an order of magnitude larger than $E_{E}$
- The _exchange effect_ means that the Coulomb energy is _below classical_ as electrons of _equal spin_ are _kept apart_
## The Hartree-Fock Equation
$$E_{0}=\sum_{n} [\Psi_{n}^{\dagger}\Psi_{n}|h]+ \frac{1}{2}\sum_{n,m}\{[\Psi_{n}^{\dagger}\Psi_{n}|g|\Psi_{m}^{\dagger}\Psi_{m}]-[\Psi_{n}^{\dagger}\Psi_{m}|g|\Psi_{m}^{\dagger}\Psi_{n}]\}$$
- _Minimise_ $E_{0}$ with the _constraint_ that the basis functions are _orthonormal_:
$$\int  d\boldsymbol{x}\,\Psi_{n}^{*}(\boldsymbol{x})\Psi_{m}(\boldsymbol{x})=[\Psi_{n}^{\dagger}\Psi_{m}]=\delta_{nm} $$

- This gives $N^{2}$ _Lagrange multipliers_ $\varepsilon_{n,m}$
$$L[\{\Psi_{n}\}]=E_{0}[\{\Psi_{n}\}]-\sum_{n,m} \varepsilon_{n,m}\big([\Psi_{n}^{\dagger}\Psi_{m}]-\delta_{nm}\big)$$
- _Without loss of generality_, assume states are already orthonormal:
$$L[\{\Psi_{n}\}]=E_{0}[\{\Psi_{n}\}]-\sum_{n=1}^{N}\varepsilon_{n}([\Psi_{n}^{\dagger}\Psi_{n}]-1)$$
- Varying the functions, one gets:
$$\begin{align}
\delta L[\{\Psi_{i}\}]&=\Bigg(\sum_{n=1}^{N} [\delta \Psi_{n}^{\dagger}\Psi_{n}|h]+\sum_{n,m=1}^{N} ([\delta \Psi_{n}^{\dagger}\Psi_{n}|g|\Psi_{m}^{\dagger}\Psi_{m}]-[\delta \Psi_{n}^{\dagger}\Psi_{m}|g|\Psi_{m}^{\dagger}\Psi_{n}]) \\ 
&-\sum_{n=1}^{N}\varepsilon_{n}[\delta \Psi_{n}^{\dagger}\Psi_{n}]\Bigg)+\Bigg(\text{h.c.} \Bigg)
\end{align}$$

- Introduce _local Hartree operator_ $J_{m}$ and the _non-local exchange operator_ $K_{m}$:
$$\displaylines{J_{m}(\boldsymbol{x})f(\boldsymbol{x})=\left(\int  d\boldsymbol{y}\,\Psi_{m}^{\dagger}(\boldsymbol{y})g(\boldsymbol{x}-\boldsymbol{y})\Psi_{m}(\boldsymbol{y}) \right)f(\boldsymbol{x}) \\ K_{m}(\boldsymbol{x})f(\boldsymbol{x})=\left(\int  d\boldsymbol{y}\,\Psi_{m}^{\dagger}(\boldsymbol{y})g(\boldsymbol{x}-\boldsymbol{y})f(\boldsymbol{y}) \right)\Psi_{m}(\boldsymbol{x}) \\ \begin{align}
\delta L[\{\Psi_{i}\}]&=\sum_{n=1}^{N}\int  d\boldsymbol{x}\,\delta \Psi_{n}^{\dagger} \Bigg(  h(\boldsymbol{x})\Psi_{n}(\boldsymbol{x}) +\sum_{m=1}^{N} \big(J_{m}(\boldsymbol{x})-K_{m}(\boldsymbol{x})\big)\Psi_{n}(\boldsymbol{x})-\varepsilon_{n}\Psi_{n}(\boldsymbol{x})\Bigg) \\ &+\sum_{n=1}^{N}\int  d\boldsymbol{x} \,\delta \Psi_{n} (\text{h.c.})
\end{align} }$$
- This is satisfied if the $\Psi_{i}$ and the _Lagrange_ multipliers satisfy:
$$\left( h(\boldsymbol{x})+\sum_{m=1}^{N} \Big(J_{m}(\boldsymbol{x})-K_{m}(\boldsymbol{x})\Big) \right)\Psi_{n}(\boldsymbol{x})=\varepsilon_{n}\Psi_{n}(\boldsymbol{x})$$
- This is the _Hartree-Fock equation_

- Interpretation: _eigenvalue equation_ for the operator:
$$\displaylines{\begin{align}
H&=h(\boldsymbol{x})+\sum_{m=1}^{N}J_{m}(\boldsymbol{x}) - \sum_{m=1}^{N}K_{m}(\boldsymbol{x}) \\ &=-\frac{\hbar^{2}}{2m} \nabla_{r}^{2}+U_\text{eff}(\boldsymbol{x})
\end{align} \\ U_\text{eff}(\boldsymbol{x})=U_\text{ion}(\boldsymbol{r})+U_{H}(\boldsymbol{x})-U_{E}(\boldsymbol{x}) \\ U_{H}(\boldsymbol{x})=\sum_{m=1}^{N}J_{m}(\boldsymbol{x}) \qquad U_{E}(\boldsymbol{x})=\sum_{m=1}^{N} K_{m}(\boldsymbol{x})}$$
- The _operators_ are also _functions of the eigenfunctions_

- $U_{H}$: _Hartree_ energy due to interactions
- $U_{E}$: _Exchange_ energy
	- A _non-local operator_ (replacing $\Psi_{n}(\boldsymbol{x})$ with $\Psi_{n}(\boldsymbol{y})$)
## Solving the Hartree-Fock Equation
- The _self-consistent iterative technique_:
1. Find _initial guesses_ for $\Psi_{n}^{(0)}(\boldsymbol{x})$ by solving $h(x)\Psi_{n}^{(0)}(x)=\varepsilon_{n}\Psi_{n}^{(0)}(x)$
2. Use it to find the _matrix elements_ for $U_{H}$ and $U_{E}$, using some given _basis_
3. _Diagonalise_ the matrix to find the _new_ eigenfunctions $\Psi_{n}^{(1)}(x)$
4. Repeat until _self-consistent_
![[Hartree Fock algorithm.png|500]]
- The iteration can be made more _stable_ with some _parameter_ $\alpha <1$ such that:
$$\Psi_{n}^{(N)}(x)=(1-\alpha)\Psi_{n}^{(N-1)}(x)+\alpha \Psi_{n}^{\text{calculated}}(x)$$


- The _difference_ between the H-F estimate and he _exact ground state energy_ is the _correlation energy_

- The Lagrange multipliers $\varepsilon_{i}$ are known as the _addition energies_ of the system
- Let $\ket{\Psi^{N}}$ and $\ket{\Psi^{N-1}_{i}}$ be the original state, and the state after having _removed_ electron $i$ (while keeping other wave-functions the same)
- _Koopman's Theorem_ states that the _addition energies_ $\varepsilon_{i}$ can be _interpreted_ as _electron excitation energies_ to the _lowest order_ in the _Coulomb interaction_:
$$\varepsilon_{i}=\braket{ \Psi^{N}|H | \Psi_{0}^{N} }-\braket{ \Psi^{N-1}_{i}|H |\Psi^{N-1}_{i}  }  $$

## Hartree-Fock in jellium
- Jellium: _interacting_ electrons on a _positively-charged background_ (neutral metal)
- There is an _exact_ solution in the Hartree-Fock approximation

- When one _ignores interactions_, one gets the _homogeneous electron gas_, or the [[Solids#Sommerfeld model|Sommerfeld model]]

### Properties of Sommerfeld metal
- The wave functions, taking _spin_ into account:
$$\Psi_{\boldsymbol{k},\lambda}(\boldsymbol{r},\sigma)=\frac{1}{\sqrt{ V }}\exp(i\boldsymbol{k}\cdot \boldsymbol{r})\chi_{\lambda}(\sigma) \qquad \varepsilon_{\lambda}(\boldsymbol{k})=\frac{\hbar^{2}k^{2}}{2m}$$
- At $T=0$, with a _filled Fermi sphere_:
$$\displaylines{n=\frac{N}{V}=\frac{k_{F}^{3}}{2\pi^{2}} \\ E_{F}=\frac{\hbar^{2}k_{F}^{2}}{2m}\qquad v_{F}=\frac{\hbar k_{F}}{m} \\ g_{V}(E)=\frac{1}{V}\sum_{\boldsymbol{k}}\delta\left( E-\frac{\hbar^{2}k^{2}}{2m} \right)=\frac{3}{2} \frac{n}{E_{F}} \sqrt{ \frac{E}{E_{F}} } \\ E_\text{tot}=\frac{3}{5}NE_{F}}$$
- For $T>0$, electron distribution follows the _Fermi distribution_:
$$f(E)=\frac{1}{\exp(\beta (E-\mu)]+1}$$

### Jellium addition energies
- Attempt the _plane wave solution_:
$$\Psi_{\boldsymbol{k},\lambda}(\boldsymbol{r},\sigma)=\frac{1}{\sqrt{ V }}\exp(i\boldsymbol{k}\cdot \boldsymbol{r})\chi_{\lambda}(\sigma) $$

- Model the ions as being _spread over the whole volume_ with charge density $N/V$
- Results of different terms:
$$\begin{align}
-\frac{\hbar^{2}}{2m}\nabla_{r}^{2}\Psi_{\boldsymbol{k}}&=\frac{\hbar^{2}k^{2}}{2m}\Psi_{\boldsymbol{k}} \\
U_{H}\Psi_{\boldsymbol{k}}&=\frac{N}{V} \left(\int  d^3\boldsymbol{r}' \frac{e^{2}}{4\pi\epsilon_{0}r'} \right)\Psi_{\boldsymbol{k}} \\
U_\text{ion}\Psi_{\boldsymbol{k}}&=-\frac{N}{V} \left(\int  d^3\boldsymbol{r}' \frac{e^{2}}{4\pi\epsilon_{0}r'} \right)\Psi_{\boldsymbol{k}} \\
-U_{E}\Psi_{\boldsymbol{k}}&=-\frac{e^{2}}{\epsilon_{0}} \left( \int_{|k|<k_{F}}  \frac{d^{3}\boldsymbol{k}'}{(2\pi)^{3}}  \frac{1}{|\boldsymbol{k}-\boldsymbol{k}'|^{2}}\right) \Psi_{\boldsymbol{k}}
\end{align}$$
- The _Hartree_ and _ion_ energies _cancel_

- The exchange energy can be evaluated _analytically_
	- Set $\boldsymbol{k}$ as along the $z$ axis then integrate with polar coordinates
	- $F$ is the _Lindhard function_
$$\displaylines{\varepsilon_{\boldsymbol{k},\lambda}=\frac{\hbar^{2}k^{2}}{2m}-\frac{e^{2}k_{F}}{2\pi^{2}\epsilon_{0}} F\left( \frac{k}{k_{F}} \right) \\ F(x)=\frac{1}{2}+ \frac{1-x^{2}}{4x}\ln \left| \frac{1+x}{1-x}\right|}$$
![[Lindhard function.png|400]]

- Jellium still has _plane wave eigenstates_
- Comparing to _free electrons_, the _exchange energy_ between _parallel spins_ will _lower_ the electron energy:
![[Jellium Hartree Fock.png|400]]

### Jellium ground state energy
- Then contrast the addition energies with the _ground state energy_ $E_{0}$
$$\begin{align}
E_{0}^{\text{HF}}=&\sum_{n} \left[ \Psi_{n}^{\dagger}\Psi_{n}\Bigg|-\frac{\hbar^{2}}{2m}\nabla^{2}+U_\text{e-ion} \right]+U_\text{ion-ion} \\
&+ \frac{1}{2}\sum_{n,m}\{[\Psi_{n}^{\dagger}\Psi_{n}|g|\Psi_{m}^{\dagger}\Psi_{m}]-[\Psi_{n}^{\dagger}\Psi_{m}|g|\Psi_{m}^{\dagger}\Psi_{n}]\}
\end{align}$$
- In the case of jellium, $E_\text{e-e}+E_\text{e-ion}+E_\text{ion-ion}=0$, leaving behind _kinetic_ and _exchange_ energy

- Evaluating the sum gives:
$$E_{0}^\text{HF}=\left( \frac{2.21}{r_{s}^{2}}-\frac{0.916}{r_{s}} \right)\text{ Ry}$$
- $r_{s}$ is the _Wigner-Seitz radius_, which on average contains _one electron_, measured in the _Bohr radius_:
$$\frac{1}{\rho}=\frac{V}{N}=\frac{4\pi}{3}(r_{s}a_{B})^{3}$$
- One can compare the _Coulomb_ and _kinetic energy_:
$$U\sim\frac{e^{2}}{4\pi\epsilon_{0}(a_{B}r_{s})} \quad K=\frac{\hbar^{2}k_{F}^{2}}{2m}\implies \frac{U}{K}\sim 0.9r_{s}$$
- In _real materials_, typical value is $r_{s}\sim 2-6$

![[Jellium ground state energy.png|500]]
- For _low_ $r_{s}$, _kinetic energy dominates_
- For _high_ $r_{s}$ (low density), _exchange energy_ dominates

- A more precise _expansion_ of ground state energy:
$$E_{0}=\left( \frac{2.21}{r_{s}^{2}}-\frac{0.916}{r_{s}}+\underbrace{ 0.0622\ln r_{s}-0.096+\mathcal{O}(r_{s}\ln r_{s})O }_\text{Correlation energy} \right)\text{ Ry}$$



# Density Functional Theory
- Based around the _electron density_, the _probability density_ of finding the $N$ electrons
$$\begin{align}
n(\boldsymbol{r}) &=\Braket{ \Psi_{0} |\left[ \sum_{i=1}^{N}\delta(\boldsymbol{r}-\boldsymbol{r}_{i}) \right] | \Psi_{0} }  \\
&=\int  d^3 \boldsymbol{x}\dots d^{3}\boldsymbol{x}_{N} \,\Psi_{0}^{\dagger}(\boldsymbol{x}_{1}\dots \boldsymbol{x}_{N})\left[ \sum_{i=1}^{N}\delta(\boldsymbol{r}-\boldsymbol{r}_{i}) \right]\Psi_{0}(\boldsymbol{x}_{1}\dots \boldsymbol{x}_{N})
\end{align}$$
- Requirements of $n(\boldsymbol{r})$:
$$n(\boldsymbol{r})\geq 0 \,\,\forall \boldsymbol{r} \qquad \lim_{ |\boldsymbol{r}| \to \infty }n(\boldsymbol{r})=0 \qquad \int  d^3 \boldsymbol{r}\,n(\boldsymbol{r})=N $$

## Functionals of the electron density
- The _Thomas-Fermi_ model for kinetic energy is a _functional of the density_
- Write the _Fermi wave-vector_ as:
$$n=2 \frac{4\pi k^{3}/3}{(2\pi)^{3}} \implies k=(3\pi^{2}n)^{1/3}$$
- One can then approximate kinetic energy as:
$$T_\text{T-F}[n(\boldsymbol{r})]= \frac{1}{V}\int  d^3\boldsymbol{r}  \left[ \sum_{\substack{|\boldsymbol{k}|<k_{F} \\\lambda=\uparrow,\downarrow}} \frac{\hbar^{2}k^{2}}{2m^{*}} \right]=\frac{\hbar^{2}}{m} \frac{3}{10} (3\pi^{2})^{2/3}\int  d^3\boldsymbol{r} \,n^{5/3}(\boldsymbol{r}) $$
- The _ground state energy_ can hen be approximated as the functional:
$$E_{0}[n(\boldsymbol{r})]=T_\text{T-F}[n(\boldsymbol{r})]-\int  d^3\boldsymbol{r}\, \sum_{i} \frac{Ze^{2}n(\boldsymbol{r})}{4\pi\epsilon_{0}|\boldsymbol{r}-\boldsymbol{R}_{i}|}+\frac{1}{2}\iint  d^{3}\boldsymbol{r}\,d^{3}\boldsymbol{r}' \frac{e^{2}n(\boldsymbol{r})n(\boldsymbol{r}')}{4\pi\epsilon_{0}|\boldsymbol{r}-\boldsymbol{r}'|}  $$

- Then, _minimise_ $E_{0}[n(\boldsymbol{r})]$ with the _constraints_:
$$n(\boldsymbol{r})>0\,\,\forall \boldsymbol{r} \qquad \lim_{ |\boldsymbol{r}| \to \infty }n(\boldsymbol{r})=0 \qquad \int  d^3\boldsymbol{r}\,n(\boldsymbol{r})=N  $$
## The Hohenberg-Kohn Theorems
- Assume a _non-degenerate ground state_
	- If degenerate, _break_ the symmetry

>[!info] First Hohenberg-Kohn Theorem
>For a system of $N$ interacting electrons, the external potential $V_\text{Ne}(\boldsymbol{r})$ is a _unique functional_ of the ground state electron density $n(\boldsymbol{r})$, apart from an arbitrary additive constant
- Proof: by _contradiction_, assuming two different Hamiltonians $H,H'$ with different trial functions $\Psi_{0},\Psi_{0}'$, then use $\Psi_{0}(\Psi_{0}')$ as a trial wave-function for $H'(H)$


- As $V_\text{Ne}$ determines the _Hamiltonian_, $n(\boldsymbol{r})$ then _determines all physical properties_ of the system

### The Hohenberg-Kohn density functional
- The _total energy functional_, along with _external potential_ $V_\text{Ne}$:
$$\begin{align}
E_{0}[n(\boldsymbol{r})]&=T[n]+E_\text{Ne}[n]+E_\text{ee}[n]  \\
&=\int  d^3\boldsymbol{r}\,n(\boldsymbol{r})V_\text{Ne}(\boldsymbol{r})+F_\text{H-K}[n] 
\end{align}$$
- Here, $F_\text{H-K}[n]$ is the _Hohenberg-Kohn density functional_
	- It is _independent_ of the specifics of the system
$$F_\text{H-K}[n]=T[n]+E_\text{ee}[n]$$

>[!info] Second Hohenberg-Kohn Theorem
>The ground state energy functional $E_{0}[\tilde{n}]$ has the global minimum at the exact ground-state density
- An extension of the _variational principle_

- For _any_ trial density $\tilde{n}(\boldsymbol{r})$ satisfying the necessary _boundary conditions_, the energy obtained from the functional $E_{0}[\tilde{n}]$ represents an _upper bound_ on the _true_ ground state energy $E_{0}$

## Kohn-Sham equations

### Form of the ground state energy
$$F_\text{H-K}[n]=T[n]+E_\text{ee}[n]$$
- The _exact forms_ of the kinetic energy and interaction energies are _unknown_

- For $E_\text{ee}$, the _largest contribution_ is the _classical Coulomb energy_ $J[n]$:
$$E_\text{ee}[n]=\frac{1}{2}\iint  d^{3}\boldsymbol{r}\,d^{3}\boldsymbol{r}' \frac{e^{2}n(\boldsymbol{r})n(\boldsymbol{r}')}{4\pi\epsilon_{0}|\boldsymbol{r}-\boldsymbol{r}'|}+E_\text{NCl}[n]=J[n]+E_\text{NCl}[n]$$
- $E_\text{NCl}$ is the _non-classical contribution_ to the interaction energy
	- Such as _exchange energy_ and _higher order correlations_
	- The _self interaction term_ cancels out with the corresponding term in $J[n]$

- Meanwhile, $T[n]$ can also be separated
- Let $T_{S}[n]$ be the _exact kinetic energy_ of a _non-interacing reference system_ with the _same elecronic density_ $n(\boldsymbol{r})$ as the interacting system
	- The two systems can have the _same density_ as the Hamiltonians differ in _not just_ the external potential

- Let the _reference system_ have eigenstates $\Psi_{i}(\boldsymbol{r},\sigma)=\phi_{i}(\boldsymbol{r})\chi_{i}(\sigma)$, with the wave function being a _single Slater determinant_:
$$\displaylines{n_{S}(\boldsymbol{r})=\sum_{i=1}^{N}|\phi_{i}(\boldsymbol{r})|^{2}=n(\boldsymbol{r}) \\ T_{S}=\sum_{i=1}^{N}\int  d^3\boldsymbol{r}\, \Psi_{i}^{\dagger}(\boldsymbol{r}) \frac{p^{2}}{2m}\Psi_{i}(\boldsymbol{r})}$$

- Write the Hohenberg-Kohn density functional as:
$$\displaylines{F_\text{HK}[n]=T_{S}[n]+J[n]+E_\text{XC}[n] \\ E_\text{XC}[n]=(T[n]-T_{S}[n])+(E_\text{ee}[n]-J[n])}$$
- $E_\text{XC}$ is the _exchange correlation energy_

- From this, using definitions from the [[#The ground state energy|Hartree-Fock approximation]], write $E_{0}$ in terms of the _eigenstates of the reference system_
	- Including the _electron self-interaction_ $i=j$
$$E_{0}[n]=\sum_{i=1}^{N}[\Psi_{i}^{\dagger}\Psi _{i}|h]+\frac{1}{2}\sum_{i,j=1}^{N}[\Psi_{i}^{\dagger}\Psi_{i}|g|\Psi_{j}^{\dagger}\Psi_{j}]+E_\text{XC}[n]$$
### Minimisation
- Use _calculus of variations_ to derive the eigenstates _of the reference system_
- Assuming that $\Psi_{i}$ are orthogonal:
$$L[\{\Psi_{i}\}]=E_{0}[\{\Psi_{i}\}]-\sum_{i=1}^{N}\varepsilon_{i}([\Psi_{i}^{\dagger}\Psi_{i}]-1)$$
- Doing the minimisation:
$$\displaylines{\sum_{i=1}^{N}\int  d\boldsymbol{x}\,\delta \Psi_{i}^{\dagger}\left( h(\boldsymbol{x})\Psi_{i}(\boldsymbol{x})+U_{H}\Psi_{i}(\boldsymbol{x})+\frac{\delta E_\text{XC}}{\delta n(\boldsymbol{r})}\Psi_{i}(\boldsymbol{x})-\varepsilon_{i}\Psi_{i}(\boldsymbol{x}) \right)+\text{h.c.}=0 \\ U_{H}=\sum_{m=1}^{N}\int  d\boldsymbol{y}\,\Psi_{m}^{\dagger}(\boldsymbol{y})g(\boldsymbol{x}-\boldsymbol{y})\Psi_{m}(\boldsymbol{y}) }$$
- Here, a _functional derivative_ is required to minimise $E_\text{XC}$
$$\delta E_\text{XC}=E_\text{XC}[n+\delta n]-E_\text{XC}[n]\equiv \int  d^3\boldsymbol{r} \,\delta n(\boldsymbol{r}) \frac{\delta E_\text{XC}}{\delta n(\boldsymbol{r})}$$
- Then, define the _exchange correlation potential_:
$$V_\text{XC}(\boldsymbol{r})=\frac{\delta E_\text{XC}}{\delta n(\boldsymbol{r})}$$
- One then gets the _Kohn-Sham equation_:
$$\left( -\frac{\hbar^{2}}{2m}\nabla ^{2}+V_\text{Ne}(\boldsymbol{r})+U_{H}(\boldsymbol{r})+V_\text{XC}(\boldsymbol{r}) \right)\Psi_{i}(\boldsymbol{x})=\varepsilon_{i}\Psi_{i}(\boldsymbol{x})$$
- $U_{H}$ and $V_\text{XC}$ are _local_ operators dependent on $n(\boldsymbol{r})$
### Local density approximation
- For regions where $n$ is _slowly varying_, $E_\text{XC}$ can be _approximated_ by the value for a _locally uniform electron gas_ of the same charge density:
$$E_\text{XC}[n]=\int \varepsilon _\text{XC}(n)n(\boldsymbol{r})\,d^{3}\boldsymbol{r} $$
- Or, the _local spin density approximation_:
$$E_\text{XC}[n_{\uparrow},n_{\downarrow}]=\int  \varepsilon _\text{XC}(n_{\uparrow},n_{\downarrow})n(\boldsymbol{r})\,d^{3}\boldsymbol{r} $$
- They are typically used in DFT codes, but tend to _underpredict atomic ground state and ionisation energies_, while _overpredicting binding energies_

- It can be improved by adding _gradient corrections_ $\varepsilon _\text{XC}(n_{\uparrow},n_{\downarrow},\nabla n_{\uparrow},\nabla n_{\downarrow})$

- LDA exchange-correlation potentials can be found using _quantum Monte Carlo_
	- The first term is the [[#Jellium ground state energy|jellium exchange energy]]
$$\displaylines{E_\text{XC}^{\text{LDA}}[n(\boldsymbol{r})]=\int  d^3\boldsymbol{r}\,\varepsilon _\text{XC}(n)n(\boldsymbol{r}) \\ \varepsilon _\text{XC}(\boldsymbol{r}_{s})=\begin{cases}
-\frac{0.9164}{r_{s}}-\frac{0.2846}{1+1.0529\sqrt{ r_{s} }+0.3334r_{s}} &r_{s}>1 \\ -\frac{0.9164}{r_{s}}+0.0622\ln r_{s}-0.096-0.0232r_{s}+0.004r_{s}\ln r_{s}&r_{s}\leq 1
\end{cases} \\ \frac{1}{n}=\frac{4\pi}{3}(r_{s}a_{B})^{3} }$$
### Solving the Kohn-Sham equations
$$\left( -\frac{\hbar^{2}}{2m}\nabla ^{2}+V_\text{Ne}(\boldsymbol{r})+U_{H}(\boldsymbol{r})+V_\text{XC}(\boldsymbol{r}) \right)\Psi_{i}(\boldsymbol{x})=\varepsilon_{i}\Psi_{i}(\boldsymbol{x})$$
- The Kohn-Sham equations can be _solved iteratively_ like the [[#Solving the Hartree-Fock Equation|Hartree-Fock equation]]
- The Hartree potential:
$$U_{H}(\boldsymbol{r})=\sum_{i=1}^{N}\int  d\boldsymbol{x}' \frac{e^{2}|\Psi_{i}(\boldsymbol{x}')|^{2}}{4\pi\epsilon_{0}|\boldsymbol{r}-\boldsymbol{r}'|}=\int  d^3\boldsymbol{r} \frac{e^{2}n(\boldsymbol{r}')}{4\pi\epsilon_{0}|\boldsymbol{r}-\boldsymbol{r}'|}$$
- The _initial guess_ for the Kohn-Sham orbitals are typically from _setting_ $U_{H}$ and $V_\text{XC}$ to $0$
- Then, _solve iteratively_

### Kohn-Sham eigenvalues and orbitals
- The _sum of Kohn-Sham eigenvalues_, from the equations:
$$\sum_{i=1}^{N}\varepsilon_{i}-E_{0}=\frac{1}{2}\frac{e^{2}}{4\pi\epsilon_{0}}\iint  d^{3}\boldsymbol{r}\,d^{3}\boldsymbol{r}'\,\frac{n(\boldsymbol{r})n(\boldsymbol{r}')}{|\boldsymbol{r}-\boldsymbol{r}'|}-E_\text{XC}[n]+\int  d^3\boldsymbol{r}\,V_\text{XC}(\boldsymbol{r})\,n(\boldsymbol{r})  $$
- The eigenvalues _do not have significance as single-particle energies_

- The Kohn-Sham orbitals are mainly useful for _calculating physical properies from density_

## DFT-based molecular dynamics
- Use the _Born-Oppenheimer approximation_
- The motion of _nuclei_ can be treated _classically_ on the _ground-state electronic surface_
$$M_{I}\ddot{\boldsymbol{R}}_{I}=-\nabla_{I}(\underbrace{ E_{0}(\boldsymbol{R}_{1}\dots \boldsymbol{R}_{N}) }_{ \text{DFT} }+\underbrace{ V_\text{N-N}(\boldsymbol{R}_{1}\dots \boldsymbol{R}_{N}) }_{ \text{Coulomb} })$$
- At _each step_, the forces are calculated by _minimising the Kohn-Sham energy_ for the _current nuclear configuration_
# Electronic response theory
- In the _independent electron_ model, the only _elementary excitations_ are _electron-hole pairs_, from _electron transitions_ between levels

- When one takes _many-body interactions_, there can be _other elementary excitations_
	- _Excitons_: bound electron-hole pairs
	- _Plasmons_: longitudinal oscillations in charge density (from Coulomb interactions)

- These elementary excitations often result from _external stimuli_, such as fields
	- Excitons: _photon_ absorption
	- Plasmons: _high-energy electron_ injection

- Stimuli can be analysed using _response theory_
	- Example: _current_ and _polarisation_ from electric fields, or _magnetisation_

- For _weak perturbations_, one can use _linear response theory_

## The dynamic response function
- The _linear response_ of some quantity $\Psi_{i}(\boldsymbol{x},t)$ from a _perturbing force_ $F_{j}(\boldsymbol{x}',t')$, using a _dynamic response function_ $\chi_{ij}(\boldsymbol{x},\boldsymbol{x}',t,t')$ that takes _all locations_ at _earlier times_ into account:
$$\Psi_{i}(\boldsymbol{x},t)=\int  d^3\boldsymbol{x}'\int  dt\,\chi_{ij}(\boldsymbol{x},\boldsymbol{x}',t,t')F_{j}(\boldsymbol{x}',t')  $$
- From _causality_, $\chi_{ij}(t<t')=0$
- If the system is _translationally invariant_, then $\chi$ can only depend on _displacement_
- If the system is in _equilibrium_, it can only depend on $t-t'$
$$\chi_{ij}=\chi_{ij}(|\boldsymbol{x}-\boldsymbol{x}'|,t-t')$$

- Consider _scalar fields_:
$$\Psi(\boldsymbol{x},t)=\int  d^3\boldsymbol{x}'\int  dt\,\chi(|\boldsymbol{x}-\boldsymbol{x}'|,t-t')F(\boldsymbol{x}',t')  $$
- Take the _Fourier transform_:
$$\begin{align}
\chi(\boldsymbol{q},\omega)&=\int  d^3\boldsymbol{x}\int  dt\, \chi(\boldsymbol{x},t)\,\exp[i(\omega t-\boldsymbol{q}\cdot \boldsymbol{x})]   \\
\chi(\boldsymbol{x},t)&=\int  \frac{d^3\boldsymbol{q}}{(2\pi)^{3}}\int  \frac{d\omega}{2\pi}\, \chi(\boldsymbol{q},\omega)\,\exp[-i(\omega t-\boldsymbol{q}\cdot \boldsymbol{x})]
\end{align}$$
- While $\chi(\boldsymbol{x},t)$ is _real_, $\chi(\boldsymbol{q},\omega)$ may be _complex_

- From the _convolution theorem_:
$$\Psi(\boldsymbol{q},\omega)=\chi(\boldsymbol{q},\omega)F(\boldsymbol{q},\omega)$$
## Kramers-Kronig relations
- Let the field be _non-spatially varying_:
$$\displaylines{\Psi(t)=\int  dt'\, \chi(t-t')F(t')\\
\Psi(\omega)=\chi(\omega)F(\omega)
}$$
- Let $\chi$ be split into _real_ and _complex_ parts with $\chi_{1},\chi_{2} \in \mathbb{R}$
$$\chi(\omega)=\chi_{1}(\omega)+i\chi_{2}(\omega)$$
- The [[Analytical classical mechanics#Linear response theory|Kramers-Kronig relations]] give that due to _causality_, the relations between the real and imaginary parts are:
$$\chi_{1}(\omega)=\mathcal{P}\int_{-\infty}^\infty\frac{\chi_{2}(\omega')}{\omega'-\omega}\frac{d\omega'}{\pi}\qquad \chi_{2}(\omega)=-\mathcal{P}\int_{-\infty}^\infty\frac{\chi_{1}(\omega')}{\omega'-\omega}\,\frac{d\omega'}{\pi}$$
- Thus, if one knows the _full spectral dependence_ of one part, one knows that of the other part
	- Example: _refractive index_ found from measuring _absorption coefficients_ over a frequency range

## Longitudinal response function for an electron gas
- The _di-electric response function_ $\varepsilon(\boldsymbol{q},\omega)$ for a _homogeneous electron gas_, in response to a _longitudinal electric field_
	- Effects: _screening_, and the creation of _elementary excitations_ (electronic transitions)

- Find the effect of a _plane wave_ by adding _electric potential_ $U$ to the Hamiltonian for the [[#Independent electrons|independent electron]]:
$$\displaylines{H=\frac{p^{2}}{2m}+V(\boldsymbol{r})+U(\boldsymbol{r},t) \\ U(\boldsymbol{r},t)=A_{0}(\boldsymbol{q},\omega)\exp[i(\boldsymbol{q}\cdot \boldsymbol{r}-\omega t)]+\text{h.c.}}$$
- The resulting electric field is _longitudinal_:
$$\displaylines{\boldsymbol{E}(\boldsymbol{r},t)=-\nabla\left( \frac{U}{-e} \right)=\boldsymbol{E}_{0}\exp[i(\boldsymbol{q}\cdot \boldsymbol{r}-\omega t)]+\text{h.c.}\\ \boldsymbol{E}_{0}=\frac{iA_{0}}{e}\boldsymbol{q}}$$
### Electronic transitions
- The _perturbation_ gives _electronic transitions_, with _transition probabilities_ from [[Time-dependent quantum mechanics#Fermi's Golden Rule|Fermi's Golden Rule]]

- The transitions are between _eigenstates_ $H_{0}$, while absorbing or emitting energy $\hbar\omega$
- For $E_{\alpha}<E_{\beta}$, the _absorption_ and _emission_ probabilities are:
$$\begin{align}
W_{\alpha\to \beta}&=\frac{2\pi}{\hbar}|\braket{ \Psi_{\beta}|A_{0}\exp(i\boldsymbol{q}\cdot \boldsymbol{r}) | \Psi _{\alpha} }|^{2} \,\delta(E_{\beta}-E_{\alpha}-\hbar\omega)f(E_{\alpha})[1-f(E_{\beta})]  \\
W_{\beta\to\alpha}&=\frac{2\pi}{\hbar}|\braket{ \Psi_{\alpha}|A_{0}^{*}\exp(-i\boldsymbol{q}\cdot \boldsymbol{r}) | \Psi _{\beta} }|^{2} \,\delta(E_{\alpha}+\hbar\omega-E_{\beta})f(E_{\beta})[1-f(E_{\alpha})] 
\end{align}$$

- For a volume $V$, the _power_ dissipated $P$, accounting for _spins_, is given by:
$$\begin{align}
P(\boldsymbol{q},\omega)&\equiv\hbar\omega W(\boldsymbol{q},\omega)=\hbar\omega \left[2\sum_{\alpha,\beta}(W_{\alpha\to\beta}-W_{\beta\to\alpha})\right] \\ &=2\hbar\omega \frac{2\pi}{\hbar}\sum_{\alpha,\beta} |\braket{ \Psi_{\beta}|A_{0}\exp(i\boldsymbol{q}\cdot \boldsymbol{r}) | \Psi _{\alpha} }|^{2} \,\delta(E_{\beta}-E_{\alpha}-\hbar\omega)[f(E_{\alpha})-f(E_{\beta})]
\end{align}$$
- This can be considered together with the _classical Joule heating_
### Power dissipation
- Consider the _current density_ arising from the electric field $\boldsymbol{E}$:
$$\displaylines{\boldsymbol{J}(\boldsymbol{q},\omega)=\sigma(\boldsymbol{q},\omega)\boldsymbol{E}(\boldsymbol{q},\omega) \\ \boldsymbol{J}(\boldsymbol{r},t)=\sigma(\boldsymbol{q},\omega)\boldsymbol{E}_{0}\exp[i(\boldsymbol{q}\cdot \boldsymbol{r}-\omega t)]+\text{h.c.}}$$
- The power dissipation from _classical Joule heating_, only keeping non-oscillating terms:
$$P(\boldsymbol{q},\omega)=\int  d^3\boldsymbol{r}\,\boldsymbol{J}\cdot \boldsymbol{E}=2\sigma_{1}(\boldsymbol{q},\omega) \frac{q^{2}}{e^{2}} |A_{0}|^{2}V $$
- Comparing with the _quantum mechanical_ result:
$$\sigma_{1}(\boldsymbol{q},\omega)=\frac{1}{2} \frac{e^{2}}{q^{2}} \frac{\hbar\omega W(\boldsymbol{q},\omega)}{|A_{0}|^{2}V}$$
### Dielectric response and conductivity
- Dielectric response function $\varepsilon$ is defined as:
$$\boldsymbol{D}=\epsilon_{0}\varepsilon \boldsymbol{E}$$
- Combining this with $\boldsymbol{J}=\sigma \boldsymbol{E}$ and using [[Electrodynamics and Optics#Electrodynamics and Maxwell's Equations|Maxwell's equations for matter]], substituting $\boldsymbol{H}=\boldsymbol{H}_{0}\exp(-i\omega t)$ and $\boldsymbol{E}=\boldsymbol{E}_{0}\exp(-i\omega t)$, one gets the _complex effective dielectric response function_
$$\displaylines{\varepsilon=1+\frac{i\sigma}{\epsilon_{0}\omega} \\ \varepsilon_{1}=1-\frac{1}{\epsilon_{0}\omega}\sigma_{2}\qquad \varepsilon_{2}=\frac{1}{\epsilon_{0}\omega }\sigma_{1}}$$

- Also define the _polarisation response function_:
$$\varepsilon=1+\chi \implies \varepsilon_{1}=1+\chi_{1} \,\,,\,\,\varepsilon_{2}=\chi_{2}$$

- The imaginary part of $\varepsilon_{2}$ leads to _energy dissipation_, as from the above, one gets that $P \propto \sigma_{1}\propto\chi_{2}$
$$P=\left[ \frac{2\epsilon_{0}\omega q^{2}}{e^{2}}|A_{0} |^{2}V\right]\chi_{2}(\boldsymbol{q},\omega)$$
### Form of dielectric response function
- From _combining_ the classical result for $P\propto\varepsilon_{2}$ with the quantum mechanical result, one gets the form of $\varepsilon_{2}$
$$\varepsilon_{2}=\frac{2\pi e^{2}}{\epsilon_{0}q^{2}} \frac{1}{V} \sum_{\alpha,\beta}|\braket{ \Psi_{\alpha}|e^{i\boldsymbol{q}\cdot \boldsymbol{r}} |\Psi_{\beta}}|^{2}\delta(E_{\beta}-E_{\alpha}-\hbar\omega)[f(E_{\alpha})-f(E_{\beta})]$$
- Then using the [[#Kramers-Kronig relations]]
$$\varepsilon_{1}=1+\frac{2 e^{2}}{\epsilon_{0}q^{2}} \frac{1}{V} \sum_{\alpha,\beta}|\braket{ \Psi_{\alpha}|e^{i\boldsymbol{q}\cdot \boldsymbol{r}} |\Psi_{\beta}}|^{2}\frac{f(E_{\alpha})-f(E_{\beta})}{E_{\beta}-E_{\alpha}-\hbar\omega}$$
- One can write $\varepsilon$ as:
$$\varepsilon=\lim_{ \eta \to 0^{+} } \left(1+{2 e^{2}}{\epsilon_{0}q^{2}} \frac{1}{V} \sum_{\alpha,\beta}|\braket{ \Psi_{\alpha}|e^{i\boldsymbol{q}\cdot \boldsymbol{r}} |\Psi_{\beta}}|^{2}\frac{f(E_{\alpha})-f(E_{\beta})}{E_{\beta}-E_{\alpha}-\hbar\omega-i\eta}\right)$$


- The _elementary excitations_ of an _independent electron system_ occur when the electron _changes energy levels_, leading to _singularities_ in the _response function_

## Lindhard dielectric function
- Take the case of the _homogeneous electron gas_:
$$\displaylines{\Psi_{\alpha}(\boldsymbol{r})=\frac{1}{\sqrt{ V }}\exp(i\boldsymbol{k}_{\alpha}\cdot \boldsymbol{r})\qquad E_{\alpha}=\frac{\hbar^{2}|\boldsymbol{k}_{\alpha}|^{2}}{2m} \\ \braket{ \Psi_{\alpha}|e^{i\boldsymbol{q}\cdot \boldsymbol{r}} |\Psi_{\beta}  } =\delta_{\boldsymbol{k}_{\beta},\boldsymbol{q}+\boldsymbol{k}_{\alpha}}}$$

- The dielectric function then has the form:
$$\varepsilon(\boldsymbol{q},\omega)=1+2e^{2}\epsilon_{0} q^{2} \frac{1}{V} \sum_{\boldsymbol{k}} \frac{f(E_{\boldsymbol{k}})-f(E_{\boldsymbol{k}+\boldsymbol{q}})}{E(\boldsymbol{k}+\boldsymbol{q})-E(\boldsymbol{k})-\hbar\omega-i\eta}$$
- At _zero temperature_, as the Fermi distribution is a _step function_, the sum can be made into an _integral over phase space_:
$$\displaylines{\varepsilon_{1}(\boldsymbol{q},0)=1+\frac{k_\text{TF}^{2}}{q^{2}}F\left( \frac{q}{2k_{F}} \right) \qquad \varepsilon_{2}(\boldsymbol{q},0)=0 \\
k_\text{TF}^{2}=\frac{me^{2}k_{F}}{\epsilon_{0}\pi^{2}\hbar^{2}} \qquad F(x)=\frac{1}{2}+\frac{1-x^{2}}{4x}\ln\left| \frac{1+x}{1-x}\right|}$$

- For $q\ll k_{F}$, this is the [[Solids#Thomas-Fermi screening|Thomas-Fermi result]]:
	- The Thomas-Fermi screening result assumes the _length scale_ of the perturbation is _much larger_ than $k_{F}$ (allows the assumption of a spatially varying $E_{F}$)
$$\varepsilon_{1}(q\ll k_{F},0)=1+\frac{k_\text{TF}^{2}}{q^{2}}$$
![[Thomas Fermi screening.png|400]]
- For $q\gg k_{F}$:
$$\varepsilon_{1}(q\gg k_{F},0)=1+\frac{4k_\text{TF}^{2}k_{F}^{2}}{q^{2}}$$
- For $q\approx 2k_{F}$:
$$\varepsilon_{1}(q\approx 2k_{F},0)=\varepsilon_{1}(2k_{F},0)+ \frac{k_\text{TF}^{2}}{16k_{F}^{3}} (q-2k_{F}) \ln\left|\frac{q-2k_{F}}{4k_{F}}\right|$$
- At $q=2k_{F}$, the second term has a _logarithmic singularity_
	- Responsible for _Friedel oscillations_
	- For $q<2k_{F}$, one can have an energy transition with $\omega=0$ (across the Fermi sphere)
	- For $q>2k_{F}$, such a transition is _no longer possible_

### Static dielectric screening
- Let there be a _static ppoint charge_ $+Ze$ in a medium
- The charge is then _screened_ by the electrons

- In a _free electron gas_:
$$U_\text{ext}(\boldsymbol{r})=-\frac{Ze^{2}}{4\pi\epsilon_{0}r}=-\frac{1}{(2\pi)^{3}}\int  d^3\boldsymbol{q} \frac{Ze^{2}}{\epsilon_{0}q^{2}}\exp(i\boldsymbol{q}\cdot \boldsymbol{r})  $$
- By analogy, the _total potential energy_ of the _point charge in a dielectric_, while _taking screening into account_:
$$U(\boldsymbol{r})=-\frac{1}{(2\pi)^{3}}\int  d^3\boldsymbol{q} \frac{1}{\varepsilon_{1}(\boldsymbol{q},0)} \frac{Ze^{2}}{\epsilon_{0}q^{2}}\exp(i\boldsymbol{q}\cdot \boldsymbol{r})$$
- The _induced charge density_ is then:
$$\frac{1}{\epsilon_{0}}\rho _\text{ind}(\boldsymbol{r})=-\nabla^{2}\frac{U(\boldsymbol{r})-U_\text{ext}(\boldsymbol{r})}{-e}$$
- One finds:
$$\displaylines{\rho _\text{ind}(\boldsymbol{r})=-\frac{Ze}{r}\int_{0}^{\infty}  dq \,g(q)\sin qr \\ g(q)=\frac{q}{2\pi^{2}} \frac{\varepsilon_{1}(q,0)-1}{\varepsilon_{1}(q,0)} \qquad \varepsilon_{1}(q,0)=1+\frac{k_\text{TF}^{2}}{q^{2}}F\left( \frac{q}{2k_{F}} \right)}$$
- The limits of $g(q)$, where $C$ is a _constant_:
$$\lim_{ q \to 0 }g(q)=\lim_{ q \to \infty }g(q)=0  \qquad \lim_{ q \to 2k_{F} } \frac{dg}{dq}=C\ln|q-2k_{F}| \qquad \lim_{ q \to 2k_{F} }=\frac{C}{q-2k_{F}}  $$

- The di-electric _screens the charge perfectly_:
$$Q_{S}=\int  d^{3}\boldsymbol{r}\,\rho _\text{ind}(\boldsymbol{r})=-Ze $$
- From _integration by parts_, and approximating the integral by considering the _region near the singularity at_ $2k_{F}$
$$\rho _\text{ind}(\boldsymbol{r})\approx \frac{ZeC}{r^{3}}\int_{2k_{F}-\Delta}^{2k_{F}+\Delta}  dq  \frac{1}{q-2k_{F}}\sin qr$$
- From _expanding_ $\sin[(q-2k_F)r+2k_{F}r]$, one can _eliminate_ the odd parity part of the function, then make the substitution $-r\Delta<x=(q-2k_{F})r<r\Delta$
$$\rho _\text{ind}(\boldsymbol{r})\approx \frac{ZeC\cos(2k_{F}r)}{r^{3}} \int_{-r\Delta}^{r\Delta}  dx\,\frac{\sin x}{x} $$
- Approximating the limits as $\pm \infty$, one gets:
$$\rho _\text{ind}(\boldsymbol{r})\approx \frac{\pi ZeC\cos(2k_{F}r)}{r^{3}}$$

- There are _Friedel oscillations_ in the _induced charge density_ with wave-vector $2k_{F}$
	- It also occurs in _spin densities_ and is resonsible for the [[#RKKY Interaction]]
	- In 1 dimension, the system is simply _unstable_ (Peierls instability)

## Scattering and correlation functions
- Define the _density correlation function_:
$$C(_{\rho}\boldsymbol{x},\boldsymbol{x}',t,t')=\braket{  \rho(\boldsymbol{x},t) \rho(\boldsymbol{x}',t')} $$
- This features an _average over a quantum ensemble_ with weighting from the _equilibrium distribution function_

- The _density fluctuation correlation function_:
$$\begin{align}
S_{\rho}(\boldsymbol{x},\boldsymbol{x}',t,t')&=\Braket{  (\rho(\boldsymbol{x},t)-\braket{ \rho(\boldsymbol{x},t)  } )(\rho(\boldsymbol{x}',t')-\braket{ \rho(\boldsymbol{x}',t')  } )  }  \\
&=C_{\rho}(\boldsymbol{x},\boldsymbol{x}',t,t')-\braket{ \rho(\boldsymbol{x},t)  }^{2} 
\end{align}$$
- At _equilibrium_, the time dependence only depends on the _interval_ $t-t'$

- It describes the _correlation_ between _charge density at_ $(\boldsymbol{x},t)$ dependent on charge density at $(\boldsymbol{x}',t')$
	- Example: _Bragg peaks_ for $\boldsymbol{x}'-\boldsymbol{x}=\boldsymbol{R}$ where $\boldsymbol{R}$ is a _lattice vector_

- The _spacetime Fourier transform_ is the _structure factor_:
$$C_{\rho}(\boldsymbol{q},\omega)=\frac{1}{V}\int  d^3\boldsymbol{x}\,d^{3}\boldsymbol{x}' \int  dt\,S_{\rho}(\boldsymbol{x},\boldsymbol{x}',t)\exp[i(\boldsymbol{q}\cdot(\boldsymbol{x}-\boldsymbol{x}')-\omega t)] $$
- It is _proportional_ to the _second derivative of the scattering cross-section_ for a probe particle with wave-vector $\boldsymbol{k}$, leaving with $\boldsymbol{k}+\boldsymbol{q}$
$$C_\rho(\boldsymbol{q},\omega)\propto \frac{d^{2}\sigma}{d\Omega\,d\omega}$$
## Fluctuation-dissipation theorem
- It can be shown that the _density function correlation_ is _proportional_ to the _dissipation response_:
$$S_{\rho}(\boldsymbol{q},\omega)=\frac{k_{B}T}{\omega}\chi_{2}(\boldsymbol{q},\omega)$$
- The [[Theories of Quantum Matter#General fluctuation-dissipation theorem|Fluctuation-Dissipation Theorem]]

- _Plasmons_: probing methods (optical conductivity, EELS, etc.) _couple_ to _fluctuations_ in electronic charge density
- _Phonons_: inelastic neutron scattering couples to _fluctuations in nuclear density_
- _Magnons_: Inelastic neutron scattering also couples to _electronic spin density_ due to the magnetic moment of the neutron
# Quasi-particles: Fermi liquid theory
- _Quasi-particles_: Elementary excitation thought of as a _non-interacting particle with modified dispersion relation_

## Normal Fermi liquids
- Even for _strong many-body interactions_, physical properties can be _well-described_ by an _independent particle model_
	- Known as _normal Fermi liquids_
- Example: _linear heat capacity_ for low temperature $\ce{ ^{3}He }$, albeit with _enhanced particle mass_

### Correspondence between non-interacting and interacting states
- Consider a system of _non-interacting fermions_ with single particle states $\{\Psi_{i}\}$
- Many-particle state is a _Slater determinant_
- Label state by _occupation numbers_ $\{n_{i}\}=0,1$
- If one _turns on_ interactions and _assume no phase transition_, the state _evolves_ into that of an _interacting system_
	- The process can be _reversed_ to go back into the product state
- Therefore, there is a _one-to-one_ correspondence between _non-interacting product states_ and _interacting many-particle states_

- The _interacting many particle state_ can then still be labelled with occupations $\{n_{i}\}$
- Any system _with_ this _one-to-one correspondence_ are then _normal Fermi liquids_

- For normal Fermi liquids, one can also assume _all energies are continuous across the Fermi surface_
### Quasi-particles
- From the _ground state_ of the _non-interacting_ system, one can _add_ a particle of momentum $\boldsymbol{p}$
- This _corresponds_ to adding a _quasi-particle_ of momentum $\boldsymbol{p}$ to the _interacting_ system

- A _quasi-particle_ can be thought of as a normal particle along with a _distortion_ in the surrounding fermion distribution
- One can also define a _quasi-particle energy_ $\varepsilon_\lambda(\boldsymbol{p})$, where $\lambda$ denotes _spin_

- Consider the ground state of the _non-interacting system_ as a _filled Fermi sphere_
![[Fermi sphere.png|200]]
- Add an extra particle of momentum $p>p_{F}$
- The energy _above_ the _chemical potential_ $\mu=p_{F}^{2}/(2m)$, also known as the _excitation energy_, for $|\boldsymbol{p}-\boldsymbol{p}_{F}|\ll p_{F}$:
$$\varepsilon_{\lambda}(\boldsymbol{p})-\mu\approx v_{F}(p-p_{F})$$
- Here, $v_{F}=p_{F}/m$ is the _group velocity_ on the _Fermi surface_

- Then _turn on interactions_, which _conserves momentum_
- The quasiparticle still has _momentum_ $\boldsymbol{p}$, now with a _quasi-particle excitaion energy_:
$$\varepsilon_{\lambda}(\boldsymbol{p})-\mu=v_F(p-p_{F})$$
- Here, the _quasiparticle group velocity_ is _re-scaled_ with some _effective mass_:
	- Effective mass _different from band effective mass_
$$v_{F}=p_{F}/m^{*}$$

- Similarly, one can define _quasiholes_, where a particle of momentum $\boldsymbol{p}$ is _removed_ from the Fermi sphere
- The _excitation energy of a quasihole_ is then:
$$-\varepsilon_{\lambda}(\boldsymbol{p})+\mu$$

- The _number_ of quasiparticles for each $(\boldsymbol{p},\lambda)$ is _conserved
	- $[H,n_{\lambda}(\boldsymbol{p})]=0$ as the phase space vanishes quadratically with energy (see below)

### Relevant quantities
- The _quasi-particle density of states_:
	- Becomes relevant for _physical properties_
	- For _low temperatures_, many quantities depend on $g(\varepsilon=0)$
$$g_{V}(\varepsilon)=\frac{1}{V}\sum_{\boldsymbol{p},\lambda}\delta[\varepsilon_{\lambda}(\boldsymbol{p})-\mu-\varepsilon]$$
- One can also define a _quasiparticle group velocity_:
$$\boldsymbol{v}_{\boldsymbol{p}}=\nabla_{\boldsymbol{p}}\varepsilon_{\boldsymbol{p}}$$
### Quasi-particle lifetime
- Quasiparticles _scatter_ and _lose energy_, while _conserving_ total number
- The dominant mechanism:
	- Quasiparticle of $\varepsilon>\mu$ _decays_ into another quasiparticle of energy $\varepsilon_{1'}>\mu$ and a _quasiparticle-quasihole_ pair of $\varepsilon_{2}<\mu$ and $\varepsilon_{2}'>\mu$
	- The energy of _creating_ a _quasihole_ is equivalent to _absorbing_ an incoming quasiparticle
![[Quasiparticle scattering.png]]
- The conditions of quasiparticles being above or below the Fermi surface:
$$\varepsilon_{1}',\varepsilon_{2}'>E_{F} \qquad \varepsilon_{2}<E_{F}$$

- The process must _conserve energy_:
$$\varepsilon=\varepsilon_{1'}+\varepsilon_{2'}-\varepsilon_{2}$$
- It must also _conserve momentum_ and _spin_:
$$\displaylines{\boldsymbol{p}=\boldsymbol{p}_{1'}+\boldsymbol{p}_{2'}-\boldsymbol{p}_{2}\implies \boldsymbol{p}-\boldsymbol{q}=\boldsymbol{p}_{1}',\quad \boldsymbol{p}_{2}+\boldsymbol{q}=\boldsymbol{p}_{2'} \\ \lambda+\lambda_{2}+\lambda_{1'}+\lambda_{2'}=0}$$
- This is also known as _forward scattering_

- At _zero temperature_, as $\mu\to E_{F}$, the above conditions mean that if the _initial_ particle is on the Fermi surface, _the final particles_ will _also be on the Fermi surface_
- Therefore, for $T=0$, the _lifetime_ for $\varepsilon_{\lambda}(\boldsymbol{p})=\mu$ is _infinite_

- The _quasi-particle scattering rate_:
$$\frac{1}{\tau(\boldsymbol{p})}\propto \frac{\pi^{2}(k_{B}T)^{2}+(\varepsilon_{\lambda}(\boldsymbol{p})-\mu)^{2}}{1+\exp[-(\varepsilon_\lambda(\boldsymbol{p})-\mu)/(k_{B}T)]}$$
- Regimes of quasiparticle energy:
	- $|\varepsilon_{\lambda}(\boldsymbol{p})-\mu|\ll k_{B}T$: excitations within energy $k_{B}T$,  $\tau\sim T^{-2}$
	- $|\varepsilon_{\lambda}(\boldsymbol{p})-\mu|\sim k_{B}T$: the _ground state_ regime
	- $|\varepsilon_{\lambda}(\boldsymbol{p})-\mu|\gg k_{B}T$: there is _no thermal broadening_, $\tau^{-1}\sim \varepsilon^{2}$

## Quasiparticle energy expansion
- For a _distribution of quasiparticles_ $n_{\lambda}(\boldsymbol{p})$, one can quantify the "amount of excitation" with the _quasiparticle excitation distribution_
	- Distribution in the _new, interacting, excited eigenstate_ of the system
$$\delta n_{\lambda}(\boldsymbol{p})=n_{\lambda}(\boldsymbol{p})-n_{\lambda}^{0}(\boldsymbol{p})$$
- Here, $n^{0}_{\lambda}(\boldsymbol{p})$ is the _ground state distribution_, treated as a _step function_ at $\mu$
 
- Assume the system is in contact with a _reservoir_ of chemical potential $\mu$, such that the number of _quasiparticles_ and _quasiholes_ are _not necessarily equal_
- Define an _effective energy_
	- Different from Helmholtz free energy, but still an _extensive quantity_
$$F=E-\mu N$$
- At _low termperatures_ $T<T_{F}=E_{F}/k_{B}$, _approximate_ $F$ as a _functional_
$$\begin{align}
F=F_{0}&+\sum_{\boldsymbol{p},\lambda}[\varepsilon_{\lambda}(\boldsymbol{p})-\mu]\delta n_{\lambda}(\boldsymbol{p}) \\
&+\frac{1}{2V}\sum_{\boldsymbol{p},\boldsymbol{p}'}\sum_{\lambda,\lambda'} f_{\lambda,\lambda'}(\boldsymbol{p},\boldsymbol{p}')\delta n_{\lambda}(\boldsymbol{p}) \delta n_{\lambda'}(\boldsymbol{p}')+O(\delta n^{3})
\end{align}$$
- The _error_ in this expansion is of order $O(T^{6})$
	- See [[#The effect of temperature]]

- The _first order_ term is the _quasiparticle excitation energy_
	- $\varepsilon_{\lambda}(\boldsymbol{p})-\mu$ is the _first variational derivative_
- The _second order_ erm is the _quasiparticle-quasiparticle interaction energy_
	- $f_{\lambda,\lambda'}(\boldsymbol{p},\boldsymbol{p}')/V$ is a _second variational derivative_
	- The _probability_ of two quasi-particles $\boldsymbol{p},\boldsymbol{p'}$ interacting is $\sim a^{3}/V$ where $a$ is the _interaction range_

## Interaction energy and Landau parameters
- The interaction energy is _spin-dependent_
	- It is both a _relativistic effect_, and a result of the _exchange interaction_
	- In _metals_, the latter is typically $\sim 10^{1}$ larger than other contributions to interaction energy

- In a material with _time-reversal symmetry_ and _inversion symmetry_:
$$f_{\lambda,\lambda'}(\boldsymbol{p},\boldsymbol{p}')=f_{-\lambda,-\lambda'}(-\boldsymbol{p},-\boldsymbol{p}')=f_{\lambda,\lambda'}(\boldsymbol{p},\boldsymbol{p}')$$
- For an _isotropic system_, the interaction parameter also only takes the _angle_ $\xi$ _between momenta_

- If spin is _conserved_ (accounting for _only the exchange interaction_), the interaction parameter can then be split into _spin-symmetric_ and _spin-antisymmetric_ parts:
$$\displaylines{f_{\lambda,\lambda'}(\boldsymbol{p},\boldsymbol{p}')=f^{(s)}(\cos \xi)+\gamma_{\lambda,\lambda'}f^{(a)}(\cos \xi) \\ \gamma_{\lambda,\lambda'}=\begin{cases}
1&\lambda=\lambda' \\ -1 &\lambda\neq\lambda'
\end{cases} \qquad \boldsymbol{p}\cdot \boldsymbol{p}'=pp'\cos \xi}$$
- The parameters can then be written as a _multipole expansion_:
$$f^{(s/a)}(\cos \xi)=\sum_{l=0}^{\infty}f_{l}^{(s/a)}P_{l}(\cos \xi)$$
- The _coefficients_ define the dimensionless _Landau parameters_:
$$F_{l}^{(\alpha)}=g_{V}(0)f_{l}^{(\alpha)}=\frac{m^{*}p_{F}}{\pi^{2}\hbar^{3}}f_{l}^{(\alpha)}$$
- The $l=0$ parameter is the _isotropic response_ of the system

- Write in terms of the _polar angles_ of $\boldsymbol{p}$ and $\boldsymbol{p}'$, using a property of $P_{l}$ (the _addition theorem_)
$$\displaylines{P_{l}(\cos \xi)=\frac{4\pi}{2l+1}\sum_{m=-l}^{l}Y_{l,m}(\theta,\phi)Y^{*}_{l,m}(\theta',\phi') \\ f^{(\alpha)}(\cos \xi)=\sum_{l=0}^{\infty} \sum_{m=-l}^{l} \frac{4\pi}{2l+1}f_{l}^{(\alpha)}Y_{l,m}(\theta,\phi)Y^{*}_{l,m}(\theta',\phi')}$$
## Local properties
- Consider a normal Fermi liquid with pre-existing quasiparticle distribution $\delta n_{\lambda}(\boldsymbol{p})$
- When _adding_ another particle at momentum $\boldsymbol{p}$, due to _interactions_, it will have some _effective energy_ $\tilde{\varepsilon}_{\lambda}(\boldsymbol{p})-\mu$, given by the _first variational derivative_
$$\tilde{\varepsilon}_{\lambda}(\boldsymbol{p})-\mu=\frac{\delta F}{\delta n_{\lambda}(\boldsymbol{p})}$$
- Using the [[#Quasiparticle excitation and effective energy|formula]] for $\delta F$:
	- It is also defined for an _inhomogeneous_ system with $\delta n_{\lambda}(\boldsymbol{p},\boldsymbol{r})$, as there are _local distortions_
$$\tilde{\varepsilon}_{\lambda}(\boldsymbol{p})-\mu=(\varepsilon_{\lambda}(\boldsymbol{p})-\mu)+\frac{1}{V}\sum_{\boldsymbol{p}',\lambda'}f_{\lambda,\lambda'}(\boldsymbol{p},\boldsymbol{p}')\delta n_{\lambda'}(\boldsymbol{p}')$$
- $\varepsilon_{\lambda}(\boldsymbol{p})-\mu$ is known as the _local quasiparticle excitation energy_

### Force, local excitation, and current
- Its _gradient_ in ordinary space represents the _average force exerted_ by the _surrounding medium_ on the quasiparticle $\boldsymbol{p}$
$$\nabla_{\boldsymbol{r}}\tilde{\varepsilon}_{\lambda}(\boldsymbol{p},\boldsymbol{r})=\nabla_{\boldsymbol{r}}\left( \frac{1}{V} \sum_{\boldsymbol{p}',\lambda'}f_{\lambda,\lambda'}(\boldsymbol{p},\boldsymbol{p}')\delta n_{\lambda'}(\boldsymbol{p}')\right)$$
- Define the _local quasiparticle excitation distribution_
	- As opposed to the [[#Quasiparticle energy expansion|quasiparticle excitation distribution]] $\delta n_{\lambda}(\boldsymbol{p})=n_{\lambda}(\boldsymbol{p})-n^{0}(\varepsilon_{\lambda}(\boldsymbol{p})-\mu)$
	- This quantifies the _departure from local equilibrium_ in the Fermi liquid
$$\displaylines{\delta \tilde{n}_{\lambda}(\boldsymbol{p})=n_{\lambda}(\boldsymbol{p})-\tilde{n}_{\lambda}^{0}(\boldsymbol{p}) \\ \tilde{n}_{\lambda}^{0}(\boldsymbol{p})=n^{0}(\tilde{\varepsilon}_{\lambda}(\boldsymbol{p})-\mu)}$$

- The _total current density_ due to local movement and departure from equilibrium:
	- Here, $v_{\boldsymbol{p}}$ is the [[#Relevant quantities|group velocity]] $\nabla_{\boldsymbol{p}}\varepsilon_{\lambda}(\boldsymbol{p})$
$$\boldsymbol{J}=\frac{1}{V}\sum_{\boldsymbol{p},\lambda}v_{\boldsymbol{p}}\delta \tilde{n}_{\lambda}(\boldsymbol{p})$$
- From comparing definitions, one also finds:
$$\begin{align}
\delta \tilde{n}_{\lambda}(\boldsymbol{p})&=\delta n_{\lambda}(\boldsymbol{p})-\frac{\partial n^{0}(\varepsilon_{\lambda}(\boldsymbol{p})-\mu)}{\partial\varepsilon_{\lambda}(\boldsymbol{p})}(\tilde{\varepsilon}_{\lambda}(\boldsymbol{p})-\varepsilon_{\lambda}(\boldsymbol{p}))  \\
&=\delta n_{\lambda}(\boldsymbol{p})-\frac{\partial n^{0}}{\partial\varepsilon_{\lambda}} \frac{1}{V}\sum_{\boldsymbol{p}',\lambda'} f_{\lambda,\lambda'}(\boldsymbol{p},\boldsymbol{p}')\delta n_{\lambda'}(\boldsymbol{p}')
\end{align}$$

### Simplifying the local quasiparticle excitation
- Simplify the above for a _system at zero temperature_

- Split $\delta n_{\lambda}$ and $\delta n_{\lambda'}$ into spin-symmetric and antisymmetric components:
$$\displaylines{\delta n_{\lambda}(\boldsymbol{p})=\delta n^{(s)}(\boldsymbol{p})+\eta_{\lambda}\delta n^{(a)}(\boldsymbol{p}) \qquad \delta \tilde{n}_{\lambda}(\boldsymbol{p})=\delta \tilde{n}^{(s)}(\boldsymbol{p})+\eta_{\lambda}\delta \tilde{n}^{(a)}(\boldsymbol{p}) \\ \eta_{\lambda}=\begin{cases}
1&\eta=\uparrow \\ -1&\eta=\downarrow
\end{cases}}$$

- Once again _splitting_ $f_{\lambda,\lambda'}(\cos \xi)$ and substituting into $\delta \tilde{n}_{\lambda}-\delta n_{\lambda}$, with $\varepsilon_{\lambda}=\varepsilon$
$$\begin{align}
\delta \tilde{n}^{(s/a)}(\boldsymbol{p})&=\delta n^{(s/a)}(\boldsymbol{p})-\frac{\partial n^{0}}{\partial\varepsilon} \frac{2}{V}\sum_{\boldsymbol{p}'}f^{(s/a)}(\cos \xi)\delta n^{(s/a)}(\boldsymbol{p}') \\
&=\delta n^{(s/a)}(\boldsymbol{p})+\frac{2}{V}\delta(\varepsilon(\boldsymbol{p})-\mu )\sum_{\boldsymbol{p}'}f^{(s/a)}(\cos \xi)\delta n^{(s/a)}(\boldsymbol{p}')
\end{align}$$
- At _zero temperature_, expand $\delta n$
$$\displaylines{\delta n^{(s/a)}(\boldsymbol{p})=\delta(\varepsilon(\boldsymbol{p})-\mu)\sum_{l,m}\delta n^{(s/a)}_{l,m}Y_{l,m}(\theta,\phi) \\ \delta \tilde{n}^{(s/a)}(\boldsymbol{p})=\delta(\varepsilon(\boldsymbol{p})-\mu)\sum_{l,m}\delta \tilde{n}^{(s/a)}_{l,m}Y_{l,m}(\theta,\phi)}$$
- _Expanding_ $\delta n^{(s/a)}$ and comparing:
$$\delta \tilde{n}^{(s/a)}_{l,m}=\left( 1+\frac{F_{l}^{(s/a)}}{2l+1} \right)\delta n_{l,m}^{(s/a)}$$

## Equilibrium properties

### Effective mass
- Derive a relation between the _bare particle mass_ $m$ and the _quasiparticle mass_ $m$
- Both the _bare_ and _quasiparticle current densities_ must be the _same_

- The _total current density_:
$$J=\frac{1}{V}\sum_{\boldsymbol{p},\lambda}v_{\boldsymbol{p},\lambda}\delta \tilde{n}_{\lambda}(\boldsymbol{p})$$
- Substituting from above, _swapping_ dummy variables and using symmetry in $\lambda,\lambda'$
	- In terms of _actual excitation number_ at $\boldsymbol{p}$ instead of departure from _local equilibrium_
$$J=\frac{1}{V}\sum_{\boldsymbol{p},\lambda}j_{\boldsymbol{p},\lambda}\delta n_{\lambda}(\boldsymbol{p})$$
- Here, $j_{\boldsymbol{p},\lambda}$ is the _current density of quasiparticles_ $(\boldsymbol{p},\lambda)$
$$j_{\boldsymbol{p},\lambda}=v_{\boldsymbol{p},\lambda}-\frac{1}{V}\sum_{\boldsymbol{p}',\lambda'}v_{\boldsymbol{p}',\lambda'} \frac{\partial n^{0}}{\partial\varepsilon_{\lambda'}(\boldsymbol{p}')}f_{\lambda,\lambda'}(\boldsymbol{p},\boldsymbol{p}')$$
- This must be equal to the _bare current density_ $\boldsymbol{p}/m$
- Define the _effective mass_ using the group velocity:
$$v_{\boldsymbol{p},\lambda}=\frac{\boldsymbol{p}}{m^{*}}$$
- Equating the two current densities and taking the dot product with $\boldsymbol{p}$, at _zero temperature_
$$\frac{1}{m}=\frac{1}{m^{*}}+\frac{1}{V}\sum_{\boldsymbol{p}'\lambda'}\frac{\cos \xi}{m^{*}}\delta[\varepsilon_{\lambda}(\boldsymbol{p})-\mu]f_{\lambda,\lambda'}(\boldsymbol{p},\boldsymbol{p}')$$
- Then perform the sum _assuming spin degeneracy_, with $P_{1}=\cos \xi$
$$\frac{1}{m}=\frac{1}{m^{*}}+\frac{2}{V}\sum_{\boldsymbol{p}'} \frac{1}{m^{*}}\delta(\varepsilon(\boldsymbol{p})-\mu)\sum_{l}f_{l}^{(s)}P_{l}(\cos \xi)P_{1}(\cos \xi)$$
- Converting the sum into a _surface integral over momentum space_:
$$\frac{1}{m}=\frac{1}{m^{*}}+\frac{1}{m^{*}} \frac{1}{4\pi}g_{V}(0)\sum_{l} f_{l}^{(s)} \int  dS\,P_{l}(\cos \xi)P_{1}(\cos \xi) $$
- Then using _orthogonality_ of the Legendre polynomials: 
$$m^{*}=\left( 1+\frac{F_{1}^{(s)}}{3} \right)m$$
### The effect of temperature
- The energy required to _add_ a particle $(\boldsymbol{p},\lambda)$ is given by $\tilde{\varepsilon}_{\lambda}(\boldsymbol{p})-\mu$
- Hence, at _finite temperature_, use the _Fermi distribution_:
$$n^{0}_{\boldsymbol{p},\lambda}(T,\mu)=\frac{1}{1+\exp[(\tilde{\varepsilon}_{\lambda}(\boldsymbol{p})-\mu)/k_{B}T]}$$
- The _interaction energy correction_ in $\tilde{\varepsilon}_{\lambda}(\boldsymbol{p})-\varepsilon_{\lambda}(\boldsymbol{p})$ is on the _order_ of:
$$\sum_{\boldsymbol{p}'}Y_{l,m}^{*}(\theta',\phi')\delta n_{\lambda'}(\boldsymbol{p}')\sim \int p^{2} \frac{\partial n^{0}}{\partial\varepsilon}\delta n(\boldsymbol{p})\, dp  \sim \int   H(\varepsilon) \delta n_{\lambda}(\boldsymbol{p}) d\varepsilon $$
- From the _Sommerfeld expansion_:
$$\int  H(\varepsilon)\delta n_{\lambda}(\boldsymbol{p})\,d\varepsilon=\frac{\pi^{2}}{6}(k_{B}T)^{2}\,\frac{dH(\varepsilon)}{d\varepsilon}\Bigg|_{\varepsilon=\mu}+O(T^{4}) $$

- The _interaction energy correction_ is of order $O(T^{2})$

- Therefore, in the _exponential_, one can replace $\tilde{\varepsilon}$:
$$n^{0}_{\boldsymbol{p},\lambda}(T,\mu)=\frac{1}{1+\exp[(\varepsilon_{\lambda}(\boldsymbol{p})-\mu)/k_{B}T]}$$
- One also typically _expands_ the free energy only up to $O(T^{2})$
$$F=F_{0}+\sum_{\boldsymbol{p},\lambda}(\varepsilon_{\lambda}(\boldsymbol{p})-\mu)\delta n_{\lambda}(\boldsymbol{p})+O(T^{4})$$
- Any thermodynamic quantity _depending solely on $F$_ is _not directly affected by interactions_
### Heat capacity
- From the definition of heat capacity:
$$C_{V}=\frac{\partial E}{\partial T}\Bigg|_{N}=T\frac{\partial S}{\partial T}=\frac{\partial F}{\partial T}\Bigg|_{\mu}$$
- Using the free energy expansion above, with _spin degeneracy_:
$$F=F_{0}+\frac{V}{(2\pi)^{3}} (2)(4\pi)\int p^{2}\,dp\,(\varepsilon(p)-\mu)\delta n_{\lambda}(p)+O(T^{4}) $$
- Changing variables with $\varepsilon=p^{2}/2m$, and using the Sommerfeld integral:
$$F=F_{0}+V\frac{m^{*}p_{F}}{6\hbar^{3}}(k_{B}T)^{2}+O(T^{4})$$
- From this:
$$C_{V}=V\frac{m^{*}p_{F}}{3\hbar^{3}}k_{B}^{2}T+O(T^{3})$$
- At _low temperatures_, it is simply the same as a _non-interacting system_ but with _renormalised mass_ due to interactions
### Isothermal bulk compressibility
- The _isothermal bulk compressibility_:
$$\frac{1}{\kappa_{T}}=-V \frac{\partial P}{\partial V}\Bigg|_{T,N}$$
- At _zero temperature_:
$$P=-\frac{\partial E}{\partial V}\Bigg|_{T,N}\implies \frac{1}{\kappa}=V \frac{\partial^{2}E}{\partial V^{2}}\Bigg|_{T,N}$$
- As $E$ is an _extensive quantity_, write:
$$\displaylines{E=Vf(\rho) \\ \mu=\frac{\partial E}{\partial N}\Bigg|_{T,V}=f' \qquad \kappa=\rho^{2}f''(\rho) =N\rho \frac{\partial \mu}{\partial N}\Bigg|_{T,V}}$$

- Consider _local excitations resulting from_ a _shift_ in $\mu$ at zero temperature:
$$\delta \tilde{n}_{\lambda}(\boldsymbol{p})=n^{0}[\tilde{\varepsilon}_{\lambda}(\boldsymbol{p})-\mu-d\mu]-n^{0}[\tilde{\varepsilon}_{\lambda}(\boldsymbol{p})-\mu]=-d\mu \frac{\partial n^{0}}{\partial\varepsilon_{\lambda}(\boldsymbol{p})}=d\mu\delta[\varepsilon_{\lambda}(\boldsymbol{p})-\mu]$$
- For an _isotropic, spin-independent system_, using the [[#Simplifying the local quasiparticle excitation|zero temperature relation]]:
$$\displaylines{\delta n_{\uparrow}(\boldsymbol{p})=\delta n_{\downarrow}(\boldsymbol{p})=\delta n^{(s)}(\boldsymbol{p}) \\\delta \tilde{n}_{\lambda}(\boldsymbol{p})=(1+F^{(s)}_{0})\delta n_{\lambda}(\boldsymbol{p}) }$$
- Change in number of particles:
$$dN=\sum_{\boldsymbol{p},\lambda}\delta n_{\lambda}(\boldsymbol{p})=\sum_{\boldsymbol{p},\lambda}\delta[\varepsilon_{\lambda}(\boldsymbol{p})-\mu] \frac{1}{1+F_{0}^{(s)}}d\mu=\frac{Vg_{V}(0)}{1+F_{0}^{(s)}}d\mu$$
- Qualitatively, a shift in $\mu$ from the compression includes both:
	- A shift in the _Fermi energy_, adding particles
	- The _addition of quasiparticles_ means _extra interaction energy_

- The _isothermal bulk compressibility_:
$$\kappa_{T}=\frac{1}{\rho^{2}} \frac{g_{V}(0)}{1+F_{0}^{(s)}}$$

- The system is only _stable if_ $1+F_{0}^{(s)}>0$
	- Otherwise, _density fluctuations_ will _grow exponentially_ to give a _phase transition_
### Spin susceptibility
- Subject a normal Fermi liquid to a _magnetic field_ $\boldsymbol{B}=(0,0,B)$

- For a particle of spin $\sigma=\pm 1/2$
$$\varepsilon_{\lambda,B}=-\frac{\lambda}{2}g\mu _{B}B$$
- The _local excitation distribution_ due to the magnetic field:
$$\delta \tilde{n}_{\lambda}(\boldsymbol{p})=n^{0}[\tilde{\varepsilon}_{\lambda}(\boldsymbol{p})-\mu+\varepsilon_{\lambda,B}]-n^{0}[\tilde{\varepsilon}_{\lambda}(\boldsymbol{p})-\mu]=-\frac{\lambda}{2}g\mu_{B}B \frac{\partial n^{0}}{\partial\varepsilon_{\lambda}(\boldsymbol{p})}$$
- At zero temperature:
$$\delta \tilde{n}_{\lambda}(\boldsymbol{p})=\frac{\lambda}{2}g\mu_{B}B\delta[\epsilon_{\lambda}(\boldsymbol{p})-\mu]$$
- Due to the magnetic field:
$$\delta n_{\uparrow}(\boldsymbol{p})=-\delta n_{\downarrow}(\boldsymbol{p})=\delta n^{(a)}(\boldsymbol{p})$$

- The _total magnetisation_:
$$M=\sum_{\boldsymbol{p},\lambda}g\mu_{B}\frac{\lambda}{2}\delta n_{\lambda}(\boldsymbol{p})$$
- Again using the relation between the excitation functions, for an _isotropic system_:
$$M=\frac{1}{4}(g\mu_{B})^{2}B \frac{Vg_{V}(0)}{1+F_{0}^{(a)}}$$
- As $B=\mu_{0}H$, the _paramagnetic spin susceptibility_ is:
$$\chi=\frac{M}{HV}=\frac{1}{4} \frac{g^{2}\mu_{B}^{2}\mu_{0}}{1+F_{0}^{(a)}}g_{V}(0)$$
# Second quantisation
- Express wave-functions in terms of _creation and annihilation operators_ for _each single particle state_
- A _many-particle product state_ with _occupation numbers_ $n_{i}$ for each _single particle state_ $\psi_{i}$ is denoted
$$\ket{n_{1},n_{2}\dots} $$
- In general, a state is a _linear combination_ of Slater determinants:
$$\ket{\Psi(t)}=\sum_{\{n\}}f(\{n\};t)\ket{\{n\}}  $$
- Each Slater determinant is denoted:
$$\ket{n_{1},\dots} =(c_{1}^{\dagger})^{n_{1}}\dots \ket{\text{VAC}} $$
- The _fermionic creation and annihilation operators_:
$$\{c_{i},c_{j}^{\dagger}\}=\delta_{ij}$$
- The Schrodinger equation can still be _expressed using product states_:
$$\displaylines{i\hbar \frac{\partial}{\partial t}\ket{\Psi(t)} =H\ket{\Psi(t)} \\ H=\sum_{i,j}\braket{ \psi _{i} |h|\psi_{j}  }c_{i}^{\dagger}c_{j}+\frac{1}{2}\sum_{i,j,k,l}\braket{ \psi_{i}|\braket{ \psi_{j} | g|\psi_{k} }  | \psi_{l} }c^{\dagger}_{i}c^{\dagger}_{j}c_{l}c_{k}  }$$
## Mean field approximation
- The _mean field approximation_
$$\begin{align}
c_{i}^{\dagger}c_{j}^{\dagger}c_{k}c_{l} &=\braket{ c_{i}^{\dagger} c_{l}  }c_{j}^{\dagger}c_{k}-\braket{ c_i^{\dagger} c_{k}  }c_{j}^{\dagger}c_{l}  \\
&+\braket{  c_{j}^{\dagger}c_{k}  } c_{i}^{\dagger}c_l-\braket{ c_{j}^{\dagger}c_{l}  }c_{i}^{\dagger}c_{k} \\
&-\braket{ c_{i}^{\dagger}c_{l}  } \braket{ c_{j}^{\dagger}c_{k}   } +\braket{ c_{i}^{\dagger}c_k}\braket{ c_{j}^{\dagger} c_{l`}  }     
\end{align}$$

## Jellium
- The _eigenstates_ in jellium:
$$\braket{ \boldsymbol{r} | \boldsymbol{k},\lambda } =\frac{1}{\sqrt{ V }}\exp(i\boldsymbol{k}\cdot \boldsymbol{r})\chi_{\lambda}$$
- The Hamiltonian:
$$\displaylines{H=\sum_{i=1}^{N} \frac{p_{i}^{2}}{2m}+\frac{1}{2}\sum_{i\neq j} \frac{e^{2}}{4\pi\epsilon_{0}} \frac{e^{-\mu|\boldsymbol{r}_{i}-\boldsymbol{r}_{j}|}}{|\boldsymbol{r}_{i}-\boldsymbol{r}_{j}|}+H_\text{e-ion}+H_\text{ion-ion} \\ H_\text{e-ion}=-\frac{e^{2}}{4\pi\epsilon_{0}}\sum_{i=1}^{N}\int  d\boldsymbol{r}\,n(\boldsymbol{r})\frac{e^{-\mu|\boldsymbol{r}-\boldsymbol{r}_{i}|}}{|\boldsymbol{r}-\boldsymbol{r}_{i}|}\\  H_\text{ion-ion}=\frac{1}{2}\frac{e^{2}}{4\pi\epsilon_{0}}\int  d\boldsymbol{r}\int  d\boldsymbol{r}' \,n(\boldsymbol{r})n(\boldsymbol{r}')\frac{e^{-\mu|\boldsymbol{r}-\boldsymbol{r}'|}}{|\boldsymbol{r}-\boldsymbol{r}'|} }$$
- The _exponential factors_ are introduced to make the integrals _converge_, and $\mu$ will later be set to 0
- For _jellium_, the _positive background density_:
$$n(\boldsymbol{r})=\frac{N}{V}$$
- From this:
$$H_\text{e-ion}=-\frac{e^{2}}{4\pi\epsilon_{0}} \frac{N^{2}}{V} \frac{4\pi}{\mu^{2}}=-H_\text{ion-ion}\implies H_\text{e-ion}+H_\text{ion-ion}=0$$

- Then going to the _second quantised representation_ with the _plane wave eigenstates_, and setting $\mu\to 0$
$$H=\sum_{\boldsymbol{k},\lambda} \frac{\hbar^{2}k^{2}}{2m^{*}}c^{\dagger}_{\boldsymbol{k},\lambda}c_{\boldsymbol{k},\lambda}+\frac{1}{2} \frac{e^{2}}{4\pi\epsilon_{0}} \frac{1}{V}\sum_{\substack{\boldsymbol{k},\boldsymbol{p},\boldsymbol{q} \\ \boldsymbol{q}\neq 0}}\sum_{\lambda_{1},\lambda_{2}} \frac{4\pi}{q^{2}}c^{\dagger}_{\boldsymbol{k}+\boldsymbol{q},\lambda_{1}}c^{\dagger}_{\boldsymbol{k}-\boldsymbol{q},\lambda_{2}}c_{\boldsymbol{p},\lambda_{2}}c_{\boldsymbol{k},\lambda_{1}}$$

## Hartree-Fock in second quantisation
- The _effective Hamiltonian_ in [[#The Hartree-Fock Equation]] is:
$$\displaylines{H=h(\boldsymbol{x})+\sum_{m=1}^{N} \Big(J_{m}(\boldsymbol{x})-K_{m}(\boldsymbol{x})\Big) \\ J_{m}(\boldsymbol{x})f(\boldsymbol{x})=\left(\int  d\boldsymbol{y}\,\Psi_{m}^{\dagger}(\boldsymbol{y})g(\boldsymbol{x}-\boldsymbol{y})\Psi_{m}(\boldsymbol{y}) \right)f(\boldsymbol{x}) \\ K_{m}(\boldsymbol{x})f(\boldsymbol{x})=\left(\int  d\boldsymbol{y}\,\Psi_{m}^{\dagger}(\boldsymbol{y})g(\boldsymbol{x}-\boldsymbol{y})f(\boldsymbol{y}) \right)\Psi_{m}(\boldsymbol{x})}$$

- In _second quantisation_, from the above, the Hamiltonian takes the form:
$$\begin{align}
H&=\sum_{i,j}\braket{ \Psi_{i}|H | \Psi_{j} } c_{i}^{\dagger}c_{j} \\ &=\sum_{i,j} \Big(\braket{ \Psi_{i}|h | \Psi_{j} }+\sum_{m} \braket{ \Psi_{i}|_{1}\braket{ \Psi_{m} |_{2}\,g\,| \Psi_{m} }_{2}  |\Psi_{j}  }_{1}  \\
&\hspace{3.8cm}-\sum_{m} \braket{ \Psi_{i}|_{1}\braket{ \Psi_{m} |_{2}\,g\,| \Psi_{j} }_{2}  |\Psi_{m}  }_{1}  \Big)c^{\dagger}_{i}c_{j}
\end{align}$$
- _Alternatively_, use the [[#Mean field approximation]] on the normal Hamiltonian, and assuming a _single Slater determinant_ such that $\braket{ c_{i}^{\dagger} c_{j}  }=\delta_{ij}$
$$H=\sum_{i,j}\braket{ \psi _{i} |h|\psi_{j}  }c_{i}^{\dagger}c_{j}+\frac{1}{2}\sum_{i,j,k,l}\braket{ \psi_{i}|\braket{ \psi_{j} | g|\psi_{k} }  | \psi_{l} }c^{\dagger}_{i}c^{\dagger}_{j}c_{l}c_{k} $$
# Magnetism
- Only arises due to _inter-particle interactions_
	- Unaccounted for by the independent electron model
- _Magnetic ordering_ is a _spontaneous symmetry breaking_ for the system of spins

## Fermionic Hubbard model
- A version of the [[Theories of Quantum Matter#Hubbard model|Hubbard model]]
- Consider a _lattice_ with orbitals $\{\Psi_{i}(\boldsymbol{r}-\boldsymbol{R}_{i})\}$, _centred_ around lattice sites $\boldsymbol{R}_{i}$

- Account for the _energy at the site_, as well as _hopping_ between sites, and an _intra-site Coulomb interaction_ when _both_ $\uparrow$ and $\downarrow$ electrons occupy the _same site_:
$$H=\sum_{i,\lambda}\varepsilon_{i}c^{\dagger}_{i}c_{i}- \sum_{\langle ij \rangle ,\lambda} t_{i,j} [c_{i,\lambda}^{\dagger} c_{j,\lambda}+c^{\dagger}_{j,\lambda}c_{i,\lambda}] +U \sum_{i}c^{\dagger}_{i,\uparrow}c_{i,\uparrow}c^{\dagger}_{i,\downarrow}c_{i,\downarrow} $$
- The _hopping term_ is related to the _overlap integral_ between orbitals $i$ and $j$
- Assume it is _only non-zero for nearest neighbours_
- Also assume _no inter-site Coulomb interaction_

- _Fermion statistics_ will _prevent_ sites from being _doubly occupied_ by particles of the _same spin_

### Example: two electrons on two sites
- The _orbital wavefunctions_ are defined relative to the _site Hamiltonians_: 
$$H_{L/R}=\frac{p^{2}}{2m^{*}}+V_{L/R}\qquad H_{L/R}\Psi_{L/R}=\varepsilon_{L/R}\Psi_{L/R}$$
- The _single particle Hamiltonian_:
$$H_{LR}=\frac{p^{2}}{2m^{*}}+V_{L}+V_{R}$$
- One has to _approximate_ the matrix elements:
$$\displaylines{\braket{ \Psi_{R}|H_{LR} |\Psi_{L}  }=\Braket{ \Psi_{L}|H_{L}+H_{R}-\frac{p^{2}}{2m} | \Psi_{R} }\approx-\Braket{ \Psi_{L}|\frac{p^{2}}{2m} | \Psi_{R} }=-t_{LR}   \\ \braket{ \Psi_{L/R}|H_{LR} | \Psi_{R} } \approx\varepsilon_{L/R
}}$$
- _Set_ $\varepsilon_{L}=\varepsilon_{R}=0$ to simplify the calculation

- There are _six_ basis states:
$$\ket{\uparrow,\uparrow}\quad\ket{\uparrow,\downarrow}\quad\ket{\downarrow,\uparrow} \quad\ket{\downarrow,\downarrow}\quad\ket{\uparrow\downarrow,0}\quad\ket{0,\uparrow\downarrow}     $$
- In this basis:
$$H=\pmatrix{0&0&0&0&0&0 \\ 0&0&0&0&-t_{LR}&t_{LR}\\0&0&0&0&0&0 \\0&-t_{LR}&t_{LR}&0&U&0 \\ 0&-t_{LR}&t_{LR}&0&0&U }$$
- The _lower energy states_ consist of the _triplet_ and an additional _singlet-like_ state
$$\displaylines{E_{T_{0}}=E_{T_{+}}=E_{T_{-}}=0 \qquad E_{S_{0}}=\frac{1}{2}(U-\sqrt{ 16t_{LR}^{2}+U^{2} }) \\ \ket{ \nu_{T_{-}}}=\ket{\downarrow,\downarrow}\quad \ket{\nu_{T_{0}}}=\frac{1}{\sqrt{ 2 }}(\ket{\uparrow,\downarrow}+\ket{\downarrow,\uparrow}  )\quad \ket{\nu_{T_{+}}}=\ket{\uparrow,\uparrow}    \\\ket{\nu_{S_{0}}}=\frac{1}{\sqrt{ 2+2(2t_{LR}/E_{S_{0}})^{2} }}\left( \frac{2t_{LR}}{E_{S_{0}}}(\ket{\uparrow,\downarrow} -\ket{\downarrow,\uparrow} ) -\ket{\uparrow\downarrow,0}-\ket{0,\uparrow\downarrow}  \right) }$$
- The _ground state_ of the system is the _singlet_
- It _maximises overlap_ in order to facilitate _hopping_

- Meanwhile, the _higher energy states_:
$$\displaylines{E_{S_{1}}=U \qquad E_{T_{1}}=\frac{1}{2}(U+\sqrt{ 16t_{LR}^{2}+U^{2} }) \\ \ket{\nu_{S_{1}}}=\frac{1}{\sqrt{ 2 }}(\ket{\uparrow\downarrow,0}-\ket{0,\uparrow\downarrow}  ) \\ \ket{\nu_{T_{1}}}=\frac{1}{\sqrt{ 2+2(2t_{LR}/E_{T_{1}})^{2} }}\left( \frac{2t_{LR}}{E_{T_{1}}}(\ket{\uparrow,\downarrow} -\ket{\downarrow,\uparrow} ) -\ket{\uparrow\downarrow,0}-\ket{0,\uparrow\downarrow}\right) }$$
![[Hubbard energies.png|500]]
### Origin of exchange interactions
- From the energies, one can obtain the _general time evolution_ of the states
- For a state _initially_ in $\ket{\downarrow,\uparrow}$:
![[Hubbard time evolution.png|400]]
- Through _hopping_, the state _oscillates_ between $\ket{\downarrow,\uparrow}$ and $\ket{\uparrow,\downarrow}$
	- The _triplet states_ are eigenstates and _do not change_
- It does this _through the doubly occupied states_
![[Direct exchange.png|400]]

### Low-energy dynamics: the Heisenberg model
- In the limit of $U\gg t$, the _high-energy states_ of $E\sim U$ have _vanishingly small amplitudes_
	- The sites are _not doubly occupied_ due to the energetic cost

- Therefore, there are _four significant eigenstates_ which take the form:
$$\displaylines{E_{T_{0}}=E_{T_{+}}=E_{T_{-}}=0 \qquad E_{S_{0}}=-\frac{4t_{LR}^{2}}{U} \\ \ket{ \nu_{T_{-}}}=\ket{\downarrow,\downarrow}\quad \ket{\nu_{T_{0}}}=\frac{1}{\sqrt{ 2 }}(\ket{\uparrow,\downarrow}+\ket{\downarrow,\uparrow}  )\quad \ket{\nu_{T_{+}}}=\ket{\uparrow,\uparrow}    \\\ket{\nu_{S_{0}}}=\frac{1}{\sqrt{ 2 }}(\ket{\uparrow,\downarrow} -\ket{\downarrow,\uparrow} ) }$$
- Define the _exchange energy_ $J$
$$J\equiv E_\text{singlet}-E_\text{triplet}=-\frac{4t_{LR}^{2}}{U}$$

- Constructing the _effective Hamiltonian_ using the basis $\ket{\uparrow\uparrow},\ket{\uparrow\downarrow},\ket{\downarrow\uparrow},\ket{\downarrow\downarrow}$
$$H_\text{eff}=\frac{t_{LR}^{2}}{U}\pmatrix{0&0&0&0\\0&-2&2&0\\0&2&-2&0\\0&0&0&0}$$
- It can be written in terms of _spin operators_:
	- Denote both _particle number_ and _site_
$$H_\text{eff}=-J\left( S_{L}^{(1)}\cdot S_{R}^{(2)}-\frac{1}{4} \right)$$
- This is the _Heisenberg Hamiltonian_

- The _exchange parameter_ $J$ can be positive or negative as one goes beyond the Fermi-Hubbard model
### Inter-site interactions: the Heitler-London model
- Add _inter-site interactions_, dependent on the _overlap integral_
$$I=\int  d\boldsymbol{r}\,\Psi_{L}^{*}(\boldsymbol{r})\Psi_{R}(\boldsymbol{r}) $$
- The _singlet/triplet states_:
$$\displaylines{\Psi_{S/T}(\boldsymbol{r}_{1},\boldsymbol{r}_{2})=\frac{1}{\sqrt{ 2(1\pm |I|^{2}) }}[\Psi_{L}(\boldsymbol{r}_{1})\Psi_{R}(\boldsymbol{r}_{2})\pm \Psi_{L}(\boldsymbol{r}_{2})\Psi_{R}(\boldsymbol{r}_{1})] \\ E_{S/T}=\int  d\mathbf{r}_{1} \,d\mathbf{r}_{2}\,\Psi_{S/T}^{*}(\mathbf{r}_{1},\mathbf{r}_{2})H\Psi_{S/T}(\mathbf{r}_{1},\mathbf{r}_{2})}$$

- Denote the [[#Interaction energy|Hartree and Exchange integrals]]
$$\begin{align}
U_{H}&=\int  d\boldsymbol{r}_{1} \,d\boldsymbol{r}_{2}\, \Psi_{L}^{*}(\boldsymbol{r}_{1})\Psi_{L}(\mathbf{r}_{1})g(\mathbf{r}_{1},\mathbf{r}_{2}) \Psi_{R}^{*}(\mathbf{r}_{2})\Psi_{R}(\mathbf{r}_{2}) >0\\ U_E
&=\int  d\boldsymbol{r}_{1} \,d\boldsymbol{r}_{2}\, \Psi_{R}^{*}(\boldsymbol{r}_{1})\Psi_{L}(\mathbf{r}_{1})g(\mathbf{r}_{1},\mathbf{r}_{2}) \Psi_{L}^{*}(\mathbf{r}_{2})\Psi_{R}(\mathbf{r}_{2}) 
\end{align}$$
- Also define:
$$\begin{align}
\Delta\varepsilon_{L}&=\int  d\boldsymbol{r}\,\Psi_{L}^{*}(\boldsymbol{r})V_{R}(\boldsymbol{r})\Psi_{L}(\boldsymbol{r})  \\
\Delta\varepsilon_{R}&=\int  d\boldsymbol{r}\,\Psi_{R}^{*}(\boldsymbol{r})V_{L}(\boldsymbol{r})\Psi_{R}(\boldsymbol{r})  \\
t&=\int  d\boldsymbol{r}\,\Psi_{L}^{*}(\boldsymbol{r}) \frac{p^{2}}{2m} \Psi_{R}(\boldsymbol{r}) 
\end{align}$$
- From this:
$$J\equiv E_{S}-E_{T}=\frac{2}{1-I^{4}}(U_{E}-2It-I^{2}(U_{H}-(\varepsilon_{L}+\varepsilon_{R})+\Delta\varepsilon_{L}+\Delta\varepsilon_{R}))$$
- Typical energy scale:
	- First inequality: Cauchy-Schwarz
	- Second inequality: integrand $\propto |\mathbf{r}_{1}-\mathbf{r}_{2}|^{-1}$
	- Third inequality: true for any system where $\Psi_{L/R}$ are _sufficiently complete single particle basis states_
$$U_{H}\gg U_{E}\gg\varepsilon_{L},\varepsilon_{R},t\gg\Delta\varepsilon_{L},\Delta\varepsilon_{R}$$
- Approximate:
$$J\equiv E_{S}-E_{T}\approx \frac{2}{1-I^{4}} (U_{E}-I^{2}U_{H})$$
- When the _exchange term is dominant_, the system favours the _triplet state_
- When the _Hartree term is dominant_ due to a _larger overlap_, the system favours the _singlet state_

### General lattice models


## Mean-field theory
- For a _ferromagnet_ $J>0$, with an _external field_ $B$, the _Heisenberg ferromagnet_ is:
$$H=-J\sum_{\langle i,j \rangle }\boldsymbol{S}_{i}\cdot \boldsymbol{S}_{j}-g\mu_{B}\sum_{i}\boldsymbol{S}_{i}\cdot \boldsymbol{B}$$
- _Effective molecular field_

- The _mean field_ Hamiltonian

- Partition function and _magnetisation_

- $B=0$: _spontaneous magnetisation_ 

## Measuring magnetic order
- _Neutron scattering_ is used to study magnetic materials

- _Thermal neutrons_ have $\lambda$ on the order of _atomic spacings_
- They _couple_ to _atomic magnetic moments_

## Magnons
- A _broken rotational symmetry_ of the Heisenberg Hamiltonian
- Leads to _gapless, low-energy collective excitations_

- See: [[Theories of Quantum Matter#Heisenberg ferromagnetic chain| Properties of the Heisenberg ferromagnetic chain]]
$$\omega(q)=J(1-\cos qa)$$
- It is _quadratic_ at low $q$

- As a magnon state _lowers_ spin by $1$, it is a _boson_ with _spin_ $1$

- A _generalisation_ to 3 dimensions:

### Bloch law
- The _magnon density of states_:
$$g(\omega)\,d\omega \propto \sqrt{ \omega }\,d\omega$$
- The _number of magnon excitations_, using the _Bose distribution_
$$n_\text{magonon}\propto T^{3/2}$$
- As magnons _reduce_ spin:
$$\frac{M(T)}{M(0)}=1-aT^{3/2}$$
- Similarly, for _magnon energy_:
$$E \propto T^{5/2} \qquad C_{V}\propto T^{3/2}$$

### Lower dimensions
- 1D and 2D: _infinitely many_ magnons
- They _destroy_ any magnetic ordering

## Magnetic interactions

### Direct coupling
- The _dipolar interaction energy_:
$$E_\text{int}\approx \mathcal{O}(1\text{ K})$$
- _Direct coupling_ is _too weak_ to explain _ferromagnetism_
	- Still affects _domain structure_

### Direct exchange
- Meanwhile, _direct exchange_ is only important when there is _sufficient wavefunction overlap_
	- In many materials, the $4f$ or $3d$ orbitals _do not extend sufficiently far_ from the nucleus to give exchange coupling

### Superexchange
- Consider the _anti-ferromagnetism_ of $\ce{ MnO }$
	- An $\ce{ NaCl }$ structure, with _little to no overlap_ between $\ce{ Mn^{2}+ }$ ions
	- The oxygen facilitates anti-ferromagnetism by _superexchange_

- Model it using a system of 2 $\ce{ Mn^{2+} }$ ions and one $\ce{ O ^{2-}}$ ion
- There are 4 electrons on 6 _spin-orbital sites_, therefore 15 basis states

- Consider the _basis of parallel_ $d$ spins:
![[Superexchange parallel.png]]
- The _off-diagonal_ elements give _possible hopping mechanisms_, with the _only one possible_ being:
![[Superexchange hoppinh.png]]
- For _antiparallel_ $d$ electrons, the hoppinh mechanisms:
![[Superexchange antiparalle.png]]

### Itinerant band ferromagnetism
- Consider _transition metals_ with _partially filled_ $d-$bands

- The _Hubbard interaction_

- Doing a _Fourier transform_:
$$H_\text{int}=\frac{U}{2N}\sum \sum$$
- Use _Wick's Theorem_

### RKKY Interaction
- _Coupling_ between _magnetic ions_, _mediated_ by a _sea of conductive electrons_

- The localised magnetic moments will _spin polarise_ the conduction electrons, which then _propagate_ the spin to other moments
- The effective interaction is _long range_
- The _sign_ of the exchange parameter _varies periodically with distance_
	- Periodicity due to _Friedel oscillations_

# Weak electron-photon interactions
- Use [[#Electronic response theory]] to look at _interactions_ between electrons and light

- At _low light intensities_, _photons_ can be used to _probe electronic properties_
	- Both _ground_ and _excited states_
	- In this regime, the photons can be considered to _not modify the states themselves_
- At _high intensities_, the electric field is sufficient to _change the quantum state_
	- Optical effects are _non-linear_

## Classical oscillator model
- The _Lorentz oscillator_ wih _damping_:
$$m^{*} \dots=eE(t)$$
- The _steady state_ with _oscillations_
$$y(\omega)=$$
- Polarisation and _susceptibility_

- Separate the dielectric constant into _real_ and _imaginary_ parts

### Optical properties
- The _complex refractive index_
$$n=\sqrt{ \varepsilon }$$
- The _reflection coefficient_

- For _intensity absorption_, _Beer's Law_:

### Relationships between properties
- Use the [[#Kramers-Kronig relations]]:


## Quantum mechanical response function
- There are responses based on if the field is _longitudinal_ or _transerse_

### Transverse field response
- Terms correspond to _absorption_ and _emission_
- Transition rates given by [[Time-dependent quantum mechanics#Fermi's Golden Rule|Fermi's Golden Rule]]

- The _power absorbed_ is then given by:
$$\begin{align}
P(\boldsymbol{q},\omega)&=
\end{align}$$
- Analagous to the derivation for the [[#Longitudinal response function for an electron gas]]

- Then use Kramers-Kronig

### Transverse dielectric response in semiconductors
- Apply the above formula to _Bloch states_

- Only take _vertical transitions_
- Bloch states _orthogonal_

- Sum over _conduction_ and _valence_ bands that _can contribute to vertical transitions_
- The _number of pairs_ which _fulfill_ this condition is given by the _joint density of states_ (JDOS):
$$J_{c\nu}(\omega)=$$
- Two _parabolic bands_: same as expression for _density of states_ in $3D$

- _Critical points_ are where the bands are _parallel_,  leading to _van Hove singularities_ in the JDOS
- The _band separation energy_ can then be written _parabolically_
$$E_{b}(\boldsymbol{k})=$$

- In $3\text{D}$, there are 4 types of critical points based on the _sign_ of the coefficients
![[van Hove singularity.png]]
- The nature of the _singularities_ give the nature of the _critical points_
	- Example: $\ce{ Ge }$
![[Ge spectrum.png|400]]
### Indirect band gap semiconductors
- In $\ce{ Si }$ and $\ce{ Ge }$, there are _indirect band gaps_, where _phonons_ are required to _conserve momentum_

# Excitons

## Wannier model
- The exciton can be described with a _hydrogenic model_


## Potential Bose-Einstein condensation
- There is a _critical temperature_ for Bose-Einstein condensation
$$T_{c} \propto \frac{1}{m}n^{2/3}$$
- For a BEC in an electronic system, _exciton lifetime_ must be _longer_ than the _time taken to reach thermodynamic equilibrium_
	- Equilibrium after _generation_ using lasers
	- Thermalisation typically takes _picoseconds_, around exciton lifetime

- Example: $\ce{ Cu_{2}O }$ has an excitonic BEC due to _symmetry forbidden transitions_ resulting in _long lifetimes_

## Polaritons
- A _superposition_ of a _photon_ and an _exciton_
- Band structure:
	- _Exciton-like_
	- _Photon-like_

# Electron-phonon interactions

## Phonons in crystals
- Let _ions_ of mass $M$ in the lattice have _equilibrium positions_ $\{\boldsymbol{R}_{n}\}$
- They are _displaced_ by vector $\{s_{n}(t)\}$

- The _potential energy_ due to the ion lattice:
	- The _first order_ term _vanishes in equilibrium_
	- $D$ includes _direct interactions_, as well as _self-consistent changes_ in _electron density_
$$U_\text{harm}=\frac{1}{2}\sum_{n,m=1}^{N}\boldsymbol{s}_{n}\cdot D(\boldsymbol{R}_n-\boldsymbol{R}_{m})\cdot \boldsymbol{s}_{m}$$
- With $\boldsymbol{P}_{n}$, the _conjugate momentum_ to $\boldsymbol{s}_{n}$
$$\displaylines{H=\sum_{n=1}^{N}\frac{P_{n}^{2}}{2M}+\frac{1}{2}\sum_{n,m=1}^{N}\boldsymbol{s}_{n}\cdot D(\boldsymbol{R}_n-\boldsymbol{R}_{m})\cdot \boldsymbol{s}_{m} \\ [s_{n}^{i},P_{m}^{j}]=i\hbar\delta_{nm}\delta_{ij}}$$

- The matrices $D$ follow:
$$D(\boldsymbol{R})=D(-\boldsymbol{R}) \qquad \sum_{\boldsymbol{R}}D(\boldsymbol{R})=0$$
- This can be written in terms of _second quantisation_
### Many-phonon Hamiltonian
- For a _single-particle_ Hamiltonian:
$$\displaylines{a=\sqrt{ \frac{M\omega}{2\hbar} }s+i\sqrt{ \frac{1}{2\hbar M\omega} }P \qquad a^{\dagger}=\sqrt{ \frac{M\omega}{2\hbar} }s-i\sqrt{ \frac{1}{2\hbar M\omega} }P \\ [a,a^{\dagger}]=1 \qquad [a,a]=[a^{\dagger},a^{\dagger}]=0}$$

- For the _crystal Hamiltonian_, use the ansatz:
$$\displaylines{a_{\boldsymbol{q},\nu}=\frac{1}{\sqrt{ N }}\sum_{n=1}^{N}e^{-i\boldsymbol{q}\cdot \boldsymbol{R}_{n}} \,\boldsymbol{\varepsilon}_{\nu}(\boldsymbol{q})\cdot\left( \sqrt{ \frac{M\omega_{\nu}(\boldsymbol{q})}{2\hbar}}\boldsymbol{s}_{n}+i\sqrt{ \frac{1}{2\hbar M\omega_{\nu}(\boldsymbol{q})} }\boldsymbol{P}_{n} \right) \\ a_{\boldsymbol{q},\nu}^{\dagger}=\frac{1}{\sqrt{ N }}\sum_{n=1}^{N}e^{i\boldsymbol{q}\cdot \boldsymbol{R}_{n}} \,\boldsymbol{\varepsilon}_{\nu}(\boldsymbol{q})\cdot\left( \sqrt{ \frac{M\omega_{\nu}(\boldsymbol{q})}{2\hbar}}\boldsymbol{s}_{n}-i\sqrt{ \frac{1}{2\hbar M\omega_{\nu}(\boldsymbol{q})} }\boldsymbol{P}_{n} \right)}$$
- Here, $\boldsymbol{\varepsilon}_{\nu}(\boldsymbol{q})$ is a set of _orthonormal_, _normal mode polarisation vectors_
- They each have a _corresponding_ normal mode frequency $\omega_{\nu}(\boldsymbol{q})$

- $\boldsymbol{\varepsilon}_{\nu}(\boldsymbol{q})$ and $\omega_{\nu}(\boldsymbol{q})$ are determined from the _equation of motion_, with a _harmonic ansatz_
$$\displaylines{M \ddot{\boldsymbol{s}}_{n}=-\sum_{m}D(\boldsymbol{R}_{n}-\boldsymbol{R}_{m})\cdot \boldsymbol{s}_{m} \\ \boldsymbol{s}_{n}(\boldsymbol{R}_{n},t)=\boldsymbol{\varepsilon}(\boldsymbol{q})\exp[i(\boldsymbol{q}\cdot \boldsymbol{R}_{n}-\omega t)] \\ \tilde{D}(\boldsymbol{q})\boldsymbol{\varepsilon}_{\nu}(\boldsymbol{q})=M\omega_{\nu}^{2}(\boldsymbol{q})\boldsymbol{\varepsilon}_{\nu}(\boldsymbol{q})}$$
- Here, $\tilde{D}(\boldsymbol{q})$ is the _dynamical matrix_, a _real, symmetric, positive-definite_ $3\times3$ matrix
$$\tilde{D}(\boldsymbol{q})=\sum_{n=1}^{N}D(\boldsymbol{R}_{n})\exp(-i\boldsymbol{q}\cdot \boldsymbol{R}_{n})$$
- From the properties of the matrix:
$$\boldsymbol{\varepsilon}_{\mu}(\boldsymbol{q})\cdot \boldsymbol{\varepsilon}_{\nu}(\boldsymbol{q})=\delta_{\mu \nu} \qquad \omega_{\nu}^{2}(\boldsymbol{q})>0$$

- From the orthonormality of $\boldsymbol{\varepsilon}_{\nu}(\boldsymbol{q})$ and the position-momentum conjugation:
$$[a_{\boldsymbol{q},\nu},a^{\dagger}_{\boldsymbol{q}',\nu'}]=\delta_{\boldsymbol{q}\boldsymbol{q}'}\delta_{\nu \nu'} \qquad [a_{\boldsymbol{q},\nu},a_{\boldsymbol{q}'\nu'}]=[a_{\boldsymbol{q},\nu}^{\dagger},a_{\boldsymbol{q}'\nu'}^{\dagger}]=0$$
- From this, one gets the _many-phonon Hamiltonian_:
$$H=\sum_{\boldsymbol{q}\in \text{BZ}  }\sum_{\nu=1}^{3}\hbar\omega_{\nu}(\boldsymbol{q})\left( a^{\dagger}_{\boldsymbol{q}\nu}a_{\boldsymbol{q}\nu}+\frac{1}{2} \right)$$
- It represents $3N$ _independent, separate harmonic oscillators_, one for _each_ $\boldsymbol{q}$ in the BZ, with _one of three polarisations_ $\nu$
$$E=\sum_{\boldsymbol{q},\nu}\hbar\omega_{\nu}(\boldsymbol{q})\left( n_{\boldsymbol{q}\nu}+\frac{1}{2} \right)$$
### Phonon branches
- From the _symmetry_ of $D(\boldsymbol{R})$, for a _monoatomic Bravais lattice_:
$$\tilde{D}(\boldsymbol{q})=-2\sum_{n=1}^{N}\sin^{2}\left( \frac{1}{2}\boldsymbol{q}\cdot \boldsymbol{R}_{n} \right)D(\boldsymbol{R}_{n})$$
- For _small_ $\boldsymbol{q}$:
$$\tilde{D}(\boldsymbol{q})\approx -\frac{q^{2}}{2}\sum_{n=1}^{N}\left( \hat{\boldsymbol{q}}\cdot \boldsymbol{R}_{n} \right)^{2}D(\boldsymbol{R}_{n})$$
- Then, from the eigenvalue equation, _all branches for a monoatomic crystal are acoustic_
$$\lim_{ \boldsymbol{q} \to 0 }\omega_{\nu}(\boldsymbol{q})\to c_{\nu}\left( \hat{\boldsymbol{q}} \right)q $$
- At _high-symmetry points_, 2 branches are _transverse_ $\boldsymbol{q}\perp \boldsymbol{\varepsilon}_{\nu}(\boldsymbol{q})$ with one _longitudinal_ branch
- For _arbitrary_ $\boldsymbol{q}$, this classification is _not possible_

- For a Bravais lattice with a $p-$atom basis, there are $3p$ _modes for each_ $\boldsymbol{q}$
- There are 3 _acoustic_ branches, corresponding to _translational_ degrees of freedom in a $p-$atomic molecule
- There are then $3(p-1)$ _optical branches_, corresponding to _vibrational_ degrees of freedom in a $p-$atomic molecule
$$\lim_{ \boldsymbol{q} \to 0 } \omega_{\nu}(\boldsymbol{q})>0$$

- In _acoustic modes_ for $q\approx0$, adjacent atoms move _in-phase_
![[Acoustic optical modes.png]]
- In _optical modes_ for $q\approx0$, adjacent atoms move _out-of-phase_
- A _dipole moment_ is then generated, which can _couple_ to _photons_
- _Optical absorption_ can then lead to the _generation of optical phonons_

- Dispersion relations can be measured by _neutron scattering_

- _All phonons_ will contribute to _specific heat_:
	- At $T\to 0$, _Debye's law_ is obeyed as $C_{V}\propto T^{3}$
$$C_{V}=\frac{\partial}{\partial T} \sum_{\nu} \int_\text{BZ}  \frac{d^{3}\boldsymbol{k}}{(2\pi)^{3}} \frac{\hbar\omega_{\nu}(\boldsymbol{k})}{\exp[\hbar\omega_{\nu}(\boldsymbol{k})/k_{B}T]-1} $$

- The _Debye temperature_ is defined in terms of the _highest frequency phonon mode_ $\omega_{D}$
$$\hbar\omega_{D}=k_{B}\Theta_{D}$$
## Manifestation of e-ph interactions
### Resistivity
- _Resistivity_ is commonly caused by the e-ph interaction
	- At _extremely low_ temperatures, scattering is dominated by _impurities_ and becomes temperature-independent
- _Temperature dependence_ of e-ph scattering is typically:
$$\begin{align} \rho(T\gg\Theta_{D})&\propto T \\ \rho(T\ll\Theta_{D})&=\rho_{0}(1+AT^{5}+\dots)
\end{align}$$

- e-ph scattering contributes to _relaxation processes_ that bring the crystal to _equilibrium_
- There is an associated _relaxation time_

### Conventional superconductivity
- Phonons _mediate_ an _effective attractive force_ between _electron pairs_, within a _Debye energy from the Fermi surface_
$$H'=\sum_{\boldsymbol{k},\boldsymbol{k}',\boldsymbol{q}}|M_{q}|^{2} \frac{\hbar\omega_{\boldsymbol{q}}}{(\varepsilon_{\boldsymbol{k}}-\varepsilon_{\boldsymbol{k}+\boldsymbol{q}})^{2}-(\hbar\omega_{\boldsymbol{q}}^{2})}c^{\dagger}_{\boldsymbol{k}'+\boldsymbol{q}}c^{\dagger}_{\boldsymbol{k}-\boldsymbol{q}}c_{\boldsymbol{k}}c_{\boldsymbol{k}'}$$
- This causes _Cooper pair formation_
- The attractive force comes from a _second order process_ as a phonon is _emitted_ then _absorbed_
### Polarons
- Quasiparticle formed by an _electron_ plus its _polarisation cloud_

- There are _large_ and _small polarons_ depending on the _extent_ of the _lattice distortion_
	- _Large_ if the region of _nuclear distortion_ is _large compared to the lattice constant_
![[Polaron.png|300]]
- Example of small polaron: _charge motion_ in a _conjugated polymer_, as the ring monomers go through _simple harmonic motion_
	- At _low temperatures_, the polymer is quasi-adiabatic as the polaron diffuses down the chain without activation energy
	- At _high temperatures_, there is an additional _activated transfer process_ corresponding to hopping between states
## e-ph Hamiltonian
- The electron-phonon interaction originates from:
	- Form for a _monoatomic Bravais lattice_
	- The ion positions can be _time-dependent_ due to the phonon excitations
$$H_\text{e-ion}=\sum_{m=1}^{N}\sum_{n=1}^{N}V_\text{ion}(\boldsymbol{r}_{m}-\boldsymbol{R}_{n}(t))=-\sum_{m=1}^{N}\sum_{n=1}^{N}\frac{Ze^{2}}{4\pi\epsilon_{0}|\boldsymbol{r}_{m}-\boldsymbol{R}_{n}|}$$
- Expand the potential around the _equilibrium positions_ $\boldsymbol{R}_{n}$
$$\displaylines{\boldsymbol{R}_{n}(t)=\boldsymbol{R}_{n}+\boldsymbol{s}_{n}(t) \\ H_\text{e-ion}=\sum_{m=1}^{N}\sum_{n=1}^{N}V_\text{ion}(\boldsymbol{r}_{m}-\boldsymbol{R}_{n})-\boldsymbol{s}_{n}(t)\cdot \nabla_{\boldsymbol{R}_{n}}V_\text{ion}(\boldsymbol{r}_{m}-\boldsymbol{R}_{n})}$$

- Take the _rigid ion model_, where $V_\text{ion}$ _only_ depends on distance between the _electron_ and the _centre_ of the ion, such that vibrations _shift each ion rigidly_ and _do not change the form of the potential_
- The _stationary part_ of the potential determines the _ground state properties_ (without phonons)

### Form of interaction Hamiltonian
- Express $\boldsymbol{s}_{n}$ in terms of the _creation and annihilation operators_:
$$\boldsymbol{s}_{n}=\frac{1}{\sqrt{ N }}\sum_{\boldsymbol{q},\nu}\sqrt{ \frac{\hbar}{2M\omega_{\nu}(\boldsymbol{q})} }(a_{\boldsymbol{q}\nu}+a^{\dagger}_{-\boldsymbol{q}\nu})e^{i\boldsymbol{q}\cdot \boldsymbol{R}_{n}}\boldsymbol{\varepsilon}_{\nu}(\boldsymbol{q})$$
- The _interaction Hamiltonian_ is then:
$$H_\text{e-ph}=\sum_{m=1}^{N} \sum_{n=1}^{N}\sum_{\boldsymbol{q},\nu}\frac{1}{\sqrt{ N }} \sqrt{ \frac{\hbar}{2M\omega_{\nu}(\boldsymbol{q})} } (a_{\boldsymbol{q}\nu}+a^{\dagger}_{-\boldsymbol{q}\nu}) e^{i\boldsymbol{q}\cdot \boldsymbol{R}_{n}} \boldsymbol{\varepsilon}_{\nu}(\boldsymbol{q})\cdot \nabla V_\text{ion}(\boldsymbol{r}_{m}-\boldsymbol{R}_{n})$$
- This is a _sum of single-electron Hamiltonians_

- One can then put it into _second quantised form_ using _plane wave states_:
	- Assuming the interaction Hamiltonian is _sufficiently weak_ that there is _no scattering between bands_
$$\displaylines{H_\text{e-ph}=\sum_{\boldsymbol{k},\boldsymbol{k}',\lambda}\sum_{\boldsymbol{q},\nu}M_{\boldsymbol{q}\nu}(\boldsymbol{k},\boldsymbol{k}')(a_{\boldsymbol{q}\nu}+a_{-\boldsymbol{q}\nu}^{\dagger})c^{\dagger}_{\boldsymbol{k}',\lambda}c_{\boldsymbol{k},\lambda} \\ M_{\boldsymbol{q}\nu}(\boldsymbol{k},\boldsymbol{k}')=\frac{1}{\sqrt{ N }}\sqrt{\frac{\hbar}{2M\omega_{\nu}(\boldsymbol{q})}  }e^{i\boldsymbol{q}\cdot \boldsymbol{R}_{n}}\boldsymbol{\varepsilon}_{\nu}(\boldsymbol{q})\cdot \braket{ \boldsymbol{k}'|\nabla V_\text{ion}(\boldsymbol{r}_{m}-\boldsymbol{R}_{n}) |\boldsymbol{k}  } }$$

### Form of e-ph matrix element
- Introduce the _atomic form factor_ associated with the potential

### Physical interpretation
- Both _normal_ and _Umklapp scattering_

## Boltzmann theory
- Theory of _electron transport_ accounting for _impurity scattering_ and _e-ph interaction_

- A _semiclassical theory_, treating the _distribution function_ as a function of _three variables_
	- In quantum mechanics, $\boldsymbol{r}$ and $\boldsymbol{k}$ are _conjugate variables_
$$f=f(\boldsymbol{r},\boldsymbol{k},t)$$
- Describes _semi-classical wave packets_


- From _Liouville's Theorem_, the classical distribution function obeys:
$$\frac{df}{dt}=0$$
- However, _collisions_ can change the total number of particles, therefore the _Boltzmann equation_ gives:
$$\frac{df}{dt}=\frac{\partial f}{\partial t}+\frac{d\boldsymbol{k}}{dt}\cdot \nabla_{k}f+\frac{d\boldsymbol{r}}{dt}\cdot \nabla_{r}f=\frac{\partial f}{\partial t}\Bigg|_\text{coll}$$
- From $f$, one then gets the _transport properties_

### Relaxation time approximation

### AC response of a metal

- Only contributions from _within_ $k_{B}T$ of the _Fermi surface_

### Scattering from a static potential

### Scattering from a charge
## Phonon mediation of e-e interactions
- The e-ph interaction results in _scattering of electrons_ via phonon emission or absorption
- There are also _second order_ processes involving a phonon being _emitted_ by one electron before being _absorbed by another_ electron

- A _canonical transformation_ of the Frochlich Hamiltonian to _eliminate first order terms_
# Quantum Transport
- [[#Boltzmann theory]] is _semi-classical_, which also _does not take phase coherence into account_

- _Quantum transport theory_ applies to _phase-coherent quantum systems_
	- Effects are more apparent in _low-dimensional, low-temperature systems_
- A _linear response_ approach

## Lower dimensional electron systems
- Typically, a three-dimensional _conduction band_ forms an energy minimum, around which the dispersion is approximated as:
	- Example: $\ce{ GaAs }$ has a parabolic band structure around $\Gamma$
$$E_{\boldsymbol{k}}=\frac{\hbar^{2}}{2}\sum_{i,j=1}^{3}\boldsymbol{k}_{i}(m^{*})^{-1}_{i,j}\boldsymbol{k}_{j}$$
- One can also _artifically make_ lower dimensional band structures

### Manufacturing a 2D Electron gas
- One can construct _two-dimensional electron gases_ via MBE:
![[2dEG production.png]]
- The _difference in charge_ causes _band bending_, which forms an [[Solids#Inversion layer formation|inversion layer]], where the electrons are _confined_ to form a 2DEG
![[2DEG inversion.png|500]]

- One can _adjust_ the 2D carrier density by applying a _potential_ $V_{g}$ to a _surface Schottky gate_
![[2DEG Schottky gate.png]]
$$\Delta Q=-e\Delta n=C\Delta V_{g}$$

- By more finely manipulating the Schottky gate, one can create an _arbitrary 2D effective potential_, such that the electrons are governed by:
$$\frac{1}{2m^{*}}(\boldsymbol{p}+e\boldsymbol{A})^{2}\Phi+V(x,y)\Phi=i\hbar \frac{\partial \Phi}{\partial t}$$

### Quasi-1D electron gas
![[1DEG.png|300]]
- By using a _split gate_, one can also make a _quasi-one dimensional system_
$$\left( \frac{p^{2}}{2m^{*}}+V(y) \right)\Phi_{kn}(x,y)=E_{kn}(x,y)$$
- The system is _separable_ as long as the system is _translationally invariant along_ $x$
$$\displaylines{\Phi_{nk}(x,y)=\exp(ikx)\phi_{n}(y) \\ \left( \frac{p_{y}^{2}}{2m^{*}}+V(y) \right)\phi_{n}(y)=\left( E_{nk}-\frac{\hbar^{2}k^{2}}{2m} \right)\phi_{}(y)=E_{n}\phi_{n}(y)}$$
- $\phi_{n}(y)$ is the _sub-band wave function_, while $E_{n}$ is the _sub-band energy_
	- In general, $\phi_{n}$ is _not_ a function of $k$ (with the exception of the $B-$field, see below)
	- In the $z$ direction, the electorn is still _trapped_ in the _lowest energy heterojunction sub-band_
- Each _sub-band_ has the _dispersion_ of a _discrete energy_ with a _free electron dispersion_

- Example: an _effective harmonic potential_
$$E_{n,k}=\hbar\omega\left( n+\frac{1}{2} \right)+\frac{\hbar^{2}k^{2}}{2m}$$

### 1DEG in a magnetic field and edge states
- Or, take the case of a _magnetic field_ $\boldsymbol{B}=(0,0,B)$
$$\left( \frac{(p+e\boldsymbol{A})^{2}}{2m^{*}}+V(y) \right)\Phi_{kn}(x,y)=E_{kn}(x,y)$$
- Take the _Landau gauge_ such that the system is still _separable_, and:
$$\left( \frac{p_{y}^{2}}{2m^{*}}+\frac{1}{2}m^{*}\omega_{c}^{2}\left( y-\frac{\hbar k}{eB} \right)^{2}+V(y) \right)\phi_{n,k}(y)=E_{nk}\phi_{nk}(y)$$
- Here, $\omega_{c}$ is the _cyclotron frequency_ $eB/m$

- This makes a _momentum-dependent parabolic potential_ in addition to the effective potential. representing the result of the _Lorentz force_ due to electrons in the $x-$direction
$$F=-e\left( \frac{\hbar k}{m}\hat{x} \times \boldsymbol{B}\right)=\omega_{c}p\hat{y}$$
- As $B$ increases, the states become _more localised against the walls_ of the 1D system, and become _edge states_

### Conductance of a 1D system


## Landauer formalism
- Conductance of a _general 2D quantum system_ with an _effective potential_ $V(x,y)$
- Consider the system _sandwiched between two infinite quasi-1D systems_, which act as _conducting leads for particles_

# Superconductivity

## BCS Theory
- Electron-phonon mediated

- No matter how _weak_ the electron-phonon interaction is, a _bound state_ can be formed