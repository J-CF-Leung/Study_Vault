>[!info] Notation
> As the speed of light is _constant_, one can use _geometrised units_:
> $$c=2.99792458\times10^8\,\text{m}\,\text{s}^{-1}=1$$

- [ ] Lorentz transformations📅 2023-10-10 ⏫ 
- [ ] Accelerating frames and rapidity 📅 2023-10-10 ⏫ 
- [ ] Length contraction and time dilation 📅 2023-10-10 ⏫ 

- In _Newtonian mechanics_, when two frames travel with _relative velocity_ $v$, one performs a _Galilean transformation_:
$$ct'=ct \hspace{1cm}x'=x-vt\hspace{1cm}y'=y\hspace{1cm}z'=z$$
- The notion of time is _absolute_

- This _distance between simultaneous events_ is _constant_
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

- From the _frame invariance_, one can _define_ the interval as the _square length_ of $\Delta\vec{x}$:
$$(\Delta\vec{x})^2\equiv(\Delta s)^2=(\Delta s')^2$$
- This can be _negative_ (for spacelike events)

- Just as _Euclidean distance_ is fundamental to geometry in flat [[Geometric principles in Newtonian mechanics|3-space]], the interval is fundamental to the geometry of _spacetime, or Minkowski space_

## Tensor algebra in Minkowski spacenot done
due after today
due before in one week
short mode
hide edit button
hide backlink
- Many [[Geometric principles in Newtonian mechanics|definitions in 3-space]] still _apply_
- A _tensor_ $\textbf{T}(\_,\_)$ is still a _real-valued linear function of vectors_ in Minkowski spacetime
	- The _rank_ is still the number of vectors needed to produce a _scalar_
- The _inner/dot product_ of two 4-vectors is still:
$$\vec{A}\cdot\vec{B}\equiv\frac{1}{4}\left[(\vec{A}+\vec{B})^2-(\vec{A}-\vec{B})^2\right]$$
	- where the squared length is simply the _interval_
- The _metric tensor_ in spacetime is still a _rank 2 tensor_ for 2 4-vectors:
$$\textbf{g}(\vec{A},\vec{B})=\vec{A}\cdot\vec{B}$$
- Then any vector is then a _rank 1 tensor_
- Similarly, the [[Geometric principles in Newtonian mechanics#Tensor algebra|tensor product and contraction]] are defined in the same way as Euclidean space

# Component-free particle kinetics
- When a particle _accelerates_ under a force, it still _carries an ideal clock ticking uniformly_ 
	- uniform compared to objects _at rest_
- The time experienced by this clock $\tau$ is known as the _proper time_

- The particle's path through space-time, or the _world-line_, can be denoted by $\mathcal{P}(\tau)$
	- As always, the curve through spacetime is _frame-independent_
- The _inertial frame_ where the particle is _momentarily at rest_ is known as the _momentary co-moving/rest frame_
- For an _interval in proper time_ $\Delta\tau$, that interval is _equal to coordinate time interval in the momentary rest frame_ $\Delta t$
- From the definition of the momentary rest frame, $\Delta x^1=\Delta x^2=\Delta x^3=0$

- From this, the _invariant interval_ is $(\Delta s)^2=(\Delta t)^2=(\Delta \tau)^2$
- Therefore, the particle's _proper time_ $\tau$ is equal to $s$ _along the world-line_

- One then defines another _frame-independent_ 4-vector, known as the _4-velocity_:
$$\vec{u}\equiv\frac{d\mathcal{P}}{d\tau}=\frac{d\vec{x}}{d\tau}$$
![[World-line.png|300]]
- It is along the _tangent of the world-line_
- Its _squared length_ is:
$$|\vec{u}|^2=\frac{d\vec{x}\cdot d\vec{x}}{d\tau^2}=\frac{ds^2}{d\tau^2}=1$$
- Therefore, it is _always a unit tangent along the world-line_

- One can then define the _4-momentum_ using the _rest mass_ $m$:
$$\vec{p}\equiv m\vec{u}=m\frac{d\vec{x}}{d\tau}\equiv\frac{d\vec{x}}{d\zeta}$$
- $\zeta$ is a _renormalised_ version of proper time, $\zeta\equiv\tau/m$
- Any _position-independent renormalised parameter_ is known as an _affine parameter_ for the world-line
- The above expression also suggests:
$$|\vec{p}|^2=m^2$$

- For particles with _zero rest mass_, to define a 4-momentum, let $m, d\tau\to0$ such that $d\zeta$ remains _finite_, and $d\vec{x}/d\zeta$ exists
- However, $\vec{u}=\vec{p}/m$ simply remains _infinite_ and undefined, since $\tau=m\zeta=0$
- From this, the _world-line of a zero rest mass particle is null_
- By contrast, the world-line of a _finite rest-mass particle_ is _time-like_

- Similar to non-relativistic 3-space, there is a _law of conservation of 4-momentum_
	- A relation between _geometric objects_ (4-vectors)
![[4-momentum conservation.png|350]]
- Given a set of _initial particles_ $\{A\}$ interacting in region $\mathcal{V}$, and a set of _final particles_ $\{\bar{A}\}$:
$$\sum_A \vec{p}_A=\sum_{\bar{A}}=\vec{p}_{\bar{A}}$$

- If one wishes to _change_ a particle's 4-momentum, one must act on it with a _4-force_:
$$\vec{F}=\frac{d\vec{p}}{d\tau}$$
- From the _invariance of rest-mass_:
$$0=\frac{d(m^2)}{d\tau}=\frac{d|\vec{p}^2|}{d\tau}=2\vec{p}\cdot\vec{F}$$
- Hence, _4-force is always orthogonal to 4-momentum_

## The Lorentz force law
- The Lorentz force for a particle with _charge_ $q$ and rest mass $m\neq0$ in an electromagnetic field, in _Newtonian_ space-time is:
$$\bm{F}=q(\bm{E}+\bm{v}\times\bm{B})$$
- It is _linear in $\bm{v}$_ and _proportional_ to $q$
- Therefore one expects that the _electromagnetic 4-force_ behaves similarly, and can thus be written as a _linear relationship_ using a _second-rank tensor_:
$$\frac{d\vec{p}}{d\tau}=\vec{F}(\_)=q\textbf{F}(\_,\vec{u})$$
- Due to the _orthogonality_ between 4-force and 4-momentum/velocity:
$$\vec{u}\cdot\vec{F}=\vec{F}(\vec{u})=q\textbf{F}(\vec{u},\vec{u})=0$$
- Hence, $\textbf{F}$ is _anti-symmetric_, or $\textbf{F}(\vec{A},\vec{B})=-\textbf{F}(\vec{B},\vec{A})$

# Component representation
## Lorentz reference frame
- In Minkowski spacetime, with an _inertial reference frame_, one defines a _Lorentz coordinate system_ $\{t,x,y,z\}=\{x^0,x^1,x^2,x^3\}$, with a set of _Lorentz basis vectors_ $\{\vec{e}_t,\vec{e}_x,\vec{e}_y,\vec{e}_z\}=\{\vec{e}_0,\vec{e}_1,\vec{e}_2,\vec{e}_3\}$
- The basis vector $\vec{e}_\alpha$ points _along_ the $x^\alpha$ coordinate direction, which is _orthogonal to all other directions_
- They have _squared length_ $1$ for $\alpha=0$, and $-1$ for $\alpha=1,2,3$:
$$\vec{e}_\alpha\cdot\vec{e}_\beta=\eta_{\alpha\beta}$$
- Here, $\eta_{\alpha\beta}$ is the _analog of the Kronecker delta in Minkowski spacetime_:
$$\eta_{00}=1 \hspace{1cm} \eta_{11}=\eta_{22}=\eta_{33}=-1 \hspace{1cm} \eta_{\alpha\beta}=0\text{ if }\alpha\neq\beta$$
- _Any_ coordinate system where $\vec{e}_\alpha\cdot\vec{e}_\beta=\eta_{\alpha\beta}$ is said to be _orthonormal_
- From this, [[Geometric principles in Newtonian mechanics#Component representation|component representations in Euclidean 3-space]] _do not hold in Minkowski spacetime_ 
- One must introduce _contravariant components_ $T^{\alpha\beta\gamma}$ and _covariant components_ $T_{\alpha\beta\gamma}$

## Tensor index kung-fu
- A vector/tensor's _contravariant components_ are defined as its _expansion coefficients_ in the basis:
$$\vec{A}\equiv A^\alpha\vec{e}_\alpha \hspace{1.5cm} \textbf{T}=T^{\alpha\beta\gamma}\,\vec{e}_\alpha\otimes\vec{e}_\beta\otimes\vec{e}_\gamma$$
- Indices are to be summed when they are _repeated with one up and one down__

- The _covariant_ components are defined as:
$$A_\alpha\equiv\vec{A}(\vec{e}_\alpha)=\vec{A}\cdot\vec{e}_\alpha \hspace{1.5cm}T_{\alpha\beta\gamma}\equiv\textbf{T}(\vec{e}_\alpha,\vec{e}_\beta,\vec{e}_\gamma)$$
- There is also a set of basis vectors $\{\vec{e}^\alpha\}$ that is _dual_ to $\{\vec{e}_\alpha\}$

- From this definition, the _metric tensor_ has the _covariant components_ $g_{\alpha\beta}=\vec{e}_\alpha\cdot\vec{e}_\beta=\eta_{\alpha\beta}$
- The covariant components can then be _calculated from its contravariant components_:
$$T_{\lambda\mu\nu}=T^{\alpha\beta\gamma}g_{\lambda\alpha}g_{\mu\beta}g_{\nu\gamma}$$
- This implies that when _lowering a spatial index_, the sign _flips_, while _lowering a temporal index leaves it unchanged_:
$$\displaylines{i,j,k=1,2,3 \\ T_{ijk}=-T^{ijk}\hspace{1cm}T_{0jk}=T^{0jk}\hspace{1cm}T_{00k}=-T^{00k}\hspace{1cm}T_{000}=T^{000}\\ g_{jk}=g^{jk}=-1\hspace{1cm}g_{0k}=g^{0k}=0\hspace{1cm}g_{00}=g^{00}=+1}$$
- The special case is the _metric tensor_, where both types of components equal $\eta_{jk}$
- From this, one can find what happens when _raising_ an index:
$$T^{\alpha\beta\gamma}=T_{\lambda\mu\nu}g^{\lambda\alpha}g^{\mu\beta}g^{\nu\gamma}$$
- One can then define _mixed components_ of a tensor:
$$T^{\alpha}_{\mu\nu}=T^{\alpha\beta\gamma}g_{\mu\beta}g_{\nu\gamma}=T_{\lambda\mu\nu}g^{\lambda\alpha}$$
- The _mixed components of the metric_ are simply $g^\alpha_\beta=g_\alpha^\beta=\delta_{\alpha\beta}$

- The contravariant vomponents of an _outer product_ $\textbf{T}\otimes\textbf{S}$ is then $T^{\alpha\beta\gamma}S^{\mu\nu}$
- From this, one can find formulas for the _inner product_ and _scalar output of a tensor_
$$\vec{A}\cdot\vec{B}=A_\alpha B^\alpha=A^\alpha B_\alpha\hspace{1.5cm}\textbf{T}(\bm{A},\bm{B},\bm{C})=T_{\alpha\beta\gamma}A^\alpha B^\beta C^\gamma=T^{\alpha\beta\gamma}A_\alpha B_\beta C_\gamma$$

- The _covariant components_ of a _contraction_ may be written as $R^\mu_{\alpha\mu\beta}$
- The _contravariant_ ones for the same contraction are then $R^{\alpha\mu\beta}_\mu$

- Laws can also be written in terms of this index notation, such as the [[#The Lorentz force law|Lorentz force law]]:
$$\frac{dp_\mu}{d\tau}=qF_{\mu\nu}u^\nu$$

- The formula for the inner product also leads to an expression for the _invariant interval_ between two events at $x^\alpha$ to $x^\alpha+dx^\alpha$:
$$ds^2=g_{\alpha\beta}dx^\alpha dx^\beta=dt^2-dx^2-dy^2-dz^2$$
- This is the _special relativistic line element_

# Particle kinetics in index notation
- Let there be a particle with _4-velocity_ $\vec{u}$ and _4-momentum_ $\vec{p}$
- Choose a _Lorentz frame_ with _coordinates_ $x^\alpha$ with _basis vectors_ $\{\vec{e}_\alpha\}$
- The components of 4-velocity:
$$u^\alpha=\frac{dx^\alpha}{d\tau}$$
- This implies that the components of _3-velocity_ are:
$$v^j\equiv\frac{dx^j}{dt}=\frac{dx^j/d\tau}{dt/d\tau}=\frac{u^j}{u^0}$$
- From the fact that $|\vec{u}|^2=1$, one gets:
$$u_0=\gamma\hspace{1.5cm}u^j=\gamma v^j$$
- where $\gamma$ is the _Lorentz factor_:
$$\gamma=\frac{1}{\sqrt{1-\delta_{ij}v^iv^j}}=\frac{1}{\sqrt{1-|\bm{v}|^2}}$$
- This 3-velocity lives in a _3-dimensional Euclidean slice_ of Minkowski spacetime, where $t=\text{const.}$
	- It is sometimes called the _slice of simultaneity_ for this specific Lorentz frame
	- The _spatial part_ of $\vec{u}$ can be thought as the 3-vector $\bm{u}=\gamma\bm{v}$
![[3-velocity.png|400]]

- The particle's _relativistic energy_ is described by $p^0$:
$$\mathcal{E}\equiv p^0=m\gamma=\frac{m}{\sqrt{1-|\bm{v}|^2}}$$
- For $|\vec{v}|<<1$:
$$\mathcal{E}\approx m+\frac{1}{2}m|\bm{v}|^2$$
- This is the _sum_ of the _rest energy_ $m$ and _klnetic energy_ $E=mv^2/2$

- The particle's _3-momentum_ is then:
$$\bm{p}=m\bm{u}=\gamma m\bm{v}=\mathcal{E}\bm{v}$$
- For a _photon_, $\mathcal{E}=\hbar\omega$, and since $|\vec{p}|^2=m^2=0$, $\bm{p}=\hbar\omega\hat{\bm{n}}$

- Conservation of energy and momentum

$$\mathcal{E}=$$

# Lorentz transformations

# Spacetime diagrams for boosts

# Derivatives

# Electromgnetism