
>[!quote]
>"There exists, if I am not mistaken, an entire world which is the totality of mathematical truths, to which we have access only with our mind, just as a world of physical reality exists, the one like the other independent of ourselves, both of divine creation."
>-Charles Hermite

## Vector spaces
- [[#The Schrödinger Equation ❤|The Schrödinger Equation]] can be put in terms of _operators_
- The _time-independent equation_ can be interpreted as an _eigenvalue equation_:
$$\hat{\Ham}\psi=E\psi$$
- The mathematics of vector spaces: [[Vectors and matrices]]
- Vector spaces in quantum mechanics are defined _on the field of complex numbers_ $\mathbb{C}$
- These vectors include _actual vectors, or matrices_
- _Generic vectors_ are denoted with _kets_:
$$\ket{V},\ket{W},\dots$$

- _Operators map vectors onto one another_:
$$\hat{\Omega}\ket{V}=\ket{W}$$

- Notation: _scalars and operators acting on kets_ can be denoted by:
$$\displaylines{\alpha\ket{V}\equiv\ket{\alpha V} \\ \hat{\Omega}\ket{V}=\ket{\hat{\Omega}V}}$$

### Bases
- If there is a set of basis vectors $\{b_n\}$, then it is _complete_ if _any_ vector $\ket{a}$ in a space $\mathbb{V}$ can be expressed as a _unique linear combination_ of these vectors:
$$\ket{V}=\sum_n a_n\ket{i}$$
- $a_n\in\mathbb{C}$ are the _expansion coefficients_, which can be said to be a _projection_ of $\ket{a}$ onto the basis vector $\ket{b_n}$

- The _maximum number of basis vectors_ is the _dimension_ of the space

### Dual spaces, adjoints and inner products
- Vector spaces used in quantum mechanics are _inner product spaces_
- The inner product involves a vector and its _dual_

- The _dual_ is in the _dual space_ $\mathbb{V}^*$ of the original vector space $\mathbb{V}$
- The _dual_ of a ket is known as the _bra_ and denoted $\bra{V}$
- It is also known as the _adjoint_ of the ket
	- For matrices and column vectors, it is the _transpose conjugate_

- The _dual of a vector multiplied by a scalar_ is:
$$\displaylines{\alpha\ket{V}=\ket{\alpha V} \\ \bra{\alpha V}=\bra{V}\alpha^*}$$

- The inner product outputs a _scalar_:
$$\braket{V|W}=c\in\mathbb{C}$$
- The inner product is _skew-symmetric_
$$\braket{V|W}^*=\braket{W|V}$$

- The _norm_ of a vector is defined as:
$$|\ket{V}|^2=\braket{V|V}$$

### Orthonormal bases
- An _orthonormal basis_ is a set of basis vector $\{\ket{i}\}$ such that:
$$\braket{i|j}=\delta_{ij}$$
- If $\ket{V}$ is _expanded_ in terms of an orthonormal basis:
$$\braket{j|V}=\sum_i a_i\braket{j|i}=a_j$$
- Thus, a vector can be written as:
$$\ket{a}=\sum_i \ket{i}\braket{i|a}$$
- So, for a basis set to be _complete_, it must satisfy the [[#Identity and projection operators|completeness relation]]

### Subspaces
- If in a vector space $\mathbb{V}$ contains a set of vectors _that form a vector space amongst themselves_. that set of vectors is called a _subspace_
- A subspace $i$ of dimensionality $n$ is denoted $\mathbb{V}_i^n$
- Example: In $\mathbb{R}^3$, all vectors _orthogonal_ to one vector forms a subspace $\mathbb{R}_i^2$

- Given two subspaces $\mathbb{V}_i^{n_i}$ and $\mathbb{V}_j^{n_j}$, their _sum_ is denoted:
$$\mathbb{V}_i^{n_i}\oplus\mathbb{V}_i^{n_i}=\mathbb{V}_k^{n_k}$$
- This consists of _all elements in each respective subspace, plus all possible linear combinations_
- Example:, all vectors along $x$, and all vectors along $y$:
$$\mathbb{R}_x^1+\mathbb{R}_y^1=\mathbb{R}_{xy}^2$$

## Operators
- Consider _operators_ acting on _generic vectors_, mapping it onto another vector _in the same vector space_
$$\hat{O}\ket{V}=\ket{W}\hspace{1cm} \ket{V},\ket{W}\in\mathbb{V}$$
- Only consider _linear operators_:
$$\displaylines{\hat{O}\alpha\ket{V}=\alpha\hat{O}\ket{V} \\ \hat{O}[\alpha\ket{V}+\beta\ket{W}]=\alpha\hat{O}\ket{V}+\beta\hat{O}\ket{W}}$$

### Identity and projection operators
- The _identity operator_ leaves the vector alone:
$$I\ket{a}=\ket{a}$$
- If the basis set in this space is $\{\ket{u_m}\}$, then this can be written as:
$$\ket{a}=\sum_m \ket{u_m}\braket{u_m|a}=\sum_m\mathbb{P}_m\ket{a}$$
- Here, $\mathbb{P}_m$ is the _projection operator_ along direction $\ket{u_m}$
- It gives the _component_ of $\ket{a}$ along $\ket{u_m}$, multiplied by $\ket{u_m}$
- The above equation also leads to the identity:
$$\sum_m\mathbb{P}_m=\sum_m\ket{u_m}\bra{u_m}=\hat{I}$$
- This is known as the _completeness relation_, and must be satisfied for a basis to be _complete_

### Matrix elements
- Expanding $\hat{O}\ket{V}$ using the completeness relation:
$$\displaylines{\hat{O}\ket{V}=\sum_{i,j} \ket{i}\braket{i|\hat{O}|j}\braket{j|V}=\sum_{i,j}O_{ij}\ket{i}\braket{j|V} \\ \hat{O}\equiv\sum_{i,j}O_{ij}\ket{i}\bra{j}}$$
- $O_{nm}=\braket{u_n|\hat{O}|u_m}$ are known as the _matrix elements_ of $\hat{O}$ in this particular basis

### Products and commutators
- The _product_ of two operators acting on $\ket{a}$ is equivalent to each acting in turn:
$$\hat{\Omega}(\hat{\Lambda}\ket{V})=(\hat{\Omega}\hat{\Lambda})\ket{V}$$
- By using the _completeness relation_, its matrix elements are:
$$\begin{aligned}(\hat{\Omega}\hat{\Lambda})_{ij}&= \braket{i|\hat{\Omega}\hat{\Lambda}|j}=\sum_k \braket{i|\hat{\Omega}|k}\braket{k|\hat{\Lambda}|j} \\ &=\sum_k A_{ik}B_{kj} \end{aligned}$$

- In _general_, operators _do not commute_:
$$\hat{\Omega}\hat{\Lambda}\neq\hat{\Lambda}\hat{\Omega}$$
- How _badly_ two operators commute is measured by the _commutator_:
$$[\hat{\Omega},\hat{\Lambda}]=\hat{\Omega}\hat{\Lambda}-\hat{\Lambda}\hat{\Omega}$$
- If the commutator is _zero_, then the operators _commute_

### Adjoints of operators and Hermiticity
- Given a ket $\ket{\hat{\Omega}V}=\hat{\Omega}\ket{V}$, its _adjoint_/dual is:
$$\bra{\hat{\Omega}V}=\bra{V}\hat{\Omega}^\dagger$$
- This _defines_ the _adjoint_ of the operator
- In terms of the inner product:
$$\braket{V|\hat{\Omega}W}=\braket{\hat{\Omega}^\dagger V|W}$$
- The _matrix elements_ of the adjoint are:
$$(\hat{\Omega}^\dagger)_{ij}=\braket{i|\hat{\Omega}^\dagger|j}=\braket{j|\hat{\Omega}|i}^*=(\hat{\Omega})_{ji}^*$$
- Therefore, the adjoint can be understood as the _transpose conjugate_

- From the nature of the product of operators, it can be proven that:
$$(\hat{\Omega}\hat{\Lambda})^\dagger=\hat{\Lambda}^\dagger\hat{\Omega}^\dagger$$
### Hermitian, anti-Hermitian, and unitary operators
- An operator is _Hermitian_ if:
$$\displaylines{\hat{\Omega}^\dagger=\hat{\Omega} \\ \braket{\hat{\Omega}V|W}=\braket{V|\hat{\Omega}W}}$$
- An operator is _anti-Hermitian_ if:
$$\displaylines{\hat{\Omega}^\dagger=-\hat{\Omega} \\ \braket{\hat{\Omega}V|W}=-\braket{V|\hat{\Omega}W}}$$
- Just as a scalar can be split into pure and imaginary parts, _operators can be split into Hermitian and anti-Hermitian parts_:
$$\hat{\Omega}=\frac{\hat{\Omega}+\hat{\Omega}^\dagger}{2}+\frac{\hat{\Omega}-\hat{\Omega}^\dagger}{2}$$
- An operator is _unitary_ if:
$$\displaylines{\hat{U}\hat{U}^\dagger=\hat{I} \\ \hat{U}^\dagger=\hat{U}^{-1}}$$

- A unitary operator _preserves the inner product_:
$$\displaylines{\ket{V'_1}=\hat{U}\ket{V_1}\hspace{1cm}\ket{V'_2}=\hat{U}\ket{V_2} \\ \braket{V_1'|V_2'}=\braket{V_1|V_2}}$$
- It is _analagous to a rotation in $\mathbb{R}^n$_
	- In real space, it is _orthogonal_

- If one treats the _columns or rows_ of an $n\times n$ unitary matrix as $n$ vectors, they are _orthonormal_
	- They correspond to a _basis_ which [[Vectors and matrices#Diagonalisation via unitary matrices|diagonalises a Hermitian matrix]]

### Active and passive transformations
- Suppose _all vectors $\ket{V}$ in a space are subject to a transformation_:
$$\ket{V}\longrightarrow \hat{U}\ket{V}$$
- This is known as an _active transformation_

- Under this transformation, the _matrix elements_ of any operator $\hat{\Omega}$ are:
$$\braket{V'|\hat{\Omega}|V}\longrightarrow \braket{\hat{U}V'|\hat{\Omega}|\hat{U}V}=\braket{V'|\hat{U}^\dagger\hat{\Omega}\hat{U}|V}$$
- The _same change_ to the inner products if the _vectors were unchanged_, and the _operator was transformed_:
$$\hat{\Omega}\longrightarrow\hat{U}^\dagger\hat{\Omega}\hat{U}$$
- This is known as a _passive transformation_, as the vectors are unchanged

- From their properties, in both cases, _traces and determinants remain unchanged_

## Eigenvectors and eigenvalues
- For every operator, there are a _set of vectors, called eigenvectors_, where the operator's action is only _rescaling_, with the scale factor called an _eigenvalue_:
$$\hat{\Omega}\ket{V}=\omega\ket{V}$$
- The eigenvectors are _determined up to a multiplicative constant_, and are often _normalised_
- They are often _labelled according to eigenvalue_ $\ket{\omega_i}$

- The eigenvalues are determined using the _characteristic equation_:
$$\det(\hat{\Omega}-\omega \hat{I})=0$$
- From the fundamental theorem of algebra, an $n\times n$ matrix _must have $n$ eigenvectors_
- Eigenvalues can be _degenerate_, and are _not necessarily real_

- If there are $n$ _degenerate eigenvalues_, the corresponding _eigenvectors form an $n$-dimensional subspace_

### Hermitian and unitary matrices
- It can be proven that _the eigenvalues of Hermitian operators are real_
- A Hermitian operator's _eigenvectors form an orthonormal basis_
- In this basis, the _matrix elements are the eigenvalues_ (i.e. the matrix is _diagonalised_)

- As for _unitary operators_, the eigenvectors are _complex numbers of unit modulus_
- The eigenvectors of a unitary operator are also _mutually orthogonal_

- For every Hermitian operator $\hat{\Omega}$, there _is a unitary matrix $\hat{U}$ such that $\hat{U}^\dagger\hat{\Omega}\hat{U}$ is diagonal_
	- The _rows of $\hat{U}$ are the orthonormal eigenvectors_

- Due to the _invariance of determinants and traces under unitary transformations_:
$$\displaylines{\det(\hat{\Omega})=\prod_{i=1}^n\omega_i \\ \text{Tr}(\hat{\Omega})=\sum_{i=1}^n\omega_i}$$

### Simultaneous diagonalisation
- If $\hat{\Omega}$ and $\hat{\Lambda}$ are _two commuting Hermitian operators_, there exists _a basis of common eigenvectors that diagonalises both_
	- Can be proven for both non-degenerate and degenerate cases

- If $\hat{\Lambda}$ is _not degenerate within any subspace_, then the _eigenbasis is unique_
	- The eigenvectors can be _given a unique label $\ket{\omega,\lambda}$ based on the eigenvalues_

- If $\hat{\Lambda}$ is _degenerate within any subspace of $\hat{\Omega}$_, then it is necessary to use _more operators_

- In _general_, if there is a set of $n$ operators $\{\hat{\Omega},\hat{\Lambda},\hat{\Gamma},\dots\}$ that _commute with each other_, one can _always find a unique common eigenbasis_ $\ket{\omega,\lambda,\gamma,\dots}$
- This is assumed to be _true if $n$ is infinite_

## Functions of operators
- The function of an operator can be formally defined via a _power series_:


## Hilbert spaces
- The relevant vector space for quantum mechanics is _the Hilbert space of square-integrable functions_
- Consider there to be a _range_ of $x$, with a _regular interval of sampling points_ $(x_1,x_2,\dots,x_N)$
- If one _samples a function_ $f(x)$ at these points, one ends up with a _vector_ $\ket{f}$
- This _components_ of the vector will be the _values_ at these sampling points:
$$\ket{f}\equiv\begin{bmatrix}f(x_1) \\ f(x_2) \\\vdots \\ f(x_N)\end{bmatrix}$$
- The _basis_ for this can be denoted $\{\ket{x_i}\}$, and just consist of a 1 at the $i$th place with 0's in all other places 
- The _value_ of the function at a specific point can be thought of as a _projection_:
$$f(x)=\braket{x|f}$$

- For any range, there is an _uncountably infinite number of points_
- This requires _infinite dimensions_

- The _inner product is redefined_, with each term _weighted_ in order to keep it finite:
$$\braket{f|g}=\sum_i f^*(x_i)g(x_i) \,\Delta x=\int f^*(x)g(x)\,dx$$
- Thus, one can define a _physical Hilbert space_, consisting of _square-integrable functions_:
$$\braket{f|f}=\int |f(x)|^2\,dx<\infty$$
- One also includes the _generalised function_ of $\exp(ikx)$ in this space

- The _orthonormality condition_ becomes:
$$\braket{x|x'}=\delta(x-x')$$
- The _completeness relation_ then becomes:
$$\int \ket{x'}\bra{x'}\,dx'=I$$
