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

## Gauge transformations
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