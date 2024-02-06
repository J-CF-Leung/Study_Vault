- _Cohesion_ in a medium is due to _interactions_ between _electrons and nuclei_, such that there is an _effective potential_ for movement of _atoms_

# Bonding mechanisms
- Bonding potential depends on the _electron configurations_ of the constituent atoms

## van der Waals
- Typical in _inert gases_
	- With _filled electron shells_, leading to _large ionisation energies_
- Between _neutral atoms_, which give _weak interactions_

- Apart from $\ce{ He }$, inert gases form _close-packed face-centred cubic solids_

### Force between induced dipoles
- Consider an atom as an _oscillator_, as electrons _fluctuate_ around the _nucleus_
- Fluctuations give a _dipole moment_ $p_{1}$, which causes an _electric field_:
$$E_{1} \propto \frac{p_{1}}{R^{3}}$$
- This then _induces_ a dipole on the second atom (with _polarisability_ $\alpha$):
$$p_{2} \propto \frac{\alpha p_{1}}{R^{3}}$$
- This then _induces_ another electric field at the first atom:
$$E_{1} \propto \frac{p_{2}}{R^{3}}\propto \frac{\alpha p_{1}}{R^{6}}$$
- The _energy_ of the system changes by:
$$\Delta U=-\langle \boldsymbol{p_{1}}\cdot \boldsymbol{E}_{1} \rangle\propto -\frac{\alpha \left<p_{1}^{2}\right>}{R^{6}} $$
- The force is always _attractive_
	- $\left<p_{1}\right>^{2}=0$, and $\left<p_{1}^{2}\right>\neq 0$

### Overall potential
- If the _electron charge distributions_ of atoms _overlap_, they start to _repel_ each other
	- Contributions from _electrostatic_ forces, and _Pauli exclusion_
- This gives a _short range potential_
- The _Lennard-Jones_ potential:
	- Purely _empirical_
$$V(r)=4\varepsilon\left[ \left( \frac{\sigma}{r} \right)^{12}-\left( \frac{\sigma}{r} \right)^{6} \right]=\epsilon\left[ \left( \frac{R_\text{min}}{r} \right)^{12}-2\left( \frac{R_\text{min}}{r} \right)^{6} \right]$$
![[Lennard-Jones potential.png|400]]
- $\sigma$ and $\varepsilon$ are parameters _depending on the atoms_

- _Layers_ of 2D materials are also held together by van der Waals forces:
![[2D materials.png]]
## Ionic bonding
- For atoms with _electronic configuration close to a filled shell_, they will _gain or lose electrons_ to have a filled shell

- An atom with _excess electrons_ will _ionise_ with _ionisation energy_ $I$ in the _gas phase_:
$$\ce{ M } \xrightarrow{I} \ce{ M+ +e- }$$
- An atom with _insufficient electrons_ can _gain_ an electron with _electron affinity_ $A$:
$$\ce{ X +e- }\xrightarrow{A}\ce{ X- }$$

- An _ionic structure_ forms if the _electrostatic binding energy_ is _stronger_ than the _energetic cost_ $I+A$
- The binding energy as the _sum of pair Coulomb interactions_:
$$U=\frac{1}{2}\sum_{i}\sum_{j\neq i}U_{ij}=\frac{1}{2}\sum_{i}\sum_{i\neq j} \frac{1}{4\pi\epsilon_{0}} \frac{\pm_{ij}q^{2}}{R_{ij}}$$
- Depending on the nature of $i$ and $j$, the interaction can be _attractive_ or _repulsive_

- For a _regular lattice_ with some constant $R$:
$$U=-\frac{\alpha_{M}q^{2}}{4\pi\epsilon_{0}R}$$
- Here, $\alpha_{M}$ is the _Madelung constant_, which is _dependent on the structure_

- One must also account for a _short range repulsive force_
	- Influenced by the _size of ions_

- Most ionic structures have _coordination number_ around $6-8$

## Covalent bonding
- A _covalent bond_ is an _electron pair_ which _hold atoms together_
- The _overlapping orbitals_ on neighbouring atoms _hybridise_ to form new orbitals
- The overall Hamiltonian must be _symmetric_ about the point _between equivalent nuclei_, hence eigenstates must have _odd or even parity_ about that point

### Hydrogen molecule
- The _toy model_ is the _hydrogen molecule_
- With a _basis_ of atomic states $\phi(\boldsymbol{r}-\boldsymbol{R})$, where the _nucleus_ is at $\boldsymbol{R}$, one gets two states, of _even_ and _odd_ parity:
$$\psi_{\pm}(r)=\phi(\boldsymbol{r}-\boldsymbol{R}_{a})\pm \phi(\boldsymbol{r}-\boldsymbol{R}_{b})$$
- $\psi_{+}$ is _non-zero_ between the nuclei, while $\psi_{-}$ has a _node_ there

- For an _attractive potential_, $E_{+}<E_{-}$ and two electrons of _opposite spin_ occupy the _lower (bonding) state_ $\psi_{+}$
- The _antibonding state_ is separated from the bonding state by $E_{g}=E_{-}-E_{+}$ and becomes _unfilled_
![[Hydrogen atom states.png]]

### Calculation of energies
- _Ignores electron repulsion_ and _spin effects_
	- Effectively the [[Atomic and molecular physics#The H2+ ion|H2+ ion]]
	- With repulsion and spin, [[Atomic and molecular physics#The H2 molecule|numerical methods]] are required 

- Denote the states by:
$$\ket{a}=\phi(\boldsymbol{r}-\boldsymbol{R}_{a}) \hspace{1.5cm}\ket{b}=\phi(\boldsymbol{r}-\boldsymbol{R}_{b})  $$
- Find energy eigenfunctions in the subspace _spanned_ by basis functions:
	- Assume that they are _orthonormal_
$$\ket{\psi}=\alpha \ket{a}+\beta \ket{b}   $$
- By taking the inner product with $\braket{ a}$ and $\bra{b}$, and denoting the matrix elements of the _Hamiltonian_ as $H_{aa}, H_{bb}, H_{ab}, H_{ba}=H_{ab}^{*}$
$\begin{vmatrix}H_{aa}-E&H_{ab} \\ H_{ab}^{*}&H_{bb}-E\end{vmatrix}=0$

- The _energy eigenvalues_:
$$\displaylines{E=\frac{H_{aa}+H_{bb}}{2}\pm \frac{\Delta E}{2} \\ \frac{\Delta E}{2}=\sqrt{ \left( \frac{H_{aa}-H_{bb}}{2} \right)^{2}+ | H_{ab}|^{2}  }}$$
- If $H_{aa}\approx H_{bb}$, then $\Delta E/2=|H_{ab}|$, and there is _covalent bonding_

- If $H_{aa}\gg H_{bb}$ or vice versa, $E=H_{aa}$ or $H_{bb}$, and $H_{ab}$ is _irrelevant_, giving _ionic bonding_
	- The electrons are _localised_

## Covalent and ionic semiconductors
- With the $s$ electrons, _molecules_ are formed first to then give a _weakly (covalently) bound molecular solid_
	- $s$ orbitals are _spherical_
- With $p$ and $d$ electrons, bonds are _directional_
	- Example: $sp^{3}$ in carbon gives _tetrahedral bonding_, as the hybrids point along $(111),(\bar{1}\bar{1}1),(\bar{1}1\bar{1}),(1\bar{1}\bar{1})$

- _Binary compounds_: GaAs and ZnS
- _Zinc blende_ structure: tetrahedral with alternating atoms
- Partly ionic, partly covalent

- Hexagonal structure with ocal tetrahedral network: _wurtzite_

## Metals
- _Bands_ form from _atomic orbitals_
- They are typically _partially filled_ and _lowers_ energy in general
	- A _generalisation_ of the covalent bond to a _giant structure_
	- It is _isotropic_, like the van der Waals force
![[Covalent vs metallic.png]]
- Electrons are _delocalised_ to minimise kinetic energy
	- Gives _high conductivity_

- Atoms are _close packed_ to _maximise_ electron wave-function overlap while also _reducing Coulomb repulsion_ by keeping the _atomic cores_ far apart
	- Closed packed structures: _hexagonal_ close packing or _face-centred cubic_
	- Giving _high coordination numbers_ $\approx 10-12$

- [[Classical and semiclassical models#Electrostatic screening|Screening]] by conduction electrons have order of $\approx 1\text{ Å}$

- Within a _row_ in the periodic table, as the _ion core potential_ grows and _density_ increases, structures _cross over_ to covalent semiconductors, then _insulating_ molecular structures
- For _transition metals_, $d$ electrons are more localised, and give _spin polarised_ materials, leading to _magnetism_

# Lattices
- An _ideal crystal_ consists of an _infinite repetition_ of some structural _unit_ in _space_
- The _repeating structure_ is known as the _lattice_

- The _group_ of atoms repeated is the _basis_
	- Can be a _single atom_, or some _group_ of atoms, or some _polymer_

- A lattice is defined by the _primitive translation vectors_ $\boldsymbol{a}_{i}, i=1,2,3$
- Form an arbitrary _lattice translation_:
$$\boldsymbol{T}=\sum$$
 - The _atomic arrangement_ looks the _same_ from _equivalent points_ in the crystal:
$$\boldsymbol{r}_{i}$$

- Bravais lattice
- Unit cell

- The _Wigner-Seitz cell_ is the _region in real space_ around some _lattice point_, which is _closer to that point than any other lattice point_
	- _Smallest volume_ enclosed by _perpendicular bisectors_ to all other neighbours

- The _first Brillouin zone_ is the _Wigner-Seitz cell_ of the _reciprocal lattice_

- The _symmetry operations_ that map a lattice _onto itself_ form a _space group_
- Symmetry operations that _keeps one point fixed_ give a _point group_
	- Reflections, inversions, rotations
- There are _seven point groups, and 14 space groups_ for Bravais lattices

- General crystal structure

## Crystal planes
- _Planes_ are labelled by the _coordinates where it cut the axes_:
$$\{\boldsymbol{r}_{i}\}=$$
- $(hkl)$ denotes planes that _cut_ the axes at
- Therefore, $xh=yk=zl=$
- A _zero_ indicates that the plane is _parallel_ to that axis

- $(hkl)$ is known as the _index_ of the plane
- A _set_ of planes equivalent _by symmetry_ are denoted by $\{hkl\}$
	- Example: $\{100\}$ for a cubic crystal has planes $(100),(010),(001),(\bar{1}00),(0\bar{1}0),(00\bar{1})$

# The reciprocal lattice
- Arises from the _scattering_ of waves by crystals
	- _Generalise_ Fraunhofer diffraction from a grating
- Consider the scattering of a _plane wave_ off a _basis_

- The _incoming wave_ $\boldsymbol{k}_{0}$ incident on a _potential_ centred on $\boldsymbol{R}_{i}$
- For _large distances_, the scattered wave is _circular_
- The _scalar field_:
$$\psi \propto \exp[i\boldsymbol{k}_{0}\cdot(\boldsymbol{r}-\boldsymbol{R}_{i})]+cf_{0} \frac{\exp[ik_{0}|\boldsymbol{r}-\boldsymbol{R}_{i}]}{}$$
- The _angular dependence_ from the _basis_ is determined by the _form factor_ $f_{0}$
	- Depends on scattering _angle_, type of atom, and their arrangement
- The _total scattered intensity_ determined by $c$ is assumed _small_

- At a _large distance_ from the scattering centre:
$$k_{0}\left| \boldsymbol{r}- \right| $$
- Here, $\boldsymbol{k}$ is the _scattered wave-vector_ $\boldsymbol{k}\equiv k_{0}\boldsymbol{r}/r$
- The _momentum transferred_ is $\boldsymbol{q}=\boldsymbol{k}-\boldsymbol{k}_{0}$
- The wave-form is then:
$$\psi \propto \exp[-i]\left[  \right]  $$
- The _effective scattering amplitude_ is:
$$f(\theta)=$$
- _Sum over all identical lattice sites_ gives the _scattering amplitude of the lattice_
	- _Multiply_ each term by the _phase of the incoming wave_ $\exp$
	- _Cancels out_ the pre-factor
- The [[Scattering#Differential cross-section|differential cross-section]]:
$$\frac{d\sigma}{d\Omega}=|f(\theta)|^{2}=$$
- The addition _cancels out all phases_, unless the _Bragg condition_ is satisfied:
$$\boldsymbol{q}\cdot \boldsymbol{R}_{i}=2\pi m_{i}$$
- In this case, all the scattered waves _constructively interfere_

- The vectors $\boldsymbol{q}\equiv\boldsymbol{G}$ satisfying this condition form a _reciprocal lattice_
	- A _linear combination_ leads to another vector satisfying the Bragg condition

- The _primitive vectors_ of the reciprocal lattice, in terms of _real space_ lattice vectors:
$$\boldsymbol{b}_{1}=$$

