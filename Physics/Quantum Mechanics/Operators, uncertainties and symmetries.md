- _Hermitian operators_ describe _observable quantities_ in quantum mechanics
	- Examples include position, momentum, and spin
- As they act on wave functions represented by ket vectors, they _can be represented by matrices_, with different matrix elements for different bases
	- The matrix can either be in finite or infinite dimensions
- The expectation value of an observable quantity for a given wave function $\wv$ is represented by:
$$\left<Q\right>=\braket{\Psi|\hat{Q}\Psi}$$
- As the outcome of a measurement must be real, the operator $\hat{Q}$ _must be Hermitian_

- For all observables, the corresponding operator has a _set of determinate states_, or _eigenstates_, represented by eigenkets $\ket{\Psi_q}$:
$$\hat{Q}\ket{\Psi_q}=q\ket{\Psi_q}$$
	- Measuring $Q$ for this state _always gives_ $q$, with a standard deviation of 0
	- $q$ is an eigenvalue of $\hat{Q}$
	- Example: time-independent Schrödinger equation $\hat{\Ham}\wv=E\wv$
- Due to the operator's _Hermiticity_, in the _eigenbasis_ formed by these kets, the matrix is always _diagonal_, with elements
$$\braket{q|\hat{Q}|q'} = q\,\delta_{qq'}=q\,\delta(q-q')$$

- As all operators for observables are Hermitian, the eigenkets are _orthogonal and span the entire complex vector space_:
$$\sum_n\ket{q_n}\bra{q_n}=\int\ket{q}\bra{q}\;dq=1$$
- If the eigenvalue spectrum of an operator are discrete, the eigenkets are normalised by:
$$\braket{m|n}=\delta_{mn}$$
- If the eigenvalue spectrum is continuous, they can only be normalised via the _Dirac Delta Function_:
$$\braket{x|y}=\delta(x-y)$$

# 1D operators

## Position and momentum
- For all operators, the matrix elements in their eigenbasis is trivial:
$$\braket{x|\hat{X}|x'}=x\,\delta(x-x') \;\;\;\; \braket{p|\hat{P}|p'}=p\,\delta(p-p')$$
- The "origin" of the momentum operator is the _Hermitian version of the differential operator_ in the position basis:
$$\braket{x|\hat{P}|x'} = -i\hbar\frac{d}{dx}\delta(x-x')$$
	- The differential operator $D_{xx'}=\delta'(x-x')$ is an odd function
	- Momentum is also the [[Analytical classical mechanics#Symmetries and Noether's Theorem|generator]] of translations
- The _eigenfunction_ of $\hat{P}$ in the position basis $\braket{x|p}$ can be solved by dotting $\hat{P}\ket{p}$ by $\bra{x}$ then using the completeness relation:
$$\braket{x|\hat{P}|p}=\int \braket{x|\hat{P}|x'}\braket{x'|p}\;dx'=p\braket{x|p}$$
$$\braket{x|p}=\frac{1}{\sqrt{2\pi\hbar}}\;\exp(ipx/\hbar)$$
	- The factor of $1/\sqrt{2\pi\hbar}$ ensures that $\braket{p|p'}=\delta(p-p')$, as it should in an orthonormal basis
	- This is the [[Fourier series and transforms#Fourier transforms|Fourier transform]] of a Delta function (wave function with definite momentum)
- Using this, the matrix elements of $\hat{X}$ in the momentum basis can also be found:
$$\braket{p|\hat{X}|p'}=i\hbar\frac{d}{dp}\delta(p-p')$$
- Summary:
|                                   | $\hat{X}$             | $\hat{P}$              |
| --------------------------------- | --------------------- | ---------------------- |
| $\braket{x \vert\hat{Q}\vert x'}$ | $x\delta(x-x')$       | $-i\hbar\delta'(x-x')$ |
| $\braket{p\vert\hat{Q}\vert p'}$  | $i\hbar\delta'(p-p')$ | $p\delta(p-p')$        |

- Due to this symmetry, the position and momentum operators are known as _conjugates_
- The two operators $\hat{X}$ and $\hat{P}$ do not commute:
$$[\hat{X},\hat{P}]=i\hbar$$
## Energies and the Hamiltonian


# Useful commutation relations
- Using the [[Vectors and matrices in physics#Commutation relations involving functions|commutation relations involving functions]]:
$$\displaylines{[\hat{x},\hat{p}^l]=i\hbar l\hat{p}^{l-1}=i\hbar\pd{\hat{p}^l}{\hat{p}} \\ [\hat{x},F(\hat{x},\hat{p})]=i\hbar\pd{F}{\hat{p}} \\ [\hat{p},F(\hat{x},\hat{p})]=-i\hbar\pd{F}{\hat{x}}}$$
- Example:
$$[\hat{x},\hat{p}\hat{x}\hat{p}]=i\hbar(\hat{x}\hat{p}+\hat{p}\hat{x})$$
# Uncertainty
- Consider the _commutator for a pair of observables_
- If they _commute_, then there is a _set of simultaneous eigenstates_
- If they _do not_, then no simultaneous eigenstate exists, and there _cannot be definite values for both observables_
	- They are said to be _incompatible_

- Example: Position and momentum, hence a particle _never has a definite path_

## The uncertainty relation
- Consider the _variances_ for two incompatible observables, $A$ and $B$
$$\sigma_A^2=\mean{\hat{A}^2}-\mean{\hat{A}}^2$$
- Due to this uncertainty, their _product_ will have a _non-zero minimum value_
- This is given by the _generalised uncertainty principle_:
	$$\sigma_A^2\sigma_B^2\geq\left(\frac{1}{2i}\left<[\hat{A},\hat{B}]\right>\right)^2$$
	-Proof: Cauchy-Schwarz inequality with $\ket{(\hat{A}-a)\Psi}$ and $\ket{(\hat{B}-b)\Psi}$
	$|\braket{f|g}|^2 = Re(\braket{f|g})^2+Im(\braket{f|g})^2$ 

- If applied to position and momentum:
$$\sigma_x\sigma_p\geq\frac{\hbar}{2}$$

## The minimum uncertainty wave packet
- From the proof of the inequality, for a packet with _minimal uncertainty in position and momentum_, it must satisfy:
$$\left(\hat{P}-\mean{\hat{P}}\right)\ket{\Psi}=i|c|\left(\hat{X}-\mean{\hat{X}}\right)\wv$$
- Defining:
$$\displaylines{\Delta=\hbar/|c| \\ \mean{\hat{X}}=a \hspace{1cm}\mean{\hat{P}}=p_0}$$
- Thus, the _minimum-uncertainty wave packet_ in position space is:
$$\psi(x)=A\exp\left[\frac{ip_0}{\hbar}(x-a)\right]\exp\left[-\frac{(x-a)^2}{2\Delta^2}\right]$$
- This is a _Gaussian packet_

# Parity operator

# Operators in three dimensions

## Position and momentum
- In the position basis in three dimensions, the momentum operator becomes:
$$\hat{\bm{P}}\xrightarrow{x\text{ basis}}-i\hbar\pd{}{x_i}\bm{e}_i$$
- This can also be written as:
$$\hat{\bm{P}}\xrightarrow{x\text{ basis}}-i\hbar\nabla$$

- The _canonical commutation relations_ become:
$$\displaylines{ [\hat{x}_i,\hat{x}_j]=[\hat{p}_i,\hat{p}_j]=0 \\ [\hat{x}_i,\hat{p}_j]=-[\hat{p}_i,\hat{x}_j]=i\hbar\delta_{ij}}$$
- The _eigenfunction_ of the 3-dimensional momentum operator in the _position basis_ is:
$$\braket{\bm{x}|\bm{p}}=\braket{xyz|p_xp_yp_z}=\frac{1}{(2\pi\hbar)^{3/2}}\exp\left(\frac{i}{\hbar}\bm{p}\cdot\bm{x}\right)$$
- This can be _separated into three one-dimensional eigenfunctions_

### In spherical coordinates


## The orbital angular momentum operators
- Appearances and eigenfunctions: [[Angular momentum in quantum mechanics]]

- The angular momentum operators have formulas _similar to their classical counterparts_:
$$\hat{L}_k=\epsilon_{ijk}\hat{x}_i\hat{p}_j=-i\hbar\epsilon_{ijk}x_i\pd{}{x_j}$$
- The commutation relations are:
$$[\hat{L}_i,\hat{L}_j]=i\hbar\epsilon_{ijk}\hat{L}_k$$
	- It can also be expressed as $\bm{\hat{L}\wedge\hat{L}}=i\hbar\bm{\hat{L}}$
- As for the operator $\bm{\hat{L}}^2=\hat{L}_x^2+\hat{L}_y^2+\hat{L}_z^2$:
$$[\bm{\hat{L}}^2,\hat{L}_i]=0$$
	- Or: $[\bm{\hat{L}}^2,\bm{\hat{L}}]=0$
- The uncertainty relation between two components of angular momentum is:
$$\Delta L_i\Delta L_j\geq \frac{\hbar}{2}|\epsilon_{ijk}\braket{L_k}|$$
- The operator along the $z-$direction can also be put into another form in spherical coordinates:
$$\hat{L}_z=-i\hbar\pd{}{\phi}$$
	- $L_z$ is the [[Analytical classical mechanics#Symmetries and Noether's Theorem|generator]] of rotation along the $z-$axis

- The $\hat{L}^2$ operator can also be written in terms of spherical coordinates:
$$\hat{L}^2=-\hbar^2\left[\frac{1}{\sin\theta}\pd{}{\theta} \left(\sin\theta\pd{}{\theta}\right) +\frac{1}{\sin^2\theta}\pd{^2}{\phi^2}\right]$$


## Spin
- The spin operators follow the same commutation relations:
