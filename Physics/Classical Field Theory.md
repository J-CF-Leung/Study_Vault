- The _degrees of freedom_ are represented by _fields_
- _Fields_ are _functions/maps between two sets of numbers_

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
- Consider _longitudinal waves_ on an elastic rod
- Let there be a _field_ $\phi(x,t)$ describing the _displacement_
- Set up the [[Analytical classical mechanics|Lagrangian]]:
$$L=T-V=\int\frac{1}{2}\rho\left(\pd{\phi}{t}\right)^2\,dx-\int\frac{1}{2}\kappa\left(\pd{\phi}{x}\right)\,dx$$