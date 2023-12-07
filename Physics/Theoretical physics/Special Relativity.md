>[!info] Notation
> As the speed of light is _constant_, one can use _geometrised units_:
> $$c=2.99792458\times10^8\,\text{m}\,\text{s}^{-1}=1$$

- In _Newtonian mechanics_, when two frames travel with _relative velocity_ $v$, one performs a _Galilean transformation_:
$$ct'=ct \hspace{1cm}x'=x-vt\hspace{1cm}y'=y\hspace{1cm}z'=z$$
- The notion of time is _absolute_

- This _distance between simultaneous events_ is _constant_

- S.R. is a _limiting case_ of [[General Relativity]] (GR)
	- It can be described in the language of _manifolds_
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
![[Lightcone structure.png]]

- From the _frame invariance_, one can _define_ the interval as the _square length_ of $\Delta\vec{x}$:
$$(\Delta\vec{x})^2\equiv(\Delta s)^2=(\Delta s')^2$$
- This can be _negative_ (for spacelike events)

- Just as _Euclidean distance_ is fundamental to geometry in flat [[Geometric principles in Newtonian mechanics|3-space]], the interval is fundamental to the geometry of _spacetime, or Minkowski space_

## Tensor algebra in Minkowski space
- Many [[Geometric principles in Newtonian mechanics|definitions in 3-space]] still _apply_
- A _tensor_ $\textbf{T}(\_,\_)$ is still a _real-valued linear function of vectors_ in Minkowski spacetime
	- The _rank_ is still the number of vectors needed to produce a _scalar_
- The _inner/dot product_ of two 4-vectors is still:
$$\vec{A}\cdot\vec{B}\equiv\frac{1}{4}\left[(\vec{A}+\vec{B})^2-(\vec{A}-\vec{B})^2\right]$$
	- where the squared length is simply the _interval_
- Like in Euclidean 3-space, the _inner product_ is as _frame-independent_ as the _4-vectors themselves_

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
	- This also means that _4-velocity_ is orthogonal to _4-acceleration_

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
- They have _squared length_ $1$ for $\alpha=0$, and $-1$ for $\alpha=1,2,3$, giving the _Minkowski metric_:
$$g_{\alpha\beta}=\vec{e}_\alpha\cdot\vec{e}_\beta=\eta_{\alpha\beta}$$
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

- Special case: the _vector_:
$$A^\alpha=(A^0,A^1,A^2,A^3)\hspace{1cm}A_\alpha=(A^0,-A^1,-A^2,-A^3)$$

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
- Choose a _Lorentz frame_ with _coordinates_ $x^\alpha$ with _basis vectors_ $\{\vec{e}_\alpha\}$
## 4-velocity, momentum, and acceleration
- Let there be a particle with _4-velocity_ $\vec{u}$ and _4-momentum_ $\vec{p}$
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
- Applying another derivative gives the _4-acceleration_:
$$\vec{a}=\frac{d\vec{u}}{d\tau}$$
![[3-velocity.png|400]]

- The particle's _relativistic energy_ is described by $p^0$:
$$\mathcal{E}\equiv p^0=m\gamma=\frac{m}{\sqrt{1-|\bm{v}|^2}}$$
- For $|\vec{v}|<<1$:
$$\mathcal{E}\approx m+\frac{1}{2}m|\bm{v}|^2$$
- This is the _sum_ of the _rest energy_ $m$ and _klnetic energy_ $E=mv^2/2$

- The particle's _3-momentum_ is then:
$$\bm{p}=m\bm{u}=\gamma m\bm{v}=\mathcal{E}\bm{v}$$
- For a _photon_, $\mathcal{E}=\hbar\omega$, and since $|\vec{p}|^2=m^2=0$, $\bm{p}=\hbar\omega\hat{\bm{n}}$

- This demonstrates that _every 4-vector_ can be _split_ in a "3+1" manner, as a _vector_ and a _scalar_
- The 3+1 split of 4-momentum gives the _energy_ and _momentum_
- From the _conservation of 4-momentum_, one gets the _conservations of 3-momentum and energy_:
$$\sum_\bar{A}\bm{p}_\bar{A}=\sum_A\bm{p}_A\hspace{1.5cm}\sum_\bar{A}\mathcal{E}_\bar{A}=\sum_A\mathcal{E}_A$$
- Energy and momentum are _frame-dependent_ as they are simply _components_

- Let there be a _particle_ with some 4-momentum $\vec{p}$, _observed_ by someone with 4-velocity $\vec{U}$
- As the 4-velocity has components $U^0=1$ and $U^i=0$, the _measured energy_ is $p^0$ in the _observer's frame_, given by:
$$\mathcal{E}=\vec{p}\cdot\vec{U}$$
- $\mathcal{E}$ is from the _observer's frame_, but the _inner product is frame-independent_

## The Doppler Effect
- Let there be some _moving atom_ with _ordinary velocity_ $\bm{v}$ emitting a photon at an _observer_, whose direction is $\bm{n}$:
![[Doppler effect.png]]

- By using the above formula using the inner product _evaluated in the receiver's frame_, one gets:
$$\frac{\nu_\text{rec}}{\nu_\text{em}}=\frac{\sqrt{1-|\bm{v}|^2}}{1-\bm{v}\cdot\bm{n}}$$
- If $\bm{v}//\bm{n}$, and $\bm{v}$ is going _towards_ the observer:
$$\frac{\nu_\text{rec}}{\nu_\text{em}}=\sqrt{\frac{1+|\bm{v}|}{1-|\bm{v}|}}$$
- If it is going _away_ from the observer, the signs are _flipped_

- If the particle has _mass_ and is emitted with velocity $\bm{V}$:
$$\frac{\mathcal{E}_\text{rec}}{\mathcal{E}_\text{em}}=\frac{\sqrt{1-|\bm{v}|^2}}{1-\bm{v}\cdot\bm{V}}$$

## Velocity addition
- Let there be two particles travelling at _ordinary velocities_ $\bm{v}$ and $\bm{v}'$
- One may want to _transform_ to the frame of the particle travelling at $\bm{v}$, and find the _transformed velocity_ of $\bm{v}'$, denoted $\bm{v}_f$

- Use the _invariance of the inner product_ $\vec{v}\cdot\vec{v}'$:
$$\gamma_f=\gamma\gamma'(1-\bm{v}\cdot\bm{v}')$$
- If $\bm{v}$ and $\bm{v}'$ face the _same direction_:
$$v_f=\frac{v+v'}{1+vv'}$$

# Lorentz transformations
- Let there be _two different inertial frames_ with coordinates $\{x^\alpha\}$ and $\{x^\bar{\mu}\}$, and basis vectors $\{\vec{e}_\alpha\}$ and $\{\vec{e}_\bar{\mu}\}$
- Write the _transformations_ as:
$$\vec{e}_\alpha=\vec{e}_\bar{\mu}{\Lambda^\bar{\mu}}_\alpha\hspace{1.5cm}\vec{e}_\bar\mu=\vec{e}_\alpha{\Lambda^\alpha}_\bar\mu$$
- It is obvious that they are _inverses_ of each other:
$${\Lambda^\bar\mu}_\alpha {\Lambda^\alpha}_\bar\nu={\delta^\bar\mu}_\bar\nu\hspace{1.5cm}{\Lambda^\alpha}_\bar\mu {\Lambda^\bar\mu}_\beta={\delta^\alpha}_\beta$$
- As in Euclidean 3-space, the _orthonormality_ of the bases dictates that the transformation is _orthogonal_ (reflection or rotation), and the same _holds in Minkowski spacetime_

- By using the transformation laws:
$$g_{\alpha\beta}={\Lambda^\bar\mu}_\alpha {\Lambda^\bar\nu}_\beta \,g_{\bar\mu\bar\nu}\hspace{1.5cm} g_{\bar\mu\bar\nu}={\Lambda^\alpha}_\bar\mu {\Lambda^\beta}_\bar\nu \,g_{\alpha\beta}$$
- Any matrix $L$ satisfying this is known as a _Lorentz transformation_

- The transformation laws for the _components_ of 4-vectors:
$$A^\bar\mu={\Lambda^\bar\mu}_\alpha A^\alpha\hspace{1.5cm}T^{\bar\mu\bar\nu\bar\rho}={\Lambda^\bar\mu}_\alpha{\Lambda^\bar\nu}_\beta{\Lambda^\bar\rho}_\gamma \,T^{\alpha\beta\gamma}$$
- As long as the _spacetime origins_ of the frames _coincide_, then the vectors to some event will have _components_ equal to the _spacetime coordinates_, such that the _coordinates also follow the above transformation laws_:
$${x^\bar\mu}={\Lambda^\bar\mu}_\alpha x^\alpha$$

- The _product_ of two Lorentz transformations gives _another_ Lorentz transformation
- Hence, all Lorentz transformations form the _Lorentz group_

- Vectors are then _classified_ as null, timelike, or spacelike based on their norm:
$$\eta_{\mu\nu}V^\mu V^\nu\begin{cases}>0 &\text{timelike} \\ <0 &\text{spacelike} \\ =0 &\text{null}\end{cases}$$
- They are classified as _future-pointing_ if $V^0>0$, and _past-pointing_ if $V^0<0$
## The Psuedo-Riemannian manifold \[GR\]
- In the language of [[General Relativity]], a _Loentz transformation_ from $\{x^\mu\}$ to $\{x^{\mu'}\}$ must _leave the metric unchanged_
	- Corresponding to _going between intertial frames_
$$\eta_{\mu\nu}=\pd{x^\rho}{x^{\mu'}}\pd{x^\sigma}{x^{\nu'}}\eta_{\rho\sigma}$$
- Stuff (check Weinberg)

- The Lorentz transformations must then be _linear_, and _satisfy_:
$$\displaylines{x^{\mu'}=\tenscom{\Lambda}{\mu'}{\nu}x^\nu+a^{\mu'} \\ \eta_{\mu\nu}=\tenscom{\Lambda}{\rho}{\mu}\tenscom{\Lambda}{\sigma}{\nu}\eta_{\rho\sigma} \\ \tenscom{\Lambda}{\rho}{\mu}=\pd{x^\rho}{x^{\mu'}} }$$
- With the _first condition_, the transformation _maps striaight lines onto straight lines_
	- With _non-zero_ $a^{\mu'}$, the transformation is in the _inhomogeneous affine group_
	- With $a^{\mu'}=0$, the transformation is in the _homogeneous affine group_
- The _second condition_ maintains the _constancy of the speed of light_, and _eliminates dilations_

- The group of _all such possible transformations_ is the _Poincare group_ or the _inhomogeneous Lorentz group_
- With $a^{\mu'}=0$, they belong to the _homogeneous Lorentz group_


## Boosts
- A specific type of Lorentz transformation is known as the _pure boost_:
$${\Lambda^\bar\mu}_\alpha=\pmatrix{\gamma&-\beta\gamma&0&0\\-\beta\gamma&\gamma&0&0\\0&0&1&0\\0&0&0&1}\hspace{1.5cm}{\Lambda^\alpha}_\bar\mu=\pmatrix{\gamma&\beta\gamma&0&0\\\beta\gamma&\gamma&0&0\\0&0&1&0\\0&0&0&1}$$
- $\gamma$ is the [[#Particle kinetics in index notation|Lorentz factor]] previously derived:
$$|\beta|<1\hspace{1cm}\gamma=\frac{1}{\sqrt{1-\beta^2}}$$

- This gives the _change of coordinates_:
$$\displaylines{\bar{t}=\gamma(t-\beta x)\hspace{1cm}\bar x=\gamma(x-\beta t)\hspace{1cm}\bar y=y\hspace{1cm}\bar z=z\\ t=\gamma(\bar t+\beta\bar x)\hspace{1cm}x=\gamma(\bar x+\beta\bar t)\hspace{1cm}y=\bar y\hspace{1cm}z=\bar z}$$
- If there is a particle _at rest_ at $x_0$ _in the unbarred frame_, $\bar{x}=\gamma x_0-\beta\bar{t}$
- In other words, an observer _at rest in the unbarred frame_ sees the _barred frame_ moving at $\bm{v}=+\beta\bm{e}_x$

- A boost along some _unit vector_ $\hat{\bm{n}}$ can be written as follows:
$${\Lambda^\bar0}_0=\gamma\hspace{1cm}{\Lambda^\bar\mu}_0={\Lambda^\bar0}_\mu=\beta\gamma n^\mu \hspace{1cm} {\Lambda^\bar\mu}_\nu={\Lambda^\bar\nu}_\mu=(\gamma-1)n^\mu n^\nu+\delta^{\mu\nu}$$
- Derivation: 
	- _Split_ positions into _parallel and perpendicular components_, then express $x^\bar{\mu}$ as a linear combination of $x^\nu$
	- Alternatively, apply _pure rotations_ along with the _boost along a spatial axis_

- As for _pure rotations_, they can be represented by:
$${\Lambda^\bar\mu}_\alpha=\pmatrix{1&0&0&0\\0&{R^1}_1&{R^1}_2&{R^1}_3 \\ 0&{R^2}_1&{R^2}_2&{R^2}_3 \\ 0&{R^3}_1&{R^3}_2&{R^3}_3}$$
- Here, $R$ is a _rotation matrix_ in Euclidean 3-space
- One can show that the _general_ Lorentz transformation is a _sequence_ of _pure boosts_, _pure rotations_, and _pure inversions_
## Rapidity
- One can define a _rapidity_ $\psi$ such that $\beta=\tanh\psi$
- Then one finds that:
$$\gamma=\cosh\psi \hspace{1.5cm}\beta\gamma=\sinh\psi$$
- One can then _rewrite the Lorentz boosts_:
$$\displaylines{{\Lambda^\bar\mu}_\alpha=\pmatrix{\cosh\psi&-\sinh\psi&0&0\\-\sinh\psi&\cosh\psi&0&0\\0&0&1&0\\0&0&0&1}\\ \bar{t}=t\cosh\psi-x\sinh\psi \hspace{1cm}\bar x=x\sinh\psi-t\cosh\psi\hspace{1cm}\bar y=y\hspace{1cm}\bar z=z}$$
- This is like a _rotation_ in Minkowski space, but with _hyperbolic_ angles

- When performing [[#Velocity addition|velocity addition]], one can also treat it as a _series of successive Lorentz transforms_:
$$\displaylines{\bar{\bar x}=\bar \gamma(\bar x-\bar\beta\bar t)\hspace{1.5cm}\bar{\bar t}=\bar\gamma(\bar t-\bar\beta\bar x) \\ \bar x=\gamma(x-\beta t)\hspace{1.5cm}\bar t=\gamma(t-\beta x)} $$
- By substituting the _rapidities_ into the transformations, one finds:
$$\bar{\bar x}=x\sinh(\psi+\bar\psi)-t\cosh(\psi+\bar\psi)$$
## Loss of simultaneity
- Consider the Lorentz boost for a _time interval_:
$$\Delta \bar t=\gamma(\Delta t-\beta\Delta x)$$
- One can see that if events $A$ and $B$ are _simultaneous_ in $S$, they _may not be simultaneous_ in $S'$
- However, provided their separation is _timelike_, the _sign_ of $\Delta t$ is conserved, or the _causality_ of the events is _Lorentz invariant_


## Time dilation and length contraction
- Consider an object of _proper length_ $l_0$ in frame $(\bar{t},\bar{x},\bar{y},\bar{z})$, lying along $\bar{x}$
	- Let the object go from points $A$ to $B$, so $\bar{x}_B(\bar t)-\bar x_A(\bar t)=l_0$
- If an observer in the frame $(t,x,y,z)$ performs the _length measurement_ $x_B(t)-x_A(t)$, from the transformations one finds that the length is _contracted_:
$$l=x_B(t)-x_A(t)=\frac{l_0}{\gamma}<l_0$$
- For a _length measurement_, one is measuring the interval between _two events in a slice of simultaneity in that frame_

- Consider an _ideal clock_ at _rest_ in frame $(\bar{t},\bar{x},\bar{y},\bar{z})$, measuring _proper time_ $T_0$
- For an observer in the frame $(t,x,y,z)$ performs the _time elapsed_ in their frame _while the clock ticks_ $T_0$, they find that:
$$T=\gamma T_0>T_0$$
- From that observer's perspective, a _moving clock runs slower_

## Acceleration and rapidity
- Let the _velocity_ of frame $\{\vec{e}_\bar\mu\}$ _vary in time_
- Taking the _derivative_ of the _velocity 4-vector_ with respect to _proper time_:
$$\vec{a}=\frac{d\vec{u}}{d\tau}$$
- Denoting the _3-acceleration_ as $\bm{a}\equiv d\bm{v}/dt$, the _4-acceleration_ can be _split_:
$$\vec{a}=(\gamma^4|\bm{v}||\bm{a}|,\gamma^4|\bm{v}||\bm{a}|\bm{v}+\gamma^2\bm{a})$$
- For _constant $m$_, the [[#Particle kinetics in index notation|4-force]] $\vec{F}=m\vec{a}$
- One can _verify_ that $\vec{v}\cdot\vec{a}=0$
	- Still a _component-free_ result

- One can _transform_ to the instantaneous rest frame of the particle to get the _proper acceleration_ $\bm{\alpha}$

- Given that a frame $\{\vec{e}_\bar\mu\}$ has some _acceleration_ $a(t)$ as observed by $\{\vec{e}_\alpha\}$, and $v(t=0)=0$, the _rapidity_ of the Lorentz transformation is given by:
$$\psi=\int a(t)\,dt$$
## Velocity transformation
- As _any 4-vectors_ transform according to the laws of a Lorentz transformation, the _components of velocities across different inertial frames also transform_:
$$u'^\mu=\tenscom{\Lambda}{\mu}{\nu}u^\nu$$
- With a boost of Lorentz factor $\gamma$ along the $x-$axis:
$$\pmatrix{\gamma_{u}' \\ \gamma'_{u}\dot{x}_{u'}^1 \\ \gamma'_{u}\dot{x}_{u'}^2 \\ \gamma'_{u}\dot{x}_{u'}^3}=\pmatrix{\gamma&-\beta\gamma&0&0 \\ -\beta\gamma&\gamma&0&0 \\ 0&0&1&0 \\ 0&0&0&1}\pmatrix{\gamma_{u} \\ \gamma_{u}\dot{x}_{u}^1 \\ \gamma_{u}\dot{x}_{u}^2 \\ \gamma_{u}\dot{x}_{u}^3}$$
- This relates the _Lorentz factors_:
$$\frac{\gamma_u'}{\gamma_u}=\gamma(1-\beta\dot{x}_u^1)$$

# Geodesics and kinetics in Minkowski space \[GR\]
- For a _free particle_, it has _zero 4-acceleration_:
$$\frac{DU^\mu}{D\tau}=0$$
- In _global Cartesian coordinates_, as the [[General Relativity#The metric connection|metric connection]] vanishes, this reduces to $DU^\mu/D\tau=0$

- The _derivative along the world-line_ (with $\tau$ as the _affine parameter_):
$$\frac{DU^\mu}{D\tau}=0$$
- This means the _tangent vector of the world-line is parallel transported_

- In other words, a _free particle in Minkowski spacetime moves along a [[General Relativity#Geodesics, proper time, and affine parameters|geodesic]]_

- From above, _accleration and velocity_, as well as _force and momentum_ are always _orthogonal_:
$$F^\mu p_\mu=a^\mu u_\mu=0$$

# Spacetime diagrams for boosts
- Boost angle

- Invariant hyperbolae

# Derivatives
- Directional derivative

- Differentiation rules

- d'Alembertian:
$$\Box^2=\nabla_0^2-\nabla^2$$

- Levi-Civita tensor

# Energy-momentum tensor
- Recall the _energy-momentum_ 4-vector $\vec{p}$
	- _Timelike_ component $p^0$ is _energy_ $E$
$$\displaylines{p^\mu=(\gamma m,\gamma\bm{p}) \\ p_\mu p^\mu=m^2}$$
- The _4-force_:
$$f^\mu=\frac{dp^\mu}{d\tau}=m\frac{d^2x^\mu}{d\tau^2}$$

- For some _collection of particles_, information on _energy and momentum_ is better conveyed using a _tensor_
	- Example: The _stress_ and _energy density_ of some fluid
	- Derived from [[Classical Field Theory#The energy-momentum tensor|Classical Field Theory]]

- Introduce the _energy-momentum tensor_ $T^{\mu\nu}$, as the _flux_ of 4-momentum component $p^\mu$ on a _surface of constant_ $x^\nu$

- The _rest frame energy density_ $\rho$ of the fluid is _flux of_ $p^0$ (energy) in the $x^0$ (time) direction, hence is $T^{00}$
- Similarly, $T^{i0}=T^{0i}$ is the _momentum density_
- The _spacelike components_ $T^{ij}$ are the _stress_ on the fluid
	- $T^{ii}$ (no sum) gives the _pressure_ in the $i$th direction
	- $T^{ij}$ where $i\neq j$ give the _shearing_ terms
## Dust
- _Dust_ is a _collection of non-interacting particles_, which are _at rest relative to each other_
- The _rest energy density_ is $\rho_0$

- Define the _number flux four-vector_ $N^\mu=nU^\mu$, where $n$ is the _number density as measured in the rest frame_
	- $N^0$ is the _number density_, and $N^i$ is the _particle flux_ in the $x^i$ direction
	- The _four-velocity_ field $U^\mu$ is _uniform by definition_
- If each particle has _mass_ $m$, then $\rho_0=mn$

- In the _rest frame_, $\rho_0=N^0p^0$

- This motivates the expression for the _energy-momentum tensor for dust_:
$$T^{\mu\nu}_\text{dust}=\rho_0U^\mu U^\nu$$
- One can check that for some frame _moving relative to the dust_, $T^{00}=\gamma^2\rho_0$
	- Due to _length contraction_ and _gain in energy_
- In the _rest frame_, there is _no pressure_

## Perfect fluid
- A _perfect fluid_ in its _rest frame_ has some _energy density_ $\rho_0$ and _isotropic pressure_ $p$
- This leads to the fact that it is _diagonal in its rest frame_: 
$$T^{\mu\nu}=\pmatrix{\rho&0&0&0\\0&p&0&0\\0&0&p&0\\0&0&0&p}$$
- One can derive the general expression:
$$T^{\mu\nu}=(\rho+p)U^\mu U^\nu-p\eta^{\mu\nu}$$

## Conservation
p
# Electromgnetism
- [[Electrodynamics and Optics#Relativistic electrodynamics|Electrodynamics]] is _inherently relativistic_
	- The _speed of light_ is always in terms of _universal constants_

## 4-potential and field tensor
- Introduce the _4-potential_ $A_\mu$
	- The _timelike_ component $A^0=\Phi$, the [[Electrodynamics and Optics#Electrodynamics and Maxwell's Equations|electric potential]]
	- The _spacelike_ components $A^i=\bm{A}$, the [[Electrodynamics and Optics#The vector potential|magnetic vector potential]]
- One can then introduce the _field-strength tensor_:
$$F_{\mu\nu}=\partial_\mu A_\nu-\partial_\nu A_\mu$$

- It replicates [[Electrodynamics and Optics#Gauge transformations|gauge invariance]]:
$$\displaylines{A_\mu\to A_\mu+\partial_\mu \lambda(x) \\ F_{\mu\nu}\to F_{\mu\nu}}$$

- _All physical quantities_ must be _gauge invariant_

- The _components_ in a certain frame give:
$$\displaylines{F^{i0}=E^i \hspace{1cm} F^{ij}=-\epsilon^{ijk}B^k \\ F^{\mu\nu}=\pmatrix{0&-E^1&-E^2&-E^3 \\ E^1&0&-B^3&B^2 \\ E^2&B^3&0&-B^1 \\ E^3&-B^2&B^1&0}}$$

- Like 4-vectors, the field tensor also _Lorentz transforms_:
$$F'^{\mu\nu}=\tenscom{\Lambda}{\mu'}{\mu}\tenscom{\Lambda}{\nu'}{\nu}F^{\mu\nu}$$

- [[#The Lorentz force law]] is then expressed in terms of the field tensor:
$$\frac{Dp^\mu}{D\tau}=qF^{\mu\nu}u_\nu$$
- Writing out the components from above recreates the _classical result_

## Maxwell's equations
- The _antisymmetry_ of the field tensor can also be presented as:
$$\displaylines{\partial_\mu F_{\nu\lambda}+\partial_\nu F_{\lambda\mu}+\partial_\lambda F_{\mu\nu}=0 \\ \partial_{[\mu}F_{\nu\lambda]}=0}$$
- This _implies_:
$$\displaylines{\epsilon^{ijk}\partial_j E_k+\partial_0 B^i=0 \\ \partial_i B^i=0}$$
- These are _Faraday's Law_ and _Gauss' Law for magnetic fields_ from _Maxwell's equations_

- Introduce the _current 4-vector_ $\vec{J}$:
	- The _timelike_ component $J^0=\rho$ is the _charge density_
	- The _spacelike_ component $J^i=\bm{J}$, the _current density_
	- Comes from the fact that _total charge in a region is Lorentz invariant_
- The 4-vector is _divergenceless_, giving the _continuity equation_:
$$\partial_\mu J^\mu=0$$

- From [[Classical Field Theory#Electromagnetic fields|the Euler-Lagrange equation for the relevant Lagrangian]]:
$$\displaylines{\partial_\mu F^{\mu\nu}=J^\nu \\ \partial_\mu F^{\mu0}=\partial_i E^i=J^0=\rho \\ \partial_\mu F^{\mu j}=J^j \Longrightarrow \epsilon^{jik}\partial_i B_k=J^j+\partial_0 E^j}$$
## Gauge
- The [[Electrodynamics and Optics#Gauge transformations|Lorenz gauge]]:
$$\partial_\mu A^\mu=0$$
- In this gauge, the equation $\nabla_\mu F^{\mu\nu}=J^\nu$ can be _simplified_:
$$\Box^2 A^\mu=0$$

## In curved spacetime \[GR\]
- In _curved spacetime_, convert to _covariant derivatives_:
$$\displaylines{\nabla_\mu F_{\nu\lambda}+\nabla_\nu F_{\lambda\mu}+\nabla_\lambda F_{\mu\nu}=0 \\ \nabla_\mu F^{\mu\nu}=J^\nu}$$