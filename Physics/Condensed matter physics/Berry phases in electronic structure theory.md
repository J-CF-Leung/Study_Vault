- Polarisation and magnetisation:
	- Classical model - _non-overlapping, classical_ charge and current distributions
	- _Quantum_: charge and current distributions characterised by _Bloch functions_
- The [[Quantum Hall Effect]]: 2D electron gas subjected to perpendicular magnetic field, with _Fermi level in a gap_, giving rise to _quantised transverse conductivity_

- Other phenomena: _Quantisation_ in superconductivity, fractional Quantum Hall Effect

- They suggest that _quantisation and topology_ play a significant role

# Quantisation in charges and currents
- The _classical definition_ of [[Electromagnetism#Polarisation and bound charge density|Polarisation]] $\bm{P}$ is _dipole moment per unit volume_:
$$\bm{P}=\frac{\bm{p}}{V_\text{cell}}=\frac{1}{V_\text{cell}}\int_\text{cell}\bm{r}\,\rho(\bm{r})\,d^3\bm{r}$$
- The _first equality assumes_ the solid can be _decomposed_ into _polarised atoms/molecules_, separated by _charge-free regions_
- The _second equality_ is a modification, evaluating $\bm{p}$ by taking _delocalised charge density_ into account

- However, the second definition _does not lead to a unique answer_, as it depends on the _choice of unit cell_
- A precise definition uses the concept of _Berry phase_
- In fact, even if $\rho(\bm{r})$ is known, there is _insufficient information_

- A new definition of polarisation must _satisfy certain bulk properties_

## Properties of polarisation
- For a crystalline insulator _changing slowly in time_ but still remaining _spatially periodic_, there will be a _macroscopic current density_ in the interior:
$$\bm{J}=\frac{d\bm{P}}{dt}$$
- Then given a _slow spatial variation_ of the Hamiltonian $\Ham$ and the resulting $\bm{P}$:
$$\rho(\bm{r})=-\nabla\cdot\bm{P}(\bm{r})$$
- With this, _charge conservation_ is satisfied, as $\dot{\rho}=-\nabla\cdot\bm{J}$

- In a _static_ crystalline insulator, with _no free charge_, and polarisation $\bm{P}$ at a surface _normal_ to $\hat{\bm{n}}$, bound charge _accumulates_:
$$\rho_\text{surf}=\bm{P}\cdot\hat{\bm{n}}$$
## Branching values of polarization
- Through a variety of arguments, one can argue that in a _repeating lattice_, values of $\bm{P}$ form _branches_, or in other words, is _well defined modulo some "quantum"_
- Firstly, assume a _non-interacting_ Hamiltonian

### Due to the lattice
- Considering a _lattice of point charges_, there may be _multiple ways_ to write the charge positions, differing by a _lattice vector_
- Therefore, when using the above definition, $\bm{P}$ is defined _modulo a 3D lattice of values_, separated by
$$\Delta\bm{P}=\frac{e\bm{R}}{V_\text{cell}}$$
- This leads to _branching values of surface charge density_ as well, separated by:
$$\Delta \bm{P}\cdot\hat{\bm{n}}=\frac{e\,\hat{\bm{n}}\cdot\bm{R}}{V_\text{cell}}=\frac{me}{A_\text{surf}}$$
- As $\Delta\bm{P}$ is a _constant_, this _does not affect_ $\rho$ or $\bm{J}$
- As for branching values of _surface charge density_, one can interpret this as there being a _surface band_ within the _bulk gap_ that can either be _fully filled_ or _empty_ depending on the Fermi level
	- Both the _bulk and surface_ must be _insulating_ or charge can flow as the _surface Hamiltonian_ changes
	- A _local_ change in the Hamiltonian only induces a _local_ change insurface charge (the "nearsightedness" principle)
	- Hence the Fermi level must have _zero density of states_ both in the bulk and the surface
- The branching values can be expressed as:
$$\sigma_\text{surf}:=\bm{P}\cdot\hat{\bm{n}}$$
- This means $\bm{P}\cdot\hat{\bm{n}}$ is _multi-valued_, and $\sigma$ is _one of the values_

### Temporal variation and charge pumping
- Consider a variation of the Hamiltonian _in time_ based on some parameter $\lambda(t)$
- Let the evolution be characterised by a _loop in parameter space_, or $\lambda(t_i)=\lambda(t_f)$
- Example: a _1D electronic Hamiltonian_, where $\lambda$ goes from $0$ to $2\pi$
$$\Ham=\frac{p^2}{2m}-V_0\cos\left(\frac{2\pi}{a}x-\lambda\right)$$
- For a _large $V_0$_, the charge is _semiclassically localised_, hence if the change in $\lambda$ is _gradual_, then a _charge_ of $-e$ can be _pumped_ by $+a\hat{x}$ in one cycle

- Hence, for a _given Hamiltonian_, $\bm{P}$ is _not uniquely defined_
- For an _adiabatic change_, $V_0$ can be _any size_, and charge transport can still be achieved

- Let the change instead be an _open path_, and using the definition of $\bm{J}$:
	$$\Delta\bm{P}_{i\to f}\equiv\int_i^f\bm{J}(t)\,dt=\int_i^f\frac{d\bm{P}}{d\lambda}\frac{d\lambda}{dt}\,dt=\int_i^f\frac{d\bm{P}}{d\lambda}\,d\lambda$$
- The derivative is _well-defined_ as the difference between branched values is _constant_
	- $\bm{R}$ is constant as long as the change is _adiabatic_
- Hence, time is a _passive variable_, and for a _closed loop_:
$$\Delta\bm{P}_\text{cyc}=\oint\frac{d\bm{P}}{d\lambda}\,d\lambda=\frac{e\bm{R}}{V_\text{cell}}$$
- To express the fact that the values are in _branches_, adopt the notation:
$$\Delta\bm{P}_{i\to f}:=\bm{P}_f-\bm{P}_i$$
- For a _definite path_ $\Delta\bm{P}$ has a _defnite value_, given by one of the values on the right-hand side, which differ by $e\bm{R}/V_\text{cell}$
- Following _two different paths_ connecting the same Hamiltonians, $\Delta\bm{P}$ is _the same modulo the quantum_

### Slow spatial variation in a supercell
- Let there be an $N\times1\times1$ _supercell_ where the _local Hamiltonian_ varies slowly from $\lambda=0$ to $\lambda=1$, where $\Ham(\lambda=0)=\Ham(\lambda=1)$
- Given the spatial variation is _adiabatic_, each primitive cell is _neutral_
- Hence, the _total charge_ is:
$$Q=bc\int_0^{Na}-\nabla\cdot\bm{P}\,dx=-bc\int_0^{Na}\frac{dP_x(\lambda(x))}{dx}\,dx=-\frac{V_\text{cell}}{a}\int_0^1\frac{dP_x}{d\lambda}\,d\lambda$$
- Here, due to the _adiabatic change_, $x$ is once again _passive_
- Treating the supercell as another unit cell, and applying [[Nearly Free Electron Model#Bloch's Theorem|Bloch's Theorem]], $Q=-Ne$
- Hence:
$$\Delta P_\text{x,cyc}=\oint \frac{dP_x}{d\lambda}\,d\lambda=\frac{Nea}{V_\text{cell}}$$
- This gives the same result as above

### Robustness against interactions
- The above arguments apply for both _non-interacting and interacting Hamiltonians_
	- Unless system are _strongly correlated_ (typically having _multiple degenerate ground states_)
- Hence, the branching nature of polarisation and the difference of $e\bm{R}/V_\text{cell}$ are said to be _robust against interactions_

## Orbital magnetisation and surface currents
- The [[Electromagnetism#Magnetostatics in homogeneous magnetic materials|magnetisation]] of a material has two contributions:
	- _Spin_ magnetisation from _excess electron spin_ in any direction
	- _Orbital_ magnetisation, typically induced by _spin-orbit coupling_

- Consider an _insulator_ with some _orbital magnetisation_ $\bm{M}_\text{orb}$
- Orbital magnetisation manifests in the form of a _surface current_:
$$\bm{K}_\text{surf}=\bm{M}_\text{orb}\times \hat{\bm{n}}$$
- $\bm{K}_\text{surf}$ is a _dissipationless current_ as it continuously generated a $\bm{B}$ field
	- _Microscopically_, dissipationless currents can manifest simply in the ground electronic states of multi-electron atoms
- Unlike polarisation, $\bm{M}_\text{orb}$ is _unique_ for a given Hamiltonian
	- Any _local change_ of the surface modifying $\bm{K}_\text{surf}$ will result in a _charge buildup_ (as the surface is insulating), which is impossible in a _stationary state_
- Hence, for an _insulator_, $\bm{M}_\text{orb}$ is a _bulk property_

- Like polarisation, this uniqueness is _robust against interactions and disorder_

## Edge band structure
- Let there be a _two-dimensional insulating crystal_
