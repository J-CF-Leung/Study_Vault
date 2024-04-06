- Electrons in atoms have many different _energy levels_
	- [[The hydrogen atom|Hydrogenic energy levels]]
	- [[Atomic and molecular physics|Energy levels of multi-electron atoms]]

- An _external_, [[Time-dependent quantum mechanics|time-dependent perturbation]] can cause _transitions_ between those energy levels
- There are [[Atomic and molecular physics|transition rules]] that _restrict possible transitions_
- The _rate_ of transition is given by [[Time-dependent quantum mechanics#Fermi's Golden Rule|Fermi's Golden Rule]]:
$$\Gamma _\text{absorb}(0\to k)=\frac{2\pi}{\hbar}|U_{k0}|^{2}g(E_{k})$$
- Here, $g(E_k)$ is the _density of final states_

# Form of external perturbation
- The perturbation is typically given by an _electromagnetic field_
- An $N-$electron atom in a field with potentials $\phi(\boldsymbol{r},t)$ and $\boldsymbol{A}(\boldsymbol{r},t)$ has the _Hamiltonian_:
$$\hat{H}=\sum_{i=1}^{N} \frac{1}{2m_{e}} \Big|\hat{\boldsymbol{p}}_{i}+e\boldsymbol{A}(\boldsymbol{r}_{i},t)\Big|^{2}-e\sum_{i=1}^{N} \phi(\boldsymbol{r}_{i},t)+V\big(\{r_{i},r_{ij}\}\big)$$

- In the _Coulomb gauge_:
$$\Big|\hat{\boldsymbol{p}}_{i}+e\boldsymbol{A}(\boldsymbol{r}_{i},t)\Big|^{2}=|\hat{p}_{i}|^{2}+2e\hat{\boldsymbol{p}}_{i}\cdot \boldsymbol{A}+e^{2}|\boldsymbol{A}|^{2}$$
- In an EM field with $\phi=0$, the Hamiltonian can be written as the time-independent part, and a _time-dependent perturbation_:
$$\displaylines{\hat{H}(t)=\hat{H}_{0}+\hat{H}'(t) \\ \hat{H}_{0}=\sum_{i=1}^{N} \frac{1}{2m_{e}}\hat{p}_{i}^{2}+V\hspace{1.5cm}\hat{H}'(t)=\sum_{i=1}^{N} \frac{e}{m_{e}}\hat{\boldsymbol{p}}_{i}\cdot \boldsymbol{A}(\boldsymbol{r}_{i},t)}$$

- From the [[Quantum electrodynamics#Quantised electromagnetic field|quantised EM field]], the vector potential can be written as an _operator_:
$$\displaylines{\hat{H}'(t)=\sum_{i=1}^{N} \frac{e}{m_{e}}\hat{\boldsymbol{A}}(\boldsymbol{r}_{i},t)\cdot \hat{\boldsymbol{p}}_{i} \\ \hat{\boldsymbol{A}}(\boldsymbol{r},t)=\sum_{\boldsymbol{k},\lambda}N(\boldsymbol{k})\Big[\hat{a}_{\boldsymbol{k},\lambda}\exp[i(\boldsymbol{k}\cdot \boldsymbol{r}-\omega t)]e_{\lambda}(\boldsymbol{k})+\hat{a}_{\boldsymbol{k},\lambda}^{\dagger}\exp[-i(\boldsymbol{k}\cdot \boldsymbol{r}-\omega t)]e_{\lambda}^{*}(\boldsymbol{k})\Big] }$$
- From this, one writes the _contribution from_ the $i-$th electron, and a _single mode_ $(\boldsymbol{k},\lambda)$
$$\hat{H}'_{i,\boldsymbol{k},\lambda}(t)= \frac{e}{m_{e}}N(\boldsymbol{k})\Big[\hat{a}_{\boldsymbol{k},\lambda}\exp[i(\boldsymbol{k}\cdot \boldsymbol{r}-\omega t)]\boldsymbol{e}_{\lambda}(\boldsymbol{k})+\hat{a}_{\boldsymbol{k},\lambda}^{\dagger}\exp[-i(\boldsymbol{k}\cdot \boldsymbol{r}-\omega t)]\boldsymbol{e}_{\lambda}^{*}(\boldsymbol{k})\Big]\cdot \hat{\boldsymbol{p}}_{i}$$

- This is of the form of the perturbation, where [[Time-dependent quantum mechanics#Fermi's Golden Rule|Fermi's Golden Rule]] is applicable:
$$\displaylines{\hat{H}_{i,\boldsymbol{k},\lambda}(t)=\hat{U}\exp(-i\omega t)+\hat{U}^{\dagger}\exp(i\omega t) \\ \hat{U}=\frac{e}{m_{e}}N(k)\hat{a}_{\boldsymbol{k},\lambda}\exp(i\boldsymbol{k}\cdot \boldsymbol{r})\boldsymbol{e}_{\lambda}(\boldsymbol{k})\cdot \hat{\boldsymbol{p}}_{i}}$$

# Transitions
- Any transition in the state of the _atom_ also involves a _transition in the EM field_
- For some transition $\ket{1}\to \ket{2}$:
$$\begin{align} \ket{1}&=\ket{\alpha;\alpha _\text{EM}}=\ket{\alpha}\otimes \ket{\alpha _\text{EM}} \\ \ket{2}&=\ket{\beta;\beta _\text{EM}}=\ket{\beta}\otimes \ket{\beta _\text{EM}}  \end{align}$$

## Absorption
- Consider an _absorption_, where $E_{\beta}>E_{\alpha}$:
$$\Gamma(1\to 2)=\frac{2\pi}{\hbar} |U_{21}|^{2}\delta(E_{\beta}-(E_{\alpha}+\hbar\omega))$$
- Computing the matrix element:
$$\begin{align}U_{21}&\equiv \braket{ \beta;\beta _\text{EM}|\hat{U} |\alpha;\alpha _\text{EM}}\\ &= \frac{e}{m_{e}}N(\boldsymbol{k})\Braket{ \beta;\beta _\text{EM}|\hat{a}_{\boldsymbol{k},\lambda}\exp(i\boldsymbol{k}\cdot \boldsymbol{r})\boldsymbol{e}_{\lambda}(\boldsymbol{k})\cdot \hat{\boldsymbol{p}}_{i} |\alpha;\alpha _\text{EM}  } \end{align} $$

- In atomic transitions, the _wavelength_ is often much _longer_ than the size of the atom, hence one can _approximate_ $\exp(i\boldsymbol{k}\cdot \boldsymbol{r})\approx 1$
	- The _spatial_ variation is neglected, hence only the _time dependence matters_
- Factorising the matrix element:
$$U_{21}=\frac{e}{m_{e}}N(\boldsymbol{k})\braket{ \beta|\boldsymbol{e}_{\lambda}(\boldsymbol{k})\cdot \hat{\boldsymbol{p}}_{i} |\alpha  }\braket{ \beta _\text{EM}|\hat{a}_{\boldsymbol{k},\lambda} |\alpha _\text{EM}  }  $$
- The matrix element is _only non-zero_ if the field _loses a photon_ from the mode $(\boldsymbol{k},\lambda)$:
$$\ket{\alpha _\text{EM}}=\ket{\dots n_{\boldsymbol{k},\lambda}+1\dots}  \hspace{1cm}\ket{\beta _\text{EM}}=\ket{\dots n_{\boldsymbol{k},\lambda}\dots}  $$
- _All other modes_ must remain _unchanged_
	- Vectors of other modes are orthonormal

- The mode $(\boldsymbol{k},\lambda)$ is _any mode that can ensure energy conservation_:
$$\omega=\omega(\boldsymbol{k})=c|\boldsymbol{k}|=\omega_{\beta}-\omega_{\alpha}\hspace{1.5cm}E_{\alpha,\beta}=\hbar\omega_{\alpha,\beta}$$

- In the case of $E_{\beta}>E_{\alpha}$, the _dominant_ process is _absorption_ of a _single photon_:
![[Absorption of photon.png]]
- The matrix element is:
$$U_{21}=\frac{e}{m_{e}}N(\boldsymbol{k})\sqrt{ n_{\boldsymbol{k},\lambda}+1 }\braket{ \beta|\boldsymbol{e}_{\lambda}(\boldsymbol{k})\cdot \hat{\boldsymbol{p}}_{i} |\alpha  } $$

## Emission
- Consider _emission_, where $E_{\beta}<E_{\alpha}$:
$$\Gamma(1\to2)=\frac{2\pi}{\hbar}|U_{21}^{\dagger}|^{2}\delta(E_{\beta}-(E_{\alpha}-\hbar\omega)) $$
- The matrix element:
$$U_{21}^{\dagger}=\frac{e}{m_{e}}N(\boldsymbol{k})\braket{ \beta|\boldsymbol{e}^{*}_{\boldsymbol{k},\lambda}\cdot \hat{\boldsymbol{p}}_i |\alpha  }\braket{ \beta _\text{EM}|\hat{a}^{\dagger}_{\boldsymbol{k},\lambda} |\alpha _\text{EM}  }  $$
- The only way to have it be non-zero is to have the EM field _gain a photon_ in this mode:
$$\ket{\alpha _\text{EM}}=\ket{\dots n_{\boldsymbol{k},\lambda}\dots}  \hspace{1cm}\ket{\beta _\text{EM}}=\ket{\dots n_{\boldsymbol{k},\lambda}+1\dots}$$
- The matrix element is:
$$U_{21}^{\dagger}=\frac{e}{m_{e}}N(\boldsymbol{k})\sqrt{ n_{\boldsymbol{k},\lambda}+1 }\braket{ \beta|\boldsymbol{e}_{\lambda}^{*}(\boldsymbol{k})\cdot \hat{\boldsymbol{p}}_{i} |\alpha  } $$
- In the case of $E_{\beta}<E_{\alpha}$, the dominant process is _emission_ of a single photon
![[Emission of photon.png]]

### Spontaneous and stimulated emission
- The case $n_{\boldsymbol{k},\lambda}=0$ corresponds to _spontaneous emission_, where the atom emits a photon for a _previously unoccupied mode_

- The case $n_{\boldsymbol{k},\lambda}\geq 1$ corresponds to _stimulated emission_, where a photon is added to an _already occupied mode_
- A photon is emitted with the _same energy, direction, polarisation state_
![[Spontaneous, stimulated emission.png]]

# Emission rates
- In the case of _emission_, the rate is dependent on the matrix element:
$$U_{21}^{\dagger}=\frac{e}{m_{e}}N(\boldsymbol{k})\sqrt{ n_{\boldsymbol{k},\lambda}+1 }\braket{ \beta|\boldsymbol{e}_{\lambda}^{*}(\boldsymbol{k})\cdot \hat{\boldsymbol{p}}_{i} |\alpha  } $$

## Evaluating the rate
- To evaluate the matrix element, use the _commutation relations_ (with $i,j$ labelling _electrons_):
$$[\hat{\boldsymbol{r}}_{i},\hat{\boldsymbol{p}}_{j}^{2}]=2i\hbar \hat{\boldsymbol{p}}_{i}\delta_{ij}\hspace{1.5cm}[\hat{\boldsymbol{r}}_{i},\hat{V}]=0$$
- The _unperturbed_ Hamiltonian $\hat{H}_{0}$ then satisfies:
$$[\hat{\boldsymbol{r}}_{i},\hat{H}_{0}]=\frac{i\hbar}{m_{e}}\hat{\boldsymbol{p}}_{i}$$

- _Substituting and expanding_ the commutator, one gets:
$$U_{21}^{\dagger}=-\frac{ie}{\hbar}N(\boldsymbol{k})(E_{\alpha}-E_{\beta})\sqrt{ n_{\boldsymbol{k},\lambda}+1 }\braket{ \beta|\boldsymbol{e}^{*}_{\lambda}(\boldsymbol{k})\cdot \hat{\boldsymbol{r}}_{i} |\alpha  } $$
- Defining the frequency difference:
$$\omega_{0}\equiv\omega_{\alpha}-\omega_{\beta}$$
- Then _summing over all $N$ electrons_ and defining the _electric dipole operator_:
$$\displaylines{\hat{U}_{21}^{\dagger}=i\omega_{0}N(\boldsymbol{k})\sqrt{ n_{\boldsymbol{k},\lambda}+1 }\braket{ \beta|\boldsymbol{e}^{*}_{\lambda}(\boldsymbol{k})\cdot \hat{\boldsymbol{d}} |\alpha  }   \\ \hat{\boldsymbol{d}}=-e\sum_{i=1}^{N}\hat{\boldsymbol{r}}_{i}}$$
- Defining the _complex three-vector_ of matrix elements of $\hat{\boldsymbol{d}}$:
$$\boldsymbol{d}_{\beta\alpha}=\Big(\braket{ \beta|\hat{d}_{x} |\alpha  },\braket{ \beta|\hat{d}_{y} |\alpha  },\braket{ \beta|\hat{d}_{z} |\alpha  } \Big)$$
- The _amplitude squared_ of the matrix element is then:
$$|\hat{U}_{21}^{\dagger}|^{2}=\omega_{0}^{2}N(\boldsymbol{k})^{2}(n_{\boldsymbol{k},\lambda}+1)\Big|\boldsymbol{e}_{\lambda}^{*}(\boldsymbol{k})\cdot \boldsymbol{d}_{\beta\alpha}\Big|^{2}$$
- The _normalisation factor_ is:
$$N(\boldsymbol{k})^{2}=\frac{\hbar}{2\epsilon_{0}\omega(\boldsymbol{k})V}$$
- The _transition rate_, in the _continuum version_:
$$\Gamma(1\to 2)=\frac{\pi\omega_{0}}{\epsilon_{0}V}(n_{\boldsymbol{k},\lambda}+1)\Big|\boldsymbol{e}_{\lambda}^{*}(\boldsymbol{k})\cdot \boldsymbol{d}_{\beta\alpha}\Big|^{2}g(E_{k})$$

## Stimulated and spontaneous emission rate
- The _total emission rate_ is _proportional_ to $(n_{\boldsymbol{k},\lambda}+1)/V$

- The part proportional to $n_{\boldsymbol{k},\lambda}/V$ is the _stimulated emission rate_
	- Proportional to the _photon number density_
- The part proportional to $1/V$ is the _spontaneous emission rate_
	- It is _independent_ of any external EM fields
	- It depends _only on the initial and final states_
![[Stimulated and spontaneous emission.png]]
## Electric dipole approximation
- The transition rate above is the _same_ as would be obtained for an _electric dipole perturbation_:
$$\hat{H}'=-\hat{\boldsymbol{E}}(\boldsymbol{r},t)\cdot \hat{\boldsymbol{d}}$$
- The [[Quantum electrodynamics#Quantised electromagnetic field|electric field as an operator]]:
$$\hat{\boldsymbol{E}}(\boldsymbol{r},t)=\sum_{\boldsymbol{k},\lambda}i\omega(\boldsymbol{k})N(\boldsymbol{k})\Big[\hat{a}_{\boldsymbol{k},\lambda}\exp[i(\boldsymbol{k}\cdot \boldsymbol{r}-\omega t)]e_{\lambda}(\boldsymbol{k})-\hat{a}_{\boldsymbol{k},\lambda}^{\dagger}\exp[-i(\boldsymbol{k}\cdot \boldsymbol{r}-\omega t)]e_{\lambda}^{*}(\boldsymbol{k})\Big]$$
- The approximation of $\exp(i\boldsymbol{k}\cdot \boldsymbol{r})\approx 1$ is the _electric dipole approximation_
- Atomic transitions from an electric dipole interaction are _E1 transitions_

# Spontaneous emission
- Consider the _spontaneous emission_ of a photon into an _infinitesimal solid angle_ around the $\boldsymbol{k}$ direction, in the _polarisation state_ $\boldsymbol{e}_{\lambda}(\boldsymbol{k})$
$$\ket{\alpha}\to \ket{\beta}+\gamma_{\boldsymbol{k},\lambda}  $$
- The photon energy and frequency:
$$E=\hbar\omega_{0}\equiv E_{\alpha}-E_{\beta}\hspace{1.5cm}\omega_{0}=c|\boldsymbol{k}|=\omega_{\alpha}-\omega_{\beta}$$
![[Spontaneous emission geometry.png|300]]

## Calculating total decay rate
- The _density of states_ available to the photon:
$$g(E_{k})=\frac{VE_{k}^{2}}{(2\pi \hbar c)^{3}}d\Omega$$
- Substituting this into the [[#Evaluating the rate|spontaneous emission rate]], the arbitrary _volume cancels_, and one can define a _differential decay rate_:
$$\frac{d\Gamma}{d\Omega}\Bigg|_{\alpha \to\beta}=\frac{\omega_{0}^{3}}{8\pi^{2}\epsilon_{0}\hbar c^{3}}\Big|\boldsymbol{e}_{\lambda}^{*}(\boldsymbol{k})\cdot \boldsymbol{d}_{\beta\alpha}\Big|^{2}$$
- $(d\Gamma/d\Omega)d\Omega$ is the _number of photons_ in polarisation state $\lambda$ emitted _per unit time per atom_ into a solid angle $d\Omega$ in the direction $(\theta,\phi)$

- The complex three-vector scalar product:
$$\boldsymbol{e}_{\lambda}^{*}(\boldsymbol{k})\cdot \boldsymbol{d}_{\beta\alpha}=\boldsymbol{e}_{\lambda}^{*}(\boldsymbol{k})\cdot \braket{ \beta|\hat{\boldsymbol{d}} |\alpha  }\hspace{1.25cm}\hat{\boldsymbol{d}}=-e\sum_{i=1}^{N}\hat{\boldsymbol{r}}_{i} $$
- The _total decay rate_ for $\alpha\to\beta$ is obtained by _integrating over all directions_, and _summing over polarisation states_:
$$\Gamma(\alpha\to\beta)=\sum_{\lambda}\int \frac{d\Gamma}{d\Omega}\Bigg|_{\alpha\to\beta} \, d\Omega $$

- By using _explicit forms_ for the polarisation vectors $\boldsymbol{e}_{\lambda}(\boldsymbol{k})$, one finds that for _any polarisation basis_:
$$\sum_{\lambda}\int \Big|\boldsymbol{e}_{\lambda}^{*}(\boldsymbol{k})\cdot \boldsymbol{d}_{\beta\alpha}\Big|^{2} \, d\Omega =\frac{8\pi}{3}\left| \boldsymbol{d}_{\beta\alpha} \right|^{2} $$
- In terms of [[Quantum electrodynamics#Spherical components|spherical components]]:
$$\left| \boldsymbol{d}_{\beta\alpha} \right|^{2}=\left| \braket{ \beta|\hat{d}_{+1} |\alpha  }  \right|^{2}+\left| \braket{ \beta|\hat{d}_{0} |\alpha  }  \right|^{2}+\left| \braket{ \beta|\hat{d}_{-1} |\alpha  }  \right|^{2}  $$
- The _total spontaneous decay rate_ is then:
$$\Gamma _\text{spon}(\alpha\to\beta)=\frac{\omega_{0}^{3}}{3\pi\epsilon_{0}\hbar c^{3}}\left| \boldsymbol{d}_{\beta\alpha} \right|^{2}$$

## Decay rules from angular momentum
- Characterise states of the $N-$electron atom using [[Atomic and molecular physics#Multi-electron atoms|angular momentum eigenstates]]:
$$\ket{\alpha Jm_{J}}\longrightarrow \ket{\alpha'J'm_{J}'}+\gamma  $$
- The _total decay rate_:
$$\Gamma=\frac{\omega_{0}^{3}}{3\pi\epsilon_{0}\hbar c^{3}}\left( \left| d_{+1} \right|^{2}+|d_{0}|^{2}+|d_{-1}|^{2}  \right)$$
- Here, $d_m$ are the _matrix elements_, computed using the [[Symmetries in quantum mechanics#The Wigner-Eckart Theorem for vector operators|Wigner-Eckart Theorem]]:
$$d_{m}=\braket{ \alpha'J'm_{J}'|\hat{d}_{m} |\alpha Jm_{J}  }=\left\langle  \alpha'J'||\hat{\boldsymbol{d}} ||\alpha J  \right\rangle \Braket{ 1m;Jm_{J} |J'm_{J}'  }   $$
- The Clebsch-Gordan coefficient gives the _selection rules_:
$$\displaylines{\Delta m_{J}\equiv m_{J}'-m_{J}=0,\pm 1 \\ \Delta J=J'-J=\pm 1\hspace{1.25cm}J+J'\geq 1}$$

- For a _given_ $J$ and $J'$, one can calculate _relative decay rates_, as they only _differ in the C-G coefficient_:
$$\Gamma(m_{J}\to m_{J}')=\frac{\omega_{0}^{3}}{3\pi\epsilon_{0}\hbar c^{3}}\left| \left\langle  \alpha'J'||\hat{\boldsymbol{d}} ||\alpha J  \right\rangle \right|^{2}\left| C_{m} \right|^{2} $$
- Example: $J=3\to J'=2$
![[Spontaneous decay 3 to 2.png]]
- The _summed rates_ from _each upper level_ are always _the same_
	- Due to _rotational invariance_
	- A _preferred direction_ would imply _polarisation_
- The lifetime is a _function of the energy level itself_

# Stimulated emission
- The _stimulated emission rate_ is given by the $n_{\boldsymbol{k},\lambda}/V$ component of the equation
- The external EM field is often characterised by _energy density_ $u(\omega)$ instead of number density
	- Example: [[Thermal Radiation]]

- Consider an _isotropic_, and _unpolarised_ EM field, with _field energy_ $U$:
$$dU=u(\omega)V\,d\omega=u(\omega)Vc\,dk$$
- For an _unpolarised_ field, $n_{\boldsymbol{k},\lambda}$ must be _independent_ of the _direction_ of $\boldsymbol{k}$, or $\lambda$:
$$n_{\boldsymbol{k},\lambda}=n_{\boldsymbol{k},\lambda}(|\boldsymbol{k}|)$$
- Accounting for _spin states_, one gets:
$$dU=2n_{\boldsymbol{k},\lambda}g(k)\hbar\omega\,dk=u(\omega)Vc\,dk$$
- Writing out the _density of states_, one then gets:
$$n_{\boldsymbol{k},\lambda}=\frac{\pi^{2}c^{3}}{\hbar\omega^{3}}u(\omega)$$
- The rate for _stimulated emission_ is then related to the [[#Calculating total decay rate|spontaneous decay rate]] by:
$$\Gamma _\text{stim}(1\to2)=\frac{\pi^{2}c^{3}}{\hbar\omega^{3}}u(\omega)\Gamma _\text{spon}(1\to 2)$$

- For an _isolated atom_, with _no polarisation_, the emission rate _cannot depend on direction_, hence the EM field _does not necessarily have to be isotropic_ for the above to be true

- The _photon_ produced by stimulated emission must be in the _same direction as the incoming photon_
	- In an _isotropic field_, photons are emitted _isotropically_
	- In a _beam_ of photons, they are emitted _along the beam_

- In _thermal radiation_, one gets:
$$\frac{\Gamma _\text{stim}(1\to 2)}{\Gamma _\text{spon}(1\to 2)}= \frac{1}{\exp(\hbar\omega/k_{B}T)-1}$$
- At _room temperature_, stimulated emission is _negligible_
# Absorption
- In the case of _absorption_:
$$\omega_{0}=\omega_{\beta}-\omega_{\alpha}>0$$
- One has to consider _matrix element_ $U_{21}$ instead, making the expression:
$$\Gamma(1\to 2)=\frac{\pi\omega_{0}}{\epsilon_{0}V}(n_{\boldsymbol{k},\lambda}+1)\Big|\boldsymbol{e}_{\lambda}(\boldsymbol{k})\cdot \boldsymbol{d}_{\beta\alpha}\Big|^{2}g(E_{k})$$

- Absorption can _only be stimulated_, as the _number of photons_ becomes:
$$n_{\boldsymbol{k},\lambda}+1\longrightarrow n_{\boldsymbol{k},\lambda}$$
- Then identify:
$$n_{\boldsymbol{k},\lambda}+1=\frac{\pi^{2}c^{3}}{\hbar\omega^{3}}u(\omega)$$
- This leads to an _absorption rate equal to stimulated emission rate_, for given $J.J',m_J,m_J'$
$$\Gamma _\text{abs}(m_{J}'\to m_{J})=\Gamma _\text{stim}(m_{J}\to m_{J}')$$
- The _total emission rate_ from a _single_ $m_J$ state is _smaller_ than the _total absorption rate_ from the lower $m_J'$ state

- As there are _different degeneracies_ for each $J$, and the _overall rates must be the same_:
$$(2J+1)\Gamma _\text{stim}(J\to J')=(2J'+1)\Gamma _\text{abs}(J'\to J)$$
![[Emission and absorption rates.png]]
# Einstein coefficients and decay lifetimes
- Let there be two _energy levels_ with _degeneracies_ $g_1,g_2$ and _occupancies_ $N_1,N_2$
$$\begin{align}\Gamma _\text{spon}(2\to 1)&=N_{2}A_{21} \\ \Gamma _\text{stim}(2\to 1)&=N_{2}B_{21}u(\omega)\\ \Gamma _\text{stim}(1\to 2)&=N_{1}B_{12}u(\omega)\end{align}$$
![[Einstein coefficients.png]]
- From the expressions of decay rates, one gets:
$$g_{1}B_{12}=g_{2}B_{21}\hspace{1.5cm}A_{21}=\frac{\hbar\omega^{3}}{\pi^{2}c^{3}}B_{21}$$

## Thermodynamic derivation
- They can also be derived _thermodynamically_
- In _thermodynamic equilibrium_, the total populations remain _constant_:
$$\displaylines{N_{2}[A_{21}+B_{21}u(\omega)]=N_{1}B_{12}u(\omega) \\ \frac{N_{1}}{N_{2}}=\frac{g_{1}}{g_{2}}\exp\left( \frac{\hbar\omega}{k_{B}T} \right)}$$
- Substitute [[Thermal Radiation|Planck radiation law]]:
$$u(\omega)=\frac{\hbar\omega^{3}}{\pi^{2}c^{3}} \frac{1}{\exp(\hbar\omega/k_{B}T)-1}$$
- $A_{21}$ must be _independent of temperature_
- From this, one recovers the relations between the coefficients
## Spontaneous decay lifetimes
- For _spontaneous decay_ $2\to 1$, the _occupancy_ of the upper level _decays exponentially_:
$$\dot{N}_{2}(t)=-A_{21}N_{2}\Longrightarrow N_{2}(t)=N_{2}(0)\exp\left( -\frac{t}{\tau_{2}} \right)$$
- The _mean lifetime_ $\tau_2$ is:
$$\tau_{2}=\frac{1}{A_{21}}$$

- In _general_, a high energy level can _decay into multiple possible lower levels_:
$$\dot{N}_{k}(t)=-[A_{k{1}}+A_{k 2}+\dots]N_{2}$$
- This gives a characteristic lifetime of:
$$\tau_{k}=\frac{1}{\sum_{j}A_{kj}}$$

# Angular distribution of spontaneous decay
- Consider the $(\theta,\phi)$ _distribution_ for different values  of $\Delta m_{J}=0,\pm 1$

## Decay rate for each transition
- Differential decay rate:
$$\frac{d\Gamma}{d\Omega}\Bigg|_{\alpha \to\beta}=\frac{\omega_{0}^{3}}{8\pi^{2}\epsilon_{0}\hbar c^{3}}\Big|\boldsymbol{e}_{\lambda}^{*}(\boldsymbol{k})\cdot \boldsymbol{d}_{\beta\alpha}\Big|^{2}$$
- The dot product can be decomposed into a _sum over spherical components_, which correspond to a _value_ of $\Delta m_{J}$

- Using the _Wigner-Eckart theorem_, the rates for _each_ $\Delta m_{J}$, for some _polarisation_ $\lambda$ is:
$$\displaylines{\frac{d\Gamma_{\lambda}}{d\Omega}\Bigg|_{\Delta m_{J}=m}=A|(\boldsymbol{e}_{\lambda})_{m}|^{2}|C_{m}|^{2} \\ A=\frac{\omega_{0}^{3}}{8\pi^{2}\epsilon_{0}\hbar c^{3}}\left| \braket{ \alpha'J'||\hat{\boldsymbol{d}} ||\alpha J  }  \right|^{2} \hspace{1.5cm}C_{m}=\braket{ Jm_{J};1m | J'm_{J}' } }$$

## Polarisation states
- Consider both _plane polarisation_ and _circular polarisation_

- The _polarisation vectors_ for possible [[Quantum electrodynamics#Polarisation states|states]], with _spherical components_:
$$\displaylines{\boldsymbol{k}=|\boldsymbol{k}|(\sin\theta \cos \phi,\sin\theta \sin \phi,\cos\theta)\\ \boldsymbol{e}=(e_{+1},e_{-1},e_{0}) \\ \begin{align}
\boldsymbol{e}_{1}&=-\frac{1}{\sqrt{ 2 }}\big(\cos\theta \exp(i\phi),-\cos\theta \exp(-i\phi),-\sin\theta\big) \\ \boldsymbol{e}_{2}&=-\frac{i}{\sqrt{ 2 }}\big(\exp(i\phi),\exp(-i\phi),0\big) \\
\boldsymbol{e}_{L}&=-\left( \frac{1}{2}(1-\cos\theta)\exp(i\phi), \frac{1}{2}(1+\cos\theta)\exp(-i\phi),-\frac{1}{\sqrt{ 2 }}\sin\theta \right) \\ \boldsymbol{e}_{R}&=-\left( \frac{1}{2}(1+\cos\theta)\exp(i\phi), \frac{1}{2}(1-\cos\theta)\exp(-i\phi),\frac{1}{\sqrt{ 2 }}\sin\theta \right)\end{align}}$$

## Δm=0
- For a decay with $\Delta m_{J}=0$, the differential decay rate is:
$$\frac{d\Gamma_{\lambda}}{d\Omega}\Bigg|_{\Delta m_{J}=0}=A\left| (\boldsymbol{e}_{\lambda})_{0} \right|^{2}|C_{0}|^{2} $$
- For _plane polarisation states_:
$$\frac{d\Gamma_{1}}{d\Omega}\Bigg|_{\Delta m_{J}=0}=A\left| C_{0} \right|^{2}\sin^{2}\theta \hspace{1.5cm} \frac{d\Gamma_{2}}{s\Omega}\Bigg|_{\Delta m_{J}=0}=0 $$
- The photon is _always emitted in state_ $\boldsymbol{e}_{1}$

- In the _circular polarisation states_:
$$\frac{d\Gamma_{L}}{d\Omega}\Bigg|_{\Delta m_{J}=0}=\frac{d\Gamma_{R}}{d\Omega}\Bigg|_{\Delta m_{J}=0}=\frac{1}{2}A|C_{0}|^{2}\sin^{2}\theta$$
- The emitted photons are a _mix_ of left and right-handed circular polarisation states

- In either basis, summing over _both states_:
$$\frac{d\Gamma}{d\Omega}\Bigg|_{\Delta m_{J}=0}=A|C_{0}|^{2}\sin^{2}\theta$$
- Photons _cannot be emitted along_ the _quantisation axis_
	- The axis is still _arbitrary_ and has no physical meaning
- They are _emitted preferentially_ in the $x-y$ plane $(\theta=\pi/2)$
![[dm=0 angular dependence.png]]

## Δm=±1
- Consider a decay with $\Delta m_{J}=+1$
$$\frac{d\Gamma_{\lambda}}{d\Omega}\Bigg|_{\Delta m_{J}=+1}=A\left| (\boldsymbol{e}_{\lambda})_{+1} \right|^{2}|C_{+1}|^{2} $$

- For the _plane polarisation_ basis:
$$\frac{d\Gamma_{1}}{d\Omega}\Bigg|_{\Delta m_{J}=+1}= \frac{1}{2} A\left| C_{+1} \right|^{2}\cos^{2}\theta \hspace{1.5cm} \frac{d\Gamma_{2}}{s\Omega}\Bigg|_{\Delta m_{J}=+1}= \frac{1}{2}A|C_{+1}|^{2} $$
- For the _circular polarisation_ basis:
$$\frac{d\Gamma_{L}}{d\Omega}\Bigg|_{\Delta m_{J}=+1}= \frac{1}{4} A\left| C_{+1} \right|^{2}(1-\cos\theta)^{2} \hspace{1.5cm} \frac{d\Gamma_{R}}{s\Omega}\Bigg|_{\Delta m_{J}=+1}= \frac{1}{4}A|C_{+1}|^{2}(1+\cos\theta)^{2} $$
- The _sum_ of the polarisation states:
$$\frac{d\Gamma}{d\Omega}\Bigg|_{\Delta m_{J}=+1}= \frac{1}{2}A|C_{+1}|^{2}(1+\cos^{2}\theta)$$

- Similarly, for decays with $\Delta m_{J}=-1$
$$\frac{d\Gamma}{d\Omega}\Bigg|_{\Delta m_{J}=\pm1}= \frac{1}{2}A|C_{\pm1}|^{2}(1+\cos^{2}\theta)$$
![[dm=+-1 angular distribution.png]]

- For both decays, for $\theta=\pi/2$, the photons are in the _plane polarisation state_ $\boldsymbol{e}_{2}$

## Overall distribution
![[Angular distribution summary.png]]

- Overall, the _sum_ of contributions from each $\Delta m_{J}$ are _constant_, corresponding to an _isotropic_ distribution

- An _unpolarised_ sample of atoms will _populate all_ $m_J$ states _equally_, hence _emit photons isotropically_
- There is also an _equal mix of polarisation states_, giving _unpolarised light_
- The system obeys _rotational symmetry_


# Polarisation effects
- Consider introducing a _weak magnetic field_
- This introduces an _anisotropy_, and the $z-$axis has _physical significance_

- There is a _splitting of energy levels_ via the [[Atomic and molecular physics#Zeeman effect|Zeeman effect]]
- In the weak-field limit, each $J$ level is _split_ into $(2J+1)$ energy levels
	- $g_J$ is the [[Angular momentum in quantum mechanics#Combining magnetic moments and the Lande g-factor|Lande g-factor]]
$$(\Delta E)_{B}=g_{J}m_{J}\mu_{B}B$$

## Photons in specific directions
- Suppose some detector _looks into the field_:
![[Emission polarisation z.png|600]]
- This corresponds to $\theta=0$, with the permissible modes:
$$\left\{ \Delta m_{J}=-1 ,\boldsymbol{e}_{L}\right\}\hspace{1.5cm}\left\{ \Delta m_{J}=+1 ,\boldsymbol{e}_{R}\right\} $$
- The $\Delta m_{J}=0$ transition _cannot be observed_
- The photons are _always circularly polarised_

- Suppose some detector _looks along the field_:
![[along the field.png]]
- This corresponds to $\theta=\pi$, with the modes:
$$\left\{ \Delta m_{J}=-1 ,\boldsymbol{e}_{R}\right\}\hspace{1.5cm}\left\{ \Delta m_{J}=+1 ,\boldsymbol{e}_{L}\right\} $$

- This corresponds to the _conservation of angular momentum_
- An atom in the state $\ket{J,m_{J}}$ has the angular momentum:
$$\left\langle  \hat{J}_{z}  \right\rangle=m_{J}\hbar  $$
- The $\Delta m_{J}=0$ transition _violates angular omentum conservation_

- When the detector is _parallel/antiparallel_ to $\boldsymbol{B}$, one _cannot view all transition lines_

- Consider a detector looking _perpendicular_ to the magnetic field (e.g. along the $x-$axis):
![[transition perpendicular field.png]]
- This corresponds to $\theta=\pi/2$:
$$\left\{ \Delta m_{J}=-1 ,\boldsymbol{e}_{2}\right\}\hspace{1.5cm}\left\{ \Delta m_{J}=0,\boldsymbol{e}_{1} \right\} \hspace{1.5cm}\left\{ \Delta m_{J}=+1 ,\boldsymbol{e}_{2}\right\} $$
- Along $\theta=\pi/2$, the _plane polarisation states_ are:
$$\boldsymbol{e}_{1}=(0,0,-1)\hspace{1.5cm}\boldsymbol{e}_{2}=(0,1,0)$$

- In summary, for $\boldsymbol{B}=B\hat{z}$

| Direction of observation | Polarisation for $\Delta m_{J}=\pm 1$ | Polarisation for $\Delta m_{J}=0$ |
| ---- | ---- | ---- |
| $z$ | Circular | Not observed |
| $x$ | Plane $(y)$ | Plane $(z)$ |
| $y$ | Plane $(x)$ | Plane $(z)$ |
- In a _general direction_, the polarisation is _elliptical_

# Optical pumping
- The polarisation characteristics of _decay_ also apply to _absorption_
- This applies to _optical pumping_, where polarised light is used to induce a _population distribution_, which is _different_ from that of _thermal equilibrium_
- An atom is placed in magnetic field $\boldsymbol{B}$, and _plane/circularly_ polarised light of the corresponding _frequency_ is _absorbed_ to promote electrons into _higher energy levels_

- For radiation travelling _along_ the magnetic field $(\theta=0)$:
	- _Left(Right)_ circular polarisation induces $\Delta m=+(-)1$ transitions
![[Optical pump +1.png]]

- Once on the upper energy level, it can still _spontaneously decay_, before being _pumped up again_:
![[Pump up.png]]
- Once it reaches the _highest_ $m_J$, _no more upward transitions are possible_, hence atoms _accumulate_
	- In _thermal equilibrium_, they are _almost equally distributed_

## Using optical pumping to find Zeeman splitting
- Consider optical pumping in $\ce{ ^{87}Rb }$, which has a _nuclear spin_ $I=3/2$
![[Rubidium atomic transitions.png]]

- They initially _accumulate_ in the $\ce{ 2S }_{1/2}m_{F}=+2$ state
- The left-handed polarised beam is _fully transmitted_ across the sample

- Then _irradiate_ the atom with _radio frequency light_ of different $\omega_{RF}$
- When $\hbar\omega_{RF}$ maycjes the _Zeeman splitting_ $(\Delta E)=g_{F}\mu_{B}B$, it _stimulates transmissions to other levels_
- As _all other levels_ are _repopulated_, one sees a _resonant dip_ in the _polarised light transmission_

- This can be used to _find_ $g_{F}$

- _Without_ optical pumping, there is an _equal amount_ of up and down transitions, and _no change in population_