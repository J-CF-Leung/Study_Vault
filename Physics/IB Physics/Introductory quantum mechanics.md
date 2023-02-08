>[!Quote]

# The birth of quantum mechanics

## The photoelectric effect
![[Photoelectric effect.png]]
- Let there be monochromatic light _incident on some electrode_ (the cathode)
- The light _gives energy to the electrons_, allowing them to escape
- By result, there will be a _photocurrent_ travelling between electrodes

- The energy needed to _release_ an electron is the _work function_ $W$
- After escaping the metal, there is still some _kinetic energy_
![[Photoelectric effect potential.png|400]]
- One can apply an _external voltage_ to either _accelerate or decelerate_ the electrons
- At some voltage $-V_0$, known as the _stopping voltage_, the _photocurrent vanishes_

![[Photoelectric effect behaviour.png]]
- The photocurrent is _dependent on intensity and frequency_
- If intensity is increased, _number of electrons emitted does not change_
	- Hence, _energy of each electron is independent of intensity_

- However, if light frequency is increased, _kinetic energy of the electrons increases_

- Conservation of energy:
$$\displaylines{\frac{1}{2}mv^2=eV_0=h\nu-W \\ V_0=\frac{h\nu}{e}-\frac{W}{e}}$$
- The _slope_ of the graph is _universal for all materials_

- From this, the conclusion was:
- Energy _can only be extracted in packets_
- The energy of each packet is _proportional to frequency_:
$$E=hf=\hbar\omega$$
- Here, $h$ is _Planck's constant_
- $\hbar$ is the _reduced Planck's constant_, given by $h/(2\pi)$

## Blackbody radiation
- A _perfect blackbody absorbs all radiation_, with no reflections 

- The _energy density_ of the radiation is given by the _density of states_ multiplies by the _energy of each state_
- Consider the _number of states_ with frequency range between $\nu$ and $\nu+d\nu$:
$$dn=N(\nu)\,d\nu=\frac{8\pi\nu^2}{c^3}d\nu$$
- From classical thermodynamics, the energy of each state is given by $k_BT$
- Hence, the _Rayleigh-Jeans Law_ gives:
$$\rho_E(\nu,T)\,d\nu=\frac{8\pi\nu^2}{c^3}k_BT\,d\nu$$
- From this, as _frequency increases_, _energy density increases without bound_
- This is known as the _ultraviolet catastrophe_
![[Blackbody radiation.png]]

- From this, Planck suggested that the energy is _quantised_ in intervals of $h\nu$
- These levels follow the _Boltzman distribution_
- Hence, the _average energy_ at frequency $\nu$ is:
$$\overline{\epsilon}=\frac{\sum_{n=0}^\infty nh\nu\exp(-nh\nu/k_BT)}{\sum_{n=0}^\infty\exp(-nh\nu/k_BT)}=\frac{h\nu}{\exp(-h\nu/k_BT)-1}$$
- Therefore, _high frequency states are relatively unoccupied_

- Hence:
$$\rho(\nu,T)=\frac{8h\pi\nu^3}{c^3}\frac{1}{\exp(-h\nu/k_BT)-1}$$
- This is _Planck's Law_
- It matched spectral measurements

- In the _low-frequency limit_, or if $h\to0$, the _Rayleigh-Jeans Law is regained_
- Hence, classical behaviour exists as some _limit_, this is known as the _Correspondence Principle_

## Quantisation and de Broglie's hypothesis
- From classical electromagnetism, light exists _as a continuous wave_
- From the above two experiments, it was concluded that electromagnetic radiation is _quantised_ in the form of _photons_, which are _wave packets_

- The _quantised energy_ $E=nh\nu$ is a property _of the photons_ (not the electrons in the photoelectric effect)

- The _de Broglie hypothesis_ states that _individual particles have wave-like properties_
- If the particle has momentum $\bm{p}$, it has the wavevector $\bm{k}$ related by:
$$\displaylines{p=h/\lambda \\\bm{p}=\hbar\bm{k}}$$

## Bohr's hydrogen atom
- According to classical electromagnetism, if _charged particles accelerate_, they _emit radiation and lose energy_
- Hence, if an electron is _orbiting around a nucleus_, they _must lose energy and the atom collapses_

- Bohr proposed that the electron can exist in _discrete, stable orbits_, corresponding to the _normal modes_ of the electron as a wave
- In order for an orbit with radius $r_n$ to be stable, it must satisfy:
$$2\pi r_n=n\lambda_n=nh/p_n$$
- Any mode not satisfying this will _destructively interfere_

- Therefore, the _angular momentum is quantised_:
$$L_n=n\hbar$$
- One can calculate the _total energy_:
$$E_n=-\frac{e^2}{8\pi\epsilon_0 r_n}=-\frac{m_ee^4}{8\epsilon_0^2h^2}\frac{1}{n^2}=-\frac{hcR}{n^2}$$
- Here, $R$ is the _Rydberg constant_:
$$R\equiv\frac{m_ee^4}{8\epsilon_0^2h^3c}$$
- The _velocity_ of the electron in the _first orbit_ can be written as $\alpha c$, where $\alpha$ is the _fine structure constant $\approx 1/137$_

- Therefore, the _atomic emission lines_ are discrete
- The emission line representing a transition from level $n$ to $m$:
$$\Delta E=hcR\left(\frac{1}{n^2}-\frac{1}{m^2}\right)$$
## Electron diffraction
- Let there be an _array_ of scatterers (e.g. atoms in a lattice)
- Let there be incident _particles or waves_, and scattering intensity can be recorded as a function of _angle to the normal of the plane_ $\theta$

- If there are incoming _particles_, there is no "interference" or collision between the particles, with _no maxima and minima_ in the intensity pattern

- If there is an incoming _wave_, an _interference pattern_ can be seen

- If the distance between the atoms is $d$, the _condition for constructive interference_ is given by _Bragg's law_:
$$d\sin\theta=n\lambda$$
- This allows $d$ to be measured, often using _X-rays_

- The _Davisson and Germer experiment_ confirmed that the same behaviour is seen from _electron beams_, accelerated by some voltage $V$
	- It was done on the $[111]$ plane of _nickel_
- The results _match Bragg's law with de Broglie's hypothesis_, using previously derived lattice spacing, with maximums seen at:
$$\sin\theta=\frac{h}{d\sqrt{2meV}}$$

## Conclusions
- In a _macroscopic scale_:
	- Physical objects (e.g. electrons) behave classically, as particles
	- Electromagnetic _radiation_ carries a _continuous spectrum_ of energy

- In a _microscopic scale_:
	- Physical objects show _wave behaviour_
	- Energy and momentum carried by waves is _quantised_

# Wavefunctions in free space
(Insert quote from Castelnovo here)

## The double-slit experiment
![[Double slit experinent.png]]
- Let $S_1$ be a _coherent source of photons_

- For _high intensity of light_, the results are consistent with classical optics, with an _interference pattern_

- For a stream of _classical particles_, the distribution would just have a _central maximum_

- When the experiment is done with a _low intensity electron beam_, where electrons go through the slit _one at a time_
- Plotting the _frequency of detection_ as a function of position after a long time, the _distribution matches the interference pattern_
- No matter how low the intensity or measurement time, the same behaviour can be seen

- This seems to imply that the behaviour of a particle can be described using a function that _interferes like a wave_
- The function itself is a _probability amplitude_, which behaves like a wave
- Its _modulus squared_/intensity gives the _probability density_

- The _deterministic_ description given by classical mechanics gives way to a _probabalistic_ description given by quantum mechanics
- The _wave function itself is deterministic_ (if the system is left alone) but _still only describes probabilities_ for measurement

## Forms of the wave function
### Plane waves
- The most simple form of a wave function is the _plane wave_
$$\psi(x,t)=A\exp[i(kx-\omega t)]$$
- The wave function has _amplitude and phase_, but _probability must be real_

- The probability of finding the particle in position range $x$ to $x+dx$ at time $t$ is:
$$P(x,t)\,dx=|\psi(x,t)|^2\,dx$$
- Since this is a _probability density_, it must be _normalised at all times_:
$$\int |\psi|^2\,dx=1$$

- If the range of space in which the particle can be found is _finite_, then the normalisation condition holds
- If not, one finds that there is _equal probability density everywhere for a plane wave_

- For a _non-relativistic particle_ with no surrounding potential:
$$E=\frac{p^2}{2m}=\frac{\hbar^2 k^2}{2m}=\hbar\omega$$
- This gives the _dispersion relation_ for a free quantum mechanical particle:
$$\omega=\frac{\hbar k^2}{2m}$$
- The _phase and group velocities_ are:
$$\displaylines{v_p=\frac{\omega}{k}=\frac{\hbar k}{2m} \\ v_g=\frac{d\omega}{dk}=\frac{\hbar k}{m}=v_\text{classical}}$$

- Plane waves are _useful for situations like the double slit experiment_, since it has _equal intensity everywhere_

### Wave packets
- In cases describing _individual particles_, one may need a _wave packet_:
$$\psi(x,t)=\frac{1}{\sqrt{2\pi}}\int_{-\infty}^\infty g(k)\exp[i(kx-\omega t)]\,dk$$
- Here, $\omega$ is _still a function of $k$_

- At $t=0$, $g(k)$ is simply the _[[Fourier series and transforms#Fourier transforms|Fourier transform]]_ of $\psi(x)$
- Inverting the Fourier transform:
$$g(k)=\frac{1}{\sqrt{2\pi}}\int_{-\infty}^\infty \psi(x)\exp[-ikx]\,dx$$
- $g(k)$ can be interpreted as the [[#The momentum representation|momentum wavefunction]]

### Gaussian wave packet
- For a Gaussian wave packet, the _momentum wave function_ is:
$$g(k)=\left(\frac{a^2}{\pi}\right)^{1/4}\exp\left[-a^2\frac{(k-k_0)^2}{2}\right]$$
- The corresponding _position wave function_ is:
$$\psi(x)=\left(\frac{1}{\pi a^2}\right)^{1/4}\exp(ik_0x)\exp\left[-\frac{x^2}{2a^2}\right]$$
- It is _already normalised_ due to Parseval's theorem

- It is a _plane wave carrier_ with wavenumber $k_0$, _modulated by a Gaussian envelope_

## Expectation values and the uncertainty relation
- The _expectation value_ of a position given the wavefunction is:
$$\mean{x}=\int x|\Psi(x,t)|^2\,dx$$
- The _variance_ in a quantity is:
$$(\Delta x)^2=\mean{x^2}-\mean{x}^2$$
- For the _Gaussian packet_ at $t=0$:
$$\mean{x}=0 \hspace{1cm} \mean{x^2}=\frac{a^2}{2} \hspace{1cm} \Delta x=\frac{a}{\sqrt{2}}$$
- Using the momentum wave function:
$$\mean{k}=k_0 \hspace{1cm} \mean{k^2}=\frac{1}{2a^2}+k_0^2 \hspace{1cm} \Delta k=\frac{1}{\sqrt{2}a}=\frac{1}{2\Delta x}$$
- This gives the _uncertainty relation_:
$$\Delta x\Delta p=\frac{\hbar}{2}$$
- _Heisenberg's uncertainty principle_ states:
$$\Delta x\Delta p\geq \frac{\hbar}{2}$$
- The Gaussian wave packet is a wavefunction of _minimum uncertainty_

## Time evolution
- Recall the _assembly of a wave packet from plane waves_ in time:
$$\psi(x,t)=\frac{1}{\sqrt{2\pi}}\int_{-\infty}^\infty g(k)\,\exp[i(kx-\omega t)]\,dk$$
- Here, $\omega$ _is a function of $k$_

- For a _narrow wave packet centred at $k_0$_, the frequency can be approximated by:
$$\displaylines{k\approx k_0+\delta k \\ \omega(k)\approx\omega(k_0)+\frac{d\omega}{dk}\Bigg|_{k=k_0}\delta k+\dots=\omega_0+v_g\delta k+\dots}$$
- Then, one can write $\psi(x,t)$ as:
$$\begin{aligned}\psi(x,t)&\approx \exp[i(k_0x-\omega t)]\frac{1}{\sqrt{2\pi}}\int_{-\infty}^\infty g(k)\exp[i(\delta kx-\delta\omega t)]\,d(\delta k) \\ &=\exp[ik_0(x-v_pt)]f(x-v_gt)\end{aligned}$$
- The _phase velocity_ characterises the travel of the _carrier wave's phase front_
- The _group velocity_ characterises the travel of the _envelope_

- If there is a _non-zero quadratic term_, then the envelope _changes shape and disperses_

### Time evolution and dispersion of the Gaussian wave packet
- The _dispersion relation in free space_:
$$\begin{aligned}\omega=\frac{\hbar k^2}{2m}&=\omega(k_0)+\frac{d\omega}{dk}\Bigg|_{k_0}\delta k+\frac{1}{2}\frac{d^2\omega}{dk^2}\Bigg|_{k_0}(\delta k)^2 \\&=\omega_0+\frac{\hbar k_0}{m}\delta k+\frac{\hbar}{2m}(\delta k)^2\end{aligned}$$

- The Gaussian wave packet _with dispersion_:
$$\displaylines{\psi(x,0)=\left(\frac{1}{\pi a^2}\right)^{1/4} \exp(ik_0x)\exp\left[-\frac{x^2}{2a^2}\right]\\g(k)=\left(\frac{1}{\pi a^2}\right)^{1/4}\exp\left[-\frac{a^2(k-k_0)^2}{2}\right]\\\psi(x,t)=\frac{1}{\sqrt{2\pi}}\int_{-\infty}^\infty g(k)\exp[i(kx-\omega t)]\,dk}$$
- With _great pain_, one obtains:
$$\psi(x,t)=\left(\frac{a^2}{4\pi}\right)^{1/4}\frac{1}{[a^2/2+i\hbar t/(2m)]^{1/2}}\,\exp[i(k_0x-\omega_0 t)]\exp\left\{-\frac{(x-\hbar k_0t/m)^2}{4[a^2/2+i\hbar t/(2m)]}\right\}$$
- The _probability density_ is:
$$|\Psi(x,t)|^2=\frac{1}{\pi^{1/2}[a^2+\hbar^2t^2/(m^2a^2)]^{1/2}}\exp\left\{-\frac{(x-\hbar k_0t/m)^2}{a^2+\hbar^2t^2/(m^2a^2)}\right\}$$

- The _centre of the wave packet propagate:s at the classical speed_ $v_g=p_0/m=\hbar k_0/m$
- The packet _spreads with time_:
$$(\Delta x)^2=\frac{a^2}{2}\left(1+\frac{\hbar^2 t^2}{m^2a^4}\right)$$
- This can be understood as combining _uncertainties for position and velocity in quadrature_, and using the _uncertainty principle_

## The momentum representation
- Recalling the expression for a generic wave packet:
$$\Psi(x,t)=\frac{1}{\sqrt{2\pi}}\int g(k)\,\exp[i(kx-\omega t)]\,dk$$
- _Absorbing the time exponential into $g$_, and using _de Broglie's relation_:
$$\Psi(x,t)=\frac{1}{\sqrt{2\pi\hbar}}\int g\left(\frac{p}{\hbar},t\right) \exp\left(\frac{ipx}{\hbar}\right)\,dp$$
- Defining:
$$\Phi(p,t)=\frac{1}{\sqrt{\hbar}}g(p/\hbar)\exp(-i\omega t)$$
- This is the _momentum representation of the wavefunction_
- Therefore:
$$\displaylines{\Psi(x,t)=\frac{1}{\sqrt{2\pi\hbar}}\int_{-\infty}^\infty \Phi(p,t)\exp(ipx/\hbar)\,dp \\ \Phi(p,t)=\frac{1}{\sqrt{2\pi\hbar}}\int_{-\infty}^\infty \Psi(x,t)\exp(-ipx/\hbar)\,dp}$$
- The _probability of observing a particle in the position range_ $x$ to $x+dx$:
$$P(x,t)\,dx=|\Psi(x,t)|^2\,dx$$
- The _probability of observing a particle with momentum in the range_ $p$ to $p+dp$:
$$P(p,t)dp=|\Phi(p,t)|^2\,dp$$

- From _Parseval's Theorem_, if $\Psi$ is normalised, $\Phi$ is also normalised

# The Schrödinger Equation ❤

## Free particle in one dimension
- Consider a _wave packet representing a free particle_
$$\displaylines{\Psi(x,t)=\frac{1}{\sqrt{2\pi}}\int g(k)\,\exp[i(kx-\omega t)]\,dk\\E=\hbar\omega=\frac{p^2}{2m} \hspace{1cm} p=\hbar k \hspace{1cm} \omega=\frac{\hbar k^2}{2m}}$$
- Consider the _partial derivatives of the wave function_:
$$\displaylines{\pd{\Psi}{t}=-i\omega\Psi \\ \pd{^2\Psi}{x^2}=-k^2\Psi}$$
- Using the dispersion relation:
$$-\frac{\hbar^2}{2m}\pd{^2\Psi}{x^2}=i\hbar\pd{\Psi}{t}$$
- This is the _Schrödinger Equation for a free particle in one dimension_

## General Schrödinger equation in one dimension
- Consider the derivatives for a _plane wave_:
$$\displaylines{\Psi(x,t)=A\exp[i(kx-\omega t)] \\ i\hbar\pd{\Psi}{t}=\hbar\omega\Psi=E\Psi \\ -i\hbar \pd{\Psi}{x}=\hbar k\Psi=p\Psi \\ -\frac{\hbar^2}{2m}\pd{^2\Psi}{x^2}=\frac{p^2}{2m}\Psi}$$
- These 3 operations can be considered _operators_:
$$\displaylines{\hat{E}\equiv i\hbar\pd{}{t} \\ \hat{p}=\frac{\hbar}{i}\pd{}{x} \\ \frac{\hat{p}^2}{2m}=-\frac{\hbar^2}{2m}\pd{^2}{x^2}}$$
- These operators "represent" _total energy_, _momentum_, and _kinetic energy_

- Adding the contribution of potential energy:
$$i\hbar\pd{\Psi}{t}=-\frac{\hbar^2}{2m}\pd{^2\Psi}{x^2}+V(x,t)\Psi(x,t)$$
- This is the _general time-dependent Schrödinger Equation in one dimension_

\- The right hand side can be written in terms of the _Hamiltonian_:
$$i\hbar\pd{\Psi}{t}=\hat{\Ham}\Psi$$
- In this case, the Hamiltonian operator is:
$$\hat{\Ham}=\frac{\hat{p}^2}{2m}+\hat{V}$$
- Similar definition to the Hamiltonian in [[Newtonian dynamics and non-inertial frames]]

- All of these operators are _linear_

## Time-independent Schrödinger Equation
- Take a _time-independent potential_:
$$V=V(x)$$
- The wave function becomes _separable_:
$$\Psi(x,t)=T(t)\psi(x)$$
- Substituting into the 1D Schrödinger Equation and dividing through by $\Psi$:
$$\frac{i\hbar}{T}\frac{dT}{dt}=\frac{1}{\psi}\left[-\frac{\hbar^2}{2m}\frac{d^2\psi}{dx^2}+V(x)\psi(x)\right]=E$$
- From this, the 2 equations are:
$$\displaylines{T(t)=A\exp\left(-\frac{iEt}{\hbar}\right) \\ \Ham\psi=-\frac{\hbar^2}{2m}\frac{d^2\psi}{dx^2}+V(x)\psi(x)=E\psi(x)}$$
- The second equation is the _Time-independent Schrödinger Equation_
- Therefore, the wave function is:
$$\Psi(x,t)=\psi(x)\exp\left(-\frac{iEt}{\hbar}\right)$$
- The _normalisation factor is absorbed_:
$$\displaylines{|\Psi(x,t)|^2=|\psi(x)|^2 \\ \int|\psi(x)|^2\,dx=1}$$
- Therefore, if $V$ is time-independent, then the solution $\Psi=T\psi$ is _stationary_, since the probability density is also time-independent

## In three dimensions
- The full Hamiltonian becomes:
$$\hat{\Ham}=\frac{1}{2m}(\hat{p}_x^2+\hat{p}_y^2+\hat{p}_z^2)+\hat{V}=-\frac{\hbar^2}{2m}\nabla^2+\hat{V}$$
- The _time-dependent Schrödinger Equation remains the same_:
$$\Ham\Psi=i\hbar\pd{\Psi}{t}$$
- The time-dependent part of the wavefunction remains the same
- The time-independent equation becomes:
$$-\frac{\hbar^2}{2m}\nabla^2\psi+V(\bm{r})\psi(\bm{r})=E\psi(\bm{r})$$

## The Probability Current
- The normalisation condition is over _all space_:
$$\int_{-\infty}^\infty |\Psi(x)|^2\,dx=1 \hspace{1cm}\forall t$$
- Consider the probability of finding a particle within some _limited volume_ $V$:
$$\int_V \Psi^*\Psi\,dx=\int_V P\,dx$$

### Proof in 1 dimension
- Consider its _time-dependence_, with a factor to make things easier, and taking the _complex conjugate of the Schrödinger Equation_:
$$i\hbar\pd{}{t}\int_V \Psi^*\Psi\,dx=-\frac{\hbar^2}{2m}\int_V\left[\psi^*\pd{^2\Psi}{x^2}-\pd{^2\Psi^*}{x^2}\Psi\right]\,dx$$
- Then:
$$\begin{aligned}i\hbar\pd{}{t}\int_V \Psi^*\Psi\,dx&=-\frac{\hbar^2}{2m}\int_V\pd{}{x}\left[\Psi^*\pd{\Psi}{x}-\Psi\pd{\Psi^*}{x}\right]\,dx \\ &=-\frac{\hbar^2}{2m}\oint_{S_V}\left[\Psi^*\pd{\Psi}{x}-\Psi\pd{\Psi^*}{x}\right]\cdot d\bm{x}\end{aligned}$$
- Where the 1D version of the _divergence theorem_ is used for the second equality
- The latter integral is effectively _the sum of a flow at the end-points_ in 1D

- This allows the quantity in the brackets to be interpreted as a _probability current_ $\bm{J}$:
$$\begin{aligned}J(x,t)&=\frac{\hbar}{2mi}\left[\Psi^*\pd{\Psi}{x}-\Psi\pd{\Psi^*}{x}\right] \\ &=\Re\left[\Psi^*\frac{\hbar}{mi}\pd{\Psi}{x}\right]\end{aligned}$$
- This leads to _continuity_:
$$\pd{P}{t}+\pd{J}{x}=0$$
- This continuity is _analagous to the travel of a particle through space_

- For a _travelling plane wave_:
$$\displaylines{\psi=A\exp[i(kx-\omega t)] \\ J=\frac{\hbar k}{m}|A|^2}$$
- Here, $\hbar k/m$ is the _classical speed_

- If $k$ is _imaginary_ (i.e. an evanescent wave), $J=0$

### In three dimensions
- Following a similar proof, the probability current is:
$$\bm{J}(\bm{r},t)=\frac{\hbar}{2mi}\left[\Psi^*\nabla\Psi-\Psi\nabla\Psi^*\right]=\Re\left[\Psi^*\frac{\hbar}{mi}\nabla\Psi\right]$$
- Similarly, continuity becomes:
$$\pd{}{t}|\Psi|^2+\nabla\cdot\bm{J}=0$$
# Unbounded particles in piecewise-constant potentials
- The wave function (or at least the probability current) behaves similarly to [[Waves#Boundaries: reflection and transmission|classical waves]]
- It is _not normalisable_ into a single particle, and should be interpreted as a _beam_

## Assumptions and boundary conditions
- Assumptions
	- Calculating _stationary states_, where $E$ is constant
	- Time-independent Schrödinger Equation

- _Physicality_: $\psi(x)$ is _finite everywhere_
- For a _finite potential_, inspection of the Schrödinger Equation yields that:
	- $\psi(x)$ is _continuous everywhere_
	- $d\psi/dx$ is _continuous everywhere_

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
- [[#The Probability Current]] in each region, for each travelling direction:
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
- When studying a particle _close to the ground state_, it is _near the bottom of a potential well_
- The potential can be _approximated as harmonic_

- Classcally, the particle _oscillates_ with classical frequency $\omega$
- The potential can be written as:
$$V(x)=\frac{1}{2}m\omega^2x^2$$
- The time-independent Schrödinger equation is then:
$$\frac{d^2\psi}{dx^2}+\left[\frac{2mE}{\hbar^2}-\frac{m^2\omega^2x^2}{\hbar^2}\right]\psi=0$$
### Solving the damn thing
- First step is to convert to _dimensionless variables_:
$$q=\sqrt{\frac{m\omega}{\hbar}}x\hspace{1cm} \epsilon=\frac{2E}{\hbar\omega}$$
- The equation then becomes:
$$\frac{d^2\psi}{dq^2}+(\epsilon-q^2)\psi=0$$
- The next step is to look at _limiting behaviour_, where $q^2>>\epsilon$:
$$\displaylines{\frac{d^2\psi}{dq^2}-q^2\psi\approx 0 \\ \psi\approx A\exp\left(-\frac{q^2}{2}\right)}$$
- Then, one can _propose an exact solution_:
$$\psi=H(q)\exp\left(-\frac{q^2}{2}\right)$$
- One will find that $H(q)$ satisfies _Hermite's equation_:
$$\frac{d^2H}{dq^2}-2q\frac{dH}{dq}+(\epsilon-1)H(q)=0$$
- Propose a _power series solution_
- From the normalisability of the wave function, $H(q)$ _must eventually terminate_, therefore $\epsilon$ can only take _discrete values_
- $H_n(q)$ are the [[Special functions and orthogonal relations#Hermite polynomials|Hermite polynomials]], given by the _Rodrigues formula_:
$$H_n(q)=(-1)^n\exp\left(q^2\right)\frac{d^n}{dq^n}\exp\left(-q^2\right)$$
- Here, $n=(\epsilon-1)/2$. therefore the energies are given by:
$$E_n=\left(n+\frac{1}{2}\right)\hbar\omega$$

- Since the Hermite polynomials are _orthogonal_, the normalising constants can be found
- Collecting these results, the wave functions can be written as:
$$\psi_n(x)=\frac{1}{\sqrt{\pi^{1/2}2^n(n!)}}H_n\left[\sqrt{\frac{m\omega}{\hbar}}x\right]\exp\left(-\frac{m\omega}{2\hbar}x^2\right)$$
- From the properties of the Hermite polynomials, the states are _alternatively even or odd_

### Properties
- From the uncertainty principle, there is _zero-point energy_ $\hbar\omega/2$
- The energy spectrum is _discrete_
- All energy levels are _equally spaced_, with spacing $\hbar\omega$

- There is _finite probability_ of finding the particle _in the classically forbidden region_
- This probability _decreases as $n$ increases_
- Therefore, at _high energies_, the particle is _more confined and acts classically_


## Parity of states
- One can define a _parity operator_, which _reflects_ a wave function:
$$\hat{P}\psi(x)=\psi(-x)$$
- Example: for the _simple harmonic oscillator_, the states are _alternatively even or odd_
$$\displaylines{\hat{P}\psi_n=(-1)^n\psi_n \\ n=0,1,2,\dots}$$
- _Ground states are often even_, as the number of nodes is _minimised_

- In this case, $\psi_n$ is an _eigenstate_ of $\hat{P}$, with eigenvalue $\pm1$
- Hence, $\psi_n$ is a _simultaneous eigenstate_ of $\hat{P}$ and $\hat{H}$, or in other words, the two operators _commute_
- For this to be true, _the potential must be even_:
$$V(x)=V(-x)\iff |\psi(x)|^2=|\psi(-x)|^2$$
- For a _symmetric potential_, the wave function must be _even or odd_

- For the _infinite square well_, _odd orders_ give _even parities_, and vice versa

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

