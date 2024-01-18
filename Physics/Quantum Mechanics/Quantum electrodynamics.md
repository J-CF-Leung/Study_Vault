- Atoms can undergo [[Time-dependent quantum mechanics|transitions]] to _other energy states_
- To describe the system accurately, one needs a _quantum description_ of the [[Electrodynamics and Optics|electromagnetic field]]
- One must _quantise_ the modes of the electromagnetic field

# Classical electrodynamics
- [[Electrodynamics and Optics#Electrodynamics and Maxwell's Equations|Maxwell's Equations]] in free space:
$$\displaylines{\nabla\cdot\bm{E}=\frac{\rho}{\epsilon_0} \\ \nabla\times\bm{E}=-\pd{\bm{B}}{t}\\\nabla\cdot\bm{B}=0\\\nabla\times\bm{B}=\mu_0\bm{J}+\mu_0\epsilon_0\pd{\bm{E}}{t}}$$
- The [[Electrodynamics and Optics#Statics|scalar]] and [[Electrodynamics and Optics#The vector potential|vector potential]] are given by:
$$\boldsymbol{E}=-\nabla \phi -\frac{\partial \boldsymbol{A}}{\partial t} \hspace{1.5cm}\boldsymbol{B}=\nabla\times \boldsymbol{A}$$
- In _free space_ where $\rho=0$ and $\boldsymbol{J}=\boldsymbol{0}$, and using the [[Electrodynamics and Optics#Gauge invariance|Coulomb gauge]] $\nabla\cdot \boldsymbol{A}=0$, one gets _Laplace's equation_:
$$\nabla^{2}\phi=0$$
- In a region where $\phi=0$, one gets that the _vector potential_ obeys the _wave equation_:
$$\nabla^{2}\boldsymbol{A}=\frac{1}{c^{2}}\frac{\partial^{2}\boldsymbol{A}}{\partial t^{2}}$$

## Plane wave solutions of the vector potential
- This has _plane wave solutions_:
$$\boldsymbol{A}(\boldsymbol{r},t)=A_{\boldsymbol{k}}\exp[i(\boldsymbol{k}\cdot \boldsymbol{r}-\omega t)]\boldsymbol{e}(\boldsymbol{k})$$
- Here, $\boldsymbol{e}(\boldsymbol{k})$ is a _unit vector_
- The angular frequency:
$$\omega=\omega(k)=c|\boldsymbol{k}|$$
- Diveregence of the plane wave:
$$\nabla\cdot[\exp(i\boldsymbol{k}\cdot \boldsymbol{r})\boldsymbol{e}]=i(\boldsymbol{e}\cdot \boldsymbol{k})\exp(i\boldsymbol{k}\cdot \boldsymbol{r})$$
- This _restricts_ $\boldsymbol{e}$ to within a _plane_
- Hence, there are two _linearly independent_ plane-wave solutions:
$$\boldsymbol{e}_{1}\cdot \boldsymbol{k}=\boldsymbol{e}_{2}\cdot \boldsymbol{k}=\boldsymbol{e}_{1}\cdot \boldsymbol{e}_{2}=0$$

- $\boldsymbol{k}$ defines the _propagation direction_ of the wave
- $\boldsymbol{e}$ defines the _polarisation direction_ of the wave, which must be _perependicular_ to $\boldsymbol{k}$

## Polarisation states
### Linear and circular polarisation modes
- For a wave-vector directed _along the $z-$axis_ $\boldsymbol{k}=(0,0,k)$, the _plane polarisation states_ are:
$$\boldsymbol{e}_{1}=(1,0,0)\hspace{1.5cm}\boldsymbol{e}_{2}=(0,1,0)$$
- This corresponds to _electric fields_ along the $x-$ and $y-$directions

- One can also introduce _circular polarisation_ unit vectors:
$$\displaylines{\boldsymbol{e}_{L}=-\frac{1}{\sqrt{ 2 }}(\boldsymbol{e}_{1}+i\boldsymbol{e}_{2})\hspace{1.5cm}\boldsymbol{e}_{R}=\frac{1}{\sqrt{ 2 }}(\boldsymbol{e}_{1}-i\boldsymbol{e}_{2}) \\ \boldsymbol{e}_{L}\cdot \boldsymbol{e}_{L}^{*}=\boldsymbol{e}_{R}\cdot \boldsymbol{e}_{R}^{*}=1\hspace{1.5cm}\boldsymbol{e}_{L}^{*}\cdot \boldsymbol{e}_{R}=0}$$
- They are _left-handed_ and _right-handed_ polarisation vectors
- Polarisation vectors are _not necessarily real_

- Each wave-vector gives rise to _two independent modes_ $(\boldsymbol{k},\lambda)$, where $\lambda=1,2$ or $L,R$
$$\boldsymbol{A}=A_{\boldsymbol{k}}\exp[i(\boldsymbol{k}\cdot \boldsymbol{r}-\omega t)]\boldsymbol{e}_{\lambda}(\boldsymbol{k})$$

### Rotating into a general direction
- A wave-vector in a _general direction_ indicated by coordinates $(\theta,\phi)$:
$$\boldsymbol{k}=|\boldsymbol{k}|(\sin\theta \cos \phi,\sin\theta \sin \phi,\cos\theta)$$
- This is achieved via the _rotation matrices_:
$$\displaylines{\boldsymbol{k}\to(R_{\phi}R_{\theta})\boldsymbol{k}\hspace{1.5cm}\boldsymbol{e}_{\lambda}\to(R_{\phi}R_{\theta})\boldsymbol{e}_{\lambda} \\ R_{\phi}=\begin{pmatrix}
\cos \phi&-\sin \phi&0\\ \sin \phi&\cos \phi&0\\0&0&1\end{pmatrix}\hspace{1.5cm}R_{\theta} =\begin{pmatrix}
\cos\theta&0&-\sin\theta\\ 0&1&0 \\ \sin\theta&0&\cos\theta\end{pmatrix}}$$
- The _plane polarisation_ states become:
$$\begin{align}
\boldsymbol{e}_{1}&=(\cos\theta \cos \phi,\cos\theta \sin \phi,-\sin\theta) \\ \boldsymbol{e}_{2}&=(-\sin \phi ,\cos \phi,0)\end{align}$$

- The _circular polarisation_ states have _components_ that _cannot be factorised_ into functions of $\theta$ and $\phi$
### Spherical components
- One can express vectors in terms of _spherical components_
	- Related to _angular momentum_
$$e_{+1}\equiv-\frac{1}{\sqrt{ 2 }}(e_{x}+ie_{y})\hspace{1cm}e_{-1}\equiv \frac{1}{\sqrt{ 2 }}(e_{x}-ie_{y})\hspace{1cm}e_{0}\equiv e_{z}$$
- The polarisation vectors _in terms of spherical components_ is then:
$$\displaylines{\boldsymbol{e}=(e_{+1},e_{-1},e_{0}) \\ \begin{align}
\boldsymbol{e}_{1}&=-\frac{1}{\sqrt{ 2 }}\big(\cos\theta \exp(i\phi),-\cos\theta \exp(-i\phi),-\sin\theta\big) \\ \boldsymbol{e}_{2}&=-\frac{i}{\sqrt{ 2 }}\big(\exp(i\phi),\exp(-i\phi),0\big) \\
\boldsymbol{e}_{L}&=-\left( \frac{1}{2}(1-\cos\theta)\exp(i\phi), \frac{1}{2}(1+\cos\theta)\exp(-i\phi),-\frac{1}{\sqrt{ 2 }}\sin\theta \right) \\ \boldsymbol{e}_{R}&=-\left( \frac{1}{2}(1+\cos\theta)\exp(i\phi), \frac{1}{2}(1-\cos\theta)\exp(-i\phi),\frac{1}{\sqrt{ 2 }}\sin\theta \right)\end{align}}$$
- _All components_ can be _factorised_ into functions of $\theta$ and $\phi$

## Mode expansion
- Any _real_ solution $\boldsymbol{A}(\boldsymbol{r},t)$ of the wave equation must be expressible as an _expansion_ over _all possible modes_ of the field:
$$\boldsymbol{A}(\boldsymbol{r},t)=\sum_{\lambda=1}^{2}\int \, d^{3}\boldsymbol{k}\Big[A_{\boldsymbol{k},\lambda}\exp[i(\boldsymbol{k}\cdot \boldsymbol{r}-\omega t)]e_{\lambda}(\boldsymbol{k})+A_{\boldsymbol{k},\lambda}^{*}\exp[-i(\boldsymbol{k}\cdot \boldsymbol{r}-\omega t)]e_{\lambda}^{*}(\boldsymbol{k})\Big] $$

- The _integral_ over $k-$space can be converted into a _sum_ in a _finite space_, such that $k-$points fall in a _lattice_
- The vector potential is then:
$$\boldsymbol{A}(\boldsymbol{r},t)=\sum_{\boldsymbol{k},\lambda}\Big[A_{\boldsymbol{k},\lambda}\exp[i(\boldsymbol{k}\cdot \boldsymbol{r}-\omega t)]e_{\lambda}(\boldsymbol{k})+A_{\boldsymbol{k},\lambda}^{*}\exp[-i(\boldsymbol{k}\cdot \boldsymbol{r}-\omega t)]e_{\lambda}^{*}(\boldsymbol{k})\Big] $$

- The _electric field_ then has the expansion:
$$\boldsymbol{E}(\boldsymbol{r},t)=\sum_{\boldsymbol{k},\lambda}i\omega(\boldsymbol{k})\Big[A_{\boldsymbol{k},\lambda}\exp[i(\boldsymbol{k}\cdot \boldsymbol{r}-\omega t)]e_{\lambda}(\boldsymbol{k})-A_{\boldsymbol{k},\lambda}^{*}\exp[-i(\boldsymbol{k}\cdot \boldsymbol{r}-\omega t)]e_{\lambda}^{*}(\boldsymbol{k})\Big] $$
- The _magnetic field_ has the expansion:
$$\boldsymbol{B}(\boldsymbol{r},t)=\sum_{\boldsymbol{k},\lambda}i\boldsymbol{k}\times\Big[A_{\boldsymbol{k},\lambda}\exp[i(\boldsymbol{k}\cdot \boldsymbol{r}-\omega t)]e_{\lambda}(\boldsymbol{k})-A_{\boldsymbol{k},\lambda}^{*}\exp[-i(\boldsymbol{k}\cdot \boldsymbol{r}-\omega t)]e_{\lambda}^{*}(\boldsymbol{k})\Big] $$

## Electromagnetic field energy
- The [[Electrodynamics and Optics#Electromagnetic energy|total field energy]] in free space with volume $V$ is:
$$U=\frac{1}{2}V\int_{V}  \left( \epsilon_{0}\boldsymbol{E}\cdot \boldsymbol{E}+\frac{1}{\mu_{0}}\boldsymbol{B}\cdot \boldsymbol{B}\, \right) dV $$
- Substituting the mode expansions, one gets:
$$U=V\sum_{\boldsymbol{k},\lambda}\epsilon_{0}\omega(\boldsymbol{k})^{2}\Big[A_{\boldsymbol{k},\lambda}A_{\boldsymbol{k},\lambda}^{*}+A_{\boldsymbol{k},\lambda}^{*}A_{\boldsymbol{k},\lambda}\Big]$$
- In _classical mechanics_, as $A_{\boldsymbol{k},\lambda}$ is a _scalar_, it and its conjugate _commute_, hence it can be _simplified_ to 
$$U_\text{clas}=2V\sum_{\boldsymbol{k},\lambda} \epsilon_0\omega(\boldsymbol{k})^2|A_{\bm{k},\lambda}|^2$$
- One can also introduce the _dimensionless_ coefficients:
$$A_{\boldsymbol{k},\lambda}=\sqrt{ \frac{\hbar}{2\epsilon_{0}\omega(\boldsymbol{k})V} }\;a_{\boldsymbol{k},\lambda}\hspace{1.5cm}A_{\boldsymbol{k},\lambda}^{*}=\sqrt{ \frac{\hbar}{2\epsilon_{0}\omega(\boldsymbol{k})V} }\;a^{*}_{\boldsymbol{k},\lambda}$$
- The field energy can then be _rewritten_ as:
$$U=\sum_{\boldsymbol{k},\lambda}\frac{1}{2}\hbar\omega(\boldsymbol{k})\big[a_{\boldsymbol{k},\lambda}a^{*}_{\boldsymbol{k},\lambda}+a_{\boldsymbol{k},\lambda}^{*}a_{\boldsymbol{k},\lambda}\big]$$
- This resembles the form of the Hamiltonian for the [[Quantum Harmonic Oscillator]]:
$$\hat{H}=\frac{1}{2}\hbar\omega[\hat{a}\hat{a}^{\dagger}+\hat{a}^{\dagger}\hat{a}]$$

# Quantised electromagnetic field
- To quantise the field _convert_ the coefficients $a_{\boldsymbol{k},\lambda}$ into _ladder operators_ for that particular mode:
$$\hat{H}=\sum_{\boldsymbol{k},\lambda}\frac{1}{2}\hbar\omega(\boldsymbol{k})\Big[a_{\boldsymbol{k},\lambda}a^{\dagger}_{\boldsymbol{k},\lambda}+a_{\boldsymbol{k},\lambda}^{\dagger}a_{\boldsymbol{k},\lambda}\Big]$$
- Each _mode_ becomes _its own quantum harmonic oscillator_
	- It is _general result_ for [[Classical Field Theory#Quantum fields|all fields]]
- There are _two oscillators_ for each wavevector $\boldsymbol{k}$ corresponding to the polarisation states

## Modes, operators, and photons
- The eigenstates are still characterised by _quantum numbers_ $n_{\boldsymbol{k},\lambda}=0,1,2,\dots$
- The ladder operators will _change_ the quantum number, or _occupancy_, by $\pm1$
$$\begin{align}\hat{a}^{\dagger}_{\boldsymbol{k},\lambda}\ket{n_{\boldsymbol{k},\lambda}}&=\sqrt{ n_{\boldsymbol{k},\lambda}+1 }\ket{n_{\boldsymbol{k},\lambda}+1} \\ \hat{a}_{\boldsymbol{k},\lambda}\ket{n_{\boldsymbol{k},\lambda}}&=\sqrt{ n_{\boldsymbol{k},\lambda} }\ket{n_{\boldsymbol{k},\lambda}-1} \\ \hat{a}_{\boldsymbol{k},\lambda}\ket{n_{\boldsymbol{k},\lambda}=0}&=0   \end{align}$$
- All _other_ mode occupancies are _unaffected_

- $\ket{n_{\boldsymbol{k},\lambda}}$ is a state with $n_{\boldsymbol{k},\lambda}$ _photons_ with wave-vector $\boldsymbol{k}$ and polarisation state $\lambda$
- The ladder operators _create and annihilate_ the photons
![[Photon ladder.png]]

- The _vacuum state_ $\ket{0}$ is the state containing _no photons in any mode_:
$$\hat{a}_{\boldsymbol{k},\lambda}\ket{0}=0\hspace{1cm} \forall \;\boldsymbol{k},\lambda $$
- States containing photons can then be built by using the _creation operator on the vacuum state_:
$$\displaylines{\hat{a}^{\dagger}_{\boldsymbol{k},\lambda}\ket{0}=\ket{\boldsymbol{k},\lambda}=\ket{1_{\boldsymbol{k},\lambda}}\\ \frac{1}{\sqrt{ n_{\boldsymbol{k},\lambda}! }}(\hat{a}_{\boldsymbol{k},\lambda})^{n}\ket{0}=\ket{n_{\boldsymbol{k},\lambda}} \\ \ket{\boldsymbol{k}_{1},\lambda_{1};\boldsymbol{k}_{2},\lambda_{2}}=\hat{a}^{\dagger}_{\boldsymbol{k}_{1},\lambda_{1}}\hat{a}^{\dagger}_{\boldsymbol{k}_{2},\lambda_{2}}\ket{0}=\ket{1_{\boldsymbol{k}_{1},\lambda_{1}},1_{\boldsymbol{k}_{2},\lambda_{2}}}     }$$

- The oscillators for _each mode_ are always _independent of each other_:
$$\displaylines{[\hat{a}_{\boldsymbol{k},\lambda},\hat{a}^{\dagger}_{\boldsymbol{k}',\lambda'}]=\delta_{\boldsymbol{kk}'}\delta_{\lambda\lambda'} \\ [\hat{a}_{\boldsymbol{k},\lambda},\hat{a}_{\boldsymbol{k}',\lambda'}]=[\hat{a}_{\boldsymbol{k},\lambda}^{^{\dagger}},\hat{a}^{\dagger}_{\boldsymbol{k}',\lambda'}]=0}$$

- The $n-$photon state $\ket{n_{\boldsymbol{k},\lambda}}$ is an eigenstate of the _number operator_:
$$\begin{align} \hat{n}_{\boldsymbol{k},\lambda}&=\hat{a}^{\dagger}_{\boldsymbol{k},\lambda}\hat{a}_{\boldsymbol{k},\lambda} \\ \hat{n}_{\boldsymbol{k},\lambda}\ket{n_{\boldsymbol{k},\lambda}}&=n_{\boldsymbol{k},\lambda}\ket{n_{\boldsymbol{k},\lambda}}   \end{align}$$
- As it is an eigenstate, there is _no uncertainty in the number of photons_:
$$\Delta n_{\boldsymbol{k},\lambda}=0$$
- They are known as _Fock states_, and have a _well-defined number of photons_
- They form a _complete, orthonormal set_ of eigenstates

## Particle exchange
- Consider the _two-electron state_ and using the commutation relation above:
$$\ket{\boldsymbol{k}_{1},\lambda_{1};\boldsymbol{k}_{2},\lambda_{2}}=\hat{a}^{\dagger}_{\boldsymbol{k}_{1},\lambda_{1}}\hat{a}^{\dagger}_{\boldsymbol{k}_{2},\lambda_{2}}\ket{0}=\hat{a}^{\dagger}_{\boldsymbol{k}_{2},\lambda_{2}}\hat{a}^{\dagger}_{\boldsymbol{k}_{1},\lambda_{1}}\ket{0}=\ket{\boldsymbol{k}_{2},\lambda_{2};\boldsymbol{k}_{1},\lambda_{1}} $$
- Hence, photons are _symmetric w.rt. particle exchange_, and they are [[Identical Particles#Particle exchange, fermions and bosons|bosons]]

- For _spin-half_ particles, one must use _anti-commutation_ relations:
$$\displaylines{[\hat{a}_{\boldsymbol{k},\lambda}^{^{\dagger}},\hat{a}^{\dagger}_{\boldsymbol{k}',\lambda'}]_{+}=0 \\ \ket{\boldsymbol{k}_{1},\lambda_{1};\boldsymbol{k}_{2},\lambda_{2}}=\hat{a}^{\dagger}_{\boldsymbol{k}_{1},\lambda_{1}}\hat{a}^{\dagger}_{\boldsymbol{k}_{2},\lambda_{2}}\ket{0}=-\hat{a}^{\dagger}_{\boldsymbol{k}_{2},\lambda_{2}}\hat{a}^{\dagger}_{\boldsymbol{k}_{1},\lambda_{1}}\ket{0}=-\ket{\boldsymbol{k}_{2},\lambda_{2};\boldsymbol{k}_{1},\lambda_{1}} }$$

## Zero-point energy
- The Hamiltonian:
$$\begin{align}\hat{H}&=\sum_{\boldsymbol{k},\lambda}\frac{1}{2}\hbar\omega(\boldsymbol{k})\Big[a_{\boldsymbol{k},\lambda}a^{\dagger}_{\boldsymbol{k},\lambda}+a_{\boldsymbol{k},\lambda}^{\dagger}a_{\boldsymbol{k},\lambda}\Big] \\ &=\sum_{\boldsymbol{k},\lambda}\hbar\omega(\boldsymbol{k})\left( \hat{n}_{\boldsymbol{k},\lambda}+ \frac{1}{2} \right)
\end{align}$$
- The _expectation value_ for the energy of the _vacuum state_:
$$U_{0}=\Braket{ 0|\hat{H} |0  }=\sum_{\boldsymbol{k},\lambda} \frac{1}{2}\hbar\omega(\boldsymbol{k}) $$
- This is the _zero-point energy_
	- It goes to _infinity_
	- Physical meaning is given after _renormalisation_

- If one _defines_ energies to be _relative_ to the zero-point energy:
$$\hat{H}=\sum_{\boldsymbol{k},\lambda} \frac{1}{2}\hbar\omega(\boldsymbol{k})\hat{a}^{\dagger}_{\boldsymbol{k},\lambda}\hat{a}_{\boldsymbol{k},\lambda}$$

## Electric field
- The _electric field operator_:
$$\hat{\boldsymbol{E}}(\boldsymbol{r},t)=\sum_{\boldsymbol{k},\lambda}i\omega(\boldsymbol{k})N(\boldsymbol{k})\Big[\hat{a}_{\boldsymbol{k},\lambda}\exp[i(\boldsymbol{k}\cdot \boldsymbol{r}-\omega t)]e_{\lambda}(\boldsymbol{k})-\hat{a}_{\boldsymbol{k},\lambda}^{\dagger}\exp[-i(\boldsymbol{k}\cdot \boldsymbol{r}-\omega t)]e_{\lambda}^{*}(\boldsymbol{k})\Big]$$
- For the [[#Modes, operators, and photons|Fock states]], one can calculate the _expectation value_:
$$\left\langle  \hat{\boldsymbol{E}}  \right\rangle=\braket{ n_{\boldsymbol{k},\lambda}|\hat{\boldsymbol{E}} |n_{\boldsymbol{k},\lambda}  }=0  $$
- One can also calculate _uncertainty_:
$$(\Delta \boldsymbol{E})^{2}=\left( n_{\boldsymbol{k},\lambda}+\frac{1}{2} \right)\frac{\hbar \omega(\boldsymbol{k})}{\epsilon_{0}V}$$
- For the _vacuum state_:
$$(\Delta \boldsymbol{E})^{2}_{0}=\frac{\hbar \omega(\boldsymbol{k})}{\epsilon_{0}V}$$
# Photons
- A _photon_ of wave-vector $\boldsymbol{k}$ and polarisation $\lambda$ is an _excitation_ in the electromagnetic _mode_ $(\boldsymbol{k},\lambda)$

## Energy
- The Hamiltonian operating on a _single photon mode_:
$$\hat{H}\ket{\boldsymbol{k},\lambda}=\sum_{\boldsymbol{k}',\lambda'}\hbar \omega(\boldsymbol{k}')\hat{a}^{^{\dagger}}_{\boldsymbol{k}',\lambda'}\hat{a}_{\boldsymbol{k},\lambda}(\hat{a}^{\dagger}_{\boldsymbol{k},\lambda}\ket{0} ) $$
- Using the commutation relation, one finds:
$$\hat{H}\ket{\boldsymbol{k},\lambda}=\hbar\omega(\boldsymbol{k})\ket{\boldsymbol{k},\lambda}  $$
- As expected, a _single-photon state_ $\ket{\boldsymbol{k},\lambda}$ is an _eigenstate_ of $\hat{H}$ with _energy_ $\hbar\omega(\boldsymbol{k})$

## Linear momentum
- _Classically_, the [[Electrodynamics and Optics#Electromagnetic energy|Poynting vector]] $\boldsymbol{N}=\boldsymbol{E}\times \boldsymbol{H}$ gives the _energy flux_ (energy per unit time per unit area)
- The _total linear momentum_ in the field is then:
$$\boldsymbol{P}=\int \frac{1}{c^{2}}\boldsymbol{E}\times \boldsymbol{H}\, d^{3}\boldsymbol{r}=-\epsilon_{0}\int \frac{\partial \boldsymbol{A}}{\partial t}\times(\nabla\times \boldsymbol{A})\, d^{3}\boldsymbol{r}  $$

- As an _operator_, the vector potential can be written as
	- With the factor $N(\boldsymbol{k})=\sqrt{ \hbar/(2\epsilon_{0}\omega(\boldsymbol{k})V) }$ to convert to the ladder operators
$$\hat{\boldsymbol{A}}(\boldsymbol{r},t)=\sum_{\boldsymbol{k},\lambda}N(\boldsymbol{k})\Big[\hat{a}_{\boldsymbol{k},\lambda}\exp[i(\boldsymbol{k}\cdot \boldsymbol{r}-\omega t)]e_{\lambda}(\boldsymbol{k})+\hat{a}_{\boldsymbol{k},\lambda}^{\dagger}\exp[-i(\boldsymbol{k}\cdot \boldsymbol{r}-\omega t)]e_{\lambda}^{*}(\boldsymbol{k})\Big] $$
- Substituting this into the _total linear momentum_ operator:
$$\begin{align}\hat{\boldsymbol{P}}&=-\epsilon_{0}\int \frac{\partial \hat{\boldsymbol{A}}}{\partial t}\times(\nabla\times \hat{\boldsymbol{A}})\, d^{3}\boldsymbol{r} \\ &=\sum_{\boldsymbol{k},\lambda}\hbar \boldsymbol{k}\hat{a}_{\boldsymbol{k},\lambda}^{\dagger}\hat{a}_{\boldsymbol{k},\lambda}\end{align}$$
- Then by a similar strategy to finding energy:
$$\hat{\boldsymbol{P}}\ket{\boldsymbol{k},\lambda}=\hbar \boldsymbol{k}\ket{\boldsymbol{k},\lambda}  $$
- Each _photon_ has _linear momentum_ $\hbar \boldsymbol{k}$, as expected

## Angular momentum (spin)
- _Classically_, the _total angular momentum_ about point $\boldsymbol{r}$ can be _decomposed_ into a _position-dependent_, _orbital_ part and an _intrinsic_ part:
$$\boldsymbol{J}(\boldsymbol{r})=\boldsymbol{J}_{O}(\boldsymbol{r})+\boldsymbol{J}_{s}$$
- The intrinsic part is given by:
$$\boldsymbol{J}_{s}=\int \boldsymbol{E}\times \boldsymbol{A} \, d^{3}\boldsymbol{r} $$
- It is _independent of position_

- After _quantisation_, it is found to be:
$$\hat{\boldsymbol{J}}_{s}=\hbar \sum_{\boldsymbol{k}} \frac{\boldsymbol{k}}{|\boldsymbol{k}|}\Big[\hat{a}^{\dagger}_{\boldsymbol{k},L}\hat{a}_{\boldsymbol{k},L}-\hat{a}^{\dagger}_{\boldsymbol{k},R}\hat{a}_{\boldsymbol{k},R}\Big]$$
- $L$ and $R$ are the [[#Polarisation states|spherical polarisation states]]
- The creation and annihilation operators for those are defined as:
$$\hat{a}_{\boldsymbol{k},L}\equiv-\frac{1}{\sqrt{ 2 }}\big[\hat{a}_{\boldsymbol{k},1}+i \hat{a}_{\boldsymbol{k},2}\big]\hspace{1.5cm}\hat{a}_{\boldsymbol{k},R}\equiv\frac{1}{\sqrt{ 2 }}\big[\hat{a}_{\boldsymbol{k},1}-i \hat{a}_{\boldsymbol{k},2}\big]$$
- Operating on the _circularly polarised single photon states_:
$$\hat{\boldsymbol{J}}_{s}\ket{\boldsymbol{k},L}=+\hbar \frac{\boldsymbol{k}}{|\boldsymbol{k}|}\ket{\boldsymbol{k},L}\hspace{1.5cm}\hat{\boldsymbol{J}}_{s}\ket{\boldsymbol{k},R}=-\hbar \frac{\boldsymbol{k}}{|\boldsymbol{k}|}\ket{\boldsymbol{k},R}  $$
- The angular momentum is _oriented parallel $(L)$_ or _antiparallel_ $(R)$
	- Convention is _not universal_
![[Photon spin directions.png]]

- From this, photons are _spin-one particles_
- They only possess _two_ degrees of freedom
	- The $m_s=0$ degree of freedom is _longitudinal_, and photons are _all transversely polarised_

- In electromagnetism, interactions of left and right handed photons are of _equal strength_
	- In _weak_ interactions, they are of different strengths (_parity_ violations)