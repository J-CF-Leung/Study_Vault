- Bonding relies heavily on the [[Symmetry in molecules]]

# Qualitative MO Diagrams
- MOs are mainly obtained from the _linear combination of atomic orbitals_ (LCAO) method, based on the [[Molecular quantum mechanics#The Variational Principle|Variational Principle]]
- However, some linear combinations may _not be symmetry allowed_ as they have [[Symmetry in molecules#Overlap integrals|zero overlap]]

- Overall, it is a better strategy to _classify orbitals according to symmetry_, creating _symmetry orbitals_, which then overlap to create MOs

## Basic properties

### Two atomic orbitals
- When two AOs interact, they form a _bonding_ MO which is _lower in energy_ then both of the AOs, airising from _in-phase overlap_
- They also form an _antibonding_ MO which is _higher in energy_ than both AOs, arising from _out of phase overlap_

- The _greater the energy separation_ between the AOs, the _smaller the shift in energy_ between the _lower AO_ and the _bonding MO_, and likewise for the higher energy orbitals

- The _greater contribution_ to the MO is _from the AO closest to it in energy_
![[AOs overlapping.png]]

### More atomic orbitals
- If there are _several AOs_ interacting, the _number of MOs is the same as number of AOs_

- _One_ MO will lie _lower in energy than the lowest energy AO_
- Likewise, _one_ MO will be _higher in energy than the highest energy AO_
- All other MOs will _lie between both extremes_

- The _greatest contribution_ to each MO is still _from the AO closest in energy_
![[Many MOs.png]]

- When _sketching_ MOs, one can _shade_ MOs to indicate _phase_, and use _size_ to indicate _contribution_

## Symmetry orbitals
- A _symmetry orbital_ (SO) is a _linear combination_ of other orbitals, such that it _transforms as a single irreducible representation_

- The method:
1. Find the _point group_ the molecule transforms as
2. Choose a _set of AOs_ to construct SOs from, typically all _from the same type of atom_
3. Find the _representation_ they collectively transform as
4. _Reduce_ the representation
5. _Construct_ orbitals that transform as each _irreducible representation_, based on _analogies with Cartesian functions_
6. _Normalise_ the orbitals

- The reducible representation commonly includes the _totally symmetric IR_, which would involve _all orbitals in phase_

- For _multi-dimensional irreducible representations_, one will need to construct a _set of symmetry orbitals_, each of which transform as one dimension of the IR

### Example: BH3
- Point group: $D_{3h}$
![[D3h character table.png]]
- Start with the _three hydrogen $1s$ orbitals_
![[BH3 hydrogen orbitals.png]]
- It can be found that these three orbitals transform as $A_1'\oplus E'$

- $A_1'$ is the _totally symmetric_ IR, so it involves _all orbitals combined in-phase_
- $E'$ is a _two-dimensional IR_, so it produces _one SO transforming like $x$_, and _one SO transforming like $y$_
- This gives the three orbitals: 
$$\displaylines{\theta_{A_1'}=\frac{1}{\sqrt{3}}(s_A+s_B+s_C) \\ \theta_{E',x}=\frac{1}{\sqrt{2}}(s_B-s_C) \\ \theta_{E',y}=\frac{1}{\sqrt{6}}(2s_A-s_B-s_C)}$$
![[BH3 hydrogen SOs.png|450]]

- Next, there are the $2s$ along with three $2p$ _boron AOs_
- The $2s$ orbital transforms as $A_1'$
- The $2p_z$ transforms as $A_2''$, while $(2p_x,2p_y)$ transforms as $E'$

- Then, _SOs with the same symmetry overlap_ to produce corresponding _bonding and anti-bonding orbitals_
- Meanwhile, as $\text{B } 2p_z$ is the only one with $A_2''$ symmetry, it produces a _non-bonding orbital_
![[BH3 SO overlap.png|600]]

- Overall, the _totally symmetric_ IR gives MOs that give _more overlap_
	- Can be justified with the [[#Hückel Approximations]]
- Then, one can make this _qualitative MO diagram_
![[BH3 MO diagram.png|500]]

### Example: BF3 and local coordinate systems
- Depending on the _symmetry_ of a molecule, instead of a coordinate system applying to all molecules, one can use _local_ coordinates for each atom

- In $\text{BF}_3$, using a universal one, the $2p_x$ and $2p_y$ AOs of different $\text{F}$ atoms _do not transform into each other_
![[BF3 universal coords.png]]

- Instead, classify them into _radial_ and _tangential_ sets:
![[BF3 local coords.png]]

- Constructing symmetry orbitals then proceeds as normal:
![[BF3 example SOs.png]]

## Projection operator
- Symmetry orbitals may not necessarily form an analogy with _Cartesian functions_
- Example: $2p$ orbitals on $\text{BF}_3$
![[BF3 SO.png|350]]

- Let the set of basis orbitals be $\{\phi_i\}$, typically being AOs
- Let the SO transforming as IR $k$ be $\theta^{(k)}$
- The SO can be found by applying the _projection operator_ $\hat{P}^{(k)}$ to a basis function:
$$\displaylines{\theta^{(k)}=\hat{P}^{(k)}\phi_i \\ \hat{P}^{(k)}=\frac{1}{n_R}\sum_R[\chi^{(k)}(R)]\hat{R}}$$
- $\hat{R}$ is a _symmetry operation_ in the group, $n_R$ is the _number of operations_, and $\chi$ is the _character_ of the operation in the representation $k$

- The sum is over _operations_, so operations _in the same class_ must be considered _separately_
- If a basis orbital is _not present in the SO_, then the operator gives _zero_

# Transition metal complexes
- _Transition metals_ can form many _coordination compounds/complexes_
- There is a _central metal atom_ surrounded by a number of _ligands_, which are often _anions_ or _small molecules_
- The ligands have a _ligating atom_ which _interacts directly_ with the metal

- Considering the _central atom_ and the _ligating atoms_, they often have a _high amount of symmetry_

- Common types:
	- _Octahedral_, often with point group $O_h$
	- _Square planar_, often with point group $D_{4h}$
	- _Tetrahedral_, often with point group $T_d$

## Octahedral complexes with $\sigma$ donors

## Field splitting and spin complexes

## Magnetic properties

## Thermodynamic properties

## Effect of $\pi$ interactions

## Spectrochemical series and the 18-electron rule

## Tetrahedral complexes

## Square planar complexes

# Linear molecules

## Symmetry orbitals

## MO diagrams

## Molecular term symbols

# Hückel Approximations

## LCAO method and secular equations

## Using symmetry

### Example: Cyclobutadiene

# Rings

# Chains

