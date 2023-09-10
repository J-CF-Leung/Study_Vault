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
 
# Schur's lemma and orthogonality
