>[!quote]
>"A tensor is an object that transforms like a tensor"
>-Pure mathmos, probably

- Notation: [[Einstein notation]]
- Only _Cartesian coordinates_, i.e. a system _independent of position_, will be used

# Vectors
- A vector is an example of a _first-rank tensor_

## What even is a vector
- A vector is a mathematical object _independent of the coordinate system used_
- For a coordinate system with basis vectors $\hat{\bm{e}}_i$, the vector is written as:
$$\bm{v}=v_i\bm{e}_i$$
- In an _orthonormal coordinate system_, $\bm{e}_i\cdot\bm{e}_j=\delta_{ij}$
- In this case, the components are given by:
$$v_j=\bm{v}\cdot\bm{e}_i$$
- For a _different coordinate system_ with basis vectors $\bm{e}_j'$:
$$\bm{v}=v_i'\bm{e}_i$$
- This is a _passive transformation_, where the coordinate system changes but _the vector remains unchanged_

- The components can be written as:
$$v_i'=v_j\bm{e}_j\cdot\bm{e}_i'=L_{ij}v_j$$
- Here, $\text{L}$ is the _transformation matrix_, with components:
$$L_{ij}=\bm{e}_i'\cdot\bm{e}_j$$
- Let $v$ and $v'$ be the _column vectors_, representing _the same abstract vector_:
$$v'=\text{L}v$$
- The basis vectors can be written as:
$$\bm{e}_i'=L_{ij}\bm{e}_j$$

- By _interchanging primed and unprimed bases_, one can find:
$$\displaylines{v_j=L_{ij}v_i'=(L^T)_{ji}v_i' \\ v=\text{L}^Tv'}$$
- Thus, one can prove that $\text{L}$ is _orthogonal_:
$$\text{LL}^T=\text{I}$$

- The _definition of a Cartesian vector_ is a _set of components_ $v_i$, defined with respect to _orthonormal coordinate system_ $\bm{e}_i$, such that the coefficients $v_i'$ with respect to _another_ orthonormal coordinate system $\bm{e}_i'$ are _given by an orthogonal transformation_ of the form:
$$v_i'=L_{ij}v_j \hspace{0.5cm}\text{ where } \hspace{0.25cm} L_{ij}=\bm{e}_i'\cdot\bm{e}_j$$

- Example: It can be proven that $\nabla$ transforms in this way, hence it is a vector _in a Cartesian coordinate system_
	- It is really a _covector_

## Axial vectors
- An orthogonal matrix has _determinant_ $\pm1$

- If $\det(\text{L})=+1$, then represents a _proper rotation_
- If $\det{\text{L}}=-1$, then it represents an _improper rotation_, which is a _rotation with a reflection_

- If $\text{L}^{(1)}$ and $\text{L}^{(2)}$ are both proper rotations, then so is $\text{L}^{(1)}\text{L}^{(2)}$, as _rotations form a subgroup_
- Meanwhile, _two improper rotations yield a proper rotation_

- A _Cartesian axial vector_ (or _pseudovector_) $\bm{a}$ is a _set of components_ $a_i$, defined with respect to _orthonormal coordinate system_ $\bm{e}_i$, such that the coefficients $a_i'$ with respect to _another_ orthonormal coordinate system $\bm{e}_i'$ are given by:
$$a_i'=\det(\text{L})L_{ij}a_j\hspace{0.5cm}\text{ where } \hspace{0.25cm} L_{ij}=\bm{e}_i'\cdot\bm{e}_j$$
- When $\det({\text{L}})=1$, its transformation is the same as a vector
- When $\det(\text{L})=-1$, the _handedness of the coordinate system is reversed_
- Examples: Angular momentum, any cross product

# Tensors
- Tensors are a _generalisation_ of vectors