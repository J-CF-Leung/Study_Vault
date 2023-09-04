- All structures are described using a _lattice_, and a _basis_

- A _lattice_ is an _infinite periodic array of discrete points_, which are all _equivalent_
	- Equivalence: the lattice _"looks the same"_ from all of the points
- Mathematically, it is an array of _delta functions_
- The points are _not necessarily where the atoms are_

- The _basis_ specifies a "repeat unit" imposed on _every lattice point_
- It can specify the _positions of atoms_, or functions such as _electron density_

- Mathematically, the crystal is a _convolution_ of the lattice and the basis

# Bravais Lattices
- In _three-dimensional space_, there are 14 possible lattices, known as _Bravais lattices_
- They can be categorised into 7 _crystal systems_
- There are also types corresponding to the _placement_ of atoms:
	- Primitive/Simple $(P)$
	- Body/Volume-centred $(I)$
	- Face-centred, on all faces $(F)$
	- Face-centred, on a single face/base-centred $(A,B,C)$

![[All Bravais lattice types.png]]

## Unit cells
- Overall, any _repeating unit_ in a lattice that can _tessellate_ all space with the pattern is known as a _unit cell_
- Unit cells are _not unique_, so one often takes _conventional unit cells_ that take _simple shapes_ and _reflect the crystal system_

- Example: the _cubic unit cells_ for the cubic crystal systems
![[Cubic unit cells.png]]

- A unit cell that only contains _one lattice point_ is known as a _primitive unit cell_
	- Example: the primitive cubic unit cell above has $1/8$ of a lattice point _per corner_
	- Example: the face-centred cubic unit cell above has 4 lattice points

## Wigner-Seitz cells
- The _Wigner-Seitz construction_ produces _unique, primitive unit cells_
- It finds a _locus of points closer in space from a particular lattice point than any other_
- Mathematically, this is known as _Voronoi decomposition_
![[Wigner-Seitz unit cell.png]]


# Vectors and planes

## Lattice vectors
- A 3D unit cell is defined by three _basis vectors_ $\bm{a}$, $\bm{b}$, and $\bm{c}$
- Then, one can construct any _vector_:
$$\bm{r}=u\bm{a}+v\bm{b}+w\bm{c}$$
- If $u,v,w$ are _integers_, this is a _lattice vector_, which goes between two _lattice points_

- The lattice vector is denoted:
$$[u\,v\,w]$$
- If the coefficients are _negative_, they are denoted with a _bar_ (e.g. $[1\,\bar{1}\,0]$)

## Planes and Miller indices
- Meanwhile, _sets of parallel planes_ can be defined by _Miller indices_ $h,k,l$
- Assume _one plane passes through the origin_
- Then, let the next plane _cut the axes_ at the points:
$$\frac{\bm{a}}{h},\frac{\bm{b}}{k},\frac{\bm{c}}{l}$$
- If a plane is _parallel to an axis_, that value is zero
- Then, the _set of planes_ is denoted:
$$(h\,k\,l)$$
- If a set of planes are _symmetrically related_, the entire set is denoted $\{h\,k\,l\}$

# The reciprocal lattice

## 1 dimension
- Assume a $1$D crystal
- Let there be a _periodic function_ $f(x)=f(x+a)$, describing a property of the crystal
- It can then be written as a _Fourier series_:
$$f(x)=\sum_{h=-\infty}^\infty C_h\exp(ik_hx)$$
- The wave vectors $k_h$ are _uniformly separated points_, in a one-dimensional wave vector space, also known as the _$k-$space_, or _reciprocal space_
$$k_h=\frac{2\pi h}{a}$$
- The _set of points_ is then known as the _reciprocal lattice_

## 3 dimensional orthorombic lattice
- Then, let there be a lattice with $\pi/2$ between axes and $a\neq b\neq c$
- Let the associated _wave vectors_ be:
$$k_h=\frac{2\pi h}{a} \hspace{1cm} k_k=\frac{2\pi k}{b} \hspace{1cm} k_l=\frac{2\pi l}{c}$$
- A periodic function is then described by:
$$\begin{aligned}f(\bm{r})&=\sum_{h,k,l=-\infty}^\infty C_{hkl}\exp[i(k_hx+k_ky+k_lz)] \\ &=\sum_{h,k,l=-\infty}^\infty C_{hkl}\exp(i\bm{k}_{hkl}\cdot\bm{r}) \end{aligned}$$
- The _set of wave vectors_ $\bm{k}_{hkl}=(k_h,k_k,k_l)$ form a 3D _reciprocal lattice_

- When referring to the _reciprocal lattice vectors_, one uses the notation $\bm{G}_{hkl}$
- $\bm{G}_{hkl}$ can _join any two points in the reciprocal lattice_

## The general case
- Let a lattice have the _lattice vectors_ $\bm{a},\bm{b},\bm{c}$
- The corresponding _reciprocal lattice vectors_ are given by:
$$\bm{A}=2\pi\frac{\bm{b}\wedge\bm{c}}{\bm{a}\cdot(\bm{b}\wedge\bm{c})} \hspace{1cm} \bm{B}=2\pi\frac{\bm{c}\wedge\bm{a}}{\bm{a}\cdot(\bm{b}\wedge\bm{c})} \hspace{1cm} \bm{C}=2\pi\frac{\bm{a}\wedge\bm{b}}{\bm{a}\cdot(\bm{b}\wedge\bm{c})}$$
- The _reciprocity_ is expressed as follows:
	$$\bm{A}\cdot\bm{a}=2\pi \hspace{1cm}\bm{A}\cdot\bm{b}=\bm{A}\cdot\bm{c}=0$$
	- And so on for other reciprocal lattice vectors

- _Any reciprocal lattice vector_ is then expressed as:
$$\bm{G}_{hkl}=h\bm{A}+k\bm{B}+l\bm{C}$$
- Any function can then be described with:
$$f(\bm{r})=\sum_{h,k,l=-\infty}^\infty C_{hkl}\exp(i\bm{G}_{hkl}\cdot\bm{r})$$
- If $\bm{r}$ is a _lattice vector_, the dot product gives an _integer multiple of $2\pi$_, giving the required _periodicity_ in the function

- If the lattice is _non-orthorombic_, then the _reciprocal lattice_ will also be _non-orthorombic_, and the reciprocal lattice vector will _not necessarily be parallel with the corresponding lattice vector_

- One can also _divide_ the reciprocal lattice into its own _Wigner-Seitz cells_, which are then named the _first Brillouin zone_

# Diffraction
- Let a beam with wave-vector $\bm{k}$ be _incident_ on a specimen, then be _elastically scattered_ with out-going wavevector $\bm{k}_f$:
![[Diffraction from crystal.png]]
- The _outgoing_ beam has the highest amplitude when $(\bm{k}_f-\bm{k}_i)\cdot\bm{r}=2n\pi$
- Hence, _diffraction peaks_ are seen when:
$$\bm{k}_f-\bm{k}_i=\bm{G}_{hkl}$$
- In other words, for a diffraction peak, the _difference in wave-vector_ must match a _recriprocal lattice vector_

- This condition can be expressed using the _Ewald sphere_:
![[Ewald sphere.png]]
- The diffraction peak is seen when the sphere _intersects two reciprocal lattice points_

- In _single-crystal diffraction_, all part of the crystal have _one uniform orientation_
- They form _diffraction spots_, and is very _precise_

- In _powder diffraction_, all parts of the sample have _different orientations_
- They form _diffraction rings_
![[Diffraction methods.png]]