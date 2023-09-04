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
- The _row_ $i$ of the matrix contain the _components_ of $\bm{e}_i'$ in $\bm{e}_j$

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

### Symmetric and antisymmetric tensors
- A tensor is _symmetric_ w.r.t. indices $\alpha$ and $\beta$ if:
$$T_{\dots\alpha\dots\beta\dots}=T_{\dots\beta\dots\alpha\dots}$$
- The tensor is _antisymmetric_ w.r.t. indices $\alpha$ and $\beta$ if:
$$T_{\dots\alpha\dots\beta\dots}=-T_{\dots\beta\dots\alpha\dots}$$
- Symmetry or antisymmetry is _invariant under changes in coordinate system_
	- Proof: Write out the transformation law

- If $S_{ijk\dots}$ is _symmetric_ w.r.t. $i,j$ and $A_{pqr\dots}$ is _antisymmetric_ w.r.t. $p,q$, then the _contraction_:
$$S_{ijk\dots}A_{ijr\dots}=0$$
	- Proof: Swap indices in this contraction

- The _Kronecker delta_ is _symmetric w.r.t. all indices_
- The _Levi-Civita tensor_ is _antisymmetric w.r.t. all indices_
- Many tensors representing _physical quantities_, such as _conductivity_ and _inertia_, are symmetric

## Second-order tensors
- Second-order tensors only have _one pair of indices_
- Therefore, they can simply be referred to as _symmetric_ or _antisymmetric_:
$$\displaylines{\text{S}^T=\text{S} \\ \text{A}^T=-\text{A}}$$
- Any _antisymmetric_ tensor must have _zeroes for diagonal entries_

### Decomposition
- _Any_ second-order tensor can be _uniquely decomposed into the sum of a symmetric and antisymmetric tensor_:
$$\displaylines{T_{ij}=S_{ij}+A_{ij} \\ S_{ij}=\frac{T_{ij}+T_{ji}}{2} \hspace{1cm} A_{ij}=\frac{T_{ij}-T_{ji}}{2}}$$

- _Antisymmetric_ tensors _only have three independent components_, and are _equivalent to axial vectors_:
$$A_{ij}=-\epsilon_{ijk}\omega_k=\begin{pmatrix}0 & \omega_3 & -\omega_2 \\ -\omega_3 & 0 & \omega_1 \\ \omega_2 & -\omega_1 & 0\end{pmatrix}$$
- Here, $\bm{\omega}$ is known as the _dual vector_
- Since $\epsilon$ is a _pseudo-tensor_, then $\bm{\omega}$ must be an _axial vector_, with components:
$$\omega_k=-\frac{1}{2}\epsilon_{klm}A_{lm}$$

- As for _symmetric_ tensors, they can be _uniquely decomposed_ in terms of a _tracless tensor_ $\tilde{\text{S}}$ and a _scalar multiple_ of the identity $\text{I}$:
$$\text{S}=\tilde{\text{S}}+\frac{1}{3}\text{tr}(\text{S})\text{I}$$

### Diagonalisation
- Suppose there is a _symmetric_ second-rank tensor $\text{S}_{ij}$
- The matrix of _components_ w.r.t. $\bm{e}_i$ must then be _Hermitian_
- Therefore, it must be _diagonalisable_, with _real eigenvalues and orthonormal eigenvectors_
	- Proof: [[Vectors and matrices#Diagonalisation via unitary matrices]]

- Consider a transformation from basis $\bm{e}_i$ to $\bm{e}_i'$, with the transformation matrix:
$$L_{ij}=\bm{e}_i'\cdot\bm{e}_j$$
$$\displaylines{\text{SL}^T=\left(\begin{array}{c|c|c}\lambda_1\bm{e}_1' & \lambda_2\bm{e}_2' & \lambda_3\bm{e}_3'\end{array}\right) \\ \text{S}'=\text{LSL}^T= \left(\begin{array}{c}\bm{e}_1' \\ \hline \bm{e}_2' \\ \hline\bm{e}_3'\end{array}\right)\left(\begin{array}{c|c|c}\lambda_1\bm{e}_1' & \lambda_2\bm{e}_2' & \lambda_3\bm{e}_3'\end{array}\right)=\begin{pmatrix}\lambda_1 &0&0\\0&\lambda_2&0\\0&0&\lambda_3\end{pmatrix}}$$
- The diagonal entries are known as the _principal values_ of the tensor
- The eigenvectors are known as the _principal axes_
- Example: Principal moments of inertia

## Isotropic tensors
- An _invariant_ tensor or pseudo-tensor is one which _has the same components in all frames_:
$$T_{ijk\dots}=T'_{ijk\dots}$$
- Both _invariant tensors_ or _pseudo-tensors_ are classified as _isotropic tensors_

- All _scalars_ are _isotropic_
- There are _no_ non-zero _isotropic vectors_ or _axial vectors_

- Any _scalar multiple_ of $\delta_{ij}$ is the _most general second-order isotropic tensor_

- Any _scalar multiple_ of $\epsilon_{ijk}$ is the _most general third-order isotropic tensor_
	- Technically a _pseudo-tensor_

- The _most general fourth-order isotropic tensor_ is:
	$$\lambda\delta_{ij}\delta_{kl}+\mu\delta_{ik}\delta_{jl}+\nu\delta_{il}\delta_{jk}$$- where $\lambda,\mu,\nu$ are _scalars_

- Isotropic tensors _do not have a preferred direction_
- An isotropic tensor is _not necessarily uniform_

### Applying to integrals

#### Vector integral over sphere
- Let there be a _vector_, which calculates a _centre of mass_ for a _spherically symmetric density_:
$$\bm{X}=\int_{r\leq a}\bm{x}\rho(r)\,dV \hspace{1cm} X_i=\int_{r\leq a} x_i\rho(r)\,dV$$
- Let there be some _rotation matrix_ $\text{R}$ such that $x_i'=R_{ij}x_j$
- Using the _orthogonality_ of the rotation tensor, one can prove that $X_i=X_i'$
- Since there are _no non-zero isotropic vectors_, $\bm{X}=0$

#### Second-order tensor integral over sphere
- Let there be a _second-order tensor_, such that:
$$K_{ij}=\int_{r\leq a}x_ix_j\rho(r)\,dV$$
- From a similar argument, the tensor _must be isotropic_:
$$K_{ij}=\lambda \delta_{ij}$$
- Here, $\lambda$ must be $1/3$ of the _trace_
- Hence:
$$K_{ij}=\left(\int_{r\leq a}\frac{1}{3}r^2\rho(r)\,dV\right)\delta_{ij}$$

## Tensor fields
- A _tensor field_ is a tensor that _depends on position_ $\bm{x}$

- A _scalar field_ is a _zeroth order tensor field_
	- Example: _Temperature_
- A _vector field_ is a _first order tensor field_
	- Example: _Electric field_

- A _second order tensor field_ includes _conductivity tensor_
- A _third order tensor field_ includes _piezo-electric strain tensor_
- A _fourth order tensor field_ includes _stiffness_

### Differential operators
- The _differential operator_ $\nabla$ is a _first-order tensor operator_, with _components_ $\partial_i=\partial/\partial x_i$

- The _gradient of a scalar field_, $\nabla \Phi$ is a _first-order tensor field_
- The _gradient of a vector field_, $\nabla\bm{E}$ is a _second-order tensor field_, with components:
$$(\nabla \bm{E})_{ij}=\nabla_iE_j$$
- Following this logic, the _gradient of a second-order tensor field_ would be a _third-order tensor field_

- The _divergence of a vector field_ $\nabla\cdot\bm{E}$ is a _zeroth-order scalar field_:
	$$\nabla\cdot\bm{E}=\partial
	_iE_i$$
	- The _contraction_ of an _outer product_ of two vectors

- The _curl of a vector field_ $\nabla\wedge\bm{E}$ is a _axial-vector field_:
	$$(\nabla\wedge\bm{E})_i=\epsilon_{ijk}\partial_jE_k$$
	- The _double contraction_ of a _fifth order tensor_

- The _Laplacian of a scalar field_ would be a _scalar field_
	- _Double contraction_ of a _fourth-order tensor_

