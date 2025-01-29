# 28/10/24
- Meeting with Prof. Artacho

- In general, a _time-dependent basis set_ may be _not orthonormal_ (oblique basis set)
- Refer to Phys. Rev. A 43, 5770 (1991) for _nonorthogonal basis sets_
	- Includes second quantisation
- Consequences of time dependence-
	- Differential geometrical interpretation, with _gauge potential_: see Phys. Rev. B 95, 115155 (2017) 
	- Manifold curvature becoming _forces_: see SciPost Physics **12**, 020 (2022)

- Start Lit. review of time-dependent basis here: [[QM in an Evolving Hilbert Space]]

- Implement an _oblique_, _time-dependent_, _second-quantised_ basis set into the Hubbard model
- Simplest: the _Hubbard dimer_

- Need to review [[Floquet theory]]
	- Summary: Bloch's Theorem, but in time
	- Complication- quasi-energy periodicicity

- Result of Hubbard with time-dependent basis: _compare_ with a simple Hubbard model with _time-dependent parameters_
	- The _gauge potential_ should have some physical effect
- Check the _non-adiabatic limit_ (high frequency)
	- Search: Magnussen corrections?

- Potentially allow the _electronic cloud_ in the dimer to _deform_
- By hybridising a $1s$ and $2p$ orbital on _each site_
- Consider if there should be different Hubbard parameters depending on orbitals

# 29/10/24
- Literature review: [[QM in an Evolving Hilbert Space]]

# 30/10/24
- Literature review: [[QM in an Evolving Hilbert Space]]

# 31/10/24
- Looked for sources on Floquet physics, found multiple on arXiv
- See: [[Floquet theory]]

# 1/11/24
- Literature review of Floquet theory, and [[QM in an Evolving Hilbert Space#Second quantisation|second quantisation]] of a nonorthogonal basis

# 4/11/24
- Second quantisation of nonorthognal basis in Prof Artacho's paper seems to _contradict_ the definition in the TQM course and other papers????

# 5/11/24
 - Reviewing notes from Prof Artacho, the confusion from yesterday seems to be because there is a distinction between Hermitian conjugates and the creation/annihilation operaors in this formalism

# 7/11/24
- There is literature for doing second quantisation with Floquet states!
- Should be able to adapt this into the Hubbard Hamiltonian w/ time dependence


# 11/11/24
- For transient dynamics: see Floquet-Magnus theory??

# 14/11/24
- Change of basis is clear at this point, next step is absolutely to go forward into deriving equations of motion
	- Does there need to be a change of basis to the Fourier modes as well?
- Heisenberg or Schrodinger picture?
- See Eckhardt et al. for example of a tight-binding chain, and how to treat a Floquet many-body Hamiltonian
	- Terminology and functions from Rudner and Lidner
- SciPost article from Emilio: uses Schrodinger equation... how to adapt to Heisenberg equation of motion? Is that even necessary?
	- What equation of motion is important in this case?

# 15/11/24
- Many approaches to Floquet in literature speak of _effective, static Hamiltonians_, how to reconcile that with concepts of manifold curvature and forces?
- Approach taken by Rudner and Lidner: using the _many-body single particle Green's function_, which uses _Heisenberg operators_

# Week 1 Lent
- Deriving effective Hamiltonian matrix elements