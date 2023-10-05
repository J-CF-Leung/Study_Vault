- [ ] Finish section from Zee Group Theory 🔼 📅 2023-10-08 

>[!quote]
"This material is almost as dry as the Sahara, or East Anglia"
>-Dr. S. J. Cowley, 2022

>[!quote]
>"You can add vectors, multiply a vector by a number, flip vectors - the fun is just endless"
>-Prof. Ramamurti Shankar

>[!INFO] Notation
>__bold__ $\bm{v}$: vector
>_Italics_ $v_i$: components of vector or matrix
>CM $\textbf{text v}$: vector or matrix within a particular basis

# Linear vector spaces
- A _linear vector space_ $\mathbb{V}$ is a collection of objects $\bm{u},\dots\bm{v},\dots$ called _vectors_
- The vector space is defined over a _field_ of scalars, which are _real_ $\mathbb{R}$ or _complex_ $\mathbb{C}$
- For vectors in $\mathbb{V}$, there must be rules for vector sums and scalar multiplication

## The axioms
- Closure for addition AND scalar multiplication: $\bm{v}+\bm{w}\in\mathbb{V}, a\bm{v}\in\mathbb{V} \textbf{ for } a\in\mathbb{C}$
- Addition is commutative: $\bm{u}+\bm{v}=\bm{v}+\bm{u}$
- Addition is associative: $(\bm{a}+\bm{b})+\bm{c}=\bm{a}+(\bm{b}+\bm{c})$
- Scalar multiplication is distributive in the vectors: $a(\bm{v}+\bm{w})=a\bm{v}+a\bm{w}$
- Scalar multiplication is distributive in the scalars: $(a+b)\bm{v}=a\bm{v}+b\bm{v}$
- Multiplication is associative: $(ab)\bm{v}=a(b\bm{v})$
- There exists a null vector $\bm{0}$ such that $\bm{v+0}=\bm{v}$  $\forall v\in\mathbb{V}$
- There exists an inverse vector $-\bm{v}$ such that $\bm{v}+(-\bm{v})=0$  $\forall \bm{v}\in\mathbb{V}$

## Corollaries and remarks
- The existence of inverse vectors _implies the existence of subtraction_
- Vector multiplication is not defined in general
- A basic example of a vector space is _n-tuples_, where vector addition and scalar multiplication are done _component-wise_

## Span and linear independence
- Let the set $S=\{\bm{u}_1,\bm{u}_2,\dots \bm{u}_n\}$ be a subset of vectors in $\mathbb{V}$ 
- A _linear combination_ of $S$ is a vector of the form:
$$a_1\bm{u}_1+a_2\bm{u}_2+\dots+a_n\bm{u}_n=a_i\bm{u}_i$$
	- Where $a_i$ are scalars

- The _span_ of $S$ is the set of all vectors that are linear combinations of $S$
- If the span of $S$ is the _entire_ vector space $\mathbb{V}$, then $S$ is said to _span $\mathbb{V}$_

- The set of vectors are _linearly independent_ if:
$$a_i\bm{u}_i=0 \iff a_i=0$$
- Otherwise, they are _linearly dependent_ and a linear combination can give the zero vector _with non-zero scalars_

- If the vector space can accmodate _a maximum_ of $n$ linearly independent vectors, or _all sets of_ $n+1$ vectors are linearly dependent, the space has _dimension_ $n$

- If an additional vector is added to a spanning set, it remains a spanning set
- If a vector is removed from a linearly independent set, it will remain linearly independent

## Basis vectors
- If $\mathbb{V}$ is an $n-$dimensional vector space, then _any_ set of $n$ linearly independent vectors $\{\bm{u}_1,\dots\bm{u}_n\}$ is a _basis set_ for $\mathbb{V}$

- For _all_ $\bm{v} \in\mathbb{V}$, there exists scalars $v_i$ such that:
$$\bm{v}=v_i\bm{u}_i$$
- This set of scalars is _unique_
- One can then write out $\bm{v}$ as a _column vector_ $\textbf{v}$ with _components_ $v_i$:
$$\textbf{v}=\pmatrix{v_1\\v_2\\\vdots \\v_n}=\pmatrix{v_1&v_2&\dots &v_n}^T$$

- Let there be a set of vectors $\{\bm{u}_1,\dots\bm{u}_m\}$ in an $n$-dimensional vector space
- If $m>n$, there exists a vector that when expanded with $\{\bm{u}_i\}$, has _non-unique_ scalar coefficients, no matter if $\{\bm{u}_i\}$ is a spanning set 
- If $m<n$, there exists a vector that _cannot_ be expressed as a linear combination of $\{\bm{u}_i\}$

- Infinite dimensional vectors exist, with _infinitely many components_
- These exist in infinite-dimensional spaces known as [[Vectors and matrices in physics#Hilbert spaces|Hilbert spaces]]

### Examples
- 3-dimensional Euclidean space $\mathbb{E}^3$, where the scalars are real
	- Not the same as physical space $\mathbb{R}^3$, which is not necessarily Euclidean

- Complex numbers
	- If defined over $\mathbb{R}$, it is 2-dimensional with basis vectors $\{1,i\}$
	- If defined over $\mathbb{C}$, it is 1-dimensional
	- No the same as $\mathbb{R}^2$ as there is a rule for multiplication

- $2\times2$ real matrices: 4-dimensional
- $2\times2$ real symmetric matrices: 3-dimensional

# Linear operators
- A _linear operator_ acts on a vector space $\mathbb{V}$ to produce _another element_ of $\mathbb{V}$

- Linearity means that for scalars $\alpha$ and $\beta$:
$$\mathcal{A}(\alpha \bm{x}+\beta \bm{y})=\alpha\mathcal{A}\bm{x}+ \beta\mathcal{A}\bm{y}$$
- A linear operator exists _independent of any basis_
- An operation can be thought of as a _linear transformation_ or _mapping_ of $\mathbb{V}$
	- Example: Rotation

## Components and matrices
- The _components_ of $\mathcal{A}$ _with respect to a basis_ $\{\bm{e}_k\}$ is defined by the _action_ of $\mathcal{A}$ on the basis vectors, involving a set of numbers $A_{ij}$, with the _definition_:
$$\mathcal{A}\bm{e}_j=\bm{e}_{i}A_{ij}$$
- These components form a _square matrix_ $\textbf{A}$, where $(\textbf{A})_{ij}=A_{ij}$
$$\textbf{A}= \begin{pmatrix} A_{11} & A_{12} & \dots & A_{1n} \\ A_{21} & A_{22} & \dots & A_{2n} \\ \vdots & \vdots & \ddots & \vdots \\ A_{n1} & A_{n2} & \dots & A_{nn}   \end{pmatrix}$$
- The _lndices_ indicate _row, then column_ IN THAT ORDER
>[!warning] Note on convention
> To keep summing indices together, the _basis vector goes on the left of the components_

- The relation $\mathbb{A}\bm{e}_j=\bm{e}_iA_{ij}$ can then be written as:
$$\textbf{A}\textbf{e}_j=\pmatrix{A_{1j}\\A_{2j}\\\vdots\\A_{nj}}$$
- For a _given basis_ $\{\bm{e}_k\}$, the $j$th column of $\textbf{A}$ gives the _transformed vector_ $\textbf{Ae}_j$
- In other words, $A_{ij}$ gives the $i$th _component_ of the vector $\bm{\psi}_{(j)}\equiv\textbf{Ae}_j$
$$\textbf{A}=\pmatrix{\bm{\psi}_{(1)}&\bm{\psi}_{(2)}&\dots&\bm{\psi}_{(n)}}$$
- Since $\mathcal{A}$ is a linear operator, knowing how it acts on a basis is enough to determine what is does on _any vector_:
$$\displaylines{\mathcal{A}\bm{x}=\mathcal{A}(\bm{e}_jx_j)=\bm{e}_iA_{ij}x_j \\ (\mathcal{A}\bm{x})_i=A_{ij}x_j}$$
>[!warning] Note on convention
> To keep summing indices together, the _vector components_ $x_j$ _go on the right_ (keeping basis vectors on the far left)

- This can be _visualised_ by writing $\bm{x}$ as a _column vector_ and writing out components of $\textbf{A}$:
$$\pmatrix{A_{11}&A_{12} \\ A_{21}&A_{22}}\pmatrix{x_1\\x_2}=\pmatrix{A_{11}x_1+A_{12}x_2 \\ A_{21}x_1+A_{22}x_2}=\pmatrix{x_1\bm{\psi}_{(1)}+x_2\bm{\psi}_{(2)}}$$
- For a _given resultant component/row_, one iterates _along the row of the matrix_, then _along the column vector_
- The components say _how much of each basis vector to transform_

- The _sum_ of two operators is given by a _matrix sum_, which simply _adds components_
$$(\mathcal{A}+\mathcal{B})\bm{x}=\bm{e}_i(A_{ij}+B_{ij})x_j$$

- The product of two operators is given by _applying the operators in succession_:
$$(\mathcal{BA})\bm{x}=\mathcal{B}(\mathcal{A}\bm{x})=\bm{e}_iB_{ik}(\mathcal{A}\bm{x})_k=\bm{e}_iB_{ik}A_{kj}x_j$$
- This defines _matrix multiplication_:
$$(\textbf{BA})_{ij}=B_{ik}A_{kj}$$
- Viewing $\textbf{BA}$ as a set of column vectors $\bm{\phi}_j=\textbf{B}(\textbf{A}\textbf{e}_j)$:
$$\textbf{BA}=\pmatrix{\bm{\phi}_{(1)}&\bm{\phi}_{(2)}&\dots&\bm{\phi}_{(n)}}=\pmatrix{\textbf{B}\bm{\psi}_{(1)}&\textbf{B}\bm{\psi}_{(2)}&\dots&\textbf{B}\bm{\psi}_{(n)}}$$

- Matrix multiplication is _not commutative_, hence neither is the application of operators:
$$\mathcal{AB}\neq\mathcal{BA}\Longleftrightarrow\textbf{AB}\neq\textbf{BA}\Longleftrightarrow A_{ik}B_{kj}\neq B_{ik}A_{kj}$$
- However, it is _associative_:
$$\textbf{A}(\textbf{BC})=(\textbf{AB})\textbf{C}\Longleftrightarrow A_{ik}(B_{kl}C_{lj})=(A_{ik}B_{kl})C_{lj}$$

## Transformations
- Let $\{\bm{u}_i\}$ and $\{\bm{u}_i'\}$ be two sets of basis vectors in an $n$-dimensional $\mathbb{V}$
- One can express the latter basis in terms of a _linear relationship_ with a set of numbers $A_{ij}$
$$\bm{u}_j'=\bm{u}_iA_{ij}$$
- The numbers $A_{ij}$ can be represented by a square $n\times n$ _transformation matrix_ $\textbf{A}$:
$$\textbf{A}= \begin{pmatrix} A_{11} & A_{12} & \dots & A_{1n} \\ A_{21} & A_{22} & \dots & A_{2n} \\ \vdots & \vdots & \ddots & \vdots \\ A_{n1} & A_{n2} & \dots & A_{nn}   \end{pmatrix}$$
- $A_{ij}$ is the _$i$th component of the vector $\bm{u}_j'$ in $\{\bm{u}_i\}$_
	- The _$j^\textbf{th}$ column_ is the components of $\bm{u}_j'$ in $\{\bm{u}_i\}$, and can be treated as a _vector in itself_

- Similarly, the unprimed basis can be described in terms of the primed one:
$$\bm{u}_i=\bm{u}_k'B_{ki}$$
- $B_{ki}$ is the $k$th component of the vector $\bm{u}_i$ in the basis $\{\bm{u}_k'\}$

- Since the basis representation of any vector is _unique_:
$$\textbf{B}=\textbf{A}^{-1}$$
- Hence, $\det{\textbf{A}}\neq 0,\det{\textbf{B}}\neq0$

- Considering the _expansion of $\bm{v}$ in two bases, and using the uniqueness_ of the representations, one can find the relationship between components:
$$\displaylines{\bm{v}=v_i\bm{u}_i=v_j'\bm{u}_j' \\ v_i=A_{ij}v_j'}$$

- Components transform _inversely to the basis vectors_

- By letting $\textbf{v}$ and $\textbf{v}'$ be the column vectors:
$$\textbf{v}=\begin{pmatrix} v_1 \\ v_2 \\ \vdots \\ v_n \end{pmatrix} \hspace{1.5cm} \textbf{v'}=\begin{pmatrix} v_1' \\ v_2' \\ \vdots \\ v_n' \end{pmatrix}$$
- The above relations can be expressed as:
$$\displaylines{\textbf{v}=\textbf{Av'} \iff \textbf{v'}=\textbf{A}^{-1}\textbf{v} 
 \\ \textbf{u'}=\textbf{uA}}$$

## Matrix multiplication


## Special properties of matrices
- Properties of _real_ matrices:
	- Symmetry: equal to transpose
 $$\textbf{A}^T=\textbf{A} \iff A_{ij}=A_{ji}$$
	- Antisymmetric: negative to transpose
 $$\textbf{A}^T=-\textbf{A} \iff A_{ij}=-A_{ji}$$
	- Orthogonal: transpose is inverse
$$\textbf{A}^T=\textbf{A}^{-1} \iff \textbf{A}^T\textbf{A}=I$$
### The Hermitian conjugate
- The _Hermitian conjugate_ of a matrix is defined as _the complex conjugate of the transpose_:
$$\displaylines{A^\dagger = (A^T)^*=(A^*)^T \\ (A^\dagger)_{ij}=(A^*)_{ji}}$$
- For a _column matrix_, its Hermitian conjugate is a _row matrix_

- The Hermitian conjugate of the Hermitian conjugate is the original matrix
- Like the transpose, the Hermitian conjugate of a product of matrices is:
$$(\textbf{AB})^\dagger=\textbf{B}^\dagger \textbf{A}^\dagger$$
- This result _extends to arbitrary products of vectors and matrices_
- The Hermitian conjugate of a scalar is the complex conjugate

### Properties of complex matrices
- Positive definiteness: an $n\times n$ square matrix $\textbf{A}$ is said to be _positive-definite_ if _for all column matrices_ $\textbf{v}$ of length $n$:
$$\textbf{v}^\dagger\textbf{Av}\geq 0,\textbf{ with equality iff v}=0$$
	- If equality is possible for non-zero $\textbf{v}$, $\textbf{A}$ is _positive_ instead of positive definite

- Hermiticity: a square $n\times n$ matrix is _Hermitian_ if it is _equal_ to the Hermitian conjugate:
$$\textbf{A}^\dagger=\textbf{A} \iff A_{ji}^*=A_{ij}$$
- Anti/skew-Hermiticity: 
$$\textbf{A}^\dagger=-\textbf{A} \iff A^*_{ji}=-A_{ij}$$
- Unitarity: A matrix is _unitary_ if its Hermitian conjugate is _equal to its inverse_:
$$\textbf{A}^\dagger=\textbf{A}^{-1} \iff \textbf{AA}^\dagger=I$$
- Normality: A matrix is _normal_ if it _commutes_ with its Hermitian conjugate:
$$\textbf{A}^\dagger\textbf{A}=\textbf{AA}^\dagger$$

- All _Hermitian, anti-Hermitian, and unitary matrices are normal_

# Scalar product/inner product

## Definition
- Defined on an $n$-dimensional vector space $\mathbb{V}$ over $\mathbb{C}$
- The scalar product is _denoted_ $\bm{u\cdot v}\in\mathbb{C}$

- Properties:
	- Linear _in second argument_:
	$$\bm{u}\cdot(a\bm{v}_1+b\bm{v_2})=a\bm{u\cdot v_1}+b\bm{u\cdot v_2}$$
	- Hermitian symmetry:
	$$\bm{u\cdot v}=(\bm{v\cdot u})^*$$
	- The scalar product of a vector with itself should be _positive-definite_:
	$$\bm{v\cdot v}\geq 0$$
		- Equality $\textbf{iff }\bm{v}=0$

- $\bm{v\cdot v}=|\bm{v}|^2$, where $|\bm{v}|$ is the _norm_

- Linearity in the second argument and Hermitian symmetry implies _anti-linearity in the first argument_:
$$(a\bm{u}_1+b\bm{u}_2)\cdot\bm{v}=a^*(\bm{u}_1\cdot \bm{v})+b^*(\bm{u}_2\cdot\bm{v})$$
- Notation:
$$\bm{u}\cdot\bm{v}=\braket{u|v}$$

- Example: scalar product of $2\times 2$ matrices
	- Sum up elements: $\braket{\textbf{A}|\textbf{B}}=A_{ij}^*B_{ij}$
	- Fulfills all properties

## Inequalities
- The Schwarz inequality:
$$|\braket{\bm{u}|\bm{v}}|\leq |\bm{u}||\bm{v}|$$
	- Equality holds when $\bm{u}=\lambda\bm{v}$

- The triangle inequality:
$$|\bm{u}+\bm{v}|\leq |\bm{u}|+|\bm{v}|$$

## Scalar product in terms of components, and the metric
- Suppose there is a scalar product defined in a vector space with basis vectors $\{\bm{u}_i\}$
- Define the complex numbers $G_{ij}$:
$$G_{ij}=\bm{u}_i\cdot\bm{u}_j$$
- For _any_ two vectors:
$$\bm{v}=v_i\bm{u}_i \hspace{1.5cm} \bm{w}=w_j\bm{u}_j$$

- Then, the inner product between these vectors is:
$$\braket{\bm{v}|\bm{w}}=v_i^*G_{ij}w_j=\textbf{v}^\dagger\textbf{Gw}$$
- $G$ is a matrix called the _metric_ of this basis, with entries $G_{ij}$

- A _metric is Hermitian:
$$G_{ij}=(G_{ji})^*$$
- A _metric is positive-definite_:
$$\textbf{v}^\dagger\textbf{Gv}\geq 0\textbf{, equality iff }\bm{v}=0$$

# Eigenvectors, eigenvalues, and diagonalisation

## Definitions of eigenvectors and eigenvalues
- Suppose $\textbf{M}$ is a square $n\times n$ matrix, then if there is a column vector $\textbf{x}$ such that:
$$\textbf{Mx}=\lambda\textbf{x}$$
- $\textbf{x}$ is a _eigenvector_ of the matrix, and $\lambda$ is an _eigenvalue_
- Any _scaled_ version of $\textbf{x}$ is also an eigenvector

- Since $\textbf{x}$ is _non-zero_, then the columns of $\textbf{M}-\lambda\textbf{I}$ are _linearly dependent_:
$$\det(\textbf{M}-\lambda\textbf{I})=0$$
- This is the _characteristic equation_ of the matrix
- The left hand side is the _characteristic polynomial_, which is an $n$th order polynomial in $\lambda$
- The _roots_ of the polynomial are the eigenvalues
- From the fundamental theorem of algebra, $\textbf{M}$ has $n$ eigenvalues (counting repeated roots)
	- Eigenvalues and eigenvectors _are not necessarily real_ (example: rotation matrix)

## Eigenvalues and diagonalisation
- If the $n$ eigenvalues are _distinct_, there are $n$ _linearly independent eigenvectors_
- If they are not distinct, then repeated eigenvalues are said to be _degenerate_

- If an eigenvalue occurs $m$ times, there may be _any number between $1$ and $m$ of linearly independent eigenvectors_
	- Any combination of the linearly independent eigenvectors is _also an eigenvector_
	- The space spanned by them is called an _eigenspace_

- Denote the $n$ eigenvalues by $\lambda_1,\lambda_2,\dots,\lambda_n$
- Let $\textbf{x}^i$ be the respective eigenvectors, obeying (written without summation convention):
$$\displaylines{\textbf{Mx}^i=\lambda_i\textbf{x}^i \\ \sum_k \textbf{M}_{jk} \textbf{x}^i_k=\lambda_ix_j^i}$$
- Let $\textbf{X}$ be the $n\times n$ matrix defined by:
$$\displaylines{\textbf{X}_{ij}=\textbf{x}^j_i \\ \textbf{X}= \begin{pmatrix} 
 x_1^1 & x_1^2 & \dots& x_1^n \\ x_2^1 & x_2^2 & \dots & x_2^n \\ \vdots & \vdots & \ddots & \vdots \\ x_n^1 & x_n^2 & \dots & x_n^n \end{pmatrix}}$$
 
- By writing out components, it can be seen that:
$$\displaylines{\textbf{X}^{-1}\textbf{MX}=\Lambda \\ \Lambda = \pmatrix{ \lambda_1 & 0 & \dots & 0 \\ 0 & \lambda_2 & \dots & 0 \\ \vdots & \vdots & \ddots & \vdots \\ 0 & 0 & \dots & \lambda_n}}$$
- i.e. $\textbf{X}$ _diagonalises_ $\textbf{M}$, as long as $\det(\textbf{X})\neq0$, which means the columns (hence, the eigenvectors), are linearly independent
- In other words, _an $n\times n$ matrix is diagonalisable iff it has $n$ linearly independent eigenvectors_

## Eigenvectors and eigenvalues of special matrices
### Hermitian matrices
- The eigenvalues of a Hermitian matrix _are all real_
- The eigenvectors of a Hermitian matrix _with distinct eigenvalues_ are _orthogonal_
- Proof: Let there be distinct eigenvectors, apply the matrix then subtract them

- For _degenerate_ eigenvalues, _$n$ orthogonal eigenvectors still exist_

- Whether or not eigenvalues are degenerate, an $n\times n$ Hermitian matrix _has $n$ linearly independent eigenvectors_
- It is also _always possible_ to find $n$ eigenvectors that are _orthonormal_

### Other matrices
- The eigenvalues of _anti-Hermitian_ matrices are _purely imaginary_
- The eigenvalues of _unitary_ matrices are _of unit modulus_

- For _normal_ matrices, eigenvectors corresponding to _distinct_ eigenvalues are _orthogonal_
- If a _repeated_ eigenvalue appears $m$ times, there are _exactly $m$_ corresponding linearly independent eigenvectors

- If the multiplicity of an eigenvalue, $m$, matches the number of linearly independent eigenvectors, the matrix is said to have _no defect_
- It is _always possible_ to construct an _orthonormal basis_ with the Gram-Schmidt procedure
- Therefore, _even if eigenvalues are degenerate_, it is possible to find $n$ _mutually orthogonal eigenvectors_ that form a basis for an $n$-dimensional vector space

## Diagonalisation via unitary matrices
- From the above results, _any Hermitian matrix_ $\textbf{H}$ can be diagonalised with a matrix $\textbf{X}$, where the _columns are the eigenvectors_ of $\textbf{H}$
- If all these eigenvectors are _orthonormal_, it can be proven that $\textbf{X}$ _must be unitary_

- Hence, _all Hermitian matrices are diagonalisable via some unitary matrix_
- For _real_ matrices, all symmetric matrices are diagonalisable by some orthogonal matrix

- For a _general_ $n\times n$ matrix $\textbf{M}$ with $n$ _distinct eigenvalues_ $\lambda_i$, it is possible to show that that there are $n$ _linearly independent eigenvectors_ $\textbf{x}^i$ 
- If there are _degenerate_ eigenvalues, it _may or may not_ have $n$ linearly independent eigenvectors
	- If any eigenvectors are linearly dependent, $\det(\textbf{X})=0$ and $\textbf{M}$ is _not diagonalisable_

- For _normal_ matrices, since there are _always $n$ linearly independent eigenvectors_, they are _always diagonalisable regardless of degeneracy_
	- Hence, _anti-Hermitian_ and _unitary_ matrices are _always diagonalisable_

# Change of basis

## Change of basis for the metric
- Vector components can be [[#Transformation matrices|transformed between bases]] $\{\bm{u}_i\}$ and $\{\bm{u}_i'\}$ 
- The components of an arbitrary vector $\bm{v}$ transform as:
$$\textbf{v}=\textbf{Av}'$$
- $A_{ij}$ is the _$i$th component of the vector $\bm{u}_j'$ in $\{\bm{u}_i\}$_
	- The _$j^\textbf{th}$ column of the matrix is the components_ of $\bm{u}_j'$ in $\{\bm{u}_i\}$

- By considering the _inner product of two arbitrary vectors_, expressed in the two bases, the _metric in the new basis_ is:
$$\textbf{G}'=\textbf{A}^\dagger\textbf{GA}$$
- By taking the Hermitian conjugate of the whole basis, it can be confirmed that _Hermiticity is preserved for any transformation_

- If the transformation matrix is _the matrix of $\textbf{G}$'s eigenvectors_ $\textbf{X}$, $\textbf{G}$ _can be diagonalised_
	- Always true since _$\textbf{G}$_ _is Hermitian_
- Since $\textbf{G}$ is _positive-definite_, it can be shown that _the eigenvalues are all strictly positive_, $\textbf{G}$ _can be diagonalised 

## Orthonormal bases
- Once the metric is _diagonalised_, the new basis vectors $\{\bm{u}_i'\}$ are _the eigenvectors of $\textbf{G}$_
- Since $\textbf{G}$ is Hermitian, this new basis set _is orthogonal_, therefore:
$$\bm{u}_i'\cdot \bm{u}_j'=G_{ij}'=\Lambda_{ij}=\lambda_i\delta_{ij}$$
- Since $\lambda_i$ are _strictly positive_, the basis _can be normalised_:
$$\bm{e}_i=\frac{1}{\sqrt{\lambda_i}}\bm{u}'_i$$
- Hence, the set of vectors $\{\bm{e}_i\}$ is _an orthonormal basis_
- So we can conclude that _any vector space with a scalar product has an orthonormal basis_
- In this orthonormal basis, _the metric is the identity matrix_

- In this basis, the scalar product $\bm{v}\cdot\bm{w}$ can be simplified to the familiar expression:
$$\bm{v}\cdot\bm{w}=\textbf{v}^\dagger\textbf{Gw}=\textbf{v}^\dagger\textbf{Iw}=\textbf{v}^\dagger\textbf{w}$$
- If the vectors are orthogonal, this just becomes 0


## Transform between orthonormal bases
- Given an orthonormal basis $\{\bm{e}_i\}$, tranform to a new orthonormal basis $\{\bm{e}_i'\}$
- Let the transformation matrix be:
$$\bm{e}_i'=\bm{e}_kU_{ki}$$
- The new metric transforms as:
$$\textbf{G}=\textbf{U}^\dagger\textbf{GU}=\textbf{U}^\dagger\textbf{IU}$$
- Since the new basis is orthonormal:
$$\textbf{U}^\dagger \textbf{U}=\textbf{I}$$
- Hence, $\textbf{U}$ is _unitary
	- Real vector space: orthogonal

## More on diagonalisation
- Many operations are easier when done in diagonalised matrices
- Using the properties:
$$\det(\textbf{AB})=\det(\textbf{A})\det(\textbf{B}) \hspace{1.5cm} \textbf{tr}(\textbf{AB})=\textbf{tr}(\textbf{A})\textbf{tr}(\textbf{B})$$
- Given:
$$\textbf{X}^\dagger\textbf{MX}=\Lambda \hspace{1cm} \textbf{or} \hspace{1cm} \textbf{M}=\textbf{X}^\dagger\Lambda\textbf{X}$$
- Useful relations:
$$\displaylines{\textbf{M}^n=\textbf{X}^\dagger\Lambda^n\textbf{X} \\ \det(\textbf{M})=\prod_i\lambda_i \\ \textbf{tr}(\textbf{M})=\sum_i\lambda_i}$$

# Forms
- A _form_ is a map $\mathcal{F}(\textbf{x})$ where:
$$\mathcal{F}(\textbf{x})=\textbf{x}^\dagger\textbf{Ax}=x_i^*A_{ij}x_j$$
- $\textbf{A}$ is the _coefficient matrix_ of the form

- If $\textbf{A}$ is Hermitian (denoted $\textbf{H}$), it is known as a _Hermitian form_
	- It can easily be proven that _Hermitian forms are real_

- In a _real vector space_ (i.e. $\textbf{x}$ and $\textbf{H}$), $\textbf{H}=\textbf{S}$, a _real symmetric matrix_
- In this case:
$$\mathcal{F}(\textbf{x})=\textbf{x}^T\textbf{Sx}=x_iS_{ij}x_j$$
- This is known as a _quadratic form_

## Principal axes
- The coefficient matrix $\textbf{H}$ of a Hermitian form can be written as:
$$\textbf{H}=\textbf{U}^\dagger\Lambda\textbf{U}$$
- By transforming $\textbf{x}$:
$$\textbf{x}'=\textbf{U}^\dagger\textbf{x}$$
- The form can be written as:
$$\mathcal{F}(\textbf{x})=\sum_i\lambda_i|x'_i|^2$$
- The form _has no off-diagonal terms_
- The orthonormal basis vectors are known as the _principal axes_

## Quadrics and conics
- A _quadric surface_ is an $n$-dimensional hypersurface defined by the _zeros of a real quadratic polynomial_
- For any general quadric:
$$x_iA_{ij}x_j+b_ix_i+c\equiv\textbf{x}^T\textbf{Ax}+\textbf{b}^T\textbf{x}+c=0$$
- By swapping indices, it can be shown that this can be written as:
$$\textbf{x}^T\textbf{Sx}+\textbf{b}^T\textbf{x}+c=0$$
- Here, $\textbf{S}=(\textbf{A}+\textbf{A}^T)/2$

- By taking the principal axes as the basis:
$$\textbf{x}'^T\Lambda\textbf{x}'+\textbf{b}'^T\textbf{x}'+c=0$$
- By translating $\textbf{x'}$ by $-\Lambda^{-1}\textbf{b'}/2$:
$$\textbf{x}'^T\Lambda\textbf{x}'=k$$

### Conic sections
- For $n=2$:
$$\textbf{x}'=\pmatrix{1 \\ 2} \hspace{1.5cm} \Lambda=\pmatrix{\lambda_1 & 0 \\ 0 & \lambda_2}$$

- If $\textbf{A}$ has all non-zero eigenvalues, the equation becomes:
$$\lambda_1\textbf{x}'^2+\lambda_2\textbf{y}'^2=k$$


## Rayleigh-Ritz method
- In an orthonormal basis, let $\textbf{x}$ be a point on the surface $\textbf{x}^T\textbf{Sx}=k$
- The _relative distance_ from the origin, independent of $k$, is:
$$(\textbf{relative distance})^2=\frac{\textbf{x}^T\textbf{x}}{\textbf{x}^T \textbf{Sx}}$$
- Look for a point where the _inverse of distance_ (hence the distance itself) is _stationary_:
$$\displaylines{\lambda(\textbf{x})=\frac{\textbf{x}^T\textbf{Sx}}{\textbf{x}^T\textbf{x}} \\ \delta\lambda(\textbf{x})\equiv\lambda(\textbf{x}+\delta\textbf{x})-\lambda(\textbf{x})=0}$$
- By expanding $\lambda(\textbf{x}+\delta\textbf{x})$, one finds that this is satisfied for all $\delta\textbf{x}$ when:
$$\textbf{Sx}=\lambda(\textbf{x})\textbf{x}$$
- Hence, _the eigenvectors of $\textbf{S}$ are directions that make the relative distance stationary_
- And, _the eigenvalues of $\textbf{S}$ are the values of $\lambda$ at the stationary points_

- By a similar argument, for a Hermitian matrix $\textbf{H}$, its eigenvalues are given by:
	$$\lambda(\textbf{x})=\frac{\textbf{x}^\dagger\textbf{Hx}}{\textbf{x}^\dagger\textbf{x}}$$
	_evaluated at the stationary points_



