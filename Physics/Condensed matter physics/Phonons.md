- The atoms in a lattice can be _excited_ in order to vibrate
- They are the [[Oscillations#Normal modes|normal modes]] of the system, where:
	- All atoms oscillate at the _same frequency_
	- All displacements are at _fixed ratios_ to each other
- Quantum mechanically, they are described by _multi-particle wave functions_

- The corresponding frequencies and displacements can be derived _classically_
- However, the _energies_ of the normal modes must follow the [[Quantum Harmonic Oscillator]]:
$$E_n=\left(n+\frac{1}{2}\right)\hbar\omega$$
- A vibration of energy $E_n$ can be said to have $n$ _phonons_, which are _quasiparticles_, of energy $\hbar\omega$, with a particular _wave vector_ $\bm{k}$ and momentum associated with the nature of the vibration
- As modes are _excited_, more phonons are said to be _created_


# Uniform 1D Harmonic crystal

## The travelling wave
![[1D harmonic crystal.png]]
- If there are $N$ atoms, there are $N$ _normal modes_
- Assume _cyclic boundary conditions_, where $u_{n}=u_{n+N}$
- Using Hooke's Law:
$$m\ddot{u}_n=\alpha(u_{n+1}+u_{n-1}-2u_n)$$

- For each normal mode, from symmetry:
	- All atoms have the _same amplitude_
	- They oscillate at the _same frequency_
	- There can only be a _constant phase shift_ between atoms:
$$u_{n+1}=u_n\exp(i\delta)$$

- Then, assume a harmonic solution:
$$u_n=u_0\exp(i\omega t)$$
- Then, substituting into the equation of motion, one gets:
$$\omega(\delta)=\sqrt{\frac{4\alpha}{m}}\left|\sin\left(\frac{\delta}{2}\right)\right|$$
- The phase is only _unique over a range_ of $2\pi$
- There is a _fixed relationship_ between the _phase difference_ and oscillation _frequency_

- The _displacement_ of the $n$th atom is then:
$$u_n=u_0\exp[i(n\delta-\omega t)]$$
- Write the phase difference as:
$$\delta =qa$$
- Here, $q$ is the _phonon wavevector_
- Then, substituting $x=na$, one gets that the modes are _travelling waves_:
$$u_n=u_0\exp[i(qx-\omega t)]$$
- Therefore, one gets the _dispersion relationship_:
$$\omega(q)=\sqrt{\frac{4\alpha}{m}}\left|\sin\left(\frac{qa}{2}\right)\right|$$
- The wavevector is only defined over a _range_:
![[Phonon dispersion relationship.png]]
- This range is known as the _First Brillouin Zone_ of the [[Crystal structure and diffraction#The reciprocal lattice|reciprocal lattice]]

- For values of $q$ outside the range, _"aliasing"_, as the _phases_ of each atom are unchanged, so the value has _no physical significance_:
![[Phonon alisasing.png]]

- In other words, a phonon with wavevector $\bm{q}$ is _equivalent_ to one with wavevector $\bm{q}+n\bm{G}$
	- This corresponds to the _periodicity of the lattice_

- The _number of modes_ is equal to the _number of atoms_ $N$
- This leads to _discrete values_ of $q$, with separation $2\pi/(Na)$, which is usually very _small_

## Properties
- As the wave is technically modelled as the [[Quantum Harmonic Oscillator]], the energy of the wave is actually _quantised_:
$$E_n=\left(n+\frac{1}{2}\right)\hbar\omega$$
- Every mode has a _zero-point energy_

- The _momentum_ associated with the phonon is $\hbar q$
	- Applying the _momentum operator_ to the wave function

- The phonons have _group velocity_ corresponding to the _velocity of sound_ in the solid:
$$v_g=\pd{\omega}{q}$$

- The phonons themselves have _particle character_, being _bosons_

### Wavelength limits
- At the _Brillouin zone boundary_, $q=\pi/a$, the wavelength is at a _minimum_, $2a$
- The _phase difference_ between each atom is $\pi$
- One then gets a _standing wave_, at the _maximum possible frequency_
$$\omega_\text{max}=\sqrt{\frac{4\alpha}{m}} \hspace{1cm} \pd{\omega}{q}=0$$

- Meanwhile, at the _long wavelength limit_, where $q\to0$:
$$\omega\approx\sqrt{\frac{4\alpha}{m}}\frac{qa}{2}$$
- The frequency is _directly proportional to wave-vector_:
$$v_p=v_g=\sqrt{\frac{\alpha a}{m/a}}=\sqrt{\frac{Y}{\rho}}$$
- This is the [[Waves#Sound in liquids and solids|speed of sound in the solid]]

## Complex behaviour
- In a _real lattice_, atoms can have _longer range interactions_, such as with the _next nearest_ neighbour
- For the next nearest neighbour interactions, the _wavelength is doubled_
- One can _superpose_ the solutions as the system is _linear_
- One then obtains:
$$\omega^2=\frac{4}{m}\left(k_1\sin^2\left(\frac{qa}{2}\right)+k_2\sin^2\left(qa\right)\right)$$

![[Phonons with more interactions.png]]


- Technically, the interaction potential is _anharmonic_, allowing phonons to _interact with each other_ without complete destructive interference

## Crystal momentum, scattering, and phonon interactions
- A phonon with wavevector $q$ has a _crystal momentum_ $\hbar q$
	- Associated with the _travelling wave/phonon itself_, not associated with the particles
- If it interacts with an _external particle_ (i.e. scattering), then the _overall momentum must be conserved_
- If the initial and final wave-vectors of the external particle are $\bm{k}_i$ and $\bm{k}_f$, then it is _analagous to_ [[Crystal structure and diffraction#Diffraction|diffraction]]:
$$\bm{k}_f=\bm{k}_i+\bm{q}$$
- This corresponds to the _annihilation_ of a phonon with wavevector $\bm{q}$, or the _creation_ of a phonon with wavevector $-\bm{q}$
- Due to _energy conservation_, this scattering is _inelastic_

- If the momentum of a _created phonon_ lies _outside_ the first Brillouin Zone, then $\bm{G}$ can be _added or subtracted_ for an equivalent $\bm{q}_\text{new}$

- Hence, the momentum conservation for _neutron scattering_ can be modified as:
$$\bm{k}_f=\bm{k}_i\pm\bm{q}\pm\bm{G}$$
- The _plus_ signs refer to the _annihilation_ of a phonon
- The _minus_ signs refer to the _creation_ of a phonon

- Similarly, _energy conservation_ requires:
$$\frac{\hbar^2}{2m}k_f^2=\frac{\hbar^2}{2m}k_i^2\pm\hbar\omega$$

- In practice, _monochromatic particle beams_ are used for diffraction
	- $\bm{k}$ are controlled by _scattering angles_ relative to the surface 
	- Each different $\bm{k}_f$ corresponds to a _different phonon interaction_
	- $\omega$ is measured by _time of flight_
	- The _neutron energy_ depends on the _type_ of phonon
	- There may also be an _elastic peak_

- Similarly, phonons can [[#Phonon-phonon scattering|scatter with other phonons]]

# 1D Diatomic Lattice
- Consider a _1D diatomic chain with two types of atoms_:
![[1D diatomic lattice.png]]
- $a$ is _half the size of the unit cell_

- The _equations of motion_ are:
$$\displaylines{m_A\ddot{u}_{2n}=\alpha(u_{2n+1}+u_{2n-1}-2u_n) \\ m_B\ddot{u}_{2n+1}=\alpha(u_{2n+2}+u_{2n}-2u_{2n+1})}$$
- Using the _trial solutions_:
$$u_{2n}=U_1\exp[i(2nqa-\omega t)] \hspace{1cm} u_{2n+1}=U_2\exp[i((2n+1)qa-\omega t)]$$
- Substituting these into the equations of motion:
$$\omega^2=\frac{\alpha}{m_Am_B}\left[(m_A+m_B)\pm\left\{(m_A+m_B)^2-4m_Am_B\sin^2(qa)\right\}^2\right]$$

- The two solutions form _two branches_ in the dispersion relationship:
![[Phonon branches.png]]
- As the lattice now _repeats_ after $2a$, the _edges_ of the Brillouin zone are at $\pm\pi/2a$

- The _lower branch_ is known as the _acoustic mode_
	- As $q\to0$, it corresponds to _sound waves_
	- As $q\to0$, $\omega\to0$
- The _upper branch_ is known as the _optical mode_
	- It interacts _strongly with electromagnetic radiation_ of similar $\omega$
	- Photons can be _absorbed_ to create phonons

- At the _edge_ of the first Brillouin zone:
$$\omega_A\left(q=\pm\frac{\pi}{2a}\right)=\sqrt{\frac{2\alpha}{m_A}} \hspace{1cm} \omega_O\left(q=\pm\frac{\pi}{2a}\right)=\sqrt{\frac{2\alpha}{m_B}}$$
- At the _centre_ of the zone:
$$\omega_A(q\to 0)\approx \sqrt{\frac{2\alpha}{m_A+m_B}}qa \hspace{1cm} \omega_O(q=0)=\sqrt{\frac{2\alpha}{\mu}}=\sqrt{2\alpha\left(\frac{1}{m_A}+\frac{1}{m_B}\right)}$$
- $\mu$ is the _reduced mass_ of the two atoms

- In the _acoustic mode_, neighbouring atoms move _roughly in phase_
- In the _optical mode_, neighbouring atoms move _roughly out of phase_
	- As _oppositely charged_ particles oscillate out of phase, this _couples strongly with an oscillating electric field_ (photons)
	- Photons of similar $\omega$ has a _very small_ wavenumber compared to other wavenumbers in the Brillouin zone
![[Acoustic optical mode displacements.png]]

- At the _zone boundaries_, each mode correspond to different _standing waves_ of wavelength $4a$, where _different sets_ of atoms move depending on the mode
![[Zone boundary acoustic optical modes.png]]
- The _lower energy_ mode corresponds to movement of _lighter atoms_
- The _higher energy_ mode corresponds to movement of _heavier atoms_

## Backfolding
- The formation of _branches_ can be understood using the process of _backfolding_
- Initially, the Brillouin zone spans $-\pi/a < q < \pi/a$
- Then, for a diatomic lattice, it is _halved_ and spans $-\pi/2a<q<\pi/2a$
- The "branches" _outside_ the zone are then _shifted_ by $\pm\pi/a$

- Then, due to _unequal masses_, the branches _split_:
![[Backfolding.png]]

- The _centre_ of the optical branch corresponds to a wavevector of $\pi/a$ in the original lattice, or a _wavelength_ of $2a$

# 3 dimensional lattices
- There are _different dispersion curves_ for _longitudinal_ and _transverse_ modes, in both _optical_ and _acoustic_ branches (if the lattice is not monoatomic)
	- Depending on the _propagation direction_, transverse modes can be _degenerate_

## Monoatomic FCC solid
- There are _only acoustic modes_, but split into _longitudinal_ and _transverse_ modes
![[Neon phonon dispersion.png]]

- _Longitudinal_ modes are typically _higher energy_
	- It is harder to _compress_ a bond than to _shear_ a bond
- _Transverse_ modes are commonly degenerate along _high symmetry_ directions
	- $(\xi\,0\,0)$ and $(\xi\,\xi\,\xi)$ but _not_ $(\xi\,\xi\,0)$

- In $fcc$, due to the structure of the lattice, there are _many neighbours_, leading to _multiple Fourier components_ for the longitudinal mode

- Further example: Lead
![[Lead phonon dispersion.png]]

## Rock salt
- Dispersion relations in $\ce{NaCl}$:
![[Salt dispersion relation.png]]

- Each _optical_ and _acoustic_ branch has its own _longitudinal_ and _transverse_ modes
- Dispersion along $(\xi\,\xi\,\xi)$ is _similar_ to the 1D diatomic lattice as there are _alternating planes_ of $\ce{Na}$ and $\ce{Cl}$

- The highest frequencies in an _ionic solid_ also tend to be _higher_ than those in a _covalent crystal_, due to the strength of the ionic bonds

# Phonon-phonon scattering
- Purely _harmonic_ normal modes _do not scatter_
	- They are the _stationary states_ of a Hamiltonian, and remain _unperturbed_
- However, due to _anharmonic effects_, they can scatter
	- Spring constant is _variable_ depending on the size of oscillation

- As one phonon _distorts_ the lattice, another phonon can _diffract off_ the phonon
![[Phonon scattering.png|450]]
- Phonons can _coalesce_: 
$$\hbar\bm{q}_3=\hbar\bm{q}_1+\hbar\bm{q}_2 \hspace{2cm} \hbar\omega_3=\hbar\omega_1+\hbar\omega_2$$
- Phonons can also _decompose_, or equivalently _diffract off_ $-\bm{q}_2$

- Scattering processes can be separated into _normal scattering_ and _Umklapp scattering_
- In _normal scattering_, the _direction_ of the wave-vector often has _no significant change in direction

- In _Umklapp scattering_, the resulting phonon wavevector lies _outside the first Brillouin zone_
- Folding back results in a _negative group velocity_
- This _strongly randomises the direction_
- It often occurs at _high temperatures_ as _higher energy phonons_ are required
![[Normal Umklapp scattering.png]]

# Heat capacities of insulators
- One can calculate the _energy stored in a crystal_ via its phonons
- Then, one can calculate its _contribution to the crystal's heat capacity_

- Only the energy of _atoms_ are included, in the form of [[Phonons|lattice vibrations]], with many _modes_ of different frequencies $\omega$
$$E_n=\left(n+\frac{1}{2}\right)\hbar\omega$$

- As temperature increases, more _modes_ are excited, hence energy increases

- Each mode has a _zero-point energy_, which can be ignored in calculating _heat capacity_

- Experimental measurements yield the _Dulong-Petit Law_, where at _high temperatures_:
$$C\approx 3Nk_B$$

## Internal energy
- Each vibrational mode contributes _separately_ to internal energy

### Energy of one mode
- If the solid is in _contact_ with a reservoir of temperature $T$, then the _number of phonons $n$ in a mode_ of frequency $\omega$ follows the [[Statistical thermodynamics#Boltzmann Distribution|Boltzmann Distribution]]:
$$P_n\propto\exp\left(-\frac{n\hbar\omega}{k_BT}\right)\equiv\exp(-n\beta\hbar\omega)$$
- One can then write the [[Statistical thermodynamics#The Partition Function|Partition Function]]:
$$Z=\sum_{n=0}^\infty \exp\left(-n\beta\hbar\omega\right)=\frac{1}{1-\exp(\beta\hbar\omega)}$$
- The _average energy_ stored in the $i$th mode at temperature $T$ is then:
$$E_i=-\frac{1}{Z}\pd{Z}{\beta}=\frac{\hbar\omega_i}{\exp(\beta\hbar\omega_i)-1}$$

### Total internal energy
- To find the _total internal energy_ of the solid, one _sums over all modes_:
$$U=\sum_\text{modes} \frac{\hbar\omega_i}{\exp(\beta\hbar\omega_i)-1}$$
- Convert this into an _integral_, with function $g(\omega)$ indicating the _density of states_ corresponding to $\omega$:
$$U=\int\frac{\hbar\omega_i}{\exp(\beta\hbar\omega_i)-1}\,g(\omega)\,d\omega$$
- This is _valid for a sufficiently large crystal_ due to the _tight spacing of allowd $k-$states_

### High and low temperature limits
- At _high temperatures_, where $\beta\hbar\omega_i<<1$:
$$E_i\approx k_BT$$
- This agrees with the [[Statistical thermodynamics#The classical limit: equipartition|equipartition theorem]], where each vibrational mode has $k_BT$ of energy, _independent of frequency_
- For $N$ atoms, there must be $3N$ normal modes
- Hence, at _high temperatures_, one gets the _Dulong-Petit law_, for the _total internal energy_ of the solid:
$$U\approx 3Nk_BT \hspace{2cm} C\approx 3Nk_B$$
- At _low temperatures_, where $\beta\hbar\omega_i>>1$:
$$E_i\approx\hbar\omega_i\exp\left(-\frac{\hbar\omega_i}{k_BT}\right)$$
## Debye model of the density of states
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
- Use a _mean speed of sound_, summing over that of _longitudinal_ modes $v_L$ and _transverse_ modes, $v_T$:
$$\frac{1}{v_s^3}=\frac{1}{3}\left(\frac{1}{v_L^3}+\frac{2}{v_T^3}\right)$$
- Therefore:
$$g(\omega)=g(k)\frac{dk}{d\omega}=\frac{3V\omega^2}{2\pi^2v_s^3}$$

- Can also be derived using _periodic boundary conditions_, allowing for _all values of $k$_

### The Debye frequency
- Integrate to obtain $U$, while accounting for the _correct number of modes_
- There are $3N$ modes, hence define the _Debye frequency_ $\omega_D$:
$$3N=\int_0^{\omega_D} g(\omega)\,d\omega$$
- One then finds the frequency as:
$$\omega_D^3=\frac{6\pi^2v_s^3N}{V}$$

- _Roughly_, this corresponds to the frequency where $\lambda=2a$
	- The _shortest possible_ wavelength

## Expression for heat capacity
- Using the above expressions:
$$U=\int_0^{\omega_D}g(\omega)\frac{\hbar\omega}{\exp(\beta\hbar\omega)-1}\,d\omega=\frac{3V\hbar}{2\pi^2v_s^3}\int_0^{\omega_D}\frac{\omega^3}{\exp(\hbar\omega/k_BT)-1}\,d\omega$$
- To find _heat capacity_, differentiate under the integral, then after _algebra:
$$C=\pd{U}{T}=9Nk_B\left(\frac{T}{\theta_D}\right)^3\int_0^{\theta_D/T}x^4\frac{e^x}{\left(e^x-1\right)^2}\,dx$$
- Where the changes of variable are:
$$\displaylines{\hbar\omega_D=k_B\theta_D \\ x=\frac{\hbar\omega}{k_BT}}$$
- $\theta_D$ is known as the _Debye temperature_
- It can be understood as a temperature under which modes become _"frozen out"_ and remaining in an _unexcited_ state
![[Debye heat capacity.png]]

## High and low temperature limits
- At _high temperatures_, or $T>>\theta_D$:
$$C\approx 9Nk_B\left(\frac{T}{\theta_D}\right)^3\int_0^{\theta_D/T}\frac{1}{x^2}\,dx=3Nk_B$$- This regains the _Dulong-Petit law_

- At _low temperatures_, as _higher frequency modes_ are not excited and do not contribute:
$$C\approx 9Nk_B\left(\frac{T}{\theta_D}\right)^3\int_0^\infty x^4\frac{e^x}{(e^x-1)^2}\,dx=\frac{12\pi^4}{5}Nk_B\left(\frac{T}{\theta_D}\right)^3$$
- This is known as the _Debye $T^3$ law_
- It can be understoof using a _semi-classical approximation_:
	- At _low temperatures_, the _fraction of modes occupied_ is on the order of $(\omega_T/\omega_D)^3$
	- Hence, there are $\sim 3N(T/\theta_D)^3$ excited modes, each of which has $\sim k_BT$ of energy
	- Therefore, $U\sim T(T/\theta_D)^3$ and $C\sim (T/\theta_D)^3$

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
- The heat flux due to _one mode_ is then:
$$H=-\frac{1}{3}(c_\text{ph}n)l\mean{c}\frac{dT}{dz}$$
- Therefore, the _total thermal conductivity_
$$\kappa=\frac{1}{3}C\mean{c}l$$
- $C$ is the _heat capacity per unit volume_
- $\mean{c}$ can often be approximated as the _speed of sound_

## Scattering
- Scattering processes will _reduce the mean free path_
- There are _different processes_ that contribute

- The _rate of scattering processes_ is:
$$\Gamma=\frac{1}{\tau}=\frac{\mean{c}}{l}=\frac{\mean{c}}{l_1}+\frac{\mean{c}}{l_2}+\dots$$
- Hence, mean free paths add _reciprocally_:
$$\frac{1}{l}=\sum_i\frac{1}{l_i}$$

- The scattering can be _geometric_, from sample _boundaries_ or _impurities_
- This gives a _temperature-independent_ mean free path

- Scattering can also [[Phonons#Phonon-phonon scattering|occur between phonons]]
- At _lower temperatures_, this is _less significant_ as there are _fewer phonons_
	- Typically, _higher temperatures_ are required for _Umklapp scattering_ which actually _randomises_ directions in order to lower conductivity significantly

## Variation with temperature
![[Germanium conductivity.png]]
- At _low temperatures_, the mean free path is _roughly constant_ due to geometric scattering
- Hence, due to the [[#High and low temperature limits|Debye law]], $\kappa\propto T^3$ due to the heat capacity

- At _high temperatures_, the number of phonons scales with $T$
- The heat capacity is also _roughly constant_
- Hence, the mean free path and $\kappa$ scale with $1/T$

- At _intermediate temperatures_, phonon-phonon scattering is typically _normal scattering_
- Even after scattering, phonons still travel in _roughly the same direction_
- Therefore, the conductivity is _higher than expected_