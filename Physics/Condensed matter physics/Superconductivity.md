![[Superconducting periodic table.png|500]]
# Phenomenology
- A _drop_ in _resistivity_ $\rho$ to _zero_ at _low temperatures_

- This leads to _dissipation-less currents_

- One consequence is that for a _ring geometry_, it _freezes_ the flux inside the ring
	- The flux takes an _infinite time_ to decay
	- The flux frozen must also be an _integer multiple_ of the _flux quantum_
$$\frac{\partial B}{\partial t}=-\nabla\times \boldsymbol{E}=\rho \nabla\times \boldsymbol{J}=0$$
- If one tries to _switch on_ a field below superconducting temperature, it _will not penetrate_ into the material
- Meanwhile, if one _keeps the magnetic field while cooling_, the material will _expel_ the magnetic field
	- The _Meissner-Ochsenfeld effect_
![[Meissner effect.png|200]]

- Above a certain _critical field_, superconductivity will be _destroyed_
	- Type I: complete breakdown of superconducting state
	- Type II: _partial_ penetration
![[Critical field for superconducting.png|400]]

- The phenomena above hint at superconductivity being _quantum mechanical_
- The _supercurrent_ may be related to the wavefunction current $\propto \psi^{*}\nabla \psi-\psi \nabla \psi^{*}$, which is due to a spatially varying _phase_
## London equations
- _Phenomenological_, _macroscopic_ equations governing superconductors

### First London equation
- From _Drude theory_ and the _relaxation time approximation_:
$$\left( \frac{\partial}{\partial t}+\frac{1}{\tau} \right)\boldsymbol{j}=\left( \frac{ne^{2}}{m} \right)\boldsymbol{E}$$
- For perfect conductivity, $\tau\to \infty$, giving the _first London equation_
	- $\Lambda=(ne^{2}/m)^{-1}$
$$\Lambda \frac{\partial}{\partial t}\boldsymbol{j}=\boldsymbol{E}$$
- One can have a _constant current without any electric field_
	- In contrast to normal metals where $\boldsymbol{j}=\sigma \boldsymbol{E}$ in steady state

### Second London equation
- Then from Maxwell's equations:
$$\displaylines{\frac{\partial \boldsymbol{B}}{\partial t}=-\nabla\times \boldsymbol{E}=-\Lambda \nabla\times \frac{\partial}{\partial t}\boldsymbol{j} \\ \boldsymbol{B}=-\Lambda \nabla\times \boldsymbol{j}}$$
- The _integration constant_ is set to _zero_ due to _flux expuision_
- Can also be found by _minimising free energy_
	- Free energy: both the _supercurrent kinetic energy_ and _magnetic field energy_

- Also using $\nabla\times \boldsymbol{B}=\mu_{0}\boldsymbol{j}$, this gives:
$$-\nabla^{2}\boldsymbol{B}=-\frac{\mu_{0}}{\Lambda}\boldsymbol{B}$$
- The magnetic field must _decay_ with some _penetration depth_:
$$B\propto \exp\left( -\frac{x}{\lambda} \right)\qquad \lambda^{2}=\frac{\Lambda}{\mu_{0}}=\left( \frac{c}{\omega_{p}} \right)^{2}$$
- Typical depth is $\sim 40\,\text{nm}$

### The London gauge
- Use the _London gauge_:
$$\nabla\cdot \boldsymbol{A}=0$$
- Meanwhile, let $\boldsymbol{A}=0$ in the _bulk_, and $\boldsymbol{A}_{\perp}=0$ on the _surface_
	- There should be no current going _out_ of the superconductor
$$\boldsymbol{A}\cdot \hat{\boldsymbol{n}}=0$$

- The London equations then imply that for the _vector potential_:
	- Satisfied iff London gauge
$$\boldsymbol{A}=-\Lambda \boldsymbol{j}$$

- After flux expulsion, _any screening supercurrent_ must also _decay in the bulk_
## Analogies

### Atomic diamagnetism
- Decompose an atomic wavefunction:
$$\psi=|\psi|\exp(i\phi)$$
- From _single-valuedness_, the _phase change_ upon circling the nucleus is $2\pi n$ regardless of field
- There is then _quantised wavelengths_ $\lambda=2\pi r/n$
- The _semiclassical_ momentum, taking the _vector potential_ into account:
$$p=mv+qA=\frac{h}{\lambda}$$

- When one _changes_ $\boldsymbol{A}$, there is some _screening current_
$$j=nqv=-\frac{nq^{2}}{m}A$$
- Same as the London eq.

- Flaws:
	- Metals have _much more closely spaced energy levels_, such that electrons can simply _redistribute without screening_
	- Persistent currents only show up in _excited states_, which _decay quickly_
- A superconducting state is _rigid_ against perturations and decay

### Mechanical analogies
- In _liquids_, shear stress corresponds to a _velocity gradient_ $\sigma \propto \Delta v$
- In solds, shear stress corresponds to _deformation_ $\sigma \propto\Delta x$

- Analogy: in metals, $\boldsymbol{j}\propto \boldsymbol{E}=- \dot{\boldsymbol{A}}$ and $\boldsymbol{j}\propto \boldsymbol{A}$ in _superconductors_

- In solids, a _static stress_ gives _no shear velocity_, as _all bonds_ must be _broken simultaneously_
- One can draw an _analogy_ between _solids_ and _superconductors_
	- The _displacement_ of atoms is some _superflow_ of rigidity
	- A displaced electron _phase_ gives a _superflow_ of charge

- The metal-superconductor transition can be compared to the _liquid-solid phase transition_

## Behaviour of specific heat and entropy
- The specific heat _around_ the transition temperature:
![[Electron specific heat superconductivity.png|300]]
- There is _exponential low temperature behaviour_, consistent with the appearance of an _energy gap_
	- In _unconventional_ superconductors, there is _power law_ behaviour

- The _matching areas_ indicate a _second order transition_

- Entropy:
![[Superconductor entropy.png|350]]
- The superconducting state has _lower entropy_, and is a _more ordered state_
- The transition is _second order_ and can be described using some _order parameter_

- Appearance of an order parameter gives rise to _Ginzburg-Landau Theory_
# Ginzburg-Landau Theory
- Phase transition from normal to superconducting state occurs when the _latter has a lower free energy_
- Taking into account the energy from the magnetic field, the _Ginzburg-Landau free energy density_:
$$G=G_{0}+\int  d\boldsymbol{r}\left\{ \alpha|\psi|^{2}+\frac{\beta}{2} |\psi|^{4}+\frac{1}{2m^{*}}\left|\left(-i\hbar \nabla-q\boldsymbol{A}\right)\psi \right|^{2}+\frac{1}{2\mu_{0}}|\nabla\times(\boldsymbol{A}-\boldsymbol{A}_{E})|^{2}\right\} $$
- The first two terms are a _symmetric free energy expansion_ in terms of some _condensate wavefunction_ $\psi$
- The third term _penalises heterogeneities_ in the system, using a _gauge-invariant gradient term_, with _phenomenological parameters_ $m^{*}$ and $q$
	- Experimentally, $q=-2|e|$

- The last term accounts for _energy due to some magnetic field in the superconductor_ $\boldsymbol{B}_{M}=\nabla\times (\boldsymbol{A}-\boldsymbol{A}_{E})$, where the magnetic field is _given by internal currents_
	- $\nabla\times\boldsymbol{A}$ is the _total field_, while $\nabla\times \boldsymbol{A}_{E}$ is the _external field_

- For there to be some _phase transition_ at $T<T_{c}$ for a homogeneous system:
$$\alpha=\alpha'(T-T_{c})$$
- Consider a _homogeneous system deep inside a superconductor_ (assume Meissner effect already applies)
$$\begin{align}
&\alpha>0\implies |\psi_{0}|=0,\quad B=B_{E},\quad f(\psi_{0})=0  \\
&\alpha<0 \implies |\psi_{0}|=\sqrt{ -\frac{\alpha}{\beta} },\quad B=0,\quad f(\psi_{0})=-\frac{\alpha^{2}}{2\beta}+\frac{B_{E}^{2}}{2\mu_{0}} \quad
\end{align}$$
- The superconducting state is _only stable below a critical field_:
$$B_{c}=\sqrt{ \frac{\mu_{0}\alpha^{2}}{\beta} }$$
## Ginzburg-Landau equations
- In general, $\psi$ and $\boldsymbol{A}$ are _inhomogeneous_
	- _Vortices_ may show up, where the magnetic field is _not completely screened_

- By _minimising_ the free energy density w.r.t. $\psi(\boldsymbol{r})$ and $\boldsymbol{A}(\boldsymbol{r})$, one gets the _Ginzburg-Landau equations_ in the bulk
	- Minimising w.r.t. $\boldsymbol{A}$: use $\nabla\cdot(\boldsymbol{B}_{M}\times\delta \boldsymbol{A})=\delta \boldsymbol{A}\cdot \nabla\times \boldsymbol{B}_{M}-\boldsymbol{B}_{M}\cdot(\nabla\times\delta \boldsymbol{A})=0$
$$\displaylines{\frac{1}{2m}\left( \frac{\hbar}{i}\nabla -e^{*}\boldsymbol{A} \right)^{2}\psi+(\alpha+\beta|\psi|^{2})\psi=0 \\ \begin{align}
\boldsymbol{J}_{s}=\frac{1}{\mu_{0}}\nabla\times \boldsymbol{B}_{M}&=\frac{q}{2m} \frac{\hbar}{i}(\psi^{*}\nabla \psi-\psi \nabla \psi^{*})-q^{2}|\psi|^{2}\boldsymbol{A}  \\
&=\frac{q}{m}\mathrm{Re}\left( \psi^{*}\left( \frac{\hbar}{i}\nabla-q\boldsymbol{A} \right)\psi \right)
\end{align}}$$

- For the first equation to hold, the contribution on the _surface_ of vector $\boldsymbol{n}$ must also be zero (for superconductor-vacuum interface)
	- _No perpendicular supercurrent_
	- Interfaces to _ferromagnets_ and _metals_ will have different boundary conditions
$$(i\hbar \nabla \psi+q\boldsymbol{A}\psi)\cdot \boldsymbol{n}=0$$
- The supercurrent $\boldsymbol{J}_{s}$ can be rewritten by writing $\psi$ as:
$$\displaylines{\psi=\sqrt{ n_{s} }\exp(i\theta) \qquad \rho_{s}=\frac{q^{2}n_{s}}{m^{*}}\\ \boldsymbol{J}_{s}=\rho_{s}\left( \frac{\hbar}{q}\nabla\theta-\boldsymbol{A} \right)}$$

- The equations suggest that the superconductor order parameter _behaves as a wavefunction, with additional nonlinear effects_
	- Without $\alpha$, it gives the [[Theories of Quantum Matter#Gross-Pitaevskii approximation|Gross-Pitaevskii equation]] for interacting condensates
	- The $\beta$ term can be interpreted as some _effective potential_
- Experimentally, $q=-2|e|$, $m^{*}=2m_{e}$ and $n_{s}=n_{e}/2$, which suggests _pairing_

### Meissner effect and penetration depth from Ginzburg-Landau
- In the London approximation, assume $n_{s}$ is _fixed_ near some equilibrium value $-\alpha/\beta$
- However, the _phase_ $\theta$ can vary

- If $\theta$ is _single-valued_, $\oint \nabla\theta \cdot d\boldsymbol{s}=0$ such that $(\nabla\times \nabla)\theta=0$
	- $\psi$ is always single-valued, but $\theta$ is only single-valued for a _simply connected domain_
- Then one gets the _second_ [[#London equations|London equation]] from the Ginzburg-Landau equations
$$\nabla\times \boldsymbol{J}_{s}=-\rho_{s}\boldsymbol{B}$$
- Then from Maxwell's eq.
$$\nabla^{2}\boldsymbol{B}=\frac{\boldsymbol{B}}{\lambda^{2}}\qquad \lambda=\frac{1}{\sqrt{ \mu_{0}\rho_{s} }}=\sqrt{ \frac{m}{4\mu_{0}e^{2}n_{s}} }$$
- $\lambda$ is some _penetration depth_ of the magnetic field into the solid

## Gauge symmetry and topology in superconductors
- The gauge transformation of $\boldsymbol{A}$:
	- Gauge symmetry: a _mathematical redundancy_ rather than anything physical
	- Akin to _coordinate transformation_
$$\boldsymbol{A}\to \boldsymbol{A}+\nabla \chi \qquad \varphi \to \varphi-\dot{\chi}$$
- The corresponding transformation for the wavefunction:
$$\psi\to \psi \exp\left( i\frac{q}{\hbar} \chi\right) \qquad \theta\to \theta+\frac{q}{\hbar}\chi$$
- The _supercurrent_ $\boldsymbol{J}_{s}$ remains _invariant_ as an observable
	- The Ginzburg-Landau equations themselves are invariant

- One can also have a gauge transformation such that $\theta$ goes to $0$ _everywhere_

- Having some nonzero $\theta$ corresponds to a _broken symmetry state_

### Coherence length and lengthscales
- The first Ginzburg-Landau equation has some _lengthscale_ such that it can be written as:
$$\xi^{2}\nabla^{2}\psi+\psi-\frac{\beta}{|\alpha|}|\psi|^{2}\psi=0\qquad \xi=\sqrt{ \frac{\hbar^{2}}{2m|\alpha|} }$$
- This is the lengthscale to which the _magnitude_ of $\psi$ might change
- In a _vortex_, it can be interpreted as the lengthscale around which $|\psi|$ reverts to the _bulk value_, also known as the width of the _vortex core_

- It is related to $\alpha$, a _phenomenological parameter_
- Hence it also _diverges_ at $T=T_{c}$

- $\lambda$ (penetration depth) and $\xi$ (coherence length) _define_ the Ginzburg-Landau parameters _in the homogeneous superconducting state_
$$\xi^{2}=\frac{\hbar^{2}}{2m|\alpha|} \qquad \lambda^{2}=\frac{m\beta}{\mu_{0}q^{2}|\alpha|}$$
- The _critical field_:
$$B_{c}\sim \lambda \xi$$

- For _inhomogeneities_, consider _vortices_
### Flux quantisation and vortices
- Consider a superconductor with some _hole_, which is _threaded_ by some magnetic field
![[Quantised flux.png|250]]
- Far away from the surface, $J_{s}\to 0$ such that:
$$\boldsymbol{A}=-\frac{\hbar}{2e}\nabla\theta$$
- Relating this to flux:
$$\Phi=\oint\,\boldsymbol{A}\cdot d\boldsymbol{l} =\frac{\hbar}{q} \oint  \nabla\theta \cdot d\boldsymbol{l} =\frac{\hbar}{q}2\pi n $$
- There is some _quantised trapped flux_ inside the superconductor
- The unit is the _flux quantum_
	- Relevant charge is $2e$ instead of $e$
$$\Phi_{0}=\frac{h}{2e}$$
- The presence of vortices indicates _macroscopic coherence_
### Vortices as a topological defect
- Identify the superconducting material with a _wire_, and each point of the wire has a corresponding _plane_ on which $\psi=|\psi|\exp(i\theta)$ is defined, such that the _locus_ of $\psi$ is on a _tube_
- A superconductor with a _hole_ means the tube is a _torus_, and the locus is some _winding around the torus_, with _winding number_ $n$ such that $\Delta\theta=2\pi n$
- The supercurrent is _topologically protected_
![[Superconductor topological defect.png|200]]

- The trapped flux gives a _topological defect_, which cannot change

### Vortex energy
- Assume $\lambda\gg \xi$, such that there is only a _small vortex core_, and one can calculate _magnetic energy outside_

- Inspect the _change in free energy_ from forming the _vortex_
	- The $|\psi|^{2}$ and $|\psi|^{4}$ terms are _approximately constant_, apart from the _vortex core_
	- To rewrite the gradient term, _assume_ $n_{s}$ is _constant outside the vortex core_
$$\displaylines{f_\text{kin}=\frac{1}{2m^{*}}\left|\left(-i\hbar \nabla-q\boldsymbol{A}\right)\psi \right|^{2}=n_{s}\frac{(mv_{s})^{2}}{2m}=\frac{\mu_{0}}{2}\lambda^{2}J_{s}^{2} \\ f_{B}=\frac{|\boldsymbol{B}-\boldsymbol{B}_{E}|^{2}}{2\mu_{0}} \\ \Delta f=f_\text{vortex}-f_\text{uniform}=\frac{1}{2\mu_{0}}[(\mu_{0}\lambda J_{s})^{2}+B^{2}-2\boldsymbol{B}\cdot \boldsymbol{B}_{E}]}$$
- There is a _kinetic energy cost_ due to the supercurrent
- Meanwhile, there is a _decrease_ in _magnetic energy_

- For some _high_ $B_{E}$, forming vortices becomes _spontaneous_ as $\Delta f<0$
### The lower critical field and type II superconductors
- Each vortex is asumed to contain _only one flux quantum_ as higher flux is _unfavourable_
- Assume $\lambda\gg \xi$ so one can _neglect the vortex core_

- The _magnetic field energy per unit length_:
$$\Delta F_\text{mag}=B_{E}\int  \frac{B}{\mu_{0}} \,d^{2}r=B_{E} \frac{\phi_{0}}{\mu_{0}}$$
- Meanwhile, the _kinetic energy cost_:
$$\displaylines{mv_{s}\sim \hbar \nabla\theta=\hbar \left( \frac{2\pi}{2\pi r} \right)=\frac{\hbar}{r} \\ \int_{\xi}^{\lambda}n_{s} \frac{(mv_{s})^{2}}{2m}(2\pi r)\,dr\approx \frac{\pi \hbar^{2}n_{s}}{m}\ln\left( \frac{\lambda}{\xi} \right)=\frac{\phi_{0}^{2}}{4\pi\lambda^{2}\mu_{0}}\ln\left( \frac{\lambda}{\xi} \right)}$$

- There is some _critical field_ $B_{c1}$ where the vortex formation is _energetically advantageous_:
$$B_{E}> \frac{\phi_{0}}{4\pi\lambda^{2}}\ln\left( \frac{\lambda}{\xi} \right) \qquad B_{c1}=\frac{\phi_{0}}{4\pi\lambda^{2}}=\frac{\xi}{\sqrt{ 2 }\lambda}B_{c}$$

- Vortices form when a _disc_ of _radius_ $\sim\lambda$ starts _enclosing_ one flux quantum

- In _type I_ superconductors, $B_{c1}>B_{c}$ such that the sample becomes _normal_ before vortex formation
- In _type II_ superconductors, _flux expulsion stops partially_, such that the magnetic field _penetrates_ forms a _vortex lattice_
	- Vortices penetrate until there is enough _repulsion_ and they settle into a lattice
	- This continues up to some other field strength $B>B_{c2}$ where the sample becomes _normal_
![[Type I and type II superconductivity.png|500]]
## Type II superconductors and vortex lattices
- Type II superconductors form _lattices_ of _circular vortices_
- Each vortex has _inner radius_ $\xi$ and _outer radius_ $r_{B}<\lambda$

- Let $\xi\ll\lambda$ such that the _vortex core_ can be ignored

- The vortex _screening_ means that _within_ the vortex, one can estimate some $\langle B \rangle$:
$$\langle B \rangle=B_{E}+\mu_{0} \langle M \rangle=B_{E}-\mu_{0}|M|  $$
### Magnetic field around the vortex
- For a _vortex line_ with a _core_ at $r=0$, the London equation becomes:
$$\boldsymbol{B}-\lambda^{2}\nabla^{2}\boldsymbol{B}=\boldsymbol{\phi}_{0}\delta^{2}(\boldsymbol{r})$$
- Integrating over a circle of some radius $r$:
$$\begin{align}
\int\boldsymbol{B}\,d^{2}r+\mu_{0}\lambda^{2}\int \nabla\times \boldsymbol{J} \,d^{2}r=\int B\,d^{2}r+\mu_{0}\lambda^{2}(2\pi rJ_{s})=\phi_{0} 
\end{align}$$
- For $r\gg\lambda$, the second term _drops out_:
$$\langle B \rangle =\frac{\phi_{0}}{\pi r_{B}^{2}} $$
- For $r\ll\lambda$, the current term _dominates_:
$$\displaylines{\mu_{0}J_{s}\approx \frac{\phi_{0}}{2\pi\lambda^{2}r}\approx -\frac{\partial B}{\partial r} \\ B(\lambda)\approx 0 \implies B(r)=\frac{\phi_{0}}{2\pi\lambda^{2}}\ln\left( \frac{\lambda}{r} \right)}$$

![[Vortex magnetic field profile.png]]
### The upper critical field
- The _internal field_ $B$ varies _slowly_ within the cylinder as $r_{B}<\lambda$
- Each vortex is assumed to enclose _one flux quantum_:
$$\phi_{0}=\pi r_{B}^{2}B$$

- The _spatial average free energy density_ of a vortex:
$$\int_{\xi}^{r_{B}} \frac{2\pi rdr}{\pi r_{B}^{2}} f_{V}=\text{const.}+\frac{\phi_{0}^{2}}{8\pi^{2}r_{B}^{2}\mu_{0}\lambda^{2}}\ln\left( \frac{r_{B}^{2}}{\xi^{2}} \right)+\frac{(B-B_{E})^{2}}{2\mu_{0}}$$
- By _minimising_ w.r.t. $B$, one can find the _most probable internal field_
$$B=B_{E}- \frac{\phi_{0}}{8\pi\lambda^{2}} \ln\left( \frac{\eta \phi_{0}}{2\pi \xi^{2}B} \right)=B_{E}+\mu_{0}M$$
- $M$ is the _magnetisation_, and $\eta$ is some _constant_ of order unity

- Magnetisation goes to _zero_ when the _flux quantum_ is distributed over a _disc_ of radius $\xi$
- The _vortex cores start to overlap_, and superconductivity _breaks down_ at the _upper critical field_ $B_{c2}$
$$B_{c2}=\frac{\phi_{0}}{2\pi \xi^{2}}$$
- Magnetisation vanishes _continuously_, as a _second order phase transition_

- This gives:
$$B_{c1}B_{c2}=B^{2}_{c}$$
![[Type II superconductivity transitions.png]]

### Critical fields in a superconductor
- Summary of _critical fields_
	- $B_{c}$: the field below which a _homogeneous system_ is superconducting
	- $B_{c1}$: the field above which _vortex formation is favourable_, as long as it is _below_ $B_{c}$
	- $B_{c2}$: the field above which _vortex cores overlap_, and _superconductivity vanishes_
$$\displaylines{B_{c}=\frac{\phi_{0}}{2^{3/2}\pi \xi\lambda}\qquad B_{c2}=\frac{\phi_{0}}{2\pi \xi^{2}} \qquad B_{c1}=\frac{\phi_{0}}{4\pi\lambda^{2}} \\ B_{c1}B_{c2}=B_{c}^{2}}$$
- Relevant lengths and relation to _Ginzburg-Landau parameters_
$$\lambda^{2}=\frac{m}{4\mu_{0}e^{2}n_{s}} \qquad \xi^{2}=\frac{\hbar^{2}}{2m\beta n_{s}}\qquad n_{s}=\frac{|\alpha|}{\beta}$$

- The critical fields are _linear_ in temperature:
$$\alpha(T)=a(T-T_{c})$$
- The Ginzburg-Landau description is only for temperatures _close to_ $T_{c}$

### Condensation energies in Ginzburg-Landau
- The condensation energy is the _total energetic advantage_ of _forming_ a superconductor:
$$\int  \boldsymbol{B}_{E}\cdot d\boldsymbol{M} -d(\boldsymbol{B}_{E}\cdot \boldsymbol{M})=\int  (-\boldsymbol{M})\cdot d\boldsymbol{B}_{E} $$
- For a _homogeneous_ superconductor, the _condensation energy density_ is simply:
$$\frac{B_{c}^{2}}{2\mu_{0}}=\frac{\alpha^{2}}{2\beta}=|\psi_{0}|^{2} \frac{|\alpha|}{2}$$
- One can then interpret $|\alpha|$ as _condensation energy per particle_
	- Matches results above from considering different _critical fields_

- The _condensation energy_ should be the _same_ with or without vortex penetration
- The _equal area construction_:
![[Superconductivity equal area.png]]

### Vortex interactions, transport, and resistivity
- There may be some _transport current_ in the superconductor, such that the _total screening current_ is:
$$\boldsymbol{J}_{s}=\boldsymbol{J}_\text{vortex}+\boldsymbol{J}_\text{tr}$$
- The current experiences a _Lorentz force_
	- Analagous to the _Magnus force_ in fluid dynamics
- The _total force per unit length_
$$f=\int  \boldsymbol{J}_{s}\times \boldsymbol{B} \,d^{2}r=\boldsymbol{J}_\text{tr}\times \int  \boldsymbol{B}\,d^{2}r=\boldsymbol{J}_\text{tr}\times\left( \phi_{0}\hat{B} \right)$$

- For _multiple vortices_, the "transport current" accounts for _current from other vortices_
- This means that _vortices can repel each other_
- Therefore, the _vortex rush_ in the formation of the vortex state will _stop_ at some point
![[Vortices repelling.png|200]]

- _Vortex motion_ implies _power dissipation_
- Power input _per unit volume_, in terms of some _average field_ $B$:
$$P=\frac{fv}{\pi r_{B}^{2}}=J_\text{tr} \frac{\phi_{0}}{\pi r_{B}^{2}}v=J_\text{tr}Bv$$

- This can be linked to some _electric field_ $\varepsilon$:
$$P=\varepsilon J_\text{tr}\implies \varepsilon=Bv$$
- There is some _resistivity due to vortex motion_:
$$\rho=\frac{\varepsilon}{J_\text{tr}}=\frac{Bv}{J_\text{tr}}$$
- Due to _vortex motion_, the _zero resistence state breaks down_

### Vortex flow and pinning
- This can be manipulated by _pinning_ vortices onto _defects_
	- One only has to _pin some fraction_ of the vortices in order to pin the whole lattice from moving

- This pinning also leads to _strong hysteresis_
![[Superconductor hysteresis.png|500]]

- Pinning means _vortices stay inside the superconductor_ and _cannot be injected or extracted completely_:
	- _Permanent magnet_-like behaviour
![[Type II superconductor pinned field.png|400]]

- At some point, for a _strong transport current_, the _pinning force_ is _insufficient_, and _resistivity becomes non-zero_ as the vortices move
- This happens at some _critical current density_ $J_{c}$:
$$J_{c}\sim  \frac{1}{B}$$
### Irreversibility
- For some quasi-2D, _low coherence length superconductors_ (e.g. cuprates), $J_{c}$ can _vanish_ at fields _below_ $B_{c2}$
- The _zero resistance state_ with $J_{c}>0$ is found below some _irreversibility line_ $B_\text{irr}(T)$

- The region between $B_\text{irr}(T)$ and $B_{c2}(T)$ is a _vortex liquid_
![[Vortex liquid phase.png|600]]

# Inhomogeneous superconductors
- The [[#London equations]] imply that an electric field will _accelerate_ supercurrent, but not required to maintain it

## Time dependence and links in zero magnetic field
- Consider a block of superconductor at the London gauge:
$$\varphi'=0 \quad \boldsymbol{A}'=0 \quad \theta'=\text{const.}$$
- Doing a _phase transformation_:
$$\varphi=\varphi'-\dot{\chi} \quad \boldsymbol{A}=\boldsymbol{A}'+\nabla \chi\quad \theta=\theta'+\frac{q}{\hbar}\chi$$
- Suppose $\varphi$ is a _finite, constant potential_ $V$:
$$\dot{\chi}=-V\implies \boldsymbol{A}=\boldsymbol{A}'=0 \quad \theta=\theta'-\varphi\frac{qt}{\hbar}$$
- When _two blocks_ of superconductors are _connected_ with some _potential difference_, there will be _current flow_
	- Typically linked by a _normal conductor_, or sometimes an insulator

- The order parameter will _wind_:
$$\psi(t)\sim\exp\left( -\frac{iqt}{\hbar} V\right)\psi(0)$$
- Meanwhile, checking the [[#Ginzburg-Landau Theory|supercurrent]]:
$$\frac{\partial \boldsymbol{J}_{s}}{\partial t}=\rho_{s}\left( \frac{\hbar}{q}\nabla\dot{\theta}-\dot{\boldsymbol{A}} \right)=\rho_{s}(-\nabla \varphi-\dot{\boldsymbol{A}})=\rho_{s}\boldsymbol{E}$$
- This is the _first London equation_

### Strong and weak links
- Consider the first Ginzburg-Landau equation, in terms of coherence length $\xi$
$$\xi^{2}\nabla^{2}\psi+\psi-\frac{\beta}{|\alpha|}|\psi|^{2}\psi=0\qquad \xi=\sqrt{ \frac{\hbar^{2}}{2m|\alpha|} }$$

- A _strong link_ has $\psi$ wind over a _distance $d$ larger than coherence length_
$$d\gg \xi$$
- Even when the order parameter _winds_ by $2\pi$, the _magnitude_ of $\psi$ is able to change such that _it cannot return to its original state_

- Meanwhile, a _weak link_ has $d\ll \xi$ such that $|\psi|$ does not change significantly
	- It can be viewed as a _tunnelling barrier_ such that the whole system can be described as _one effective condensate wavefunction_ (or the sum of two evanescent waves)

- Consider supercurrent from the [[#Ginzburg-Landau equations]], for a _constant_ $\psi$
$$\frac{\partial}{\partial t}\boldsymbol{J}_{s}=\rho_{s}\left( \frac{\hbar}{q}\nabla\dot{\theta}-\dot{\boldsymbol{A}} \right)=\rho_{s}(-\nabla \varphi- \dot{\boldsymbol{A}})=\rho_{s}\boldsymbol{E}$$
- This is the first [[#London equations|London equation]]
	- An electric field can _kick-start_ the supercurrent, but not sustain it

### Josephson phase relation
- Consider the weak link with $d\ll \xi$ and _potential difference_ $V$
![[Superconductor weak link.png]]
- From the gauge transformation, the _phase drop_ $\Theta=\theta_{1}-\theta_{2}$ obeys:
$$\frac{\partial\Theta}{\partial t}=\frac{qV}{\hbar}=\frac{2\pi V}{\phi_{0}}$$
- From the expression for supercurrent in the absence of $\boldsymbol{A}$:
$$J_{s}=\frac{q\hbar}{m}\mathrm{Im}[-\psi^{*}\nabla \psi]$$
- Replace $\psi$ using the values at either side of the junction:
$$-\psi^{*}\nabla \psi= \frac{\psi_{1}^{*}+\psi_{2}^{*}}{2}\frac{\psi_{1}-\psi_{2}}{d}=\frac{1}{2d}(\psi_{1}\psi_{2}^{*}-\psi_{1}^{*}\psi_{2})$$
- One then gets the _Josephson phase relation_, relating the _supercurrent_ $I_{s}$ to the _phase drop_ $\Theta$, with some _constant_ $I_{J}$
$$I_{s}=I_{J}\sin\Theta$$
- $I_{J}$ is known as the _Josephson critical current_
## Josephson junctions
- Consider the setup of a Josephson junction, _shunted_ with a resistor and capacitor:
$$\displaylines{I=I_{s}+I_{n}=I_{J}\sin\Theta+\frac{V}{R}+C\dot{V} \\ I=I_{J}\sin\Theta+\frac{\phi_{0}}{2\pi R}\dot{\Theta}+\frac{\phi_{0}C}{2\pi}\ddot{\Theta}}$$
- Evolution of $\theta$ can be compared to _forced, damped oscillations_
- The use of a Josephson junction leads to a _unique I-V characteristic_

### DC and AC Josephson effects
- Using the relation between $\Theta$ and $V$, write:
$$\Theta=\Theta_{0}+\frac{2\pi}{\phi_{0}}\int_{0}^{t} V(t') dt' $$
- Considering only a _purely resistive shunted junction_:
$$I(t)=I_{J}\sin\left(\Theta_{0}+\frac{2\pi}{\phi_{0}}\int_{0}^{t}  V(t')\,dt' \right)+\frac{V(t)}{R}$$

- Consider the case of $V=0$, such that:
$$I=I_{s}=I_{J}\sin\Theta_{0}$$
- This is the _DC Josephson effect_, such that _supercurrent flows through the weak link without applied voltage_

- When one applies a _finite DC voltage_ $V$:
$$\Theta=\Theta_{0}+\frac{2\pi V}{\phi_{0}}t\implies I=I_{J}\sin(\Theta_{0}+\omega_{J}t)+\frac{V}{R} \qquad \omega_{J}=\frac{2\pi V}{\phi_{0}}$$
- $\omega_{J}$ is the _Josephson frequency_
- This is the _AC Josephson effect_, where a DC voltage drives an _oscillating super-current_ with a frequency $\propto 1/\phi_{0}$
![[ACDC Josephson.png]]
### Combining AC and DC
- Applying both a DC, and a _radio frequency_ AC
$$\displaylines{\Theta=\Theta_{0}+\omega_{J0}t+\frac{\omega _\text{JRF}}{\omega _\text{RF}}\sin(\omega _\text{RF}t) \\ \omega_{J0}=\frac{2\pi V_{0}}{\phi_{0}} \qquad \omega _\text{JRF}=\frac{2\pi V_\text{RF}}{\phi_{0}}}$$
- This gives the current:
$$I=I_{J}\sin\left( \Theta_{0}+\omega_{J0}t+\frac{\omega _\text{JRF}}{\omega _\text{RF}}\sin(\omega _\text{RF}t) \right)+\frac{V}{R}$$
- Using a _harmonic expansion_:
$$I=I_{J}\sum_{\nu=-\infty}^{\infty} J_{\nu}\left( \frac{\omega _\text{JRF}}{\omega _\text{RF}} \right)\sin[\Theta_{0}+(\omega _\text{J0}+\nu\omega _\text{RF})t]+\frac{V_{0}}{R}+\frac{V_\text{RF}}{R}\cos(\omega _\text{RF}t)$$
- It generates _sideband frequencies_ $\omega_{J0}+\nu\omega _\text{RF}$
- There is a _constant DC part $V_{0}/R$ unless_ the Josephson frequency _matches a multiple of the AC frequency_:
$$\omega_{J0}+\nu\omega _\text{RF}=0\implies \langle I \rangle=J_{\nu}\left( \frac{\omega _\text{JRF}}{\omega _\text{RF}} \right)I_{J}\sin(\Theta_{0})+\frac{V_{0}}{R} $$

- These are _Shapiro spikes_
![[Shapiro spikes.png]]
## Gauge invariant phase with a vector potential
- In the presence of a _magnetic vector potential_ $\boldsymbol{A}$, the _supercurrent_ becomes:
$$J_{s}\propto \nabla\theta+\frac{2\pi }{\phi_{0}}\boldsymbol{A}$$
- Therefore, the _gauge invariant phase drop_ is in fact:
$$\Theta=\theta_{1}-\theta_{2}-\left( \frac{2\pi}{\phi_{0}} \right)\int_{1}^{2} \boldsymbol{A}\cdot d\boldsymbol{s} $$
### Matter wave interferometry
- Consider taking a line integral in a holed superconductor with _weak links_, _sufficiently deep_ such that $J_{s}=0$, similar to the [[#Flux quantisation]] argument
$$\nabla\theta=-\frac{2\pi}{\phi_{0}}\boldsymbol{A}$$
![[Two weak links.png|400]]
- The _phase jump_, allowing for _phase drop in the weak links_, must be $2\pi n$ to keep the wavefunction single-valued:
$$\oint \nabla\theta \,ds=2\pi n=\Theta_{a}-\Theta_{b}+\frac{q}{\hbar}\Phi\implies \Theta_{a}-\Theta_{b}=-2\pi \frac{\Phi}{\Phi_{0}}\,\mathrm{mod}\,2\pi$$
- The _total current_ is then:
$$I_\text{tot}=I_{a}+I_{b}=I_{J}(\sin\Theta_{a}+\sin\Theta_{b})=2I_{J}\cos\left( \frac{\Theta_{a}-\Theta_{b}}{2} \right)\sin\left( \frac{\Theta_{a}+\Theta_{b}}{2} \right)$$
- The current then depends on flux, _oscillating_ with a period of $\phi_{0}$
	- Analagous to _double slit interference_
	- Can be interpreted as _matter wave interference_
$$I_{c}=2I_{J}\left|\cos\left( \frac{\pi \Phi}{\Phi_{0}} \right)\right|$$
![[SQUID interference.png|400]]
- This is used for _SQUIDs_, which can make _high-sensitivity measurements_ of _changes_ in $B,V,I$

# Superfluidity
- Example: $^{4}\ce{ He }$ at $\sim 2\mathrm{K}$, $\ce{ ^{3}He }$ in $\sim \mathrm{mK}$, or cold atoms in $\mathrm{nK}$
	- Observable in helium as there is _high zero point energy_ to overcome _interatomic attraction_, and it _does not solidify at ambient pressure_
- There is a _phase transition_ between the normal liquid and _superfluid_ phase
- Seen in the specific heat anomaly:
![[Superfluid heat anomaly.png|150]]

- In superfluid helium, there is _zero viscosity_

## Behaviour of superflow
- The presence of a phase transition implies the superfluid is a _more ordered phase_ than the normal fluid
- Therefore, like superconductors, one can define a _Ginzburg-Landau order parameter_, still a complex field $\psi(\boldsymbol{r})$

- The system is _charge neutral_, giving a _mass current_
$$\boldsymbol{J}_{s}=\frac{\hbar}{2\mathrm{Im}}(\psi^{*}\nabla \psi-\psi \nabla \psi^{*})=\rho_{s}\frac{\hbar }{m}\nabla\theta=\rho_{s}\boldsymbol{v}_{s} \qquad \psi=\sqrt{ \rho_{s} }\exp(i\theta)$$
- One can define the _superfluid velocity_:
$$\boldsymbol{v}_{s}=\frac{\hbar}{m}\nabla\theta$$
- The flow is _irrotational_:
$$\nabla\times \boldsymbol{v}_{s}=0$$
- From an analogy with [[#Inhomogeneous superconductors|phase in superconductors]] ($\varphi \,dq\to \mu dN$), one gets the _Anderson-Josephson relation_:
$$\frac{\partial\theta}{\partial t}=-\frac{\mu}{\hbar}$$

- Typically, a superfluid has _much lower coherence length_ than a superconductor such that _fluctuations_ play a large role

### Two fluid model
- Model the system as a _superposition_ of the _superfluid_ and a _normal fluid_
	- The normal fluid can be thought of as resulting from _excitations_ such as _phonons_

- From the Gibbs-Duhem relation:
$$d\mu=-\frac{S}{N}dT+\frac{V}{N}dp\implies  \dot{\boldsymbol{v}}_{s}=\frac{1}{m}\left( \frac{S}{N}\nabla T-\frac{V}{N}\nabla p \right)$$
- Any _pressure gradient_ will cause an _acceleration_

- In the presence of _normal fluid/excitations_, $S>0$ such that $\Delta T$ can also cause an acceleration

- One can then _induce osmosis_ using a nonzero $\Delta T$, such as in the fountain effect:
![[Fountain effect.png|300]]

### Flow quantisation
- Take a _holed_ geometry, the _circulation_ $\kappa$ is:
$$\kappa=\oint \boldsymbol{v}_{s}\cdot d\boldsymbol{s}=\frac{\hbar}{m}\oint  \nabla\theta \cdot d\boldsymbol{s}=\frac{\hbar}{m}\Delta\theta=\frac{nh}{m} =n\kappa_{0}$$
- Circulation is _quantised_

- This gives a superfluid velocity around a _vortex_ of one _circulation quantum_:
$$\kappa_{0}=\oint  \boldsymbol{v}_{s}\cdot d\boldsymbol{s} =v_{s}(r)2\pi r\impliedby v_{s}(r)=\frac{\kappa_{0}}{2\pi r}$$

- Unlike superconductors, there is _no screening_, and the vortex core is typically _small compared to superconductors_
	- Indication of _low coherence length_

- Vortices can be generated by _rotating_ a vessel

## Elementary excitations in liquid helium
- Spectrum of excitations from _neutron scattering_
![[Superfluid excitations.png|300]]
- There are _phonons_, which are _linearly dispersed_ at low $k$

- The spectrum will have some _minimum_ near $2\pi/d$, where $d$ is the _average separation_ of $^{4}\ce{ He }$ atoms
- This corresponds to _rotons_, which arise due to _correlations_ as the particles are _near forming a rigid lattice_
	- Can also be thought of as _low-energy vortex rings_

### Superfluidity and critical velocity
- For a particle of mass $M$ _moving through_ the superfluid medium with momentum $P$, it may _dissipate energy by forming excitations_ of energy $\omega_{k}$
$$\frac{P^{2}}{2M}=\frac{(P-\hbar k)^{2}}{2M}+\omega_{k}\implies \omega_{k}=Vk-\frac{\hbar k^{2}}{2M}\approx Vk$$
- If $V$ is _below some critical velocity_, this is impossible as there are _no excitations of low enough energy_, such that the flow is _dissipationless_

## Time-dependent Ginzburg-Landau theory
- Phenomenologically, the order parameter may _evolve_ in a Schrodinger-like equation
$$i\hbar \dot{\psi}=\frac{\delta f}{\delta \psi^{*}}=\alpha \psi+\beta|\psi|^{2}\psi-\gamma \nabla^{2}\psi$$
- Setting this to _zero_ gives the Ginzburg-Landau equations

- Suppose there is some _time-dependent fluctuation_ near the equilibrium:
$$\psi=\psi_{0}+\varepsilon\qquad |\psi_{0}|^{2}=-\frac{\alpha}{\beta}$$
- From the equations:
$$\begin{align}
i\hbar \dot{\varepsilon}&=(\alpha+2\beta|\psi_{0}|^{2}-\gamma \nabla^{2})\varepsilon+\beta|\psi_{0}|^{2}\varepsilon^{*} \\ i\hbar \dot{\varepsilon}^{*}&=(\alpha+2\beta|\psi_{0}|^{2}-\gamma \nabla^{2})\varepsilon^{*}+\beta|\psi_{0}|^{2}\varepsilon
\end{align}$$

- Use a _Fourier representation_:
$$\displaylines{\varepsilon=\sum_{k}e^{ikr}\varepsilon_{k} \qquad \varepsilon^{*}=\sum_{k}e^{ikr}\varepsilon_{-k}^{*} \\ \Delta=\beta|\psi_{0}|^{2} \qquad \alpha=-\Delta \\ i\hbar\dot{\varepsilon}_{k}=(\Delta+\gamma k^{2})\varepsilon_{k}+\Delta\varepsilon_{-k}^{*}}$$
- There is _mixing_ between $\varepsilon_{k}$ and $\varepsilon_{-k}^{*}$

- Let each of them evolve as a _normal mode_:
$$\displaylines{\varepsilon_{k}(t)=\varepsilon_{k}(0)\exp(-i\omega_{k}t) \\ \begin{align}
\hbar\omega_{k}\varepsilon_{k}&=(\Delta+\gamma k^{2})\varepsilon_{k}+\Delta\varepsilon_{-k}^{*} \\ -\hbar\omega_{k}\varepsilon_{-k}^{*}&=(\Delta+\gamma k^{2})\varepsilon_{-k}^{*}+\Delta\varepsilon_{k}
\end{align} \\ \hbar\omega_{k}\boldsymbol{\varepsilon}=\pmatrix{\Delta+\gamma k^{2} & \Delta \\ -\Delta & -(\Delta+\gamma k^{2})}\boldsymbol{\varepsilon}}$$

- This gives the _normal mode frequencies_:
$$\hbar\omega_{k}=\sqrt{ 2\gamma\Delta k^{2}+\gamma^{2}k^{4} }$$
- As expected, it is a _Goldstone mode_

# Microscopic theory of condensates
- The BCS wavefunction describes the _microscopics_ of electron pairing
- Using [[Theories of Quantum Matter#Second quantisation and correlations|Second quantisation]]

## Coherent states
- The BCS state is related to the _coherent state_, an eigenstate of the _lowering_ operator
	- A _superposition_ of _Fock states_
$$a\ket{\psi}=\psi \ket{\psi}\implies \psi=|\psi|e^{i\theta}\qquad \ket{\psi}=\exp\left( -\frac{1}{2}|\psi|^{2}+\psi a^{\dagger} \right)\ket{0}  $$
- It is a _Poisson distribution_ distributed over _Fock states_
- The _average particle number_ and _variance_:
$$\bar{n}=|\psi|^{2}\qquad \mathrm{Var}(n)=\Delta n^{2}=\bar{n}\implies \frac{\Delta n}{\bar{n}}=\frac{1}{\sqrt{ \bar{n} }}$$
- In the _thermodynamic limit_, the variance shrinks, and _number distribution_ becomes _sharply peaked_

- It is a state of _minimal uncertainty_:
	- Proof: use $x=(a+a^{\dagger})/2$ and $p=(a-a^{\dagger})/(2i)$
$$\displaylines{\langle a \rangle=\langle x \rangle+i\langle p \rangle=|\psi|e^{i\theta} \\\Delta x=\Delta p=\frac{1}{2}\qquad \Delta x\Delta p=\frac{1}{4}}$$

- One can also find that $n$ and $\theta$ are _conjugate variables_:
$$-i \frac{\partial}{\partial\theta}\ket{\psi}=n\ket{\psi} \qquad n=-i \frac{\partial}{\partial\theta} \qquad [n,\theta]=i  $$
- There is then a _number-phase uncertainty relation_
$$\Delta n\Delta\theta=\frac{1}{4}$$
## Effective two-body Hamiltonian
- A Hamiltonian with _two-body contact interactions_:
$$H=\sum_{k}\varepsilon_{k}a^{\dagger}_{k}a_{k}+\frac{g}{2V}\sum_{k,k',q}a^{\dagger}_{k+q}a^{\dagger}_{k'-q}a_{k'}a_{k}\quad,\quad g<0$$
- $g$ is some _mean field average_ of the interaction
### Mean field approximation
- Take a _mean-field approximation_ for operators $A,B$
	- The _double counting correction_: $\langle A \rangle\langle B \rangle$
$$\langle AB \rangle= \langle A \rangle B+A\langle B \rangle  -\mathrm{DCC}  $$
- This comes from assuming the _fluctuations_ $\delta A$ and $\delta B$ are _uncorrelated_:
$$\langle \delta A\delta B \rangle=0 $$
- For _four operator terms_, there are _three separate decoupling schemes_ that manifest _different interactions_

- Bogoliubov decoupling:
$$a_{4}^{\dagger}a_{3}^{\dagger}a_{2}a_{1}\approx\langle a_{4}^{\dagger}a_{3}^{\dagger} \rangle a_{2}a_{1}+a_{4}^{\dagger}a_{3}^{\dagger}\langle a_{2}a_{1} \rangle  $$
- Exchange interaction:
$$\pm a_{4}^{\dagger}a_{2}a_{3}^{\dagger}a_{1}\approx \pm \langle a_{4}^{\dagger}a_{2} \rangle a_{3}^{\dagger}a_{1}\pm a_{4}^{\dagger}a_{2}\langle a_{3}^{\dagger}a_{1} \rangle $$
- Direct interaction:
$$a_{4}^{\dagger}a_{1}a_{3}^{\dagger}a_{2}\approx \langle a_{4}^{\dagger}a_{1} \rangle a_{3}^{\dagger}a_{2}+a_{4}^{\dagger}a_{1}\langle a_{3}^{\dagger}a_{2} \rangle  $$
- These correspond to different terms from [[QFT#Wick's Theorem|Wick's Theorem]]
### Weakly interacting Bose gas
- The Hamiltonian, taking into account the _chemical potential_:
$$H-\mu N=\sum_{k}(\varepsilon_{k}-\mu)a^{\dagger}_{k}a_{k}+\frac{g}{2V}\sum_{k,k',q}a^{\dagger}_{k+q}a^{\dagger}_{k'-q}a_{k'}a_{k}$$

- Introduce the parameters:
	- $\xi_{k}$: the _Hartree-Fock energy_, relative to _chemical potential_
	- For the latter approximation, $a_{0}\sim~ \sqrt{ N_{0} }$
$$ \xi_{k}=\varepsilon_{k}^{\text{H-F}}-\mu\approx\varepsilon_{k}+n_{0}g \qquad \delta=\frac{g}{V}\sum_{k} \langle a_{-k}a_{k} \rangle\approx n_{0}g$$
- Then with _mean field decoupling_, only considering _zero momentum pairs_:
$$H_\text{eff}=\frac{1}{2} \sum_{k}\left[\xi_{k}(a^{\dagger}_{k}a_{k}+a^{\dagger}_{-k}a_{-k})+\delta (a_{k}^{\dagger}a^{\dagger}_{-k}+a_{-k}a_{k})\right]$$
### BCS Hamiltonian
- For _fermions_, accounting for _spins_, with Bogoliubov decoupling:
$$H_\text{BCS}=\sum_{k}\left[ \xi_{k}(a_{k\uparrow}^{\dagger}a_{k\uparrow}+a^{\dagger}_{-k\downarrow}a_{-k\downarrow})-\Delta(a^{\dagger}_{k\uparrow}a^{\dagger}_{-k\downarrow}+a_{-k\downarrow}a_{k\uparrow}) \right]$$
- The _BCS gap parameter_:
$$\Delta=\frac{|g|}{V}\sum_{k}\langle a_{-k\downarrow}a_{k\uparrow} \rangle >0$$
### Bogoliubov transformation
- For a single-particle Hamiltonian of the form:
$$h\equiv \xi(a^{\dagger}a+b^{\dagger}b)+\delta(a^{\dagger}b^{\dagger}+ba)$$
- One can then _define_:
	- Upper(lower) sign: bosons(fermions)
$$\alpha=ua+vb^{\dagger} \qquad \beta=ub\pm va^{\dagger}$$
- Find $u$ and $v$ such that:
$$h=E(\alpha ^{\dagger}\alpha+\beta ^{\dagger}\beta)+\eta$$
- $E$ is the _excitation energy_ for particles created by $\alpha ^{\dagger},\beta ^{\dagger}$

- For this to occur, $u$ and $v$ must satisfy:
	- $E$ is the _positive solution_ for the quadratic equation
$$\displaylines{u^{2}=\frac{1}{2}\left( 1+ \frac{\xi}{E} \right)\qquad v^{2}=\mp\frac{1}{2}\left( 1-\frac{\xi}{E} \right)\qquad uv=\frac{\delta}{2E}\qquad \\ \eta=\mp (\xi-E) \qquad E^{2}=\xi^{2}\mp\delta^{2} \qquad E\geq 0}$$

- Bosons:
$$\displaylines{a=a_{k} \qquad b=a_{-k}\qquad H_\text{eff}=\frac{1}{2}\sum_{k} h_{k} \\ h=\pmatrix{a^{\dagger} &b} \pmatrix{\xi&\delta\\\delta&\xi}\pmatrix{a\\b^{\dagger}}-\xi=\pmatrix{\alpha ^{\dagger}&\beta}\pmatrix{E&0\\0&E}\pmatrix{\alpha\\\beta ^{\dagger}}-\xi \\ E^{2}=\xi^{2}-\delta^{2}}$$
- Fermions:
$$\displaylines{a=a_{k\uparrow} \qquad b=a_{-k\downarrow} \qquad H_\text{eff}=\frac{1}{2}\sum_{k}h_{k} \\ h=\pmatrix{a^{\dagger}&b}\pmatrix{\xi&-\Delta\\-\Delta&-\xi}\pmatrix{a\\ b^{\dagger}}+\xi=\pmatrix{\alpha ^{\dagger}&b}\pmatrix{E&0\\0&-E}\pmatrix{\alpha \\ \beta ^{\dagger}}+\xi \\ E^{2}=\xi^{2}+\Delta^{2}}$$
## Excitations in BECs and in BCS

### Excitation spectrum in BECs
- For the _Bose liquid_:
$$E_{k}=\sqrt{ \varepsilon_{k}(\varepsilon_{k}+2n_{0}g) }$$
- Limits:
$$\displaylines{\varepsilon_{k}\ll n_{0}g\implies E_{k}=\hbar \sqrt{ \frac{n_{0}g}{m} }k \\ \varepsilon_{k}\gg n_{0}g\implies E_{k}=\frac{\hbar^{2}k^{2}}{2m}}$$
- At _low wavenumber_, the spectrum is _linear_ with _speed of sound_:
$$c=\sqrt{ \frac{n_{0}g}{m} }$$
- The creation of an _excitation_:
$$\alpha_{k}^{\dagger}=u_{k}a_{k}^{\dagger}+v_{k}a_{-k}$$

### Condensate depletion in BECs
- The _condensate occupancy_ $n_{0}=\langle a_{0}^{\dagger}a_{0} \rangle$ must _satisfy_ $n_{0}\gg 1$ to make a BEC
- Using the fact that there are _no $\alpha$ or $\beta$ excitations_ in the ground state
$$n_{0}=v_{0}^{2}=\frac{1}{2}\left( \frac{\xi_{0}}{E_{0}} -1\right)$$
- For there to be a _condensate_, $E_{0}\ll \xi_{0}$, so the _ground state_ must have zero energy
	- Justifies $\delta\approx n_{0}g$ such that $E_{0}\approx 0$

- One can calculate:
$$n-n_{0}=\sum_{k\neq 0}v_{k}^{2}=\frac{1}{3\pi^{2}}\left( \frac{mc}{\hbar} \right)^{3}$$

- _Interaction_ causes _condensate depletion_
	- Atomic gases: $n_{0}/n \sim 0.9$, $\ce{ He-II }: n_{0}/n <0.1$
	- Not due to thermal excitations
- The _excited particles_ are _part of the coherent ground state_ along with the condensate
### Density fluctuations in BECs
- Consider the _density operator_ in reciprocal space:
$$\rho_{q}=\frac{1}{\sqrt{ V }}\sum_{k}a^{\dagger}_{k-q}a_{k}\to \frac{1}{\sqrt{ V }}(a^{\dagger}_{-q}a_{0}+a_{0}^{\dagger}a_{q})\to \sqrt{ n_{0} }(a^{\dagger}_{-q}+a_{q})\sim \alpha_{q}$$
- The _low level excitation_ of wave-vector $q$ is therefore interpreted as a _density fluctuation_ of the corresponding wavelength

- The [[#Superfluidity and critical velocity|Landau critical velocity]] becomes _finite_, matching the _speed of sound_
	- Above critical velocity: generation of _density fluctuations_ which _dissipate energy_
	- The repulsive ineraction _reduces the density of states of excitations_ to allow superfluidity

- The excitations correspond to _Goldstone modes_ due to symmetry breaking

- Bogoliubov theory with _weak interactions_ does not predict _rotons_
### BCS fermion excitation spectrum
- A _gapped spectrum_:
$$E_{k}=\sqrt{ \xi_{k}^{2}+\Delta^{2} }\qquad \xi_{k}=\varepsilon^{\text{HF}}_{k}-\mu$$
![[BCS gapped spectrum.png|300]]

- The _fermionic excitation_ is:
$$\alpha ^{\dagger}_{k\sigma}=u_{k}a^{\dagger}_{k\sigma}+v_{k}a_{-k,-\sigma}$$
- Analagous to the Bogoliubov Bose gas, $v_{k}^{2}$ corresponds to _normal electron occupation_ 
	- Even at _zero temperature_, the _Fermi sea becomes destabilised_
![[BCS excitation.png|300]]
- It is a _coherent superposition_ of _adding_ an electron to $(k,\sigma)$ and _removing_ an electron at $(-k,-\sigma)$
	- When _well above_ the Fermi surface, it is _adding a bare electron_ into the vacuum at $(k,\sigma)$
	- When _well below_ the Fermi surface, it is _removing a bare electron_ from the Fermi sea at $(-k,-\sigma)$

- It has a _well-defined spin_, but an _indeterminate particle number/charge_
	- At $\xi_{k}=\mu$, there is _zero charge_ 

### BCS gap equation
- An equation for $\Delta(T)$
$$\begin{align}
\Delta&=\frac{|g|}{V}\sum_{k}\langle a_{-k\downarrow}a_{k\uparrow} \rangle \\ &=-\frac{|g|}{V}\sum_{k}u_{k}v_{k}(1-\langle \alpha ^{\dagger}\alpha \rangle -\langle \beta ^{\dagger}\beta \rangle )_{k} \\ \Delta&=\frac{|g|}{V}\sum_{k} \frac{\Delta}{2E_{k}}(1-2f(E_{k}))
\end{align}$$
- For a _finite temperature_, the gap function must then satisfy:
	- $N(\xi)$: _density of states_ per spin per unit volume
	- $\varepsilon_{c}$: _energy cut-off_ of $\mu$
$$1=|g|\int_{0}^{\varepsilon_{c}}  \frac{N(\xi)d\xi}{\sqrt{\xi^{2}+\Delta(T)^{2}  }}\tanh\left( \frac{\sqrt{ \xi^{2}+\Delta(T)^{2} }}{2k_{B}T} \right) $$
- Assume the density of states is _constant_ within $\sim \varepsilon_{c}$ of $\mu$

- Setting $T=0$:
$$1=|g| \int_{0}^{\varepsilon_{c}}\frac{N(\xi)d\xi}{\sqrt{ \xi^{2}+\Delta(0)^{2} }} \approx N(0)|g|\sinh^{-1}\left( \frac{\varepsilon_{c}}{\Delta(0)} \right)$$
- One can also find a _critical temperature_ where $\Delta=0$
$$1=|g| \int_{0}^{\varepsilon_{c}} \frac{N(\xi)d\xi}{\xi}\tanh\left( \frac{\xi}{2k_{B}T_{c}} \right) $$
- In the limit of _weak binding_ $N(0)|g|\ll 1$
$$\Delta(T=0)\approx 2\varepsilon_{c}\exp\left( -\frac{1}{N(0)|g|} \right)\approx 1.76k_{B}T_{c}$$

- From $f(E_{k})$, one can also calculate the corresponding _entropy_ and _heat capacity_
![[Conventional superconductor properties.png]]
## Ginzburg-Landau and BCS Theory
### Ginzburg-Landau order parameter from BCS theory
- The _particle-particle_ field:
$$\Psi(r)=\psi_{\downarrow}(\boldsymbol{r})\psi_{\uparrow}(\boldsymbol{r})=\frac{1}{\sqrt{ V }}\sum_{\boldsymbol{q}}\Psi_{\boldsymbol{q}}\exp(i\boldsymbol{q}\cdot \boldsymbol{r}) \qquad \Psi_{\boldsymbol{q}}=\frac{1}{\sqrt{ V }}\sum_{\boldsymbol{k}}a_{\boldsymbol{q}-\boldsymbol{k}\downarrow}a_{\boldsymbol{k}\uparrow}$$
- The _BCS order parameter_ is proportional to the $q=0$ Fourier component of $\Psi(\boldsymbol{r})$
- The _Ginzburg-Landau_ order parameter also allows for _spatial variation_

- From this, a suitable order parameter is a _coarse-grained average_ of the field:
$$\psi_{s}(\boldsymbol{r})\propto \langle \psi_{\downarrow}(\boldsymbol{r})\psi_{\uparrow}(\boldsymbol{r}) \rangle_\text{coarse-grained} $$

### Coherence length from BCS theory
- The _modification_ to excitation spectrum via _gap formation_ is significant for a _range_ around $k_{F}$
$$\delta k\sim \frac{\Delta}{\hbar (\partial E/\partial k)}=\frac{\Delta}{\hbar v_{F}}$$
- The relevant _lengthscale_:
$$\delta x\sim \frac{\hbar}{\delta k}$$
- This can be identified with the [[#Ginzburg-Landau Theory|Ginzburg-Landau coherence length]] $\xi$

### Ginzburg-Landau parameters from BCS Theory
- Compare [[#Condensation energies in Ginzburg-Landau|condensation energies]] in both Ginzburg-Landau and BCS theory
	- BCS theory: condensation energy is of order $\Delta$ times the _density of electrons near Fermi energy with energies modified_, which is $n_{e}(\Delta/\varepsilon_{F})$
$$\displaylines{n_{e}\sim \frac{|\alpha|}{\beta}\times 2 \\  \Delta\left( n_{e} \frac{\Delta}{\varepsilon_{F}} \right) \sim \frac{\alpha^{2}}{2\beta}}$$

- A more rigorous calculation gives:
$$\xi\approx \frac{\hbar v_{F}}{\pi\Delta}=\frac{2\varepsilon_{F}}{\pi k_{F}\Delta}$$

- One can then relate the _critical fields_ to microscopic parameters:
$$B_{c2}=\frac{\phi_{0}}{2\pi \xi^{2}}=\frac{\pi \phi_{0}k_{F}^{2}\Delta^{2}}{8\varepsilon_{F}^{2}}$$
- The Ginzburg-Landau parameters from BCS theory:
$$|\alpha|=\frac{\hbar^{2}}{2m\xi^{2}}=\frac{\pi^{2}\Delta^{2}}{8\varepsilon_{F}} \qquad \beta=\frac{2|\alpha|}{n_{e}}\qquad m=2m_{e}$$
## Intepretations of BCS Theory
- One can _build_ the BCS wavefunction from _pair wavefunctions_
$$\Psi= \mathcal{A}\{\varphi(\mathbf{r}_{1}-\mathbf{r}_{2};\sigma_{1}\sigma_{2})\varphi\dots\}$$
- The BCS state as _combining coherent states_ for each wavenumber:
	- There are _no second order terms_ from the exponential, then one must _normalise_
$$\displaylines{\exp(s_{\boldsymbol{k}}a^{\dagger}_{\boldsymbol{k}\uparrow}a^{\dagger}_{-\boldsymbol{k}\downarrow})\ket{\text{VAC}} =(1+s_{\boldsymbol{k}}a^{\dagger}_{\boldsymbol{k}\uparrow}a^{\dagger}_{\boldsymbol{k}\downarrow})\ket{\text{VAC}} \\ u_{\boldsymbol{k}}=\frac{1}{\sqrt{ 1+|s_{\boldsymbol{k}}|^{2} }}\qquad v_{\boldsymbol{k}}=\frac{s_{\boldsymbol{k}}}{\sqrt{ 1+|s_{\boldsymbol{k}}|^{2} }} \\ \ket{\Psi _\text{BCS}}=\prod_{\boldsymbol{k}}(u_{\boldsymbol{k}}+v_{\boldsymbol{k}}a^{\dagger}_{\boldsymbol{k}\uparrow}a^{\dagger}_{-\boldsymbol{k}\downarrow})\ket{\text{VAC}}  }$$
- From a _variational approach_ w.r.t. the BCS Hamiltonian, one gets the _mean field parameters_ back once $E_\text{BCS}$ is minimised
$$\displaylines{E_\text{BCS}=\braket{ \Psi _\text{BCS} |H|\Psi _\text{BCS}  } \\ H_\text{red}=\sum_{\boldsymbol{k}}\varepsilon_{\boldsymbol{k}}a^{\dagger}_{\boldsymbol{k}}a_{\boldsymbol{k}}-\frac{|g|}{V}\sum_{\boldsymbol{k},\boldsymbol{k}'}a^{\dagger}_{\boldsymbol{k}'\uparrow}a^{\dagger}_{-\boldsymbol{k}'\downarrow}a_{-\boldsymbol{k}\downarrow}a_{\boldsymbol{k}\uparrow}}$$

- For $\xi\gg d$, where $d$ is the _characteristic electron spacing_ (e.g. lattice constant), this describes _pairings in $k-$space_

- This is _in contrast to real-space pairing_ $\xi\ll d$
	- Some _cuprate high $T_{c}$ superconductors_

### Comparison to Stoner ferromagnetism
- In _Stoner ferromagnetism_, there is an _on-site repulsion_ resulting in magnetisation
$$\displaylines{E_{k\sigma}=\xi_{k}-\frac{\sigma}{2}\Delta _\text{St}\\ \Delta _\text{St}=U(n_{\uparrow}-n_{\downarrow})=\frac{U}{V}\sum_{k}[f(E_{\boldsymbol{k}\uparrow})-f(E_{\boldsymbol{k}\downarrow})]=\frac{U}{V}\sum_{\boldsymbol{k}}\frac{f(E_{\boldsymbol{k}\uparrow})-f(E_{\boldsymbol{k}\downarrow})}{E_{\boldsymbol{k}\uparrow}-E_{\boldsymbol{k}\downarrow}}\Delta _\text{St}}$$
- The [[#BCS gap equation]]:
$$\displaylines{E_{\boldsymbol{k}}=\sqrt{ \xi_{\boldsymbol{k}}^{2}+\Delta^{2} } \\ \Delta _\text{BCS}=\frac{|g|}{V}\sum_{\boldsymbol{k}}\frac{1-2f(E_{\boldsymbol{k}})}{2E_{\boldsymbol{k}}}\Delta _\text{BCS}=\frac{|g|}{V}\sum_{\boldsymbol{k}}\frac{1-f(E_{-\boldsymbol{k}\downarrow})-f(E_{\boldsymbol{k}\uparrow})}{E_{\boldsymbol{k}\uparrow}+E_{\boldsymbol{k}\downarrow}}\Delta _\text{St}}$$

- At $T_{c}$ where $E_{k}\approx \xi_{k}$, the BCS gap equation can be obtained from the Stoner gap equation via the _particle-hole transformation_:
$$(-\xi_{\boldsymbol{k}\downarrow})\to \xi_{-\boldsymbol{k}\downarrow} \qquad f(\xi_{\boldsymbol{k}\downarrow})\to 1-f(\xi_{-\boldsymbol{k}\downarrow})$$
- Similar to Stoner ferromagnetism, superconductivity _spontaneously emerges_

- Higgs phenomenon: _transverse_ currents are _gapped_

### Pairing as avoidance
- Interactions between the electrons can be thought of as _induced interactions_
	- One electron (an "emitter") will _induce_ a change in the surrounding field
	- The second electron (the "absorber") will experience this change, resulting in an _attraction_

- Take a simplified model, with some _constant_ $g$ being the _particle-field interaction_, where the field has some _impulse response_ $\chi(\boldsymbol{r},t)$
- The _interaction potential_ between two particles, induced by one moving at velocity $u$:
$$\displaylines{\mathcal{V}_\text{ret}(\boldsymbol{r},t)=\int V_\text{ret}(\boldsymbol{r}-\boldsymbol{r}',t-t')\delta(\boldsymbol{r}'-\boldsymbol{u}t')\,d\boldsymbol{r}'\,dt' \\ V_\text{ret}(\boldsymbol{r}-\boldsymbol{r}',t-t')=-g^{2}\chi _\text{ret}(\boldsymbol{r}-\boldsymbol{r}',t-t')}$$
- $V_\text{ret}$ is known as the _retarded impulse interaction_
![[ret.png]]

- Electron-electron _attraction_ can only occur when there is a _finite separation/avoidance in time and/or space_
	- The _pair wave-function_ should be _zero_ wherever there is significant _repulsion_

- Time avoidance pairing:
	- e.g. a _retarded interaction_ due to the _screening cloud of a moving charge_ (the [[#Bardeen-Pines effective electron-electron interaction|Bardeen-Pines model]])
![[Time avoidance pairing.png|500]]
- Space avoidance
	- e.g. induced _spin-spin interactions_ (such as _superexchange_)
![[Spatial avoidance.png|500]]
# Conventional superconductivity beyond BCS Theory
## Generalisation of gap parameter
- The gap equation in BCS theory, with a singular $\Delta$ parameter coming from _mean field decoupling_:
$$\Delta=-\frac{1}{V}\sum_{\boldsymbol{k}'}g\Delta \frac{1-2f(E_{\boldsymbol{k}'})}{2E_{\boldsymbol{k}'}}$$

- Generalise to a $k-$_dependent_ interaction, maintaining _singlet pairing_
- With some _kernel_ $K_{kk'}$ for transitions from $(\boldsymbol{k},-\boldsymbol{k})$ to $(\boldsymbol{k}',-\boldsymbol{k}')$
$$\Delta_{k}=-\sum_{k'}K_{kk'}\Delta_{k'} \frac{1-2f(E_{k'})}{2E_{k'}}\qquad E_{\boldsymbol{k}}=\sqrt{ \xi_{\boldsymbol{k}}^{2}+|\Delta_{\boldsymbol{k}}|^{2} }$$

- One can also generalise the model to be _spin-dependent_:
$$\displaylines{H=\sum_{\boldsymbol{k}\sigma}\varepsilon_{\boldsymbol{k}}a^{\dagger}_{\boldsymbol{k}\sigma}a_{\boldsymbol{k}\sigma}+\sum_{\boldsymbol{k}\boldsymbol{k}'}\sum_{\alpha\beta\gamma\delta}V_{\boldsymbol{k}\boldsymbol{k}'}^{\alpha\beta\gamma\delta}a^{\dagger}_{\boldsymbol{k}'\alpha}a^{\dagger}_{-\boldsymbol{k}'\beta}a_{-\boldsymbol{k}\gamma}a_{\boldsymbol{k}\delta} \\ \Delta_{\boldsymbol{k}}^{\alpha\beta}=\sum_{\boldsymbol{k}'}V^{\alpha\beta\gamma\delta}_{\boldsymbol{k}\boldsymbol{k}'}\langle a_{-\boldsymbol{k}'\gamma}a_{\boldsymbol{k}'\delta} \rangle }$$
### Conventional and unconventional singlet pairing
- In _conventional singlet superconductors_, $\Delta_{\boldsymbol{k}}$ has the _same sign over the Fermi surface_
	- Its sign should still _change with magnitude_ of $\boldsymbol{k}$ to reduce repulsion
- In _unconventional singlet superconductors_, it can change sign over the Fermi surface

- Denoting the _width_ of the energy gap $\Delta_{k}/(\hbar v_{F})$:
![[convcentional and unconventional singlets.png|450]]
## Bardeen-Pines effective electron-electron interaction
- The _effective interaction_ is taken as the _real part_ of the [[#Pairing as avoidance|retarded impulse response]]

- Take _jellium_, with the [[Solids#Thomas-Fermi screening|Thomas-Fermi approximation]]
- The _Bardeen-Pines_ model: a _test charge_ in a _jellium_ will _induce_ a _dipolar field_
![[Bardeen-Pines interaction.png]]
- The pairing interaction:
	- Consisting of an _instantaneous screened Coulomb repulsion_, and an _electron-phonon mediated attraction_
	- Here, $\nu_{\boldsymbol{q}}$ is the _longitudinal phonon frequency_
	- $\gamma_{\boldsymbol{q}}\leq 1$ is a _coupling parameter_
$$V_{\boldsymbol{q}\omega}=\frac{e^{2}}{\epsilon_{0}} \frac{1}{q^{2}+k_\text{TF}^{2}}\left( 1-\frac{\gamma_{\boldsymbol{q}}\nu_{\boldsymbol{q}}^{2}}{\nu_{\boldsymbol{q}}^{2}-\omega^{2}} \right)$$

- It is _attractive_ for $\omega<\nu_{\boldsymbol{q}}$, and can lead to _pairing_
	- The _gap function_ should _change in sign_ w.rt. energy

### Relation to the gap equation kernel
- $V_{\boldsymbol{q}\omega}$ describes a _dynamical interaction_
- Its effect is still included in the _kernel_ $K_{\boldsymbol{k}\boldsymbol{k}'}$

- $\boldsymbol{q}$ and $\omega$ represent _momentum_ and _energy_ transfer in the _effective_ electron-electron interaction
- From transforming the [[AQCMP#Electron-phonon interactions|Frohlich Hamiltonian]]:
	- Applies _near the Fermi surface_
$$K^{\text{Frohlich}}_{\boldsymbol{k}\boldsymbol{k}'}=V(\boldsymbol{q}=\boldsymbol{k}'-\boldsymbol{k},\hbar\omega=\xi_{\boldsymbol{k}'}-\xi_{\boldsymbol{k}})$$

## Generalised Bardeen-Pines interaction
- Instead of jellium, consider a _dielectric medium_
- Result:
![[BCS vs Bardeen-Pines.png|600]]

### Contribution from polarised dielectric medium
- A _test charge_ will induce _polarisation_ in the _dielectric medium_
![[Bardeen-Pines polarisation.png|400]]
- The total field is caused by both the _free test charge_ and the _bound charges_
- Consider the dielectric to be _homogeneous_
	- As the interaction is _long range_, the lattice effects are _averaged out_

- Gauss' Law in a _linear dielectric_:
$$\displaylines{\nabla\cdot \boldsymbol{E}=\frac{1}{\epsilon_{0}}(\rho+\rho_{b})=\frac{1}{\epsilon_{0}} (\rho-\nabla\cdot \boldsymbol{P}) \\ E=-\nabla \varphi \qquad \boldsymbol{P}=\epsilon_{0}\chi \boldsymbol{E}}$$
- Taking the Fourier transform:
$$\varphi_{\boldsymbol{q}\omega}=\frac{\rho_{\boldsymbol{q}\omega}}{\epsilon_{0}q^{2}(1+\chi_{\boldsymbol{q}\omega})}$$
- Take a [[Solids#Lorentz dipole oscillator model|Lorentz oscillator]], with _no damping_, the _real part_ of the susceptibility: 
	- $\Omega_{p}$ is the _plasma frequency_ of the dielectric
	- $\Omega_{t\boldsymbol{q}}$ is the _transverse frequency_ of the medium
$$\chi_{\boldsymbol{q}\omega}=\frac{\Omega_{p}^{2}}{\Omega_{t\boldsymbol{q}}^{2}-\omega^{2}}$$
- The effective interaction can then be written as:
$$\displaylines{V_{\boldsymbol{q}\omega}=\frac{e^{2}}{\epsilon_{0}q^{2}(1+\chi_{\boldsymbol{q}\omega})}=\frac{e^{2}}{\epsilon_{0}q^{2}} \left( 1-\gamma_{\boldsymbol{q}} \frac{\Omega_{l\boldsymbol{q}}^{2}}{\Omega_{l\boldsymbol{q}}^{2}-\omega^{2}} \right) \\ \gamma_{\boldsymbol{q}}=1-\frac{\Omega_{t\boldsymbol{q}}^{2}}{\Omega_{t\boldsymbol{q}}^{2}} \qquad \Omega_{l\boldsymbol{q}}^{2}=\Omega_{p}^{2}+\Omega_{t\boldsymbol{q}}^{2}}$$
- It is a combination of the _direct potential_ and the potential due to _induced polarisation_ by the test charge

- $\gamma_{\boldsymbol{q}}$, the _coupling parameter_, tends to $1$ for $\Omega_{t\boldsymbol{q}}\ll\Omega_{l\boldsymbol{q}}$

### Contribution from charge carriers
- In the _absence of free charge carriers_, the interaction becomes _singular_ at low $q$
- The free charge carriers will _screen_ the interaction
	- Typically due to _doped itinerant charge carriers_
- If one takes the _Thomas-Fermi approximation_, screening is given by:
$$q^{-2}\to (q^{2}+k_\text{TF}^{2})^{-1}$$
![[Generalised Bardeen-Pines.png|300]]

- More rigourous analysis gives an additional term given by the [[AQCMP#Lindhard dielectric function|Lindhard function]]
- The mobile charge carriers have some other _plasma frequency_ $\omega_{p}$, as well as a _transverse frequency_ $\omega_{t\boldsymbol{q}}=v_{F}q/\sqrt{ 3 }$
![[Bardeen-Pines transverse.png|250]]
- For $\omega\ll\omega_{t\boldsymbol{q}}$ or $\omega\gg \omega_{t\boldsymbol{q}}$, also accounting for a _core contribution_, $\chi$ reduces to:
$$\chi_{\boldsymbol{q}\omega}=\chi_{\infty}+\frac{\Omega_{p}^{2}}{\Omega_{t\boldsymbol{q}}^{2}-\omega^{2}}+\frac{\omega_{p}^{2}}{\omega_{t\boldsymbol{q}}^{2}-\omega^{2}}$$
- The _total effective interaction_ accounting for both _bound charges_ and _itinerant carriers_
$$V_{\boldsymbol{q}\omega}=\frac{e^{2}}{\epsilon_{0}q^{2}(1+\chi _{\boldsymbol{q}\omega})}=\frac{e^{2}}{\epsilon_{0}q^{2}}\left( 1-\frac{\gamma_{1\boldsymbol{q}}\omega_{1\boldsymbol{q}}^{2}}{\omega_{1\boldsymbol{q}}^{2}-\omega^{2}}-\frac{\gamma_{2\boldsymbol{q}}\omega_{2\boldsymbol{q}}^{2}}{\omega_{2\boldsymbol{q}}^{2}-\omega^{2}} \right)$$
- $\omega_{1,2}$ are taken as the _lower and upper longitudinal frequencies_, with corresponding couplings $\gamma_{1,2}$

### Back to the Bardeen-Pines limit
- The _Bardeen-Pines limit_ is taking limits to reduce the surroundings to _jellium_:
$$\Omega_{t\boldsymbol{q}}\ll\omega\ll\omega_{t\boldsymbol{q}}\quad,\quad \chi_{\infty}=0 \implies \chi_{\boldsymbol{q}\omega}=-\frac{\Omega_{p}^{2}}{\omega^{2}}+\frac{\omega_{p}^{2}}{\omega_{t\boldsymbol{q}}^{2}}$$
- The effective interaction is then:
$$\displaylines{V_{\boldsymbol{q}\omega}=\frac{e^{2}}{\epsilon_{0}q^{2}}\left( 1-\gamma_{2\boldsymbol{q}}-\frac{\gamma_{1\boldsymbol{q}}\omega_{1\boldsymbol{q}}^{2}}{\omega_{1\boldsymbol{q}}^{2}-\omega^{2}} \right) \\ \gamma_{1\boldsymbol{q}}=1-\gamma_{2\boldsymbol{q}}=\frac{q^{2}}{q^{2}+k_\text{TF}^{2}} \qquad k_\text{TF}^{2}=\frac{3\omega_{p}^{2}}{v_{F}^{2}}=\frac{2N(0)e^{2}}{\epsilon_{0}} \qquad \omega_{1\boldsymbol{q}}=\frac{\Omega_{p}q}{k_\text{TF}}}$$
- The _lower longitudinal frequency_ is taken, with both _direct_ and _induced_ interactions reduced by the _same screening factor_

- For $\nu_{\boldsymbol{q}}=\omega_{\boldsymbol{q}}$, this gives the _Bardeen-Pines interaction_
	- Attractive for $\omega<\nu_{\boldsymbol{q}}$
	- It is _weakened_ for increasing $k_\text{TF}$

## Quantum treatment of mediated electron interactions
- Due to _virtual emission and reabsorption_, from _second order perturbation theory_, the _ground state energy_ should shift
	- $\xi=\varepsilon-\mu$
$$\Delta E_{G}=\sum_{\boldsymbol{k},\boldsymbol{k}'} \frac{|w_{\boldsymbol{q}}|^{2}f_{k}(1-f_{\boldsymbol{k}'})}{\xi_{\boldsymbol{k}}-(\xi_{\boldsymbol{k}'}+\hbar \nu_{\boldsymbol{q}})}$$
- Here, $w_{\boldsymbol{q}}$ is a _transition amplitude_ for the electron-phonon process
- $f_{\boldsymbol{k}}$ is the _Fermi distribution_
![[Electron phonon perturbation.png|250]]

### Shift in quasiparticle energy
- From [[AQCMP#Quasiparticle energy expansion|Fermi liquid theory]], the _shift in quasi-particle energy_ for wavenumber $\boldsymbol{p}$ is:
	- Quasi-particle energy: energy of _adding_ a particle to state $\boldsymbol{p}$
$$\Delta \xi_{\boldsymbol{p}}=\frac{\partial}{\partial f_{\boldsymbol{p}}}\Delta E_{G}=\sum_{\boldsymbol{k}'} \frac{|w_{\boldsymbol{q}}|^{2}(1-f_{\boldsymbol{k}'})}{\xi_{\boldsymbol{p}}-(\xi_{\boldsymbol{k}'}+\hbar \nu_{\boldsymbol{q}})}-\sum_{\boldsymbol{k}}\frac{|w_{\boldsymbol{q}}|^{2}f_{\boldsymbol{k}}}{\xi_{\boldsymbol{k}}-(\xi_{\boldsymbol{p}}+\hbar \nu_{\boldsymbol{q}})}$$
- The two terms represent _shifts_ due to:
	- Transitions from $\boldsymbol{p}$ to _unoccupied states_ $\boldsymbol{k}'=\boldsymbol{k}+\boldsymbol{q}$ to create another, higher energy quasiparticle (a _polaron_)
	- The _blocking of transitions_ from _occupied states_ $\boldsymbol{k}$ to $\boldsymbol{p}$ which could have lowered ground state energy via thje e-ph interaction
![[superconductor quasiparticle.png|400]]

- Changes to quasiparticle energy leads to _mass renormalisation_:
![[Phonon quasiparticle mass renormalisation.png|400]]

### Change to quasiparticle interactions
- The _Landau quasiparticle interaction function_ also has two contributions:
	- $\boldsymbol{q}=\boldsymbol{k}'-\boldsymbol{k}$ and $\hbar\omega=\xi_{\boldsymbol{k}'}-\xi_{\boldsymbol{k}}$
$$\begin{align}
\Delta \mathcal{f}_{\boldsymbol{p}\boldsymbol{p}'}=\frac{\partial}{\partial f_{\boldsymbol{p}'}}\Delta \xi_{\boldsymbol{p}}&=- \frac{|w_{\boldsymbol{q}}|^{2}}{\xi_{\boldsymbol{p}}-(\xi_{\boldsymbol{p}'}+\hbar \nu_{\boldsymbol{q}})}- \frac{|w_{\boldsymbol{q}}|^{2}}{\xi_{\boldsymbol{p}'}-(\xi_{\boldsymbol{p}}+\hbar \nu_{\boldsymbol{q}})} \\
&=\frac{2|w_{\boldsymbol{q}}|^{2}\hbar \nu_{\boldsymbol{q}}}{(\hbar \nu_{\boldsymbol{q}})^{2}-(\xi_{\boldsymbol{p}}-\xi_{\boldsymbol{p}'})^{2}} \\
&=\frac{2|w_{\boldsymbol{q}}|^{2}}{\hbar \nu_{\boldsymbol{q}}} \frac{\nu_{\boldsymbol{q}}^{2}}{\nu_{\boldsymbol{q}}^{2}-\omega^{2}}
\end{align}$$
- This represents the _total forward scattering amplitude_
	- Accounting for both _direct_ and _exchange_ terms

- This must be _negative_ of the induced electron-electron interaction, giving:
	- $V$ is the _volume_ of the system
$$\displaylines{\Delta \xi_{\boldsymbol{k}}=\sum_{\text{occ }\boldsymbol{k}'}\Delta f_{\boldsymbol{k}\boldsymbol{k}'}=-\frac{1}{V}\sum_{\text{occ }\boldsymbol{k}'}V^{\text{ind}}_{\boldsymbol{q}\omega} \\ V^{\text{ind}}_{\boldsymbol{q}\omega}=- \frac{2V|w_{\boldsymbol{q}}|^{2}}{\hbar \nu_{\boldsymbol{q}}} \frac{\nu_{\boldsymbol{q}}^{2}}{\nu_{\boldsymbol{q}}^{2}-\omega^{2}}}$$
- The _total effective interaction_, including screened Coulomb interaction:
$$V_{\boldsymbol{q}\omega}=V_{\boldsymbol{q}}^{c}+V^{\text{ind}}_{\boldsymbol{q}\omega} \qquad V_{\boldsymbol{q}}^{c}=\frac{e^{2}}{\epsilon_{0}(q^{2}+k_\text{TF}^{2})}$$
- This agrees with Bardeen-Pines theory if:
$$|w_{\boldsymbol{q}}|^{2}=\frac{e^{2}}{2V\epsilon_{0}} \frac{\hbar \nu_{\boldsymbol{q}}}{q^{2}+k_\text{TF}^{2}}$$
### Mass renormalisation
- Renormalisation of the _Fermi velocity_ $\hbar k/m$ via parameter $\lambda$, due to shift in $\xi_{k}$
$$\frac{1}{\hbar}\frac{\partial}{\partial k}(\xi_{k}+\Delta \xi_{k})=\frac{1}{\hbar}\left( \frac{\partial \xi_{k}}{\partial k}+\frac{\partial\Delta \xi _{k}}{\partial \xi_{k}} \frac{\partial \xi_{k}}{\partial k} \right)= \frac{1}{\hbar}\frac{1}{1+\lambda} \frac{\partial \xi_{k}}{\partial k}$$
- Approximating $(1+\lambda)^{-1}\approx 1-\lambda$
$$\displaylines{\Delta \xi_{\boldsymbol{k}}=-\frac{1}{V}\sum_{\text{occ }\boldsymbol{k}'}V^{\text{ind}}_{\boldsymbol{q}\omega} \\ \lambda=-\frac{\partial\Delta \xi_{k}}{\partial \xi_k}=\int_{\text{occ. }\boldsymbol{k}'}\, \frac{d^{3}k'}{(2\pi)^{3}} \frac{dV^{\text{ind}}_{\boldsymbol{q}\omega}}{\hbar d\omega(k)}}$$
- Take the limit where the _maximum phonon energy_ $\varepsilon_{c}\ll\varepsilon_{F}$, and the _wavenumber dependence_ of $V_{\boldsymbol{q}\omega}$ near the Fermi surface can be _ignored_
- This can then be _transformed_ into an integral of energies _near the Fermi surface_:
$$\lambda=N(0)\langle V^{\text{ind}}_{\boldsymbol{q},\omega=0} \rangle_\text{FS} \qquad\langle  \rangle_\text{FS}= \int_{0}^{2k_{F}} \frac{q\,dq}{2k_{F}^{2}}$$
#### $k$ and $\omega$ integrals near the Fermi surface
- The integral over $k'-$space can be converted into a _surface integral_ and one over energy
$$\int \frac{d^{3}k'}{(2\pi)^{3}}=\int \frac{d\xi_{k'}}{\hbar \nu_{k'}}\int dS$$
- The measure can be converted for a _fixed_ $\xi_{k}$ and $\xi_{k'}$:
$$\displaylines{d^{3}k'=2\pi\,d(-\cos\theta)\,(k')^{2}dk' \\ q^{2}=|\boldsymbol{k}-\boldsymbol{k}'|^{2}=k^{2}+(k')^{2}-2kk'\cos\theta \\ d(-\cos\theta)=\frac{q\,dq}{kk'}}$$
- Then for $\xi_{k'}\ll\varepsilon_{F}$
$$\int_\text{occ} \frac{d^{3}k'}{(2\pi)^{3}}=N(0)\int_{-\varepsilon_{c}}^{0} \hbar\,d\omega \int_{0}^{2k_{F}}\frac{q\,dq}{2k_{F}^{2}}$$

### Quasiparticle renormalisation
- Going back to the Hamiltonian:
$$H-\mu N=\sum_{\boldsymbol{k}}\xi_{\boldsymbol{k}}a^{\dagger}_{\boldsymbol{k}}a_{\boldsymbol{k}}+\frac{g}{2V}\sum_{\boldsymbol{k}\boldsymbol{k}'\boldsymbol{q}}a^{\dagger}_{\boldsymbol{k}+\boldsymbol{q}}a^{\dagger}_{\boldsymbol{k}'-\boldsymbol{q}}a_{\boldsymbol{k}'}a_{\boldsymbol{k}}$$
- The electron operators can be expressed in terms of _quasiparticle operators_ $\alpha,\alpha ^{\dagger}$
$$a_{\boldsymbol{k}}^{\dagger}=z^{1/2}\alpha ^{\dagger}_{\boldsymbol{k}}+\dots$$
- This gives the Hamiltonian as:
$$H-\mu N=\sum_{\boldsymbol{k}}z\xi_{\boldsymbol{k}}\alpha ^{\dagger}_{\boldsymbol{k}}\alpha_{\boldsymbol{k}}+ \frac{gz^{2}}{V}\sum_{\boldsymbol{k}\boldsymbol{k}'\boldsymbol{q}}\alpha ^{\dagger}_{\boldsymbol{k}+\boldsymbol{q}}\alpha ^{\dagger}_{\boldsymbol{k}'-\boldsymbol{q}}\alpha_{\boldsymbol{k}'}\alpha_{\boldsymbol{k}}+\dots$$
- $z$ is a _quasiparticle renormalisation factor_, also related to _mass renormalisation_
	- Assumed to be _independent_ of $k$
$$z=\frac{1}{1+\lambda}$$
- This leads to a _reduction of Fermi velocity_ by $z$ and therefore _enhancement of density of states_ $N(0)$ by a factor of $(1+\lambda)$
- Also, there is an _attenuation_ of the _coupling_ ($|g|$ in the BCS gap equation) by $1/(1+\lambda)^{2}$

- There is then an _enhancement_ of the exponential factor in $T_{c}$

# Electron-phonon coupling
- Treat e-ph interactions in more detail to find the _interaction vertex_ $w_{q}$

## e-ph interaction for a single band and monoatomic lattice

### Derivation of the e-ph interaction vertex
- A Hamiltonian dependent on _electron coordinate_ $\boldsymbol{r}_{i}$ and _ion coordinate_ $\boldsymbol{R}_{i}$
$$\displaylines{H_\text{e-ph}=\sum_{i,l}U(\boldsymbol{r}_{i}-\boldsymbol{R}_{l})=\int d\boldsymbol{r}\,d\boldsymbol{R}\, n(\boldsymbol{r})U(\boldsymbol{r}-\boldsymbol{R})N(\boldsymbol{R})=\sum_{\boldsymbol{q}}n_{-\boldsymbol{q}}U_{\boldsymbol{q}}N_{\boldsymbol{q}} \\ n(\boldsymbol{r})=\sum_{i}\delta(\boldsymbol{r}-\boldsymbol{r}_{i}) \qquad N(\boldsymbol{R})=\sum_{i}\delta(\boldsymbol{R}-\boldsymbol{R}_{i}) \\ U_{\boldsymbol{q}}=\int d\boldsymbol{s}\,U(\boldsymbol{s})e^{i\boldsymbol{q}\cdot \boldsymbol{s}} \quad n_{\boldsymbol{q}}= \frac{1}{\sqrt{ V }}\int d\boldsymbol{r}\,n(\boldsymbol{r})e^{i\boldsymbol{q}\cdot \boldsymbol{r}} \quad N_{\boldsymbol{q}}= \frac{1}{\sqrt{ V }}\int d\boldsymbol{R}\,N(\boldsymbol{R})e^{i\boldsymbol{q}\cdot \boldsymbol{R}}}$$
- Given an ion is _displaced_ from the lattice point $\boldsymbol{R}_{0l}$ by $\boldsymbol{u}_{l}$:
$$N_{\boldsymbol{q}}=\frac{1}{\sqrt{ V }} \sum_{l}e^{i\boldsymbol{q}\cdot \boldsymbol{R}_{l}}\approx \frac{1}{\sqrt{ V }}\sum_{l}\exp(i\boldsymbol{q}\cdot \boldsymbol{R}_{0l})(1+i\boldsymbol{q}\cdot \boldsymbol{u}_{l})=N_{0\boldsymbol{q}}+N_{1\boldsymbol{q}}$$
- Only _longitudinal phonons_ contribute in this model
	- Transverse phonons contribute in _higher orders_

- Going to _first order in displacement_, the interaction Hamiltonian is:
$$\displaylines{N_{1\boldsymbol{q}}=i\boldsymbol{q} \cdot \frac{\boldsymbol{u}_{\boldsymbol{q}}}{V} \qquad \boldsymbol{u}_{\boldsymbol{q}}=\sqrt{ V }\sum_{l}\exp(i\boldsymbol{q}\cdot \boldsymbol{R}_{0l})\boldsymbol{u}_{l} \\ u_{\boldsymbol{q}+\boldsymbol{G}}=u_{\boldsymbol{q}} \qquad n_{\boldsymbol{q}}=n_{-\boldsymbol{q}}^{*} \\ H_\text{e-ph}^{(1)}=\sum_{\boldsymbol{q}}n_{-\boldsymbol{q}}U_{\boldsymbol{q}}N_{1\boldsymbol{q}}=\frac{i}{V}\sum_{\boldsymbol{q}}n^{*}_{\boldsymbol{q}}U_{\boldsymbol{q}}\boldsymbol{q}\cdot u_{\boldsymbol{q}}=\frac{i}{V}\sum_{\boldsymbol{Q},\boldsymbol{G}}n^{*}
_{\boldsymbol{Q}+\boldsymbol{G}}U_{\boldsymbol{Q}+\boldsymbol{G}}(\boldsymbol{Q}+\boldsymbol{G})\cdot u_{\boldsymbol{Q}+\boldsymbol{G}}}$$
- Here, $\boldsymbol{Q}$ is _in the 1st BZ_ and $\boldsymbol{G}$ is a _reciprocal lattice vector_

- Then consider only $\boldsymbol{G}=0$ and _second quantise_
	- $a_{\boldsymbol{Q}}$: _fermion_ operators
	- $b_{\boldsymbol{Q}}$: _boson_ operators
	- _Ignoring spin degeneracy_

- The _electron density_:
$$n_{\boldsymbol{Q}}^{\dagger}= \frac{1}{\sqrt{ V }}\sum_{\boldsymbol{k}}a^{\dagger}_{\boldsymbol{k}+\boldsymbol{Q}}a_{\boldsymbol{k}}$$
- Considering the _longitudinal phonons_ as a _quantum harmonic oscillator_ of frequency $\nu_{\boldsymbol{Q}}$
	- $N=N_{s}/V$, where $N_{s}$ is the _number of lattice sites_
$$u_{\boldsymbol{Q}}=\sqrt{ \frac{N\hbar}{2M\nu_{\boldsymbol{Q}}} }(b_{\boldsymbol{Q}}+b^{\dagger}_{-\boldsymbol{Q}})$$
- This gives the _interaction Hamiltonian_ for _longitudinal phonons_
$$H_\text{e-ph}^{(1)}=\sum_{\boldsymbol{k},\boldsymbol{Q}}w_{\boldsymbol{Q}}a^{\dagger}_{\boldsymbol{k}+\boldsymbol{Q}}a_{\boldsymbol{k}}(b_{\boldsymbol{Q}}+b_{-\boldsymbol{Q}}^{\dagger}) \qquad w_{\boldsymbol{Q}}=iQ\sqrt{ \frac{N\hbar}{2M\nu_{\boldsymbol{Q}}}U_{\boldsymbol{Q}} }$$
- The interaction parameter is $\propto |\boldsymbol{Q}|$, as it is a _Goldstone mode_

- $|w_{Q}|^{2}$ gives the [[#Generalised Bardeen-Pines interaction|Bardeen-Pines model]] if $U_{Q}$ is of the _Thomas-Fermi form_ with ionic charge $Ze\to e$ and in the limit $q\ll k_\text{TF}$

### Canonical transformation of the Frohlich Hamiltonian
- The Frohlich Hamiltonian:
$$H=\sum_{\boldsymbol{k}}\varepsilon_{\boldsymbol{k}}a^{\dagger}_{\boldsymbol{k}}a_{\boldsymbol{k}}+\sum_{\mathbf{Q}} \hbar \nu_{\boldsymbol{Q}}b_{\boldsymbol{Q}}^{\dagger}b_{\boldsymbol{Q}}+\sum_{\boldsymbol{k},\boldsymbol{Q}}w_{\boldsymbol{Q}}a^{\dagger}_{\boldsymbol{k}+\boldsymbol{Q}}a_{\boldsymbol{k}}(b_{\boldsymbol{Q}}+b_{-\boldsymbol{Q}}^{\dagger})$$
- Then use an _operator transformation_ to make an _effective electron-electron interaction term_, while _preserving (anti)commutation relations_

- Analagous to _completing the square_, the boson field can be [[AQCMP#Phonon mediation of e-e interactions|transformed]] to give the _effective electron Hamiltonian_:
$$H^{\text{eff}}_\text{int}=\frac{1}{2}\sum_{\boldsymbol{k},\boldsymbol{p},\boldsymbol{q}} |w_{\boldsymbol{q}}|^{2} \left( \frac{1}{\varepsilon_{\boldsymbol{k}}-\varepsilon_{\boldsymbol{k}-\boldsymbol{q}}-\hbar \nu_{\boldsymbol{q}}}+\frac{1}{\varepsilon_{\boldsymbol{p}+\boldsymbol{q}}-\varepsilon_{\boldsymbol{p}}-\hbar \nu_{\boldsymbol{q}}} \right)a^{\dagger}_{\boldsymbol{p}+\boldsymbol{q}}a^{\dagger}_{\boldsymbol{k}-\boldsymbol{q}}a_{\boldsymbol{k}}a_{\boldsymbol{p}}$$
![[Effective e-e interaction ph.png]]
- This suggests an [[#Generalisation of gap parameter|interaction kernel]]
	- The kernel describes a _dynamic interaction_ while the above approach is _static_
	- The approaches agree for $\xi_{\boldsymbol{k}},\xi_{\boldsymbol{k}'}\ll\epsilon_{D}$
$$K_{\boldsymbol{k}\boldsymbol{k}'}=V(\boldsymbol{q}=\boldsymbol{k}-\boldsymbol{k}',\hbar\omega=\xi_{\boldsymbol{k}'}-\xi_{\boldsymbol{k}})$$

- For _pairing_, restrict $\boldsymbol{p}=-\boldsymbol{k}$
	- With _spin degeneracy_, pre-factor of $1/2$ drops out
$$H^{\text{eff}}_\text{pair}=-\frac{1}{2}\sum_{\boldsymbol{k},\boldsymbol{q}} |w_{\boldsymbol{q}}|^{2} \frac{2\hbar \nu_{\boldsymbol{q}}}{(\hbar \nu_{\boldsymbol{q}})^{2}-(\varepsilon_{\boldsymbol{k}+\boldsymbol{q}}-\varepsilon_{\boldsymbol{k}})^{2}} a^{\dagger}_{-\boldsymbol{k}+\boldsymbol{q}}a^{\dagger}_{\boldsymbol{k}-\boldsymbol{q}}a_{\boldsymbol{k}}a_{-\boldsymbol{k}}$$
## BCS gap equation with Frohlich kernel
- At $T=T_{c}$, the [[#Generalisation of gap parameter|generalised gap equation]] is _linearised_
	- Include both the _Frohlich kernel_ $V_{\boldsymbol{q}\omega}^\text{ind}$ and the _Coulomb repulsion_ $V_{\boldsymbol{q}}^{c}$
$$\Delta_{\boldsymbol{k}}=-\int \frac{d^{3}k'}{(2\pi)^{3}} \frac{V^{\text{ind}}_{\boldsymbol{q}\omega}+V^{c}_{\boldsymbol{q}}}{2\xi_{\boldsymbol{k}'}}\Delta_{\boldsymbol{k}'}\tanh\left( \frac{\xi_{\boldsymbol{k}'}}{2k_{B}T_{c}} \right) \qquad \boldsymbol{q}=\boldsymbol{k}'-\boldsymbol{k}\quad \hbar\omega=\xi_{\boldsymbol{k}'}-\xi_{\boldsymbol{k}}$$
- This is an _eigenvalue equation_ for the vector $\Delta_{\boldsymbol{k}}$ as the operator is _linear_
- At $T=T_{c}$, the _eigenvalue_ is $1$

- The eigenvector can _vary in magnitude and sign_ with $\boldsymbol{k}$ to _minimise total energy_

- Take the approximation where $\Delta$ is _constant_ for $|\xi_{\boldsymbol{k}}|\ll\epsilon_{c}\ll\epsilon_{F}$ and _zero elsewhere_
- [[#$k$ and $ omega$ integrals near the Fermi surface|Transforming the integral]], the gap equation becomes
	- $\lambda$ is the [[#Mass renormalisation|mass renormalisation parameter]] where $m^{*}=(1+\lambda)m$
$$\displaylines{1=(\lambda-\mu_{c}) \int_{0}^{\epsilon_{c}} \frac{d\xi'}{\xi'}\tanh\left( \frac{\xi'}{2k_{B}T_{c}} \right)\implies T_{c}\approx \frac{\epsilon_{c}}{k_{B}}\exp\left( - \frac{1}{\lambda-\mu_{c}} \right) \\ \lambda=N(0)\langle |V_{\boldsymbol{q}\omega=0}^\text{ind}| \rangle_\text{FS} \qquad \mu_{c}=N(0)\langle V_{\boldsymbol{q}}^{c} \rangle_\text{FS}  }$$
- Comparing to the [[#BCS gap equation]], the interaction parameter $|g|$ is replaced with $(\lambda-\mu_{c})$ which includes the effect of both _induced attraction_ and _Coulomb repulsion_
- In the _Bardeen-Pines model_, $\lambda\approx \mu_{c}$ and $T_{c}$ is vanishingly small ($\Delta$ should not have been taken as a constant)
	- The effect of repulsion is _over-estimated_

### Retardation effect and critical temperature
- Let the _induced interaction_ be non-zero in range $-\epsilon_c'<\xi <\epsilon_{c}'$
- Meanwhile let the _repulsive interaction_ be in range $-\epsilon_{c}<\xi<\epsilon_{c}$
- Then take $\Delta$ as a _positive constant_ up to $\epsilon_{c}$ and a _negative constant_ up to $\epsilon_{c}'>\epsilon_{c}$
![[Gap equation retardation effect.png]]
- This gives the same expression for $T_{c}$ but with:
$$\mu^{*}=\frac{\mu_{c}}{1+\mu_{c}\ln(\epsilon_{c}'/\epsilon_{c})}<\mu_{c}$$
- Typically, from _Debye theory_, $\epsilon_{c}\sim\epsilon_{D}$, and from [[#Eliashberg-MacMillan Theory]], $\epsilon_{c}'\approx \epsilon _F$

- The _frequency space sign change_ in $\Delta$ corresponds to the _Cooper pair state in real space_ moving _away from the repulsive core towards the retarded attractive part_ of the total interaction potential
	- This is the _retardation effect_ (of the Cooper pair state, _in addition to_ retardation in the potential)
- In _weak coupling_, combined with the [[#Quasiparticle renormalisation|quasiparticle renormalisation factor]], the transition temperature is:
$$T_{c}\approx \frac{\epsilon_{c}}{k_{B}} \exp\left( -\frac{1+\lambda}{\lambda-\mu^{*}} \right)$$
- Typically, $\mu^{*}<\lambda$

- From the Bardeen-Pines model:
$$\lambda=N(0)\langle V^\text{ind}_{\boldsymbol{q}\omega=0} \rangle=\frac{N(0)e^{2}}{4\epsilon_{0}k_{F}^{2}} \int_{0}^{4k_{F}^{2}} \frac{dq^{2}}{q^{2}+k_\text{TF}^{2}}=\frac{k_\text{TF}^{2}}{8k_{F}^{2}}\ln\left( 1+\frac{4k_{F}^{2}}{k_\text{TF}^{2}} \right)\approx \mu_{c}$$
- _Without_ retardation, $T_{c}$ vanishes
- For $\epsilon_{c}'/\epsilon_{c}\approx \epsilon_{F}/\epsilon_{D}\approx 10^{2}$, tjhis gives $\lambda\approx 0.5$ and $\mu^{*}\approx{0}.15$
- In this model, $\lambda$ is _independent_ of $\epsilon_{c}$ while $\mu^{*}$ is _weakly dependent_ on $\epsilon_{c}$, such that $T_{c}$ will _rise monotonically_ with $\epsilon_{c}$
	- $\epsilon_c$ is some _average_ over phonon modes which is _smaller than Debye energy_

### McMillan formula for critical temperature
- _Eliashberg-McMillan theory for stronger couplings_ and numerical calculation gives the _McMillan formula_, as a _correction_ from the above
	- $\theta_{D}$ is an _effective Debye temperature_ given by some averaging
$$\displaylines{\theta_{D}\ll T_{F}=\frac{\epsilon_{F}}{k_{B}} \qquad \lambda\lesssim 2 \qquad \mu^{*} \lesssim 0.15 \\ T_{c}\approx \frac{\theta_{D}}{1.45}\exp\left( -\frac{1.04(1+\lambda)}{\lambda-\mu^{*}(1+0.62\lambda)} \right)}$$

# Unconventional superconductivity
- Superconducting phases are often observed _around the quantum phase transition between magnetic and Fermi liquid states_
- Evidence of _magnetically mediated superconductivity_
	- Can occur on the border of both _anti-ferromagnetic_ and _ferromagnetic_ states
![[Magnetic order and superconductivity.png|500]]

- As $d-$electron bands have _broader energy bands_, they can exhibit _higher_ $T_{c}$

## Cuprates
- Cuprates have common $\ce{ CuO_{2} }$ _planes_, separated by _plane of other atoms_, which act as _spacers and electron reservoirs_ in order to _modify carrier conentration in cuprate planes_

- The electrons can be modelled by a _single tight-binding $d_{x^{2}-y^{2}}$ band_ in a _square lattice_ near _half-filling_
	- High Coulomb repulsion, such that a _Mott insulator_ is favourable
- Effect of spacer/doping planes in cuprates:
![[Cuprate doping.png]]

- The _Fermi surface_ is a _cylinder_ about the _point_ $(\pi,\pi)$ in the BZ
- The _gap function_ $\Delta_{\boldsymbol{k}}$ has _nodal points_ 
![[d wave Fermi surface.png|500]]
- The _gap function_ has $d-$wave symmetry:
$$\displaylines{\Delta_{\boldsymbol{k}}(T=0)=-\sum_{\boldsymbol{k}'} \frac{K_{\boldsymbol{k}\boldsymbol{k}'}\Delta_{\boldsymbol{k}'}}{2E_{\boldsymbol{k}'}} \\ E_{\boldsymbol{k}}=\sqrt{ (\epsilon_{\boldsymbol{k}}-\epsilon_{F})^{2}+|\Delta_{\boldsymbol{k}}|^{2} } \qquad \Delta_{\boldsymbol{k}}=\Delta(\cos k_{x}-\cos k_{y})=\Delta \eta_{\boldsymbol{k}}}$$
- Phase diagram in $\ce{ La_{2}CuO_{4} }$:
	- Transforms into a _d-wave superconducting state_ with a _maximum_ $T_{c}$ at $\sim 0.2$ holes per $\ce{ CuO_{2} }$ square
	- Antiferromagnetic (AF), pseudo-gap (PG), and charge density wave (CDW) phases
![[La2CuO4 phases.png|400]]

### Possible mechanism for superconductivity on the border of a Mott transition
- e-ph interactions alone _cannot account fully_ for superconductivity in the cuprates
- Accounting for $d-$wave gap symmetry requires _spin-spin_ interactions between carriers

- Considering _spin singlet pairing_ interactions between _quasiparticles of anti-parallel spin_ in a _square lattice_ gives either $k_{x}^{2}+k_{y}^{2}$ or $k_{x}^{2}-k_{y}^{2}$ gap parameter
![[d wave singlet interaction.png]]

### The t-J model
- Take a _Hubbard Hamiltonian_ for the $d_{x^{2}-y^{2}}$ tight binding band
- Account for _nearest neighbour hopping_ and _Coulomb repulsion_
$$H=\sum_{\boldsymbol{k}\sigma}\epsilon_{\boldsymbol{k}}n_{\boldsymbol{k}\sigma}+U\sum_{i}n_{i\downarrow}n_{i\uparrow} \qquad \epsilon_{\boldsymbol{k}}=-2t(\cos k_{x}+\cos k_{y})=-t\gamma_{k}$$

- Consider a _nearly half full band_ with $U\gg t$
- The _Schrieffer-Wolff canonical transformation_, a _low-energy description_ (well below $U$)
$$H_\text{red}=P\left(\sum_{\boldsymbol{k}\sigma}\epsilon_{\boldsymbol{k}}n_{\boldsymbol{k}\sigma}+J\sum_{\langle ij \rangle }\left( \boldsymbol{S}_{i}\cdot \boldsymbol{S}_{j}-\frac{1}{4} \right)\right)$$
- It is _projected_ onto states with _no double occupancy_ with operator $P$

- Here, $J$ is the _Anderson kinetic superexchange_ parameter:
$$J=\frac{4t^{2}}{U}$$
- For _anti-parallel spins_, there can be _virtual hopping_
- From second order perturbation theory with $t\ll U$ (_strong coupling_ limit), this will _lower energy_ by $-t^{2}/U$, to give the latter term of the Hamiltonian
	- The _increase in repulsion_ is _offset_ by a _greater decrease in kinetic energy_
	- In contrast to [[#Quantum treatment of mediated electron interactions|weak coupling]] where the increase in kinetic energy is offset by the decrease in potential energy

- _Projection_ onto single occupancy states _renormalises_ the exchange and hopping
- Consider an _effective Hamiltonian_ with parameters $t_\text{eff}$ and $J_\text{eff}$
![[t-J model parameters.png|600]]
### d-wave gap parameter from t-J model
- The gap equation at zero temperature:
$$\displaylines{\Delta_{\boldsymbol{k}}=-\sum_{\boldsymbol{k}'} \frac{K_{\boldsymbol{k}\boldsymbol{k}'}\Delta_{\boldsymbol{k}'}}{2E_{\boldsymbol{k}'}} \\ E_{\boldsymbol{k}}=\sqrt{ (\epsilon_{\boldsymbol{k}}-\epsilon_{F})^{2}+|\Delta_{\boldsymbol{k}}|^{2} } \qquad \epsilon_{\boldsymbol{k}}=-2t_\text{eff}(\cos k_{x}+\cos k_{y})=-t_\text{eff}\gamma_{\boldsymbol{k}}}$$
- The _kernel_ is the _Fourier transform_ of the nearest neighbour interaction
	- $N_{s}$: number of _atomic sites_
$$\displaylines{V_{\boldsymbol{q}}=\frac{1}{N_{s}}\sum_{j}V_{0,j}\exp(-i\boldsymbol{q}\cdot \boldsymbol{r}_{j})=-\frac{3J_\text{eff}/4}{N_{s}}\gamma_{\boldsymbol{q}} \\ K_{\boldsymbol{k}\boldsymbol{k}'}=- \frac{3J_\text{eff}/4}{N_{s}}\gamma_{\boldsymbol{k}-\boldsymbol{k}'}}$$
- From _substitution_, there is a _d-wave solution_:
$$\Delta_{\boldsymbol{k}}=\Delta(\cos k_{x}-\cos k_{y})=\Delta \eta_{\boldsymbol{k}}$$
- The _amplitude_ must satisfy:
$$1=\frac{3J_\text{eff}/4}{N_{s}}\sum_{\boldsymbol{k}} \frac{\eta_{\boldsymbol{k}}^{2}}{2\sqrt{ (-t_\text{eff}\gamma_{\boldsymbol{k}}-\epsilon_{F})^{2}+\Delta^{2}\eta_{\boldsymbol{k}}^{2} }}$$

### t-J model reormalisation
- The effective parameters are determined by _projecting_ eigenstates out in the _strong coupling limit_
- From Gutzwiller Mean Field Theory:
$$\displaylines{t_\text{eff}=g_tt=\frac{2x}{1+x}t \qquad J_\text{eff}=g_{J}J=\left( \frac{2}{1+x} \right)^{2}J \\ x=1-\langle n_{i\downarrow}+n_{i\uparrow} \rangle }$$
- $x$ is the _probability_ that there is an _empty neighbouring site_
- $t_\text{eff}$ must scale with $x$, then require that $t_\text{eff}\to t$ as $x\to 1$, as _double occupancy vanishes_
- As $x\to 0$, the _effective bandwidth_ vanishes as there are _no empty sites_ in the Mott state (at half filling)

- Given the renormalised parameters (from doping), one can _numerically calculate_ $\Delta$
- Example: $\ce{ Bi_{2}Sr_{2}CaCu_{2}O_{8+\delta} }$
![[t-J model gap.png]]

- $\Delta$ gives the _energy scale for pairing_ (not necessarily superconductivity)
- At small $x$, _small electronic bandwidth_ and _superfluid phase stiffness/coherence_ will _vanish_, therefore $T_{c}$ is _suppressed_
	- There will be _strong fluctuations of local particle-particle order parameter_
- $k_{B}T_{c}$ will scale as $g_{t}\Delta$ instead