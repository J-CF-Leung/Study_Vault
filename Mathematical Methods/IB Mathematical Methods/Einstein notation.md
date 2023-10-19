- [ ] Information about covariant/contravariant components🔼 
# The suffix notation
- The _free suffices_ (typically $i,j,k$) range over the number of basis vectors
- Equality of vectors implies equality of components:
$$\begin{aligned}\bm{a}&=\bm{b} \\ a_i&=b_i\end{aligned}$$
- Relations between vectors:
$$\begin{aligned}\bm{c}&=\lambda\bm{a}+\mu\bm{b} \\ c_i&=\lambda a_i+\mu b_i\end{aligned}$$

- When summing up vector components, the sum is taken over _dummy suffices_
- Einstein convention: the summation sign $\sum$ is omitted
	- Free suffices: appear once, range over number of basis vectors, appear on both sides
	- Dummy suffices: appear twice, summed over
	- WRONG suffix: appears more than twice
- Dot products:
$$\bm{a}\cdot\bm{b}=a_ib_i$$
- The transpose of a matrix $A$:
$$(A^T)_{ij}=A_{ji}$$
- Matrix $A$ multiplied by vector $\bm{x}$:
$$y=A\bm{x} \iff y_i=A_{ij}x_j$$
- Matrix $A$ multiplied by matrix $B$:
$$C=AB \iff C_{ij}=A_{ik}B_{kj}$$
- The trace of a matrix $A$:
$$\text{Tr}(A)=A_{ii}$$
- The determinant of a $3\times 3$ matrix $A$:
$$\text{det} \,A=\epsilon_{ijk}A_{1i}A_{2j}A_{3k}$$
## The Kronecker Delta
- The Kronecker Delta $\delta_{ij}$ is a matrix with indices $i,j=1,2,3$
- The matrix element equals 1 for $i=j$, and 0 otherwise
- Properties:
$$\delta_{ij}=\delta_{ji}$$
$$a_i\delta_{ij}=a_j$$
$$\delta_{ij}\delta_{jk}=\delta_{ik}$$
$$\delta_{ii}=3$$
	- Equal to the number of dimensions/degrees of freedom
$$a_pb_q\delta_{pq}=a_pb_p=\bm{a\cdot b}$$
$$\bm{e_i\cdot e_j}=\delta_{ij}$$
- Contraction: Setting one free suffix equal to another so they are summed over
	- Contracting $a_{ij}$ makes it $a_ii$
	- Equivalent to multiplying by $\delta_{ij}$

## The Levi-Civita tensor
- The tensor can have values $0$, $1$, and $-1$
- The tensor is completely _anti-symmetric_
- The value depends on the ordering of its indices
- For an odd permutation (odd number of swaps from the ordered permutation), $\epsilon=-1$
- For an even permutation, $\epsilon=1$
- For a permutation where two indices have the same value, $\epsilon=0$
- Cyclic permutations are even, therefore cycling indices does not change the value of $\epsilon$
$$\epsilon_{ijk}=\epsilon_{jki}=\epsilon_{kij}$$
- For a symmetric tensor $s$ where $s_{ij}=s_{ji}$:
$$\epsilon_{ijk}s_{ij}=\epsilon_{ijk}s_{ji}=-\epsilon_{jik}s_{ji}=-\epsilon_{ijk}s_{ij}=0$$

## The vector product
- The vector productcan be written as:
$$(a\wedge b)_i=\epsilon_{ijk}\,a_j\,b_k$$
- Equivalently:
$$a\wedge b=\epsilon_{ijk}\,\bm{e}_i\,a_j\,b_k=
\begin{vmatrix}
     \bm{e}_{1} & \bm{e}_{2} & \bm{e}_{3}\\ 
     a_{1} & a_{2} & a_{3}\\
     b_{1} & b_{2} & b_{3} 
\end{vmatrix}
$$
## Product of two Levi-Civita tensors
$$\epsilon_{ijk}\epsilon_{lmn} = 
\begin{vmatrix}
     \delta_{il} & \delta_{im} & \delta_{in}\\ 
     \delta_{jl} & \delta_{jm} & \delta_{jn}\\
     \delta_{kl} & \delta_{km} & \delta_{kn} 
\end{vmatrix}$$
- Proof: Check results of changing indices on both sides
- Contraction:
$$\epsilon_{ijk}\epsilon_{lmk}=\delta_{il}\delta_{jm}-\delta_{im}\delta_{jl}$$
- Contracting the contraction:
$$\epsilon_{ijk}\epsilon_{ljk}=2\delta_{il}$$
- Contracting the contraction of the contraction:
$$\epsilon_{ijk}\epsilon_{ijk}=6$$

## Triple products
- The scalar triple product:
$$\bm{a\cdot(b\wedge c)}=a_i(b\wedge c)_i=\epsilon_{ijk}\,a_i\,b_j\,c_k$$
- The vector triple product: use the product of two Levi-Civita tensors
$$a\wedge(b\wedge c) = (\bm{a\cdot c})\bm{b}-(\bm{a\cdot b})\bm{c}$$


# Covariant and contravariant components
