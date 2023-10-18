- The _degrees of freedom_ are represented by _fields_
- _Fields_ are _functions/maps between two sets of numbers_

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
$$S=\int\Lagr\left(\phi,\pd{\phi}{t},\nabla\phi\right)\,dt\,dx_1dx_2\dots dx_d$$
- The Euler-Lagrange equation is then:
$$\pd{\Lagr}{\phi}=\pd{}{t}\left(\pd{\Lagr}{\dot{\phi}}\right)+\nabla\cdot\left(\pd{\Lagr}{(\nabla\phi)}\right)$$
- The _conservation of canonical momentum_ is then:
$$\pd{\pi}{t}+\nabla\cdot\bm{J}=0$$
- As time and space are on _equal footing_, treat $t$ as _another coordinate variable_:
$$\displaylines{\Lagr=\Lagr(\phi,\partial_\mu\phi) \\ \pd{\Lagr}{\phi}=\partial_\mu\pd{\Lagr}{[\partial_\mu\phi]}}$$
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

- One writes down the most _general_ Lagrangian, up to _second order terms_:
$$\Lagr=\alpha(\partial^\mu\phi)(\partial_\mu\phi)+\beta\partial^\mu\partial_\mu\phi+\gamma\phi\partial^\mu\partial_\mu\phi+\delta\phi+\epsilon\phi^2$$
- Impose the _boundary condition_ that

- One can _rewrite_ this as:
$$\Lagr=(\alpha-\gamma)(\partial^\mu\phi)(\partial_\mu\phi)+\partial^\mu$$

- One can then _define_ $\alpha-\gamma$ as
- This leads to the _equation of motion_:

- Then redefine $\epsilon$ as, getting the Lagrangian density as:
$$\Lagr=\frac{1}{2}(\partial^\mu\phi)(\partial_\mu\phi)-\frac{1}{2}m^2\phi^2$$


- The equation of motion is then the _Klein-Gordon equation_:
$$\partial^\mu\partial_\mu\phi+m^2\phi=0$$