- Like in [[Analytical classical mechanics#Symmetries and Noether's Theorem|classical mechanics]], a _symmetry_ leads to a _conservation law_
	- _Time_ translation: _energy_
	- Spatial: _momentum_
	- Rotation: _angular momentum_
	- Inversion: _parity_

- A _symmetry transformation_ can be considered:
	- Active (moving the system)
	- Passive (moving the axes)

# The transformation operator
- In _quantum mechanics_, a transforation is implemented with an _operator_:
$$\ket{\psi}\to\ket{\psi'}=\hat{U}\ket{\psi}$$
- If the system is _invariant_, then the _probabilities_ and _normalisations_ are unchanged, so for _any two states_:
$$|\braket{\phi'|\psi'}|^2=|\braket{\hat{U}\phi|\hat{U}\psi}|^2=|\braket{\phi|\psi}|^2$$
- This means the operator is _unitary_
	- The condition can also be satisfied by _conjugating_ the overlap, but $\hat{U}$ is _unitary by definition_
	$$\hat{U}^{-1}=\hat{U}^\dagger$$
- An _antiunitary_ transformation is _time reversal_

## Infinitesimal transformation
- _Continuous symmetries_ must be taken _arbitrarily close_ to the identity:
$$\hat{U}(\epsilon)=\hat{I}+i\epsilon\hat{T}+O(\epsilon^2)$$
- _Unitarity_ then gives that $\hat{T}$ is _Hermitian_
$$\hat{T}^\dagger=\hat{T}$$
- $\hat{T}$ is the _generator_ of the transformation
	- Term from [[Rotations and Lie Algebra|Lie groups]]

## Finite transformation
- Any _finite transformation_ can be _built up_ from infinitesimal ones
- Let the _finite_ transformation be $\theta\equiv N\epsilon$:
$$\hat{U}(\theta)=\left(\hat{I}+i\frac{\theta}{N}\hat{T}\right)^N\longrightarrow \exp(i\theta\hat{T})$$
- The _matrix elements_ of some observable $\hat{A}$:
$$\braket{\phi|\hat{A}|\psi}\to \braket{\phi|\hat{U}^\dagger\hat{A}\hat{U}|\psi}$$
- Hence the _effect_ of the transformation are obtained by _transforming the observable_ while _leaving the system unchanged_

## Conservation
- Suppose the matrix elements are _left unchanged_, then it _must satisfy_:
$$[\hat{A},\hat{U}]=0\Longrightarrow[\hat{A},\hat{T}]=0$$

- If the _Hamiltonian is invariant under symmetry_:
$$[\hat{H},\hat{T}]=0$$
- Then from [[Fundamental concepts of quantum mechanics#Ehrenfest's Theorem|Ehrenfest's Theorem]]:
$$\frac{d}{dt}\braket{\psi|\hat{H}|\psi}=\frac{i}{\hbar}\braket{\psi|[\hat{H},\hat{T}]|\psi}=0$$

- Hence, the _generator is conserved_
	- Conservation: _constant expectation value_

- For some _energy eigenstate_ $\ket{\psi}$:
$$\hat{H}\ket{\psi'}=\hat{H}\hat{U}\ket{\psi}=\hat{U}\hat{H}\ket{\psi}=E\ket{\psi'}$$
- Provided the states $\ket{\psi}$ and $ket{\psi'}$ are _distinct_, the _energy level_ must be _degenerate_

# Time translation
- The _time-translation operator_ shifts the _origin of the time coordinate_ by time $\tau$:
$$\hat{U}(\tau)\ket{\psi(t)}=\ket{\psi(t+\tau)}$$

- Provided the probabilities are _conserved_, $\hat{U}$ is _unitary_
- For an _infinitesimal translation_, give a _generator_ $\hat{H}$:
$$\hat{U}=1-i\frac{\hat{H}}{\hbar}\tau+O(\tau^2)$$
- A _finite time translation_ is then:
$$\hat{U}(\tau)=\exp\left(-i\frac{\hat{H}\tau}{\hbar}\right)$$
- Considering states at times $t$ and $t+dt$, one obtains the time-dependent Schrodinger equation:

# Spatial translation
- In [[Analytical classical mechanics|classical mechanics]], the _conservation of total momentum_ for an _isolated system_ is a consequence of _invariance under spatial translations_
- Consider a translation by vector $\bm{a}$, for a _system of particles_ with positions $\{\bm{r}_n\}$:
$$\braket{\psi'|\hat{\bm{r}}_n|\psi'}=\braket{\psi|\hat{\bm{r}}_n|\psi}+\bm{a}$$
- Then define the _spatial translation operator_:
$$\hat{U}(\bm{a})\ket{\psi}=\ket{\psi'}$$
- To leave the system _invariant_, it must be _unitary_
- From the above, it must also satisfy:
$$\hat{U}^\dagger\hat{\bm{r}}_n\hat{U}=\hat{\bm{r}}+\bm{a}$$

## Momentum as a generator
- Let there be a _vector of Hermitian operators_ as the _generator_:
$$\displaylines{\hat{U}=1-\frac{i}{\hbar}\hat{\bm{P}}\cdot\bm{a}+O(a^2) \\ \hat{\bm{P}}=(\hat{P}_1,\hat{P}_2,\hat{P}_3)}$$
- From this, one obtains the _commutation relation_:
$$[\hat{\bm{r}}_n,\hat{\bm{P}}\cdot\bm{a}]=i\hbar\bm{a}$$
- This must hold for _any choice_ of $\bm{a}$, hence:
$$[\hat{r}_{nj},\hat{P}_k]=i\hbar\delta_{jk}$$
- The _spatial translation generator_ $\hat{\bm{P}}$ is the _total momentum operator_ of the system

- For an _isolated_ system, the _energy eigenvalues_ must be _invariant_
	- Energy cannot be dependent on _where the system is_
$$[\hat{H},\hat{U}]=0$$
- Then using _Ehrenfest's Theorem_:
$$\frac{d}{dt}\braket{\psi|\hat{\bm{P}}|\psi}=0$$
- From this, _spatial invariance_ leads to _conservation of total angular momentum_

## Form of the operator
- The _order of spatial translations_ is _irrelevant_, hence the operators $\hat{U}(\bm{a})$ and $\hat{U}(\bm{b})$ must _commute_:
$$\hat{U}(\bm{a})\hat{U}(\bm{b})=\hat{U}(\bm{b})\hat{U}(\bm{a})$$
- By _equating_ coefficients on both sides, one gets:
$$[\hat{P}_j,\hat{P}_k]=0$$

- Applying a _spatial translation_: 
$$\psi(x)\to\psi'(x)=\psi(x-a)\equiv\hat{U}(a)\psi(x)$$
- For an _infinitesimal translation_, and _Taylor expanding_ the wave function:
$$\hat{P}_x=-i\hbar\pd{}{x}$$
# Spatial rotations
- In [[Analytical classical mechanics|classical mechanics]], the _conservation of angular momentum_ for an _isolated system_ is a consequence of _invariance under spatial rotations_

## The rotation matrix
- A _spatial rotation_ is a real, linear transformation of the form:
$$r_i\to r_i'=\sum_j R_{ij}r_j$$
- $R_{ij}$ is a _rotation matrix_ hence:
$$R^TR=I \hspace{1.5cm}\text{det}(R)=+1$$
	- One can also have $\text{det} (R)=-1$, which incorporates a _spatial inversion_
- One can [[Rotations and Lie Algebra#Lie's approach|show]] that $R$ takes the form:
$$R=I+\omega+O(\omega^2)\hspace{1.5cm} \omega^T=-\omega$$
- One therefore needs _three independent parameters_ for $\omega$:
$$\omega=\pmatrix{0 & \omega_3 & -\omega_2 \\ -\omega_3 & 0 & \omega_1 \\ \omega_2 & -\omega_1 & 0} \hspace{1.5cm} \bm{\omega}=(\omega_1,\omega_2,\omega_3)$$
- Example: for a _rotation of angle $\phi$ along the $z-$axis_, $\omega=(0,0,\phi)$
$$R\approx\pmatrix{1&\phi&0 \\ -\phi&1&0 \\ 0&0&1}$$

## The operator
- Under some spatial rotation, the states _transform_ as:
$$\ket{\psi}\to\hat{U}(R)\ket{\psi}$$
- If the system is _rotationally invariant_, then $\hat{U}(R)$ is _unitary_

- _Successive rotations_ can _combine_:
$$\hat{U}(R_n)\dots\hat{U}(R_2)\hat{U}(R_1)=\hat{U}(R_n\dots R_2R_1)$$
- The _rotation_ can then be written as:
$$\displaylines{\hat{U}(\omega)=\hat{I}+\frac{i}{\hbar}(\hat{\bm{\omega}}\cdot\hat{\bm{J}})+O(\omega^2) \\ \hat{\bm{J}}=(\hat{J}_1,\hat{J}_2,\hat{J}_3)}$$
- Consider _three successive infinitesimal rotations_ $R_1,R_2,R_3$ with $\omega'$, $\omega$, and $-\omega'$:
$$\displaylines{R_3R_2R_1=I+\omega+\omega\omega'-\omega'\omega+O(\omega^2,\omega'^2)\approx I+\omega+\Omega \\ \Omega_i=\epsilon_{ijk}\omega_j'\omega_k}$$
- Expanding the unitary operators:
$$\hat{U}(R_3R_2R_1)=\hat{I}+\frac{i}{\hbar}(\hat{\bm{\omega}}\cdot\hat{\bm{J}})+\frac{i}{\hbar}(\hat{\bm{\Omega}}\cdot\hat{\bm{J}})+\dots$$
- Expanding $\hat{U}(R_3)\hat{U}(R_2)\hat{U}(R_1)$, then _equating coefficients_:
$$[\hat{J}_i,\hat{J}_j]=i\hbar\epsilon_{ijk}\hat{J}_k$$
- One can then interpret $\bm{J}$ as the _total angular momentum operator_

## The form of the operator
- Let there be a rotation though some _angle_ $\phi_0$ about the $z-$axis:
$$\displaylines{\bm{\omega}=(0,0,\phi_0) \\ \psi(\phi)\to\psi'(\phi)=\hat{U}(\phi_0)\psi(\phi)=\psi(\phi+\phi_0)}$$
- In the case of an _infinitesimal rotation_:
$$\hat{U}(\phi_0)=\hat{I}+\phi_0\pd{}{\phi}+\dots\equiv\hat{I}+\frac{i}{\hbar}\phi_0\hat{J}_z+\dots$$
- This gives the _form_ of $\hat{J}_z$:
$$\hat{J}_z=-i\hbar\pd{}{\phi}$$

## Scalar operators and angular momentum conservation
- A _scalar operator_ is one that _remains invariant after some rotation_:
$$\ket{\psi'}=\hat{U}(R)\psi\longrightarrow\braket{\psi'|\hat{K}|\psi'}=\braket{\psi|\hat{K}|\psi}$$
- This gives that it must _commute with $\hat{U}$_ and $\hat{\bm{J}}$:
$$[\hat{U},\hat{K}]=0\hspace{1.5cm}[\hat{\bm{J}},\hat{K}]=0$$
- For some _isolated system_, $H$ (a scalar operator) must be _invariant under spatial rotations_:
$$[\hat{\bm{J}},\hat{H}]=0$$
- Therefore, from Ehrenfest's theorem:
$$\frac{d}{dt}\mean{\hat{\bm{J}}}=0$$
## Scalar operators and commutation relations
- From the above, one can see that for _single particle systems_, $\hat{\bm{L}}$ and $\hat{\bm{L}}^2$ must _always commute with all scalar operators_:
$$\displaylines{[\hat{\bm{L}},\hat{\bm{r}}^2]=[\hat{\bm{L}},\hat{\bm{p}}^2]=[\hat{\bm{L}},V(r)]=0 \\ [\hat{\bm{L}}^2,\hat{\bm{r}}^2]=[\hat{\bm{L}}^2,\hat{\bm{p}}^2]=[\hat{\bm{L}}^2,V(r)]=0}$$
- For the _total angular momentum_ $\hat{\bm{J}}=\hat{\bm{L}}+\hat{\bm{S}}$, the relations above hold, as well as:
$$[\hat{\bm{J}},\hat{\bm{L}}\cdot\hat{\bm{S}}]=[\hat{\bm{J}}^2,\hat{\bm{L}}\cdot\hat{\bm{S}}]=0$$
- With respect to $\hat{\bm{L}}$ and $\hat{\bm{S}}$, $\hat{\bm{L}}\cdot\hat{\bm{S}}$ is _not a scalar operator_
	- This explains why in the [[The hydrogen atom|hydrogen atom fine structure]], the _relativistic and Darwin terms_ will _commute_ with the _uncoupled set_, while the _spin-orbit_ term commutes with the _coupled set_

# The Wigner-Eckart Theorem
- Let $\hat{\bm{J}}$ be a _generic angular momentum operator_ satisfying:
$$[\hat{J}_i,\hat{J}_j]=i\hbar\epsilon_{ijk}\hat{J}_k$$
- Consider the _scalar operator_ $\hat{K}$, satisfying:
$$[\hat{J}_z,\hat{K}]=[\hat{\bm{J}}^2,\hat{K}]=0$$
- By considering the _average of these commutators_ w.r.t. _angular momentum eigenstates_:
$$\braket{j'm_j'|\hat{K}|jm_j}=\braket{jm_j|\hat{K}|jm_j}\delta_{jj'}\delta_{m_jm_j'}$$
- The states may also be characterised by _other quantum numbers_ $\alpha$

>[!info] The Wigner-Eckart Theorem
>For angular momentum operator $\hat{\bm{J}}$ and scalar operator $\hat{K}$, the _matrix elements satisfy_:
>$$\braket{\alpha''j''m''|\hat{K}|\alpha' j'm'}=\langle\alpha''j''||\hat{K}||\alpha' j'\rangle\;\delta_{j'j''}\delta_{m'm''}$$
>Here, $\braket{\alpha'j'||\hat{K}||\alpha j}$ is the _reduced matrix element_, which is _independent of_ $m$
- The _reduced matrix element_ is _not strictly a matrix element_
	- It is the _common constant_ for a _set_ of matrix elements

- One can also restate it as:
$$\braket{\alpha''j''m''|\hat{K}|\alpha' j'm'}=\langle \alpha'' j''||\hat{K}||\alpha'j'\rangle$$
- In other words, the _expectation values of a scalar operator are independent of $m$_
	- $m$ indicates the _orientation_ of angular momentum
	- A _scalar operator_ is _rotationally invariant_

- Since the _Hamiltonian_ $\hat{H}$ is a scalar operator, _energy must be independent of $m$_:
$$\hat{H}\ket{\alpha jm}=E_{\alpha j}\ket{\alpha jm}$$
- For some _isolated system_, this forces energy levels to be _always degenerate_
- Degeneracy is usually due to _underlying symmetry_ (rotational in this case)

- One can also prove the above using $[\hat{H},\hat{J}_\pm]=0$

- One can also express the Wigner-Eckart Theorem using the [[Angular momentum in quantum mechanics#The trivial case|trivial case]] of angular momentum addition:
$$\braket{\alpha''j''m''|\hat{J}|\alpha' j'm'}=\langle \alpha''j''||\hat{K}||\alpha j\rangle\braket{00;j'm'|j''m''}$$

# Vector operators
- Define a _vector operator_ $\hat{\bm{V}}$, with its components _transforming like ordinary 3-vectors_:
$$\displaylines{\hat{\bm{V}}=(\hat{V}_1,\hat{V}_2,\hat{V}_3) \\ \mean{\hat{V}_i'}=R_{ij}\mean{\hat{V}_j}}$$
- Setting $\ket{\psi'}=\hat{U}(R)\ket{\psi}$:
$$\hat{U}^\dagger(R)\hat{V}_i\hat{U}(R)=R_{ij}\hat{V}_j$$
- Substituting the form of $\hat{U}$, one gets:
$$[\hat{J}_i,\hat{V}_j]=i\hbar\epsilon_{ijk}\hat{V}_k$$
- $\hat{\bm{r}}$, $\hat{\bm{p}}$, $\hat{\bm{L}}$ are _all vector operators_:
$$[\hat{J}_i,\hat{r}_j]=i\hbar\epsilon_{ijk}\hat{r}_k\hspace{1cm}[\hat{J}_i,\hat{p}_j]=i\hbar\epsilon_{ijk}\hat{p}_k \hspace{1cm} [\hat{J}_i,\hat{L}_j]=i\hbar\epsilon_{ijk}\hat{L}_k$$
- This also applies to $\hat{\bm{J}}$ as the vector operator
- For a _single particle system_, $\hat{\bm{L}}=\hat{\bm{J}}$

## The Wigner-Eckart Theorem for vector operators
- The _constraints_ on matrix elements of a vector operator are expressed in terms of _spherical components_ $(V_{+1},V_{-1},V_0)$:
$$V_{+1}=-\frac{1}{\sqrt{2}}(V_1+iV_2)\hspace{1cm}V_{-1}=\frac{1}{\sqrt{2}}(V_1-iV_2)\hspace{1cm} V_0=V_3$$
- For operators $\hat{\bm{V}}$ and $\hat{\bm{J}}$ obeying the commutation relations above:
>[!info] Wigner-Eckart Theorem
>The _matrix elements_ of the _spherical components_ of a vector operator are given by:
>$\braket{\alpha''j''m''|\hat{V}|\alpha'j'm'}=\langle\alpha''j''||\hat{V}||\alpha'j'\rangle\braket{1m;j'm'|j''m''}$
>where $m=-1,0,1$
- The _reduced matrix element_ is _dependent on $\hat{V}$_, and _not_ on $m$
- The _Clebsch-Gordan coefficient_ is entirely _dependent_ on $m,m',m''$

# Spatial inversion and parity
- The _spatial inversion operation_ is:
$$\hat{P}: \bm{r}\to-\bm{r}$$
- The _eigenvalues and eigenstates_ of the operator:
$$\hat{P}\ket{\psi}=P\ket{\psi}$$
- Applying parity _twice_ gives back the _original wave function_, hence:
$$P=\pm1$$
