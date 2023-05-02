- The _electrical conductivity_ of a material is defined by [[Electromagnetism#Current resistivity and conductivity|Ohm's Law]]:
$$\bm{J}=\sigma\bm{E}$$
- The _current density_ in an _isotropic material_ can be expressed in terms of:
$$\bm{J}=ne\bm{v}$$

- The _charge carriers_ of a material can be:
	- _Electrons_, negatively charged particles in _metals, semiconductors and insulators_
	- _Ions_ in ceramics, positive or negatively charged particles in [[Solid ionic conductors|ceramics]]
	- _Holes_, positively charged carriers indicating the _absence of an electron_ in _semiconductors_

- Conductivity values at _room temperature_:
- The conductivity of an _insulator_ such as polymers or some ceramics is $\sigma\sim 10^{-16}\to10^{-15}$
- The conductivity of a _semiconductor_ is around $10^{-4}\to10^0$
- The conductivity of a _metal_ is around $10^7$

# Classical theory
- Models the solid as a _fixed array of nuclei_, with a sea of _free electrons moving as particles in straight lines_

## The Drude model and drift velocity
- The _free electrons_ will move in _one direction_, until they _collide with nuclei_
	- They are modelled as _not colliding with each other_
	- Similar to particles in an _ideal gas_

- If there is _no electric field_, then the _average velocity_ vanishes:
$$\mean{\bm{v}_0}=0$$
- There is some _mean free path_ $l$ travelled by each electron _between collisions_
- There is an _average collision time_ $\tau$:
$$l=v_\text{rms}\tau$$
- $v_\text{rms}$ is the _root-mean-square speed_: $v_\text{rms}^2=\mean{v^2}$

- Let there be some _electric field_ $\bm{E}$
- In the time _between collisions_:
$$\bm{v}=\bm{v}_0-\frac{e\bm{E}}{m}\tau$$
- Taking the _time-average_:
$$\mean{\bm{v}}=-\frac{e\bm{E}}{m}\tau$$
- This gives the electrons some _drift velocity_

- This gives the current density:
$$\sigma=\frac{ne^2\tau}{m}$$
- The _mobility_ $\mu$ of charge carriers is defined as:
$$\mu=\frac{|\bm{v}|}{|\bm{E}|}=\frac{e\tau}{m}=\frac{\sigma}{ne}$$
- The _lower the mass_, and _higher the collision time_, the higher the mobility

- By comparing the electrons in a _metal with an ideal gas:
$$\frac{1}{2}mv_\text{rms}^2=\frac{3}{2}kT$$
- A _typical mean-free path_ is $l\sim 10^{-9}\,\text{m}$
- A _typical charge carrier density_ is $10^{28}\to10^{29}\,\text{m}^{-3}$
- At _room temperature_, this gives $\sigma\sim 10^{6}\to10^7\,\Omega^{-1}\text{m}^{-1}$

## The Hall Effect
- Let there be an _electric field_ $\bm{E}=E_x\hat{\bm{x}}$, causing a current density $\bm{J}=J_x\hat{\bm{x}}$
- Then, apply a _magnetic field_ $\bm{B}=B_z\hat{\bm{z}}$, causing a _Lorentz force_:
$$\bm{F}_B=ev_xB_z\hat{\bm{y}}$$
- This causes electrons to _drift in the $y-$direction_, and _cause a potential difference in that direction_, known as the _Hall voltage_
- This then causes an _electric field opposing the Lorentz force_

- In _equilibrium_:
$$-E_y=v_xB_z$$
- Expressing $v_x$ in terms of $J_x$:
$$\displaylines{E_y=R_HJ_xB_z\equiv-\frac{J_xB_z}{ne} \\ R_H=-\frac{1}{ne}}$$
- $R_H$ is known as the _Hall coefficient_
- The _sign_ of the Hall coefficient indicates whether _electrons_ or _holes_ are the charge carriers
	- Electron density: $n$
	- Hole density: $p$
- The _magnitude_ of the Hall coefficient can also indicate the _charge carrier density_

## Limitations of the classical theory
- The Drude model assumes _all materials act like metals_
- It also predicts that the _energy spectrum of electrons is continuous_

- Comparing values of $n$ and $p$ from _crystal structures_, Hall coefficients agree for _most metals_, but _not semiconductors_
- At _high magnetic fields_, the Hall coefficient can also _change magnitude and sign_
	- Example: aluminium

# Quantum mechanical models
- Electrons are modelled as _waves_
- From [[The failure of classical mechanics#Quantisation and de Broglie's hypothesis|de Broglie's hypothesis]]:
$$\displaylines{|\bm{p}|=\frac{h}{\lambda} \\ \bm{p}=\hbar\bm{k}}$$
- $\bm{k}$ is the _wave-vector_, pointing in the _wave propagation direction_
$$|\bm{k}|=\frac{2\pi}{\lambda}$$
- The wave-vectors in a crystal are described in _reciprocal space_

- Electrons are described using the [[Fundamental concepts of quantum mechanics#The wave function|wave function]] $\psi(\bm{r})$

## The free electron model
- This _ignores the potential energy in a crystal_
- Hence, the Hamiltonian is simply:
$$\hat{\Ham}=-\frac{\hbar^2}{2m}\nabla^2$$
- The time-independent equation is then:
$$-\frac{\hbar^2}{2m}\nabla^2\psi=E\psi$$
- As the electron is in a _lattice_, impose _periodic boundary conditions_:
$$\psi(\bm{r})=\psi(\bm{r}+\bm{a})$$

- A 1D model is suitable for materials where _electrons are confined to one dimension_, such as in _carbon nanotubes_
- A 3D model is suitable for most crystals

- Let the _lattice parameters_ be $(a_x,a_y,a_z)$
- The _solution_ for $\psi$ is:
$$\psi=\exp(i\bm{k}\cdot\bm{r})=\exp(ik_xx)\exp(ik_yy)\exp(ik_zz)$$
- The _energy_ is then:
$$E=\frac{\hbar^2k^2}{2m}=\frac{\hbar^2}{2m}(k_x^2+k_y^2+k_z^2)$$
![[E(k) free electron.png]]

- From the _boundary conditions_, the _wave-vector_ is _quantised_:
$$\bm{k}=(k_x,k_y,k_z)=2\pi\left(\frac{l}{a_x},\frac{m}{a_y},\frac{n}{a_z}\right)$$
- Here, $l,m,n$ are _integers_
- This also gives _quantised energies_, quadratic w.r.t. each index
	- For each energy, there are _two electrons_ occupying it, with _opposite spins_
- In _recriprocal space_, there is a set of _points_ with _permitted energies_
	- It is _not a lattice_, as $E\propto k^2$

- The wave functions can be pictured as _standing waves_

- At _absolute zero_, all of the _lowest-energy states_ are filled
- For metals, the _highest energy state_ is the _Fermi level_ $E_F$

### Fermi sphere and the density of states
- For simplification, assume a _simple cubic crystal_, where $a_x=a_y=a_z=L$
- As $E\propto k^2$, the energy levels are _non-uniformly distributed in reciprocal space_
- Equal values are _equidistant from the origin_

- At _absolute zero_, the _lowest energy states each have two electrons_
- The _sphere_ in reciprocal space with the lowest energy states is known as the _Fermi sphere_, with radius $k_F$
- At the _Fermi surface_, all the states have the _Fermi energy_:
$$E_F=\frac{\hbar^2k_F^2}{2m}$$
- Typically, the radius of the Fermi sphere is _much larger than the spacing between states_

- For a given arbitrary energy $E$, the _number of available states_ $N(E)$ for electrons to occupy is:
	$$N(E)=2\left(\frac{4}{3}\pi k^3\right)\left(\frac{2\pi}{L}\right)^{-3}=\frac{L^3}{3\pi^2}k^3=\frac{V}{3\pi^2}k^3$$
	- Factor of 2: accounting for _spin_
- Writing as a function of $E$:
$$N(E)=\frac{V}{3\pi^2}\left(\frac{2mE}{\hbar^2}\right)^{3/2}$$
- Then, one can find the _density of states_ $D(E)$ that gives the _density of electron states per unit energy_:
$$D(E)\equiv\frac{dN}{dE}=\frac{V}{2\pi^2}\left(\frac{2m}{\hbar}\right)^{3/2}E^{1/2}\propto \sqrt{E}$$
- This is assuming that the states are _dense_, making $E$ and $D$ _continuous functions_

- Similarly, in _one dimension_, consider the _free electron line_, with length $2k$:
$$\displaylines{N_\text{1D}(E)=2(2k)\left(\frac{2\pi}{L}\right)^{-1}=\frac{2L}{\pi}\left(\frac{2mE}{\hbar^2}\right)^{1/2} \\ D_\text{1D}(E)=\frac{L}{\pi}\left(\frac{2m}{\hbar^2}\right)^{1/2}E^{-1/2}\propto\frac{1}{\sqrt{E}}}$$
- This is useful for modelling _carbon nanotubes_

- Similarly, in _two dimensions_, considering the _free electron circle_, with radius $k$:
$$\displaylines{N_\text{2D}(E)=2(\pi k^2)\left(\frac{2\pi}{L}\right)^{-2}=\frac{L^2}{2\pi}\left(\frac{2mE}{\hbar^2}\right) \\ D_\text{2D}(E)=\frac{L^2}{2\pi}\left(\frac{2m}{\hbar^2}\right)=\frac{mL^2}{\pi\hbar^2}}$$
- This is useful for modelling _graphene sheets_
- Notably, the density of states is _independent of $E$_

### Occupation of energy levels at absolute zero
- For _metals_, states are occupied _up to the Fermi surface_
- For _insulators and semiconductors_, there are _no electronic states at the Fermi surface_
	- Reason: [[#The nearly free elctron model]]
	- Instead, at the Fermi energy, the _probability of occupation_ is $1/2$

- Define $n$ as the _number of valence electrons per unit volume_
- Rearranging the expression for $N_\text{3D}(E)$:
$$k_F=(3\pi^2 n)^{1/3}$$
- Example: In _copper_, the Fermi sphere volume is $\sim10^{22}$ times _bigger than the volume per state_

### Occupation of energy levels at a finite temperature
- A small fraction of valence electrons are _promoted_ from just below the Fermi surface, to _above_ the Fermi surface
- The _probability_ of an electron energy level $E$ being occupied is given by the [[Statistical thermodynamics|Fermi-Dirac distribution]]:
$$f(E)=\frac{1}{\exp\left(\frac{E-E_F}{k_BT}\right)+1}$$
- If $f(E)=1$, the state is _fully occupied_
- If $f(E)=0$, the state is _fully vacant_
- If $E=E_F$, $f(E)=1/2$
![[Fermi-Dirac distribution.png]]
- At finite temperatures, the distribution is _smeared_ over an energy interval of order $k_BT$

- One can then define the _occupied density of states_ $Z(E)$ as:
$$Z(E)=D(E)f(E)$$
- At absolute zero, there is a _sudden drop_ at $E=E_F$

### Electrical conductivity
- In contrast to the [[#The Drude model and drift velocity|Drude model]], where _all electrons_ contribute to conductivity, in the _free electron model_, only electrons _at the Fermi energy_ are viable _charge carriers_

- Use a _semi-classical model_, where _classical laws_ are governing the "motion" of waves
- A semi-classical electron with wave-vector $k$ has _velocity_:
$$\bm{v}=\frac{\hbar \bm{k}}{m}$$
- As $\mean{\bm{k}}=0$, this means there is _zero average velocity_

- When an _electric field_ is applied:
$$\bm{F}=\hbar\frac{d\bm{k}}{dt}=-e\bm{E}$$
- Taking _collisions_ into account:
$$\Delta\bm{k}=-\frac{e\tau\bm{E}}{\hbar}$$
- This gives a _shift in the sphere of occupied wave-vectors_, hence a _shift in average velocity_:
$$\Delta\bm{v}=\frac{\hbar\Delta\bm{k}}{m}=-\frac{e\tau\bm{E}}{m}$$
- Hence, there is a _net velocity_, depending on both $\bm{E}$ as well as the _magnitude of_ $k_F$
- The _conductivity_ can then be found:
$$\sigma=\frac{n^*e^2\tau}{m}$$
- $n^*$ is the _effective valence electron density_, as only the electrons _near the Fermi surface_ will contribute to conductivity
- The total number of _promoted_ valence electrons is $n^*V$, with $n^*<<n$

- The _net effect_ of an applied electric field is to make electrons _near the Fermi energy_ gain an _increment_ of energy $\Delta E$, promoting them into higher energies

- Hence, conductivity depends on the _occupied_ [[#Fermi sphere and the density of states|density of states]] _at the Fermi level_

### Limitations
- Although _better than the Drude model_, it still predicts that _all materials are metals_
- The _potential of positive ions_ is still ignored

## The nearly free electron model
- The new Hamiltonian is:
$$\hat{\Ham}=-\frac{\hbar^2}{2m}\nabla^2+V(\bm{r})$$
- In _one dimension_, $V(x)$ is simply a _simple periodic_ potential modelling ions with spacing $a$
- When it is _near ion cores_, it goes to _negative infinity_ as $1/x$
![[Nearly free electron model potential.png]]

- The electrons can be said to _scatter_ from the potential well
- This causes _band gaps_, at $k=n\pi/a$
- These wave vectors are at the _Brillouin zone boundaries_
- The _magnitude_ of the gaps depends on the _strength_ of the potential

- Hence, there are _permitted ranges_ of energy known as _bands_
	- Within the bands, the energies are still _quantised_

- At the _boundaries_:
$$\pd{E}{k}=0$$
- When _away_ from the boundaries, the bands are _similar in shape_ to those in the free electron model (i.e. _parabolic_)

- In _insulators_, the lower band is _full_, and fields _cannot easily promote_ the electrons to cause any _change_ in $k$ and $v$

- In _metals_, bands are _partally filled_, so fields can cause a _change_ in $k$ and $v$