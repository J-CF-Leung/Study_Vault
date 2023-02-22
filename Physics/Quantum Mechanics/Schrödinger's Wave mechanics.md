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

- The _centre of the wave packet propagates at the classical speed_ $v_g=p_0/m=\hbar k_0/m$
- The packet _spreads with time_:
$$(\Delta x)^2=\frac{a^2}{2}\left(1+\frac{\hbar^2 t^2}{m^2a^4}\right)$$
- This can be understood as combining _uncertainties for position and velocity in quadrature_, and using the _uncertainty principle_

