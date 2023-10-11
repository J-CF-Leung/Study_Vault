- A note on notation: use _upper indices_ on _complex column vectors_
- Then define the _lower index_ such that:
$$\phi_i\equiv(\phi^i)^*$$
- The _inner product_ is then:
$$\braket{\phi|\psi}=\phi_i\psi^i$$
# Representations and characters
- The idea is to _represent group elements by matrices_
- The matrices must _reflect the [[Foundations of Group Theory#Multiplication tables|multiplicative table]] of the group_
- One _associates each element_ $g$ with its own $d\otimes d$ matrix $D(g)$ such that: 
$$D(g_1)D(g_2)=D(g_1g_2)$$
- From this, one can immediately tell that $D(I)=I_d$, where $I_d$ is the $d\otimes d$ _identity matrix_
- One can also prove that $D(g^{-1})=D(g)^{-1}$
## Representing the permutation group
- Consider $S_4$, the [[Foundations of Group Theory#Permutation Groups and Cayley's Theorem|permutation group]] of four objects
- Let the four objects be represented by _vectors_:
$$\bm{v}_1 = \pmatrix{1\\0\\0\\0} \hspace{1cm} \bm{v}_2 = \pmatrix{0\\1\\0\\0} \hspace{1cm} \bm{v}_3 = \pmatrix{0\\0\\1\\0} \hspace{1cm} \bm{v}_4 = \pmatrix{0\\0\\0\\1}$$
- For a 2-cycle $(ij)$, construct $D(ij)$ such that $D(ij)\bm{v}_i=\bm{v}_j$ and vice versa
- Similarly, $D(ijk)\bm{v}_k=\bm{v}_i$ and so on
- For example:
$$D(2413)=\pmatrix{0 & 0 & 0 & 1 \\ 0 & 0 & 1 & 0 \\ 1 & 0 & 0 & 0 \\ 0 & 1 & 0 & 0}$$
- One finds that these matrices _follow the multiplicative structure of permutations_
- As $S_4$ has 24 elements, there are 24 _distinct_ $4\otimes4$ matrices representing the group

## Representations for all groups
- It is easy to deduce that one can come up with _representation matrices_ for _any_ $S_n$
- From [[Foundations of Group Theory#Permutation Groups and Cayley's Theorem|Cayley's Theorem]], _all finite groups_ can be represented by matrices

- As for [[Rotations and Lie Algebra|continuous groups]], many are _initially defined using matrix multiplication_ (rotations and Lorentz boosts), hence they must have representations
	- The _additive group_ can be represented by the _one-dimensional_ matrix $D(u)=\exp(u)$
	- $2-$dimensional matrices are also viable for the additive group (there is yet another alternative using the Lorentz group with _boost angles_)
$$D(u)=\pmatrix{1&0\\u&1}$$

- One can define a _$d-$dimensional representation_, where the group $G$ is [[Foundations of Group Theory#Mappings|mapped]] into some _subgroup_ of $GL(d,\mathbb{C})$
	- $GL(d,\mathbb{C})$ is the group consisting of _invertible_ $d\times d$ matrices with _complex entries_
	- $GL(d,\mathbb{C})$ contains the _subgroup_ $SL(d,\mathbb{C})$ defined [[Foundations of Group Theory#Other (important) examples|here]]
- The requirement of a representation is simply that _the mapping is homomorphic_

- For _any group_, there is a _trivial representation_ where $D(g)=1\;\;\forall \;g\in G$
	- Obviously _homomorphic_, but not _isomorphic_ (one-to-one)
- An _isomorphic representation_ is known as _faithful_
	- Otherwise, it is _unfaithful_, like the trivial representation

- If a group is _defined in terms of matrices_, such as the [[Rotations and Lie Algebra#Higher dimensions and the rotation group|special orthogonal groups]] $SO(N)$, then these representations are the _defining/fundamental representations_
	- The defining representation of $SO(3)$ are the 3-dimensional orthogonal matrices
	- The defining representation of $Z_N$ is 1-dimensional, with elements $\exp(2i\pi j/N)$, for $j=0,1,\dots,N-1$
		- There are $N$ 1-dimensional representations of $Z_N$, with elements $\exp(2i\pi kj/N)$ where $k=0$ is the trivial representation

## Character
>[!quote]
>"Character is a function of class"

- Given a _particular representation_ $r$ of a group $G$, let the _representation matrix_ of the _element_ $g$ be denoted $D^{(r)}(g)$
- Then, _define_ the _character_ $\chi^{(r)}$ of that representation by:
$$\chi^{(r)}(g)\equiv \text{tr }D^{(r)}(g) $$
- One may expect that $\chi$ is _dependent on_ $r$ and $g$
- Instead, recall the concept of [[Foundations of Group Theory#Equivalence classes and invariant subgroups|equivalence classes]], where elements $g_1$ and $g_2$ are _equivalent_ $(g_1\sim g_2)$ if there exists _another element_ $f$ such that
$$g_1=f^{-1}g_2f$$
- Then for $g_1\sim g_2$ one finds using the _cyclic property of the trace_:
$$\chi^{(r)}(g_1)=\text{tr}\;D^{(r)}(g_1)=\text{tr }\left[D^{(r)}(f^{-1})D^{(r)}(g_2)D^{(r)}(f)\right]=\text{tr }D^{(r)}(g_2)=\chi^{(r)}(g_2)$$
- Denoting $c$ as an _equivalence class_, where $g\in c$:
$$\chi^{(r)}(c)=\text{tr }D^{(r)}(g)$$
- Hence, _character is a function of only class_

## Equivalent representations
- Given a representation $D(g)$, one can carry out a _change of basis_ using matrix $S$:
$$D'(g)=S^{-1}D(g)S$$
- Then one finds that for _any two elements_ $g_1$ and $g_2$:
$$D'(g_1)D'(g_2)=D'(g_1g_2)$$
- One also finds that:
$$\chi'(c)=\text{tr }D(g)=\text{tr }D'(g)=\chi(c) \;\;\;\;\text{ for }\forall\;g\in c$$
- $D(g)$ and $D'(g)$ are essentially _the same representation_

- Hence, for two representations, if $\chi'(c)\neq\chi(c)$, then _they must be different_ and cannot be related by a change of basis
	- In fact, the characters are [[#Schur's lemma and orthogonality|orthogonal]]
- If $\chi'(c)=\chi(c)$ for _all_ $c$, then the representations are _equivalent_

## Reducible representations
- Given a group with a 3-dimensional representation $D^{(3)}(g)$, such as $SO(3)$, denote the _trivial representation_ as $D^{(1)}(g)$
- Then, one can _create a 4-dimensional representation_ as a _block-diagonal matrix_
$$D^{(4)}(g)=\pmatrix{D^{(1)}(g)&\Big|&0&\\\hline0&\Big|&D^{(3)}(g)}$$
- This is known as a _reducible representation_, as it can be written as a _direct sum_:
$$D^{(4)}(g)=D^{(1)}(g)\oplus D^{(3)}(g)$$
- $D^{(1)}(g)$ and $D^{(3)}(g)$ are known as the _irreducible representations_ of the group
	- The _trivial representation_ is simply the scalar $1$
	- One can construct a $k\otimes k$ _identity matrix_ as a $k-$dimensional representation, using a direct sum of trivial representations
	- Hence, there must be _infinitely many reducible representations_ for any group

- Reducible representations are _not necessarily block diagonal representations_, as they can be altered via a _change of basis_

## Restricting to a subgroup
- For a group $G$ with elements $g$, let there be a subgroup $H$ with elements $h$
- If $D(g_1)D(g_2)=D(g_1g_2)$ for any elements in $G$, then $D(h_1)D(h_2)=D(h_1h_2)$ _for any elements in_ $H$

- When _restricted_ to a subgroup $H$, then an _irreducible representation of_ $G$ can likely be _decomposed into irreducible representations of_ $H$
- There may be a basis where _only_ $D(h)$ is block diagonal

## Unitary representations
>[!info] Unitarity Theorem
>All _finite_ groups have _unitary representations_
>i.e. $D^\dagger(g)D(g)=I$ for _all_ $g$ and _all representations_

- Related to the fact that for _any element_ $g$ in a _finite group_, there is some $k$ such that $g^k=I$

- Proof:
	- 

## Compactness
- Consider whether or not the _unitarity theorem_ applies to _infinite groups_
- It holds for the _special orthogonal groups_: $R(\theta)^TR(\theta)=I$

- However, it _does not hold_ for many other orthogonal groups, no matter if it is _discrete_ (e.g. additive group for integers) or _continuous_ (Lorentz group)

- The proof for the unitarity theorem in this case requires an _integral over the continuous group_:
$$\int\,d\mu(g)\,(\dots)$$
- If this integral _converges_, the group is _compact_, and _proofs for finite groups apply_

## Product representation
- One can create _larger, reducible representations_ using [[#Reducible representations|direct sums]]
- However, one can also use [[Vectors and matrices in physics#Direct product spaces|direct products]] to create larger representations

- Given _two representations_ of dimensions $d_r$ and $d_s$, with rep. matrices $D^{(r)}(g)$ and $D^{(s)}(g)$, one defines the _direct product representation_ with the direct product matrices
	- The representations exist in _different vector spaces_ with different dimensionalities
$$\displaylines{D(g)=D^{(r)}(g)\otimes D^{(s)}(g) \\ D(g)_{a\alpha,b\beta}=D^{(r)}(g)_{ab}\,D^{(s)}(g)_{\alpha\beta}}$$


- The resulting representation has $d_rd_s$ dimensions
- One can check using the _definition of the direct product_ that $D(g)$ _is a representation_

- In _general_, this product representation is _not necessarily reducible_

- The _characters_ of the direct product representation:
$$\chi(c)=\sum_{a\alpha}D(g)_{a\alpha,a\alpha}=\left(\sum_a D^{(r)}(g)_{aa}\right)\left(\sum_\alpha D^{(s)}(g)_{\alpha\alpha}\right)=\chi^{(r)}(c)\chi^{(s)}(c)$$

# Schur's lemma and orthogonality

>[!info] Schur's lemma
>If $D(g)$ is an _irreducible representation_ of a finite group $G$ and if there is some matrix $A$ such that $AD(g)=D(g)A$ for all $g$, then $A=\lambda I$ for some _constant_ $\lambda$

- In other words, if there is a matrix $A$ which is _NOT the identity_, and it _commutes with a representation matrix $D(g)$_ for _all_ $g$, then $D(g)$ must _not be irreducible_

- From this, one can prove _Schur's Orthogonality Relation_
- Given a $d-$dimensional irreducible representation $D(g)$ for a _finite group_ $G$ with $N(G)$ _elements_:
$$\sum_g D^\dagger(g)^i_jD(g)^k_l=\frac{N(G)}{d}\delta^i_l\delta^j_k$$
- In other words, when _summing over_ group elements, any information related to _orientation_ disappears
- Proof: using Schur's Lemma
- If $j=k$, then the left hand side becomes $N(G)\delta_{il}$ due to [[#Unitary representations|unitarity]] and the constant on the right hand side must be $N(G)/d$

- Corollary: for _two representations_:
$$\sum_g D^{(r)\dagger}(g)^i_j\,D^{(s)}(g)^k_l=\frac{N(G)}{d_r}\delta^{rs}\delta^i_l\delta^j_k$$
- One can argue that if $r\neq s$, then $i,j$ and $k,l$ are indices over _different vector spaces_ and the RHS is invalid
- For the right hand side to be non-zero, the representations _must be equivalent_

## Character orthogonality and character tables
- Setting $i=j$ and $k=l$ above, then _summing_:
$$\sum_c n_c\left(\chi^{(r)}(c)\right)^*\left(\chi^{(s)}(c)\right)=N(G)\delta^{rs}$$
- Where $n_c$ is the number of _elements belonging to class_ $c$
- Example: the cyclic group $Z_N$
	- $D^{(k)}(j)=\chi^{(k)}(j)=\exp(2i\pi kj/N)$
	- Equivalence classes are labelled _by element_ as the group is Abelian
	- $\sum_{j=0}^{N-1}\exp[2i\pi(l-k)j/N]=N\delta_{kl}$
	- This is the basis of [[Fourier series and transforms|Fourier series analysis]]

- For a given _finite group_, one can construct a _character table_
- Along the _vertical axis_, one lists the _equivalence classes_ $c$
	- List by naming a "typical element"
	- Can also include information on $n_c$ as well as the _generated subgroup_ from each class
- Along the _horizontal axis_, one lists the different _irreducible representations_ $r$
	- Often named by their _dimensions_

- Example: character table for $A_4$, with $\omega=\exp(2\pi i/3)$
![[A4 character table.png]]
- The IR $1$ is simply the _trivial representation_
- As the _identity_ is always _in its own equivalence class_, its row simply gives the _dimension of each representation_ $\chi^{(r)}(I)=d_r$

## The dimensions of a character table
- Let the _number of classes_ be $N(C)$ and the _number of representations_ be $N(R)$

- For each _representation_ $s$, one can form an _array_ $\sqrt{n_c}\,\chi^{(s)}(c)$ with $N(C)$ elements, treated as a _vector_ in $N(C)-$dimensional space
- From _character orthogonality_, all $N(R)$ such possible vectors are _orthogonal_, hence this places a _restriction on the number of representations_
$$N(R)\leq N(C)$$
