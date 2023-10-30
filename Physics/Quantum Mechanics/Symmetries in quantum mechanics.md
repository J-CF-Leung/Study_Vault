- Like in [[Analytical classical mechanics#Symmetries and Noether's Theorem|classical mechanics]], a _symmetry_ leads to a _conservation law_
	- _Time_ translation: _energy_
	- Spatial:
	- Rotation:
	- Inversion:

- A _symmetry transformation_ can be considered:
	- Active (moving the system)
	- Passive (moving the axes)

- In _quantum mechanics_, a transforation is implemented with an _operator_:
$$\ket{\psi}\to\ket{\psi'}=\hat{U}\ket{\psi}$$
- If the system is _invariant_, then the _probabilities_ and _normalisations_ are unchanged, so for _any two states_:
$$|\braket{\phi'|\psi'}|^2=|\braket{\hat{U}\phi|\hat{U}\psi}|^2=|\braket{\phi|\psi}|^2$$
- This means the operator is _unitary_
	- The condition can also be satisfied by _conjugating_ the overlap, but $\hat{U}$ is _unitary by definition_
	$$\hat{U}^{-1}=\hat{U}^\dagger$$
- An _antiunitary_ transformation is _time reversal_

- _Continuous symmetries_ must be taken _arbitrarily close_ to the identity:
$$\hat{U}(\epsilon)=\hat{I}+i\epsilon\hat{T}+O(\epsilon^2)$$
- _Unitarity_ then gives that $\hat{T}$ is _Hermitian_
$$\hat{T}^\dagger=\hat{T}$$
- $\hat{T}$ is the _generator_ of the transformation
	- Term from [[Rotations and Lie Algebra|Lie groups]]

- Any _finite transformation_ can be _built up_ from infinitesimal ones
- Let the _finite_ transformation be $\theta\equiv N\epsilon$:
$$\hat{U}(\theta)=\left(\hat{I}+i\frac{\theta}{N}\hat{T}\right)^N\longrightarrow \exp(i\theta\hat{T})$$
- The _matrix elements_ of some observable $\hat{A}$:
$$\braket{\phi|\hat{A}|\psi}\to \braket{\phi|\hat{U}^\dagger\hat{A}\hat{U}|\psi}$$
- Hence the _effect_ of the transformation are obtained by _transforming the observable_ while _leaving the system unchanged_

- Suppose the matrix elements are _left unchanged_, then it must satisfy:
$$[\hat{A},\hat{U}]=0$$
- Also commute with T

- Hamiltonian is invariant, then Ehrenfest's theorem
- T is conserved (expectation values are constant)

- For some _energy eigenstate_
- Provided the states are _distinct_, the _energy level_ must be _degenerate_

- Symmetries and selection rules

# Time translation
- The _time-translation operator_ shifts the _origin of the time coordinate_ by time $\tau$:
$$\hat{U}(\tau)\ket{}$$

- Provided the probabilities are _conserved_, $\hat{U}$ is _unitary_
- For an _infinitesimal translation_, give a _generator_ $\hat{H}$:
$$\hat{U}=$$
- A _finite time translation_ is then

- All states must then have a _time dependence_:

- One then obtains the _time-dependent Schrodinger equation_

# Spatial translation
- The _conservation of total momentum_ for an _isolated system_ is a consequence of _invariance under spatial translations_

# Spatial rotations
