
- For _electromagnetic_ phenomena in quantum mechanics, assume that the _quantum Hamiltonian_ has the _same form_ as the _classical Hamiltonian_ found in [[Electrodynamics and Optics|Classical Electrodynamics]]
	- From one of the [[Principles of quantum mechanics#The fundamental postulates|postulates]]
- Then, the effects of _spin_ are added _by hand_ based on experiment

- In _classical electrodynamics_, the equation of motion is
$$m\ddot{\bm{r}}=q(\bm{E}+\bm{v}\times\bm{B})$$
- The _fields_ are given by:
$$\bm{E}=-\nabla\phi-\pd{\bm{A}}{t}\hspace{1.5cm}\bm{B}=\nabla\times\bm{A}$$
- Get the [[Analytical classical mechanics#Electromagnetism|electromagnetic Hamiltonian]]
$$\Ham=\frac{1}{2m}\left|\bm{p}-q\bm{A}(\bm{r},t)\right|^2+q\phi(\bm{r},t)$$
- $\bm{p}$ is the _canonical momentum_
	- $\bm{p}=m\dot{\bm{x}}+q\bm{A}=\bm{p}_m+q\bm{A}$, where $\bm{p}_m=m\dot{\bm{x}}$ is the _mechanical momentum_

- This suggests the _Hamiltonian operator_:
$$\hat\Ham=\frac{1}{2m}\left|\hat{\bm{p}}-q\bm{A}\right|^2+q\phi$$
- In the _position basis_, the _time-dependent Schrödinger equation_ is:
$$i\hbar\pd{\psi}{t}=\frac{1}{2m}\left|-i\hbar\nabla-q\bm{A}(\bm{r},t)\right|^2\psi+q\phi(\bm{r},t)\psi$$

- For a _free particle_, the _eigenstates_ are:
$$\psi(\bm{r},t)=\exp\left[i\left(\bm{k}\cdot\bm{r}+\frac{q}{\hbar}\bm{A}\cdot\bm{r}\right)\right]$$
# Gauge invariance of the Schrödinger equation
- The electric and magnetic fields are known to be _gauge-invariant_:
$$\bm{A}\to\bm{A}'=\bm{A}+\nabla f\hspace{1.5cm}\phi\to\phi'=\phi-\pd{f}{t}$$
- Here, $f(\bm{r},t)$ is any _arbitrary function_, and the above always leaves $\bm{E}$ and $\bm{B}$ _unchanged_

- However, the above _changes the Schrödinger equation_ with _extra terms_
- The only option to recover gauge invariance is to _change $\psi$ as well_:
$$\displaylines{\bm{A}\to\bm{A}'\hspace{1cm}\phi\to\phi'\\\psi(\bm{r},t)\to\psi'(\bm{r},t)=\psi(\bm{r},t)\exp[i\Lambda(\bm{r},t)]}$$
- The phase factor makes sure the _probability density_ is unchanged, hence leaving the physics invariant

- One can prove that with the transformation:
$$\displaylines{\bm{A}\to\bm{A}'=\bm{A}+\nabla f\hspace{1cm}\phi\to\phi'=\phi-\pd{f}{t}\hspace{1cm}\psi\to\psi'=\psi\exp\left[i\frac{q}{\hbar}f\right] \\ i\hbar\pd{\psi'}{t}=\frac{1}{2m}\left|-i\hbar\nabla-q\bm{A}(\bm{r},t)\right|^2\psi'+q\phi(\bm{r},t)\psi'}$$

## The case of zero magnetic field
- For $\bm{B}=0$, the potential $\bm{A}$ can take the form of _the gradient of any function_:
$$\bm{A}=\nabla\chi$$
- Given two points $\bm{r}$ and $\bm{r}_0$:
$$\chi(\bm{r})-\chi(\bm{r}_0)=\int_{\bm{r}_0}^{\bm{r}}\bm{A}(\bm{s})\cdot d\bm{s}$$
- Choosing $f=-\chi$, one can have a _gauge_ where $\bm{A}=0$
- This works as long as the integration path is in a _simply-connected region_

- Denote wave functions such that $\psi_\chi$ in the _gauge_ for $\bm{A}=\nabla\chi$, and $\psi_0$ in the gauge for $\bm{A}=0$:
$$\psi_0(\bm{r})=\psi_\chi(\bm{r})\exp\left[-i\frac{q}{\hbar}\chi\right]$$
- Absorbing a _constant phase factor_, one can rewrite the above:
$$\psi_\chi(\bm{r})=\psi_0(\bm{r})\exp\left[i\frac{q}{\hbar}\int_{\bm{r}_0}^\bm{r}\bm{A}(\bm{s})\cdot d\bm{s}\right]$$
- One can then _solve for_ $\psi_0(\bm{r})$ in the _gauge_ $\bm{A}=0$ to get $\psi_\chi$
# The Aharanov-Bohm Effect
- In _classical physics_, it is _only the fields_ which have physical significance
- In _quantum mechanics_, the potential $\bm{A}$ has significance

- Suppose there is some _double-slit setup_:
![[Aharonov-Bohm 1.png]]
- The observed _fringe pattern_ will be a result of _interference_:
$$I\propto|\psi_D|^2=|\psi_A+\psi_B|^2$$
- For the gauge where $\bm{A}=0$, $\psi_{D,0}=\psi_{A,0}+\psi_{B,0}$
- For the gauge where $\bm{A}=\nabla\chi$:
$$\psi_{D,\chi}=\psi_{A,0}\exp\left[i\frac{q}{\hbar}\int_A\bm{A}(\bm{s})\cdot d\bm{s}\right]+ \psi_{B,0}\exp\left[i\frac{q}{\hbar}\int_B\bm{A}(\bm{s})\cdot d\bm{s}\right]$$
- When there is _no field anywhere_:
$$\displaylines{\oint\bm{A}\cdot d\bm{s}=\iint_S\bm{B}\cdot d\bm{S}=0\Longrightarrow \int_A\bm{A}(\bm{s})\cdot d\bm{s}=\int_B\bm{A}(\bm{s})\cdot d\bm{s} \\ I\propto |\psi_{A,\chi}+\psi_{B,\chi}|^2=|\psi_{A,0}+\psi_{B,0}|^2}$$

- Then place a _solenoid_ with flux $\Phi$ behind the slits:
![[Aharonov-Bohm 2.png]]
- With a _shielded solenoid_, the flux is _contained_, and $\bm{B}=0$ _along the paths of the electrons_
- However, $\bm{A}$ _cannot be zero along both trajectories_:
$$\oint\bm{A}\cdot d\bm{s}=\iint_S\bm{B}\cdot d\bm{S}=\Phi$$
- In _cylindrical coordinates_ with origin at the centre of the solenoid:
$$\bm{A}=\frac{\Phi}{2\pi\rho}\hat{\phi}=\nabla\left(\frac{\Phi\phi}{2\pi}\right)$$
- As $\chi$ is _multiple-valued_, the entire region is now _multiply-connected_

- As each _path_ is still in a _simply-connected region_:
$$\psi_{D,\chi}=\psi_{A,0}\exp\left[i\frac{q}{\hbar}\int_A\bm{A}(\bm{s})\cdot d\bm{s}\right]+ \psi_{B,0}\exp\left[i\frac{q}{\hbar}\int_B\bm{A}(\bm{s})\cdot d\bm{s}\right]$$
- As $A-B$ is a _loop_ around the solenoid:
$$|\psi_{D,\chi}|^2=\left|\psi_{A,0}\exp\left[i\frac{q\Phi}{\hbar}\right]+\psi_{B,0}\right|^2$$
- This effect on the interference pattern is _detectable_
- Physical reasoning: the potential affects the _phase_ of each beam
- The total _phase difference_ $\delta$:
$$|\delta|=\frac{e\Phi}{\hbar}=2\pi\frac{\Phi}{\Phi_0}\hspace{1.5cm}\Phi_0\equiv\frac{h}{e}\approx 4.1\times 10^{-15}\,\text{T m}^2$$
- $\Phi_0$ is the _flux quantum_

- This proves that there can still be _electromagnetic effects_ in regions where the _field is zero_
- This effect is still _gauge invariant_ as it only depends on the _total enclosed flux_

# Landau levels
- _Classically_, a charged particle goes into _cyclotron motion_ when in a _magnetic field_ $\bm{B}$:
$$E=\frac{1}{2}mr^2\omega_c^2\hspace{1.5cm}\omega_c=\frac{q|\bm{B}|}{m}$$
- In the _quantum_ case, one finds that orbital energies can be _quantised_

- With _no electric potential_, the Hamiltonian is:
$$\hat\Ham=\frac{1}{2m}\left|\hat{\bm{p}}-q\bm{A}\right|^2=\frac{1}{2m}\hat{\bm{\Pi}}^2$$
- The operator $\hat{\bm{\Pi}}$ is defined as:
$$\hat{\bm{\Pi}}=\hat{\bm{p}}-q\bm{A}$$
- It follows the _commutation relation_:
$$[\hat{\Pi}_i,\hat{\Pi}_j]=iq\hbar\epsilon_{ijk}B_k$$
- Introduce the _non-Hermitian_ operators:
$$\displaylines{\hat{a}_\pm=\sqrt{\frac{1}{2q\hbar B}}\left(\hat{\Pi}_x\pm i\hat{\Pi}_y\right)\\ [\hat{a}_+,\hat{a}_-]=-\frac{i}{q\hbar B}[\hat{\Pi}_x,\hat{\Pi}_y]=\frac{B_z}{B}}$$
- One finds that the Hamiltonian can be _rewritten_ as:
$$\hat\Ham=\hbar\omega_c\left(\hat{a}_+\hat{a}_-+\frac{1}{2}\right)+\frac{1}{2m}\hat{\Pi}_z^2\hspace{2cm}\omega_c=\frac{qB}{m}$$
- The _first term_ corresponds to the [[Quantum Harmonic Oscillator]], with the energy levels:
$$E_\nu=\hbar\omega_c\left(\nu_L+\frac{1}{2}\right)$$
- Therefore, the terms in the Hamiltonian _transverse to the magnetic field_ give rise to the quantised _Landau levels_:
$$\Delta E=\hbar\omega_c$$
- For a magnetic field of $1\text{T}$, this gives $\Delta E\approx 1.2\times 10^{-4}\,\text{eV}$
	- This is _much smaller_ than $kT$ at _room temperature_
	- At $1.3\,\text{K}$, $kT\sim \Delta E$

## Choosing the Landau gauge
- Choose a _Coulomb gauge_ such that:
$$\bm{A}=(-By,0,0)$$
- The Hamiltonian then becomes:
$$\hat{\Ham}=\frac{1}{2m_e}\left[(\hat p_x-eBy)^2+\hat p_y^2+\hat p_z^2\right]$$
- The Schrödinger equation now admits _separated variable solutions_ of the form (as it _commutes_ with $\hat{p}_x$ and $\hat{p}_z$)
$$\displaylines{\psi(\bm{r})=\exp[ik_xx+ik_zz]\chi(y)\hspace{1.5cm}\hat{\Ham}_\chi\chi(y)=E\chi(y)\\ \hat\Ham_\chi=\frac{1}{2m}\left[(\hbar k_x-eBy)^2+\hat{p}_y^2+\hbar^2k_z^2\right]}$$

- The Hamiltonian then has the form of the _harmonic oscillator_, where $\omega=\omega_c$ and the _central position_ is $y=y_0$:
$$\displaylines{\hat\Ham_\chi=\frac{\hat{p}_y^2}{2m_e}+\frac{1}{2}m\omega_c^2(y-y_0)^2+\frac{\hbar^2k_z^2}{2m_e} \\ y_0=\frac{\hbar k_x}{eB}}$$
- This gives the _total energy_:
$$E_{\nu,k_x}=\left(\nu_L+\frac{1}{2}\right)\hbar\omega_c+\frac{\hbar^2k_z^2}{2m_e}$$
- In _2-dimensional systems_, one can _ignore_ the contribution of $k_z$
	- Example: _boundaries_ between materials

## 2D Electron gas
- Consider a _layer_ of electrons confined to $z=0$ in the region:
$$-\frac{L_x}{2}<x<\frac{L_x}{2}\hspace{1.5cm} -\frac{L_y}{2}<y<\frac{L_y}{2}$$
- Consider the case where there is _no magnetic field_
- For a 2D [[Free Electron Model|free electron gas]] (accounting for _degeneracy due to spin_), the _density of states in energy_ is _constant_:
$$g(E)=\frac{1}{A}\frac{dN}{dE}=\frac{m_e}{\pi\hbar^2}$$
- Then, for a system of $N$ electrons, states are occupied up to the _Fermi level_:
$$\frac{N}{A}=g(E)E_F$$

- Once the _magnetic field_ $B_z$ is applied, the _Landau levels_ appear
- The eigenstates then have the form:
$$\psi(\bm{r})=\exp(ik_xx)\chi(y)$$
- Assuming that the _extent_ of $\chi$ is much _smaller_ than $L_y$:
$$|y_0|<\frac{L_y}{2}\Longrightarrow |k_x|<\frac{eBL_y}{2\hbar}$$
- Hence the _number of available states per Landau level_ is:
$$N_L=\frac{2|k_{x,\text{max}}|}{\pi/L_x}=\frac{2eBh}{h}=\frac{2\Phi}{\Phi_0}$$
- where $\Phi_0$ is the [[#The Aharanov-Bohm Effect|flux quantum]]
- Hence, the _number of states per unit area per level_ is $n=2B/\Phi_0$
- Each Landau level is _highly degenerate_

- At _zero field_, one can check that the _number of electrons per unit area in an energy interval_ of $\hbar\omega_c$ is:
$$g(E)\hbar\omega_c=\frac{2B}{\Phi_0}$$
- Therefore, the effect of switching on a field is to transform a _continuum of states_ into a set of _delta functions_:
![[landau levels.png]]

- One can find the _occupied fraction_ of the _highest Landau level_ as:
$$f_L=\frac{E_F}{\hbar\omega_c}-\text{int}\left[\frac{E_F}{\hbar\omega_c}\right]$$
- Therefore, as $B$ increases, $f_L$ is _periodic_ with a period of:
$$\Delta\left(\frac{E_F}{\hbar\omega_c}\right)=1\Longrightarrow\Delta\left(\frac{1}{B}\right)=\frac{he}{m_eE_F}$$
- Hence, many _physical properties_ vary periodically as $1/B$
- This is responsible for the [[Quantum Hall Effect]]


# Spin and the magnetic moment operator
- _Classically_, one can define an _orbital magnetic moment_:
$$\bm{\mu}_L=\frac{q}{2m}\bm{L}=\gamma_L\bm{L}$$
- $\gamma_L$ is known as the _gyromagnetic ratio_
	- Derivation: let there be a _charged particle_ in a circular orbit, then $\mu=IA$

- Similarly, one can define an _orbital magnetic moment operator_, in terms of the [[Angular momentum in quantum mechanics#Orbital angular momentum|orbital angular momentum]]
$$\hat{\bm{\mu}}_L=\gamma_L\hat{\bm{L}}$$
- One can also define an _intrinsic magnetic moment_, proportional to the [[Angular momentum in quantum mechanics#Spin angular momentum|spin]]:
$$\hat{\bm{\mu}}_S=\gamma_S\hat{\bm{S}}$$
- The _Dirac equation_ for spin-half particles predicts that the intrinsic magnetic moment is:
$$\hat{\bm\mu}_S=\gamma_S\hat{\bm{S}}\equiv\frac{q}{m}\hat{\bm{S}}$$
- The gyromagnetic ratio is _different_ for orbital and spin angular momentum
	- There is an additional _factor of two_

- For _electrons_:
$$(\hat{\bm\mu}_S)_e=-\frac{e}{m_e}\hat{\bm{S}}=-2\frac{\mu_B}{\hbar}\hat{\bm{S}}$$
- $\mu_B$ is the _Bohr magneton_:
$$\mu_B\equiv\frac{e\hbar}{2m_e}$$

- _Experimental measurements_ have led to _adjustments_ to the factor for _electrons_
- QED reason: the electron is _not exactly pointlike_, but is _constantly absorbing/re-emitting virtual photons_
- Introduce the $g-$factor:
$$\displaylines{g_e\approx2.0023\\(\hat{\bm\mu}_S)_e=-\frac{g_e}{2}\frac{e}{m_e}\hat{\bm{S}}=-g_e\frac{\mu_B}{\hbar}\hat{\bm{S}}\hspace{1.5cm} (\gamma_S)_e=-g_e\frac{\mu_B}{\hbar}}$$

## Scalar magnetic moment
- One can define the _scalar magnetic moment_ of a particle $\mu$:
$$\mu\equiv\braket{\uparrow|\hat{\mu}_z|\uparrow}=\gamma_S\braket{\uparrow|\hat{S}_z|\uparrow}=\gamma_S\frac{\hbar}{2}$$
- Therefore, for the _electron_:
$$\mu=-g_e\frac{\mu_B}{2}\approx-\mu_B$$

# Interaction with a magnetic field
- The term of the Hamiltonian describing _interaction of spin with an external field_:
$$\hat{H}=-\hat{\bm{\mu}}\cdot\bm{B}$$
- Expanding out the $\hat{\bm{\mu}}$ operator:
$$\displaylines{\hat{H}_B=-(\gamma_L\hat{\bm{L}}+\gamma_S\hat{\bm{S}})\cdot\bm{B}=-\frac{e}{2m_e}(\hat{\bm{L}}+g_e\hat{\bm{S}})\cdot\bm{B} \\ \hat{H}_B=-\frac{\mu_B}{\hbar}(\hat{\bm{L}}+g_e\hat{\bm{S}})\cdot\bm{B}}$$

## Spin precession
- Consider a particle of spin $\bm{S}$ in a _magnetic field_ $\bm{B}$
- The _time-evolution_ of the expectation value of $\bm{S}$, using [[Principles of quantum mechanics#Ehrenfest's Theorem|Ehrenfest's Theorem]]:
$$\frac{d}{dt}\mean{\hat{\bm{S}}}=\frac{i}{\hbar}\mean{[\hat{H},\hat{\bm{S}}]}$$
- Most components of $\hat{H}$ will _commute_ with $\hat{\bm{S}}$, _except_ the spin interaction:
$$[\bm{B}\cdot\hat{\bm{S}},\hat{S}_i]=\bm{B}\cdot[\hat{\bm{S}},\hat{S}_i]=i\hbar\epsilon_{ijk}\hat{S}_jB_k=i\hbar\left(\hat{\bm{S}}\times\bm{B}\right)_i$$
- Therefore, the _expectation value_ of spin satisfies:
$$\frac{d}{dt}\mean{\hat{\bm{S}}}=\gamma_S\mean{\hat{\bm{S}}}\times\bm{B}=\mean{\hat{\bm{\mu}}}\times\bm{B}$$
- This resembles the [[Electromagnetism#Magnetic dipoles|precession of a magnetic dipole]] in classical mechanics

- This corresponds to _precession_ of the spin expectation values _around_ $\bm{B}$:
![[Spin precession.png]]
- This is at the _Larmor frequency_ $\omega_S$:
$$\omega_S=\gamma_SB$$
- For $\bm{B}=(0,0,B)$, the spin expectation value behaves as:
$$\mean{\hat{S}_x}=A\cos(\omega t+\phi)\hspace{1.5cm}\mean{\hat{S}_y}=-A\sin(\omega t+\phi)\hspace{1.5cm}\mean{\hat{S}_z}=\text{const.}$$

## Precession of the spin-1/2 particle
- For a _spin-1/2 particle_, the _Larmor frequency_ is:
$$\omega_S=\gamma_S B=g_e\frac{e}{2m_e}B=\frac{g_e}{2}\omega_c$$
- Here, $\omega_c$ is the _cyclotron frequency_, or the frequency of the _particle's circular motion_
- The _difference in frequencies_ is:
$$\omega_S-\omega_c=\frac{g_e-2}{2}\omega_c$$
## Energy eigenstates
- Orienting the _magnetic field_ along the $z-$axis:
$$\bm{B}=(0,0,B)\hspace{2cm}\hat{H}=-\mu_SB\hat{S}_z$$
- From this, the eigenstates of $\hat{S}_z$ are _also energy eigenstates_:
$$\displaylines{\hat{S}_z\ket{sm_s}=m_s\hbar\ket{sm_s} \\ \hat{H}\ket{sm_s}=-\gamma_Sm_sB\hbar\ket{sm_s}\Longrightarrow E_s=-\gamma_sm_sB\hbar=-m_s\hbar\omega_s}$$
- Here, $\omega_s$ is the _Larmor frequency_
- Therefore, in $B$, for spin $s$, there are $2s+1$ _discrete energy levels_

## Wave-function evolution
- For a particle _in a spin eigenstate_, $\ket{\psi(t=0)}=\ket{sm_s}$, the spin state evolves as:
$$\ket{\psi(t)}=\exp(im_s\omega_st)\ket{sm_s}$$
- The _expectation value_ of spin is then:
$$\mean{\hat{S}_z}(t)=\braket{\psi(t)|\hat{S}_z|\psi(t)}=m_s\hbar$$
- With the ladder operators, one also finds that:
$$\mean{\hat{S}_+}=\mean{\hat{S}_-}=\mean{\hat{S}_x}=\mean{\hat{S}_y}=0$$
- From this, one finds that from the _expectation value of spin_, there is _no "visible" precession_:
$$\mean{\hat{\bm{S}}}=\Braket{\psi(t)|\hat{\bm{S}}|\psi(t)}=(0,0,m_s\hbar)$$

- For an _arbitrary spin state_:
$$\Ket{\psi(t=0)}=\sum_{m_s}c_{m_s}\ket{sm_s}$$
- The state then evolves with time as:
$$\ket{\psi(t)}=\sum_{m_s}c_{m_s}\exp(im_s\omega_st)\ket{sm_s}$$
- The expectation values are then:
$$\mean{\hat{\bm{S}}}=\Braket{\psi(t)|\hat{\bm{S}}|\psi(t)}=(A_{xy}\cos(\omega_st), B_{xy}\sin(\omega_st),m_s\hbar)$$
- This matches _predictions from Ehrenfest's Theorem_

## Magnetic moment of nuclei
- The _proton_ has a charge, while the _neutron_ is _neutral_, hence one might expect an _analogy_ with the electron, where the proton has a moment while the neutron doesn't
- However, _both protons and neutrons have non-zero magnetic moments_
- Introduce the _nuclear magneton_ $\mu_N$:
$$\mu_N\equiv\frac{e\hbar}{2m_p}$$
- Then define proton and neutron _g-factors_:
$$\displaylines{\hat{\bm{\mu}}_p=g_p\frac{\mu_N}{\hbar}\hat{\bm{S}}_p \hspace{1.5cm} \mu_p=g_p\frac{\mu_N}{2} \\ \hat{\bm{\mu}}_n=g_n\frac{\mu_N}{\hbar}\hat{\bm{S}}_n \hspace{1.5cm} \mu_n=g_n\frac{\mu_N}{2}}$$
- Experimental evidence shows:
$$\displaylines{g_p\approx+5.586 \\ g_n\approx-3.826}$$
- This is evidence that these particles have _internal structure_ (quarks)

- _Atomic nuclei_ can possess _any possible value of spin_
- One then needs to _generalise_ the definition of scalar magnetic moment, to instead use the _maximal value of $m_s$_:
$$\mu\equiv\Braket{S,S|\left(\hat{\mu}_s\right)_z|S,S}$$
- Using this definition:
$$\mu=\gamma_SS\hbar=g_S\mu_NS$$
- The _spin precession frequency_ for the nuclei is then:
$$\omega_s=\gamma_SB=\frac{\mu B}{S\hbar}=\frac{g_S\mu_NB}{\hbar}$$
- The spin of the nucleus is typically denoted $\hat{\bm{I}}$
- One may also use a different _convention_ for nuclear spin:
$$\hat{\bm{\mu}}_I=-g_I\frac{\mu_B}{\hbar}\hat{\bm{I}}$$
- The Hamiltonian is then:
$$\hat{H}_B=-\hat{\bm{\mu}}_I\cdot\bm{B}$$
- The _total magnetic contribution_ to the Hamiltonian is then:
$$\hat{H}_B=\frac{\mu_B}{\hbar}(\hat{\bm{L}}+g_e\hat{\bm{S}}+g_I\hat{\bm{I}})\cdot\bm{B}$$

# Stern-Gerlach experiment
- _Classically_, with a magnetic dipole moment $\bm{\mu}$ in an _external magnetic field_ $\bm{B}$, it is subject to a _torque_:
$$\bm{G}=\bm{\mu}\times\bm{B}$$
- If the field is _non-uniform_, then it is subject to a _force_:
$$\bm{F}=\nabla(\bm{\mu}\cdot\bm{B})$$
- For a sample of _identical, randomly oriented dipoles_, there is a _continuum of possible trajectories_

- In the _quantum_ case, there is a _finite number_ of _distinct spatial trajectories_
- Consider a beam of _neutral_ particles in a _slowly varying magnetic field_:
$$\bm{B}(\bm{r})=\bm{B}_0+\bm{B}_1(\bm{r}) \hspace{1.5cm}|\bm{B}_1(\bm{r})|\ll|\bm{B}_0|$$
- Orient $\bm{B}_0$ along the $z-$axis: $\bm{B}_0=(0,0,B_0)$
- Letting the particles have _magnetic dipole moment_ $\hat{\bm{\mu}}_S=\gamma_S\hat{\bm{S}}$:
$$\hat{H}=\frac{\hat{\bm{p}}^2}{2m}-\hat{\bm{\mu}}_S\cdot\bm{B}=\frac{\hat{\bm{p}}^2}{2m}-\gamma_S\left(\hat{S}_zB_0-\hat{\bm{S}}\cdot\bm{B}_1(\bm{r})\right)$$
- Then use _Ehrenfest's theorem_:
$$\frac{d}{dt}\mean{\hat{\bm{r}}}=\frac{i}{\hbar}\mean{[\hat{H},\hat{\bm{r}}]} \hspace{1.5cm} \frac{d}{dt}\mean{\hat{\bm{p}}}=\frac{i}{\hbar}\mean{[\hat{H},\hat{\bm{p}}]}$$
- As $\hat{\bm{S}}$ commutes with $\hat{\bm{r}}$ and $\hat{\bm{p}}$, and calculating the remaining commutator:
$$\frac{d}{dt}\mean{\hat{\bm{r}}}=\frac{1}{m}\mean{\hat{\bm{p}}}$$
- By using the [[Principles of quantum mechanics#Useful commutation relations|commutator relation]] $[f(\bm{r}),\hat{\bm{p}}]=i\hbar\nabla f$:
$$\frac{d}{dt}\mean{\hat{\bm{p}}}=\gamma_S\sum_{i}\mean{\hat{S}_i}\mean{\nabla B_{1,i}(\bm{r})}$$
- _Neglecting_ the effect of $\bm{B}_1$ on the _spin component_, and supposing that the particle _is in a spin eigenstate_ $\ket{sm_s}$, such that $\braket{\hat{\bm{S}}}$ [[#Wave-function evolution|remains constant]]: 
$$\frac{d}{dt}\mean{\hat{\bm{p}}}=m\frac{d^2}{dt^2}\mean{\hat{\bm{r}}}=\gamma_S m_s\hbar\mean{\nabla B_{1,z}(\bm{r})}$$
- Hence, there are $2s+1$ _different trajectories_

- For some _arbitrary initial spin state_, there is _precession_
- However, as long as $|\bm{B}_1(\bm{r})|$ is _small_, the precession will be _extremely rapid_ relative to the _timescale associated with motion through the field_
- There must be _multiple trajectories_, with _intensity_ proportional to $|c_{m_s}|^2$:
![[Stern-Gerlach trajectories.png]]

- If the experiment is performed with _atoms_, one must take into account the _total spin_:
$$\hat{\bm{F}}=\hat{\bm{I}}+\hat{\bm{L}}+\hat{\bm{S}}$$
- For example, $\text{Cs}$ has $I=7/2$ and a _single valence electron_ $(S=1/2)$, with $L=0$, hence $F=3,4$, and there are _nine beams_