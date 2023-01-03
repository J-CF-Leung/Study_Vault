#IB_Natsci 

- Spectroscopy: _Determining structures using the interaction of electromagnetic radiation with matter_

## Physical principles and approximations

- Contributions to the energy of a molecule are: 
	- Translation (_ignored_ as light does not significantly affect motion)
	- Vibration
	- Rotation
	- Electronic

- These energies are _quantised_
- The _energy level spacing_ for the different contributions are _on very different scales_
- With the [[Molecular quantum mechanics#The Born-Oppenheimer approximation|Born-Oppenheimer approximation]], the different contributions can be regarded as _independent of each other_
- Thus, the energy level _transitions are also independent_:
$$\displaylines{\Delta E_\text{tot}=\Delta E_\text{elec}+\Delta E_\text{vib}+\Delta E_\text{rot} \\ \Delta E_\text{elec}>>\Delta E_\text{vib} >> \Delta E_\text{rot}}$$
![[Energy level spacings.png]]

- Not all transitions between energy levels are allowed: see [[Molecular quantum mechanics#Spectroscopic principles]]

- Vibrational transitions are _always accompanied by_ rotational transitions
- Similarly, electronic transitions are _always accompanied by_ vibrational and rotational transitions
- Corresponding sections of the EM spectrum for transitions:
![[Wavelengths for transitions.png]]

## Summary of spectroscopy

### Low-resolution infrared spectroscopy
- Details from IA: [[IA Spectroscopy- NMR and IR#IR spectroscopy]]
- Broadly able to tell _what bonds are present_ via peaks found in particular ranges of wavenumber

### Origin of spectra
- A spectrum arises from the _absorption or emission of photons_, changing the molecular energy level
- This can occur in three ways:
	- _Absorption_: $M+h\nu\rightarrow M^*$
	- _Spontaneous emission_: $M^* \rightarrow M+h\nu$
	- _Stimulated emission_: $M^*+h\nu\rightarrow M+2h\nu$

- All of these require an _oscillating dipole_ with a _frequency corresponding to the interacting photon_

### Pure rotational spectra
- A _pure_ rotational spectrum is one generated only from microwave radiation 
- To generate an _oscillating electric field_ while rotating, the molecule must possess a _permanent dipole moment_
	- The component along one direction will oscillate
- This requires _a difference in electronegativity_ between atoms plus symmetry requirements

### Vibrational spectra
- This also requires a _difference in electronegativities_ as _internuclear distance oscillates_ to bring about a change in dipole moment

### Raman spectroscopy
- Many molecules _cannot generate the required oscillating dipole_ (such as homonuclear diatomics)
- For these molecules, _Raman spectroscopy_ is needed

- In Raman spectroscopy, photons of _any energy_ are absorbed by the molecule
- The oscillating electric field _induces a dipole_ in the molecule
- The molecule is promoted to a _virtual state_ 
	- The energy of this state does not necessarily match an energy level
- A photon is then re-emitted
- This is analagous to the classical phenomenon of _scattering_

- The _majority_ of photons emerge with the _same energy as before_, meaning the "collision" is _elastic_, this is known as _Rayleigh scattering_: $M+h\nu\rightarrow M+h\nu$

- Some photons emerge with _different energies_
- _Stokes scattering_ lowers radiation frequency, _raising molecular energy level_
$$M+h\nu'\rightarrow M^*+h\nu\hspace{0.3cm}, \hspace{0.3cm}\nu'>\nu$$
- _Anti-Stokes scattering_ raises radiation frequency, _lowering molecular energy level_
$$M^*+h\nu\rightarrow M+h\nu'\hspace{0.3cm}, \hspace{0.3cm}\nu'>\nu$$

- In order for inelastic scattering to occur, the molecule's _polarisability_ must change during vibration or rotation

#### Mathematical description
- From the [[Electromagnetism#Molecular origins of dielectrics|definition of polarisability]], the dipole moment $\bm{\mu}$ of a molecule given an electric field $\bm{E}$ is:
$$\bm{\mu}=\alpha\bm{E}$$
- Given an _oscillating electric field_ $E=E_0\sin2\pi\nu t$, the dipole also oscillates:
$$\mu=\alpha E_0\sin2\pi\nu t$$
- If the molecule is either _rotating or vibrating_ with frequency $\nu_m$, the polarisability can be written as:
$$\alpha=\alpha_0+\beta\sin2\pi\nu_mt$$
- So, the dipole oscillates with _three distinct frequency components_:
$$\mu=\alpha_0E_0\sin2\pi\nu t+\frac{1}{2}\beta E_0\left\{\cos2\pi(\nu-\nu_m)t-\cos2\pi(\nu+\nu_m)t\right\}$$
- If $\beta=0$ (i.e. invariant polarisability), _Raman spectroscopy is impossible_

### NOTATION
- Quantities in _wavenumbers_ with units of $\text{cm}^{-1}$ are denoted with a tilde ~
- $\tilde{c}$ is the speed of light in $\text{cm s}^{-1}$

- Branches of emission lines:
| $\Delta J$        | $-2$ | $-1$ | $0$ | $+1$ | $+2$ |
| ----------------- | ---- | ---- | --- | ---- | ---- |
| Naming convention | O    | P    | Q   | R    | S     |


## Rotational microwave spectroscopy
- Applicable to molecules with a _permanent dipole moment_

### Rotating molecules
- A molecule moving in 3-dimensions has _three principal axes_
- Thus, angular momentum can be decomposed into 3 components, $x$,$y$, and $z$
- The components are given by the equations:
$$L_i=I_i\omega_i$$
- Here, $I_i$ is the _moment of inertia_ for the $i$th direction
- $\omega_i$ is the _angular velocity_ for the $i$th direction

- A _spherical top_ molecule has $I_x=I_y=I_z$
- For a _linear_ molecule, $I_x=I_y$, $I_z=0$

### The rigid rotor
- _Diatomic molecules_ can be modelled by a [[Molecular quantum mechanics#The Rigid Rotor|rigid rotor]]
- Let the masses be $m_1$ and $m_2$, and be separated by distance $r$
- The moment of inertia is:
$$I=\mu r^2=\frac{m_1m_2}{m_1+m_2}r^2$$
- The energy levels are given by:
$$E_J=BJ(J+1)\hspace{0.3cm},\hspace{0.3cm}J=0,1,2,3\text{...}$$
- $B$ is the _rotational constant_, in Joules, the formula is:
$$B=\frac{\hbar^2}{2I}$$
- In wavenumbers:
$$\tilde{B}=\frac{h}{8\pi^2\tilde{c}I}$$
- The energy in wave-numbers:
$$\mathcal{E}_J=\tilde{B}J(J+1)$$

### Degeneracy of energy levels
- $J$ specifies $L^2$
- Angular momentum can take different orientations
- Each energy level has a $(2J+1)-$fold degneracy as the _magnetic quantum number_ $M_J$ can take integer values from $-J$ to $J$
- $M_J$ specifies $L_z$

### Populations of energy levels
- From the _Boltzmann distribution_, with the _degeneracy_, the _population_ of each rotational energy level _relative to ground level_ is:
$$N_J\propto(2J+1)\exp\left(-\frac{h\tilde{c}\tilde{B}J(J+1)}{kT}\right)$$
- From this, there is an energy level with _maximum population_:
$$J_\text{max}\approx \sqrt{\frac{kT}{2h\tilde{c}\tilde{B}}}-\frac{1}{2}$$

### Transitions between energy levels
- From [[Molecular quantum mechanics#Spectroscopic principles|Fermi's Golden Rule]], not only do the molecules need to have a _permanent dipole moment_, there is also a restriction on $\Delta J$:
$$\Delta J=\pm1$$
- The difference in wavenumber from energy level $J$ to $J+1$ is:
$$\Delta\mathcal{E}=\mathcal{E}_{J+1}-\mathcal{E}_J=2\tilde{B}J(J+1)$$
- This gives _equally spaced transitions_ of $2\tilde{B},4\tilde{B},6\tilde{B},...$
![[Rotational transitions.png|450]]

- The _intensity_ of a peak depends on the _population_ of the originating energy level
- Practically, emission (both spontaneous and stimulated) must be taken into account
![[N2O rotational spectrum.png]]

### Linear polyatomic molecules
- For linear polyatomic molecules, transitions are _also spaced by $2\tilde{B}$_
- However, given a molecule $A-B-C$, the moment of inertia is:
$$I=m_Ar_{AB}^2+m_Cr_{BC}^2-\frac{(m_Ar_{AB}-m_Cr_{BC})^2}{m_A+m_B+m_C}$$
- Therefore, to determine _both bond lengths_, the technique of _isotopic substitution_ is used
- Assuming _bond length does not change_, this changes $\tilde{B}$
- Therefore, both bond lengths can be found

## Rotational Raman spectroscopy
- For rotational Raman spectroscopy to work, _polarisability must change during rotation_
- The selection rule in rotational Raman spectroscopy is:
$$\Delta J=0,\pm2$$
- The change in rotational energy for $|\Delta J|=2$ is therefore given by:
$$\mathcal{E}_\text{upper}-\mathcal{E}_\text{lower}=\tilde{B}(4J+6)$$
- _Stokes lines_, where the molecule gains energy, are at $\tilde{\nu}_\text{incident}-\tilde{B}(4J+6)$
- _Anti-Stokes lines_, where the molecule loses energy, are at $\tilde{\nu}_\text{incident}+\tilde{B}(4J+6)$
![[Raman lines.png]]
- $\Delta J$ is defined by convention to be $J(\text{upper})-J(\text{lower})$
- Therefore, all Raman lines _are in the S branch_
![[N2 Raman.png]]

## Vibrational potentials and selection rules

## Vibrational spectroscopy for diatomics

## Vibration modes in polyatomic molecules

## Electronic spectroscopy

