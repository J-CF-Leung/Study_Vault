## Groups
- Definition of a [[Foundations of Group Theory|group]]- a _set_ of elements $g_{1},g_{2},\dots \in G$ with _group product_ $g_{1}g_{2}$\
- They must satisfy-
	1. _Closure_: The result of taking a _product_ between any two elements of the group must _also be an element_ of the group $$g_1\in G \hspace{1cm} g_2\in G \Longrightarrow g_1g_2\in G$$
	2. _Identity_: There must exist a single _identity element_, denoted by $I$, such that, for _every element_ $g\in G$ $$Ig=g \hspace{1cm} gI=g$$
	3. _Inverse_: For every element $g\in G$, there must exist an _inverse_ of that element $g^{-1}\in G$ such that $$gg^{-1}=I=g^{-1}g$$
	4. _Associativity_: For any 3 elements $g_1,g_2,g_3\in G$, $$(g_1g_2)g_3=g_1(g_2g_3)$$
- A group is _commutative_, or _Abelian_ if:
$$g_{1}g_{2}=g_{2}g_{1}$$

# Symmetries in physics
- Systems often have _symmetries_: transformations that _leave the physical laws unchanged_
- There can be _discrete_ symmetries like _parity_:
$$V(\boldsymbol{r})=V(-\boldsymbol{r})$$
- They can also be _continuous_, like _rotational symmetry_:
$$V(\boldsymbol{r})=V(|\boldsymbol{r}|)$$
- Sets of symmetries must form a [[Foundations of Group Theory|group]]

## In classical mechanics
- Symmetries often lead to _conserved quantities_
- Example: in _classical mechanics_, space-time translation leading to conservation of momentum and energy
	- _Noether's Theorem_: for each symmetry, there is a _conserved quantity_
	![[Analytical classical mechanics#Symmetries and Noether's Theorem]]
## In quantum mechanics
- In _quantum mechanics_, let a _transformation_ $\mathcal{U}$ take states $\ket{\Psi}$ to $\ket{\Psi'}$
- For it to be a _symmetry_, for _any two states_ $\ket{\Psi}$ and $\ket{\Phi}$, the _inner product_ must be _preserved_, up to a _phase_, meaning:
$$\begin{align}
\ket{\Psi'}&=\exp[i\theta(\Psi)]\ket{\Psi}  \\
\left| \braket{ \Psi | \Phi }  \right|^{2} &= \left| \braket{ \Psi' | \Phi' }  \right|^{2} 
\end{align}$$
>[!Wigner's Theorem]
>_Symmetry operators_ are either:
>1. _Linear_ and _unitary_
>2. _Anti-linear_ and _anti-unitary_
### Unitarity and anti-unitarity
- _Unitary_ operator:
$$\mathcal{U}^{\dagger}\mathcal{U}=1$$
- An _anti-unitary_ and _anti-linear_ operator (e.g. _time reversal_):
$$\begin{align}
UU^{\dagger}&=1 \\
U(\alpha \ket{\Psi}+\beta \ket{\Phi}  )&=\alpha^{*}U\ket{\Psi}+\beta^{*}U\ket{\Phi}  \\
\braket{ U\Psi | U\Phi }&=\braket{ \Psi |\Phi  } ^{*}
\end{align}$$

- For a _time-independent_ Hamiltonian $H$:
$$\ket{\Psi(t)}=\exp(-iHt)\ket{\Psi(0)}  $$
- The wave function $U\ket{\Psi(t)}$ must remain _normalised_, and one gets:
$$[U, H]=0$$
- Analagous to classical mechanics:
	- If $[p,H]=0$, then $[x,H]\neq 0$: momentum is _conserved_, and $H$ _cannot be only explicitly dependent on position_, or in other words, it is _invariant under translation_, with translation operator $\exp(ipa)$
	- If $H$ is _rotationally symmetric_, then _angular momentum_ is conserved
# Lie groups
- _Manifold_: space which _looks like Euclidean $\mathbb{R}^{n}$_ in a _small neighbourhood_
- _Differentiable manifold_: satisfies smoothness conditions

- _Lie group_: a _differentiable manifold_ $G$, along with a _binary operation_ $\cdot$, such that the _group axioms hold_, and $\cdot$ is a _smooth operation_

- Lie groups describe _continuous symmetries_
	- The transformations depend on a _continuous parameter_
- Examples: _translations_, and _rotations_

## The general linear group
- Take the _general linear group_ $GL(n,\mathbb{F})$, the group of _invertible_ $n\times n$ matrices over field $\mathbb{F}=\mathbb{R}$ or $\mathbb{C}$, with the _operation_ of _matrix multiplication_
$$GL(n,\mathbb{F})=\{M \in \mathrm{Mat}_{n}(\mathbb{F}) | \det M\neq0\}$$
- The _dimension_ of $GL(n,\mathbb{R})$ is $n^{2}$
	- The requirement of $\det M\neq 0$ does not restrict dimensionality
- For $GL(n,\mathbb{C})$, the _real dimension_ is $2n^{2}$ (real and imaginary arguments), while the _complex dimension_ is said to be $n^{2}$

### Subgroups
- The _subgroups_ of $GL(n,\mathbb{F})$:
- The _special linear group_, which has dimensionality $n^{2}-1$: $$SL(n,\mathbb{F})=\{M\in GL(n,\mathbb{F})| \det M=1\}$$
- The _orthogonal group_, where $\det M=\pm{1}$$$O(n)=\{M \in GL(n,\mathbb{R})|M^{T}M=\mathbb{I}\}$$
- The _special orthogonal group_: $$SO(n)=\{M \in O(n)|\det M=1\}$$
- The _pseudo-orthogonal group_: define an $(n+m)\times(n+m)$ metric matrix: 
$$\displaylines{\eta=\pmatrix{I_{n}&0\\0&-I_{m}} \\
O(n,m)=\{M \in GL(n+m,\mathbb{R})|M^{T}\eta M=\eta\}}$$
- One can also define $SO(n,m)$ with $\det M=1$
- From the definition of the metric, one sees that these matrices _preserve the scalar product_ $v_{2}^{T}\eta v_{1}$ for $v_{1},v_{2} \in \mathbb{R}^{n+m}$
	- Example: in _special relativity_, $O(1,3)$ is the _Lorentz group_, with $M$ describing _boosts_ and _rotations_

- The _unitary group_:$$U(n)=\{M\in GL(n,\mathbb{C})|M^{\dagger}M=\mathbb{I}\}$$
- The _pseudo-unitary group_:$$U(n,m)=\{M \in GL(n+m,\mathbb{C})|M^{T}\eta M=\eta\}$$
- The _symplectic group_: define a fixed, anti-symmetric $2n\times{2}n$ matrix $$\Omega=\pmatrix{0&I_{n}\\-I_{n}&0}$$ $$Sp(2n,\mathbb{R})=\{M\in GL(2n,\mathbb{R})|M^{T}\Omega M=\Omega\}$$
- One can show that $\det(M)=1$ in $Sp(2n,\mathbb{R})$ using the _Pfaffian_ of $\Omega$ $$\mathrm{Pf}(A)=\frac{1}{2^{n}n!}\varepsilon_{i_{1}i_{2}\dots i_n}A_{i_{1}i_{2}}A_{i_{3}i_{4}}\dots A_{i_{2n-1}i_{2n}}$$
## Groups as transformations
- Define _actions_ of a group element $g \in G$ on a set $X$
	- $X$ might be $G$ itself, or vectors in a vector space

- The _left action_ of $G$ on $X$ is the map:
	- Compact notation - $\forall g \in G$, associate a map $g:X\to X$ such that $g(x)=gx$
$$L: G\cdot X \to X$$
- For the identity of $G$, $e$:
$$L(e, x)=x$$
- Composition:
$$L(g_{2},L(g_{1},x))=L(g_{2}g_{1},x) \quad \forall x \in X \quad \forall g_{1},g_{2} \in G$$


- The _right action_ of $G$ on $X$ is defined by $g:X\to X$ such that $g(x)=xg^{-1}$, $\forall g \in G$ and $\forall x \in X$
- The inverse preserves composition:
$$g_{2}(g_{1}(x))=xg_{1}^{-1}g_{2}^{-1}=(g_{2}g_{1})(x)$$

- Define _composition_ by $G$ on $X$ as the action:
$$g(x)=gxg^{-1} \quad \forall g\in G \quad \forall x \in X$$

- Given a group $G$ and set $X$, an _orbit_ of an element $x \in X$ is the _set formed by_ elements of $X$ which are in the image of an action of $G$ on $x$
- If the action is _left_, the _orbit_ of $x \in X$ is $$Gx=\{ gx |g \in G\}$$
- It can be shown that the _set of orbits_ under $G$ will _partition_ $X$


- Orthogonal group $O(n)$ represents _reflections and rotations_ on $\mathbb{R}^{n}$
	- It _preserves inner products_ $(v_{2},v_{1})=v_{2}^{T}v_{1}$
$$R\in O(n): (Rv_{2},Rv_{1})=v_{2}^{T}R^{T}Rv_{1}=v_{2}^{T}v_{1}$$
- Over a complex field, $U(n)$ has similar properties

- Example: the $SO(2)$ group
$$SO(2)= \Bigg\{ R(\theta)=\pmatrix{\cos\theta&-\sin\theta\\ \sin\theta &\cos\theta} \Bigg| \theta \in [0, 2\pi)\Bigg\}$$
$$R(\theta_{1})R(\theta_{2})=R(\theta_{1}+\theta_{2})$$

- Example: the $SO(3)$ group, representing rotations of vectors in $\mathbb{R}^{3}$
	- The _axes of rotation_ spanned by a unit vector $\hat{n}$ on the 2-sphere
	- Due to freedom to orientate $\hat{n} \to -\hat{n}$, define $\theta \in [0,\pi]$
	- One can depict the _manifold_ of $SO(3)$ as a _ball_ of radius $\pi$ in $\mathbb{R}^{3}$
		- The antipodal points must be _identified_: $\pi \hat{n}=-\pi \hat{n}$

## Parametrisation of Lie groups
- In _small neighbourhoods_ of a manifold, one should be able to _assign coordinates_
	- One may need to _change_ coordinates at different points, but not in the "neighbourhood"
- For an $n-$dimensional manifold:
$$\boldsymbol{x}:= (x^{1},\dots,x^{n}) \in \mathbb{R}^{n}$$
- Such that for a Lie group $G$, one can _label_ group elements, and they obey _closure_:
$$g(x) \in G \qquad g(x)g(y)=g(z) \;\;\forall x,y,z \in \mathbb{R}^{n}$$

- For the manifold to be _smooth_, components $z^r$ of $z$ must be _continuously differentiable_ functions of $x,y$
$$z^{r}=\varphi^{r}(x,y)$$
- One must also choose a _coordinate origin_ such that for identity element $e$:
$$g(0)=e \implies g(0)g(x)=g(x)$$
- For all $x$, there must be an _inverse_ $\bar{x}$ such that
$$g(x)g(\bar{x})=g(0)$$
- _Associativity_:
$$[g(z)g(y)]g(x)=g(z)[g(y)g(x)]$$

## Lie algebras
- A _Lie algebra_ is determined by:
$$[X_{j},X_{k}]=i\sum_{\alpha}^{n}f_{jk\alpha}X_{\alpha}$$
- $f_{jk\alpha}$ are the _structure constants_
- Example: Pauli spin matrices
$$[\sigma_{i},\sigma_{j}]=i\varepsilon_{ijk}\sigma_{k}$$

- The _subgroup_ of generators that _commute_ with each other is the _rank_ of the Lie group





## General Lie groups
- In _general_, a Lie group can be characterised by $n$ parameters:
$$g(a_{1},a_{2},\dots a_{n})=\exp\left( -i\sum_{j} a_{j}X_{j}\right)$$
- It has $n$ _generators_ $X_{j}$
- It is a _Lie group of dimension_ $n$

## Example: Translation group
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