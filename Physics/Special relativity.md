>[!info] Notation
> As the speed of light is _constant_, one can use _geometrised units_:
> $$c=2.99792458\times10^8\,\text{m}\,\text{s}^{-1}=1$$
# Foundational concepts

## Inertial reference frames and spacetime
- All measurements are made in _inertial reference frames_, also known as _Lorentz frames_
- It can be imagined as a 3D _lattice_ with clocks at every point
- The _spacing_ between points is _uniform_, and the _clocks tick uniformly_
	- On the scale of _wavelength and period_ of _light emitted by atoms_
- The clocks are _synchronised_
	- If clock A _emits_ a pulse of light at $t_e$, which is then _reflected_ by clock B and _returned_ to A at $t_r$, the _time of bouncing_ $t_b$ measured by B is _equal_ to $(t_e+t_r)/2$ measured by A
- Measurements in an inertial frame are made by an _observer_
![[Inertial frame.png]]

- A particular set of _spatial and temporal coordinates_ is termed an _event_
	- Or a precise _point_ in 4-dimensional _spacetime_
- A _4-vector_ is an _arrow_ in 4-D _spacetime_, reaching _from one event to another_
	- 3-vector: $\Delta\bm{x}$
	- 4-vector: $\Delta\vec{x}$
- They are _geometric, frame-independent objects_

- An inertial reference frame provides a _coordinate system_ in spacetime, with events characterised by the coordinates:
$$(x^0,x^1,x^2,x^3)\equiv(t,x,y,z)$$
- This described an event at _location_ $(x,y,z)$ and time $t$
- The time is _measured by a clock at the event's location_

- Events can be depicted on _spacetime diagrams_, where _time is vertical_ and _one spatial coordinate is omitted_:
![[Spacetime diagram.png]]
- The axes can either be that of the _preferred inertial frame_ or _completely arbitrary_ if the viewpoint is _frame-independent_
- The _trajectory_ of an object forms a _world-line_
	- An object with _uniform velocity_ will produce a _straight_ world-line
# The fundamental principles of Einsteinian relativity

1. The laws of physics are _expressible as a geometric, frame-independent relation among geometric, frame-independent objects_
	- Geometric objects: 4-vectors, tensors
	- In other words, the laws are _the same in every inertial frame_
2. The velocity at which interactions _propagate_ (aka. the maximum possible velocity in the universe), the speed of light $c$, is the _same in all inertial frames of reference_
$$c=2.99792458\times10^8\,\text{m}\,\text{s}^{-1}$$
	- This can be said to a _consequence_ of the first principle, as $c$ is embedded in _Maxwell's equations_, which are special relativistic laws
	- Reason: light _does not require a medium to propagate_, and _does not have a mass_

- In Galilean relativity, distances are relative, and time is absolute
- In Einsteinian relativity (or just relativity), _neither distance and time are absolute_
	- From the fact that _no velocities exceed_ $c$
	- This implies that _simultaneity_ of events is not conserved across inertial frames
	- Galilean relativity can be obtained by letting $c\rightarrow\infty$

# Intervals and Minkowski space
- For _any two events_ $1$ and $2$, with a separation $\Delta\vec{x}$, the _interval_ defined in a given inertial frame is:
$$(\Delta s)^2\equiv(\Delta t)^2-(\Delta x)^2-(\Delta y)^2-(\Delta z)^2=(\Delta t)^2-\sum_{i,j}\delta_{ij}\Delta x^i\Delta x^j$$
- If the two events are _infinitely close_:
$$ds^2=dt^2-dx^2-dy^2-dz^2$$
- The _coordinate separation_ $\Delta x^\alpha$ can _depend on the frame_ $(\Delta x^\alpha\neq\Delta x^{\alpha'})$

- It can be proven that the interval is _invariant between frames_
	- If $ds=0$, $ds'=0$, and as they are of the same order, $ds^2$ between two frames must be _proportional_ to each other
	- Due to the _homogeneity and isotropy of space and time_, the proportionality constant must only depend on the _magnitude of relative velocity_ between the two frames
	- By comparing the _ratios of proportionality constants_ for 3 frames, one concludes that the constant must be _unity_
$$\displaylines{ds^2=ds'^2 \\ (\Delta s)^2=(\Delta s')^2}$$
- One can classify the _separation between two events_ by the _square of the interval_:

| Interval         | Separation     |
| ---------------- | -------------- |
| $(\Delta s)^2>0$ | Timelike       |
| $(\Delta s)^2=0$ | Null/lightlike |
| $(\Delta s)^2<0$ | Spacelike               |

- From the _frame invariance_, one can regard the interval as the _square length_ of $\Delta\vec{x}$:
$$(\Delta\vec{x})^2\equiv(\Delta s)^2=(\Delta s')^2$$
- This can be _negative_ (for spacelike events)

- Just as _Euclidean distance_ is fundamental to geometry in flat [[Geometric principles in Newtonian mechanics|3-space]], the interval is fundamental to the geometry of _spacetime, or Minkowski space_

## Tensor algebra in Minkowski space
- Many [[Geometric principles in Newtonian mechanics|definitions in 3-space]] still _apply_
- A _tensor_ $\bm{T}(\_,\_)$ is still a _real-valued linear function of vectors_ in Minkowski spacetime
	- The _rank_ is still the number of vectors needed to produce a _scalar_
- The _inner/dot product_ of two 4-vectors is still:
$$\vec{A}\cdot\vec{B}\equiv\frac{1}{4}\left[(\vec{A}+\vec{B})^2-(\vec{A}-\vec{B})^2\right]$$
	- where the squared length is simply the _interval_
- The _metric tensor_ in spacetime is still a _rank 2 tensor_ for 2 4-vectors:
$$\bm{g}(\vec{A},\vec{B})=\vec{A}\cdot\vec{B}$$
- Then any vector is then a _rank 1 tensor_
- Similarly, the [[Geometric principles in Newtonian mechanics#Tensor algebra|tensor product and contraction]] are defined in the same way as Euclidean space

# 