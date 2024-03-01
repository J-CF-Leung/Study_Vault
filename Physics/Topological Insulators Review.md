- [[Quantum Dynamics#Berry's phase|Berry phase]]:
$$\gamma_{n}(t)=i \int_{0}^{t}\Braket{ n(\boldsymbol{R}(t'))| \frac{d}{dt'} |n(\boldsymbol{R}(t'))  }  \, dt' $$
- _Berry connnection_:
$$\boldsymbol{A}_{n}(\boldsymbol{R})=i  \braket{ n(\boldsymbol{R})|\nabla_{\boldsymbol{R}} |n(\boldsymbol{R})  } \hspace{1cm}\gamma_{n}=\int _{\mathcal{C}} d\boldsymbol{R}\cdot \boldsymbol{A}_{n}(\boldsymbol{R})  $$
- _Berry curvature_:
$$\boldsymbol{F}_{n,\mu \nu}=\frac{\partial}{\partial R^{\mu}}A_{n,\nu}-\frac{\partial}{\partial R^{\nu}}A_{n,\mu}$$

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

- Chern number: Berry curvature over a _closed surface_

# Concepts in topological band theory
- Wilson loop

# Electric polarisation

# Quantum Hall Effect
- (Ando, 2013)
- TKNN invariant $\nu_{n}$: related to _Berry flux enclosed_ after _circling BZ boundary_:
$$\displaylines{\nu=\sum_{n}\nu_{n}=\sum_{n} -\frac{1}{2\pi}\gamma_{n}[\partial \text{BZ}] \\ \gamma_{n}[\partial \text{BZ}]=\oint \boldsymbol{A}_{n}\cdot d\boldsymbol{k}=2\pi m}$$
- Analagous to the _Gauss-Bonnet Theorem_

- The _Hall conductivity_:
$$\sigma_{xy}=\nu\frac{e^{2}}{h}$$
- A _non-zero TKNN variant_ means the system has a _non-trivial topology_

- Integer quantum Hall effect: skipping orbits

- This system _breaks time reversal symmetry_

- Use _perturbation theory_ to obtain new eigenstates
	- Treat the _electric field_ as the perturbation, $V=-eEy$
- Magnetic field in the $z-$direction
- Calculate $\sigma$ using _Heisenberg's equation of motion_ to determine $\left<j\right>_{x}$

# Z2 topological invariant
- Time-reversal symmetry often given by _spin-orbit interaction_

- Time-reversal symmetry: bands come in _Kramers pairs_ (witj $+\boldsymbol{k}$ and $-\boldsymbol{k}$ being at the _same energy_)
- They are _degenerate_ at the _time-reversal invariant momentum_ (TRIM)
	- Here, the $+\boldsymbol{k}$ and $-\boldsymbol{k}$ states are _equivalent_ due to periodicity of the BZ

- Similarly for _inversion symmetry_

- There is a $\mathbb{Z}^{2}$ _topological invariant_

## Time reversal symmetry

## Inversion symmetry

# BHZ model
- Motivated by the $\ce{ CdTe/HgTe/CdTe }$ quantum well, where the $s-$ and $p-$bands _invert_ at $\boldsymbol{k}=0$

# Types of topological materials

## 2D Materials

## 3D Materials

## Topological semimetals

- Weyl semimetal:
	- Weyl fermions are _massless_ and _chiral_
	- Two-component Dirac equation
- When TRS is broken in an _inversion-symmetric_ solid
- Weyl points come in _pairs_
- They give rise to an _arc of zero-energy excitation_ (Fermi arc) in the projected surface BZ

# New developments in theory
- Multi-band braiding? (Euler class instead of Berry flux)