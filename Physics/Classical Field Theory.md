- The _degrees of freedom_ are represented by _fields_
- _Fields_ are _functions/maps between two sets of numbers_

- Notation: _natural units_, $\hbar=c=1$
	- Conversion: $\hbar c=0.2\,\text{GeV}\,\text{fm}$
	- $[\text{T}]=[\text{E}]^{-1}=[\text{M}]^{-1}$

- [ ] Add bits from TP1 notes 📅 2023-10-19 ⏫ 
# Field theories in physics
- The dynamics of a _point particle_ is a classical field theory
	- The map: from a set in $\mathbb{R}$ (_time_) to a set in $\mathbb{R}^3$ (_space_)
- This also applies to a set of $n$ particles
	- From a set in $\mathbb{R}$ (time) to a set in $\mathbb{R}^{3n}$ 
	- As long as _collisions_ are _not accounted for_
- Or one can think of _waves on a string_
	- A map from $\mathbb{R}^2$ (_time_, _length_ along string) to $\mathbb{R}^2$ (_displacements_)

- _Electromagnetism_ is a classical field theory
	- A map from $\mathbb{R}^4$ (_spacetime_) to $\mathbb{R}^6$ (the _electric_ and _magnetic_ fields)
- _General relativity_ is a field theory
	- $\mathbb{R}^4$ (spacetime) to $\mathbb{R}^{10}$ (the _metric tensor_)
- _String theory_ is a field theory
	- Map from $\mathbb{R}^2$ or $\mathbb{R}$ (depending on if the string is _open or closed_) to $\mathbb{R}^{26}$
- Mathematically, _thermodynamics_ is also a field theory

- Ultimately, for a _Lorentz invariant_ theory, one takes $\mathbb{R}^4$, or _Minkowski spacetime_, as the _source_ of the map

# Lagrangian density

## The wave on an elastic rod
- Consider _longitudinal waves_ on an elastic rod, with density $\rho$ and some _elastic modulus_ $\kappa$
- Let there be a _field_ $\phi(x,t)$ describing the _displacement_
- Set up the [[Analytical classical mechanics|Lagrangian]]:
$$L=T-V=\int\frac{1}{2}\rho\left(\pd{\phi}{t}\right)^2\,dx-\int\frac{1}{2}\kappa\left(\pd{\phi}{x}\right)\,dx$$
- The _action_ is then:
$$S=\int L\,dt=\int\Lagr\,dt\,dx$$
- $\Lagr$ is known as the _Lagrangian density_:
$$\Lagr\left(\phi,\phi',\dot{\phi}\right)=\frac{1}{2}\rho\dot{\phi}^2-\frac{1}{2}\kappa\phi'^2$$
- In general, it is a function of the _field_, and its _time and space derivatives_
- Considering a _variation_ in $\phi$ while fixing the _endpoints_, and using [[Analytical classical mechanics#Hamilton's Principle of Stationary Action|Hamilton's Principle]]:
$$\pd{\Lagr}{\phi}-\pd{}{x}\left(\pd{\Lagr}{\phi'}\right)-\pd{}{t}\left(\pd{\Lagr}{\dot{\phi}}\right)=0$$
- This is the _Euler-Lagrange equation for the Lagrangian density_
- The form is the _same for $x$ and $t$_, as expected
	- This later leads to the fact that $\Lagr$ is _Lorentz invariant_

- Applying the above equation to the string:
$$\kappa\phi''-\rho\ddot{\phi}=0$$
- This is simply the _wave equation_

- One can then define the _canonical momentum density_:
$$\pi(x,t)=\pd{\Lagr}{\dot{\phi}}$$
- This _depends_ on the choice of _"time" coordinate_
	- Hence, it is _not a Lorentz invariant_

- One can then define a _Hamiltonian density_:
$$\Ham(\phi,\pi,\phi')=\pi\dot{\phi}-\Lagr$$
- For the _elastic rod_, one gets:
$$\Ham=\frac{\pi^2}{2\rho}+\frac{1}{2}\kappa\phi'^2$$

- If $\Lagr$ _does not depend explicitly on_ $\phi$, from the Euler-Lagrange equation, one gets:
$$\pd{\pi}{t}+\pd{}{x}J(x,t)=0$$
- $J(x,t)=\partial\Lagr/\partial\phi'$ can be interpreted as the _canonical momentum current_
- The change in _total canonical momentum_ is:
$$\frac{dp}{dt}=\int\pd{\pi}{t}\,dx-\int\pd{J}{x}\,dx=0$$
- The latter term is _zero_ if one has _periodic boundary conditions_
- This gives the _conservation of canonical momentum_
## Generalising to more dimensions
- For _more dimensions_, the action is:
$$S=\int\Lagr\left(\phi,\pd{\phi}{t},\nabla\phi,x^\mu\right)\,dt\,dx_1dx_2\dots dx_d$$
- The Euler-Lagrange equation is then:
$$\pd{\Lagr}{\phi}=\pd{}{t}\left(\pd{\Lagr}{\dot{\phi}}\right)+\nabla\cdot\left(\pd{\Lagr}{(\nabla\phi)}\right)$$
- The _conservation of canonical momentum_ is then:
$$\pd{\pi}{t}+\nabla\cdot\bm{J}=0$$
- As time and space are on _equal footing_, treat $t$ as _another coordinate variable_:
$$\displaylines{\Lagr=\Lagr(\phi,\partial_\mu\phi) \\ \pd{\Lagr}{\phi}=\partial_\mu\left(\pd{\Lagr}{[\partial_\mu\phi]}\right)}$$
- Then if $\partial\Lagr/\partial\phi=0$:
$$\partial_\mu J^\mu=0$$

## Relativistic scalar field
- For a relativistic theory, the field used must be _Lorentz invariant_
- The field could be a _scalar_ or _vector_
	- $\phi\in\mathbb{R}^2$: spin-1/2 particle
	- $\phi\in\mathbb{R}^4$: photon

- The _action_ is the integration of $\Lagr$ with respect to an _element of spacetime_:
$$S=\int\Lagr\,dx^\mu$$
- The spacetime element is _Lorentz invariant_

- One writes down the most _general_ Lagrangian, up to _second order terms_
	- Dimension of $\Lagr$: $[M]^4$
$$\Lagr=\alpha(\partial^\mu\phi)(\partial_\mu\phi)+\beta\partial^\mu\partial_\mu\phi+\gamma\phi\partial^\mu\partial_\mu\phi+\delta\phi+\epsilon\phi^2$$
- Impose the _boundary condition_ that $\phi\to 0$ at _infinity_, and is _fixed_ for _two points in time_ (distant past and future)

- One can _rewrite_ this as:
$$\Lagr=(\alpha-\gamma)(\partial^\mu\phi)(\partial_\mu\phi)+\partial^\mu(\beta\partial_\mu\phi+\gamma\phi\partial_\mu\phi)+\delta\phi+\epsilon\phi^2$$
- _Integrating_ this over a 4D surface, the second term gives a _constant_, which _does not affect_ the equations of motion

- One can then _define_ $\alpha-\gamma$ as $1/2$
- This leads to the _equation of motion_:
$$\partial^\mu\partial_\mu\phi-\delta-2\epsilon\phi=0$$
	- _Lower_ the index using the metric, making the $(\partial_\mu\phi)(\partial^\mu\phi)$ term contribute _twice_
- Then impose the boundary conditions to make $\delta$ _vanish_

- Then redefine $\epsilon$ as $-m^2/2$, getting the Lagrangian density as:
$$\Lagr=\frac{1}{2}(\partial^\mu\phi)(\partial_\mu\phi)-\frac{1}{2}m^2\phi^2$$
- Writing it out in more detail:
$$\Lagr=\frac{1}{2c^2}\left(\pd{\phi}{t}\right)^2-\frac{1}{2}(\nabla\phi)^2-\frac{1}{2}m^2\phi^2$$

- The equation of motion is then the _Klein-Gordon equation_:
$$\partial^\mu\partial_\mu\phi+m^2\phi=0$$
	- For a _different metric_, there is a _minus sign_

- One also gets the _canonical momentum density_:
$$\pi=\pd{\Lagr}{\dot{\phi}}=\frac{1}{c^2}\left(\pd{\phi}{t}\right)$$
- The _Hamiltonian density_ is then:
$$\Ham=\frac{c^2\pi^2}{2}+\frac{1}{2}(\nabla\phi)^2+\frac{1}{2}m^2\phi^2$$
- This can only be _positive-definite_ iff the $\phi^2$ coefficient is _positive_
	- Negative: one gets states with _arbitrary large negative energy_, hence the state has _no stable ground state_, which is _unphysical_
	- This justifies $\epsilon=-m^2/2$

## Fourier analysis of Klein-Gordon equation
- For simplicity, take _one spatial dimension_
- Let there be a _plane wave solution_ to the Klein-Gordon equation:
$$\phi=\exp[i(kx-\omega t)]$$
- This gives the condition:
$$\omega^2=k^2+m^2$$
- One can then _superimpose_ solutions (with $N(-k)=N(k)$ as a normalising factor)
	- Ensure $\phi$ is _real_:
$$\phi=\int\,dk\,N(k)\,\left[a(k)\exp[i(kx-\omega t)]+a^*(k)\exp[-i(kx-\omega t)]\right]$$
- One can then try to write the Hamiltonian:
$$H=\int\left(\frac{c^2\pi^2}{2}+\frac{1}{2}(\nabla\phi)^2+\frac{1}{2}m^2\phi^2\right)\,dx$$
- Using:
$$\int\,dx\exp[i(k\pm k')x]=2\pi\delta(k\pm k')\hspace{1.5cm} N(-k)=N(k)\hspace{1.5cm}\omega(-k)=\omega(k)$$
- One finds:
$$H=2\pi\int\,dk\,[N(k)\omega(k)]^2[a(k)a^*(k)+a^*(k)a(k)]$$
- The _explicit time dependence disappears_ as $\Lagr$ is _not explicitly dependent on time_
- In _quantum field theory_, $a(k)$ is an _operator_ and $a$ and $a^*$ _may not commute_
- Choose $N(k)$:
$$N(k)=\frac{1}{2\pi}\frac{1}{2\omega}$$
- This _keeps the Hamiltonian Lorentz invariant_
- The Hamiltonian is then:
$$H=\int\,dk\,N(k)\frac{\omega(k)}{2}[a(k)a^
*(k){+a^*(k)a(k)}]$$
- In the _classical_ regime:
$$H=\int\,dk\,N(k)\omega(k)|a(k)|^2$$
- $N(k)$ can be interpreted as _number of modes_
- $\omega(k)$ is the _energy of modes_
- Each mode behaves as a _simple/quantum harmonic oscillator_
	- Energy is _relativistic_

- For _3 spatial dimensions_:
$$\phi\propto\exp[i(\bm{k}\cdot\bm{r}-\omega t)]$$
- Normalisation:
$$N(k)=\frac{1}{(2\pi)^3}\frac{1}{2\omega(k)}$$
- The expression for the _Hamiltonian_ holds

## Complex scalar fields
- Let there be a general _complex scalar field_ $\phi(x^\mu)$
- The Lagrangian must be _invariant_ with respect to adding a _phase_ to $\phi$
- The most _general Lagrangian_:
$$\Lagr=\partial_\mu\phi(\partial^\mu\phi^*)-m^2\phi^*\phi$$
- _Decompose_ the scalar field:
$$\phi=\phi_1+i\phi_2$$
- Treating $\phi$ and $\phi^*$ as _independent_:
$$\pi=\pd{\Lagr}{\dot{\phi}}=\dot{\phi}^* \hspace{1.5cm} \pi^*=\pd{\Lagr}{\dot{\phi^*}}=\dot{\phi}$$
- The _Hamiltonian density_:
$$\Ham=\pi\dot{\phi}+\pi^*\dot{\phi^*}-\Lagr$$
- One then gets _separate Klein-Gordon equations_ for $\phi$ and $\phi^*$

- The Fourier decomposition:
$$\phi=\int\,dk\,N(k)[a(k)\exp(ikx-i\omega t)+b^*(k)\exp(-ikx+i\omega t)]$$
- The Hamiltonian:
$$H=\int\,dk\,N(k)\omega(k)[|a(k)|^2+|b(k)|^2]$$
