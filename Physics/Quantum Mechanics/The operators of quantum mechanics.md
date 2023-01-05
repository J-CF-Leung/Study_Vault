## Operators and observables
- Operators describe _observable quantities_ in quantum mechanics
	- Examples include position, momentum, and spin
- As they act on wave functions represented by ket vectors, they are represented by matrices, with different matrix elements for different bases
	- The matrix can either be in finite or infinite dimensions
- The expectation value of an observable quantity for a given wave function $\wv$ is represented by:
$$\left<Q\right>=\braket{\Psi|\hat{Q}\Psi}$$
- As the outcome of a measurement must be real, the operator $\hat{Q}$ must be Hermitian

### Eigenkets of operators
- For all observables, the corresponding operator has a set of determinate states, or _eigenstates_, represented by eigenkets $\ket{\Psi_q}$:
$$\hat{Q}\ket{\Psi_q}=q\ket{\Psi_q}$$
	- Measuring $Q$ for this state always gives $q$, with a standard deviation of 0
	- $q$ is an eigenvalue of $\hat{Q}$
	- Example: time-independent Schrödinger equation $\hat{\Ham}\wv=E\wv$
- Due to the operator's Hermiticity, in the eigenbasis formed by these kets, the matrix is always diagonal, with elements
$$\braket{q|\hat{Q}|q'} = q\,\delta_{qq'}=q\,\delta(q-q')$$

- As all operators for observables are Hermitian, the eigenkets are orthogonal and span the entire complex vector space:
$$\sum_n\ket{q_n}\bra{q_n}=\int\ket{q}\bra{q}\;dq=1$$
- If the eigenvalue spectrum of an operator are discrete, the eigenkets are normalised by:
$$\braket{m|n}=\delta_{mn}$$
- If the eigenvalue spectrum is continuous, they can only be normalised via the Dirac Delta Function:
$$\braket{x|y}=\delta(x-y)$$

## The position and momentum operators
- For all operators, the matrix elements in their eigenbasis is trivial:
$$\braket{x|\hat{X}|x'}=x\,\delta(x-x') \;\;\;\; \braket{p|\hat{P}|p'}=p\,\delta(p-p')$$
- The "origin" of the momentum operator is the Hermitian version of the differential operator in the position basis:
$$\braket{x|\hat{P}|x'} = -i\hbar\frac{d}{dx}\delta(x-x')$$
	- The differential operator $D_{xx'}=\delta'(x-x')$ is an odd function
	- Momentum is also the [[Symmtries, transformations and generators in mechanics|generator]] of translations
- The eigenfunction of $\hat{P}$ in the position basis $\braket{x|p}$ can be solved by dotting $\hat{P}\ket{p}$ by $\bra{x}$ then using the completeness relation:
$$\braket{x|\hat{P}|p}=\int \braket{x|\hat{P}|x'}\braket{x'|p}\;dx'=p\braket{x|p}$$
$$p(x)=\braket{x|p}=\frac{1}{\sqrt{2\pi\hbar}}\;\exp(ipx/\hbar)$$
	- The factor of $1/\sqrt{2\pi\hbar}$ ensures that $\braket{p|p'}=\delta(p-p')$, as it should in an orthonormal basis
	- This is the [[Fourier series and transforms#Fourier transforms|Fourier transform]] of a Delta function (wave function with definite momentum)
- Using this, the matrix elements of $\hat{X}$ in the momentum basis can also be found:
$$\braket{p|\hat{X}|p'}=i\hbar\frac{d}{dp}\delta(p-p')$$
- Summary:
|                                   | $\hat{X}$             | $\hat{P}$              |
| --------------------------------- | --------------------- | ---------------------- |
| $\braket{x \vert\hat{Q}\vert x'}$ | $x\delta(x-x')$       | $-i\hbar\delta'(x-x')$ |
| $\braket{p\vert\hat{Q}\vert p'}$  | $i\hbar\delta'(p-p')$ | $p\delta(p-p')$        |

- Due to this symmetry, the position and momentum operators are known as conjugates
- The two operators $\hat{X}$ and $\hat{P}$ do not commute:
$$[\hat{X},\hat{P}]=i\hbar$$

- Using this, the [[Fundamentals of quantum mechanics#Uncertainty|uncertainty relation]] for these two variables is:
$$\Delta X\Delta P\geq \frac{\hbar}{2}$$
## Converting between bases


## Operators in three dimensions
- In the position basis in three dimensions, the momentum operator becomes:
$$\braket{x_i|\bm{\hat{P}}|x_i'}=-i\hbar\pd{}{x_i}$$
- The canonical commutation relations become:
$$\displaylines{ [\hat{x}_i,\hat{x}_j]=[\hat{p}_i,\hat{p}_j]=0 \\ [\hat{x}_i,\hat{p}_j]=-[\hat{p}_i,\hat{x}_j]=i\hbar\delta_{ij}}$$
### The orbital angular momentum operators
- Appearances and eigenfunctions: [[Angular momentum in quantum mechanics]]

- The angular momentum operators have formulas similar to their classical counterparts:
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
	- $L_z$ is the [[Symmtries, transformations and generators in mechanics|generator]] of rotation along the $z-$axis

- The $\hat{L}^2$ operator can also be written in terms of spherical coordinates:
$$\hat{L}^2=-\hbar^2\left[\frac{1}{\sin\theta}\pd{}{\theta} \left(\sin\theta\pd{}{\theta}\right) +\frac{1}{\sin^2\theta}\pd{^2}{\phi^2}\right]$$
### Spin
- The spin operators follow the same commutation relations:
