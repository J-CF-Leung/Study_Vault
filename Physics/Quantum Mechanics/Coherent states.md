- Often, the behaviour of quantum systems is _vastly different from classical behaviour_
- Consider the 1D _classical_ harmonic oscillator:
$$V(x)=\frac{1}{2}m\omega^{2}x^{2}$$
- The _classical_ solution gives a _continuum of energies_:
$$E=\frac{1}{2}m\omega^{2}a^{2}$$
- The particle _oscillates between fixed bounds_ $x=\pm a$
$$x(t)=a\sin(\omega t+\phi)\hspace{1.5cm}p(t)=m\omega a\cos(\omega t+\phi)$$

- In the [[Quantum Harmonic Oscillator]], there are _stationary states_ $\ket{n}$, with _quantised energies_
$$E_{n}=\left( n+\frac{1}{2} \right)\hbar\omega$$
- The _expectation values_ are _time-independent_:
$$\langle x \rangle =\langle p \rangle =0$$

- However, one can find _linear combinations_ of states with _classical behaviour_, known as _coherent states_:
$$\langle x \rangle (t)=A\sin(\omega t+\phi)\hspace{1.5cm}\langle p \rangle(t) =m\omega A\cos(\omega t+\phi)$$
- They turn out to be _eingenstates_ of the [[Quantum Harmonic Oscillator#Ladder operators|annihilation operator]] $\hat{a}$

## Deriving the coherent state
$$\hat{a}\ket{\alpha}=\alpha \ket{\alpha}  $$
- As the operator is _not Hermitian_, the eigenstate $\ket{\alpha}$ might be _complex_

- As the eingenstates are _complete_, express the coherent state as:
$$\ket{\alpha}=\sum_{n=0}^{\infty}c_{n}\ket{n}  $$
- To derive the coefficients:
$$\displaylines{c_{n}=\braket{ n | \alpha } =\frac{1}{\alpha}\braket{ n|\hat{a} | \alpha } \\ \bra{n}\hat{a}=\left( \hat{a}^{\dagger}\ket{n}  \right)^{\dagger}=\ket{n+1}\sqrt{ n+1 } \\    }$$
- One then obtains a _recursion relation_ between the coefficients:
$$\sqrt{ n+1 }c_{n+1}=\alpha c_{n} $$
- Fixing $c_{0}$, one gets:
$$c_{n}=\frac{\alpha^{n}}{\sqrt{ n! }}c_{0}=\frac{\alpha^{n}}{\sqrt{ n! }}\braket{ 0 |\alpha } $$

- The normalisation factor $\braket{ 0 | \alpha }$ is determined by:
$$1=\braket{ \alpha | \alpha } =\sum_{n=0}^{n}\frac{|\alpha|^{2n}}{n!}\left| \braket{ 0 | \alpha }  \right| ^{2}=\exp(|\alpha|^{2})\left| \braket{ 0 | \alpha }  \right| ^{2}\implies \braket{ 0 | \alpha } =\exp\left( -\frac{|\alpha|^{2}}{2} \right) $$

- One then gets a _spectrum of coherent states_, each characterised by _complex number_ $\alpha$
$$\ket{\alpha}=\exp\left( -\frac{|\alpha|^{2}}{2} \right)\sum_{n=0}^{n}\frac{\alpha^{n}}{\sqrt{ n! }}\ket{n}  $$
- It can also be written as:
$$\ket{\alpha}=\exp\left( -\frac{|\alpha|^{2}}{2} \right)\exp\left( \alpha \hat{a}^{\dagger} \right)\ket{0}  $$

## Properties of the coherent state
- The _probability_ of having $n$ quanta in the state $\ket{\alpha}$ is:
$$P_{\alpha}(n)=|c_{n}|^{2}=\frac{\left| \alpha \right|^{2n}}{n!}\exp(-|\alpha|^{2}) $$
- This is a _Poisson distribution_:
$$P_{\alpha}(n)=\frac{\langle n \rangle \exp(-\langle n \rangle )}{n!}\hspace{1.5cm}\langle n \rangle=|\alpha|^{2}  $$
- One can also get the latter result using the _number operator_:
$$\braket{ \alpha|\hat{n} |\alpha  }=\braket{ \alpha|\hat{a}^{\dagger}\hat{a} |\alpha  }=|\alpha|^{2}  $$

- It can also be shown as a [[Principles of quantum mechanics#Uncertainty principles|minimal uncertainty state]]:
$$(\Delta x)(\Delta p)=\frac{\hbar}{2}$$
- It _evolves_ as:
$$\ket{\alpha (t)}=\exp\left( -\frac{i\omega t}{2} \right)\Ket{\exp(-i\omega t)\alpha(0)}  $$
- The _expectation values_ are solutions of the _classical equations of motion_:
$$\langle x \rangle(t) =A\sin(\omega t+\phi)\hspace{1.5cm}\langle p \rangle (t)=m\omega A\cos(\omega t+\phi)$$
- The _width_ of the coherent state also remains _constant_

- TP2 problem 1.5 (coherent state stays coherent)

## Coherent states of the EM field
- The electromagnetic field can be [[Quantum electrodynamics|quantised]]
- Each [[Quantum electrodynamics#Polarisation states|mode]] $(\boldsymbol{k},\lambda)$ of the EM field are their own _quantum harmonic oscillator_

- The _coherent state_ of the EM field:
$$\hat{a}_{\boldsymbol{k},\lambda}\ket{\alpha_{\boldsymbol{k},\lambda}}=\alpha_{\boldsymbol{k},\lambda}\ket{\alpha_{\boldsymbol{k},\lambda}}  $$
- As all modes are _independent_, one can generalise the above relation:
$$\hat{a}_{\boldsymbol{k}',\lambda'}\ket{\alpha_{\boldsymbol{k},\lambda}}=\alpha_{\boldsymbol{k},\lambda}\ket{\alpha_{\boldsymbol{k},\lambda}}\delta_{\boldsymbol{k},\boldsymbol{k}'}\delta_{\lambda,\lambda'}  $$
- The _expectation values_ of the creation and annihilation operators:
$$\begin{align}\bra{\alpha_{\boldsymbol{k},\lambda}} \hat{a}_{\boldsymbol{k}',\lambda'}\ket{\alpha_{\boldsymbol{k},\lambda}}&=\alpha_{\boldsymbol{k},\lambda}\delta_{\boldsymbol{k},\boldsymbol{k}'}\delta_{\lambda,\lambda'} \\ \bra{\alpha_{\boldsymbol{k},\lambda}} \hat{a}^{\dagger}_{\boldsymbol{k}',\lambda'}\ket{\alpha_{\boldsymbol{k},\lambda}}&=\alpha_{\boldsymbol{k},\lambda}^{*}\delta_{\boldsymbol{k},\boldsymbol{k}'}\delta_{\lambda,\lambda'}  \end{align}$$
- The _average number_ of quanta:
$$\langle n_{\boldsymbol{k},\lambda} \rangle=\braket{ \alpha_{\boldsymbol{k},\lambda}|\hat{a}_{\boldsymbol{k},\lambda}^{\dagger}\hat{a}_{\boldsymbol{k},\lambda} | \alpha_{\boldsymbol{k},\lambda} } =|\alpha_{\boldsymbol{k},\lambda}|^{2} $$

### Electric field
- Write the _complex eigenvalue_ as:
$$\alpha_{\boldsymbol{k},\lambda}=|\alpha_{\boldsymbol{k},\lambda}|\exp(i\theta)$$
- The _electric field operator_:
$$\displaylines{\hat{\boldsymbol{E}}(\boldsymbol{r},t)=\sum_{\boldsymbol{k},\lambda}i\omega(\boldsymbol{k})N(\boldsymbol{k})\Big[\hat{a}_{\boldsymbol{k},\lambda}\exp[i(\boldsymbol{k}\cdot \boldsymbol{r}-\omega t)]e_{\lambda}(\boldsymbol{k})-\hat{a}_{\boldsymbol{k},\lambda}^{\dagger}\exp[-i(\boldsymbol{k}\cdot \boldsymbol{r}-\omega t)]e_{\lambda}^{*}(\boldsymbol{k})\Big] \\ N(\boldsymbol{k})\equiv \sqrt{ \frac{\hbar}{2\epsilon_{0}\omega(\boldsymbol{k})V} }}$$
- In a coherent state, for a _plane polarisation_ where $\boldsymbol{e}_{\lambda}(\boldsymbol{k})$ is _real_:
$$\left\langle  \hat{\boldsymbol{E}}  \right\rangle= \Braket{ \alpha_{\boldsymbol{k},\lambda}|\hat{\boldsymbol{E}} |\alpha_{\boldsymbol{k},\lambda}  } =-\sqrt{ \frac{2\left<n_{\boldsymbol{k},\lambda}\right>\hbar\omega}{\epsilon_{0}V} }\sin(\boldsymbol{k}\cdot \boldsymbol{r}-\omega t+\theta)\boldsymbol{e}_{\lambda}(\boldsymbol{k})$$
- This in contrast to the _Fock states_ $\ket{n_{\boldsymbol{k},\lambda}}$ where the [[Quantum electrodynamics#Electric field|expected electric field]] is _zero_

- An electric field in a _coherent state_ corresponds to a _classical harmonic wave_

- The _fluctuation_ of the electric field:
$$\left\langle  \hat{\boldsymbol{E}}^{2}  \right\rangle= \Braket{ \alpha_{\boldsymbol{k},\lambda}|\hat{\boldsymbol{E}}^{2} |\alpha_{\boldsymbol{k},\lambda}  } =- \frac{2\left<n_{\boldsymbol{k},\lambda}\right>\hbar\omega(\boldsymbol{k})}{\epsilon_{0}V} \sin^{2}(\boldsymbol{k}\cdot \boldsymbol{r}-\omega t+\theta)+\frac{\hbar\omega(\boldsymbol{k})}{2\epsilon_{0}V}$$
- This gives the _fluctuation_, which is _constant_
$$(\Delta\boldsymbol{E}^{2})=\frac{\hbar\omega(\boldsymbol{k})}{2\epsilon_{0}V}$$
- Fluctuations in field strength for a field state is [[Quantum electrodynamics#Electric field|equivalent to that of a vacuum]]

- Hence, the electric field coherent state shares similiar [[#Interpretation of the coherent state|properties]] as the simplest quantum harmonic oscillator
