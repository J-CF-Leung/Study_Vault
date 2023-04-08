
- Spectroscopy: _Determining structures using the interaction of electromagnetic radiation with matter_

# Physical principles and approximations

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

# Summary of spectroscopy

## Low-resolution infrared spectroscopy
- Details from IA: [[IA Spectroscopy- NMR and IR#IR spectroscopy]]
- Broadly able to tell _what bonds are present_ via peaks found in particular ranges of wavenumber

## Origin of spectra
- A spectrum arises from the _absorption or emission of photons_, changing the molecular energy level
- This can occur in three ways:
	- _Absorption_: $M+h\nu\rightarrow M^*$
	- _Spontaneous emission_: $M^* \rightarrow M+h\nu$
	- _Stimulated emission_: $M^*+h\nu\rightarrow M+2h\nu$

- All of these require an _oscillating dipole_ with a _frequency corresponding to the interacting photon_
- This leads to the _gross selection rules_ for each type of spectroscopy, specifying _what molecules_ can generate that type of spectrum
- Then, there are _specific selection rules_ detailing _which transitions_ are allowed

## Pure rotational spectra
- A _pure_ rotational spectrum is one generated only from microwave radiation 
- To generate an _oscillating electric field_ while rotating, the molecule must possess a _permanent dipole moment_
	- The component along one direction will oscillate
- _Gross selection rule_:  There must be a _permanent dipole moment_
	- Caused by an _electronegativity difference_, plus the right type of _symmetry_

## Vibrational spectra
- As _internuclear distance oscillates_, a _change in dipole moment_ can be caused
- _Gross selection rule_: At _equilibrium_, there must be a _non-zero rate of change in dipole moment_:
$$\pd{\mu}{q}\Bigg|_\text{eq}\neq0$$

## Raman spectroscopy
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

- _Gross selection rule_: The molecule's _polarisability_ must have a _non-zero rate of change_ at _equilibrium_
$$\pd{\alpha}{q}\Bigg|_\text{eq}\neq0$$

### Mathematical description
- This is a mostly _classical description_, which is not wholly accurate
- From the [[Electromagnetism#Molecular origins of dielectrics|definition of polarisability]], the dipole moment $\bm{\mu}$ of a molecule given an electric field $\bm{E}$ is:
$$\bm{\mu}=\alpha\bm{E}$$
- Given an _oscillating electric field_ $E=E_0\sin2\pi\nu t$, the dipole also oscillates:
$$\mu=\alpha E_0\sin2\pi\nu t$$
- If the molecule is either _rotating or vibrating_ with frequency $\nu_m$, the polarisability can be written as:
$$\alpha=\alpha_0+\beta\sin2\pi\nu_mt$$
- So, the dipole oscillates with _three distinct frequency components_:
$$\mu=\alpha_0E_0\sin2\pi\nu t+\frac{1}{2}\beta E_0\left\{\cos2\pi(\nu-\nu_m)t-\cos2\pi(\nu+\nu_m)t\right\}$$
- If $\beta=0$ (i.e. invariant polarisability), _Raman spectroscopy is impossible_

## NOTATION
- Quantities in _wavenumbers_ with units of $\text{cm}^{-1}$ are denoted with a tilde ~
- $\tilde{c}$ is the speed of light in $\text{cm s}^{-1}$

- Branches of emission lines:
| $\Delta J$        | $-2$ | $-1$ | $0$ | $+1$ | $+2$ |
| ----------------- | ---- | ---- | --- | ---- | ---- |
| Naming convention | O    | P    | Q   | R    | S     |


# Rotational microwave spectroscopy
- Applicable to molecules with a _permanent dipole moment_

## Rotating molecules
- A molecule moving in 3-dimensions has _three principal axes_
- Thus, angular momentum can be decomposed into 3 components, $x$,$y$, and $z$
- The components are given by the equations:
$$L_i=I_i\omega_i$$
- Here, $I_i$ is the _moment of inertia_ for the $i$th direction
- $\omega_i$ is the _angular velocity_ for the $i$th direction

- A _spherical top_ molecule has $I_x=I_y=I_z$
- For a _linear_ molecule, $I_x=I_y$, $I_z=0$

## The rigid rotor
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

## Degeneracy of energy levels
- $J$ specifies $L^2$
- Angular momentum can take different orientations
- Each energy level has a $(2J+1)-$fold degneracy as the _magnetic quantum number_ $M_J$ can take integer values from $-J$ to $J$
- $M_J$ specifies $L_z$

## Populations of energy levels
- From the _Boltzmann distribution_, with the _degeneracy_, the _population_ of each rotational energy level _relative to ground level_ is:
$$N_J\propto(2J+1)\exp\left(-\frac{h\tilde{c}\tilde{B}J(J+1)}{kT}\right)$$
- From this, there is an energy level with _maximum population_:
$$J_\text{max}\approx \sqrt{\frac{kT}{2h\tilde{c}\tilde{B}}}-\frac{1}{2}$$

## Transitions between energy levels and selection rule
- From [[Molecular quantum mechanics#Spectroscopic principles|Fermi's Golden Rule]], not only do the molecules need to have a _permanent dipole moment_, there is also a restriction on $\Delta J$:
$$\Delta J=\pm1$$

- _Intuitive_ explanation: The _photon carries angular momentum_ of $\hbar$, therefore the molecule _gains or loses_ angular momentum when absorbing/emitting it

- The difference in wavenumber from energy level $J$ to $J+1$ is:
$$\Delta\mathcal{E}=\mathcal{E}_{J+1}-\mathcal{E}_J=2\tilde{B}J(J+1)$$
- This gives _equally spaced transitions_ of $2\tilde{B},4\tilde{B},6\tilde{B},...$
![[Rotational transitions.png|450]]

- The _intensity_ of a peak depends on the _population_ of the originating energy level
- Practically, emission (both spontaneous and stimulated) must be taken into account
![[N2O rotational spectrum.png]]

## Linear polyatomic molecules
- For linear polyatomic molecules, transitions are _also spaced by $2\tilde{B}$_
- However, given a molecule $A-B-C$, the moment of inertia is:
$$I=m_Ar_{AB}^2+m_Cr_{BC}^2-\frac{(m_Ar_{AB}-m_Cr_{BC})^2}{m_A+m_B+m_C}$$
- Therefore, to determine _both bond lengths_, the technique of _isotopic substitution_ is used
- Assuming _bond length does not change_, this changes $\tilde{B}$
- Therefore, both bond lengths can be found

# Rotational Raman spectroscopy
- For rotational Raman spectroscopy to work, _polarisability must change during rotation_
- The selection rule in rotational Raman spectroscopy is:
$$\Delta J=0,\pm2$$

- _Intuitive_ explanation: The photon can pass through _without changing spin_, which gives _elastic_ scattering; or it can _change spin direction_, which changes molecule angular momentum by 2 units

- The change in rotational energy for $|\Delta J|=2$ is therefore given by:
$$\mathcal{E}_\text{upper}-\mathcal{E}_\text{lower}=\tilde{B}(4J+6)$$
- _Stokes lines_, where the molecule gains energy, are at $\tilde{\nu}_\text{incident}-\tilde{B}(4J+6)$
- _Anti-Stokes lines_, where the molecule loses energy, are at $\tilde{\nu}_\text{incident}+\tilde{B}(4J+6)$
![[Raman lines.png|600]]
- $\Delta J$ is defined by convention to be $J(\text{upper})-J(\text{lower})$
- Therefore, all Raman lines _are in the S branch_
![[N2 Raman.png|600]]
# Vibrational potentials and selection rules
![[Internuclear potential.png|500]]
- General behaviour of a diatomic:
	- If stretched or compressed, there is a _restoring force_
	- The more _compressed_ the molecule is, the _stronger the repulsion_
	- As the molecule is _stretched_ more and more, the molecule _dissociates_ with $V(r)\to0$
## The harmonic oscillator
- Form of potential:
$$V(x)=\frac{1}{2}kx^2$$

- More details: [[Molecular quantum mechanics#Nuclei: The quantum harmonic oscillator|The quantum harmonic oscillator]]
- The _intrinsic frequency of oscillation_ is given by:
$$\displaylines{\omega=\sqrt{\frac{k}{\mu}}\\ \tilde{\omega}=\frac{1}{2\pi\tilde{c}}\sqrt{\frac{k}{\mu}}}$$
- The energy levels are given by:
$$\displaylines{E_\nu=\left(\nu+\frac{1}{2}\right)\hbar\omega \\ \mathcal{E}_\nu=\left(\nu+\frac{1}{2}\right)\tilde{\omega}}$$
- As before, the molecule can only give a _vibrational spectrum_ if it has a _change in dipole moment_
- There is a _specific selection rule_ for the harmonic oscillator, derived from Fermi's Golden Rule:
$$\Delta\nu=\pm1$$
- Therefore, _all allowed vibrations are at_ $\tilde{\omega}$
- The absorption spectrum should have a _single line_

## Anharmonic oscillator: the Morse potential
- Form of potential:
$$V_M(x)=D_e\left[1-\exp(-\beta x)\right]^2$$
- More details: [[Molecular quantum mechanics#Nuclei: The Morse oscillator|The Morse Oscillator]]
- $D_e$ determines well _depth_, $\beta$ determines well _steepness_

- Taylor expanding the potential for _small displacements_, it can be approximated as _quadratic_:
$$\displaylines{V_x\approx D_e\beta^2x^2=\frac{1}{2}kx^2 \\k_M=2D_3\beta^2}$$
- Then, one can define the _frequency of small oscillations_:
$$\omega=\sqrt{\frac{k_M}{\mu}}$$

- The energy levels for this potential are:
$$\displaylines{E_\nu=\left(\nu+\frac{1}{2}\right)\hbar\omega-\left( \nu+\frac{1}{2}\right)^2\hbar\omega\chi_e \\ \mathcal{E}_\nu=\left(\nu+\frac{1}{2}\right)\tilde{\omega}-\left(\nu+\frac{1}{2}\right)^2\tilde{\omega}\chi_e}$$
- $\chi_e$ is the _anharmonicity constant_:
$$\chi_e=\frac{\hbar\beta^2}{2\mu\omega}$$
- The constant is _dimensionless_ and small, typically $<<1$

- Due to the negative term, energy level spacing _decreases_ with increasing $\nu$
- There is a _maximum energy level_ at:
$$\nu_\text{max}=\frac{1}{2\chi_e}-\frac{1}{2}$$
- The corresponding energy is $D_e$

- Due to the _zero-point energy_, the actual dissociation energy is $D_0=D_e-E_0$

- The population distribution _still follows the Boltzmann distribution_
- For typical molecules, $(E-E_0)>>kT$, hence _only the ground state is significantly populated at room temperature_

- The _specific selection rule is less restrictive_
- _All transitions are allowed_, as the asymmetric potential means the transition dipole moment, given by the Golden Rule, is _not completely cancelled out_
![[Morse transitions.png]]

- The appearance of the spectrum is:
![[Morse vib spectrum.png]]
- The lines are _approximately equally spaced_ since $\chi_e$ is small
- Typical spacing: $100-1000\text{cm}^{-1}$

- Vibrational spectrum of carbon monoxide:
![[C=O vib spectrum.png]]

- The hot band is _hidden under the fundamental_
- At _room temperature_, up to the 2nd overtone can be seen

- _Additional structure_ can be seen in the form of small peaks with spacing of $\approx10\text{cm}^{-1}$
- This is due to _change in rotational energy level_

# Vibrational spectroscopy for diatomics

## Vibrating rotor
- At _every vibrating energy level_, the molecule can have _many different rotational energies_
- However, the rotational constant is _not exactly the same for all vibrational states_

- As the _total energy_ gets higher, the _Born-Oppenheimer approximation starts to break down_
	- Independent from centrifugal distortion
- Since $\tilde{B}\propto 1/r^2$, and bond length increases with $\nu$, $\tilde{B}$ _decreases with $\nu$_
- The approximate relationship is:
$$\tilde{B}_\nu=\tilde{B}_e-\tilde{\alpha}\left(\nu+\frac{1}{2}\right)$$
- Here, $\tilde{B}_e$ is the rotational constant _at equilibrium_
- From this, the _equilibrium bond length_ can be found

## Spectrum
- In an IR spectrum of a _diatomic_, there is a _simultaneous change_ of both vibrational and rotational energy:
$$\Delta\nu=\pm1,\pm2,\pm3,...\hspace{1cm}\Delta J=\pm1$$
- Convention: 
	- _Rotational_ energy level in _lower vibrational state_: $J''$
	- _Rotational_ energy level in _upper vibrational state_: $J'$

- Transitions with $\Delta J=+1$ is denoted the _R branch_
	- _Higher_ wavenumber than pure vibrational transition
- Transitions with $\Delta J=-1$ is denoted the _P branch_
	- _Lower_ wavenumber than pure vibrational transition
- Transition lines are numbered by $J''$ (in the _lower vibrational energy level_)
	- Hence, _there is no_ $P_0$

- For _diatomics_, _only the P and R branches_ are seen

- For _any transition in the fundamental band_:
$$\begin{aligned}\mathcal{E}_\text{upper}-\mathcal{E}_\text{lower}&= \left[\frac{3}{2}\tilde{\omega}-\frac{9}{4}\tilde{\omega}\chi_e+\tilde{B}_1J'(J'+1)\right]-\left[\frac{1}{2}\tilde{\omega}-\frac{1}{4}\tilde{\omega}\chi_e+\tilde{B}_0J''(J''+1)\right] \\ &=\tilde{\omega}-2\tilde{\omega}\chi_e+\tilde{B}_1J'(J'+1)-\tilde{B}_0J''(J''+1) \\ &=\tilde{\omega}_0+\tilde{B}_1J'(J'+1)-\tilde{B}_0J''(J''+1)\end{aligned}$$

- For the purposes of simplifying the expressions, _assume_ $\tilde{B}_1\approx\tilde{B}_0\approx\tilde{B}$
- For the _R branch_, where $J'=J''+1$:
$$\begin{aligned}\tilde{R}_{J''}&=\tilde{\omega}_0+(\tilde{B}_1-\tilde{B}_0)J''^2+(3\tilde{B}_1-\tilde{B}_0)J''+2\tilde{B}_1 \\ &\approx\tilde{\omega}_0+2\tilde{B}(J''+1)\end{aligned}$$
- For the _P branch_, where $J'=J''-1$:
$$\begin{aligned}\tilde{P}_{J''}&=\tilde{\omega}_0+(\tilde{B}_1-\tilde{B}_0)J''^2-(\tilde{B}_1+\tilde{B}_0)J'' \\ &\approx \tilde{\omega}_0-2\tilde{B}J''\end{aligned}$$
- Hence, adjacent lines are _approximately $2\tilde{B}$ apart_
![[Vibrational fine structure.png]]

- The effect of $\tilde{B}_1<\tilde{B}_0$ can be seen for higher values of $J''$ as the _quadratic term becomes more significant_
	- As the term is positive, _all lines are shifted towards a lower frequency_
- In the _P branch_, the absorption lines become _more widely spaced_ as $J''$ increases
- In the _R branch_, the absorption lines become _more compressed_ as $J''$ increases
![[Carbon monoxide fundamental.png]]
## Finding the rotational constants
- To find $\tilde{B}_1$, consider _two transitions that share the same lower state_ $J$
- The energy difference between these two transitions is:
$$\tilde{R}_J-\tilde{P}_J=\mathcal{E}_1(J+1)-\mathcal{E}_1(J-1)=2\tilde{B}_1(2J+1)$$
- Hence, the plot of $\tilde{R}_J-\tilde{P}_J$  as a variable of $J$ is a _straight line_ with slot $4\tilde{B}_1$

- Similarly, to find $\tilde{B}_0$, consider _two transitions that share the same upper state_ $J$
- The energy difference is:
$$\tilde{R}_{J-1}-\tilde{P}_{J+1}=\mathcal{E}_0(J+1)-\mathcal{E}_0(J-1)=2\tilde{B}_0(2J+1)$$
- Once again, plot $\tilde{R}_{J-1}-\tilde{P}_{J+1}$ as a variable of $J$

- Using these values, $\tilde{\alpha}$, $\tilde{B}_e$ and the equilibrium bond length can be found

# Vibration modes in polyatomic molecules
- _Diatomics_ only have _one vibrational mode_
- For _polyatomic_ molecules, there are multiple characteristic _normal modes_, where _all_ atoms in a molecule move _synchronously_ with a different relationships between displacements
- All molecular vibration can be _broken down_ into the normal modes

- On the whole, a molecule with _N atoms_ has $3N$ _degrees of freedom_
- The _overall translation_ of the _centre of mass_ takes up 3 D.O.F.
- A _linear_ molecule only has 2 _rotational_ D.O.F.
- A _non-linear_ molecule has 3 _rotational_ D.O.F.

- Hence, a _linear_ molecule has $3N-5$ _vibrational modes_
- A _non-linear_ molecule has $3N-6$ _vibrational modes_
- Examples:
	- Diatomics: 1 vibrational mode
	- Bent triatomics ($H_2O$, $SO_2$): 3 vibrational modes
	- $CO_2$: 4 vibrational modes (2 stretches, 2 _degenerate_ bends)

- Convention: _Symmetric_ vibrations labelled _first_, with _decreasing frequency_, followed by _antisymmetric_

- For _ACYCLIC_ molecules, since there are $N-1$ bonds, there will be $N-1$ _stretches_, and the rest will be _bends_
- Example: Acetylene
![[C2H2 vibes.png]]

## Gross selection rules
- _Not all vibrational modes will appear in an IR or Raman spectrum_

### IR spectra
- For _IR spectra_, as mentioned above, the _gross selection rule_ is:
$$\frac{d\mu}{dx}\Bigg|_{x=0}\neq0$$
- Example: _symmetric stretch_ in a _mirror symmetric_ molecule (e.g. $CO_2$) is _IR-inactive_
- However, the _antisymmetric stretch_ and _symmetric bends_ are _IR-active_

### Raman spectra
- For _Raman spectra_, the _gross selection rule_ is:
$$\frac{d\alpha}{dx}\Bigg|_{x=0}\neq0$$
- Polarisability is _positively correlated to bond length_
- _Shorter bonds are harder to polarise_

- Example: _symmetric stretch_ in $CO_2$ is _Raman active_
- For the _antisymmetric stretch_ and _symmetric bend_, it is _equally polarisable in both directions_, hence at _equilibrium_, $d\alpha/dx=0$ and it is _Raman inactive_

### The rule of mutual exclusion
- For many molecules (e.g. $NO_2$), vibrational modes _can be both IR and Raman active_

- However, for molecules with a _centre of inversion_, it _cannot be both IR and Raman active at the same time_
![[Mutual exclusion.png]]

## Some actual spectra
- Simpler example: $SO_2$
![[SO2 IR.png]]

- Note: There are typically _more peaks than IR-active modes_
- There are _combination and difference bands_
- As mentioned before, there are also _overtones and hot bands_
![[Complicated spectrum.png]]

## Perpendicular and parallel vibrations
- Previously, the selection rules for a rigid rotor were $\Delta\nu=\pm1,\pm2,\dots$ and $\Delta J=\pm1$
- However, these _only hold for vibrations parallel to the axis_

- There are bends _perpendicular to the axis_ and are _degenerate_
- The degenerate modes _combine_ to produce _circular motion_
- The extra rotation makes it so that the new selection rules are:
$$\Delta\nu=\pm1,\pm2,\pm3,\dots\hspace{1cm}\Delta J=0, \pm1$$
- The $J=0$ transitions give rise to the _Q branch_
- From the same process as before, the frequency of the _fundamental_ is:
$$\mathcal{E}_\text{upper}-\mathcal{E}_\text{lower}=\tilde{\omega}_0 +(\tilde{B}_1-\tilde{B}_0)J(J+1)$$
- If $\tilde{B}_1\neq\tilde{B}_0$, this means the Q branch is _spread out_

- If there is no Q branch in _ANY vibrational mode_, the molecule _must be linear_
![[Parallel or perp vibrations.png]]

- For _bending modes_, the moment of inertia _decreases with degree of bending_
- Hence, $\tilde{B}_1>\tilde{B}_0$, and the _Q branch is spread out on the high frequency side_
- The _P and R branches_ also undergo the _opposite_ of the distortion seen for stretches

# Electronic spectroscopy

## Electronic energy levels
- Once an electron _changes state_, the _bond order_ is likely to change
- Promoting an electron _can change energies of all other electrons_
- This leads to a _different potential energy curve_
- These energy levels _may not be described by the original molecular orbitals_

- Each potential energy curve has _different parameters_ $r_e, \tilde{\omega}, \chi_e, D_0, D_e$
- They are denoted with _double prime_ $''$ for the _lower_ energy level and _single prime_ $'$ for the _upper_
- The _electronic excitation energy_ $T_e$ is measured _between the bottoms of the two curves_

![[Electronic energy levels.png]]

- The _Born-Oppenheimer approximation_ means the _electronic, vibrational and rotational energies are independent_

- Transitions are often _from the vibrational ground state_
- Depending on _temperature_, there may be transitions from $\nu''=1$ or $\nu''=2$ in the _UV-VIS spectrum_
- The vibrational wave functions in each electronic level _differ enough for $\Delta\nu$ to take any value_
- Each $\Delta\nu$ can _differ in intensity_
- However, there can be restrictions

### The transition dipole moment and Franck-Condon Factor
- According to [[Molecular quantum mechanics#Spectroscopic principles|Fermi's Golden Rule]], the intensity is proportional to the _transition dipole moment_:
$$B_{mn}\propto|\braket{\psi''|\hat{\mu}|\psi'}|^2$$
- From the _Born-Oppenheimer approximation_, the wave functions are _separable_:
$$\psi''=\psi''_E\psi''_V \hspace{1cm} \psi'=\psi_E''\psi_V''$$
- The _electronic wave functions_ $\psi_E$ are all from the _same electronic Hamiltonian_, and are _orthonormal_
- The _nuclear wave functions_ $\psi_V$ are all from _different nuclear Hamiltonians_ 

- The _dipole is also separable_:
$$\hat{\mu}=\hat{\mu}_E+\hat{\mu}_V$$
- Each _dipole operator_ $\hat{\mu}_i$ _only acts on respective electronic or vibrational coordinates_
- Expanding the inner product, one gets:
$$B_{mn}\propto |\braket{\psi_E''|\hat{\mu}_E|\psi_E'}|^2|\braket{\psi_V''|\psi_V
}|^2$$
- The former factor is the _electronic transition dipole moment_, which _must be non-zero_ for there to be a transition
- The latter factor is the _Franck-Condon Factor_
- This can be used to _estimate transition intensity_

## The Franck-Condon Principle, transitions and progressions
- The _Franck-Condon Principle_ asserts that the transition _occurs without appreciable change in geometry or bond length_
- This means the transition is _vertical_ in the energy diagram
- The _Franck-Condon Factor_ can be thought of as the _overlap between 2 vibrational wave functions_

- A _progression_ is a series of transitions _originating from the same $\nu''$_

- There are 3 cases for transitions:
	- Bond order _decrease_, or $r_e'>r_e''$
	- Bond order is _unchanged_, or $r_e'\approx r_e''$
	- Bond order _increase_, or $r_e'<r_e''$

- Only considering the _$\nu''=0$ progression:_
![[Electronic transitions.png]]

- If _bond order decreases_, there is a _weak $\nu'=0$ transition_, with _greatest overlap when_ $\nu''>>0$
- If _bond order is unchanged_,  the $\nu'=0$ transition is the _strongest_
- If _bond order increases_, it is similar to the $r_e'>r_e''$ case but there are _fewer strong transitions_ since the energy rise is _less steep_

- If _sufficient vibrational fine structure_ is known for each progression, the _vibrational parameters_ can be obtained

### Example: Diatomic iodine
![[Iodine UV-VIS.png]]
- Since there are _very extensive progressions_, it can be seen that _equilibrium bond length $r_e$ has changed significantly_
- The _presence of $\nu''=1$ and $\nu''=2$_ suggests that the _vibrational spacing for the ground electronic state is comparable to $kT$_

- From inspecting the _molecular orbital diagram_, it can be seen that an _antibonding electron_ is promoted from $4\pi_g^*$ to $9\sigma_u^*$, indicating _weakening of the bond_
![[I2 MO.png]]

- All of this agrees with _actual data_
	- $X$ is the _ground state_, $B$ is an _excited state_
![[I2 energy level data.png]]