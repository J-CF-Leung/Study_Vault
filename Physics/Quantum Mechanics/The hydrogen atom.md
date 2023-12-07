- Considerations:
	- _Electron_ spin
	- _Relativistic_ effects lead to _fine structure_
	- _Proton_ spin leads to _hyperfine structure_

# With electron spin
- The "zeroth-order" Hamiltonian for the hydrogen atom:
$$\hat{H}_0=\frac{\hat{p}^2}{2m_e}+V(r)\hspace{1.5cm} V(r)=-e\phi(r)=-\frac{Ze^2}{4\pi\epsilon_0r}$$
- It _does not include spin_
- The eigenstates are then _direct products_ of spatial and spin eigenstates:
$$\ket{nlm_lsm_s}=\ket{nlm_l}\otimes\ket{sm_s}$$
- The energies depend _only on_ $n$:
$$\hat{H_0}\ket{nlm_lsm_s}=E_n\ket{mlm_lsm_s} \hspace{1.5cm}E_n=-\frac{Z^2}{n^2}R_\infty$$
- The _degeneracy_ of each level is $2n^2$

- In _spherical polars_, the spatial components:
$$\ket{nlm_l}=R_{nl}(r)Y_{lm_l}(\theta,\phi)$$
- [[3D time-independent Hamiltonians#The hydrogen-like atom|Functional forms]]
- The energy eigenstates are _orthonormal_

- One can use the [[Angular momentum in quantum mechanics#Addition of angular momenta|total angular momentum]] as the basis states $\ket{njm_jls}$
$$\hat{\bm{J}}=\hat{\bm{L}}+\hat{\bm{S}}\hspace{1.5cm}j=l\otimes s=l\pm\frac{1}{2}$$
- They are also _energy eigenstates_ as they only depend on $n$
- They are known as the _coupled_ eigenstates
	- They are simply _linear combinations_ of the uncoupled eigenstates
- One can denote the states using [[Molecular quantum mechanics#Energy levels and term symbols|term symbols]]:
$$n^{2S+1}L_J$$

- The coupled eigenstates can be written as:
$$\ket{njm_jls}=\sum_{m_l+m_s=m_j}\ket{nlm_lsm_s}\braket{lm_lsm_s|jm_j}$$

- Consider that $\hat{\bm{L}}$ and $\hat{\bm{S}}$ _commute_ with each other
- One can prove that:
$$[\hat{\bm{L}}\cdot\hat{\bm{S}},\hat{\bm{L}}^2]=[\hat{\bm{L}}\cdot\hat{\bm{S}},\hat{\bm{S}}^2]=0$$
- Therefore:
$$[\hat{\bm{J}}^2,\hat{\bm{L}}^2]=[\hat{\bm{J}}^2,\hat{\bm{S}}^2]=[\hat{\bm{J}}^2,\hat{\bm{L}}\cdot\hat{\bm{S}}]=0$$

- One can see that for the Hamiltonian, there are _two mutually commuting sets of operators_, each of which has _its own set of simultaneous eigenstates_:
$$\displaylines{\{\hat{H},\hat{\bm{L}}^2,\hat{L}_z,\hat{\bm{S}}^2,\hat{S}_z\}\Longrightarrow\ket{nlm_lsm_s} \\ \{\hat{H},\hat{\bm{J}}^2,\hat{J}_z,\hat{\bm{L}}^2,\hat{\bm{S}}^2\}\Longrightarrow\ket{njm_jls}}$$

# Relativistic effects
- The Schrodinger equation is _not Lorentz invariant_
	- It has a _first-order time derivative_ and _second-order space derivatives_

## Zero spin: Klein-Gordon equation
- Applying the operator replacements:
$$\bm{p}\longrightarrow -i\hbar\nabla \hspace{1.5cm} E\longrightarrow i\hbar\pd{}{t}$$
- Using the _relativistic_ relation:
$$E^2=|\bm{p}|^2c^2+m^2c^4$$
- This gives the _Klein-Gordon_ equation:
$$\frac{1}{c^2}\pd{^2\psi}{t^2}-\nabla^2\psi+\frac{m^2c^2}{\hbar^2}\psi=0$$
- This describes _relativistic particles of zero spin_

## Spin-half: Dirac equation
- [[The Dirac Equation]] can be expressed as:
$$i\hbar\pd{\psi}{t}=\hat{H}\psi \hspace{1.5cm} \hat{H}=c\hat{\bm{\alpha}}\cdot\hat{\bm{p}}+\beta mc^2$$
- Here, $\bm{\alpha}$ is a vector of three $4\times4$ matrices, and $\beta$ is a $4\times4$ matrix

- One has to describe the wave function via a _spinor_:
$$\psi=\pmatrix{\psi_1 & \psi_2 & \psi_3 &\psi_4}^T$$
- The first two degrees of freedom correspond to a _particle_, either spin _up or down_
- The second two degrees of freedom correspond to an _antiparticle_ with spin _up or down_
- In the _non-relativistic limit_, $\psi$ becomes a _two-component_ spinor

- An external field is introduced with the _substitutions_:
$$\bm{p}\to\bm{p}-q\bm{A} \hspace{1.5cm} E\to E+q\phi$$
- This gives the equation:
$$\begin{aligned}(E'-q\phi)\psi = &\Bigg[\frac{1}{2m}|\hat{\bm{p}}-q\bm{A}|^2-\frac{q}{m}\hat{\bm{S}}\cdot\bm{B}-\frac{\hat{\bm{p}}^4}{8m^3c^2} \\ &+\frac{q\hbar^2}{8m^2c^2}(\nabla^2\phi)+\frac{q}{2m^2c^2}\hat{\bm{S}}\cdot(\nabla\phi\times\hat{\bm{p}})\Bigg] \psi\end{aligned}$$

- $E'$ is the _relativistic kinetic energy_:
$$E'\equiv E-mc^2$$

- The operator $\hat{\bm{S}}$ is the familiar [[Angular momentum in quantum mechanics#Spin angular momentum|spin operator]] for spin$-1/2$ particles
	- It obeys the same _commutation relation_
- The _intrinsic nature_ of spin can be said to be _derived_ from the Dirac equation
- The Hamiltonian includes a term:
$$\hat{H}_B=-\hat{\bm{\mu}}_S\cdot\bm{B} \hspace{1.5cm}\hat{\bm{\mu}}\equiv\frac{q}{m}\hat{\bm{S}}$$
- The [[Charged Particles#Spin precession|magnetic interaction with spin]] is also _derived_ fom the Dirac equation

## Application to the hydrogen atom
- Compute the _leading_ relativistic effects, up to terms of _order_ $v^2/c^2$
- With the _absence_ of an external _magnetic_ field:
$$\displaylines{\bm{A}=0 \hspace{1cm}\bm{B}=0 \hspace{1cm}q=-e\hspace{1cm}\phi=\phi(r)=-\frac{Ze}{4\pi\epsilon_0r} \\ E'\psi = \left[\frac{1}{2m_e}|\bm{p}|^2-e\phi(r)-\frac{\hat{\bm{p}}^4}{8m_e^3c^2} -\frac{e\hbar^2}{8m_e^2c^2}(\nabla^2\phi)-\frac{e}{2m_e^2c^2}\hat{\bm{S}} \cdot(\nabla\phi\times\hat{\bm{p}}) \right]\psi}$$

- This corresponds to applying some _perturbation_ $H'$ given by:
$$\begin{aligned}\hat{H}'&=-\frac{\hat{\bm{p}}^4}{8m_e^3c^2} -\frac{e\hbar^2}{8m_e^2c^2}(\nabla^2\phi)-\frac{e}{2m_e^2c^2}\hat{\bm{S}} \cdot(\nabla\phi\times\hat{\bm{p}}) \\ &=\hat{H}_R+\hat{H}_D+\hat{H}_{SO} \end{aligned}$$

### Terms in the perturbation
- $\hat{H}_R$ can be understood as the _first-order relativistic correction_ to electron energy:
$$E=\sqrt{p^2c^2+m_e^2c^4}=m_ec^2+\frac{p^2}{2m_e}-\frac{(p^2)^2}{8m_e^3c^2}+\dots$$
- This gives the correction term:
$$\hat{H}'_R=-\frac{\hat{\bm{p}}^4}{8m_e^3c^2}$$

- $\hat{H}_{SO}$ can be evaluated:
$$\nabla\phi\times\hat{\bm{p}}=\frac{1}{r}\pd{\phi}{r}\hat{\bm{r}}\times\hat{\bm{p}}=\frac{1}{r}\pd{\phi}{r}\hat{\bm{L}}$$
- This gives the _spin-orbit term_:
$$\hat{H}_{SO}=\frac{1}{2m_e^2c^2}\frac{1}{r}\frac{dV(r)}{dr}\hat{\bm{L}}\cdot\hat{\bm{S}}$$
- Then for a _hydrogen-like atom_:
$$V(r)=-\frac{Ze^2}{4\pi\epsilon_0r}\Longrightarrow\hat{H}_{SO}=\frac{1}{2m_e^2c^2}\frac{Ze^2}{4\pi\epsilon_0}\frac{1}{r^3}\hat{\bm{L}}\cdot\hat{\bm{S}}$$
- The _semi-classical approach_:
	- The _orbiting_ of the electron through an _electric field_
	- After a _Lorentz transformation_, this gives a _magnetic field_
	- The interaction of the _dipole moment_ $\hat{\bm{\mu}}$ with the _apparent magnetic field_

- The _Darwin term_ is _purely quantum_ in origin:
$$\hat{H}_D=-\frac{e\hbar^2}{8m_e^2c^2}(\nabla^2\phi)$$
- This results from the _"smearing"_ (or _Zitterbewegung_) of the _electron wave-function_

- All of the perturbations are typically _small_:
$$\frac{\mean{\hat{H}_R}}{\mean{\hat{H}_0}}\sim\frac{p^4/(8m_e^3c^2)}{p^2/(2m_e)}\sim\frac{v^2}{c^2}\ll1$$
- This justifies the use of _first-order perturbation theory_
### Applying perturbation theory
- As the _unperturbed_ energy levels are _degenerate_, one must use [[Approximation Methods#Degenerate perturbation theory|degenerate perturbation theory]]
- One must find and _diagonalise_ a $2n^2\times 2n^2$ matrix with elements $\braket{n_j^{(0)}|\hat{H}'|n_k^{(0)}}$
- This _breaks_ the degeneracy of each level, to give the _fine structure_

#### Relativistic correction
- As the term is _independent of spin_, work in the _uncoupled basis_ $\ket{nlm_lsm_s}$:
$$\braket{nl'm_l's'm_s'|\hat{H}_R|nlm_lsm_s}=\braket{nl'm_l'|\hat{H}_R|nlm_l}\delta_{m_s'm_s}$$
- Instead of working with $\hat{p}^4$, express the perturbation _in terms of_ $\hat{H}_0$:
$$\hat{H}_R=-\frac{1}{2m_ee^2}\left(\frac{\hat{\bm{p}}^2}{2m_e}\right)^2=-\frac{1}{2m_ee^2}(\hat{H}_0-V)^2=-\frac{1}{2m_ee^2}(\hat{H}_0^2-\hat{H}_0V-V\hat{H}_0+V^2)$$
- The _spatial wavefunction_ is:
$$\ket{nlm_l}\to R_{nl}(r)Y_{lm_l}(\theta,\phi)$$
- From the fact that the _spherical harmonics are orthonormal_, the _matrix elements_ are:
$$\displaylines{\braket{nl'm_l'|f(r)|nlm_l}=\mean{f(r)}_{nl}\delta_{ll'}\delta_{m_l'm_l} \\ \mean{f(r)}_{nl}=\int_0^\infty r^2f(r)\,R_{nl}(r)^2\,dr}$$
- Therefore, the _uncoupled basis_ $\ket{nlm_l}$ _diagonalises_ the matrix $\hat{H}_R$
	- The expectation values depend _only_ on $n$ and $l$
- Therefore, this basis can be used for _degenerate perturbation theory_

- Define the _fine structure constant_:
$$\alpha\equiv\frac{e^2}{4\pi\epsilon_0\hbar c}\approx\frac{1}{137}$$
- The _unperturbed energies_:
$$E_n=-\frac{Z^2}{n^2}R_\infty\hspace{1.5cm}2R_\infty=\alpha^2m_ec^2$$
- Using the equations above:
$$(\Delta E)_R=-\left(\frac{Z}{n}\right)^4\left(\frac{n}{l+1/2}-\frac{3}{4}\right)\alpha^2 R_\infty$$

#### Spin-orbit correction
- The spin-orbit pertubration:
$$\hat{H}_{SO}=\xi(r)\hat{\bm{L}}\cdot\hat{\bm{S}}\hspace{1.5cm}\xi(r)\equiv\frac{1}{2m_e^2c^2}\frac{Ze^2}{4\pi\epsilon_0}\frac{1}{r^3}$$
- Express the dot product as:
$$2\hat{\bm{L}}\cdot\hat{\bm{S}}=\hat{\bm{J}}^2-\hat{\bm{L}}^2-\hat{\bm{S}}^2$$
- The _coupled_ basis states $\ket{njm_jls}$ are _simultaneous eigenstates_ of these operators
- Combinging this with the fact that $\xi(r)$ is _radial_, the _matrix elements_ are then:
$$\braket{nj'm_j'l's'|\xi(r)\hat{\bm{L}}\cdot\hat{\bm{S}}|njm_jls}=\frac{\hbar^2}{2}\left[j(j+1)-l(l+1)-s(s+1)\right] \mean{\xi(r)}_{nl}\delta_{j'j}\delta_{m_jm_j'}\delta_{ll'}$$

- For _any_ $s$ state, where $l=0$, one gets that there is _no spin-orbit energy_:
$$(\Delta E)_{SO,l=0}=0$$
- For states with $l>0$:
$$\mean{\frac{1}{r^3}}=\int_0^\infty \frac{1}{r}R_{nl}^2\,dr=\frac{Z^3}{a_0^3n^3}\frac{1}{l(l+1/2)(l+1)}$$
- The _energy correction_ is then:
$$(\Delta E)_{SO}=\frac{1}{2m_e^2c^2}\frac{Ze^2}{4\pi\epsilon_0}\frac{Z^3}{a_0^3n^3}\left[\frac{j(j+1)-l(l+1)-s(s+1)}{2l(l+1/2)(l+1)}\right]\hbar^2$$

- As $s=1/2$, $j=l\pm1/2$ and the _spin-orbit correction_ for $l>0$ can be written as:
$$(\Delta E)_{SO}=\pm\frac{1}{2}\left(\frac{Z}{n}\right)^4\frac{n}{j+1/2}\frac{1}{l+1/2}\alpha^2R_\infty$$
- Using the fact that $l=0,1,2,\dots n-1$, each level $n$ is _split_ into $(2n+1)$ energies

#### Spin-orbit commutation relations
- One can check that $\hat{\bm{L}}\cdot\hat{\bm{S}}$ _commutes_ with the set of operators $\{\hat{\bm{J}}^2,\hat{J}_z,\hat{\bm{L}}^2,\hat{\bm{S}}^2\}$
- As the choice of axis is arbitrary:
$$[\hat{\bm{L}}\cdot\hat{\bm{S}},\hat{\bm{L}}]=-[\hat{\bm{L}}\cdot\hat{\bm{S}},\hat{\bm{S}}]\neq0 \hspace{1cm} [\hat{\bm{L}}\cdot\hat{\bm{S}},\hat{\bm{J}}]=0$$
- From this, the the _spin-orbit term_ commutes with the _coupled set_ $\{\hat{\bm{J}}^2, \hat{\bm{J}_z}, \hat{\bm{L}}^2.\hat{\bm{S}}^2\}$ but _not the uncoupled set_ 
- Can be explained as a consequence of [[Symmetries in quantum mechanics#Scalar operators and commutation relations|rotational symmetry]]

#### The Darwin term
- For a $1/r$ potential, the _Laplacian_ gives:
$$\nabla^2(1/r)=-4\pi\delta^3(\bm{r})$$
- Therefore the _matrix element_:
$$\braket{\psi|(\nabla^2\phi)|\psi}=-\frac{Ze}{\epsilon_0}|\psi(0)|^2$$
- _Only_ the $s$ states have a _non-zero potential_ at $r=0$, evaluating $|\psi(0)|^2$:
$$(\Delta E)_D=\begin{cases}\frac{Z^4\alpha^2}{n^3}R_\infty &l=0 \\ 0 & l>0\end{cases}$$
### Resulting fine structure
- The _scale_ of the energy perturbations:
$$\frac{\alpha^2R_\infty}{n^3}=\frac{7.25\times 10^{-4}}{n^3}\,\text{eV}$$

- The _perturbations_, in units of $Z^4\alpha^2R_\infty/4n^3$:
$$\displaylines{(\Delta E)_R=\frac{3}{n}-\frac{4}{l+1/2}\hspace{1.5cm}(\Delta E)_D=\begin{cases}4 &l=0 \\ 0&l>0\end{cases} \\ (\Delta E)_{SO}=\begin{cases}\pm{2}/[(j+1/2)(l+1/2)] &l>0 \\ 0&l=0\end{cases}}$$

- The _individual perturbations_ are _independent of_ $m_l$ and $m_s$

- When the corrections are _summed_, the _total correction_ is:
$$(\Delta E)_{FS}=\frac{Z^4}{4n^3}\left(\frac{3}{n}-\frac{4}{j+1/2}\right)\alpha^2R_\infty$$
- It depends on $n$ and $j$, but _not_ $l$
- Hence, the $n$th energy level _splits_ into $n$ separate energy levels
	- The _lowest_ $j$ gives the _lowest energy_

- States with the _same_ $j$ but _different_ $l$ will remain _degenerate in energy_
![[Hydrogen fine structure.png]]
![[Hydrogen fine structure energies.png]]

## The Lamb shift
- There is _experimental evidence_ that levels of the _same_ $l$ are _not degenerate_:
$$\delta\nu(2S_{1/2}-2SP_{1/2})\approx 1000\,\text{MHz}$$
- Along with the fact that $g_e\neq 2$, this is evidence of _quantum electrodynamics_

- Experiment: a _beam_ of hydrogen atoms _excited_ to $2S_{1/2}$
- _Microwave radiation_, in the presence of an _external magnetic field_, is used to induce _transitions_

- The _QED correction_ is much _larger for_ $S$ states:
![[Lamb shifts.png]]

# Hyperfine structure
- _Hyperfine structure_ is the effect due to the _atomic nucleus_, _except_ those due to its _charge_ or _finite mass_
	- Examples: _finite size_, the _nuclear spin_, _magnetic dipoles_, _electric quadrupoles_

- The most significant effect is due to the _dipole moment_ assoiated with _nuclear spin_:
$$(\hat{\bm{\mu}}_S)_p=g_p\frac{\mu_N}{\hbar}\hat{\bm{I}}$$
- This gives a _magnetic field_ $\bm{B}_p$
- Its interaction with the _electron magnetic dipole moment_ gives the _hyperfine interaction_:
$$\hat{H}_{bf}=-(\hat{\bm{\mu}}_S)_e\cdot\bm{B}_p=-\frac{\mu_B}{\hbar}(\hat{\bm{L}}+g_e\hat{\bm{S}})\cdot\bm{B}_p$$

- _Classically_, the magnetic moment $\bm{M}$ generates a [[Electrodynamics and Optics#The magnetic vector potential|magnetic potential]] and _field_:
$$\displaylines{\bm{A}=-\frac{\mu_0}{4\pi}\bm{M}\times\grad\left(\frac{1}{r}\right) \\ \bm{B}=\frac{\mu_0}{4\pi}\left[\frac{3\bm{r}(\bm{r}\cdot\bm{M})-r^2\bm{M}}{r^5}+\frac{8\pi}{3}\bm{M}\delta^3(\bm{r})\right]}$$
- The _Hamiltonian_ is then:
$$\hat{H}_{hf}=g_p\frac{\mu_B\mu_N}{\hbar^2}(\hat{\bm{L}}+g_e\hat{\bm{S}})\frac{\mu_0}{4\pi}\left[\frac{3\bm{r}(\bm{r}\cdot\bm{I})-r^2\bm{I}}{r^5}+\frac{8\pi}{3}\bm{I}\delta^3(\bm{r})\right]$$
## S states
- For $l=0$, the hyperfine interaction is:
$$(\Delta E)_{l=0}=\braket{n00|\hat{H}_{hf}|n00}=\int\psi^*_{n00}(\bm{r})\hat{H}_{hf}\psi_{n00}(\bm{r})\,d^3\bm{r}$$
- There is _no contribution from orbital angular momentum_ $(\bra{n00}|\hat{\bm{L}}=0)$
- Due to _symmetry_:
$$\mean{r_i^2}=\frac{1}{3}\mean{r^2}\hspace{1.5cm}3\bm{r}(\bm{r}\cdot\bm{I})-r^2\bm{I}=0$$
- Hence, only the _delta function term_ contributes:
$$(\Delta E)_{l=0}=g_eg_p\frac{\mu_B\mu_N}{\hbar^2}\frac{\mu_0}{4\pi}\mean{\hat{\bm{S}}\cdot\hat{\bm{I}}}\frac{8\pi}{3}|\psi_{n00}(0)|^2$$
- This indicates that it is an _interaction between electron and proton dipoles_
- Substituting $|\psi_{n00}(0)|^2=Z^3/(\pi n^3a_0^3)$:
$$(\Delta E)_{l=0}=g_eg_p\frac{2}{3m_p}\frac{Z^3}{n^3}\frac{\alpha^4m_e^2c^2}{\hbar^2}\mean{\hat{\bm{S}}\cdot\hat{\bm{I}}}$$

- _Total angular momentum_ of the _hydrogen atom_:
$$\hat{\bm{F}}=\hat{\bm{L}}+\hat{\bm{S}}+\hat{\bm{I}}$$
- For $l=0$, as $\hat{L}\ket{n00}=0$:
$$\displaylines{\mean{\hat{\bm{F}}^2}=\mean{\hat{\bm{S}}^2}+\mean{\hat{\bm{I}}^2}+2\mean{\hat{\bm{S}}\cdot\hat{\bm{I}}} \\ \mean{\hat{\bm{S}}\cdot\hat{\bm{I}}}=\frac{\hbar^2}{2}[F(F+1)-s(s+1)-l(l+1)]}$$
- For the hydrogen atom, $s=l=1/2$, hence $F=0,1$:
$$\displaylines{\Delta E=\begin{cases}-(3/4)(\Delta E)_{hf} & F=0 \\ +(1/4)(\Delta E)_{hf} & F=1 \end{cases} \\ (\Delta E)_{hf}=\frac{4g_eg_p}{3}\frac{Z^3}{n^3}\frac{m_e}{m_p}\alpha^2R_\infty}$$

- The hyperfine interaction _splits_ each $S-$state into 2 separate levels:
![[Hyperfine split.png]]
- The _degeneracy_ of the zeroth-order states is now $4n^2$
	- Each hyperfine level has _degeneracy_ $2F+1$

- In comparison to _fine structure_, the splitting is _suppressed_ by a factor of:
$$m_e/m_p\sim 1/2000$$
- For the _ground state_ $n=1$, the hyperfine splitting is:
$$(\Delta E)_{hf}\approx 5.87\times 10^{-6}\,\text{eV} \hspace{1cm}\Delta\nu=1420.4\,\text{MHz}\hspace{1cm}\lambda=21.1\,\text{cm}$$
- The _21cm_ line is produced when the _upper level_ is _decays_
	- Correponds to a temperature of $0.07\,\text{K}$, so it is _significantly occupied_

- For _excited_ states, $(\Delta E)_{hf}\propto 1/n^3$

### The 21cm line

## P,D,F states
- Any _non-S state_ will also be _split into two separate levels_, $F=j\pm1/2$
- The first-order energy shifts are then:
$$(\Delta E)_{hf}=\frac{g_eg_p}{4}\frac{Z^3}{n^3}\frac{m_e}{m_p}\alpha^2R_\infty\left[\frac{F(F+1)-j(j+1)-3/4}{j(j+1)(l+1/2)}\right]$$
- The splttings are of a _similar order_
![[Hydrogen hyperfine structure.png]]

- Each _hyperfine level_ has _degeneracy_ $2F+1$
- For an _isolated atom_, the energy levels _cannot be split further_
	- It can only be broken by some _external field_, which _breaks the rotational symmetry_