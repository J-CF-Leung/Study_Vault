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
- The _state ket_ time dependence _arises from the potential term_ $\hat{V}$
- The _observable_ time dependence arises from $\hat{H}_{0}$

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
- Using the [[#Dynamics in the Heisenberg picture|Heisenberg equations of motion]]:
$$\displaylines{\frac{d\hat{x}}{dt}=\frac{\hat{p}(t)}{m} \\ \frac{d\hat{p}}{dt}=-m\omega^{2}\hat{x}+F(t)}$$
- The Hamiltonian can also be written as:
$$\hat{H}(t)=\hbar \omega\left( \hat{a}^{\dagger}\hat{a}+\frac{1}{2} \right)-F(t)\sqrt{ \frac{\hbar}{2m\omega} }\left( \hat{a}+\hat{a}^{\dagger} \right)$$
- This gives:
$$\frac{d\hat{a}}{dt}=-i\omega \hat{a}+iF(t)\sqrt{ \frac{1}{2m\hbar\omega} }$$
- One can _define_ the operator $\tilde{a}$:
$$\displaylines{\tilde{a}=\exp(i\omega t)\hat{a} \implies \frac{d\tilde{a}}{dt}=+i \frac{F(t)\exp(i\omega t)}{\sqrt{ 2m\hbar \omega }}\\ \tilde{a}(t)=\tilde{a}(0)+\frac{i}{\sqrt{ 2m\hbar\omega }}\int_{0}^{t} F(t')\exp(i\omega t') \, dt' }$$
- Similarly:
$$\tilde{a}^{\dagger}(t)=\tilde{a}^{\dagger}(0)-\frac{i}{\sqrt{ 2m\hbar\omega }}\int_{0}^{t} F(t')\exp(-i\omega t') \, dt' $$
- This matches the _classical evolution_ of position and momentum

- Consider the _ground state_:
$$\hat{a}\ket{0}=0 $$
- Since $\hat{a}(t)=\hat{U}^{\dagger}(t)\hat{a}\hat{U}(t)$, $\hat{U}(t)\hat{a}(t)=\hat{a}\hat{U}(t)$:
$$\hat{a}\hat{U}(t)\ket{0}= \frac{i}{\sqrt{ 2m\hbar\omega }}\int_{0}^{t}F(t')\exp[-i\omega (t-t')]  \, dt' \hat{U}(t)\ket{0} $$
- Hence, $\hat{U}(t)\ket{0}$ is a [[Coherent states|coherent state]], with _eigenvalue_:
$$\alpha=\frac{i}{\sqrt{ 2m\hbar \omega }}\int_{0}^{t}F(t')\exp[-i\omega(t-t')] \, dt' $$

- One can prove that if the system _starts in a coherent state_, it _stays coherent_:
$$\displaylines{\hat{U}(t)\ket{\alpha}=\exp(i\phi)\ket{\alpha'} \\ \alpha'=\alpha \exp(-i\omega t)+\frac{i}{\sqrt{ 2m\hbar\omega }}\int _{0}^{t} F(t')\exp[i\omega(t-t')] \, dt' }  $$
## Spin in a magnetic field
- The _simplest quantum system_ is one with _two states_, e.g. spin $1/2$
- The Hilbert space is _two-dimensional_, and all operators are $2\times2$ _matrices_
	- Living in the $SU(2)$ group

- Expressing some _spin-like_ variable with operator $\hat{\boldsymbol{S}}$, the _most general Hamiltonian_ is
	- The addition of an _identity_ simply _shifts_ the energy
$$\hat{H}(t)=\boldsymbol{h}(t)\cdot \hat{\boldsymbol{S}}$$
- Here, $\boldsymbol{h}(t)$ is some _"magnetic field"_

- Expressing everything in the _basis_ of $S_{z}$ and using [[Angular momentum in quantum mechanics#Spin 1/2|Pauli matrices]]:
$$\hat{S}_{i}=\frac{1}{2}\sigma_{i}\hspace{1cm}\hat{H}(t)=\frac{1}{2}\begin{pmatrix}h_{z}(t)&h_x(t)-ih_{y}(t) \\ h_{x}(t)+ih_{y}(t)&-h_{z}(t)\end{pmatrix}\hspace{1cm}\ket{\Psi}=\begin{pmatrix}\psi_{\uparrow}\\ \psi_{\downarrow}\end{pmatrix} $$
- Time-dependent Schrodinger equation:
$$i\hbar \frac{d\ket{\Psi}}{dt}=\hat{H}(t)\ket{\Psi}  $$
- The formal solution:
$$\ket{\Psi(t)}=\hat{U}(t,t')\ket{\Psi(t')}  $$
- $\hat{U}(t,t')$ represents some _rotation_ in Hilbert space, with $\hat{H}$ being an _angular velocity_
- As rotations at different times _do not commute_, there is _no simple relation_ for $\hat{U}$

- In the _Heisenberg picture_, adding on the time-dependence, and using the _equation of motion_ (using commutation relations for the Pauli matrices):
$$\displaylines{\hat{S}(t)=\exp\left( i \frac{\hat{H}t}{\hbar} \right)\hat{S}\exp\left( -i \frac{\hat{H}t}{\hbar} \right) \\ \frac{d\hat{S}}{dt}=\frac{i}{\hbar}\left[ \hat{H},\hat{S} \right]=\frac{1}{\hbar}\boldsymbol{h}(t)\times \hat{\boldsymbol{S}}}$$

- Therefore, the spin [[Charged Particles#Precession of the spin-1/2 particle|precesses about the magnetic field]]
- The solution can be expressed using some $3\times 3$ _rotation matrix_:
	- The $SU(2)$ algebra and $SO(3)$ algebras are the _same locally_
	- The rotation matrix and the _time-evolution operator_ contain the _same information_
$$\boldsymbol{S}(t)=R(t)\boldsymbol{S}(0)$$
- The rotation matrix can be expressed as:
$$R(t,t')=\mathcal{T}\exp\left( \int_{t'}^{t} \Omega(t_{i}) \, dt_{i}  \right)$$
- It is a _composition of infinitesimal rotation matrices_
	- The rotations must be _applied in the correct order_, hence the _time ordering_
- $\Omega$ is some _instantaneous angular velocity_:
$$\Omega_{jk}(t)=-\frac{1}{\hbar}\epsilon_{ijk}h_{i}(t)$$

## Rabi oscillations
- Given a _Rabi field_ $h_{R}$, consider the magetic field:
$$\boldsymbol{h}(t)=\begin{pmatrix}h_{R}\cos(\omega t) \\ h_{R}\sin(\omega t) \\ h_{0}\end{pmatrix}$$
- Express the Hamiltonian using the _ladder operators_:
$$\hat{H}(t)=h_{0}\hat{S}_{z}+\frac{h_{R}}{2}\left[ \exp(-i\omega t)\hat{S}_{+}+\exp(i\omega t)\hat{S}_{-} \right]$$
- Do a _time-dependent basis transformation_
	- It is _unitary_, hence the motion is _unchanged_
$$\hat{\mathcal{U}}(t)=\exp\left( i\omega t\hat{S}_{z} \right)\implies\ket{\Psi_{R}(t)}= \exp\left( i\omega t\hat{S}_{z} \right)\ket{\Psi(t)} $$
- This corresponds to going into a _rotating frame_
- The Hamiltonian becomes _time-independent_, as the transformed state obeys:
$$\begin{align}i\hbar \frac{d}{dt}\ket{\Psi_{R}}&=i\hbar \hat{\mathcal{U}} \frac{d}{dt}\ket{\Psi}-\hbar\omega \hat{S}_{z}\ket{\Psi_{R}} \\&=\hat{\mathcal{U}}H(t)\ket{\Psi}-\hbar\omega \hat{S}_{z}\ket{\Psi_{R}} \\ &=\hat{\mathcal{U}}H(t)\hat{\mathcal{U}}^{\dagger}\ket{\Psi_{R}}-\hbar\omega S_{z}\ket{\Psi_{R}}  \\ &=\hat{H}_\text{Rabi}\ket{\Psi_{R}}   \end{align} $$
- The new Hamiltonian:
$$\begin{align}
\hat{H}_\text{Rabi}&=\hat{\mathcal{U}}H(t)\hat{\mathcal{U}}^{\dagger}-\hbar\omega \hat{S}_{z}  \\ &=(h_{0}-\hbar\omega)\hat{S}_{z}+h_{R}\hat{S}_{z}
\end{align}$$
- This corresponds to _precession_ about the _axis_:
$$\boldsymbol{h}_\text{Rabi}=\begin{pmatrix}h_{R} \\ 0 \\ h_{0}-\hbar\omega\end{pmatrix}$$
- The state lies on a _spherical manifold_

- The _precession frequency_:
$$\omega_{R}=\frac{1}{\hbar}\sqrt{ (h_{0}-\hbar\omega)^{2}+h_{R}^{2} }$$
- The _amplitude is at a maximum_ when $h_{0}=\hbar\omega$, which matches the _natural frequency_ where $h_{R}=0$

# The adiabatic approximation
- Corresponds to some _separation of time-scales_
- Let the Hamiltonian _vary very slowly_
- One can _solve_ for eigenstates at some time $t^{*}$, giving _instantaneous eigenstates_:
$$\hat{H}(t)\ket{\pm_{t}}=E_{\pm}(t)\ket{\pm_{t}}  $$

- If the system _varies very slowly_ over time $\tau$
	- Compared to the _natural frequency_ of the states
$$\frac{\Delta E\tau}{\hbar}\ll 1$$
- There are _no transitions_ between levels of energy interval $\Delta E$, and the system _stays in the instantaneous eigenstate_
	- Requires that _off-diagonal_ elements of $\dot{H}$ are _small_

## Time evolution of wave function

### For a two-state system
- One can _expand_ the state at any time _in terms of instantaneous eigenstates_:
$$\ket{\Psi(t)}=c_{+}(t)\ket{+_{t}}+c_{-}(t)\ket{-_{t}}   $$

- Treat changes in the Hamiltonian as a [[Time-Independent Approximation Methods|time-independent perturbation]]
	- $t$ is treated as a _parameter_
	- One gets the _same result_ by substituting into the time-dependent Schrodinger equation and differentiating both sides
- Each state changes by amount:
$$\delta \ket{\pm_{t}}=\frac{\braket{ \mp_{t}|\delta H|\pm_{t}  }}{E_{\pm}(t)-E_{\mp}(t)}\ket{\mp_{t}}   $$

- From the time-dependent Schrodinger equation, the coefficients then vary by:
$$i\hbar \frac{d}{dt}\begin{pmatrix} c_{+} \\ c_{-}\end{pmatrix} = \begin{pmatrix} E_{+}(t)& i\hbar\frac{\braket{ +_{t}|\dot{H} | -_{t} }}{E_{+}-E_{-}}  \\i\hbar \frac{\braket{ -_{t}|\dot{H} | +_{t} }}{E_{-}-E_{+}}  &E_{-}(t) \end{pmatrix} \begin{pmatrix} c_{+} \\ c_{-}\end{pmatrix}$$
- For a _slow enough variation_, the _off-diagonal terms vanish_

- The solution is then:
$$c_{\pm}(t)= \exp\left(-\frac{i}{\hbar} \int E_{\pm}(t')  \, dt'  \right) c_{\pm}(0) $$
- The amplitudes _evolve independently_, and there are _no transitions_ between the instantaneous eigenstates
	- A _generalisation_ for $c_{n}(t)=\exp(-iE_{n}t/\hbar)c_{n}(0)$

- The approximation is valid when:
$$\hbar \left| \braket{ -_{t} |\dot{H}|+_{t}  }  \right| \ll [E_{+}(t)-E_{-}(t)]^{2} $$

- As expected, this corresponds to a _large splitting_

- It is a _semiclassical_ approximation as it _improves_ with _smaller_ $\hbar$

### General case
- The _instantaneous energy eigenstates_:
$$H(t)\ket{n;t}=E_{n}(t)\ket{n;t}  $$
- The time-dependent Schrodinger equation:
$$i\hbar \frac{\partial}{\partial t}\ket{\alpha;t}=H(t)\ket{\alpha;t}  $$
- Writing the wave function as:
$$\displaylines{\ket{\alpha;t}=\sum_{n} c_{n}(t)\exp[i\theta_{n}(t)]\ket{n;t} \\ \theta_{n}(t)\equiv-\frac{1}{\hbar}\int _{0}^{t}E_{n}(t')\, dt' } $$
- $\theta_{n}(t)$ is the _dynamical phase_
	- _Independent_ of adiabaticity

- _Substituting_ this into the time-independent Schrodinger equation and taking the _inner product_ with energy eigenbra $\bra{m;t}$
$$\dot{c}_{m}=-\sum_{n}c_{n}(t)\exp[i(\theta_{n}-\theta_{m})]\Braket{ m;t|\frac{\partial}{\partial t} |n;t  } $$

- By taking the _time derivative_ of the time-independent equation, one gets:
$$\dot{c}_{n}=-c_{n}\Braket{n;t| \frac{\partial}{\partial t} | n;t }-\sum_{m\neq n} c_{m}(t)\exp[i(\theta_{n}-\theta_{m})] \frac{\braket{ n;t|\dot{H} |m;t  }}{E_{m}-E_{n}}  $$

- In the _adiabatic approximation_:
$$\frac{|\braket{ n;t|\dot{H} | m;t }|}{E_{m}-E_{n}}\equiv \frac{1}{\tau}\ll \Braket{ n;t|\frac{\partial}{\partial t} | n;t }  $$
- The _timescale_ for change must be _very large_ compared to the _inverse natural frequency_ 

- The coefficients are then:
$$\displaylines{c_{n}(t)=\exp[i\gamma_{n}(t)]c_{n}(0) \\ \gamma_{n}(t)\equiv i \int_{0}^{t}  \bra{n;t'}\left[\frac{\partial}{\partial t'} \ket{  n;t' }\right]\, dt' }$$
- If the energy eigenstates are _normalised_, then the integrand is purely _imaginary_ and the phase $\gamma_{n}$ is _real_

- If a system is _initially_ in an energy eigenstate $\ket{n}$, it _stays_ there:
$$\ket{\alpha^{(n)};t}=\exp[i\gamma_{n}(t)](\exp[i\theta_{n}(t)]\ket{n;t}) $$
- $\theta_{n}(t)$ is the _dynamical phase_
- $\gamma_{n}(t)$ is a _result of the adiabatic approximation_

- For a _time-dependent_ Hamiltonian, one uncovers the expected result:
$$\displaylines{\theta_{n}=-\frac{E_{n}t}{\hbar} \hspace{1cm}\gamma_{n}(t)=0 \hspace{1cm}\ket{n;t}=\ket{n} \hspace{1cm}c_{n}(t)=c_{n}(0) \\ \ket{\Psi}=\sum_{n}c_{n}(0)\exp\left( -i\frac{E_{n}t}{\hbar} \right)\ket{n}  }$$
- The derivation only works when there is _no degeneracy_ or _level crossings_
## Landau-Zener tunnelling
- Consider the Hamiltonian:
$$H=\begin{pmatrix} \beta t & \Delta \\ \Delta &-\beta t\end{pmatrix}$$
- The _instantaneous eigenvalues_:
$$E_{\pm}(t)=\pm\sqrt{ (\beta t)^{2}+\Delta^{2} }$$
- As a _function_ of $t$, it shows an _avoided crossing_
	- $\Delta$ acts like a _mass_
- The _minimum splitting_ is $2\Delta$

- Hence, for the _adiabatic approximation_ to hold, one must have:
$$\frac{\hbar\beta}{\Delta^{2}}\ll 1$$
- Instead, consider the limit:
$$\frac{\hbar\beta}{\Delta^{2}}\gg 1$$
- The state is _very likely to tunnel_

- Take the _very small parameter_ $\Delta^{2}/\hbar\beta$ 
- The _probability of transition_:
$$P(\ket{-}_{t=-\infty}\to \ket{+}_{t=+\infty}  )=\frac{\pi\Delta^{2}}{\hbar\beta}$$

# Berry's phase
- States are a _ray_ in a vector space, and _phases_ in the wavefunction _do not affect motion_
$$\psi\to \exp(i\theta)\psi$$
- However, if the Hamiltonian _traverses a closed path in Hilbert space_, the wavefunction can _accumulate_ a _global_ phase which is _geometric_ (depending on the _closed path_ in Hilbert space)
## Two-state system
- A _change_ to eigenstates, with some _phase ambiguity_:
$$\delta \ket{+_{t}}= \frac{\braket{ -_{t}|\delta H |+_{t}  }}{E_{+}(t)-E_{-}(t)}\ket{-_{t}}  $$
- It is _orthogonal_ to the original state
	- A _parallel_ change is simply _dilation_ or adding a _phase_
	- The phase is _local_

- Let the Hamiltonian undergo a _closed path $\gamma$ in parameter space_
	- It is a _field in parameter space_, which is _parametrised_ by vector $\boldsymbol{H}$
	- Example: _magnetic field_
- Let the change be _cyclic_:
$$\boldsymbol{H}(T)=\boldsymbol{H}(0)$$

- The state can pick up a _global phase_, which _only depends on the path_
$$\ket{\pm_{T}}= \ket{\pm_{0}}\exp\left( -\frac{i}{\hbar} \int _{0}^{t}E_{\pm}(t') \, dt'  \right)\exp(i\theta_{B}[\gamma]) $$

- Define the _instantaneous eigenstates_:
	- _Fix_ the phase of the eigenstates
$$\ket{\pm_{t}}\equiv\ket{H(t),\pm}  $$
- As $H(t)$ changes _smoothly_, the _perturbation_ to the state:
$$\delta \ket{H(t),\pm}= \frac{\braket{  H(t),\mp|\delta H|H(t),\pm  }}{E_{\pm}-E_{\mp}}\ket{H(t),\mp}+\braket{ H,\pm| \delta H| H,\pm  }\ket{H(t),\pm}     $$
- In the _adiabatic regime_, the first term _vanishes_
	- The second term is typically _neglected_ as it is a parallel change, but it has an effect for a _closed adiabatic change_ in Hamiltonian

- Take a _derivative_ w.r.t. the _parameters_ of the Hamiltonian:
	- $\delta \boldsymbol{H}$ is a _differential vector in parameter space_
$$\delta H=\delta \boldsymbol{H}\cdot \nabla_{H}$$

- The vector field:
$$\boldsymbol{A}_{\pm}(\boldsymbol{H})\equiv i\braket{H,\pm|\nabla_{\boldsymbol{H}}|H,\pm  } $$

- This is the _Berry potential_, or _Berry connection_
- When it is _integrated over a closed path_, then it contributes a _global phase_ which _cannot be ignored_
	- Similar to the [[Charged Particles#The Aharanov-Bohm Effect|Aharanov-Bohm Effect]]

- With the adiabatic approximation:
$$\delta \ket{H,+}=-i\boldsymbol{A}_{+}(\boldsymbol{H})\cdot \dot{\boldsymbol{H}}\ket{H,+}  $$
- The _solution_ to the coefficients:
$$c_{\pm}(t)=\exp\left( - \frac{i}{\hbar}\int[E_{\pm}(t')+\hbar \boldsymbol{A}_{\pm}(\boldsymbol{H})\cdot \dot{\boldsymbol{H}}]  \, dt'  \right)c_{\pm}(0)$$
- There are _two contributions_
	- A _dynamical phase_ from $E_{\pm}$, which _vanishes over a closed path_ (depending on _energy_, and the _amount of time taken_ in an open path)
	- A _geometric phase_ from $\boldsymbol{A}_{\pm}$, which _depends on the path_
- It also depends on the _manifold_ in parameter space and its _topology_

## General case
- From the adiabatic approximation for a general, non-degenerate Hamiltonian, the _phase term_ can be written as an _integral over parameter space_:
$$\gamma_{n}(t)\equiv i \int _{0}^{t}\braket{ n;t'}\left[ \frac{\partial}{\partial t}\ket{n;t'}  \right]  \, dt' =i \int _{\boldsymbol{H}(0)}^{\boldsymbol{H}(t)} \braket{n;t | \nabla_{\boldsymbol{H}}|n;t } {}  \cdot d\boldsymbol{H} $$
- It is a _function of the path_, and _not_ how it is traversed in time

- For a _closed path_ $\mathcal{C}$:
$$\gamma_{n}(\mathcal{C})=i \oint_{\mathcal{C}}\braket{ n;t|\nabla_{\boldsymbol{H}} | n;t }\cdot d\boldsymbol{H} =\oint_{\mathcal{C}} \boldsymbol{A}_{n}\cdot d\boldsymbol{H}$$
- The vector field:
$$\boldsymbol{A}_{n}(\boldsymbol{H})=i\braket{ n;t|\nabla_{\boldsymbol{H}} |n;t  } $$

## Berry potential and curvature
- The geometric phase $\gamma_{n}$ is a _gauge invariant quantity_
- Let there be a _local gauge transformation_:
$$\ket{n;t}\to \exp[i\delta(\boldsymbol{H})]\ket{n;t} \implies \boldsymbol{A}_{n}(\boldsymbol{H})\to \boldsymbol{A}_{n}(\boldsymbol{H})-\nabla_{\boldsymbol{R}}\delta(\boldsymbol{H})   $$
- This leaves $\gamma_{n}$ _unchanged_
- This reinforces the fact that $\gamma_{n}$ is a _geometric property_ of the path taken

- $\boldsymbol{A}_{n}$ is analagous to the _vector potential_
- One can then define an analagous _"magnetic field"_, known as the _Berry curvature_
	- As expected, also _gauge invariant_
$$\displaylines{\boldsymbol{B}_{n}(\boldsymbol{H})=i(\nabla_{\boldsymbol{H}}\bra{n;t})\times (\nabla_{\boldsymbol{H}}\ket{n;t} )  \\ \gamma_{n}(\mathcal{C})=\oint_{\mathcal{C}} \boldsymbol{A}_{n}\cdot d\boldsymbol{H}=\iint \boldsymbol{B}_{n}\cdot d\boldsymbol{S}}$$
- It can also be defined as a _second-order tensor_:
$$\Omega_{n,jk}(\boldsymbol{H})=\frac{\partial}{\partial H^{j}}A_{n,k}(\boldsymbol{H})-\frac{\partial}{\partial H^{k}}A_{n,j}(\boldsymbol{H})$$

- The _Berry phase_ is then a _surface integral_ of the Berry curvature

## Berry phase for a rotating magnetic field
- Example: the _direction_ of a [[#Spin in a magnetic field|magnetic field]] lives on a _2-sphere_
$$\displaylines{\boldsymbol{h}=h_{0}\hat{\boldsymbol{n}} \hspace{1cm}\hat{\boldsymbol{n}}=\begin{pmatrix}\sin\theta \cos \phi \\ \sin\theta \sin \phi \\ \cos\theta\end{pmatrix} \\ H=\boldsymbol{h}\cdot \boldsymbol{S}=\frac{h_{0}}{2}\begin{pmatrix}
\cos\theta & \sin\theta\, e^{-i\phi}\\ \sin\theta\, e^{i\phi}&\cos\theta\end{pmatrix} \\ E_{\pm}=\pm \frac{h_{0}}{2} \hspace{1cm}\ket{\boldsymbol{h},+}=\begin{pmatrix}\cos(\theta/2)\,e^{-i\phi/2} \\ \sin(\theta/2)e^{i\phi/2} \end{pmatrix} \hspace{1cm}\ket{\boldsymbol{h},-}=\begin{pmatrix}\sin(\theta/2)\,e^{-i\phi/2} \\ \cos(\theta/2)e^{i\phi/2} \end{pmatrix} }$$
- The gradient in parameter space:
$$\nabla_{h}=\frac{1}{h_{0}}\left( \frac{\partial}{\partial\theta}\hat{\theta}+\frac{1}{\sin\theta}\frac{\partial}{\partial \phi}\hat{\phi} \right)$$
- This gives the _Berry potentials_:
$$\boldsymbol{A}_{\pm}=\pm \frac{\cot\theta}{2h_{0}} \hat{\phi}$$
- There are _singularities_, and is _not always well-behaved_

- The associated _Berry curvature_:
$$\boldsymbol{B}_{\pm}(\boldsymbol{H})=\nabla_{\boldsymbol{H}}\times \boldsymbol{A}_{\pm}=\mp \frac{\hat{\boldsymbol{n}}}{2h_{0}^{2}}$$
- This corresponds to a _magnetic monopole_ of charge $\mp 1/2$ at the _origin_
	- Also _gauge invariant_

- From this, for a _closed path_, the Berry phase is _half the solid angle $\Omega$ enclosed_:
$$\gamma_{\pm}(\mathcal{C})=\iint \boldsymbol{B}_{\pm}\cdot d\boldsymbol{S}=\mp \frac{\Omega}{2}$$

- When integrating over the _whole surface_, one gets $\mp 2\pi$
	- For a _spin_$-s$ particle, one gets $4\pi s$
	- This is from the _Chern theorem_
	- Indicates the space is _topologically non-trivial_
## Berry phase in crystalline systems
- The _energy bands_ in a 2D material live in $k-$space
- _Periodicity_ in $k_{x}$ and $k_{y}$ gives a _torus_

- Integrating the _Berry curvature_ over a band gives the _Chern number_, a _topological invariant_