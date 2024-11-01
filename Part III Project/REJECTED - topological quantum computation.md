Localisation and quantum error correction 
>[!Abstract]
>Topological superconductor systems emerge both as exotic electronic systems and as effective models linked to quantum error correction in certain many-qubit topological codes. The effects of disorder are key in both arenas: disorder is naturally present in electronic systems, and it also arises from patterns of error signatures in topological codes. This project aims to investigate the quantum mechanical effects of disorder in a class of two-dimensional topological superconductors relevant to both fields. The goal is to establish the phase diagram of the system: how the strength of disorder and system parameters set whether the eigenstates are localized or delocalized, as probed through the lens of quasiparticle transport through the system. A particular focus will be to study how spatial symmetries of the underlying clean system, and potentially also of disorder (at least in the sense of a statistical ensemble) impact the phase diagram; the results may be of relevance both to our understanding of superconducting electronic systems and quantum error correction.
# Background                                                                              
Quantum computer: susceptible to perturbation
How to measure information loss

Toric code/surface code

Qubits on edges of a 2D lattice 

Vertex and face stabiliser operators (they commute)

Prepare states: +1 eigenstates of stabilisers
Some degeneracy

Measure state --> error correction without destroying information

Another operator within the space: can change state

Different ways of connecting faces: inside/across boundary

Error --> perform stabiliser measurement --> correction operation
Depending on operation: can change state
Choosing correct operation - nontrivial problem

Some statistics/probability (when is it possible to correct an error)
Success: above some threshold, increase system size to decrease error rate exponentially

Define a partition function using effective Hamiltonian (random bond Ising model)
Phase transition for error correcting probabilities

1 kind of error: some stochastic noise to apply operator to side -> decoherence

Another error: unitary rotation (unknown angle, some error) (coherent error)
Errors can build up by constructive interference
Random bond ising model with complex coupling (not a classical partition function)

Related to a network model (charge transport)
Current conserving network -> compute conductivities (model for a superconductor)
Errors indicate direction of charge transport
Also displays phase transition for incoherent error (both insulating, but topologically distinct)
Coherent errors: transition between insulator and metal (up to which point one can correct errors)

# Project
Different lattices for toric/planar code
Example: hexagonal lattice
Behaviour of threshold is different from square lattice
Hexagonal: network model does not work (wrong connectivity)
	Difference in odd/even number of connections

Complex partition function : probability amplitude (absolute value to get probability)
Result: complex conjugate of model

Numerically simulate
Find phase diagrams for the lattice