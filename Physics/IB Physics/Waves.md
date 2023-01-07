#IB_Natsci

## The wave equation
- Waves transport energy and information without _bulk_ translation of the medium

- The _non-dispersive_ wave equation:
$$\pd{^2\psi}{t^2}=v^2\nabla^2\psi$$
	- Non-dispersive: $v$ _does not depend on frequency_

- The one-dimensional version:
$$\pd{^2\psi}{t^2}=v^2\pd{^2\psi}{x^2}$$
	- Example: Transverse string wave

- The wave equation is _linear_, hence the _superposition principle_ applies
- Due to the nature of wave motion:
$$\psi(x,t)=\psi(x\pm vt,0)=f(x\pm vt)$$
- Any function of the form $f(x\pm vt)$ obeys the wave equation

- A special set of solutions is the _harmonic waves_, which oscillate _sinusoidally_
- For a 1D wave travelling to the right, the displacement at position $x$ at time $t$ is given by:
$$\Psi(x,t)=\Re[A\exp{i(kx-\omega t)}]$$
	- $k=\omega/v=2\pi/\lambda$: wavenumber
	- Phase: $kx-\omega t$

## Waves with different types of symmetry
### Plane wave
- Let there be a plane defined by $\bm{\hat{n}\cdot r}=d$ 
- Define a wave vector $\bm{k}=k\bm{\hat{n}}$, $\bm{k\cdot r}$ is constant along the plane

- For a _plane wave_ propagating in the direction $\bm{k}$, the wave function can be written:
$$\psi(\bm{r},t)=\Re\left(Ae^{i(\bm{k\cdot r}-\omega t)}\right)$$
	- Opposite direction: phase$=\bm{k\cdot r}+\omega t$

- $\nabla\psi=-i\bm{k}\psi$
- Satisfies wave equation

### Spherical wave
- For a wave propagating with _spherical symmetry_, using the Laplacian for spherical coordinates:
$$\psi(r,t)=\frac{f(r\pm vt)}{r}$$
- $1/r$ dependence for amplitude gives $1/r^2$ dependence for power, conserving energy

### Cylindrical wave
- Wave propagating with _cylindrical symmetry_
- EXACT solution: involves _cylindrical Bessel functions_

- For long distances, using the energy conservation argument, one can guess the solution:
$$\psi(r,t)\approx\frac{f(r\pm vt)}{\sqrt{r}}$$
- Long distance requirement: $r>>\lambda$

## Polarisation
- For a _transverse wave_ travelling in the $x$ direction, the displacement could be along $y$ or $z$
- The waves in the two directions are _independent but have the same speed_:
$$v^2\pd{^2\psi_i}{x^2}=\pd{^2\psi_i}{t^2}\hspace{0.25cm},\hspace{0.25cm}i=y,z $$

- The waves must be _coherent_ for the overall wave to be polarised
- _Partial polarisation_ can occur when two incoherent waves are added
- _Unpolarised_: two orthogonal, _incoherent oscillations_ with equal magnitude

- The displacements can be written as:
$$\begin{aligned}\psi_y&=A_y\cos(kx-\omega t) \\ \psi_z &= A_z\cos(kx-\omega t+\phi)\end{aligned}$$

- Value of $\phi$ determines polarisation state

### Linear polarisation
- $\phi=n\pi$
- The field vector oscillates _along a straight line_
- Amplitude $A=\sqrt{A_y^2+A_z^2}$

### Circular polarisation
- Equal in magnitude
- $\phi=(m+1/2)\pi$
- Convention: Looking _towards the wave source_
	- Using the right-hand-rule: finger points _TOWARDS source_
	- Right-circular: clockwise motion of field vector as $z$ increases![[Polarisation conventions.png]]

### Elliptical polarisation
- Most general
- _Not necessarily equal_ in amplitude, $0\leq \phi \leq 2\pi$
- Reduction to _special cases_
	- Circular: $A_y=A_z, \phi=(m+1/2)\pi$, s
		- Sum of equal amplitude, coherent, _orthogonal linearly polarised_ waves with $\pi/2$ phase
	- Linear: $A_y=A_z$, $\phi=n\pi$ 
		- Sum of equal amplitude, coherent, _left and right-handed circularly polarised_ waves

- Two amplitudes and one angle needed to specify elliptical polarisation

### Vector representation
- _Jones vector_ representation for completely polarised light
- $\exp[i(kz-\omega t)]$ is dropped
- Opposite sign convention if $\omega t-kz$ is used as phase
- Linear polarisation:
$$\ket{\Psi_\text{lin}}=\begin{pmatrix} A \\ B \end{pmatrix}$$
- Circular polarisation, left and right:
$$\ket{\Psi_\text{left}}=\begin{pmatrix}A \\ -Ai \end{pmatrix} \hspace{2cm} \ket{\Psi_\text{right}}=\begin{pmatrix}A \\ Ai \end{pmatrix}$$
- Elliptical polarisation:
$$\ket{\Psi}=\begin{pmatrix} A \\ B\,\exp(i\phi)\end{pmatrix}$$

## Impedance and power
- Impedance for any system is defined as a _ratio of a driving force to a flow or velocity_
- For a transverse wave, the velocity response is the _transverse response_ $\dot{\psi}$

- The power input is the _transverse force_ $F$ times the _transverse velocity_ $\dot{\psi}$
- Like the case in [[Oscillations#Power|oscillations]], the power is:
$$\braket{P}=\frac{1}{2}\Re[F\dot{\psi}^*]=\frac{1}{2}\Re[Z]|\dot{\psi}|^2$$
- For real $Z$ and $u=-i\omega A_0\exp[i(kx-\omega t)]$:
$$\braket{P}=\frac{1}{2}Z\omega^2A_0^2$$

### String wave
- For a string wave:
$$Z=\frac{-T\,\partial\psi/\partial x}{\partial\psi/\partial t}$$
	- Driving force: _transverse tension_

- For a waveform $\psi=f(x-vt)$:
$$Z=\frac{T}{v}=\sqrt{T\rho}=\rho v$$
	- Becomes _negative_ for a waveform travelling _in the $-x$ direction_

### Energy flow per unit length
- By looking at a short length of string, the _kinetic energy per unit length_ is:
$$K=\frac{1}{2}\rho\left(\pd{\psi}{t}\right)^2$$
- The _potential energy per unit length_ is:
$$U=\frac{1}{2}T\left(\pd{\psi}{x}\right)^2$$

- As $\rho\omega^2=Tk^2$, the two terms are equal
- The power is energy per unit length times wave speed, hence:
$$\braket{P}=\braket{K+U}v=\frac{1}{2}Z\omega^2A_0^2$$

## Boundaries: reflection and transmission
- There can be _discontinuities_ during wave travel, such as a _sudden change in density_ (hence, change in impedance)

- Boundary conditions:
	- Displacement $\psi$ _must be continuous_
	- Transverse force $T(\partial\Psi/\partial x)$ _must be continuous_
		- _Avoid infinite acceleration_ of infinitesimal mass element
	- _Constant frequency_ $\omega$
- Wavenumber $k$ will be discontinuous

- Goal: _STEADY-STATE_ response of the wave on both sides of a boundary

### Reflection and transmission coefficients
- Assume a semi-infinite [[#The wave equation|harmonic wave]] on each side of the boundary, look for the _steady-state response_
- More convenient to write the wave as $A\exp[i(\omega t-kx)]$

- Let there be 2 regimes, with impedances $Z_1$ and $Z_2$ respectively
- Let there be an incident wave with amplitude $A_1$, reflected wave with amplitude $B_2$, and transmitted wave with amplitude $A_2$, the reflection and transmission are:
$$\displaylines{\tau\equiv\frac{A_2}{A_1}=\frac{2Z_1}{Z_1+Z_2} \\ r\equiv \frac{B_1}{A_1}=\frac{Z_1-Z_2}{Z_1+Z_2}}$$
- Limiting cases:
	- $Z_2=\infty$: fixed end, $\tau=0$, no transmission, $r=-1$, pure anti-phase reflection
	- $Z_2=0$: free end, $\tau=2$, $r=1$, pure in-phase reflection, no energy transmitted
	- $Z_2=Z_1$: $r=0$, $\tau=1$, no boundary exists

- As impedances can be complex, there can be arbitrary phase differences

### Reflection and transmission of energy
- For real impedance, as the power transmitted is _proportional to $Z\omega^2A^2$_, the Power Reflection and Transmission coefficients are:
$$R\equiv\frac{Z_1B_1^2}{Z_1A_1^2}=r^2=\left(\frac{Z_1-Z_2}{Z_1+Z_2}\right)^2$$
$$T\equiv \frac{Z_2A_2^2}{Z_1A_1^2}=\frac{4Z_1Z_2}{(Z_1+Z_2)^2}$$
- Due to energy conservation, the following _always applies_:
$$R+T=1$$
- If any _impedance is complex_, replace $Z$ with $\Re(Z)$ and $A$ with $|A|$ in the above, making $R$:
$$R=\left|\frac{Z_1-Z_2}{Z_1+Z_2}\right|^2$$

### Impedance matching
- Let there be two _infinite substrates_ with impedances $Z_1$ and $Z_3$, with a _layer_ of length $l$ inbetween that has impedance $Z_2$
- If $l$ is equal to a _quarter of the wavelength_ in $Z_2$, the reflection coefficient from the $Z_1-Z_2$ interface becomes:
$$r=\frac{Z_1-Z_{eff}}{Z_1+Z_{eff}}\hspace{0.5cm},\hspace{0.5cm} Z_{eff}=\frac{Z_2^2}{Z_3}$$
- If $Z_2^2=Z_1Z_3$, the waves reflected at the first and second interfaces are _out of phase_


## Longitudinal waves
- Longitudinal: displacement is _parallel to propagation direction_
- Displacement: compression and rarefraction
	- _Centre_ of compression/rarefraction: _zero displacement_
- Polarisation not defined

### Sound in a gas
- Pressure and displacement are $\pi/2$ out of phase
- Maximum/minimum pressure at zero displacement

- [[Thermodynamics#Gases|Thermodynamics of a gas]]
- The compression/rarefraction of an ideal gas: an adiabatic process, which satisfies:
$$pV^\gamma=\text{const.}$$
- Let the _original position_ of the gas be $x$, and the _displacement_ be $a(x,t)$
- Let there be a _parcel_ of gas with cross-section $S$, from $x$ to $x+\Delta x$
- The displacement of the gas produces an _extra pressure_ $\Psi_p(x,t)$
- The _fractional volume change_ is:
$$\frac{\Delta V}{V}=\pd{a}{x}$$
- By considering the _pressure gradient_ and the acceleration of the gas, one gets:
$$-\pd{\Psi_p}{x}=\rho\pd{^2a}{t^2}$$
- By _differentiating the adiabatic equation_, with $dp=\Psi_p$ one gets:
$$\Psi_p=-\gamma p\pd{a}{x}$$
- Physical interpretation: compression and rarefrac
$$\pd{^2a}{x^2}=\frac{\rho}{\gamma p}\pd{^2a}{t^2}$$
- As the speed is independent of frequency, one sees that sound waves are _dispersionless_
- The wave speed $v$ is given by:
$$v=\sqrt{\frac{\gamma p}{\rho}}=\sqrt{\frac{\gamma RT}{M}}$$
	- $M$: molar mass $m/n$

- The RMS speed of molecules is slightly larger than $v$
- Propagation of sound _does not require net movement_ of molecules, only _bulk movement_

#### Impedance
- If $a$ is a harmonic wave of the form:
$$a=a_0\exp[i(\omega t-kx)]$$
- The pressure wave, according to the above, is:
$$\Psi_p=i\gamma pka$$
- Pressure _leads displacement_ by $\pi/2$
- The characteristic impedance is:
$$Z=\frac{S\Psi_p}{\dot{a}}=S\sqrt{\gamma p\rho}$$
- The impedance _per unit area_, or _acoustic impedance_ $\Lagr$ is:
$$\Lagr=\sqrt{\gamma p\rho}=\frac{\gamma p}{v}$$
#### Power
- Let the amplitude of the pressure be $A_0=i\gamma pka_0$
- The mean power per unit area, or _intensity_, is:
$$I=\frac{1}{2}\Re[\Psi_p\dot{a}^*]=\frac{|A|^2}{2\Lagr}=\frac{A_\text{rms}^2}{\Lagr}=\frac{1}{2}\Lagr\omega^2|a_0|^2$$
- The Decibel scale is defined to be:
$$\text{dBA level}=10\log_{10}\left(\frac{I}{I_\text{ref}}\right)= 10\log_{10}\left(\frac{p_\text{rms}^2}{p_\text{ref}^2}\right)= 20\log_{10}\left(\frac{p_\text{rms}}{p_\text{ref}}\right) $$

### Sound in liquids and solids
- In liquids and solids, the _general relationship_ between pressure and displacement is:
$$\Psi_p=-K\pd{a}{x}$$
- Here, $K$ is the relevant _elastic modulus_ of the medium
- From this, the speed of a longitudinal wave is:
$$v=\sqrt{\frac{K}{\rho}}$$
- There are also transverse waves that _shear_ the medium, known as _shear waves_
- Shear waves are typically _slower_ than longitudinal waves

- For gases and liquids, although $\Psi_p$ is isotropic, compression and rarefraction only takes place in _the direction of wave passage_
- The relevant compression is described by:
$$dp=-B\frac{dV}{V}$$
- Here, $B$ is the _bulk modulus_
	- Equal to $\gamma p$ for a gas
- Hence, the speed of sound in a _liquid_ is:
$$v_l=\sqrt{\frac{B}{\rho}}$$

- For _bulk solids_, transverse waves are ignored
	- For thin bars, consider the _Poisson's ratio_
- The longitudinal stress is given by _Young's modulus_ $Y$:
$$\tau=Y\pd{a}{x}$$
- Hence, the speed of sound in a solid is given by 
$$v_s=\sqrt{\frac{Y}{\rho}}$$

- Acoustic impedance is much _larger in a solid_ than a gas
- An _open air-solid interface_ is essentially a pressure node, or displacement antinode

## Standing waves
- A standing wave is _confined_ within a region of space
- A _superposition_ of forward and backward waves

### One dimension
- For boundary conditions $\Psi(0,t)=\Psi(b,t)=0$:
$$\Psi=A[\cos(\omega t-kx)-\cos(\omega t+kx)]=2A\sin(\omega t)\sin(kx)$$
- The boundary conditions are satisfied for quantised wavenumbers $k$:
$$k=\frac{n\pi}{b}$$

### Two and three dimensions
- For a 3D box of dimensions $(a,b,c)$, where $\Psi$ has to be zero at the boundary
- To satisfy the [[#The wave equation|wave equation]] and the boundary conditions:
$$\Psi=A\sin(k_xx)\sin(k_yy)\sin(k_zz)\cos(\omega t)=A\sin(\bm{k\cdot r})\cos(\omega t)$$
$$\bm{k}=\left(\frac{l\pi}{a},\frac{m\pi}{b},\frac{n\pi}{c}\right)$$


## Damped waves
- There may be a transverse damping force proportional to transverse speed
$$\pd{^2\psi}{t^2}=v^2\pd{^2\psi}{x^2}-\frac{\beta}{\rho}\pd{\psi}{t}$$
$$\pd{^2\Psi}{t^2}+\Gamma\pd{\psi}{t}=v^2\pd{^2\Psi}{x^2}$$
- For a harmonic wave:
$$\omega^2-i\Gamma\omega=v^2k^2$$
- Therefore, _$k$ must be complex_, giving exponential and oscillating parts of $\Psi$
- Spltting $k$ into $k_r-ik_i$:
$$k_r^2-k_i^2=\frac{\omega^2}{v^2} \hspace{1cm} 2k_rk_i=\frac{\Gamma\omega}{v^2}$$
### Light damping
- Condition: $\Gamma<<\omega$
$$k_r\approx\frac{\omega}{v}\hspace{1.5cm} k_i\approx\frac{\Gamma}{2v}$$
- The wave becomes a _decaying travelling wave_:
$$\psi=\exp(-k_ix)\Re[D\exp(i\omega t-ik_rx)]$$
- Damping is independent of wavelength

- The impedance still has the usual definition:
$$Z(\omega)=\frac{-T\partial\psi/\partial x}{\partial\psi/\partial t}=\frac{T}{\omega}(k_r-ik_i)\approx \sqrt{T\rho}\left(1-\frac{i\Gamma}{2\omega}\right)$$
- Returns to [[#Impedance and power|impedance without damping]] for $\Gamma=0$

- Let an undamped string meet a damped one at a boundary, the reflection coefficient is:
$$r(\omega)=\frac{Z_0-Z}{Z_0+Z}\approx\frac{i\Gamma}{4\omega}$$
- Small $r$ with phase $\pi/2$, meaning most power is transmitted

### Heavy damping
- Condition: $\Gamma>>\omega$
$$k'=k_r\approx k_i\approx \pm\sqrt{\frac{\Gamma\omega}{2v^2}}$$
- $k$ has equal real and imaginary parts
- Wave decays over a short distance, varies as $\omega^{-1/2}$

- Impedance:
$$Z(\omega)=\sqrt{T\rho}(1-i)\sqrt{\frac{\Gamma}{2\omega}}$$
- Reflection coefficient:
$$r(\omega)\approx -1$$
- The wave is almost completely reflected in anti-phase

### Phase speed
- The phase of the propagating wave is $(\omega t-k_rx)$, therefore the phase speed is:
$$v_\phi=\frac{\omega}{k_r}$$
- By expressing $\omega$ in terms of $k_r$:
$$v_\phi=v\left(1+\frac{\Gamma^2}{4v^2k_r^2}\right)^{-1/2}$$

- _Dispersion relation_ for a damped string
- Phase speed increases as frequency increases
	- Approaches $v$ in high frequency limit

## Group velocity
- Dispersion: wave speed _depends on wavelength_
- Different components of a wave group will have _different speeds_
- The wave group will _disperse_

- The _phase velocity_ is how fast a _particular point_ in the wave travels
$$v_\text{phase}=\frac{\omega}{k}$$

- The _group velocity_ $v_g$ is how fast a "bump" in a wave group travels

### Narrow spread in frequencies
- Loose derivation: the "bump" occurs when the phase of all components is the same
	- This occurs when:
	$$\left[\frac{d}{d\omega}(\omega t-kx+\phi)\right]_{\omega_0}=0$$
	- $\omega_0$ is a "typical" frequency in a wave group
	- Hence, the group velocity is:
	$$v_h=\frac{d\omega}{dk}\Bigg|_{\omega_0}$$

- The group velocity can also be interpreted as a _wave packet at $(x,t)$ being similar to the one at $(x-v_gt,0)$_
- Proof for wave packets with _narrow spread of $k$_
	- Let the dispersion relation be approximated as
	$$\omega(k)\approx \omega(k_0)+\frac{d\omega}{dk}\Big|_{k_0}(k-k_0)=\omega_0+\omega_0'(k-k_0)$$
	- The wave packet is defined as:
	$$\Psi(x,t)=\frac{1}{\sqrt{2\pi}}\int_{-\infty}^\infty\phi(k)\exp[i(kx-\omega t)]\,dk$$
	- By changing variables from $k$ to $s=k-k_0$, one gets:
 $$\Psi(x,t)\approx\exp[-i(\omega_0-k_0\omega_0')t]\,\Psi(x-\omega_0't,\,0)$$
	- So, one gets that the _carrier wave_ travels at speed $v_g=\omega_0'$

- When $v_\text{phase}\neq v_g$, the wave crests will _move relative to the envelope_
- The group velocity is the velocity for _propagation of information_
- The _spread of wave-numbers_ is inversely proportional to the _spread in position_:
$$\Delta k\Delta x\approx 1$$

### Large spread in frequencies
- A broad-band signal can be thought of as a _superposition of narrow-band signals_
- Each narrow-band signal will move with _different group velocities_
- The second-order term in the Taylor expansion of $\omega(k)$ is _no longer negligible_
- The wave packet will _elongate_

- Let the group contain a spread of wave-numbers $2\Delta k$ 
- The _extreme values of wave-numbers_ are:
$$v_{g1}=\pd{\omega}{k}\Bigg|_{k_0-\Delta k} \hspace{1cm} v_{g2}=\pd{\omega}{k}\Bigg|_{k_0+\Delta k}$$
- The spread in length becomes:
$$\Delta x\approx \Delta x_0+(v_{g2}-v_{g1})t\approx \Delta x_0 +2|\beta| (\Delta k) t\approx \Delta x_0+2|\beta|\frac{t}{\Delta x_0}$$
$$\beta\equiv \pd{^2\omega}{k^2}\Bigg|_{k_0}$$

### Example: water waves
- In _deep water_, water has the dispersion relation:
$$\omega^2=gk+\frac{\sigma k^3}{\rho}$$
- Here, $\sigma$ is the surface tension

- The two terms are equal for $k^2=\rho g/\sigma$, corresponding to a wavelength of $\lambda_0=17\text{mm}$
- _Ripples_/capillary waves in deep water with _short wavelengths_ are surface-tension driven:
	 $$\omega\approx\sqrt{\frac{\sigma k^3}{\rho}}\hspace{1cm} v_\phi=\sqrt{\frac{\sigma k}{\rho}} \hspace{1cm} v_g\approx \frac{3}{2}v_\phi$$
	 - Phase and group velocity _decrease as wavelength increases_
	 - Case of _'anomalous' dispersion_
	 - As $v_\phi<v_g$, ripples _appear to move backwards in the packet_

- _Deep water gravity waves_, with _long wavelengths_
 $$\omega\approx \sqrt{gk}\hspace{1cm} v_\phi\approx\sqrt{\frac{g}{k}} \hspace{1cm} v_g\approx \frac{1}{2}v_\phi$$
	- Phase and group velocity _increase as wavelength increases_
	- Case of _'normal' dispersion_
	- Individual waves _appear to move forwards in the packet_

- _Shallow water gravity waves_, with wavelength exceeding depth $h$:
 $$\omega^2=ghk^2\left(1-\frac{h^2k^2}{3}\right)$$
	- Motion is _mainly longitudinal_
	- For _very shallow water_, the wave becomes approximately non-dispersive
	- As $h$ decreases when the wave approaches the shore, amplitude increases to _conserve water_

## Guided waves
- Confining travelling waves to transmit energy or information

### The wave
- Consider a non-dispersive wave on a two-dimensional membrane:
$$\nabla^2\psi=\pd{^2\psi}{x^2}+\pd{^2\psi}{y^2}=\frac{1}{v^2}\pd{^2\psi}{t^2}$$
- The general solution is:
$$\psi=a\exp[i(\omega t\pm \bm{k}\cdot\bm{r})]$$
- The boundary conditions: _clamp_ the wave at $y=0$ and $y=b$
$$\psi(y=0)=\psi(y=b)=0$$
- At the edges, a reflection with opposite amplitude is produced, creating a _standing wave in the $y$ direction while still propagating in the $x$ direction_:
$$\psi=A'\sin(k_yy)\exp[i(\omega t-k_xx)]$$
- To satisfy the boundary conditions, $k_y$ _has to be quantised_:
$$k_y=\frac{n\pi}{b}$$
- To determine the dispersion relation of the resulting wave, substitute this back into the wave equation:
$$\omega^2=v^2\left(k_x^2+\frac{n^2\pi^2}{b^2}\right)$$

### The properties
- The _group velocity_ is:
$$v_g=\frac{v^2}{\omega}\sqrt{\frac{\omega^2}{v^2}-\frac{n^2\pi^2}{b^2}}=\frac{v^2}{v_{\phi x}}=v\cos\theta$$
- The angle $\theta$ of the wavefronts is defined as:
$$\tan\theta=\frac{k_y}{k_z}$$
- The _phase velocity along the $x$ direction_ is:
$$v_p=\frac{\omega}{k_x}=\omega\left(\frac{\omega^2}{v^2}+\frac{n^2\pi^2}{b^2}\right)^{-1/2}=\frac{v}{\cos\theta}$$

- The _faster the wave_ (high $v$), the _effect of the boundaries become less apparent_

- $n$ specifies the _waveguide mode_
- The wavelength of the guided wave is $2\pi/k_x=\lambda_x$, which _exceeds the original_ $\lambda$
- If there is a spread of frequencies, _multiple modes can be excited_

- As $k_x\to0$, $v_p\to\infty$ and $v_g\to 0$, which _does not violate relativity as information travels at $v_g$_
- As $k_x\to\infty$, $v_p$ and $v_g$ both tend towards $v$ as behaviour approaches an unguided wave

### Cut-off frequency and evanescent waves
- For a given mode, there is a _cutoff frequency_ $\omega_c$:
$$\omega_c=\frac{n\pi v}{b}$$
- Below this frequency, $k_x^2<0$ and a propagating wave is _not possible_
- By choosing a frequency between $\omega_c(n=1)$ and $\omega_c(n=2)$, the wave can be _single-moded_

- For $\omega<\omega_c$, the wave becomes _evanescent_:
$$\psi=A\sin\left(\frac{n\pi v}{b}y\right)\exp(i\omega t)\exp(\pm|k_x|x)$$
- The positive solution is usually excluded unless the region is short $(L<1/|k_x|)$
- There is _no net power flow slong the guide_
- An incident wave on the guide _will be perfectly reflected_, forming a standing wave

- If there is a second discontinuity, the wave can be transmitted _beyond the guide_