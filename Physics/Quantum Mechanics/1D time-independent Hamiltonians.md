- The [[Fundamental concepts of quantum mechanics#Time-independent Hamiltonians and stationary states|time-independent Schrödinger equation]] solves for the eigenkets of the Hamiltonian:
$$\Ham\ket{E}=E\ket{E}$$
- The resultant [[Fundamental concepts of quantum mechanics#The time-evolution operator|time-evolution operator]] and wave function become:
$$\teo = \sum_n\ket{E_n}\bra{E_n}\exp(-iE_nt/\hbar)=\int\ket{E}\bra{E}\exp(-iEt/\hbar)\,dE$$
$$\ket{\Psi(t)} =\sum_n\ket{E_n}\braket{E_n|\Psi_0}\exp(-iE_nt/\hbar) =\int \ket{E}\braket{E|\Psi_0}\exp(-iEt/\hbar)\,dE$$

# Characteristics of the wave function
- The energy $E$ has to be real, and larger than minimum of $V(x)$ for $\wv$ to be normalisable
- The eigenfunctions of $\hat{\Ham}$ can always be taken to be real

- If $V(x)$ is an even function, then $\braket{x|\Psi}$ can always be taken to be even or odd
	- In other words, the wave function _is an eigenfunction of the parity operator_

## Continuity
- Consider the 1D time-independent Schrödinger equation in the position basis:
 $$-\frac{\hbar^2}{2m}\frac{d^2\psi}{dx^2}+V\psi=E\psi$$
 $$\frac{d^2\psi}{dx^2}=-\frac{2m(E-V)}{\hbar^2}\psi$$
	- If there is an _abrupt but finite jump_ in $V$ (and therefore $\psi''$), $\psi'$ _will still be continuous_
	- If the jump is _infinitely large_ (e.g. Dirac delta), $\psi'$ is discountinuous but $\psi$ is still continuous

## Boundedness
- _Classically_, a particle is _bound_ if its energy is _smaller than the maximum potential over a finite region of space that contains the particle_
- Quantum mechanically, if a particle is _unbound_, there is a _continuum of states_ with energy $E$ within some range
- If the particle is _bound_, they can only have a _discrete spectrum_ of energies $E$
- The wave-function will also be _normalisable_:
$$\int |\psi(\bm{r})|^2\,d^3\bm{r}<\infty$$

# The free particle
- From an older perspective: [[Schrödinger's Wave mechanics]]
- The Hamiltonian and time-independent Schrödinger equation for a free particle is:
$$\Ham=\frac{P^2}{2m}$$
$$\Ham\ket{E} = \frac{P^2}{2m}\ket{E}=E\ket{E}$$
- Any eigenvector of $P$ is also an eigenvector of $\Ham$, therefore allowed values of momentum are:
$$p=\pm\sqrt{2mE}$$
- Difference with classical case: degeneracy of energy leads to a subspace of eigenvectors
$$\ket{E} = \beta\Ket{p=+\sqrt{2mE}}+\gamma\Ket{p=-\sqrt{2mE}}$$
	- One particle with energy $E$ can be observed to be moving left or right
- Due to the degeneracy, it is more appropriate to _label states and construct $\teo$ using $p$_:
$$\begin{aligned} \teo(t) &= \int_{-\infty}^\infty \ket{p}\bra{p}\exp(-ip^2t/2m\hbar)\,dp \\ &= \sum_{\alpha=\pm} \int_0^{\infty} \frac{m}{\sqrt{2mE}} \ket{E,\alpha}\bra{E,\alpha} \,\exp(-iEt/\hbar)\, dE \end{aligned}$$
- As the $x$-space momentum eigenfunction is $\exp(ipx/\hbar)/\sqrt{2\pi\hbar}$, the _energy eigenfunction_ is:
$$\braket{x|E} = \beta\frac{\exp(i\sqrt{2mE}x/\hbar)}{\sqrt{2\pi\hbar}} +\gamma\frac{\exp(-i\sqrt{2mE}x/\hbar)}{\sqrt{2\pi\hbar}}$$
- The stationary state in the position space is:
$$\braket{x|\Psi_E(t)}=\beta\frac{\exp[ik(x-\hbar kt/2m)]}{\sqrt{2\pi\hbar}}+ \gamma\frac{\exp[(-ik(x+\hbar kt/2m)]}{\sqrt{2\pi\hbar}}$$
	- $p=\hbar k$
	- The _phase velocity_ of a point on the wave is $\hbar k/2m$, or half of the classical velocity
- As for the [[Path integrals in quantum mechanics#The propagator|propagator]], it can be constructed from $\teo$:
$$K(x,t,x',t_0)=\braket{x|\teo(t,t_0)|x'}=\sqrt{\frac{m}{2\pi i\hbar t}} \exp\left[\frac{im(x-x')^2}{2\hbar t}\right]$$
- In _three dimensions_, the free particle eigenvector is:
$$\braket{\bm{r}|\bm{p}}=\frac{1}{\sqrt{2\pi\hbar}}\exp\left(i\frac{\bm{p}\cdot\bm{r}}{\hbar}\right)$$

### Wave packets and the group velocity
- The stationary states are _non-normalisable, and cannot represent physical particles_
	- They can instead be interpreted as a _beam_
- Instead, a linear combination of the stationary states has to be used:
$$\begin{aligned}\braket{x|\Psi(t)}&=\frac{1}{\sqrt{2\pi\hbar}}\int_{-\infty}^\infty\phi(p) \exp\left[\frac{ip}{\hbar}x-\frac{ip^2}{2m\hbar}t\right]\,dp \\ &= \int_{-\infty}^\infty \braket{x|p}\braket{p|\Psi(0)}\exp\left(-\frac{ip^2}{2m\hbar}t\right)\,dp\end{aligned}$$
- This _wave packet_ has a range of energies and phase velocities, and can represent a particle, as long as it is normalisable
- The velocity of the particle represented by the wave packet is the [[Waves#Group velocity|group velocity]]:
$$v_g=\frac{d\omega}{dk}=\frac{\hbar k}{m}=v_{clas}$$
- The momentum-space wave function can be found with transforming $\braket{x|\Psi(0)}$:
$$\braket{p|\Psi(0)}=\frac{1}{\sqrt{2\pi\hbar}}\int_{-\infty}^\infty \exp(-ipx/\hbar)\braket{x|\Psi(0)}\,dx$$

### The Gaussian wave packet
>[!quote]
>There is an unwritten law which says that the derivation of the free-particle propagator be followed by its application to the Gaussian packet. Let us follow this tradition.
>-Ramamurti Shankar

- Consider the initial wave function in position space:
$$\braket{x|\Psi(0)}=\frac{1}{(\pi\Delta^2)^{1/4}}\exp\left(ip_0x/\hbar\right) \exp\left(-\frac{x^2}{2\Delta^2}\right)$$
- The time evolution of the position-space wave function is:
$$\braket{x|\Psi(t)}=\left[\sqrt{\pi}\left(\Delta+\frac{i\hbar t}{m\Delta}\right)\right]^{-1/2}\exp\left[-\frac{(x-p_0t/m)^2}{2\Delta^2(1+i\hbar t/m\Delta^2)}+\frac{ip_0}{\hbar}\left(x-\frac{p_0t}{2m}\right)\right]$$

- The corresponding position probability density is:
$$|\braket{x|\Psi}|^2=\frac{1}{\sqrt{\pi}(\Delta^2+\hbar^2t^2/m^2\Delta^2)^{1/2}} \exp\left[-\frac{(x-p_0t/m)^2}{\Delta^2+\hbar^2t^2/m^2\Delta^2}\right]$$

- The mean position and the width become:
$$\displaylines{\braket{X}=\frac{p_0t}{m}=\frac{\braket{P}t}{m} \\ \Delta X(t)=\frac{\Delta}{\sqrt{2}}\left(1+\frac{\hbar^2t^2}{m^2\Delta^4}\right)^{1/2}}$$
- This can be understood as combining _uncertainties for position and velocity in quadrature_, and using the _uncertainty principle_

- The mean momentum is constant, with $\braket{P}=p_0$ and $\Delta P=\hbar/(\sqrt{2}\Delta)$
	- A small spread in position indicates a large spread in momentum

- The wave packet disperses, but maintains its group velocity

# Unbound states in piecewise-constant potentials

## Constant potential
- Let there be a _constant potential_ $V_0$
- The time-independent Schrödinger Equation is:
$$-\frac{\hbar^2}{2m}\frac{d^2\psi}{dx^2}=(E-V_0)\psi$$
- Analagous to $T=E-V$ in classical mechanics

- The _general solution_ is:
$$\displaylines{\psi(x)=A\exp(\pm ikx) \\ k=\sqrt{\frac{2m(E-V_0)}{\hbar^2}}}$$
- In the _classically possible_ regime, where $E>V_0$, $k$ is _real_
- Combining this with $T(t)$, the _positive_ solution yields a wave with phase $(kx-\omega t)$, hence travelling to the _right_

- In the _classically forbidden_ regime, where $E<V_0$, $k$ is _purely imaginary_, $k=i\kappa$
- For the sake of physicality, the classically forbidden solution _exponentially decays_:
$$\displaylines{\psi(x)=A\exp(-\kappa x) \\ \kappa=\sqrt{\frac{2m(V_0-E)}{\hbar^2}}}$$

## Single step potential
- Let there be 2 regions:
	- In region $I$, there is _zero potential_
	- In region $II$, $V=V_0$
![[Potential step.png]]
- Let there be an _incident wave_ coming from the negative $x$ direction
- Defining two wavenumbers:
$$k_1=\frac{\sqrt{2mE}}{\hbar}\hspace{1cm} k_2=\frac{\sqrt{2m(E-V_0)}}{\hbar}$$

- In region $I$:
$$\Psi_1(x,t)=A\exp[i(k_1x-\omega t)]+rA\exp[-i(k_1x+\omega t)]$$
- In region $II$:
$$\Psi_2(x,t)=tA\exp[i(k_2x-\omega t)]$$
- Applying the _boundary conditions for continuity_:
$$r=\frac{k_1-k_2}{k_1+k_2} \hspace{1cm} t=\frac{2k_1}{k_1+k_2}$$
- [[Fundamental concepts of quantum mechanics#Probability flow|The probability current]] in each region, for each travelling direction:
$$\displaylines{J_1^+=\frac{\hbar k_1}{m}|A|^2 \\ J_1^-=|rA|^2\frac{\hbar k_1}{m}=|A|^2\left|\frac{k_1-k_2}{k_1+k_2}\right|^2\frac{\hbar k_1}{m} \\ J_2^+=|tA|^2\frac{\hbar k_2}{m}=|A|^2\left|\frac{2k_1}{k_1+k_2}\right|^2\frac{\hbar k_2}{m}}$$
- It can be checked that it is _conserved across the boundary_, $J_1^+-J_1^-=J_2^+$
- Only _valid for travelling wave_, or $k_2\in\mathbb{R}$
- If $E<V_0$, $J_2^+=0$

- The _reflection and transmission coefficients_ are:
$$\displaylines{R=\frac{J_1^-}{J_1^+}=|r|^2 \hspace{1cm} T=\frac{J_2^+}{J_1^+}=|t|^2\frac{k_2}{k_1}\\ R+T=1}$$
### Downward step
- If $V_0<0$, then $k_2>k_1$, indicating an _increase in kinetic energy and momentum_
- For this case:
	- $r<0$ and real, meaning there is a _$\pi$ phase shift upon reflection_
	- $t>0$ and real, so the _transmitted wave is in phase with incident wave_
- The reflection is _relatively small_
- _Classically_, reflection _would not occur_ due to lack of confinement
![[Downward step.png]]
	- Left: Blue- $|\Psi|^2$, Green- $\Re(\Psi)$, Red- $\Im(\Psi)$
	- Right: Blue - Incident flux, Green - Transmitted flux, Red - Reflected flux

### Upward step: Sufficient energy
- If $V_0>0$, then $k_2<k_1$, indicating a _decrease in kinetic energy and momentum_
- $r,t>0$ and real, indicating both reflected and transmitted waves are _in phase with incident wave_

- As with the downward step, _reflection is relatively small_ since the particle is _not classically confined_
![[High energy upward.png]]

### Upward step: Classically forbidden
- If $0<E<V_0$, then $k_2$ becomes _imaginary_ and the wave is _evanescent_
- The _transmitted_ wave function is:
$$\psi_2(x,t)=\frac{2k_1}{k_1+i\kappa _2}\exp(-\kappa_2x)$$
- It is _non-zero_ but still _exponentially decays_
- While the wavefunction decays with _characteristic length_ $1/\kappa_2$, the _probability density_ has characteristic length $1/(2\kappa_2)$
- This _violates classical mechanics_ as the particle is found in a region where $V>E$

- In this case, $R=1$ and $T=0$ since there is _no probability flow into the barrier_

![[Low energy upward.png]]

- If $V_0\to\infty$, $r$ _approaches_ $-1$ and $t$ approaches 0
- The _reflected wave becomes sinusoidal_
![[Upward limiting case.png]]

### Tunnelling via uncertainty
- _Tunnelling into a classically forbidden region_ can be understood with a more "hand-wavy" argument
- The [[#Expectation values and the uncertainty relation|Uncertainty Principle]] states:
$$\Delta p_x\geq \frac{\hbar}{2\Delta x}$$
- This gives an _uncertainty in energy_:
$$\Delta E\geq \frac{\hbar^2}{8m(\Delta x)^2}$$
- If $0<E<V_0$ and $\Delta E>V_0-E$, there is a _probability that the particle has a measured energy higher than $V_0$_
- From this, one gets:
$$\Delta x\leq \frac{1}{2}\sqrt{\frac{\hbar^2}{2m(V_0-E)}}=\frac{1}{2\kappa_2}$$
- This corresponds to the _penetration depth_



## Potential barrier
- The potential $V(x)$ is:
$$V(x)=\begin{cases}0 & x<0 \\ V_0 &0<x<a \\ 0 &x>a \end{cases}$$
![[Potential barrier.png]]
- For regions 1 and 3, where $x<0$ or $x>a$:
$$\displaylines{\psi=A\exp(\pm ik_1x) \\ k_1=\frac{\sqrt{2mE}}{\hbar}}$$
- For region 2, in the barrier:
$$\displaylines{\psi=A\exp(\pm ik_2x) \\ k_2=\frac{\sqrt{2m(E-V_0)}}{\hbar}}$$
- For a wave _incoming from the left_, the wave-functions are:
$$\begin{aligned}\Psi_1 &= A\left[\exp(ik_1x)+r\exp(-ik_1x)\right]\exp(-i\omega t) \\ \Psi_2 &= A[\alpha \exp(ik_2x)+\beta \exp(-ik_2x)]\exp(-i\omega t) \\ \Psi_3&= A[t\exp(ik_1x)]\exp(-i\omega t)\end{aligned}$$
- With _great pain_, applying the _boundary conditions_:
$$\displaylines{t=\left[\frac{2k_1k_2}{2k_1k_2\cos(k_2a)-i\left(k_1^2+k_2^2\right)\sin(k_2a)}\right]\exp(-ik_1a) \\ r=\frac{(k_1^2-k_2^2)\sin(k_2a)}{2ik_1k_2\cos(k_2a)+(k_1^2+k_2^2)\sin(k_2a)}}$$
- As one expects, $R+T=1$

### The potential well
- In this case, the potential follows the definition above with $V_0<0$
- Therefore, $k_2>k_1$
- The probability density of finding the particle is _lower in the well_
	- Classically, the particle is _spending less time in the well_
![[Potential well scattering.png]]

### Low barrier
- As $k_2<k_1$, the particle travels _slower at the barrier_
![[Low potential barrier.png]]
### High barrier and tunnelling
- If the barrier is higher than the actual energy, the probability density _decays exponentially inside the barrier_
- However, on the other side of the barrier, _a wave with very small amplitude is still transmitted_
- This is a _purely quantum phenomenon_ 
![[High potential barrier tunneling.png]]
- $k_2$ becomes imaginary, and one can define:
$$\kappa_2=\frac{\sqrt{2m(V_0-E)}}{\hbar}$$
- For a _thick barrier_, such that $\sinh(\kappa_2a)\approx\cosh(\kappa_2a)\approx\exp(\kappa_2a)$:
$$T\approx\frac{16k_1^2\kappa_2^2}{k_1^2+\kappa_2^2}\exp(-\kappa_2a)$$
- Transmission _falls exponentially with $a$_

### Resonances and analogies to classical behaviour
![[Barrier R and T.png]]
- For _small energies_, it approaches classical behaviour as _most of the wave is reflected_
	- $T$ falls approximately exponentially with increasing $V_0$
- For $k_2a=n\pi$, _quantum resonances_ occur with $T=1$
	- One can imagine it as _the two reflected waves destructively interfering_

# Bound particles
- _Classically_, a particle is _bound_ if its energy is _smaller than the maximum potential over a finite region of space that contains the particle_
- Quantum mechanically, if a particle is _unbound_, there is a _continuum of states_ with energy $E$ within some range
- If the particle is _bound_, they can only have a _discrete spectrum_ of energies $E$

## The infinite square well
- Consider the potential:
$$V(x)=\begin{cases}V_0 &|x|<a/2 \\ +\infty &|x|>a/2\end{cases}$$
- In this case, the particle is _always bound_
- The potential is _symmetric_ in this coordinate system, meaning $|\Psi|^2$ _must also be symmetric_ (i.e. $\psi$ is _even or odd_)

- The _continuity_ of $\psi$ _still holds_
- $\psi'$ can be _discontinuous_ since from the Schrödinger Equation, $\psi''$ is _infinite_ at the boundary of the well
- Due to the potential, $\psi(x)=0$ for $|x|>a/2$
- From continuity of $\psi$:
$$\psi(\pm a/2)=0$$
- _Within the well_, the Schrödinger equation gives:
$$\frac{d^2\psi}{dx^2}+\frac{2m(E-V_0)}{\hbar^2}\psi=0$$

### Energy less than or equal to minimum potential
- If $E<V_0$, then the wave function contains _real exponentials_
- From the _boundary conditions_, the wave function _cannot exist_

- If $E=V_0$, this gives a _linear_ wave function
- From the _boundary conditions_, this wave function _cannot exist_
- Classically, this corresponds to the _stationary particle_
- Quantum mechanically, this violates the _uncertainty principle_

### Energy above the bottom of the well
- If $E>V_0$, applying the _boundary conditions_ and _normalising_:
$$\psi_n(x)=\begin{cases} \sqrt{\frac{2}{a}}\cos(k_nx) &\text{for $n$ odd} \\ \sqrt{\frac{2}{a}}\sin(k_nx) &\text{for $n$ even}\end{cases}$$
- The boundary conditions also require:
$$k_n=\frac{n\pi}{a}$$
- This gives _discrete energy levels_:
$$E_n-V_0=\frac{(\hbar n\pi)^2}{2ma^2}$$
- The _lowest energy level is above $V_0$_, meaning there is some _zero point energy_, and the particle _cannot be stationary_
- Generally, if a particle is _confined_, the energy _must be discrete_ to satisfy boundary conditions

![[Particle in a box.png]]
- Taking the _inner product_ of the wave functions, one finds that they are _orthogonal_:
$$\int \psi_m^*\psi_n\,dx=\delta_{mn}$$
- Unlike the classical case, the _probability distribution is not uniform_

- The _number of nodes increases with $n$_
- Nodes are associated with _quick change in $\psi$_, which raises $\psi''$

## The finite square well
- Consider a _finite square potential_:
$$V(x)=\begin{cases}-V_0 &|x|<a/2 \\ 0 &|x|>a/2\end{cases}$$
- For $E>0$, this has been explored as a special case of the [[#Potential barrier]]
- For $E<-V_0$, it is obvious that _no solution is possible_

- For $-V_0<E<0$, there is a _finite spectrum of solutions_
- Let $E=-E_0$

- The wave function is:
$$\psi(x)=\begin{cases}A\sin(kx)+B\cos(kx) &\text{for }|x|<a/2 \\ C\exp(\kappa x)+D\exp(-\kappa x)&\text{for }|x|>a/2\end{cases}$$
- The wave-numbers are:
$$k=\frac{\sqrt{2m(V_0-E_0)}}{\hbar} \hspace{1cm} \kappa=\frac{\sqrt{2mE_0}}{\hbar}$$
- For the wave-function to be _normalisable_:
$$\psi(x)=\begin{cases}C\exp(\kappa x)&\text{for }x<-a/2 \\A\sin(kx)+B\cos(kx) &\text{for }|x|<a/2 \\ D\exp(-\kappa x)&\text{for }x>a/2\end{cases}$$
- At this point, it is useful to _define the parameters_:
$$X=\frac{ka}{2} \hspace{1cm} Y=\frac{\kappa a}{2}$$
- By _matching boundary conditions_, and using the fact that the wave function _must be even or odd_, one can find _two branches of solutions_:
$$\displaylines{\text{Even solution} \hspace{1cm} A=0 \hspace{0.75cm} C=D \hspace{0.75cm} X\tan (X)=Y \\ \text{Odd solution} \hspace{1cm} B=0 \hspace{0.75cm} C=-D \hspace{0.75cm} -X\cot (X)=Y}$$
- From the _definitions_ of the wave-numbers, one finds:
$$X^2+Y^2=\frac{mV_0a^2}{2\hbar^2}$$
- This forms a _circle in $X-Y$ space_, which is _set by the parameters of the system_
- Therefore, $X$ and $Y$, and therefore the energy, can be found _graphically_:
![[Finite well solutions.png]]
- The energies are:
$$E_n=-\frac{\hbar^2\kappa^2}{2m}=-\frac{2\hbar^2Y_n^2}{ma^2}=-\frac{Y_n^2V_0}{X_n^2+Y_n^2}$$
### Comments on solutions
- The _number of solutions in each branch depends on $V_0$ and $a$_
- The _even branch_ will always have _at least one_ solution _no matter how shallow the well is_
- The _odd branch may not always have a solution_ for a shallow well 

- The _overall_ spectrum of this potential has both a _continuous_ (scattering) and _discrete_ (bound) part
- Like the infinite well, _probability distribution is not uniform_
- There is a _non-zero probability_ of finding a particle _in the classically forbidden region_

- As the potential well _gets deeper_, the solutions and energies _approach those of the infinite well_

## The 1D quantum harmonic oscillator
- So good it needs [[Quantum Harmonic Oscillator|its own note!]]

## The Correspondence Principle
- The principle states that _at high quantum numbers, quantum mechanics predicts the same results as classical mechanics_

- Consider the _even-parity solutions of the infinite square well_:
$$\psi_n\propto\left[\exp\left(-\frac{in\pi x}{a}\right)+\exp\left(\frac{in\pi x}{a}\right)\right]$$
- One can evaluate the [[#The momentum representation|momentum representation]] of the wave-function as a _convolution_:
$$\phi_n(p)\propto\left[\delta\left(\frac{p}{\hbar}-\frac{n\pi}{a}\right)+\delta\left(\frac{p}{\hbar}+\frac{n\pi}{a}\right)\right]\otimes \sinc\left(\frac{pa}{2\hbar}\right)$$
- This gives _two sinc-shaped spikes_ at $p=\pm n\hbar\pi/a$
- There is an _equal chance_ of detecting the particle in _both directions_
- The _width_ of the spikes is _independent of $n$_
- Hence, as $n$ increases, the _uncertainty of $p$ decreases_
- So, it gets _more likely to detect the momentum at the particle at the classical momentum_ $p_n\approx\sqrt{2mE_n}$

- In terms of Ehrenfest's Theoem: [[Fundamental concepts of quantum mechanics#Expectation values and the classical limit|The classical limit]]

# Other potentials

## The Delta Function potential