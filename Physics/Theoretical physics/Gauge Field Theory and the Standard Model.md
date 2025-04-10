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
	- Up $(u)$, down $(d)$, strange $(s)$, charm $(c)$, top $(t)$, bottom $(b)$

- Each quark $\psi$ transforms as 4-component _spinors_ in terms of _spacetime_
- In terms of _gauge transformations_, it is a 3-component _triplet_
	- They correspond to _colour_

- The QCD Lagrangian:
	- $a$: 8 possible indices corresponding to the _gauge bosons_
	- $A_{\mu}$: $3\times 3$ matrix in terms of _colour indices_
	- $\lambda^{a}$: the _Gell-Mann matrices_
$$\mathcal{L}=-\frac{1}{4}G^{a}_{\mu \nu}G^{a\mu \nu}+\sum_{f \in \{u,d,s,c,t,b\}}\bar{\psi}_{f}\left( i\cancel{ \partial }-g_{s}\cancel{ A }^{a}\frac{\lambda^{a}}{2}-m_{f} \right)\psi_{f}$$
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
### Parity violation, unification, and hypercharge
- Only the _left-handed_ quarks and leptons will couple to $W^{\mu}$ via $SU(2)$
- This can be implemented using a [[#Weyl spinors and chirality|projector]] $P_{L}$ on the fields $l$ and $q$

- However, the $Z$ boson of the weak force _couples to both left and right handed particles_
- The $Z$ boson and the _photon_ are interpreted as a _linear combination_ of $W_{\mu}^{3}$ (coupling to _only left-handed_ fermions) and another $U(1)$ field, denoted $B_{\mu}$ (coupling to _both_ left and right handed fermions)
- This gives _electroweak theory_

- The _left-handed fermions_ in the $SU(2)$ doublets $q_{L},l_{L}$ (with coupling $g$), are _also given a $U(1)$ charge_ for coupling to $B_{\mu}$ (with coupling $g'$), known as the _weak hypercharge_ $Y_{q,l}$
- The _right-handed fermions_ $u_{R},d_{R},e_{R}$ are _singlets_ of $SU(2)$ such that they _do not transform_ under $SU(2)$, while given the $U(1)$ _weak hypercharges_ $Y_{u,d,e}$
	- Only _left-handed_ neutrinos have been observed

- The _physical gauge fields_ $A_{\mu}$ and $Z_{\mu}$ must be some _linear combination_ of $W_{\mu}^{3}$ and $B_{\mu}$
$$\displaylines{W_{\mu}^{3}=\cos\theta_{W}Z_{\mu}+\sin\theta_{W}A_{\mu} \qquad B_{\mu}=-\sin\theta_{W}Z_{\mu}+\cos\theta_{W}A_{\mu} \\ \sin^{2}\theta_{W}=0.231}$$
- $\theta_{W}$ is the _Weinberg angle_

### From hypercharge to electric charge
- _Inspect_ both left and right handed parts of the Lagrangian to find the _resulting couplings_ to _photons_ (represented by $A_{\mu}$) in terms of $g,g',\theta_{W},Y_{q,l,u,d,e}$
- _Matching_ to QED, find the above values in terms of $|e|$

- The _electroweak coupling Lagrangian_ for _right-handed_ fermions
$$\mathcal{L} \supset -\overline{\psi_{R}}g'Y_{\psi}\cancel{ B }\psi_{R} \supset -\overline{\psi_{R}} (g'\cos\theta_{W})Y_{\psi}\cancel{ A }\psi_{R}$$
- From this, $g'\cos\theta_{W}$ must be the _electric charge_, and $Y_{\psi}$ are the _charges in units of_ $|e|$
	- Quark charges: from _compositions of $p$ and $n$_
$$\displaylines{g'\cos\theta_{W}=|e| \\ Y_{e}=1 \qquad Y_{u}=+\frac{2}{3} \qquad Y_{d}=-\frac{1}{3}}$$
- The same for _left-handed fermions_:
$$\mathcal{L} \supset -\overline{\psi_{L}} \left( \frac{g}{2}\sigma^{3}\cancel{ W }^{3}+g'Y_{\psi}\cancel{ B } \right)\psi_{L}\supset -\overline{\psi_{L}}\left(  \frac{g\sin\theta_{W}}{2}\sigma^{3}+g'\cos\theta_{W}Y_{\psi} \right)\cancel{ A }\psi_{L}$$
- Using the fact that particles in doublets have a _charge difference_ of $1$, then solving for the values in $Y_{\psi}$:
$$g\sin\theta_{W}=|e| \qquad Y_{q}=+\frac{1}{6} \qquad Y_{l}=-\frac{1}{2}$$
### Couplings to the Z boson
- The $Z$ boson _couples differently_ to left and right-handed bosons
- Inspecting the $\cancel{ Z }$ terms of the left and right-handed Lagrangians, the couplings are:
$$g\cos\theta_{W}I_{3}-g'\sin\theta_{W}Y=\frac{|e|}{\sin(2\theta_{W})}(I_{3}-Q\sin^{2}\theta_{W})$$
- Here, $I_{3}$ is the _weak isospin_
	- Equal to $0$ for _right-handed_ fermions
	- Equal to the _eigenvalues_ of $\sigma^{3}/2$ for _left-handed_ fermions

### Remaining issues with electroweak theory
- The left-handed and right-handed fermions _transform as different representations_ of $SU(2)$ and $U(1)$
- This _disallows a mass term_ for the fermions, contrary to observations

- _Gauge invariance_ forbids _mass terms_ for the gauge fields
	- The most general Lagrangian contains a _coupling term_ and a _Maxwell-like field term_, neither of which contains a mass term
- While the _photon_ is massless, the _weak interaction gauge bosons_ have mass
	- Massless means _long range interaction_, and the weak interaction is _short range_

- Masses are in fact given by _spontaneous symmetry breaking_ and the _Higgs mechanism_

# The Higgs mechanism
- Mechanism by which particles gain a _mass_

## Spontaneous symmetry breaking, Goldstone's Theorem, and the Higgs mechanism
- Toy model: $\phi^{4}$ theory
$$\mathcal{L}=(\partial_{\mu}\phi^{*})(\partial^{\mu}\phi)-V(\phi) \qquad V(\phi)=m^{2}|\phi|^{2}+\lambda|\phi|^{4}$$
- For a classical theory, the $m^{2}>0$ case has a _minimum at the origin_
- For a quantum theory, the _vacuum expectation value_ vanishes, such that one can make _expansions_ around $\phi=0$ and consider _fluctuations_ about that point
$$\braket{ 0|\phi |0  }=0 $$
- However, for $m^{2}<0$, there is a _potential minimum_ at:
$$|\phi|^{2}=\frac{-m^{2}}{2\lambda}\equiv \frac{v^{2}}{2}$$
- This gives a _set of degenerate ground states_ which one can quantise around
- However, these ground states _do not obey phase symmetry_:
$$\phi\to \phi'=\exp(i\alpha)\phi\implies \mathcal{L}[\phi']\neq \mathcal{L}[\phi]$$
- Fluctuations about the minimum _in the degenerate direction_ carry _no energy cost_

- For a _large wavelength excitation_, there is _little to no kinetic/potential energy cost_
- _Goldstone's Theorem_ states that _spontaneous symmetry breaking_ always implies the _existence of a massless particle_

- Example: choose the _vacuum direction_ to be the _real axis_, and add _real scalar fields_ $\phi_{1,2}$ as _fluctuations_
$$\phi=\frac{1}{\sqrt{ 2 }}(v+\phi_{1}+i\phi_{2})$$
- $\phi_{1}$ has _mass_ $\sqrt{ -2m^{2} }$
- $\phi_{2}$ is _massless_

### Abelian Higgs model
- Go to a $U(1)$ gauge symmetry instead:
$$\displaylines{\phi\to \exp(ie\alpha(x))\phi \qquad A_{\mu}\to A_{\mu}-\partial_{\mu}\alpha \\ \mathcal{L}=(D_{\mu}\phi)^{*}(D^{\mu}\phi)-m^{2}|\phi|^{2}-\lambda|\phi|^{4} \\ D_{\mu}=\partial_{\mu}+ieA_{\mu}}$$
- After spontaneous symmetry breaking, expanding around $|\phi|^{2}=v^{2}/2$, one gains a _mass term_ for $A_{\mu}$:
$$\mathcal{L} \supset +\frac{e^{2}v^{2}}{2}A^{\mu}A_{\mu}$$
- _Spontaneous symmetry breaking_ of some _scalar field_ gives rise to _gauge boson mass_

- A _massless vector boson_ only has 2 _degrees of freedom_
	- Example: two photon _helicities_
	- One eliminated by equation of motion, the other eliminated by _gauge fixing_
- A _massive_ vector boson has 3 degrees of freedom
	- 3 polarisations along which the _spin_ can point in the _rest frame_

- One can _gauge fix_ into the _unitary gauge_:
$$\alpha(x)=-\tan \frac{\phi_{2}}{v+\phi_{1}}$$
- The _transformed scalar field_ $\phi_{2}'$ _vanishes_ ("eaten" by $A_{\mu}$), giving $A_{\mu}$ the _additional degree of freedom_ (the third polarisation)
- The "eaten" scalar field is known as the _Higgs field_

### Higgs mechanism for a non-Abelian gauge group
- In general, for some gauge group $G$, after spontaneous symmetry breaking of the _scalar field_, $G$ will be broken into the _subgroup_ $H \subset G$
	- The scalar field will still transform as some _representation_ of $G$
- For a _global symmetry_, the _dimension_ of the Lie algebra gives the _number of Goldstone bosons_
- For a _local symmetry_ with _representation_ $r$, the _mass term_ is given by:
$$\frac{g^{2}}{2}v^{\dagger} T_{r}^{a}T_{r}^{b}vA^{\mu a}A^{b}_{\mu}=\frac{(m^{2})^{ab}}{2}A^{\mu a}A^{b}_{\mu}$$

- Gauge bosons corresponding to _broken generators_ where $T^{a}v\neq 0$ become _massive_
- The others will remain _massless_

## The Higgs mechanism in electroweak theory
- Applying to electroweak theory, which has group $SU(2)\otimes U(1)$ and gauge bosons:
$$W_{\mu}^{\pm},W^{3}_{\mu},B_{\mu}$$
- $W_{\mu}^{\pm}$ and $Z_{\mu}$ become _massive_ while $A_{\mu}$ remains _massless_
- From the above, the group should be broken into $U(1)$, which is some _combination_ of the original $U(1)$ and the $U(1)$ _subgroup of_ $SU(2)$

### Gauge boson masses
- Introduce a _scalar field_ (as opposed to spinor), the _Higgs field_ $H$, transforming as a _doublet_ of $SU(2)$, with a _hypercharge_ of $Y=1/2$
- The Lagrangian involving $H$, with the _Higgs potential_:
$$\displaylines{\mathcal{L} \supset (D^{\mu }H)^{\dagger}(D_{\mu }H)-\mu^{2}(H^{\dagger}H)+\lambda(H^{\dagger}H)^{2} \\ D_{\mu}H=\left( \partial_{\mu}+i \frac{g}{2}\sigma^{i}W_{\mu}^{i}+i \frac{g'}{2}B_{\mu} \right)H}$$
- The _vacuum expectation value_ for $H$:
$$\sqrt{ H^{\dagger}H }=\sqrt{ \frac{\mu^{2}}{2\lambda} }\equiv \frac{v}{\sqrt{ 2 }}$$
- Without loss of generality, for _real_ $v$
$$\langle H \rangle=\pmatrix{0 \\ v/\sqrt{ 2 }} $$
- The _gauge boson mass term_ is then:
$$\frac{1}{8}\pmatrix{0 & v} \pmatrix{gW_{\mu}^{3}+g'B_{\mu} & \sqrt{ 2 }gW_{\mu}^{+} \\ \sqrt{ 2 }gW_{\mu}^{-} &-gW_{\mu}^{3}+g'B_{\mu}}\pmatrix{gW_{\mu}^{3}+g'B_{\mu} & \sqrt{ 2 }gW_{\mu}^{+} \\ \sqrt{ 2 }gW_{\mu}^{-} &-gW_{\mu}^{3}+g'B_{\mu}}\pmatrix{0 \\ v}$$
- Using the below expressions for the Weinberg angle:
$$\cos\theta_{W}=\frac{g}{\sqrt{ g^{2}+g'^{2} }} \qquad \sin\theta_{W}=\frac{g'}{\sqrt{ g^{2}+g'^{2} }}$$
- The mass term then gives:
$$\frac{(gv)^{2}}{4}W_{\mu}^{+}W^{\mu-}+\frac{(g^{2}+g'^{2})v^{2}}{8}Z_{\mu}Z^{\mu}$$
- Since $W_{\mu}^{\pm}$ is _complex_, and $Z_{\mu}$ is _real_, one must take their different _normalisations_ into account to get the masses:
$$m_{W}=\frac{gv}{2} \qquad m_{Z}=\frac{\sqrt{ g^{2}+g'^{2} }v}{2}=\frac{m_{W}}{\cos\theta_{W}} \qquad m_{A}=0$$
- The _massless photon_ and the ratio of $m_{W}/m)Z$ are in agreement with the _choice of symmetry breaking_ from $SU(2)\otimes U(1)$ to $U(1)$

### Fermion masses
- The _quarks_ and _leptons_ also get their masses from the Higgs field
- Given the Higgs field as a scalar field doublet of $Y=1/2$, one can write the _Yukawa couplings_ to the fermionic fields:
$$\mathcal{L} \supset -\lambda^{u}\overline{q_{L}}H^{c}u_{R}-\lambda^{d}\overline{q_{L}}Hd_{R}-\lambda^{e}\overline{l_{L}}He_{R}+\text{h.c.}$$
- Here, $H^{c}$ is a doublet of _opposite hypercharge_ $Y=-1/2$
$$H^{c}\equiv i\sigma^{2}H$$
- This represents an _interaction_ between the fermionic fields and the Higgs field
- From the Higgs vacuum expectation value:
$$m_{u}=\frac{\lambda^{u}v}{\sqrt{ 2 }}\qquad m_{d}=\frac{\lambda^{d}v}{\sqrt{ 2 }}\qquad m_{e}=\frac{\lambda^{e}v}{\sqrt{ 2 }}$$
# The Standard Model
- The Standard Model includes _three generations_ of quarks and leptons

- Also taking QCD into account, it is reliant on the gauge group:
$$SU(3)\otimes SU(2)\otimes U(1)$$

- Fields and their representations:
![[Standard model representations.png|400]]
## The Higgs boson
- The $H$ field has 4 degrees of freedom ($SU(2)$ doublet, with complex values)

- 3 degrees of freedom are _"eaten" by the electroweak gauge bosons_
- The final scalar field is the _Higgs boson_, which is _massive_

- Going to the _unitary gauge_, one writes the field as:
$$H=\frac{1}{\sqrt{ 2 }}\pmatrix{ 0\\ v+h(x)}$$
- $h(x)$ is a _real scalar field_
	- It has _no electric charge_ due to the lack of global phase symmetry

- Its _coupling_ to other fields can be found by substituting $v+h$ in the _Higgs coupling_ Lagrangians
- The _Yukawa coupling_ to fermion $i$:
$$\mathcal{L} \supset -\frac{m_{i}}{v}h\bar{\psi}_{i}\psi_{i}$$
- Coupling to the _gauge bosons_:
$$\mathcal{L} \supset m_{W}^{2}\left( \frac{2h}{v}+\frac{h^{2}}{v^{2}} \right)W_{\mu}^{+}W^{\mu-}+\frac{m_{Z}^{2}}{2}\left( \frac{2h}{v}+\frac{h^{2}}{v^{2}} \right)Z_{\mu}Z^{\mu}$$
- The Higgs boson also has _self interactions_:
$$\displaylines{\begin{align}
\mathcal{L} \supset +\frac{\mu^{2}}{2}(v+h)^{2}-\frac{\lambda}{4}(v+h)^{4} &\supset -\lambda v^{2}h^{2}-\lambda vh^{3}-\frac{\lambda}{4}h^{4} \\
&=-\frac{m_{h}^{2}}{2}h^{2}-\frac{m_{h}^{2}}{2v}h^{3}-\frac{m_{h}^{2}}{8v^{2}}h^{4}
\end{align} \\ m_{h}^{2}=2\lambda v^{2}}$$
### Higgs boson decays
- Despite the self-interaction term, energy-momentum conservation _prevents_ decaying into multiple Higgs bosons
	- Gluons: self-interaction is allowed as it is _massless_

- For a _light Higgs_, it will be _below mass threshold_ to decay into gauge boson pairs
	- Competing factor: the _Higgs-gauge boson couplings_ all grow with the mass of the gauge boson
- For light Higgs $>10 \text{ GeV}$, decay to _bottom quark pairs_ dominates
- For _heavy_ Higgs $m_{h}>2m_{W}$, decay to $W^{+}W^{-}$ and $ZZ$ pairs dominates
	- The _crossover_ to this regime is slightly below $2m_{W}=160\text{ GeV}$, at $\sim 140\text{ GeV}$ instead by allowing _one virtual boson_ (not on-shell), which then subsequently decays into non-virtual quarks and leptons

- Partial decay widths and branching ratios:
![[Higgs boson decays.png]]
- The actual mass of $m_{h}\approx 125\text{ GeV}$ has a variety of decay modes

- The Higgs has a coupling to $\gamma\gamma$ and $gg$ modes despite having _no electric or colour charge_
- They can be generated by _quark loops_, such as:
![[Higgs to photons.png|250]]

- Higgs boson generation in $p+p$ collisions is mainly due to the _$gg$ coupling_ as the quark-Higgs coupling is _small_

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
$$[\phi_{B}]=1 \qquad [\psi_{f}]=\frac{3}{2}$$
- The _mass_ in the Lagrangian will always have dimension $1$
- The _gauge couplings_ are always _dimensionless_

### Renormalisability from diagrams
- Given some diagram, to find renormalisability, one must find the _superficial degree of divergence_ $D$, for any _loop momentum_ in the diagram:
$$D=\text{power of }k\text{ in numerator}-\text{power of }k\text{ in denominator}$$

- Divergences:
	- $D>0$ is a _divergent diagram_
	- $D=0$ is a _logarithmically divergent_ diagram
	- $D<0$ is _finite_

- Characterise a diagram with the integers:
	- $L$ loops
	- $F_{I,E}$ _internal/external fermion propagators_
	- $B_{I,E}$ _internal/external boson propagators_
	- $V$ _vertices_
	- $P_{j}$ as the _power_ of _loop momentum_ entering vertex $j$ (e.g. 3-gluon vertex $P=1$)

- This gives:
$$D=4L-F_{I}-2B_{I}+\sum_{j}P_{j}$$
- This can be cast into another form from the _geometric properties_ of the diagram

- The _number of integrated loops_:
	- Each vertex has a _delta function_ which fixes one of the momenta
$$L=F_{I}+B_{I}-V+1$$
- Meanwhile, each _vertex_ $j$ comes from a term in $\mathcal{L}$ with dimension 4, with $F_{j},B_{j}$ fermionic/bosonic fields, momenta $P_{j}$, and _coupling_ $g_{j}$
$$4=\frac{3}{2}F_{j}+B_{j}+P_{j}+\mathrm{dim}(g_{j})$$
- When one then _sums over all vertices_, as _internal_ propagators end on 2 of them, and each _external_ propagator ends in 1:
$$\sum_{j}F_{j}=2F_{I}+F_{E} \qquad \sum_{j}B_{j}=2B_{I}+B_{E}$$
- Combining these results, one gets:
$$D=4-\frac{3}{2}F_{E}-B_{E}-\sum_{j}\mathrm{dim}(g_{j})$$
- For _fixed initial and final states_, the superficial degree of divergence is _only dependent on the dimension of couplings involved_

- If a coupling has _negative mass dimension_, the divergence _gets worse for each loop diagram included_, and the theory _cannot be renormalised_
- For both QED and the Standard Model, they are _renormalisable_
	- Only couplings of _vanishing_ or positive mass dimension

- Meanwhile, gravity (with the _Einstein-Hilbert action_) has _negative mass coupling_ and is therefore _not renormalisable perturbatively_
## Non-renormalisable interactions
