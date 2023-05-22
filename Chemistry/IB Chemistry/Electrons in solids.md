- The _behaviour of electrons_ in a solid depends on the _structure of the solid_
- An accurate description requires _quantum mechanics_, where the _potential_ depends on the atoms themselves, and the structure

- The _simplest_ model is the _free electron gas_, applicable to metals
- For _semi-conductors_, one requires the _tight-binding model_, which is similar to [[Bonding in molecules|MO theory]]

# Crystal structures
- Crystals have _long-range translational order_
- After a translation in a _particular direction_ for some distance, _identical features_ are seen

## Bravais lattices
- Crystals are described in terms of _Bravais lattices_
- They are a _set of lattice points_ which are _translationally periodic_
- All lattice points are _indistringuishable_

- Each lattice point is _not necessarily where atoms are_
- Instead, every lattice point is associated with a _motif/basis_, which specifies _types of atoms/ions and their positions relative to the lattice point_, in order to make a _crystal structure_
![[Lattices in crystals.png]]

- A _lattice vector_ is a vector _connecting two lattice points_
![[Lattice vectors.png]]
- Starting from some _arbitrary lattice point_, any _linear combination_ of _primitive lattice vectors_ $\bm{a}_i$, with _integer coefficients_, will be able to _generate the entire lattice_

- _Any_ $n$ _non-collinear lattice_ vectors in an $n-$dimensional lattice will form a _parallelepiped_ known as a _unit cell_:
![[Unit cells.png]]
- A _unit cell_ can _tessellate/tile_ the entire plane
	- Tessellation: _repeatedly_ translate the unit cell periodically, _completely covering_ an area _without overlap_

- A unit cell can contain _any number of lattice points_
	- Example: on the left, each lattice point contributes _a quarter_ of itself to the unit cell
- If it only contains _one lattice point_, the unit cell is known as a _primitive unit cell_
- For each lattice, primitive unit cells are _not unique_:
![[Primitive cells.png]]

- In _two-dimensions_, the _area_ of a unit cell defined by vectors $\bm{a}_1$ and $\bm{a}_2$ is $|\bm{a}_1\wedge\bm{a}_2|$
- In _three dimensions_, the _volume_ of the unit cell defined by vectors $\bm{a}_1$, $\bm{a}_2$, and $\bm{a}_3$ is $|\bm{a}_1\cdot(\bm{a}_2\wedge\bm{a}_3)|$

## Common examples of lattices
- In three-dimensional space, there are $14$ _possible Bravais lattices_
- The simplest structures will have _one atom per lattice point_

### Simple cubic (Cubic P)
- The points are _arranged at the corners of a cube_:
$$\bm{a}_1=a(1,0,0) \hspace{1cm} \bm{a}_2=a(0,1,0) \hspace{1cm} \bm{a}_3=a(0,0,1) \hspace{1cm} V_c=a^3$$
![[Cubic P primitive cell.png]]

- If there is _one hard sphere at each lattice point_, each having some radius $r$ such that they _all touch_, then the _percentage of volume filled_ is known as the _packing fraction_
- For the simple cubic lattice, as there is only _one lattice point_, the packing fraction can be shown to be:
$$\rho=\frac{(4/3)\pi(a/2)^3}{a^3}=\frac{\pi}{6}\approx52\%$$

### Body-centred cubic (Cubic I)
- The $bcc$ lattice is arranged as follows:
![[bcc lattice cubic cell.png]]
- It is a _cubic arrangement of points_, with an _additional point in the centre_
	- Hence, a cubic unit cell with side length $a$ will contain _two lattice points_

- The _primitive unit cell_ is a cube with _half the volume_:
$$\bm{a}_1=\frac{a}{2}(1,1,-1) \hspace{1cm} \bm{a}_2=\frac{a}{2}(-1,1,1) \hspace{1cm} \bm{a}_3=\frac{a}{2}(1,-1,1) \hspace{1cm} V_c=\frac{1}{2}a^3$$
- If packed with spheres, they touch _along the body diagonal_, with $r=\sqrt{3}a/4$
- The packing fraction is then:
$$\rho=\frac{\sqrt{3}\pi}{8}\approx 68\%$$

### Face-centred cubic (Cubic F)
- The $fcc$ lattice is arranged as follows:
![[fcc cubic unit cell.png]]
- It is a _cubic arrangement of points_, with an _additional point at the centre of each face_
	- Hence, a cubic unit cell with side length $a$ will contain _four lattice points_

- The _primitive unit cell_ has a _quarter_ of the volume:
$$\bm{a}_1=\frac{a}{2}(1,1,0) \hspace{1cm} \bm{a}_2=\frac{a}{2}(0,1,1) \hspace{1cm} \bm{a}_3=\frac{a}{2}(1,0,1) \hspace{1cm} V_c=\frac{1}{4}a^3$$

- If packed with spheres, they touch _along the face diagonal_
	- Then the structure can be seen as _three hexagonal layers_ in different positions, with pattern $ABCABC\dots$
- The packing fraction is then:
$$\rho=\frac{\pi}{3\sqrt{2}}\approx 74\%$$
- It is also known as the _cubic close-packed lattice_, as it has the _greatest packing density_ for a cubic structure
- Each lattice point is _coordinated with $12$ other lattice points

## Attaching a motif
- For each lattice point $\bm{r}_i$, attach the $j$th atom of the _motif_ at $\bm{r}_i+\bm{a}_j$

### Example: Hexagonal net in graphene
- Take a _two-dimensional_ _hexagonal_ Bravais lattice, with side length $a$:
![[2D hexagonal lattice.png]]
- For each lattice point at $(x_i,y_i)$, the _motif_ consists of _two identical atoms_:
$$\text{Atom 1: } (x_i,y_i) \hspace{1cm}\text{Atom 2: }\left(x_i,y_i+\frac{1}{\sqrt{3}}\right)$$
- This forms _two inter-penetrating hexagonal lattices_, making a _hexagonal net_, which is _distinct from the original lattice_:
![[Graphene sheet.png]]
### Example: Rock salt ($\ce{NaCl}$)
- The lattice is $fcc$ with a cube side length of $a$
- The motif is:
$$\ce{Cl-}\text{ ion : } (x_i,y_i,z_i) \hspace{1cm}\ce{Na+}\text{ ion : }\left(x_i,y_i,z_i+\frac{a}{2}\right)$$
- This forms _two inter-penetrating $fcc$ lattices_:
![[NaCl structure.png]]

### Example: Diamond
- The lattice is $fcc$
- The motif consists of _two identical atoms_:
$$\text{Atom 1: } (x_i,y_i,z_i) \hspace{1cm}\text{Atom 2: }\left(x_i+\frac{a}{4},y_i+\frac{a}{4},z_i+\frac{a}{4}\right)$$

- This forms a _tetrahedral network_:
![[Diamond cubic structure.png|600]]

### Example: Hexagonal close-packed
- The _hexagonal close-packed_ structure contains _alternating_ hexagonally packed layers
	- Pattern $ABAB\dots$
![[hcp hexagonal cell.png]]
- It is a _primitive hexagonal lattice_, with motif:
$$\text{Atom 1: } (x_i,y_i,z_i) \hspace{1cm}\text{Atom 2: }\left(x_i+\frac{a}{2},y_i+\frac{a}{2\sqrt{3}},z_i+\frac{c}{2}\right)$$
- Where $c$ is the _height_ of the hexagonal unit cell
- This structure also has the _highest packing density_, as it also consists of hexagonal layers

## Periodicity and plane waves
- Let some function in the crystal be modelled as a _plane wave_
- The effect on the atoms is dependent on the _value of the wave function at that point_
- Consider _two waves_, with a _difference in wave-vector_ $2\pi/a$:
![[Plane wave aliasing.png]]
- In general, waves with wavenumbers $\bm{k}+n(2\pi/a)$ will be _equivalent_, as the wave functions have _the same value at lattice points_
- They are said to be _commensurate_

- Therefore, only waves of wavenumber $-\pi/a<k<\pi/a$ will be _well-defined_
- This is known as the _reduced zone representation_

- In _multiple dimensions_, each wave-number is also only defined within:
$$\displaylines{-\pi/a_x<k_x<\pi/a_x \\ -\pi/a_y<k_y<\pi/a_y \\ -\pi/a_z<k_z<\pi/a_z}$$
- Then, to use the _reduced-zone representation_:
$$(k_x,k_y,k_z) \iff \left(k_x+n_x\frac{2\pi}{a_x},k_y+n_y\frac{2\pi}{a_y},k_z+n_z\frac{2\pi}{a_z}\right)$$

## The reciprocal lattice
- The _reciprocal lattice_ provides a way to describe what _plane waves in a lattice_ will be _commensurate_
- In _one dimension_, commensurate waves have $\Delta k=2\pi/a$
- Therefore, one can form a _lattice in $k-$space_, which consist of _commensurate wave-numbers_:
![[1D reciprocal lattice.png]]

- If a _primitive real-space lattice vector_ is $\bm{a}_i$, and a _primitive reciprocal lattice vector_ is $\bm{b}_j$:
$$\bm{a}_i\cdot\bm{b}_j=2\pi\delta_{ij}$$

- In _three dimensions_:
$$\bm{b}_1=\frac{2\pi(\bm{a}_2\cdot\bm{a}_3)}{\bm{a}_1\cdot(\bm{a}_2\wedge\bm{a}_3)}$$
- There are other _cyclic permutations_ that form $\bm{b}_2$ and $\bm{b}_3$
- The _volume_ of a reciprocal lattice cell is:
$$\bm{b}_1\cdot(\bm{b_2}\cdot\bm{b}_3)=\frac{(2\pi)^3}{\bm{a}_1\cdot(\bm{a}_2\wedge\bm{a}_3)}=\frac{(2\pi)^3}{V_c}$$

- _Examples_ of reciprocal lattices:
![[Reciprocal lattice examples.png]]
- Similarly, the reciprocal lattice of cubic $I$ is cubic $F$

## Brillouin zones
- Similar to how a _real lattice_ can be divided into _primitive unit cells_, a _reciprocal lattice_ can be divided into _Brillouin zones_

- The _first Brillouin zone_ from a lattice point is the region _closer to the origin_ than it is to _any other point_ in reciprocal space

- _Planes_ between two _nearest-neighbour points_ are known as _Bragg planes_
- In general, the $n$th Brillouin zone is a region of reciprocal space that can be _reached from the first Brillouin zone_, while crossing $(n-1)$ Bragg planes
- They must _all have the same area/volume_

- In 1D: ![[1D Brillouin zones.png]]
- A 2D _rectangular_ lattice: ![[2D Brillouin zones.png]]
- The _volume_ of each Brillouin zone in reciprocal space is the _volume of a reciprocal lattice unit cell_, or $(2\pi)^3/V_c$

- Brillouin zones of a 2D _square_ lattice:
![[Square lattice BZ 1-6.png]]

# Ionic crystals
- For ionic crystals, the _lattice energy_ is defined as the _energy needed to dissociate a solid lattice into widely separated gaseous ions_
- It must be deduced from a _thermodynamic cycle_
	- Using _ionisation energies, electron affinities, and enthalpies of formation_

## Electrostatic interactions
- Assume a simple _one-dimensional lattice_:
![[1D ionic lattice.png]]
- Considering the electrostatic energy arising from interactions with _one ion_, then multiplying by _one mole_:
$$E_\text{electrostatic}=-2N_A\frac{z_+z_-e^2}{4\pi\epsilon_0a}\left(1-\frac{1}{2}+\frac{1}{3}-\dots\right)$$

- Define the dimensionless _Madelung constant_ $\mathcal{A}$ such that:
$$E_\text{electrostatic}=-\frac{N_A\mathcal{A}z_-z_+e^2}{4\pi\epsilon_0a}$$
- The Madelung constant is a _function of the lattice arrangement_
- This model _generalises to 3D_, with different values of $\mathcal{A}$

![[Madelung constant table.png]]

## Finding lattice enthalpy
- If _only the electrostatic energy_ is accounted for, the lattice would simply _collapse_
- One must account for the _overlap of filled orbitals_, causing a _repulsion between ions_
- This is modelled by an _empirical term_:
$$E=-\frac{N_A\mathcal{A}z_-z_+e^2}{4\pi\epsilon_0a}+\frac{B}{a^n}$$
- A _typical_ value of $n$ is 9 or greaer

- The _equilibrium separation_ is found by _minimising_ $E$ w.r.t. $a$
- The _equilibrium energy_, with equilibrium separation $a_0$ is then given by:
$$E_0=-\frac{N_A\mathcal{A}z_-z_+e^2}{4\pi\epsilon_0a_0}\left(1-\frac{1}{n}\right)$$
- As this is an _crude theory_, it is often tolerable to _approximate_ the lattice _enthalpy_ as:
$$\Delta_L H^o\approx\frac{N_A\mathcal{A}z_-z_+e^2}{4\pi\epsilon_0a_0}\left(1-\frac{1}{n}\right)$$
## Ionic radii
- By considering _many ionic crystals_, one can define _ionic radii_ for each ion:
$$a_0=r_++r_-$$
- The ions are considered to be _hard spheres_
- The _tabulated values_ are only derived from _empirical data_, made to _fit the ionic model_
	- "Take them with a large pinch of salt"

- Approximating the ions as hard spheres, _equilibrium_ is reached when the _spacing is the sum of the ionic radii_
- For a _fixed_ $a_0$, one also requires an _optimum value_ of $r_\pm$ to achieve _maximum contact_ between the spheres
![[Radius ratio.png]]
- This gives an optimum _radius ratio_, which is a function of the _structure_
- If $r_+/r_-$ is _smaller_ than the optimum radius ratio, then the _cations and anions are not guaranteed to touch_, this gives an _unstable_ structure
- If $r_+/r_-$ is _larger_ than the optimum radius ratio, then as oppositely charged ions _touch_, it still gives a _stable_ structure
- Hence, the _optimum_ radius ratio is also the _minimum_ required by the structure

- Example: Sodium chloride
	![[NaCl radius ratio.png]]
	- The optimum/minimum radius ratio is:
	$$\frac{r_+}{r_-}=\sqrt{2}-1\approx 0.414$$
- The optimal/minimal radius ratio for various structures:
![[Minimum radius ratios.png]]

- Given some _ionic radii_, one can then work out the _optimum structure_ where the _radius ratio_ is _large enough_, and the _Madelung constant_ is also larger
	- Example: $r_+/r_-$ for $\ce{MgO}$ is 0.51, and can be _accommodated_ by the rock salt or sphalerite structure, but the _optimum_ is the rock salt structure for a larger $\mathcal{A}$

# The free electron gas
- The simplest model of the _potential_ experienced by electrons is the _free electron gas_
- It _ignores the periodic potential from nuclei_, as well as the _electron-electron repulsion_
- The [[Molecular quantum mechanics|Hamiltonian]] experienced by the electrons is:
$$\hat{\Ham}=-\frac{\hbar^2}{2m}\nabla^2$$

## Electrons as plane waves
- The _eigenfunctions_ of this Hamiltonian are:
$$\psi_\bm{k}(\bm{r})=A\exp(i\bm{k}\cdot\bm{r})$$
- $\bm{k}$ is the _wave-vector_ $(k_x,k_y,k_z)$
- The electrons are _un-constrained plane waves_ with momentum $\bm{p}=\hbar\bm{k}$
	- The _wavefronts_ are _planes linking points of constant phase_, perpendicular to $\bm{k}$
- They have _wavelength_:
$$\lambda=\frac{2\pi}{|\bm{k}|}=\frac{2\pi}{\sqrt{k_x^2+k_y^2+k_z^2}}$$

- The corresponding _energies_ are:
$$E_k=\frac{\hbar^2|\bm{k}|^2}{2m_e}$$
- This can be visualised as a _sphere_ in the _space of wave-vectors_, or $k-$_space_

- In _one-dimension_, this results in a _parabolic dispersion curve_:
![[1D FEG dispersion curve.png]]

- Without considering the boundary conditions, this results in a _continuous spectrum of energy_, making it difficult to define _energy levels_

## Born-von Karman boundary conditions
- The _BvK boundary conditions_ take the _periodicity_ of the lattice into account
	- Still does not take the _nuclei_ into account

- Let there be a _block_ of unit cells, with $N_i$ cells in each dimension $(i=1,2,3)$
	- This block is in the _bulk_ of the material to neglect _edge effects_
- Let the _lattice translation vector_ be:
$$\bm{T}=\sum_i N_i\bm{a}_i=N_1\bm{a}_1+N_2\bm{a}_2+N_3\bm{a}_3$$

- The boundary conditions assert that the function is _cyclic across the block of material_:
$$\psi(\bm{r}+\bm{T})=\psi(\bm{r})$$

- This _quantises_ the range of wave-vectors:
$$\bm{k}=2\pi\left(\frac{n_1}{N_1a_1},\frac{n_2}{N_2a_2},\frac{n_3}{N_3a_3}\right)$$
- Here, $n_i$ are _integers_
- If $a_1=a_2=a_3$, this gives _equally spaced $k-$states_
- They _do not correspond_ to [[#The reciprocal lattice|reciprocal lattice points]]
	- They are much more _densely packed_ than the reciprocal lattice
	- NvK points are also _not a physical quantity_, while the reciprocal lattice is completely physical

- In _one-dimension_, the [[Chemical thermodynamics#Density of states|density of states]] is the _reciprocal of the spacing_:
$$D_\text{1D}=\frac{N_1a_1}{2\pi}=\frac{\Lagr}{2\pi}$$
- Here, $N_1a_1=\Lagr$ is known as the _Born-von Karman length_

- In _two-dimensions_:
$$D_\text{2D}=\frac{N_1N_2A_c}{(2\pi)^2}=\frac{\mathcal{A}}{(2\pi)^2}$$
- Here, $A_c=a_1a_2$ is the _area of the unit cell_
- $\mathcal{A}=N_1N_2A_c$ is the _Born-von Karman area_

- In _three-dimensions_:
$$D_\text{3D}=\frac{N_1N_2N_3V_c}{(2\pi)^3}=\frac{\mathcal{V}}{(2\pi)^3}$$
- Here, $V_c=a_1a_2a_3$ is the _volume of the unit cell_
- $\mathcal{V}=N_1N_2N_3V_c$ is the _Born-von Karman volume_

## Populations of energy levels
- In [[Chemical thermodynamics|Molecular thermodynamics]], the _number of accessible translational states_ is _much higher than the number of molecules_
- For the _free electron gas_, the _energy spacing_ is much _larger_, and the _number density of electrons_ is very _high_ compared to a _gas_
- This results in the fact that the _number of accessible states is too high_
- Furthermore, one has to consider the [[Molecular quantum mechanics#Pauli Principle|Pauli Principle]] for electrons, which are _fermions_

- Therefore, one _cannot use the Boltzmann distribution_
- Instead, one needs the _Fermi-Dirac distribution_

- In _absolute zero_, the electrons fill the energy levels up to an energy level known as the _Fermi level_ $E_F$
- At a _finite temperature_, there is _sufficient energy_ to move some upper electrons to somewhat _above the Fermi level_
- The number of levels are within $\sim k_BT$ of the Fermi level
![[Fermi-Dirac distribution schematic.png]]

- The Fermi-Dirac distribution is written as:
$$f(E)=\frac{1}{\exp\left(\frac{E-\mu}{k_BT}\right)+1}$$
- $f(E)$ is the _probability an electron occupies energy level $E$_
- $\mu$ is the [[Chemical thermodynamics|chemical potential]] of the electron

- In most cases, $\mu$ is _approximated as the Fermi energy_ $E_F$:
$$f(E)=\frac{1}{\exp\left(\frac{E-E_F}{k_BT}\right)+1}$$
![[Fermi-Dirac distribution graph.png]]
- In most cases, $E_F>>k_BT$, so the _smoothing_ of the curve is very _slight_

- In the _limiting case_ $E>>E_F$, the _exponential_ dominates, and one regains the _Boltzmann distribution_

## Properties of the Free Electron gas
- One can use the model to predict _physical properties_
- They _should not depend_ on the BvK volume, which is a _mathematical construction_
- These _measurable quantities_ can serve as a _test_ for the model
	- Generally found to work well for _group 1 metals_

### Fermi energy and wave-vector
- Given some energy $E\propto k^2$, the corresponding $k-$states lie on a _spherical shell_ in $k-$space

- The _number of states_ $W(E)$ with an energy _up to_ $E$ can then be calculated by multiplying the _volume in $k-$space_, with the _density of BvK states_, then accounting for _spin_:
$$W(E)=2\left(\frac{4}{3}\pi k^3\right)\left(\frac{\mathcal{V}}{(2\pi)^3}\right)=\frac{k^3\mathcal{V}}{3\pi^2}=\frac{\mathcal{V}}{3\pi^2}\left(\frac{2m_eE}{\hbar^2}\right)^{3/2}$$
- If the _electron number density_ is $n_e$, within one _BvK volume_ $\mathcal{V}=N_1N_2N_3V_c$, the number of _experimentally accessible states_ is:
$$W(E_F)=n_e\mathcal{V}$$
- Then, one can calculate the _Fermi energy_
$$E_F=\left(\frac{\hbar^2}{2m_e}\right)(3\pi^2 n_e)^{2/3}$$
- At the Fermi enegry, the _Fermi wave-vector_ is then:
$$k_F=(3\pi^2n_e)^{1/3}$$
- These are _physically measurable quantities_, hence they must be _independent of $\mathcal{V}$_

### Average energy
- To obtain _average energy at absolute zero_, one must find the _density of states_ $D(E)$ as a function of energy:
$$D(E)=\frac{d\,W(E)}{dE}=\frac{\mathcal{V}}{2\pi^2}\left(\frac{2m_e}{\hbar^2}\right)^{3/2}\sqrt{E}$$
- The density of states _increases with energy_

- Then, one obtains the _average energy_ by:
$$\mean{E}=\frac{\int_0^{E_F}E\,D(E)\,dE}{\int_0^{E_F}D(E)\,dE}=\frac{3}{5}E_F$$
### Heat capacity
- The _Debye law_ says that _insulating_ solids have a heat capacity $\propto T^3$ at _low temperatures_
- For _metals_, there is an _additional_ linear term

- At a _low temperature_, only electrons _within $k_BT$ of the Fermi level_ are excited
- The total _change in thermal energy_ for one _mole_ of electrons is then _approximately_:
	$$U\sim(k_BT)N_A\frac{k_BT}{E_F}$$
	- This _ignores the non-uniform density of states_

- The _heat capacity_ is then:
$$C_V=\pd{U}{T}\sim \frac{2Rk_BT}{E_F}=2R\frac{T}{T_F}$$
- Here, $T_F$ is the _characteristic Fermi temperature_:
$$T_F=\frac{E_F}{k_B}$$
- A more _rigorous treatment_ using the Fermi-Dirac distribution then gives:
$$C_V=\frac{\pi^2R}{2}\frac{T}{T_F}$$

### Bulk modulus
- The _bulk modulus_ of a material is defined as:
$$B=-\frac{p}{\delta V/V}$$
- $p$ is the _pressure_ used to _compress_ the material
- Expressing in terms of _infinitesimals_:
$$B=-V\left(\pd{p}{V}\right)_{T,N} \hspace{1cm} p=-\left(\pd{U}{V}\right)_N$$
- Considering the _bulk_ of the crystal, using the _BvK volume_ as the variable:
$$E_F=\frac{\hbar^2}{2m_e}\left(3\pi^2n_e\right)^{2/3}=\frac{\hbar^2}{2m_e}\left(3\pi^2\frac{N}{\mathcal{V}}\right)^{2/3}$$
- Doing the derivatives:
$$B=-\mathcal{V}\left(\pd{p}{\mathcal{V}}\right)_{T,N} \hspace{1cm} p=-\left(\pd{U}{\mathcal{V}}\right)_N$$
- One finds the bulk modulus as:
$$B=\frac{2}{3}E_Fn_e$$

## Electrical conductivity
- Metals are _good conductors_ of electricity
	- Conductivity often _decreases with increasing temperature_
- When there is _no applied electric field_, $\bm{k}$ is _spread symmetrically_ in the _Fermi sphere_
- On _average_, the electrons have _zero net velocity_

- When an _electric field_ is applied, the electrons experience a _force_ opposite the field
- Electrons regularly _collide_ with nuclei, but _on average_, they manage to _drift_ in the direction opposite the field
- This means _on average_, the Fermi sphere is _shifted_:
![[Fermi circle shift.png]]
- This gives a _net drift velocity_, which gives rise to a _current_

- For this to occur, there must also be _empty states_ in the direction of the field
	- Always true for the _free electron gas_

- In this model, only the _number of electrons near the Fermi energy_ will _contribute_ to conductivity
	- In contrast to the classical _Drude model_, where _all electrons_ drift and contribute to conductivity

- In the _Drude model_, the _drift velocity_ is given by:
	$$\bm{v}_d=\frac{e\bm{E}\tau}{m_e}$$
	- $\tau$: average _scattering time_
- This gives the _current density_:
$$\bm{J}=\frac{n_ee^2\tau}{m_e}\bm{E}$$

# The nearly-free electron gas
- This _starts from the FEG model_, then makes adjustments by _taking the electronic potential of nuclei_ into account

## Applying the reduced-zone representation
- Consider the [[#Electrons as plane waves|dispersion curve]] in the free electron gas model, then apply the [[#Periodicity and plane waves|reduced-zone representation]]:
![[FEG backfolding.png]]

- Similarly, considering _differently angled lines_ in a two-dimensional dispersion plot, one can construct:
![[2D reduced zone FEG dispersion.png]]

## Band gap formation in 1D
- Consider two _degenerate wave-functions_:
$$\psi_+=\exp\left(+i\frac{\pi x}{a}\right) \hspace{1cm} \psi_-=\exp\left(-i\frac{\pi x}{a}\right)$$
- Then, consider the _linear combinations_:
$$\psi_c=\cos(\pi x/a)=\frac{\psi_++\psi_-}{2} \hspace{1cm} \psi_s=\sin(\pi x/a)=\frac{\psi_+-\psi_-}{2i}$$
- $\psi_c$ has a _non-zero value_ at the _lattice points_
- $\psi_s$ has _nodes_ at lattice points
![[psic and psis.png]]
- Then, if there are _interactions with atoms_, this will cause an _energy split_ (the degeneracy is _lifted_)

- Then, considering _lower wave-numbers_:
![[psic and psis lower wavenumber.png]]
- Averaged over _several cycles_, the degeneracy _remains_

- Hence, this forms a _perturbation_ to the dispersion plot due to the loss of degeneracy:
![[Band gap formation.png]]
- Hence, for a _range of energies_, there are _no available $k-$states_
- These band gaps will appear at the _edge of the_ [[#Brillouin zones|Brillouin zone]]

- If the _Fermi level_ is within the band gap, for _low temperatures_, electric conduction is _impossible_, as the electrons _cannot be promoted_

- In the _first band_, for $L$ _unit cells_, the _number of available states_ is:
$$N_1=\frac{2\pi}{a}\frac{La}{2\pi}=L$$
- If each unit cell has _one valence electron_, they would fill $L/2$ states, which _fills up half of the first band_, therefore the material will be a _metallic conductor_
	- Each BvK state can hold two electrons
- If each unit cell has _two valence electrons_, this _completely fills up the first band_, making the material an _insulator_

- Hence, this model predicts _group 2 metals are insulators_
- Therefore, one must consider _more dimensions_ for a viable model

## Band gaps in more dimensions
- A band diagram for 2 dimensions, in the _reduced zone representation_:
![[2D NFEG dispersion curve.png]]

- In 2 or 3 dimensions, the _bands corresponding to different $\bm{k}$ directions_ will _overlap_, as their gaps are at _different energies_
- The electrons will _start filling the second band before the first one is completely filled_

- Overall, each _Brillouin zone_ for a crystal of $L$ unit cells can still fit $L$ $k-$states
	- This means each zone can fit $2L$ _electrons_

## Fermi surfaces
- As electrons _start to fill up_ the first Brillouin zone, as $E\propto k^2$, the _filled states are within a sphere in_ $k-$space, also known as the _Fermi sphere_

- A _group 1_ metal with one valence electron _per unit cell_ will occupy _half_ the states, with the presence of _empty states_ above the Fermi level leading to _conduction_
	- In other words, the _Fermi sphere is within the first Brillouin zone_

- A _group 2_ metal will lead to a _Fermi sphere intersecting the first Brillouin zone_ (depending on the metal), and having regions inside _both the 1st and 2nd Brillouin zones_:
![[Group 1 group 2 fermi circles.png]]
- The first Brillouin zone is _partially filled_, however due to the _band gap_ between the first and second Brillouin zones, the Fermi surface is _distorted_, and starts to _bulge_

# The tight-binding model
- Instead of considering _each electron separately in a potential_ (akin to a _gas_), consider the solid as a "giant molecule"
- Like [[Bonding in molecules|normal molecules]], use _atomic orbitals as a basis_ in order to form _molecular orbitals_ extending over the solid

- With the _large amount of atomic orbitals_, this leads to a _large number of closely-spaced molecular orbitals_
- The molecular orbitals must take the _translational symmetry_ of the crystal into account

## Electron bands in one dimension
- Let there be $N$ unit cells, contributing $N$ _atomic orbitals_ in total
- Let the orbital at _position_ $r$ be $\phi_r$
- This then forms the _crystal orbital_ $\psi_k$:
$$\psi_k=\sum_{r=1}^\infty c_k^{(r)}\phi_r$$
- $k$ ranges from $1$ to $N$

- Then, deploy the [[#Born-von Karman boundary conditions]], where the wave-function must _repeat_ after $N$ atoms:
$$c_k^{(N+r)}=c_k^{(r)}$$
- This is _satisfied_ by coefficients of the form:
	$$c_k^{(r)}=\exp(ikra) \;\;,\;\; k=\frac{2m\pi}{Na}$$
	- Where $m$ is an _integer

- Hence, the states are also _quantised_, with _spacing_ $2\pi/Na$

- For $m=0$, _all orbitals_ will contribute _in-phase_, which gives the _most bonding crystal orbital possible_
- For $m=\pm N/2$, _all orbitals_ will _alternate_ between phases $0$ and $\pi$, which gives the _most anti-bonding crystal orbital_

- It can easily be proven that if $|m|>N/2$, it simply gives a _crystal orbital that can be represented by_ $m-N$
- This matches the assertion that there are $N$ crystal orbitals, with:
$$\displaylines{-\frac{N}{2}<m<\frac{N}{2} \\ -\frac{\pi}{a}<k<\frac{\pi}{a}}$$

- The _energies_ are then simply given by:
$$E_k=\left(\int \psi_k^*\,\hat{\Ham}\,\psi_k\,d\tau\right)\left(\int \psi_k^*\psi_k\,d\tau\right)^{-1}$$

### Hückel Approximations
- To calculate the energy, apply the [[Bonding in molecules#Hückel Approximations|Hückel Approximations]]
	- They assume _tight binding_ of electrons to their nuclei
	- While "loose" enough to _overlap_ with other orbitals, still "tight" enough that the interactions are _short range_

- All AOs have the _same energy_ $\alpha$:
$$\int \phi_r^*\,\hat{\Ham}\,\phi_r\,d\tau=\alpha$$
- The _resonance integral_ is only non-zero for _neighbouring atoms_, and always takes the _same value_ $\beta$:
$$\int \phi_r^*\,\hat{\Ham}\,\phi_{r+1}\,d\tau=\beta\,\delta_{r',r+1}$$
- Neglect the _overlap integral_:
$$\int\phi_r^*\phi_s\,d\tau=0 \;\;\text{ for }r\neq s$$
- The atomic orbitals are _normalised_:
$$\int \phi_r^*\phi_r\,d\tau=1$$

- Then, using these approximations:
$$\displaylines{ \int\psi_k^*\psi_k\,d\tau=N \\ \int\psi_k^*\,\hat{\Ham}\,\psi_k\,d\tau=N\alpha+[\exp(ika)+\exp(-ika)]N\beta}$$
- This then gives the _energies of the crystal orbitals_:
$$E_k=\alpha+2\beta\cos(ka)$$
- These _discrete values_ of energy then form a _band_, of width $|4\beta|$
- The energy is _symmetric_ w.r.t. $k$

### The s band
- Considering $s$ orbitals, an _in-phase_ interaction is _always favourable_, hence $\beta<0$:
![[Tight binding 1D band.png]]
- Each band can then accomodate $2N$ _electrons_ in total
- One can also _normalise_ the crystal orbitals:
$$\Psi_k=\frac{1}{\sqrt{N}}\sum_{r=1}^N \exp(ikra)\,\phi_r$$

- The _number of $k-$states_ $W(E)$, up to energy $E$ is calculated by:
$$W(E)=\frac{2|k(E)|}{2\pi/Na}=\frac{Na}{\pi}|k(E)|$$
- The _density of $k-$states_ $D(E)$ is then given by:
$$D(E)=\frac{d\,W(E)}{dE}=\frac{dW}{dk}\left(\frac{dE}{dk}\right)^{-1}=-\frac{N}{2\pi\beta}\frac{1}{\sin(ka)}$$
![[1D s band density of states.png]]
- This is a function of $E$, hence only consider _absolute value_ of $k$
- It is _inverse_ to the _slope_ of the dispersion curve
- The rise to _infinity_ is only seen in _one dimension_

### The p bands
- Consider _head-on_ $(\sigma)$ interactions between $p$ orbitals
- If all orbitals are combined _in-phase_, this gives rise to _anti-bonding_ interactions
- Hence, $\beta>0$, and the dispersion relation gives:
![[1D p band dispersion curve.png]]

- When considering $\pi$ interactions, an _in-phase_ combination is _bonding_
- This gives a dispersion curve _similar to the $s-$band_

### s-p mixing
- Like orbitals in molecules, _s-bands and p-bands can mix_
- Like the _symmetry criteria_ in molecules, only _crytal orbitals with the same_ $k$ can mix

- Consider the interactions between the $s$ and $p$ crystal orbitals at $k=0$:
	- $s$ crystal orbital is _bonding_, $p$ crystal orbital is _antibonding_
![[sp band mixing k0.png]]
- The _constructive_ and _destructive_ interferences will _cancel out_
- Hence, at $k=0$, there is _no mixing_
- Similarly, at $k=\pm\pi/a$, there is _no mixing_

- Then consider the interactions at $k=\pm\pi/2a$:
![[sp band mixing halfway.png]]
- Consider the _real parts_ of the orbitals
	- From symmetry, the _imaginary parts_ have the same interactions
- This then gives _bonding interactions_, hence there is _mixing_
- This _pushes the band energies apart_
	- The $s$ band is _stabilised_, and vice versa
- From _symmetry_, this $k$ value gives the _maximum mixing_

- If the $s$ and $p$ orbitals are _spaced far apart_, this gives _weak mixing_ (left figure below):
![[s-p band mixing.png]]

- If $s$ and $p$ orbitals are _close in energy_, and the _original energies cross_ at some value of $k$, the _mixing_ will create an _avoided crossing_ (right figure above)
- The bands will "interconvert" in nature at $k=\pi/a$

### Bands from hybrid atomic orbitals
- Bands can be created from _hybrid atomic orbitals_
	- Useful for considering _semiconductors_
- For example, consider the $sp$ orbitals in 1D

- First, consider _localised pairwise interactions_ between _adjacent_ hybrid orbitals
- There are _bonding MOs_ that form _across_ atoms:
	- Formed due to interactions between $sp$ orbitals in _different directions_, belonging to _adjacent_ atoms
![[Band formation from sp bonding.png]]
- At $k=0$, all of the _bonding_ orbitals are _in-phase_, and form an _overall bonding_ orbital
	- It is the _lowest energy crystal orbital_ possible
- At $k=\pi/a$, there is a mix of _bonding and antibonding interactions_, which leads to a _higher energy_ orbital relative to $k=0$
- So, the bonding orbitals form their own _band_ of crystal orbitals

- Then, consider the _antibonding_ MOs formed across atoms:
![[sp band antibonding.png]]
- At $k=0$, all the _antibonding_ orbitals combine in-phase to form an _overall antibonding_ orbital
	- It is the _highest energy crystal orbital_ possible
- At $k=\pi/a$, there is a mix of _bonding and antibonding_ interactions, which forms a _lower energy_ orbital relative to $k=0$
- So, the antibonding orbitals form a _separate band_ of crystal orbitals

- The process of band formation can be summarised by:
![[sp band formation summary.png]]
- The band width is $|2\beta_2|$, where $\beta_2$ depends on the _energy difference_ between $s$ and $p$:
$$\beta_2=\alpha_s-\alpha_p$$

## Electron bands in two dimensions
- Similar to one dimension, the _crystal orbitals_ are still a _linear combination_ of atomic orbitals, but determined by _two parameters_, $k_x$ and $k_y$
- Characterise the _atomic_ orbitals by two positional parameters, $r$ and $s$
$$\psi_{k_x,k_y}=\sum_{r,s} c_{k_x,k_y}^{(r,s)}\;\phi_{r,s}$$
- The simplest case is a _square lattice_
- The solution is given by:
$$\displaylines{c_{k_x,k_y}^{(r,s)}=\exp(ik_xra)\exp(ik_ysa) \\ k_x=m_x\frac{2\pi}{Na} \hspace{1cm} k_y=m_y\frac{2\pi}{Na}}$$
![[2D crystal orbitals.png]]
- The Hückel Approximations _hold respectively in each dimension_
	- Orbital $(r.s)$ intreracts with orbitals at $(r\pm1,s)$, contributing $2\beta\cos(k_xa)$
	- It also interacts with orbitals at $(r,s\pm1)$, contributing $2\beta\cos(k_ya)$
- There are $N^2$ such terms in total
- Adding the energy _of the orbital_ itself, and normalising:
$$E_{k_x,k_y}=\alpha+2\beta[\cos(k_xa)+\cos(k_ya)]$$

- The _first Brillouin zone_ is a _square_ where $-\pi/a<k_x,k_y,\pi/a$
- The dispersion curve can be represented as a _path between high symmetry points_, or a _contour plot_ can be used:
![[2D electron dispersion.png]]

- The _density of states_ $D(E)$ can be understood as being proportional to the _length of a constant energy contour_
- It is _zero_ at $E=\alpha\pm4\beta$, or $(0,0)$ and $(\pm\pi/a,\pm\pi/a)$
	- The drop is _abrupt_, and is known as a _van Hove singularity_, commonly seen in 2D and 3D systems
	- A singularity appears in the [[#The s band|1D case]] as a rise to _infinity_ instead of a drop
- There is a _maximum_ at $E=\alpha$

## A two-atom basis
- Consider a lattice with _two atoms per lattice point_:
![[1D two atom lattice.png]]
- Let the separation between each atom be _smaller_ than half the lattice point separation, or $2a'<a$
	- In other words, the _closest distance between neighbouring pairs_ is _longer_ than the _distance between atoms in a basis_

- Let each atom contribute _one orbital_
	- Typically formed using $\pi$ systems
- Like the [[#Bands from hybrid atomic orbitals|case of hybridised orbitals]], the _bonding_ and _antibonding_ orbitals will form _separate bands_

- The _bonding orbitals_:
![[2 atom lattice bonding.png]]
- As $2a'<a$, the _bonding interaction in the basis_ is _stronger_ than any _antibonding_ interaction between _neighbouring pairs_
- Hence, all crystal orbitals in the band are _bonding_
	- The totally in-phase combination is the _most bonding_, and vice versa

- The _antibonding_ orbitals:
![[2 atom lattice antibonding.png]]
- Similarly, the _antibonding interaction in the basis_ is _stronger_ than any _bonding_ interaction between _neighbouring pairs_
- Hence, all crystal orbitals in the band are _antibonding_

- Therefore, as long as $2a'<a$, there is a _band gap_:
![[1D two atom basis bands.png]]

- Like the case of [[#s-p mixing]], there are still _minor interactions_ between the crystal orbitals
- If $2a'<a$, and each orbital contributes _one electron_, the material is an _insulator_
	- There are _two electrons per cell_, therefore the $\pi$ band is _full_

- If $2a'=a$, the orbitals at $k=\pm\pi/a$ are _purely non-bonding_
	- If each orbital contributes one electron, at the Fermi level, there are more _available states_, hence the material is a _conductor_

### Polyacetylene and Peierl's distortion
- A _one-dimensional_ system which _approximates_ the system above is _polyacetylene_:
![[Polyacetylene.png]]
- Each _carbon atom_ gives one $p_\pi$ orbital, containing _one electron_

- The electrons _fully fill_ the $\pi$ band
- Even if $2a'=a$, the _total energy can be lowered_ by _distorting_ the molecule and _shortening_ $a'$
- This is known as _Peierl's distortion_
- Hence, _neutral_ 1D systems can only be _insulators_

### Graphene
- In order to make a _conductor_ in low dimensions with the above _band structure_, one would need to _move the Fermi level_

- [[#Example: Hexagonal net in graphene|Graphene]] is a _2D hexagonal net_ of carbons, each contributing _one electron_
- Its 1st Brillouin zone is:
![[Graphene 1st BZ zone.png]]

- The $p_\pi$ orbitals in graphene form:
![[Graphene dispersion.png]]

- One still needs to _dope_ graphene in order to _move the Fermi level_ and make a conductor
- Typical donors are $\ce{Li}$ or $\ce{Na}$
- Typical acceptors are $\ce{Br}$ and $\ce{AsF5}$

# Semiconductors
- Building blocks for _electronic devices_

## Conductivity
- The _resistance $R$_ of a material is given by:
$$R=\frac{\rho l}{A}$$
- It is equal to the _ratio_ of _potential difference_ across the material to the _current_ through it
- $R$ depends on the _dimensions_ of the material, with length $l$ and area $A$
- The _resistivity_ $\rho$ of the material is an _intrinsic property_ of the material
	- Metals: $\sim 10^{-8}\Omega\text{m}$
	- Semiconductors: $\sim 10^{-2}\Omega\text{m}$
	- Glass: $\sim 10^{11}\Omega\text{m}$

- The _conductivity $\sigma$_ of a material is defined as:
$$\sigma=\frac{1}{\rho}$$
- Conductivity is often _temperature-dependent_

- _Metals_ are said to have _high conductivity_ over a _wide range of temperatures_
	- Resistivity _increases linearly_ over a narrow range of temperature

- _Semiconductors_ have _intermediate conductivity_
	- Conductivity _increases_ with temperature, via an _Arrhenius relation_: 
	$$\sigma_\text{semi}\propto\exp\left(-\frac{E}{k_BT}\right)$$
- Semiconductors can be _intrinsic_ or _extrinsic_
- An _intrinsic semiconductor_ is often a _pure substance_, which is intrinsically conductive
- An _extrinsic semiconductor_ is often conductive due to _impurities_, introduced by _doping_

- _Insulators_ have _low conductivity_ over a _wide range of temperatures_

- _Superconductors_ will have _exactly zero resistivity_ at _extremely low temperatures_ $\sim 10K$

## Intrinsic semiconductors
- A common _band structure_ in intrinsic semiconductors:
![[Intrinsic semiconductor band structure.png]]
- There is a lower _valence band_, as well as an upper _conduction band_, with a _band gap_ in between, of magnitude denoted $E_g$
	- Typical $E_g\sim 10^0\text{ eV}$ for silicon and germanium

- The lower _valence band_ can be imagined to be formed from _bonding orbitals_, such as the $\sigma$ band formed from $sp^3$ orbitals in silicon
	- [[#Bands from hybrid atomic orbitals]]
- Similarly, the conduction band can be imagined to form from _antibonding orbitals_

- At _absolute zero_, the valence band is _full_ and the conduction band is _empty_

- At a _finite temperature_, electrons are _promoted_ into the conduction band
- Therefore, there are _empty states_ for electrons to move into, making the material a _conductor_

### Holes
- The _absence of an electron_ is called a _hole_, denoted $h^+$
- The _migration of electrons_ can be thought of as _migration of holes in an opposite direction_

- In an _intrinsic_ semiconductor, the _number of promoted electrons_ $n_e$ is _equal_ to the _number of holes_ in the valence band $n_h$:
$$n_e=n_h$$
- The _total conductivity_ due to the _number densities_ of electrons and holes, $n_e$ and $n_h$:
$$\sigma=n_ee\mu_e+n_he\mu_h$$
- $\mu_e$ and $\mu_h$ are the _mobilities_ of the electrons and holes
	- Applying an electric field $E$ will cause them to move at _speed_ $\mu E$

### Distribution of electrons
- Consider the [[#Population of energy levels|Fermi-Dirac distribution]]:
$$f(E)=\frac{1}{\exp[(E-E_F)/k_BT]+1}$$
- The _density of occupied states_ $Z(E)$ is then:
$$Z(E)=f(E)D(E)$$
- Where $D(E)$ is the _density of states_ and is a property of the system
- For a _semiconductor_:
![[Semiconductor density of occupied states.png]]
- At a _finite temperature_, the electrons _leave the valence band_ and go _into the conduction band_
- The _total number of electrons_ is _conserved_

- If the _density of states_ of the two bands have _the same form_, the _Fermi energy_ must be exactly in the _middle of the band gap_
- If they have _different forms_, then from the _conservation_ of number of electrons, one can see that the Fermi energy is _displaced_

- At _absolute zero_, the position Fermi energy can be seen as the _limit_ of its position at _low temperatures_

### Temperature dependence of conductivity
- The number of _promoted electrons_:
$$N_e=\int_{E_c}^\infty\,Z(E)\,dE=\int_{E_c}^\infty\frac{D(E)}{\exp[(E-E_F)/k_BT]+1}\,dE$$
- $E_c$ is the _energy at the bottom of the conduction band_
- The limit at _infinity_ is justified as long as the _width of the conduction band_ $>>kT$

- Assume $D(E)$ is a _constant_ $c$
- Normally, $E_c-E_F>>k_BT$, therefore:
$$N_e\approx c\int_{E_c}^\infty \exp\left(-\frac{E-E_F}{k_BT}\right)\,dE=ck_BT\exp\left(-\frac{E_c-E_F}{k_BT}\right)$$
- If the Fermi energy is _in the middle of the band gap_:
$$\displaylines{E_c-E_F=\frac{1}{2}E_g \\ \sigma\propto N_e\propto \exp\left(-\frac{E_g}{2k_BT}\right)}$$
- Under typical conditions, as $E_g>>k_BT$, ignore the _linearity_ in $T$
- One can approximate the _activation energy_ of the process as _half the band gap_

### Equilibrium of electrons and holes
- The _generation_ of an _electron in the conduction band_, with a _hole in the valence band_ can be modelled as a _"reaction"_:
$$\cdot\ce{<=>e-+h+}$$
- $\cdot$ is the _ground state_, with the filled conduction band and empty conduction band at absolute zero
	- It is _non-degenerate_ and _immobile_, hence it is _ignored_ when calculating $K_c$
- Consider the [[Chemical thermodynamics#Reactions and equilibrium|equilibrium]] of this reaction:
$$K_c=\frac{n_hn_e}{(c^o)^2}=\frac{f_ef_h}{(c^o)^2}\exp\left(-\frac{\Delta\varepsilon_0}{k_BT}\right)$$
- The electrons and holes have _electronic degeneracies_ of $2$ due to spin
	- This is then effectively their _electronic partition function_
- By considering the [[Chemical thermodynamics#Translational partition function|translational partition functions]] as well:
$$K_c=\frac{4(m_e^*m_h^*)^{3/2}}{(c^o)^2}\left(\frac{2\pi k_BT}{h^2}\right)^{3}\exp\left(-\frac{E_g}{k_BT}\right)$$
- The masses are replaced with _effective masses_

- A typical value of $K_c$ for $\ce{Si}$ at $300\text{K}$ is $\sim 10^{30}$, which works out to $n_e\approx 10^{15}\text{ m}^{3}$, which is still only _one promoted electron per_ $10^{13}$ _atoms_

### Effective mass
- The _effective mass_ allows one to apply results from the _nearly free/tight-binding_ models to results from the _free electron model_
- The _dispersion curve_ can be approximated as _parabolic_ in certain limits

- For a _free electron_, $E_k=k^2\hbar^2/2m_e$
- From the [[#The tight-binding model|tight-binding model]]:
$$E_k=\alpha+2\beta\cos(ka)$$
- Consider the _long wavelength limit_, where $|ka|<<\pi$:
$$E_k\approx \alpha+2\beta-\beta k^2a^2$$
- Ignoring the _constant terms_, $E_k\propto k^2$, which is _similar to the free electron energy_
- Hence, define the _effective mass_ $m_e^*$:
$$\displaylines{\frac{\hbar^2k^2}{2m_e^*}=-\beta k^2a^2 \\ m_e^*=-\frac{\hbar^2}{2\beta a^2}}$$
- As $\beta<0$, the effective mass is still _positive_

- Similarly, in the _short wavelength limit_:
$$m_e^*=\frac{\hbar^2}{2\beta a^2}<0$$

- $\beta$ determines the _width_ of the band, and it is _inversely proportional_ to the effective mass
- The _definition_ of the effective mass can be written as:
$$\frac{1}{m_e^*}=\frac{1}{\hbar^2}\frac{d^2E_k}{dk^2}$$
- It depends on the _curvature_ of the dispersion curve

- The effective mass gives the _response of an electron to an applied electric field_
	- A _positive_ $m_e^*$ moves _opposite_ to the field
	- A _negative_ $m_e^*$ moves _in the direction of the field_

- In the _tight-binding model_:
$$\frac{1}{m_e^*}=-\frac{2\beta a^2}{\hbar^2}\cos(ka)$$
- For $ka=\pi/2$, the effective mass becomes _infinite_
	- An applied electric field _will not affect the electron_

## Extrinsic semiconductors
- An _extrinsic_ semiconductor is a semiconductor with _low concentration dopant atoms_, which act as _impurities_
	- A typical dopant atom concentration is in _parts per million_

- The most important form is _substituional doping_, which _swaps out_ the original atoms with dopant atoms
- If the dopant has _more valence electrons_ than the host, the semiconductor is _n-type_
	- There is an _excess_ of electrons, and the dopant is known as a _donor_
	- The charge carriers are _electrons_
- If the dopant has _fewer valence electrons_ than the host, the semiconductor is _p-type_
	- Electrons are _withdrawn_, and the dopant is known as an _acceptor_
	- The charge carriers are _holes_

- If the host is _silicon_ $\ce{Si}$ or _germanium_ $\ce{Ge}$
	- Typical _donors_: $\ce{P, As, Sb}$
	- Typical _acceptors_: $\ce{Al, Ga}$
- An alternative to silicon is _gallium arsenide_, $\ce{GaAs}$
	- Typical _donors_; $\ce{Ge}$ substituting $\ce{Ga}$
	- Typical _acceptors_: $\ce{Ge}$ substituting $\ce{As}$

### Electronic structure
- In an _n-type_ semiconductor, the electrons from the dopant give a _discrete set of levels_ right under the conduction band
	- The electrons are effectively _bound_ to the donor atom
	- The _dilute concentration_ means there is _no overlap_, and there is no band
- A typical gap between $E_d$ and the conduction band is on the order of $\text{meV}$
- At room temperature, they can be _excited into the conduction band_
- Typically, the number of _excited electons from the dopant_ will _greatly exceed_ the number of excited _intrinsic electrons_
	- The gap between 

- In a _p-type_ semiconductor, the acceptor atoms create _discrete vacancies_ right above the valence band
- At room temperature, _electrons can be excited onto the acceptor level_
- This creates _holes in the valence band_
- There are _very few electrons in the conduction band_
![[Doped semiconductors electronic structure.png]]

### Donor levels
- To model the donor levels, assume the _donor atoms are hydrogen-like_, with the lone electron being the one _donated into the conduction band_
- When calculating the _Coulomb potential_, use the _relative permittivity_ of the semiconductor
- This _decreases the charge-charge interaction_
- One also needs to use the _effective mass of the electron_:
$$\displaylines{\epsilon_0\to\epsilon_r\epsilon_0 \hspace{1cm} m_e\to m_e^* \\ E_n=-\frac{R_H}{n^2}=-\frac{e^4m_e}{32\pi^2\epsilon_0^2}\frac{1}{n^2} \\ R_{H,\text{eff}}=R_{H,\text{eff}}\frac{m_e^*}{m_e\epsilon_r^2}}$$
- The orbitals will also _change size_ due to this interaction
- Therefore, one must change the _Bohr radius_:
$$a_0=\frac{4\pi\hbar^2}{e^2}\frac{\epsilon_0}{m_e}\to a_{0,\text{eff}}=a_0\frac{\epsilon_rm_e}{m_e^*}$$
- Define the _zero energy_ as the _bottom of the conduction band_
	- Ionisation is then defined as _taking the electron into the conduction band_

### Acceptor levels
- To model te acceptor levels, similar to the donor levels, assume the _acceptor atoms are hydrogen-like_
- The zero energy is defined as _relative to the top of the valence band_:
$$E_n=+\frac{R_{H,\text{eff}}}{n^2}$$
![[Donor and acceptor levels.png]]

### Fermi energy
- In [[#Intrinsic semiconductors]], the _Fermi level_ is near the _middle of the band gap_
- In _extrinsic_ semiconductors, the Fermi level is _dependent on the donor/acceptor level_

- For _n-type_ semiconductors:
![[n type Fermi level.png]]

- The _density of states_ is _much higher in the conduction band_ than in the donor levels
- At _low temperatures_, the valence band is still _completely filled_, while _most donor levels_ are unoccupied, as the electrons are excited
- Therefore, the Fermi level is _between the bottom of the conduction band and the donor levels_, when the temperature is _ambient_

- At _high temperatures_, the Fermi level will be _somewhere below the acceptor levels_, as the valence band becomes _partially filled_

### Temperature dependence of conductivity
- At _low temperatures_, the _donor electrons/acceptor holes_ are steadily _promoted/occupied_
	- For an _n-type_ semiconductor where $E_c-E_d$ is the _energy difference_ between the conduction band and donor levels:
$$\sigma\propto\exp\left(-\frac{E_c-E_d}{2k_BT}\right)$$
- This is the _extrinsic region_

- At _higher temperatures_, all electrons/holes from doping _run out_, and conductivity remains _constant_
- This is the _exhaustion region_

- At _even higher temperatures_, electrons can be promoted directly _from the valence band to the conduction band_, and conductivity increases exponentially again
- This is the _instrinsic region_

- Therefore, _ideal behaviour_ will show clear separation between the temperature regimes:
![[Extrinsic semiconductor conductivity.png]]

### Equilibrium between electrons and holes
- Consider the [[#Statistical mechanics of electrons and holes|equilibrium for electron and hole concentrations]]
- For _extrinsic_ semiconductors, this equilibrium is _also established_, with a _similar equilibrium constant_
- Any _addition_ of _electrons/holes_ will _disturb_ the equilibrium and _push_ the equilibrium the other way
- Then, electrons/holes become the _majority charge carrier_

### Impurity bands
- When the _dopant concentration is high_

# Semiconductor devices
- Most devices use _extrinsic semiconductors_

## The p-n junction
- The _p-n diode_ consists of _n-type_ and _p-type_ semiconductors _attached_ in a particular direction
- If there is a voltage such that the _positive side_ is connected to the _p-type_ semiconductor, this is _forward bias_
	- Vice versa, there is a _reverse bias_

- If a _forward bias_ is applied, there is a _current flow_, as the _excess electrons_ in the _n-type_ material will _flow to the positive side_ and _recombine_ with the holes
	- Similarly, the _holes migrate to the negative side_
- The electrons are then _replenished_ by the battery
- If there is a _reverse bias_, _current cannot flow through the junction_ as the electrons and holes _stay_ on their respective sides

- If an _AC current_ is applied, it is _rectified_ as only one direction of current flow is _allowed_
![[p-n junction.png]]

### Electron bands in a p-n junction
- The Fermi energy can be approximated by the _chemical potential_
- At equilibrium, the _chemical potentials_ in the two semiconductors must be _equal_

![[p-n contact potential.png]]
- Let the two types of semiconductor intially come into _contact_, without any _external potential_
- There is a _flow of electrons_ from the _n-type_ to the _p-type_ semiconductor, as the _chemical  potential decreases_ across the junction
- There is a _build-up of opposite charges_ in the semiconductors
- In the _n-type_ semiconductor, there is a _build-up of positive charge_, which _lowers the energies of the bands_
- Similarly, in the _p-type_ semiconductor, there is a _rise in energies_
- This occurs until the _Fermi energies are equal_

- In the end, there is a _contact potential_ between the semiconductors
- On either side of the _contact point_, there is a _depletion region_ where the electrons and holes have _combined_

- The contact potential is of _similar magnitude to the band gap_
	- A $1\text{eV}$ band gap gives rise to $\sim1\,\text{V}$ contact potential

![[p-n junction forward bias.png]]
- When there is a _forward bias_, the external potential produces a _constant gradient in chemical potential_

![[p-n junction reverse bias.png]]
- When there is a _reverse bias_, the chemical potential gradient is _unfavourable_ as there are _no uphill electrons_ that can lower their energy

### Applications
- As electrons _recombine with holes_, they can _emit energy in the form of photons_
- This forms a _light-emitting diode_

- Meanwhile _solar cells_ will _create_ electrons and holes by _absorbing photons_
- The electrons and holes then flow and create a _current_

## Bipolar junction transistor
![[Bipolar junction transistor.png]]
- In the transistor, there are _two pieces of n-type_ semiconductor, with _one piece of p-type_ semiconductor in-between
- This is effectively _two p-n junctions_, one of which has a _forward bias_, while the other has a _reverse bias_
	- The side of the forward bias is the _emitter_, while the other is the _collector_
- The _p-type_ piece is known as the _base_, and has to be _thin_

- The _emitter_ will flow _from the emitter_ into the _base_, as well as the _collector_
- Define the _current ratios_:
$$\alpha=\frac{I_c}{I_e} \hspace{1cm} \beta=\frac{I_c}{I_b}$$
- From _current conservation_:
$$\beta=\frac{\alpha}{1-\alpha}$$
- As the base is _thin_, $I_c>>I_b$, hence $\beta>>1$
- $\beta$ is known as the _gain_ of the transistor

- By manipulating the _base current_, the transistor can be made into an _amplifier_

# Spectroscopic measurement of electrical properties

## Band gaps in intrinsic semiconductors
- An electron can _absorb energy_ to be _promoted_ from the _valence band_ into the _conduction band_
- There is a _minimum absoption energy_ corresponing to the _band gap_
![[Chemistry/Images/Electron promotion.png]]
- During promotion, _angular momentum_ of the system must be _conserved_
- This leads to an _angular momentum selection rule_:
$$\Delta l=\pm1$$
- Example: transition from _s-band_ to _p-band_
	- But no transition _within a band_

- There is also a _linear momentum selection rule_:
$$\bm{k}_f=\bm{k}_i+\bm{k}_\text{photon}$$
- $\bm{p}=\hbar\bm{k}$
- For photons, $E=pc$, and for a band gap of $\sim 1\text{eV}$, $k_p\approx 10^6\text{m}^{-1}$

### Direct band gaps
- For a typical crystal, $k$ at the _zone boundary_ $\approx 10^9\text{m}^{-1}$
- Therefore, for _vertical transitions_, one can _approximate_:
$$\Delta\bm{k}=\bm{k}_f-\bm{k}_i\approx 0$$
![[Chemistry/Images/Direct vs indirect band gaps.png]]

### Indirect band gaps and phonons
- For a material where the _lowest separation in energy_ matches the _band gap_, it is a _direct band gap_, where the lowest energy transition is _vertical_
	- Typically, $\ce{GaAs}$ has a direct band gap

- For some materials, the _lowest energy separation_ also has a _difference in $\bm{k}$
- These are _indirect band gaps_
- The difference in $\bm{k}$ are provided by _lattice vibrations_ known as [[Phonons]]

- A typical phonon has energy $\sim k_BT$
	- Typically _much smaller_ than band gap $(\approx \,25\text{meV})$
- Given the phonon has _speed_ $c_\text{phon}$:
$$k_\text{phon}\approx \frac{k_BT}{\hbar c_\text{phon}}$$
- The speed of a phonon is typically _the speed of sound_ in the material
- This gives a momentum $\sim 10^9\text{m}^{-1}$, matching the _wavevector at the zone boundary_

- _Indirect_ transitions involving phonons are typically _less likely_
- Transitions can _generate or eliminate phonons_
	- _Thermal processes_ can also change phonon number

- Typical absorption profile:
![[Indirect transitions.png]]
- Typically, for _light-emitting diodes_, one wants a _direct band gap_ material as the _creation of phonons wastes energy_

## Band gaps in extrinsic semiconductors
- Consider an _n-type semiconductor_:
![[Doped n-type bands.png]]
- The _donor levels_ are approximately [[#Donor levels|hydrogenic]]:
$$E_n=-\frac{R_\text{H, eff}}{n^2}=-\frac{R_H}{n^2}\frac{m_e^*}{m_e\epsilon_r^2}$$
- The _transition_ from level $1$ to level $n$:
$$h\nu_{1\to n}=R_H\frac{m_e^*}{m_e\epsilon_r^2}\left(1-\frac{1}{n^2}\right)$$
- In _actual experiments_, the frequencies are _about the right order of magnitude_, suggesting the hydrogenic model is _too simplistic_
	- Typical magnitude: $10^0\,\text{meV}$, in the _infrared_ spectrum
![[Donor level transitions.png]]

- At _higher temperatures_, one can see a _series of transitions in the optical region_ corresponding to excitations _from the valence band_ into the hydrogenic levels

## Excitons
- _Excitons_ consist of _electrons and holes bound together_
- They are created when electrons are _excited_ via _irradiation_, as the _electron and the created hole_ can be _bound together_ and occupy energy levels

- The exciton effectively has the _reduced mass_:
$$\mu=\frac{m_e^*m_h^*}{m_e^*+m_h^*}$$
- They can then occupy _hydrogenic energy levels_:
$$E_n=-\frac{R_{H,\text{eff}}}{n^2}=-\frac{R_H}{n^2}\frac{\mu}{m_e\epsilon_r^2}$$
- $R_{H,\text{eff}}$ is then the _effective binding energy_ of the exciton
![[Exciton levels.png]]
- At _low temperatures_, the exciton transitions can be observed:
$$h\nu_R=E_h-\frac{R_{H,\text{eff}}}{n^2}$$
![[Cu2O exciton spectrum.png]]
- A _low temperature_ is required such that the electrons are not simply promoted _into the conduction band_
![[GaAs exciton peak.png]]