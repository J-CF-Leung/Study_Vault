- One can calculate the _energy stored in a crystal_ via its normal modes, or [[Phonons]]
- Then, one can calculate its _contribution to the crystal's heat capacity_

- If the crystal is also a _conductor_, the _electrons_ also contribute to energy

# Heat capacities of insulators
- Only the energy of _atoms_ are included, in the form of [[Phonons|lattice vibrations]], with many _modes_ of different frequencies $\omega$
$$E_n=\left(n+\frac{1}{2}\right)\hbar\omega$$

- As temperature increases, more _modes_ are excited, hence energy increases

- Each mode has a _zero-point energy_, which can be ignored in calculating _heat capacity_

## Internal energy


## The density of states
- Assuming the crystal is a _rectangular box_ of side lengths $A, B, C$
- The _phonon modes_ are simply _plane wave states_, which satisfy the _boundary conditions_
- The allowed wave-vectors are then:
$$\bm{k}=\left(\frac{n_x\pi}{A},\frac{n_y\pi}{B},\frac{n_z\pi}{C}\right)$$
- These states then form a _lattice_ in $k-$_space_
- Each state occupies a _volume_ $\pi^3/(ABC)=\pi^3/V$

- Then, consider the states within a _shell_ of width $dk$
	- Only consider _positive_ $k$, hence an _eighth_ of a sphere
- The _number of states_ in that shell is:
$$dN=g(k)\,dk=\frac{3(4\pi k^2/8)\,dk}{\pi^3/(ABC)}$$
- $g(k)$ is the _density of states_ in $k-$space:
$$g(k)=\frac{3Vk^2}{2\pi^2}$$
- The factor of 3 accounts for _transverse and longitudinal modes_
- Then, transforming to $\omega-$space:
$$g(\omega)\,d\omega=g(k)\,dk$$
- The _Debye theory_ makes a simple _approximation_
- Assume a _linear dispersion relationship_, for _all wavelengths_
	- In reality, only holds for _small wavelengths_ due to the _atomic nature_ of the material
$$\omega=v_sk$$
- Here, $v_s$ is the _speed of sound_
- Therefore:
$$g(\omega)=g(k)\frac{dk}{d\omega}=\frac{3V\omega^2}{2\pi^2v_s^3}$$

- Can also be derived using _periodic boundary conditions_, allowing for _all values of $k$_

## The Debye frequency
- Integrate to obtain $U$, while accounting for the _correct number of modes_
- There are $3N$ modes, hence define the _Debye frequency_ $\omega_D$:
$$3N=\int_0^{\omega_D} g(\omega)\,d\omega$$
- _Roughly_, this corresponds to the frequency where $\lambda=2a$
	- The _shortest possible_ wavelength

## Limitations
- At _low_ $\omega$, the _actual dispersion relationship_ is also approximately linear, hence the Debye model is a _good match_

- At _high_ $\omega$, for phonons _near the zone boundary_ (which depends on the lattice), there are _large deviations_ from the large relationship
- Phonons with _different modes_ also have different disperion relationships

# Thermal conductivity in insulators
- In insulators, heat is _carried by phonons_, which _conduct heat_ by travelling along the crystal
- Phonons will travel a certain distance before they are _scattered_

## Deriving the conductivity
- They have some _mean free path_ $l$

- Consider the _excess energy_ in a phonon crossing a plane at angle $\theta$:
![[Travelling phonon excess energy.png]]
$$c_\text{ph}\Delta T=c_\text{ph}\frac{dT}{dz}\Delta z=-c_\text{ph}\frac{dT}{dz}l\cos\theta$$
- Let the _distribution_ of phonon speed $c$ be $nf(c)$
- Then, _integrating over all angles_ in a plane to obtain _total normal heat flux_:
$$H=\int_0^\pi \int_0^\infty \left(nf(c)\,dc\frac{2\pi\sin\theta\,d\theta}{4\pi}\right)\left(c\cos\theta\right)\left(-c_\text{ph}\frac{dT}{dz}l\cos\theta\right)$$
- Working out the integral, and letting there be an _average speed_:
$$\int_0^\infty cf(c)\,dc=\mean{c}$$
- The heat flux is then:
$$H=-\frac{1}{3}(c_\text{ph}n)l\mean{c}\frac{dT}{dz}=-\kappa\frac{dT}{dz}$$

## Scattering
- Scattering processes will _reduce the mean free path_
- There are _different processes_ that contribute

- The _rate of scattering processes_ is:
$$\Gamma=\frac{1}{\tau}=\frac{\mean{c}}{l}=\frac{\mean{c}}{l_1}+\frac{\mean{c}}{l_2}+\dots$$

- The scattering can be _geometric_, from sample _boundaries_ or _impurities_
- This gives a _temperature-independent_ mean free path

- Scattering can also _scatter with other phonons_
- The scattering is only possible because the interaction is _anharmonic_
	- As bonds are _compressed_, the spring constant _changes_
- A phonon can _"diffract"_ due to another phonon
- This is _temperature dependent_