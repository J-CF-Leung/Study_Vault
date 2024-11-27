# Floquet physics in a non-orthogonal basis
- Basis states:
$$\displaylines{\ket{e_{\mu}}=c^{\dagger}_{\mu}\ket{0}\\ \braket{ \boldsymbol{r} |e_{\mu}(t)  }=\phi_{\mu}(\boldsymbol{r},t)=\phi_{\mu}(\boldsymbol{r}-\boldsymbol{R}(t)) }$$
- Dual basis and metric:
$$\displaylines{\braket{ e^{\mu}| e_{\nu} }=\delta^{\mu}_{\nu}  \\ S_{\mu \nu}=\braket{ e_{\mu} |e_{\nu}  } }$$
- Floquet's theorem, with _Floquet basis_ $\ket{\tilde{e}_{\mu}(t)}$
$$\displaylines{H(t+T)=H(t) \\ H(t)=\sum_{m}\exp(-im\omega t)H^{(m)} \\ \ket{e_{\mu}(t)}=\exp\left( -\frac{i\varepsilon_{\mu}t}{\hbar} \right)\ket{\tilde{e}_{\mu}(t)} \\ \ket{\tilde{e}_{\mu}(t)}=\sum_{m}\exp(-im\omega t)\ket{\tilde{e}_{\mu}^{(m)}}\rangle   }$$
- The states $\ket{\tilde{e}_{\mu}^{(m)}}\rangle$ satisfy:
$$(\varepsilon_{\mu}+m\hbar\omega)\ket{\tilde{e}_{\mu}^{(m)}}\rangle=\sum_{m'}H^{(m-m')}\ket{\tilde{e}_{\mu}^{(m')}}\rangle$$

## Change of basis to Floquet states
$$\ket{e_{\mu}}=\exp(-i\varepsilon_{\mu}t)\ket{\tilde{e}_{\mu}}  \qquad \bra{e^{\mu}}=\bra{\tilde{e}^{\mu}}\exp(i\varepsilon_{\mu}t)  $$
- From the definition of the dual basis:
$$\braket{ e^{\mu} | e_{\nu} }=\braket{ \tilde{e}^{\mu} | \tilde{e}_{\nu} }=\delta^{\mu}_{\nu}  $$
- One can define the _change of basis_ matrices:
$$\braket{ \tilde{e}^{n} | e_{\mu} }=\delta^{n}_{\mu}\exp(-i\varepsilon_{\mu}t) \equiv{A^{n}}_{\mu } \qquad \braket{ e^{\mu} | \tilde{e}_{n} }=\delta^{\mu}_{n}\exp(i\varepsilon_{\mu}t) \equiv {A^{\mu}}_{n}$$
- The _overlap matrix_:
$$\braket{ e_{\mu} | e_{\nu} }=S_{\mu \nu} \implies \braket{ \tilde{e}_{\mu} |\tilde{e}_{\nu}  } =\exp[-i(\varepsilon_{\mu}-\varepsilon_{\nu})t]S_{\mu \nu} \equiv \tilde{S}_{\mu \nu}$$

- Matrix elements transform as expected:
$${h^{\mu}}_{\nu}=\braket{ e^{\mu}|H | \nu }={A^{\mu}}_{n}{A^{m}}_{\nu}\braket{ \tilde{e}^{n}|H | \tilde{e}_{m} }\equiv {A^{\mu}}_{n}{A^{m}}_{\nu}{\tilde{h}^{n}}_{m} $$

## Second quantisation in a non-orthogonal basis
- From: PhysRevA 43, and Emilio's note

- Second quantisation:
$$\displaylines{c^{\dagger}_{\mu}\ket{0}=\ket{e_{\mu}} \qquad \bra{0}c^{\mu}=\bra{e^{\mu}} \\ c^{\mu}\ket{0}=\bra{0}c^{\dagger}_{\mu}=0  }$$
- Anti-commutation relations:
$$\{c^{\mu},c^{\nu}\}=\{c_{\mu}^{\dagger},c_{\nu}^{\dagger}\}=0 \qquad \{c^{\mu},c^{\dagger}_{\nu}\}=\delta^{\mu}_{\nu}$$
- Raising and lowering:
	- Derived opposite?
$$(c^{\mu})^{\dagger}=S^{\mu \nu}c_{\nu}^{\dagger} \qquad (c_{\mu}^{\dagger})^{\dagger}=S_{\mu \nu}c^{\nu}$$

- Doing a _change of basis_:
$$\tilde{c}_{\mu}^{\dagger}=\exp(i\varepsilon_{\mu}t)c_{\mu}^{\dagger} \qquad \tilde{c}^{\mu}=\exp(-i\varepsilon_{\mu}t)c^{\mu}$$

## Floquet second quantisation in: Rudner & Lidner
- Basis states in Schrodinger picture:
$$\displaylines{\ket{\psi_{\nu}(t)}=\exp\left( -\frac{i\varepsilon_{\nu}t}{\hbar} \right)\ket{\phi_{\nu}(t)}  \\ \ket{\phi_{\nu}(t+T)} =\ket{\phi_{\nu}(t)} }$$
- In the Schrodinger picture, one can define a _creation operator at time $t$_ $c_{\nu}^{\dagger}(t)$, with the _field operator_ $\Psi (\boldsymbol{r})$
	- _Ignore_ the quasi-energy phase factor
$$c_{\nu,S}^{\dagger}(t)=\int  d\boldsymbol{r}\,\phi_{\nu}(\boldsymbol{r},t)\,\Psi ^{\dagger}(\boldsymbol{r}) $$
- For a _non-interacting_ Hamiltonian
	- Hubbard model: Mott insulator as non interacting Hamiltonian?
$$c_{\nu,H}^{\dagger}(t)=\exp[i\varepsilon_{\nu}(t-t_{0})]c^{\dagger}_{\nu}(t_{0})$$
- If Floquet states orthonormal at one point in time:
$$\braket{ \phi_{\mu}(t_{0}) | \phi_{\nu}(t_{0}) }=\delta_{\mu \nu} \implies \{c_{\mu,H}(t),c_{\nu,H}^{\dagger}(t')\}=\exp[-i\varepsilon_{\mu}(t-t')]\delta_{\mu \nu} $$

## Attempt at Floquet non-orthogonal second quantisation
- Assume _one orbital per site_

- Overlap between _site orbitals_:
	- Does this mean there must be hopping...? And it cannot be treated as a perturbation?
$$S_{\mu \nu}(t)=\braket{ e_{\mu}(t) |e_{\nu}(t)  } $$
- Overlap matrix for _Floquet states_:
$$\tilde{S}_{\mu \nu}(t)=\exp[i(\varepsilon_{\mu}-\varepsilon_{\nu})t]S_{\mu \nu}(t)$$
- Anti-commutation relations _hold_:
$$\{\tilde{c}^{\mu},\tilde{c}^{\nu}\}=\{\tilde{c}_{\mu}^{\dagger},\tilde{c}_{\nu}^{\dagger}\}=0 \qquad \{\tilde{c}^{\mu},\tilde{c}^{\dagger}_{\nu}\}=\delta^{\mu}_{\nu}$$