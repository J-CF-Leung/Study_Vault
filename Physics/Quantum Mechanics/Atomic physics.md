- For a _single-electron atom_, see [[The hydrogen atom]]

- Many principles from the single-electron atom can also be applied

# Selection rules
- Consider an atom _absorbing/emitting a photon_ during a transition:
$$\ket{\alpha}\longleftrightarrow \ket{\beta}+\gamma$$
![[Atomic emission.png]]

## The hydrogen atom
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


# Multi-electron atoms
