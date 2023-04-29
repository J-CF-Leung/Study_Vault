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

![[Bravais lattices.png]]

## Cubic unit cells
![[Cubic unit cells.png]]


## Wigner-Seitz cells
- The _Wigner-Seitz construction_ produces _unique, primitive unit cells_
- It finds a _locus of points closer in space from a particular lattice point than any other_

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
- The wave vectors $k_h$ are _uniformly separated points_, in a one-dimensional wave vector space, also known as the _$k-$space_
$$k_h=\frac{2\pi h}{a}$$
- The _set of points_ is then known as the _reciprocal lattice_

## 3 dimensional orthorombic lattice
- Then, let there be a lattice with $\pi/2$ between axes and $a\neq b\neq c$
- A periodic function is then described by:
$$\begin{aligned}f(\bm{r})&=\sum_{h,k,l=-\infty}^\infty C_{hkl}\exp[i(k_hx+k_ky+k_lz)] \\ &=\sum_{h,k,l=-\infty}^\infty C_{hkl}\exp(i\bm{k}_{hkl}\cdot\bm{r}) \end{aligned}$$
- The set of wave vectors 

## The general case
- Let a lattice have the _lattice vectors_ $\bm{a},\bm{b},\bm{c}$
- The corresponding _reciprocal lattice vectors_ are given by:
$$\bm{A}=2\pi\frac{\bm{b}\wedge\bm{c}}{\bm{a}\cdot(\bm{b}\wedge\bm{c})} \hspace{1cm} \bm{B}=2\pi\frac{\bm{c}\wedge\bm{a}}{\bm{a}\cdot(\bm{b}\wedge\bm{c})} \hspace{1cm} \bm{C}=2\pi\frac{\bm{a}\wedge\bm{b}}{\bm{a}\cdot(\bm{b}\wedge\bm{c})}$$

# Diffraction
