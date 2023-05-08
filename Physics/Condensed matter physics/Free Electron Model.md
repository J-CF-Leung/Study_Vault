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

- DERIVATION

- This gives the _Fermi-Dirac distribution_:
$$p_F(\varepsilon)=\frac{1}{\exp[(\varepsilon-\mu)/k_BT]+1}$$
- At _absolute zero_, it is a _step function_
	- The states are _filled up to_ energy $\mu$

- At a _finite temperature_, it is _smeared out_ with order $k_BT$

- The _density of occupied electron states_ is given by $g(\varepsilon)p_F(\varepsilon)$
- It is the _graph of_ $g(\varepsilon)$ _smeared out_ at the step

- The _chemical potential_ $\mu(T)$ is the _energy at which_ a state has a _$1/2$ chance of being occupied_
	- The value of $\mu$ at _absolute zero_ is then the Fermi energy

- There is often a _weak variation_ in $\mu(T)$ at _low_ $T$
	- At low temperatures, it is _assumed_ $\mu(T)\approx \mu(T=0)$

## Electronic energy and heat capacity
- The _total thermal energy_ of the electrons is given by:
$$U_\text{el}=\int_0^\infty \varepsilon g(\varepsilon)p_F(\varepsilon)\,d\varepsilon=\int_0^\infty \frac{\varepsilon g(\varepsilon)}{\exp[(\varepsilon-\mu)/k_BT]+1}\,d\varepsilon$$
- The _electronic heat capacity_ is then:
$$C_\text{el}=\frac{\pi^2}{2}Nk_B\frac{T}{T_F}$$
- The _Fermi temperature_ is given by:
$$T_F=\frac{E_F}{k_B}$$
- The heat capacity is _linear in temperature_, in contrast to [[Phonons|heat capacity of phonons]], which have a _cubic dependence_

### An intuitive derivation
- Raising temperature _only raises energy of thermally excited electrons_, which may be treated _classically_
$$\Delta U_\text{el}=n_\text{ex}\frac{3}{2}k_BT=\frac{3}{2}g(\varepsilon_F)(k_BT)^2$$
- To find $g(\varepsilon_F)$ in terms of $N$:
$$g(\epsilon_F)\propto \varepsilon_F^{1/2} \longrightarrow N=\int_0^{\varepsilon_F} g(\varepsilon)\,d\varepsilon\propto \varepsilon_F^{3/2}\longrightarrow g(\varepsilon_F)\propto \frac{N}{\varepsilon_F}$$
- Taking the _factors_ into account:
$$C_\text{el}\approx\frac{9}{2}Nk_B\frac{T}{T_F}$$

### Heat capacity in metals
- Taking both _electrons and phonons_ into account:
$$C_\text{metal}=\gamma T+\beta T^3$$
- This can be _linearised_ by plotting $C/T$ as a function of $T^2$

- The electronic heat capacity is _proportional to_ $NTmn^{-2/3}$
- The discrepancy due to _lattice interactions_ can be accounted for by replacing $m$ with an _effective mass_ $m^*$
	- $m^*/m_e$ can be _larger than_ or _less than_ $1$
	- A _strong_ electron-electron interaction can lead to $m^*/m_e\sim 10^3$
