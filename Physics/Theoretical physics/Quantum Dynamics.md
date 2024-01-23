- For a _time-dependent system_, one can have different _pictures_ of dealing with time-dependence
- In the _Schrodinger picture_, the time dependence is in the _state vector_
	- The _Hamiltonian_ can also be time-dependent, depending on $\hat{V}$

# Time-independent Hamiltonian
## Dynamics in the Schrodinger picture
- For a _time-independent Hamiltonian_, the _time-independent equation_ gives the _eigenstates_ $\ket{\psi}$
$$\hat{H}\ket{\psi}=E\ket{\psi}  $$
- $E$ is a _constant eigenvalue_
- One can then create the _time-evolution operator_:
$$\hat{U}(t)=\exp\left( -i \frac{\hat{H}t}{\hbar} \right)$$
- As $\hat{H}$ is _Hermitian_, $\hat{U}$ is _unitary_

- The time-dependence of the eigenstates:
$$\ket{\psi(t)}=\hat{U}(t)\ket{\psi(0)}  $$
- One can then _expand_ any state ket in the _eigenbasis of the Hamiltonian_:
$$\displaylines{\hat{H}\ket{\psi_{n}}=E_{n}\ket{\psi_{n}} \\ \ket{\psi(t)}=\sum_{n}c_{n}\exp\left( -\frac{iE_{n}t}{\hbar} \right)\ket{\psi_{n}}    } $$

- One can also choose to solve for eigenstates in _position/momentum bases_
- Example: [[Quantum Harmonic Oscillator]]
	- One can solve the equation in the _position basis_, with $\hat{p}\to (\hbar/i)\partial/\partial x$
	- One can also use the _ladder operators_ $\hat{a},\hat{a}^{\dagger}$
## Dynamics in the Heisenberg picture
- For a _unitary operator_ $\hat{\mathcal{U}}$
$$\hat{\mathcal{U}}\hat{\mathcal{U}}^{\dagger}=1$$
- Physical quantities are _invariant under unitary transformations_
	- They must be _independent of basis_
$$\ket{\psi}\to \hat{\mathcal{U}}\ket{\psi} \hspace{1.5cm} \hat{\mathcal{O}}\to \hat{\mathcal{U}}\hat{\mathcal{O}}\hat{\mathcal{U}}^{\dagger} \hspace{1.5cm}\braket{ \psi|\hat{\mathcal{O}} | \psi }\to \braket{ \psi|\hat{\mathcal{O}} |\psi  }   $$

- Take the _Hermitian conjugate of time evolution operator_ as the _unitary transformation_:
$$\hat{\mathcal{U}}=\hat{U}^{\dagger}=\exp\left( \frac{i\hat{H}t}{\hbar} \right)$$
- Then the _wave function time dependence cancels out_:
$$\ket{\psi(t)}=\hat{U}\ket{\psi(0)}\longrightarrow \hat{\mathcal{U}}\hat{U}\ket{\psi(0)}=\ket{\psi(0)}    $$
- Then, _all time dependence_ is in the _operator_:
$$\hat{\mathcal{O}}\to \hat{\mathcal{O}}(t)=\hat{U}^{\dagger}\hat{\mathcal{O}}\hat{U}$$
- As $\hat{U}$ and $\hat{H}$ obviously commute, $\hat{H}$ is _unchanged_
- The fundamental _commutation relations_ still hold:
$$\left[ \hat{x}(t),\hat{p}(t) \right]=i\hbar$$
 
- This then gives the _Heisenberg equation of motion_:
$$\frac{d\hat{\mathcal{O}(t)}}{dt}=\frac{i}{\hbar}\left[ \hat{H},\hat{\mathcal{O}}(t) \right]$$
- This is analagous to the [[Analytical classical mechanics#Poisson brackets|Poisson bracket]] in classical mechanics

- Given the Hamiltonian:
$$\hat{H}=\frac{\hat{p}^{2}}{2m}+\hat{V}\left( \hat{x} \right)$$

- The Heisenberg equations of motion then give [[Analytical classical mechanics#Hamiltonian formulation|Hamilton's equations of motion]]:
$$\frac{d\hat{x}}{dt}=\frac{\partial \hat{H}}{\partial \hat{p}}=\frac{\hat{p}(t)}{m}\hspace{1.5cm}\frac{d\hat{p}}{dt}=-\frac{\partial \hat{H}}{\partial x}=-\frac{d\hat{V}}{dx}$$
- When a _time average_ is taken by taking _matrix elements with constant state kets_, one recovers [[Principles of quantum mechanics#Ehrenfest's Theorem|Ehrenfest's Theorem]]

### Harmonic oscillator
- For the _harmonic oscillator_:
$$\frac{d\hat{x}}{dt}=\frac{\hat{p}}{m}\hspace{1.5cm} \frac{d\hat{p}}{dm}=-m\omega^{2}\hat{x}$$
- This traces out an _elliptical trajectory_ in phase space
	- _Different from the expected value_, which is _dependent on the wave function_
$$\begin{align}x(t)&=\cos(\omega t)x(0)+\sin(\omega t) \frac{p(0)}{m\omega} \\ p(t)&=\cos(\omega t)p(0)-m\omega \sin(\omega t)x(0) \end{align}$$

- Using the _equation of motion_ and expressing the Hamiltonian using _ladder operators_:
$$\hat{a}(t)=\exp(-i\omega t)\hat{a}(0)\hspace{1.5cm}\hat{a}^{\dagger}(t)=\exp\left( i\omega t \right)\hat{a}(0)$$

## The interaction picture
- Take the Hamiltonian as:
$$\hat{H}=\hat{H}_{0}+\hat{V}$$
- The _unitary transformation_:
$$\hat{\mathcal{U}}=\exp\left( +i \frac{\hat{H}_{0}t}{\hbar} \right)$$
- The time dependence _arises from the potential term_ $\hat{V}$

# Time-dependent Hamiltonian
- Have a general _time-dependent Hamiltonian_
- Example: quantum harmonic oscillator with a _driving force_:
$$\hat{H}(t)=\frac{\hat{p}^{2}}{2m}+\frac{1}{2}m\omega^{2}\hat{x}^{2}-F(t)\hat{x}$$
- The time-dependent Schrodinger equation still holds:
$$\hat{H}(t)\ket{\psi(t)}=i\hbar \frac{\partial}{\partial t}\ket{\psi(t)}  $$
- If the _Hamiltonian at different times does not commute_, one _cannot_ find a _common eigenbasis_ for _all times_
- For the case of a _time-dependent force_, one gets:
$$\left[ \hat{H}_{1},\hat{H}_{2} \right]=-i\hbar \frac{\hat{p}}{m}[F(t_{1})-F(t_{2})]$$

- If it _does_ commute:
$$\left[ \hat{H}(t),\hat{H}(t') \right]=0\hspace{1cm}\forall\, t.t'$$
- Then one can write the time-evolution as:
$$\hat{U}(t)=\int -\frac{i}{\hbar}\hat{H}(t') \, dt' $$


- So, in the general case, one must consider _infinitesimally intervals of time_, where:
$$\lim_{ \delta t \to 0 } \left[ \hat{H}(t),\hat{H}(t+\delta t) \right]=0$$
- One can then _split_ the evolution into many _infinitesimal stages_:
$$\hat{U}(t)=\lim_{ \Delta t \to 0 } \exp\left( -\frac{i\hat{H}(t-\Delta t)\Delta t}{\hbar} \right)\exp\left( -\frac{i\hat{H}(t-2\Delta t)\Delta t}{\hbar} \right)\dots\exp\left( -\frac{i\hat{H}(0)\Delta t}{\hbar} \right)$$
- Here, $\hat{H}$ are _evaluated at each time_ $t-\Delta t,t-2\Delta t\dots 0$
- By using a _Taylor expansion_ then _multiplying all terms_, one gets:
$$\begin{align}\hat{U}(t)&=1-\frac{i}{\hbar}\int _{0}^{t} dt_{1}\,\hat{H}(t_{1})-\frac{1}{\hbar^{2}}\int_{0}^{t}\, dt_{2}\int _{0}^{t_{2}}\, dt_{1}\hat{H}(t_{2})\hat{H}(t_{1})+\dots  \\ &=1+\sum_{n=1}^{\infty}\left( -\frac{i}{\hbar} \right)^{n}\int _{0}^{t} \, dt_{n}\int _{0}^{t_{n}} \, dt_{n-1}\dots \int_{0}^{t_{2}}  \, dt_{1}\hat{H}(t_{n})\hat{H}(t_{n-1})\dots \hat{H}(t_{1})\end{align}$$
- This is the _Dyson series_
- In the limit of _commuting Hamiltonians_, one recovers the single integral

- Introduce the _time-ordering operator_, which places the _operator evaluated at later times first_:
$$\mathcal{T}\left[ \hat{H}(t_{1})\hat{H}(t_{2}) \right]=\begin{cases} \hat{H}(t_{1})\hat{H}(t_{2})&t_{1}\geq t_{2} \\ \hat{H}(t_{2})\hat{H}(t_{1})&t_{2}>t_{1}\end{cases}$$
- In this case, one can let _all integrals_ range from $0$ to $t$, and introduce a _normalisation factor_ $1/n!$
$$\hat{U}(t)=1-\frac{i}{\hbar}\int _{0}^{t} dt_{1}\,\hat{H}(t_{1})-\frac{1}{2\hbar^{2}}\int_{0}^{t}\, dt_{2}\int _{0}^{t}\, dt_{1}\,\mathcal{T}[\hat{H}(t_{2})\hat{H}(t_{1})]+\dots$$
- One can then write:
$$\hat{U}(t)=\mathcal{T}\exp\left( -\frac{i}{\hbar}\int _{0}^{t}\hat{H}(t') \, dt'  \right)$$
- For a _time-independent Hamiltonian_, the time-ordering does not matter

## Driven harmonic oscillator and coherent states
$$\hat{H}(t)=\frac{\hat{p}^{2}}{2m}+\frac{1}{2}m\omega^{2}\hat{x}^{2}-F(t)\hat{x}$$
