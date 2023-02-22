
# Notation
- Generic vectors are denoted with _kets_ $\ket{V}$
- Operators have capital letters and hats $\hat{\Omega}$
- The _eigenvalues_ are denoted with the small version of the letter for the operator:
$$\hat{\Omega}\ket{\omega}=\omega\ket{\omega}$$

# The Wave function and the fundamental postulates 
- __Postulate 1:__ In quantum mechanics, the state of a system is represented by the wave function, a state vector in [[Vectors and matrices in physics|complex vector space]]
- __Postulate 2:__ The independent variables $x$ and $p$ of the Hamiltonian formulation are represented by the Hermitian operators $\hat{X}$ and $\hat{P}$ ([[The operators of quantum mechanics#The position and momentum operators|definition]]), with classical variables $\omega(x,p)$ _represented by operator_ $\hat{\Omega}(\hat{X},\hat{P})$ 
- __Postulate 3:__ Measurement of a variable corresponding to $\hat{\Omega}$ _always yields one of the eigenvalues $\omega$ with probability (density) $|\braket{\omega|\Psi}|^2$_, with the _subsequent state represented by normalised eigenvector_ $\ket{\omega}$. Values other than the eigenvalues are impossible.
	- In terms of projection operator $\mathcal{P}_\omega=\ket{\omega}\bra{\omega}$, $P(\Omega=\omega) \propto \braket{\Psi|\mathcal{P}_\omega\Psi} = \braket{\Psi\mathcal{P}_\omega|\mathcal{P}_\omega\Psi}$
- __Postulate 4:__ The state ket $\wv$ obeys [[#Time-evolution The Schrödinger equation|the Schrödinger equation]]

## Normalisation
- Each physical state is more precisely described as a _"ray" in the complex vector space_
	- Just normalised vectors do not form a complete vector space
- If $\wv$ is a _proper vector_, it is normalised ($\braket{\Psi|\Psi}$ = 1) to _normalise the probability distribution_
- There is _freedom to multiply_ the ket by $exp(i\theta)$ to make certain components real
- $\wv$ could be an _improper vector_, which can only be _normalised to a Delta function_
	- Example: Continuous wave

## Measurement
- Measurement can be defined as _interaction with a classical object_
- The conversion from a classical quantity to a quantum mechanical operator can be ambiguous ($\hat{X}\hat{P}\neq \hat{P}\hat{X}$)
	- For 2 operators, a Hermitian, symmetric sum can be used: $(\hat{X}\hat{P}+\hat{P}\hat{X})/2$
- If the operator $\hat{\Omega}$ is _degenerate_, the projection operator becomes $\ket{\omega_1}\bra{\omega_1}+\ket{\omega_2}\bra{\omega_2}$, and the subsequent state is some _linear combination of the eigenkets_
- If the eigenvalue spectrum is continuous, $|\braket{\omega|\Psi}|^2$ becomes a probability density
	- If the wave function is improper, it is only a relative probability density
- A quantum variable does not necessarily have a classical counterpart
	- Example: spin
- To test quantum theory, one must use a _quantum ensemble_ of particles in pre-determined, definite states as wave functions collapse after measurement

## Compatible and incompatible observables
- For only one given variable $\omega$, one can produce a state with a definite value of $\omega$ by performing a measurement and collapsing the wave function
	- The state is not definite if $\Omega$ is degenerate
- Consider two variables $\omega$ and $\lambda$, measured one after the other
	- In general, the final state will not always have a definite value for both
	- There will be a definite value of both if the eigenkets of $\Omega$ are also eigenkets of $\Lambda$
	- For the above to be true, a necessary condition is $[\Omega,\Lambda]=0$
- Compatibility:
	- If two operators commute, a complete set of simultaneous eigenkets exist, and the observables are _compatible_
	- If they can never commute, they are _incompatible_ (example: $x$ and $p$)
	- Some pairs of observables have an incomplete set of simultaneous eigenkets

### Measuring compatible observables
- If neither operator is degenerate, only one measurement collapses the wave function into a definite state, with $P(\omega,\lambda)=P(\lambda,\omega)$
- If one of the operators is degenerate, $P(\omega,\lambda)=P(\lambda,\omega)$, but the wave functions after the measurements depends on measurement order
- If both operators are degenerate, a third compatible must be found to "nail down" the wave function
	- In general, a complete set of commuting observables exists

## The wave function in different bases
- $\wv$ itself only exists in Hilbert space, other spaces representing observable quantities are auxiliary finite-dimensional manifolds on which to project $\wv$
$$\Psi(x,t)=\braket{x|\Psi(t)}\;\;\;\;\Phi(p,t)=\braket{p|\Psi(t)}$$
	- Classical: particles are described by a finite number of definite variables
	- Quantum: particles are described in terms of probabilities for an often infinite range of values
- As the eigenkets of any [[The operators of quantum mechanics|operator representing an observable]] span the entire vector space, any wave function can be written in terms of eigenstates:
$$\begin{aligned}\wv&=\sum_n\ket{q_n}\braket{q_n|\Psi}=\sum_nc_n\ket{q_n} \\ &= \int \ket{q_n}\braket{q_n|\Psi}\,dq = \int c(q)\, \ket{q} \,dq \end{aligned}$$
- Discrete spectrum: $P(Q=q_n)=|c_n|^2=|\braket{q_n|\Psi}|^2$
- Continuous spectrum: $P(q<Q<q+dq)=|c(q)|^2\,dq=|\braket{q|\Psi}|^2\,dq$
- As the wave function is normalised, the coefficients sum/integrate to one
$$\sum_n|c_n|^2=\int |c(q)|^2\,dq=1$$
- As for the expectation value, expanding $\braket{\Psi|\hat{Q}\Psi}$ gives:
$$\braket{\Psi|\hat{Q}\Psi}=\sum_nq_n|c_n|^2=\int q\,|c(q)|^2\;dq$$
- To convert to another base, use the _completeness relation_:
$$I=\int\ket{q}\bra{q}\,dq$$
$$\Phi(p,t)=\braket{p|\Psi}=\int\braket{p|x}\braket{x|\Psi}dx=\frac{1}{\sqrt{2\pi\hbar}}\exp(-ipx/\hbar)$$
## Uncertainty
- Variance $\sigma^2 = \left<(\hat{A}-a)^2\right>$ 
- The _generalised uncertainty principle_:
$$\sigma_A^2\sigma_B^2\geq\left(\frac{1}{2i}\left<[\hat{A},\hat{B}]\right>\right)^2$$
	- Proof: Cauchy-Schwarz inequality with $\ket{(\hat{A}-a)\Psi}$ and $\ket{(\hat{B}-b)\Psi}$
		- $|\braket{f|g}|^2 = Re(\braket{f|g})^2+Im(\braket{f|g})^2$ 
- Strict uncertainty principle:
$$\sigma_A^2\sigma_B^2 \geq \left(\frac{1}{2}\left<\{\hat{A},\hat{B}\}\right>-ab\right)^2+\left(\frac{1}{2i}\left<[\hat{A},\hat{B}]\right>\right)^2$$

# Time-evolution: The Schrödinger equation
## The time-evolution operator
- Let the state ket at time $t$ be:
$$\ket{\Psi(t)}=\teo(t-t_0)\ket{\Psi(t_0)}$$
	- $\teo$ is the _time-evolution operator_, also known as the _propagator_
- The time-evolution operator must fulfill the following properties:
	- Composition: $\teo(t_2-t_0)=\teo(t_2-t_1)\teo(t_1-t_0)$
	- [[Vectors and matrices|Unitarity]]/probability conservation: $\braket{\Psi|\Psi}=\braket{\Psi_0|\Psi_0}=1$ -> $\teo^\dagger\teo=1$
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
- The _normal modes_ of the equation, $\ket{E_n(t)}=\exp(-iE_nt/\hbar)\ket{E_n}$, are known as _stationary states_, as the _probability distribution for any variable remains constant_:
$$|\braket{q|E_n(t)}|^2=|\braket{q|E_n}\exp(-iE_nt/\hbar)|^2=|\braket{q|E_n}|^2$$
- The eigenvalue equation for the energy eigenkets is also known as the _time-independent  Schrödinger equation_:
$$\Ham\ket{E_n}=E_n\ket{E_n}$$
- Projected onto the $x$ basis with $\Ham=T+V$:
$$-\frac{\hbar^2}{2m}\nabla^2\psi_n(x)+V\psi_n(x)=E_n\psi_n(x)$$
- Solving this thing: [[Time-independent quantum mechanics]]

## Time-dependent Hamiltonians: various methods

# Transition amplitude
- Given two eigenkets, $\ket{b}$ at time $t$ and $\ket{a}$ at time $t=0$, the _transition amplitude_ between them is defined as:
$$\braket{b|\teo(t,0)|a}$$
- This describes the probability amplitude of the system "transitioning" from eigenstate $\ket{a}$ at $t=0$ to eigenstate $\ket{b}$ at time $t$
- This quantity is particularly useful in defining the [[Path integrals in quantum mechanics|path integral formulation]]

# The Schrödinger and Heisenberg pictures
- So far, we have been working with the _Schrödinger picture_, where the _state kets evolve with time, with the operators remaining constant_

- Consider the time-evolution of inner product $\braket{\beta|\Omega|\alpha}$:
$$\braket{\beta|\Omega|\alpha} \rightarrow \braket{\teo\beta|\Omega|\alpha}=\braket{\beta|\teo^\dagger\Omega\teo|\alpha}$$
- This can be interpreted as the state ket remains unchanged, with the operator representing the observable evolving with time
- This is known as the _Heisenberg picture_
- It applies not only to time-evolution, but to _any unitary transformation_, such as translation
- It is a "closer" approach to classical mechanics, which has no state vectors, and observables that vary with time
## State kets and observables in the Heisenberg picture
- The Heisenberg picture observable $A^{(H)}$ is defined by:
$$A^{(H)}(t)=\teo^\dagger(t) A^{(S)}\teo(t)$$
	- The Heisenberg and Schrödinger pictures coincide at $t=0$
- State kets in the Heisenberg picture are frozen:
$$\ket{\Psi,t_0=0,t}_H=\ket{\Psi,t_0=0}$$
	- In the Schrödinger picture, $\ket{\Psi,t_0=0,t}_S=\teo(t)\ket{\Psi,t_0}$
- The expectation value is the same across both pictures
$${}_{S}\braket{\Psi(t)|A^{(S)}|\Psi(t)}_S=\braket{\Psi(t_0)|A^{(H)}|\Psi(t_0)}$$
## The Heisenberg equation of motion
- Expressing the Heisenberg operator in terms of the Schrödinger operator, then taking the total time derivative, one gets the _Heisenberg equation of motion_:
$$\frac{dA^{(H)}}{dt}=\frac{1}{i\hbar}[A^{(H)},\Ham^{(H)}]+\pd{A^{(H)}}{t}$$
- The Heisenberg Hamiltonian $\Ham^{(H)}$ is defined the same as other $(H)$ operators
- For a time-independent Hamiltonian, $[\Ham,\teo]$ commute, and $\Ham^{(S)}=\Ham^{(H)}$
- This echoes the equation for rate of change of variables in classical mechanics:
$$\frac{dA}{dt}=\PB{A}{\Ham}+\pd{A}{t}$$
	- where $\{,\}$ is the [[Analytical classical mechanics|Poisson bracket]]
- This further establishes that the commutator is a "quantum version" of the PB
## Base kets in the Heisenberg picture
- In the Schrödinger picture, the operators and base kets are stationary
- At $t=0$, the two pictures coincide:
$$A^{(H)}(0)\,\ket{a'} = a'\ket{a'}$$
- Operating on both sides with $\teo^\dagger$, the time-evolution for $\ket{a'}_H$ is found:
$$\teo^\dagger A^{(H)}(0)\,\teo(\teo^\dagger\ket{a'})=A^{(H)}(t)\,(\teo^\dagger\ket{a'})=a'(\teo^\dagger\ket{a'})=a'\ket{a',t}_H$$
- The base kets in the Heisenberg picture _rotate oppositely_ compared to Schrödinger's state kets
- The eigenvalues stay constant, as expected
- $\teo^{(H)}=\teo^\dagger\teo^{(S)}\teo$ can be recovered by expanding the former in terms of $\ket{a',t}_H$
- Expansion coefficients remain the same:
$$c_{a'}(t)={}_{H}\braket{a',t|\alpha}=\braket{a'|\alpha,t}_S=\braket{a'(t=0)|\teo|\alpha(t=0)}$$
- Transition amplitudes between two eigenstates are also the same within the two pictures, with the same reasoning as above

# Multiple degrees of freedom
- In quantum theory, there exist $N$ mutually commuting operators $X_1,...,X_N$, with a simultaneous orthonormal eigenbasis where:
$$\braket{x_1,x_2,...,x_N|x_1',x_2',...,x_N'}=\delta(x_1-x_1')\,\delta(x_2-x_2')...\delta(x_n-x_n')$$
- Other definitions involving the wave function have the following correspondence:
$$\begin{aligned} \braket{x_1,x_2...x_N|\Psi}&=\Psi(x_1,x_2...x_N) \\
\braket{x_1,x_2...x_N|X_i|\Psi}&=x_i\Psi(x_1,x_2...x_N) \\
\braket{x_1,x_2...x_N|P_i|\Psi}&=\frac{\hbar}{i}\pd{}{x_i}\Psi(x_1,x_2...x_N)
\end{aligned}$$
- For _non-Cartesian coordinate systems_, it is easier to use mathematical identities to construct quantum operators, for example:
$$\begin{aligned} \Omega&=\frac{P_x^2+P_y^2+P_z^2}{2m}+X^2+Y^2+Z^2\\ &\equiv -\frac{\hbar^2}{2m}\nabla^2+R^2 \\ &\equiv -\frac{\hbar^2}{2m}\left[\frac{1}{r^2}\pd{}{r}\left(r^2\pd{}{r}\right)+\frac{1}{r^2\sin\theta}\pd{}{\theta}\left(\sin\theta\pd{}{\theta}\right)+\frac{1}{r^2\sin^2\theta}\pd{^2}{\phi^2}\right]+r^2\end{aligned}$$

# Time evolution of expectation values
- Due to the probabilistic nature of quantum mechanics, one _cannot define a time derivative of an observable quantity_
- However, one can talk about the _time evolution of the expectation value_

## Ehrenfest's Theorem
- By applying the time derivative to $\mean{A}=\braket{\psi|\hat{A}|\psi}$:
$$\frac{d}{dt}\mean{A}=\mean{\pd{A}{t}}+\frac{1}{i\hbar}\mean{[\hat{A},\hat{H}]}$$
- This is _analagous_ to the time evolution of a quantity using [[Analytical classical mechanics#Poisson brackets|Poisson brackets]]

- It is also most apparent with respect to the [[#The Heisenberg equation of motion|Heisenberg picture]], where it is the time-averaged version of the _Heisenberg equation of motion_

- Assuming $\hat{A}$ does not explicitly depend on time:
	- If $\hat{A}$ commutes with $\hat{H}$ (they _share eigenstates_), then $\mean{A}$ is a _constant of motion_
	- If the system is in an _energy eigenstate_, then _expectation values of all observables are independent in time_

- Let there be a time-independent Hamiltonian, such that the wave function is:
$$\wv=\sum_nc_n\exp\left(-\frac{iE_nt}{\hbar}\right)\ket{E_n} \hspace{0.5cm}\text{ where } c_n=\braket{E_n|\Psi(0)}$$
- From this, the time evolution can be written as:
$$\mean{A}=\sum_{m,n}c_m^*c_n\exp\left(-\frac{i(E_n-E_m)t}{\hbar}\right)A_{mn}$$
- Here, $A_{mn}$ is the _matrix element of $\hat{A}$ in the energy eigenbasis_:
$$A_{mn}\equiv\braket{E_m|\hat{A}|E_n}$$

## Important cases

## Energy-time uncertainty principle

# Probability flow
- The total probability of finding a particle anywhere in the universe is conserved:
$$\braket{\Psi(0)|\Psi(0)}=\braket{\Psi(t)|\Psi(t)}=\int_\text{all space}\braket{\Psi(t)|\bm{r}}\braket{\bm{r}|\Psi(t)}\,d^3\bm{r}=\int_\text{all space}P(\bm{r},t)\,d^3\bm{r}$$
- Consider the time derivative of $P(\bm{r},t)$, and using the [[Fundamentals of quantum mechanics#The Schrödinger wave equation|Schrödinger wave equation]]:
$$\begin{aligned}\pd{P}{t}&=\pd{}{t}[\Psi^*(x,t)\Psi(x,t)] \\
&= \frac{i\hbar}{2m}\left[\Psi^*\nabla^2\Psi-\Psi\nabla^2\Psi^*\right] \\ &=  \frac{i\hbar}{2m} \nabla\cdot\left[\Psi^*\nabla\Psi-\Psi\nabla\Psi^*\right] \\\pd{P}{t}&=-\nabla\cdot\bm{J}\end{aligned}$$
- Here, $\bm{J}$ is the _probability current density_
- This is the continuity equation for the probability of finding a particle
	- For an ensemble of $N$ particles, $N\bm{J}\cdot d\bm{S}$ particles per unit time flow past an area $d\bm{S}$

# The classical limit
