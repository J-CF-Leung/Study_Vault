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
- Then applying the _independent electron approximation_, the last term

- Bloch's Theorem

- Crystal momentum

- Bands
- Electron filling
- Types of materials

## Breakdown of approximation
- Experimental evidence
	- _Hund's rule_ results from repulsive interaction between electrons
	- _Magnetism_ results from coupling of electrons and parallel spins
	- _Plasmons_ are collective _longitudinal electron density fluctuations_
	- _Friedel oscillations_ from screening of charges
	- _Heavy fermions_ in Fermi liquids
	- _One dimensional_ systems with interacting fermions form _Luttinger liquids_

# Hartree-Fock Theory
- In _general_, the electron wave-function is a _super-position of product states_

- In the _Hartree-Fock_ approximation, _assume_ the ground state is a single _Slater determinant_

- Then, use _variational calculus_ to find the _best fit spin-orbital wave functions_, by _minimising_ the estimated ground state energy

## The ground state energy

### Single particle energy


### Interaction energy
- Split into the _Hartree energy_ and the _exchange energy_