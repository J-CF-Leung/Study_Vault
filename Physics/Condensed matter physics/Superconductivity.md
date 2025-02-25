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
- From _Drude theory_:
$$\left( \frac{\partial}{\partial t}+\frac{1}{\tau} \right)\boldsymbol{j}=\left( \frac{\partial}{\partial t}+\frac{1}{\tau} \right)\left( \frac{ne^{2}}{m} \right)\boldsymbol{E}$$
- For perfect conductivity, $\tau\to \infty$
	- $\Lambda=(ne^{2}/m)^{-1}$
$$\Lambda \frac{\partial}{\partial t}\boldsymbol{j}=\boldsymbol{E}$$
- One can have a _constant current without any electric field_

- Then from Maxwell's equations:
$$\displaylines{\frac{\partial \boldsymbol{B}}{\partial t}=-\nabla\times \boldsymbol{E}=-\Lambda \nabla\times \frac{\partial}{\partial t}\boldsymbol{j} \\ \boldsymbol{B}=-\Lambda \nabla\times \boldsymbol{j}}$$
- The _integration constant_ is set to _zero_ due to _flux expuision_

- Also using $\nabla\times \boldsymbol{B}=\mu_{0}\boldsymbol{j}$, this gives:
$$-\nabla^{2}\boldsymbol{B}=-\frac{\mu_{0}}{\Lambda}\boldsymbol{B}$$
- The magnetic field must _decay_ with some _penetration depth_:
$$B\propto \exp\left( -\frac{x}{\lambda} \right)\qquad \lambda^{2}=\frac{\Lambda}{\mu_{0}}=\left( \frac{c}{\omega_{p}} \right)^{2}$$
- Typical depth is $\sim 40\,\text{nm}$

- Use the _London gauge_:
$$\nabla\cdot \boldsymbol{A}=0$$
- Meanwhile, let $\boldsymbol{A}=0$ in the _bulk_, and $\boldsymbol{A}_{\perp}=0$ on the _surface_
	- There should be no current going _out_ of the superconductor

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

- The last term accounts for _energy due to some magnetic field in the superconductor_ $\nabla\times (\boldsymbol{A}-\boldsymbol{A}_{E})$
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
$$\displaylines{\frac{1}{2m}\left( \frac{\hbar}{i}\nabla -e^{*}\boldsymbol{A} \right)^{2}\psi+(\alpha+\beta|\psi|^{2})\psi=0 \\ \begin{align}
\boldsymbol{J}_{s}=\frac{1}{\mu_{0}}\nabla\times(\nabla\times \boldsymbol{A})&=\frac{q}{2m} \frac{\hbar}{i}(\psi^{*}\nabla \psi-\psi \nabla \psi^{*})-q^{2}|\psi|^{2}\boldsymbol{A}  \\
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

### Meissner effect from Ginzburg-Landau
- In the London approximation, assume $n_{s}$ is _fixed_ near some equilibrium value $-\alpha/\beta$
- However, the _phase_ $\theta$ can vary

- If $\theta$ is _single-valued_, $\oint \nabla\theta \cdot d\boldsymbol{s}=0$ such that $(\nabla\times \nabla)\theta=0$
	- $\psi$ is always single-valued, but $\theta$ is only single-valued for a _simply connected domain_
- Then one gets the _second_ [[#London equations|London equation]] from the Ginzburg-Landau equations
$$\nabla\times \boldsymbol{J}_{s}=-\rho_{s}\boldsymbol{B}$$
- Then from Maxwell's eq.
$$\nabla^{2}\boldsymbol{B}=\frac{\boldsymbol{B}}{\lambda^{2}}\qquad \lambda=\frac{1}{\sqrt{ \mu_{0}\rho_{s} }}=\sqrt{ \frac{m}{4\mu_{0}e^{2}n_{s}} }$$
- $\lambda$ is some _penetration depth_ of the magnetic field into the solid

## Gauge transformations in a superconductor
- The gauge transformation of $\boldsymbol{A}$:
$$\boldsymbol{A}\to \boldsymbol{A}+\nabla \chi \qquad \varphi \to \varphi-\dot{\chi}$$
- The corresponding transformation for the wavefunction:
$$\psi\to \psi \exp\left( i\frac{q}{\hbar} \chi\right) \qquad \theta\to \theta+\frac{q}{\hbar}\chi$$
- The _supercurrent_ $\boldsymbol{J}_{s}$ remains _invariant_ as an observable
	- The Ginzburg-Landau equations themselves are invariant

- One can also have a gauge transformation such that $\theta$ goes to $0$ _everywhere_

- Having some nonzero $\theta$ corresponds to a _broken symmetry state_

### Coherence length
- The first Ginzburg-Landau equation has some _lengthscale_ such that it can be written as:
$$\xi^{2}\nabla^{2}\psi+\psi-\frac{\beta}{|\alpha|}|\psi|^{2}\psi=0\qquad \xi=\sqrt{ \frac{\hbar^{2}}{2m|\alpha|} }$$
- This is the lengthscale to which the _magnitude_ of $\psi$ might change
### Flux quantisation
- Consider a superconductor with some _hole_, which is _threaded_ by some magnetic field
- Far away from the surface, $J_{s}\to 0$ such that:
$$\boldsymbol{A}=-\frac{\hbar}{2e}\nabla\theta$$
- Relating this to flux:
$$\Phi=\oint\,\boldsymbol{A}\cdot d\boldsymbol{l} =\frac{\hbar}{q} \oint  \nabla\theta \cdot d\boldsymbol{l} =\frac{\hbar}{q}2\pi n $$
- There is some _quantised trapped flux_ inside the superconductor
- The unit is the _flux quantum_
$$\Phi_{0}=\frac{h}{2e}$$

- Identify the superconducting material with a _wire_, and each point of the wire has a corresponding _plane_ on which $\psi=|\psi|\exp(i\theta)$ is defined, such that the _locus_ of $\psi$ is on a _tube_
- A superconductor with a _hole_ means the tube is a _torus_, and the locus is some _winding around the torus_, with _winding number_ $n$ such that $\Delta\theta=2\pi n$
- The supercurrent is _topologically protected_
![[Superconductor topological defect.png|200]]

- The trapped flux gives a _topological defect_, which cannot change

### Vortex energy and type II superconductors
- Within the vortex, the _gradient term_ of the free energy increases, as a _kinetic energy cost_
$$\Delta F_\text{kin}=$$
- Meanwhile, there is a _decrease_ in _magnetic energy_
- Each vortex is asumed to contain _only one flux quantum_ as higher flux is _unfavourable_
$$\Delta F_\text{mag}=B_{E}\int  \frac{B}{\mu_{0}} \,d^{2}r=B_{E} \frac{\phi_{0}}{\mu_{0}}$$
- There is some _critical field_ $B_{c1}$ where the vortex formation is _energetically advantageous_

- It is when a _disc_ of _radius_ $\sim\lambda$ starts _enclosing_ one flux quantum

- In _type I_ superconductors, $B_{c1}>B_{c}$ such that the sample becomes _normal_ before vortex formation
- In _type II_ superconductors, _flux expulsion stops partially_, such that the magnetic field _penetrates_ forms a _vortex lattice_
	- Vortices penetrate until there is enough _repulsion_ and they settle into a lattice
	- This continues up to some other field strength $B_{c2}$ where the sample becomes _normal_

## Type II superconductors and vortices
- Type II superconductors form _lattices_ of _circular vortices_
- Each vortex has _inner radius_ $\xi$ and _outer radius_ $r_{B}<\lambda$

- $B$ varies _slowly_ within the cylinder as $r_{B}<\lambda$
- Each vortex is assumed to enclose _one flux quantum_:
$$\phi_{0}=\pi r_{B}^{2}B$$

- The _spatial average free energy density_ of a vortex:
$$\int_{\xi}^{r_{B}} \frac{2\pi rdr}{\pi r_{B}^{2}} f_{V}=\text{const.}+\frac{\phi_{0}^{2}}{8\pi^{2}r_{B}^{2}\mu_{0}\lambda^{2}}\ln\left( \frac{r_{B}^{2}}{\xi^{2}} \right)+\frac{(B-B_{E})^{2}}{2\mu_{0}}$$
- By _minimising_ w.r.t. $B$, one can find the _most probable internal field_
$$B=B_{E}- \frac{\phi_{0}}{8\pi\lambda^{2}} \ln\left( \frac{\eta \phi_{0}}{2\pi \xi^{2}B} \right)=B_{E}+\mu_{0}M$$
- $M$ is the _magnetisation_, and $\eta$ is some _constant_ of order unity

- Magnetisation goes to _zero_ when the _flux quantum_ is distributed over a _disc_ of radius $\xi$
- The _vortex cores start to overlap_, and superconductivity _breaks down_:
$$B_{c2}=\frac{\phi_{0}}{2\pi \xi^{2}}$$
- Magnetisation vanishes _continuously_, as a _second order phase transition_

- This gives:
$$B_{c1}B_{c2}=B^{2}_{c}$$
![[Type II superconductivity transitions.png]]

- In terms of the _Ginzburg-Landau parameters_:

- The critical fields are _linear_ in temperature
	- GL theory description only close to $T_{c}$

### Condensation energies
- The condensation energy is the _total energetic advantage_ of _forming_ a superconductor:
$$\int  \boldsymbol{B}_{E}\cdot d\boldsymbol{M} -d(\boldsymbol{B}_{E}\cdot \boldsymbol{M})=\int  (-\boldsymbol{M})\cdot d\boldsymbol{B}_{E} $$

- The _condensation energy_ should be the _same_ with or without vortex penetration
- The _equal area construction_:
![[Superconductivity equal area.png]]

### Vortex interactions and resistivity
- There may be some _transport current_ in the superconductor, such that the _total screening current_ is:
$$\boldsymbol{J}_{s}=\boldsymbol{J}_\text{vortex}+\boldsymbol{J}_\text{tr}$$
- The current experiences a _Lorentz force_
	- Analagous to the _Magnus force_ in fluid dynamics
- The _total force per unit length_
$$f=\int  \boldsymbol{J}_{s}\times \boldsymbol{B} \,d^{2}r=\boldsymbol{J}_\text{tr}\times \int  \boldsymbol{B}\,d^{2}r=\boldsymbol{J}_\text{tr}\times\left( \phi_{0}\hat{B} \right)$$

- For _multiple vortices_, the "transport current" accounts for _current from other vortices_
- This means that _vortices can repel each other_
- Therefore, the _vortex rush_ in the formation of the vortex state will _stop_ at some point

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
$$I=I_{J}\sum_{\nu=-\infty}^{\infty} J_{\nu}\left( \frac{\omega _\text{JRF}}{\omega _\text{RF}} \right)\sin[\theta_{0}+(\omega _\text{J0}+\omega _\text{RF})t]+\frac{V_{0}}{R}+\frac{V_\text{RF}}{R}\cos(\omega _\text{RF}t)$$
- It generates _sideband frequencies_ $\omega_{J0}+\nu\omega _\text{RF}$
- There is a _constant DC part unless_ the Josephson frequency _matches a multiple of the AC frequency_:
$$\omega_{J0}+\nu\omega _\text{RF}=0\implies \langle I \rangle=J_{\nu}\left( \frac{\omega _\text{JRF}}{\omega _\text{RF}} \right)I_{J}\sin(\Theta_{0})+\frac{V_{0}}{R} $$

- These are _Shapiro spikes_

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
$$I_\text{tot}=I_{a}+I_{b}=I_{J}(\sin\Theta_{a}+\sin\Theta_{b})=2I_{J}\cos\left( \frac{\Theta_{a}+\Theta_{b}}{2} \right)\sin\left( \frac{\Theta_{a}+\Theta_{b}}{2} \right)$$
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
- Therefore, like superconductors, one can define a _Ginzburg-Landau order parameter_
- Unlike Ginzburg-Landau order parameter, except _charge neutral_
$$\boldsymbol{J}_{s}=\frac{\hbar}{2i}(\psi^{*}\nabla \psi-\psi \nabla \psi^{*})=\rho_{s}\hbar \nabla\theta=\rho_{s}\boldsymbol{v}_{s} \qquad \psi=\sqrt{ \rho_{s} }\exp(i\theta)$$
- One can define the _superfluid velocity_:
$$\boldsymbol{v}_{s}=\frac{\hbar}{m}\nabla\theta$$
- The flow is _irrotational_:
$$\nabla\times \boldsymbol{v}_{s}=0$$
- From an analogy with [[#London equations|superconductors]] ($\varphi \,dq\to \mu dN$), one gets the _Anderson-Josephson relation_:
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

- There is _no screening_, and the vortex core is typically _small compared to superconductors_
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
$$\frac{p^{2}}{2M}=\frac{(P-\hbar k)^{2}}{2M}+\omega_{k}\implies \omega_{k}=Vk-\frac{\hbar k^{2}}{2M}\approx Vk$$
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

# BCS Theory
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
## Excitations

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

- _Interaction_ causes _condensate depletion_
	- Atomic gases: $n_{0}/n \sim 0.9$, $\ce{ He-II }: n_{0}/n <0.1$
	- Not due to thermal excitations

### Density fluctuations in BECs
- Consider the _density operator_ in reciprocal space
$$\rho_{q}\to \sqrt{ n_{0} }(a^{\dagger}_{-q}+a_{q})\sim \alpha_{q}$$
- The _low level excitation_ is therefore interpreted as a _density fluctuation_

- The [[#Superfluidity and critical velocity|Landau critical velocity]] becomes _finite_


### BCS fermion excitation spectrum
- A _gapped spectrum_:
$$E_{k}=\sqrt{ \varepsilon_{k}^{2}+\Delta^{2} }$$
- The excitation is:
$$\alpha ^{\dagger}_{k\sigma}=$$
- It is a _coherent superposition_ of _adding_ an electron and _removing_ an electron
- It has a _well-defined spin_
	- Spin-charge separation

### BCS gap equation
- An equation for $\Delta(T)$
$$\begin{align}
\Delta&=\frac{|g|}{V}\sum_{k}\langle a_{-k\downarrow}a_{k\uparrow} \rangle \\ &=-\frac{|g|}{V}\sum_{k}u_{k}v_{k}(1-\langle \alpha ^{\dagger}\alpha \rangle -\langle \beta ^{\dagger}\beta \rangle )_{k} \\ \Delta&=\frac{|g|}{V}\sum_{k} \frac{\Delta}{2E_{k}}(1-2f(E_{k}))
\end{align}$$
- For a _finite temperature_, the gap function must then satisfy:
	- $N(\xi)$: _density of states_ per spin per unit volume
$$1=|g|\int  \frac{N(\xi)d\xi}{\sqrt{\xi^{2}+\Delta(T)^{2}  }}\tanh\left( \frac{\sqrt{ \xi^{2}+\Delta(T)^{2} }}{2k_{B}T} \right) $$

### Ginzburg-Landau order parameter from BCS theory
- The _particle-particle_ field

- The order parameter is a _coarse-grained average_ of the field