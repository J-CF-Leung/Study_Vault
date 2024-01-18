- Systems with a _time-varying perturbation_ can potentially induce _transitions between eigenstates_
	- Time-independent Hamiltonian: linear combination of [[Principles of quantum mechanics#Time-independent Hamiltonians and stationary states|stationary states]]

# Time-dependent perturbation theory
- A general _time-dependent_ Hamiltonian, with _all dependence within the perturbation_:
$$\hat{H}(t)=\hat{H}_{0}+\hat{H}'(t)$$
- The _eigenstates_ of the time-independent part:
$$\hat{H}\ket{n} =E_n\ket{n}\hspace{1cm}E_{n}\equiv \hbar\omega_{n}\hspace{1cm}\braket{ n | m } =\delta_{nm} $$
- The wave-function in general can be written as:
$$\ket{\psi} =\sum_{j}c_{j}(t)\exp(-i\omega_{j}t)\ket{j} $$
- Substituting the above into the _time-dependent Schrodinger equation_:
$$i\hbar \frac{dc_{j}}{dt}=\sum_{k}c_{k}(t)\exp[i(\omega_{j}-\omega_{k})t]H'_{jk}(t)$$
- Here, $H'_{jk}$ are the _matrix elements_ of the perturbation:
$$H'_{jk}(t)=\braket{ j|\hat{H}'(t) | k } $$

## Harmonic perturbations in two-state systems
- Let there be _two eigenstates_ of the unperturbed Hamiltonian $\hat{H}_{0}$, with some _energy difference_ $E_{2}-E_{1}=\hbar\omega_{0}$
$$\displaylines{\hat{H}_{0}\ket{\psi_{i}}=E_{i}\ket{\psi_{i}} \hspace{1.5cm}i=1,2  \\ \omega_{0}=\omega_{2}-\omega_{1}}$$

### Oscillating perturbation
- Let the time-dependent perturbation be _harmonic_ at frequency $\omega$:
$$\hat{H}'(t)=\hat{H}'\cos\omega t$$
- Here, $\hat{H}'$ is _time-independent_

- Expanding $\cos\omega t=[\exp(i\omega t)+\exp(-i\omega t)]/2$ and substituting into the equation above:
$$\begin{align}
i\hbar \frac{dc_{1}}{dt}&=\frac{H'_{11}}{2}c_{1}(t)[e^{i\omega t}+e^{-i\omega t}] +\frac{H'_{12}}{2}c_{2}(t)[e^{i(\omega-\omega_{0})t}+e^{-i(\omega+\omega_{0})t}] \\ i\hbar \frac{dc_{2}}{dt}&=\frac{H'_{22}}{2}c_{1}(t)[e^{i\omega t}+e^{-i\omega t}] +\frac{H'_{21}}{2}c_{2}(t)[e^{i(\omega+\omega_{0})t}+e^{-i(\omega-\omega_{0})t}]
\end{align}$$

- Suppose the _driving frequency_ $\omega$ is _close to_ $\omega_{0}$, such that $\omega,\omega+\omega_{0}\gg|\omega-\omega_{0}|$
- Apply the _rotating wave approximation_, which _averages out_ the $\omega$ and $\omega+\omega_{0}$ terms
- Then defining $H'_{12}=\hbar\omega'$, where $\omega'$ is a _complex constant_:
$$\begin{align}
i \frac{dc_{1}}{dt}&=\frac{\omega'}{2}c_{2}\exp[i(\omega-\omega_{0})t] \\ i \frac{dc_{2}}{dt}&=\frac{(\omega')^{*}}{2}c_{1}\exp[-i(\omega-\omega_{0})t]
\end{align}$$
- Then one gets a _damped SHM equation_ for $c_{1}$ and $c_{2}$:
$$\frac{d^{2}c_{2}}{dt^{2}}+i(\omega-\omega_{0})\frac{dc_{2}}{dt}+\frac{1}{4}|\omega'|^{2}c_{2}=0$$

### Resonant oscillation of transition probabilities
- For $\omega=\omega_{0}$, the _damping term vanishes_, and the solution is:
$$c_{2}=A\cos\left( \frac{|\omega'|}{2}t \right)+B\sin\left( \frac{|\omega'|}{2}t \right)$$
- $|\omega'|$ is known as the _Rabi frequency_ in this case:
$$\frac{|\omega'|}{2}=\frac{1}{2\hbar}|\braket{ \psi_{1}|\hat{H}' | \psi_{2} }| $$
- It is determined by the _coupling_ of the two states _induced by_ $\hat{H}'$
- Measures the _frequency of transition_ (See below)

- Suppose $c_{1}(0)=1$, one gets the solutions:
$$P_{1}(t)=|c_{1}(t)|^{2}=\cos^{2}\left( \frac{|\omega'|t}{2} \right)\hspace{1.5cm}P_{2}(t)=|c_{2}(t)|^{2}=\sin^{2}\left( \frac{|\omega'|t}{2} \right)$$
![[Rabi oscillation.png]]

- $P_{2}(t)$ is the _transition probability_ from state 1 to 2 at time $t$
### General driving frequency
- For a _general value_ of driving frequency $\omega$, one can try a solution of the form:
$$c_{2}(t)=A\exp(i\Omega t)$$
- Substituting into the equation, one gets:
$$\Omega=\frac{1}{2}(\omega-\omega_{0})\pm \frac{1}{2}\sqrt{ (\omega-\omega_{0})^{2}+|\omega'|^{2} }\equiv\frac{1}{2}(\omega-\omega_{0})\pm \frac{\omega_{R}}{2}$$
- Here, $\omega_{R}$ is the _Rabi frequency_:
$$c_{2}=\exp\left[ \frac{1}{2}i(\omega-\omega_{0})t \right][A\cos(\omega_{R}t)]$$

- Suppose $c_{1}(0)=1$, solving for $c_{1}$ and $c_2$, one gets:
$$P_{2}(t)=\left( \frac{|\omega'|}{\omega_{R}} \right)^{2}\sin^{2}\left( \frac{1}{2}\omega_{R}t \right)$$
- The _maximum transition probability_ is:
$$P_{2,\text{max}}=\left( \frac{|\omega'|}{\omega_{R}} \right)^{2}=\frac{|\omega'|^{2}}{(\omega-\omega_{0})^{2}+|\omega'|^{2}}$$
![[Rabi oscillation general frequency.png]]

- If the driving frequency does _not exactly match_ the original energy difference, the transition probability is _always less than $1$_
- The Rabi frequency $\omega_{R}$ is _always larger_ than $|\omega'|$

- There is a _Lorentzian resonance_ in transition probability as a function of $\omega$
![[Rabi Lorentzian.png]]
- $\Delta\omega$ is given by the _full-width half maximum_
- The peak gets _sharper_ as $|\omega'|$ falls

## Spin one-half particle in a time-varying magnetic field
- Consider a _spin-half_ particle with [[Charged Particles#Spin and the magnetic moment operator|magnetic moment]]:
$$\hat{\boldsymbol{\mu}}=\gamma \hat{\boldsymbol{S}}$$
- In the time-dependent magnetic field:
$$\boldsymbol{B}=(B_{x}\cos\omega t,0,B_{z})$$
- The constant field along the $z-$axis gives rise to [[Charged Particles#Spin precession|spin precession]]

- The Hamiltonian:
$$\displaylines{\hat{H}(t)=-\hat{\boldsymbol{\mu}}\cdot \boldsymbol{B}=\hat{H}_{0}+\hat{H}'\cos(\omega t) \\ \hat{H}_{0}=-\gamma B_{z}\hat{S}_{z}\hspace{1.5cm} \hat{H}'=-\gamma B_{x}\hat{S}_{x}}$$

### Resonant spin transitions
- Eigenstates of the _time-independent_ Hamiltonian:
$$\displaylines{\ket{\psi_{1}}=\ket{\uparrow}\;,\;\ket{\psi_{2}}=\ket{\downarrow}  \hspace{1cm}E_{1}=-\frac{\hbar\gamma B_{z}}{2}\;\,\;E_{2}=\frac{\hbar\gamma B_{z}}{2} \\ \omega_{0}=\gamma B_{z}}$$

- The constant $\omega'$:
$$\omega'=\frac{1}{\hbar}\braket{ \uparrow | \hat{H}'|\downarrow }=-\frac{\gamma B_{x}}{2\hbar}\Braket{ \uparrow|\hat{S}_{+} +\hat{S}_{-} | \downarrow }=-\frac{\gamma B_{x}}{2}  $$

- The _resonant transitions_ occur at
$$\omega=\omega_{0}=\gamma B_{z}$$
- The _width_ of the resonance peak:
$$\frac{|\Delta\omega|}{\omega_{0}}=\frac{2|\omega'|}{\omega_{0}}=\frac{B_{x}}{B_{z}}$$

### Time-evolution of expectation values
- Write the wave-function as:
$$\ket{\psi}=c_{1}(t)\exp(i\omega_{0}t/2)\ket{\uparrow}+c_{2}(t)\exp(-i\omega_{0}t/2)  \ket{\downarrow} $$
- One can then evaluate the expectation values:
$$\begin{align}
\langle \hat{S}_{z} \rangle &=\frac{\hbar}{2}\left[|c_{1}(t)|^{2}-|c_{2}(t)|^{2}\right] \\
\langle \hat{S}_{x} \rangle &=\hbar \,\mathrm{Re}[c_{1}(t)^{*}c_{2}(t)\exp(-i\omega_{0}t)] \\
\langle \hat{S}_{y} \rangle &=\hbar \,\mathrm{Im}[c_{1}(t)c_{2}(t)^{*}\exp(+i\omega_{0}t)]
\end{align}$$

- Suppose the driving frequency is _in resonance_ $\omega=\omega_{0}$, and the system is _initially_ in the low-energy (spin up) state, hence $c_{1}(0)=1$:
$$c_{1}(t)=\cos\left( \frac{1}{2}|\omega'|t\right)\hspace{1.5cm}c_{2}(t)=i\sin\left( \frac{1}{2}|\omega'|t \right)$$

- The three-vector of _spin expectation values_:
$$\langle \hat{\boldsymbol{S}} \rangle=\frac{\hbar}{2}\begin{pmatrix}
\sin(\omega't)\sin(\omega_{0}t) \\
\sin(\omega't)\cos(\omega_{0}t) \\
\cos(\omega't)
\end{pmatrix} $$

- It is a _combination_ of:
	- _Precession_ about the $z-$axis with frequency $\omega_{0}$
	- _Precession_ about the _horizontal_ axis with frequency $|\omega'|$, where the axis _itself_ rotates about $z$ with frequency $\omega_{0}$
![[Spin precession 2 axes.png]]

- In particular times:
	- $\omega't=\pi$, $\langle \hat{\boldsymbol{S}} \rangle=\begin{pmatrix} 0&0&-\hbar/2\end{pmatrix}$
	- $\omega't=\frac{\pi}{2}$, $\langle \hat{\boldsymbol{S}} \rangle=\hbar/2\begin{pmatrix}\sin(\omega_{0}t)&\cos(\omega_{0}t)&0 \end{pmatrix}$

- If the field is only applied for some _time interval_ $\Delta t$ before being _switched off_:
	- $\omega'\Delta t=\pi$, the particle is _flipped_ into the spin-down state, then _stays_ there, where it is _stationary
	- $\omega'\Delta t=\pi/2$, the particle is rotated _into_ the $x-y$ plane, then _stays_ there, where it _precesses_ at the [[Charged Particles#Spin precession|Larmor frequency]] $\omega_{0}=\gamma B_{z}$

- Applications: NMR, MRI

## A general Hamiltonian
- Suppose an _analytic solution_ to $c_j(t)$ is _unavailable_
- Still write the wave-function as:
$$\ket{\psi}=\sum_{j}c_{j}(t)\exp(-i\omega_{j}t)\ket{j}  $$
- Writing the Hamiltonian as:
$$\hat{H}(t)=\hat{H}_{0}+\lambda \hat{H}'(t)$$
- Write the coefficients as an _expansion_ in powers of $\lambda$:
$$c_{j}(t)=c_{j}^{(0)}+\lambda c_{j}^{(1)}+\lambda^{2}c_{j}^{(2)}+\dots$$
- Substituting into Schrodinger's equation, and _comparing powers of $\lambda$_, one finds:
$$\begin{align}
i\hbar\frac{dc_{j}^{(0)}}{dt}&=0 \\ i\hbar \frac{dc_{j}^{(1)}}{dt}&=\sum_{k} c_{k}^{(0)}(t)\exp[i(\omega_{j}-\omega_{k})t]H'_{jk}(t)  \\
i\hbar \frac{dc_{j}^{(2)}}{dt}&=\sum_{k} c_{k}^{(1)}(t)\exp[i(\omega_{j}-\omega_{k})t]H'_{jk}(t)
\end{align}$$

- Suppose the perturbation is _small_, and the system is intially in state $\ket{0}$
$$c_{0}(0)=1\hspace{1.25cm}c_{j}(0)=0\;\;\;(j\neq 0)$$
- One can then _approximate_ by replacing $c_{k}$ with $c_{0}$:
$$\begin{align}
i\hbar \frac{dc_{j}}{dt}&=\exp[i(\omega_{j}-\omega_{0})t]H'_{j 0}(t) \\
c_{j}(t)&=\frac{1}{i\hbar}\int_{0}^{t} \exp[i(\omega_{j}-\omega_{0})t']H'_{j 0}(t')\, dt' 
\end{align}$$

- The _probability_ that there is a _transition_ $\ket{0}\to \ket{j}$ is given by:
$$P_{0\to j}(t)=|c_{j}(t)|^{2}$$
- Higher order approximations can be obtained by _iteration_ of the above
# Fermi's Golden Rule
- Consider a _Hermitian, monochromatic_ perturbation of the form:
$$\hat{H}'(t)=\hat{U}\exp(-i\omega t)+\hat{U}^{\dagger}\exp(i\omega t)$$

- Here, $\hat{U}^{\dagger}$ is _not necessarily Hermitian_, and _time-independent_
- Let $\omega$ be _positive_

- Substituting this into the formula for $c_{j}(t)$, one finds:
$$c_{j}(t)=-\frac{1}{\hbar}U_{k0}\frac{\exp[i(\omega_{j}-\omega_{0}-\omega)t]-1}{\omega_{j}-\omega_{0}-\omega}-\frac{1}{\hbar}U_{k0}^{\dagger}\frac{\exp[i(\omega_{j}-\omega_{0}+\omega)t]-1}{\omega_{j}-\omega_{0}+\omega}$$
- The matrix elements of $\hat{U}$:
$$U_{k0}=\braket{ k|\hat{U} |0  }\hspace{1.5cm} U_{k0}^{\dagger}=\braket{ k|\hat{U}^{\dagger} |0  } $$
## Absorption and emission probabilities
- Consider the _magnitude_ of the _first term_ of $c_{j}(t)$:
$$\displaylines{ |c_{j}(t)|^{2}=\frac{1}{\hbar^{2}}|U_{k0}|^{2}\frac{\sin^{2}[(\Delta\omega)t/2]}{(\Delta\omega/2)^{2}} \\\Delta\omega=\omega_{j}-(\omega_{0}+\omega)}$$
![[Monochromatic absorption probability.png]]
- The transition probability _peaks_ at $\omega_{0}+\omega \approx\omega_{j}$
- The _width_ of the peak also _narrows with time_

- Using the _limit_ of a long time:
$$\lim_{ t \to \infty } \frac{\sin^{2}(\alpha t)}{\alpha^{2}}=\pi t\delta(\alpha)=2\pi t\delta(2\alpha)$$
- One gets that the _transition rate_ for $\ket{0}\to \ket{k}$ is:
$$\Gamma(0\to k)=\frac{|c_{k}(t)|^{2}}{t}=\frac{2\pi}{\hbar}|U_{k0}|^{2}\delta(E_{k}-(E_{0}+\hbar\omega))$$
- This is _Fermi's Golden Rule_

- Therefore, with the appropriate $\omega$, the _perturbation_ $\hat{H}'(t)$ provides the _transition_ to $E_k$:
$$\hat{H}'(t)=\hat{U}\exp(-i\omega t)\implies E_{k}=E_{0}+\hbar\omega$$
- This is an _absorption_ as $E_k>E_0$

- Similarly, the _second term_ of the monochromatic perturbation is:
$$\displaylines{\hat{H}'(t)=\hat{U}^{\dagger}\exp(i\omega t)\implies E_{k}=E_{0}-\hbar\omega \\ \Gamma(0\to k)=\frac{|c_{k}(t)|^{2}}{t}=\frac{2\pi}{\hbar}|U_{k0}^{\dagger}|^{2}\delta(E_{k}-(E_{0}-\hbar\omega))}$$
- This corresponds to _emission_

## Continuum of states
- In many cases, there is a _continuum of available final states_ labelled by $E_k$
- Let there be a _density of final states_ $g(E_{k})$:
$$dN=g(E_{k})dE_{k}$$
- Then for perturbation $\hat{U}\exp(-i\omega t)$:
$$\begin{align}
\Gamma(0\to k)&=\frac{2\pi}{\hbar}\int |U_{k0}|^{2}\delta(E_{k}-(E_{0}+\hbar\omega))  \, g(E_{k})dE_{k} \\ &=\frac{2\pi}{\hbar}|U_{k0}|^{2}g(E_{k})
\end{align}$$
- This is the _total absorption rate_ to _all states_ of energy $E_{k}=E_{0}+\hbar\omega$

- Similarly, _total emission rate_ to states of energy $E_{k}=E_{0}-\hbar\omega$ is:
$$\Gamma(0\to k)=\frac{2\pi}{\hbar}|U_{k0}^{\dagger}|^{2}g(E_{k})$$

