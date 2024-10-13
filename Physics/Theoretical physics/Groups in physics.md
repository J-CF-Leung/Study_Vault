- Systems often have _symmetries_: transformations that _leave the physical laws unchanged_
- There can be _discrete_ symmetries like _parity_:
$$V(\boldsymbol{r})=V(-\boldsymbol{r})$$
- They can also be _continuous_, like _rotational symmetry_:
$$V(\boldsymbol{r})=V(|\boldsymbol{r}|)$$
- Sets of symmetries must form a [[Foundations of Group Theory|group]]

## Unitarity and anti-unitarity
- Let a _transformation_ take states $\ket{\Psi}$ to $\ket{\Psi'}$
- For it to be a _symmetry_, for _any two states_ $\ket{\Psi}$ and $\ket{\Phi}$:
$$\left| \braket{ \Psi | \Phi }  \right|^{2} = \left| \braket{ \Psi' | \Phi' }  \right|^{2} $$
- This is satisfied when the transformation is _unitary_:
$$\mathcal{U}^{\dagger}\mathcal{U}=1$$
- It can also be _anti-unitary_ (e.g. _time reversal_)

# Lie groups
- Lie groups describe _continuous symmetries_
	- The transformations depend on a _continuous parameter_
- Examples: _translations_, and _rotations_

## Translation group
- Translations:
$$\Psi'(\boldsymbol{r},t)=\Psi(\boldsymbol{r}+\boldsymbol{a},t)=\mathcal{U}_{T}(\boldsymbol{a})\Psi(\boldsymbol{r},t)$$
- It satisfies _composition_:
$$\mathcal{U}_{T}(\boldsymbol{b})\,\mathcal{U}_{T}(\boldsymbol{a})=\mathcal{U}_{T}(\boldsymbol{a}+\boldsymbol{b})$$
- It forms an _Abelian group_ (translations _commute_)

- Consider an _infinitesimal change_ in the parameter:
$$\boldsymbol{a}\to\boldsymbol{a}+\delta \boldsymbol{a}$$
- Then _expanding_ in $\delta \boldsymbol{a}$:
$$\Psi(\boldsymbol{r}+\boldsymbol{a}+\delta \boldsymbol{a})=(1-\delta \boldsymbol{a}\cdot \nabla)\Psi(\boldsymbol{r}+\boldsymbol{a})$$
- From this, one gets:
$$\frac{d}{d\boldsymbol{a}}\mathcal{U}_{T}(\boldsymbol{a})=-\nabla \mathcal{U}_{T}(\boldsymbol{a}) \implies \mathcal{U}_{T}(\boldsymbol{a})=\exp(-\boldsymbol{a}\cdot \nabla)$$
- Define the _Hermitian operator_:
$$\boldsymbol{D}=-i\nabla$$
- The operator can be written as:
$$\mathcal{U}_{T}(\boldsymbol{a})=\exp(-i\boldsymbol{a}\cdot \boldsymbol{D})$$
- $\boldsymbol{D}$ is the _generator of spatial translations_
	- $-i\hbar\nabla$ is _momentum_

## General Lie groups
- In _general_, a Lie group can be characterised by $n$ parameters:
$$g(a_{1},a_{2},\dots a_{n})=\exp\left( -i\sum_{j} a_{j}X_{j}\right)$$
- It has $n$ _generators_ $X_{j}$
- It is a _Lie group of dimension_ $n$

## Lie algebras
- A _Lie algebra_ is determined by:
$$[X_{j},X_{k}]=i\sum_{\alpha}^{n}f_{jk\alpha}X_{\alpha}$$
- $f_{jk\alpha}$ are the _structure constants_
- Example: Pauli spin matrices
$$[\sigma_{i},\sigma_{j}]=i\varepsilon_{ijk}\sigma_{k}$$

- The _subgroup_ of generators that _commute_ with each other is the _rank_ of the Lie group

# Constants of motion
- Let a symmetry $g$ leave a system's _time dependence unchanged_:
$$g^{-1}\exp\left( -\frac{iHt}{\hbar} \right)g\ket{\psi}=\exp\left( -\frac{iHt}{\hbar} \right)\ket{\psi}  $$
- This means $H$ and $g$ _commute_:
$$[H,g]=0$$
- It must then commute with the _generators_:
$$[H,X_{g}]=0$$
- Therefore, $X_{g}$ are _conserved charges_

- Example: for translations
$$\boldsymbol{D}=-i\nabla$$
- Example: _rotations_ in 3D
- Rotate $\boldsymbol{r}$ by angle $\theta$ around the $z-$axis:
$$R\left( \theta \hat{z} \right)=\pmatrix{\cos\theta&-\sin\theta&0 \\ \sin\theta&\cos\theta&0\\0&0&1}$$

- Rotation matrices are _orthogonal_ $(RR^{T}=1)$, with $\mathrm{\det}=1$
	- No inversions
- They are elements of the $SO(3)$ group

- The _generator_ of $z-$rotations:
$$R\left( d\theta \hat{z} \right)=\pmatrix{}=1-id\theta X_{z}$$
$$X_{z}=iA_{3}$$
- There are two other generators:
$$X_{x}=iA_{1}\hspace{1.5cm}X_{y}=iA_{2}$$
- The _general rotation_:
$$R\left( \theta \hat{n} \right)=\exp\left( -i\theta \hat{n}\cdot \boldsymbol{X} \right)$$
- Rotations are _non-Abelian_:
$$[X_{j},X_{k}]=i\varepsilon_{jk\alpha}X_{\alpha}$$
- It is a _3-dimensional_ Lie group
- It has _rank_ $1$
	- Only rotations _about the same axis_ will commute

- Its _Lie algebra_ is _isomorphic_ to $SU(2)$, as the latter has the _same commutation relation_
	- Spin-1/2 particle: $SU(2)$ Hamiltonian, spin described by $SO(3)$ matrix

# Representations
- Representations matrices that _fulfill composition_:
$$U(R_{1})U(R_{2})=U(R_{1}R_{2})$$
- They must also _satisfy_ the _group algebra_

## Representations of SO(3)
- Angular momentum: _representation_ of the rotation generators

- Representations can have _different dimensions_
- Some can be written as _block diagonals_
- The representation $L^{2}$ is _reducible_
- Each value of $l$ for $L^{2}=\hbar^{2}l(l+1)$ is _its own irreducible representation_

- The _zero representation_ $l=0$ is _trivial_, as each rotation matrix is simply $1$
- Each representation has _dimension_ $2l+1$

- $l=1$ is the _fundamental representation_ (smallest faithful representation)

- If angular momentum is _conserved_, then _symmetry multiplets_ are formed, _degenerate subspaces_ spanned by _states_ of the same energy

## SU(2)
- The group of $2\times2$ _unitary matrices_
- They have the _same generators_ as $SO(3)$
	- Said to be _homeomorphic_

- Each $SO(3)$ matrix can be _mapped_ into _two distinct_ $SU(2)$ matrices
	- Rotations of $\theta$ and $\theta+2\pi$

## SO(4)
- Corresponds to the _hydrogen atom_:
	- Full spatial rotational symmetry
- From symmetry multiplets, energies must be specified by _three quantum numbers_

## Lorentz group
- The Lorentz group is $SO(1,3)$
- Represents all _spacetime transformations_, which _preserve_ the _interval_