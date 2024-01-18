- **L**ight **A**mplification by **S**timulated **E**mission of **R**adiation
- [[Atomic transitions#Stimulated emission|Stimulated emission]] leads to _amplification_ of photon emission
![[Stimulated emission amplification.png]]
- The _stimulated emission rate_ is _proportional_ to the _number density_ of photons, $n_{\gamma}$
- _Emission_ in the same mode _increases_ number density, hence the rate of emission

## Population inversion
- Amplification requires that the _emission_ (downward rate) _exceed_ the _absorption_ (upward rate)
	- It is a _necessary_ but _insufficient_ condition, as the _stimulated emission rate_ must be higher than the _spontaneous rate_, requiring a large [[#Rate of change of photon population|pumping rate]]
- Using [[Atomic transitions#Einstein coefficients and decay lifetimes|Einstein coefficients]] to describe transition rates:
![[Transition einstein coefficients.png]]
$$g_{2}B_{21}=g_{1}B_{12}$$

- A _necessary condition_ for amplification is:
$$\frac{N_{2}}{N_{1}} >\frac{g_{2}}{g_{1}}$$
- This _exceeds the thermal population_, where $(N_2/N_1)>(g_2/g_1)\exp(-\Delta E/k_BT)$
- This is known as _population inversion_
- This requires some _pumping mechanism_ to maintain

## Laser cavity
- Mechanism of laser:
![[Laser system.png]]

- The _laser cavity_ enables wavelengths $\lambda_{n}$ to form _standing waves_

- The laser is _initiated by spontaneous emissions_, in _all directions_
- Some will _emit in the right direction to form a standing wave_
- They then cause _stimulated emission_ to give more photons in the same direction
- A _steady state_ is formed with a _large energy density_ in the cavity, and a _fraction_ is allowed to _escape_
- The radiation is _highly coherent_, with the _same mode_ and all _in phase_
	- _Highly coherent sources_ are essential for [[Electrodynamics and Optics#Coherence|interfereometry]]
![[Laser process.png]]

- Radiation from atoms is typically _not a perfect delta function_ spectrum
- The spectrum is typically a [[Electrodynamics and Optics#Spectral lines|doppler-broadened]] _Gaussian_, for an atom of mass $M$:
$$\frac{\sigma_{\lambda}}{\lambda_{0}}=\sqrt{ \frac{k_{B}T}{Mc^{2}} }$$
- For a _helium-neon laser_:
![[He-Ne laser spectrum.png]]
- The _spikes_ correspond to the _standing waves_, with $n\sim 10^{6}$

- The _broadened peak_ gives _several resonant cavity modes_

- Lasers can typically be _well-focused_
- The beam can be _continuous_ or _pulsed_, with the latter with _much higher achievable power_
- It is _highly monochromatic_
- It is [[Electrodynamics and Optics#Spatial coherence|spatially]] and [[Electrodynamics and Optics#Temporal coherence|temporally]] _coherent_
- One can produce _very short pulses_

## Helium-neon laser
- The helium-neon laser uses a _mixture_ of gases:
![[He-Ne laser.png]]
- The $\ce{ He }$ provides _long-lived, metastable states_ that can be populated by _pumping_
- The $\ce{ Ne }$ provides transitions suitable for _amplification_

![[Helium laser energy levels.png]]

- Fortunately, the $2^{1}\ce{ S }_{0}$ level of helium _matches in energy with an excited state of_ $\ce{ Ne }$
![[He-Ne energy levels.png]]
- The electrons are _transferred_ from $\ce{ He^{*} }$ to $\ce{ Ne }$ with a _collision_:
$$\ce{ He^{*} + Ne -> He + Ne^{*} }$$
- There is then a _decay_ which gives the _laser emission_
- If _only neon_ is used, then there are _many excited states_, only some of which are useful for lasers, hence it is _inefficient_

- The helium-neon laser is essentially a _four-level system_:
![[He-Ne 4 levels.png]]
- If the _relaxation times_ for levels $1$ and $3$ are sufficiently _rapid_, then _population inversion_ is possible:
$$\frac{N_{2}}{N_{1}} > \frac{g_{2}}{g_{1}}$$
- The process $0\to 3 \to 2$ is effectively a _single step_, allowing an approximation as a _three-level system_

## Laser cavity rate equations
- Let there be a _three-level system_, with energies $E_{2}>E_{1}>E_{0}$
- Considering _all possible transitions_:
![[3 level transitions.png]]

- $R$ is the _pumping rate per atom_ from the ground state
- $A_{ij}$ are the [[Atomic transitions#Einstein coefficients and decay lifetimes|Einstein coefficients]] for _spontaneous decay_
- $B_{ij}$ are the _Einstein coefficients_ for _spontaneous absorption and decay_
- $u(t)$ is the _EM energy density_ in the cavity for the _resonant cavity mode_

- One then gets the _rate equations_:
$$\begin{align} \dot{N}_{0}&=-RN_{0}+A_{10}N_{1}+A_{20}N_{2} \\ \dot{N}_{1}&=-A_{10}N_{1}-B_{12}uN_{1}+A_{21}N_{2}+B_{21}uN_{2} \\ \dot{N}_{2}&=RN_{0}+B_{12}uN_{1}-A_{20}N_{2}-A_{21}N_{1}-B_{21}uN_{2} \end{align}$$
- The rates _sum to zero_ (there are only 2 independent equations):
$$\frac{d}{dt}(N_{0}+N_{1}+N_{2})=0$$

### Steady-state and requirement for population inversion
- The _steady-state solution_ gives:
$$\dot{N}_{0}=\dot{N}_{1}=\dot{N}_{2}=0\hspace{1.25cm}\dot{u}=0$$
- The rate equations for the lower 2 levels:
$$\begin{align}RN_{0}&=A_{10}N_{1}+A_{20}N+2 \\ (A_{10}+B_{12}u)N_{1}&=(A_{21}+B_{21}u)N_{2}\end{align}$$
- Use the relation between Einstein coefficients:
$$g_{2}B_{21}=g_{1}B_{12}$$
- One gets that for _population inversion_, level 1 must _empty fast enough_:
	- One can get the same result by assuming $A_{20}=0$, or the _general case_:
$$\frac{N_{2}}{N_{1}}> \frac{g_{2}}{g_{1}} \iff A_{10}> \frac{g_{2}}{g_{1}}A_{21}$$
- For example, for an $\ce{ He-Ne }$ laser, $A_{10}/(g_{2}A_{21}/g_{1})\approx 26$

### In terms of photon population
- _Population inversion_ is _not sufficient_, as the _stimlated emissions_ must _build up_, before the excited electrons _spontaneously decay_
	- Spontaneous decay occurs in _many modes_, and is hence undesirable
- This requires a _high pumping rate_ $R$

- The above equations are _insufficient_ to _determine_ the populations $N_{2,1,0}$, as the _energy density_ $u$ is still _unknown_
- The _amplification_ is measured by $u(t)$

- One must then _reformulate_ the equations to include $N_{\gamma}$, the number of photons _in the cavity mode_
- One can rewrite the coefficients as:
$$\displaylines{B_{12}u(t)\equiv B_{12}'N_{\gamma}(t)\hspace{1.5cm}B_{21}u(t)=B_{21}'N_{\gamma}(t) \\ g_{2}B_{21}'=g_{1}B_{12}'}$$
![[1-2 laser transitions.png]]
- The _spontaneous_ transition rate $N_{2}A_{21}$ give photons in _all directions_, at random
- The _stimulated_ transition rate $N_{2}B_{21}'N_{\gamma}$ emits photons in the _cavity mode_

- The [[Atomic transitions#Spontaneous and stimulated emission|stimulated transmission rate]] for a given mode is _greater than_ the spontaneous emission rate by _factor_ $N_{\gamma}$
- From this, one gets the _spontaneous decay rates_:
	- $N_2A_{21}$ is the rate of transition into _any mode_
	- $N_2B_{21}'$ is the rate of transition into the _resonant cavity mode_
- The latter must be a _small subset_:
$$B_{21}'\ll A_{21}$$

### Loss from the resonant cavity
- The laser beam represents _energy loss from the cavity_, which is often _fractional_:
![[Resonant cavity loss.png]]
- Let the _fractional loss in intensity per round trip_ be $f$
$$f\equiv-\frac{\Delta I}{I}$$
- The _rate of change in intensity_:
$$\frac{dI}{dt}=\frac{\Delta I}{2d/c}=-\frac{fI}{2d/c}$$
- This results in _exponential decay_:
$$I(t)=I(0)\exp\left( -\frac{t}{\tau_{c}} \right)\hspace{1.5cm}\tau_{c}=\frac{2d}{fc}$$
- This gives the _photon loss rate_:
$$N_{\gamma}(t)=N_{\gamma}(0)\exp\left( -\Gamma _\text{cav}t \right)\hspace{1.5cm}\Gamma _\text{cav}\equiv\frac{1}{\tau_{c}}=\frac{cf}{2d}$$
- $\Gamma _\text{cav}$ is the _loss rate per photon_

- The _rate_ in which photons are lost:
$$F\equiv-\frac{dN_{\gamma}}{dt}=\Gamma _\text{cav}N_{\gamma}$$
- Given the _difference in energy_ between the lasing levels is $\hbar \omega_{21}$
- The _beam output_ is then:
$$P_\text{beam}=\Gamma _\text{cav}N_{\gamma}\hbar\omega_{21}$$
- The transitions governing the _number of resonant cavity mode photons_:
![[Resonant photon population.png]]
$$\displaylines{\dot{N}_{\gamma}=N_{1}B_{21}'(N_{\gamma}+1)-N_{1}B_{12}'N_{\gamma}-\Gamma _\text{cav}N_{\gamma} \\ g_{2}B_{21}'=g_{1}B_{12}'}$$

## Reformulated laser cavity rate equations
![[Laser all transitions.png]]
$$\displaylines{\begin{align} \dot{N}_{0}&=-RN_{0}+A_{10}N_{1}+A_{20}N_{2} \\ \dot{N}_{1}&=-A_{10}N_{1}-B_{12}'N_{1}B_{\gamma}+A_{21}N_{2}+B_{21}'N_{2}N_{\gamma} \\ \dot{N}_{2}&=RN_{0}+B_{12}'N_{1}N_{\gamma}-A_{20}N_{2}-A_{21}N_{1}-B_{21}'N_{2}N_{\gamma} \\  \dot{N}_{\gamma}&=N_{1}B_{21}'(N_{\gamma}+1)-N_{1}B_{12}'N_{\gamma}-\Gamma _\text{cav}N_{\gamma} \end{align} \\ g_{2}B_{21}'=g_{1}B_{12}'}$$
- One can _solve_ for $N_{2,1,0}$ and $N_{\gamma}$ given the _initial conditions_:
$$N_{0}(0)=N\hspace{1.5cm}N_{1}(0)=N_{2}(0)=N_{\gamma}(0)=0$$
- This can only be done _numerically_

- One can also obtain an _analytic steady-state solution_

## Analytic steady-state solution
$$\dot{N}_{0}=\dot{N}_{1}=\dot{N}_{2}=\dot{N}_{\gamma}=0$$
- This also satisfies the _contraint_ $\dot{N}_{0}+\dot{N}_{1}+\dot{N}_{2}=0$
- There are only _three independent rate equations_:
$$\begin{align} 0&=-RN_{0}+A_{10}N_{1}+A_{20}N_{2} \\ 0&=-A_{10}N_{1}-B_{12}'N_{1}B_{\gamma}+A_{21}N_{2}+B_{21}'N_{2}N_{\gamma} \\  0&=N_{1}B_{21}'(N_{\gamma}+1)-N_{1}B_{12}'N_{\gamma}-\Gamma _\text{cav}N_{\gamma} \end{align}$$

- One can then _solve_ for $N_{\gamma}$ by _eliminating_ $N_{1}$ and $N_{2}$:
$$N_{\gamma}^{2}+\alpha N_{\gamma}+\beta=0$$

### Steady-state solution for He-Ne laser
- Parameters of a helium-neon laser:
![[He-Ne laser parameters.png]]
- There is a _very low chance_ that a photon is _spontaneously_ emitted parallel to the cavity axis, and can undergo _amplification_
$$\frac{B_{21}'}{A_{21}}\sim 10^{-8}$$
- Typically, the _pumping rate_ is about $R\approx 1.6\,\text{s}^{-1}$
	- Each _neon atom_ undergoes $1.6$ full cycles per second

#### Low pumping rates
- Up to $R=0.6\,\text{s}^{-1}$:
![[Low pumping rate populations.png]]
- _Population inversion_ occurs even for low pumping rates
- The _lasing threshold_ is $R_\text{th}\approx 0.3 \text{s}^{-1}$
	- Above the threshold, _stimulated transitions dominate_
- Above the threshold, the _photon population grows rapidly_, as _stimulated emission dominates_

#### Larger pumping rates
- Up to $R=3\,\text{s}^{-1}$
![[Large pumping rate populations.png]]
- The photon population $N_{\gamma}$ increases approximately _linearly_ with the pumping rate above the lasing threshold
- The population of the _upper level_ $N_{2}$ is approximately _clamped_

- For $N_{\gamma}\gg 1$, the steady state solution gives:
$$N_{2}-\frac{g_{2}}{g_{1}}N_{1}\approx \frac{\Gamma _\text{cav}}{B_{21}'}$$

- _Summing_ the steady-state equations, one gets:
$$0=N_{0}R-N_{2}A_{21}-N_{2}A_{20}+N_{2}B_{21}'-\Gamma _\text{cav}N_{\gamma}$$
- _Ignoring_ the spontaneous emission contributions, and using that $B_{21}'$ is _small_:
$$N_{\gamma}\approx \frac{N_{0}R}{\Gamma _\text{cav}}$$
- Provided only a _small fraction_ of atoms occupy the _excited_ levels:
$$\displaylines{N=N_{0}+N_{1}+N_{2}\approx N_{0} \\ N_{\gamma}\approx \frac{NR}{\Gamma _\text{cav}}}$$
- The beam output is _approximately linear_ to the pumping rate:
$$P_\text{beam}=\Gamma _\text{cav}N_{\gamma}\hbar \omega_{21}\approx NR\hbar\omega_{21}\propto R$$
![[Power output function of R.png|500]]
- The beam is _spatially and temporally_ [[Coherent states|coherent]]

#### Asymptotically large pumping rates
- Extend to $R\to \infty$:
![[R infinity population.png]]
- The _excited state_ and _photon_ populations eventually _saturate_
	- The pumping rate required is typically _unfeasible_




