# Presentation

## Intro slide
- Quick intro to projects
- What is project are you presenting?
- Thank the TCM group?

## Background: Multi-gap topology and frame charges
### Multi-gap topology
- Real multi-band Hamiltonian
	- Single-gap: two bands (Berry curvature, Chern number, e.g. IQHE)

- Each band: _one quaternion_ $(i,j,k)$
	- _Frame_ charge: due to the _frame_ of _real eigenvectors_
	- Real eigenvector frame -> gauge freedom -> encircling nodes
- There is a _gauge freedom_ in determining signs
	- However, _relative sign_ is _gauge-independent_

### Braiding of frame charges
- _Braiding_ around a node of an adjcaent gap: equivalent to _conjugation_

- Implementation: _band inversion_
### Frame charges and Euler class
- Euler curvature and Euler class
	- Analagous to Berry curvature in single-gap topologies
	- A _fragile topology_

- Euler class: a _topological invariant_ for a fragile multi-band topology
	- Analagous to _Chern number_
	- Order of _band dispersion_: linear VS quadratic
- Stability of charges
	- $\chi=0$: equivalent to _no charges_

### Dirac strings
- For a _consistent global topological configuration_ between adjacent gaps
	- _Gauge fixing_ for _all gaps_

- _Sign_ of eigenvector must _flip_ over the Dirac string
	- A $\pi$ disinclination line in Berry phase between 2 nodes (branch cut?)

### Transition
- Electrons: have to find bands near the Fermi-level
- Hence: phonons! (automatically satisfies $\mathcal{T}$ symmetry)
	- One can get _band crossings_ from _different representations_

## $\ce{ Zr_{2}O_{3} }$

### Structure and bands
- _Ab initio_ calculations
 - VASP for force constants
	 - Structure optimisation: by _relaxing_ lattice constants and atomic coordination
	 - Passivation atoms: _hydrogen_
	 - Using a _finite difference method_
 - Phonopy for dispersion
	 - VASP only computes frequencies near $\Gamma$

- Change in band structure: 
	- Perpendicular electric field (doping), as the atoms _respond differently_
	- Strain

- Focus on a _group of bands_
	- Many bands, rich phenomena
	- Is _isolated_ from other gaps

### Determining Euler classes
- Calculate Euler classes in _patches_
- Draw Dirac strings
- Consistency with translational symmetry and continuity with other fields

- There are _multiple equivalent configurations_ due to _gauge freedom_
	- Only _node annihilation/creation_ is gauge-invariant

- Representation: $K$ in centre as elimination takes place on BZ boundaries

- Red nodes: _hidden_ under purple, actually along $\Gamma-K$

### Braiding: 1
- A simple two-gap process (red, purple)

- Red _linear_ nodes leave $K$
- The _red and purple quadratic nodes swap_ (split quadratic nodes then braid)
- _After passing Dirac string_, they are all of the _same charge_
- A _band inversion_ at $\Gamma$ leads to nodes of _opposite charges_
- Charges are _transferred_ from $\Gamma-K$ direction to $\Gamma-M$ direction
- They _annihilate_ at $M$

- _No change_ in blue and yellow nodes
### Braiding: 2
- A two-gap process

- Blue nodes _cross Dirac string_ going towards $M$
- _Band inversion_ near $M$ generates _nodes along_ $M-K$
- Nodes annihilate to leave $M-K$ nodes
- Blue nodes _braid with yellow_ at $K$ 
- Yellow nodes start to leave $K$

### Braiding: 3
- A four-gap process

- Red nodes _merge_ to become linear at $K$
	- Band inversion going the _other way_
- Purple nodes go along $M-K$
- Blue braids with green and _annihilate_ (green also moves towards $\Gamma$)
- The _quadratic nodes swap_
- _Oppositely charged green and puple nodes_ are created then _braid_ (green faster than purple)

- Purple nodes cross Dirac string to _annihilate_ at $M$

- Final state: _red and green nodes_ are _not adjacent_, braiding is finished

## Future
- _Bilayers_

- Accounting for strain (_from substrate_)
- Two degrees of freedom: precise control of nodes? Computing?

- Optical multi-band systems
# Interview

## Alter-magnetism
- A combination of:
	- _Ferromagnetic_ behaviour: $\mathcal{T}-$_symmetry breaking_, along with _spin-split bands_ in $k-$space
	- _Anti-ferromagnetic_ behaviour: _anti-parallel_ (compensated) _magnetic ordering_ in _real space_

- To describe this behaviour, one needs a formalism for _symmetry operations which combine generally different operations in real and reciprocal space_

- _Altermagnetism_ is described by behaviour in _both_ real and reciprocal spaces:
	- Real space- _Compensated magnetic order_ with _opposite spin sublattices_, which are related by _crystal rotation symmetries_
	- Reciprocal space- A _spin polarisation order_, which reflects the _same rotation symmetry_

- In terms of _band structure_, one gets _broken TRS_ and an _alternating momentum-dependent sign_ of spin-splitting:
![[Altermagnetism.png]]

- Significance: allows for _d-wave magnetism_, analagous to _d-wave superconductivity_