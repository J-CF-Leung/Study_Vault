

# Abstract
- A _time-varying basis set_ for electronic structure calculations
- Work: a _geometric perspective_ on the results of varying parameters 

- "Effect of the basis set evolution within the spanned Hilbert space separates explicily from the effect of the turning of the space itself when moving in parameter space, as the tangent space turns when moving in a curved space"
	- What???
	- I assume this statement will be unpacked later...

- Mathematical framework: fibre bundles
- _Gauge_ from the varying basis set: connects with [[Quantum Dynamics#Berry's phase|Berry curvature]]

- _Generalised expressions_ for Berry connection and curvature obtained for a _parameter-dependent Hilbert space_, spanned by _nonorthogonal Wannier functions_
	- Non-orthogonal...??

- _Applications of the formalism_:
	- Atomic-like orbitals
	- Adaptive moving basis funcions
	- Other nonorthogonal functions

# Introduction
- Typical basis set: atomic-like
	- Product of _radial_ function and spherical harmonics
	- _Centred_ around the atom
- Alternativly: obtained "dynamically, using a finer auxiliary basis"

- _Generally_: basis set is 
	- _Not orthonormal_
	- Spans a _subspace_ of the Hilbert space
	- _Change_ with _external parameters_

## Matrix representation with a non-orthogonal basis
- The _overlap matrix_ is not diagonal:
$$S_{\mu \nu}=\braket{ e_{\mu} |e_{\nu}  } $$
- The wave-function:
$$\ket{\psi}=\sum_{\nu}C_{\nu}\ket{e_{\nu}}  $$
- The _time-independent_ Schrodinger equation becomes
	- Derivaion: dot both sides with $\bra{e_{\mu}}$
$$\sum_{\nu}H_{\mu \nu}C_{\nu}=E\sum_{\nu}S_{\mu \nu}C_{\nu}$$
- The _time-dependent_ equation, using the _covariant derivative_ to track the _time dependence of the basis_:
$$\displaylines{\sum_{\nu}(H_{\mu \nu}-iD_{\mu \nu})C_{\nu}=\sum_{\nu}iS_{\mu \nu}\dot{C}_{\nu}\\
D_{\mu \nu}=\braket{ e_{\mu}|\partial_{t} | e_{\nu} } }$$

## Goal
- A _more general formalism_ based on _tensors_
	- Nonorthogonal basis sets: analagous to _Euclidean space with oblique axes_
- One can _formulate second quantisation_ with this formalism

- _Differenial geometry_ interpretation of dynamical equations
	- Concepts: _affine connection_, and _covariant derivatives_
	- Not just addressing dynamics of scalars

# Tensorial formulation
- A _geometric_ formulation of time-dependent quantum mechanics relying on _tensors_

- Referred to as the _natural representation_
## Basis and metric
- A set of linearly independent, _non-orthogonal_ basis kets
	- They span a _subapce_ $\Omega$ of the Hilbert space $\mathcal{H}$
$$\{\ket{e_{\mu}},\mu=1,\dots N \}$$
- There is also a _dual basis_:
$$\displaylines{\{\ket{e^{\mu}},\mu=1,\dots N \} \\ \braket{ e^{\mu} | e_{\nu} }={\delta^{\mu}}_{\nu}=\braket{ e_{\nu} | e^{\mu} } }$$
- One can construct a _projector_ into $\Omega$:
$$\sum_{\mu}\ket{e_{\mu}}\bra{e^{\mu}} =\sum_{\mu} \ket{e^{\mu}}\bra{e_{\mu}}=P_{\Omega}    $$
- The _metric tensor_ is given by the _overlap_:
$$S_{\mu \nu}=\braket{ e_{\mu} | e_{\nu} } \qquad S^{\mu \nu}=\braket{ e^{\mu} | e^{\nu} } $$

## States and operators
- Applicable to both _single particle_, and _multi-particle_ states
- The bra and ket basis states need to _represent the same number of particles_ as $\ket{\psi}$

### State bras and kets
- A _state ket_ $\ket{\psi} \in \Omega$ is represented by a _contravariant first-rank tensor_:
$$\psi^{\mu}=\braket{ e^{\mu} | \psi } \qquad,\qquad \ket{\psi}=\ket{e_{\mu}}\psi^{\mu}  $$
- The _state bra_ is then the _covariant first-rank tensor_:
$$\psi_{\mu}=\braket{ \psi | e_{\mu} } \qquad,\qquad \bra{\psi}=\psi_{\mu}\bra{e^{\mu}}  $$
- _Kets_: upper index
- _Bras_: lower index

- Complex conjugation:
$$\psi^{\mu*}=\braket{ \psi | e^{\mu} }\qquad\psi_{\mu}^{*}=\braket{ e_{\mu} |\psi  } $$
- From the above, the _raising and lowering_ of indices also brings _conjugation_:
$$\psi_{\nu}S^{\nu \mu}=\psi^{\mu*}\qquad S_{\mu \nu}\psi^{\nu}=\psi_{\mu}^{*}$$

### Operators
- Use _second rank tensors_ for operators:
$${H^{\mu}}_{\nu}=\braket{ e^{\mu} | H|e_{\nu} } $$
- Schrodinger's equation can then be written as:
$${H^{\mu}}_{\nu}\psi^{\nu}=E\psi^{\mu}$$

## Parameter vector space
- Formalise _derivatives with respect to parameters_ that the basis may depend on 
	- Must account for _change of basis within_ $\Omega$ and the _change of_ $\Omega$ _itself_
	- Example: _nuclear positions_

- Let there be a _parameter space_ $\Theta$ of dimension $N$, with basis:
$$\{\boldsymbol{u}_{i},i=1,\dots N\}$$
- Such that _any vector_ $\boldsymbol{R} \in \Theta$ becomes:
$$\boldsymbol{R}=R^{i}\boldsymbol{u}_{i}$$
- The _electronic basis set and space_ are dependent on $\boldsymbol{R}$:
$$\Omega=\Omega(\boldsymbol{R})\qquad \ket{e_{\mu}}=\ket{e_{\mu}(\boldsymbol{R})}  $$
- $\Theta$ is the _base space_, and $\Omega(\boldsymbol{R})$ is a _fibre_ for each $\boldsymbol{R}$
- As $\boldsymbol{R}$ changes within $\Theta$, the Hilbert space for each fire _turns within_ the ambient $\mathcal{H}$, analagous to the _turning of tangent spaces_
- $\Theta$ and $\Omega(\boldsymbol{R})$ is a _flat Euclidean space_, but the _overall fibre bundle_ is _curved_

- The _change_ in $\Omega(\boldsymbol{R})$ gives the [[Quantum Dynamics#Berry's phase|geometric phase]]
- In this case, $\Omega$ is associated with the _ground states_ for different $\boldsymbol{R}$

- The _change of basis_ between fibres is a _gauge transformation_ given by any matrix belonging to group $\mathrm{GL}(\mathcal{N},\mathbb{C})$

## Differential geometry of the Hilbert space

### Covariant derivative
- The _derivative_ of components of the state w.r.t. $R^{i}$:
$$\partial_{i}\psi^{\mu}=\frac{\partial \psi^{\mu}}{\partial R^{i}}$$
- It _does not transform as a tensor_

- Instead, define a _covariant derivative_:
$$\bar{\partial}_{i}\psi^{\mu}\equiv \braket{ e^{\mu}|P_{\Omega} \,\partial_{i}\{P_{\Omega}| \psi } \}=\braket{ e^{\mu} | \partial_{i}\{P_{\Omega} |\psi} \}$$
- The _projector_ $P_{\Omega}$ is _necessary_, as $\Omega$ _varies with time_
	-  $\ket{\psi}$ and $P_{\Omega}\ket{\psi}$ are _not equal for neighbouring points_ of $\Theta$
- The covariant derivative is _applied before projection onto_ $\Omega$

- For an _unchanging_ $\ket{\psi},\Omega$, or for unchanging $\{e^{\mu}\}$, the _covariant derivative is zero_ while the usual derivative is not
	- In other words, the covariant derivative is an _intrinsic rate of change_
	- Analagous to [[Classical Field Theory#Local phase (gauge) symmetry|gauge dependent theories]], where the covariant derivative is gauge independent

- By expanding $P_{\Omega}$, one also gets:
$$\displaylines{\begin{align}
\bar{\partial}_{i} \psi^{\mu}&=\braket{ e^{\mu}|\partial_{i} | e_{\nu} }\psi^{\nu}+\partial_{i}\psi^{\mu} \\ &=\partial_{i}\psi^{\mu}+ D^{\mu}_{\nu i}\psi^{\nu}
\end{align} \\ D^{\mu}_{\nu i}\equiv \braket{ e^{\mu} |\partial_{i}| e_{\nu} }=\braket{ e^{\mu}| \partial_{i}e_{\nu}  }  }$$

### Affine connection
- $D^{\mu}_{\nu i}$ is _analagous_ to [[General Relativity#Connection and curvature tensor|Christoffel symbols]] in the Levi-Civita connection
	- Arises from the _movement_ of $\Omega$, not necessarily from the curvature of a manifold
$$P_{\Omega}\partial_{i}\ket{e_{\nu}} =\ket{e_{\mu}}\braket{ e^{\mu} | \partial_{i}|e_{\nu} }=D^{\mu}_{\nu i}  $$
- From movement $d\boldsymbol{R}$ in parameter space, the basis transforms as:
$$\ket{e_{\nu}(\boldsymbol{R}+d\boldsymbol{R})}=\ket{e_{\nu}(\boldsymbol{R})}+\ket{e_{\mu}(\boldsymbol{R})}D^{\mu}_{\nu i}\,dR^{i}   $$

- When $\Omega(\boldsymbol{R})$ _turns_, $\ket{\psi(\boldsymbol{R})}$ must then _propagate_ in $\Omega(\boldsymbol{R})$ then be _projected_ into $\Omega(\boldsymbol{R}_+d\boldsymbol{R})$
$$\displaylines{\psi^{\mu}(\boldsymbol{R}+d\boldsymbol{R})=\psi^{\mu}(\boldsymbol{R})+\partial_{i}\psi^{\mu}(\boldsymbol{R})dR^{i} \\ \ket{\psi(\boldsymbol{R}+d\boldsymbol{R})}=P_{\Omega(\boldsymbol{R}+d\boldsymbol{R})}\big\{P_{\Omega(\boldsymbol{R})}\ket{\psi(\boldsymbol{R})}+P_{\Omega(\boldsymbol{R})}\partial_{i}[P_{\Omega(\boldsymbol{R})}\ket{\psi(\boldsymbol{R})} ]dR^{i} \big\} }$$

# Second quantisation
- Source: Phys. Rev. A **43**, 5770 (1991).

- Maintain same notation as previous sections

- To second quantise, _generate_ the _Fock space_ from a given _one-particle (nonorthogonal) basis set_, as well as the _dual basis_
- Still define _creation_ and _annihilation_ operators by their action on the basis, and find the _commutation relations_
	- The ones for the _dual basis_ are found by Hermitian conjugation
- Then, other operators are _constructed_ from the creation and annihilation operators

- If the _one particle basis_ is not orthogonal, _neither_ will the Fock space basis