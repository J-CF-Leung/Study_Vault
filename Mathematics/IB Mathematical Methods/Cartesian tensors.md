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
- They have a meaning _independent of coordinate basis_, and the _components can be measured w.r.t. some basis_

- Example: Conductivity $\sigma$
- In two different bases:
$$J_i=\sigma_{ij}E_j \hspace{1cm} J_i'=\sigma'_{ij}E_j'$$
- From the transformation laws:
$$J_i'=L_{il}J_l=L_{il}\sigma_{lm}E_m=L_{il}\sigma_{lm}L^T_{mj}E_{j}'$$
- From this, one can deduce that:
$$\sigma'_{ij}=L_{il}L_{jm}\sigma_{lm} \hspace{1cm} \sigma'=L\sigma L^T$$
- The components _transform inversely to the basis vectors_
- $\sigma$ is known as a _second-rank tensor_

- A _Cartesian tensor_ $T$ of _order/rank_ $n$ is a _set of coefficients_ $T_{i_1i_2\dots i_n}$, labelled by $n$ indices, defined w.r.t. an orthonormal basis $\bm{e}_i$, such that the coefficients _defined w.r.t. another orthonormal basis_ $\bm{e}_i'=L_{ij}\bm{e}_j$ are given by the _transformation law_:
$$T'_{i_1\dotsi_n}=L_{i_1j_1}L_{i_2j_2}\dots L_{i_nj_n}T_{i_1\dots i_n}$$
- A _zeroth rank_ tensor is a _scalar_
- A _first rank_ tensor is a _vector_

- Similarly, a _Cartesian pseudotensor_ $E$ transforms as:
$$E'_{i_1\dotsi_n}=L_{i_1j_1}L_{i_2j_2}\dots L_{i_nj_n}E_{i_1\dots i_n}$$
- A _first rank pseudo-tensor_ is a _pseudo-vector_

- The _Kroncecker delta_ is a _tensor_
- Meanwhile, the _Levi-Civita symbol_ is a _pseudotensor_

- Second-rank tensors: Stress, strain, inertia
- Third rank tensors: Piezo-electric tensor
- Fourth rank tensors: Stiffness

## Operations on tensors

### Addition
- Let $A_{i_1\dots i_n}$ and $B_{i_1\dots i_n}$ be tensors of order $n$, and $\alpha$,$\beta$ be _scalars_
- Then, the _linear combination_:
 $$C_{i_1\dots i_n}=\alpha A_{i_1\dots i_n}+\beta B_{i_1\dots i_n}$$
- This is _another tensor of order $n$_
- It obey _the same transformation law_

### Outer/tensor product
- Let $A_{i_1\dots i_n}$ and $B_{i_1\dots i_m}$ be tensors of order $n$ and $m$ respectively
- Then, the _tensor product_:
$$C_{i_1\dots i_{n}i_{n+1}\dots i_{n+m}}=A_{i_1\dots i_n}B_{i_{n+1}\dots i_{n+m}}$$
- $\text{C}$ is a _tensor of order_ $n+m$
- Proof: Apply the transformation law

- This is denoted:
$$\text{C}=\text{A}\otimes \text{B}$$
- Any tensor can then be written as:
$$\text{T}=T_{i_1\dots i_n}\bm{e}_{i_1}\otimes\bm{e}_{i_2}\dots\otimes \bm{e}_{i_n}$$
- If $\text{A}$ is a _pseudo-tensor_, and $\text{B}$ is a _tensor_, then $\text{C}=\text{A}\otimes \text{B}$ is a _pseudo-tensor_
- If both are _pseudo-tensors_, then the result is a _tensor_

### Contraction/inner product
- If $T_{i_1\dots i_m}$ is a tensor of order $m$, and _two indices are set identical then summed over_, it is _contracted by two orders_ to produce $\text{S}$, a tensor of order $m-2$:
$$\displaylines{S_{i_1\dots i_{k-1}i_ki_{k+1}\dots i_{l-1}i_li_{l+1}\dots i_m}=T_{i_1\dots i_{k-1}i_ki_{k+1}\dots i_{l-1}i_ki_{l+1}\dots i_m} \\ S_{ij\dots m}=T_{ijk\dots km}}$$
- If $\text{T}$ is a second-rank tensor, then its contraction is a _scalar_

### Examples
- If $\text{T}$ is a _second-rank tensor_, then $\text{tr}(\text{T})=T_{ii}$ is a _scalar_
- If $\bm{u}$ and $\bm{v}$ are _vectors_, then the outer product $\text{T}=\text{u}\otimes\text{v}$, or $T_{ij}=u_iv_j$ is a _second-rank tensor_
- Meanwhile, $T_{ii}=u_iv_i=\braket{\bm{u}|\bm{v}}$ is a _scalar_, or zeroth-rank tensor
- If $\text{A}$ is a second-rank tensor and $\bm{u}$ is a vector, then $v_i=A_{ij}u_j$ is a _vector_, since the rank is $(2+1)-2=2$
	- Thought of as _outer product with one contraction_
- If $\text{A}$ and $\text{B}$ are second-rank tensors, then the _matrix product_ $C_{ij}=A_{ij}B_{jk}$ is another second-rank tensor since $(2+2)-2=2$
- The _cross product_ $(\bm{u}\wedge\bm{v})_i=\epsilon_{ijk}u_jv_k$ is a _pseudo-vector_, since the Levi-Civita symbol is a _pseudo-tensor_
	- Can be thought of as _two outer products with two contractions_
