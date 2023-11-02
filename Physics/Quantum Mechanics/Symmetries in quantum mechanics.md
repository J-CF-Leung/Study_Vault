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

# Scalar operators

# The Wigner-Eckart Theorem

# Spatial inversion and parity
- The _spatial inversion operation_ is:
$$\hat{P}: \bm{r}\to-\bm{r}$$
- The _eigenvalues and eigenstates_ of the operator:
$$\hat{P}\ket{\psi}=P\ket{\psi}$$
- Applying parity _twice_ gives back the _original wave function_, hence:
$$P=\pm1$$
