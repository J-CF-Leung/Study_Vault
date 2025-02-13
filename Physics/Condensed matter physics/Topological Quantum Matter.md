- _Quantum many-body theories_ with _topological order_
- Concepts from both _field theory_ and _band theory_ apply

- Applications to _quantum computing_
	- Topological _quantum computation_ and _error correction_

- Topologically ordered systems may have the emergence of _anyons_
# Transverse field Ising model (TFIM)
- An $N-$site _lattice_ of _qubits_
- The _Pauli_ $X,Y,Z$ operators on site $j$:
$$X_{j}=\underbrace{ \mathbb{I} }_{ \text{site }1 }\otimes \mathbb{I}\otimes \dots \otimes  \underbrace{ X }_{\text{site }j} \otimes \dots \otimes \mathbb{I}$$

- A system which displays _spontaneous symmetry breaking_
- The Ising Hamiltonian, with _nearest neighbour_ interactions
$$H=-J\sum_{\langle i,j \rangle }Z_{i}Z_{j}-h\sum_{j}Z_{j}\quad,\quad J>0$$
- The _eigenstates_ of the Hamiltonian correspond to the _classical lattice configurations_
$$H\ket{\{z_{j}\}} =E(\{z_{j}\})\ket{\{z_{j}\}} $$
- The Hamiltonian also acts as the _time evolution operator_ of the system, for any general superposition

- A purely _quantum model_, adding a _transverse field_:
$$H=-J\sum_{\langle i,j \rangle }Z_{i}Z_{j}-h\sum_{j}X_{j}$$
- The eigenstates are a _superposition_ of lattice configurations

## Symmetry of the Hamiltonian
- The _parity_ operator:
$$P=\prod_{j}X_{j} \qquad P\ket{\{z_{j}\}}=\ket{\{-z_{j}\}} \quad PZ_{j}P^{\dagger}=-Z_{j} $$
- For any $J,h$, the _transverse field_ model is _symmetric under parity_:
$$PH=HP$$
- It is a $\mathbb{Z}_{2}$ symmetry

### Paramagnetic and ferromagnetic phases
- For the $J=0$ limit, the _ground state_ is a simultaneous ground state of all spins in the state $\ket{+}_{j}$
$$\ket{\text{GS}}=\otimes _{j}\ket{+}_{j}\equiv \ket{\boldsymbol{X}} \qquad X_{j}\ket{+}_{j}=\ket{+}_{j}    $$
- In the $h=0$ limit, there are _two distinct, fully polarised_ ground states
$$\displaylines{\ket{\Uparrow} =\otimes _{j}\ket{\uparrow}_{j}\qquad Z_{j}\ket{\uparrow}_{j}=\ket{\uparrow}_{j}   \\ \ket{\Downarrow}=\otimes _{j}\ket{\downarrow}_{j}\qquad Z_{j}\ket{\downarrow}_{j}=\ket{\downarrow}_{j}     }$$
- Any _linear combination_ of these states will also be a ground state in this limit

### Symmetry (breaking)
- These phases differ in their _symmetry_
- One can use the _ground state expectation_ of $Z_{j}$ as an _order parameter_
$$\displaylines{P\ket{\boldsymbol{X}}=\ket{\boldsymbol{X}} \qquad \braket{ \boldsymbol{X} |Z_{j}|  \boldsymbol{X}}=0 \\ P\ket{\Uparrow} =\ket{\Downarrow} \qquad \braket{ \Uparrow|Z_{j} | \Uparrow }\neq 0   }$$
- $\ket{\boldsymbol{X}}$ is known as the _paramagnetic state_, which is _symmetric_
- $\ket{\Uparrow},\ket{\Downarrow}$ are the _ferromagnetic states_, which have _broken symmetry_

- However, as $[H,P]=0$, one can _simultaneously diagonalise_ them with the states:
$$\ket{\text{GS}_{\pm}}=\frac{\ket{\Uparrow}\pm \ket{\Downarrow}  }{\sqrt{ 2 }}\qquad P\ket{\text{GS}_{\pm}}=\pm \ket{\text{GS}_{\pm}}   $$
- They are _invariant up to_ a $\pi$ phase shift under $P$
- It is a state which _does not break symmetry_:
$$\braket{ \text{GS}_{\pm}|Z_{j} |\text{GS}_{\pm}  }=0 $$

- In the paramagnetic phase, the ground state is _unique_
- In the ferromagnetic phase, it is _degenerate_ hence one can _choose_ ground states to be _exchanged_ by the symmetry operator


## Brillouin-Wigner perturbation theory
- Study the system as a _ferromagnetic system_ with some _perturbation_
$$H_{0}=-J\sum_{\langle i,j \rangle }Z_{i}Z_{j}\qquad \delta H=-h\sum_{j}X_{j}$$
- $H_{0}$ is _gapped_, as any _perturbation_ has energy of _at least_ $\sim J$ above the ground state
	- Must be in the _thermodynamic limit_ $N\to \infty$ such that there are _no quantisation effects_

- The goal is to develop an _effective Hamiltonian within_ the _ground state space_
### Perturbed eigenstates
- Let the _unperturbed_ $H_{0}$ and perturbed $H$ both have a set of _orthonormal eigenstates_
$$H_{0}\ket{n}=E_{n}\ket{n}\qquad H\ket{\tilde{n}}=E_{\tilde{n}}\ket{\tilde{n}}    $$
- Let the _unperturbed ground state energy_ be $E_{0}$, with a _degenerate ground state subspace_ $S$, of dimension (number of states) $d_{G}$
- The _excited state_ then has an _orthogonal complement_ $S^{\perp}$
- Projectors to the subspaces:
$$P=\sum_{n \in S}\ket{n}\bra{n}\qquad Q=1-P=\sum_{n \in S^{\perp}}\ket{n}\bra{n}    $$

- Assume that $H_{0}$ has a _gap_ $\Delta$ between the ground and lowest excited states

- In the presence of $\delta H$, the _degenerate ground states_ will _split_ into energies $E_{\tilde{m}}$
- For a _weak_ perturbation, assume the splitting is _much smaller_ than $\Delta$ for all $d_{G}$ states:
$$E_{0}<E_{\tilde{m}}<E_{0}+\Delta\qquad \tilde{m}=1,2,\dots d_{G}$$
- Denote the corresponding _un-normalised_ eigenstates as $\ket{\tilde{m}^{u}}$
- Demand that the _projection_ is normalised:
$$P\ket{\tilde{m}^{u}}\equiv\ket{\psi_{\tilde{m}}}\qquad \braket{ \psi_{\tilde{m}} |\psi_{\tilde{m}}  }=1   $$

### Effective Hamiltonian
- From the Schrodinger equation, with _eigenkets_ $\ket{n} \in S^{\perp}$
$$\displaylines{(H_{0}+\delta H)\ket{\tilde{m}^{u}}=E_{\tilde{m}}\ket{\tilde{m}^{u}}\implies \delta H\ket{\tilde{m}^{u}}=(E_{\tilde{m}}-H_{0})\ket{\tilde{m}^{u}} \\  \braket{ n|\delta H |\tilde{m}^{u}  } =(E_{\tilde{m}}-E_{n})\braket{ n |\tilde{m} ^{u} }  }$$
- From this, _summing over_ the basis in $S^{\perp}$, one gets an expression for $Q\ket{\tilde{m}^{u}}$
	- The expression always _converges_ due to the gap
	- $G$ is a _Greens function_
$$Q\ket{\tilde{m}^{u}}=G\delta H\ket{\tilde{m}^{u}}\qquad G=\sum_{n\in S^{\perp}} \frac{\ket{n}\bra{n}}{E_{\tilde{m}}-E_{n}}    $$
- The eigenket can then be written as an _infinite series_
	- Only the _first term_ is within $S$
$$\displaylines{\ket{\tilde{m}^{u}}=\ket{\psi_{\tilde{m}}}+G\delta H\ket{\tilde{m}^{u}} \\ \ket{\tilde{m}^{u}}=(1-G\delta H)^{-1}\ket{\psi_{\tilde{m}}}=\ket{\psi_{\tilde{m}}}+G\delta H\ket{\psi_{\tilde{m}}}+G\delta HG\delta H\ket{\psi_{\tilde{m}}}+\dots        }$$
- To find the _energies_ $E_{\tilde{m}}$, applying eigenket $\ket{n'} \in S$
$$(E_{\tilde{m}}-E_{0})\braket{ n' |\tilde{m} ^{u} } =\braket{ n' |\delta H(1-G\delta H)^{-1}|\psi_{\tilde{m}}  } $$
- Introducing the _components_:
$$\displaylines{v_{n'}^{(\tilde{m})}=\braket{ n' |\tilde{m}^{u}  }  \\ \ket{\psi_{\tilde{m}}}=\sum_{n' \in S}\ket{n'}\braket{ n' |\tilde{m} ^{u} }=\sum_{n' \in S}\ket{n'}v_{n'}^{(\tilde{m})}    }$$
- One can then define an _effective Hamiltonian_:
$$\displaylines{\sum_{n'\in S}H^{\text{eff}}_{nn'}v_{n'}^{(\tilde{m})}=(E_{\tilde{m}}-E_{0})v_{n}^{(\tilde{m})} \\ n,n' \in S\qquad H^{\text{eff}}_{nn'}=\braket{ n |\delta H(1-G^{(\tilde{m})}\delta H)^{-1}|n'  } }$$
- The _energy corrections_ are obtained from _diagonalising_ the $d_{G}\times d_{G}$ $H^{\text{eff}}$
- The equation has to be solved _self-consistently_ as $G^{(\tilde{m})}$ is dependent on $E_{\tilde{m}}$

### Approximations
- The energy denominator:
$$E_{\tilde{m}}-E_{n}=(E_{0}-E_{n})\left( 1+\frac{E_{\tilde{m}}-E_{0}}{E_{0}-E_{n}} \right)=(E_{0}-E_{n})\left( 1+\mathcal{O}\left[ \frac{E_{\tilde{m}}-E_{0}}{\Delta} \right] \right)$$
- The equation can be _simplified_ by replacing $E_{\tilde{m}}$ with $E_{0}$, introducing a _small relative error_

- It also encodes _standard perturbation theory_, by separating into _orders_
$$\frac{1}{E_{\tilde{m}}-E_{n}}=\frac{1}{E_{0}-E_{n}}\sum_{k=0}^{\infty}\left( \frac{E_{0}-E_{\tilde{m}}}{E_{0}-E_{n}} \right)^{k}$$

## Perturbation theory analysis of the TFIM
$$H_{0}=-J\sum_{\langle i,j \rangle }Z_{i}Z_{j}\qquad \delta H=-h\sum_{j}X_{j}$$
- The ground states are $\ket{\text{GS}_{\pm}}$
- The perturbation theory is applied _within a $\mathbb{Z}_{2}$ symmetry sector_ (subspaces labelled by eigenvalues $p=\pm1$)
- _Within_ each sector, the ground state is _unique_ such that $H^{\text{eff}}$ is $1\times 1$
$$\begin{align}
\delta E_{\pm}&=\braket{ \text{GS}_{\pm} | \delta H(1-G\delta H)^{-1}|\text{GS}_{\pm} }  \\
&=\braket{ \text{GS}_{\pm} |\delta H |\text{GS}_{\pm} }+\braket{ \text{GS}_{\pm} |\delta HG\delta H |\text{GS}_{\pm} }+\braket{ \text{GS}_{\pm} |\delta HG\delta HG\delta H |\text{GS}_{\pm} }\dots 
\end{align}$$
### Energy correction: shifts
- For a lattice of $N$ qubits, applying $\delta H$ gives a _sum of excited states_, where a single spin is _flipped_
$$\delta H\ket{\text{GS}_{\pm}} =-h\sum_{j}X_{j}\ket{\text{GS}_{\pm}} \qquad \braket{ \text{GS}_{\pm}|\delta H |\text{GS}_{\pm}  }=0 $$
- The $h^{1}$ term is _zero_

- From this, $G$ simply gives a _denominator_ resulting from the excited states of $H_{0}$
	- $z$: number of _nearest neighbours_ 
$$G\delta H\ket{\text{GS}_{\pm}}=-h\sum_{j} \frac{X_{j}}{E_{\tilde{m}}-(E_{0}+4zJ)} \ket{\text{GS}_{\pm}} \propto \frac{h}{J}\sum_{j}X_{j}\ket{\text{GS}_{\pm}} $$
- Applying $\delta H$ again will _unflip_ spins back to the original, giving the $h^{2}$ term:
$$\braket{ \text{GS}_{\pm}|\delta HG\delta H | \text{GS} }_{\pm}\propto -N \frac{h^{2}}{J} $$
- This applies for _both parities_ $p=\pm1$

- As for $(G\delta H)(G\delta H)\ket{\text{GS}_{\pm}}$, this _leads to zero_ $h^{3}$ contribution
	- The _flipped, then unfliped_ spins _will not contribute_ due to the second $G$
	- Only the _two flipped spin_ terms will contribute and _cannot be undone_ by $\delta H$

- So on, $(G\delta H)^{m-1}\ket{\text{GS}_{\pm}}$ only gives non-zero contributions for _one flipped spin_
- These are the _energy shifts_ for both $\ket{\text{GS}_{\pm}}$ that go as $J(h/J)^{2n}$

### Energy corrections: exponentially accurate splitting
- However, for $m\geq N$, it can give $N-1$ flipped spins, $\delta H$ then flips the last to give a _parity-dependent energy correction_ with coefficient $\delta\varepsilon^{(m)}/2$
$$\begin{align}
\braket{ \text{GS}_{\pm}|\delta H(G\delta H)^{m-1} |\text{GS}_{\pm}  } &\to \frac{\delta\varepsilon^{(m)}}{2}\Braket{ \text{GS}_{\pm}|\prod_{j=1}^{N}X_{j} |\text{GS}_{\pm}  } \\
&=\frac{\delta\varepsilon^{(m)}}{2}\braket{ \text{GS}_{\pm}|P |\text{GS}_{\pm}  }=\pm\frac{\delta\varepsilon^{(m)}}{2}  
\end{align}$$
- This gives a _splitting_ between the ground states
- To _leading order_ in $h/J$, the energy splitting is:
$$\delta\varepsilon _\text{split}\propto J\left( \frac{h}{J} \right)^{N}$$
- In the limit of $0<|h|\ll J$, the ground state degeneracy is _not exact_
- However, it is _exponentially suppressed_ in the thermodynamic limit $N\to \infty$

### Linear fragility
- The _splitting_ relies on the $Z_{2}$ symmetry of $H_{0}+\delta H$

- One can add a _symmetry breaking term_ for _one site_ $j$ to the Hamiltonian:
$$\delta H'=-h'Z_{j}$$
- In this case, simply use $\ket{\Uparrow},\ket{\Downarrow}$ as the unperturbed ground states
- The _splitting_ is then $2h'$, a _first order splitting_

- The degeneracy is _exponentially accurate_, but _linearly fragile_

### Perturbed eigenstates
- In _each sector_, as there is only $\ket{\text{GS}_{\pm}}$ in the subspace $S$, $\ket{\psi_{\tilde{\pm}}}=\ket{\text{GS}_{\pm}}$ 
$$\ket{\tilde{\text{GS}}^{u}_{\pm}}=(1-G\delta H)^{-1}\ket{\text{GS}_{\pm}}  $$
- The perturbed eigenstate is an _admixture of spin flips_ due to $\delta H$
- One can also write:
	- $\ket{\tilde{\Uparrow}^{u}}$ and $\ket{\tilde{\Downarrow}^{u}}$ are _not eigenstates_ as $\ket{\tilde{\text{GS}}^{u}}$ are not degenerate
	- They only become eigenstates in the _thermodynamic limit_ $N\to \infty$
$$\ket{\tilde{\text{GS}}_{\pm}^{u}}=(1-G\delta H)^{-1} \frac{\ket{\Uparrow}\pm \ket{\Downarrow}  }{\sqrt{ 2 }}= \frac{1}{\sqrt{ 2 }}(\ket{\tilde{\Uparrow}^{u}}+\ket{\tilde{\Downarrow}^{u}}  )$$
## Characteristics of spontaneous symmetry breaking
- For nonzero $J,h$, _any eigenstate_, such as the _exact ground state_ $\ket{\psi}$, will _preserve_ $\mathbb{Z}_{2}$ symmetry:
$$P\ket{\psi}=p\ket{\psi} \implies PZ_{j}=-Z_{j}P\implies \braket{ \psi|Z_{j} |\psi}=0 $$
- This can be _generalised to other symmetries and their order parameters_
- In _finite systems_, spontaneous symmetry breaking is _absent in eigenstates_

- In the thermodynamic limit $N\to \infty$:
	- _Ferromagnetic ground states_ become _degenerate_
	- The _paramagnetic phase_ remains a _unique ground state_
- Paramagnetic ground state is _symmetric_:
$$\braket{ \psi|Z_{j} |\psi  }=0 $$
- For the _ferromagnetic phase_ at _finite_ $N$, the states $\ket{\psi_{\Uparrow,\Downarrow}}$ are _approximate ground states_
	- They are _constructed_ from the _exact ground states_ $\ket{\psi_{\pm}}$
$$\displaylines{P\ket{\psi_{\pm}}=\pm \ket{\psi_{\pm}} \qquad \ket{\psi_{\Uparrow,\Downarrow}}\equiv(\ket{\psi_{+}}-\ket{\psi_{-}}  )/\sqrt{ 2 }   \\ P\ket{\psi_{\Uparrow}}=\ket{\psi_{\Downarrow}}\qquad \braket{ \psi_{\Uparrow}|Z_{j} |\psi_{\Uparrow}  }=M_{0}\neq 0   }$$
- One may _choose_ either as the ground state by adding an _explicitly symmetry breaking term_ $\pm h'Z_{j}$
- Denoting $\ket{\psi}$ as the chosen ground state:
$$\lim_{ h' \to 0 }\lim_{ N \to \infty } \braket{ \psi|Z_{j} |\psi  }=M_{0}~\neq 0  $$
- This _defines spontaneous symmetry breaking_ in $\mathbb{Z}_{2}$

- The _order of limits_ matters as one must _go to the thermodynamic limit before turning off explicit symmetry breaking_


- One can also _distinguish_ the phases without explicit symmetry breaking
- Consider the _ground state correlation functions_ for finite $N\gg 1$ and state $\ket{\psi}$
$$C^{(Z)}_{|j-j'|}=\braket{ \psi|Z_{j}Z_{j'} | \psi }-\braket{ \psi|Z_{j} |\psi  } \braket{ \psi|Z_{j} | \psi } \to \begin{cases}
M_{0}^{2}&\text{FM} \\\propto \exp(-c|j-j'|),c>0 &\text{PM}
\end{cases} $$
- This also _defines spontaneous symmetry breaking_

- It shows that the _ferromagnetic phase has long range order_
- It is a _symmetry-broken ordered phase_

- Meanwhile, the paramagnetic phase is a _disordered phase_
# The surface code
- The _simplest topologically ordered system_
- Capable of supporting _quantum error correction_

- Useful formula for Pauli operators: for _two sets of qubits_ $M,M'$:
	- Proof: pull $Z_{j}$ to the left, will pick up a minus sign if they are at the _intersection_
	- $|M\cap M'|$ is the _number of elements in the intersection_
$$\left( \prod_{j \in M}X_{j} \right)\left( \prod_{j \in M'}Z_{j} \right)=(-1)^{|M \cap M'|  }\left( \prod_{j \in M'}Z_{j} \right)\left( \prod_{j \in M}X_{j}\right)$$

## Square lattice Hamiltonian
- Model a _two dimensional surface code_, on a _square lattice_
- With _one qubit on each link_

- A graphical representation of the surface code:
![[Toric code setup.png|250]]
- The Hamiltonian, consisting of _vertex operators_ and _plaquette operators_
$$H=-J_{A}\sum_{v}A_{v}-J_{B}\sum_{p}B_{p},\quad J_{A,B}=0$$
- The _vertex operator_ $A_{v}$ will _flip spins surrounding_ vertex $v$
- The _plaquette operator_ $B_{p}$ calculates the _parity_ of spins _around a plaquette_
$$A_{v}=\prod_{j \in v}X_{j}\qquad B_{p}=\prod_{j \in p}Z_{j}$$
- The operators are both _idempotent_, and thus have eigenvalues $\pm1$
$$A_{v}^{2}=B_{p}^{2}=1\implies a_{v},b_{p}=\pm1$$
- The operators also _commute_, as vertex and plaquette operators _share_ 0 or 2 sites
$$[A_{v},B_{p}]=0$$
- The operators $\{A_{v}\}\cup\{B_{p}\}$ form a set of _mutually commuting elements_, which also commute with $H$
- They are _integrals of motion_, that allow eigenstates to be _labelled_ $\{a_{\nu}\},\{b_{p}\}$

- One can then also take products to create other integrals of motion:
$$\prod_{v\in V}A_{v}\prod_{p \in P}B_{p}$$
### Integrals of motion from loops
- Attempt to construct integrals of motion that are _not simply a product_ as above

- Try an operator corresponding to some _set of qubits_ $M$, already commuting with $A_{\nu}$
$$\mathcal{X}_{M}=\prod_{j \in M} X_{j}$$
- For it to _also commute_ to $B_{p}$, it must share an _even number of sites_
- Representing $X_{j}$ as a line perpendicular to the link (see figure above), they must _not end in a plaquette_ for the operators to commute
- Therefore, $\mathcal{X}_{M}$ must correspond to a _set of loops_

- A _large loop_ is simply a _product of adjacent_ $A_{\nu}$, as $A_{v}^{2}=1$
![[Toric code loop contraction.png|200]]
- Following the same logic, _any path can be deformed_ by applying $A_{v}$
- If a loop can be _contracted into nothing_ by applying suitable $A_{v}$, then _it is not a new integral of motion_

- Therefore, depending on the _manifold topology_ on which the _surface code_ lives, one can have _noncontractible loops_
	- The _number of independent, noncontractible loops_ gives the _homology_
	- For a _closed manifold_, this is known as the _1st Betti number_ $\beta_{1}$
	- It is related to the _genus_ by $\beta_{1}=2g$
	- They are _topological invariants_ (unaffected by continuous deformations)

- A _noncontractible loop_ gives a _new integral of motion_
- For example, take the _torus_ where $g=1,\beta_{1}=2$, giving the _toric code_

### Toric code
- A _torus_ is created by _identifying_ opposite edges of a square surface
- Define two _non-contractible loops_ $\gamma_{1,2}$ over the torus
$$\bar{X}_{j}\equiv\mathcal{X}_{\gamma_{j}}=\prod_{i \in \gamma_{j}}X_{i}\neq \prod_{v \in V}A_{v}$$
- They _commute_ with the vertex and plaquette operators
$$[\bar{X}_{j},A_{v}]=[\bar{X}_{j},B_{p}]=0$$
- Also define:
$$\bar{Z}_{j}=\prod_{i \in \gamma_{j}}Z_{i}\neq \prod_{p  \in P}B_{p}$$
- For both operators:
$$\bar{X}_{j}^{2}=\bar{Z}_{j}^{2}=1$$
- They behave like Pauli operators:
$$\bar{X}_{i}\bar{Z}_{j}=(-1)^{\delta_{ij}}\bar{Z}_{j}\bar{X}_{i}$$
- As they _do not commute_, one can use _either_ $\bar{z}_{i}$ or $\bar{x}_{i}$ as a _quantum number_

- Thus, one completes labelling _eigenstates for a general manifold_ as:
$$\ket{n}=\ket{\{a_{v}\},\{b_{p}\};\bar{z}_{1},\bar{z}_{2}\dots \bar{z}_{\beta_{1}}}  $$
- As the energy _does not depend_ on the $\bar{z}$ eigenvalues

- Therefore, there is a _topological ground state degeneracy_
$$\text{GSD}=2^{\beta_{1}}$$
- Unlike the Ising model, this is _topology-dependent_

## Surface code excitations
- The _ground state_ $\ket{\psi}$:
$$a_{v}=b_{p}=1\quad \forall v,p$$
- The _excited states_ will have some $a_{v}$ or $b_{p}=-1$, and their _combinations_

- To get some excitation, one can _apply_ $X_{j}$ and $Z_{j}$ on some _set_ of qubits $\alpha$
$$\mathcal{Z}_{\alpha}=\prod_{j \in \alpha}Z_{j}\qquad \mathcal{X}_{\beta}=\prod_{j \in \beta}X_{j}$$
- $\alpha$ must _not be a loop_ (have some _boundary_)
- For $v$ at the _boundary_ $\partial\alpha$
$$A_{v}(\mathcal{Z}_{\alpha}\ket{\psi} )=-\mathcal{Z}_{\alpha}(A_{v}\ket{\psi} )=-\mathcal{Z}_{\alpha}\ket{\psi} \implies a_{v}=-1\quad (v \in \partial\alpha)$$

- _Flipping_ each vertex requires $2J_{A}$ of energy
- One can interpret them as _particles_ $e$ (electric)
- For $M$ particles, the energy is $2MJ_{A}$, there is _no interaction energy_

- As _endpoints_ for the path comes in _pairs_, particles are connected by _strings_
- The _pairing_ of particles is also _arbitrary_
	- By applying $B_{p}$ between 2 string midpoints, one can _"exchange"_ strings

- One can also create particles $m$ (magnetic) with $b_{p}=-1$
- The surface code is also _gapped_, with gap $4\,\mathrm{min}(J_{A},J_{B})$

- States with the _same number of excitations_ may _not be the same_, if they are _built_ on top of _different ground states_

# Particle exchange and braiding
- Focus on the _exchange effects_ of _identical particles_ instead of any dynamical details
- _Exchange_ means the _initial and final configurations are the same_

- Assume the particles are _much further apart_ than the _interaction range_
- This leads to _non-intersecting worldlines_

- Also strip away _local details_ along the paths
- This gives _topologically invariant features_

## Exchange effects in 2D
- Consider a _2+1D_ system

- Braids: _cannot be backwards in time_
- Example: a _4-particle braid_
![[4 particle braiding.png]]
- Trivial: the _identity_ braid
- One can _compose_ braids
- One can have _clockwise_ braids $\sigma_{i}$ and _counterclockwise_ braids $\sigma_{i}^{-1}$
	- From composition, they are _inverses_ of each other

- For $N$ particles, the braids form a _braid group_ $B_{N}$
	- They satisfy the _group axioms_

- The exchanges are known as _generators_ of the group
- The group is generally _non-Abelian_:
$$\sigma_{j+1}\sigma_{j}\neq\sigma_{j}\sigma_{j+1}$$

- For _distinguishable particles_, one will have different _braid types_
- For $N_{a}$ and $N_{b}$ of each type, the group is denoted $B_{N_{a},N_{b}}$
- There can be _indistinguishable particles braiding_ $\sigma_{a},\sigma _b$, as well as _distinguishable particles encircling each other_ $\mu_{a,b}$
	- Distinguishable particles must _encircle_ to end up with the same configuration

### Exchange in 3D
- In 3D, there is _no distinction_ between clockwise and anticlockwise exchange:
	- From considering braiding two particles as moving on a 2-sphere (with antipodal points identified)
$$\sigma^{-1}=\sigma$$
- Particle exchange in 3D is governed by the _permutation group_ $S_{N}$
## Effect on quantum states
- The exchange can be seen as a _time evolution operator_
$$\sigma_{j}\to \mathcal{U}(\sigma_{j})$$
- The _composition_ of braids:
$$\mathcal{U}(\sigma_{j}\sigma_{i})=\mathcal{U}(\sigma_{j})\mathcal{U}(\sigma_{i})$$
- The operators should be a _unitary representation_ of $B_{N}$ or $S_{N}$

- One can have an _Abelian representation_:
$$U(\sigma_{j})=\exp(i\theta_{j})$$

- In 3D, as $\sigma^{2}=1$, the _only acceptable representations_:
$$\theta=0,\pi$$
- One then gets _bosons and fermions_

- In 2D, they can have _any phase_
- One then gets _Abelian anyons_
$$U(\sigma_{j})=\exp(i\theta _{j}) \quad \theta_{j}\in [0,2\pi)$$
- For _distinguishable particles_, define:
$$U(\mu_{ab})=\exp(2i\theta_{ab})$$
![[Abelian anyons.png]]

- As the braid group is non-Abelian, one can also have _non-Abelian representations_:
$$U(\sigma_{i})U(\sigma_{j})\neq U(\sigma_{j})U(\sigma_{i})$$
- This occurs when _spatial coordinates_ are _not sufficient to specify the quantum state_ (i.e. there is some _degeneracy_)

- Example: spin-1/2 fermions, where one has to specify _spin_, and the Hilbert space can be _factorised_ into _spatial_ and _spin_ subspaces

- One can also have situations where the _Hilbert space does not factorise_

## Statistics in the surface code
- One can _move_ some $e$ or $m$ particle by applying a _sequence_ of $Z_{j}$ or $X_{j}$ onto the original sequence $\alpha$

- Let there be some _eigenstate_ with some $e$ and $m$ particles with strings $\alpha_{e}$ and $\alpha_{m}$
$$\ket{\Psi_{0}}=\mathcal{X}_{\alpha_{m}}\mathcal{Z}_{\alpha_{e}}\ket{\Psi}  $$
- Let $e$ _encircle_ $m$ clockwise with some operator $\mathcal{Z}_\text{loop}$, corresponding to a _path_ $\alpha _\text{loop}$
- The loop must _intersect only once_ with $\alpha_{m}$
- As it is a _contractible loop_, $\mathcal{Z}_\text{loop}\ket{\Psi}=\ket{\Psi}$

- From these considerations:
$$\mathcal{Z}_\text{loop}\ket{\Psi_{0}} =\mathcal{Z}_\text{loop}\mathcal{X}_{\alpha_{m}}\mathcal{Z}_{\alpha_{e}}\ket{\Psi}=-\mathcal{X}_{\alpha_{m}}\mathcal{Z}_{\alpha_{e}}\mathcal{Z}_\text{loop}\ket{\Psi}=-\ket{\Psi_{0}}   $$
- From the definition of $\theta_{em}$:
$$\exp(2i\theta _\text{em})=-1$$
- From similar considerations:
$$\exp(i\theta_{e})=\exp(i\theta_{m})=1$$

- One finds that $e$ and $m$ are _bosons_, but they are _mutual semions_
![[Surface code braiding.png]]

# Path integrals and charge-flux composite anyons
- For any _time evolution_, the _toplogical part_ can be encoded by some element $g$ of the braid group $B_{N}$

- Consider some _transition amplitude_
$$\Braket{ \{x_{j}(t_{f})\}|\mathcal{T}\exp\left( -\frac{i}{\hbar}\int  dt\,H(t)  \right) | \{x_{j}(t_{i})\} } $$
- This is some [[AQFT#Path integrals|path integral]]:
$$\int_{\{x_{j}(t_{f})\}\leftarrow \{x_{j}(t_{i})\}} \mathcal{D}\{x_{j}\}\exp\left( \frac{i}{\hbar}S[\{x_{j}\}] \right) $$
- Consider _braids_, where:
$$\{x_{j}(t_{f})\}=\{x_{j}(t_{i})\}$$
- One can then _classify_ the worldlines based on elements $g$ of the braid group $B_{N}$
- The action can then be _decomposed_ into a part due to _local details_, and a part depending on _topology_
$$S[x_{j}(t)]=S_{0}[x_{j}(t)]+\hbar W(g)$$
- The path integral is then:
$$\sum_{g \in B_{N}}\exp(iW[g]) \int_{\{x_{j}(t_{f})\}=\{x_{j}(t_{i})\} \in g}\mathcal{D}\{x_{j}\}\exp\left( \frac{i}{\hbar}S_{0}[\{x_{j}\}] \right) $$
## Aharonov-Bohm and Aharonov-Casher effects
- A mechanism through which a nontrivial $W$ emerges

- Aharonov-Bohm: a _charge encircling flux_
- Aharonov-Casher: a _flux encircling charge_

- Consider a _2D system_ with one particle of charge $q$
- The Lagrangian, due to some _scalar potential_ $\phi$ and _vector potential_ $\boldsymbol{A}$
$$L=L_{0}-q(\phi-\dot{\boldsymbol{x}}\cdot \boldsymbol{A})$$
- Consider some _time-independent, point-like flux_ $\Phi$, from a particle $\boldsymbol{X}$
- Let there be a charged particle, following path $\boldsymbol{x}$ _encircling_ the flux
	- It is outside the region of flux such that $\boldsymbol{E}=\boldsymbol{B}=0$ everywhere

- The _action_ from the path has a _topological contribution_ from the flux:
$$\displaylines{S[\boldsymbol{x}]=S_{0}+q\int  dt\, \dot{\boldsymbol{x}}\cdot \boldsymbol{A} =S_{0}+q \oint d\boldsymbol{x}\cdot \boldsymbol{A} =S_{0}+qn\Phi \\ W[n]=\frac{qn\Phi}{\hbar}}$$
- This is the _Aharonov-Bohm effect_
- The paths are _topologically classified_ by $n$

- Alternatively, let the _flux particle_ $\boldsymbol{X}$, following path $X_{f}$, give some vector potential:
	- $\boldsymbol{A}_{f}$ is the potential for a flux at the origin
	- This potential is _invariant under translation_
$$\boldsymbol{A}(\boldsymbol{x})=\boldsymbol{A}_{f}(\boldsymbol{x}-\boldsymbol{X}_{f})$$
- Requiring $\boldsymbol{E}=0$ along path $\boldsymbol{x}$, the _corresponding scalar potential_ is then:
$$\phi=\dot{\boldsymbol{X}}_{f}\cdot \boldsymbol{A}(\boldsymbol{x})$$
- The Lagrangian, only depending on the _relative motion_ between $\boldsymbol{x}$ and $\boldsymbol{X}$
$$L=L_{0}-q(\dot{\boldsymbol{X}}_{f}-\dot{\boldsymbol{x}})\cdot A_{f}(\boldsymbol{x}-\boldsymbol{X}_{f})$$
- For a path encircling $\boldsymbol{x}$, there is the same _topological contribution to phase_
$$W[n]=\frac{qn\Phi}{\hbar}$$

## Charge-flux composite model for anyons
- Let particles have some charge $q_{j}$ and _flux_ $\Phi_{j}$
- Let the flux have some _extent_ $\delta \boldsymbol{x}_{j}$

- For _non-intersecting worldlines_, interparticle separation must be much larger than $|\delta \boldsymbol{x}_{j}|$

- The _flux-charge interaction Lagrangian_:
$$L_{I}=\sum_{j,k} q_{j}(\dot{\boldsymbol{X}}_{k}-\dot{\boldsymbol{x}}_{j})\cdot \boldsymbol{A}_{f}(\boldsymbol{x}_{j}-\boldsymbol{X}_{k})$$
- When particle $j$ _encircles_ $k$, the contributions to phase:
	- Aharonov-Bohm: _charge_ $q_j$ circles _flux_ $\Phi_{k}$
	- Aharonov-Casher: _flux_ $\Phi_{j}$ circles _charge_ $q_{k}$

- The definition of $\theta_{jk}$:
$$\exp(2i\theta_{jk})=\exp\left[ \frac{i}{\hbar}(q_{j}\Phi_{k}+q_{k}\Phi_{j}) \right]$$
- When the particles are _identical_:
$$\exp(i\theta)=\exp\left( \frac{i}{\hbar}q\Phi \right)$$
- This then models _anyons_ as there is no restriction on $q$ and $\Phi$

### Spin statistics
- For some _spin_ $J$, a _rotation_ about $z$ with angle $\alpha$ is given by the operator
$$R(\alpha)=\exp\left( -\frac{i\alpha J_{z}}{\hbar} \right)$$
- For a _half-integer spin_, $R(2\pi)=-1$
- For an _integer spin_, $R(2\pi)=1$

- For the charge-flux composite, a $2\pi$ rotation gives $\boldsymbol{x}_{j}$ encircling $\boldsymbol{X}_{j}$ once:
$$R(2\pi)=\exp\left( \frac{i}{\hbar} q\Phi \right)=\exp(i\theta)$$

### Anyon fusion
- Bringing two charge-flux composites $j$ and $k$ together
- For the purposes of _both particles braiding around others_, it is _effectively_ one anyon of charge $q_{j}+q_{k}$ and flux $\Phi_{j}+\Phi_{k}$
![[Anyon fusion.png|200]]

### Anti-anyons and vacuum particles
- Let there be some _vacuum particle_ $q,\Phi=0$

- One can then define an _anti-particle_ $(-q_{j},-\Phi_{j})$
- One can _annihilate_ particles with the anti-particles
- Or, consider a _reversed worldline_
![[Anti-anyons.png|400]]
- Clockwise encircling an anyon of phase $\theta$ by its _antiparticle_ gives $\exp(-2i\theta)$

- Applying this to the _surface code_, as $e$ and $m$ are _created in pairs from vacuum_, they are _their own antiparticle_
## Ground state degeneracy from braiding
- Consider the _torus_ with non-contractible loops $\gamma_{1,2}$

- Consider a _unitary operator_ $T_{j}$, where one _creates_ an anyon-antianyon pair, _moves_ the anyon along $\gamma_{j}$, then _annihilates_ the pair
- It moves the system _between ground states_

- Choose a _basis of ground states_ $\{\Psi_{\alpha}\}$ such that:
$$T_{2}\ket{\Psi_{\alpha}}=\exp(i\alpha)\ket{\Psi_{\alpha}}  $$
- $T_{1}\ket{\Psi_{\alpha}}$ must also be a ground state

- Inspect:
$$T_{2}^{-1}T_{1}^{-1}T_{2}T_{1}$$
![[Torus braiding.png]]

- This braid gives:
$$T_{2}^{-1}T_{1}^{-1}T_{2}T_{1}\ket{\Psi}=\exp(2i\theta)\ket{\Psi}\implies T_{2}T_{1}\ket{\Psi}=\exp(2i\theta)T_{1}T_{2} \ket{\Psi}   $$
- This gives the relation:
$$T_{2}(T_{1}\ket{\Psi_{\alpha}} )=\exp[i(\alpha+2\theta)](T_{1}\ket{\Psi_{\alpha}} )$$
- Unless $\theta=2\pi n$ (i.e. bosons or fermions), $T_{1}\ket{\Psi_{\alpha}}$ is _orthogonal_ to $\ket{\Psi_{\alpha}}$, meaning the _ground state is degenerate_
- Repeating the procedure $m$ times, one gets the _phase_ $\alpha+2m\theta$ for the $m$th degeneracy

- As _degeneracy cannot be infinite_, $m\theta=n\pi$ for some integer $n$
- In other words, $\theta$ is a _rational multiple_ of $\pi$

- For $\theta=\pi/m$ for integer $m$, there are _at least_ $m$ _orthogonal ground states_
- Assuming _no other degeneracies_ due to _symmetry_ or other characteristics, the _exchange phase_ can be linked to the _ground state degeneracy_
$$\exp(i\theta)=\exp\left( \frac{i\pi}{m} \right) \Longleftrightarrow \text{Torus GSD}=m$$

- This _generalises_ to other manifolds of genus $g=\beta_{1}/2$
- Each hole comes with its own _pair_ of $T_{1,2}^{(q)}$, with $q=1,2\dots g$
- Therefore, without other sources of degeneracy:
$$\exp(i\theta)=\exp\left( \frac{i\pi}{m} \right) \Longleftrightarrow \text{GSD}=m^{g}$$

# Chern-Simons theory
- Consider a Lagrangian in 2+1D
$$L=L_{0}+\int  d^2x\,\mathcal{L} $$
- The extra term, with 2+1 component _Chern-Simons field_ $a$, consists of a _Lagrangian density_ term and a _coupling term_ due to current
$$\mathcal{L}=\mathcal{L}_\text{CS}-j^{\alpha}a_{\alpha} \qquad \mathcal{L}_\text{CS}=\frac{\kappa}{2}\epsilon^{\alpha\beta\gamma}a_{\alpha}\partial_{\beta}a_{\gamma}\equiv \frac{\kappa}{2}a(\varepsilon\partial a)$$
- $\kappa$ is the _Chern-Simons field parameter_

- The _current_ from $N$ _particles_ with positions $\boldsymbol{x}_{l}$ and charge $q_{l}$
$$\displaylines{j^{0}= \sum_{l=0}^{N}q_{l}\,\delta(\boldsymbol{x}-\boldsymbol{x}_{l})\qquad \boldsymbol{j}= \sum_{l=0}^{N}q_{l} \boldsymbol{\dot{x}}_{l}\,\delta(\boldsymbol{x}-\boldsymbol{x}_{l})\\ \partial_{\alpha}j^{\alpha}=0}$$
- For $a_{0}=\phi$, $\boldsymbol{a}=\boldsymbol{A}$, this recreates the expected _electromagnetic Lagrangian_

- The Lagrangian is _gauge symmetric_
	- Using $\varepsilon\partial\partial=0$ and flux conservation
	- There are _total derivative_ terms in $\delta \mathcal{L}$, which _vanish_ when $j^{0}(t_{i})=j^{0}(t_{f})=0$ on a _closed spatial manifold_
$$a_{\alpha}\to a_{\alpha}+\partial_{\alpha}\Lambda\implies \delta L=0$$
- Thus, $a$ can be interpreted as a _gauge field_

## Flux attachment
### Classical approach
- Take some _variation_ in $a$:
$$a_{\alpha}\to a_{\alpha}+\delta a_{\alpha}$$
- The _equation of motion_ (can also be obtained from Euler-Lagrange equations):
$$j=\kappa\varepsilon\partial a$$
- The zeroth component:
$$j^{0}=\kappa\varepsilon^{0\alpha\beta}\partial_{\alpha}a_{\beta}\equiv\kappa b$$
- This can be thought of as being due to some _magnetic field_ $b$
	- A _curl_ of the spatial components of $a_{\beta}$

- _Integrating_ this over some area $x_{l}$:
$$q_{l}=\kappa \Phi_{l}\implies \Phi_{l}=\frac{q_{l}}{\kappa}$$
- Then, from conservation, the _spacelike components_:
$$\partial_{0}j^{0}=-\partial_{k}j^{k}=-\partial_{k}(\kappa\varepsilon^{k{0}l}\partial_{0}a_{l})\implies j^{k}=\kappa\varepsilon^{k0l}\partial_{0}a_{l}+\kappa\varepsilon^{kl0}\partial_{l}\chi$$
- Here, $\chi$ is an _arbitrary function_

- Since $j^{k}$ must be _gauge invariant_, $\chi$ must _transform_ as $\chi+\partial_{0}\Lambda$
- One can then identify $\chi$ with $a_{0}$:
$$j^{k}=\kappa\varepsilon^{k\beta\gamma}\partial_{\beta}a_{\gamma}$$
### Quantum approach
- The path integral, which integrates over all $a_{\mu}$:
$$\int  \mathcal{D}a\,\exp\left( \frac{i}{\hbar}S[a_{\alpha}] \right) $$
- Consider only terms with an $a_{0}$ component:
$$\mathcal{L}_\text{CS}=\kappa a_{0}b+\frac{\kappa}{2}\varepsilon^{\alpha0\beta}a_{\alpha}\partial_{0}a_{\beta}+\partial_{\beta}(\dots)$$
- The second term is the part of $\mathcal{L}_\text{CS}$ that remains when $a_{0}\to 0$

- Dropping the total derivative, and accounting for _coupling_, one gets:
$$S[a_{0}]=\int  d^3x\,a_{0}(\kappa b-j^{0}) $$
- The relevant bit of the path integral:
$$\int  \mathcal{D}a_{0}\exp\left( \frac{i}{\hbar}S[a_{0}] \right) $$
- This becomes a _delta function_ $\delta(\kappa b-j^{0})$

- This enforces _flux attachment_ as a _constraint_ in the path integral

### The braiding phase
- Given the _attached flux_ $\Phi_{l}=q_{l}/\kappa$
- The _classical_ calculation:
$$\exp(2i\theta_{kl})=\exp\left( \frac{i}{\hbar}[q_{l}\Phi_{k}+q_{k}\Phi_{l}] \right)$$

- When calculating the _braiding phase_ in the _path integral_ formulation, one needs to take into account the _remaining part of the path integral after flux attachment_

- After _enforcing_ the $a_{0}$ path integral as a constraint, the remaining _effective Lagrangian_ is:
$$\mathcal{L}_\text{CS}(a_{0}\to 0)=\frac{\kappa}{2}\varepsilon^{\alpha0\gamma}a_{\alpha}\partial_{0}a_{\gamma}-a_{\alpha}j^{\alpha}=-\frac{1}{2}a_{\alpha}j^{\alpha}$$

- Therefore, the effective _magnetic field_ is _halved_, giving:
$$\theta_{kl}=\frac{q_{l}q_{k}}{2\hbar\kappa}$$

## Gauge invariance and quantisation
- In the presence of a "matter" field $\psi$ along with the _gauge field_ $a_{\alpha}$:
$$\psi\to \exp\left( \frac{i}{\hbar}q_{0}\Lambda \right)\psi$$
- If all fields have some _integer multiple_ of $q_{0}$ as their charge, $a_{\alpha}$ is a _compact field_

### Quantisation of charge
- Consider the action from _encircling_ charge $q$ over the _contractible loop_ $\gamma^{j}$ of a torus, with the loop circumfrence $L$
$$S_\text{curr}=q\int  dt\,\dot{x}^{j}a_{j}=q\int  d\gamma^{j}\,a_{j}=q \oint d \boldsymbol{\gamma}\cdot \boldsymbol{a} $$
- Under some _gauge transformation_ with $\Lambda$, for $\psi$ to be _single-valued_ at every point along the loop:
$$\Lambda(x+L)=\Lambda(x)+\frac{2\pi \hbar}{q_{0}}$$
- The corresponding _change in action_:
$$S\to S+q \int  d \boldsymbol{\gamma}\cdot \nabla\Lambda=S+2\pi \hbar \frac{q}{q_{0}} $$

- _Gauge invariance_ requires that $\exp(iS/\hbar)$ is gauge invariant
	- The action itself does not need to be gauge-invariant, only the _path integral_ needs to be

- Therefore, $q$ is _quantised_ in units of $q_{0}$

### Quantisation of monopole charge/flux
- Consider a _closed orientable manifold_ $\mathcal{M}$ as the _union_ of two single-connected patches $P_{1,2}$
- They share the _same boundary_ with _opposite orientations_ $\partial P_{1}=-\partial P_{2}$

- Define $\boldsymbol{a}_{1,2}$ as _smooth functions on patches_ $P_{1,2}$
- Integrate the _flux_, then using _Stokes theorem_:
$$\int_{\mathcal{M}}d^{2}x\,b =\sum_{J=1,2}\int_{P_{J}}  d^{2}x\,b=\sum_{J} \oint_{\partial P_{J}}d\boldsymbol{l}\cdot \boldsymbol{a}_{J}=\oint_{\partial P_{1}}d\boldsymbol{l}\cdot(\boldsymbol{a}_{1}-\boldsymbol{a}_{2})  $$
- This can only be _non-zero_ iff $\boldsymbol{a}_{1}-\boldsymbol{a}_{2}\neq 0$ on $\partial P_{1}$
- As they _both_ describe the same function, they are _related by gauge transformation_
$$\boldsymbol{a}_{1}=\boldsymbol{a}_{2}+\nabla\Lambda$$
- From the same _single-valued_ constraint of $\psi$:
$$\int_{\mathcal{M}}d^{2}x\,b=\oint_{\partial P_{1}}d\boldsymbol{l}\cdot \nabla\Lambda=\frac{2\pi \hbar}{q_{0}} n=n\Phi_{0}$$
- $\Phi_{0}$ is the _flux quantum_ $2\pi \hbar/q_{0}$
### Quantisation of field parameter $\kappa$
- Suppose the system is on a _closed orientable manifold_ $\mathcal{M}$
- Integrating the flux attachment over the manifold:
$$\kappa \int  d^2x\,b=\int_{\mathcal{M}}d^{2}x\,j^{0}  =\kappa n\Phi_{0}$$
- As the flux is _quantised_, the _overall charge_ must also be quantised as $mq_{0}$
$$\kappa n\Phi_{0}=mq_{0}$$
- The _smallest nonzero allowed_ $m$ comes from _one flux quantum_ $\Phi_{0}$

- For this to be consistent, $\kappa$ is also _quantised_
$$\kappa=\frac{mq_{0}}{\Phi_{0}}=\frac{q_{0}^{2}}{2\pi \hbar}m$$
- $m$ is the _Chern-Simons level_, the _number of charges_ corresponding to a _single flux quantum_ $\Phi_{0}$

- The _exchange phase_ is then:
$$\theta=\frac{q_{0}^{2}}{2\hbar\kappa}=\frac{\pi}{m}$$

### Chern-Simons and ground state degeneracy
## Many particle types and matrix C-S Theory
- The Chern-Simons field is now a _vector of gauge fields_, for $I=1,\dots M$
$$a_{I\alpha}$$
- For simlicity, set the _fundamental charges_ to unity:
$$q_{I0}=1$$

- The Lagrangian can be _generalised_:
$$\mathcal{L}=\mathcal{L}_\text{CS}-\sum_{I=1}^{M} j^{\alpha}_{I}a_{I\alpha} $$

- The Chern-Simons density is now encoded using a _matrix_:
$$\mathcal{L}_\text{CS}=\frac{1}{4\pi \hbar}\sum_{I,J}K_{IJ}a_{I}(\varepsilon\partial a_{J})\qquad K_{IJ}=K_{JI}$$
- Generalising the proofs above, the _encircling phase_ between _composite particles_ with charges $\boldsymbol{q}=(q_{1},\dots q_{M})$ and $\boldsymbol{q}'=(q'_{1},\dots q_{M}')$
	- The single particle case has $K=m$
$$\theta_{\boldsymbol{q}\boldsymbol{q}'}=\pi \boldsymbol{q}'K^{-1}\boldsymbol{q}$$

- The ground state degeneracy can be expressed as:
$$\text{GSD}=|\det K|^{g}$$
- On the _surface code_, as they are _mutual semions_:
$$K_\text{surf}=\pmatrix{0&2 \\2&0}\implies \text{GSD}=4^{g}$$
# Topological phases
- The _perturbed surface code_:
$$H=-J\sum_{v}A_{v}-J\sum_{p}B_{p}+\delta H \qquad \delta H=h\sum_{j}O_{j}$$

- Conditions of the perturbation:
	- 

- The surface code is _gapped_
- The perturbation will _split_ the degenerate levels
## Robustness of ground state degeneracy
- From [[#Brillouin-Wigner perturbation theory]]

- The _ground subspace_ $S$ 
- Eigenstates labelled by _vertex and plaquette eigenvalues_, and $\prod Z_{i}$ over _noncontractible loops_
$$\ket{n}=\ket{\{a_{v},b_{p}\},\{\bar{z}_{j}\}}  $$

- Take $O=Z_{j}$ such that $Z_{j}$ are still _quantum numbers_ one can label states by
	- Results below will _generalise_ to more general perturbations

- See which $\braket{ |\delta HG\dots |  }$ terms contribute to perturbed energies

- First contribution: a $\bar{z}_{j}$ _independent_ shift

- Second contribution: the _ground state degeneracy splits_

- Spltting _exponentially decays_

- Result _generalises_ to _any local perturbation_

### Comparison to the [[#Transverse field Ising model (TFIM)]]

- Requires _no symmetry breaking_, as the result only depends on _topological order_

## Topological order
- Consider a 2D _local Hamiltonian_
$$H=$$
- It has _topological order if_:
	1. $H$ is _gapped_
	2. It has a _topological ground state degeneracy_
	3. For any _locally supported operator_ $A$, the ground states $\ket{\psi_{j}}$ satisfy
$$\braket{ \psi_{j}|A | \psi_{j'} } =$$
- The latter should hold up to $\exp(-cL),c>0$ where $L$ is the _shortest circumfrence of a noncontractible loop_

## Topological order as a phase
- A _phase_ of matter can be defined as some _region_ $\mathcal{R}$ in _parameter space_, in the _thermodynamic limit_, there is some set of features which are _constant everywhere_ in $\mathcal{R}$

- Features must be robust against _local perturbation_

### Equivalence class of Hamiltonians
- Two _gapped local Hamiltonians_ $H_{0}$ and $H_{1}$ belong to the _same topological phase_ if and only if they can be _continuously deformed_ into each other _without closing the gap_

- Argument: 

### Equivalence class of states
- $\ket{\psi_{0}}\sim \ket{\psi_{1}}$ if they are _both ground states_ of _gapped, local Hamiltonians_ $H_{0},H_{1}$ where $H_{0}\sim H_{1}$

- Alternatively, one can define $\ket{\psi_{0}}\sim \ket{\psi_{1}}$ iff $\ket{\psi_{1}}=U\ket{\psi_{0}}$ where $U$ is a _local unitary_

- A _local unitary_ $U$ are operators _for which_ there exist $U_{i}=\prod_{j}W_{j}^{(i)}, i=1,2$ with unitary $W_{j}^{(i)}$ satisfying $\mathrm{diam}[\mathrm{supp}(W_{j}^{(i)})]=l<\infty$, and $\mathrm{supp(W_{j}^{(i)})}$ _non-overlapping_ for $j~=j'$ for a given $i$, such that $U=U_{2}U_{1}$ up to _corrections_ exponentially decaying with $l$

- In other words, $U$ can be expressed as a _two-layer local quantum circuit_ up to corrections exponentially decaying with the diameter $l$ _of the gates_
![[Local unitary circuit.png]]

- These two definitions of _state equivalence_ are the _same_, given one can have _quasilocal Hamiltonians_:
$$\displaylines{H=\sum_{j}c_{j}O_{j} \\ O_{j}\text{ bounded, } c_{j}\propto \exp(-\alpha _{j}\,\mathrm{diam}[\mathrm{supp}(O_{j})]), \, 0<\alpha_{j}=\text{const.}}$$
- In other words, a _quasilocal_ $H$ can have terms with _support of any diameter_, as long as the _coefficients decay exponentially_ with diameter

## Robustness of braiding statistics