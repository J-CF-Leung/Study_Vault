- Physical quantities and laws can be expressed in _geometric forms_, i.e. _independent of any coordinate system, basis vectors, or reference frames_
	- This can be viewed as a _Newtonian version_ of one of the [[Relativity#The fundamental principles of Einsteinian relativity|principles of Einsteinian relativity]]

- Instead of describing tensors using _components_, they can be interpreted as _vector-valued linear function of vectors_

- Laws are in fact _constrained_ by the fact that they are _coordinate and basis independent_
- Instead, they are _geometric relationships_ between _geometric objects_ such as vectors and tensors
# Mathematical prerequisites

## Vectors
- _Points_ in $3-$space are denoted $\mathcal{P}$
- Some physical quantities are represented by _scalars_, which are _usually real_
- A _vector_ in $3-$space is _between two points_, such as from an _origin_ to some point
	- From some origin: denoted $\bm{x}$
	- Between some other two points: typically denoted $\Delta\bm{x}$

- The _translation_ of vectors is _unambiguous in Euclidean space_ due to _parallelism_
- Hence, a vector can be treated as _completely determined by length and direction_

- This _distance_ $\Delta\sigma$ between two points is the _magnitude of the vector_ $|\Delta\bm{x}|$:
$$|\Delta\bm{x}|^2\equiv(\Delta\bm{x})^2\equiv(\Delta\sigma)^2$$
- When the points are _infinitesimally close_, $\Delta\bm{x}$ becomes the _infinitesimal displacement_ $d\bm{x}$
- Any _finite vector_ is composed of _infinitesimal ones_ from vector addition
	- Vector _addition_ is _independent of components_

![[Vector addition.png|600]]

- Vectors can also be _rotated_, either by _directly rotating the physical vector_, or by _rotating a basis with the vector being fixed_
- The space of _all physically possible changes of length and direction at a point_ is known as the point's _tangent space_

### Curves
- A _path_ through space can be constructed with a _sequence of_ $d\bm{x}$ vectors, resulting in a _curve_ $\mathcal{C}$ to which $d\bm{x}$ are tangent
- Points _on the curve_ can be denoted $\mathcal{P}(\lambda)$, with $\lambda$ being a _parameter along the curve_
- Letting $\bm{x}$ be from $\mathcal{O}$ to $\mathcal{P}(\lambda)$, the _infinitesimal vector_ constructing the curve at that point:
$$d\bm{x}=\frac{d\mathcal{P}}{d\lambda}d\lambda=\frac{d\bm{x}}{d\lambda}d\lambda$$
- $d\bm{x}/d\lambda$ is known as the _tangent vector_ of the curve at $\mathcal{P}(\lambda)$
### Products
- Given _a pair of vectors at the same point_, they can define a _parallelogram_
- The _cross product_ between the vectors is the _vector orthogonal to the parallelogram_, with the _length equal to the area_

- If a vector is _rotated towards the other_ by a _right angle_, then the _area of the new parallelogram_ is the _inner product_
- The _inner product_ can also be defined by:
$$\bm{A}\cdot\bm{B}\equiv\frac{1}{4}\left[(\bm{A}+\bm{B})^2-(\bm{A}-\bm{B})^2\right]$$

### Fields and spatial derivatives
- One can _associate a scalar/vector to each point in a region of space_
- This is known as a _scalar/vector field_

- The _difference of a scalar_ between points separated by $d\bm{x}$ is known as the _gradient_
- Similarly, the _divergence_ and _curl_ are defined using these _spatial derivatives_

## Tensor algebra

### Tensors (and vectors) as linear functions
- A _rank $n$ tensor_ $\textbf{T}$ can be treated as a _linear function of $n$ vectors_ which _outputs a real scalar_
	- Example: if $\textbf{T}$ is a rank-3 tensor, $\textbf{T}(\bm{A},\bm{B},\bm{C})$ is a real scalar
- [[Cartesian tensors|Component-focused treatment of tensors]]
- _Linearity_:
$$\textbf{T}(e\bm{E}+f\bm{F},\bm{B},\bm{C})=e\,\textbf{T}(\bm{E},\bm{B},\bm{C})+f\,\textbf{T}(\bm{F},\bm{B},\bm{C})$$

- The [[#Products|inner product]] is a _function of two vectors_, and therefore can be regarded as a _tensor of rank $2$_, known as the _metric tensor_ $\textbf{g}$:
$$\textbf{g}(\bm{A},\bm{B})=\bm{A}\cdot\bm{B}$$
- The metric tensor is _symmetric_, as $\bm{A}\cdot \bm{B}=\bm{B}\cdot \bm{A}$

- A vector can then be regarded as a _tensor of rank one_:
$$\bm{A}(\bm{C})=\bm{A}\cdot\bm{C}$$

- "Inputting" only _one vector into a rank 2 tensor_ will output _another vector_
	- Example: given the _moment of inertia_ $\textbf{I}$, and "inputting" _angular velocity_ $\bm{\Omega}$ gives the _angular momentum vector_ $\bm{J}(\_)=\textbf{I}(\_,\bf{\Omega})$ 

### Outer product and contraction
- Tensors can be _constructed from vectors_, using the _tensor product_ or _outer product_:
$$\bm{A}\otimes\bm{B}\otimes\bm{C}(\bm{E},\bm{F},\bm{G})\equiv\bm{A}(\bm{E})\bm{B}(\bm{F})\bm{C}(\bm{G})=(\bm{A}\cdot\bm{E})(\bm{B}\cdot\bm{F})(\bm{C}\cdot\bm{G})$$
- Outer products can also be performed _between two tensors of different rank_:
$$\textbf{T}\otimes\textbf{S}(\bm{E},\bm{F},\bm{G},\bm{H},\bm{J})=\textbf{T}(\bm{E},\bm{F})\,\textbf{S}(\bm{G},\bm{H},\bm{J})$$
- Given _rank $n$_ tensor $\textbf{T}$ and _rank_ $m$ tensor $\textbf{S}$, the resultant tensor $\textbf{T}\otimes\textbf{S}$ has rank $n+m$

- _Contraction_ will _reduce_ the rank of a tensor _by two_:
$$\text{contraction}(\bm{A}\otimes\bm{B})\equiv\bm{A}\cdot\bm{B}$$
- For a tensor of _rank $n>2$_, the _indices to contract must be specified_:
$$\text{contract 1,3}(\bm{A}\otimes\bm{B}\otimes\bm{C}+\bm{E}\otimes\bm{F}\otimes\bm{G}+\dots)=(\bm{A}\cdot\bm{C})\bm{B}+(\bm{E}\cdot\bm{G})\bm{F}+\dots$$
# The laws of motion
- At _time_ $t$, the particle has position $\bm{x}(t)$
- The _velocity $\bm{v}$_, _momentum_ $\bm{p}$, _acceleration_ $\bm{a}$, and _kinetic energy_ $E$ are:
$$\bm{v}(t)=\frac{d\bm{x}}{dt}\hspace{1cm}\bm{p}(t)=m\bm{v}(t) \hspace{1cm} \bm{a}(t)=\frac{d\bm{v}}{dt}=\frac{d^2\bm{x}}{dt^2}\hspace{1cm}E(t)=\frac{1}{2}m\bm{v}^2=\frac{\bm{p}^2}{2m}$$
- All of these are _geometric objects_
- Given the _freedom to translate_ vectors, one can associate a _single vector_ with a _group of particles or an extended body_

- _Newton's second law_ states that given a _force_ $\bm{F}$:
$$\bm{F}=m\bm{a}=\frac{d\bm{p}}{dt}$$
- Example: the [[Electromagnetism#The Lorentz Force and the Biot-Savart Law|Lorentz force]]
$$\frac{d\bm{p}}{dt}=q(\bm{E}+\bm{v}\times\bm{B})$$

- _Properties_ of certain kinds of motion, such as _conserved quantities_, can be _derived geometrically_
- Example: Kepler's _equal area_ rule derived _with no coordinates/components_
	- With _no gravitational force_, the planet has _constant velocity_, and one finds that the _triangles swept in an infinitesimal time interval have equal areas_
	- With the _gravitational force_, since it is _radial_, it can be shown that the _infinitesimal swept area is unchanged to the first order_
	- [[Orbits#Elliptical orbits and Kepler's Laws|Analysis using radial coordinates]]

# Component representation
- Notation: [[Einstein notation|Einstein summation notation]], tensor components are labelled with _index notation_

- In _Euclidean_ 3-space, one often uses a set of [[Vectors and matrices#Orthonormal bases|orthonormal basis vectors]] $\{\bm{e}_1,\bm{e}_2,\bm{e}_3\}$
- They are associated with a _Cartesian coordinate system_:
$$\{x,y,z\}\equiv\{x^1,x^2,x^3\}\equiv\{x_1,x_2,x_3\}$$
- $\bm{e}_j$ points _along_ the $x_j$ direction, and the _orthonormality_ can be expressed as:
$$\bm{e}_j\cdot\bm{e}_k=\delta_{jk}$$

- _Any vector_ $\bm{A}$ can be _expanded_, and the components can be found by:
$$\bm{A}=A_j\bm{e}_j \hspace{1cm} A_j=\bm{A}\cdot\bm{e}_j$$
- _Any tensor_ $\textbf{T}$ can then be _expanded_ in terms of the _tensor products of basis vectors_:
$$\textbf{T}=T_{ijk}\,\bm{e}_i\otimes\bm{e}_j\otimes\bm{e}_k$$
- Using the [[#Outer product and contraction|definition of the outer product]], the components are:
$$T_{ijk}=\textbf{T}(\bm{e}_i,\bm{e}_j,\bm{e}_k)$$

- For example, the [[#Tensors (and vectors) as linear functions|metric tensor]] has components:
$$g_{jk}=\textbf{g}(\bm{e}_j,\bm{e}_k)=\bm{e}_j\cdot\bm{e}_k=\delta_{jk}$$
- Given a tensor formed by a _tensor product_, the components are the _product of the components of the original vectors_
$$(T\otimes S)_{ijklm}=T_{ijk}S_{lm}$$
- In _component notation_, by _expanding_ the vectors in terms of components, one can write:
$$\bm{A}\cdot\bm{B}=A_jB_j \hspace{1cm} \textbf{T}(\bm{A},\bm{B},\bm{C})=T_{ijk}A_iB_jC_k$$

- As for _contraction_, the components of the contracted tensor is a _sum of original components over two indices_
$$\text{components of [1\&3 contraction of } \textbf{R}] = R_{ijik}$$

- If two tensors have _the same set of components_, but with _swapped indices_:
$$F_{ab}=G_{ba}$$
- For this to be _true in one basis_, it has to be _the same in all bases_, hence this is _still a basis-independent, geometric statement_
## Laws of motion in index notation
- [[#The laws of motion]] expressed using the _vector components_ are:
$$\displaylines{v_i=\frac{dx_i}{dt}\hspace{1cm}p_i=mv_i\hspace{1cm}a_i=\frac{dv_i}{dt}=\frac{d^2x_i}{dt^2} \\ E=\frac{1}{2}mv_jv_j \hspace{1cm} \frac{dp_i}{dt}=q(E_i+\epsilon_{ijk}v_jB_k)}$$
- This is still _basis-independent_, although it can be _interpreted_ as being in terms of _a particular Cartesian coordinate system_

## Orthogonal transformations of bases
- Consider _two different Cartesian coordinate systems_ $\{x,y,z\}\equiv\{x_1,x_2.x_3\}$, and $\{\bar{x},\bar{y},\bar{z}\}\equiv\{x_\bar{1},x_\bar{2},x_\bar{3}\}$, with _bases_ $\{\bm{e}_i\}$ and $\{\bm{e}_\bar{p}\}$
- One can _expand_ the basis vectors of one basis _in terms of those of the other_:
$$\bm{e}_i=\bm{e}_\bar{p}R_{\bar{p}i} \hspace{1cm} \bm{e}_\bar{p}=\bm{e}_iR_{i\bar{p}}$$
- $R_{\bar{p}i}$ and $R_{i\bar{p}}$ are the components of a _transformation matrix_:
$$[R_{\bar{p}i}]=\begin{bmatrix}R_{\bar{1}1}&R_{\bar{1}2}&R_{\bar{1}3}\\R_{\bar{2}1}&R_{\bar{2}2}&R_{\bar{2}3}\\R_{\bar31}&R_{\bar{3}2}&R_{\bar{3}3}\end{bmatrix}$$
	- The components on the $i-$th _column_ are the _components of_ $\bm{e}_i$ in the $\{\bm{e}_\bar{p}\}$ basis

- These two matrices must be _inverses_ of each other:
$$R_{i\bar{p}}R_{\bar{p}j}=\delta_{ij}$$
- The _orthonormality_ of the two bases implies that the _transverse_ of a transformation matrix must be its _inverse_:
$$\displaylines{\delta_{ij}=\bm{e}_i\cdot\bm{e}_j=(R_{\bar{p}i}R_{\bar{q}j})\bm{e}_\bar{p}\cdot\bm{e}_\bar{q}=R_{\bar{p}i}R_{\bar{p}j} \\ R_{i\bar{p}}=(R_{\bar{p}i})^{-1}=(R_{\bar{p}i})^T}$$
- These _transformations between orthonormal bases_ are represented by _orthogonal matrices_, which are associated with _reflections and rotations_
	- This _does not imply the matrix is symmetric_
	- Example: rotating by angle $\phi$ _about_ the $z-$axis:
	$$[R_{\bar{p}i}]=\begin{bmatrix}\cos\phi & \sin\phi & 0 \\ -\sin\phi & \cos\phi & 0 \\ 0&0&1\end{bmatrix}$$

- Vectors have _components depending on the basis_:
$$\displaylines{\bm{A}=A_i\bm{e}_i=A_i(R_{\bar{p}i}\bm{e}_p)=(R_\bar{pi}A_i)\bm{e}_\bar{p}=A_\bar{p}\bm{e}_\bar{p} \\ A_\bar{p}=R_{\bar{p}i}A_i}$$
- Similarly, for _components of tensors_:
$$T_{\bar{p}\bar{q}\bar{r}}=R_{\bar{p}i}R_{\bar{q}j}R_{\bar{r}k}T_{ijk}$$
- These transformation laws are _different to those of the bases_:
$$\displaylines{\bm{e}_\bar{p}=\bm{e}_iR_{i\bar{p}} \\ A_\bar{p}=R_{\bar{p}i}A_i\hspace{1cm }T_{\bar{p}\bar{q}\bar{r}}=R_{\bar{p}i}R_{\bar{q}j}R_{\bar{r}k}T_{ijk}}$$
- Useful convention:
	- Indices to _sum over_ are on the _"same side"_
	- _Basis_ vectors _before transformation_ go on the _left_
	- Vector/tensor _components before transformation_ go on the _right_

- These laws _do not imply_ that the physical vectors _share an origin_
- If the basis sets have the _same origin_, then the _components are equal to the coordinates_ in those basis sets
- Hence, the _coordinates follow the transformation laws_

- The _product_ of two rotation matrices $[R_{i\bar{p}}R_{\bar{p}\bar{\bar{s}}}]$ is _another rotation matrix_ $[R_{i\bar{\bar{s}}}]$
- This means the rotation matrices form a [[Rotations and Lie Algebra|rotation group]]

# Differentiation of scalars, vectors and tensors
- Consider a _tensor field_ $\textbf{T}(\mathcal{P})$ in Euclidean 3-space
	- The tensor is _dependent_ on the vector $\bm{x}_\mathcal{P}$ from some arbitrary origin ($\bm{x}_\mathcal{P}$ is not in any of the slots)
- Along some _vector_ $\bm{A}$, one defines the _directional derivative_ of $\textbf{T}$ along $\bm{A}$ as:
$$\nabla_\bm{A}\textbf{T}(\mathcal{P})=\lim_{\epsilon\to0}\frac{1}{\epsilon}\left[\textbf{T}(\bm{x}_\mathcal{P}+\epsilon\bm{A})-\textbf{T}(\bm{x}_\mathcal{P})\right]$$
- This also applies to _vector fields_ $\bm{B}(\mathcal{P})$ and _scalar fields_ $\psi(\mathcal{P})$
- The directional derivative is _the same rank as_ $\textbf{T}$

- Hence, there is some tensor $\nabla\textbf{T}$, known as the _gradient_ of $\textbf{T}$
- If $\textbf{T}$ has rank $n$, $\nabla\textbf{T}$ has rank $n+1$:
$$\nabla_\bm{A}\textbf{T}=\nabla\textbf{T}(\_,\_,\dots,\_,\bm{A})$$

- The gradient is written in _index notation_ as:
$$T_{i_1i_2\dots i_n;j}$$
- The _directional derivative_ is then:
$$(\nabla_\bm{A}\textbf{T})_{i_1i_2\dots i_n}=T_{i_1i_2\dots i_n;j}A_j$$
- Then one can prove that in _any Cartesian coordinate system_:
$$T_{i_1i_2\dots i_n;j}=\pd{T_{i_1i_2\dots i_n}}{x_j}\equiv T_{abc,j}$$
- This _does not apply to curvilinear coordinate systems_

- From the definition of the derivative, _product rules apply_:
$$\displaylines{\nabla_\bm{A}(\textbf{S}\otimes\textbf{T})=(\nabla_\textbf{A}\textbf{S})\otimes\textbf{T}+\textbf{S}\otimes(\nabla_\textbf{A}\textbf{T} \\ (S_{ab}T_{cde})_{;j}A_j=(S_{ab;jA_j})T_{cde}+S_{ab}(T_{cde;j}A_j)  \\ \\\nabla_\bm{A}(f\textbf{T})=(\nabla_\textbf{A}f)\textbf{T}+f(\nabla_\bm{A}\textbf{T})\\ (fT_{abc})_{;j}=(f_{;j}A_j)T_{abc}+f(T_{abc;j}A_j)}$$
