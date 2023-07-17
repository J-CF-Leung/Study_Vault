- Typical elementary particles: _fermions_ and _bosons_
	- An _interchange_ of _identical particles_ leads to a _change in sign_ of the wave-function

- In _two-dimensional_ systems: _quasiparticles_ become _non-Abelian_
- Consequences:
	- _Degenerate_ ground state
		- _Independent_ of _symmetry_
		- _Robust_ against _perturbations_ and the _surrounding environment_
	- _Interchange_ of _identical_ quasiparticles will _shift_ the system _between different ground states_
		- If there is a _series_ of interchanges, then the _final state_ is _dependent_ on the _order of interchanges_

- Like how the interchange of _fermions_ gives a _sign change regardless of the system_, the _shifts_ resulting from interchange of _non-Abelian particles_ is also _independent of interparticle interactions and outside environment_

- For the interchange to occur, there must be an _energy gap_ between the ground states and their _excitations_
	- Common in many-body systems

- The _insensitivity to noise_ makes this an ideal candidate for _quantum computing_

## Abelian anyons
- Let there be a _many-body_ wave-function:
$$\Psi(r_1,r_2,\dots,r_N)$$
- Let the wave function be the _ground state_ of a many-body system, with an _energy gap_ separating it from excitations

- Let the process of interchanging particles be _adiabatic_ (slow)

- In _three spatial dimensions_, an interchange of _identical particles_ results in a _sign change_:
$$\Psi(r_2,r_1,\dots,r_N)=\pm\Psi(r_1,r_2,\dots,r_N)$$
- _Even_: the particles are _bosons_
- _Odd_: the particles are _fermions_

- In _two spatial dimensions_, a similar interchange can simply result in a _phase change_ of the _original wavefunction_:
$$\Psi(r_2,r_1,\dots,r_N)=\exp(i\phi)\Psi(r_1,r_2,\dots,r_N)$$
- Where $0<\phi<2\pi$

- These particles are known as _Abelian anyons_, as multiplying by a phase is _Abelian_
- The interchange is then known as a _braiding_

## Non-Abelian anyons
- In some _many-body_ systems, the ground state for a set of _quasiparticles_ is _degenerate_
- Then, it is possible to _interchange_ quasiparticles and lead to a _shift_ in ground state
- This interchange is _non-Abelian_

- Let the set of _particle positions_ be $\{r_i\}$, while the _collective excitations_ are described by coordinates $\{R_i(t)\}$ 
- The degenerate ground states are labelled by $\ket{\Psi_\alpha\{R_i\}}$