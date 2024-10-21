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