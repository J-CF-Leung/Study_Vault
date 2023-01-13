#IB_Natsci 
# Electromagnetic waves
- From [[Electromagnetism#Maxwell's equations|Maxwell's equations]], it can be shown that in a _current and charge free region_, the $\bm{E}$ and $\bm{B}$ fields _satisfy the [[Waves#The wave equation|wave equation]]_:
$$\nabla^2\bm{E}=(\mu\mu_0)(\epsilon\epsilon_0)\pd{^2\bm{E}}{t^2}=\frac{1}{c^2}\pd{^2\bm{E}}{t^2}$$
- The speed of light in vacuum is _exactly_:
$$c_0=\frac{1}{\sqrt{\mu_0\epsilon_0}}=299792458\text{ m s}^{-1}$$
- The _refractive index_ $n$ is defined as:
$$n\equiv\frac{c_0}{c}=\sqrt{\epsilon\mu}$$
- For most materials, $\mu\approx 1$, hence:
$$n\approx\sqrt{\epsilon}$$
- For free spece, the fields are _transverse to propagation direction_ and _orthogonal_

- A plane electromagnetic wave can be written as:
$$\displaylines{\bm{E}=\bm{E_0}\exp(i\omega t-i\bm{k\cdot r}) \\ \bm{B}=\bm{B_0}\exp(i\omega t-i\bm{k\cdot r})}$$
- From Faraday's Law:
$$\nabla\wedge\bm{E}=-\dot{\bm{B}} \longrightarrow -i\bm{k\wedge E_0}=-i\omega\bm{B_0}$$
- This not only gives the relative orientations of the two fields, but also the magnitudes:
$$\frac{|\bm{E}_0|}{\bm{B}_0}=\frac{\omega}{|\bm{k}|}=c=\frac{c_0}{n}$$
- The [[Waves#Impedance|impedance]] is defined as:
$$Z=\frac{|\bm{E}|}{|\bm{H}|}=c\mu=\sqrt{\frac{\mu\mu_0}{\epsilon\epsilon_0 }}=Z_0\sqrt{\frac{\mu}{\epsilon}}$$
- For $\mu\approx 1$:
$$Z=\frac{Z_0}{n} \hspace{1.5cm} Z_0=\sqrt{\frac{\mu_0}{\epsilon_0}}$$
# Approximations of physical optics
- Most accurate - Quantum Electrodynamics (QED) - nope
- Maxwell's Equations: accurate for situations where light has intensity _much higher than the energy of individual protons_
- Physical optics/scalar wave theory: ignores polarisation, using _Huygen's Principle to model wave propagation_
- Ray optics: _very small $\lambda$_, wave properties can be ignored

## Huygens' Principle
>[!info] Huygens' Principle
>Each point on a wavefront acts as a source of secondary wavelets which propagate, overlap, and interfere to carry the wavefront forward

- Can be used to derive the laws of reflection and refraction

- To avoid a backward propagating wavefront, an _inclination factor_ $K(\theta)$ is included
	- Huygens: $K=1$ forwards, 0 backwards
	- Fresnel: $(1+\cos\theta)/2$

# Diffraction

## The Fresnel-Kirchoff Diffraction integral
- Let there be a source of _monochromatic_ waves $S$ placed behind an _aperture_ $\Sigma$

- The illumination must be _spatially coherent_, with a _well-defined phase relationship_ between different parts of the wave

- The source produces a _spherical wave_, with the strength _at an aperture element_ some distance $s$ away being:
$$\psi_1(\bm{r})=\frac{a_S\exp(iks)}{s}$$
- In general, the aperture _can change amplitude and phase_, it can be characterised by an _aperture function_ $h(x,y)$
- The wave emitted _from aperture element $d\Sigma$_ is therefore written as $Ah(x,y)\psi_1d\Sigma$
- The _secondary waves produce a disturbance_ at point $P$, distance $r$ away:
$$d\psi_P=AKh(x,y)\psi_1\frac{\exp(ikr)}{r}d\Sigma$$

- Each element of the aperture _can be considered to be a source of secondary wavelets_
- The _prefactor_ $A$ and _inclination factor_ derived by Kirchoff (see proof in Lipson):
$$\displaylines{A=-\frac{i}{\lambda} \\ K=\frac{\cos\theta_S+\cos\theta_P}{2}}$$
	- Angles relative to aperture normal
	- $K$ _often approximated_ as 1 (The _paraxial_ approximation)

- To find the total amplitude at $P$, _sum over all aperture elements_:
$$\psi_P=\iint_\Sigma -\frac{i}{\lambda}\,h(x,y)\,K(\theta_S,\theta_P)\frac{a_S\exp[ik(s+r)]}{sr}\,dx\,dy$$
	- $s$ and $r$ are also functions of $x$ and $y$

- Often breaks down for points very close to aperture

## Fraunhofer diffraction
- Consider the _source to be infinite_
- The aperture is illuminated with a _plane wave at normal incidence_
- The geometry of the setup:
![[Fraunhofer setup.png]]

- Consider _small angles_, where $K\approx1$

- The phase of each wavelet is _proportional to_ $kr$
- _Expanding_ $r$, it is found that it can vary both _linearly and quadratically_ with $x,y$:
$$\displaylines{r^2=L^2+(x-x_0)^2+(y-y_0)^2 \\r\approx R-\frac{x_0x+y_0y}{R}+\frac{x^2+y^2}{2R}}$$

- The _condition for Fraunhofer diffraction_ is that phase _varies linearly_ with $x$ and $y$
- This condition can be expressed as:
$$\frac{k(x^2+y^2)}{2R}<<\pi$$
- For an aperture of _maximum extent_ $D$, the condition is:
$$R>>\frac{D^2}{\lambda}$$

- Then, the wave amplitude at $P$ is given by the _Fraunhofer integral_:
$$\psi_P\propto\iint_\Sigma \psi_\Sigma \,h(x,y)\,\exp\left[-ik\left(\frac{x_0x+y_0y}{R}\right)\right]\,dx\,dy$$
- If illuminated with a _plane wave_, $\psi_\Sigma$ remains constant
	- Often satisfied by using a lens to make a _parallel beam_

- For a _1-dimensional aperture_, the integral becomes:
$$\psi_P\propto \int_\Sigma h(y)\exp\left(-ik\frac{y_0y}{R}\right)\,dy$$
- Redefining:
$$y_0\equiv R\sin\theta\hspace{1cm} q=k\sin\theta$$
- Then, the integral is:
$$\psi_P\propto \int h(y)\,\exp(-iqy)\,dy$$
- Hence, $\psi_P$ is the _[[Fourier series and transforms#Fourier transforms|Fourier transform]] of the aperture function_
- $y$ and $q$ are the _reciprocal coordinates_ which play the roles of $x$ and $k$

## Examples of 1D Fraunhofer diffraction

### Young's double slits
- Slits are _modelled by Delta functions_
- Spacing between slits is $D$
- Consider the aperture function:
$$h(y)=\delta\left(y+\frac{D}{2}\right)+\delta\left(y-\frac{D}{2}\right)$$
- The Fourier transform of this is simply a cosine function
- This gives an intensity $I\propto \psi_P^2$:
$$I_P(q)=I_0\cos^2\left(\frac{qD}{2}\right)=I_0\cos^2\left(\frac{kD\sin\theta}{2}\right)$$
- This can also be derived using a _phasor diagram_

### N slits
- The aperture function for $N$ narrow slits is:
$$h(y)=\sum_{m=0}^{N-1}\delta(y-mD)$$
- Hence:
$$\psi_P=\sum_{m=1}^{N-1}\exp(-imqD)=\frac{1-\exp(-iNqD)}{1-\exp(-iqD)}$$
$$I_P=I_0\left[\frac{\sin(NqD/2)}{\sin(qD/2)}\right]^2$$
- The intensity has _primary maxima_ when $\sin(qD/2)=0$
- The _subsidiary maxima_ occur when $\sin(NqD/2)=\pm1$
- Between each primary maxima, there are $N-2$ subsidiary maxima and $N-1$ zeros
- The _width_ of the primary maxima is given by $q=2\pi/(ND)=G/N$
	- The larger $N$ is, the _thinner_ the peaks and _chromatic resolving power_ increases

- For monochromatic light on a grating with a _large number of slits_, diffraction occurs in directions:
$$k\sin\theta=q=2m\pi/D\equiv mG$$
- A _comb_ with spacing $D$ in x-space is _transformed_ into a comb with spacing $G$ _in q-space
	- Fourier transform tends to the comb function as $N$ approaches infinity

### Single wide aperture
- The aperture function of an aperture with witdth $a$ is:
$$h(y)=\begin{cases}1 &|y|<a/2 \\ 0 &|y|>a/2\end{cases}$$
- The diffracted intensity is:
$$I_p(q)=I_0a^2\sinc^2\left(\frac{qa}{2}\right)$$
### Series of wide apertures
- _Convolution_ in linear space becomes _multiplication_ in Fourier space
- A series of wide apertures is a _convolution of one aperture with a series of Dirac deltas_
- Hence, for $N$ wide slits all with width $a$:
$$I_P(q)=I_0\left(\frac{\sin(NqD/2)}{\sin(qD/2)}\right)^2\sinc^2\left(\frac{qa}{2}\right)$$

- The diffraction pattern is _modulated_ by a diffraction envelope
- For $D=na$, this leads to _missing orders_ due to the envelope

### Complex aperture function
- Consider a triangular _wedge_ of material with small angle $\alpha$ and refractive index $n$
- It introduces a _phase shift_ proportional to position along the wedge
- By placing in front of the aperture, $h(y)$ is _multiplied_ by $\exp(ik(n-1)\alpha y)$

- _Multiplying by exponential_ in $x$-space is a _translation_ in $q$-space
- The pattern is _shifted_ by an angle $(n-1)\alpha$

## Spectra and line widths
- _Spectral lines_ emerge from electrons transitioning in energy levels
- An excited state in an atom has a _finite lifetime_ $\tau_L$
- From the energy-time uncertainty principle, this gives a _spectral line width_
- Since the _electric field decays exponentially_, the intensity $I(\omega)$ is _Lorentzian_:
$$\displaylines{E(t)=E_0\exp(-\gamma t)\cos\omega_0t \\ I(\omega)\propto \frac{1}{(\omega-\omega_0)^2+\gamma^2}}$$
- At half-maximum, $\delta\omega=\gamma\approx1/\tau_L$

### Collision/pressure broadening
- Collisions _shortens the lifetime_ of excited states
- The mean time between collisions in a gas is $\tau_c\approx1/(n\Sigma u)$
	- $n$: Number density
	- $\Sigma$: Collision cross section
	- $u$: particle speed
- The new range of frequencies is:
$$\Delta\omega\approx n\Sigma u$$
- The peak is a _Lorentzian_

### Doppler/thermal broadening
- If an atom is in motion, it causes a _Doppler shift_ in the observed frequency:
$$\omega=\omega_0\sqrt{\frac{1+u_x/c}{1-u_x/c}}\approx\omega_0\left(1+\frac{u_x}{c}\right)$$
- From the Boltzmann distribution, the distribution of frequencies is _Gaussian_:
$$\displaylines{I(\omega)\propto\exp\left(-\frac{mc^2(\omega-\omega_0)^2 }{2\omega_0^2k_BT}\right)=\exp\left(-\frac{(\omega-\omega_0)^2}{2\sigma_\omega^2}\right) \\ \sigma_\omega=\omega_0\sqrt{\frac{k_BT}{mc^2}}}$$
### Spectrometers
- Light is incident onto a grating of spacing $D$, with angle $\theta_1$, and exits at $\theta_2$
- The diffraction angle satisfies:
$$D(\sin\theta_2-\sin\theta_1)=m\lambda$$

### Resolution
- Spectrometer resolution will eventually become _limited by the properties of the grating_
- For a grating of finite width, the peaks will also have a finite width
- If light with two wavelengths $\lambda$ and $\lambda+\delta\lambda$ is incident on a slit, the _Rayleigh criterion_ requires that the _maximum of the latter peak falls on the minimum of the former_
- For a _diffraction grating_, the _resolving power_ of the grating is:
$$\frac{\lambda}{\delta\lambda}\approx mN$$
- Here, $m$ is the _order_ and $N$ is the _number of slits_

## 2D Fraunhofer diffraction
- For a 2-dimensional aperture, the conditions of Fraunhofer diffraction give:
$$\psi_P\propto\iint_\Sigma \psi_\Sigma \,h(x,y)\,\exp\left(ik\frac{x_0x+y_0y}{R}\right)\,dx\,dy$$
- The position on the screen can be specified by 2 small angles:
$$\xi\approx\sin\xi\equiv x_0/R \hspace{1.5cm} \theta\approx\sin\theta\equiv y_0/R$$
- By using the variables $p\equiv x_0/R\approx k\sin\xi$ and $q\equiv y_0/R\approx k\sin\theta$
- This allows the integral to be written as a _two-dimensional Fourier transform_:
$$\psi_P\propto\iint_\Sigma h(x,y)\,\exp[-i(px+qy)]\,dx\,dy$$
- The transform is easy to evaluate if the aperture function is _separable_

- Example: For a _rectangular aperture with sides $a$ and $b$_:
$$\psi_P\propto ab\,\sinc\left(\frac{qa}{2}\right)\,\sinc\left( \frac{qb}{2}\right)$$
### The circular aperture
- Let there be a circular aperture with diameter $d$
- The amplitude can be written as a function of $\rho$, the _radial distance_, or angle $\theta$
- Since the integral is not separable, the amplitude is written as:
$$\psi_P\propto \frac{\psi_0d^2}{2}\frac{J_1(kd\sin\theta/2)}{kd\sin\theta/2}$$
- Here, $J_1$ is a _first order [[Special functions and orthogonal relations#Bessel functions|Bessel function]] of the first kind_
- $J_1(x)$ has a zero at $x=3.83$, hence the first _angular zero_ is at $1.22\lambda/d$
- The central disc is also known as an _Airy disc_

- This also defines the _angular resolution_ of a telescope from the Rayleigh criterion
- In geometrical optics, the _approximation_ is that a finite lens can produce a point image
- In fact, the _angular radius_ of the image is $1.22\lambda/d$

## Babinet's Principle
- Consider two _complementary apertures_ $a$ and $b$
- $a$ is an _opaque_ object with a _transparent hole_ $A$, with $b$ being _opaque_ and having the _shape of the hole_
- It can be shown by splitting the latter integral:
$$\displaylines{\psi_a\propto\iint_A\exp[-i(px+qy)]\,dx\,dy \\ \psi_b\propto\iint_\text{all space}\exp[-i(px+qy)]\,dx\,dy-\psi_a=\delta(p,q)-\psi_a}$$
- Central spike in $\psi_b$ is from the _undiffracted beam_

## Fresnel diffraction
- For Fresnel diffraction, one cannot neglect the _quadratic terms_ as distance to the screen is of a similar, or smaller order than $D^2/\lambda$

- To (massively) simplify the calculation, examine the diffracted intensity _on the axis_
- To find intensity at off-axis locations, _change the source of origin_

![[Fresnel diffraction geometry.png]]

- Define $R$:
$$\frac{1}{R}=\frac{1}{a}+\frac{1}{b}$$
- _Approximate_ $r_1+r_2$ via binomial expansion
- The _general_ Fresnel diffraction integral is:
$$\psi_P\propto\iint_\Sigma \frac{h(x,y)K(x,y)\exp\left(ik\frac{x^2+y^2}{2R}\right)}{r_1r_2}\,dx\,dy$$
- Assumptions:
1. Small diffraction angle, hence $K(\theta)=1$
2. Variations of distance _in the aperture_ are negligible compared to $\lambda$
- _Final_ Fresnel diffraction integral:
$$\psi_P(0,0)\propto\iint_\Sigma h(x,y)\exp\left(ik\frac{x^2+y^2}{2R}\right)\,dx\,dy$$
### Rectangular aperture and the Fresnel integrals
- Let there be a rectangular aperture where $x_1<x<x_2$ and $y_1<y<y_2$
- Since the aperture function is separable, the integral can be written as:
$$\psi_P\propto\int_{x_1}^{x_2}\exp\left(\frac{ikx^2}{2R}\right)\,dx \int_{y_1}^{y_2}\exp\left(\frac{iky^2}{2R}\right)\,dy$$
- Redefining the _dimensionless_ variables:
$$u=x\sqrt{\frac{2}{R\lambda}} \hspace{1.5cm} v=y\sqrt{\frac{2}{R\lambda}}$$
- Then, one can define the _Fresnel integrals_:
$$C(w)=\int_0^w\cos\left(\frac{\pi u^2}{2}\right)\,du\hspace{1.5cm} S(w)=\int_0^w\sin\left(\frac{\pi u^2}{2}\right)\,du$$

- The Fresnel integrals can be represented _graphically_ with the _Cornu spiral_

### The Cornu/Euler spiral
- The spiral is a locus of points _in the complex plane_ defined by $C(w)+iS(w)$
- The _arc length_ between points $w_1$ and $w_2$ is equal to $w_2-w_1$
- The _curvature_ is $\pi w$
- The _gradient_ is $tan(\pi w^2/2)$
- The curve is _odd_
- The curve spirals in towards the point $(C(\infty),S(\infty))=(0.5,0.5)$
![[Euler spiral.png]]
### Diffraction from straight edge(s)

#### On-axis
- Let there be a _slit_ extending from $y=y_1$ to $y_2$
- The relevant diffraction integral becomes:
$$\psi_P\propto\int_{w_1}^{w_2}\exp\left(\frac{i\pi u^2}{2}\right)\,du=[C(w_2)-C(w_1)]+i[S(w_2)-S(w_1)]$$
- The is the length of a _vector spanning the Cornu spiral_ from $w_1$ to $w_2$
- The amplitude is _normalised_ by the vector spanning $w=-\infty$ and $\infty$ with length $\sqrt{2}$

- If the obstructing edge was _from $0$ to $\infty$_, the amplitude _at the centre of the screen_ is represented by vector $(0.5,0.5)$, _from the origin to the centre of the first "half"_
	- On-axis: _Half_ the amplitude compared to unobstructed wave


#### Off-axis
- For _off-axis_ points on the screen, the _origin must be moved to maintain the form of the diffraction integral_
- Move the _position of the aperture_ instead
![[Fresnel off axis.png]]
- Example: in _geometrical shadow_, integral is _from $x_a$ to $\infty$_

![[Fresnel straight edge.png]]
- Maximum: $x_d$, with $\psi\approx1.22\psi_P$


### Finite length aperture
- For an aperture of _finite length_, the amplitude at some point along the screen is represented by a _spanning vector between points of arc length $\Delta w$ apart_
![[Fresnel limited aperture.png]]
- For _small $\Delta w$_ there will be a _central maximum_, and the amplitude _decreases monotonically_ away from the centre
- For _large $\Delta w$_ (small $R$ or large $d$), the diffraction pattern approaches _two single-edge patterns_ 
- For _intermediate_ $\Delta w$, there may be an _on-axis minimum_ with 2 maxima on the side
![[Fresnel diffraction patterns.png]]
### The circular aperture: on-axis
- Start from the _most general form_
- _Retain the obliquity factor_ and define $s=\rho^2=x^2+y^2$
- The _on-axis_ diffraction integral is:
$$\psi_P\propto\int_{s=0}^{s=r_a^2}\frac{K}{\sqrt{a^2+s}\sqrt{b^2+s}} \,\exp\left(\frac{i\pi s}{\lambda R}\right)\pi\,ds$$
- $K$ _decreases with $s$_
- One can evaluate this integral _graphically_ using a _Phasor diagram_:
![[Fresnel circular phasors.png]]
- As phase is _linear_ with $s$, the diagram is _approximately circular_ with _decreasing radius_ 
- The diffracted amplitude is represented by the _spanning vector_ between the origin and point on the diagram with _arc length $s$_
- For an _unobstructed aperture_, $s$ goes to infinity, and the amplitude is the _radius of the outer circle_

- For _finite_ obstructions, there are points where phase is an integer of multiple of $\pi$:
$$\displaylines{\rho^2=2n\lambda R \Rightarrow \phi=2n\pi \Rightarrow \psi\approx 0 \\ \rho^2=(2n+1)\lambda R \rightarrow \phi=(2n+1)\pi \rightarrow \psi\approx 2\psi_u}$$
- From this, one can see there are _concentric circlar zones in the aperture plane_, across which the phase at the _central observation point_ changes by $\pi$
- The $n$th _Fresnel half-period zone_ is an _annulus_ satisfying:
$$\displaylines{(n-1)\pi<\phi(\rho)<n\pi \\ \sqrt{(n-1)\lambda R}<\rho<\sqrt{n\lambda R}}$$
- In the quadratic approximation, the _area of each zone_ is always $\pi\lambda R$

- Neglecting $K$ and variations in $r_1r_2$, _each zone contributes equally_
	- Odd zones add, even zones subtract
- Approximations break down _for large apertures_
	- "Spiralling in" of the phasor diagram, the obliquity factor, and higher order terms means _outer zones are wider than predicted_

### Circular obstruction
- Consider an _on-axis circular obstruction_, with small radius $r_a$
- The spanning vector is _from the centre_ of the circles, to a point with phase $\phi_a=\pi r_a^2/(\lambda R)$
- Provided $\phi_a$ is not too large, _there will be a bright spot on the axis_, known as _Poisson's spot_

### The circular aperture: off-axis
- The zones are _centred on the line between source and observation line_
- Fixing those 2 points, _the aperture shifts sideways to obstruct zones_
- This means as observation point _moves off-axis, intensity oscillates_
- From symmetry, _the fringes must be circular_

- Fringe spacing is _approximately equal to zone width at aperture edge_
- For larger apertures, as _zone widths decrease_, fringe spacing gets smaller
- A _long way off-axis_, intensity falls rapidly as there is a large number of narrow zones

### The Fresnel zone plate
- A zone plate _blocks out alternate Fresnel half-period zones_
- Let the edges of the $n$th zone on the plate be $\rho_n$
- For $N$ open zones in the plate, the net amplitude on axis is $\approx2N\psi_u$
- The incident wave is _focused_ at the observation point, as the plate acts as a _lens_ with focal length:
$$f=R=\frac{\rho_1^2}{\lambda}=\frac{\rho_n^2}{\lambda}$$

- Moving the observation point _along the axis towards the zone plate_, the zones _become smaller_
- When the new distance $R'=f/(2m)$, each open area _allows an even number of zones_, meaning $\psi_{P'}\approx0$
- When $R'=f/(2m+1)$, each open area admits _an odd number of zones_, hence $\psi_{P'}\approx 2N\psi_u$
	- Reduces for increasing $m$ due to obliquity factor, but still remain as _maxima_

# Interferometry
- Consider two waves interfering:
$$\Psi=\Re\left\{\psi_1\exp(-i\omega_1t)+\psi_2\exp(-i\omega_2t)\right\}$$
- Most detectors respond to _intensity_
- Expressing the wave functions as:
$$\psi_1=a_1\exp(i\phi_1)\hspace{1.5cm}\psi_2=a_2\exp(i\phi_2)$$
- The detector often _cannot detect quickly oscillating signals_
- Retaining the slowest oscillating term:
$$\braket{I}\propto\frac{1}{2}\braket{a_1^2}+\frac{1}{2}\braket{a_2^2} +\braket{a_1a_2}\Re\left\{\exp[i(\phi_1-\phi_2-(\omega_1-\omega_2)t)]\right\}$$
- To get good detection, $(\omega_1-\omega_2)\tau<<1$, where $\tau$ is the _response timescale_
- For most cases, $\omega_1=\omega_2$ to a very good degree of approximation

- The sources must be _coherent_, meaning $\phi_1-\phi_2$ must be constant, and the waves must come from _the same source_
- Coherency usually achieved using _lasers_

- Interfering waves can be derived from _different spatial points of a wavefront_ (spatial coherence)
- They can also be derived from _dividing amplitude_ (e.g. By reflection and transmission)

## The Michelson interferometer
![[Michelson.png]]
- The _beam-splitter_ splits then recombines the beam
- Interference depends on _path difference_
- Mechanical vibration can _smear_ the fringes

- Simplest form: the beams are _focused onto a photodiode_, intensity is recorded _as a function of mirror position_ to retrieve the interference pattern

- _Without the lens_, _circular fringes_ can be seen on a plane (see Lipson)

- One can also use an _extended light source_
- Beams originating from different parts of the source have a _differential delay_ to produce _fringes_ while still holding the mirrors fixed

- With $\omega_1=\omega_2$, the intensity _averaged over response time_ is:
$$\mean{I}=\frac{1}{2}\mean{a_1^2}+\frac{1}{2}\mean{a_2^2}+\mean{a_1a_2\Re{\left[e^{i\delta}\right]}}$$
- Here, $\delta=(\phi_1-\phi_2)=kx$ is the _phase difference_ between the two beams, where $x$ is the _path difference_
- If the beams have equal intensities $I=I_0/2$:
$$I(x)=I_0\left(1+\Re\left[e^{ikx}\right]\right)$$
- $x$ is a _function of positions of the mirrors and beamsplitter_

## Fourier transform spectrometry

## Thin film spectrometry

## Fabry-Perot interferometer