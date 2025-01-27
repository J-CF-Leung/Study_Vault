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