# One-dimensional models

## Identical atoms
- Simplest model: row of _identical atoms_
	![[Identical atoms phonons.png]]
	- Inter-atomic spacing $a$
	- Atomic mass $m$
	- Spring constant $K$

- Displacement of the $n$th atom $u_{n}$ obeys:
$$m\frac{\partial^{2}u_{n}}{\partial t^{2}}=K(u_{n+1}-u_{n})-K(u_{n}-u_{n-1})$$
- _Harmonic solution_ of wave-vector $q$:
$$u_{n}(t)=u_{0}\cos(qr_{n}-\omega(q)t)$$
- This gives:
$$\omega(q)=2\sqrt{ \frac{K}{m} }\left| \sin\left( \frac{qa}{2} \right) \right| $$
- It is _periodic_ in $q$ with period $2\pi/a$
![[Monoatomic chain dispersion.png]]

- The _long wavelength modes_ $q\to 0$ gives _linear dispersion_
	- Same for a _wire_ with tension $Ka$ and _density_ $m/a$
	- They are _compressive waves_ with group and phase velocity $\sqrt{ K/m }$ 

- These waves behave as _sound waves_, and are an _acoustic mode_

- For $qa=0$ and $qa=2\pi$, neighbouring atoms are _in phase_
	- Wavelength is effectively $a$
- For $qa=\pi$, they move in _antiphase_

- One can consider only the _range_:
$$-\frac{\pi}{a}<q<\frac{\pi}{a}$$
- Values _outside_ are equivalent to the value at $q-2n\pi$
	- Analagous to _aliasing_
- This corresponds to the _first Brillouin zone_
![[Phonon aliasing.png]]

## Two types of atoms
- Consider _two different types_ of atoms in a unit cell, giving different masses and spring constants:
![[Diatomic chain.png]]
- The equations of motion:
$$\begin{align} m_{A}\frac{\partial^{2}u_{n,A}}{\partial t^{2}}&= K(u_{n,B}-u_{n,A})-K'(u_{n,A}-u_{n-1,B}) \\ m_{B} \frac{\partial^{2}u_{n,B}}{\partial t^{2}}&=K'(u_{n+1,A}-u_{n,B})-K(u_{n,B}-u_{n,A})\end{align}$$

### Diatomic molecules
- The limit of _same mass_ $(m_{A}=m_{B})$, with $K\gg K'$, simulating a _chain of strongly bound diatomics_
	- Let the spacing _between molecules_ be $a_{2}$

- Then each molecule has a mode where _each atom oscillates out of phase_
	- The coordinate $u_\text{opt}(q=0)=u_{A}-u_{B}$ undergoes oscillation

- _Branches_ to the dispersion curve
	- Acoustic branch: for low frequency, it vanishes _linearly_ with $q$
	- Optical branch: finite frequency as $q\to 0$, often _interacts with light_
- The optical branch frequency is _largely independent of_ $q$
![[Diatomic dispersion curve.png|500]]
- Atomic displacements:
![[Acoustic optical displacements.png]]
### Same springs, different masses
- In the limit of the _same spring constant_
- With lattice constant $a$, travelling wave solutions lead to:
$$\begin{align}u_{n,A}&= \\ u_{n,B}&=\end{align}$$

- Limiting results:
![[Acoustic optical phonons.png|500]]
- The branches _split_ such that there are _no solutions_ between $\sqrt{ 2K/m_{A} }$ or $\sqrt{ 2K/m_{B} }$


# Real phonons

## 3 dimensions
- 3 dimensions: _transverse_ and _longitudinal_ modes
- For a solid with $m$ atoms per unit cell:
	- $3$ acoustic modes (2 transverse, 3 longitudinal)
	- $3(m-1)$ optical modes

- Plot along a _path in reciprocal space_
![[Ge phonon dispersion.png|600]]

## Inelastic neutron scattering
- Inelastic neutron scattering: neutron _transfers_ energy and momentum _to phonons_
$$\boldsymbol{Q}=\boldsymbol{k}'-\boldsymbol{k}+\boldsymbol{G}$$
- Here, $\boldsymbol{G}$ is _any reciprocal lattice vector_
- Measurement: outgoing neutron energy:
$$E(\boldsymbol{Q})=\varepsilon(\boldsymbol{k}')-\varepsilon(\boldsymbol{k})$$

![[Inelastic neutron scattering.png]]

# Density of states and heat capacity
- For a _1D chain_ of $N$ atoms, there must be $N$ _modes_
- The allowed _density of states_, with _periodic boundary conditions_, are then:
	- There is a _maximum momentum_ on the _Brullouin zone boundary_ (due to the _discreteness_ of the atomic chain)
$$k_{n}=\frac{2\pi}{L}n \hspace{1cm}n=[]$$
- Here, $a=L/N$ and $<k<$
- In 3 dimensions, each _branch_ has $N=L^{3}/\Omega _\text{cell}$ states
- The volume for each $k-$state is $(2\pi)^{3}/L^{3}$

- The _Einstein model_ assumes a _flat dispersion_ $\omega(\boldsymbol{k})=\omega_{0}$
- The _density of states_ per branch is then $D_{E}(\omega)=$
- This is suitable for _optical branches_

- For _acoustic modes_, with _linear dispersion_, use $\omega=vk$
- Density of states
- This _fails at the zone boundary_
- _Cut off_ at the Debye frequency
- _Count_ the number of states and cut off at $N$:
$$\int _{0}^{\omega_{D}}D_{D}(\omega) \, dx $$
- _Replacing_ the Brillouin zone with a _sphere_ of radius $k_{D}=\omega_{D}/v$

- Einstein: phonons obey [[Advanced statistical mechanics#The Bose gas|Bose-Einstein distribution]]
- As their _number is not conserved_, $\mu=0$:
$$n(\omega)=\frac{1}{\exp()}$$
- For $k_{B}T<\hbar\omega$
- For $k_{B}T>\hbar\omega$

- The _internal energy_:
$$U=\int  D(\omega)n(\omega)\hbar\omega \, d\omega =$$
- The _heat capacity_:
$$C_{V}=$$
- At _low temperatures_
- Dulong-Petit
- _Characteristic temperature_

- Debye model
- At _low temperatures_, the contribution of _optical modes_ is _small_
- Debye temperature
- Substitution: $x=\hbar\omega/k_{B}T$
- Factor of $3$ for different modes

- Internal energy:
$$U_{D}=$$
- Heat capacity:
$$C_{V}=$$
- For $T\gg\theta_{D}$, $x\to 0$, giving $C_{V}=3Nk_{B}$
- Low temperature: $\propto T^{3}$

- Phonons and electrons:
$$C_{V}=$$
- Straight line plot

- At _low temperatures_, it is difficult to _thermally excite_ optical modes, giving the _Einstein model_ a _low heat capacity_
- Real density of states
	- _Branches_ of the phonon spectrum
	- van Hove singularities: the dispersion is _flat_, giving an _infinite_ density of states

# Heat capacity
- For _heat flux_ $\boldsymbol{J}_{q}$ (energy per unit area per unit time)
$$\boldsymbol{J}_{q}=-\kappa \nabla T$$
- Kinetic theory:
$$\kappa=\frac{1}{3}C_{B}lv=\frac{1}{3}C_{V}v^{2}\tau$$
- $v$: phonon velocity
- $l=v\tau$: mean free path
- $\tau$: scattering time

- $v$ is the _speed of sound_, which is _almost constant_
- Scattering processes:
	- Normal and Umklapp scattering
	- Point defects
	- Sample boundaries
	- Crystal dislocations
$$\tau^{-1}=\sum \tau^{-1}=$$
- Low temperature: large $l$, $\tau$ given by _sample boundaries_ (constant w.r.t. $\tau$), giving $\kappa \propto T^{3}$
- Middle range: $\kappa$ often _peaks_, dominated by _impurity scattering_
- Beyond $\theta_{D}$, phonon _numbers_ increase, Umklapp scattering becomes important, $\kappa$ _decreases_ rapidly

![[Thermal conductivities.png]]