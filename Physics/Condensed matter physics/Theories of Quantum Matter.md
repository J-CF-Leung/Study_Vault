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

- Single particle density:
$$\rho_1(x_1) = N \int dx_2\ldots dx_N \,\lvert\Psi(x_1,x_2,\ldots,x_N)\rvert^2$$
$$\rho(x)=\sum_{j}\delta(x-x_{j}) \qquad \rho_{1}(x)=\braket{ \Psi|\rho(x) |\Psi  } $$
- Single particle density matrix:
$$g(x,y) \equiv N\int dx_2\ldots dx_N \,\Psi^{}(x,x_2,\ldots,x_N)\Psi^{*}(y,x_2,\ldots,x_N)$$
- Pair correlations:
$$\rho_2(x_1,x_{2}) = N(N-1) \int dx_3\ldots dx_N \,\lvert\Psi(x_1,x_2,\ldots,x_N)\rvert^2$$
$$\rho_{2}(x_{1},x_{2})=\rho_{1}(x_{1})\rho_{2}(x_{2})-g(x_{1},x_{2})g(x_{2},x_{1})$$
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
- States that satisfy:
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
- Analagous to the [[Second quantisation#Example Free particles on a ring|1D Fermi gas]], where states are simply $z^{n}$
	- 1D - powers of plane wave states $z$ / 2D - $z$ living on complex plane
- Similar arguments give:
$$\Psi(z_1,\ldots, z_N) = \prod_{j<k}^N (z_j-z_k) \exp\left(-\frac{1}{4}\sum_{j=1}^N\left|z_j\right|^2\right)$$
- The _single particle density_:
$$\rho_1(z,\bar z) = \frac{e^{-|z|^2/2}}{2\pi}\sum_{n=0}^{N-1} \frac{\left|z\right|^{2n}}{2^n n!} = \frac{1}{2\pi} \frac{\Gamma(N,|z|^2/2)}{(N-1)!}$$
![[LLL density.png|500]]
- At _small_ $|z|$, approximate by an _infinite sum_ such that $\rho_{1} \to 1/2\pi$
- Density is _fixed_ until $|z| \sim \sqrt{ 2N }$, after which it _falls_ to zero with _length scale_ $l_{B}$
- The filled LLLs can be described as a _circular droplet_

- There is _one state_ per _flux quantum_ $h/e$

- A _different confining potential_ will change the _droplet shape_

## Laughlin wavefunction
- A _generalised Laughlin wavefunction_:
$$\Psi_m(z_1,\ldots, z_N) = \prod_{j<k}^N (z_j-z_k)^{m} \exp\left(-\frac{1}{4}\sum_{j=1}^N\left|z_j\right|^2\right)$$
- For $m\neq 1$, it is _not a product state_

- For $m$ _odd/even_, it is (anti)symmetric hence it is for _fermions/bosons_

### m=2 boson state
- For the _delta function repulsion_:
$$H_{\text{int}} = g\sum_{j<k}\delta(\mathbf{r}_j-\mathbf{r}_k)\quad,\quad g>0$$

- $m=2$ state has _zero interaction energy_ as the state _prevents bunching_

- Hence, _states with no interaction energy_ must have $\Psi_{2}$ as a _factor_
	- For a _higher degree wave-function_, any perturbing harmonic potential will give a higher energy
	- $\Psi_{2}$ is the _ground state_

- _Compared_ to an _uncorrelated sampling_, the Laughlin state results in _more uniform sampling_ due to the anti-bunching
	- Left: uncorrelated ; Right: Laughlin
![[Laughlin state.png]]

### Plasma statistical analogy
- Coulomb potential in _2 dimensions_:
$$\nabla^{2}V=-q\delta(\boldsymbol{r}) \implies V=-\frac{q}{2\pi}\log|\boldsymbol{r}|$$
- For a _constant charge density_:
$$V=\frac{\rho_{0}}{4}|\boldsymbol{r}|^{2}$$
- Then, for a _collection of charges_ with a _constant background_:
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

### Excited states and fractional charge
- The _simplest_ excited state is the _quasi-hole_ state
	- It is also _degenerate_ as energy is independent of $Z$ 
	- A _higher power_ of the excitation part would mean _multiple excitations_, meaning a higher energy
$$\Psi_\text{hole}(z_1,\ldots, z_N|Z) = \left(\prod_j (Z-z_j)\right)\Psi_m(z_1,\ldots, z_N)$$
- Applying the plasma analogy again:
$$V(\mathbf{r}_1, \ldots, \mathbf{r}_N)=-\frac{q^2}{2\pi m}\sum_j \log\left|\mathbf{r}_j-\mathbf{R}\right|-\frac{q^2}{2\pi} \sum_{j<k}\log\left|\mathbf{r}_j-\mathbf{r}_k\right|+ \frac{\rho q_0}{4}\sum_j \left|\mathbf{r}_j\right|^2$$
- This state describes _adding a fractional charge_ $q/m$, at location $Z=X+iY$
- The _plasma_ will then _screen_ the charge, leaving a _hole_ of fractionalised charge $-q/m$ 

### Fractional statistics
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
- This is a _sum of_ [[Quantum Harmonic Oscillator|quantum harmonic oscillators]] at different wavenumbers, and the _dispersion relation_ emerges

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
- Limit of a _large system_, with $N \to \infty$
- One expects energy to be _extensive_

- As $N\to \infty$, calculate ground state energy as:
$$E_{0}\to \frac{N}{2} \int  \frac{d \eta}{2\pi} \omega=\frac{2N}{\pi} \sqrt{ \frac{k}{m} } $$

### Continuum limit
- Treating the chain as a _continuum_ of length $L=Na$
- Take the $1\text{D}$ density $\rho$, with $m=\rho a$

- The _elastic modulus_ (dimension independent quantity) is:
$$\kappa=ka$$
- In terms of material properties, one then gets:
$$\frac{E_{0}}{L}=\left( \frac{N}{L} \right)^{2} \frac{2}{\pi} \sqrt{ \frac{\kappa}{\rho} }$$

- As one _approaches a continuum of finite length_, the _energy density diverges_
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
- _Bragg peaks_ are _replaced_ with cusps
- _Long range order_ is destroyed in one dimension
![[1D Bragg peaks.png]]

- The _prevention_ of crystalisation forms _quantum liquids_
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
- Does not respect rotational symmetry

## Heisenberg ferromagnetic chain
$$H=J\sum_{\langle jk \rangle } \boldsymbol{s}_{j}\cdot \boldsymbol{s}_{k}$$
- A _rotationally symmetric_ model

- Take the _1D spin chain_:
$$H = J \sum_{j=1}^N \mathbf{s}_j \cdot \mathbf{s}_{j+1}$$
- Convenient identity:
$$\boldsymbol{s}_{i}\cdot \boldsymbol{s}_{j}=s_{i}^{z}s_{j}^{z}+\frac{1}{2}(s_{i}^{+}s_{j}^{-}+s^{-}_{i}s_{j}^{+})$$
- Periodic boundary conditions: $\boldsymbol{s}_{j}=\boldsymbol{s}_{j+N}$

### Ground states
- The _ferromagnet_ state, with _all spins aligned_:
$$\ket{\text{FM}}\equiv \ket{+}_{1}\ket{+}_{2}\dots\ket{+}_{N} $$
- It is an eigenstate of the Hamiltonian with eigenvalue $JN/4$

- Consider the _total spin_ $\boldsymbol{S}$
- An eigenstate of $S^{z}$ and $S^{2}$, with eigenvalues $N/2$ and $N (N/2-1)/2$
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

- $N$ one-magnon states out of $2^{N}$ states

- The down spins propagate as _magnons_

### N-magnon states
- A magnon has energy $\propto|J|$
- Systems of _extensive_ energy and finite temperature will have _many_ magnons

- For $n$ flipped spins, the _dimension_ of the subspace is $\pmatrix{N \\ n}$

- Magnons _cannot sit on the same site_, and can _scatter_

### Anti-ferromagnets
- Anti-ferromagnet: the _ground state_ for $J>0$
$$\ket{\text{AFM}?}= $$
- _Not_ an eigenstate of he Hamiltonian 
	- Flipping spins moves them around

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

- Writing in terms of $x$ and $p$:
$$\begin{align}
s^x &\sim \sqrt{s}x \\
s^y &\sim  \sqrt{s}p\\
s_z &= \left(s - \frac{1}{2}[x^2 + p^2 - 1] \right)
\end{align}$$
- The Hamiltonian:
$$H\sim NJ s^2 + sNJ+ \overbrace{sJ \sum_{j=1}^N \left[x_j x_{j+1} + p_j p_{j+1}-x_j^2 - p_j^2\right]}^{\equiv H^{(2)}} + \ldots$$
- Use the _Fourier expansions_:

- One _regains_ the dispersion relation:
	- Approximation is still _few oscillator quanta_
$$\omega_{\text{FM}}(\eta) = 4s\left|J\right|\sin^2(\eta/2)$$
### Anti-ferromagnetic case
- For the _ferromagnet_, _close to ground state_, the harmonic approximation _applies_

- The anti-ferromagnetic state has _many flipped spins_ to make it "far away" from FM state

- Therefore, _rotate every other spin_ through $\pi$ about the $y$ axis
- This _changes the Hamiltonian_:
$$H = -J \sum_{j=1}^N \left[s^x_j s^x_{j+1} - s^y_j s^y_{j+1} + s^z_j s^z_{j+1}\right]$$
- Therefore, the _harmonic oscillation applies_ close to the AFM state
$$\omega_{\text{AFM}}(\eta) = 2sJ\left|\sin(\eta)\right|$$
- _Vanishes_, and is _linear_ at $\eta=0$ and $\eta=\pi$

- Ferromagnet: _both_ position and momentum terms _vanish_ at $\eta=0$
- Anti-ferromagnet: _eiher_ position or momentum vanish at $\eta=0$ or $\eta=\pi$

- For the anti-ferromagnet, the _size_ of the unit cell is _doubled_, therefore _halving_ the period
### Ground state fluctuations
- Crude approximation:
$$\braket{ \text{FM}|s_{j}^{z} | \text{FM} } =s \qquad \braket{ \text{AFM}|s_{j}^{z} | \text{AFM} } =s(-1)^{j}$$
- In Holstein-Primakoff, there is an _additional term_
$$s_{j}^{z}=s-a_{j}^{\dagger}a_{j}$$
- FM: commutes with Harmonic Hamiltonian
- AFM: does not commute

- AFM: evaluate $\Delta s=\braket{ 0|a_{j}^{\dagger}a_{j} | 0 }$

$$\begin{align}
\Delta s &= - \langle{0}\rvert\frac{1}{N}\sum_{j=1}^N a^\dagger_j a^{\vphantom{\dagger}}_j\lvert{0}\rangle\\
&= \frac{1}{2}-\frac{1}{4N}\sum_n \left[|\tan(\eta_n/2)| + |\cot(\eta_n/2)|\right]\\
&= \frac{1}{2}- \frac{1}{4}\int_{-\pi}^\pi \frac{d\eta}{2\pi} \left[|\tan(\eta_n/2)| + |\cot(\eta_n/2)|\right]
\end{align}$$
- There must be a _cutoff_ for the integral to stop the divergence
- From this, one gets:
$$\Delta s\sim -\log \eta _\text{min}\sim -\log \left( \frac{2\pi}{N} \right)\sim \log N$$

### Two-dimensional square lattice