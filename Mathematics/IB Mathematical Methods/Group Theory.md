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
- The group must also contain a _group product_, denoted $g_1g_2$

## The axioms
- The _axioms_ a group must satisfy:
1. _Closure_: The result of taking a _product_ between any two elements of the group must _also be an element_ of the group $$g_1\in G \hspace{1cm} g_2\in G \Longrightarrow g_1g_2\in G$$
2. _Identity_: There must exist a single _identity element_, denoted by $I$, such that, for _every element_ $g\in G$ $$Ig=g \hspace{1cm} gI=g$$
3. _Inverse_: For every element $g\in G$, there must exist an _inverse_ of that element $g^{-1}\in G$ such that $$gg^{-1}=I=g^{-1}g$$
4. _Associativity_: For any 3 elements $g_1,g_2,g_3\in G$, $$(g_1g_2)g_3=g_1(g_2g_3)$$

## Example: The integers $\mathbb{Z}$ under addition
1. _Closure_: $$a,b\in \mathbb{Z} \Longrightarrow a+b\in\mathbb{Z}$$
2. _Identity_: $$a+0=a \hspace{1cm} 0+a=a$$
3. _Inverse_: $$a+(-a)=0 \hspace{1cm} (-a)+a=0$$
4. _Associativity_: $$(a+b)+c=a+(b+c)$$
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
>"There's nothing wrong with non-Abelian groups"

# A point group: The symmetries of a square
- Consider the _group of transformations_, representing the _symmetries of a square_

- One symmetry operation is _clockwise rotation by $\pi/2$ radians_
- The operation leaves the square _indistinguishable_ from its initial state
- To illustrate its effect, one puts _labels_ on the corners, which _do not affect the symmetry_

- Denote this _rotation_ by: $$g_1=R$$ ![[Square rotation.png]]
- Denote a _reflection_ by: $$g_2=m_1$$ ![[Square reflection.png]]
- The convention for _successive operations_ is from _right-to-left_
- Then, do a _rotation followed by reflection_, denoting it by:$$m_1R$$![[Square m1R.png]]
- Then, do a _reflection followed by rotation_, denoting it by: $$Rm_1$$ ![[Square Rm1.png]]
