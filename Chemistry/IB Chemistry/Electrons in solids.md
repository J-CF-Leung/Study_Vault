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

## Population of energy levels
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

- If the _Fermi level_ is within the band gap, for _low temperatures_, electric conduction is _impossible_, as the electrons _cannot be promoted_

- In the _first band_, the _number of available states_ is:
$$N_1=\frac{2\pi}{a}\frac{\mathcal{L}}{2\pi}=\frac{\mathcal{L}}{a}$$
- If each unit cell has _one valence electron_, they would fill $\mathcal{L}/(2a)$ states, which _fills up half of the first band_, therefore the material will be a _metallic conductor_
- If each unit cell has _two valence electrons_, this _completely fills up the first band_, making the material an _insulator_

- Hence, this model predicts _group 2 metals are insulators_
- Therefore, one must consider _more dimensions_ for a viable model

## Band gaps in 2 dimensions
![[2D NFEG dispersion curve.png]]

- In 2 dimensions, the _bands corresponding to different $\bm{k}$ directions_ will _overlap_, as their gaps are at _different energies_
- The electrons will _start filling the second band before the first one is completely filled_



# The tight-binding model

# Semiconductors