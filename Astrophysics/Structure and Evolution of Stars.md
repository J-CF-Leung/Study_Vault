- The _Big Bang_ formed a universe of _ionised gas_
- About $400,000$ years after the Big Bang the universe became _cool_, there was an epoch of _recombination_, after which the universe was _mostly neutral hydrogen_

- About $600$ million years later was the _epoch of reionisation_, where the _first stars_ emitted _enough energetic photons_ to _reionise_ the elements
- Most of the universe then becomes _transparent_ to light

- At the _end of a star's life cycle_, they form _supernovae or gamma ray bursts_, with the _latter_ happening to _massive, rapidly rotating stars_

- Most stars have _their own planetary systems_

- Many stars are in _binary/multiple systems_
- If they are _massive_, they form _neutron stars_ and _black holes_, which can then _merge to form gravitational waves_
- The _resultant neutron star/black hole_ has a mass _smaller than the sum of previous masses_, as energy is emitted in the G-waves
![[Stellar graveyard.png]]
# Useful units

## Distances and masses
- Radius of _Earth's orbit_: 1 Astronomical Unit (AU) = $1.496\times 10^{11}\,\text{m}$
- Sun and moon: 0.5 arcminutes in the sky
- Parsec: distance at which _$1\,\text{AU}$ subtends $1$ arc second_ = $206265 \,\text{AU}$
![[Parsec definition.png]]
- Nearest star: Proxima Centauri, $1.3\,\text{pc}$ away, $\theta=0.764\,\text{arcsec}$
- To the _galactic centre_: $8.5\,\text{kpc}$

- Astronomical coordinate system:
![[Astronomical coordinate system.png|500]]

- Radius of the Sun: $6.96\times 10^{8} \,\text{m}$

- Mass of sun $M_\odot=1.989\times 10^{30}\,\text{kg}$
- Milky Way: $\approx 1\times10^{11}\,M_\odot$

## Luminosity
- Brightness is measured on a _log scale_

- The _flux_ of a star is _energy per unit time per unit area_
- Given two _fluxes_ $F_1$ and $F_2$, the _magnitudes_ $m$ are defined as:
$$\frac{F_1}{F_2}=10^{0.4(m_2-m_1)}$$
- The _luminosity_ $L$ of a star is the _total power_
	- For a _star_, it is $4\pi d^2F$

- The _absolute magnitude_ $M$ of an object is the magnitude of the object would have if placed at a _distance_ of $10\,\text{pc}$, from which a _distance modulus_ is defined:
$$m-M=2.5\log(d/10)^2=5\log d-5$$
- $d$ is the _distance in parsecs_

# Galactic Chemical Evolution
- Definition: an object where _nuclear reactions balance surface radiative losses_

- Birth of a star:
	- A _cloud_ of cold gas is pushed _out of equilibrium_ by some perturbative process (e.g. a passing shockwave)
	- The cloud _collapses_, with potential energy converting into _heat_
	- As _temperature_ and _density_ increase, nuclear _fusion_ begins
	- _Hydrogen_ is fused to _helium_
	- This provides a _non-gravitational source of energy_
	- This _maintains temperature and pressure_

- Death of a star:
	- After helium, _heavier elements_ are formed
	- However, elements _heavier than iron_ will _not yield energy when fused_
	- Once the star has an _iron core_, it is _unable to maintain pressure_
	- The _outer layers_ are often ejected, in _supernova explosions_ or _planetary nebulae_

- Left: Crab nebula, remnants of supernova
- Right: Helix nebula, planetary nebula
![[Nebulae.png]]

- Heavy elements/_metals_: anything produced by _stellar evolution_ or _supernovae_
	- In other words, not $\text{H}$, $\text{He}$, or $\text{Li}$, which were created during _big bang nuclearsynthesis_
- After a star's death, its elements are _returned to the interstellar medium_
- Hence, there is a _cycle_ of _galactic/cosmic chemical evolution_

![[Solar system elements.png]]

- Recent _composition_ of _regions of star formation_:
	- Hydrogen: $X=0.7392$
	- Helium: $Y=0.2486$
	- Everything else: $Z=0.0122$

- Galaxies have _different regions_, with distinct populations, kinematics, ages and metallicities:
![[Milky way schematic.png]]
- The _disk_ contains _most of the stellar mass_, and is often _metal rich_, with many _young stars_
- The _bulge_ is _thicker_ and _roughly spherical_, with a young and old stars, and a _supermassive black hole_
- The _halo_ has largely _dispersion-dominated kinematics_, is _metal-poor_, and has _globular clusters_ containing _very old objects_

# Stars
- Most stars form in _clusters_
- To first approximation, they are:
	- Roughly at the _same distance_ from us
	- Roughly the _same age_
	- Roughly the same _chemical composition_

- The _main properties_ of a star:
	- Mass
	- Temperature
	- Luminosity
	- Gravity
	- Age
	- Chemical composition $(Z)$
- _Mass_ is typically the _dominant factor_ in all factors _except chemical composition_

## Motion
- Tracking a star's position and _eliminating the effects of Earth's orbit_ gives the _proper motion_ of a star
	- Position of stars _within a galaxy_ is _not fixed_
	- Measured in $\text{arcsec}/\text{yr}$

- One can measure the _redshift_ of a star to find the _radial velocity_
- Reddening can either be due to _motion_ or is _intrinsic_
- Therefore, one must use _well-defined spectral features_
- The redshift is defined as:
$$z\equiv\frac{\lambda_\text{obs}-\lambda_0}{\lambda_0}$$
- One can then find the _radial velocity_ $v$:
$$v=cz$$
- This is a _limiting case_ of the _result from special relativity_, as $v<<c$

- By _combining_ proper motion and radial velocity, one finds the _true space motion_ of a star

## Luminosity
- One measures the light of a star through _broad-band filters_
- _Vega_ provides a _zero-point_ for magnitude:
![[Vega spectrum.png]]

- One can often _estimate_ the spectrum for a star with a _blackbody spectrum_
- This is given by _Planck's Law_:
$$\displaylines{B_\lambda(T)=\frac{2hc^2}{\lambda^5}\frac{1}{\exp(hc/\lambda kT)-1}\\ B_\nu(T)=\frac{2h\nu^3}{c^2}\frac{1}{\exp(h\nu/kT)-1}}$$
- The _maximum_ of the spectrum is given by _Wien's displacement law_:
$$\lambda_\text{max}T=0.290\text{ cm K}$$
- The _energy per unit area per unit time_ is given by the _Stefan-Boltzmann law_:
$$\int B_\lambda\,d\lambda=\sigma T^4$$
- The _total luminosity_ is then:
$$L=4\pi R^2\sigma T^4$$
- By _comparing the fluxes through different filters_, one has a _photometric estimate_ of the star's _effective temperature_
- The _Hertzsprung-Russell diagram_:
![[H-R diagram.png]]