- Using [[QFT|Quantum Field Theory]] and [[AQFT|Renormalisation Techniques]]

- The _Pauli matrices_ in the Pauli-Dirac representation:
$$\gamma^{0}=\pmatrix{1&0\\0&-1}\qquad \gamma^{i}=\pmatrix{0&\sigma^{i}\\-\sigma^{i}&0} \qquad \gamma^{5}=\pmatrix{0&1\\1&0}$$
# Spin 0: Scalar fields
- The _Lagrangian_ for a _real scalar field_
$$\mathcal{L}=\frac{1}{2}(\partial_{\mu}\phi)(\partial^{\mu}\phi)-\frac{1}{2}m^{2}\phi^{2}$$
- The resulting _equation of motion_, the [[QFT#Classical Field Theory recap|Klein-Gordon equation]]
$$(\partial_{\mu}\partial^{\mu}+m^{2})\phi=0$$
## Canonical quantisation of the Klein-Gordon field
- The corresponding _canonical momentum_
$$\pi=\frac{\partial \mathcal{L}}{\partial \dot{\phi}}$$

- The field can be _quantised_ with _equal time commutation relations_
$$\displaylines{
[\phi(\boldsymbol{x},t),\phi(\boldsymbol{x}',t)]=[\pi(\boldsymbol{x},t), \pi(\boldsymbol{x}',t)]=0 \\ [\phi(\boldsymbol{x},t),\pi (\boldsymbol{x}',t)]=i\delta^{3}(\boldsymbol{x}-\boldsymbol{x}')
}$$
- Then doing a _Fourier transform_
	- With a _different_ [[QFT#Relativistic normalisation|normalisation factor]]
$$\phi(\boldsymbol{x},t)=\int \frac{d^{3}p}{(2\pi)^{3}} \frac{1}{2E}(a_{\boldsymbol{p}}e^{-i(Et-\boldsymbol{p}\cdot \boldsymbol{x})}+a_{\boldsymbol{p}}^{\dagger}e^{i(Et-\boldsymbol{p}\cdot \boldsymbol{x})})$$
- The momentum state commutation relations:
$$\displaylines{[a_{\boldsymbol{p}},a_{\boldsymbol{p}'}]=[a_{\boldsymbol{p}}^{\dagger},a^{\dagger}_{\boldsymbol{p}'}]=0 \\ [a_{\boldsymbol{p}},a_{\boldsymbol{p}'}^{\dagger}]=(2\pi)^{3}(2E)\delta^{3}(\boldsymbol{p}-\boldsymbol{p}')}$$
- This gives the Hamiltonian, after _normal ordering_:
$$H=\int \frac{d^{3}p}{(2\pi)^{3}(2E)} E\,a_{\boldsymbol{p}}^{\dagger}a_{\boldsymbol{p}}$$
## Complex scalar field
- For a _complex scalar field_:
$$\mathcal{L}=(\partial_{\mu}\psi)(\partial^{\mu}\psi^{*})-m^{2}|\psi|^{2}$$
- Each component follows its own Klein-Gordon equation:
$$\partial_{\mu}\partial^{\mu}\psi+m^{2}\psi =0 \qquad \partial_{\mu}\partial^{\mu}\psi^{*}+m^{2}\psi^{*}=0$$
- Corresponding [[QFT#Internal symmetry complex scalar field|conserved current]], from an _internal_ $U(1)$ _symmetry_:
$$\displaylines{J^{\mu}=i(\psi \partial^{\mu}\psi ^{*}-\psi^{*}\partial^{\mu}\psi) \\ \partial_{\mu}J^{\mu}=0}$$

- Mode expansion now includes both _particles_ and _anti-particles_:
$$\displaylines{\psi(\boldsymbol{x},t)=\int \frac{d^{3}p}{(2\pi)^{3}(2E)}(a_{\boldsymbol{p}}e^{-ip\cdot x}+b_{\boldsymbol{p}}^{\dagger}e^{ip\cdot x}) \\ [a_{\boldsymbol{p}},a_{\boldsymbol{p}'}^{\dagger}]=[b_{\boldsymbol{p}},b_{\boldsymbol{p}'}^{\dagger}]=(2\pi)^{3}(2E)\delta^{3}(\boldsymbol{p}-\boldsymbol{p}')}$$
- They both carry positive energy:
$$H=\int \frac{d^{3}p}{(2\pi)^{3}(2E)} E(a^{\dagger}_{\boldsymbol{p}}a_{\boldsymbol{p}}+b^{\dagger}_{\boldsymbol{p}}b_{\boldsymbol{p}})$$
- However, they carry _opposite charge_
$$Q=\int \frac{d^{3}p}{(2\pi)^{3}(2E)} (a^{\dagger}_{\boldsymbol{p}}a_{\boldsymbol{p}}-b^{\dagger}_{\boldsymbol{p}}b_{\boldsymbol{p}})$$
# Spin 1/2: Dirac fermions
- A _linear_ version of the Klein-Gordon equation
$$i\gamma^{\mu}\partial_{\mu}\psi-m\psi=0$$
- Here, $\gamma^{\mu}$ must satisfy the _Clifford algebra_
	- Must be $4\times 4$ matrices
$$\{\gamma^{\mu},\gamma^{\nu}\}=2\eta^{\mu \nu}\mathbb{I}_{4}$$
- $\psi$ is a _spinor_

- The _Dirac adjoint_
$$\bar{\psi}=\psi ^{\dagger}\gamma^{0}$$
- The _conserved current_, corresponding to $U(1)$ symmetry
$$j^{\mu}=\bar{\psi}\gamma^{\mu}\psi$$

- Spin: a _rest frame angular momentum_
## Plane wave solutions in Pauli-Dirac basis
- Consider some _ansatz_, a combination of _positive and negative energy solutions_
$$\psi=u\exp(-ip\cdot x)+v\exp(ip\cdot x)$$

- Plugging into the Dirac equation gives that for any $\phi,\chi$, in the _Pauli-Dirac basis_
$$u^{s}=N\pmatrix{\phi \\ \frac{\boldsymbol{\sigma}\cdot \boldsymbol{p}}{E+m}\phi} \qquad v^{s}=N\pmatrix{\frac{\boldsymbol{\sigma}\cdot \boldsymbol{p}}{E+m}\chi \\ \chi}$$
- The _basis states_, with $1,2$ referring to different _spins_
$$\phi_{1}=\pmatrix{1\\0}\qquad \phi_{2}=\pmatrix{0\\1} \qquad \chi_{1}=\pmatrix{1\\0}\qquad \chi_{2}=\pmatrix{0\\1}$$
## Spinor field quantisation
- Mode expansion:
$$\psi(\boldsymbol{x},t)=\int \frac{d^{3}p}{(2\pi)^{3}} \sum_{s} \frac{1}{2E}(c_{\boldsymbol{p}}^{s}u_{\boldsymbol{p}}^{s}e^{-ip\cdot x}+d_{\boldsymbol{p}}^{s{\dagger}}v_{\boldsymbol{p}}^{s}e^{ip\cdot x})$$
- Anticommutation relations:
$$\{c_{\boldsymbol{p}}^{s},c^{s'{\dagger}}_{\boldsymbol{p}'}\}=\{d_{\boldsymbol{p}}^{s},d_{\boldsymbol{p}'}^{s'{\dagger}}\}=(2\pi)^{3}\delta^{ss'}(2E)\delta^{3}(\boldsymbol{p}-\boldsymbol{p}')$$

## Weyl spinors and chirality
- The 4-component _Dirac spinor_ $\psi$ is the direct sum of two _2-component [[QFT#Weyl spinors and chirality|Weyl spinors]]_
- The Weyl spinors are each of _opposite chirality_

- Define $\gamma^{5}$:
$$\gamma^{5}=i\gamma^{0}\gamma^{1}\gamma^{2}\gamma^{3}$$
- Define the _left and right handed projectors_
	- In the _chiral basis_, they correspond to $\mathbb{I}$ in each $2\times{2}$ diagonal block
	- $\overline{\psi_{L}}=(\bar{\psi})_{R}$
$$P_{L,R}=\frac{1}{2}(1\pm\gamma^{5}) \qquad \psi_{L,R}=P_{L,R}\psi$$
- The Lagrangian can be written as:
$$\mathcal{L}=(\overline{\psi_{L}}\cancel{ \partial }\psi_{L}+\overline{\psi_{R}}\cancel{ \partial }\psi_{R})-m(\overline{\psi_{L}}\psi _{R}+\overline{\psi_{R}}\psi_{L})$$
- The mass term _couples_ the left and right handed Weyl spinors
	- If they are _massless_, then $\mathcal{L}$ describes separate _Weyl fermions_
## CPT

### Charge conjugation


### Parity
- Parity is the transformation:
$$x^{0}\to x^{0} \qquad x^{i}\to -x^{i}$$

### Time reversal



# U(1) gauge field: Electromagnetism
- The 4-vector potential:
$$A^{\mu}=(V, \boldsymbol{A})$$
- The _field strength tensor_
$$F_{\mu \nu}\equiv\partial_{\mu}A_{\nu}-\partial_{\nu}A_{\mu}$$
- Free electromagnetic Lagrangian:
$$\mathcal{L}=-\frac{1}{4}F_{\mu \nu}F^{\mu \nu}$$

- The _Bianchi identity_ and the _Euler-Lagrange equations_ will give Maxwell's equations
	- They restrict $A^{\mu}$ to have 3 degrees of freedom instead of 4 (The lack of $\dot{A}_{0}$ in $F_{\mu \nu}$ means there are 3 dynamical components)

- Invariant under the _gauge transformation_
$$A_{\mu}\to A_{\mu}+\partial_{\mu}\chi$$
- One then has to _fix_ the gauge
	- Further reduces $A^{\mu}$ to 2 degrees of freedom (polarisation states)
	- Mathematical redundancy rather than physical symmetry
- Lorenz gauge:
$$\partial_{\mu}A^{\mu}=0$$

- For a _plane wave solution_, attach some _polarisation vector_ $\epsilon^{\mu}$
$$A^{\mu}\sim \epsilon^{\mu}\exp(-ip\cdot x)$$
- The field is _massless_:
$$p^{2}=0$$
- The Lorenz gauge then gives:
	- Changing gauge means shifting $\epsilon^{\mu}$ by an amount _proportional_ to $p^{\mu}$, to give an _equivalent polarisation_ (manifestation of gauge symmetry)
$$\epsilon \cdot p=0$$
## Quantisation in the Coulomb gauge
- Coulomb gauge:
$$A_{0}=0 \qquad \nabla\cdot \boldsymbol{A}=0$$
- The plane wave solution is then:
$$\boldsymbol{A}=\boldsymbol{\epsilon}\exp(-ip\cdot x)\qquad p^{2}=0\qquad \boldsymbol{\epsilon}\cdot \boldsymbol{p}=0$$
- For a plane wave, $\boldsymbol{\epsilon}$ has two _independent polarisations_

- Fourier expansion:
$$A_{i}=\int \frac{d^{3}\boldsymbol{p}}{(2\pi)^{3}(2E)}\sum_{P}(a_{\boldsymbol{p}}^{P}\epsilon_{i}^{P}e^{-ip\cdot x}+a_{\boldsymbol{p}}^{\dagger P}\epsilon_{i}^{*P}e^{ip\cdot x})$$
- The _completeness relation_ between polarisation vectors:
$$\sum_{P}\epsilon_{i}^{P}\epsilon_{j}^{*P}=\delta_{ij}-\frac{p_{i}p_{j}}{|\boldsymbol{p}|^{2}}$$

- Canonical commutation relations:
$$[a_{\boldsymbol{p}}^{P},a^{\dagger P'}_{\boldsymbol{p}'}]=(2\pi)^{3}(2E)\delta^{PP'}\delta^{3}(\boldsymbol{p}-\boldsymbol{p}')$$

# Interactions and cross-sections
- Go to the _interaction picture_

- Wick's Theorem
# Quantum Electrodynamics
- Through minimal coupling:
	- There is _no mass term_ for $A_{\mu}$ due to gauge invariance
$$\displaylines{\mathcal{L}=\bar{\psi}(i\cancel{ D }-m)\psi-\frac{1}{4}F_{\mu \nu}F^{\mu \nu} \\ D_{\mu}=\partial_{\mu}+ieA_{\mu}}$$
- The _local gauge symmetry_, given a function $\alpha$
	- The gauge field $A_{\mu}$ only transforms under _local_ transformations, _not global_ ones
$$\psi\to \exp[ie\alpha(x)]\psi \qquad A_{\mu}\to A_{\mu}-\partial_{\mu}\alpha$$
- It is a $U(1)$ gauge theory, as the transformation $U=\exp(ie\alpha)$ is a _group element_ of $U(1)$

- The theory has two _free parameters_, the fermion mass $m$ and electron charge $e<0$
- $e$ measures the _coupling_ between the Dirac field $\psi$ and the gauge field $A_{\mu}$
	- It is a characteristic of $\psi$, instead of $A_{\mu}$
	- Charge manifests in _global symmetries_, which only transforms $\psi$, not $A_{\mu}$
### Momentum Feynman rules
![[QED Feynman rules.png]]

# Non-Abelian gauge theory
- QED is a $U(1)$ _gauge theory_
- $U(1)$ is an _Abelian group_

- One can have _non-Abelian gauge theories_ from groups such as $SU(N)$ and $SO(N)$
	- Both are _unitary_, with $SO(N)$ being restricted to real elements

## Lie groups
- Gauge theories are always based on a [[Groups in physics|Lie group]]
- A group element must be _continuously linked to the identity_, with generators $T^{a}$
$$U(\epsilon^{a})=\exp(i\epsilon^{a}T^{a})=1+i\epsilon^{a}T^{a}+\dots$$
- The generators are $N\times N$ _Hermitian matrices_ such that $U$ is _unitary_

### Lie algebra
- The _Lie algebra_ of generators is given by the _commutator_:
$$[T^{a},T^{b}]=if^{abc}T^{c}$$
- $f^{abc}$ are the _structure constants_ of the Lie algebra
- Lie algebras also obey the _Jacobi identity_
$$[T^{a},[T^{b},T^{c}]]+[T^{b},[T^{c},T^{a}]]+[T^{c},[T^{a},T^{b}]]=0$$

- The dimension of the Lie algebra is the _number of independent components_
### Relevant Lie groups
- The _special unitary group_ $SU(N)$, where $M^{\dagger}M=I_{n}$ and $\det M=1$
	- Generated by _traceless Hermitian $N\times N$ matrices_, giving dimension $N^{2}-1$
- The _special orthogonal group_ $SO(N)$, where $M^{T}M=I_{n}$ and $\det M=1$
	- Generated by _antisymmetric Hermitian $N\times N$ matrices_, giving dimension $N(N-1)/2$
- The _symplectic group_ $Sp(2N)$ where $M^{T}\Omega M=\Omega$
$$\Omega=\pmatrix{0&I_{n} \\ -I_{n}&0}$$

- The fields must transform in some _representation_ of the relevant _gauge group_
	- They can be _reducible_ or _irreducible_
- $SU(N):$ a _defining representation_ of vectors in $\mathbb{C}^{N}$, on which the $N\times N$ matrices act
- $SO(N):$ vectors in $\mathbb{R}^{N}$, as well as _spinors_
	- Dirac fields: spinor representation of the Lorentz group $SO(3,1)$

### Adjoint representation
- From the Jacobi identity:
$$f^{bcd}f^{ade}+f^{abd}f^{cde}+f^{cad}f^{bde}=0$$
- Define the _adjoint representation_
$$(T^{a}_\text{adj})^{bc}\equiv-if^{abc}$$
- They follow the same algebra:
$$[T^{a}_\text{adj},T^{b}_\text{adj}]=if^{abc}T_\text{adj}^{c}$$
- The adjoint representation has the _dimension of the original Lie group_

## Building a non-Abelian gauge theory
- With QED as a blueprint, one expects a _Dirac-like_ term in $\mathcal{L}$ representing the _coupled matter field_, along with a _Maxwell-like_ term constructed using a _field tensor_

### Matter and gauge field terms
- Given a gauge group $G$, the _matter field_, representing some _fermion_, should transform under some _representation_ $r$ of $G$, with a coupling $g$:
$$\psi\to U\psi\equiv \exp(ig\alpha^{a}T_{r}^{a})\psi$$
- Each generator $T^{a}$ is a $n_{r}\times n_{r}$ _matrix_, while $\psi$ is an $n_{r}-$component _spinor_

- For a _local gauge symmetry_ where $\alpha^{a}=\alpha^{a}(x)$, there must be some _covariant derivative_
$$D_{\mu}=\partial_{\mu}+igA_{\mu}$$
- This representss coupling to a _gauge field_ $A_{\mu}$, representing a _gauge boson_
- $D_{\mu,}A_{\mu}$ are $n_{r}\times n_{r}$ matrices, such that the latter can be written as:
	- $A_{\mu}^{a}$ carries both a _spacetime index_ and a _Lie index_
$$A_{\mu}\equiv A_{\mu}^{a}T^{a}_{r}$$

- The gauge fields _must transform $(A_{\mu}\to A_{\mu}')$ such that_
	- For operators, $\partial_{\mu}U^{-1}=U^{-1}\partial_{\mu}+(\partial_{\mu}U^{-1})$
$$\begin{align}
D_{\mu}\psi&\to U(D_{\mu}\psi) \\ \partial_{\mu}+igA_{\mu}'&=U(\partial_{\mu}+igA_{\mu})U^{-1} \\ A_{\mu}'&=UA_{\mu}U^{-1}+\frac{i}{g}(\partial_{\mu}U)U^{-1}
\end{align}$$
- Substituting the form of $A_{\mu}$ and considering an _infinitesimal transformation_:
$$A_{\mu}'^{a}=A_{\mu}^{a}-\partial_{\mu}\alpha^{a}-gf^{bca}\alpha^{b}A_{\mu}^{c}$$
- The transformation of $A_{\mu}$ is dependent on the _structure constants_
	- For an _Abelian gauge theory_, this reverts to the form seen in QED

### Maxwell-like field term
- Recognise that as $D_{\mu}$ transforms _covariantly_ $(D_{\mu}\to UD_{\mu}U^{-1})$, inspect:
$$[D_{\mu},D_{\nu}]$$
- Drawing an analogy to QED, define the new field tensor:
	- $F_{\mu \nu}^{a}$, like $A_{\mu}^{a}$, is a _scalar_ carrying both _spacetime indices_ and _Lie indices_
$$\displaylines{[D_{\mu},D_{\nu}]\equiv igF_{\mu \nu}^{a}T_{r}^{a} \\ F_{\mu \nu}^{a}=\partial_{\mu}A_{\nu}^{a}-\partial_{\nu}A_{\mu}^{a}-gf^{abc}A_{\mu}^{b}A_{\nu}^{c}}$$
- Again, there is a _new term_ since the gauge group is _non-Abelian_

- The new, _gauge invariant_ Maxwell field term can then be written as:
$$\frac{1}{2g^{2}}\mathrm{Tr}[D_{\mu},D_{\nu}][D^{\mu},D^{\nu}]=-\frac{1}{4}F_{\mu \nu}^{a}F^{a\mu \nu}$$
- Unlike QED, there are _cubic_ and _quartic_ terms here, indicating _self coupling_

- As the non-Abelian gauge fields _do transform under global transformations_, they _carry their own charge_ and can _self-couple_ unlike the $U(1)$ field
# Quantum chromodynamics
- The theory of the _strong force_
- Based on the $SU(3)$ gauge group

- It is an 8-dimensional Lie algebra, giving 8 _gauge bosons_, known as _gluons_
- The _gauge field_ $A_{\mu}$ is a $3\times 3$ _matrix_

- This couples to 6 _fermions_, known as _quarks_
- They still transform as 4-component _spinors_ in terms of _spacetime_
- In terms of _gauge transformations_, it is a 3-component _triplet_
	- They correspond to _colour_

- The QCD Lagrangian:
	- $a$: 8 possible indices corresponding to the _gauge bosons_
	- $A_{\mu}$: $3\times 3$ matrix in terms of _colour indices_
	- $\lambda^{a}$: the _Gell-Mann matrices_
$$\mathcal{L}=-\frac{1}{4}G^{a}_{\mu \nu}G^{a\mu \nu}+\sum_{f \in \{u,d,s,c,t,b\}}\bar{\psi}\left( i\cancel{ \partial }-g_{s}\cancel{ A }^{a}\frac{\lambda^{a}}{2}-m_{f} \right)\psi$$
- The Gell-Mann matrices, explicitly:
$$\displaylines{\lambda^{1}=\pmatrix{0&1&0 \\ 1&0&0 \\ 0&0&0} \qquad \lambda^{2}=\pmatrix{0&-i&0\\i&0&0\\0&0&0} \qquad \lambda^{3}=\pmatrix{1&0&0 \\ 0&-1&0 \\ 0&0&0} \\ \lambda^{4}=\pmatrix{0&0&1 \\ 0&0&0 \\ 1&0&0} \qquad \lambda^{5}=\pmatrix{0&0&-i \\ 0&0&0 \\ i&0&0} \qquad \lambda^{6}=\pmatrix{0&0&0 \\ 0&0&1 \\ 0&1&0} \\ \lambda^{7}=\pmatrix{0&0&0 \\ 0&0&-i \\ 0&i&0} \qquad \lambda^{8}=\frac{1}{\sqrt{ 3 }} \pmatrix{1&0&0 \\ 0&1&0 \\ 0&0&-2}}$$

- The coupling _between quarks_ is _strong at low energies_, resulting in _quark confinement_

## Scattering in QCD
- Feynman rules _without gauge fixing_ (works at _tree level_)
![[QCD Feynman rules.png]]
# Electroweak theory
- Based on the $SU(2)\times U(1)$ gauge group

## A theory of the weak interaction
- A theory of _decay_ should contain _interaction vertices_ which conserve _baryon number_ and _lepton number_, giving necessitating a _two-element_ representation, the simplest of which is $SU(2)$
- The Lie algebra of $SU(2)$ is the Pauli matrices:
$$\sigma^{1}=\pmatrix{0&1\\1&0} \qquad \sigma^{2}=\pmatrix{0&-i\\i&0}\qquad \sigma^{3}=\pmatrix{1&0\\0&-1}$$
- Denote the $SU(2)$ gauge field by $W_{\mu}^{i}$
$$\displaylines{\begin{aligned}
D_{\mu}=\partial_{\mu}+i \frac{g}{2}W_{\mu}^{i}\sigma^{i} &=\partial_{\mu}+i \frac{g}{2}\pmatrix{ W_{\mu}^{3} &W_{\mu}^{1}-iW_{\mu}^{2} \\ W_{\mu}^{1}+iW_{\mu}^{2} & -W_{\mu}^{3}} \\
&\equiv\partial_{\mu}+i \frac{g}{2} \pmatrix{W_{\mu}^{3} & \sqrt{ 2 } W_{\mu}^{+} \\ \sqrt{ 2}W_{\mu}^{-} & -W_{\mu}^{3}}
\end{aligned} \\ W_{\mu}^{\pm}=\frac{1}{\sqrt{  2}}(W_{\mu}^{1}\mp iW_{\mu}^{2})}$$

- The _quarks_ and _leptons_ can then be packaged into $SU(2)$ _doublets_:
$$l\equiv \pmatrix{\nu \\ e} \qquad q\equiv \pmatrix{u \\ d}$$
- The Lagrangian will contain the terms:
$$\mathcal{L} \supset i(\bar{l}\cancel{ D }l+\bar{q}\cancel{ D }q) \supset ig\sqrt{ 2 }\bar{\nu}\cancel{ W }^{+}e$$

- The $W_{\mu}^{\pm}$ fields carry an _electric charge_ of $\pm |e|$
- [[#Charge conjugation]] sends fields into the _minus transpose_, giving:
$$W_{\mu}^{\pm}\to W_{\mu}^{\mp}$$

- However, weak interactions _do not conserve parity_
### Parity violation and hypercharge
- Only the _left-handed_ quarks and leptons will couple to $W^{\mu}$ via $SU(2)$
- This can be implemented using a [[#Weyl spinors and chirality|projector]] $P_{L}$

# Renormalisation

## Ultraviolet divergences
- _Loop corrections_ to propagators and matrix elements are _infinite_
- The one-loop correction to _electron self-energy_ in QED:
![[one loop correction.png]]
$$i \mathcal{M}=\int \frac{d^{4}k}{(2\pi)^{4}} \bar{u}^{s}(-ie\gamma^{\mu}) \left( -\frac{i\eta_{\mu \nu}}{k^{2}} \right) \frac{i(\cancel{ p }-\cancel{ k }+m)}{(p-k)^{2}-m^{2}}(-ie\gamma^{\nu})u^{s}$$
- At _large_ $k$, it is _divergent_
	- Logarithmically divergent as the integrand is _odd_
$$\sim \int d^{4}k \frac{\cancel{ k }}{k^{4}}$$

- The amplitude $i\Sigma$ can be _absorbed_ into the _mass term_ when one considers:
![[QED renormalise.png]]
$$\frac{i}{\cancel{ p }-m}+\left( \frac{i}{\cancel{ p }-m} \right)i\Sigma\left(\frac{i}{\cancel{ p }-m}\right)+\dots=\frac{i}{\cancel{ p }-m+\Sigma}$$
- $m$ can be chosen as an _infinite parameter_, such that $m-\Sigma$ yields the _physically measured electron mass_

- The _renormalisability_ of a theory is not always guaranteed
### Mass dimension
- Work in _natural units_
$$\hbar=c=1$$
- _Mass/energy dimensions_:
$$[S]=0 \qquad[x^{\mu}]=-1 \qquad [\mathcal{L}]=4$$
- _Bosonic fields_ $\phi$ and _fermionic fields_ $\psi$ have _different dimensions_
	- Bosonic term: _two derivatives_ / fermionic term: _one derivative_
$$[\phi]=1 \qquad [\psi]=\frac{3}{2}$$
- The _mass_ in the Lagrangian will always have dimension $1$
- The _gauge couplings_ are always _dimensionless_

### Renormalisability from diagrams


## Non-renormalisable interactions
