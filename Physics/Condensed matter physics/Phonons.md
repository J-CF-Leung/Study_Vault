- Phonons are _collective excitations_ in a lattice
- They are the [[Oscillations#Normal modes|normal modes]] of the system, where:
	- All atoms oscillate at the _same frequency_
	- All displacements are at _fixed ratios_ to each other

- The corresponding frequencies and displacements can be derived _classically_
- However, the _energies_ of the normal modes must follow the [[Quantum Harmonic Oscillator]]:
$$E_n=\left(n+\frac{1}{2}\right)\hbar\omega$$

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

- The phonon has _group velocity_ corresponding to the _velocity of sound_ in the solid:
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
	- Associated with the _travelling wave_, not associated with the particles
- If it interacts with an _external particle_ (i.e. scattering), then the _overall momentum must be conserved_
- If the initial and final wave-vectors of the external particle are $\bm{k}_i$ and $\bm{k}_f$, then it is _analagous to_ [[Crystal structure and diffraction#Diffraction|diffraction]]:
$$\bm{k}_f=\bm{k}_i+\bm{q}$$
- This corresponds to the _annihilation_ of a phonon with wavevector $\bm{q}$, or the _creation_ of a phonon with wavevector $-\bm{q}$
- Due to _energy conservation_, this scattering is _inelastic_

- If two phonons _coalesce_ and form a _new phonon_:
$$\bm{q}_\text{new}=\bm{q}_1+\bm{q}_2$$
- If it lies _outside_ the first Brillouin Zone, then $\bm{G}$ can be _subtracted_ for an equivalent $\bm{q}_\text{new}$

- Hence, the momentum conservation for _neutron scattering_ can be modified as:
$$\bm{k}_f=\bm{k}_i\pm\bm{q}\pm\bm{G}$$
- The _plus_ signs refer to the _annihilation_ of a phonon
- The _minus_ signs refer to the _creation_ of a phonon

- Similarly, _energ conservation_ requires:
$$\frac{\hbar^2}{2m}k_f^2=\frac{\hbar^2}{2m}k_i^2\pm\hbar\omega$$

- In practice, _monochromatic particle beams_ are used for diffraction
	- $\bm{k}$ are controlled by _scattering angles_ relative to the surface 
	- Each different $\bm{k}_f$ corresponds to a _different phonon interaction_
	- $\omega$ is measured by _time of flight_
	- The _neutron energy_ depends on the _type_ of phonon
	- There may also be an _elastic peak_

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

- The _lower branch_ is known as the _acoustic mode_
	- As $q\to0$, it corresponds to _sound waves_
	- As $q\to0$, $\omega\to0$
- The _upper branch_ is known as the _optical mode_
	- It interacts _strongly with electromagnetic radiation_ of similar $\omega$
	- Photons can be _absorbed_ to create phonons