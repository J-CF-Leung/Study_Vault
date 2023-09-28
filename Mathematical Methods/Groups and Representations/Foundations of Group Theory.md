- An object being _symmetric_ means that there is a _set of transformations_ which will leave the object _invariant_, or _indistringuishable_ from its original state
- These transformations are known as the _symmetry operations_ of the object

- Sets of symmetry operations can form _groups_

# The definition of a group

## Sets, algebras, and groups
- A _set_ is a _collection of objects_
- If the object $a$ is in the set $S$, it is denoted $a\in S$

- An _algebra_ is a _set_ of objects, along with an _operation_ which _combines two elements_ in the set, to produce _another element of the set_

- A _group_ is an _algebra_ which must _satisfy several axioms_
![[Sets algebras groups.png]]
- A generic group is denoted $G$, with _elements_ $g_1,g_2,\dots$
	- The _label_ of group elements can be _discrete or continuous_
	- The set of elements can be _infinite_ or _finite_ (See [[#Orders]])
- The group must also contain a _group product_, denoted $g_1g_2$

## The axioms
- The _axioms_ a group must satisfy:
1. _Closure_: The result of taking a _product_ between any two elements of the group must _also be an element_ of the group $$g_1\in G \hspace{1cm} g_2\in G \Longrightarrow g_1g_2\in G$$
2. _Identity_: There must exist a single _identity element_, denoted by $I$, such that, for _every element_ $g\in G$ $$Ig=g \hspace{1cm} gI=g$$
3. _Inverse_: For every element $g\in G$, there must exist an _inverse_ of that element $g^{-1}\in G$ such that $$gg^{-1}=I=g^{-1}g$$
4. _Associativity_: For any 3 elements $g_1,g_2,g_3\in G$, $$(g_1g_2)g_3=g_1(g_2g_3)$$
## Corollaries
- A group's _identity element is unique_
	- Assume that there are two _different_ identity elements, $I$ and $I'$, where $I\neq I'$
	- Using the _definition_ of an identity element: $$II'=I \hspace{1cm} II'=I'$$
	- Therefore, $I=I'$ since the products must be the same

- A group element's _inverse is unique_
	- Assume that for $g\in G$, there are _two inverses_ $h$ and $k$ such that $h\neq k$: $$gh=I \hspace{1cm} kg=I$$
	- Multiply the expression on the left by $k$: $$k(gh)=(kg)h=k$$
	- Since $kh=I$, $h=k$

## Commutativity
- The group of integers under addition is _commutative_:
$$\displaylines{a,b\in\mathbb{Z} \\ a+b=b+a}$$
- However, this property is _not common to all groups_

- For _commutative_, or _Abelian groups_, if $g_1,g_2\in G$:
$$g_1g_2=g_2g_1$$
- For _non-Abelian groups_, if $g_1,g_2\in G$:
$$g_1g_2\neq g_2g_1$$
>[!quote]
>"There's nothing wrong with non-Abelian groups!"

## Examples
- Elements can be _physical transformations_, or operations done on sets

### Example: The integers $\mathbb{Z}$ under addition
- To see that it follows the axioms:

1. _Closure_: $$a,b\in \mathbb{Z} \Longrightarrow a+b\in\mathbb{Z}$$
2. _Identity_: $$a+0=a \hspace{1cm} 0+a=a$$
3. _Inverse_: $$a+(-a)=0 \hspace{1cm} (-a)+a=0$$
4. _Associativity_: $$(a+b)+c=a+(b+c)$$
- Addition is _commutative_, or _Abelian_

- This can also be expanded to _all real numbers under addition_

### Other (important) examples
- _Rotations_ in _3-dimensional Euclidean_ space, $SO(3)$
	- This group is _non-Abelian_
	- Clearly, it has _infinite_ elements
	- $SO$ stands for _special orthogonal group_
- _Rotations_ in _2-dimensional Euclidean_ space, $SO(2)$
	- This group is _Abelian_

- The _permutation group_ $S_n$, which _rearranges_ an _ordered set_ of $n$ elements
	- The group has $n!$ elements
- The group of _even permutations_ $A_n$

- The $n$ _roots_ of $1$ form the group $Z_n$ under _multiplication_
	- This group is said to be _cyclic_
- This can be expanded to _all complex numbers of magnitude_ $1$, or $\exp(i\phi)$, under multiplication, with a group denoted $U(1)$
	- This is [[#Mappings|isomorphic]] to $SO(2)$

- The _addition_ of integers $\text{mod} \;N$
	- Example: Under addition $\text{mod}\;5$, $\{0,1,2,3,4\}$ form a group
	- This is [[#Mappings|isomorphic]] to the cyclic group of order $N$, $Z_N$

- The [[Special relativity|Lorentz boost]] with _boost angle_ $\varphi$

- The set of $n\times n$ matrices with determinants equal to $1$, or _special matrices_, with the group being denoted $SL(n,R)$, or the _special linear group_ with _real entries_
	- The _complex_ case is $SL(n,C)$

- Sets of transformations leaving a [[Crystal structure and diffraction|crystal lattice]] invariant are known as _space groups_
	- Consisting of _translations_, _rotations_, _reflections_, and sometimes _inversions_
- _Excluding translations_ from space groups gives _point groups_
	- They leave a point _invariant_
	- They are used to describe [[Symmetry in molecules|molecules]]
- An example of point groups are the _dihedral groups_ $D_n$, the symmetries of an _$n-$sided regular polygon_


# A point group: The symmetries of a square
- Consider the _group of transformations_, representing the _symmetries of a square_

- One symmetry operation is _clockwise rotation by $\pi/2$ radians_
- The operation leaves the square _indistinguishable_ from its initial state
- To illustrate its effect, one puts _labels_ on the corners, which _do not affect the symmetry_

- Denote this _rotation_ by: $$g_1=R$$ ![[Square rotation.png]]
- Denote a _reflection_ by: $$g_2=m_1$$ ![[Square reflection.png]]
- Define the _group product_ as applying operations _successively_
- The convention for _successive operations_ is from _right-to-left_
- Then, do a _rotation followed by reflection_, denoting it by:$$m_1R$$![[Square m1R.png]]
- Then, do a _reflection followed by rotation_, denoting it by: $$Rm_1$$ ![[Square Rm1.png]]

- _Successive_ rotations, by $0$, $\pi/2$, $\pi$, and $3\pi/2$ radians in total can be denoted:
$$I, R, R^2, R^3$$
- Meanwhile, a rotation by $2\pi$ radians:$$R^4=I$$
- The _mirror planes_ can also be denoted:
![[Square mirror planes.png]]
- Each symmetry is its _own inverse_:
$$m_i^2=I$$
- The symmetries are _algebraically related_:
$$\displaylines{m_1m_2=m_2m_1=m_3m_4=m_4m_3=R^2 \\ m_1m_3=m_4m_1=m_2m_4=m_3m_2=R^3=R^{-1}}$$
- There is some _minimal subset_ of operations, from which _all other_ operations of the group can be _obtained by composition_
- In other words, the group is _generated_ from this subset, elements of which are known as the _generators_

- In this case, the _generators_ are $\{R, m_1\}$:
	- All _successive rotations_ are obtained by repeatedly applying $R$
	- The mirror planes are then generated by: $$m_2=R^3m_1 \hspace{1cm} m_3=R^2m_1 \hspace{1cm} m_4=Rm_1$$
	- The _identity element_ can be generated in two different ways: $$m_1^2=I \hspace{1cm} R^4=I$$
- In summary, the _subset $\{R,m_1\}$ generates the entire group_:
$$\{I,R,R^2,R^3,m_1,m_2,m_3,m_4\}=\{R^4,R,R^2,R^3,m_1,R^3m_1,R^2m_1,Rm_1\}$$
- This is known as the _$4-$fold dihedral group_ $D_4$
- In general, the symmetry group for a _regular polygon of $n$ sides_ is the $n-$_fold dihedral group_ $D_n$

# Orders
- The _order_ $|G|$ of a group $G$ is _how many elements it contains_

- If a group has _infinitely many elements_, it is called an _infinite group_
- Example: the _dihedral groups_ $$|D_n|=2n$$
- The _order of a group element_ $g\in G$ is the _least integer_ $k$ such that:
$$g^k=I$$
- Since a group is _closed_, $\{I,g,g^2,\dots g^{k-1}\}\in G$
- Hence:
$$k\leq|G|$$
- If an element $g$ has order $q$:
$$g^{-1}=g^{k-1}$$
# Subgroups
- A _subgroup_ of $G$ is a _subset_ of $G$ which is _a group in its own right_
- If $H$ is a _subset_ of $G$, $H\subset G$
- If $H$ is a _subgroup_ of $G$, $H<G$
	- If $G$ is also to be _included as a subgroup_ of itself, $H\leq G$

- Examples:
	- $SO(2)\subset SO(3)$
	- $S_m\subset S_n$ for $m<n$
	- $A_n\subset S_n$
	- $SO(3)\subset SL(3,R)$
	- $Z_2\subset Z_4$ but $Z_2\not\subset Z_5$

## Cyclic subgroups
- For element $g$ in some _finite_ group $G$, consider:
$$\{I,g,g^2,\dots,g^{k-1}\}$$
- Since $G$ is finite, this sequence is _also finite_, as $g^k=I$
- This set of elements forms the _cyclic subgroup_ $Z_k$
- If $k=|G|$, then the cyclic subgroup is $G$ _itself_

## Example: The subgroups of $D_4$
- By inspection, $D_4$ has 5 order-2 subgroups:
$$\{I,R^2\}, \{I, m_1\}, \{I, m_2\}, \{I, m_3\}, \{I, m_4\}$$
- There is also an order-4 subgroup:
$$\{I,R,R^2,R^3\}$$
- This is a _cyclic group_

- There are other order-4 subgroups:
$$\{I,R^2,m_1,m_2\}, \{I,R^2,m_3,m_4\}$$
- They are the [[#The Vierergruppe|Klein 4-groups/Vierergruppe]], denoted $K_4$ or $V$

- Although $D_4$ itself is _non-Abelian_, its _subgroups_ are

# Cosets and Lagrange's Theorem
- Given a group $G$, along with _subgroup_ $H=\{I,h_1,h_2,\dots\}$ of $G$, and an element $g\in G$
- The _left coset_ of $H$ in $G$ is defined as:
$$gH=\{g,gh_1,gh_2,\dots\}$$
- The _right coset_ of $H$ in $G$ is defined as:
$$Hg=\{g,h_1g,h_2g,\dots\}$$
- If $G$ is _Abelian_, then the left and right cosets are _equivalent_
- Unsurprisingly, they are _not groups themselves_
- Each coset contains $|H|$ elements

- The subgroup $H$ and its _left cosets_ will _partition_ $G$, as they _divide_ $G$ into _disjoint subsets_
- Similarly, $H$ and its _right cosets_ will also _partition_ $G$ but in a different way, unless $H$ is _normal_

- Two cosets are _either disjoint or identical_
	- Suppose $Hg_1$ and $Hg_2$ have one element in common, $h_1g_1=h_2g_2$
	- Then $Hg_1=Hh_1^{-1}h_2g_2=Hg_2$, since $h_1^{-1}h_2\in H$ due to closure
- Two cosets are _only identical iff_ $g_1g_2^{-1}\in H$

- Then, one can state _Lagrange's Theorem_:
>[!info] Lagrange's Theorem
>Let $G$ be a _finite group_ and let $H\subset G$, not necessarily invariant, then the theorem states:
$$|G|=n|H| \hspace{1cm} n\in \mathbb{Z}$$

- Proof: Suppose there are $n$ _distinct right cosets_ of $H$, including $HI$
	- As they are all _disjoint_, and each has $|H|$ elements
	- Each element of $G$ is _in exactly one coset_, hence $|G|=n|H|$

- Corollary: The _order of any element_ in $G$ will _divide_ $|G|$
	- Each element can form a [[#Subgroups|cyclic subgroup]] with _order equal to that of the generating element_ 

- _Example_: $Z_3$ is a subgroup of any $Z_{3n}$, where $n$ is an integer
	- Then if $p$ is _prime_, $Z_p$ has _no non-trivial subgroups_

# Direct products
- Given two groups $F$ and $G$, with elements $f$ and $g$, one can generate a group $H$ via their _direct product_:
$$H\equiv F\otimes G$$
- The elements of $H$ are denoted $(f,g)$

- The _product_ of two elements in $H$, $(f,g)$ and $(f',g')$ is then $(ff',gg')$
	- It is obvious that _closure_ is satisfied
- The _identity_ of $H$, $I_H$ is then $(I_F,I_G)$
	- The _identities_ are technically _different_ as they apply to different groups
- The _inverse_:
$$(f,g)^{-1}=(f^{-1},g^{-1})$$
- The _order_ of the group:
$$|F\otimes G|=|F||G|$$

- $F$ and $G$ can then be considered _subgroups_ of $F\otimes G$ with elements $(f,I)$ and $(g,I)$

## The Vierergruppe
-  Consider the direct product $Z_2\otimes Z_2$
- The elements are $(1,1)$, $(1,-1)$, $(1,-1)$ and $(-1,-1)$
- This is another definition of Klein's _Vierergruppe_, denoted $V$
	- Can also be noted as one of the [[#Example The subgroups of $D_4$|subgroups of D4]]

- It is _distinct_ from $Z_4$, as the _square of any element_ in $V$ gives the _identity_
	- In other words, _every element is self-inverse_

# Multiplication tables and presentations
- Ways to _define_ groups by stating the results of _group products_

## Multiplication tables
- Consider organising _all possible products between two group elements_ into a table
- The elements of the table are $g_2g_1$, where $g_1$ is on the _top row_, and $g_2$ is on the _left row_
- For example, the multiplication table of $D_4$:
![[D4 multiplication table.png]]
- Each row is a _complete rearrangement_ of every other row
- Each element appears in a row or column _once and only once_
	- Suppose in the $i$th row, $g_ig_j=g_ig_k$, then $g_j=g_k$

## Constructing multiplication tables for small n
- Using the "once and only once" rule, one can construct _all possible groups_ of small order $n$ by only considering the multiplication table
- Let there be some group of order $4$, with elements $(I,A,B,C)$, and use the definition of the identity:

![[Order 4 Cayley table stage 1.png|250]]

- Then, there are _two possible choices_:
$$A^2=I \;\;\;\text{ or }\;\;\; A^2=B$$
- $A^2=B$ and $A^2=C$ are the same as the only difference is _relabelling_

- Then continuing to use the _once and only once_ rule, one finds that there are _only two possible order-4 groups_:
![[Order 4 Cayley tables.png|500]]

- The left is the $Z_4$ _cyclic group_
- The right is the _Vierergruppe_ $V$

## Presentations
- For _large groups_, it is much easier to define groups via _presentations_
- They list elements from which _all other elements_ can be obtained, or the _generators_
- Example: the generators of the [[#A point group The symmetries of a square|D4 group]] are $\{R,m_1\}$
- For the two order 4 groups:
$$\displaylines{Z_4: \braket{A|A^4=I} \\ Z_2\otimes Z_2:\braket{A,B|A^2=B^2=I\;,\; AB=BA}}$$

# Mappings
- A _mapping_ is basically a _single-valued function_
- A mapping:
$$f:G\to G'$$
- This _associates_ an element $f(g)\in G'$ to an element $g\in G$

- A mapping is _one-to-one_ if $f(g_1)=f(g_2)$ _implies_ $g_1=g_2$
- A mapping is _onto_ if for every $g'\in G'$, there is _at least one_ $g\in G$ such that $f(g)=g'$
	![[1-1 vs onto.png]]
	- Left: One-to-one, but _not onto_
	- Right: Onto, but _not one-to-one_

- Let there be a mapping is _between two finite groups_ $G$ and $G'$, i.e. $$f:G\to G'$$
- If such a mapping _preserves the group operations_ (i.e. the _structure of the group table_ stays the same), then the groups are said to be _homomorphic_, and the mapping is known as an _homomorphism_

- Let the group operation in $G$ be denoted $\circ$, and the group operation in $G'$ be $*$
- For $G$ and $G'$ to be _homomorphic_:
$$\text{If }g_3=g_1\circ g_2\text{ , then } f(g_3)=f(g_1)*f(g_2)$$
- For isomorphic groups, the _identities map onto each other_:
$$\displaylines{ I'=f(I) \\ h\circ g=I \Longrightarrow f(h)*f(g)=I'}$$

- If a homomorphism is also _one-to-one and onto_, then it is also an _isomorphism_
- In most cases, one would consider mappings between _groups of the same order_, which are _isomorphic_

## Examples of isomorphisms
- _Every order-4 group_ $G$ is _isomorphic_ either to the _cyclic group_ $C_4$, or the _Vierergruppe_ $V$
	- Can be seen from constructing all possible [[#Constructing multiplication tables for small n|multiplication tables]] for $n=4$

- One can also form a set of $n\times n$ _matrices_ that become _isomorphic_ to a group under _matrix multiplication_, this is known as a _faithful representation_ of the group

- Consider the group $Z_2\otimes Z_3$, and the _repeated composition_ of $(1,1)$, starting from $(0,0)$:
$$\displaylines{Z_2\otimes Z_3 \\ (0,0)\to(1,1)\to(2,2)=(0,2)\to(1,0)\to(0,1)\to(1,2)\to(0,0)}$$
- This _cycles_ through _all 6 possible elements_
- Hence, $Z_2\otimes Z_3$ is _isomorphic_ to $Z_6$

- An _isomorphism_ between $Z_p\otimes Z_q$ and $Z_{pq}$ only occurs when $p$ and $q$ are _relatively prime_
- Example: consider the same case with $Z_2\otimes Z_4$:
$$\displaylines{Z_2\otimes Z_4 \\ (0,0)\to(1,1)\to(0,2)\to(1,3)\to(0,0) \\ (0,1)\to(1,2)\to(0,3)\to(1,0)\to(0,1)}$$
- This can be represented using a _discrete lattice on a torus_:
![[Z2 Z4 structure.png]]

- In another example, $SO(2)$ and $U(1)$ are _isomorphic_

# Permutation Groups and Cayley's Theorem
- The _permutation groups_ $S_n$ is rearranges $n$ objects, and evidently has $n!$ elements
	- The _subgroup_ $A_n$ only has the _even permutations_

>[!info] Cayley's Theorem
> _All_ finite groups are _isomorphic to a subgroup_ of $S_n$

- A row in the [[#Multiplication tables|multiplication table]] of some group $G$ with elements $\{g_1,g_2,\dots,g_n\}$ will have products $\{g_ig_1,g_ig_2,\dots,g_ig_n\}$, which from the _once and only once_ rule, must be _some permutation_ of the elements of $G$
- Hence, $g_i$ can be _mapped onto_ a subgroup of the permutation group 
	- $(n<n!)$, especially for _large $n$_

- Example: 
	- $Z_2$ is isomorphic to $S_2$ 
	- $Z_3$ is isomorphic to $A_3$, a _subgroup_ of $S_3$

## Cycles and transpositions
- An _element_ of the permutation group $S_5$ can be written as:
$$g=\pmatrix{1&2&3&4&5 \\ 4&1&5&2&3}$$
- This permutation takes: $1\to 5$, $2\to1$, and so forth
- It can also be said that it _cyclically permutes_ $1\to4\to2\to1$ and $3\to5\to3$
- This suggests a _compact notation_:
$$g=(142)(35)$$
- In other words, the permutation consists of a _3-cycle_ and a _2-cycle_
	- 2-cycles are also known as _transpositions_

- _Any_ permutation $P$ can be _resolved_ into cycles of various lengths, with _no cycle containing any number in common_
	- A _1-cycle_ means leaving a number _unchanged_
	- Proof: _construct_ a cycle, and if there are numbers left over, construct another cycle until the entire permutation is resolved
- 1-cycles are usually _omitted_:
$$g=\pmatrix{1&2&3&4&5 \\ 1&5&3&4&2}\longrightarrow g=(25)$$

- _Any_ $n-$cycle, with $n>2$, can be _written as a product of transpositions_:
	- In the above example, $(142)=(14)(42)$
- Properties of products:
	- If 2-cycles _have no numbers in common_, they _commute_ (Example: $(12)(34)=(34)(12)$)
	- $(ab)(ba)=I$
	- $(ab)(bc)(cd)=(abcd)$
	- $(abc)(cde)=(abcde)$

- All 2-cycles are _odd_, and hence all 3-cycles are _even_, and so on
- Then, a permutation is _even or odd_ if it _decomposes_ into an _even or odd number of exchanges/transpositions_

- This leads to the theorem that _all groups of even order_ have _at least one element_ $g$ with order 2, or in other words, $g^2=I$

# Equivalence classes and invariant subgroups

## Equivalence
- A _property_ of inverses:
$$(g_1g_2)^{-1}=g_2^{-1}g_1^{-1}$$
- Can be proven using _associativity_ of group products

- Two _group elements_ $g_1,g_2\in G$ are known to be _equivalent_ to each other if _there exists any group element_ $g$ such that:
$$g_2=gg_1g^{-1} \text{ or } g_2g=gg_1$$
- If $g_1$ and $g_2$ are _equivalent_, it is denoted:
$$g_1\sim g_2$$

- The _equivalence relation_ has the properties:
1. Reflexivity: $$g_1\sim g_1$$
2. Symmetry: $$g_1\sim g_2\text{ implies }g_2\sim g_1$$
3. Transitivity: $$\text{If }g_1\sim g_2 \text{ and }g_2\sim g_3\text{, then } g_1\sim g_3$$
- In general, if an equivalence relation exists in a set $S$, this _separates_ the set into _distinct subsets_, known as _equivalence classes_, where any elements $a$ and $b$ in the class satisfy $a\sim b$, but elements in _different classes_ are not equivalent

- Example: The equivalence classes of $D_4$ (denoted in the top row)
	![[D4 conjugacy classes.png]]
	- Example: $m_2R=Rm_1$

- Example: $A_4$ falls into 4 equivalence classes:
$$\displaylines{\{I\}, \;\{(12)(34),(13)(24),(14)(23)\},\;\{(123),(142),(134),(243)\} \\ \{(132),(124),(143),(234)\}}$$
	- Example: $1\leftrightarrow2$ and $3\leftrightarrow4$ exchanges $(123)$ to $(214)=(142)$
- Within $S_4$, $(124)$ and $(134)$ are equivalent, but _not in_ $A_4$ as $(23)$ is not an element there
- Permutations in the _same equivalence class_ must _have the same cycle structure_
- However, elements with _the same cycle structure_ are _not necessarily equivalent_

- The _identity_ element is _always in its own equivalence class_
- An _Abelian group_ has all of its elements _in their own equivalence class_

- A group element _and its inverse_ (if different), _may or may not_ be in the same class
- However, for a class $c$ consisting of $\{g_1,\dots,g_{n_c}\}$, then the _inverses of those elements_, $\{g_1^{-1},\dots,g_{n_c}^{-1}\}$ _also forms a class_ $\bar{c}$, which may or may not be the same as $c$

## Invariant subgroups
- An _invariant subgroup_ $H$ of a group $G$ is a _subgroup_ containing _complete conjugacy classes_

- $H$ is _normal_ if $H\leq G$, and $\forall h\in H$ and $\forall g\in G$:
$$ghg^{-1}\in H$$
	- Or in other words, the group $gHg^{-1}=\{gh_1g^{-1},gh_2g^{-1},\dots\}$ is identical to $H$ for any $g$ in $G$ but not in $H$
- This is _denoted_ $H\trianglelefteq G$, or $G\trianglerighteq H$
	- If $H\neq G$, and $H$ is an invariant subgroup of $G$, then $H\triangleleft G$ or $G\triangleright H$

- Example: one can show that the _order-4 subgroups_ of $D_4$ are _invariant_, while the order-2 subgroups are not
	- However, the order-2 subgroups can be invariant subgroups of the Vierergruppe
- Example: $Z_4$ is a subgroup of $\mathcal{Q}$
- Given a [[#Direct products|direct product group]] $G=E\otimes F$, $E$ and $F$ are _both invariant subgroups_ of $G$

- _Trivially_, $\{I\}$ and $G$ itself are _invariant subgroups_ of $G$
- Invariant subgroups, _excluding_ these, are known as _proper invariant subgroups_ of $G$

- If $G$ is _Abelian_, then _all subgroups are invariant_

- Invariant subgroups can have _invariant subgroups of themselves_

## Derived subgroups
- Given a group $G$, with elements $a,b$, let:
$$\braket{a,b}\equiv a^{-1}b^{-1}ab=(ba)^{-1}(ab)$$
- This is also known as the _commutator_
	- Confusing name for physicists!
- Note:
$$\braket{a,a}=I\hspace{1cm}\braket{a,b}^{-1}=\braket{b,a}$$
- The product $\braket{a,b}\braket{c,d}$ does _not necessarily_ have the form $\braket{e,f}$ for some $e$ and $f$

- Denote $\{x_1,x_2,\dots\}$ the objects $\braket{a,b}$ as $a$ and $b$ _range over all elements_ of $G$
- Then, this set, along with _all possible products_ of the objects, constitute a _subgroup_ of $G$
	- Not all products are of the form $\braket{a,b}$ 
- This is known as the _derived subgroup_ $\mathcal{D}$
	- Or the _commutator subgroup_, denoted $[G,G]$ (confusing!)

- Example: the derived subgroup of $S_n$ is $A_n$
	- Any product of four permutation is, by definition, _even_
- Example: the derived subgroup of $A_4$ is $V=Z_2\otimes Z_2$

- For an _Abelian_ group $G$, $\braket{a,b}=I$, hence $\mathcal{D}$ is simply the _trivial subgroup_ $\{I\}$
- Hence, the _size_ of the subgroup is a "measure" of _how non-Abelian_ $G$ is

- All _derived_ subgroups are also _invariant_
	- Let $g^{-1}ag=\tilde{a}$, then one can show $g^{-1}a^{-1}g=\tilde{a}^{-1}$
	- One can show that $g^{-1}\braket{a,b}g=\braket{\tilde{a},\tilde{b}}$
	- As the latter _must also be in $\mathcal{D}$_, $\mathcal{D}$ must be _invariant_

- Example: the derived subgroup of the [[The Finite Groups#The dihedral group|dihedral group]] is $Z_{n/2}$ for _even_ $n$, and $Z_n$ for _odd_ $n$

### Solvable and perfect groups
- Denoting $G$ by $G^{(0)}$, there can be a _series_ where $G^{(i+1)}=[G^{(i)},G^{(i)}]$
- If this ends with the _trivial group_ of $I$, then the group is _solvable_
- If $G^{(1)}=G$, then the group is _perfect_

- The _smallest perfect group_ is $A_5$

## Simple groups
- A group is _simple_ if it has _no proper invariant subgroups_
	- In other words, the _only_ invariant subgroups are $\{I\}$ and the group itself
	- As all groups will have cyclic subgroups, "simplicity" is better expressed with the absence of _invariant_ subgroups
- If the _derived subgroup_ is _non-trivial_, then $G$ is _not simple_
	- Good way of quickly finding out if a group is simple

## The kernel
- Let there be a [[#Mappings|homomorphic mapping]] $f$, which maps $G$ onto itself
	- In other words, $f(g_1)f(g_2)=f(g_1g_2)$
- The _kernel_ of $G$ is a _subgroup_, comprised of the elements _mapped onto the identity_
- The kernel is _always an invariant subgroup_ of $G$

## Cosets, the quotient group and abelianisation
- Let $G\triangleright H$, meaning $H$ is an _invariant subgroup_ of $G$
- Consider the _left cosets_ $gH$ for some element $g\in G$:
$$gH=\{gh_1,gh_2,\dots\}$$
- There are many such possible cosets $g_aH,g_bH,\dots$
- Since $H$ is _invariant_, the left cosets $gH$ are _identical_ to the right cosets $Hg$

- The set of _elements from separate cosets multiplied_:
$$(g_ah_i)(g_bh_j)=(g_ag_b)(g_b^{-1}h_ig_b)h_j=(g_ag_b)(h_lh_j)=g_ch_k$$
- The last equality is due to _closure_
- Hence, _cosets close under multiplication_
- The _identity_ of the set of cosets is simply $IH$, as $(IH)(gH)=gH$
- The _inverse_ of $gH$ is $g^{-1}H$
- The group product between cosets is also _associative_

- Hence, _cosets form a group of their own_
- This is known as the _quotient group_, denoted $Q=G/H$

- The _order_ (number of elements) of $Q$, is $|Q|=|G|/|H|$
	- It is proven [[#Cosets and Lagrange's Theorem|above]] that the cosets _partition_ $G$, and Lagrange's Theorem guarantees that $|Q|$ is an integer
- In _general_, $Q$ is _not a subgroup_ of $G$

- Example: the quotient group $Q=\mathcal{Q}/Z_4$ is $Z_2$
	- The cosets are $Z_4$ and $jZ_4$, where the latter is equivalent to $kZ_4$

- Consider the quotient group $Q=G/\mathcal{D}$, where $\mathcal{D}$ is the [[#Derived subgroups|derived subgroup]]
	- $\mathcal{D}$ is _always invariant_
- This is known as the _abelianization_ of $G$

## Composition series and the maximal invariant subgroup
- Suppose there is some invariant subgroup $H_1$ of $G$
- $H_1$ may contain _its own invariant subgroup_ $H_2$
- Following this, one can make a _composition series_:
$$G\triangleright H_1\triangleright H_2\triangleright \dots\triangleright H_k\triangleright I$$
- One can then have a sequence of _quotient groups_:
$$G/H_1\supset H_1/H_2\supset\dots\supset H_k$$
- Example: $\mathcal{Q}\triangleright Z_4\triangleright Z_2\triangleright I$

- The shortest series would be given by the _maximal invariant subgroups_
- This is helped by the theorem:
>[!info] Theorem
>Given a group $G$ with invariant subgroup $H$, forming the quotient group $Q=G/H$. Suppose that Q has no proper invariant subgroup. Then, $H$ is the _maximal invariant subgroup_.

# Vector spaces
- Consider _vectors_ imposed on a square, an object with point group $D_4$, with the _origins at the centre of the square_:
![[D4 vectors.png]]
- The vectors are represented:
$$\underline{x}=\pmatrix{x_1 \\ x_2}$$
- Then, consider the _rotation matrix_:
$$\dunderline{R}\underline{x}=\pmatrix{0 & 1 \\ -1 & 0}\pmatrix{x_1 \\ x_2}=\pmatrix{x_2 \\ x_1}$$
- This corresponds to a _clockwise rotation_ by $\pi/2$ radians

- In fact, _all elements of the group_ can be represented using a _matrix_
	- The matrices form a _group under matrix multiplication_, which is _isomorphic_ to $D_4$

- For each _subgroup_, there are _subspaces_ of $\mathbb{R}^2$ which are _invariant_ (still mapped onto an element of the subspace after the operation)

- The _Vierergruppe_ $\{I, R^2, m_1, m_2\}$ leaves _scalar multiples_ of $(0\;1)^T$ and $(1\;0)^T$ invariant
- The _Vierergruppe_ $\{I,R^3,m_3,m_4\}$ leaves _scalar muliples_ of $(1\;1)^T$ and $(1\;-1)^T$ invariant

