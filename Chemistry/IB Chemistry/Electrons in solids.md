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

## The ionic model
- For ionic crystals, the _lattice energy_ is defined as the _energy needed to dissociate a solid lattice into widely separated gaseous ions_
- It must be deduced from a _thermodynamic cycle_
	- Using _ionisation energies, electron affinities, and enthalpies of formation_

### Electrostatic interactions
- Assume a simple _one-dimensional lattice_:
![[1D ionic lattice.png]]
- Considering the electrostatic energy arising from interactions with _one ion_, then multiplying by _one mole_:
$$E_\text{electrostatic}=-2N_A\frac{z_+z_-e^2}{4\pi\epsilon_0a}\left(1-\frac{1}{2}+\frac{1}{3}-\dots\right)$$

- Define the dimensionless _Madelung constant_ $\mathcal{A}$ such that:
$$E_\text{electrostatic}=-\frac{N_A\mathcal{A}z_-z_+e^2}{4\pi\epsilon_0a}$$
- The Madelung constant is a _function of the lattice arrangement_
- This model _generalises to 3D_, with different values of $\mathcal{A}$

![[Madelung constant table.png]]

### Finding lattice enthalpy
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
### Ionic radii
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

# The nearly-free electron gas

# The tight-binding model

# Semiconductors