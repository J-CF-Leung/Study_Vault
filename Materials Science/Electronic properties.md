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

## Fermi sphere and the density of states
- For simplification, assume a _simple cubic crystal_, where $a_x=a_y=a_z=L$
- As $E\propto k^2$, the energy levels are _non-uniformly distributed in reciprocal space_
- Equal values are _equidistant from the origin_

- At _absolute zero_, the _lowest energy states each have two electrons_
- The _sphere_ in reciprocal space with the lowest energy states is known as the _Fermi sphere_, with radius $k_F$
- At the _Fermi surface_, all the states have the _Fermi energy_:
$$E_F=\frac{\hbar^2k_F^2}{2m}$$

## The nearly free elctron model