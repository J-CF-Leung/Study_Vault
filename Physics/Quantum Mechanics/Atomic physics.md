- For a _single-electron atom_, see [[The hydrogen atom]]

- Many principles from the single-electron atom can also be applied

# Hydrogen atom selection rules
- Consider an atom _absorbing/emitting a photon_ during a transition:
$$\ket{\alpha}\longleftrightarrow \ket{\beta}+\gamma$$
![[Atomic emission.png]]

- For a _hydrogen atom_, the _rate_ of emission or absorption is proportional to:
$$\Gamma\propto\omega^3|\braket{\alpha|\hat{\bm{d}}|\beta}|^2$$
- Here, $\hat{\bm{d}}$ is the _electric dipole operator_:
$$\hat{\bm{d}}=-e\hat{\bm{r}}$$
- As it is a vector operator, use the [[Symmetries in quantum mechanics#The Wigner-Eckart Theorem for vector operators|Wigner-Eckart Theorem]]
- The [[Symmetries in quantum mechanics#Spatial inversion and parity|parity selection rule]] also applies
	- Eliminates $l_1+l_2$ _even_, meaning $l_1\neq l_2$, and $\Delta l$ is restricted to $\pm1$

- The _electric dipole transition_ is known as the _E1 transition_

- For a given emission or absorption:
$$\displaylines{\ket{n_1l_1m_1}\longleftrightarrow\ket{n_2l_2m_2}+\gamma \\\braket{n_1l_1m_1|\hat{\bm{d}}|n_2l_2m_2}\neq0 \text{ iff} \\ \Delta l=\pm1 \hspace{1cm}l_1+l_2\geq1\hspace{1cm}\Delta m_l=0,\pm1}$$
- There are _no restrictions_ on $\Delta n$
![[Grotrian_H.png]]

- A _special case_:
$$\displaylines{\hat{z}\equiv\hat{r}_0 \\ \braket{n_1l_1m_1|\hat{z}|n_2l_2m_2}\neq0\;\text{ iff} \\ \Delta l=\pm1 \hspace{1cm} l_1+l_2\geq1\hspace{1cm} \Delta m_l=0}$$
## Fine and hyperfine structure
- Include [[The hydrogen atom#Relativistic effects|fine structure]] (accounting for _electron spin_)
- Account for _total angular momentum_ $\hat{\bm{J}}=\hat{\bm{L}}+\hat{\bm{S}}$ in Wigner-Eckart Theorem
	- Parity selection rule _does not apply_
- The previous selection rules _also apply_ as $\hat{\bm{d}}$ is _independent of spin_
	- The Wigner-Eckart Theorem applies to _any vector operator and any angular momentum operator_
$$\displaylines{\Delta j=0,\pm1\hspace{1cm}j_1+j_2\geq1\hspace{1cm}\Delta m_j=0,\pm1 \\ \Delta l=\pm1 \hspace{1cm} l_1+l_2\geq1 \hspace{1cm} \Delta m_l=0,\pm1}$$

- Possible resulting transitions:
	- Example: the Balmer $2\to3$ transition has _two doublets and a triplet_, for 7 lines in total
![[Fine structure transitions.png]]
- As there are _no restrictions_ on $\Delta n$, the transitions can be within the _same shell_

- With _hyperfine_ structure, account for _nuclear spin_:
$$\hat{\bm{F}}=\hat{\bm{L}}+\hat{\bm{S}}+\hat{\bm{I}}$$
- All _previous selection rules_ still apply:
$$\displaylines{\Delta F=0,\pm1\hspace{1cm}F_1+F_2\geq1\hspace{1cm}\Delta m_F=0,\pm1 \\ \Delta j=0,\pm1\hspace{1cm}j_1+j_2\geq1\hspace{1cm}\Delta m_j=0,\pm1 \\ \Delta l=\pm1 \hspace{1cm} l_1+l_2\geq1 \hspace{1cm} \Delta m_l=0,\pm1}$$
- From these rules, the _21cm_ transition $(n=1. |\Delta F|=1, \Delta j=\Delta l=0)$ is _not an electric dipole transition_
	- It is a _magnetic dipole_ transition

- For each _degenerate_ transition (between _degenerate sets of states_), the $\Delta m_j$ selection rule _restricts the number of possible transitions_
	- Between $j=0$ and $j=1$, _all transitions_ are allowed
	- Between $j=1$ and $j=2$, 6 of the 15 possible transitions are _disallowed_ (e.g. $m_j=0\to2$)

# The helium atom
- Assume _no relativistic effects_, or _spin-orbit interactions_
- Ignore _nuclear mass and spin_

- Hamiltonian for the _electrons_:
$$\displaylines{\hat{H}(\bm{r}_1,\bm{r}_2)=-\frac{\hbar^2}{2m_e}(\nabla_1^2+\nabla_2^2)-\frac{e^2}{4\pi\epsilon_0}\left(\frac{Z}{r_1}+\frac{Z}{r_2}-\frac{1}{r_{12}}\right) \\ r_{12}=|\bm{r}_1-\bm{r}_2|}$$
- There is _no analytic solution_

- Strategy:
	- Assume $1/r_{12}$ _does not exist_ (the _zeroth-order_ helium atom)
	- Apply the [[Approximation Methods#Variational method|variational method]]

## The zeroth-order atom
- _Neglect_ the electron-electron repulsion:
$$\hat{H}(\bm{r}_1,\bm{r}_2)=-\frac{\hbar^2}{2m_e}(\nabla_1^2+\nabla_2^2)-\frac{e^2}{4\pi\epsilon_0}\left(\frac{Z}{r_1}+\frac{Z}{r_2}\right)=\hat{H}(\bm{r}_1)+\hat{H}(\bm{r}_2)$$
- The Hamiltonian becomes _separable_
- The _spatial wave-functions_:
$$\displaylines{\hat{H}[\ket{n_1l_1m_1}\ket{n_2l_2m_2}]=(E_1+E_2)\ket{n_1l_1m_1}\ket{n_2l_2m_2} \\ E_1+E_2=-\left(\frac{1}{n_1^2}+\frac{1}{n_2^2}\right)Z^2R_\infty}$$

### Ground state
- The _ground state_ has $n_1=n_2=1$:
$$E_0=-2Z^2R_\infty=-8R_\infty$$
- As electrons are _fermions_, it must be paired with an _antisymmetric_ wave function:
$$\ket{\psi}=\ket{100}\ket{100}\otimes\frac{1}{\sqrt 2}[\ket{\uparrow}\ket{\downarrow}-\ket{\downarrow}\ket{\uparrow}]$$
- This state is _non-degenerate_, with _spin_ $S=0$

### One-electron excited state
- Consider the spatial state:
$$\ket{100}\ket{nlm}$$
- For _parahelium_, $S=0$, and the total state is:
$$\ket{\psi}=\frac{1}{\sqrt{2}}[\ket{100}\ket{nlm}+\ket{nlm}\ket{100}]\otimes\frac{1}{\sqrt{2}}[\ket{\uparrow}\ket{\downarrow}-\ket{\downarrow}\ket{\uparrow}]$$

- For _orthohelium_, $S=1$ and the total state is:
$$\ket{\psi}=\frac{1}{\sqrt{2}}[\ket{100}\ket{nlm}-\ket{nlm}\ket{100}]\otimes\frac{1}{\sqrt{2}}[\ket{\uparrow}\ket{\downarrow}+\ket{\downarrow}\ket{\uparrow}]$$
- The spin wave-function can also be $\ket{\uparrow}\ket{\uparrow}$ or $\ket{\downarrow}\ket{\downarrow}$

- The single-particle excited state of _lowest energy_ has $n_1=1$ and $n_2=2$:
$$E_1=-5R_\infty$$
- The _limit_ to the one-particle excited state is the $\text{He}^+$ ion:
$$E(\text{He}^+)=-4R_\infty$$
- In general, the one-particle excited state has _angular momentum quantum numbers_:
$$\displaylines{L=0,1,2,\dots (n-1) \hspace{1.5cm} S=0,1 \\ J_\text{p}=L \hspace{1.5cm}J_\text{o}=L,L\pm1}$$
![[Helium excited states.png]]
- For the zeroth-order atom, energies are _only dependent on_ $n_1,n_2$
	- _All_ of the excited states are _degenerate_
### Two-electron excited state
- Consider the spatial state:
$$\ket{n_1l_1m_1}\ket{n_2l_2m_2}$$
- The _lowest energy_ two-electron excited state has $n_1=n_2=2$:
$$E_2=-2R_\infty$$
- As this is _higher_ than the energy of $\text{He}^++\text{e}^-$, the atom _auto-ionises_:
$$\text{He}^{**}\longrightarrow\text{He}^++\text{e}^-$$
- The _two-electron excited state_ is _not observed_

## Ground state energy
- Write the Hamiltonian as the _zeroth-order_ terms, and an _interaction term_:
$$\displaylines{\hat{H}=\hat{H}_0+\hat{H'} \\ \hat{H}_0=-\frac{\hbar^2}{2m_e}(\nabla_1^2+\nabla_2^2)-\frac{e^2}{4\pi\epsilon_0}\left(\frac{Z}{r_1}+\frac{Z}{r_2}\right)\hspace{1cm}\hat{H}'=\frac{e^2}{4\pi\epsilon_0 r_{12}}}$$
- The interaction term _cannot be treated as a small perturbation_
- Hence, use the [[Approximation Methods#Variational method|variational method]]
- The _variational parameter_ will be some _effective nuclear charge_ $Z'$
	- Expected: $1<Z'<2$
- The _ground state wave function_ with the parameter:
$$\ket{\psi_\text{trial}(Z')}=\frac{Z'^3}{\pi a_0^3}\exp\left(-\frac{Z'(r_!+r_2)}{a_0}\right)=\ket{\psi_{100}'(Z',r_1)}\ket{\psi_{100}'(Z',r_2)}$$

- From the zeroth-order Hamiltonian:
$$E_1=E_2=\braket{\psi_{100}'|\hat{H}_0|\psi_{100}'}=(Z^2-2ZZ')R_\infty$$
- From the interaction:
$$E_{12}=\frac{e^2}{4\pi\epsilon_0}\int\frac{\exp[2Z'(r_1+r_2)/a_0]}{|\bm{r}_1-\bm{r}_2|}\,d^3\bm{r}_1\,d^3\bm{r}_2$$
- Evaluating the integral:
$$E_{12}=\frac{e^2}{4\pi\epsilon_0}\left(\frac{Z'^3}{\pi a_0^3}\right)^2(20\pi^2)\left(\frac{a_0}{2Z'}\right)^5=\frac{5}{4}Z'R_\infty$$
- _Minimising_ the total energy w.r.t. $Z'$:
$$\displaylines{Z'=Z-\frac{5}{16} \\ E(Z')=-2\left(Z-\frac{5}{16}\right)^2R_\infty\approx 5.695R_\infty=-77.4\,\text{eV}}$$
- It is _way above_ the ground state energy of $-8R_\infty\approx -109\,\text{eV}$

- For _improved estimates_, one can have _more variational parameters_:
$$\psi(s,t,u)=\exp\left(-\frac{k(r_1+r_2)}{2}\right)[1+c_1kr_{12}+c_2k^2(r_1-r_2)^2]$$

## Energy of excited states
- Use [[Approximation Methods#Time-independent perturbation theory|time-independent perturbation theory]]
- The _spatial states_, for _para/orthohelium_:
$$\ket{nlm^{(0)}}=\frac{1}{\sqrt{2}}[\ket{100(\bm{r}_1)}\ket{nlm(\bm{r}_2)}\pm\ket{nlm(\bm{r}_1)}\ket{100(\bm{r}_2)}]$$
- The _first-order energy correction_:
$$\Delta E^{(1)}=\braket{nlm^{(0)}|\hat{H}'|nlm^{(0)}}=\frac{e^2}{4\pi\epsilon_0}\Braket{nlm^{(0)}|\frac{1}{r_{12}}|nlm^{(0)}}$$
- As it is a _matrix element of a scalar operator_, from the [[Symmetries in quantum mechanics#The Wigner-Eckart Theorem for scalars|Wigner-Eckart Theorem]], it is _independent of_ $m$:
$$\Delta E^{(1)}=J_{nl}+K_{nl}$$
- Choosing $m=0$:
$$\begin{aligned}J_{nl}&=\frac{e^2}{4\pi\epsilon_0}\int\int\frac{|\psi_{100}(\bm{r}_1)|^2|\psi_{nlm}(\bm{r}_2)|^2}{|\bm{r}_1-\bm{r}_2|}\,d^3\bm{r}_1\,d^3\bm{r}_2 \\ K_{nl}&=\frac{e^2}{4\pi\epsilon_0}\int\int\frac{\psi^*_{100}(\bm{r}_1)\psi^*_{nlm}(\bm{r}_2)\psi_{100}(\bm{r}_2)\psi_{nlm}^*(\bm{r}_1)}{|\bm{r}_1-\bm{r}_2|}\,d^3\bm{r}_1\,d^3\bm{r}_2\end{aligned}$$
- $J_{nl}$ represents the _electrostatic repulsion_:
$$J_{nl}>0$$
- It is said to _break_ the degeneracy in $l$

- $K_{nl}$ is the _exchange interaction_, and can be shown to be _positive_
![[Helium excited state energies.png]]
- It _breaks_ the degeneracy in $S$
	- For $S=1$, as the spatial state is _antisymmetric_, it is _zero_ at $\bm{r}_1=\bm{r}_2$
	- They tend to be _further apart_, and have _less Coulomb repulsion_

## E1 transitions in helium
- The E1 transition:
$$\ket{\alpha}\longleftrightarrow \ket{\beta}+\gamma$$
- The _rate_ of absorption and emission depends on the _matrix element_:
$$\Gamma\propto\omega^3|\braket{\alpha|\hat{\bm{d}}|\beta}|^2$$
- In this case, the _electric dipole operator_ is:
$$\hat{\bm{d}}=-e\hat{\bm{r}}_1-e\hat{\bm{r}}_2$$
- As the operator _does not involve spin_, one gets the selection rule:
$$\Delta S=0\hspace{1.5cm}\Delta m_S=0$$
- Therefore, _ortho_ and _para_ helium form _separate spectroscopic series_

- Consider the transition:
$$(1s)(nl)\to(1s)(n'l')$$
- Evaluating the _matrix element_, using the _Wigner-Eckart theorem_:
	- Uses _unsymmetrised_ states but are still part of the _actual_ element $\braket{\beta|\hat{\bm{d}}|\alpha}$
$$\braket{100;n'l'm'|\hat{\bm{d}}|100;nlm}=-e\braket{n'l'm'|\hat{\bm{r}}_2|nlm}$$
- One then gets the selection rule:
$$\Delta l=\pm1, \hspace{1.6cm}\Delta m_l=0,\pm1$$
- Then _para-/ortho-helium_ will each _recreate_ the _hydrogen spectrum_

- The $(1s)(2s)$ state in each system have _no E1 decays_, and are _metastable_
	- $S=0$, _two_ photons are emitted with timescale $\sim 20\,\text{ms}$
	- $S=1$, it _violates_ the $\Delta S=0$ rule with timescale $\sim 8000s$

## Fine structure
- For _parahelium_, there is _no fine structure splitting_ as $S=0$

- For _orthohelium_:
$$J=L\otimes 1=\begin{cases}L,L\pm1&L\geq1 \\ L&L=0\end{cases}$$
- Each $L$ is _split_ into _separate levels_

- From the Wigner-Eckart theorem, the selection rules:
$$\Delta J=\pm1\hspace{1cm}J_\alpha+J_\beta\geq1\hspace{1cm}\Delta m_J=0,\pm1$$
- For $S=0$, they must necessarily all be _singlets_

- For $S=1$, the transition lines must be _multiplets_
	- Transitions _to the lowest energy state_ are _triplets_
	- _Other_ transitions are _sextuplets_ due to the selection rules

# Multi-electron atoms
- The _principal contributions_ to a Hamiltonian:
$$\displaylines{\hat{H}=\hat{H}_0+\hat{H}_1+\hat{H}_2 \\ \hat{H}_0=\sum_{i=1}^N\left[-\frac{\hbar^2}{2m}\nabla_i^2-\frac{Ze^2}{4\pi\epsilon_0r_i}\right]\hspace{1cm}\hat{H}_1=\sum_{i<j}^N\frac{e^2}{4\pi\epsilon_0r_{ij}}\hspace{1cm}\hat{H}_2=\sum_{i=1}^N\xi_i(r_i)\hat{\bm{L}}_i\cdot\hat{\bm{S}}_i}$$
- _Electron-electron repulsion_ as well as _spin-orbit coupling_ become _significant_

- Other terms such as _relativistic corrections_ can be taken as _perturbations_

## Full subshells
- The _hydrogen-like Hamiltonian_ possesses _eigenstates_, which are _products_ of $N$ _single-particle states_ $\ket{nlm_l}\ket{sm_s}$
- The _energies and degeneracies_:
$$E_n=-\frac{Z^2}{n^2}\hspace{1.5cm}g_n=2n^2$$
- As they are _identical particles_ and _fermions_, they must obey the [[Identical Particles#Particle exchange, fermions and bosons|Pauli Exclusion Principle]], hence _each electron occupies a different state_

- For a _full subshell_ of angular momentum $l$, the $2(2l+1)$ electrons occupy _different states_
	- There is _only one totally antisymmetric state_, given by the _Slater determinant_
	- Every one of the terms has $m_J=m_L=m_S=0$
- Hence, a _full subshell_ has _no angular momentum_

- It is _not possible_ to fill the subshell with _more_ than $2(2l+1)$ electrons
- The _overall charge distribution_ is _isotropic_:
$$\sum_{m_l=-l}^l|Y_{lm_l}(\theta,\phi)|^2=\text{const.}$$

- Hence, the _total angular momentum_ of a multi-electron atom is _only determined by the outer/valence shell_

- Atoms with _full shells_ are said to be _particularly stable_
	- With _one more electron_, the atom would be _much less tightly bound_
![[Ionisation energies.png]]
- The $Z-$dependence is _weaker_ than $Z^2$ due to _screening_ of electric charges

- There are _additional stabilities_ due to _electron-electron repulsion_

## Central field approximation
- The electron-electron repulsion $\hat{H}_1$ is _too large to be treated as a perturbation_
- Instead, assume repulsion force on electron $i$ results from a _spherically symmetric potential_ $U_i(r_i)$
- Then _repartition_ $\hat{H}_0+\hat{H}_1$:
$$\displaylines{\hat{H}=\hat{H}_0'+\hat{H}_1' \\ \hat{H}_0'=\sum_{i=1}^N\left[-\frac{\hbar^2}{2m}\nabla_i^2-\frac{Ze^2}{4\pi\epsilon_0r_i}+U_i(r_i) \right] \\ \hat{H}_1'=\sum_{i<j}\frac{e^2}{4\pi\epsilon_0r_{ij}}-\sum_{i=1}^NU_i(r_i)}$$

- $\hat{H}_0'$ contains _most inter-electron repulsion_
- $\hat{H}_1'$ is the _residual Coulomb interaction_, which can be interpreted as a _perturbation_

- For $\hat{H}_0'$, it creates $N$ _separable single-particle wavefunctions_:
$$\left[-\frac{\hbar^2}{2m}\nabla_i^2-\frac{Ze^2}{4\pi\epsilon_0r_i}+U_i(r_i)  \right]\Phi_i=E_i\Phi_i$$

- The _eigenfunctions_ can be characterised as $\ket{nlm}$
- 
 
## Electron configurations

## Coupling schemes

## Hund's rules

## jj coupling

# Atomic spectra

# Zeeman effect
- When an $N-$electron atom is placed in an _external magnetic field_ $\bm{B}$, the _contributions_ to the Hamiltonian:
$$\hat{H}_B=\frac{e}{2m_e}(\hat{\bm{L}}+g_e\hat{\bm{S}})\cdot\bm{B}$$
- Here, $\hat{\bm{L}}$ and $\hat{\bm{S}}$ are the _total angular momenta_:
$$\hat{\bm{L}}=\sum_{i=1}^N\hat{\bm{L}}_i\hspace{1.5cm}\hat{\bm{S}}=\sum_{i=1}^N\hat{\bm{S}}_i$$