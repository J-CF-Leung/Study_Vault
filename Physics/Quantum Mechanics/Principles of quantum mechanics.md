>[!Quote]
>"There is no general consensus as to what the fundamental principles of quantum physics are, how it should be taught, or what it really means"
>-David J. Griffiths
>
>"If you are not confused by quantum physics then you haven't really understood it."
>-Niels Bohr
>
>"I think I can safely say that nobody understand quantum mechanics"
>-Richard Feynman

- [x] Bosons and fermions 🔼 📅 2023-10-04 ✅ 2023-10-09
# Notation
- Generic vectors are denoted with _kets_ $\ket{V}$
- Operators have capital letters and hats $\hat{\Omega}$
- The _eigenvalues_ are denoted with the small version of the letter for the operator:
$$\hat{\Omega}\ket{\omega}=\omega\ket{\omega}$$

# The fundamental postulates 
- After many experiments proving the [[The failure of classical mechanics|inadequacy of classical mechanics]], many attempts were made to create a quantum theory
- Eventually, a set of _postulates_ were agreed upon
- These postulates assume _non-relativistic particles_

- __Postulate 1:__ In quantum mechanics, the state of a system is represented by the wave function, a state vector $\wv$ in [[Vectors and matrices in physics|complex vector space]]

- __Postulate 2:__ All _observables_ $\omega$ in quantum mechanics are represented by an _operator_ $\hat{\Omega}$ 

- __Postulate 3:__ Measurement of a variable corresponding to $\hat{\Omega}$ _always yields one of the eigenvalues $\omega$ with probability (density) $|\braket{\omega|\Psi}|^2$_, with the _subsequent state represented by normalised eigenvector_ $\ket{\omega}$. Values other than the eigenvalues are impossible.
	- In terms of [[Vectors and matrices in physics#Identity and projection operators|projection operator]] $\mathcal{P}_\omega=\ket{\omega}\bra{\omega}$, $P(\Omega=\omega) \propto \braket{\Psi|\mathcal{P}_\omega\Psi} = \braket{\Psi\mathcal{P}_\omega|\mathcal{P}_\omega\Psi}$
	- An important _consequence_ of this postulate is that $\hat{\Omega}$ is always _Hermitian_

- __Postulate 4:__ The state ket $\wv$ evolves in time according to [[#Time-evolution The Schrödinger equation|the Schrödinger equation]]

# The wave function

## Normalisation
- Each physical state is more precisely described as a _"ray" in the complex vector space_
	- Just normalised vectors do not form a complete vector space
- If $\wv$ is a _proper vector_, it is normalised ($\braket{\Psi|\Psi}$ = 1) to _normalise the probability distribution_
- There is _freedom to multiply_ the ket by a _phase factor_ $exp(i\theta)$ to make certain components real
- $\wv$ could be an _improper vector_, which can only be _normalised to a Delta function_
	- Example: Continuous _wave train/beam_

## Superposition
- The state vector $\wv$ is an _element of a vector space_
- Hence if $\wv$ and $\ket{\Psi'}$ both represent _possible states_, then all _linear combinations_ $\alpha\wv+\beta\ket{\Psi'}$ are _also possible states_
- When making measurements, the mixed state will (loosely speaking) _sometimes_ resemble $\wv$, and at other times resemble $\ket{\Psi'}$


## The wave function in different bases
- $\wv$ itself _only exists in Hilbert space_
- However, it can be _projected_ onto different bases, with the _components_ encoding information about the state
- The bases considered are those of _Hermitian operators_, representing _observables_
- These are _complete, orthonormal eigenbases_

### Position and momentum
- The most important ones are _position_ $\hat{X}$ and _momentum_ $\hat{P}$
- The latter is derived from the [[Vectors and matrices in physics#The k basis|k basis]]:
$$\displaylines{\hat{P}=\hbar\hat{K} \\ \hat{P}f(x)=-i\hbar\frac{df}{dx} \\ \braket{x|p}=\frac{1}{\sqrt{2\pi}}\exp(ipx/\hbar)}$$
- Position and momentum are the most commonly considered variables to describe particles:
$$\Psi(x,t)=\braket{x|\Psi(t)}\;\;\;\;\Phi(p,t)=\braket{p|\Psi(t)}$$
- $\Psi(x,t)$ is commonly referred to as the _position-space wave function_
- $\Phi(p,t)$ is commonly referred to as the _momentum-space wave function_

### Spectral decomposition
- As the eigenkets of any Hermitian operator _span the entire vector space_, any wave function can be written _in terms of eigenstates_, in a _spectral decomposition_:
$$\begin{aligned}\wv&=\sum_n\ket{q_n}\braket{q_n|\Psi}=\sum_nc_n\ket{q_n} \\ &= \int \ket{q_n}\braket{q_n|\Psi}\,dq = \int c(q)\, \ket{q} \,dq \end{aligned}$$

- The _information encoded by the components of the wave function_ is a _probability (density) for measurement_
	- See postulate 3
- Discrete spectrum: $P(Q=q_n)=|c_n|^2=|\braket{q_n|\Psi}|^2$
- Continuous spectrum: $P(q<Q<q+dq)=|c(q)|^2\,dq=|\braket{q|\Psi}|^2\,dq$

- As the wave function is _normalised_, the coefficients sum/integrate to one
$$\sum_n|c_n|^2=\int |c(q)|^2\,dq=1$$
### Converting between bases
- To convert to another basis, use the _completeness relation_:
$$I=\int\ket{q}\bra{q}\,dq$$
- Example: from position to momentum
$$\Phi(p,t)=\braket{p|\Psi}=\int\braket{p|x}\braket{x|\Psi}dx=\frac{1}{\sqrt{2\pi\hbar}}\int\exp(-ipx/\hbar)\Psi(x)\,dx$$
# Observables, operators and measurements

## Measurement and state vector collapse
- In _classical_ mechanics, _ideal measurements_ will _leave the object intact_
- In _quantum_ mechanics, _ideal measurements_ will _always cause a collapse of the wave function_
- A quantum measurement can be defined as _interaction with a classical object_

- Given an operator $\hat{\Omega}$ representing physical quantity $\omega$, the _spectral decomposition_ of the wave function is:
$$\wv=\sum_i\ket{\omega_i}\braket{\omega_i|\Psi}=\sum_i \hat{\mathcal{P}}_i\ket{\Psi}$$
- If the result of the measurement was $\omega$, the wave function _collapses_ into:
$$\wv\xrightarrow{\Omega\text{ measured, }\omega_i \text{ obtained}} \frac{\hat{\mathcal{P}}_i\wv}{\braket{\hat{\mathcal{P}}_i\Psi|\hat{\mathcal{P}}_i\Psi}^{1/2}}=\ket{\omega_i}$$
- The _only case_ where the wave function is _unaffected_ is if it is _already in the eigenstate_ $\ket{\omega_i}$
- The equality sign is _only applicable if the eigenvalue has no degeneracy_

- Any _subsequent measurement of $\omega$_ will continue to yield $\omega_i$ with probability of 1

- To test quantum theory, one must use a _quantum ensemble_ of particles in pre-determined, definite states as _wave functions collapse after measurement_

### Probabilities, expectation values and uncertainties
- Assume a _normalised_ wave function
- According to postulate 3, the _probability_ that a measurement of $\omega$ leads to $\omega_i$ is:
$$P(\omega_i)=|\braket{\omega_i|\Psi}|^2$$
- If the eigenvalue spectrum is _discrete_, this is the _probability_

- If the eigenvalue spectrum is _continuous_, this is the _probability density_
- The probability that the measured value $\omega_m$ lies in the _range_ from $\omega$ to $\omega+d\omega$ is:
$$P(\omega<\omega_m<\omega+d\omega)=|\braket{\omega|\Psi}|^2\,d\omega$$

- If the wave function is an _improper vector_, this is only a _relative_ probability
	- Example: _Reflection_ and _transmission_ amplitudes for a _particle beam_

- Given this, the _expectation value_ of a measurement is then:
$$\mean{\Omega}=\sum_iP(\omega_i)\omega_i=\sum_i\braket{\Psi|\omega_i}\omega_i\braket{\omega_i|\Psi}=\braket{\Psi|\hat{\Omega}|\Psi}$$
- The proof is analagous for _continuous spectra_

- This is an average over an _ensemble_ of particles all with wave function $\wv$
- If $\wv=\ket{\omega_i}$, then $\mean{\Omega}=\omega_i$
- The _eigenvalues and eigenvectors do not necessarily need to be known_, only the _matrix elements_ of $\hat{\Omega}$ in a particular basis, as well as $\Psi$ in that basis

- With this, the _variance_ of measuring $\omega$ over an ensemble is then:
$$\sigma_\omega^2=\mean{(\Omega-\mean{\Omega})^2}=\mean{\Omega^2}-\mean{\Omega}^2$$

### Degeneracy of eigenvalues
- If each eigenvalue $\omega$ has _degeneracy_ $g_i$, the spectral decomposition is:
$$\wv=\sum_i\sum_{n=1}^{g_i}c_{in}\ket{\omega_i^{(n)}}$$
- $\hat{\mathcal{P}}_i$ is then a _sum of outer products of the eigenbasis_:
$$\hat{\mathcal{P}}_i=\sum_{n=1}^{g_i}\ket{\omega_i^{(n)}}\bra{\omega_i^{(n)}}$$
- The wave function is then _collapsed into an eigenspace_ $\mathbb{V}_\omega$
$$\wv\xrightarrow{\Omega\text{ measured, }\omega \text{ obtained}} \frac{1}{\sqrt{\sum_n|c_{i n}|^2}}\sum_{n=1}^{g_i} c_{i n}\ket{\omega_i^{(n)}}$$
- If the initial state is _unknown_, the coefficients of this linear combination are also unknown

### Compatibility of multiple measurements
- For only one given variable $\omega$, one can _produce a state with a definite value_ of $\omega$ by performing a measurement and collapsing the wave function
	- The state is not definite if $\Omega$ is degenerate
- Consider two variables $\omega$ and $\lambda$, _measured one after the other_
	- In general, the final state will not always have a definite value for both
	- There will be a definite value of both if the eigenkets of $\Omega$ are also eigenkets of $\Lambda$
	- For the above to be true, a necessary condition is $[\Omega,\Lambda]=0$
- Compatibility:
	- If two operators _commute_, a complete set of simultaneous eigenkets exist, and the observables are _compatible_
	- If they can never commute, they are _incompatible_ (example: $x$ and $p$)

- If two observables are _incompatible_, since _no simultaneous eigenkets exist_, this introduces some _uncertainty_ when trying to measure the two variables
- _Position_ and _momentum_ are one such conjugate pair, hence _the classical notion of a path does not exist in quantum mechanics_
- This uncertainty in measurements of conjugate variables can be _quantified_ with the [[#Uncertainty principles|generalised uncertainty principle]]

### Measuring compatible observables
- If _neither_ operator is degenerate, only _one measurement_ collapses the wave function into a definite state, with $P(\omega,\lambda)=P(\lambda,\omega)$
- If _one_ of the operators is degenerate, $P(\omega,\lambda)=P(\lambda,\omega)$, but the wave functions after the measurements _depends on measurement order_
- If both operators are degenerate, a third compatible must be found to "nail down" the wave function
	- In general, a _complete set of commuting observables_ exists

## Constructing an operator
- Let there be a _classical dynamical variable_ $\omega(x,p)$, a _function_ of the _position_, and _conjugate momentum_ in the [[Analytical classical mechanics#Hamiltonian formulation|Hamiltonian formulation]]
- Then, its _quantum analogue_ is an operator $\hat{\Omega}(\hat{X},\hat{P})$
	- [[#Position and momentum]]
	- [[Vectors and matrices in physics#Functions of operators|Functions of operators]]

- Sometimes, there may be _ambiguities_ involving products such as $xp$
- In these cases, one can use a _symmetrised sum_ $(\hat{X}\hat{P}+\hat{P}\hat{X})/2$

- Sometimes, there _may be no classical analogue_
- Example: Spin
- In that case, some intuition may be used to determine commutation relations and other properties

### The Hamiltonian
- To construct the Hamiltonian, one starts from the _classical_ Hamiltonian $\Ham(x,p)$
- Then, one makes the _substitution_ $\hat{\Ham}(x\to\hat{X}, p\to\hat{P})$
- For example. the _1-dimensional harmonic oscillator_:
$$\Ham=\frac{p^2}{2m}+\frac{1}{2}m\omega^2x^2 \hspace{0.25cm} \longrightarrow\hspace{0.25cm} \hat{\Ham}=\frac{\hat{P}^2}{2m}+\frac{1}{2}m\omega^2\hat{X}^2$$

## Uncertainty principles
- As the measured values of observables is now _probabilistic_, the distributions will come with some _variance_
- There are certain _incompatible/conjugate variables_ where the operators _do not commute_

- Since _no simultaneous eigenstate exists_, one _cannot get precise values of both variables_, and the _product of variances_ have some _minimum, non-zero value_
- This is the _Heisenberg's uncertainty principle_, at first applied to _position and momentum_:
$$\sigma_x\sigma_p\geq \frac{\hbar}{2}$$
- This can often be used to _estimate ground state energies_ by setting _minimum uncertainty_, then _minimise energy_

- Variance $\sigma^2 = \left<(\hat{A}-a)^2\right>$ 
- The _generalised uncertainty principle_:
$$\sigma_A^2\sigma_B^2\geq\left(\frac{1}{2i}\left<[\hat{A},\hat{B}]\right>\right)^2$$
	- Proof: Cauchy-Schwarz inequality with $\ket{(\hat{A}-a)\Psi}$ and $\ket{(\hat{B}-b)\Psi}$
		- $|\braket{f|g}|^2 = Re(\braket{f|g})^2+Im(\braket{f|g})^2$ 

### The minimum uncertainty wave packet
- From the proof of the inequality, for a packet with _minimal uncertainty in position and momentum_, it must satisfy:
$$\left(\hat{P}-\mean{\hat{P}}\right)\ket{\Psi}=i|c|\left(\hat{X}-\mean{\hat{X}}\right)\wv$$
- Defining:
$$\displaylines{\Delta=\hbar/|c| \\ \mean{\hat{X}}=a \hspace{1cm}\mean{\hat{P}}=p_0}$$
- Thus, the _minimum-uncertainty wave packet_ in position space is:
$$\psi(x)=A\exp\left[\frac{ip_0}{\hbar}(x-a)\right]\exp\left[-\frac{(x-a)^2}{2\Delta^2}\right]$$
- This is a _Gaussian packet_
- Example occurence: the _ground state_ of the [[Quantum Harmonic Oscillator]]

# Generalising to more dimensions
- Consider a system with $N>1$ _degrees of freedom_

- Corresponding to $N$ Cartesian coordinates $x_1,x_2\dots x_N$ describing the _classical_ system, there exist $N$ _mutually commuting position operators_ $\hat{X}_1,\dots,\hat{X}_N$
- There exists a _simultaneous eigenbasis_ $\ket{x_1x_2\dots x_N}$ in a [[Vectors and matrices in physics#Direct product spaces|direct product space]]
- Likewise, there exist $N$ _mutually commuting momentum operators_ $\hat{P}_1,\dots,\hat{P}_N$

- Projected onto the position basis, the wave function and the action of the operators are:
$$\displaylines{\wv\xrightarrow{x\text{ basis}}\braket{x_1x_2\dots x_N|\Psi}=\Psi(x_1,x_2,\dots,x_N) \\ \hat{X}_i\wv\xrightarrow{x\text{ basis}}\braket{x_1x_2\dots x_N|\hat{X}_i\Psi}=x_i\Psi(x_1,x_2,\dots,x_N) \\ \hat{P}_i\wv\xrightarrow{x\text{ basis}}\braket{x_1x_2\dots x_N|\hat{P}_i|\Psi}=-i\hbar\pd{}{x_i}\Psi(x_1,x_2,\dots,x_N)}$$
- One can write the operators as _vectors_:
$$\hat{\bm{r}}=(\hat{x}_1,\hat{x}_2,\dots,\hat{x}_N) \hspace{1.5cm}\hat{\bm{p}}=(\hat{p}_1,\hat{p}_2,\dots,\hat{p}_N)$$
- Relationship between basis:
$$\displaylines{\braket{\hat{\bm{r}}|\hat{\bm{p}}|\hat{\bm{r}}'}=-i\hbar\delta'(\bm{r}-\bm{r}')=-i\hbar\delta(\bm{r}-\bm{r}')\nabla_x \\ \braket{\hat{\bm{p}}|\hat{\bm{r}}|\hat{\bm{p}}'}=i\hbar\delta'(\bm{p}-\bm{p}')=i\hbar\delta(\bm{p}-\bm{p}')\nabla_p}$$

- Then, dynamical variables $\omega(x_i,p_j)$ are represented by operators $\hat{\Omega}(\hat{X}_i,\hat{P}_j)$
- The _commutation relations_ remain the same:
$$[\hat{x}_i,\hat{x}_j]=[\hat{p}_i,\hat{p}_j]=0\hspace{1.5cm}[\hat{x}_i,\hat{p}_j]=i\hbar\delta_{ij}$$

- The other postulates remain the same
- The probability that one finds the particle in range $(x_1,x_2,\dots,x_N)$ and $(x_1+dx_1,x_2+dx_2,\dots,x_N+dx_N)$ is:
$$|\Psi(x_1,x_2,\dots,x_N)|^2\,dx_1dx_2\dots dx_N$$

- One can also perform _changes of variable_ once the operator is written down

- Example: the _3-dimensional harmonic oscillator_
$$\hat{\Ham}=\frac{\hat{P}_x^2+\hat{P}_y^2+\hat{P}_z^2}{2m}+\frac{1}{2} m\omega^2(\hat{X}^2+\hat{Y}^2+\hat{Z}^2)$$
- In the coordinate basis, this is written as:
$$\begin{aligned}\hat{\Ham}&\xrightarrow{x\text{ basis}}-\frac{\hbar^2}{2m}\left(\pd{^2}{x^2}+\pd{^2}{y^2}+\pd{^2}{z^2}\right)+\frac{1}{2}m\omega^2(x^2+y^2+z^2) \\ &\equiv-\frac{\hbar^2}{2m}\nabla^2+\frac{1}{2}m\omega^2r^2 \\ &\equiv-\frac{\hbar^2}{2m}\left(\frac{1}{r^2}\pd{}{r}\left(r^2\pd{}{r}\right) + \frac{1}{r^2\sin\theta}\pd{}{\theta}\left(\sin\theta\pd{}{\theta} \right) + \frac{1}{r^2\sin^2\theta}\pd{^2}{\phi^2}\right)+\frac{1}{2}m\omega^2r^2 \end{aligned}$$
- There is _not necessarily a procedure for quantisation from non-Cartesian coordinates_

# Useful commutation relations
- Using the [[Vectors and matrices in physics#Commutation relations involving functions|commutation relations involving functions]]:
$$\displaylines{[\hat{x},\hat{p}^l]=i\hbar l\hat{p}^{l-1}=i\hbar\pd{\hat{p}^l}{\hat{p}} \\ [\hat{x},F(\hat{x},\hat{p})]=i\hbar\pd{F}{\hat{p}} \\ [\hat{p},F(\hat{x},\hat{p})]=-i\hbar\pd{F}{\hat{x}}}$$
- Example:
$$[\hat{x},\hat{p}\hat{x}\hat{p}]=i\hbar(\hat{x}\hat{p}+\hat{p}\hat{x})$$
$$[\hat{\bm{r}},\hat{\bm{p}}^2]=2i\hbar\hat{\bm{p}}$$

- If $[\hat{A},\hat{B}]=0$, then $[\hat{A}^m,\hat{B}^n]=0$
- If $[\hat{C},\hat{A}]=[\hat{C},\hat{B}]=0$, even if $[\hat{A},\hat{B}]\neq0$, $[\hat{C},\hat{AB}]=0$


# Time-evolution: The Schrödinger equation

## The time-evolution operator
- Let the state ket at time $t$ be:
$$\ket{\Psi(t)}=\teo(t-t_0)\ket{\Psi(t_0)}$$
	- $\teo$ is the _time-evolution operator_, also known as the _propagator_
- The time-evolution operator must fulfill the following properties:
	- Composition: $\teo(t_2-t_0)=\teo(t_2-t_1)\teo(t_1-t_0)$
	- [[Vectors and matrices in physics#Hermitian and unitary matrices|Unitarity]]/probability conservation: $\braket{\Psi|\Psi}=\braket{\Psi_0|\Psi_0}=1$ -> $\teo^\dagger\teo=1$
- Considering the _infinitesimal_ time-evolution operator $\teo(t_0+dt,t_0)$:
	- It satisfies the limit $\lim_{dt\to 0}\teo(t_0+dt,t_0)=1$
- These properties are satisfied by $\teo(t_0+dt,t_0)=1-i\Omega dt$
	- $\Omega$ has to be a _Hermitian operator_ to satisfy unitarity
	- With the Planck-Einstein equation $E=\hbar\omega$, and the fact that the _Hamiltonian is the generator of time-evolution_, $\Omega$ is related to the Hamiltonian by: $\Omega=\Ham/\hbar$
	- Minus sign allows _approximation to classical limit_
- With this, the infinitesimal time evolution operator is:
$$\teo(t_0+dt,t_0)=1-\frac{i\Ham}{\hbar}dt$$
- Using the composition property and writing this as a differential equation:
$$i\hbar\pd{\teo}{t}=\Ham\teo$$
	- This is the _Schrödinger equation for the time-evolution operator_


## Interpreting time evolution
- The time-evolution operator is a _unitary operator_, which can be understood as a _rotation operator in Hilbert space_
- This is necessary for the _norm of the state ket to remain constant_
- As a result, _all inner products between state bras and kets $\braket{\beta|\alpha}$ also remain constant_(this also gives rise to the different [[#The Schrödinger and Heisenberg pictures|pictures of quantum mechanics]])
- For the time evolution of the wave function itself, multiply by the initial state ket on both sides:
$$i\hbar\frac{\partial}{\partial t}\ket{\Psi}=\Ham\wv$$

## The Schrödinger wave equation
- The Schrödinger wave equation is the _Schrödinger equation for the wave function_, but projected onto the position basis:
$$\begin{aligned}i\hbar\frac{\partial}{\partial t}\Psi(x,t)&= \braket{x|\Ham|\Psi} \\ &=-\frac{\hbar^2}{2m}\nabla^2\Psi +V\Psi\end{aligned}$$
- The second equality only applies when the _Hamiltonian is in the form $T+V$_

- The Schrödinger wave equation is a _dispersive wave equation_
	- [[Waves|Wave equations]]

# How to actually solve the Schrödinger equation

## Time-independent Hamiltonians and stationary states
- For a _time-independent Hamiltonian_, the Schrödinger equation for the time-evolution operator is solved by:
$$\teo = \exp\left(-\frac{i\Ham t}{\hbar}\right)$$
- One can express this in terms of the _Hamiltonian's eigenkets and eigenvalues_:
$$\teo=\sum_n\ket{E_n}\bra{E_n}\exp\left(-\frac{iE_nt}{\hbar}\right)$$
	- If there is _degeneracy_, an extra label $\alpha$ should be added to the eigenkets and summed over
	- The sum can be replaced by an _integral for an continuous spectrum_
	- The matrix elements of $\teo$ in the $x$-basis gives the [[Path integrals in quantum mechanics|propagator]]
- Thus, the state ket becomes:
$$\ket{\Psi(t)} = \teo\ket{\Psi(0)}=\sum_n\braket{E_n|\Psi(0)}\exp\left(-\frac{iE_nt}{\hbar}\right)\ket{E_n}=\sum_nc_{E,n}\exp\left(-\frac{iE_nt}{\hbar}\right)\ket{E_n}$$
- The _normal modes_ of the equation, $\ket{E_n(t)}=\exp(-iE_nt/\hbar)\ket{E_n}$, are known as _stationary states_, as the _probability distribution for ANY variable remains constant_:
$$|\braket{q|E_n(t)}|^2=|\braket{q|E_n}\exp(-iE_nt/\hbar)|^2=|\braket{q|E_n}|^2$$
- Each eigenstate _evolves on its own_, and the wave function _remains a linear combination with the same coefficients_

- The eigenvalue equation for the energy eigenkets is also known as the _time-independent  Schrödinger equation_:
$$\Ham\ket{E_n}=E_n\ket{E_n}$$
- Projected onto the $x$ basis with $\Ham=T+V$:
$$-\frac{\hbar^2}{2m}\nabla^2\psi_n(x)+V\psi_n(x)=E_n\psi_n(x)$$
- Solving this thing: [[1D time-independent Hamiltonians]], [[3D time-independent Hamiltonians]]

## Time-dependent Hamiltonians: various methods

# Transition amplitude
- Given two eigenkets, $\ket{b}$ at time $t$ and $\ket{a}$ at time $t=0$, the _transition amplitude_ between them is defined as:
$$\braket{b|\teo(t,0)|a}$$
- This describes the probability amplitude of the system "transitioning" from eigenstate $\ket{a}$ at $t=0$ to eigenstate $\ket{b}$ at time $t$
- This quantity is particularly useful in defining the [[Path integrals in quantum mechanics|path integral formulation]]

# Probability flow
- The total probability of finding a particle anywhere in the universe is conserved:
$$\braket{\Psi(0)|\Psi(0)}=\braket{\Psi(t)|\Psi(t)}=\int_\text{all space}\braket{\Psi(t)|\bm{r}}\braket{\bm{r}|\Psi(t)}\,d^3\bm{r}=\int_\text{all space}P(\bm{r},t)\,d^3\bm{r}$$
- Consider the time derivative of $P(\bm{r},t)$, and using the [[Principles of quantum mechanics#The Schrödinger wave equation|Schrödinger wave equation]]:
$$\begin{aligned}\pd{P}{t}&=\pd{}{t}[\Psi^*(x,t)\Psi(x,t)] \\
&= \frac{i\hbar}{2m}\left[\Psi^*\nabla^2\Psi-\Psi\nabla^2\Psi^*\right] \\ &=  \frac{i\hbar}{2m} \nabla\cdot\left[\Psi^*\nabla\Psi-\Psi\nabla\Psi^*\right] \\\pd{P}{t}&=-\nabla\cdot\bm{J}\end{aligned}$$
- Here, $\bm{J}$ is the _probability current density_
- This is the continuity equation for the probability of finding a particle
	- For an ensemble of $N$ particles, $N\bm{J}\cdot d\bm{S}$ particles per unit time flow past an area $d\bm{S}$

- For a _travelling plane wave_:
$$\displaylines{\psi=A\exp[i(kx-\omega t)] \\ J=\frac{\hbar k}{m}|A|^2}$$
- Here, $\hbar k/m$ is the _classical speed_

- If $k$ is _imaginary_ (i.e. an evanescent wave), $J=0$

# The Schrödinger and Heisenberg pictures
- So far, we have been working with the _Schrödinger picture_, where the _state kets evolve with time, with the operators remaining constant_

- Consider the time-evolution of inner product $\braket{\beta|\Omega|\alpha}$:
$$\braket{\beta|\Omega|\alpha} \rightarrow \braket{\teo\beta|\Omega|\alpha}=\braket{\beta|\teo^\dagger\Omega\teo|\alpha}$$
- This can be interpreted as the state ket remains unchanged, with the operator representing the observable evolving with time
- This is known as the _Heisenberg picture_
- It applies not only to time-evolution, but to _any unitary transformation_, such as translation
- It is a "closer" approach to classical mechanics, which has no state vectors, and _observables that vary with time_
## State kets and observables in the Heisenberg picture
- The Heisenberg picture observable $A^{(H)}$ is defined by:
$$A^{(H)}(t)=\teo^\dagger(t) A^{(S)}\teo(t)$$
	- The Heisenberg and Schrödinger pictures coincide at $t=0$
- _State kets_ in the Heisenberg picture are _frozen_:
$$\ket{\Psi,t_0=0,t}_H=\ket{\Psi,t_0=0}$$
	- In the Schrödinger picture, $\ket{\Psi,t_0=0,t}_S=\teo(t)\ket{\Psi,t_0}$
- The _expectation value is the same across both pictures_
$${}_{S}\braket{\Psi(t)|A^{(S)}|\Psi(t)}_S=\braket{\Psi(t_0)|A^{(H)}|\Psi(t_0)}$$
## The Heisenberg equation of motion
- Expressing the Heisenberg operator in terms of the Schrödinger operator, then taking the total time derivative, one gets the _Heisenberg equation of motion_:
$$\frac{dA^{(H)}}{dt}=\frac{1}{i\hbar}[A^{(H)},\Ham^{(H)}]+\pd{A^{(H)}}{t}$$
- The _Heisenberg Hamiltonian_ $\Ham^{(H)}$ is defined the same as other $(H)$ operators
- For a _time-independent Hamiltonian, $[\Ham,\teo]$ commute, and $\Ham^{(S)}=\Ham^{(H)}$_
- This echoes the equation for _rate of change of variables in classical mechanics_:
$$\frac{dA}{dt}=\PB{A}{\Ham}+\pd{A}{t}$$
	- where $\{,\}$ is the [[Analytical classical mechanics|Poisson bracket]]
- This further establishes that the commutator is a "quantum version" of the PB
## Base kets in the Heisenberg picture
- In the _Schrödinger_ picture, the _operators and base kets are stationary_
- At $t=0$, the two pictures coincide:
$$A^{(H)}(0)\,\ket{a'} = a'\ket{a'}$$
- Operating on both sides with $\teo^\dagger$, the time-evolution for $\ket{a'}_H$ is found:
$$\teo^\dagger A^{(H)}(0)\,\teo(\teo^\dagger\ket{a'})=A^{(H)}(t)\,(\teo^\dagger\ket{a'})=a'(\teo^\dagger\ket{a'})=a'\ket{a',t}_H$$
- The base kets in the Heisenberg picture _rotate oppositely_ compared to Schrödinger's state kets
- The eigenvalues stay constant, as expected
- $\teo^{(H)}=\teo^\dagger\teo^{(S)}\teo$ can be recovered by expanding the former in terms of $\ket{a',t}_H$
- Expansion coefficients remain the same:
$$c_{a'}(t)={}_{H}\braket{a',t|\alpha}=\braket{a'|\alpha,t}_S=\braket{a'(t=0)|\teo|\alpha(t=0)}$$
- _Transition amplitudes_ between two eigenstates are also the same within the two pictures, with the same reasoning as above

# Expectation values and the classical limit
- Due to the probabilistic nature of quantum mechanics, one _cannot define a time derivative of an observable quantity_
- However, one can talk about the _time evolution of the expectation value_

## Ehrenfest's Theorem
- By applying the time derivative to $\mean{A}=\braket{\psi|\hat{A}|\psi}$:
$$\frac{d}{dt}\mean{A}=\mean{\pd{A}{t}}+\frac{1}{i\hbar}\mean{[\hat{A},\hat{\Ham}]}$$
- This is _analagous_ to the time evolution of a quantity using [[Analytical classical mechanics#Poisson brackets|Poisson brackets]]

- It is also most apparent with respect to the [[#The Heisenberg equation of motion|Heisenberg picture]], where it is the time-averaged version of the _Heisenberg equation of motion_

- Assuming $\hat{A}$ does not explicitly depend on time:
	- If $\hat{A}$ commutes with $\hat{H}$ (they _share eigenstates_), then $\mean{A}$ is _always a constant of motion_
	- If the system is in an _energy eigenstate_, then _expectation values of all observables are independent in time_

- Let there be a time-independent Hamiltonian, such that the wave function is:
$$\wv=\sum_nc_n\exp\left(-\frac{iE_nt}{\hbar}\right)\ket{E_n} \hspace{0.5cm}\text{ where } c_n=\braket{E_n|\Psi(0)}$$
- From this, the time evolution can be written as:
$$\mean{A}=\sum_{m,n}c_m^*c_n\exp\left(-\frac{i(E_n-E_m)t}{\hbar}\right)A_{mn}$$
- Here, $A_{mn}$ is the _matrix element of $\hat{A}$ in the energy eigenbasis_:
$$A_{mn}\equiv\braket{E_m|\hat{A}|E_n}$$

## Important cases
- Using the [[#Useful commutation relations|commutation relations involving functions]]:
$$\displaylines{\frac{d\mean{x}}{dt}=\frac{1}{i\hbar}\mean{[\hat{x},\hat{\Ham}]}=\frac{\mean{p}}{m} \\ \frac{d\mean{p}}{dt}=-\mean{\pd{V}{x}}}$$
- These are a _direct analogues of the classical case_
- There is an important distinction to make:
$$\mean{F(\hat{x})}\neq F(\mean{x})$$
- The equality _holds approximately for small uncertainties relative to mean_

- So, when the _uncertaintiers are small relative to the scale of the system_, then the behaviour of the system _approaches the classical case_
- This is another manifestation of the _correspondence principle_

## Energy-time uncertainty principle
- Let there be some _arbitrary physical quantity_ $Q$
- From Ehrenfest's Theorem:
$$\frac{d\mean{Q}}{dt}=\frac{1}{i\hbar}\mean{[\hat{Q},\hat{H}]}$$
- From the [[#Uncertainty|generalised uncertainty principle]]:
$$\displaylines{\Delta E\Delta t\geq\frac{\hbar}{2} \\ \Delta t\equiv \frac{\Delta Q}{|d\mean{Q}/dt|}}$$
- $\Delta t$ is _the time taken for expectation value to change by the size of the uncertainty_

- If $\Delta E$ is _small_, then it takes _a long time for physical quantities to change_
- If it is a _stationary state_, then _no expectation values will change_

# Multiple degrees of freedom
- Much of the discussion above was dedicated to one degree of freedom, i.e. _one particle in one dimension_

## Two particles in one dimension
- Consider two particles described _classically_ by $(x_1,p_1)$ and $(x_2,p_2)$
- When quantising the system, establish operators $X_1$, $X_2$, $P_1$, $P_2$ such that they obey the _canonical commutation relations_:
$$\displaylines{[\hat{X}_i,\hat{P}_j]=i\hbar\delta_{ij}\hspace{1cm}\text{ for }i,j=1,2 \\ [\hat{X}_i,\hat{X}_j]=[\hat{P}_i,\hat{P}_j]=0}$$
- In this case, the coordinate basis must be a _simultaneous eigenbasis_ for $x_1$ and $x_2$, normalised using a _two-dimensional Dirac Delta_:
$$\displaylines{\hat{X}_1\ket{x_1x_2}=x_1\ket{x_1x_2} \\ \hat{X}_2\ket{x_1x_2}=x_2\ket{x_1x_2} \\ \braket{x_1'x_2'|x_1x_2}=\delta(x_1-x_1')\delta(x_2-x_2')}$$
- In the coordinate basis:
$$\displaylines{\wv\xrightarrow{x\text{ basis}}\braket{x_1x_2|\Psi}=\Psi(x_1,x_2) \\ \hat{X}_i\xrightarrow{x\text{ basis}} x_i \\ \hat{P}_i\xrightarrow{x\text{ basis}} -i\hbar\pd{}{x_i}}$$
- In general, the _probability density_ that particle 1 is near $x_1$, _and_ particle 2 is near $x_2$ is:
$$P(x_1,x_2)=|\braket{x_1x_2|\Psi}|^2$$
- The wave function would then be normalised as:
$$\braket{\Psi|\Psi}=\int |\braket{x_1x_2|\Psi}|^2\,dx_1\,dx_2=1$$

- Aside from this coordinate basis, one can also define a _momentum basis_ with simultaneous eigenkets $\ket{p_1p_2}$
- In _general_, one can define simultaneous eigenkets $\ket{\omega_1\omega_2}$ for _any two commuting operators_ $\Omega_1(X_1,P_1)$ and $\Omega_2(X_2,P_2)$
	- Any function of $X_1,P_1$ must commute with any function of $X_2,P_2$

- The operators still act normally:
$$\hat{T}_\text{CM}=\frac{\hat{P}_\text{CM}^2}{2M}=\frac{\hat{P}_1^2+\hat{P}_2^2+2\hat{P}_1\hat{P}_2}{2(m_1+m_2)}$$

- Denote the Hilbert space _spanned by the simultaneous eigenkets_ as $\mathbb{V}_{1\otimes2}$

- The _simultaneous eigenbasis_ can be established for _any physical quantity_:
$$\wv=\sum_{\omega_1}\sum_{\omega_2}C_{\omega_1,\omega_2}\ket{\omega_1\omega_2}$$
### The direct product space
- The eigenkets _for each particle_ span their _own Hilbert space_
	- The eigenbasis $\ket{x_1}$ spans the space $\mathbb{V}_1$, likewise for particle 2
	- For _any physical quantity_, not just position
- The corresponding _operators for each particle_ act on _their own vector spaces_

- The _two-particle Hilbert space_ can be derived from the [[Vectors and matrices in physics#Direct product spaces|direct product space]] $\mathbb{V}_1\otimes\mathbb{V}_2$
- The _operators_ in this space are _direct products of operators in the original spaces_:
$$\displaylines{\hat{X}_1^{(1)\otimes(2)}\ket{x_1x_2}=\hat{X}_1^{(1)\otimes(2)}(\ket{x_1}\otimes\ket{x_2})=\ket{\hat{X}_1^{(1)}x_1}\otimes\ket{\hat{I}^{(2)}x_2} \\\hat{X}_1^{(1)\otimes(2)}=\hat{X}_1^{(1)}\otimes \hat{I}^{(2)}\\ (\hat{\Gamma}_1^{(1)}\otimes\hat{\Lambda}_2^{(2)})(\ket{\omega_1}\otimes\ket{\omega_2})=\ket{\hat{\Gamma}_1^{(1)}\omega_1}\otimes\ket{\hat{\Lambda}_2^{(2)}\omega_2}}$$

- One can prove the following properties:
	- Operators on _different particles_ always _commute_: $\left[\Omega_1^{(1)}\otimes I^{(2)},I^{(1)}\otimes\Lambda_2^{(2)}\right]$
	- $\left(\Omega_1^{(1)}\otimes\Gamma_2^{(2)}\right)\left(\theta_1^{(1)}\otimes\Lambda_2^{(2)}\right)=\left(\Omega\theta\right)_1^{(1)}\otimes\left(\Gamma\Lambda\right)_2^{(2)}$
	- If $\left[\Omega_1^{(1)},\Lambda_1^{(1)}\right]=\Gamma_1^{(1)}$, then $\left[\Omega_1^{(1)\otimes(2)},\Lambda_1^{(1)\otimes(2)}\right]=\Gamma_1^{(1)}\otimes I_2^{(2)}$  
	- $\left(\Omega_1^{(1)\otimes(2)}+\Omega_2^{(1)\otimes(2)}\right)^2 = (\Omega_1^2)^{(1)}\otimes I^{(2)} + I^{(1)}\otimes(\Omega_2^2)^{(2)}+2\Omega_1^{(1)}\otimes\Omega_2^{(2)}$

- From this, one regains the commutation relations from [[#Two particles in one dimension|above]]
### Time-evolution of two particles
- The _state vector_ $\wv$ in the vector space $\mathbb{V}_{1\otimes2}$ evolves in time according to:
$$i\hbar\ket{\dot{\Psi}}=\left[\frac{\hat{P}_1^2}{2m_1}+\frac{\hat{P}_2^2}{2m_2}+\hat{V}(\hat{X}_1,\hat{X}_2)\right]\wv=\hat{\Ham}\wv$$
#### Separable Hamiltonians
- In the case where the two particles _do not interact with each other_ but experience _independent potentials_ (which are not necessarily identical):
$$\Ham=\frac{P_1^2}{2m_1}+V_1(X_1)+\frac{P_2^2}{2m_2}+V_2(X_2)=\Ham_1+\Ham_2$$

- As in _classical mechanics_, this means the two particles _evolve independently of each other_, hence the energies are _separately conserved_:
$$E=E_1+E_2$$
- The _time-independent_ equation becomes:
$$[\Ham_1(X_1,P_1)+\Ham_2(X_2,P_2)]\ket{E}=E\ket{E}$$
- As the two Hamiltonians _commute_, there are _simultaneous eigenstates_, which are formed from the _direct product_ between the eigenstates of the _single-particle_ Hamiltonians
	- $\ket{E}$ is a _basis vector_ for $\mathbb{V}_{1\otimes2}$ if the energy eigenstates are used instead of position
$$\displaylines{\ket{E}=\ket{E_1}\otimes\ket{E_2} \\ \Ham_1^{(1)}\ket{E_1}=E_1\ket{E_1} \hspace{1.5cm} \Ham_2^{(2)}\ket{E_2}=E_2\ket{E_2}}$$
- In this state, particle 1 is in _eigenstate_ $E_1$ and similarly for particle 2:
$$\Ham\ket{E}=(\Ham_1+\Ham_2)\ket{E}=(E_1+E_2)\ket{E}$$
- For a _stationary state_:
$$\wv=\ket{E}\exp(-iEt/\hbar)=\ket{E_1}\exp(-iE_1t/\hbar)\otimes\ket{E_2}\exp(-iE_2t/\hbar)$$

##### In the coordinate basis
- _Projecting_ the time-independent equation into the _coordinate basis_ $\ket{x_1x_2}=\ket{x_1}\otimes\ket{x_2}$:
$$\displaylines{\left[-\frac{\hbar^2}{2m_1}\pd{^2}{x_1^2}+V_1(x_1)-\frac{\hbar^2}{2m_2}\pd{^2}{x_2^2}+V_2(x_2)\right]\psi_E(x_1,x_2)=E\,\psi_E(x_1,x_2) \\ \psi_E(x_1,x_2)=\braket{x_1x_2|E}}$$
- Use the method of [[Partial differential equations#Separation of variables|separation of variables]] (substitute the separable solution then divide the equation by $\psi_E$)
$$\displaylines{\psi_E(x_1,x_2)=\psi_{E_1}(x_1)\psi_{E_2}(x_2) \\ \begin{aligned}\frac{1}{\psi_{E_1}}\left[-\frac{\hbar^2}{2m_1}\pd{^2}{x_1^2}+V_1(x_1)\right]\psi_{E_1}(x_1)&=E_1 \\ \frac{1}{\psi_{E_2}}\left[-\frac{\hbar^2}{2m_2}\pd{^2}{x_2^2}+V_2(x_2)\right]\psi_{E_2}(x_2)&=E_2 \\E_1+E_2&=E\end{aligned}}$$
- From this, one gets:
$$\braket{x_1x_2|\Psi_E}=\Psi_E(x_1,x_2,t)=\psi_{E_1}\exp(-iE_1t/\hbar)\,\psi_{E_2}\exp(-iE_2t/\hbar)$$
#### Two interacting particles
- Consider the _general problem_ where:
$$\displaylines{\Ham=\frac{P_1^2}{2m_1}+\frac{P_2^2}{2m_2}+V(x_1,x_2) \\ V(x_1,x_2)\neq V_1(x_1)+V_2(x_2)}$$
- _Generally_, this _cannot be reduced_ to two independent single-particle problems

- However, consider the case where there is _no external potential_, only an _interaction potential_:
$$V(x_1,x_2)=V(x_1-x_2)$$
- In order to make this Hamiltonian _separable_, use the same transformation of variables as in the [[Analytical classical mechanics#The two-body problem|classical two-body problem]]:
$$\displaylines{x_\text{CM}=\frac{m_1x_1+m_2x_2}{m_1+m_2} \hspace{1.5cm} p_\text{CM}=M\dot{x}_\text{CM}=m_1\dot{x}_1+m_2\dot{x}_2\\ x=x_1-x_2 \hspace{1.5cm} p=\mu\dot{x}\equiv\frac{m_1m_2}{m_1+m_2}\dot{x} \\ \Ham=\Ham_\text{CM}+\Ham_\text{rel}=\frac{p_\text{CM}^2}{2M}+\frac{p^2}{2\mu}+V(x)}$$
- The system is effectively a _free particle_ of mass $M$, at $x_\text{CM}$ with $p_\text{CM}$, as well as a particle with _reduced mass_ $\mu$, at $x$, moving under the influence of $V(x)$

- The _new quantisation conditions_, with _all other commutators zero_:
$$[X_\text{CM},P_\text{CM}]=[X,P]=i\hbar$$
- Following similar steps as above:
$$\displaylines{\Ham=\frac{P_\text{CM}^2}{2M}+\frac{P^2}{2\mu}+V(X) \\ \psi_E(x_\text{CM},x)=\left[\frac{1}{\sqrt{2\pi\hbar}}\exp(ip_\text{CM}x_\text{CM}/\hbar)\right]\psi_{E_\text{rel}}(x) \\E=\frac{p_\text{CM}^2}{2M}+E_\text{rel}}$$
- If one transforms to a frame where $p_\text{CM}=0$, then the free particle wave function becomes _constant_
- All the dynamics is _within_ $\psi_\text{rel}(x)$
## More particles in more dimensions
- In _one dimension_, for _more than two non-interacting_ particles, the technique of _separation_ still applies
- For _interacting particles_, one _generally cannot_ use the technique of centre-of-mass coordinates
	- Exception: _harmonic oscillator_ Hamiltonians using _normal coordinates_

- For _one particle in two dimensions_, one typically refers to the degrees of freedom as $x$ and $y$, with position eigenkets $\ket{xy}$ and momentum eigenkets $\ket{p_xp_y}$

- In _three dimensions_, the _position eigenket_ can be written as $\ket{\bm{r}}$, and the _orthonormality_ relation becomes:
$$\braket{\bm{r}|\bm{r}'}=\braket{xyz|x'y'z'}=\delta(x-x')\delta(y-y')\delta(z-z')=\delta^3(\bm{r}-\bm{r}')$$
- When there are _more particles_, an extra label will be used
	- A _two-particle momentum eigenstate in 3 dimensions_ is $\ket{\bm{p}_1\bm{p}_2}$

## Identical particles
- If two particles are _identical_, it means it is _impossible to observe a difference in intrinsic properties_ (mass, charge, spin, etc.)
- In _classical mechanics_ it is always possible to _label_ identical particles by _following their non-identical past trajectories_, such that _exchanging_ the particles at any particular time creates a _non-equivalent situation_
- In _quantum mechanics_, as particles _do not have continuous trajectories_, a _particle exchange_ at _any time_ must _not change the physical situation_

### Allowed state vectors for two identical particles
- Suppose two _distinguishable particles_, $1$ and $2$, are found at $x_1=a$ and $x_2=b$ (where $a\neq b$) denote the state as $\wv=\ket{x_1=a, x_2=b}=\ket{ab}$ 
- When the particles are _exchanged_, $\wv=\ket{ba}$
- $\wv$ is described by an _ordered pair_ of numbers

- If the observation is repeated with _identical particles_, as the configuration is _physically equivalent_:
$$\ket{\Psi(a,b)}=\pm\ket{\Psi(b,a)}$$
- Proof:
	- Let $\ket{\Psi(a,b)}=\pm\ket{\Psi(b,a)}$ where $\alpha\in\mathbb{C}$
	- As $a$ and $b$ are an _unordered pair_, one can only define a _unique sum_ $a+b$
	- Therefore, the state vector lies in an _eigenspace_ spanned by $\ket{ab}$ and $\ket{ba}$
	- $\wv=\beta\ket{ab}+\gamma\ket{ba}$
	- Substituting this into the above relation, $\beta=\alpha\gamma$ and $\gamma=\alpha\beta$
	- Hence, $\alpha=\pm1$

- One can then construst the (unnormalised) _allowed state vectors_, which can be _symmetric_ $(\alpha=1)$ or _antisymmetric_ $(\alpha=-1)$:
$$\displaylines{\ket{ab, S}=\ket{ab}+\ket{ba} \\ \ket{ab,A}=\ket{ab}-\ket{ba}}$$
- _Labels_ of $x_1$ and $x_2$ become _physically irrelevant_

- This process applies to _any variable_ $\Omega$
- If the values $\omega_1$ and $\omega_2$ are mentioned, the allowed state vectors are $\ket{\omega_1\omega_2, S}$ and $\ket{\omega_1\omega_2,A}$
	- If $\Omega$ is _degenerate_, let $\omega$ represent the eigenvalues of a _complete set of commuting operators_

### Bosons and Fermions
- For a _given species of particle_, it must _only collapse into either symmetric or antisymmetric states_
	- If the contrary were true, the Hilbert space of possible states contains both $S$ and $A$ vectors, along with its _linear combinations_ which are not physically allowed

- Particles _always in symmetric states_ are known as __bosons__
	- Particle _exchange_ leaves the wave function _completely unchanged_
- Particles _always in antisymmetric states_ are known as __fermions__
	- Particle _exchange_ only _flips the sign_ of the wave function

- Due to the _antisymmetry_ of _fermions_, one gets the _Pauli Exclusion Principle_:
>[!info] Pauli Exclusion Principle
>Two identical fermions cannot be in the same quantum state
- Proof: $\ket{\omega\omega, A}=\ket{0}$

- The _spin statistics theorem_, derived from _quantum field theory_, asserts that, in _three dimensions_, where particles have _spin_ $s$:
	- Particles with _integer spin_ are _bosons_
	- Particles with _half-integer spin_ are _fermions_
- This _does not apply_ to _one or two dimensions_

- In three dimensions, for _spin-1/2 particles_, which can only go _spin up or down_, means the state vector must be _antisymmetric w.r.t. spin as well_:
$$\ket{\omega_1s_1,\omega_2s_2,A}=\ket{\omega_1s_1,\omega_2s_2}-\ket{\omega_2s_2,\omega_1s_1}$$
- Of course, it vanishes if $\omega_1=\omega_2$ and $s_1=s_2$

### Bosonic and Fermionic Hilbert Spaces
- The set of _symmetric_ state vectors can form a _Hilbert space_ $\mathbb{V}_S$
- The set of _anti-symmetric_ state vectors can form another Hilbert space $\mathbb{V}_A$

- Consider the [[#The direct product space|two-particle Hilbert space]] $\mathbb{V}_{1\otimes2}$ 
- For every pair of vectors $\ket{\omega_1=a,\omega_2=b}$ and $\ket{\omega_1=b,\omega_2=a}$, they can form a _bosonic_ state vector and a _fermionic_ state vector
	- If $a=b$, it automatically forms a _bosonic_ state vector, with no corresponding fermionic vector
- Therefore, $\mathbb{V}_{1\otimes2}$ is the _direct sum_ of two vector spaces:
$$\mathbb{V}_{1\otimes2}=\mathbb{V}_S\oplus\mathbb{V}_A$$
- The former has _slightly higher dimensionality_

- By considering the propagator, one can show that particles _starting out_ in $\mathbb{V}_S$ or $\mathbb{V}_A$ will _stay in that Hilbert space_

### Normalisation
- For the ket $\ket{\omega_1\omega_2,S}$, since $\ket{\omega_1\omega_2}$ and $\ket{\omega_2\omega_1}$ are _orthonormal_, the normalisation is:
$$\ket{\omega_1\omega_2,S}=\frac{1}{\sqrt{2}}[\ket{\omega_1\omega_2}+\ket{\omega_2\omega_1}]$$
- If $\omega_1=\omega_2$, the eigenket is _already normalised_

- Then the probability of finding two _bosons_ with wave function $\ket{\Psi_S}$ in the eigenstate $\ket{\omega_1\omega_2,S}$ is:
$$P_S(\omega_1,\omega_2)=|\braket{\omega_1\omega_2,S|\Psi_S}|^2$$
- The normalisation condition:
$$1=\braket{\Psi_S|\Psi_S}=\sum_\text{dist}|\braket{\omega_1\omega_2,S|\Psi_S}|^2=\sum_\text{dist}P(\omega_1,\omega_2)$$
- The sum is over _physically distinct_ states, as $\ket{\omega_1\omega_2,S}=\ket{\omega_2\omega_1,S}$
	- If $\omega$ takes discrete values, the sum would be $$\sum_\text{dist}=\sum_{\omega_2=\omega_\text{min}}^{\omega_\text{max}}\sum_{\omega_1=\omega_{\text{min}}}^{\omega_2}$$
	- Or, one could sum over _the whole range of values for both_, then _divide_ by 2

- Similarly, for a _continuous variable_ like position:
$$1=\iint P_S(x_1,x_2)\frac{dx_1dx_2}{2}=\iint |\braket{x_1x_2,S|\Psi_S}|^2\frac{dx_1dx_2}{2}$$
- It is customary to denote the _position-space wave function as_:
$$\Psi_S(x_1,x_2)=\frac{1}{\sqrt{2}}\braket{x_1x_2,S|\Psi_S}$$
- Such that:
$$1=\iint|\Psi_S(x_1,x_2)|^2\,dx_1dx_2\hspace{1.5cm}P_S(x_1,x_2)=2|\Psi_S(x_1,x_2)|^2\,dx_1dx_2$$
- Exploiting the fact that $\ket{\Psi_S}$ is _symmetrised_, one can write $\Psi_S(x_1,x_2)$ as:
$$\Psi_S(x_1,x_2)=\braket{x_1x_2|\Psi_S}$$
- The normalisation condition can also be rewritten as:
$$1=\braket{\Psi_S|\Psi_S}=\iint\braket{\Psi_S|x_1x_2}\braket{x_1x_2|\Psi_S}\,dx_1dx_2=\iint |\Psi_S(x_1,x_2)|^2\,dx_1dx_2$$
- $\ket{x_1x_2}$ is _not_ an element of $\mathbb{V}_S$, and $\braket{x_1x_2|\Psi_S}$ has _no physical significance_ apart from the fact that it is _related to_ $\braket{x_1x_2,S|\Psi_S}$ by a _scale factor_ only

- One can repeat the above for _fermionic state vectors_:
$$\displaylines{\ket{\omega_1\omega_2,A}=\frac{1}{\sqrt2}[\ket{\omega_1\omega_2}-\ket{\omega_2\omega_1}]\\P_A(\omega_1,\omega_2)=|\braket{\omega_1\omega_2,A|\Psi_A}|^2\\\Psi_A(x_1,x_2)=\frac{1}{\sqrt{2}}\braket{x_1x_2,A|\Psi_A}=\braket{x_1x_2|\Psi_A}\\1=\iint|\braket{x_1x_2,A|\Psi_A}|\,\frac{dx_1dx_2}{2}=\iint|\Psi_A(x_1,x_2)|^2\,dx_1dx_2}$$
- For a two-particle system with states characterised by _quantum number_ $n$, where $\braket{x|n}=\Psi_n(x)$, a normalised bosonic/fermionic state vector would be:
$$\displaylines{\ket{\Psi_{S/A}}=\frac{1}{\sqrt{2}}(\ket{n_1n_2}\pm\ket{n_2n_1})\\ \begin{aligned}\Psi_{S/A}(x_1,x_2)&=\frac{1}{\sqrt{2}}\braket{x_1x_2,S/A|\Psi_{S/A}}\\&=\frac{1}{\sqrt{2}}[\Psi_{n_1}(x_1)\Psi_{n_2}(x_2)\pm\Psi_{n_2}(x_1)\Psi_{n_1}(x_2)]\\&=\braket{x_1x_2|\Psi_{S/A}}\end{aligned}}$$
- The _fermionic_ state vector can be written as a _determinant_:
$$\Psi_A(x_1,x_2)=\frac{1}{\sqrt{2}}\begin{vmatrix}\Psi_{n_1}(x_1)&\Psi_{n_2}(x_1)\\\Psi_{n_1}(x_2)&\Psi_{n_2}(x_2)\end{vmatrix}$$

- Expanding out $P_{S/A}(x_1,x_2)$:
$$\begin{aligned}P_{S/A}(x_1,x_2)&=|\Psi_{n_1}(x_1)|^2|\Psi_{n_2}(x_2)|^2+|\Psi_{n_2}(x_1)|^2|\Psi_{n_1}(x_2)|^2\\&\pm\left[\Psi_{n_1}^*(x_1)\Psi_{n_2}(x_1)\Psi_{n_2}^*(x_2)\Psi_{n_1}(x_2)+\Psi_{n_2}^*(x_1)\Psi_{n_1}(x_1)\Psi_{n_1}^*(x_2)\Psi_{n_2}(x_2)\right]\end{aligned}$$
- The first two terms are the same as the probability distribution for _distinguishable particles_
- The latter are the _interference terms_
	- For _fermions_, as $x_1\to x_2$, $P_A\to0$ as expected
	- For _bosons_, as $x_1\to x_2$, the probability is _double that of distinguishable particles_
- This helps to _distinguish bosons and fermions using measurements_
- This treatment _ignores spin_
- This also shows that for cases where the _particle wave functions have negligible overlap_, one can simply _ignore symmetrisation_
	- e.g. if inter-particle distance $>>$ extent of wave-functions
### More identical particles
- For $N>2$, in general, one can _only_ form vectors that are either _always symmetric or antisymmetric_ under _all possible exchanges_
- There are only _two possible state vectors_ out of $N!$ _product vectors_
- Therefore, the _dimensionality_ of $\mathbb{V}_S\oplus\mathbb{V}_A$ is _smaller_ than that of the direct product space for $N\geq 3$

- For $N$ particles, with possible states $\Psi_n$, one can write the _bosonic_ state as:
$$\displaylines{\wv=\sqrt{\frac{\prod_im_i!}{N!}}\sum_n\ket{\Psi_{n_1}}\otimes\ket{\Psi_{n_2}}\otimes\dots\otimes\ket{\Psi_{n_N}} \\ \Psi(x_1,x_2,\dots x_N)=\sqrt{\frac{\prod_im_i!}{N!}}\sum_n\Psi_{n_1}(x_1)\Psi_{n_2}(x_2)\dots\Psi_{n_N}(x_N)}$$
- The normalisation factor includes the fact that _multiple bosons can occupy the same state_ (with $\sum m_i=N$), and the sum takes place over _all permutations_ of possible wave functions

- For the _fermionic state_, one can write it as a _Slater determinant_:
$$\Psi(x_1,x_2,\dots x_N)=\frac{1}{\sqrt{N!}}\begin{vmatrix}\Psi_{n_1}(x_1)&\Psi_{n_2}(x_1)&\dots&\Psi_{n_N}(x_1)\\\Psi_{n_1}(x_2)&\Psi_{n_2}(x_2)&\dots&\Psi_{n_N}(x_2) \\ \vdots&\vdots&\ddots&\vdots\\ \Psi_{n_1}(x_N)&\Psi_{n_2}(x_N)&\dots&\Psi_{n_N}(x_N)\end{vmatrix}$$
- One can see that _interchange_ corresponds to _swapping columns_, which _switches_ the sign of the determinant
- If two particles occupy the _same state_, one sees that the determinant _vanishes_

# Spin
