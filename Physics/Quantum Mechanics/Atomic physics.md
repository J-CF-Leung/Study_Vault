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

- The _eigenfunctions_ can be characterised as $\ket{nlm_l}$
	- Atoms can still be said to have _subshells_ and _orbitals_
- However, states of _same_ $n$ and _different_ $l$ are _no longer degenerate_
	- $\hat{H}_0'$ is _not purely_ $1/r$
- States of _higher_ $l$ tend to be _further out_ and hence have _higher energy_

### Self-consistent field approach
- $U(r)$ depends on the _wave functions of all electrons_
- One can make an _initial guess_ for $U(r)$ by taking a _smooth function_ between limits:
$$U(r)\approx\begin{cases}0 &r\to0 \\ (Z-1)e^2/(4\pi\epsilon_0r)&r\to\infty \end{cases}$$
- For $r\to0$, the other electrons effectively have an _isotropic_ repulsion around the electron
- For $r\to\infty$, the other electrons are effectively _at the origin_

- Then solve for:
$$\hat{H}_0'\ket{nlm}=E_{nlm}\ket{nlm}$$
- Estimate the _ground state_ by _filling levels with electrons_

- Using this, obtain the _charge density_:
$$\rho(\bm{r})=e\sum|\psi_{nlm}(\bm{r})|^2$$
- Then use _Gauss' Theorem_ to obtain the _electric field_
- Using that, obtain a _better estimate of $U(r)$

- Repeat solving the Schrodinger equation then _iterate until convergence_

### Hartree-Fock approach
- Assume the overall wave-function is a [[Identical Particles#Slater determinants|Slater determinant]]:
$$\psi=\frac{1}{\sqrt{N!}}\begin{vmatrix}\psi_1(\bm{r}_1)&\psi_1(\bm{r}_2)&\cdots&\psi_1(\bm{r}_N) \\ \psi_2(\bm{r}_1)&\psi_2(\bm{r}_2)&\cdots&\psi_2(\bm{r}_N) \\ \vdots &\vdots  &\ddots&\vdots \\ \psi_N(\bm{r}_1)&\psi_N(\bm{r}_2)&\cdots&\psi_N(\bm{r}_N) \end{vmatrix}$$
- Here, $\psi_k(\bm{r}_i)$ denotes the wavefunction for electron $i$, with _set of quantum numbers_ $n,l.m$ denoted by $k$

### Radial electron densities
![[Electron densities.png]]
- There are _wide peaks_ for contributions from each _shell_
	- The _subshells_ have slightly _different peak positions_
- Each _peak_ gets _further away from the core_ as $n$ increases

### Energies
- One finds that energies are ordered according to values of _increasing_ $n+l$
- There is also a _large jump_ in energy for new values of $n$

- This leads to the _Aufbau principle_:
![[Aufbau principle.png]]

- This sequence gives the _ground state configurations_ of multi-electron atoms
	- There can be _exceptions_ (e.g. copper)
- The _outermost electrons_ give rise to chemical activity
	- Elements with _same number of outer electrons_ (groups) have _similar properties_
## Electron configurations
- Only stating _subshell occupation_ will _not fully specify_ the ground state
- The _orbital and spin_ angular momenta can _combine_ in different ways, and some are _forbidden_

### Two electrons
- For _two-electron configurations_ where the electrons are in _separate subshells_:
	1. $L=l_1+l_2,l_1+l_2-1,\dots |l_1-l_2|$
	2. $S=0,1$
	3. $J=l_1+l_2+1,l_1+l_2,\dots |l_1-l_2-1|$
- Example: $(2p)(3p)$:
	1. $L=0,1,2$
	2. $S=0,1$
	3. $J=3,2,1,0$
	- Term symbols: $$^1\text{S}_0\;\;^1\text{P}_1\;\;^1\text{D}_2\;\;^3\text{S}_1\;\;^3\text{P}_{0,1,2}\;\;^3\text{D}_{1,2,3}$$

- For _two-electron configurations_ where the electrons are in _the same subshell_, there are _restrictions_ as the wavefunction is _overall antisymmetric_
- For a _symmetric spin_ wavefunction, the _spatial wavefunction_ must be _antisymmetric_ and have an _odd_ value of $L$
	- And vice versa

- Example: $(2p)^2$:
	- For $S=0$ (singlet, antisymmetric), $L=0,2$ hence $J=0,2$
	- For $S=1$ (triplet, symmetric), $L=1$, hence $J=0,1,2$
	- Term symbols:
	$$^1\text{S}_0\;\;^1\text{D}_2\;\;^3\text{P}_{0,1,2}$$

### More electrons
- For _full subshells_, $S=L=J=0$
- If there is _one vacancy_, as the other electrons have to obey the _Pauli exclusion principle_, it _acts as an electron_
- For $m$ vacancies, it has the _same energy levels as $m$ electrons_
- Example:
	- $(2p)^5$: one electron, same as $(2p)^1$, term $^2\text{P}_{1/2,3/2}$
	- $(2p)^4$: two electrons, same as $(2p)^2$

- The most _general_ way to find energy levels is to _tabulate all possibilities_ that follow Pauli's Exclusion Principle and give _ladders_ of distinct $J$

### Maximal spin states and half-filled shells
- Often, only the state of _maximum spin_ is of interest
- In this case, all electrons have the _same spin state_, hence must have _all different orbital angular momenta_

- From this, one deduces that for _half-filled shells_, $L=0$
- Example: $(2p)^3$
	- $L=0$, $S=J=3/2$
	- $^4\text{S}_{3/2}$

## Coupling schemes
- The _coupling schemes_ of operators describes what _quantum numbers_ can describe the _system_

- In $L-S$ (Russel-Saunders) coupling, states are described with numbers $L,S,J$
- One _constructs total_ $L$ and $S$ from _individual_ $l$ and $s$ before computing $J$
$$\hat{\bm{L}}=\sum_i\hat{\bm{L}}_i\hspace{1cm}\hat{\bm{S}}=\sum_i\hat{\bm{S}}_i\hspace{1cm}\hat{\bm{J}}=\hat{\bm{L}}+\hat{\bm{S}}$$
- Alternatively, for the $j-j$ coupling scheme, one _constructs individual_ $j$ from $l$ and $s$ first:
$$\hat{\bm{J}}_i=\hat{\bm{L}}_i+\hat{\bm{S}}_i\hspace{1.5cm}\hat{\bm{J}}=\sum_i\hat{\bm{J}}_i$$

- Example: The [[#Two electrons|(2p)(3p) electron configuration]]:
$$j_1=j_2=1\otimes\frac{1}{2}=\frac{1}{2},\frac{3}{2}\hspace{1.5cm}j=j_1\otimes j_2=0,1,2,3$$

- The _accuracy_ of the coupling schemes depends on the _terms of the Hamiltonian_ which the quantum numbers _commute_ with

### Commuting with interaction terms
- Consider the _electron-electron repulsion term_:
$$\hat{H}_1=\sum_{i>j}\frac{e^2}{4\pi\epsilon_0r_{ij}}$$
- $r_{ij}$ is _not rotationally invariant_ w.r.t. $\hat{\bm{L}}_i$ and $\hat{\bm{L}}_j$
- However, it is _rotationally invariant_ w.r.t. $\hat{\bm{L}}$, hence it must _commute_ with it

- Consider the _spin-orbit term_:
$$\hat{H}_2=\sum_i\xi_i(r_i)\hat{\bm{L}}_i\cdot\hat{\bm{S}}_i$$

- Using the [[The hydrogen atom#Spin-orbit commutation relations|spin-orbit commutation relations]], for _single-electron operators_:
$$\displaylines{[\hat{\bm{L}}_i\cdot\hat{\bm{S}}_i,\hat{\bm{L}}_i^2]=[\hat{\bm{L}}_i\cdot\hat{\bm{S}}_i,\hat{\bm{S}}_i^2]=[\hat{\bm{L}}_i\cdot\hat{\bm{S}}_i,\hat{\bm{J}}_i^2]=0 \\ [\hat{\bm{L}}_i\cdot\hat{\bm{S}}_i,\hat{\bm{L}}_i]=-[\hat{\bm{L}}_i\cdot\hat{\bm{S}}_i,\hat{\bm{S}}_i]\neq0 \hspace{1.5cm} [\hat{\bm{L}}_i\cdot\hat{\bm{S}}_i,\hat{\bm{J}}_i]=0}$$
- Hence, the _spin-orbit term_ will _only commute_ with $\hat{\bm{L}}_i^2,\hat{\bm{S}}_i^2, \hat{\bm{J}}_i, \hat{\bm{J}}$

![[Coupling scheme commutation.png]]

### Light atoms
- For _light_ atoms, $\mean{\hat{H}_1}\gg\mean{\hat{H}_2}$
	- Example: [[#The helium atom]]
- The energy correction due to _repulsion_ is much stronger than that due to _spin-orbit coupling_
- Spin-orbit coupling is treated as a _perturbation_
- For $\hat{H}_0+\hat{H}_1$, as $\hat{\bm{L}},\hat{\bm{S}},\hat{\bm{J}}$ _commute_, then $L,S,J$ are _good quantum numbers_
- Hence, $L-S$ coupling is used

### Heavy atoms
- The energy from [[The hydrogen atom#Spin-orbit correction|spin-orbit coupling]] scales as:
$$\mean{\hat{H}_2}\sim Z^4$$
- Hence for _heavy atoms_, electron-electron _repulsion_ is the _perturbation_
- In this case, the $j_i$ are _good quantum numbers_
- Hence, $jj$ coupling is used
## Hund's rules
- Assume $L-S$ coupling
- Then _Hund's Rules_ give the _ordering of energy levels_ for a _given_ [[#Electron configurations|electron configuration]]
	- They are _empirical_

1. The _largest_ allowed value of $S$ gives the _lowest energy_
2. For a _given_ $S$, the _largest_ $L$ gives the _lowest energy_
3. For a _given_ $S$ and $L$:
	- If a subshell is _less than half-full_, the _lowest_ $J$ is lowest in energy
	- If a subshell is _more than half-full_, the _highest_ $J$ is lowest in energy

- A _high_ $S$ gives a _highly symmetric spin wave-function_, hence a highly _antisymmetric spatial wave function_
- On _average_, electrons are then _more far apart_

- Similarly, _maximising_ $L$ also keeps electrons apart

- The mini/maximising of $J$ originate from _fine structure_

### Lande interval rule
- From [[Symmetries in quantum mechanics#The Wigner-Eckart Theorem for scalars|the Wigner-Eckart Theorem]], one can get:
$$\Braket{Jm_JLS|\sum_i\xi_i(r_i)\hat{\bm{L}}_i\cdot\hat{\bm{S}}_i|Jm_JLS}=\zeta(L,S)\Braket{Jm_JLS|\hat{\bm{L}}\cdot\hat{\bm{S}}|Jm_JLS}$$
- The _sign_ of $\zeta(L,S)$ _flips_ depending on if the subshell is _more/less than half-filled_

- From this, for _constant_ $L$ and $S$, one gets:
$$E_J-E_{J-1}\propto J$$
- This is the _Lande interval rule_

### Exceptions
- For _excited states_, the rules can occasionally be violated
	- Mainly in the _ordering_ of $J$
- In the $(2s)^1(2p)^1$ excited state of _helium_ has $J=2$ in the _ground state_
	- Due to _"spin-other spin"_ and other such interactions $(\hat{\bm{S}}_1\cdot\hat{\bm{S}}_2,\hat{\bm{L}}_1\cdot\hat{\bm{S}}_2\dots)$

- When a shell is _half full_, the ordering is _not always obeyed_
## jj coupling
- The effect of _electron-electron repulsion_ as a _perturbation_ is to _split_ the levels
	- Analagous to spin-orbit coupling in $L-S$ coupling

# Atomic spectra

# Zeeman effect
- When an $N-$electron atom is placed in an _external magnetic field_ $\bm{B}$, the _contributions_ to the Hamiltonian:
$$\hat{H}_B=-\hat{\bm{\mu}}_L\cdot\hat{\bm{L}}-\hat{\bm{\mu}}_S\cdot\hat{\bm{S}}=\frac{\mu_B}{\hbar}(\hat{\bm{L}}+g_e\hat{\bm{S}})\cdot\bm{B}$$
- Here, $\hat{\bm{L}}$ and $\hat{\bm{S}}$ are the _total angular momenta_:
$$\hat{\bm{L}}=\sum_{i=1}^N\hat{\bm{L}}_i\hspace{1.5cm}\hat{\bm{S}}=\sum_{i=1}^N\hat{\bm{S}}_i$$
- Orienting $\bm{B}$ along the $z-$axis:
$$\hat{H}_B=(g_L\hat{L}_z+g_S\hat{S}_z)B_z$$
- The resulting energy correction is of the _order_ $6\times 10^{-5} (B/\text{T})\,\text{eV}$
	- _Small_ relative to atomic binding energies, hence first-order perturbation theory applies


