# Main characteristics

## Heat
- The earth has _internal heat_

- The Earth can _lose heat_, with the current rate at $4\times 10^{13}\text{ W}$, or $80\text{ mW m}^{-2}$
- _Sources_ of heat:
	- _Release_ of _gravitational energy_
	- _Tidal dissipation_ of _kinetic energy_
	- _Radioactive decay_

- Earth's _temperature field_ is dependent on 
	- _Initial_ temperature distribution
	- Distribution (spatial and temporal) of _heat sources_
	- The _mechanism_ of _internal heat transfer_

- Heat flux is _low_ in _old continental sheilds or oceanic sea floor_ $(\approx 40\text{ mW m}^{-2})$
- Heat flux is _high_ in _tectonically active continental regions_, and _near ocean ridges_ $(\approx 100\text{ mW m}^{-2})$

- The primary means of _heat transfer_ is _convection_

![[Earth heat flow.png]]

## Gravitational field
- Gravitational field on the surface: $\approx 9.827\text{ ms}^{-2}$
	- Corresponds to _homogeneous sphere_ of mass $5.98\times 10^{24} \text{ kg}$ and radius $6.371\times 10^{5}\text{ m}$
- Gravity _fluctuates_ throughout the _surface_ of Earth, due to _asymmetry_ in mass distribution within the _crust and mantle_

- The _reference spheroid/ellipsoid_ is an _equipotential surface_ that coincides with _mean sea-level_ on an _imaginary rotating Earth_ with the _same mass and size_ as the _real_ Earth but with _uniform mass distribution_

- The _geoid_ is the _equipotential surface_ that coincides with the _mean sea level_ on the real Earth
	- Deviates from reference ellipsoid by up to $\pm 100\text{ m}$
![[Gravity references.png]]
![[Geoid deviation.png]]
- The _geoid_ does _not_ show the outline of continents
	- One uses _mass compensation_ at some _depth_ in the Earth, to account for the _lack of variation in $g$_ between (dense) continents and (light) oceans
	- Different models: _Pratt_ and _Airy_ compensation
![[Pratt andf Airy compensation.png]]

- On a timescale of $\sim 10^{4}\text{ yrs}$ or greater, the Earth behaves as a _viscous fluid_

## Earth's magnetic field
- The Earth's magnetic field has existed for $\sim 3.5\times 10^{9}\text{ yrs}$

- It can be modelled as a _dipole_ at the centre of the Earth, _tilted_ at $10^{\circ}$ from the rotational axis
	- Pole strength: $65,000\text{ nT}$
	- Equator strength: $25,000\text{ nT}$
![[Earth magnetic field.png]]
- There is a _secular variation_ in the _magnetic declination_, the _angle_ between the _magnetic North_ and _true North_, with a _westward shift_ of $\sim0.2^{\circ}/\text{yr}$

- _Reversals_ occur at _random intervals_ between $10^{5}-5\times 10^{7}\text{ yrs}$

## Seismology
- _Information_ on the Earth interior comes from _seismology_
- _Divisions_ of the Earth:
	- Crust: $\sim 1\%$
	- Mantle: $\sim 68\%$
	- Core: $\sim 31\%$

- On _short time scales_, the Earth is _elastic_, and transmits _elastic waves_
- Two main kinds of waves: _P waves_ (compression) or _S waves_ (shear)
![[Earth elastic waves.png]]

- _Whole earth_ oscillation modes:
![[Whole earth oscillation modes.png|600]]
- One _earthquake_ can _diffract_ and cause multiple seismogram measurements in different places on the Earth:
![[Earthquake diffraction.png]]
- The _locations_ and _mechanisms_ of these waves give information about the _location of the fault_ and the nature of the plate movement

![[Earth velocity profile.png|500]]
- There are zones where seismic activity is _roughly constant_, which _alternate_ with zones where _wave velocity increases with depth_

## Composition of the Earth
- _Evidence_ of the Earth's composition comes from _meteorites_ and _volcanic nodules_
- The dominant _upper mantle_ material is _olivine_
	- A _magnesium/iron/silicon oxide_
- With _high pressure_, olivine will _rearrange_ to _pack more closely_
	- _High pressure_ can be _replicated_ using _large presses_, _shock waves_, and _diamond cells_

- The _core_ is mainly _iron_
	- With some _nickel_ and _light elements_

- Profile of Earth:
![[Earth composition profile.png|500]]
- _Alternating zones_ of wave velocity are likely due to _changes in packing arrangement_ instead of composition

## Governing equations
- Continuum mechanics equations, modelling Earth
	- Short timescales: _elastic solid_
	- Long timescales: _viscous fluid_

- _Incompressibility_:
$$\nabla\cdot \boldsymbol{v}=0$$
- _Cauchy's equation_: momentum transport
$$\rho\left( \frac{\partial \boldsymbol{v}}{\partial t}+(\boldsymbol{v}\cdot \nabla)\boldsymbol{v} \right)=\nabla\cdot \underline{\underline{\sigma}}+\boldsymbol{f}$$
- _Conservation of energy_/heat flow:
$$\rho C_{p}\left( \frac{\partial T}{\partial t}+(\boldsymbol{v}\cdot \nabla)T \right)=\nabla\cdot(k\nabla T)+\rho H$$