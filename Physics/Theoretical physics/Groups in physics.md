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
# Lie groups and Lie algebras
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
- A Lie group is _homogeneous_, as any _neighbourhood_ can be _mapped to_ any _other_ neighbourhood
	- If $\varepsilon$ is "close" to $g_{1}$, then $g_{2}g_{1}^{-1}\varepsilon$ is "close" to $g_{2}$

- Therefore, _linearise_ the Lie group _near the identity_
- This gives rise to its _Lie algebra_
### Algebras
- A Lie algebra is a _vector space_ $\mathbb{V}$, which additionally has a _vector product_, the _Lie bracket_:
$$[\cdot,\cdot]: \mathbb{V}\times \mathbb{V}\to \mathbb{V}$$
- For $X,Y,Z \in \mathbb{V}$, the Lie bracket must have the properties:
1. Antisymmetry $$[X,Y]=-[Y,X]$$
2. The _Jacobi identity_: $$[X,[Y,Z]]+[Y,[Z,X]]+[Z,[X,Y]]=0$$
3. _Linearity_: for $\alpha,\beta \in \mathbb{F}$
$$[\alpha X+\beta Y,Z]=\alpha[X,Z]+\beta[Y,Z]$$

- In fact, _any_ vector space with vector product $*$ can be made into a _Lie algebra_ with bracket $[x,y]=x*y-y*x$

### Generators and structure constants
- One can then choose a _basis_ for $\mathbb{V}$, $\{T_{a}\}$ with $a=1,\dots \mathrm{dim} \,\mathbb{V}$
- These basis vectors are the _generators_ of the Lie algebra

- A _Lie algebra_ is then determined by:
$$[T_{a},T_{b}]={f^{c}}_{ab}T_{c}$$
- ${f^{c}}_{ab}$ are the _structure constants_
	- In general, they are _basis dependent_
- They must then obey _anti-symmetry_ and _Jacobi's identity_:
$$\displaylines{{f^{c}}_{ab}=-{f^{c}}_{ba} \\ {f^{e}}_{ad}{f^{d}}_{bc}+{f^{e}}_{bd}{f^{d}}_{ca}+{f^{e}}_{cd}{f^{d}}_{ab}=0}$$

- _General elements_ of Lie algebras are _linear combinations_ of $\{T_{a}\}$:
$$\displaylines{X \in \mathbb{V} \implies X=X^{a}T_{a} \quad, \quad X^{a} \in \mathbb{F} \\ [X,Y]=X^{a}Y^{b}{f^{c}}_{ab}T_{c}}$$

## Examples of Lie algebras

### Rotation groups
- Group elements: _rotation matrices_

- $SO(2)$: a _one-dimensional maifold_ $\theta$
$$g(\theta)=\pmatrix{\cos\theta & -\sin\theta \\ \sin\theta & \cos\theta}$$
- The _generator_ is an _antisymmetric matrix_
$$\displaylines{g(\theta)=I+\theta \frac{dg(\theta)}{d\theta}\Bigg|_{\theta=0}+O(\theta^{2}) \\ T=\pmatrix{0&-1\\1&0}}$$
- The generator is the _tangent_ to the manifold
- $SO(2)$ has a _one dimensional Lie algebra_

- For $SO(n)$, the Lie algebra has dimension $d=n(n-1)/2$ and require $d$ coordinates on the manifold

- Consider a _single parameter family_ of $SO(n)$ elements:
$$M(t):= M(x(t)) \in SO(n) \qquad M(0)=I_{n}$$
- From _orthogonality_:
$$0=\frac{d}{dt}(M^{T}M)=M^{T} \frac{dM}{dt}+ \frac{dM^{T}}{dt}M$$
- At $t=0$, one gets:
$$\frac{dM}{dt}=\sum_{i=1}^{d} \frac{\partial M}{\partial x^{i}} \frac{d x^{i}}{d t}=-\frac{dM^{T}}{dt}$$
- Therefore, the _tangent spaces_ of the $SO(n)$ Lie algebras always consist of _antisymmetric matrices_ 
	- They must also then be _traceless_
	- The tangent spaces of $O(n)$ are also the same, given that curves passing through $I_{n}$ must also have $\det M=1$
	- For $O(n)$, there are matrices _disconnected_ from the identity

### Unitary groups
- For $M \in SU(n)$, expand:
$$\displaylines{M(t)=I+tX+O(t^{2}) \\ I=MM^{\dagger}=I+t(X+X^{\dagger})+O(t^{2})}$$
- Therefore, the _tangent space_ consists of _anti-Hermitian matrices_:
$$X=-X^{\dagger}$$
- One can prove that $\mathrm{Tr}\, X=0$ for $SU(n)$
	- Not true in general for $U(n)$
	- Prove: only linear term in $\det M=1$ comes from diagonal terms

## Connecting Lie groups to their algebras
- The _Lie algebra_ of a group is the _tangent space_ to the group at identity element $e$
### From commutators to brackets
- Consider two curves through identity $e$, for some Lie group $G$:
$$g_{1}(x(t)), g_{2}(y(t)) \in G \qquad X_{1}=\dot{g}_{1}|_{0}\,,\, X_{2}=\dot{g}_{2}|_{0} \in T(G)$$
- Let there be a _product_ $g_{3}$, one finds that its derivative at $t=0$ is _still in the tangent space_:
$$g_{3}(z(t))=g_{1}g_{2} \qquad \dot{g}_{3}|_{0}=X_{1}+X_{2} \in T(G)$$
- Define the _group commutator_ of $g_{1}, g_{2} \in G$ as:
$$[g_{1},g_{2}]_{G}:=g_{1}^{-1}g_{2}^{-1}g_{1}g_{2}=:h \in G$$

- With $g_{1}(t)$ and $g_{2}(t)$ as curves through the identity:
$$\displaylines{g_{i}(t)=e+tX_{i}+t^{2}W_{i}+O(t^{3}) \\ g_{1}g_{2}=e+t(X_{1}+X_{2})+t^{2}(X_{1}X_{2}+W_{1}+W_{2})}$$
- The _group commutator_ is then:
$$h=e+t^{2}(X_{1}X_{2}-X_{2}X_{1}):=e+t^{2}[X_{1},X_{2}]$$
- Therefore, the _tangent_ to $h$ at $e$ is $[X_{1},X_{2}] \in L(G)$

- There is _closure under the Lie bracket_ 
### Tangent spaces and the exponential map
- Examine the _tangent space_ to Lie group $G < GL(n, \mathbb{F})$, at some _general element_ $p$, denoted $T_{p}(G)$
	- _Subgroup_ of the general linear group

- Let $g(t)$ be some _curve_ through the manifold through $p$ with $g(t_{0})=p$
- For some small interval $\varepsilon$, define $h_{p}(\varepsilon) \in G$ such that:
$$\displaylines{g(t_{0}+\varepsilon)=g(t_{0})+\varepsilon \dot{g}(t_{0})=g(t_{0})h_{p}(\varepsilon) \\ h_{p}(\varepsilon)=e+\varepsilon X_{p}+O(\varepsilon^{2}) ,\quad X_{p} \in L(G)=T_{e}(G)}$$
- Applying $p^{-1}$ to both sides, one gets:
$$X_{p}=g(t_{0})^{-1}\dot{g}(t_{0})$$
- $\dot{g}(t_{0})$ is _not_ in the Lie algebra, but it can be _mapped_ into the Lie algebra
- The Lie algebra is _homogeneous_

- Conversely, for $X \in L(G)$, there exists a _unique curve_ $g(t)$ with $g(t)^{-1}\dot{g}(t)=X$ and $g(0)=g_{0}$
- A consequence of the _uniqueness_ of solutions to the ODE, given by:
$$g(t)=g_{0}\exp(Xt)$$
### One parameter subgroups
- Given $X \in L(G)$, the curve:
$$g_{X}(t)=\exp(tX)$$
- Forms an _Abelian subgroup_ of $G$, "generated" by $X$
	- Satisfies closure, associativity, commutativity

- It is _isomorphic_ to the group of _reals_ $(\mathbb{R},+)$ if $g_{X}(0)=e$
- If $g_{X}(t_{0}\neq 0)=e$, it is _periodic_ and isomorphic to the _circle_ $S^{1}$

## Lie groups from Lie algebras
- Given a Lie algebra $L(G)$ of a Lie group $G$, define the _exponential map_
$$\exp: L(G)\to G$$
- For matrix Lie groups:
$$X \to \exp X =\sum_{k=0}^{\infty} \frac{X^{k}}{k!}$$
- _Locally_, the map is _bijective_ (1 to 1)
- _Globally_, the map is generally not 1 to 1
	- Example: $U(1)=\{\exp(i\theta)| \theta \in [0,2\pi)]\}$ and its Lie algebra $L(U(1))=\{ix|x \in \mathbb{R}\}$, where $L(U(1))\to U(1)$ is a _many-to-one_ map

- Example: the _orthogonal group_ $O(n)$, with _skew-symmetric matrices_ as _generators_:
$$\displaylines{M=\exp(tX), \quad X^{T}=-X\implies M^{T}=\exp(-tX) \\ MM^{T}=I, \quad M \in O(n)}$$
- Since $\mathrm{Tr}(X)=0$, let $\lambda_{i}$ be the eigenvalues of $X$:
$$\displaylines{\sum_{i} \lambda_{i}=0 \\ \det M=\det(\exp tX)=\exp\left( \sum_{i}t\lambda_{i} \right)=1 \implies M \in SO(n)}$$
- Elements in $O(n)$ but not $SO(n)$ are _not in the image of the exponential map_
	- $O(n)$ is a _disconnected manifold_, corresponding to _proper_ and _improper_ rotations

- _Any_ skew-symmetric matrix (in $\mathrm{Skew}_{n}$) can _generate_ an element of $SO(n)$
- Therefore, $L(SO(n))$ contains all elements of $\mathrm{Skew}_{n}$

## Lie brackets to the group product
- The Baker-Campbell-Hausdorff formula, for $X,Y \in L(G)$
$$\displaylines{\exp(tX)\exp(tY)=\exp(tZ) \\ Z=X+Y+\frac{t}{2}[X,Y]+\frac{t^{2}}{12}([X,[X,Y]]+[Y,[X,Y]])+O(t^{3})}$$
- As $L(G)$ is [[#From commutators to brackets|closed under the Lie bracket]], $Z \in L(G)$
# Representations
- Groups are _transformations_ under which things are invariant
- _Representations_ are _how groups transform vectors_ in a vector space

- $GL(n,\mathbb{F})$ is a group of _invertible matrices_, acting as _linear maps_ on the vector space $\mathbb{F}^{n}$:
$$GL(n,\mathbb{F}): \mathbb{F}^{n}\to \mathbb{F}^{n}$$
- _Generalise_ to any other vector space $\mathbb{V}$

## Representations of Lie groups
- A representation $D$ of a group $G$ is a _smooth group homomorphism_ from $G$ to the _group of linear automorphisms_ on some vector space $\mathbb{V}$, the _representation space_ associated with $D$
$$D: G \to GL(\mathbb{V})$$
- In other words, $\forall g \in G$, $D(g): \mathbb{V} \to \mathbb{V}$ is an invertible, linear map such that:
$$v \to D(g)v\quad \forall v \in \mathbb{V}$$
- _Linearity_:
$$D(g)(\alpha v_{1}+\beta v_{2})=\alpha D(g)v_{1}+\beta D(g)v_{2} \qquad \forall \alpha,\beta \in \mathbb{F},\quad v_{1},v_{2} \in \mathbb{V}$$
- For the homomorphism to hold:
$$D(g_{2}g_{1})=D(g_{2})D(g_{1})$$
- This implies:
$$\displaylines{D(e)=\mathrm{id}_{\mathbb{V}} \\ D(g)^{-1}=D(g^{-1})}$$

- The _dimension_ of the representation is the _dimension of_ the associated _vector space_ $\mathbb{V}$
	- If $\mathbb{V}$ is _finite dimensional_ with $\mathrm{dim} \,\mathbb{V}=N$, then $GL(\mathbb{V})$ is isomorphic to $GL(N,\mathbb{F})$
	- The isomorphism can be identified by choosing a basis for $\mathbb{V}$

- The _kernel_ of a map $D:G \to GL(\mathbb{V})$ consists of the _elements of_ $G$ which map to the _identity_ $\mathrm{id}_{\mathbb{V}}$
- A representation $D$ is said to be _faithful_ if $D(g_{0})=\mathrm{id}_{\mathbb{V}}$ only for $g_{0}=e$, or if $\mathrm{ker}\,D =\{e\}$

- _Faithfulness_ implies that $D$ is _injective_:
$$D(g_{1})=D(g_{2}) \implies g_{1}=g_{2}$$
### Example: representations of the reals
- Group:
$$G=(\mathbb{R},+)$$
- For some fixed $k \in \mathbb{R}$, $D(\alpha)=\exp(k\alpha) \,\forall \alpha \in \mathbb{R}$ is a _one-dimensional representation_
	- Group homomorphism: $D(\alpha)D(\beta)=D(\alpha+\beta)$
	- For $k\neq 0$, it is a _faithful representation_
	- For $k=0$, $\mathrm{ker }\,D=G$, which is a _trivial representation_

- Or, one can have $D(\alpha)=\exp(ik\alpha)$, another 1D representation, which is _not faithful_
	- $\mathrm{ker}\,D=\{0,2\pi\dots\}$

- Or, a _two-dimensional representation_
$$D(\alpha)=\pmatrix{\cos\alpha & -\sin\alpha \\ \sin\alpha & \cos\alpha}$$

- Or, an _infinite-dimensional representation_
	- The representation is _faithful_
$$\displaylines{\mathbb{V}=\{\text{space of all real functions }f(x)\} \\ D(\alpha)f(x)=f(x-\alpha)}$$
### More on representations
- The _trvial representation_ $D_{0}$ is where:
$$D_{0}(g)=1\quad \forall g \in G$$
- By definition, it is _not faithful_, and _one dimensional_

- Quantities which are _invariant_ under group transformations is a _trivial representation_
	- Known as a _singlet_
- One can form _trivial representations of any dimension_ $M$, with $D_{0}(g)=\mathbb{I}_{M}$
	- It is a _reducible representation_
 

- If $G$ is a _matrix Lie group_, then the _fundamental representation_ $D_{f}$ is given by:
$$D_{f}(g)=g\quad \forall g \in G$$
- It is _faithful_ as only $D_{f}(e)=e$
- If $G < GL(n,\mathbb{F})$, then $\mathrm{dim}\,D_{f}=n$

- If $G$ is a matrix Lie group and consider tge case where the _Lie algebra is a vector space_ $\mathbb{V}=L(G)$
- The _adjoint representation_ $D^{\text{adj}}:=\mathrm{Ad}$ is the map
$$\displaylines{\mathrm{Ad}: G \to GL(L(G)) \quad \text{ such that }\forall g \in G, \mathrm{Ad}_{g}: L(G) \to L(G) \\\text{ with }\mathrm{Ad}_{g}\,X = gXg^{-1}}$$
- The action of $\mathrm{Ad}_{g}$ is [[#Groups as transformations|conjugation]]
- It is a _linearised_ version of the action of a group _on itself_ by _conjugation_
- One can check that the adjoint representation satisfies _closure_ 

## Representations of Lie algebras
- A representation $d$ of the Lie algebra $L(G)$ is a _map_ from $L(G)$ to a _set_ of linear maps within $gl(V)$, where $gl(v)$ is the _Lie algebra of_ $GL(V)$, or $L(GL(V))$, and where the _Lie bracket is preserved_


- In other words, for each $X \in L(G)$:
$$d(X): V\to V\qquad \text{ such that }\forall v \in V, v\to d(X)v$$
- It is _linear_:
$$d(\alpha X+\beta Y)=\alpha d(X)+\beta d(Y)$$
- It preserves Lie brackets:
$$d([X,Y])=[d(X),d(Y)]$$

- The _dimension_ of the Lie algebra is that of the vector space $V$

- The _trivial representation_ $d_{0}$ of a Lie algebra maps each $X \in L(G)$ to the _zero element_
$$\displaylines{d_{0}(X)=0 \qquad \forall X \in L(G) \\ d_{0}(X)v=\vec{0} \qquad \forall X \in L(G),\forall v \in V}$$

- Considering a _matrix Lie group_ $G\leq GL(n,\mathbb{F})$, the _fundamental representation_ of $L(G)$ is $d_{f}:L(G) \to \mathrm{Mat}_{n}(\mathbb{F})$ with:
$$d_{f}(X)=X\qquad \forall X \in L(G)$$
- The _dimension_ of $d_{f}$ is $n$

- The _adjoint representation_ $\mathrm{ad}:L(G)\to gl(L(G))$, $\forall X \in L(G)$:
$$\mathrm{ad}_{X}:L(G)\to L(G), \quad \mathrm{ad}_{X}Y=[X,Y]$$
- The action of an [[#More on representations|adjoint representation]] of a Lie group has _conjugation_
- The action of an adjoint representattion of a Lie algebra is the _Lie bracket_

- The _dimension_ $\mathrm{ad}$ is that of $L(G)$
## Algebra representations from group representations
- Consider _tangents_ to curves in the group manifold, passing through $e$:
$$g(t)=e+tX+\dots \in G$$
- Here, $X \in L(G)$

# OLD Example: Translation group
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

# OLD: Constants of motion
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

# OLD: Representations
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