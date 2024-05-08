- For a _single-electron atom_, see [[The hydrogen atom]]

- Many principles from the single-electron atom can also be applied

# Hydrogen atom selection rules
- Consider an atom _absorbing/emitting a photon_ during a transition:
$$\ket{\alpha}\longleftrightarrow \ket{\beta}+\gamma$$
![[Atomic emission.png]]

- For a _hydrogen atom_, the _rate_ of emission or absorption, given by [[Time-dependent quantum mechanics#Fermi's Golden Rule|Fermi's Golden Rule]], is proportional to:
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
	- Apply the [[Time-Independent Approximation Methods#Variational method|variational method]]

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
- Hence, use the [[Time-Independent Approximation Methods#Variational method|variational method]]
- The _variational parameter_ will be some _effective nuclear charge_ $Z'$
	- Expected: $1<Z'<2$
- The _ground state wave function_ with the parameter:
$$\ket{\psi_\text{trial}(Z')}=\frac{Z'^3}{\pi a_0^3}\exp\left(-\frac{Z'(r_1+r_2)}{a_0}\right)=\ket{\psi_{100}'(Z',r_1)}\ket{\psi_{100}'(Z',r_2)}$$

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
- Use [[Time-Independent Approximation Methods#Time-independent perturbation theory|time-independent perturbation theory]]
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
![[Helium energy levels.png]]
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
	- [[Angular momentum in quantum mechanics#Adding equivalent angular momenta|Symmetry of angular momentum eigenstates]]

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
- _Neither_ coupling scheme is _completely accurate_

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
# jj coupling
- The effect of _electron-electron repulsion_ as a _perturbation_ is to _split_ the levels
	- Analagous to spin-orbit coupling in $L-S$ coupling
- Example: the _shell model_ of nuclear structure

- One _combines_ $l$ and $s$ for each electron:
$$j_{i}=l_{i}\otimes s_{i}=l_{i}\pm \frac{1}{2}$$
- Then combine $j$ for each electron:
$$J=j_{1}\otimes j_{2}\otimes \dots \otimes j_{N}$$
- The effect of _electron repulsion_ is to _split_ the $J$ levels for given $J$

- If two electrons have the _same value_ of $j$, one must make sure the state has the required [[Identical Particles#Coupled angular momentum|antisymmetry]]
# Atomic spectra
- In multi-electron atoms, the dominant transitions are _electric dipole_ (E1) transitions
	- [[#Hydrogen atom selection rules]]
	- [[#E1 transitions in helium]]

- Transition rate between states $\ket{\alpha}$ and $\ket{\beta}$:
$$\Gamma \propto\omega^{3}|\braket{ \alpha | \hat{\boldsymbol{d}}|\beta } |^{2}\hspace{1cm}\hat{\boldsymbol{d}}=-e\sum_{i=1}^{N}\hat{\boldsymbol{r}}_{i}\hspace{1cm}\hbar \omega=\left|E_{\alpha}-E_{\beta}\right| $$

## General selection rules from symmetry
- From the [[Symmetries in quantum mechanics#The Wigner-Eckart Theorem for vector operators|Wigner-Eckart Theorem]], one gets that for _any_ E1 transition:
$$\Delta J=0,\pm1\hspace{1cm}J_\alpha+J_\beta\geq1\hspace{1cm}\Delta m_J=0,\pm1$$
- Under a _parity transformation_, $\hat{\boldsymbol{d}}$ _changes_ sign, giving the [[Symmetries in quantum mechanics#Spatial inversion and parity|selection rule]]:
$$P_{\beta}=-P_{\alpha}$$
- These are _exact_, regardless of [[#Coupling schemes|coupling scheme]]

## LS coupling selection rules
- In LS coupling, $L$ and $S$ are _good quantum numbers_
	- It is _not exact_
- As $\hat{\boldsymbol{d}}$ does not involve spin, one gets the same spin selection rule as helium:
$$\Delta S=0\hspace{1.5cm}\Delta m_{S}=0$$
- Combined with the general selection rules:
$$\Delta L=0,\pm 1\hspace{1cm}L_{\alpha}+L_{\beta}\geq 1\hspace{1cm}\Delta m_{L}=0,\pm1$$

- Almost all transitions are _single-electron_, which changes these rules to:
$$\Delta l=0,\pm 1\hspace{1cm}\Delta m_{l}=0,\pm 1$$

## Periodicity
- Elements with _single valence electrons_ $(\text{Li},\text{Na},\dots)$ typically have _similar spectra_ to [[#Hydrogen atom selection rules|hydrogen]]
- States with _different_ $l$ are _no longer_ approximately degenerate
- As $n$ _increases_, the nuclear charge is _more effectively screened_
- _Spin-orbit coupling_ also becomes more significant as it scales with $Z^4$

- Elements with _two valence electrons_ $(\pu{Be},\pu{ Mg },\dots)$ also have similar spectra to [[#E1 transitions in helium|helium]]
- They have two _separate spectra_ due to $\Delta S=0$
- As $n$ increases, that starts to _break down_ as $LS$ coupling is no longer accurate

## Emission and absorption
- An _emission_ spectrum has atoms _excited to all levels_, then _decay_ into lower levels
- _All transitions_ can be seen as _bright lines_

- An _absorption_ spectrum has lines _irradiated_ with a spectrum of wavelengths
- _Transitions from the ground state_ can be seen as missing lines
- Transitions from _metastable states_ can also be seen

# Zeeman effect
- When an $N-$electron atom is placed in an _external magnetic field_ $\bm{B}$, the _contributions_ to the Hamiltonian:
$$\hat{H}_B=-\hat{\bm{\mu}}_L\cdot\hat{\bm{L}}-\hat{\bm{\mu}}_S\cdot\hat{\bm{S}}=\frac{\mu_B}{\hbar}(\hat{\bm{L}}+g_e\hat{\bm{S}})\cdot\bm{B}$$
- Here, $\hat{\bm{L}}$ and $\hat{\bm{S}}$ are the _total angular momenta_:
$$\hat{\bm{L}}=\sum_{i=1}^N\hat{\bm{L}}_i\hspace{1.5cm}\hat{\bm{S}}=\sum_{i=1}^N\hat{\bm{S}}_i$$
- Orienting $\bm{B}$ along the $z-$axis:
$$\hat{H}_B=\left(g_L\hat{L}_z+g_S\hat{S}_z\right)\frac{\mu_{B}B_{z}}{\hbar}$$
- The resulting energy correction is of the _order_ $6\times 10^{-5} (B/\text{T})\,\text{eV}$
	- _Small_ relative to atomic binding energies, hence first-order perturbation theory applies

- Atomic energy levels have a _degeneracy_ $2J+1$
- Hence, [[Time-Independent Approximation Methods#Degenerate perturbation theory|degenerate perturbation theory]] applies
- Works for any _general field strength_ $B$

- To simplify, go to _extremes_ in the field strengths and consider splitting relative to the _fine structure_ splitting $(\Delta E_{\text{FS}})$
- For _strong field strengths_, $\mu_{B}B\gg(\Delta E)_{\text{FS}}$, hence one can use an _uncoupled basis_ $\ket{L,m_{L},S,m_{S}}$
- For _weak field strengths_, $\mu_{B}B\ll(\Delta E)_{FS}$, hence one can use a _coupled basis_ $\ket{J,m_{J},L,S}$

## Strong-field Zeeman effect
- For a _strong field_, splitting due to _fine structure_ can be _neglected_:
$$\mu_{B}B\gg \left<\hat{H}_{2}\right> =\left<\xi(r)\hat{\boldsymbol{L}}\cdot\hat{\boldsymbol{S}}\right>$$

- In this case, $\hat{H}_{B}$ is treated as the _perturbation_ and spin-orbit coupling $\hat{H}_{2}$ is _neglected_:
$$\hat{H}=(\hat{H}_{0}+\hat{H}_{1})+\hat{H}_{B}$$
- Neglecting fine structure, states of same $J$ are _degenerate_ in energy
	- Only the first two of [[#Hund's rules]] apply
- The degeneracy is $g=(2L+1)(2S+1)$

- As $\hat{H}_{B}$ is _diagonal_ with respect to $\hat{L}_{z}$ and $\hat{S}_{z}$, the _energy_ from first-order perturbation theory is:
$$\begin{align}
(\Delta E)_{B}&=(g_{L}m_{L}+g_{S}m_{S})\mu_{B}B_{z} \\ &\approx(m_{L}+2m_{S})\mu_{B}B_{z}
\end{align}$$
- This _lifts_ the degeneracy in $m_L$ and $m_S$

- For $L=0$, it splits into $2S+1$ levels of spacing $2\mu_{B}B_{z}$
- For $L>0$, it splits into $2(L+2S)+1$ levels of spacing $\mu_{B}B_{z}$

- The [[#From LS coupling|selection rules from LS coupling]] still apply, hence $\Delta m_{S}$ still applies for _E1 transitions_ between the split levels

## Weak-field Zeeman effect
- For a _weak field_, energy corrections are much _smaller_ than that of fine structure:
$$\mu_{B}B\ll \left<\hat{H}_{2}\right> =\left<\xi(r)\hat{\boldsymbol{L}}\cdot\hat{\boldsymbol{S}}\right>$$
- The unperturbed Hamiltonian is then:
$$\hat{H}=(\hat{H}_{0}+\hat{H}_{1}+\hat{H}_{2})+\hat{H}_{B}$$
- The fine structure has levels _degenerate_ in $J$
	- Ordering: [[#Hund's rules]]

- The [[Angular momentum in quantum mechanics#The projection formula|projection formula]] gives that $\hat{H}_{B}$ is _diagonal_ w.r.t. the basis $\ket{\alpha Jm_{J}LS}$
- Using the definition of the [[Angular momentum in quantum mechanics#Combining magnetic moments and the Lande g-factor|Lande g-factor]]:
$$\displaylines{(\Delta E)_{B}=m_{J}g_{J}\mu_{B}B \\ g_J=g_L\frac{J(J+1)+L(L+1)-S(S+1)}{2J(J+1)}+g_S\frac{J(J+1)+S(S+1)-L(L+1)}{2J(J+1)}} $$

- The original level _splits_ into $2J+1$ levels

- Hence, in the weak limit:
$$\hat{H}_{B}=-\hat{\boldsymbol{\mu}}_{J}\cdot \boldsymbol{B}\hspace{1.5cm}\hat{\boldsymbol{\mu}}_{J}=-g_{J}\frac{\mu_{B}}{\hbar}\hat{\boldsymbol{J}}$$
- The dipoles _combine_ to become a single dipole, with g-factor:
$$g_{J}\approx \frac{3}{2}+\frac{S(S+1)-L(L+1)}{2J(J+1)}$$

- Transition between the levels are governed by the [[#General selection rules from symmetry|selection rule]]:
$$\Delta m_{J}=0,\pm 1$$

- Zeeman effect in sodium $D$ lines:
![[D lines Zeeman effect.png]]

![[D line Zeeman splitting.png]]
## General field strength
- In an _external field_, the atom is no longer _isolated_
- The _total angular momentum_ is _no longer conserved_ ($J$ is not well defined)
- Hence, by expanding the Hamiltonian, one finds:
$$[\hat{H}_{B},\hat{J}_{x}]\;,\; [\hat{H}_{B},\hat{J}_{y}]\neq 0$$

- However, the system still has _rotational symmetry_ about the direction of the field:
$$[\hat{H}_{B},\hat{J}_{z}]=0$$

- Hence, $m_J$ is _always a good quantum number_ even if $J$ is _not_

- Considering the whole Hamiltonian for intermediate strengths, the _common basis_ of all terms must be found _numerically_
	- Involves diagonalisation of a $6\times{6}$ matrix

- _E1 transitions_ at _any field strength_ are governed by $\Delta m_{J}=0,\pm 1$

## Zeeman effect for hyperfine splitting
- Consider a magnetic field strength _small_ enough such that splitting is comparable to [[The hydrogen atom#Hyperfine structure|hyperfine splitting]] $(\Delta E)_{\text{HFS}}$
$$\displaylines{\mu_{B}B\lesssim(\Delta E)_{\text{HFS}} \\ \hat{H}=(\hat{H}_{0}+\hat{H}_{1}+\hat{H}_{2}+\hat{H}_{\text{HF}})+\hat{H}_{B}}$$

- In the _weak-field_ regime, the dipoles from $\hat{\boldsymbol{L}}$ and $\hat{\boldsymbol{S}}$ can already be combined:
$$\displaylines{\hat{\boldsymbol{\mu}}_{B}=-\frac{\mu_{B}}{\hbar}(g_{J}\hat{\boldsymbol{J}}+g_{I}\hat{\boldsymbol{I}}) \\ \hat{H}_{B}=\frac{\mu_{B}B_{z}}{\hbar}(g_{J}\hat{J}_{z}+g_{I}\hat{I}_{z})}$$
- Consider the _total angular momentum operator_:
$$\hat{\boldsymbol{F}}=\hat{\boldsymbol{J}}+\hat{\boldsymbol{I}}$$

-  As in the fine structure case, $m_F$ is _always a good quantum number_

### Hyperfine weak field
- Hyperfine weak field limit: splitting is much _smaller_ than hyperfine separation
$$\mu_{B}B\ll \left<\hat{\boldsymbol{L}}\cdot\hat{\boldsymbol{I}} \right>$$
- In this case, the dipoles _combine_ into a single $\hat{\boldsymbol{F}}$ dipole:
$$\displaylines{\hat{H}_{B}=-\hat{\boldsymbol{\mu}}_{F}\cdot \boldsymbol{B} \hspace{1.5cm} \hat{\boldsymbol{\mu}}_{F}=-\frac{\mu_{B}}{\hbar}g_{F}\hat{\boldsymbol{F}} \\ g_F=g_J\frac{F(F+1)+J(J+1)-I(I+1)}{2F(F+1)}+g_{I}\frac{F(F+1)+I(I+1)-J(J+1)}{2F(F+1)}}$$
- The _energy corrections_ are then:
$$(\Delta E)_{B}=m_{F}g_{F}\mu_{B}B$$
- Each hyperfine level $F$ splits into $2F+1$ levels

- As _nuclear magnetic dipole moments_ are typically small:
$$g_{I}\ll g_{J}\hspace{1.5cm}g_F\approx g_J\frac{F(F+1)+J(J+1)-I(I+1)}{2F(F+1)}$$

### Hyperfine strong field
- Analagous to the strong field fine structure case:
$$(\Delta E)_{B}=(m_{J}g_{J}+m_{I}g_{I})\mu_{B}B\approx m_{J}g_{J}\mu_{B}B$$
- Therefore, at high field, one expects $2J+1$ levels, like the fine weak field case

- The _subdominant_ contribution _splits_ the $2J+1$ levels into $2I+1$ _closely spaced levels_

### Hyperfine general field
- For a general field, the total Hamiltonian:
$$\hat{H}=\hat{H}_{\text{HF}}+(g_{J}\hat{J}_{z}+g_{I}\hat{I}_{z})\frac{\mu_{B}B_{z}}{\hbar}$$
- The square matrix to diagonalise has dimensions $(2I+1)(2J+1)$

- The general selection rule for transitions:
$$\Delta m_{F}=0,\pm 1$$
![[Hyperfine Zeeman splitting.png]]

## Summary
| Fine structure | Hyperfine structure |
| :--: | :--: |
| $\hat{\boldsymbol{\mu}}_{J}=\hat{\boldsymbol{\mu}}_{L}+\hat{\boldsymbol{\mu}}_{S}$ | $\hat{\boldsymbol{\mu}}_{F}=\hat{\boldsymbol{\mu}}_{J}+\hat{\boldsymbol{\mu}}_{I}$ |
| $[\hat{H},\hat{J}_{z}]=0$ | $[\hat{H},\hat{F}_{z}]=0$ |
| **Weak field** | < |
| $(\Delta E)_{B}=m_{J}g_{J}\mu_{B}B$ | $(\Delta E)_{B}=m_{F}g_{F}\mu_{B}B$ |
| $(2J+1)$ equally spaced levels | $(2F+1)$ equally spaced levels |
| **Strong field** | < |
| $(\Delta E)_{B}\approx(m_{L}+2m_{S})\mu_{B}B$ | $(\Delta E)_{B}\approx g_{J}m_{J}\mu_{B}B$ |
| Spacing of $\mu_{B}B$ for $L>0$ | $(2J+1)$ widely spaced multiplets |
| Spacing of $2\mu_{B}B$ for $L=0$ | Each level has $(2I+1)$ substructure |

# Stark effect
- Consider the effect of an _external electric field_ $\boldsymbol{E}$ on a _hydrogen atom_
- wlog, let $\boldsymbol{E}=(0,0,\mathcal{E})$, hence $\phi=-q\mathcal{E}z$
- The Hamiltonian is then:
$$\hat{H}_{e}=e\mathcal{E}(z_{e}-z_{p})=e\boldsymbol{E}\cdot(\hat{\boldsymbol{r}}_{e}-\hat{\boldsymbol{r}}_{p})\equiv -\boldsymbol{E}\cdot \hat{\boldsymbol{d}}$$
- Here, $\hat{\boldsymbol{d}}$ is the _electric dipole operator_ for the hydrogen atom $e(\hat{\boldsymbol{r}}_{p}-\hat{\boldsymbol{r}}_{e})$

- One typically expects the atom's energy to _decrease_ as the dipole _aligns_ with the field

- Assume an _infinite mass proton_:
$$\hat{H}_{e}=e\mathcal{E}z=e\mathcal{E}r\cos\theta$$

- Consider the eigenstates $\ket{njm_{j}ls}$, representing the level $n^{2S+1}L_{J}$
	- The states are _degenerate_ w.r.t. $m_{j}$, with degenerate $2j+1$
- Treating $\hat{H}_{E}$ as a perturbation, the first order energy correction from [[Time-Independent Approximation Methods#Degenerate perturbation theory|degenerate perturbation theory]] is:
$$\braket{ njm_{j}'l | z|njm_{j}l } $$
- As $\hat{z}$ is _odd_ under spatial inversion, they _vanish_ for $l=l'$

- Hence, the _first-order energy correction vanishes_
- The [[Time-Independent Approximation Methods#Second-order perturbation theory|second-order energy correction]] leads to the _quadratic Stark effect_

- However for _large field strengths_, energy levels of _different_ $l$ can become _degenerate_
- In this case, the _first-order_ perturbation leads to the _linear Stark effect_

## Quadratic Stark effect
- Consider the _ground state_ of the hydrogen atom:
$$\ket{nlm_{l}} =\ket{100} $$
- An explicit calculation confirms that the _first-order energy correction vanishes_

- The [[Time-Independent Approximation Methods#Second-order perturbation theory|second-order energy correction]]:
$$\Delta E^{(2)}=\sum_{n>2,l,m}\frac{|\braket{ nlm |e\mathcal{E}\hat{z} |  100} |^{2}}{E_{1}^{(0)}-E_{n}^{(0)}}$$
- The denominator makes sure it is _negative_

- This can be evaluated _exactly_ as:
$$(\Delta E)^{(2)}=-\frac{9}{4}(4\pi\epsilon_{0})\mathcal{E}^{2}a_{0}^{3}$$
- The _classical_ definition of [[Electromagnetism#Dipoles|polarisability]] is:
$$\Delta E=-\frac{1}{2}\boldsymbol{E}\cdot \boldsymbol{d}=-\frac{1}{2}\alpha \mathcal{E}^{2}$$
- This gives the polarisability:
$$\alpha=18\pi a_{0}^{3}$$

## Linear Stark effect
- Consider the $n=2$ states:
$$\ket{nlm}=\ket{200}, \ket{210}, \ket{21\pm 1}     $$
- For a _high enough_ electric field, with energy correction _much larger than fine structure_, they become _effectively degenerate_ with energy:
$$E_{2}^{(0)}=-\frac{1}{4}R_{\infty}$$
- Using [[Time-Independent Approximation Methods#Degenerate perturbation theory|degenerate perturbation theory]], this requires the calculation of _all matrix elements_
$$\braket{ 2lm |\hat{z}|2l'm'} $$
- From the [[Symmetries in quantum mechanics#The Wigner-Eckart Theorem for vector operators|Wigner-Eckart Theorem]], as well as [[Symmetries in quantum mechanics#Spatial inversion and parity|parity]], this is _only non-zero iff_:
$$\Delta l=\pm 1\hspace{1.5cm}\Delta m_{l}=0$$
- From this, the _only non-zero matrix elements_ are:
$$\braket{ 200 |\hat{z}|210  }=\braket{ 210 |\hat{z} | 200 } =-3e\mathcal{E}a_{0} $$
- The _zeroth-order eigenstates_ and _first-order energy shifts_:
$$\ket{\psi_{\pm }}=\frac{1}{\sqrt{ 2 }}(\ket{200}\pm \ket{210}  )\hspace{1.5cm} (\Delta E)_{2}^{(1)}=\mp 3e\mathcal{E}a_{0}$$

- The states $\ket{21\pm1}$ have _no energy correction_ and remain _degenerate_
![[Linear Stark effect n2.png]]
- To first order, the $n=2$ level splits into _3 equally spaced levels_

- A similar analysis of the $n=3$ level:
![[Linear Stark effect n3.png]]

## General field strength
- At general field strengths where the Stark correction is _comparable to fine structure_, the _total perturbation_ of the field, fine structure, and the Lamb shift must be _considered together_
- This leads to the _diagonalisation_ of a $(2n^{2})\times(2n^{2})$ matrix
- This must be done _numerically_

- For $n=2$, the levels _asymptotically reach_ the 3 levels from the linear Stark effect
![[Real stark effect n2.png]]

- The remnants of _fine structure_ persist

- Similarly for $n=3$:
![[Real Stark effect n3.png]]

# Molecular structure
- A _molecule_ has a collection of $n$ _electrons_ and $N$ _nuclei_, in a _potential_ set up by all the other charges

- As nuclei have a _much greater mass_ than electrons, they are treated _separately_:
>[!info] The Born-Oppenheimer approximation
>To study the eigenstates of electrons in a molecule, _nuclei_ can be treated as being in _fixed positions_
>To study _nuclear motion_ such as rotations and vibrations, assume that electrons _respond instantly_ to changes in nuclear positions

- The _complete_ Hamiltonian for a molecule is:
$$\hat{H}=\sum_{i=1}^{n}\frac{\hat{\boldsymbol{p}}_{i}^{2}}{2m_{e}}+\sum_{I=1}^{N}\frac{\hat{\boldsymbol{p}}_{I}^{2}}{2m_{I}}+V(\{\boldsymbol{r}_{n}\},\{\boldsymbol{R}_{N}\})$$

- In the B-O approximation, the Schrodinger equation is:
$$\left[ -\frac{\hbar^{2}}{2m_{e}}\sum_{i=1}^{n}\nabla_{i}^{2}+V(\{\boldsymbol{r}_{n}\},\{\boldsymbol{R}_{N}\}) \right]\Psi(\{\boldsymbol{r}_{n}\},\{\boldsymbol{R}_{N}\})=E(\{\boldsymbol{R}_{N}\})\Psi(\{\boldsymbol{r}_{n}\},\{\boldsymbol{R}_{N}\})$$

- As the _molecular conformation_ is varied (changing _nuclear positions_), one can _minimise_ the ground state energy to find the _equilibrium conformation_
## The H2+ ion
- The _simplest molecule_, with protons at $\boldsymbol{R}_{a},\boldsymbol{R}_{b}$ plus an electron at $\boldsymbol{r}$
![[H2+ ion.png]]
$$\boldsymbol{R}\equiv|\boldsymbol{R}_{a}-\boldsymbol{R}_{b}|\hspace{1cm}r_{a}\equiv|\boldsymbol{r}-\boldsymbol{R}_{a}|\hspace{1cm}r_{b}\equiv|\boldsymbol{r}-\boldsymbol{R}_{b}|$$
- wlog, orient $\boldsymbol{R}_{a,b}$ along the z-axis, and let the _origin_ be at the _centre_ between the two nuclei
$$\displaylines{\hat{H}=-\frac{\hbar^{2}}{2m_{e}}\nabla_{r}^{2}-\frac{e^{2}}{4\pi\epsilon_{0}}\left( \frac{1}{r_{a}}+\frac{1}{r_{b}}-\frac{1}{R} \right)  \\r_{a,b}=x^{2}+y^{2}+\left(z\pm \frac{R}{2} \right)^{2}}$$

### Variational parameters
- For the _approximate solution_, use the [[Time-Independent Approximation Methods#Rayleigh-Ritz method|Rayleigh-Ritz method]]:
$$\displaylines{\psi_\text{trial}(\boldsymbol{r};R,Z')=\alpha_{a}\psi_{a}(\boldsymbol{r})+\alpha_{b}\psi_{b}(\boldsymbol{r}) \\ \psi_{a,b}(\boldsymbol{r})=\left( \frac{\beta^{3}}{\pi} \right)^{1/2}\exp(-\beta r_{a,b})\hspace{1.5cm}\beta\equiv \frac{Z'}{a_{0}}}$$
- The _variational parameters_ are $\alpha_{a},\alpha_{b},Z',R$

- For $Z'=1$, this is the [[Molecular quantum mechanics#Linear combination of atomic orbitals for diatomics|linear combination of atomic orbitals (LCAO)]] method

- One can use the secular equations to find values of $\alpha_{a},\alpha_{b}$ to _minimise energy_ for a _given set_ of $R,Z'$
	- An _analytical_ process
- Then, _scan_ the ground state energy as functions of $R,Z'$ to find the _equilibrium configuration_
	- A _numerical_ process
### Rayleigh-Ritz method, bonding and antibonding
- The Hamiltonian and overlap matrices (noting the fact that $\psi_{a},\psi_{b}$ are not necessarily orthogonal):
$$ \displaylines{S_{aa}=S_{bb}=1\hspace{1.5cm}S_{ab}=S_{ba}=\braket{ \psi_{a} |  \psi_{b}} \\ H_{aa}=H_{bb}=\braket{ \psi_{a} |\hat{H} | \psi_{a} } \hspace{1cm}H_{ab}=\braket{ \psi_{a} |\hat{H}|\psi_{b}  }  }$$
- The secular equation:
$$\begin{vmatrix}H_{aa}-E &H_{ab}-ES_{ab} \\ H_{ab}-ES_{ab} &H_{aa}-E \end{vmatrix}=0$$

- The resulting eigenstates have $\alpha_{a}=\pm \alpha_{b}$
	- Result: (anti)symmetry w.r.t. _exchange_ $a\leftrightarrow b$
- The _even_ ("gerade") state:
$$\psi_{g}=\frac{\psi_{a}+\psi_{b}}{\sqrt{ 2(1+S_{ab}) }}\hspace{1.5cm}E_{g}=\frac{H_{aa}+H_{ab}}{1+S_{ab}}$$
- The _odd_ ("ungerade") state:
$$\psi_{u}=\frac{\psi_{a}-\psi_{b}}{\sqrt{ 2(1-S_{ab}) }}\hspace{1.5cm}E_{u}=\frac{H_{aa}-H_{ab}}{1-S_{ab}}$$

- For _all_ values of $R$ and $Z'$, the _even_ state $\psi_g$ has _lower energy_

- These two states are _orthonormal_, and _diagonalise_ the Hamiltonian
- For $\psi_{g}$, the wavefunctions interfere _constructively_ to give electron density _between the nuclei_, which _screens_ the proton charge, and hence is _bonding_
- For $\psi_u$, the wavefunctions interfere _destructively_ and cannot screen the proton charge

### Effective nuclear charge and internuclear separation
- Evaluating $E_{g}(R,Z')$ _numerically_:
![[H2+ energies.png]]

- There is only one _stable minimum_:
$$\displaylines{R=2.002a_{0}=106.0\,\text{pm}\hspace{1cm}Z'=1.238 \\ E_{0}\leq -1.173R_{\infty}=-15.96\,\text{eV}}$$

- The _predicted value_ of $R$ is close to the _true value_
- The true value of the energy is about $0.4\,\text{eV}$ _lower_

![[H2+ binding energy.png]]

- As $R\to\infty$, the system becomes a _hydrogen atom plus a proton_, with energy $-R_\infty$
	- $E=0$ corresponds to _all three particles_ infinitely separated

- The _molecular binding energy_ is defined as:
$$E_{b}=-R_{\infty}-E_{0}(R)$$
- For a _molecular bound state_, $E_b>0$
	- In this case, it is $0.173R_{\infty}=2.354\,\text{eV}$

## The H2 molecule
- Geometry of the hydrogen molecule:
![[H2 molecule.png]]
- The full Hamiltonian:
$$\hat{H}=-\frac{\hbar^{2}}{2m_{e}}\left(\nabla_{1}^{2}+\nabla_{2}^{2}\right)-\frac{e^{2}}{4\pi\epsilon_{0}}\left( \frac{1}{r_{a1}}+\frac{1}{r_{a2}}+\frac{1}{r_{b1}}+\frac{1}{r_{b2}}-\frac{1}{R}-\frac{1}{r_{12}} \right)$$
- This is the _sum_ of two $\ce{H_{2}^{+}}$ Hamiltonians plus the term:
$$\frac{e^{2}}{4\pi\epsilon_{0}}\left( \frac{1}{r_{12}}-\frac{1}{R} \right)$$
- Hence, an _estimate_ of the electron _spatial states_:
$$\psi_{g}(\boldsymbol{r}_{1})\psi_{g}(\boldsymbol{r}_{2})\;,\;\psi_{g}(\boldsymbol{r}_{1})\psi_{u}(\boldsymbol{r}_{2})\;,\;\psi_{u}(\boldsymbol{r}_{1})\psi_{g}(\boldsymbol{r}_{2})\;,\;\psi_{u}(\boldsymbol{r}_{1})\psi_{u}(\boldsymbol{r}_{2})$$

### First estimate of ground state
- The _ground state_ is deduced to be:
$$\psi_{g}(\boldsymbol{r}_{1})\psi_{g}(\boldsymbol{r}_{2})=\frac{1}{2(1+S_{ab})}[\psi_{a}(\boldsymbol{r}_{1})+\psi_{b}(\boldsymbol{r}_{1})][\psi_{a}(\boldsymbol{r}_{2})+\psi_{b}(\boldsymbol{r}_{2})]$$
- As this is _symmetric_ w.r.t. interchange, one must _pair_ it with the _spin singlet state_:
$$\ket{\psi}=\psi_{g}(\boldsymbol{r}_{1})\psi_{g}(\boldsymbol{r}_{2})\otimes \frac{1}{\sqrt{ 2 }}(\ket{\uparrow}_{1}\ket{\downarrow}_{2}-\ket{\downarrow}_{1}\ket{\uparrow}_{2}    ) $$
- The new _trial wave-function_ is then:
$$\displaylines{\psi_{\text{trial}}=\frac{\beta^{3}/\pi}{2(1+S)}[\exp(-\beta r_{a1})+\exp(-\beta r_{b1})][\exp(-\beta r_{a2})+\exp(-\beta r_{b2})] \\ S=\left( 1+\beta R+\frac{1}{3}(\beta R)^{2} \right)\exp(-\beta R)\hspace{1.5cm}\beta\equiv \frac{Z'}{a_{0}}}$$
- The _overlap_ $S$ comes from evaluation of $S_{ab}$ for the $\ce{H_{2}^{+}}$ ion

- Using the variational method again gives:
$$R=73.0\,\text{pm}\hspace{1.5cm}E_{b}\equiv-2R_{\infty}-E_{0}=3.49\,\text{eV}$$
- However, the _real value_ of $E_b$ is around $4.75\,\text{eV}$

###  The ionic contribution
- Expanding the estimate for the ground state reveals:
$$\begin{align}
\psi_{g}(\boldsymbol{r}_{1})\psi_{g}(\boldsymbol{r}_{2})&\propto[\psi_{a}(\boldsymbol{r}_{1})+\psi_{b}(\boldsymbol{r}_{1})][\psi_{a}(\boldsymbol{r}_{2})+\psi_{b}(\boldsymbol{r}_{2})] \\ &=[\psi_{a}(\boldsymbol{r}_{1})\psi_{b}(\boldsymbol{r}_{2})+\psi_{b}(\boldsymbol{r}_{1})\psi_{a}(\boldsymbol{r}_{2})]+[\psi_{a}(\boldsymbol{r}_{1})\psi_{a}(\boldsymbol{r}_{2})+\psi_{b}(\boldsymbol{r}_{1})\psi_{b}(\boldsymbol{r}_{2})]
\end{align}$$

- The first two terms contribute to _covalent bonding_, where the electrons are _assigned to different protons_
- The other two terms contribute to _ionic bonding_, where the electrons are _assigned to the same proton_

- Having _equal contributions_ gives a likelihood that $\ce{H_{2}}$ dissociates into $\ce{H^{+}}$ and $\ce{H^{-}}$ instead of two atoms
	- This is unlikely due to _electron-electron repulsion_

- One can add a parameter to _tune_ the ionic contribution:
$$[\psi_{a}(\boldsymbol{r}_{1})\psi_{b}(\boldsymbol{r}_{2})+\psi_{b}(\boldsymbol{r}_{1})\psi_{a}(\boldsymbol{r}_{2})]+\lambda[\psi_{a}(\boldsymbol{r}_{1})\psi_{a}(\boldsymbol{r}_{2})+\psi_{b}(\boldsymbol{r}_{1})\psi_{b}(\boldsymbol{r}_{2})]$$
- The $\lambda=0$ approximation is known as the _valence bond approximation_

- With the extra parameter, one finds equilibrium at:
$$R=75.7\,\text{pm}\hspace{1cm}E_{b}=4.03\,\text{eV}\hspace{1cm}\lambda=0.26$$

- This leads to the likelihood $\lambda^{2}=0.07$ of the molecule _ionising_

![[H2 binding energy.png]]