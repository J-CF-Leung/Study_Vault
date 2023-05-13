- Models electrons in solids _while ignoring the periodic potential_ of the crystal lattice

- The _classical_ Drude model, assumes valence electrons are _free particles_, scattered by nuclei
- It producrs reasonable values for conductivity
- It predicts _incorrect values_ for charge carrier density and heat capacity
- It _fails to predict the existence of semiconductors_

## Principles
- The electrons are _not under any potential_
	- Ignoring _nuclear attraction_, as well as electron-electron _repulsion_
- There are still _boundary conditions_ taking the _periodicity_ of the crystal into account
- The [[Fundamental concepts of quantum mechanics#Multiple degrees of freedom|Pauli Exclusion Principle]] still applies

- The _number of electrons_ depends on the _material_
- There may be an _effective mass_ $m^*$ taking _lattice interactions_ into account

## States in the model
- Given a _box_ with lengths $a_x, a_y, a_z$
- There are _cyclic boundary conditions_

- This gives wave-functions:
$$\displaylines{\psi(x,y,z)\propto \sin\left(\frac{2\pi n_xx}{a_x}\right)\sin\left(\frac{2\pi n_yy}{a_y}\right)\sin\left(\frac{2\pi n_zz}{a_z}\right) \\ k_x=\pm n_x\frac{2\pi}{a_x}\hspace{1cm}k_y=\pm n_y\frac{2\pi}{a_y} \hspace{1cm} k_z=\pm n_z\frac{2\pi}{a_z}}$$
- This makes a _lattice of points_ in $k-$space
- Each point occupies _volume_ $2\pi/(a_xa_ya_z)$

- Each state in $k-$space accounts for the _spin_ of the electrons
- Then, considering a _spherical shell_ in $k-$space:
$$dN=g(k)\,dk=2\frac{4\pi k^2\,dk}{8\pi^3/V} \Longrightarrow g(k)=\frac{Vk^2}{\pi^2}$$
- Then, using the _dispersion relationship for a free particle_:
$$g(\varepsilon)=\frac{dN}{d\varepsilon}=\frac{dN}{dk}\frac{dk}{d\varepsilon}=g(k)\frac{m}{\hbar^2k}=\frac{V}{2\pi^2}\left(\frac{2m}{\hbar^2}\right)^{3/2}\varepsilon^{1/2}$$
- Hence, the _density of states in energy_ is proportional to $\sqrt{\varepsilon}$

- In _2 dimensions_, considering a _circular perimeter_, $g(\varepsilon)$ is _constant_
	- Example: graphene
- In _1 dimension_, considering a _line_ in $k-$space, $g(\epsilon)\propto 1/\sqrt{\varepsilon}$
	- Example: Carbon nanotubes

## Fermi energy
- At _absolute zero_, there is _no thermal excitation_
- Due to _Pauli exclusion principle_, there is _one electron per state_ (accounting for _spin_)

- The states are _filled from the lowest energy_
- This forms a _sphere of filled states_ in $k-$space, known as the _Fermi sphere_
	- The _radius_ of the sphere is known as the _Fermi wave-vector_ $k_F$
- The states are filled up to the _Fermi energy_ $\varepsilon_F$
	- Typical values for metals are of order $10^0\,\text{eV}$
$$\varepsilon_F=\frac{\hbar^2k_F^2}{2m}$$
- The _number of states_ $N$ is:
$$N=2\frac{4\pi k_F^3/3}{(2\pi)^2/V}$$
- Hence, the _Fermi wave-vector and energy_ are:
$$\displaylines{k_F^3=3\pi^2\frac{N}{V}=3\pi^2n \\ \varepsilon_F=\frac{\hbar^2}{2m}(3\pi^2n)^{2/3}}$$

## Fermi-Dirac distribution
- Find the _distribution of electrons_ at a finite temperature
- Consider the [[Classical Thermodynamics#Number of particles and the chemical potential|master equation]] for internal energy, and let there be a _constant volume_:
$$dS=\frac{dU}{T}-\frac{\mu \,dN}{T}$$
- Consider a _particle reservoir_ of temperature $T$
- There is an _electron of energy $\varepsilon$_ in equilibrium with the reservoir
- In the _ground state_, the entropy of the reservoir is $S_0=k_B\ln\Omega_0$
- To occupy a state of energy $\varepsilon$, the _reservoir entropy_ is then:
$$S_0+dS=S_0-\frac{\varepsilon}{T}+\frac{\mu}{T}=k_B\ln\Omega$$
- The _ratio of microstates_ is then given by:
$$\ln\frac{\Omega}{\Omega_0}=-\frac{\varepsilon-\mu}{k_BT}$$
- The probability can then be _normalised:
$$p_F(\varepsilon)=\frac{\exp[-(\varepsilon-\mu)/k_BT]}{1+\exp[-(\varepsilon-\mu)/k_BT]}$$

- This gives the _Fermi-Dirac distribution_:
$$p_F(\varepsilon)=\frac{1}{\exp[(\varepsilon-\mu)/k_BT]+1}$$
- At _absolute zero_, it is a _step function_
	- The states are _filled up to_ energy $\mu$

- At a _finite temperature_, it is _smeared out_ with order $k_BT$
![[Physics/Images/Fermi-Dirac distribution.png]]

- The _density of occupied electron states_ is given by $g(\varepsilon)p_F(\varepsilon)$
- It is the _graph of_ $g(\varepsilon)$ _smeared out_ at the step
![[Occupied electron states.png]]

- The _chemical potential_ $\mu(T)$ is the _energy at which_ a state has a _$1/2$ chance of being occupied_
	- The value of $\mu$ at _absolute zero_ is then the Fermi energy

- There is often a _weak variation_ in $\mu(T)$ at _low_ $T$
	- At low temperatures, it is _assumed_ $\mu(T)\approx \mu(T=0)=\varepsilon_F$
- The _exact_ chemical potential can be obtained by:
$$N=\int_0^\infty \frac{g(\varepsilon)}{\exp[(\varepsilon-\mu)/k_BT]+1}\,d\varepsilon$$

## Electronic energy and heat capacity
- The _total thermal energy_ of the electrons is given by:
$$U_\text{el}=\int_0^\infty \varepsilon g(\varepsilon)p_F(\varepsilon)\,d\varepsilon=\int_0^\infty \frac{\varepsilon g(\varepsilon)}{\exp[(\varepsilon-\mu)/k_BT]+1}\,d\varepsilon$$
- The _electronic heat capacity_ is then:
$$C_\text{el}=\frac{\pi^2}{2}Nk_B\frac{T}{T_F}$$
- The _Fermi temperature_ is given by:
$$T_F=\frac{E_F}{k_B}$$
- The heat capacity is _linear in temperature_, in contrast to [[Phonons|heat capacity of phonons]], which have a _cubic dependence_

### An intuitive derivation
![[Electronic heat capacity.png]]
- Raising temperature _only raises energy of thermally excited electrons_, which may be treated _classically_
$$\Delta U_\text{el}=n_\text{ex}\frac{3}{2}k_BT=\frac{3}{2}g(\varepsilon_F)(k_BT)^2$$
- To find $g(\varepsilon_F)$ in terms of $N$:
$$g(\epsilon_F)\propto \varepsilon_F^{1/2} \longrightarrow N=\int_0^{\varepsilon_F} g(\varepsilon)\,d\varepsilon\propto \varepsilon_F^{3/2}\longrightarrow g(\varepsilon_F)\propto \frac{N}{\varepsilon_F}$$
- Taking the _factors_ into account:
$$C_\text{el}\approx\frac{9}{2}Nk_B\frac{T}{T_F}$$

### Total heat capacity in metals
- Taking both _electrons and phonons_ into account:
$$C_\text{metal}=\gamma T+\beta T^3$$
- This can be _linearised_ by plotting $C/T$ as a function of $T^2$

- From finding [[#Fermi energy]], the electronic heat capacity is _proportional to_ $NTmn^{-2/3}$
- The discrepancy due to _lattice interactions_ can be accounted for by replacing $m$ with an _effective mass_ $m^*$
	- $m^*/m_e$ can be _larger than_ or _less than_ $1$
	- A _strong_ electron-electron interaction can lead to $m^*/m_e\sim 10^3$

### Average electronic energy
- At absolute zero. states are only filled _up to the Fermi level_
- The _average energy per electron_ $U$, at _absolute zero_ can then be found as:
$$\mean{U}=\int_0^{\varepsilon_F}\varepsilon\,g(\varepsilon)\,d\varepsilon\left(\int_0^{\varepsilon_F}\,g(\varepsilon)\,d\varepsilon\right)^{-1}=\int_0^{\varepsilon_F}\varepsilon^{3/2}\,d\varepsilon\left(\int_0^{\varepsilon_F}\,\varepsilon^{1/2}\,d\varepsilon\right)^{-1}=\frac{3}{5}\varepsilon_F$$

## Electron pressure and bulk modulus
- When _compressing_ a solid, the _wavelengths_ shorten, and the _occupied states rise in energy_, which also changes _Fermi energy_
- From [[Classical Thermodynamics|thermodynamics]], compute the derivative of the _total energy_ of $N$ electrons:
$$P=-\left(\pd{U}{V}\right)_S$$
- Computing the derivative, _keeping $N$ constant_:
$$P=-\pd{U}{\varepsilon_F}\pd{\varepsilon_F}{V}=-\left(\frac{3}{5}N\right)\left(-\frac{2}{3}\frac{\varepsilon_F}{V}\right)=\frac{2}{5}n\varepsilon_F$$

- The _bulk modulus_ is then defined by:
$$K_T=-V\left(\pd{P}{V}\right)_T$$

- Computing the derivative, _keeping $N$ constant_, the bulk modulus can then be found as:
$$K_T=\frac{2}{3}n\varepsilon_F$$
![[Bulk modulus actual values.png]]

- The electron gas contributes to a _short-range repulsive interaction_
- Meanwhile, there is also an unaccounted _Coulombic attraction_ between electrons and ion cores

## Motion of electrons
- Applying an _electric or magnetic_ field causes electrons to _accelerate_
- Electrons can also _collide_ with either _phonons_ or _defects_ in the solid:
$$\frac{1}{\tau}=\frac{1}{\tau_\text{phonon}}+\frac{1}{\tau_\text{defect}}$$
- Interaction _between electrons_ cannot be treated as scattering

### Accounting for scattering
- After an electron _collides_, the direction is _randomised_, and $\mean{\bm{v}}=0$
- After some time, the _probability_ that an electron has _not collided_ is $\exp(-t/\tau)$
- The _mean velocity_ is then:
$$\mean{v}=v\exp(-t/\tau)$$
- The collisions then induce an _exponential decay_ of velocity:
$$\frac{d\mean{v}}{dt}=-\frac{\mean{v}}{\tau}$$

- _Without scattering_, the force of the electron is given by the [[Electromagnetism#The Lorentz Force and the Biot-Savart Law|Lorentz force]]:
$$m^*\frac{d\bm{v}}{dt}=-e\bm{E}-e\bm{v}\wedge\bm{B}$$
- With _collisions_, there is effectively a _drag term_:
$$\displaylines{\frac{d\bm{v}}{dt}=\frac{1}{m^*}(-e\bm{E}-e\bm{v}\wedge\bm{B})-\frac{\bm{v}}{\tau} \\ m^*\left(\frac{d\bm{v}}{dt}+\frac{\bm{v}}{\tau}\right)=-e\bm{E}-e\bm{v}\wedge\bm{B}}$$

### Electron drift, mobility and conductivity
- The _drift velocity_ $\bm{v}_\text{drift}$ of electrons is defined as:
$$m^*\frac{\bm{v}_\text{drift}}{\tau}=-e\bm{E}$$
- The _electron mobility_ $\mu$ is defined as:
$$\mu=\frac{v_\text{drift}}{E}=\frac{e\tau}{m^*}$$

- The _current density_ $\bm{j}$, or _current per area_:
$$\bm{j}=n(-e)\bm{v}_\text{drift}=\frac{ne^2\tau}{m^*}\bm{E}=ne\mu\bm{E}$$
- Hence, one obtains _Ohm's Law_:
$$\displaylines{\bm{j}=\sigma\bm{E} \\ \sigma=\frac{ne^2\tau}{m^*}=ne\mu}$$
- $\sigma$ is known as the _conductivity

### Optical reflectivity
- Reflectivity is related to the _inertia of the free electrons_ when they are _driven_ by an oscillating electric field
- At _optical frequencies_, $\omega>>1/\tau$, so _scattering can be ignored_
	- Equivalent condition: $\lambda>>l$
- Applying an electric field $\bm{E}$ causes a _response_ $\bm{x}$:
$$\bm{E}=\bm{E}_0\exp(i\omega t) \hspace{1cm} \bm{x}=\bm{x}_0\exp(i\omega t)$$
- Substituting into the _equation of motion_:
$$\bm{x}_0=\frac{e\bm{E}_0}{m^*\omega^2}$$

- This causes a _dipole moment_ $\bm{p}=-e\bm{x}_0$
- This then causes a [[Electromagnetism#Polarisation and bound charge density|polariation]]:
$$\bm{P}=-ne\bm{x}_0=-\frac{ne^2}{m^*\omega^2}\bm{E}_0$$
- The _dielectric constant_ is then:
$$\epsilon(\omega)=1-\frac{ne^2}{\epsilon_0m^*\omega^2}=1-\frac{\omega_p^2}{\omega^2}$$
- $\omega_p$ is known as the _plasma frequency_:
$$\omega_p^2=\frac{ne^2}{\epsilon_0m^*}$$
- The _refractive index_ $n$ is defined as $\sqrt{\epsilon}$

- If $\omega<\omega_p$, $n$ is _imaginary_, creating an _evanescent wave_, and _reflecting all power_
- If $\omega>\omega_p$, $n$ is _real_, and the material is _transparent_
![[Optical reflectivities.png]]

### Electrical conductivity
- When an _electric field_ is applied to a material, electrons gain some _extra momentum_ oppposite to the field
- Originally, there is a _sphere of states_, which is _centered_ in $k-$space
- With the field, the sphere is _displaced_:
$$\frac{d\bm{k}}{dt}=-\frac{1}{\hbar}e\bm{E}$$
- Eventually, _scattering_ will _limit displacement_ of the sphere
![[Conductivity in k space.png]]

- _Phonon scattering_ have wave-vectors _comparable_ to electrons, but with _very small energies_ compared to $\varepsilon_F$
- This can _strongly change direction_ of the electrons, but with _slight changes to magnitude_

- Electrons can also _scatter off defects_, with large changes in _direction_, not _energy_

- In order for scattering to occur, there must be _available states_ for the electron, at a _similar energy_ to before scattering
- All states in the _bulk_ of the Fermi sphere are filled
- Hence, electrons must scatter to states _near the Fermi surface_

- Scattering causes electrons at the _front_ of the Fermi sphere to go to the _back_
- Hence, the sphere eventually reaches an _equilibrium displacement in $k-$space_
![[Fermi sphere scattering.png]]

- The total scattering rate is an _average_ of electrons in the _bulk_ which are _not scattered_, and electrons at the _front_ which are scattered strongly

### Temperature deendence of resistivity
- Consider the rate of collision:
$$\frac{1}{\tau}=\frac{1}{\tau_\text{phonon}}+\frac{1}{\tau_\text{defect}}$$
- The _defect rate_ is _temperature-independent_

- At _low temperatures_, phonon density is _low_, hence scattering is _defect-dominant_
- At _high temperatures_, the _phonon density_ is _proportional to temperature_
- The scattering is _phonon-dominant_, where $\tau_\text{phonon}<<\tau_\text{defect}$
- _Resistivity_ $\rho=1/\sigma$ is then _proportional to temperature_
![[Matthiessen.png]]
- This is known as _Matthiessens' rule_

### Electron thermal conductivity
- For _electron thermal conductivity_, it is _analagous_ to [[Phonons#Thermal conductivity in insulators|phonons]]:
$$\kappa_\text{el}=\frac{1}{3}C_\text{el}\mean{c}l$$
- As only electrons near the _Fermi level_ are excited, let $\mean{c}\approx v_F$, and $l\approx v_F\tau$
- $\kappa_\text{el}$ then becomes:
$$\kappa_\text{el}=\frac{\pi^2}{3}\frac{nk_B^2T}{m^*}\tau$$
- Generally, for _pure metals_, this is _much bigger than phonon conductivity_
	- At _high temperatures_, phonons dominate scattering and are much less conductive
- As $\tau\propto 1/T$, thermal conductivity is _roughly constant with temperature_

### Wiedemann-Franz law
- Consider the ratio $\kappa_\text{el}/(\sigma T)$:
$$\frac{\kappa}{\sigma T}=\frac{\pi^2}{3}\frac{nk_B^2T}{m^*}\tau \left(\frac{ne^2\tau}{m^*}\right)^{-1}\frac{1}{T}=\frac{\pi^2}{3}\left(\frac{k_B}{e}\right)^2$$
- This is the _Lorenz number_, and theoretically, is _constant for all metals_
- Reinforces that both conductivities have the _same underlying mechanism_
- Typically holds for _not too low temperatures_

- Typically _agrees with experimental results_

## Hall Effect
- A _magnetic field_ is applied _perpendicular_ to the current flow of a conductor
- This causes electrons to _drift_, and _build up_ across the side of the conductor
- Eventually, the _field from built-up charges_ causes a _Hall voltage_, and _balances_ the magnetic force:
![[Hall effect.png]]
- _Equilibrium_ is established when:
$$-e\bm{E}_H=-e\bm{v}\wedge\bm{B}=-e\frac{\bm{j}}{-ne}\wedge\bm{B}$$
- Hence:
$$\bm{E}_H=-\frac{1}{ne}\bm{j}\wedge\bm{B}=R_H\bm{j}\wedge\bm{B}$$
- The measured _Hall voltage_ gives $E_H$, and $\bm{j}$ and $\bm{B}$ are controlled
- $R_H$ is the _Hall coefficient_:
$$R_H=-\frac{1}{ne}$$
- It gives the _density and sign of charge carriers_
- As _electrons_ are the predicted charge carriers, it should be _negative_

- The ratio of _density of charge carriers_ $n$ to the _density of atoms_ $n_\text{atom}$:
$$\frac{n}{n_\text{atom}}=-\frac{1}{n_\text{atom}eR_H}$$
![[Hall effect values.png]]
- Therefore, the free electron model _cannot adequately describe some metals_
- This leads to the [[Nearly Free Electron Model]]
