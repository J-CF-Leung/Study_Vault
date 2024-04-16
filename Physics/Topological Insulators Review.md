- Introduction: former classification: _symmetry breaking_ (Landau theory)
	- (Bernevig & Hughes, 2013, Chapter 1)
- The order parameter is _local_

- _Topological_ phases do _not_ have a local order parameter
	- Excitations with _fractional statistics_ (Anyons?) (fractional quantum hall states)
		- Braiding and quantum computing
- Topological phases are _insensitive to smooth changes in material parameters_
	- (Kane, 2013)

- Topological insulators: _gapless_ edge states
	- _Protected_ by time reversal symmetry
	- Said to be _topologically protected_
	- Integer quantum hall effect

- Description can be formulated using _single-particle_ electron dynamics
- The "turning on" of _interaction terms_ can be interpreted as a _smooth change_, hence _does not affect topological state_

- _Fractional_ quantum Hall effect: quasiparticles of _fractional_ charge
	- Anyonic statistics

# Background

## Berry phase and topology
- [[Quantum Dynamics#Berry's phase|Berry phase]]:
	- Only significant in $n>2$ dimensions in parameter space
$$\gamma_{n}(t)=i \int_{0}^{t}\Braket{ n(\boldsymbol{R}(t'))| \frac{d}{dt'} |n(\boldsymbol{R}(t'))  }  \, dt' $$
- _Berry connnection_:
$$\boldsymbol{A}_{n}(\boldsymbol{R})=i  \braket{ n(\boldsymbol{R})|\nabla_{\boldsymbol{R}} |n(\boldsymbol{R})  } \hspace{1cm}\gamma_{n}=\int _{\mathcal{C}} d\boldsymbol{R}\cdot \boldsymbol{A}_{n}(\boldsymbol{R})  $$
- _Berry curvature_:
	- Gauge-_independent_
$$\boldsymbol{F}_{n,\mu \nu}=\frac{\partial}{\partial R^{\mu}}A_{n,\nu}-\frac{\partial}{\partial R^{\nu}}A_{n,\mu}$$

- If the closed loop encloses a _toplogically nontrivial manifold_, it can be _gauge-invariant up to discrete jumps_
	- e.g. $2n\pi$, where $n \in \mathbb{N}$, the _phase factor_ for the wave-function is still unchanged
	- The closed path is known as a _Wilson loop_

- A _connection_ allows one to _compare_ vector spaces associated with different points
- The vector spaces at different points form a _vector bundle_
	- e.g. the _tangent bundle_ on a Riemannian manifold

- Topological idea: holonomy
	- The _holonomy_ of a connection is how _curvature_ affects _parallel transport_

- The Berry connection comes from a _complex vector bundle_ in _parameter space_

- Abelian and non-Abelian connections??

- Berry phase can be defined using paths with a _finite number of points_

- Example: _spin in a magnetic field_
	- Berry connection
	- Singularity at the _pole_
	- For _any gauge choice_, there is a singularity
	- _Dirac string_ at the singularity

## Landau levels
(Moessner & Moore, 2021)
- Consider a charged particle moving in a _magnetic field_, which is _perpendicular_ to its plane of motion
- It oscillates with _cyclotron frequency_ $\omega_{c}=qB/m$
- The _radius_ of the circle is given by $R_{L}=|\dot{\boldsymbol{r}}(0)|/\omega_{c}$

- Energy levels:
$$E_{n}=\hbar\omega_{c}\left( n+ \frac{1}{2} \right)$$
- The _degeneracy_ of an energy level is _proportional_ to the _area_ $A$ of the system
	- Density of states is proportional to $A$
- A Landau level _groups_ states over energy interval $\hbar\omega_{c}$
- The density of states is $1/(2\pi l^{2})$
- $l$ is the _length scale_ of the problem, where $l^{2}=\hbar/qB$

- Each electron encloses a _flux quantum_ $h/e$ from the applied field

- Derivation
- A _non-Abelian algebra_ as the _momentum operators no longer commute_
## Bloch's Theorem
- Lattice transformations form an _Abelian group_
	- Hence, states can be labelled by _crystal momentum_ $\boldsymbol{k}$
- $\boldsymbol{k}$ can also be used to label _energy eigenstates_
	- No longer applies with a magnetic field (non-Abelian algebra)

- Bloch's theorem:
$$\psi_{k}(x+a)=\exp(ika)\psi(x)$$

- Due to the _periodicity_ of the Brillouin zone, there is a _non-trivial closed loop_
- In one dimension:
$$\gamma= \oint_{-\pi/a}^{\pi/a} \braket{ u_{k}|i\partial_{k} |u_{k}  } \,dk$$
- For _plane waves_, $i\partial_{k}$ corresponds to $x$
	- Related to _electric polarisation_
	- Need to introduce _Wannier functions_

## Tight-binding model

## Dirac band structure

## Symmetry breaking (qualitative)

## Topology
- _Cohomology_: what quantities (integrals over path/surface) are _invariant to smooth changes of path_, but are _sensitive to topology_
- _Homotopy_: an _equivalence relation_, which states that curves/surfaces are _homotopic_ if they can be _smoothly distorted_ into each other

## Chern Theorem
$$\oint \Omega_{\mu \nu}\cdot ds_{\mu}\times ds_{\nu}=2\pi C$$
- $C$ is the _Chern number_
- If it is _zero_, the space has _trivial topology_
	- One can have a _smooth gauge everywhere_
- If it is _non-zero_, there is a _topological obstruction_ that stops there from being a _smooth gauge_
# Why is topology important?
- (Ando, 2013)

- The _Hilbert space_ may have a _non-trivial topology_

- In crystals, $\boldsymbol{k}$ is a _map_ from $\boldsymbol{k}-$space to the Hilbert space (where the wave-functions live on a _manifold_)
- Hence, topology is _relevant to existing electronic states_

- _Topological invariants_ are _unaffected_ by _smooth changes_ in parameters of the system
	- Similar to the _genus_ of a manifold

- For a nontrivial topology, a _gapless interface state_ necessarily shows up when the insulator is _physically terminated_, facing an _ordinary insulator_ (e.g. vacuum)

- The _periodicity_ of a $d-$dimensional Brillouin zone makes it equivalent to a $d-$dimensional _torus_
	- (Kane, 2013)

- Given two _topologically distinct phases_ in _contact_ (some _spatial interface_)
	- Topologically distinct _Hamiltonians_
- Let the crystal _interpolate_ between the two phases
- As they are _topologically distinct_, the _energy gap_ must _go to zero_ at some point _within the interface_
	- If it _remains non-zero_, the phases are then _equivalent_

- _Bulk-boundary_ correspondence: relates _bulk_ topological invariants to the _boundary_ TIs
	- Example: $\ce{ Bi_{2}Se_{3} }$ is a _bulk insulator_, with _massless electronic excitations_ on the surface (linearly dispersing cone) (Zhang et al., 2009)

- Chern number: Berry curvature over a _closed surface_

- The _source_ of topological behaviour is _spin-orbit coupling_

# Concepts in topological band theory
- Wilson loop

# Electric polarisation

# Quantum Hall Effect
- First observed topological phenomenon

- (Ando, 2013)
- TKNN invariant/Chern number $\nu_{n}$: related to _Berry flux enclosed_ after _circling BZ boundary_:
$$\displaylines{\nu=\sum_{n}\nu_{n}=\sum_{n} -\frac{1}{2\pi}\gamma_{n}[\partial \text{BZ}] \\ \gamma_{n}[\partial \text{BZ}]=\oint \boldsymbol{A}_{n}\cdot d\boldsymbol{k}=2\pi m}$$
- Analagous to the _Gauss-Bonnet Theorem_

- The _Hall conductivity_:
$$\sigma_{xy}=\frac{I_{x}}{V_{y}}=\nu\frac{e^{2}}{h}$$
- A _non-zero TKNN variant_ means the system has a _non-trivial topology_
	- Connecting a _topological quantity_ to a _physical observable_

- Integer quantum Hall effect: skipping orbits

- This system _breaks time reversal symmetry_

- Use _perturbation theory_ to obtain new eigenstates
	- Treat the _electric field_ as the perturbation, $V=-eEy$
- Magnetic field in the $z-$direction
- Calculate $\sigma$ using _Heisenberg's equation of motion_ to determine $\left<j\right>_{x}$

- Bulk band structure: _Landau levels_
	- Unit cells are defined as areas enclosing a _flux quantum_, such that Bloch's theorem applies and $\boldsymbol{k}$ is a good quantum number
- Explanation of _edge states_: _boundary_ between two topologically distinct states
	- Cited in Kane and Bernevig

- Over entire band structure: Chern number 0?
# Z2 topological invariant
- Time-reversal symmetry often given by _spin-orbit interaction_

- Time-reversal symmetry: bands come in _Kramers pairs_ (witj $+\boldsymbol{k}$ and $-\boldsymbol{k}$ being at the _same energy_)
- They are _degenerate_ at the _time-reversal invariant momentum_ (TRIM)
	- Here, the $+\boldsymbol{k}$ and $-\boldsymbol{k}$ states are _equivalent_ due to periodicity of the BZ

- Similarly for _inversion symmetry_

- There is a $\mathbb{Z}^{2}$ _topological invariant_

## Time reversal symmetry
- _Electric_ fields: even under time-reversal (odd under inversion)
- _Magnetic_ fields: odd under time-reversal (even under inversion)

- In QM, particles in a _time reversal symmetric system_ have _degenerate eigenstates_ (Kramers pairs)
	- Each one-electron state is _different from_, but _degenerate with_, the time-reversed version
	- Time reversal is represented by an _anti-unitary operation_

- The _spin-orbit coupling_ interaction is _roughly analagous_ to a magnetic field
- However, as both $\boldsymbol{L}$ and $\boldsymbol{S}$ are _odd_ under time reversal, the interaction is _even_
- It can also _very on the scale of a unit cell_

- The _charge current_ is cancelled out, but there is a _spin current_

- Kramers pairs _cannot mix_ (why?)
- For an _even number_ of Kramers pairs, _time-reversal-invariant backscattering_ will go to _zero_ pairs
- First TI!

## Inversion symmetry

# 3D topological insulators
- Experimental techniques for surface state: ARPES
	- First: $\ce{ Bi }_{1-x}\ce{ Sb }_{x}$
	- _Spin sensitivity_: distribution of spin orientations on Fermi surface
- Surface states _cannot be reduced_ into a _quantum spin Hall state_
	- Spin and linear momentum are _locked_ (1 to 1)
	- 2D Fermi surface carries a _non-trivial_ Berry's phase $(\pi)$
	- _Odd number_ of states carrying non-trivial Berry's phase

- A layered QSH insulator is a _weak 3D TI_
	- Even number of Dirac cones, net Berry phase of $0$ or $2\pi$
	- Not robust against disorder

- 4 $\mathbb{Z}_{2}$ invariants $(\nu_{0};\nu_{1}\nu_{2}\nu_{3})$
	- 4 Dirac points at the TRIM $\Gamma_{1},\Gamma_{2},\Gamma_{3},\Gamma_{4}$
	- Depending on how they are _connected_ by surface states (even or odd), it may be a _weak_ or _strong_ TI
# Types of topological materials

## 2D Materials

## 3D Materials

## Topological semimetals

- Weyl semimetal:
	- Weyl fermions are _massless_ and _chiral_
	- Two-component Dirac equation
- When TRS is broken in an _inversion-symmetric_ solid
- Weyl points come in _pairs_
	- A _source_ and _sink_ of Berry curvature
	- Nielsen-Ninomiya theorem
- They give rise to an _arc of zero-energy excitation_ (Fermi arc) in the projected surface BZ
	- Another example of _bulk-boundary correspondence_

- Dirac point: two Weyl points

- Existence of degeneracies: only in 3 dimensions, with either $\mathcal{P}$ or $\mathcal{T}$ broken
- Then describes by _generic Hamiltonian_:
$$H(\boldsymbol{k})=f_{0}(\boldsymbol{k})\mathbb{I}+f_{1}(\boldsymbol{k})\sigma_{1}+f_{2}(\boldsymbol{k})\sigma_{2}+f_{3}(\boldsymbol{k})\sigma_{3}$$
- Around the degeneracy, _Taylor expand_

# New developments in theory
- Multi-band braiding? (Euler class instead of Berry flux)
	- Example: ZrTe

## Majorana zero modes



Order: 
- Introduction
- TIs --> Weyl -- > Multi-band
- (Only what is needed for final part)


Scientific content (explanation) + how "well"? (how it was done, what was reviwed, etc.) + report + viva

20-40 papers

Important papers: bring up to date (last year-ish)