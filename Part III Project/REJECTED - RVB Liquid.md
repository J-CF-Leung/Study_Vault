>[!Abstract]
>The resonant valence bond (RVB) quantum liquid state was proposed by Anderson in the late 80's as a possible competitor to the Neel antiferromagnet. While the idea underpinned a whole new direction of research on quantum spin liquids and topological phases of matter, it was not until very recently that a realisation of an RVB state was proposed in a realistic Hamiltonian for a doped Mott insulator ([https://arxiv.org/abs/2408.03372](https://arxiv.org/abs/2408.03372)). This raises a new paradigm for the quantum spin liquids based on kinetic energy frustration, rather than geometric frustration of interactions. 
A particular instance where this novel RVB state can be found is the 2D checkerboard lattice, which had been previously studied numerically by Poilblanc ([https://link.aps.org/doi/10.1103/PhysRevLett.93.197204](https://link.aps.org/doi/10.1103/PhysRevLett.93.197204)). Notably, Poilblanc considered the additional effect of interactions and showed that this induces pairing between dopants, seemingly mediated by magnetic correlations, of potential interest as a novel route for unconventional superconductivity. 
In this project the student should try and extend Poilblanc's work taking advantage of the new analytical results available in [https://arxiv.org/abs/2408.03372](https://arxiv.org/abs/2408.03372). For instance, one could try to compute the statistics of the dopants (believed to be fermions but this is yet to be demonstrated, and it should be possible from the exact wavefunction). One could then try to add interactions at a perturbative level, and see if one can find an analytical understanding of the pairing (beyond Poilblanc's numerics); this will be a very tall order, as the exact ground state is no longer known in presence of interactions; some approximate techniques (possibly aided by numerics) may be needed.

- What is an RVB?
	- Alternative model to Neel antiferromagnet (anti-parallel spins)
	- Spins are _valence bond paired_ into _singlets_
	- The singlets _resonate quantum mechanically_ (superposition between all possible states) amongst different _pairing configurations_, which _compensates_ for the _partial loss of antiferromagnetic energy_
	- Analogy: resonant bonds in chemistry lowering energy

- High-temperature superconductivity _may be underpinned by spin-charge separation of strongly correlated electrons in an RVB liquid phase_
	- Spin-charge separation in the material (fractionalisation into two quasiparticles)
	- Strongly correlated: interactions >> free kinetic energy
	- The _charge_ can act as a _boson_ and _condense_, leading to a superconducting phase

- Proposal of RVB led to development of _spin liquids_

- Paper - demonstrates that _doping a large $U$ Hubbard model_, on a lattice of _corner-sharing tetrahedra_, with _half-filling_, can exhibit _spin-charge separation and RVB behaviour_
	- Large $U$ Hubbard model (Coulomb energy): Mott insulator --> Doped Mott insulator
	- Lattice: planar checkerboard, or 3D pyrochlore lattice
- Reliant on _kinematic spin correlations_, set by _frustrated hopping_ (kinetic energy frustration)
	- The _ground state_ is shown to be exactly an RVB liquid
	- Exact for single hole and two holes
	- Instance of _counter-Nagaoka effect_
	- frustrated quantum hole hopping leads to antiferromagnetic correlations in a Mott insulator near half-filling

- Compute correlations (exactly/numerically/statistically sampling)
- Statistical properties

- If fermions: pairing (maybe similar to BCS with phonon mediation?)
- Poilblanc: interactions lead to pairing
	- 2D checkerboard
- Interactions as perturbation

- Work in 2D or 3D
	- 2D: perturbative interactions can lead to conventional order
	- Antiferromagnetic exchange leads to RVB plaquette solid (liquid), only in 2D