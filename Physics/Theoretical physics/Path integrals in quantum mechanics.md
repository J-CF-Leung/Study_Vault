- In the [[Quantum Dynamics#Dynamics in the Schrodinger picture|Schrodinger picture]], the _wave function_ will _evolve in time_ with the operator $U$:
$$\ket{\Psi(t)}=\hat{U}(t,t')\ket{\Psi(t')}  $$
- In the [[Quantum Dynamics|Heisenberg picture]], the _state kets_ are _constant_ but the _operators_ will follow an _equation of motion_:
$$\frac{d}{dt}\mathcal{O}(t)=\frac{i}{\hbar}[H(t),\mathcal{O}(t)]$$

- The _path integral formalism_ includes consideration of _possible trajectories_ $\boldsymbol{r}(t)$ into the evolution of a quantum system

# The propagator
- Consider the _propagator_, a [[Principles of quantum mechanics#The wave function in different bases|position-space representation]] of the _time evolution operator_:
$$K(\boldsymbol{r},t|\boldsymbol{r}',t')=\theta(t-t')\braket{ \boldsymbol{r}|U(t-t') |\boldsymbol{r}'  } $$
- Here, $\theta$ is the _step function_:
$$\theta(t-t')=\begin{cases} 1 &t>t' \\ 0&t<t'\end{cases}$$
- This has a [[Analytical classical mechanics#Propagators and causality|classical analogue]]

- Consider a position-space wave function at time $t$, evolved from $\ket{\Psi(t')}$:
$$\begin{aligned}\Psi(\boldsymbol{r},t)=\braket{\boldsymbol{r}|\Psi(t)}&=\braket{ \boldsymbol{r}|U(t-t') |\Psi(t')  } \\ &= \int \, d^{3}\boldsymbol{r}' \braket{ \boldsymbol{r}|U(t-t') |\boldsymbol{r}'  } \braket{ \boldsymbol{r}' | \Psi(t') } \\ &= \int \, d^{3}\boldsymbol{r}'  K(\boldsymbol{r},t|\boldsymbol{r}',t') \Psi(\boldsymbol{r}',t') \end{aligned}$$

## Properties of the propagator

### As a Green's Function
- _Equivalently_, it is the _fundamental solution_ to the time-dependent Schrodinger equation:
	- Proof: consider $i\hbar (\partial/\partial t)K$
$$\begin{aligned}\left[ i\hbar \frac{\partial}{\partial t}-H \right]K(\boldsymbol{r},t|\boldsymbol{r}',t')&=i\hbar \delta^{3}(\boldsymbol{r}-\boldsymbol{r}')\delta(t-t') \\ K(\boldsymbol{r},t|\boldsymbol{r}',t')&=0 \;\;\;\text{for }t<t'\end{aligned}$$
- This makes the propagator a _Green's function_ for the equation

### Composition
- From the definition of $U$:
$$U(t-t')=U(t-t'')U(t''-t)$$
- For the _propagator_, by inserting an identity using eigenkets $\ket{\boldsymbol{r}''}$
$$K(\boldsymbol{r},t|\boldsymbol{r}',t')=\int\, d^{3}\boldsymbol{r}'' \,K(\boldsymbol{r},t|\boldsymbol{r}'',t'')K(\boldsymbol{r}'',t''|\boldsymbol{r}',t')$$

## Propagator of a free particle
- Consider the propagator for the _heat equation_
	- The heat equation is of a _similar form_ to the time-dependent Schrodinger equation
$$\displaylines{\frac{\partial\Theta}{\partial t}=\mathcal{D}\nabla_{\boldsymbol{r}}^{2}\Theta \\ \Theta(\boldsymbol{r},t)=\int K_\text{heat}(\boldsymbol{r},t|\boldsymbol{r}',t')\Theta(\boldsymbol{r}',t') \, d^{3}\boldsymbol{r}'  \\ \left[ \frac{\partial}{\partial t}-\mathcal{D}\nabla_{\boldsymbol{r}}^{2} \right]K_\text{heat}(\boldsymbol{r},t|\boldsymbol{r}',t')=\delta(\boldsymbol{r}-\boldsymbol{r}')\delta(t-t') \\ K_\text{heat}(\boldsymbol{r},t|\boldsymbol{r}',t')=0 \;\;\text{for }t<t'}$$
- It can be shown that the solution is:
$$K_\text{heat}(\boldsymbol{r},t|\boldsymbol{r}',t')=\frac{\theta(t-t')}{[4\pi \mathcal{D}(t-t')]^{3/2}}\exp\left[ -\frac{|\boldsymbol{r}-\boldsymbol{r}|^{2}}{4\mathcal{D}(t-t')} \right]$$
- For the _free particle_:
$$\left[ \frac{\partial}{\partial t}+\frac{\hbar^{2}}{2m}\nabla_{\boldsymbol{r}}^{2} \right]\Psi(\boldsymbol{r},t)=0$$
- Then make the _substitutions_ $t\to it$ and $\mathcal{D}\to \hbar/2m$:
$$K_\text{free}(\boldsymbol{r},t|\boldsymbol{r}',t')=\theta(t-t')\left( \frac{m}{2i\pi \hbar(t-t')} \right)^{3/2}\exp\left[ -\frac{m\left| \boldsymbol{r}-\boldsymbol{r}' \right|^{2}}{2i\hbar(t-t')}  \right]$$
- It is only a function of the _duration_ of the propagation, $t-t'$
### In momentum space
- In _momentum space_, the Hamiltonian is _diagonal_, and _time independent_:
$$\begin{align}K_\text{free}(\boldsymbol{p},t|\boldsymbol{p}',t')&=\theta(t-t')\braket{ \boldsymbol{p}|U(t-t') |\boldsymbol{p}'  } \\ &= \theta(t-t')\delta(\boldsymbol{p}-\boldsymbol{p}')\exp\left( -i \frac{\boldsymbol{p}^{2}}{2m} \frac{t-t'}{\hbar} \right)\end{align}$$
- Using a _Fourier transform_, this can be verified to be the _same_ as the formula in position space

## For a general Hamiltonian
- For a [[Quantum Dynamics#Dynamics in the Schrodinger picture|time-independent Hamiltonian]], the time-evolution operator is:
$$\hat{U}(t,t')=\exp\left[ -\frac{i\hat{H}(t-t')}{\hbar} \right]=\sum_{n}\ket{n}\bra{n}\exp\left[ -\frac{iE_{n}(t-t')}{\hbar} \right]  $$
- For a time-independent Hamiltonian, it is always a _function of the duration of propagation_ $t-t'$
- This gives the propagator:
$$K(\boldsymbol{r},t|\boldsymbol{r}',t')=\theta(t-t')\sum_{n}\psi_{n}(\boldsymbol{r})\psi_{n}^{*}(\boldsymbol{r}')\exp\left[ -\frac{iE_{n}(t-t')}{\hbar} \right]$$

- For a [[Quantum Dynamics#Time-dependent Hamiltonian|general time-dependent Hamiltonian]], $\hat{U}$ is a _function of both initial and final times_:
$$\displaylines{\ket{\Psi(t)}=\hat{U}(t,t')\ket{\Psi(t')} \\ \hat{U}(t,t')=\mathcal{T}\exp\left[ -\frac{i}{\hbar}\int_{t'}^{t}  dt_{i}\,H(t_{i})  \right]}$$
- The definition of the propagator still applies:
$$K(\boldsymbol{r},t|\boldsymbol{r}',t')=\theta(t-t')\braket{ \boldsymbol{r} |U(t,t')|\boldsymbol{r}'  }  $$

# Path integrals
- Consider _dividing_ some _time interval_ $t_{i}$ to $t_{f}$ into $N$ _infinitesimally small intervals_, with
$$\Delta t=\frac{t_{f}-t_{i}}{N}$$
- Each _interval_ is characterised by _its own propagator_, which can then be _combined_
$$K(\boldsymbol{r}_{f},t_{f}|\boldsymbol{r}_{i},t_{i})=\int  \, d\boldsymbol{r}_{1}\,d\boldsymbol{r}_{2}\dots d\boldsymbol{r}_{N-1} \, K(\boldsymbol{r}_{f},t_{f}|\boldsymbol{r}_{N-1},t_{N-1})\dots K(\boldsymbol{r}_{1},t_{1}|\boldsymbol{r}_{i},t_{i}) $$
- This is an _integral over all possible paths_ between $(\boldsymbol{r}_{i},t_{i})$ and $(\boldsymbol{r}_{f},t_{f})$, characterised by $\boldsymbol{r}_{1},\boldsymbol{r}_{2}\dots \boldsymbol{r}_{N-1}$

- As the _propagation time_ $\Delta t$ goes to zero, the propagator is a _delta function_, and one can take the _potential_ as a _constant value_
	- Taking the value in the _midpoint_ of the interval $((\boldsymbol{r}_{n}-\boldsymbol{r}_{n-1})/2, (t_{n}-t_{n-1})/2)$
- Modify the _free particle propagator_ for the _constant potential_:
$$K_\text{free}(\boldsymbol{r},t|\boldsymbol{r}',t')=\theta(t-t')\left( \frac{m}{2i\pi \hbar(t-t')} \right)^{3/2}\exp\left[ -\frac{m\left| \boldsymbol{r}-\boldsymbol{r}' \right|^{2}}{2i\hbar(t-t')}  -\frac{iV_{0}(t-t')}{\hbar}\right]$$

- For an _infinitesimal time interval_:
$$\frac{\left|\boldsymbol{r}_{n}-\boldsymbol{r}_{n-1}\right|^{2}}{t_{n}-t_{n-1}} \to \dot{\boldsymbol{r}}^{2}\Delta t $$
- The path integral then becomes:
$$K(\boldsymbol{r}_{f},t_{f}|\boldsymbol{r}_{i},t_{i})=\int  \, \mathcal{D}[\boldsymbol{r}(t)] \exp \left[ \frac{i}{\hbar}S \right] $$
- Here, $S$ is the [[Analytical classical mechanics#Hamilton's Principle of Stationary Action|classical action]]:
$$S[\boldsymbol{r}(t)]=\int_{t_{i}}^{t_{f}}L \, dt=\int _{t_{i}}^{t_{f}} \frac{1}{2}m \dot{\boldsymbol{r}}^{2}-V(\boldsymbol{r},t) \, dt  $$
- Here, $\mathcal{D}[\boldsymbol{r}(t)]$ represents a _volume element_ in the _space of paths_:
$$\int  \,\mathcal{D}[\boldsymbol{r}(t)]=\left( \frac{m}{2i\pi \hbar\Delta t} \right)^{3N/2}\int  \, d\boldsymbol{r}_{1}\int  \, d\boldsymbol{r}_{2}\dots \int  \, d\boldsymbol{r}_{N-1}    $$

- The _sum over paths_ is _weighted_ by a _phase factor_ given by the _classical action_
- As the action is _minimised_ for the _classical path_, paths which _deviate_ from it tend to _destructively interfere_

- For the _classical limit_ $\hbar\to 0$, the integral is _dominated by the classical path_ where the action is at a _minimum_

## Applications
- For [[Classical Field Theory|classical fields]], one can define a _Lagrangian density_:
$$S=\int \mathcal{L} \, d^{3}\boldsymbol{r}\,dt $$
- For _quantum fields_, one can add _perturbations_ to the action

- Also useful to evaluate _partition functions_ (weighted with a _temperature_ related factor instead)

- The _topology_ of paths is also important
	- e.g. _Aharonov-Bohm effect_

## Quantum harmonic oscillator
$$L_\text{SHO}(x,\dot{x})=\frac{1}{2}m\dot{x}^{2}-\frac{1}{2}m\omega^{2}x^{2}$$
- The propagator:
$$K(x,t|x',t')=\int \mathcal{D}[x(t)] \, \exp\left[ \frac{i}{\hbar}S_\text{SHO}[x(t)] \right] $$
- _Split_ the path into the _classical path_ $x_{0}(t)$ and some _deviation_ $\eta(t)$:
$$\displaylines{x(t)=x_{0}(t)+\eta(t) \\ \eta(t_{i})=\eta(t_{f})=0\\ \frac{d}{dt} \frac{\partial L}{\partial \dot{x}}\Bigg|_{x_{0}}=\frac{\partial L}{\partial x}\Bigg|_{x_{0}}}$$
- The action is then evaluated as:
$$S[x_{0}(t)+\eta(t)]=S[x_{0}(t)]+S[\eta(t)]+\int_{t_{i}}^{t_{f}} [m\dot{x}_{0}\dot{\eta}-m\omega^{2}x_{0}\eta] \, dt $$
- _Integrate_ the last term _by parts_,  it is _eliminated_ as the _classical path_ obeys the _Euler-Lagrange equation_
- This works for _any quadratic potential_

- The propagator is then written as:
$$K(x_{f},t_{f}|x_{i},t_{i})=\exp\left[ \frac{i}{\hbar}S_\text{SHO}[x_{0}(t)] \right]\int  \,\mathcal{D}[\eta(t)] \exp\left[ \frac{i}{\hbar}S_\text{SHO}[\eta(t)] \right]  $$
- The integral is taken _over deviations from the path_

- From the _boundary conditions_, one can expand $\eta(t)$ as a _Fourier expansion_:
$$\eta(t)=\sum_{n} \eta_{n}\sin\left[ \frac{\pi n(t-t_{i})}{t_{f}-t_{i}} \right]$$
- The _action_ is then:
$$S_\text{SHO}[\eta(t)]=\frac{m(t_{f}-t_{i})}{4}\sum_{n=1}^{\infty}\left[ \frac{\pi^{2}n^{2}}{(t_{f}-t_{i})^{2}}-\omega^{2} \right]\eta_{n}^{2}$$
- The path integral measure:
$$\mathcal{D}[\eta(t)]\propto \prod d\eta_{n}$$
- This is then a _product of Gaussian integrals_

- For $\omega\to 0$, it must approach the [[#Propagator of a free particle|free particle propagator]]:
$$K_\text{free}(x,t|x',t')=\theta(t-t')\left( \frac{m}{2i\pi \hbar(t-t')} \right)^{1/2}\exp\left[ -\frac{m\left( x-x' \right)^{2}}{2i\hbar(t-t')}  \right]$$
- This gives the result:
$$K(x,t|x',t')=\sqrt{ \frac{m}{2\pi i\hbar(t_{f}-t_{i})} }\exp\left( \frac{i}{\hbar}S_\text{SHO}[x_{0}(t)] \right)\prod_{n=1}^{\infty}\left( 1-\frac{\omega^{2}(t_{f}-t_{i})^{2}}{\pi^{2}n^{2}} \right)^{-1/2}$$
- Using the product:
$$\prod_{n=1}^{\infty}\left( 1-\frac{\omega^{2}(t_{f}-t_{i})^{2}}{\pi^{2}n^{2}} \right)=\frac{\sin[\omega(t_{f}-t_{i})]}{\omega(t_{f}-t_{i})}$$
- This gives the _propagator for the quantum harmonic oscillator_:
$$K(x,t|x',t')=\sqrt{ \frac{m\omega}{2\pi i\hbar \sin[\omega(t_{f}-t_{i})]} }\exp\left( \frac{i}{\hbar}S_\text{SHO}[x_{0}(t)] \right)$$
## The semiclassical limit
- The general propagator:
$$K(\boldsymbol{r}_{f},t_{f}|\boldsymbol{r}_{i},t_{i})=\int  \, \mathcal{D}[\boldsymbol{r}(t)] \exp \left[ \frac{i}{\hbar}S \right] $$
- For the _semiclassical limit_, take $\hbar\to 0$
- The _maximum contribution_ to the _path integral_ comes from the path of _stationary phase_, where $S$ is _stationary_
	- Also known as the _path of stationary phase_
	- Analagous to [[Time-Independent Approximation Methods#JWKB method and stationary phase|JWKB Approximation]]
$$\frac{\delta S}{\delta \boldsymbol{r}}\Bigg|_{\boldsymbol{r}=\boldsymbol{r}_\text{cl}}=0$$

- This is simply the _classical path_
	- The contributions _around the path_ begin to _oscillate quickly_, and _cancel out_

- Expansion of the action:
$$S[\boldsymbol{r}(t)]=S[\boldsymbol{r}_\text{cl}(t)+\eta(t)]=S[\boldsymbol{r}_\text{cl}(t)]+\frac{1}{2}\int \, dt \int  \, dt' \frac{\delta^{2}S}{\delta \boldsymbol{r}\delta \boldsymbol{r}'}\eta(\boldsymbol{r})\eta(\boldsymbol{r}') +\dots$$
- Keeping _quadratic terms_ in the _semiclassical_ regime, this gives the _van Vleck propagator_
$$K_\text{van Vleck}\sim (\text{Gaussian integral})\exp\left( \frac{i}{\hbar}S[\boldsymbol{r}_\text{cl}] \right)$$
- It is _exact_ for the quantum harmonic oscillator
