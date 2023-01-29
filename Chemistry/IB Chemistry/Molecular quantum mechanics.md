
- Only considering [[Fundamentals of quantum mechanics#Time-independent Hamiltonians and stationary states|time-independent wave functions and Hamiltonians]]
- Considering position-space wave functions

# Models of bonding

## Electrons: Particle in a box
- Used to model conjugated $\pi$ systems
- For a box of length $a$ from $x=0$ to $x=a$, the wave functions are:
$$\psi_n=A\sin\frac{n\pi x}{a}$$
- The corresponding energies are:
$$E_n=\frac{n^2\hbar^2\pi^2}{2ma^2}$$
- Details: [[Time-independent quantum mechanics#Particle in a box|Particle in a box]]

## Nuclei: The quantum harmonic oscillator
- Mathematical details and derivation: [[Quantum Harmonic Oscillator]]
- Potential:
$$V(r)=\frac{1}{2}m\omega^2r^2=\frac{1}{2}kr^2$$
- General solution in terms of [[Special functions and orthogonal relations#Hermite polynomials|Hermite polynomials]] $H_n$:
$$\psi_n(x)=\frac{1}{\sqrt{2^{n}n!}}\left(\frac{m\omega}{\pi\hbar} \right)^{1/4}H_n\left(\sqrt{\frac{m\omega}{\hbar}}x\right)\exp\left(-\frac{m\omega}{2\hbar}x^2\right)$$
- Define the dimensionless variable $q\equiv \sqrt{m\omega/\hbar}\,x$:
$$\psi_n(q)=\frac{1}{\sqrt{2^nn!}}\left(\frac{m\omega}{\pi\hbar} \right)^{1/4}H_n(q)\exp\left(-\frac{1}{2}q^2\right)$$

- Energy levels:
$$E_n=(n+\frac{1}{2})\hbar\omega$$
- There is a _non-zero probability_ that the particle is in the _classically-forbidden region_
- The _lowest energy level_ is given by $E_0=\hbar\omega/2$, this is the _zero-point energy_
	- Consequence of the _uncertainty principle_


## Nuclei: The Morse oscillator
>[!quote]
>"Oh this is a good page. It's a great equation, it should give you a fizz"
>"I'm excited by the Morse potential, and by the end of the lecture series you should be too"
>-Prof. Steven Lee, 2022
- For an actual diatomic molecule, the energy _does not diverge when $r\rightarrow\infty$_
- Energy becomes very large (but not infinite) at $r=0$
- A better approximation is the Morse potential:
$$V_M(r)=D_e\left(1-e^{-\beta(r-r_e)}\right)^2$$
- $D_e$ is the dissociation energy (controls well _depth_)
- $\beta$ controls well _width_ (higher $\beta$ leads to narrower well)
- The _harmonic force constant_ at equilibrium is $k=2\beta^2D_e$
	- Found by Taylor expanding the potential
- This gives another _vibration angular frequency_ $\omega=\sqrt{k/m}$
- $D_0$: energy required to dissociate a molecule originally at the ground state

- The _asymmetry_ of the potential means _average bond length increases_ with increasing $\nu$

- The potential was obtained _empirically_, and only an _approximation_

- The bound energy levels for the Morse potential:
$$E_n=\left(n+\frac{1}{2}\right)\hbar\omega- \left(n+\frac{1}{2}\right)^2 \hbar\omega\chi_e$$
- $\chi_e$ is the _anharmonicity constant_
$$\chi_e=\frac{\hbar\beta^2}{2m\omega}=\frac{\hbar\omega}{4D_e}$$
- Dimensionless, typically $<<1$

- Molecules fit this model for small $n$
- Anharmonic term _becomes larger for higher energy levels_ 
	- Bigger deviation from harmonic energy levels
- _Spacing between levels decreases_ for higher energy levels

- There is a _finite_ number of vibrational levels/bound states
	- At some point, the calculated energy levels decrease with increasing $n$, further levels have no physical meaning
	- Number of levels depends on $D_e$
- The _maximum level_ is given by $n_\text{max}=1/(2\chi_e)-1/2$
- The _maximum energy_ is simply $E(\nu_\text{max})=D_e$

![[Morse energy levels.png]]

# Angular momentum
- Details: [[Angular momentum in quantum mechanics]]
- The eigenvalues of $\hat{L}^2$ and $\hat{L}_z$ are:
$$\displaylines{\hat{L}^2\ket{JM}=\hbar^2J(J+1)\ket{JM} \hspace{1cm}\hat{L}_z\ket{JM}=\hbar M\ket{JM} \\ J=0,1,2\dots \hspace{1cm} M=-J,-J+1,\dots,J-1,J}$$
- $J$: _orbital_ quantum number
- $M$: _magnetic_ quantum number

- The value of $L^2$ is _always_ larger than the maximum value of $L_z$ as $J(J+1)>J^2$
- Remember that when $L^2$ and $L_z$ are determinate, $L_x$ and $L_y$ are _always indeterminate_

- As for the eigenfunctions, they are the [[Special functions and orthogonal relations#Spherical harmonics|spherical harmonics]]

# The Rigid Rotor
- Consider a diatomic molecule, where nuclei have mass $m_1$ and $m_2$, with bond length $R$
- It freely rotates around its centre of mass
- There is no potential
- The Hamiltonian is equal to the kinetic energy:
$$\hat{\Ham}=\frac{\hat{L}^2}{2I}=\frac{\hat{L}^2}{2\mu R^2}$$
	- $I$: moment of inertia
	- $\mu$: reduced mass $m_1m_2/(m_1+m_2)$

- As the Hamiltonian is proportional to $\hat{L}^2$, its eigenfunctions are the spherical harmonics
- The eigenvalues are proportional to eigenvalues of $\hat{L}^2$
$$E_n=\frac{\hbar^2}{2I}J(J+1)$$
- Define the _rotational constant_ $B=\hbar^2/2I$
- As the energy eigenfunctions are independent of $m$, $J_z$ has a $2J+1$ fold _degeneracy_

## Centrifugal distortion
- The atoms in the rotor actually experience a _centrifugal force_
- The _restoring force_ obeys Hooke's Law with force constant $k_f$
- Because of this, there is an _extra term_ in the rotational energy, proportional to $J^2(J+1)^2$
	- Atkins, Friedman p. 274-275

# Rotation and vibration
- Molecules both rotate and vibrate
- Vibration has the variable $r-r_e$
	- Example: harmonic oscillator, Morse potential
- Rotation has variables $\theta$ and $\phi$
	- Example: rigid rotor

- Assume vibration and rotation are independent (A form of the _Born-Oppenheimer approximation_)
	- Good approximation for low energy levels
- The Hamiltonian can be written as $\Ham=\Ham_{vib}+\Ham_{rot}$
- As the two Hamiltonians have different degrees of freedom, the _wave function is separable_ into $\psi_{vib}$ and $\psi_{rot}$:
$$\psi=\psi_\text{vib}\psi_\text{rot}$$

- The overall time-independent Schrodinger equation becomes:
$$\Ham\Psi=[E_{vib}+BJ(J+1)]\Psi$$
- $B$ is often _much smaller_ compared to vibrational energy spacing ($\approx\hbar\omega$)
	- Typically 1000 times smaller

- $B$ can become _dependent on vibrational energy level_ (deviation from BO approximation)
- As vibrational energy level increases, _bond length increases_
- As a result, since $B\propto 1/I$, $B$ _decreases_

# Spectroscopic principles
- Bohr condition: for a transition between two states $\psi_m$ and $\psi_n$ facilitated by a photon, its _frequency $\nu_{mn}$ must equal_ $|E_n-E_m|/h$
- Fermi's Golden Rule: Under an electric field, the rate of induced absorption and emission-
$$B_{mn}=\frac{2\pi}{4\pi\epsilon_0(3\hbar^2)}|\braket{\psi_m|\hat{\mu}|\psi_n}|^2$$
- Spontaneous emission: a molecule in an excited state $\psi_m$ may undergo a spontaneous transition to lower energy state $\psi_n$ with rate
$$A_{mn}=\frac{8\pi h\nu_{mn}^3}{c^3}B_{mn}$$

- The _selection rules_: if a transition is forbidden or allowed (if $B_{mn}=0$)
	- Details: [[Molecular spectroscopy]]
	- Harmonic oscillator: transitions _only allowed between neighbouring levels_ ($v=\pm 1$)
		- $\hat{\mu}\propto\hat{x}$, can be expressed using ladder operators
	- Rotational transitions: $\Delta J=\pm 1$, $\Delta E=2BJ(J+1)$
	- Morse oscillator: non-neighbouring transitions are _much weaker_


# The Born-Oppenheimer approximation
>[!quote]
>It is an unfortunate fact that, having arrived in sight of the promised land, we are forced to make an approximation at the outset.
>-Peter Atkins
- Nuclei are much heavier than electrons
- The approximation: _the motion of nuclei can be ignored
	- When the nuclei move, the electrons respond almost instantaneously
- Split the Hamiltonian into nuclear and electronic wavefunctions
- Very reliable for lower energy states

- First step: the clamped-nucleus electronic Hamiltonian:
$$\hat{\Ham}_\text{elec}=\hat{T}_e+\hat{V}(\bm{Q},\bm{q})$$
	- $\bm{Q}$: positions of nuclei, _fixed when considering the wave function of electrons_
	- $\bm{q}$: positions of the electrons

- The electronic Schrödinger equation:
$$\hat{\Ham}_\text{elec}\psi_\text{elec}(\bm{Q},\bm{q})=E_\text{elec}(\bm{Q})\psi_\text{elec}(\bm{Q},\bm{q})$$
	- Energy: function of positions of nuclei

- For nuclear motion, the electronic equation must be solved many times to obtain $E_\text{elec}$ as a function of $Q$, which is then used as the potential in the nuclear Hamiltonian
- The nuclear Hamiltonian:
$$\hat{\Ham}_\text{nuc}=\hat{T}_N+E_\text{elec}(\bm{Q})$$
- The nuclear wave function is then calculated by solving the nuclear Schrödinger equation:
$$\hat{\Ham}_\text{nuc}\psi_\text{nuc}(\bm{Q})=E\psi_\text{nuc}(\bm{Q})$$
	- $E$: total energy

- Each electronic energy level gives rise to its own $E_\text{elec}(\bm{Q})$ which are completely different
- Each $E_\text{elec}(\bm{Q})$ has its own energy levels for $E$

- Zero point energy: difference between lowest $E$ and $E_\text{elec}$ at equilibrium

- The total wave function of the system:
$$\Psi_\text{molecule}=\psi_\text{elec}\psi_\text{nuc}$$

## Precise formulation and example
- Consider the $H_2^+$ ion, where nuclei are constrained to move along the $z-$axis
- Position of electron is $z$, position of nucleus $i$ is $Z_i$
- The _complete Hamiltonian_ is:
$$\hat{\Ham}=-\frac{\hbar^2}{2m_e}\pd{^2}{z^2}-\sum_{i=1}^2\frac{\hbar^2}{2m_i}\pd{^2}{Z_i^2}+V(z,Z_1,Z_2)=\hat{T}_e+\hat{T}_N+\hat{V}$$
- The approximation _assumes a solution of the form_:
$$\Psi(z,Z_1,Z_2)=\psi(z,Z_1,Z_2)\,\psi_N(Z_1,Z_2)$$
- Substituting this into the time-independent Schrödinger equation:
$$\displaylines{\hat{H}\psi\psi_N=\psi_N\hat{T}_e\psi+\psi\hat{T}_N\psi_N+\hat{V}\psi\psi_N+W=E\psi\psi_N \\ W=-\sum_{i=1}^2\frac{\hbar^2}{2m_i}\left(2\pd{\psi}{Z_i}\pd{\psi_N}{Z_i}+\pd{^2\psi}{Z_i^2}\Psi_N\right)}$$
- Since $m_i>>m_e$, $W$, also known as the _non-adiabatic term_, is _ignored_
- Ignoring $W$ and rearranging:
$$\psi\hat{T}_N\psi_N+\left(\hat{T}_e\psi+\hat{V}\psi\right)\psi_N=E\psi\psi_N$$
- The term in parentheses constitutes the left-hand side of the _electronic Schrödinger equation_:
$$\hat{T}_e\psi+\hat{V}\psi=E_e(Z_1,Z_2)\psi$$
- Solving this gives the _electronic wave function_ and eigenvalue of _the electron's contribution to energy_
	- Includes both _electron kinetic energy_ and _electron-nucleus interactions_
- The function $E_e(Z_1,Z_2)$ gives the _molecular potential energy curve_

- Finding the function then substituting back into the equation and cancelling $\psi$:
$$\hat{T}_N\psi_N+E_e\psi_N=E\psi_N$$
- This eigenvalue $E$ is the _total energy of the molecule_ given by the approximation

- For 3-dimensional motion, the linear momentum operators use $\nabla$

# The hydrogen atom
- [[Time-independent quantum mechanics#The hydrogen atom|Detailed derivation]]
- The Hamiltonian for a hydrogen-like atom is:
$$\begin{aligned}\hat{\Ham}&=-\frac{\hbar^2}{2m_e}\nabla^2-\frac{Ze^2}{4\pi\epsilon_0r} \\ &=-\frac{\hbar^2}{2m_e}\frac{1}{r^2} \pd{}{r}\left(r^2\pd{}{r}\right) + \frac{\hat{L}^2}{2m_er^2} -\frac{Ze^2}{4\pi\epsilon_0r} \end{aligned}$$
- Here we introduce _atomic units_:
| Unit             | Symbol  | Name          | Definition                       |
| ---------------- | ------- | ------------- | -------------------------------- |
| Length           | $a_0$   | Bohr          | $4\pi\epsilon_0\hbar^2/(m_ee^2)$ |
| Mass             | $m_e$   | Electron mass |                                  |
| Charge           | $e$     | Proton charge |                                  |
| Energy           | E_h     | Hartree       | $e^2/(4\pi\epsilon_0a_0)$        |
| Angular momentum | $\hbar$ |               |                                  |

- Rewriting in atomic units,  the Hamiltonian becomes:
$$\hat{\Ham}_\text{at}=\frac{\hat{\Ham}}{E_h}=-\frac{1}{2r^2}\pd{}{r}\left(r^2\pd{}{r}\right)+\frac{\hat{L}^2}{2r^2}-\frac{Z}{r}$$
	- All obtained values are in atomic units

- From this, one can see that the wave function is separable:
$$\psi=R(r)Y(\theta,\phi)$$
- $Y$ are the spherical harmonics, [[#Angular momentum|eigenfunctions of total angular momentum]]

- Then, one can get the _radial equation_:
$$-\frac{1}{2r^2}\pd{}{r}\left(r^2\pd{R}{r}\right)+\frac{l(l+1)}{2r^2}R-\frac{ZR}{r}=ER$$
- The allowed energies are determined from this equation alone

- Here, we (re)introduce the quantum numbers:
- $n$ is the _principal quantum number_, which can run from $l+1$ to $\infty$
- $l$ is the _orbital quantum number_, which can run from $0$ to $\infty$
- $m$ is the _magnetic quantum number_, which can run from $-l+1$ to $l+1$

- The wave function is then labelled:
$$\psi_{nlm}=R_{nl}(r)\,Y_{lm}(\theta,\phi)$$
- Energy determined by $n$, angular part (spherical harmonic) determined by $l$ and $m$

## Higher atomic numbers
- By defining $\rho\equiv Zr$, one can modify the radial equation:
$$-\frac{1}{2\rho^2}\pd{}{\rho}\left(\rho^2\pd{R}{\rho}\right)+\frac{l(l+1)}{2\rho^2}R-\frac{R}{\rho}=\frac{E}{Z^2}R$$
- The radial wavefunctions as a function of $\rho$ are _the same for any hydrogen-like atom_
- Energy scales with $Z^2$

## The orbitals
- The energy of an atomic orbital is (written _in Hartrees_):
$$E_{n}=-\frac{Z^2}{2n^2}$$
- Energy levels get closer together as $n$ increases

- The radial wave function can be described using the [[Special functions and orthogonal relations#Associated Laguerre polynomials|associated Laguerre polynomials]]
- The entire normalised wave function is:
$$\psi_{nlm}=\sqrt{\left(\frac{2}{n}\right)^3\frac{(n-l+1)!}{2n(n+l)!}}\exp(-\rho/n)\left(\frac{2\rho}{n}\right)^l\left[L^{2l+1}_{n-l-1}(2\rho/n)\right]Y^m_l(\theta,\phi)$$
- The wave functions are mutully orthogonal

- When $m\neq0$, the solutions are complex
- To make real orbitals, use a _linear combination_ of $+m$ and $-m$ 
	- Still a solution to the Schrodinger equation as the orbitals are degenerate
	- Results are _NOT eigenfunctions of $\bm{\hat{L}}_z$_

- Example: $2p$ orbitals
	- $m=0$: $p_z$ orbital, purely real, proportional to $z$
	- $m=\pm 1$: combine $\psi_{2s1}$ nd $\psi_{2s\bar{1}}$ in equal magnitudes to make $p_x$ and $p_y$, proportional to $x$ and $y$ respectively

- Example: $3d$ orbitals
	- $m=0$: $d_{z^2}$ (actually proportional to $3z^2-r^2$)
	- $m=1$: $d_{xz}$ and $d_{yz}$
	- $m=2$: $d_{x^2-y^2}$ and $d_{xy}$


## Nodal structure
- Lowest energy function has no nodes
- Node increases by one as energy level increases
- Total number of nodes: $n-1$
	- Total number of radial nodes: $n-l-1$
	- Total number of angular nodes: $l$

## Radial probability density
- The radial probability density $P_nl(r)$ is:
	$$P_{nl}(r)=r^2R_{nl}^2$$
	- Consider the _probability of finding an electron in a spherical shell_ between $r$ and $r+dr$
	- Spherical harmonics are irrelevant as they are normalised

- The _expectation value_ of $r$ is given by:
$$\braket{r}=\int_0^\infty rP_{nl}\,dr=\int_0^\infty r^3R_{nl}^2\,dr$$
- This is different from the _most likely value_ of $r$, given by $\partial P_{nl}/\partial r=0$

# Many-electron atoms
>[!quote]
>"So that was the hydrogen atom, no approximations made there, now you must be feeling confident to tackle the rest of chemistry...well let's go in baby steps"
>-Prof. Stuart Althorpe, 2022


- Hamiltonian for a Helium atom:
$$\hat{\Ham}=-\frac{\hbar^2}{2m_e}\nabla_1^2-\frac{\hbar^2}{2m_e}\nabla_2^2-\frac{Ze^2}{4\pi\epsilon_0r_1}-\frac{Ze^2}{4\pi\epsilon_0r_2}+\frac{e^2}{4\pi\epsilon_0r_{12}}$$
	- $KE$ of both electrons, $PE$ of both electrons due to the nucleus
	- Plus the "mutual hatred" of the two electrons

- _Unseparable_ into $\psi_1$ and $\psi_2$ due to $r_{12}$ term

## Central field approximation
- _Approximate_ the Hamiltonian as $\Ham_1$ and $\Ham_2$, where:
$$\hat{\Ham}_i=-\frac{\hbar^2}{2m_e}\nabla_i^2+V(r)$$
- $V(r)$ is a _spherical average_ of repulsion from the other electron
	- Derive the potential $V_1(r)$ from $\braket{1/r_{12}}=\braket{\psi_2|1/r_{12}|\psi_2}$
- Therefore, $\Ham_1$ depends on $\psi_2$ and vice versa
	- "It's like the chicken and the egg!" - Prof. Althorpe

- Solution: The self-consistent field approach
1. Guess the forms of $\psi_1$ and $\psi_2$
2. Average over $\psi_2$ to generate $\Ham_1$, and do the same for $\psi_1$ and $\Ham_2$
3. Solve the radial Schrodinger equations for $\psi_1$ and $\psi_2$ computationally
4. Repeat steps 2 and 3 with the new functions to get better approximations
5. Iterate until self-consistent

## Energies of the electrons
- Energy will now also depend on $l$
	- Expectation value of potential is given by:
 $$\braket{V}_{nl}=\int\hat{V}(r)P_{nl}(r)\,dr$$
	- The potential behaves like $-Z/r$ near the nucleus but $1/r$ far outside
	- Orbitals with lower $l$ (e.g. $s$) has a density _peak near the nucleus_
	- Hence, orbitals with lower $l$ have a _lower energy_
	- Lower $l$: _penetrate_ into the nucleus
	- Higher $l$: nuclear charge is _screened_
- As the potential only depends on $r$, the angular part is _still a spherical harmonic_

- The _effective nuclear charge_ is defined using the orbital energy:
$$E_{nl}=-\frac{Z_\text{eff}^2}{2n^2}$$
- It can be estimated using _Slater's Rules_:
	- Purely empirical
	- $Z_\text{eff}=Z-s_{nl}$, where the latter term is a _screening constant_

## Ionisation energy
- Energy needed to remove one electron from an atom to form an ion
- General increase across a period due to lowering orbital energies
- Increase interrupted when electrons fill a new shell
- Ionisation energy decreases down a group
- Details: [[IA Inorganic chemistry-periodicity and the elements#Ionisation energy|IA inorganic chemistry-Ionisation energy]]

# Spin
- Detailed quantum mechanics of spin: [[Angular momentum in quantum mechanics]]
- No classical analogue
- Like orbital angular momentum, described by two quantum numbers:
	- $l\rightarrow s$ : _magnitude_ of angular momentum
	- $m_l \rightarrow m_s$: magnitude _along $z$ component_
- Operators obey the same eigenvalue equations:
$$\displaylines{\hat{S}^2\ket{sm_s}=\hbar^2s(s+1)\ket{sm_s} \hspace{1cm}\hat{S}_z\ket{sm_s}=\hbar m_s\ket{sm_s} \\ s=0,\frac{1}{2},1,\frac{3}{2}\dots \hspace{1cm} m_s=-s,-s+1,\dots,s-1,s}$$

- No boundary conditions, _can take half odd-integer values_ unlike orbital $\hat{\bm{J}}$
- $s$ has a fixed value for fundamental particles
	- Half-integer: fermions (e.g. electrons)
	- Integer: bosons

- Nuclei also have spin, denoted $I$, with component $m_I$

- For an electron, the spin is $1/2$, hence $m_s$ is either $+1/2$ or $-1/2$
	- Denoted "spin up" $\upharpoonleft$ and "spin down" $\downharpoonright$

- Notation:
- The state with $m_s=1/2$ is written as $\alpha\equiv\ket{\alpha}\equiv\ket{\frac{1}{2}\frac{1}{2}}\equiv\sigma_{1/2}$
- The state with $m_s=-1/2$ is written as $\beta\equiv\ket{\beta}\equiv\ket{\frac{1}{2}-\frac{1}{2}}\equiv\sigma_{-1/2}$

## Generic wave function for electron
- With the addition of spin, electrons can now be described by the _spin-orbital_:
$$\ket{nlm_lm_s}=R_{nl}(r)Y_{l,m_l}(\theta,\phi)\sigma_{m_s}$$
	- Technically described by 5 quantum numbers with $s$, but it is always $1/2$ for an electron

- It can be described by 5 eigenvalue equations, featuring 5 commuting operators:
$$\displaylines{\hat{\Ham}\ket{nlm_lm_s}=E_{nl}\ket{nlm_lm_s} \\
\hat{L}^2\ket{nlm_lm_s}=\hbar^2l(l+1)\ket{nlm_lm_s} \\
\hat{L}_z\ket{nlm_lm_s}=\hbar m\ket{nlm_lm_s} \\
\hat{S}^2\ket{nlm_lm_s}=\hbar^2s(s+1)\ket{nlm_lm_s} \\
\hat{S}_z\ket{nlm_lm_s}=\hbar m_s\ket{nlm_lm_s}}$$
## Two spins
- Rigorous discussion: [[Angular momentum in quantum mechanics#Singlet and triplet states|addition of angular momentum]]
- Consider two electrons
- The possible states are: $\alpha_1\alpha_2$, $\alpha_1\beta_2$, $\beta_1\alpha_2$, $\beta_1\beta_2$

- The two spins are independent of each other
- When measuring the total $\hat{S}_z$, the corresponding eigenvalues are $\hbar, 0, 0, -\hbar$
- The four possibilities are split into 2 sets, one with $s=0$ and one with $s=1$

| $m_s$ |                    $s=1$                     |                    $s=0$                     |
| ----- |:--------------------------------------------:|:--------------------------------------------:|
| 1     |              $\alpha_1\alpha_2$              |                                              |
| 0     | $(\alpha_1\beta_2+\beta_1\alpha_2)/\sqrt{2}$ | $(\alpha_1\beta_2-\beta_1\alpha_2)/\sqrt{2}$ |
| -1    |               $\beta_1\beta_2$               |                                              |

- States with $s=1$ are _triplet states_, and are _symmetric_
- The state with $s=0$ is a _singlet state_, and is _antisymmetric_
- The two-electron spin function is denoted $\sigma$

- In general, more useful to consider the _total_ spin and $m_s$ of a system to construct allowed states (by the Pauli Principle below)

# Pauli Principle
- The quantum mechanics of identical particles: [[Multiple particles in quantum mechanics]]
- For 2 identical particles, the collective wavefunction is denoted $\Psi_{12}=\psi_1\psi_2$
- In quantum mechanics, 2 electrons are _indistinguishable_ (labelling is impossible)

- Since the probability distribution should not change when the particles are exchanged:
$$\displaylines{|\Psi_{12}|^2=|\Psi_{21}|^2 \\ \Psi_{12}=\pm\Psi_{21}}$$
- The _Pauli principle_ states that all electronic wave-functions are _antisymmetric_ with respect to exchanging particles

- Given two arbitrary electron wave functions _excluding spin_, $\psi_a$ and $\psi_b$
- "Electron 1" in state $\psi_a$ is denoted $\psi_a(1)$ 
- The total wave function $\psi_a(1)\psi_b(2)$ does not satisfy exchange (anti)symmetry _in general_
- However, a(n) _(anti)symmetric wave function can be constructed_:
$$\psi_\pm=\frac{1}{\sqrt{2}}[\psi_a(1)\psi_b(2)\pm\psi_a(2)\psi_b(1)]$$

- Antisymmetry for electron wave functions can be achieved in two ways:
	- _Symmetric_ wave function $\times$ _singlet_ spin state $(\psi_+\sigma_s)$
	- _Antisymmetric_ wave function $\times$ _triplet_ spin state $(\psi_-\sigma_t)$

- For $\psi_a=\psi_b$, the _antisymmetric wave function vanishes_
- The _Pauli Exclusion Principle_: two electrons can only go into the _same orbital_ when they have _different spins_
	- The acceptable wave function is:
	$$\psi_{tot}=\psi_+\sigma_s=\frac{1}{2}\Big[\psi_a(1)\psi_b(2)+\psi_a(2)\psi_b(1)\Big]\Big[\alpha_1\beta_2-\beta_1\alpha_2\Big]$$

## Fermi holes
- Consider two electrons with collective _spatial_ wave function $\psi(\bm{r}_1, \bm{r}_2)$
- Consider the case when $\bm{r}_1=\bm{r}_2$
	- Same spin (triplet): $|\psi|^2=0$
	- Opposite spin (singlet): $|\psi|^2>0$

- Due to the continuity of $\psi$, for small $r_{12}$ _it is much more likely to find two electrons in a singlet state_, this is the _Fermi hole_
- Repulsion potential is inversely proportional to $r_{12}$
- Average repulsion energy is _substantially less for electrons of triplet states_

# The Helium atom
- The $1s^2$ configuration can _only accommodate a singlet state_
	- Position wave function is _symmetric_

- Consider the $1s2s$ configuration, there are two possible states (including spin):
$$\Psi_+=\psi_+\sigma_s=\frac{1}{\sqrt{2}}\Big[\psi_{1s}(1)\psi_{2s}(2)+\psi_{1s}(2)\psi_{2s}(1)\Big]\sigma_s$$
$$\Psi_-=\psi_-\sigma_t=\frac{1}{\sqrt{2}}\Big[\psi_{1s}(1)\psi_{2s}(2)-\psi_{1s}(2)\psi_{2s}(1)\Big]\sigma_t$$

## Coulomb and exchange integrals
- The average electron repulsion is found by:
$$\braket{\frac{1}{r_{12}}}_\pm=\braket{\Psi_\pm|\frac{1}{r_{12}}|\Psi_\pm}=\braket{\psi_\pm|\frac{1}{r_{12}}|\psi_\pm}$$
- Expanding the average electron repulsion:
$$\displaylines{\braket{\frac{1}{r_{12}}}_\pm=J\pm K \\ J=\int\int \psi_{1s}(1)\psi_{2s}(2)\frac{1}{r_{12}}\psi_{1s}(1)\psi_{2s}(2)\,d^3\bm{r}_1d^3\bm{r}_2=\int\int |\psi_{1s}(1)|^2|\psi_{2s}(2)|^2\frac{1}{r_{12}}\,d^3\bm{r}_1\,d^3\bm{r}_2 \\ K=\int\int \psi_{1s}(1)\psi_{2s}(2)\frac{1}{r_{12}}\psi_{1s}(2)\psi_{2s}(1)\,d^3\bm{r}_1\,d^3\bm{r}_2 }$$
- $J$ is the _Coulomb integral_, quantifying the classical electron repulsion
- $K$ is the _exchange integral_, resulting from the particles being indistinguishable, it can be understood as an "overlap density" of $\psi_{1s}\psi_{2s}$

- The 3 triplet states have a _lower energy_ than the singlet state due to the Fermi hole

# More on multi-electron atoms

- Notation for quantum numbers: _lower-case_ for single electrons, _upper-case_ for total

- The _Hartree-Fock_ method to construct a wave function for a multi-electron atom:
	1. Make the SCF approximation to give the spatial $\psi$
	2. Make the symmetric and antisymmetric wave functions $\psi_\pm$, resulting in the stabilisation of higher spin states by Fermi holes

- The Hartree-Fock approximation gives the energy eigenvalue to within 1%
	- Inaccuracy from the _mean-field approximation_
- The remaining 1% is the _electron correlation_, from _direct Coulombic interactions_

## Electron correlation
- In the central field approximation, electrons still have a _well-defined_ orbital angular momentum and $l$, with the _angular parts still being spherical harmonics_

- In a real atom, the electrons _exert mutual torques_ on each other, and _exchange orbital angular momentum_, resulting in individual angular momentum _not being well defined_
- Only _total orbital angular momentum_ $L$ and $M_L$ are defined

- The orbital angular momentum can _couple_ with the spin angular momentum
- _Spin-orbit coupling_ relates $M_L$ and $M_S$, making them less well-defined

- More useful to consider _total angular momentum_ $J$ and $M_J$
- The quantum number $J$ _can take values_ $L+S$, $L+S-1,\dots$, down to $|L-S|$
	- When $S\leq L$, there are $2S+1$ possible values of $J$

- Therefore, the multi-electron wave function is defined by 4 quantum numbers:
$$\ket{\Psi}=\ket{LSJM_J}$$
- Energy _does not depend on $M_J$_, and levels are $2J+1$-fold degenerate

## Terminology and term symbols
- _Configuration_: _which orbital shells_ contain electrons
- _Term_: Values of _total orbital and spin angular momentum_ $L$ and $S$
- _Level_: All three _total angular momentum quantum numbers_, $L$, $S$, and $J$
	- Specifies energy
- _Multiplicity_: $2S+1$, number of possible values for $M_S$
	- Number of values of $J$ when $S\leq L$
- The term symbol:
![[Term symbol.png|300px]]

- $L$: Total angular momentum, _not necessarily subshell of outermost electron_

## Hund's rules
- Used to determine which energy level $E_{LSJ}$ is the lowest
- Only applies to the _ground configuration_

- Hund's _First Rule_: the lowest energy is given by _maximum $S$_
	- Maximises the number of Fermi holes
	- Number of Fermi holes: _number of pairs of electrons with parallel spins_
		- Calculated by $\,^nC_2$ (binomial coefficient)

- Hund's _Second Rule_: at maximum $S$, the lowest energy is given by _maximum $L$_

- Hund's _Third Rule_: 
	- For a shell that is _less than half-full_, take the _lowest $J$_
	- For a shell that is _more than half-full_, take the _maximum_ $J$
	- Origin: spin-orbit coupling in _relativistic quantum mechanics_

- Technique: draw out grid of orbitals with $M_S$ on one axis, $M_L$ on the other, fill by applying the rules in order

### Examples: carbon, nitrogen, oxygen
- Example 1: ground state of carbon $(1s^22s^22p^2)$
	- Ignore closed shells
	- First rule: find maximum possible $S$
		- Fill all spin-up $\alpha$ orbitals first to maximise $M_S$, resulting in $S=1$
		- Multiplicity $=3$, a triplet state
	- Second rule: find maximum possible $L$
		- Fill orbitals to achieve maximum $M_L$, _while keeping the maximum value of $S$_
		- Resulting in $L=1$
	- Third rule: possible $J$ values are $0,1,2$
		- Shell is less than half full, hence $J=0$
	- Hence, the lowest energy level is $\,^3P_0$

- Example 2: ground state of oxygen $(1s^22s^22p^4)$
	- Ignore closed shells
	- First rule: $S=1$, multiplicity $=3$
	- Second rule: $L=1$
	- Third rule: $J=2$
	- Lowest energy level is $\,^3P_2$

- Example 3: ground state of nitrogen $(1s^22s^22p^3)$
	- Ignore closed shells
	- First rule: $S=3/2$, multiplicity $=4$
	- Second rule: $L=0$
	- Third rule: $J$ can only be $3/2$
	- Lowest energy level is $\,^4S_{3/2}$

### Anomalous ionisation energies
- Hund's Rules _also apply to ground states of ions_
- Consider _decrease in number of Fermi holes_ when ionising
- Causes an energy penalty when ionising atoms with half or fully filled orbitals


# The Variational Principle
- Origin and detail: [[Topics in Quantum Mechanics#The Variational Principle]]
>[!info] The Variational Principle
>Let there be an arbitrary Hamiltonian $\Ham$, with ground state energy $E_0$. For _any_ normalised wave function $\wv$:
$$\tilde{E}=\braket{\Psi|\Ham|\Psi}\geq E_0$$

- The 'trial' wave function must be a _physically motivated guess_
	- Not necessarily an eigenfunction of $\hat{\Ham}$, hence the expectation value will not be an eigenvalue
- The guess should _satisfy boundary conitions_

- $\tilde{\psi}$ and $\tilde{E}$ can be _parametrised_ in terms of some parameter $\alpha$
- The best estimate would have a value of $\alpha$ that _minimises_ $\tilde{E}$

## Applying it to known systems

### Particle in a box
- Guess: satisfies $\psi(x=0)=\psi(x=a)=0$
- Trial wave function:
$$\tilde{\psi}(x)=x(a-x)$$

- After normalising and finding the expectation value of $\hat{\Ham}$:
$$\tilde{E}=\frac{10\hbar^2}{2ma^2}>\frac{\hbar^2\pi^2}{2ma^2}$$
	- Estimate within $1\%$

### Harmonic oscillator
- Guess: $\tilde{\psi}=\exp(-\alpha x^2/2)$
- After normalising and applying the Hamiltonian:
$$\tilde{E}=\frac{\hbar^2\alpha}{4m}+\frac{k}{4\alpha}$$
- To find the lowest energy, set $d\tilde{E}/d\alpha=0$
- The desired value of $\alpha$ is then found to be $m\omega/\hbar$

- First term in $\tilde{E}$: kinetic, a large $\alpha$ gives a narrow spread in $x$ and large spread in $p$
- Second term in $\tilde{E}$: potential, a small $\alpha$ gives a wide spread in $x$ and high potential

## Linear combination of atomic orbitals
- [[#The Born-Oppenheimer approximation]]: clamp the nuclei

### The technique for homoatomics
- Consider the simplest diatomic: $H_2^+$
- Let the trial wave function be a _linear combination of $1s$ orbitals_ of the two atoms
$$\tilde{\psi}=c_as_a+c_bs_b$$
	- $s$: normalised $1s$ orbitals of the two atoms $a$ and $b$
	- $c$: coefficients

- Parameters: $c_a$ and $c_b$ 
- The expected energy $\tilde{E}$ of the trial function is:
$$\tilde{E}=\frac{(c_a^2+c_b^2)\alpha+2c_ac_b\beta}{c_a^2+c_b^2+2c_ac_bS}$$
- The integrals $\alpha$, $\beta$, and $S$ are defined as:
$$\displaylines{\alpha= \int s_a\Ham s_a\,d\tau=\int s_b\Ham s_b\, d\tau\\ \beta= \int s_a\Ham s_b\,d\tau =  \int s_b\Ham s_a\,d\tau \\ S=\int s_as_b\,d\tau}$$
- $\alpha$ is the _energy of a $1s$ orbital_ (The Hamiltonian is _for the molecule_, not the atom)
- $\beta$ is the _energy of the overlap_, describing the strength of bonding
- $S$ is the _overlap integral_, $\approx 0$ to simplify calculations

- Both $\alpha$ and $\beta$ are _negative_

- By setting $\partial\tilde{E}/\partial c_a=\partial\tilde{E}/\partial c_b=0$:
$$\begin{pmatrix} \alpha-\tilde{E} & \beta \\ \beta & \alpha-\tilde{E} \end{pmatrix} \begin{pmatrix} c_a \\ c_b \end{pmatrix}=\begin{pmatrix} 0 \\ 0\end{pmatrix}$$

- This is _equivalent to finding the eigenvalues of a matrix_, with eigenvalue $\tilde{E}$
- To solve this, set the _secular determinant_ to zero:
$$\displaylines{\begin{vmatrix} \alpha-\tilde{E} & \beta \\ \beta & \alpha-\tilde{E} \end{vmatrix}=0 \\ \tilde{E}=\alpha\pm\beta}$$

- Substituting this back into the original equations and _normalising_ $(c_a^2+c_b^2=1)$:
$$\displaylines{\tilde{E}=\alpha+\beta \longrightarrow c_a=c_b=\frac{1}{\sqrt{2}} \\ \tilde{E}=\alpha-\beta \longrightarrow c_a=-c_b=\frac{1}{\sqrt{2}}}$$
- As $\beta<0$, the combination where the orbitals combine _in-phase_ gives _lower energy_
	- This is the _bonding orbital_
![[H2 MOs.png]]

### Heteroatomics
- Consider Lithium Hydride $\ce{LiH}$, consisting of the $2s$ and $1s$ orbitals, labelled $s_a$ and $s_b$
- Hence, the two $\alpha$ will be different:
$$\alpha_a = \int s_a\hat{\Ham}s_a d\tau \hspace{1cm} \alpha_b = \int s_b\hat{\Ham}s_b d\tau$$

- Going through the same process:
$$\tilde{E}=\frac{1}{2}(\alpha_a+\alpha_b)+\frac{1}{2}\sqrt{(\alpha_a-\alpha_b)^2+4\beta^2}$$

- For $\alpha_a>\alpha_b$:
	- The bonding orbital has $|c_b|>|c_a|$ (bigger contribution from $\ce{Li}$), and vice versa
	- Coefficients have the same sign for the bonding orbital, opposite for antibonding

- $\alpha_a=\alpha_b=\alpha$: regain expressions for homonuclear diatomic
- $\beta=0$: no interaction, energies are $\alpha_a$ and $\alpha_b$
- For a _fixed $\beta$_, the bonding orbital is _most stabilised when $\alpha_a=\alpha_b$_

- For lithium hydride, the bond is better modelled using an _sp hybrid orbitaIn 2003, the mantra was worked into the theme Navras by Juno Rl_
- From the same method as above, it can be shown that $c_{2s}=c_{2p}$

### Non-zero overlap integral
- For the $H_2^+$ ion, for a non-zero overlap integral, from solving for $\tilde{E}$:
$$(\alpha-\tilde{E})^2=(\beta-\tilde{E}S)^2$$
- Setting energies _relative to $\alpha$_, and since $S>0$, by solving for $\tilde{E}$, it can be shown that _the strength of the bonding is reduced, while the strength of the antibonding is increased_
![[With overlap integral.png]]