>[!Convention]
>$$\hbar =1$$

- _Simple_ quantum models of _many-body_ systems

- Actual Hamiltonian for atoms and electrons solid:
$$H=-\frac{1}{2m}\sum_{j=1}^{N}\nabla_{j}^{2} +\dots$$
- Find a _many-electron_ wavefunction
- Intractable for $N\sim N_{A}$

- Requirement for _simple models_ with solutions for $N\to \infty$ that produce physical behaviour
- Tools from [[Second quantisation|second quantisation]] and quantum field theory are needed to represent wave functions

 - Fermions: _anti-bunching_
 - Bosons: _bunching_

# Many-body wave-functions
- Boson and fermion wave-functions:
$$\displaylines{\ket{\Psi^{S}_{\alpha_{1}\alpha_{2}\dots\alpha_{N}}}=\sqrt{ \frac{N!}{\prod_{\alpha}N_{\alpha}!}}\mathcal{S}[\phi_{\alpha_{1}}(\boldsymbol{r}_{1})\phi_{\alpha_{2}}(\boldsymbol{r}_{2})\dots \phi_{\alpha_{N}}(\boldsymbol{r}_{N})] \\ \ket{\Psi^{A}_{\alpha_{1}\alpha_{2}\dots\alpha_{N}}}=\sqrt{ N! }\mathcal{A}[\phi_{\alpha_{1}}(\boldsymbol{r}_{1})\phi_{\alpha_{2}}(\boldsymbol{r}_{2})\dots \phi_{\alpha_{N}}(\boldsymbol{r}_{N})]  } $$

- Single particle _density_:
$$\rho_1(x_1) = N \int dx_2\ldots dx_N \,\lvert\Psi(x_1,x_2,\ldots,x_N)\rvert^2$$
- It is the _expectation value_ of the _density operator_
$$\rho(x)=\sum_{j}\delta(x-x_{j}) \qquad \rho_{1}(x)=\braket{ \Psi|\rho(x) |\Psi  } $$


- Single particle _density matrix_:
	- Result from _tracing out_ $N-1$ particles from an $N$ particle system
$$g(x,y) \equiv N\int dx_2\ldots dx_N \,\Psi^{}(x,x_2,\ldots,x_N)\Psi^{*}(y,x_2,\ldots,x_N)$$
- The _pair distribution function_:
$$\rho_2(x_1,x_{2}) = N(N-1) \int dx_3\ldots dx_N \,\lvert\Psi(x_1,x_2,\ldots,x_N)\rvert^2$$
- It can be expressed in terms of another _expectation value_
$$\rho_{2}(x_{1},x_{2})=\braket{ \Psi|\rho(x_{1})\rho(x_{2}) |\Psi  }-\rho_{1}(x_{1})\delta(x_{1}-x_{2}) $$

## Example cases
### Example: Free particles on a ring
- Ring: circumfrence $L$, no potential
- Eigenstates:
$$\phi_{n}(x)=\frac{1}{\sqrt{ L }}\exp(ik_{n}x)$$
- Boundary conditions:
$$k_{n}=\frac{2\pi n}{L} \qquad E_{n}=\frac{\hbar^{2}k_{n}^{2}}{2m}$$

- Bosons: all in _ground state_, such that $N_{0}=N$
$$\Psi_{0}^{S}(x_{1},x_{2},\dots x_{N})=\frac{1}{L^{N/2}}$$

- Fermions: each level with _one particle_
	- $N$ odd: filled symmetrically from $-(N-1)/2$ to $0$ to $(N-1)/2$ 
	- $N$ even: last particle either at $\pm N/2$
	- Last filled: at _Fermi wave-vector_ $k_F$ and _Fermi energy_ $E_F$

- $z_{i}=\exp(2\pi ix_{i}/L)$
- Slater determinant:
$$\Psi^A_0(x_1,\ldots, x_N)=\begin{vmatrix}
    z_{1}^{-(N-1)/2} &  z_{2}^{-(N-1)/2} & \cdots & z_{N}^{-(N-1)/2} \\
    z_{1}^{-(N-3)/2} &  \cdots & \cdots & \cdots  \\
    \cdots & \cdots & \cdots & \cdots  \\
    z_{1}^{(N-1)/2} &  \cdots & \cdots & z_{N}^{(N-1)/2}
\end{vmatrix}$$

- $N=3$ fermion case, from evaluating the determinant and _factorising_:
$$\Psi_{0}\propto \sin\left[ \frac{\pi(x_{1}-x_{2})}{L} \right]\sin\left[ \frac{\pi(x_{1}-x_{3})}{L} \right]\sin\left[ \frac{\pi(x_{2}-x_{3})}{L} \right]$$

- Generalisation:
	- Using _Vandermonde determinant_
$$\Psi_{0}(x_{1},\dots x_{N})\propto \prod_{i<j}^{N}\sin\left[ \frac{\pi(x_{i}-x_{j})}{L} \right]$$
- The _single particle density matrix_ in this case:
### Example: impenetrable Bose Gas
$$H=-\frac{\hbar^{2}}{2m} \sum_{j}\frac{\partial^{2}}{\partial x_{j}^{2}}+c\sum_{j>k}\delta(x_{j}-x_{k})$$
- A _pair interaction_ modelled by delta function
- All energy is _kinetic_, with the delta function _imposing boundary conditions_

- For _fermions_, the interaction _has no effect_ as it requires bunching
- For _bosons_ with $c\to \infty$, eigen-energies _coincide with that of fermions_, and eigenstates are _modulus of fermion eigenstates_
- The boson ground state is then:
$$\Psi_{0}(x_{1},\dots x_{N})\propto \prod_{i<j}^{N}\left|\sin\left( \frac{\pi(x_{i}-x_{j})}{L} \right)\right|$$
- The _observables_ can be _mapped_ from the fermion case to the boson one as long as it is _insensitive to taking the modulus of the wavefunction_
	- $\rho_{1}(x)$ and $\rho_{2}(x_{1},x_{2})$ can be mapped, but $g(x,y)$ cannot
# Quantum Hall Effect
- A _2D gas_ in a _magnetic field_ $\boldsymbol{B}$

- Single particle Hamiltonian:
	- $\boldsymbol{A}$ is the _vector potential_, where $\nabla\times \boldsymbol{A}=\boldsymbol{B}$
$$H = -\frac{1}{2m}\left(\nabla -i q \mathbf{A}\right)^2$$
- Use the _symmetric gauge_
	- The [[Charged Particles#Landau levels|Landau gauge]] leads to _harmonic oscillator states_ in one direction, _plane waves_ in the other
$$A_x = -\frac{1}{2} B y,\quad A_y = \frac{1}{2} B x$$
## Landau levels
- Use _complex coordinates_
$$z=x+iy\qquad \bar{z}=x-iy$$
$$\partial_{z}=\frac{1}{2}(\partial_{x}-i\partial_{y})\qquad \partial_{\bar{z}}=\frac{1}{2}(\partial_{x}+i\partial_{y}) \qquad \partial_{z}f(\bar{z})=0$$
- Rewrite $H$:
$$H = -\frac{2}{m}\left(\partial_z -\frac{qB \bar z}{4}\right)\left(\partial_{\bar z} +\frac{qB z}{4}\right) + \frac{\omega_c}{2}$$
- The _cyclotron frequency_:
$$\omega_{c}\equiv \frac{qB}{m}$$
### Lowest Landau levels
- The _ground states_ satisfy:
$$\left(\partial_{\bar z} +\frac{qB z}{4}\right)\psi(z,\bar z) = 0$$

- They have energy $\omega_{c}/2$ and are the _lowest Landau levels_ (LLL) $\psi(z,\bar{z})$

- They have the form:
$$\psi(z,\bar{z})=f(z)\exp\left( -\frac{qB}{4}|z|^{2} \right)$$
- $f(z)$ is _arbitrary_, leading to _high degeneracy_

- Denoting by $f(z)$, write the _inner product_:
	- Use _magnetic length_ $l=(qB)^{-1/2}$
	- $d^{2}z=dx\,dy$
$$\braket{ f_{1} | f_{2} } =\int  \frac{d^2z}{(2\pi)^{2}} \overline{f_{1}(z)}f_{2}(z)\exp\left( -\frac{1}{2}|z|^{2} \right)$$
- A possible _orthonormal basis_:
$$f_{n}(z)=\frac{z^{n}}{\sqrt{ 2^{n}n! }}$$
## Filling the Lowest Landau levels
- _Lift_ the degeneracy by adding the _harmonic potential_
$$V_\text{harm}(x,y)=\frac{v}{2}(x^{2}+y^{2})=\frac{v}{2}|z|^{2}$$
- As it is _not a function of_ $x+iy$, $V_\text{harm}f(z)$ is _not in the LLL subspace_

- Only _consider the LLL subspace_
	- Assume $\omega_{c}$ is the _largest energy scale_
- _Replace_ the harmonic potential with:
	- From considering _matrix elements_, and integrating by parts
$$V_\text{harm}\to v\partial_{z}z=v(1+z\partial _{z})$$
- Application to $f_{n}(z)$, $V$ gives an _energetic cost_ to each state:
$$V_\text{harm}f_{n}=v(1+n)f_{n}$$

- Then, consider _filling states_ from $n=0,1,\dots N-1$
- Analagous to the [[#Example Free particles on a ring|1D Fermi gas]], where states are simply $z^{n}$
	- 1D - powers of plane wave states $z$ 
	- 2D - $z$ living on complex plane
- Similar arguments to the [[#Example Free particles on a ring|Fermi gas ground state]] give:
$$\Psi(z_1,\ldots, z_N) = \prod_{j<k}^N (z_j-z_k) \exp\left(-\frac{1}{4}\sum_{j=1}^N\left|z_j\right|^2\right)$$
- The _single particle density_:
$$\rho_1(z,\bar z) = \frac{e^{-|z|^2/2}}{2\pi}\sum_{n=0}^{N-1} \frac{\left|z\right|^{2n}}{2^n n!} = \frac{1}{2\pi} \frac{\Gamma(N,|z|^2/2)}{(N-1)!}$$
![[LLL density.png|500]]
- At _small_ $|z|$, approximate by an _infinite sum_ such that $\rho_{1} \to 1/2\pi$
- Density is _fixed_ until $|z| \sim \sqrt{ 2N }$, after which it _falls_ to zero with _length scale_ $l_{B}$
- The filled LLLs can be described as a _circular droplet_

- There is _one state_ per _flux quantum_ $h/e$

- A _different confining potential_ will change the _droplet shape_, but still with _constant density_

## Laughlin wavefunction
- A _generalised Laughlin wavefunction_:
$$\Psi_m(z_1,\ldots, z_N) = \prod_{j<k}^N (z_j-z_k)^{m} \exp\left(-\frac{1}{4}\sum_{j=1}^N\left|z_j\right|^2\right)$$
- For $m\neq 1$, it is _not a product state_

- For $m$ _odd/even_, it is (anti)symmetric hence it is for _fermions/bosons_

- For _electrons_ with _Coulomb interaction_, $m$ odd is a _good variational wave-function_ as the electrons will tend to be _further away from each other_ compared to $m=1$

### m=2 boson state
- For the _delta function repulsion_:
$$H_{\text{int}} = g\sum_{j<k}\delta(\mathbf{r}_j-\mathbf{r}_k)\quad,\quad g>0$$

- $m=2$ state has _zero interaction energy_ as the state _prevents bunching_

- Hence, _states with no interaction energy_ must have $\Psi_{2}$ as a _factor_
	- For a _higher degree wave-function_, any perturbing harmonic potential will give a higher energy
	- $\Psi_{2}$ is the _ground state for any state with zero interaction energy_

- _Compared_ to an _uncorrelated sampling_, the Laughlin state results in _more uniform sampling_ due to the anti-bunching
	- Left: uncorrelated ; Right: Laughlin
![[Laughlin state.png]]

### Plasma statistical analogy
- Coulomb potential in _2 dimensions_:
$$\nabla^{2}V=-q\delta(\boldsymbol{r}) \implies V=-\frac{q}{2\pi}\log|\boldsymbol{r}|$$
- For a _constant charge density_ $-\rho_{0}$:
$$V_\text{bg}(\boldsymbol{r})=\frac{\rho_{0}}{4}|\boldsymbol{r}|^{2}$$
- Then, for a _collection of identical charges_ with a _constant background_:
$$V(\mathbf{r}_1,\ldots,\mathbf{r}_N) = -\frac{q^2}{2\pi} \sum_{j<k}\log\left|\mathbf{r}_j-\mathbf{r}_k\right| + \frac{q\rho_0}{4}\sum_j \left|\mathbf{r}_j\right|^2$$

- Then, at a non-zero temperature, the _Boltzmann factor_ for such a configuration is:
$$\displaylines{\exp[-\beta V(\mathbf{r}_1, \ldots, \mathbf{r}_N)] = \left|\Psi_m(\mathbf{r}_1, \ldots, \mathbf{r}_N)\right|^2 \\ \frac{\beta q^{2}}{2\pi}=2m \qquad \beta q\rho_{0}=2}$$
- In the large $N$, or _continuum limit_, one can convert the terms to:
$$\beta V[\rho] = -m\int d^2\mathbf{r}\, d^2\mathbf{r}'\, \rho(\mathbf{r})\log\left|\mathbf{r}-\mathbf{r}'\right|\rho(\mathbf{r}') + \frac{1}{2}\int d^2\mathbf{r}\, \left|\mathbf{r}\right|^2\rho(\mathbf{r})$$
- Minimising w.r.t. $\rho(\boldsymbol{r})$ (by evaluating $V[\rho + \delta \rho]$ and applying $\nabla^{2}$ to the condition) gives:
$$\rho(\boldsymbol{r})=\frac{1}{2\pi m}$$

- For _regions with non-zero_ $\rho$, there is _filling fraction_ $1/m$ compared to the $m=1$ case
	- With the thermo-dynamic limit, one _ignores_ the falling off of $\rho$ over a finite length
	- In the continuum limit, one also ignores the _configurational entropy_ of the system
- The _droplet_ now has radius $\sqrt{ 2Nm }$

## Excited states and fractional charge
- The _simplest_ excited state is the _quasi-hole_ state
	- It is also _degenerate_ as energy is independent of $Z$ 
	- A _higher power_ of the excitation part would mean _multiple excitations_, meaning a higher energy
$$\Psi_\text{hole}(z_1,\ldots, z_N|Z) = \left(\prod_j (Z-z_j)\right)\Psi_m(z_1,\ldots, z_N)$$
- Applying the plasma analogy again:
$$V(\mathbf{r}_1, \ldots, \mathbf{r}_N)=-\frac{q^2}{2\pi m}\sum_j \log\left|\mathbf{r}_j-\mathbf{R}\right|-\frac{q^2}{2\pi} \sum_{j<k}\log\left|\mathbf{r}_j-\mathbf{r}_k\right|+ \frac{\rho q_0}{4}\sum_j \left|\mathbf{r}_j\right|^2$$
- This state describes _adding a fractional charge_ $q/m$, at location $Z=X+iY$
- The _plasma_ will then _screen_ the charge, leaving a _hole of fractionalised charge_ $-q/m$ 

- The _normalisation_ of a quasi-hole state is then _approximated_ with the _Boltzmann weight_
$$\int  \prod_{j=1}^{N}d^{2}z_{j}|\Psi _\text{hole}(z_{1},\dots z_{N}|Z)|^{2}\sim \exp\left( \frac{1}{2m}|Z|^{2} \right) $$
### Fractional statistics
- The _two quasi-hole wavefunction_
$$\Psi _\text{2 hole}(z_{1},\dots z_{N}|Z_{1},Z_{2})=\left( \prod_{j}(Z_{1}-z_{j})(Z_{2}-z_{j}) \right)\Psi_{m}(z_{1}\dots z_{N})$$
- This is a _Coulomb plasma_ with _two_ $1/m$ charges
	- There is _no interaction_ between the charges, each is only surrounded by its own _region of depleted density_

- The _Boltzmann weight_ is then:
$$\int  \prod_{j=1}^{N}d^{2} z_{j}|\Psi _\text{2 hole}(z_{1}\dots z_{N}|Z_{1},Z_{2})|^{2}\sim \exp\left( \frac{2}{m}\log|Z_{1}-Z_{2}|+\frac{1}{2m}(|Z_{1}|^{2}+|Z_{2}|^{2}) \right)$$
- Interpreting this as a _probability density_ for a _two-particle wave-function_:
$$\Psi _\text{2 hole}(Z_{1},Z_{2})\sim (Z_{1}-Z_{2})^{1/m}\exp\left( \frac{1}{4m}(|Z_{1}|^{2}+|Z_{2}|^{2}) \right)$$
- For $m=1$, it is _antisymmetric_, therefore the holes are _fermions_

- For $m>1$, it is _multi-valued_ and the holes have _fractional statistics_
# Elastic chain
- A _many-body_, _coupled_ system
![[Elastic chain.png]]
- Impose _periodic boundary conditions_:
$$u_{j}=u_{N+j}$$

## Classical treatment
- The Hamiltonian:
$$H = \sum_{j=1}^N \left[\frac{p_j^2}{2m} + \frac{k}{2} (u_j-u_{j+1})^2 \right]$$
- Poisson bracket:
$$\{u_{j},p_{k}\}=\delta_{jk}$$

### Displacements and normal modes
- From this, obtain the _equations of motion_, and look for an _oscillatory solution_:
	- The boundary conditions lead to a _circulant matrix_, which has _plane wave eigenvectors_
$$u_{j}(t)=u_{j}e^{-i\omega t}\implies -\omega^2 \begin{pmatrix}u_1 \\u_2 \\\cdots \\u_{N-1}\\u_N\end{pmatrix} =\frac{k}{m}\begin{pmatrix}-2 & 1 & 0 & \cdots & 1 \\1 & -2 & 1 & \cdots & 0\\\cdots & \cdots & \cdots & \cdots & \cdots \\0 & \cdot & 1 & -2 & 1\\1 & 0 & \cdots & 1 & -2\end{pmatrix} \begin{pmatrix}u_1 \\u_2 \\\cdots \\u_{N-1}\\u_N\end{pmatrix}$$
- The _eigenvectors_ are given by the _plane waves_:
$$u_{j}=\exp\left( \frac{2\pi in}{N}j \right)\equiv \exp(i\eta_{n}j)$$
- For convenience, take $N$ to be odd and $n=-(N-1)/2,\dots{0}\dots (N-1)/2$

- From the equation of motion, one then gets:
	- The $\eta=0$ mode corresponds to _translation_
	- Dispersion is approximately _linear_ as $\eta\to 0$
$$\omega(\eta) = \sqrt{\frac{4k}{m}}\left|\sin\eta/2\right|$$
- The _general motion_ is then a _superposition_ of the normal modes:
$$u_j(t) = \frac{1}{\sqrt{N}}\sum_{|n| \leq (N-1)/2} q_n(t) e^{i\eta_n j}$$
- For it to be _real_, $q_{-n}=q_{n}^{*}$
- Then for $n\neq 0$:
$$q_{n}(t)=\alpha_{n}\exp[i\omega(\eta_{n})t]+\beta_{n}\exp[-i\omega(\eta_{n})t]$$
- The _zero mode_ for _translation_ of the centre of mass:
$$q_{0}(t)=\sqrt{ N }(X+Vt)$$

### Re-writing the Hamiltonian
- Similar to displacement, write the momenta in terms of normal modes:
$$p_j(t) = \frac{1}{\sqrt{N}}\sum_{|n| \leq (N-1)/2} \pi_n(t) e^{-i\eta_n j}$$
- From the Poisson bracket $\{u_{j},p_{k}\}$, one gets:
$$\{q_{m},p_{n}\}=\delta_{mn}$$
- One then gets the Hamiltonian, _similar_ to that of a harmonic oscillator:
$$H = \sum_{|n| \leq (N-1)/2} \left[\frac{1}{2m}\pi_n \pi_{-n} + k  (1-\cos \eta_n) q_n q_{-n}\right]$$
- If one _splits_ amplitudes between the real and imaginary parts:
	- Corresponds to splitting between _sines and cosines_
$$\begin{align}
q_n &= \frac{1}{\sqrt{2}}\left(q_n' + i q_n''\right),\quad q_{-n} = \frac{1}{\sqrt{2}}\left(q_n' - i q_n''\right)\\
\pi_n &= \frac{1}{\sqrt{2}}\left(\pi_n' + i \pi_n''\right),\quad \pi_{-n} = \frac{1}{\sqrt{2}}\left(\pi_n' - i \pi_n''\right),\quad n\geq 0\end{align}$$
- Split the Hamiltonian as:
$$\displaylines{H=H+H'' \\ H' = \sum_{0 < n \leq (N-1)/2} \left[\frac{1}{2m}\pi'_n \pi'_{n} + k  (1-\cos \eta_n) q'_n q'_{n}\right].}$$
- This is a _sum of_ [[Quantum Harmonic Oscillator|quantum harmonic oscillators]] at different wavenumbers, and the _dispersion relation_ emerges from inspecting the Hamiltonian

### Complex coordinates
- From this, take inspiration from the solution to the quantum harmonic oscillator:
$$\begin{align}
a_n &= \sqrt{\frac{m\omega(\eta_n)}{2}}\left(q_n + \frac{i}{m\omega(\eta_n)}\pi_{-n}\right)\\
a^*_n &= \sqrt{\frac{m\omega(\eta_n)}{2}}\left(q_{-n} - \frac{i}{m\omega(\eta_n)}\pi_{n}\right),\qquad n\neq 0.
\end{align}$$
- The corresponding Poisson bracket:
$$\{a_{m},a_{n}^{*}\}=-i\delta_{mn}$$
- Inverting the transformation:
$$\begin{align}
q_n &= \sqrt{\frac{1}{2m\omega(\eta_n)}}\left(a_n + a_{-n}^*\right)\\
\pi_n &= -i\sqrt{\frac{m\omega(\eta_n)}{2}}\left(a_{-n} - a_{n}^*\right)
\end{align}$$

- The Hamiltonian then takes the form:
$$H = \frac{\pi_0^2}{2m}+\sum_{\substack{n\neq 0 \\ |n| \leq (N-1)/2}} \omega(\eta_n) \left|a_n\right|^2$$
- There is a _centre of mass_ term and the _oscillation Hamiltonian_

## Quantum treatment
- In the quantum chain, take the commutator:
$$[a_{m},a_{n}^{\dagger}]=\delta_{mn}$$
- Accounting for the order of operators, the Hamiltonian becomes:
$$H = \frac{\pi_0^2}{2m}+\sum_{\substack{n\neq 0 \\ |n| \leq (N-1)/2}} \frac{\omega(\eta_n)}{2}\left(a^\dagger_na^{\vphantom{\dagger}}_n+a^{\vphantom{\dagger}}_na^\dagger_n\right)$$
- _Ignoring_ the _translation term_, the new eigenstates are _product states_ of oscillators for each $n$:
$$\lvert{\mathbf{N}}\rangle = \prod_{\substack{n\neq 0 \\ |n| \leq (N-1)/2}} \frac{\left(a^\dagger_n\right)^{N_n}}{\sqrt{N_n!}} \lvert{0}\rangle$$
- Here, $\boldsymbol{N}=\{N_{n}\}$ are the _occupation numbers_ of each mode

- This eigenstate has energy:
$$E(\mathbf{N}) = E_0 + \sum_{\substack{n\neq 0 \\ |n| \leq (N-1)/2}} \omega(\eta_n) N_n$$
- The _ground state energy_ $E_{0}$ is:
$$E_0 = \frac{1}{2}\sum_{|n| \leq (N-1)/2} \omega(\eta_n)$$
### Oscillator quanta as bosons
- The treatment above, with occupation number labelling, matches that of _multiple non-interacting bosons_
- Each normal mode $n$, has $N_{n}$ _quanta_ of energy corresponding to its wavenumber

- One must then still _symmetrise_ the wave-function:
$$\Psi^{\text{S}}_{\alpha_{1}\alpha_{2}\cdots\alpha_{M}}(\mathbf{r}_1,\ldots,\mathbf{r}_M)=\sqrt{\frac{M!}{\prod_{\alpha}N_{\alpha}!}}\mathcal{S}\,\varphi_{\alpha_{1}}(\mathbf{r}_{1})\varphi_{\alpha_{2}}(\mathbf{r}_{2})\cdots\varphi_{\alpha_{M}}(\mathbf{r}_{M})$$

- Its bosonic nature is _independent_ of the _constituent particles_ in the chain
	- The original particles are labelled by _position_, and are assumed to not be able to switch places

## Limits
### Thermodynamic limit
- Limit of a _large system_, with $N \to \infty$:
$$\sum_{|n|<(N-1)/2}\xrightarrow{N\to \infty}N\int_{-\pi}^{\pi}  \frac{d \eta}{2\pi} $$
- One expects energy to be _extensive_

- As $N\to \infty$, calculate ground state energy as:
$$E_{0}\to N\int  \frac{d \eta}{2\pi} \frac{\omega(\eta)}{2}=\frac{2N}{\pi} \sqrt{ \frac{k}{m} } $$

### Continuum limit
- Treating the chain as a _continuum_ of length $L=Na$
- Take the $1\text{D}$ density $\rho$, with $m=\rho a$

- The _elastic modulus_ (dimension independent quantity) is:
$$\kappa=ka$$
- In terms of material properties, one then gets:
$$\frac{E_{0}}{L}=\left( \frac{N}{L} \right)^{2} \frac{2}{\pi} \sqrt{ \frac{\kappa}{\rho} }$$

- As one _approaches a continuum of finite length_, the _energy density diverges_
	- Due to an _infinite number of degrees of freedom_
- The presence of _infinite ground state energy_, analagous to divergences in [[QFT#Hamiltonians|quantum field theory]]

- Aside from the infinity, one can take a _continuum limit of the potential_ with $u(x=ja):=u_{j}$
$$V=\frac{k}{2}\sum_{j}(u_{j}-u_{j-1})^{2}\xrightarrow{{N\to \infty}} \frac{\kappa}{2} \int_{0}^{L}\,dx\,[u'(x)]^{2} $$
- One can also define the _momentum density_ $\pi(x=ja):= p_{j} N/L$, such that:
$$[u(x),\pi(x')]=i\delta(x-x')$$
- The kinetic energy is also well-defined:
$$T\to\frac{1}{2\rho} \int_{0}^{L}\,dx\,[\pi(x)]^{2} $$

- Take the Fourier series, with $k_{n}=2\pi n/L$
$$\displaylines{u(x)=\sum_{n=-\infty}^{\infty} u_{n}\exp(ik_{n}x) \qquad \pi(x)=\frac{1}{L}\sum_{n=-\infty}^{\infty}\pi_{n} \exp(-ik_{n}x) \\ [u_{m},\pi_{n}]=\delta_{mn}}$$
- The continuum Hamiltonian:
$$H=\sum_{n=-\infty}^{\infty }\left[ \frac{1}{2\rho L} \pi_{n}\pi_{-n}+\frac{\kappa Lk_{n}^{2}}{2}u_{n}u_{-n} \right]$$
- Reading off the dispersion relation, it is _linear_:
$$\omega(k)=\sqrt{ \frac{\kappa}{\rho} }|k|\equiv c|k|$$
- The sinusoidal dispersion relation is a result of _lattice discretisation_
- Then, define the _impedance_:
$$Z\equiv \sqrt{ \kappa \rho }$$
- Define ladder operators and the Hamiltonian:
$$\displaylines{\begin{align}
a_n &= \frac{1}{\sqrt{2}}\left[\sqrt{ZkL} u_n + \frac{i}{\sqrt{ZkL}}\pi_{-n}\right]\\
a^*_n &= \frac{1}{\sqrt{2}}\left[\sqrt{ZkL} u_{-n} - \frac{i}{\sqrt{ZkL}}\pi_{n}\right]
\end{align} \\ H - E_0 = \sum_{n=-\infty}^\infty c\left|k_n\right|a^\dagger_na_n}$$
- Energy still written _in terms of oscillator modes_
## Finite temperature
- _Occupancies_ at a finite temperature at equilibrium: the Bose distribution
$$\langle N_{n} \rangle=n_{B}(\omega(\eta_{n})) \equiv \frac{1}{\exp(\beta\omega)-1}$$
- The _thermal average_ of the energy of excited states:
$$\langle H-E_{0} \rangle =\sum_{|n|\leq (N-1)/2} \omega(\eta_{n})n_{B}(\omega(\eta_{n}))$$
- This is _finite_ even for $N \to \infty$

- At _low energies_, this gives the _equipartition theorem_
	- _Classical_ result, leads to divergence if applied to all energy levels
$$\omega n_{B}(\omega) \xrightarrow{\omega\to 0}k_{B}T$$

## Fluctuations
- Fluctuations of a _quantum_ nature, instead of thermal
- From _quantum mechanical uncertainty_

### Position fluctuations
- $u_{j}-u_{k}$ can _fluctuate_ in the ground state
- Measure fluctuations by:
$$\braket{ 0|(u_{j}-u_{k})^{2} | 0 } $$
- Using the Fourier expansions and expressing in terms of $a_{n},a^{\dagger}_{n}$

- One gets:
$$\langle {0}\rvert\left(u_j-u_k\right)^2\lvert{0}\rangle  = \frac{1}{m}\int_{-\pi}^\pi \frac{d\eta}{2\pi} \frac{1-\cos\left(\eta[j-k]\right)}{\omega(\eta)}$$
- For $|j-k|\gg 1$, the integral is _dominated_ by $|j-k|^{-1}<\eta<\pi$

- For the _linear dispersion_ at low $\eta$ (long wavelength), the integrand _blows up_
- Any _fast oscillations_ in the integrand will _average out_

- As the integral is dominated by the linear part:
	- The _oscillator length_ $l_\text{osc}=(km)^{1/4}$
$$\omega \sim \sqrt{ \frac{k}{m} }|\eta| \implies \braket{ 0|(u_{j}-u_{k})^{2} | 0 } \sim \frac{l_\text{osc}^{2}}{\pi} \ln|i-j|$$

- Uncertainty in separation will _increase with separation_
- The ground state of the _one-dimensional_ chain is _not a crystal_
- In _three dimensions_, there is no divergence, and there is _long-range order_

### Density fluctuations
- For a _periodic system_, take $L-$periodic delta functions for the [[#Many-body wave-functions|single particle density]]
$$\rho(x)=\sum_{j=1}^{N}\delta_{L}(x-x_{j})$$
- Alternatively, the _Fourier components_:
$$\rho_{k}=\sum_{j=1}^{N}\exp
(-ikx_{j})$$

- For an _ordered crystal_, one expects the presence of _Bragg peaks_:
$$\rho_{k_n} = \begin{cases}
N & n = 0 \mod N \\
0 & \text{ otherwise}
\end{cases}$$
- For the quantum mechanical ground state, evaluate:
$$\langle{0}\rvert \rho_q \rho_{-q} \lvert{0}\rangle = \sum_{j,k=1}^N \langle{0}\rvert \exp(iq[x_j-x_k])\lvert{0}\rangle$$

$$\langle{0}\rvert \rho_q \rho_{-q} \lvert{0}\rangle = \sum_{j,k=1}^N \exp\left(iqa[j-k]-\frac{q^2}{2mN}\sum_{|n| \leq (N-1)/2} \frac{1-\cos\left(\eta_n[j-k]\right)}{\omega(\eta_n)}\right)$$
- _Bragg peaks_ are _replaced_ with _cusps_ due to the second exponent
- _Long range order_ is destroyed in one dimension
![[1D Bragg peaks.png]]
- Taking the $N\to \infty$ limit with $|j-k|\gg 1$, _near_ the first Bragg peak, using the same sum as in the [[#Position fluctuations]], the second sum is:
$$\exp(i\Delta qa[j-k])|j-k|^{-2\pi l_\text{osc}^{2}/a^{2}}$$
- $\Delta q$ is the _deviation_ of $q$ from the first Bragg peak
- This gives:
$$\braket{ 0|\rho_{q}\rho_{-q} |0  } \sim(\Delta q)^{-1+2\pi l_\text{osc}^{2}/a^{2}}$$
- This _widens_ the peak, with _increasing disorder_ as $l_\text{osc}/a$ _increases_ due to quantum fluctuations

- The _prevention_ of crystalisation forms _quantum liquids_

- In _higher dimensions_, crystals can _stay in ordered configurations_
# Spin models
- Ising model:
$$H = J\sum_{\langle j\,k\rangle} \sigma_j \sigma_k$$
- Here, the spins take $\sigma_{j}=\pm{1}$
- Summed with _nearest neighbours_
- $J<0$ leads to _ferromagnetism_

## States and operators
- For $N$ spins, use the $s^{z}$ basis with eigenstates $\psi_{\pm}$
$$s^{z}\ket{\psi_{\pm}} =\pm \frac{1}{2}\ket{\psi_{\pm}} $$
- The general state has $2^{N}$ components, with a basis of _product states_:
$$\lvert{\Psi}\rangle=\sum_{\{\sigma_j=\pm\}}\Psi_{\sigma_1\cdots \sigma_N}\lvert{\sigma_1}\rangle\lvert{\sigma_2}\rangle\cdots \lvert{\sigma_N}\rangle$$
- The spin operators:
$$[s^{a}_{j}, s^{b}_{k}]=i\varepsilon_{abc}s^{c}_{j}\delta_{jk}$$
- The Ising model is then:
$$H=4J\sum_{\langle jk \rangle } s_{j}^{z}s_{k}^{z}$$
- The model does not respect rotational symmetry

## Heisenberg ferromagnetic chain
$$H=J\sum_{\langle jk \rangle } \boldsymbol{s}_{j}\cdot \boldsymbol{s}_{k}$$
- A _rotationally symmetric_ model

- Take the _1D spin chain_:
$$H = J \sum_{j=1}^N \mathbf{s}_j \cdot \mathbf{s}_{j+1}$$
- Convenient identity:
$$\boldsymbol{s}_{i}\cdot \boldsymbol{s}_{j}=s_{i}^{z}s_{j}^{z}+\frac{1}{2}(s_{i}^{+}s_{j}^{-}+s^{-}_{i}s_{j}^{+})$$
- Periodic boundary conditions: $\boldsymbol{s}_{j}=\boldsymbol{s}_{j+N}$

### Ground states
- The _ferromagnet_ state, with _all spins aligned_
	- It _breaks_ rotational symmetry
$$\ket{\text{FM}}\equiv \ket{+}_{1}\ket{+}_{2}\dots\ket{+}_{N} $$
- It is an eigenstate of the Hamiltonian with eigenvalue $JN/4$

- Consider the _total spin_ $\boldsymbol{S}$
- An eigenstate of $S^{z}$ and $S^{2}$, with eigenvalues $N/2$ and $(N/2) (N/2+1)$
- $S^{x},S^{y},S^{z}$ _all commute_ with $H$ due to rotational invariance

- This suggests that $\ket{\text{FM}}$ is part of a _multiplet_ of $N+1$ states
- $S^{-}\ket{\text{FM}}$ is _also an eigenstate of the Hamiltonian_
$$S^-\lvert{\text{FM}}\rangle = \sum_{j=1}^N s^-_j\lvert{\text{FM}}\rangle = \sum_{j=1}^N \lvert{+}\rangle_1\lvert{+}\rangle_2\cdots \lvert{+}\rangle_{j-1} \lvert{-}\rangle_j\lvert{+}\rangle_{j+1}\cdots \lvert{+}\rangle_N$$
- Then, $(S^{-})^{2}\ket{\text{FM}}$ is a _constant amplitude superposition_ of states with _two spins flipped_
	- Double sum with $j\neq k$, always _exactly two spins_ flipped
- Continuing, $(S^{-})^{N}\ket{\text{FM}}$ is _all spins pointing down_
- This _degenerate set_ of ground states corresponds to _rotational invariance_ in classical mechanics

### First excited state
- Consider state:
$$\lvert{j}\rangle = \lvert{+}\rangle_1\lvert{+}\rangle_2\cdots \lvert{+}\rangle_{j-1} \lvert{-}\rangle_j\lvert{+}\rangle_{j+1}\cdots \lvert{+}\rangle_N$$
- Acting on it with the Hamiltonian:
	- Set $J=-1$
$$H\lvert{j}\rangle = (1-N/4) \lvert{j}\rangle - \frac{1}{2}\left(\lvert{j-1}\rangle+\lvert{j+1}\rangle\right).$$
- State is put into the _subspace_ spanned by set of states $\ket{j}$, with $S^{z}=N/2-1$
	- The Hamiltonian _conserves number_

- $H$ can be _diagonalised_ by noting that like the [[#Classical treatment|phonon case]], it is a _circulant matrix_
- Eigenstates are _plane waves_:
$$\ket{\eta}=\frac{1}{\sqrt{ N }} \sum_{j} \exp(i\eta j)\ket{j} \quad,\quad \eta=\frac{2\pi n}{N}  $$
- Eigenvalues of the Hamiltonian:
$$E=E_{0}+\omega(\eta)$$
- The _dispersion relation_ is now _quadratic_
$$\omega(\eta)=2|J|\sin^{2} \frac{\eta}{2}$$
- _Long wavelength_ excitations that break symmetries have _gapless dispersion relations_, as a result of [[Classical Field Theory#Goldstone's Theorem|Goldstone's Theorem]]

- There are $N$ one-magnon states out of $2^{N}$ states of the system

- The down spins propagate as _magnons_

### N-magnon states
- A magnon has energy $\propto|J|$
- Systems of _extensive_ energy and finite temperature will have _many_ magnons

- For $n$ flipped spins, the _dimension_ of the subspace is $\pmatrix{N \\ n}$

- Magnons _cannot sit on the same site_, and can _scatter_

### Anti-ferromagnets
- Anti-ferromagnet: the _ground state_ for $J>0$
$$\lvert{\text{AFM}}?\rangle  \equiv \lvert{+}\rangle_1\lvert{-}\rangle_{2}\cdots \lvert{+}\rangle_{N-1}\lvert{-}\rangle_{N}$$
- _Not_ an eigenstate of the Hamiltonian 
	- Flipping spins moves them around, more akin to a _dense gas of interacting magnons_

- For the 1D chain, _quantum fluctuations_ are too strong for anti-ferromagnetic order

- In _higher dimensions_, the _Neel state_ may be a ground state for the AFM

## Large s expansion
- _Generalise_ to $s> 1/2$, and develop _approximations_ on $s\gg 1/2$
	- Some _qualitative_ behaviour may still hold for $s= 1/2$

### Holstein-Primakoff approximation
- A _non-linear map_ between spin and the _harmonic oscillator_
$$\begin{align}
s^+ &=\sqrt{2s}\sqrt{1-\frac{a^\dagger a}{2s}}a \\
s^- &= \sqrt{2s}a^\dagger\sqrt{1-\frac{a^\dagger a}{2s}} \\
s^z &= \left(s - a^\dagger a\right)
\end{align}$$
- The spin commutation relations are _preserved_ for $[a,a^{\dagger}]=1$
- Raising and lowering spins become _analagous_ to removing/adding quanta, with a _factor_ dependent on the _number_ of quanta, such that $(s^{\pm})^{s+1}=0$

- Interpretation:
	- A _classical spin_ is described as a point on sphere of radius $s$
	- For lage $s$, locally approximate with a _plane_
	- Near the North pole, since $[s^{x},s^{y}]=is^{z}\sim s$, analagous to $[x,p]=i$
	- Hence, $s^{\pm}$ analagous to ladder operators

### Large s spin waves
- Large $s$ approximation: neglect terms of order $s^{-1/2}$
- Staying near the North Pole with _few oscillator quanta_

- Hamiltonian, _discarding_ the lower values of $s$
$$H \sim NJs^2 + sJ\sum_j \left[a^\dagger_ja^{\vphantom{\dagger}}_{j+1}+a^\dagger_{j+1}a^{\vphantom{\dagger}}_j - 2a^\dagger_ja^{\vphantom{\dagger}}_j\right]$$
- $s^{2}$ part: the $s^{z}s^{z}$ interaction
- The state with _no quanta_ is then an eigenstate
	- A _generalisation_ of the _ferromagnetic state_ with _aligned spins_ at $m_{s}=s$, the _ground state_ for $J<0$

- Writing in terms of $x$ and $p$:
$$\begin{align}
s^x &\sim \sqrt{s}x \\
s^y &\sim  \sqrt{s}p\\
s_z &= \left(s - \frac{1}{2}[x^2 + p^2 - 1] \right)
\end{align}$$
- The Hamiltonian:
$$H\sim NJ s^2 + sNJ+ \overbrace{sJ \sum_{j=1}^N \left[x_j x_{j+1} + p_j p_{j+1}-x_j^2 - p_j^2\right]}^{\equiv H^{(2)}} + \ldots$$
- The quadratic part is a _harmonic chain_

- Use the _Fourier expansions_:
$$\begin{align}
x_j(t) &= \frac{1}{\sqrt{N}}\sum_{|n| \leq (N-1)/2} q_n(t) e^{i\eta_n j}\\
p_j(t) &= \frac{1}{\sqrt{N}}\sum_{|n| \leq (N-1)/2} \pi_n(t) e^{-i\eta_n j}
\end{align}$$
- The Hamiltonian is then:
$$H^{(2)}=-2sJ\sum_{|n|<(N-1)/2} \sin^{2}\left( \frac{\eta_{n}}{2} \right)(q_{n}q_{-n}+\pi_{n}\pi_{-n})$$

- One _regains_ the dispersion relation:
	- Approximation is still for _few oscillator quanta_
$$\omega_{\text{FM}}(\eta) = 4s\left|J\right|\sin^2(\eta/2)$$
### Anti-ferromagnetic case
- For the _ferromagnet_, _close to ground state_, the harmonic approximation _applies_

- The anti-ferromagnetic state has _many flipped spins_ to make it "far away" from FM state

- Therefore, _rotate every other spin_ through $\pi$ about the $y$ axis:
$$(s_{j}^{x},s_{j}^{y},s_{j}^{z})\to (-s_{j}^{x},s_{j}^{y},-s_{j}^{z})\quad j\text{ odd}$$
- This _changes the Hamiltonian_:
$$H = -J \sum_{j=1}^N \left[s^x_j s^x_{j+1} - s^y_j s^y_{j+1} + s^z_j s^z_{j+1}\right]$$
- Therefore, the _harmonic oscillation applies_ close to the AFM state
$$\displaylines{H^{(2)}=2sJ\sum_{|n|<(N-1)/2}\left[ \sin^{2}\left( \frac{\eta_{n}}{2} \right)q_{n}q_{-n}+\cos^{2}\left( \frac{\eta_{n}}{2} \right)\pi_{n}\pi_{-n} \right] \\ \omega_{\text{AFM}}(\eta) = 2sJ\left|\sin(\eta)\right|}$$
- _Vanishes_, and is _linear_ at $\eta=0$ and $\eta=\pi$

- Ferromagnet: _both_ position and momentum terms _vanish_ at $\eta=0$
- Anti-ferromagnet: _either_ position or momentum vanish at $\eta=0$ or $\eta=\pi$

- For the anti-ferromagnet, the _size_ of the unit cell is _doubled_, therefore _halving_ the period
### Ground state fluctuations
- Crude approximation:
$$\braket{ \text{FM}|s_{j}^{z} | \text{FM} } =s \qquad \braket{ \text{AFM}|s_{j}^{z} | \text{AFM} } =s(-1)^{j}$$
- In Holstein-Primakoff, there is an _additional term_
$$s_{j}^{z}=s-a_{j}^{\dagger}a_{j}$$
- FM: commutes with Harmonic Hamiltonian, hence _no fluctuations_

- AFM: does not commute due to $a_{j}a_{j+1}$ terms

- AFM: evaluate $\Delta s=\braket{ 0|a_{j}^{\dagger}a_{j} | 0 }$

$$\begin{align}
\Delta s &= - \langle{0}\rvert\frac{1}{N}\sum_{j=1}^N a^\dagger_j a^{\vphantom{\dagger}}_j\lvert{0}\rangle\\
&= \frac{1}{2}-\frac{1}{4N}\sum_n \left[|\tan(\eta_n/2)| + |\cot(\eta_n/2)|\right]\\
&= \frac{1}{2}- \frac{1}{4}\int_{-\pi}^\pi \frac{d\eta}{2\pi} \left[|\tan(\eta_n/2)| + |\cot(\eta_n/2)|\right]
\end{align}$$
- There must be a _cutoff_ for the integral to stop the divergence
- From this, one gets:
$$\Delta s\sim -\log \eta _\text{min}\sim -\log \left( \frac{2\pi}{N} \right)\sim \log N$$
- In 1D, there is _no long-range antiferromagnetic order_
# Second quantisation and correlations
- Use language of [[Second quantisation]]

## Particles and states
- _Bosons_:
$$\displaylines{\left[a^{\vphantom{\dagger}}_\alpha,a^{\vphantom{\dagger}}_\beta\right]=0,\quad \left[a^\dagger_\alpha,a^\dagger_\beta\right]=0,\quad \left[a^{\vphantom{\dagger}}_\alpha,a^\dagger_\beta\right] = \delta_{\alpha\beta} \\ \left[\psi^{\vphantom{\dagger}}(\mathbf{r}_1),\psi^\dagger(\mathbf{r}_2)\right]=\delta(\mathbf{r}_1-\mathbf{r}_2)\\
\left[\psi^{\vphantom{\dagger}}(\mathbf{r}_1),\psi^{\vphantom{\dagger}}(\mathbf{r}_2)\right]=\left[\psi^\dagger(\mathbf{r}_1),\psi^\dagger(\mathbf{r}_2)\right]=0}
$$
- Action on a product state:
$$\displaylines{\ket{\Psi}\leftrightarrow  \Psi(x_{1},\dots x_{N}) \\ \psi(x)\ket{\Psi} \leftrightarrow  \sqrt{ N }\Psi(x,x_{1},\dots x_{N-1})  }$$

- _Fermions_:
$$\displaylines{\left\{a^{\vphantom{\dagger}}_\alpha,a^{\vphantom{\dagger}}_\beta\right\}=0,\quad \left\{a^\dagger_\alpha,a^\dagger_\beta\right\}=0,\quad \left\{a^{\vphantom{\dagger}}_\alpha,a^\dagger_\beta\right\} = \delta_{\alpha\beta} \\ \left\{\psi^{\vphantom{\dagger}}(\mathbf{r}_1),\psi^\dagger(\mathbf{r}_2)\right\}=\delta(\mathbf{r}_1-\mathbf{r}_2)\\
\left\{\psi^{\vphantom{\dagger}}(\mathbf{r}_1),\psi^{\vphantom{\dagger}}(\mathbf{r}_2)\right\}=\left\{\psi^\dagger(\mathbf{r}_1),\psi^\dagger(\mathbf{r}_2)\right\}=0}$$

- Constructing _product states_:
$$\lvert{\mathbf{N}}\rangle \equiv \prod_\alpha \frac{\left(a^\dagger_\alpha\right)^{N_\alpha}}{\sqrt{N_\alpha!}}\lvert{\text{VAC}}\rangle$$

- For _fermions_, the _ground state_ is the _Fermi sea_:
$$\ket{\text{Fermi sea}}=\prod_{|\boldsymbol{k}|<k_{F}}a_{\boldsymbol{k}}^{\dagger}\ket{\text{VAC}}  $$
## Representation of operators
- Second quantised _one particle operators_:
$$\hat A = \sum_{\alpha\beta}A_{\alpha\beta}a^\dagger_\alpha a^{\vphantom{\dagger}}_\beta$$
- Matrix element between _product states_:
$$\displaylines{\langle{\mathbf{N}}\rvert \hat A \lvert \mathbf{N'} \rangle = A_{\alpha\beta} \sqrt{N_\alpha N'_\beta} \\ N_{\beta}=N_{\beta}'-1 \qquad N_{\alpha}=N_{\alpha}'+1}$$
### Hamiltonian
- The _single particle Hamiltonian_:
$$\begin{align}
    \mathop{\hat H}&=\int d\mathbf{r}\left[-\frac{1}{2m}\psi^\dagger(\mathbf{r})\nabla^{2}\psi^{\vphantom{\dagger}}(\mathbf{r})+V(\mathbf{r})\psi^\dagger(\mathbf{r})\psi^{\vphantom{\dagger}}(\mathbf{r})\right]\\
                    &=\int d\mathbf{r}\left[\frac{1}{2m}\nabla\psi^\dagger(\mathbf{r})\cdot\nabla\psi^{\vphantom{\dagger}}(\mathbf{r})+V(\mathbf{r})\psi^\dagger(\mathbf{r})\psi^{\vphantom{\dagger}}(\mathbf{r})\right]
\end{align}$$
- From _Heisenberg's equation of motion_, one gets the _time-dependent Schrodinger equation_ for the field operator
$$\begin{equation}
    \begin{split}
    i\partial_{t}\psi^{\vphantom{\dagger}}(\mathbf{r},t) &= -\left[\mathop{\hat H},\psi^{\vphantom{\dagger}}(\mathbf{r},t)\right]\\
    &= -\frac{1}{2m}\nabla^{2}\psi^{\vphantom{\dagger}}(\mathbf{r},t)+V(\mathbf{r})\psi^{\vphantom{\dagger}}(\mathbf{r},t)
    \end{split}
\end{equation}$$
### Single particle density operator
- The [[#Many-body wave-functions|single particle density]] in terms of _field operators_
$$\rho(x)\equiv\delta(x-r)\implies \hat{\rho}(x)\equiv \psi ^{\dagger}(x)\psi(x)$$
- Integrating over position then gives the _total number of particles_:
$$\int  dx\,\psi ^{\dagger}(x)\psi(x)=\sum_{\alpha}a^{\dagger}_{\alpha}a_{\alpha}=\sum_{\alpha}N_{\alpha} $$
- The _expectation value_ for a given product state:
$$\braket{ N_{0},N_{1}\dots |\rho(\boldsymbol{r})| N_{0},N_{1}\dots } =\sum_{\alpha}N_{\alpha}|\varphi_{\alpha}(\boldsymbol{r})|^{2}$$
- Also consider the _Fourier components_:
$$\rho_{\boldsymbol{q}}\equiv \int  d\boldsymbol{r}\,\rho(\boldsymbol{r})\exp(-i\boldsymbol{q}\cdot \boldsymbol{r})=\sum_{\boldsymbol{k}}a^{\dagger}_{\boldsymbol{k}-\boldsymbol{q}}a_{\boldsymbol{k}} $$
- The $q=0$ mode is the _total particle number_
### Single particle current
- The _particle current_, second quantised:
$$\boldsymbol{j}(\boldsymbol{r})=-\frac{i}{2m}[\psi ^{\dagger}(\boldsymbol{r})\nabla \psi(\boldsymbol{r})-\nabla \psi ^{\dagger}(\boldsymbol{r})\psi(\boldsymbol{r})]$$
- The Fourier component:
$$\boldsymbol{j}_{\boldsymbol{q}}\equiv \int  d\boldsymbol{r} \,\boldsymbol{j}(\boldsymbol{r}) \exp(-i\boldsymbol{q}\cdot \boldsymbol{r})=\frac{1}{m}\sum_{\boldsymbol{k}}\left( \boldsymbol{k}-\frac{\boldsymbol{q}}{2} \right)a^{\dagger}_{\boldsymbol{k}-\boldsymbol{q}}a_{\boldsymbol{k}}$$
- The $q=0$ mode is simply _total momentum_ divided by mass

### Single particle density matrix
- In terms of _field operators_, the [[#Many-body wave-functions|single particle density matrix]]:
$$g(\boldsymbol{r},\boldsymbol{r}')=\braket{ \Psi|\psi ^{\dagger}(\boldsymbol{r})\psi (\boldsymbol{r}') | \Psi } $$
- For a _product state_:
$$g(\boldsymbol{r},\boldsymbol{r}')=\sum_{\alpha}N_{\alpha}\varphi_{\alpha}^{*(\boldsymbol{r})}\varphi_{\alpha}(\boldsymbol{r}')$$

### Two particle operators
- Second quantised _two particle operators_:
$$\hat B = \frac{1}{2}\sum_{\alpha\beta\gamma\delta} B_{\alpha\beta,\gamma\delta}a^\dagger_\alpha a^\dagger_\beta a^{\vphantom{\dagger}}_\delta a^{\vphantom{\dagger}}_\gamma$$
- Matrix elements:
$$\displaylines{\langle{\mathbf{N}}\rvert \hat B \lvert \mathbf{N'} \rangle =\left[B_{\alpha\beta,\gamma\delta}\pm B_{\alpha\beta,\delta\gamma}\right] \sqrt{N_\alpha N_\beta N'_\gamma N'_\delta} \\ N_{\gamma ,\delta}=N_{\gamma,\delta}'-1 \qquad N_{\alpha,\beta}=N_{\alpha,\beta}'+1}$$
- A _two-particle interaction Hamiltonian_:
$$\hat H_\text{int.} = \frac{1}{2}\int d\mathbf{r}_1 d\mathbf{r}_2\, U(\mathbf{r}_1-\mathbf{r}_2)\psi^\dagger(\mathbf{r}_1)\psi^\dagger(\mathbf{r}_2)\psi^{\vphantom{\dagger}}(\mathbf{r}_2)\psi^{\vphantom{\dagger}}(\mathbf{r}_1)$$
- It is the _normal ordered_ equivalent of:
$$H_\text{int}=\frac{1}{2}\int  d\mathbf{r}_{1}\,d\mathbf{r}_{2}\,U(\mathbf{r}_{1}-\mathbf{r}_{2}) \rho(\mathbf{r}_{1})\rho(\mathbf{r}_{2})$$
## Correlations
- The [[#Many-body wave-functions|pair distribution function]]:
$$\rho_2(x,y) =\langle{\Psi}\rvert \psi^\dagger(x)\psi^\dagger(y)\psi^{\vphantom{\dagger}}(y)\psi^{\vphantom{\dagger}}(x) \lvert \Psi \rangle$$
- Evaluate for _product states_, going into the _energy eigenstate_ basis
$$  \rho_2(x,y)=\sum_{\alpha, \beta, \gamma, \delta}\varphi^{*}_{\alpha}(x)\varphi^{*}_{\beta}(y)\varphi^{}_{\gamma}(y)\varphi^{}_{\delta}(x)\langle{\Psi}\rvert a^\dagger_{\alpha}a^\dagger_{\beta}a^{\vphantom{\dagger}}_{\gamma}a^{\vphantom{\dagger}}_{\delta} \lvert \Psi \rangle$$
- The _possibilities_ to sum over are:
	- $\alpha=\beta=\gamma=\delta$ is a _sum over only one index_, which scales with $L$ instead of $L^{2}$ in the continuum limit
	- Does not apply for _Bose condensates_, where one state can have a significant fraction of particles
$$\alpha=\delta,\beta=\gamma \quad \text{ or }\quad \alpha=\gamma,\beta=\delta$$

- Ths results in _Wick's theorem_:
$$\rho_2(x,y) = \rho_1(x)\rho_1(y) \pm g(x,y)g(y,x)$$
- For _Fermi gases_, this shows _exclusion_ as $|x-y|\to 0$
- There are also _liquid-like oscillations_ where there are _particles_, known as _Friedel oscillations_
![[Friedel oscillations.png|400]]
## Interference of Bose-Einstein condensates
- The wave-function for a _Bose condensate_ of ground state $\varphi_{0}(\boldsymbol{r})$
$$\ket{\Psi}=\frac{1}{\sqrt{ N! }} \left( a_{0}^{\dagger} \right)^{N} \ket{\text{VAC}}  $$
- Let there be a Bose-Einstein condensate initially in a _localised trap_
- Let the trap be _released_, and the condensate has some _momentum distribution_

- The mean density:
$$\langle \rho(\boldsymbol{r},t) \rangle = N|\varphi_{0}(\boldsymbol{r},t)|^{2}$$
- Let the state disperse as a _Gaussian_ of initial width $R_{0}$
	- Initial _momentum distribution_ is a Gaussian of width $\hbar/R_{0}$
$$\displaylines{\varphi(\boldsymbol{r},t)=\frac{1}{(\pi R_{t}^{2})^{3/4}}\exp\left[ -\frac{|\boldsymbol{r}|^{2}(1-i\hbar t/mR_{0}^{2})}{2R_{t}^{2}} \right] \\ R_{t}^{2}=R_{0}^{2}+\left( \frac{\hbar t}{mR_{0}} \right)^{2}}$$
- At long times, $R_{t} \sim \hbar t/mR_{0}$, and:
$$|\varphi(\boldsymbol{r},t\to \infty)|^{2} \propto \exp\left[ -\left( \frac{mR_{0}}{\hbar t}|\boldsymbol{r}| \right)^{2} \right]$$
- The _final density distribution_ simply reflects the _initial momentum distribution_
### Interference
- Let there be two wells separated by displacement $\boldsymbol{d}$
- Let the condensates in the wells have _relative phase_ $\theta$, and population $N_{L},N_{R}$
	- Can be accomplished by _adiabatically separating_ one well
- They separately evolve as:
$$\displaylines{\varphi_{L/R}(\boldsymbol{r},t)=\frac{1}{(\pi R_{t}^{2})^{3/4}}\exp\left[ -\frac{|\boldsymbol{r}\pm \boldsymbol{d}/2|^{2}(1-i\hbar t/mR_{0}^{2})}{2R_{t}^{2}} \right] \\ |\varphi_{L/R}(\boldsymbol{r},t\to \infty)|^{2} \propto \exp\left[ -\left( \frac{mR_{0}}{\hbar t}|\boldsymbol{r}\pm \boldsymbol{d}/2| \right)^{2} \right]}$$

- The initial state:
$$\ket{N_{L},N_{R}}_{\theta}=\frac{1}{\sqrt{ N! }}\left[ \sqrt{ \frac{N_{L}}{N} }\exp\left( -\frac{i\theta}{2} \right)a_{L}^{\dagger}+\sqrt{ \frac{N_{R}}{N} }\exp\left( \frac{i\theta}{2} \right)a_{R}^{\dagger} \right]^{N}\ket{\text{VAC}}  $$
- Single particle density:
$$\displaylines{\rho(\boldsymbol{r})=\psi ^{\dagger}(\boldsymbol{r})\psi(\boldsymbol{r}) \hspace{1cm} \psi(\boldsymbol{r})=\varphi_{L}(\boldsymbol{r})a_{L} +\varphi_{R}(\boldsymbol{r})a_{R}\\ \begin{align}
\langle \rho(\boldsymbol{r},t) \rangle_{\theta}&=N_{L}|\varphi_{L}(\boldsymbol{r},t)|^{2}+N_{R}|\varphi_{R}(\boldsymbol{r},t)|^{2}+2\sqrt{ N_{L}N_{R} }\mathrm{Re}[e^{i\theta}\varphi_{L}^{*}(\boldsymbol{r},t)\varphi_{R}(\boldsymbol{r},t)] \\ &=N_{L}|\varphi_{L}(\boldsymbol{r},t)|^{2}+N_{R}|\varphi_{R}(\boldsymbol{r},t)|^{2}+\rho_{\text{int}}(\boldsymbol{r},t)
\end{align}} $$
- As the condenstaes _overlap_, the latter term indicates _interference_, dependent on the _relative phase_
$$\displaylines{\rho_{\text{int}}(\boldsymbol{r},t)=A(\boldsymbol{r},t)\cos\left[ \theta+\frac{\hbar \boldsymbol{r}\cdot \boldsymbol{d}}{mR_{0}^{2}R_{t}^{2}}t \right] \\ A(\boldsymbol{r},t)=\frac{2\sqrt{ N_{L}N_{R} }}{\pi^{3/2}R_{t}^{3}}\exp\left( -\frac{\boldsymbol{r}^{2}+\boldsymbol{d}^{2}/4}{R_{t}^{2}} \right)}$$
- At _long times_, the interference fringes have separation $2\pi \hbar t/md$

- This is the _Hanbury Brown and Twiss effect_
### With Fock states
- Let the two wells have _no phase relation_ to each other
	- Made up of _Fock states_
$$\ket{N_{L},N_{R}}_{F} = \frac{1}{\sqrt{ N_{L}!N_{R}!}} (a_{L}^{\dagger})^{N_{L}}(a_{R}^{\dagger})^{N_{R}}\ket{\text{VAC}}  $$
- In this case:
	- $\langle \rho \rangle$ only the _expected value_ of many measurements
$$\langle \rho(\boldsymbol{r},t) \rangle_{F}=N_{L}|\varphi_{L}(\boldsymbol{r},t)|^{2}+N_{R}|\varphi_{R}(\boldsymbol{r},t)|^{2} $$
- However, the _correlation_ shows interference fringes which _depend on the correlation distance_
$$\begin{align}
\langle :\rho(\boldsymbol{r})\rho(\boldsymbol{r}') :\rangle = &\langle \rho (\boldsymbol{r}) \rangle_{F} \langle \rho(\boldsymbol{r}') \rangle_{F} + N_{L}N_{R} \varphi_{L}^{*}(\boldsymbol{r})\varphi_{R}^{*}(\boldsymbol{r}')\varphi_{L}(\boldsymbol{r}')\varphi_{R}(\boldsymbol{r}')  \\
 &+N_{L}N_{R}  \varphi_{R}^{*}(\boldsymbol{r})\varphi_{L}^{*}(\boldsymbol{r}')\varphi_{R}(\boldsymbol{r}')\varphi_{L}(\boldsymbol{r}')  
\end{align}$$
- In _each measurement_, there will be _fringes_ but with a _random phase_


- _Expectation values_ for a system of a Fock state are identical to a _relative phase state after averaging_
$$\displaylines{\begin{align}
\rho&=\int \, \frac{d\theta}{2\pi} \ket{N_{L},N_{R}}_{\theta}\bra{N_{L},N_{R}}_{\theta} \\ &= \frac{1}{ N! } \sum_{n} \ket{n,N-n} \bra{n,N-n} 
\end{align} \\ \ket{n,N-n}=\pmatrix{N \\ n} (a_{L}^{\dagger})^{n}(a_{R}^{\dagger})^{N-n}\ket{\text{VAC}}  }  $$
### Distinguishing between momentum distributions
- Distinguish between the _Bose-Einstein condensate_ (sharp in momenta) and the _Mott insulator_ (sharp in position)
- The single particle density:
$$\displaylines{\hat{\psi}(x,t)=\frac{1}{\sqrt{ N }}\sum_{j=1}^{N} \varphi_{j}(x,t)a_{j} \\ \rho(x,t)=\psi ^{\dagger}(x,t)\psi(x,t) \\ \langle  \rho(x,t)\rangle = \frac{1}{N}\sum_{j,k} \varphi_{j}^{*}\varphi_{k}\langle a_{j}^{\dagger}a_{k} \rangle }$$

- In the far field, this evolves as
$$\varphi_{j}^{*}\varphi_{k} \sim\exp\left( \frac{(x_{j}-x_{k})x_{0}\alpha}{\hbar t} \right)$$
- For a _Bose-Einstein condensate_, $\langle a_{j}^{\dagger}a_{k} \rangle \sim N/L$ (long range order)
- There is _interference_ between different sites
- There is a _narrow peak_ in momentum space distribution

- For a _Mott insulator_, $\langle a_{j}^{\dagger}a_{k} \rangle = (N/L)\delta_{jk}$
- They are _localised_ in position space


## Hartree-Fock theory
- The _interaction Hamiltonian_:
$$\begin{align}
H_\text{int}&= \frac{1}{2} \int  \, d\boldsymbol{r}\,d\boldsymbol{r}' :\rho(\boldsymbol{r})U(\boldsymbol{r}-\boldsymbol{r}')\rho(\boldsymbol{r}'):\\&=\frac{1}{2}\int  \, d\boldsymbol{r}\,d\boldsymbol{r}' \psi ^{\dagger}(\boldsymbol{r})\psi ^{\dagger}(\boldsymbol{r}')U(\boldsymbol{r}-\boldsymbol{r}')\psi(\boldsymbol{r}')\psi(\boldsymbol{r}) 
\end{align} $$
- Then from _Wick's Theorem_, for a _product state_:
$$\begin{align}
    \langle \hat V\rangle &= \overbrace{\frac{1}{2}\int d\mathbf{r}\, d\mathbf{r}'\, \rho_1(\mathbf{r}) U(\mathbf{r}-\mathbf{r}')\rho_1(\mathbf{r}')}^{\equiv E_\text{Hartree}} \\
    &\qquad\overbrace{\pm \frac{1}{2}\int d\mathbf{r}\, d\mathbf{r}'\,  U(\mathbf{r}-\mathbf{r}')g(\mathbf{r},\mathbf{r}')g(\mathbf{r}',\mathbf{r})}^{\equiv E_\text{Fock}}
\end{align}$$
- The _Hartree-Fock method assumes_ the state is a _product state_

- Translationally invariant Hamiltonian

### Hartree-Fock for the electron gas
- _Fermions_:
$$\begin{gather}
    \left\{\psi^{\vphantom{\dagger}}_{\sigma_1}(\mathbf{r}_1),\psi^\dagger_{\sigma_2}(\mathbf{r}_2)\right\}=\delta_{\sigma_1\sigma_2}\delta(\mathbf{r}_1-\mathbf{r}_2)\\
    \left\{\psi^{\vphantom{\dagger}}_{\sigma_1}(\mathbf{r}_1),\psi^{\vphantom{\dagger}}_{\sigma_2}(\mathbf{r}_2)\right\}=\left\{\psi^\dagger_{\sigma_1}(\mathbf{r}_1),\psi^\dagger_{\sigma_2}(\mathbf{r}_2)\right\}=0
\end{gather}$$
- The _density matrix_ is in both _spin space_ and _real space_
$$g_{\sigma_1\sigma_2}(\mathbf{r}_1,\mathbf{r}_2) = \langle{\Psi}\rvert \psi^\dagger_{\sigma_1}(\mathbf{r}_1)\psi^{\vphantom{\dagger}}_{\sigma_2}(\mathbf{r}_2) \lvert \Psi \rangle$$
- One can find both the _density_, and the _spin density_
	- Latter is a _vector_, corresponding to _magnetisation_
$$\mathbf{\rho}(\mathbf{r}) = \mathrm{Tr}\left[g(\mathbf{r},\mathbf{r})\right],\quad \mathbf{s}(\mathbf{r}) = \frac{1}{2}\mathrm{Tr}\left[\boldsymbol{\sigma}g(\mathbf{r},\mathbf{r})\right].$$
- For a _spin-independent interaction_:
$$\hat H_\text{int.} = \frac{1}{2}\sum_{\sigma_1,\sigma_2}\int d\mathbf{r}_1 d\mathbf{r}_2\, U(\mathbf{r}_1-\mathbf{r}_2)\psi^\dagger_{\sigma_1}(\mathbf{r}_1)\psi^\dagger_{\sigma_2}(\mathbf{r}_2)\psi^{\vphantom{\dagger}}_{\sigma_2}(\mathbf{r}_2)\psi^{\vphantom{\dagger}}_{\sigma_1}(\mathbf{r}_1)$$
- Considering _all spin combinations_:
$$\begin{align}
    \langle \hat H_\text{int.}\rangle &=\frac{1}{2}\int d\mathbf{r}\, d\mathbf{r}'\, \rho(\mathbf{r}) U(\mathbf{r}-\mathbf{r}')\rho(\mathbf{r}')\\
    &- \frac{1}{2}\int d\mathbf{r}\, d\mathbf{r}'\,  U(\mathbf{r}-\mathbf{r}')\mathrm{Tr}\left[g(\mathbf{r},\mathbf{r}')g(\mathbf{r}',\mathbf{r})\right]
\end{align}$$
- Rewrite the _Fock term_ using the identity:
$$\delta_{ab}\delta_{cd} = \frac{1}{2}\left[\boldsymbol{\sigma}_{a c}\cdot \boldsymbol{\sigma}_{d b} + \delta_{ac}\delta_{db}\right]$$
$$\begin{align}
E_{\text{Fock}} &=-\frac{1}{4} \int d\mathbf{r}\, d\mathbf{r}'\,  U(\mathbf{r}-\mathbf{r}')\mathrm{Tr}\left[g(\mathbf{r},\mathbf{r}')\right]\mathrm{Tr}\left[g(\mathbf{r}',\mathbf{r})\right]\\&-\frac{1}{4}\int d\mathbf{r}\, d\mathbf{r}'\,  U(\mathbf{r}-\mathbf{r}')\mathrm{Tr}\left[\boldsymbol{\sigma}g(\mathbf{r},\mathbf{r}')\right]\cdot\mathrm{Tr}\left[\boldsymbol{\sigma}g(\mathbf{r}',\mathbf{r})\right]
\end{align}$$
- Model using the _delta function interaction_ $U(\boldsymbol{r})=V_{0}\delta(\boldsymbol{r})$
$$E_{\text{Fock}} =-\frac{V_0}{4} \int d\mathbf{r}\, \rho(\mathbf{r})^2-V_0\int d\mathbf{r}\, \mathbf{s}(\mathbf{r})\cdot\mathbf{s}(\mathbf{r})$$
- For a _repulsion_, the _ferromagnetic state_ becomes favourable
	- For _parallel spins_, the particles are on average _further away_

### Stoner criterion for ferromagnetism
- _Polarising_ spins in the Fermi gas has a _cost in kinetic energy_
- Kinetic energy for a _Fermi gas_, assume _different spin densities_
	- No need to assume quadratic dispersion
$$E_\text{kin}(n_{\uparrow},n_{\downarrow})\propto \frac{L^{3}}{m}(n_{\uparrow}^{5/3}+n_{\downarrow}^{5/3})$$

- Rewrite in terms of _spin polarisation_:
$$\displaylines{P\equiv \frac{n_{\uparrow}-n_{\downarrow}}{n} \\ E_\text{kin}(P)=\frac{E_{K}}{2}[(1+P)^{5/3}+(1-P)^{5/3}]}$$
- Kinetic energy is _minimised_ for _no spin polarisation_

- Meanwhile, the _Hartree-Fock interaction energy_, for the _contact interaction_:
$$E_\text{HF}=\frac{V_{0}L}{2}n^{2}-\frac{V_{0}L^{3}}{2}(n_{\uparrow}^{2}+n_{\downarrow}^{2})=\frac{E_{V}}{2}(1-P^{2})$$
- The interaction energy favours _polarisation_

- The _polarisation_ of the ground state depends on the _relative sizes_ of kinetic and potential energy

### Excited states
- Use the plane wave basis:
$$\begin{align}
    \psi^{\vphantom{\dagger}}(\mathbf{r})\equiv\frac{1}{L^{3/2}}\sum_{\mathbf{k}} \exp(i\mathbf{k}\cdot\mathbf{r})a^{\vphantom{\dagger}}_{\mathbf{k}},\\
  \psi^\dagger(\mathbf{r})\equiv\frac{1}{L^{3/2}}\sum_{\mathbf{k}} \exp(-i\mathbf{k}\cdot\mathbf{r})a^\dagger_{\mathbf{k}}
\end{align}$$
- Represent the _interaction potential_ in terms of the Fourier components:
$$U(\mathbf{r}-\mathbf{r}') = \frac{1}{L^3}\sum_\mathbf{q}\tilde U(\mathbf{q}) \exp(i\mathbf{q}\cdot[\mathbf{r}-\mathbf{r}'])$$
- The _interaction Hamiltonian_ is then:
$$\hat H_\text{int.}  = \frac{1}{2L^3} \sum_{\mathbf{k}_1+\mathbf{k}_2=\mathbf{k}_3+\mathbf{k}_4} \tilde U(\mathbf{k}_1-\mathbf{k}_4) a^\dagger_{\mathbf{k}_1}a^\dagger_{\mathbf{k}_2}a^{\vphantom{\dagger}}_{\mathbf{k}_3}a^{\vphantom{\dagger}}_{\mathbf{k}_4}$$
- Interactions can be represented in terms of _Feynman diagrams_
![[Interaction Feynman diagram.png|400]]
- The _Hartree_ and _Fock_ terms then depend on the _pairings_:
![[Interaction Hartree Fock.png|400]]
$$\langle{\mathbf{N}}\rvert \hat H_\text{int.} \lvert \mathbf{N} \rangle = \frac{1}{2V}\tilde U(0) \sum_{\mathbf{k}_1,\mathbf{k}_2} N_{\mathbf{k}_1}N_{\mathbf{k}_2} - \frac{1}{2V} \sum_{\mathbf{k}_1,\mathbf{k}_2} \tilde U(\mathbf{k}_1-\mathbf{k}_2) N_{\mathbf{k}_1}N_{\mathbf{k}_2}$$
- The _Hartree term_ simply depends on the _total number_ of particles
- The _Fock term_ will depend on _individual occupations_

- _Adding_ a single particle to state $\boldsymbol{k}$ will add _interaction energy_
$$\Delta U_{\mathbf{k}} = \frac{\tilde U(0)}{V} \sum_{\mathbf{k}'} N_{\mathbf{k}'} - \frac{1}{V}\sum_{\mathbf{k}'} \tilde U(\mathbf{k}-\mathbf{k}') N_{\mathbf{k}'}$$
# Hubbard model
- Assume that particles stay in _highly localised orbitals_ on a _lattice_
- In this limit, the _kinetic energy_ of the particles is from a _tight binding Hamiltonian_:
$$H_t = -t \sum_{j} \left[a^\dagger_ja^{\vphantom{\dagger}}_{j+1}+a^\dagger_{j+1}a^{\vphantom{\dagger}}_j\right]$$
## Bose Hubbard model
- Accounting for _on-site interactions_:
$$H = H_t + H_U = -t \sum_{\langle j\,k\rangle}  \left[a^\dagger_ja^{\vphantom{\dagger}}_{k}+a^\dagger_{k}a^{\vphantom{\dagger}}_j\right] + \frac{U}{2}\sum_j \mathsf{N}^{\vphantom{\dagger}}_j(\mathsf{N}^{\vphantom{\dagger}}_j-1)$$

### The Mott state
- Take the $U/t\to \infty$ limit:
$$E(\mathbf{N}) = \frac{U}{2} \sum_j N_j(N_j-1)$$
- For the _ground state_, fill the sites _as uniformly as possible_
- Let the _filling fraction_ be:
$$\nu=\frac{N_\text{particles}}{N_\text{sites}}$$
- For a _non-integer_ value of $\nu$, there will be two different occupation numbers:
$$\displaylines{e(N)=\frac{U}{2}N(N-1) \\ \frac{E_0}{N_\text{sites}} = \left(\nu - \lfloor \nu\rfloor\right)e(\lceil \nu\rceil) + \left(\lceil \nu\rceil - \nu\right)e(\lfloor \nu\rfloor)}$$
- Therefore, the _chemical potential_ $\nu$ is _piece-wise constant_
$$\mu = e(\lceil \nu\rceil) -e(\lfloor \nu\rfloor)=U\lfloor \nu\rfloor$$
![[Mott state mu.png|500]]

- States of _integer filling_ $\nu$ correspond to _Mott states_
	- If interactions dominate, even if _band theory_ demands a metal be an insulator, a _Mott insulator_ can form instead

### Effect of hopping
- _Start_ from the Fock states, then tune $H_{t}$ back on as a _perturbation_
$$H_t = -t \sum_{j} \left[a^\dagger_ja^{\vphantom{\dagger}}_{j+1}+a^\dagger_{j+1}a^{\vphantom{\dagger}}_j\right]$$
- The _unperturbed eigenstates_:
$$\ket{\boldsymbol{N}}= \bigotimes_{j} \ket{N_{j}}_{j}  $$
- Then _applying_ to $H_{t}$, one gets a _superposition_ of states with particles _moved to adjacent sites_
	- A _Mott state_ is entirely _unchanged_ by the perturbation

- For a _Mott state_ of $\nu=N$, with _one extra particle_, there are $N_\text{sites}$ _degenerate ground states_, which are _mixed_ by $H_{t}$
- The _excited states_ are _separated_ from the ground states with energies $\sim U$

- States in the _ground state multiplet_:
$$\ket{i,+}\equiv\frac{a_{i}^{\dagger}}{\sqrt{ N+1 }} \bigotimes_{j} \ket{N}_{j}   $$
- The _matrix elements_ for _adjacent states_:
$$\braket{ j|H_{t} | k } =-t(N+1)$$
- $H_{t}$ in the _multiplet subspace_ can then be written as:
$$H_{t}|_{+}=-t(N+1)\sum_{\braket{ jk   } } [\ket{j,+}\bra{ k,+} +\text{h.c.} ]$$
- There is an _extra factor_ of $N$ due to _Bose statistics_
- The _splitting_ of degenerate states in $d$ dimensions is then given by the _tight binding dispersion_:
$$\omega_{+}(\boldsymbol{\eta})=-2t(N+1)\sum_{n=1}^{d}\cos \eta_{n}$$
- Alternatively, _removing_ particles from Mott state $\nu=N$:
$$\displaylines{\ket{i,-}\equiv \frac{a_{i}}{\sqrt{ N }} \bigotimes_{j}\ket{N}_{j} \\ H_{t} | _{-}=-tN\sum_{\braket{ jk } }[\ket{j,-}\bra{k,-}+\text{h.c.}  ] \\ \omega_{-}(\boldsymbol{\eta})=-2tN\sum_{n=1}^{d}\cos \eta_{n} }$$

### Ground state with hopping perturbation
- Consider the _grand canonical Hamiltonian_:
$$\mathcal{H}_{\mu}=H-\mu N_\text{particles}$$
- For $t=0$ for a _Mott state_ of $\nu=N$:
$$\frac{\varepsilon_{\mu}^{(N)}}{N_\text{sites}}=\frac{U}{2}N(N-1)-\mu N$$
- At $\mu=U N$ for $t=0$, $\varepsilon_{\mu}^{(N)}$ and $\varepsilon_{\mu}^{(N+1)}$ become _degenerate_ (in terms of $\mathcal{H}_{\mu}$)

- For the _ground state with one extra particle_ on top of $\nu=N$, the ground state is the _bottom of the tight binding band_:
$$\varepsilon_{\mu}^{(N)}+UN-\mu-2td(N+1)$$
- For $t>(UN-\mu)/[2d(N+1)]$, having an _extra particle_ gives _lower energy_

- Meanwhile, _remove_ a particle from $\nu=N+1$:
$$\varepsilon_{\mu}^{(N+1)}-UN+\mu-2td(N+1)$$
- For $t>(\mu-UN)/[2d(N+1)]$, having a _hole_ gives _lower energy_
![[Bose Hubbard ground state.png|500]]

### Ground state phase diagram
- The above is for _low_ $t/U$ where the hopping is a _perturbation_

- For $t/U \to \infty$, the bosons form a _Bose condensate_, where _all particles_ are in the $\eta=0$ state
- For _finite_ but big $t/U$, it forms a _superfluid_
![[Bose Hubbard phase diagram.png|400]]
## Fermi Hubbard model
- Allowing for spin:
	- For _fermions_, spin must be accounted for to have an interacting model
	- Model for _cuprates_
$$H=-t \sum_{\substack{\langle j\,k\rangle\\ s=\uparrow,\downarrow}}  \left[a^\dagger_{j,s}a^{\vphantom{\dagger}}_{k,s}+a^\dagger_{k,s}a^{\vphantom{\dagger}}_{j,s}\right] + U\sum_j N_\uparrow N_\downarrow$$

- Consider $U/t\to \infty$, with _Mott states_ $N=0,1,2$
- The $N=1$ Mott state (_half-filling_) is $2^{N_\text{sites}}-$fold _degenerate_ 

- A site being _double filled_ gives a _spin singlet_
	- Symmetric in site index, therefore _antisymmetric in spin index_

### Two sites, two fermions
- There are $6$ _basis states_:
$$\begin{align}
a^\dagger_{1,\uparrow}a^\dagger_{1,\downarrow} \lvert{\text{VAC}}\rangle,\quad a^\dagger_{2,\uparrow}a^\dagger_{2,\downarrow} \lvert{\text{VAC}}\rangle\\
a^\dagger_{1,s}a^\dagger_{2,s'} \lvert{\text{VAC}}\rangle,\quad s,s'=\uparrow,\downarrow
\end{align}$$
- For states with _two fermions of the same spin_ on _each site_, $H_{t}$ has _no effect_
- Therefore, consider the states:
$$\displaylines{a^{\dagger}_{1,\uparrow}a^{\dagger}_{1,\downarrow}\ket{\text{VAC}}\quad,\quad a^{\dagger}_{2,\uparrow},a^{\dagger}_{2,\downarrow}\ket{\text{VAC}}\quad,\quad a^{\dagger}_{1,\uparrow}a^{\dagger}_{2,\downarrow}\ket{\text{VAC}} \quad,\quad a^{\dagger}_{1,\downarrow}a^{\dagger}_{2,\uparrow}\ket{\text{VAC}}    \\ H=\pmatrix{U&0&t&-t \\ 0&U&t&-t \\ t&t&0&0\\-t&-t&0&0}}$$
- The _off-diagonal terms_ are in _block_ form, which only connects two _sets_ of states:
$$\displaylines{\frac{1}{\sqrt{ 2 }}(a^{\dagger}_{1,\uparrow}a^{\dagger}_{1,\downarrow}+ a^{\dagger}_{2,\uparrow},a^{\dagger}_{2,\downarrow})\ket{\text{VAC}} \qquad \frac{1}{\sqrt{ 2 }}(a^{\dagger}_{1,\uparrow}a^{\dagger}_{2,\downarrow}- a^{\dagger}_{1,\downarrow},a^{\dagger}_{2,\uparrow})\ket{\text{VAC}} \\ H=\pmatrix{U&2t\\2t&0} \\ E=\frac{U}{2}\pm \sqrt{ \frac{U^{2}}{4}+4t^{2} }\xrightarrow{t/U\ll 1}U+\frac{4t^{2}}{U},-\frac{4t^{2}}{U}}$$
- The energy of the spin _triplet_ is unaffected
- The effect of $t$ is to _lower_ the energy of the _singlet_ state relative to the _triplet_ state
### Effective Hamiltonian
- Find an _effective Hamiltonian_ that only _acts_ on the _half-filled Mott states_ in order to describe their _splitting_ for $t/U\ll 1$

- $H_{t}$ takes the state _out_ of the half-filling subspace

- Instead, consider _second order_ degenerate perturbation theory
- Consider representing the Hamiltonian in _block_ form depending on whether or not the matrix elements _act on the Mott state or not_
$$H=\pmatrix{H_\text{Mott}&V\\V^{\dagger}&H_\text{Not}}$$
- Denote the _projection_ operator on the Mott states as $P_\text{Mott}\equiv \mathbb{I}-P_\text{Not}$:
$$\begin{align}
H_\text{Mott}= P_\text{Mott} H P_\text{Mott},\quad H_\text{Not}= P_\text{Not}H P_\text{Not}\\
V^{} = P_\text{Mott} H P_\text{Not},\qquad V^\dagger = P_\text{Not} H P_\text{Mott}
\end{align}$$
- Applying it to the Hubbard model:
$$\begin{align}
H_\text{Mott}= P_\text{Mott} H_U P_\text{Mott},\quad H_\text{Not}= P_\text{Not}H P_\text{Not}\\
V^{} = P_\text{Mott} H_t P_\text{Not},\qquad V^\dagger = P_\text{Not} H_t P_\text{Mott}
\end{align}$$
- Write the _eigenvalue equation_ in block form:
$$\begin{pmatrix}H_{\text{Mott}} & V^{} \\V^\dagger & H_\text{Not} \\\end{pmatrix}\begin{pmatrix}\lvert{\Psi}\rangle\\\lvert{\Phi}\rangle\end{pmatrix} = E\begin{pmatrix}\lvert{\Psi}\rangle\\\lvert{\Phi}\rangle\end{pmatrix}$$
- Eliminating $\ket{\Phi}$:
$$\left[H_{\text{Mott}} -V^{}\left(H_\text{Not}-E\right)^{-1}V^\dagger\right]\lvert{\Psi}\rangle = E\lvert{\Psi}\rangle$$
- Then, apply an _approximation_ where energies are much _smaller_ than the eigenvalues of $H_\text{Not}\sim O(U)$, to get an _effective Hamiltonian_ acting on the _Mott state_:
$$H_\text{eff} = H_{\text{Mott}} -V^{} H^{-1}_\text{Not}V^\dagger$$
- On a _Mott state_, $H_\text{Mott}=0$
- $V^{\dagger}$ creates an _adjacent hole_ and a _doublon_
- $V$ then goes _back_ to the Mott state

- From this, the _effective Hamiltonian_ is:
$$H_\text{eff} = -\frac{V^{}V^\dagger}{U} = -\frac{t^2}{U} \sum_{\substack{\langle j\,k\rangle\\s,s'}} \left[a^\dagger_{j,s}a^{\vphantom{\dagger}}_{k,s} a^\dagger_{k,s'}a^{\vphantom{\dagger}}_{j,s'}+j\leftrightarrow k\right]$$

- Re-ordering the operators:
$$a^\dagger_{j,s}a^{\vphantom{\dagger}}_{k,s} a^\dagger_{k,s'}a^{\vphantom{\dagger}}_{j,s'} = -a^\dagger_{j,s}a^{\vphantom{\dagger}}_{j,s'}a^\dagger_{k,s'}a^{\vphantom{\dagger}}_{k,s} + \delta_{s^{}s'}a^\dagger_{j,s}a^{\vphantom{\dagger}}_{j,s'}\qquad j\neq k$$
- Use the identity:
$$\delta_{ab}\delta_{cd} = \frac{1}{2}\left[\boldsymbol{\sigma}_{a d}\cdot \boldsymbol{\sigma}_{c b} + \delta_{ad}\delta_{cb}\right]$$
- Then in $d$ dimensions:
$$H_\text{eff} = -\frac{dN_\text{sites}t^2}{U}+J\sum_{\langle j\,k\rangle} \mathbf{s}_j\cdot \mathbf{s}_k$$
- Here, $J$ is the _coupling_ $4t^{2}/U$
- The _spin operators_:
$$\mathbf{s}_j=\frac{1}{2}\sum_{s,s'}a^\dagger_{j,s}\boldsymbol{\sigma}_{s^{}s'}a^{\vphantom{\dagger}}_{j,s'}$$

- It is the _Hamiltonian_ of the [[#Heisenberg ferromagnetic chain|spin-1/2 Heisenberg model]]
- A consequence of the _Jordan-Schwinger map_ as the _commutation relations_ hold in the second quantised form

### Doping
- At half-filling, from the above model, cuprates are _anti-ferromagnetic Mott insulators_

- When a cuprate is _doped_, electrons and holes are _introduced_, and can be modelled by the Hubbard Hamiltonian
- _Freely moving_ holes will _destroy_ anti-ferromagnetic order and give rise to superconductivity

- The _effective Hamiltonian_ for the _doped Mott insulator_:
$$H_\text{eff} = -t \sum_{\substack{\langle j\,k\rangle\\ s=\uparrow,\downarrow}}  \left[a^\dagger_{j,s}a^{\vphantom{\dagger}}_{k,s}+a^\dagger_{k,s}a^{\vphantom{\dagger}}_{j,s}\right] + J\sum_{<j\,k>}\left[\mathbf{s}_j\cdot \mathbf{s}_k - \frac{N_j N_k}{4}\right]$$


# Bose Gas
- _Non-interacting Bose gases_ will form a _Bose condensate_
- This state is modified by _interactions_, and can lead to _superfluidity_

## Gross-Pitaevskii approximation
- A _variational approach_
- Start with the _Bose condensate_, as the _ground state_ of a _non-interacting Hamiltonian_
$$\Psi(\mathbf{r}_1,\ldots \mathbf{r}_N) = \prod_{j=1}^N \varphi_0(\mathbf{r}_i)= \frac{1}{\sqrt{N!}}\left(a^\dagger(\varphi_0)\right)^N\lvert{\text{VAC}}\rangle$$
- Add the _two-body interaction Hamiltonian_
- For the ground state in this case, use the _Bose-Einstein form_ with $\varphi_{0}$ as the _variational function_
	- A Bose version of Hartree-Fock
	- $\varphi_{0}$ then obeys the _Gross-Pitaevskii equation_

- Let there be the short range interaction:
$$\displaylines{U(\boldsymbol{r}-\boldsymbol{r}')=U_{0}\delta(\boldsymbol{r}-\boldsymbol{r}') \\ \begin{align}
\langle{\Psi}\rvert H \lvert \Psi \rangle=N \int d\mathbf{r}\left[\frac{1}{2m}|\nabla\varphi_0|^2+V(\mathbf{r})|\varphi_0(\mathbf{r})|^2\right]\\ 
+\frac{1}{2}N(N-1)U_0\int d\mathbf{r}|\varphi_0(\mathbf{r})|^4
\end{align}}$$
- For large $N$, $N-1\approx N$
- Then _minimise_ $\braket{ \Psi|H | \Psi }$ with the _Lagrange multiplier_ $\mu$ for _fixed norm_:
$$\langle{\Psi}\rvert H \lvert \Psi \rangle - \mu N \int d\mathbf{r}|\varphi_{0}(\mathbf{r})|^{2}$$
- With _first order variations_ $\delta \varphi_{0}$ and $\delta \varphi_{0}^{*}$, and defining the _condensate wavefunction, or order parameter_ $\varphi(\boldsymbol{r})=\sqrt{ N }\varphi_{0}(\boldsymbol{r})$, one gets the _Gross-Pitaevskii equation_:
$$\left[-\frac{1}{2m}\nabla^2-\mu+V(\mathbf{r})+U_0|\varphi(\mathbf{r})|^2\right]\varphi(\mathbf{r})=0$$

- Considering that $\braket{ \Psi|H-\mu N |\Psi  }$ is extremised under _general variations_ that _change particle number_:
$$\mu=\frac{\partial \braket{ \Psi|H | \Psi } }{\partial N}$$

### Healing length
- Consider the $1D$ case
- The introduction of $|\varphi|^{2}$ (unit of _density_) gives a _length scale_ to the system

- Introduce the _dimensionless form_:
$$\varphi(\boldsymbol{r})=\sqrt{ n }\phi\left( \frac{\boldsymbol{r}}{\xi} \right)$$
- For $\varphi_{0}\to \text{const.}$, $\mu\approx U_{0}n$:
$$-\frac{1}{2m\xi^{2}}\phi''+\mu(|\phi|^{2}-1)\phi=0$$
- Set:
$$\xi\equiv \frac{1}{\sqrt{ 2mnU_{0} }}$$

- The _healing length_ $\xi$ is the length-scale on which $\varphi(\boldsymbol{r})$ is _disturbed_ by some _localised perturbation_ of scale $\ll \xi$
- $U_{0}$ sets the _steepness_ of the _recovery_

- _Example_: near a _hard wall_ where $\varphi(x)=0$, and a _density_ $n_{\infty}=\varphi_{\infty}^{2}$ far from the wall:
$$\varphi(x)=\varphi_{\infty }\tanh \frac{x}{\sqrt{ 2 }\xi}$$

### Observables
- _Density_ and _current density_:
$$\begin{align}
\rho(\mathbf{r})&=|\varphi(\mathbf{r})|^2\\
\mathbf{j}(\mathbf{r})&=-\frac{i}{2m}\left[\varphi^{*}(\mathbf{r})\left(\nabla\varphi(\mathbf{r})\right)-\left(\nabla\varphi^{*}(\mathbf{r})\right)\varphi(\mathbf{r})\right]
\end{align}$$
- $|\varphi|^{2}$ is an _extensive quantity_, both $\rho$ and $\boldsymbol{j}$ are _macroscopic_

- Decompose into magnitude and modulus:
$$\varphi(\boldsymbol{r})=\sqrt{ \rho(\boldsymbol{r}) }\exp[i\chi(\boldsymbol{r})]$$
- With $\boldsymbol{j}=\rho \boldsymbol{v}$, one gets the _superfluid velocity_
$$\boldsymbol{v}_{s}\equiv \frac{1}{m}\nabla \chi$$
### Superfluid vortex
- From the above, one expects the flow to be _irrotational_ with $\nabla\times \boldsymbol{v}_{s}=0$

- However, phase can simply _increase_ by a multiple of $2\pi$, leading to the _Onsager-Feynman quantisation condition_:
$$\oint m\boldsymbol{v}_{s}\cdot d\boldsymbol{\mathrm{l}}=2\pi l=hl ,\quad l \in \mathbb{Z}$$
- A _non-zero winding_ requires that density _vanishes at a point_ in 2D, or a _line_ in 3D
	- $\varphi$ must be _approximately_ $\propto z^{l}$ for $z=x+iy$ to give the non-zero winding

- This is _analagous_ to _vortices_ in _fluid dynamics_
	- In a _classical_ fluid, vorticity is not generally quantised

- Look for two-dimensional solutions with _winding number_ $l\neq 0$
$$\varphi(r,\theta)\xrightarrow{r\to \infty} \sqrt{ n }\exp(il\theta)$$
- _Parametrise_ $\varphi(r,\theta)$:
$$\varphi(r,\theta)=\sqrt{ n }f\left( \frac{r}{\xi} \right)\exp(il\theta)$$

- From the _Gross-Pitaevskii equation_, with $s\equiv r/\xi$
$$-f''-\frac{f'}{s}+\frac{l^{2}f}{s^{2}}-f+f^{3}=0$$
- For _small_ $s$ and $s\to \infty$ respectively:
$$f(s)\sim s^{l} \qquad f(s\to \infty)\to 1$$
- The region of _suppressed density_ has size $\xi$, and is known as the _vortex core_
	- In 3D, it is a _line_

- The _energy_ of the vortex can be found using $\braket{ \Psi|H | \Psi }$ in terms of $\varphi$
- The _excess energy_ relative to the _uniform density state_:
$$\Delta E = \int d\mathbf{r}\left[\frac{n^2}{2m\xi^2}(f')^2+\frac{U}{2}n^2 \left(f^2-1\right)^2\right] + \frac{n^2}{2m}\int d\mathbf{r}\, f^2(\nabla\chi)^2$$
- There is a _potential part_ and a _kinetic part_
	- Potential: deviation of density from bulk value, as well as energy from the _gradient_

- From the winding, introducing _cutoffs_ $\xi<r<L$, one gets a _logarithmically divergent_ kinetic contribution
$$\displaylines{\nabla \chi=\frac{l}{r}\hat{\boldsymbol{e}}_{\theta} \\ \Delta E=\text{const.}+\frac{\pi nl^{2}}{m}\log\left( \frac{L}{\xi} \right)}$$
- For _finite systems_, this still gives finite energy

- One can also have _two vortices_ of _opposite vorticity_
- Kinetic energy _increases_ as they are further away, therefore _opposite vortices attract_, and similarly _like vortices repel_:
$$\Delta E_{K} \propto \log|\boldsymbol{r}_{1}-\boldsymbol{r}_{2}|$$
- Vortices of $l>1$ are then likely to _break apart_ into multiple vortices of $l=\pm1$
	- They can then form _vortex lattices_

- The vortices in 3D are _analagous to wires in magnetostatics_

- A manifestation of _superfluidity_
	- Persistent flow _without resistance_
	- Vortices require _breaking rotational symmetry_

## Bogoliubov theory
- Assume a _uniform condensate_ with $V(\boldsymbol{r})=0$
- Then work with $\varphi(\boldsymbol{r})=\sqrt{ n }$, then expand in the _plane wave basis_
$$H =\sum_\mathbf{k}\epsilon(\mathbf{k})a^\dagger_\mathbf{k}a^{\vphantom{\dagger}}_\mathbf{k}+ \overbrace{\frac{U_0}{2V}\sum_{\mathbf{k}_1+\mathbf{k}_2=\mathbf{k}_3+\mathbf{k}_4} a^\dagger_{\mathbf{k}_1}a^\dagger_{\mathbf{k}_2}a^{\vphantom{\dagger}}_{\mathbf{k}_3}a^{\vphantom{\dagger}}_{\mathbf{k}_4}}^{\equiv H_\text{int}}$$
- The Gross-Pitaevskii approximation _does not give an eigenstate
$$\displaylines{\lvert{\Psi_\text{GP}}\rangle = \frac{1}{\sqrt{N!}}\left(a^\dagger_0\right)^N\lvert{\text{VAC}}\rangle \\H_\text{int}\lvert{\Psi_\text{GP}}\rangle =  \frac{U_0}{2V}\sum_{\mathbf{k}} a^\dagger_{\mathbf{k}}a^\dagger_{-\mathbf{k}}a^{\vphantom{\dagger}}_{0}a^{\vphantom{\dagger}}_{0}\lvert{\Psi_\text{GP}}\rangle}$$
- Interactions lead to states with $(\boldsymbol{k},-\boldsymbol{k})$ _pairs_

- For _weak interactions_, the state still has _most particles_ in the $\boldsymbol{k}=0$ state
- As $a\ket{N}=\sqrt{ N }\ket{N-1}$, terms with $a_{0}^{({\dagger})}$ will be _most significant_

- Take terms in $H_\text{int}$ with _two operators of wavenumber_ $0$:
$$\begin{align}
H_\text{pair} &= \sum_\mathbf{k}\epsilon(\mathbf{k})a^\dagger_\mathbf{k}a^{\vphantom{\dagger}}_\mathbf{k}+\frac{U_0}{2V}a^\dagger_0a^\dagger_0a^{\vphantom{\dagger}}_0a^{\vphantom{\dagger}}_0 \nonumber\\ &\quad+\frac{U_0}{2V}\sum_{\mathbf{k}\neq0}\left[a^\dagger_{\mathbf{k}}a^\dagger_{-\mathbf{k}}a^{\vphantom{\dagger}}_{0}a^{\vphantom{\dagger}}_{0} + a^\dagger_{0}a^\dagger_{0}a^{\vphantom{\dagger}}_{\mathbf{k}}a^{\vphantom{\dagger}}_{-\mathbf{k}}+4a^\dagger_\mathbf{k}a^\dagger_0a^{\vphantom{\dagger}}_0a^{\vphantom{\dagger}}_\mathbf{k}\right]
\end{align}$$
- The first two terms are an eigenstate for the _Gross-Ptaevskii eigenstate_
- The latter terms indicate the movement of $(0,0)$ and $(\boldsymbol{k},-\boldsymbol{k})$ _particle pairs_

### The Bogoliubov Hamiltonian
- To separate $\boldsymbol{k}\neq 0$ modes from the rest:
$$\displaylines{a^\dagger_0a^{\vphantom{\dagger}}_0 = N - N',\quad N'\equiv \sum_{\mathbf{k}\neq 0} N_\mathbf{k} \\ a^\dagger_0a^\dagger_0a^{\vphantom{\dagger}}_0a^{\vphantom{\dagger}}_0 =  N(N-1) - 2N'N_0+O(N_0^0   ) \\ \begin{align}
H_\text{pair} = &N\epsilon(0)+\frac{U_0}{2V}N(N-1) \\
&+\sum_{\mathbf{k}\neq 0}\left(\left[\epsilon(\mathbf{k})-\epsilon(0)\right]a^\dagger_\mathbf{k}a^{\vphantom{\dagger}}_\mathbf{k}\right.\\
&\left.+\frac{U_0}{2V}\left[a^\dagger_{\mathbf{k}}a^\dagger_{-\mathbf{k}}a^{\vphantom{\dagger}}_{0}a^{\vphantom{\dagger}}_{0} + a^\dagger_{0}a^\dagger_{0}a^{\vphantom{\dagger}}_{\mathbf{k}}a^{\vphantom{\dagger}}_{-\mathbf{k}}+2a^\dagger_\mathbf{k}a^\dagger_0a^{\vphantom{\dagger}}_0a^{\vphantom{\dagger}}_\mathbf{k}\right]\right)
\end{align}}$$
- Then use the approximation, _replacing_ $a_{0},a^{\dagger}_{0}$ with $\sqrt{ N }$

- Consider the _product state_ $\ket{\Psi'}\otimes \ket{N_{0}}_{0}$ between non-zero momentum product state, and zero momentum state
$$\begin{align}
a^\dagger_\mathbf{k}a^{\vphantom{\dagger}}_0\lvert{\Psi'}\rangle\otimes\lvert{N_0}\rangle_0 &= \left(a^\dagger_\mathbf{k}\lvert{\Psi'}\rangle\right)\otimes a^{\vphantom{\dagger}}_0\lvert{N_0}\rangle_0\\
&= \left(a^\dagger_\mathbf{k}\lvert{\Psi'}\rangle\right)\otimes \sqrt{N_0}\lvert{N_0-1}\rangle_0
\end{align}$$
- Similarly for $a_{\boldsymbol{k}}a_{0}^{\dagger}$, ignore difference between $N_{0}$ and $N_{0}+1$
- Effectively, only take the Hamiltonian which _describes non-zero momentum particles_, which are _excited out of_ a _condensate_ of zero momentum states

- Then, one gets the _Bogoliubov Hamiltonian_
	- _Zero momentum density_ $n_{0}=N_{0}/V$
	- $\tilde{\epsilon}(\boldsymbol{k})=\epsilon(\boldsymbol{k})-\epsilon(0)$
$$\begin{aligned}
H_\text{pair} &= N\epsilon(0)+\frac{U_0}{2V}N(N-1)\\
&+\sum_{\mathbf{k}\neq 0}\left(\left[\tilde\epsilon(\mathbf{k})+U_0n_0\right]a^\dagger_\mathbf{k}a^{\vphantom{\dagger}}_\mathbf{k}+\frac{U_0n_0}{2}\left[a^\dagger_{\mathbf{k}}a^\dagger_{-\mathbf{k}} + a^{\vphantom{\dagger}}_{\mathbf{k}}a^{\vphantom{\dagger}}_{-\mathbf{k}}\right]\right)
\end{aligned}$$
### Bogoliubov transformation
- Suppose there is a _Hermitian operator_:
$$h = \epsilon\left[a^\dagger_1a^{\vphantom{\dagger}}_1+a^\dagger_2a^{\vphantom{\dagger}}_2\right] + \delta\left[a^\dagger_1a^\dagger_2+a^{\vphantom{\dagger}}_1a^{\vphantom{\dagger}}_2\right]= \pmatrix{a^\dagger_1 & a^{\vphantom{\dagger}}_2}\pmatrix{\epsilon & \delta \\\delta & \epsilon}\pmatrix{a^{\vphantom{\dagger}}_1 \\ a^\dagger_2}-\epsilon$$
- Seek to express $h$ in the form:
$$\displaylines{h = \Omega\left[b^\dagger_1b^{\vphantom{\dagger}}_1+b^\dagger_2b^{\vphantom{\dagger}}_2\right] +\text{const.} \\ \begin{pmatrix}b^{\vphantom{\dagger}}_1 \\ b^\dagger_2\end{pmatrix}=\Lambda\begin{pmatrix}a^{\vphantom{\dagger}}_1 \\ a^\dagger_2\end{pmatrix}}$$
- To keep _commutation relations_ $[b_{i},b_{j}^{\dagger}]=\delta_{ij}$, $\Lambda$ must be _pseudo-unitary_:
	- Unitary: trigonometric; pseudo-unitary: hyperbolic
	- Proof: consider vector $\Psi=\pmatrix{a_{1}&a_{2}^{\dagger}}^{T}$ such that $[\Psi_{i},(\Psi ^{\dagger})_{j}]=(\sigma_{3})_{ij}$
$$\displaylines{\Lambda^\dagger \sigma_3 \Lambda = \sigma_3 \\ \Lambda=
\begin{pmatrix}
\cosh\kappa & \sinh\kappa \\
\sinh\kappa & \cosh\kappa
\end{pmatrix}}$$
- To demand that $b_{1}b_{1}$ and other similar terms _vanish_:
$$\begin{align}
\tanh 2\kappa = \frac{\delta}{\epsilon},\qquad \Omega = \sqrt{\epsilon^2-\delta^2}\\
h = \Omega\left[b^\dagger_1b^{\vphantom{\dagger}}_1+b^\dagger_2b^{\vphantom{\dagger}}_2\right] + \Omega - \epsilon
\end{align}$$
- Applying to the Bogoliubov Hamiltonian:
	- A factor of $2$ due to the $a_{\boldsymbol{k}}^{\dagger}a_{-\boldsymbol{k}}^{\dagger}$ terms $(\delta_{\boldsymbol{p},}=n_{0}U_{0},\,\epsilon_{\boldsymbol{p}}=\tilde{\epsilon}_{\boldsymbol{p}}+n_{0}U_{0})$
$$b^{\vphantom{\dagger}}_\mathbf{p}=a^{\vphantom{\dagger}}_\mathbf{p}\cosh\kappa_\mathbf{p}+a^\dagger_{-\mathbf{p}}\sinh\kappa_\mathbf{p}\nonumber\\
\qquad \tanh2\kappa_\mathbf{p}=\frac{n_0 U_0}{\tilde\epsilon(\mathbf{p})+n_0 U_0}$$
- The Hamiltonian, a _harmonic oscillator_ for _Bogoliubov excitations_
$$H=E_0+\sum_{\mathbf{p}\neq 0}\omega(\mathbf{p})b^\dagger_\mathbf{p}
b^{\vphantom{\dagger}}_\mathbf{p}$$
- The _Bogoliubov dispersion relation_ is _shifted up_ from the typical dispersion
$$\omega(\mathbf{p}) = \sqrt{\tilde\epsilon(\mathbf{p})\left(\tilde\epsilon(\mathbf{p})+2U_0n_0\right)}$$
- The _ground state energy_:
$$E_0=\frac{1}{2}nU_0  N+\sum_{\mathbf{p}\neq 0}\frac{1}{2}\left[\omega(\mathbf{p})-\tilde\epsilon(\mathbf{p})-n_0U_0\right]$$
- It _diverges_ in the ultraviolet limit
- Instead, _regularise_ the potential
$$\displaylines{E_0=\frac{1}{2}nU_0  N\left[1-\frac{1}{V}\sum_\mathbf{p}\frac{U_0}{2\tilde\epsilon(\mathbf{p})}\right]+E_\text{reg} \\ E_\text{reg}\equiv\sum_{\mathbf{p}\neq 0}\frac{1}
{2}\left[\omega(\mathbf{p})-\tilde\epsilon(\mathbf{p})-n_0U_0+ \frac{(n_0U_0)^2}{2\tilde\epsilon(\mathbf{p})}\right]}$$
- The first two terms come from _second order perturbation theory_ for any pair potential
- $E_\text{reg}$ is _finite_ for a _finite range potential_

### The ground state
- The ground state is a _vacuum_ of the _Bogoliubov excitation_

- A state that satisfies $b_{\boldsymbol{k}}\ket{0}=0$:
	- Proof: consider that the _coherent state_ $\exp(\alpha a^{\dagger})\ket{\text{VAC}}$ is an eigenstate of $a$ with eigenvalue $\alpha$, then $a_{\boldsymbol{k}}\ket{0}=-\tanh\kappa_{\boldsymbol{k}}a_{-\boldsymbol{k}}^{\dagger}\ket{0}$
$$\lvert{0}\rangle=\prod_{\mathbf{k}\neq 0} \exp\left(-\frac{1}{2}\tanh\kappa_\mathbf{k}a^\dagger_{\mathbf{k}}a^\dagger_{-\mathbf{k}}\right)\lvert{\Psi_\text{GP}}\rangle$$
- It is a _superposition_ of _pairs_ being _excited_ out of the Gross-Pitaevskii state
	- Unlike the Gross-Pitaevskii state, there are _correlations_ between the pairs

#### Density fluctutations
- Consider the _Fourier components_ of the [[#Single particle density operator|density operator]]:
$$\rho_\mathbf{q}= \sum_\mathbf{k}a^\dagger_{\mathbf{k}-\mathbf{q}}a^{\vphantom{\dagger}}_\mathbf{k}$$
- The most significant contribution is from having either operator act on $\boldsymbol{k}=0$:
$$\rho_\mathbf{q}\sim \sqrt{N}\left(a^\dagger_{-\mathbf{q}} + a^{\vphantom{\dagger}}_{\mathbf{q}}\right) = \sqrt{  \frac{N\tilde{\epsilon}(\boldsymbol{q})}{\omega(\boldsymbol{q})} }(b^{\dagger}_{-\boldsymbol{q}}+b_{\boldsymbol{q}})\equiv \sqrt{N}e^{-\kappa_\mathbf{q}} \left(b^\dagger_{-\mathbf{q}} + b^{\vphantom{\dagger}}_{\mathbf{q}}\right)$$
- _Density fluctuations_ are then:
$$\langle{0}\rvert \rho_{-\mathbf{q}}\rho_{\mathbf{q}} \lvert 0 \rangle = N\frac{\tilde\epsilon(\mathbf{q})}{\omega(\mathbf{q})}\xrightarrow{\mathbf{q}\to 0} \frac{N\lvert{\mathbf{q}}\rvert}{2mc}$$
- Here, the _speed of sound_:
$$\omega(\mathbf{q})\xrightarrow{\mathbf{q}\to 0}\sqrt{ \frac{n_{0}U_{0}}{m} }|\boldsymbol{q}|\equiv c\lvert{\mathbf{q}}\rvert$$
- As $\boldsymbol{q}\to0$, density fluctuations _vanish_
	- For the _Gross-Piatevskii_ ground state, fluctuations are _uncorrelated_ and _Poisonnian_ as $\braket{ 0|\rho_{\boldsymbol{-q}}\rho _{\boldsymbol{q}} |0  }=N$
#### Condensate depletion
- The _number operator_ for the _original bosons in terms of quasi-particles_:
$$a^\dagger_{\mathbf{p}}a^{\vphantom{\dagger}}_{\mathbf{p}}=(b^\dagger_\mathbf{p}\cosh\kappa_{\mathbf{p}}-b^{\vphantom{\dagger}}_{-\mathbf{p}}\sinh\kappa_{\mathbf{p}})(b^{\vphantom{\dagger}}_\mathbf{p}\cosh\kappa_{\mathbf{p}}-b^\dagger_{-\mathbf{p}}\sinh\kappa_{\mathbf{p}})$$
- For _non-zero temperature_, the _mean occupation of a Bogoliubov mode_ is in terms of the _Bose distribution_ using Bogoliubov dispersion $\omega(\boldsymbol{p})$
$$\tilde{n}_{B}(\boldsymbol{p})=\langle b_{\boldsymbol{p}}^{\dagger}b_{\boldsymbol{p}} \rangle=\frac{1}{\exp(\omega(\boldsymbol{p})/k_{B}T)-1} $$

- The average at _zero temperature_:
	- The _radial density_ $4\pi p^{2}N_{p}$ _peaks_ around $\xi^{-1}$
$$\langle N_\mathbf{p}\rangle=\langle a^\dagger_{\mathbf{p}}a^{\vphantom{\dagger}}_{\mathbf{p}}\rangle = \sinh^2\kappa_{p}\xrightarrow{ \lvert{\mathbf{p}}\rvert\ll \xi^{-1}}\frac{mc_s}{2\lvert{\mathbf{p}}\rvert}$$
- Then, the _fraction_ of atoms _not in the condensate_:
	- The _Born approximation_ scattering length $a=mU_{0}/(4\pi)$
	- In 3 dimensions, there is no phase space volume at $\boldsymbol{p}=0$
$$\frac{1}{N}\sum_{\mathbf{p}\neq 0} \langle N_\mathbf{p}\rangle=\frac{8}{3\sqrt{\pi}}\sqrt{n a^3}$$
- Typically, for ultracold atoms, the fraction is $\sim 0.01$

- The system can go through a _quantum phase transition_ between states which can change depletion dramatically
- Liquid $^{4}\ce{ He }$ has a _condensate_ fraction of only $10\%$
	- Bogoliubov theory fails to capture phenomenonlogy
# Fermi gas
- Take the _weakly interacting_ Fermi gas:
$$H = \int d\mathbf{r}\left[ \sum_{s=\uparrow,\downarrow}\frac{1}{2m}\nabla\psi^\dagger_s\cdot\nabla\psi^{\vphantom{\dagger}}_s + U_0 \psi^\dagger_\uparrow\psi^\dagger_\downarrow\psi^{\vphantom{\dagger}}_\downarrow\psi^{\vphantom{\dagger}}_\uparrow\right]$$
- Going into momentum space:
$$H =\sum_{\mathbf{k},s} \epsilon(\mathbf{k})a^\dagger_{\mathbf{k},s}a^{\vphantom{\dagger}}_{\mathbf{k},s} + \overbrace{\frac{U_0}{V}\sum_{\mathbf{k}_1+\mathbf{k}_2=\mathbf{k}_3+\mathbf{k}_4} a^\dagger_{\mathbf{k}_1,\uparrow}a^\dagger_{\mathbf{k}_2,\downarrow}a^{\vphantom{\dagger}}_{\mathbf{k}_3,\downarrow}a^{\vphantom{\dagger}}_{\mathbf{k}_4,\uparrow}}^{\equiv H_\text{int}}$$
- At $U_{0}=0$, the eigenstates are _product states_ $N_{s}(\boldsymbol{k})=0,1$
- Energy of the state:
$$E^{(0)}(\mathbf{N}) = \sum_{\mathbf{k},s} \epsilon(\mathbf{k})N_{s}(\mathbf{k})$$

- The _ground state_ has $N_{s}(\boldsymbol{k})=\theta(|\boldsymbol{k}|-k_{F})$
- A _low-energy state_ has $N_{s}(k\ll k_{F})=1$ and $N_{s}(k\gg k_{F})=0$

- When _perturbed_, the eigenstates can still be _labelled_ using occupation numbers
- The occupations correspond to _quasi-particles_
- One has to add _corrections_ to the energy using _perturbation theory_

## Fermi liquid theory
- Use a [[Time-Independent Approximation Methods|second order perturbation theory]]
$$\begin{align}
E^{(1)}(\mathbf{N}) &= \langle{\mathbf{N}}\rvert H_\text{int} \lvert \mathbf{N} \rangle\\
E^{(2)}(\mathbf{N}) &= \sum_{\mathbf{N}'\neq \mathbf N}\frac{\lvert{\langle{\mathbf{N'}}\rvert H_\text{int} \lvert \mathbf{N} \rangle}\rvert^2}{E^{(0)}(\mathbf{N})-E^{(0)}(\mathbf{N}')}
\end{align}$$
- The _first order correction_:
$$E^{(1)}(\mathbf{N}) = \frac{U_0}{V} \sum_{\mathbf{k},\mathbf{k}'} N_{\uparrow}(\mathbf{k})N_{\downarrow}(\mathbf{k}') = \frac{U_0}{V}N_\uparrow N_\downarrow$$
- The _second order correction_ (ignoring co-inciding momenta):
$$E^{(2)}(\mathbf{N}) = \left(\frac{U_0}{V}\right)^2 \sum_{\mathbf{k}_1+\mathbf{k}_2=\mathbf{k}_3+\mathbf{k}_4}\frac{\left(1-N_{\uparrow}(\mathbf{k}_1)\right)\left(1-N_{\downarrow}(\mathbf{k}_2)\right)N_{\downarrow}(\mathbf{k}_3)N_{\uparrow}(\mathbf{k}_4)}{\epsilon(\mathbf{k}_3)+\epsilon(\mathbf{k}_4)-\epsilon(\mathbf{k}_1)-\epsilon(\mathbf{k}_2)}$$
- This comes from _removing_ particles in $\boldsymbol{k}_{3},\boldsymbol{k}_{4}$, and _adding_ particles to $\boldsymbol{k}_{1},\boldsymbol{k}_{2}$
	- Involves 3 _independent momentum sums_

- _Expand_ in terms of _change in occupation_:
$$N_{s}(\mathbf{k}) = \theta(k_F-\lvert{\mathbf{k}}\rvert) + n_{s}(\mathbf{k})$$
- Take a _continuum limit_ with many $\boldsymbol{k}$. such that $n_{s}$ is some _average_
![[Landau excitation continuum.png|400]]

### Energy expansion
- The _excitation energy_ expansion (independent of perturbation theory)
	- Applies for _any_ interacting system, as long as there is no _phase transition_
$$\Delta E = \sum_{\mathbf{k},s} \varepsilon_s(\mathbf{k})n_{s}(\mathbf{k}) + \frac{1}{2V}\sum_{\mathbf{k}, s,\mathbf{k}', s'} f_{s^{}s'}(\mathbf{k},\mathbf{k}')n_{s}(\mathbf{k})n_{s'}(\mathbf{k}')$$
- At _first order_, from $E^{(1)}(\boldsymbol{N})$:
$$\begin{align}
\varepsilon_s(\mathbf{k}) &= \epsilon(\mathbf{k}) + \frac{U_0 N_{\bar s}}{V}+\cdots\\
f_{\uparrow\downarrow} &= f_{\downarrow\uparrow} = U_0+\cdots,\quad f_{\uparrow\uparrow}=f_{\downarrow\downarrow}=0+\cdots\end{align}$$
- To _second order_, for example, expanding in the _up spins_:
$$\begin{align}
f_{\uparrow\uparrow}(\mathbf{k},\mathbf{k}') = -\frac{U_0^2}{V}\left[\sum_{\mathbf{k}+\mathbf{k}_3=\mathbf{k}'+\mathbf{k}_2} \frac{N_{\downarrow}(\mathbf{k}_3)(1-N_{\downarrow}(\mathbf{k}_2))}{\epsilon(\mathbf{k})+\epsilon(\mathbf{k}_3)-\epsilon(\mathbf{k}')-\epsilon(\mathbf{k}_2)}\right.\\
\left.+\sum_{\mathbf{k}'+\mathbf{k}_3=\mathbf{k}+\mathbf{k}_2}\frac{N_{\downarrow}(\mathbf{k}_3)(1-N_{\downarrow}(\mathbf{k}_2))}{\epsilon(\mathbf{k}')+\epsilon(\mathbf{k}_3)-\epsilon(\mathbf{k})-\epsilon(\mathbf{k}_2)}\right]
\end{align}$$
- Take the _low-temperature limit_, where $n_{s}$ is non-zero only for a _narrow region_ around $\boldsymbol{k}_{F}$, hence take $|\boldsymbol{k}|\approx |\boldsymbol{k}'|\approx k_{F}$
$$\begin{align}
f_{\uparrow\uparrow}(\mathbf{k},\mathbf{k}') = -\frac{U_0^2}{V}\left[\sum_{\mathbf{k}+\mathbf{k}_3=\mathbf{k}'+\mathbf{k}_2} \frac{N(\mathbf{k}_3)(1-N(\mathbf{k}_2))}{\epsilon(\mathbf{k}_3)-\epsilon(\mathbf{k}_2)}
+\sum_{\mathbf{k}'+\mathbf{k}_3=\mathbf{k}+\mathbf{k}_2}\frac{N(\mathbf{k}_3)(1-N(\mathbf{k}_2))}{\epsilon(\mathbf{k}_3)-\epsilon(\mathbf{k}_2)}\right]
\end{align}$$
- Calculating these parameters is simpler than $E^{(2)}(\boldsymbol{N})$ directly as there is _only one independent momentum_
- However, there is a _non-trivial dependence_ on the _angle_ between $\boldsymbol{k},\boldsymbol{k}'$

- Meanwhile:
$$\begin{align}
f_{\uparrow\downarrow}(\mathbf{k},\mathbf{k}') = U_0 + f_{\uparrow\uparrow}(\mathbf{k},\mathbf{k}') +\frac{U_0^2}{V}\left[\sum_{\mathbf{k}+\mathbf{k}'=\mathbf{k}_3+\mathbf{k}_4}\frac{N(\mathbf{k}_3)N(\mathbf{k}_4)}{\epsilon(\mathbf{k}_3)+\epsilon(\mathbf{k}_4)-2E_\text{F}}\right.\\
\left.\sum_{\mathbf{k}+\mathbf{k}'=\mathbf{k}_1+\mathbf{k}_2}\frac{(1-N(\mathbf{k}_1))(1-N(\mathbf{k}_2))}{2E_\text{F}-\epsilon(\mathbf{k}_1)-\epsilon(\mathbf{k}_2)}\right]
\end{align}$$
### Angular dependence of Landau parameters
- Take the _thermodynamic limit_: 
$$\begin{align}
f_{\uparrow\uparrow}(\mathbf{k},\mathbf{k}') = \frac{U_0^2}{(2\pi)^3}\left[\int_{\substack{\lvert{\mathbf{k}_3}\rvert<k_\text{F},\lvert{\mathbf{k}_2}\rvert>k_\text{F}\\ \mathbf{k}+\mathbf{k}_3=\mathbf{k}'+\mathbf{k}_2 }} \frac{d\mathbf{k}_3}{\epsilon(\mathbf{k}_2)-\epsilon(\mathbf{k}_3)}\right.\nonumber\\
\left.+\int_{\substack{\lvert{\mathbf{k}_3}\rvert<k_\text{F},\lvert{\mathbf{k}_2}\rvert>k_\text{F}\\ \mathbf{k}'+\mathbf{k}_3=\mathbf{k}+\mathbf{k}_2 }}\frac{d\mathbf{k}_3}{\epsilon(\mathbf{k}_2)-\epsilon(\mathbf{k}_3)}\right].
\end{align}$$
- Introduce the notation:
$$\displaylines{\epsilon(\mathbf{k}_2)-\epsilon(\mathbf{k}_3) = \frac{2}{m}\mathbf{K}\cdot\mathbf{q} \\ \mathbf{K} = \frac{1}{2}\left(\mathbf{k}_2+\mathbf{k}_3\right),\quad \mathbf{q}= \frac{1}{2}\left(\mathbf{k}_2-\mathbf{k}_3\right) \\ 
\left(\mathbf{K}+\mathbf{q}\right)^2>k_\text{F}^2,\quad \left(\mathbf{K}-\mathbf{q}\right)^2<k_\text{F}^2}$$
![[Landau parameter integration k.png|300]]
- This gives $K_{-}(\theta)<|\boldsymbol{K}|<K_{+}(\theta)$
$$K_{\pm}(\theta)=\pm q\lvert{\cos\theta}\rvert+\sqrt{k_\text{F}^2-q^2\sin^2\theta}$$

- From this, for $|\boldsymbol{k}-\boldsymbol{k}'|=2k_{F}\sin \phi/2$
$$\begin{align}
f_{\uparrow\uparrow}(\mathbf{k},\mathbf{k}') &= \frac{U_0^2 m}{(2\pi)^2} \int_0^{\pi} d\theta \sin\theta \sqrt{k_\text{F}^2-q^2\sin^2\theta}\nonumber\\
&=\frac{U_0^2 m k_\text{F}}{(2\pi)^2}\left[1 - \frac{\cos^2\phi/2}{2\sin\phi/2}\log\left(\frac{1-\sin\phi/2}{1+\sin\phi/2}\right)\right]
\end{align}$$
- Due to _rotational invariance_, accounting for spins in other directions:
$$\displaylines{N_{s,s',\boldsymbol{k}}=a^{\dagger}_{\boldsymbol{k},s}a_{\boldsymbol{k},s'} \\ \mathsf{N}(\mathbf{k})=\begin{pmatrix}
N_{\uparrow\uparrow}(\mathbf{k}) & N_{\uparrow\downarrow}(\mathbf{k}) \\
N_{\downarrow\uparrow}(\mathbf{k}) & N_{\downarrow\downarrow}(\mathbf{k})
\end{pmatrix}}$$
- The $f$ function then has $4$ indices:
$$\frac{1}{2V}\sum_{\mathbf{k}, s_1,s_2,\mathbf{k}', s_3,s_4} f_{s_1s_2,s_3s_4}(\mathbf{k},\mathbf{k}')n_{s_1s_2}(\mathbf{k})n_{s_3s_4}(\mathbf{k}')$$
- Final form of $f$
$$\begin{align}
f_{s_1s_2,s_3s_4}(\mathbf{k},\mathbf{k}') = \frac{U_0}{2}\left[\left(1+ \frac{mU_0 k_\text{F}}{2\pi^2}\left[2+\frac{\cos\phi}{2\sin\phi/2}\log\frac{1+\sin\phi/2}{1-\sin\phi/2}\right]\right)\delta_{s_1s_3}\delta_{s_2s_4}\right.\nonumber\\
\left.\left(1+ \frac{mU_0 k_\text{F}}{2\pi^2}\left[1-\frac{1}{2}\sin\phi/2\log\frac{1+\sin\phi/2}{1-\sin\phi/2}\right]\right)\boldsymbol{\sigma}_{s_1s_3}\cdot\boldsymbol{\sigma}_{s_2s_4}\right]
\end{align}$$

- In _general_, the interaction between quasi-particles can be written as:
	- $F$ and $G$ are _dimensionless_, with the normalisation of $\nu(E_{F})$ as the _density of states at the Fermi surface_ $k_{F}m/\pi^{2}$
$$\nu(E_F)f_{s_1s_2,s_3s_4}(\mathbf{k},\mathbf{k}') = F(\phi) \delta_{s_1s_3}\delta_{s_2s_4} + G(\phi)\boldsymbol{\sigma}_{s_1s_3}\cdot\boldsymbol{\sigma}_{s_2s_4}$$
### Quasiparticle energy and effective mass
- $\varepsilon_{s}(\boldsymbol{k})$ has _two momentum sums_ in the _second order_, which is difficult to evaluate

- However, one should expect some _linear dispersion_ near the Fermi energy:
$$\varepsilon_s(\mathbf{k}) - E_\text{F} = v_\text{F}(\lvert{\mathbf{k}}\rvert-k_\text{F})$$
- The _Fermi velocity_:
$$v_{F}=\frac{p_{F}}{m^{*}}$$
- Here, $m^{*}$ is the _effective mass_

- Consider a _shift_ in the Fermi sea:
$$\begin{align}
N_s(\mathbf{k}-\delta\mathbf{k}) &=\theta(k_F-\lvert{\mathbf{k}-\delta\mathbf{k}}\rvert) + n_{s}(\mathbf{k}-\delta\mathbf{k})+\cdots\nonumber\\
&=\theta(k_F-\lvert{\mathbf{k}}\rvert) + n_s(\mathbf{k}) + \delta(k_F-\lvert{\mathbf{k}}\rvert)\hat{\mathbf{k}}\cdot\delta\mathbf{k}- \delta\mathbf{k}\nabla_\mathbf{k}n_{s}(\mathbf{k})+\cdots
\end{align}$$
- Treating the last 3 terms as $n_{s}(\boldsymbol{k}')$, this _shifts the excitation energy_:
$$\begin{align}
\Delta E &= \sum_{\mathbf{k},s} n_{s}(\mathbf{k})\delta\mathbf{k}\cdot\nabla_\mathbf{k}\varepsilon_s(\mathbf{k}) \nonumber\\
&+\frac{1}{V}\sum_{\mathbf{k}, s,\mathbf{k}', s'} f_{s^{}s'}(\mathbf{k},\mathbf{k}')n_{s}(\mathbf{k})\left[\delta(k_F-\lvert{\mathbf{k}'}\rvert)\hat{\mathbf{k}}'\cdot\delta\mathbf{k}- \nabla_{\mathbf{k}'}n_{s'}(\mathbf{k}')\cdot\delta\mathbf{k}\right]
\end{align}$$
- Since this applies to the _whole system_ and _does not change interaction energy_, the shift in energy must be _kinetic_:
$$\Delta E = \frac{\mathbf{P}}{m}\cdot\delta\mathbf{k} \qquad \mathbf{P} = \sum_{\mathbf{k},s} \mathbf{k}n_{s}(\mathbf{k})$$
- If this applies for _all_ $n_{s}(\boldsymbol{k})$ and $\delta \boldsymbol{k}$ to _first order_:
$$\frac{\mathbf{k}}{m} = \nabla_\mathbf{k}\varepsilon_s(\mathbf{k}) +  \sum_{s'}\int  f_{s^{}s'}(\mathbf{k},\mathbf{k}')\delta(k_F-\lvert{\mathbf{k}'}\rvert)\hat{\mathbf{k}}' \frac{d\mathbf{k}'}{(2\pi)^3}$$
- Only considering momenta on the Fermi surface:
$$\frac{\mathbf{k}}{m} = \frac{\mathbf{k}}{m_*} +\frac{1}{m} \int F(\phi) \mathbf{k}' \frac{d\Omega_{\mathbf{k}'}}{4\pi}$$
- Writing $\boldsymbol{k}'=\cos \phi \boldsymbol{k}+\sin \phi \boldsymbol{k}_{\perp}$
$$\frac{1}{m} = \frac{1}{m_*} +\frac{1}{m} \int F(\phi) \cos\phi \frac{\sin\phi d\phi}{2}$$
- This gives the _effective mass_:
$$\frac{m_*}{m} = 1 + \frac{1}{30\pi^4}(7\log 2 - 1)\left(mU_0k_\text{F}\right)^2+\cdots$$
- For _heavy fermion materials_, this can go up to $10^{3}$

## Quasiparticles
- Consider the _first order perturbation_ to the _wavefunction_:
$$\displaylines{\lvert{\mathbf{N}^{(1)}}\rangle = \sum_{\mathbf{N}'\neq \mathbf N}\frac{\langle{\mathbf{N'}}\rvert H_\text{int} \lvert \mathbf{N} \rangle}{E^{(0)}(\mathbf{N})-E^{(0)}(\mathbf{N}')}\lvert{\mathbf{N}'}\rangle \\ H_\text{int}=\frac{U_0}{V}\sum_{\mathbf{k}_1+\mathbf{k}_2=\mathbf{k}_3+\mathbf{k}_4} a^\dagger_{\mathbf{k}_1,\uparrow}a^\dagger_{\mathbf{k}_2,\downarrow}a^{\vphantom{\dagger}}_{\mathbf{k}_3,\downarrow}a^{\vphantom{\dagger}}_{\mathbf{k}_4,\uparrow}}$$
- From the _Fermi sea ground state_ $\ket{\text{FS}}$, the perturbation must _create two particle-hole pairs_ out of the Fermi sea, such that _total momentum_ is zero
$$\lvert{0}\rangle=\lvert{\text{FS}}\rangle+\text{two particle-hole pair states}+\cdots$$
- Consider the _excited state_:
$$a^{\dagger}_{\boldsymbol{k},s}\ket{\text{FS}} $$
- Contributions to the wavefunction:
	- Creating two particle-hole pairs
	- Create a _single_ particle-hole pair and _move_ the particle at $\boldsymbol{k}$ to elsewhere

- Denote the _excited state with interactions_ (_quasiparticle state_) as $\ket{\boldsymbol{k},s}$
- Consider _creating_ a particle _from_ the excited ground state $a^{\dagger}_{\boldsymbol{k},s}\ket{0}$
- To first order, allowing for all possibilities, with _normalisation factor_ $z_{k}$
$$\begin{align}
\lvert{\mathbf{k},s}\rangle &= \sqrt{\frac{z_k}{\langle{0}\rvert a^{\vphantom{\dagger}}_{\mathbf{k},s}a^\dagger_{\mathbf{k},s} \lvert 0 \rangle}}a^\dagger_{\mathbf{k},s}\lvert{0}\rangle \nonumber\\
&\qquad + \frac{U_0}{V}\sum_{\substack{\mathbf{k}_1+\mathbf{k}_2=\mathbf{k}_3+\mathbf{k}\\ s,s'}}\frac{a^\dagger_{\mathbf{k}_1,s}a^\dagger_{\mathbf{k}_2,s'}a^{\vphantom{\dagger}}_{\mathbf{k}_3,s'}\lvert{\text{FS}}\rangle}{\epsilon(\mathbf{k}_1)+\epsilon(\mathbf{k}_2)-\epsilon(\mathbf{k}_3)-\epsilon(\mathbf{k})},
\end{align}$$
- For _higher order corrections_ to this _quasi-particle state_, there will be _more_ particle-hole pairs
- The quasi-particle state _always conserves momentum and spin_ compared to the free theory

- The normalisation, also known as the _quasiparticle residue_:
$$z_\mathbf{k}= 1 - \left(\frac{U_0}{V}\right)^2\sum_{\substack{\mathbf{k}_1+\mathbf{k}_2=\mathbf{k}_3+\mathbf{k}\\\lvert{\mathbf{k}_3}\rvert<k_\text{F},\lvert{\mathbf{k}_2}\rvert,\lvert{\mathbf{k}_1}\rvert>k_\text{F}\\ s,s'}}\frac{1}{\left[\epsilon(\mathbf{k}_1)+\epsilon(\mathbf{k}_2)-\epsilon(\mathbf{k}_3)-\epsilon(\mathbf{k})\right]^2}+\cdots$$
- It can be interpreted as an _overlap_ between $\ket{\boldsymbol{k},s}$ and $a^{\dagger}_{\boldsymbol{k},s}\ket{0}$
$$z_\mathbf{k}= \frac{\lvert{\langle{\mathbf{k},s}\rvert a^\dagger_{\mathbf{k},s} \lvert 0 \rangle}\rvert^2}{\langle{0}\rvert a^{\vphantom{\dagger}}_{\mathbf{k},s}a^\dagger_{\mathbf{k},s} \lvert 0 \rangle}$$
- A _finite overlap_ is required for the _Fermi liquid theory_ to hold
	- Without it, there is _no correspondence_ between the quasiparticle state and the free state
$$z_{\lvert{\mathbf{k}}\rvert=k_\text{F}} = 1 - \frac{(mUk_\text{F})^2}{8\pi^4}\left[\log 2 + \frac{1}{3}\right]$$
- It is also the _occupation number_ of the _original fermions_ just _below the Fermi surface_
- Even with interactions, there is a _finite step_ in the distribution function at $k_{F}$
![[Fermi step with interactions.png|500]]

# Superconductivity
- Caused by _electrons_ forming _Cooper pairs_, which behaves like _bosons_ and forms _superfluid-like behaviour_, which then gives rise to _superconductivity_
- The _Coulomb repulsion_ can be _overcome_ by _lattice distortions_

- This pairing is only _enabled_ by the presence of other fermions
	- Impossible in vacuum, as the size of the bound state $\gg\lambda_{F}$

- Model Hamiltonian:
$$H = \int d\mathbf{r}\left[ \sum_{s=\uparrow,\downarrow}\frac{1}{2m}\nabla\psi^\dagger_s\cdot\nabla\psi^{\vphantom{\dagger}}_s + U_0 \psi^\dagger_\uparrow\psi^\dagger_\downarrow\psi^{\vphantom{\dagger}}_\downarrow\psi^{\vphantom{\dagger}}_\uparrow\right]$$
- Equivalent to a _two-particle Hamiltonian for opposite spins_:
$$H = -\frac{1}{2m}\left[\nabla_1^2+\nabla_2^2\right] + U_0\delta(\mathbf{r}_1-\mathbf{r}_2)$$
- For $U_{0}<0$, one expects a _bound state_ which has a _spin singlet_
	- Effectively, a _reduced mass_ $m/2$

## Short-range potentials and bound states
- Covert this into a _one-particle problem_ with an _effective Hamiltonian_

- Consider some _variational wave-function_ which varies on lengthscale $l$ 
$$\varphi(z)\equiv \varphi(r/l)$$
- Considering $\braket{ \varphi|H |\varphi  }$ in terms of the _dimensionless parameter_:
$$\braket{ \varphi|H | \varphi } \sim \frac{\alpha}{l^{2}}-\frac{|\beta|}{l^{d}}$$
- In 1 dimension, there _must always be a minimum in energy_, forming _bound states_
- In 2 dimensions, there is _no condition for bound states_
- In $3$ dimensions, there is some _critical value_ of $\beta$ for a bound state to form

- Take the _contact interaction_, and do a _Fourier transform_ on the Schrodinger equation
$$\epsilon(\boldsymbol{p})\tilde{\psi}(\boldsymbol{p})+U_{0}\int \tilde{\psi}(\boldsymbol{p}) \frac{d^{d}\boldsymbol{p}}{(2\pi)^{d}}=E \tilde{\psi}$$
- Taking the second term as $\Delta$, solving for $\tilde{\psi}$ then substituting back with $U_{0},E<0$
$$1=|U_{0}|\int  \frac{1}{|E|+2\epsilon (\boldsymbol{p})}\,\frac{d^{d}\boldsymbol{p}}{(2\pi)^{d}} $$
- Write in terms of density of states $\nu_{d}(\xi)$
$$1=|U_{0}|\int  d\xi\,\frac{\nu_{d}(\xi)}{|E|+2\xi} $$

- In 1 dimension with $\nu_{d}\propto \xi^{-1/2}$, $|E|\neq 0$ cuts off the $\xi^{-3/2}$ behaviour in the integrand, and can be _satisfied for any_ $U_{0}$
- In 2 dimensions with $\nu_{d}=\text{const.}$, $|E|\neq 0$ gives some _upper cut-off_ for the logarithmic behaviour
	- With some cut-off $\Lambda$
$$|E|=2\Lambda \exp\left( -\frac{2}{|U_{0}|\nu_{2}} \right)$$
## The BCS wave-function
- Momentum space:
$$H =\sum_{\mathbf{k},s} \epsilon(\mathbf{k})a^\dagger_{\mathbf{k},s}a^{\vphantom{\dagger}}_{\mathbf{k},s} + \overbrace{\frac{U_0}{V}\sum_{\mathbf{k}_1+\mathbf{k}_2=\mathbf{k}_3+\mathbf{k}_4} a^\dagger_{\mathbf{k}_1,\uparrow}a^\dagger_{\mathbf{k}_2,\downarrow}a^{\vphantom{\dagger}}_{\mathbf{k}_3,\downarrow}a^{\vphantom{\dagger}}_{\mathbf{k}_4,\uparrow}}^{\equiv H_\text{int}}$$
- The _ground state_ of the _non-interacting problem_ is the _Fermi sea_:
$$\lvert{\text{FS}}\rangle=\prod_{|\mathbf{p}|<k_\text{F}} a^\dagger_{\mathbf{p}\uparrow}a^\dagger_{-\mathbf{p}\downarrow}\lvert{\text{VAC}}\rangle$$
- Applying the _interaction Hamiltonian_ gives terms of the form:
$$a^\dagger_{\mathbf{p}+\mathbf{q}\uparrow}a^\dagger_{-\mathbf{p}\downarrow}a^{\vphantom{\dagger}}_{-\mathbf{p}'\downarrow}a^{\vphantom{\dagger}}_{\mathbf{p}'+\mathbf{q}\uparrow}\lvert{\text{FS}}\rangle\qquad |\mathbf{p}|,|\mathbf{p}+\mathbf{q}|>k_\text{F},\, |\mathbf{p}'|,|\mathbf{p}'+\mathbf{q}|<k_\text{F}$$
- Different from the [[#Bogoliubov theory|Bose gas]], there are _not only pair excitations_ with $\boldsymbol{q}=0$

- Still, for BCS theory, assume the ground state _only involves zero momentum pairs_
- With _variational coefficients_, the _most general state_ is:
$$\lvert{\text{pair}}\rangle\equiv\sum_{\sum_\mathbf{p}n^P_\mathbf{p}=N/2} c_{\{n^P_{\mathbf{p}}\}} \prod_{\mathbf{p}}\left[a^\dagger_{\mathbf{p}\uparrow}a^\dagger_{-\mathbf{p}\downarrow}\right]^
{n_{\mathbf{p}}}\lvert{\text{VAC}}\rangle$$
- This gives (accurate for the limit $V\to \infty$)
$$\langle{\text{pair}}\rvert H_\text{int} \lvert \text{pair} \rangle = \frac{U_0}{V}N_\uparrow N_\downarrow+\langle{\text{pair}}\rvert \tilde H_{\text{int}} \lvert \text{pair} \rangle$$
- The first term is the _Hartree-Fock energy_, and the latter term:
$$\tilde H_{\text{int}}=\frac{U_0}{V}\sum_{\mathbf{p}, \mathbf{p}'}a^\dagger_
{\mathbf{p}\uparrow}a^\dagger_{-\mathbf{p}\downarrow}a^{\vphantom{\dagger}}_{-\mathbf{p}'\downarrow}a^{\vphantom{\dagger}}_{\mathbf{p}'\uparrow}$$

### Pair creation operator
- Introducing the _pair creation operator_ $b_{\boldsymbol{p}}=a^{\dagger}_{\boldsymbol{p}\uparrow}a^{\dagger}_{-\boldsymbol{p}\downarrow}$
	- $2b^\dagger_\mathbf{p}b^{\vphantom{\dagger}}_\mathbf{p}= a^\dagger_{\mathbf{p},\uparrow}a^{\vphantom{\dagger}}_{\mathbf{p},\uparrow}+a^\dagger_{-\mathbf{p},\downarrow}a^{\vphantom{\dagger}}_{-\mathbf{p},\downarrow}$
$$H_{\text{pair}}=2\sum_{\mathbf{p}}\epsilon_{\mathbf{p}}b^\dagger_\mathbf{p}b^{\vphantom{\dagger}}_\mathbf{p}+\frac{U_0}{V}\sum_{\mathbf{p},\mathbf{p}'} b^\dagger_\mathbf{p}
b^{\vphantom{\dagger}}_{\mathbf{p}'}$$
- $b_{\boldsymbol{p}}$ _do not obey Bose commutation relations_
	- They _commute at different momenta_, but obey a _hardcore constraint_
$$(b^\dagger_\mathbf{p})^2=0$$
- The variational state where the _amplitudes are uncorrelated_
	- Corresponding to the earlier state $\ket{\text{pair}}$ but with a set of coefficients which _factorise_
$$\lvert{N \text{ pair}}\rangle\equiv\left[\sum_\mathbf{p}c_\mathbf{p}b^\dagger_\mathbf{p}\right]^{N/2}\lvert{\text{VAC}}\rangle\implies \mathrm{K.E}=2\sum_\mathbf{p}\epsilon_{\mathbf{p}}\langle b^\dagger_\mathbf{p}b^{\vphantom{\dagger}}_\mathbf{p}\rangle\equiv 2\sum_\mathbf{p}\epsilon_{\mathbf{p}} \langle n^P_
\mathbf{p}\rangle$$
- The _expected number of pairs_ is hard to determine

### BCS Wavefunction
- Instead, consider the _normalised BCS wavefunction_
$$\lvert{\text{BCS}}\rangle =\prod_\mathbf{p}\left[v_\mathbf{p}b^\dagger_\mathbf{p}+u_\mathbf{p}\right]\lvert{\text{VAC}}\rangle\qquad |u_\mathbf{p}|^2+|v_\mathbf{p}|
^2=1$$
- A _superposition of pairs/no pairs_, which gives a _superposition over numbers of particles_
	- A _projection_ to fixed number $N$ gives $\ket{\text{N pair}}$ for $c_{p}=v_{p}/u_{p}$

- For this wavefunction, $\langle n_{\boldsymbol{p}}^{P} \rangle=v_{p}^{2}$

- Total variational energy:
$$\langle{\text{BCS}}\rvert H \lvert \text{BCS} \rangle=2\sum_\mathbf{p}\epsilon_{\mathbf{p}}|v_\mathbf{p}|^2+\frac{U_0}{V}\sum_{\mathbf{p},\mathbf{p}'}u^*_\mathbf{p}v_
\mathbf{p}u_{\mathbf{p}'}v^*_{\mathbf{p}'}$$
- The _expected value_ of any particle-conserving operator can be _decomposed_:
$$\displaylines{\langle{\text{BCS}}\rvert \mathcal{O} \lvert \text{BCS} \rangle=\sum_N P_N \langle{N \text{ pair}}\rvert \mathcal{O} \lvert N\text{ pair} \rangle \\ P_N=\sum_{\sum n^P_\mathbf{p}=N/2}\prod_\mathbf{p}\left[n^P_\mathbf{p}|v_\mathbf{p}|^2+\left(1-n^P_\mathbf{p}\right)|u_\mathbf{p}|^2 \right]}$$
- The distribution is _strongly peaked_ around:
$$\langle N \rangle=2\sum_{\boldsymbol{p}}|v_{\boldsymbol{p}}|^{2}=2\sum_{\boldsymbol{p}}\langle n_{\boldsymbol{p}}^{P} \rangle  $$
- There is _variance_ $O(N)$, therefore at large $N$:
$$\langle{\text{BCS}}\rvert \mathcal{O} \lvert \text{BCS} \rangle\to \langle{\langle N\rangle \text{ pair}}\rvert \mathcal{O} \lvert \langle N\rangle\text{ pair} \rangle$$
- _Fixing_ the number of particles requires a _chemical potential_

## Anderson spin chain
- _Map_ the operators onto a _spin chain_
	- The _hardcore condition_ implies ladder operator behaviour
$$S_\mathbf{p}^+ \equiv b^\dagger_\mathbf{p},\quad S_\mathbf{p}^- \equiv b^{\vphantom{\dagger}}_\mathbf{p},\quad S^z_\mathbf{p}= b^\dagger_\mathbf{p}b^{\vphantom{\dagger}}_\mathbf{p}-1/2$$
- An _up_ spin indicates the _formation_ of a pair

- The spin commutation relations:
$$\left[b^\dagger_\mathbf{p},b^{\vphantom{\dagger}}_\mathbf{p}\right]=2\left(b^\dagger_\mathbf{p}b^{\vphantom{\dagger}}_\mathbf{p}-1/2\right)\qquad
\left[b^\dagger_\mathbf{p},\left(b^\dagger_\mathbf{p}b^{\vphantom{\dagger}}_\mathbf{p}-1/2\right)\right]=-b^\dagger_\mathbf{p}$$
- Model as a spin chain:
	- Interaction is _NOT nearest neighbour_
$$H_{\text{pair}}-\mu N=2\sum_\mathbf{p}\xi({\mathbf{p}})S_\mathbf{p}^z+\frac{U_0}{V}\sum_{\mathbf{p},\mathbf{p}'}S^+_\mathbf{p}S^-_{\mathbf{p}'}$$
- The _chemical potential_ $\mu$ is introduced to give $\xi(\boldsymbol{p})\equiv\epsilon(\boldsymbol{p})-\mu$

- Parametrise:
	- This gives $\pmatrix{u_{\boldsymbol{p}}&v_{\boldsymbol{p}}}^{\dagger}\boldsymbol{\sigma}\pmatrix{u_{\boldsymbol{p}}&v_{\boldsymbol{p}}}=\boldsymbol{\hat{n}}(\theta,\phi )$
$$(u_{\boldsymbol{p}},v_{\boldsymbol{p}})=(\cos(\theta/2)e^{i\varphi/2},\sin(\theta/2)e^{-i\varphi/2})$$
- Variational energy:
$$\langle{\text{BCS}}\rvert H \lvert \text{BCS} \rangle=-\sum_\mathbf{p}\xi_\mathbf{p}\cos\theta_\mathbf{p}+\frac{U_0}{4V}\sum_{\mathbf{p},\mathbf{p}'}\sin\theta_\mathbf{p} \sin\theta_{\mathbf{p}'}\cos\left(\varphi_\mathbf{p}-\varphi_{\mathbf{p}'}\right)$$
- The _first term_ tends to _align spins_ with $z-$axis
	- $-$ direction for $\xi_{\boldsymbol{p}}<0$ and vice versa
- The _second term_ tends to align spins in the $x-y$ plane

- For _repulsive interactions_ $U_{0}>0$, all spins point along $\pm z$
- The _average number_ of pairs:
$$\braket{ n^{P}_{\boldsymbol{p}}  }=v_{\boldsymbol{p}}^{2}=\frac{1+\cos\theta_{\boldsymbol{p}}}{2} $$
- There is a _domain wall_ where $\xi_{\boldsymbol{p}}$ _changes sign_, forming a _Fermi step_
![[Anderson spin chain map.png|400]]
- For _attractive_ interactions $U_{0}<0$, the system can _lower energy_ with $\sin\theta_{\boldsymbol{p}}\neq 0$, compensating for _excess kinetic energy_ from _smoothing_ the step

- To extremise energy, set _all azimuthal angles to be the same_
- Extremising gives: 
$$\xi_{\mathbf{p}}\sin\theta_\mathbf{p}-|\Delta|\cos\theta_\mathbf{p}=0$$
- Here, $\Delta$ is the _gap parameter_:
$$\Delta=-\frac{U_0}{2V}\sum_\mathbf{p}e^{i\varphi}\sin\theta_\mathbf{p}=-\frac{U_0}{V}\sum_\mathbf{p}u_\mathbf{p}v^*_\mathbf{p}$$
$$\cos\theta_\mathbf{p}=\frac{\xi_{\mathbf{p}}}{E_\mathbf{p}},\qquad \sin\theta_\mathbf{p}=\frac{|\Delta|}{E_\mathbf{p}}, \qquad E_\mathbf{p}=\sqrt{\xi
(\mathbf{p})^2+|\Delta|^2}$$
- Each spin corresponds to _aligning with an effective magnetic field_
	- An _up_ spin corresponds to the formation of a _pair_
$$\left(\mathrm{Re}\,\Delta,\mathrm{Im}\,\Delta,\xi_\mathbf{p}\right)$$
- To be _self consistent_, the _gap condition_ must be satisfied:
$$\Delta=-\frac{U_0}{2V}\sum_\mathbf{p}\frac{\Delta}{E_\mathbf{p}}=-\frac{U_0}{2}\int \frac{d\mathbf{p}}{\left(2\pi\right)^3} \frac{\Delta}{E_\mathbf{p}}$$
- For $U_{0}>0$, there are _no non-trivial solutions_

- In 3 dimensions, this is _divergent in the ultra-violet_
- With density of states per spin $\nu(\mu)$ and a high-energy cutoff $\Lambda$
$$\sim-\frac{U_0}{2}\nu(\mu)\Delta\log \Lambda/\Delta$$
- Even for _arbitrarily weak_ $U_{0}$, there is _always a solution_

### Quasiparticle excitations in BCS
- One can introduce _Bogoliubov-like_ excitations by choosing:
$$\begin{eqnarray}
\alpha^{\vphantom{\dagger}}_{\mathbf{p}\uparrow}&=&u_\mathbf{p}a^{\vphantom{\dagger}}_{\mathbf{p}\uparrow}-v_\mathbf{p}a^\dagger_{-\mathbf{p}\downarrow}\\
\alpha^{\vphantom{\dagger}}_{\mathbf{p}\downarrow}&=&u_{-\mathbf{p}}a^{\vphantom{\dagger}}_{\mathbf{p}\downarrow}+v_{-\mathbf{p}}a^\dagger_{-\mathbf{p}\uparrow}
\end{eqnarray}$$
- They still obey the _fermionic commutation relations_
- It annihilates the BCS state:
$$\alpha^{\vphantom{\dagger}}_{\mathbf{p},s}\lvert{\text{BCS}}\rangle\rangle=0$$
- Excited state, the _creation_ of a _quasiparticle_, which _stops $\boldsymbol{p},\uparrow$ from forming a pair_
$$\lvert{\mathbf{p},s}\rangle=\alpha^\dagger_{\mathbf{p},s}\lvert{\text{BCS}}\rangle=a^\dagger_{\mathbf{p},s}\prod_{\mathbf{p}'\neq \mathbf{p}} \left[v_{\mathbf{p}'}a^\dagger_
{\mathbf{p}'\uparrow}a^\dagger_{-\mathbf{p}'\downarrow}+u_{\mathbf{p}'}\right]\lvert{\text{VAC}}\rangle$$
- The level is said to be _blocked_
	- The corresponding term _no longer appears in the interaction_

- Taking _kinetic energy_ and _loss of interaction energy_ into account:
$$E_{s}(\mathbf{p})=\xi_{\mathbf{p}}[\overbrace{\left(1-\langle n^P_\mathbf{p}\rangle\right)}^{\left(\mathbf{p},s\right)\,\mathrm{occupied}}
\overbrace{-\langle n^P_\mathbf{p}\rangle}^{\left(-\mathbf{p},-s\right)\,\mathrm{empty}}]+\overbrace{\Delta\sin\theta_
\mathbf{p}}^{\mathrm{'blocking'}}=E_{\mathbf{p}}$$
- There is always a _gap_ in the dispersion:
$$\Delta_s=\min_\mathbf{p}E_\mathbf{p}=\begin{cases}
\Delta, & \mu>0,\\
\sqrt{\Delta^2+\mu^2},&  \mu<0.
\end{cases}$$
- In BCS, $\varphi$ also gives rise to _phase modes_
	- In _charged systems_, phase modes will have a _plasmon gap_
	- In _neutral systems_, they have a _gapless dispersion_

# Responses and correlation
- How systems _respond to external probes_
- The _evolution of fluctuations_ will _behave similarly to dissipation_

- There are both _quantum fluctuations_ and _thermal fluctuations_

## Fluctuations of an oscillator

### Fluctuations and noise in a single oscillator
- Consider the undamped oscillator, and its _ground state oscillations_
$$H=\frac{p^{2}}{2m}+\frac{1}{2}m\omega_{0}^{2}y^{2} \implies \braket{ 0|y^{2} |0  }= \frac{1}{2m\omega_{0}}$$
- At _finite temperature_, consider both _thermodynamic and quantum effects_:
$$\braket{  \braket{  y^{2}  }  } =\mathrm{Tr}[\rho y^{2}]=\frac{\coth(\beta\omega_{0}/2)}{2m\omega_{0}}$$

- For _time dependent fluctuations_, using the _Heisenberg picture_:
	- Assume _time-translation invariance_ of the system
$$\braket{ \braket{  y(t)y(0)  }   } $$
- This gives the _quantum noise power spectrum_:
$$S(\omega)=\int_{-\infty}^{\infty} \braket{  \braket{  y(t)y(0)  }  }  \exp(i\omega t) dt $$

- As time-evolved operators _do not commute_:
	- $\langle\langle y(t)y(0)\rangle\rangle\neq \langle\langle y(0)y(t)\rangle\rangle=\langle\langle y(-t)y(0)\rangle\rangle$
$$S(\omega)\neq S(-\omega)$$

- _Expanding_ $y(t)$ in terms of _energy eigenstates_:
$$S(\omega) = 2\pi\sum_{m,n} \frac{e^{-\beta E_n}}{Z} |\langle{n}\rvert y\lvert{m}\rangle|^2 \delta(\omega-E_m+E_n)$$

- It is composed of _weighted delta functions_ which become more _dense_ in the thermodynamic limit
- The _asymmetry_ is due to the _weighting_:
$$S(\omega) = S(-\omega) e^{\beta\omega}$$
- As $T\to 0$, or $\beta\to \infty$, only _positive_ $\omega$ survives

- For the _harmonic oscillator_, evaluating the matrix elements gives:
$$\begin{align}
S(\omega)&=\frac{\pi}{m\omega_0} \sum_n \frac{e^{-\beta E_n}}{Z} \left[n\delta(\omega+\omega_0)+(n+1)\delta(\omega-\omega_0)\right]\nonumber\\
& = \frac{\pi}{m\omega_0}\left[n_\text{B}(\omega_0)\delta(\omega+\omega_0)+(n_\text{B}(\omega_0)+1)\delta(\omega-\omega_0)\right]
\end{align}$$
- Here, the Bose distribution function:
$$n_{B}(\omega)\equiv \frac{1}{\exp(\beta\omega)-1}$$
- These terms are _asymmetrical_, as expected
- This also gives:
$$\int S(\omega)\frac{d\omega}{2\pi} = \langle\langle y^2\rangle\rangle= \frac{\coth(\beta\omega_0/2)}{2m\omega_0}$$

- One can take a _classical limit_ $\beta\omega\to 0$
$$S(\omega)\to \frac{k_{B}T}{2m\omega_{0}^{2}}\times 2\pi[\delta(\omega+\omega_{0})+\delta(\omega-\omega_{0})]$$
### Coupled oscillators
- Take a system of _coupled oscillators_:
$$\displaylines{y(t) = \sum_k \left[c^{}_k a^\dagger_k(t) + c_k^* a^{\vphantom{\dagger}}_k(t)\right] \\ a^\dagger_k(t) = e^{i\omega_k t}a^\dagger_k,\quad a^{\vphantom{\dagger}}_k(t) = e^{-i\omega_k t}a^{\vphantom{\dagger}}_k}$$
- This gives:
$$\begin{align}
S(\omega)= 2\pi\sum_k |c_k|^2\left[n_\text{B}(\omega_k)\delta(\omega+\omega_k)+(n_\text{B}(\omega_k)+1)\delta(\omega-\omega_k)\right]
\end{align}$$
- Then taking the _continuum limit_, this gives a _smooth function_
## Responses

### Response function of an oscillator
- The _Heisenberg equation of motion_:
$$\displaylines{H=\sum_{k}\omega_{k}a_{k}^{\dagger}a_{k}-f(t)y \\ \frac{da_{k}}{dt}=-i\omega_{k}a_{k}+ic_{k}f(t)}$$
- The solution is:
$$\displaylines{a_{k,f}(\omega)=\exp(-i\omega_{k}t)a_{k}(0)+a_{k,f}(t) \\ a_{k,f}(\omega)\equiv \frac{c_{k}}{\omega_{k}-\omega-i\epsilon}f(\omega)}$$
- The $i\epsilon$ prescription moves the _poles_ such that response is _always causal_
	- The response $\chi(t-t')$ must be 0 for $t<t'$

- Transforming back to $y$:
$$y(\omega) = \sum_k |c_k|^2\left[\frac{1}{\omega_k-\omega-i0}+\frac{1}{\omega_k+\omega+i0}\right]f(\omega)=y^{*}(-\omega)$$
- This defines the _response function_:
$$\chi(\omega) \equiv \frac{y(\omega)}{f(\omega)}= \sum_k |c_k|^2\left[\frac{1}{\omega_k-\omega-i0}+\frac{1}{\omega_k+\omega+i0}\right]$$
- Then using:
$$\mathrm{Im} \frac{1}{x\mp i0}=\pm \pi\delta(x)$$
- This gives:
$$\mathrm{Im }\,\chi(\omega) = \mathrm{sgn}(\omega)\,\pi\sum_k |c_k|^2\delta(\omega_k-\omega)$$

- The _quantum fluctuation-dissipation relation_:
$$S(\omega) = 2\mathrm{Im}\,\chi(\omega)\left[n_\text{B}(\omega)+1\right]$$
### Linear response function
- For any _drive_ $f(t)$, in a _linear system_, the response:
$$y(t)=\int  \chi(t-t')f(t')\,dt' $$
- $\chi(t-t')$ is the _response function_

- Due to causality:
$$\chi(t<0)=0$$
- $\chi(\omega)$ is _only analytic in the upper half-plane_

### Dissipation
- From the _Golden Rule_, the _dissipation_ in energy for $f(t)=f_{0}\cos(\omega t)$
$$\omega\Gamma(\omega) = \omega S(\omega)\left(\frac{f_0}{2}\right)^2 = \frac{1}{2}\omega\chi''(\omega)\left[n_\text{B}(\omega)+1\right]f_0^2$$
## Formal theory
- Let there be some _general perturbed Hamiltonian_
$$H_{t}=H_{0}-\lambda _{t}B$$
- Here, $B=-\partial H/\partial\lambda$ is the _generalised force_ to the _general displacement_ $\lambda_{t}$

### Kubo formula
- In the _interaction picture_:
$$\displaylines{B_{I}(t)=e^{iH_{0}t}Be^{-iH_{0}t} \\ i\frac{\partial \lvert{\Psi_I(t)}\rangle}{\partial t} = -\lambda_t B_I(t) \lvert{\Psi_I(t)}\rangle}$$
- From _first order time-dependent perturbation theory_:
$$\displaylines{\lvert{\Psi_I(t)}\rangle=\lvert{\Psi(0)}\rangle+\lvert{\Psi^{(1)}_I(t)}\rangle+\cdots \\ \lvert{\Psi^{(1)}_I(t)}\rangle = i\int_0^t dt' \lambda_{t'} B_I(t') \lvert{\Psi(0)}\rangle}$$
- The _expectation value of some observable_:
$$\begin{align}
\langle{\Psi(t)}\rvert A\lvert{\Psi(t)}\rangle &= \langle{\Psi_I(t)}\rvert A_I(t) \lvert{\Psi_I(t)}\rangle\\
&=\langle{\Psi(0)}\rvert A_I(t)\lvert{\Psi(0)}\rangle +i \int_0^t dt' \lambda_{t'}\langle{\Psi(0)}\rvert \left[A_I(t),B_I(t')\right] \lvert{\Psi(0)}\rangle
\end{align}$$
- Then doing a _thermal average_, one gets the _Kubo formula_
	- Using the _Heisenberg picture of the unperturbed system_
$$\chi_{AB}(t) = i\langle\langle\left[A_I(t),B_I(0)\right]\rangle\rangle,\quad t>0$$
- This is the _Kubo formula_, expressing $\chi$ in terms of the _dynamics of the unperturbed system_

### General fluctuation-dissipation theorem
- _Define_ the _correlation function_:
$$S_{AB}(t) \equiv \langle\langle A_I(t)B_I(0)\rangle\rangle$$
- From the cyclic property of the trace:
$$S_{AB}(t) = S_{BA}(-t-i\beta)\implies S_{AB}(\omega) = e^{\beta\omega} S_{BA}(-\omega)$$
- The response function is then:
$$\begin{align}
\chi_{AB}(t) &= \begin{cases}
i\left[S_{AB}(t)-S_{BA}(-t)\right] & t>0\\
0 & t<0
\end{cases}  \\
&=i\theta(t)[S_{AB}(t)-S_{BA}(-t)]
\end{align}$$
- Therefore, $\chi_{AB}(\omega)$ is a _convolution_ with the step function:
$$\displaylines{\tilde{\theta}(\omega)=\frac{i}{\omega+i0} \\ \begin{align}
\chi_{AB}(\omega)&= -\int \frac{d\omega'}{2\pi}\frac{S_{AB}(\omega')-S_{BA}(-\omega')}{\omega-\omega'+i0}\\
&=-\int \frac{d\omega'}{2\pi}\frac{S_{AB}(\omega')\left[1-e^{-\beta\omega'}\right]}{\omega-\omega'+i0}
\end{align}}$$
- Then using the _Kramers-Kronig relation_:
$$\begin{align}
\chi_{AB}(\omega) &=\chi'(\omega) + i\chi''(\omega)\\
&= \mathcal{P}\int_{-\infty}^\infty \frac{d\omega'}{\pi}\frac{\chi''(\omega')}{\omega'-\omega} + i\chi''(\omega)\\
&= \int_{-\infty}^\infty \frac{d\omega'}{\pi}\frac{\chi''(\omega')}{\omega'-\omega-i0}
\end{align}$$
- The quantum fluctuation dissipation relation can then be read off:
$$S_{AB}(\omega) = 2\chi_{AB}''(\omega)\left[n_\text{B}(\omega)+1\right]$$
### Spectral representation
- In terms of the energy eigenstates:
$$S_{AB}(\omega)  = 2\pi\sum_{m,n} \frac{e^{-\beta E_m}}{Z} \langle{m}\rvert A\lvert{n}\rangle\langle{n}\rvert B\lvert{m}\rangle \delta(\omega-E_n+E_m)$$

## Response of matter
- A system subject to the _perturbation_:
$$H_\text{pert} = \sum_{j=1}^N V(\mathbf{r}_i,t) = \int  V(\mathbf{r},t)\rho(\mathbf{r})\, d\mathbf{r}= \frac{1}{L^3}\sum_\mathbf{q}V_\mathbf{q}(t) \rho_{-\mathbf{q}}$$
- Perturbation _couples to the density_

### Structure factor
- The _general linear response for the density_, in a system with _translational invariance_:
$$\rho(\boldsymbol{r},t)=\int  \chi(\boldsymbol{r}-\boldsymbol{r}',t-t')V(\boldsymbol{r}',t')\,d^{3}\boldsymbol{r}'\,dt' $$
- One can then write in _Fourier space_:
$$\langle\langle \rho_\mathbf{q}(t)\rangle\rangle = -\frac{1}{L^3} \int_{-\infty}^t  \chi^{\rho}_\mathbf{q}(t-t') V_\mathbf{q}(t)\,dt'$$
- The density response function, from the [[#Kubo formula]]
$$\chi_\rho(\mathbf{q},t) = i\langle\langle\left[\rho_\mathbf{q}(t),\rho_{-\mathbf{q}}(0)\right]\rangle\rangle$$
- This setup has $A=\rho_{\boldsymbol{q}},B=\rho_{-\boldsymbol{q}}$

- Then define:
$$S_{\rho}(\boldsymbol{q},t)=\langle\langle \rho_{\boldsymbol{q}}(t)\rho_{-\boldsymbol{q}}(0)\rangle\rangle$$
- Using $\rho_{\boldsymbol{q}}=\rho_{-\boldsymbol{q}}^{\dagger}$, and the _spectral representation_, one gets the _dynamical structure factor_ $S_{\rho}(\boldsymbol{q},\omega)$ at _zero temperature_ 
	- $\exp(-\beta E_{m})/Z=\delta_{m{0}}$
$$S_\rho(\mathbf{q},\omega) = 2\pi\sum_{n}  |\langle{0}\rvert\rho_\mathbf{q}\lvert{n}\rangle|^2 \delta(\omega-E_n+E_0)$$
- Then, summing up the _equal time contributions_, one gets the _static structure factor_
$$S_\rho(\mathbf{q}) = \int S_\rho(\mathbf{q},\omega) \frac{d\omega}{2\pi} = \langle\langle\rho_\mathbf{q}\rho_{-\mathbf{q}}\rangle\rangle$$
- This quantifies all _equal time density fluctuations_ in the system

### Sum rules
- Properties of structure factor _regardless of the system_

#### f-sum rule
- Assume the _interaction only depends on density_:
$$[H_\text{int},\rho_{\boldsymbol{q}}]=0 \implies [H,\rho_{\boldsymbol{q}}]=[T,\rho_{\boldsymbol{q}}]$$
- By explicit calculation:
$$[[H,\rho_\mathbf{q}],\rho_{-\mathbf{q}}] = -\frac{N\mathbf{q}^2}{m}$$
- From resolution of identity:
$$\braket{ 0|[[H,\rho_{\boldsymbol{q}}],\rho_{-\boldsymbol{q}}] |0  } =2\sum_{n} |\braket{ 0|\rho_{\boldsymbol{q}} |n  }|^{2}(E_{0}-E_{n}) $$
- Relate this to the _spectral representation_ of $S_{\rho}(\boldsymbol{q},\omega)$

- The _f-sum rule_:
$$\int_{-\infty}^\infty \omega S(\mathbf{q},\omega) \frac{d\omega}{2\pi}= \frac{N\mathbf{q}^2}{2m}$$

#### Compressibility sum rule
- The _compressibility_:
$$\beta=-\frac{1}{V}\frac{\partial V}{\partial p}$$
- At _zero temperature_, $p=-\partial E_{0}/\partial V$, therefore with _energy per unit volume_ $\epsilon$:
$$\beta^{-1}=\rho^{2}\epsilon''(\rho)$$
- In the presence of $V(\boldsymbol{r})$, the _change in energy density_ is:
$$\epsilon(\rho_0+\delta\rho)-\varepsilon(\rho_{0}) = \frac{1}{2\beta\rho_0^2} \left[\delta\rho\right]^2 + V(\mathbf{r})\delta\rho$$
- Minimising the change:
$$\epsilon(V(\mathbf{r})) = - \frac{\beta\rho_0^2}{2} \left[V(\mathbf{r})\right]^2$$
- Compare this result to _second order perturbation theory_, for a perturbation of some wave-vector $\boldsymbol{q}$
$$\displaylines{\sum_{j}V_{0}\cos(\boldsymbol{q}\cdot \boldsymbol{r}_{j})=\frac{V_{0}}{2}(\rho_{-\boldsymbol{q}}+\rho_{\boldsymbol{q}}) \\ E^{(2)}=\frac{V_{0}^{2}}{4}\sum_{n\neq 0}\frac{|\braket{ 0|\rho_{\boldsymbol{q}} |n  }|^{2}}{E_{0}-E_{n}}=-\frac{V_{0}^{2}}{4}\int_{0}^{\infty}\frac{S(\boldsymbol{q},\omega)}{\omega}\, \frac{d\omega}{2\pi}  }$$
- This gives the _compressibility sum rule_:
$$\lim_{\mathbf{q}\to 0}\int_0^\infty \frac{S(\mathbf{q},\omega)}{\omega}\frac{d\omega}{2\pi} = \frac{N\rho\beta}{2}\equiv \frac{N}{2mc^{2}}$$
- Here, $c\equiv(\beta m\rho)^{-1/2}$ is the _speed of sound_

### Onsager bound
- From the _Cauchy-Schwarz inequality_:
$$\left|{\int f(x)g^*(x) dx}\right|^2 \leq \int \lvert{f(x)}\rvert^2 dx \int \lvert{g(x)}\rvert^2 dx$$
- The _Onsager bound_ on the _static structure factor_:
$$\lim_{\mathbf{q}\to 0}\frac{S_\rho(\mathbf{q})}{\lvert{\mathbf{q}}\rvert}\leq \frac{N}{2mc}$$
### Single mode approximation
- Some Bose gases at _low momentum_ are described by a _single mode_:
$$S_\rho(\mathbf{q},\omega) \sim 2\pi S_\rho(\mathbf{q}) \delta(\omega - \omega(\mathbf{q}))$$
- Here, $\omega(\boldsymbol{q})$ corresponds to the _collective excitations_ in the gas

- The f-sum rule gives:
$$S_\rho(\mathbf{q}) = \frac{N\mathbf{q}^2}{2m\omega(\mathbf{q})}$$
- For a _Bose condensate_ with no interactions $(\omega=q^{2}/2m)$
$$S_{\rho}^{\text{BEC}}(\boldsymbol{q})=N$$
- Particle positions are _uncorrelated_ with _Poisson statistics_

- For a _linear dispersion_
	- Elastic chain or Bogoliubov at low $\boldsymbol{q}$
$$S_\rho(\mathbf{q}) = \frac{N|\mathbf{q}|}{2mc}$$
- Density fluctuations _vanish_ as $\boldsymbol{q}\to 0$
	- There are _long-range correlations_ between positions in the _ground state_