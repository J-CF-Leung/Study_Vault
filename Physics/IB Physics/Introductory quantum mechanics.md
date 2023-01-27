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
- Similar definition to the Hamiltonian in [[Topics in Classical Mechanics]]

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

## The Probability Current
- The normalisation condition is over _all space_:
$$\int_{-\infty}^\infty |\Psi(x)|^2\,dx=1 \hspace{1cm}\forall t$$
- Consider the probability of finding a particle within some _limited volume_ $V$:
$$\int_V \Psi^*\Psi\,dx=\int_V P\,dx$$
- Consider its _time-dependence_, with a factor to make things easier, and taking the _complex conjugate of the Schrödinger Equation_:
$$i\hbar\pd{}{t}\int_V \Psi^*\Psi\,dx=-\frac{\hbar^2}{2m}\int_V\left[\psi^*\pd{^2\Psi}{x^2}-\pd{^2\Psi^*}{x^2}\Psi\right]\,dx$$
- Then:
$$\begin{aligned}i\hbar\pd{}{t}\int_V \Psi^*\Psi\,dx&=-\frac{\hbar^2}{2m}\int_V\pd{}{x}\left[\Psi^*\pd{\Psi}{x}-\Psi\pd{\Psi^*}{x}\right]\,dx \\ &=-\frac{\hbar^2}{2m}\oint_{S_V}\left[\Psi^*\pd{\Psi}{x}-\Psi\pd{\Psi^*}{x}\right]\cdot d\bm{x}\end{aligned}$$
- Where the 1D version of the _divergence theorem_ is used for the second equality
- The latter integral is effectively _the sum of a flow at the end-points_ in 1D

- This allows the quantity in the brackets to be interpreted as a _probability current_ $\bm{J}$:
$$J(x,t)=\frac{\hbar}{2mi}\left[\Psi^*\pd{\Psi}{x}-\Psi\pd{\Psi^*}{x}\right]$$
- This leads to _continuity_:
$$\pd{P}{t}+\pd{J}{x}=0$$
- This continuity is _analagous to the travel of a particle through space_

# Piecewise-constant potentials
- Assumptions
	- Calculating _stationary states_, where $E$ is constant
	- Time-independent Schrödinger Equation

## Constant potential
- Let there be a _constant potential_ $V_0$
- The time-independent Schrödinger Equation is:
$$-\frac{\hbar^2}{2m}\frac{d^2\psi}{dx^2}=(E-V_0)\psi$$
- Analagous to $T=E-V$ in classical mechanics

- The _general solution_ is:
$$\displaylines{\psi(x)=A\exp(\pm ikx) \\ k=\sqrt{\frac{2m(E-V_0)}{\hbar^2}}}$$
- In the _classically possible_ regime, where $E>V_0$, $k$ is _real_
- In the _classically forbidden_ regime, where $E<V_0$, $k$ is _purely imaginary_, $k=i\kappa$

- Since the wave function should be normalisable and _not go to infinity_, the classically forbidden solution _exponentially decays_