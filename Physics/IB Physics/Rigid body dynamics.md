- Definition of a rigid body: A _multi-particle_ system where _all inter-particle distances are fixed_ (i.e. No deformation)
- The _location of all particles_ can be described by 6 coordinates:
	- Position of the _centre of mass_
	- 3 _Euler angles_, which give the _attitude_ w.r.t. Cartesian axes

## Angular momentum and the inertia tensor
- The _velocity_ is determined by the _velocity of the CM_ and the _angular velocity_ $\bm{\omega}$
- The _dynamics_ of the body is determined by its mass and the _inertia tensor_, relating _angular momentum_ $\bm{J}$ and $\bm{\omega}$

- The inertia tensor is a _generalisation of the moment of inertia_, an _intrinsic property_ of the body
- For a simply body spinning with a _fixed high-symmetry axis_, it becomes the moment of inertia $I$, with $J=I\omega$ and $T=I\omega^2/2$

- The _centre of mass_ moves like a _particle_ of mass $M$ under the resultant external force $\bm{F}_0$
- Same is true for _total angular momentum_:
$$M\bm{\ddot{R}}=\bm{F}_0 \hspace{1cm}\bm{\dot{J}}=\bm{G}_0$$
- The angular momentum is:
$$\bm{J}=\sum \bm{r}\wedge\bm{p}=\sum \bm{r}\wedge m(\bm{\omega}\wedge\bm{r})=\sum mr^2\omega-\sum m\bm{r}(\bm{\omega}\cdot\bm{r})$$
- Therefore, $\bm{J}$ is _not necessarily parallel_ to $\bm{\omega}$
- The inertia tensor is a _rank 2 tensor_
- This is a _tensor relationship_:
$$\displaylines{\bm{J}=\dunderline{I}\bm{\omega} \\\bm{J}_i=I_{ij}\omega_j \\ I_{ij}=\sum_\alpha m_\alpha[r_\alpha^2\delta_{ij}-(\bm{r_\alpha})_i(\bm{r}_\alpha)_j]}$$
- In _matrix notation_, the relationship is:
$$\begin{pmatrix} J_x \\ J_y \\ J_z \end{pmatrix}=\begin{pmatrix} \sum m(y^2+z^2) & -\sum mxy & -\sum mxz \\ -\sum mxy & \sum m(x^2+z^2) & -\sum myz \\ -\sum mxz & -\sum myz & \sum m(x^2+y^2) \end{pmatrix} \begin{pmatrix} \omega_x \\ \omega_y \\ \omega_z \end{pmatrix}$$
- The matrix is _real and symmetric_, hence can be _diagonalised_
- The _kinetic energy_ can be written as:
$$T=\frac{1}{2}\bm{J}\cdot\bm{\omega}$$


- As something rotates around a _fixed axis_, $\bm{J}$ can _precess_, meaning a _couple is needed to maintain the motion_
	- Couple is perpendicular to $\bm{J}$ and does _no work_
	- The same couple can be derived by _switching to a rotating frame_
- If the axis is _not about the centre of mass_, another _centripetal force_ is required

## The principal axes and the inertia ellipsoid
- The moment of inertia tensor has _3 eigenvalues and eigenvectors_
- The eigenvalues $(I_1,I_2,I_3)$ are the _moments of inertia_
- The eigenvectors $(\bm{e}_1,\bm{e}_2,\bm{e}_3)$ are the _principal axes_
	- They must be _mutually perpendicular_

- By splitting $\bm{\omega}$ into _components along the principal axes_:
$$T=\frac{1}{2}(I_1\omega_1^2+I_2\omega_2^2+I_3\omega_3^2)$$

- In $\omega-$space, _surfaces of constant energy_ give the _inertia ellipsoid_
- The axes have length $\propto 1/\sqrt{I_i}$
- Hence, the _smallest $I$_ gives the _longest axis_

- Here, the _gradient_ on the ellipsoid is:
$$\nabla_\omega T=\left(\pd{T}{\omega_1},\pd{T}{\omega_2},\pd{T}{\omega_3}\right)=\bm{J}$$
- Therefore, $\bm{J}$ is _perpendicular to the surface of constant $T$_

## Types of bodies, theorems and examples
- Rotational bodies come in _three types_:
	- Spherical tops: $I_1=I_2=I_3=I$
		- Inertia tensor is _the identity matrix scaled by $I$_
		- The body is _isotropic_, with arbitrary axis choice as long as they are orthogonal
	- Symmetrical tops: $I_1=I_2\neq I_3$
		- A _lens or disc_ shape is _oblate_
		- A _cigar_ shape is _prolate_
		- The $\bm{e}_3$ axis is _unique_, with the other 2 axes _arbitrary_ as long as they are _orthogonal_ to $\bm{e}_3$ and each other
	- Asymmetrical top: all 3 $I_i$ are different

- From looking at the sums, _no $I_i$ can be larger than the sum of the other two_

- Special case: the _lamina_, with $z=0$ and $I_1+I_2=I_3$, known as the _perpendicular axis theorem_

- For an axis _not about the centre of mass_, but is displacement $\bm{a}$ away and _parallel to a principal axis_:
$$I_a=\sum m(\bm{r}+\bm{a})\cdot(\bm{r}+\bm{a})=I_0+Ma^2$$
- Where $I_0$ is _about the centre of mass_, otherwise there is an extra term
- This is the _parallel axis theorem_

- Moment of inertia of _sphere_: $2Ma^2/5$
- _Thin rod_, around centre of mass: $Ml^2/12$
- _Rod_ with radius $a$: $I_1=I_2=Ma^2/4+Ml^2/12$

## Free precession
>[!quote]
>“To those who study the progress of exact science, the common spinning-top is a symbol of the labours and the perplexities of men.”
>-James Clerk Maxwell
- Suppose the body is _isolated_:
$$\bm{F}=\bm{G}=\bm{0}$$
- The _angular momentum is constant_
- If $\bm{J}$ and $\bm{\omega}$ are both _along a principal axis_, then it simply continues spinning in the same way

- If they do not lie along a principal axis, _the direction of $\omega$ varies in both space and w.r.t. the body_, known as _precession_
- The _magnitude can also change_

### Euler's equations
- Consider the relationship of rates of change between inertial and [[Newtonian dynamics and non-inertial frames#Rotating frame|rotating frames]]:
$$\left[\frac{d\bm{J}}{dt}\right]_{S_0}=\left[\frac{d\bm{J}}{dt}\right]_{S}+\omega\wedge\bm{J}$$
- Let there be a torque $\bm{G}$
- For $\bm{J}_S$, take _components of $\bm{J}$ and $\bm{\omega}$ along the principal axes_
- Then, one gets _Euler's equations_:
$$\displaylines{G_1=I_1\dot{\omega}_1+(I_3-I_2)\omega_2\omega_3 \\ G_2=I_2\dot{\omega}_2+(I_1-I_3)\omega_3\omega_1 \\ G_3=I_3\dot{\omega}_3+(I_2-I_1)\omega_1\omega_2}$$
- One can consider this being from the _re-orientation of different components of angular momentum w.r.t. the principal axes_

### Free precession of the symmetric top
- Definition: $I_1=I_2\neq I_3$
- From Euler's equations, $\dot{\omega_3}=0$

#### The body frame
- Define the _body frequency_ $\Omega_b$:
$$\Omega_b\equiv \frac{I_1-I_3}{I_1}\omega_3$$
- From Euler's equations, one gets _coupled ODEs_ for $\omega_1$ and $\omega_2$, which leads to:
$$\ddot{\omega}_i+\Omega_b^2\omega_i=0 \hspace{1cm} \text{for i} =1,2$$
- Hence _in the body frame_, $\bm{\omega}$ _precesses around the $3-$axis with the body frequency_:
$$\bm{\omega}=(\omega_{0}\cos(\Omega_bt+\phi_0),\omega_{0}\sin(\Omega_bt+\phi_0),\omega_{3})$$
- $\bm{J}$ is _not parallel to $\bm{\omega}$_ but _still precesses around the $3-$axis_

- The _relative signs_ of $\omega_3$ and $\Omega_b$ depends on whether the inertia ellipsoid is _prolate or oblate_ (i.e. $I_1>I_3$ or $I_1<I_3$)
- The _surface traced out_ by $\bm{\omega}$ is the _body cone_, with the line being the _polhode_

#### The space frame
- To find the angle between $\bm{J}$ and $\bm{\omega}$, _consider the inertial space frame_
- Considering $\bm{J}$ and $\bm{\omega}$, one can find:
$$\bm{\omega}=\frac{J}{I_1}\hat{\bm{J}}+\Omega_b\hat{\bm{e}}_3$$
- The rate of change of $\hat{\bm{e}}_3$ is:
$$\frac{d\hat{\bm{e}}_3}{dt}=\bm{\omega}\wedge\hat{\bm{e}}_3=\frac{J}{I_1}(\hat{\bm{J}}\wedge\hat{\bm{e}}_3)$$
- Therefore, $\bm{\omega}$ and $\hat{\bm{e}}_3$ _precess around $\bm{J}$_ with _space frequency_ $\Omega_s$:
$$\Omega_s=\frac{J}{I_1}$$

#### Poinsot's construction
- For a _prolate ellipsoid_:
![[Poisot's construction.png]]
- For the _oblate ellipsoid_, the _space cone is "inside" the body cone_

- From the _conservations of angular momentum and energy_, the _component of $\bm{\omega}$ along $\bm{J}$ is constant_
- Hence, there is an _invariable plane_

- Since $\bm{J}$ is perpendicular to the inertia ellipsoid, _the ellipsoid must be tangential to the invariable plane_
- Since instantaneous motion is _perpendicular to $OP$_, the ellipsoid must _roll on the invariable plane_

- From the condition of _no slipping_:
$$\Omega_b\sin\theta_b=\Omega_s\sin\theta_s$$

- Does _not only apply to symmetrical tops_

### Free precession of triaxial bodies: stability
- Three _different_ moments of inertia: $I_1<I_2<I_3$
- _Angular momentum and kinetic energy are conserved_

- Consider the body _initially steadily spinning around an axis, then there being a perturbation_
- Use Euler's equations and ignore 2nd order terms

- Spinning around the $1-$/$3-$axis: $\omega$ cannot change at constant $\bm{J}$ _without decreasing/increasing energy_, therefore it is _stable_
- Spinning around the $2-$axis: _Unstable_, the polhode will make large excursions around the body
- This is the famous _tennis racket theorem_

### Free precession of triaxial bodies


## The Major Axis Theorem for non-rigid bodies
- Real objects are _not perfectly rigid_
- During _free precession_, the _centrifugal forces_ change as $\bm{\omega}$ changes, and the object _deforms_, and _loses energy_

- $\bm{J}$ moves w.r.t. principal axes, but $|\bm{J}|^2$ must be _constant_
- Therefore, the _energy ellipsoid shrinks_
- At _minimum energy_, $\bm{J}$ must be _aligned with largest_ $I$ (the _major axis_)

## Lagrange's Approach and Euler Angles
- Characterise the motion of a _symmetric top_ with the _Euler angles_
- $\theta$ and $\phi$ are the spherical polar coordinates _of the $3-$axis_
- $\chi$ is the _angle of rotation_
![[Euler Angles.png]]

- Symmetric top: $I_1=I_2\neq I_3$
- The _angular velocity_ in terms of the Euler angles:
$$\bm{\omega}=\dot{\phi}\hat{\bm{e}}_z+\dot{\theta}\hat{\bm{e}}_1+\dot{\chi}\hat{\bm{e}}_3$$
- Let the $1-$axis be _instantaneously horizontal_
- The $z-$axis is in the $2-3$ plane

- The angular velocity and momentum are:
$$\displaylines{\bm{\omega}=(\dot{\theta},\dot{\phi}\sin\theta,\dot{\chi}+\dot{\phi}\cos\theta) \\ \bm{J}=(I_1\dot{\theta},I_1\dot{\phi}\sin\theta,I_3(\dot{\chi}+\dot{\phi}\cos\theta))}$$
- Take $I_1$ w.r.t. the _stationary point_
- If present, the _gravitational couple is in the $1-$direction_

### Free precession revisited
- The _stationary point_ is the _centre of mass_

### Forced precession - the gyroscope
- The _stationary point_ is the _support_, which is $h$ away from the CM
- The _gravitational couple_ is along the $1-$direction

- Hence, $J_z$ and $J_3$ are still _constants of motion_

- From this, the _energy_ is:
$$E=\frac{1}{2}I_1\dot{\theta}^2+\frac{(J_z-J_3\cos\theta)^2}{2I_1\sin^2\theta}+mgh\cos\theta+\frac{J_3^2}{2I_3}$$
- Hence, there is an _effective potential_ $U_\text{eff}(\theta)$

![[Gyroscope effective potential.png]]
- There is an _allowed region_ where $T>0$
- Let $U_0$ be the minimum
- Therefore, $\theta$ _moves between_ $\theta_1$ and $\theta_2$
	- Exception: "Sleeping top", where $J_z=J_3$, with the axis _vertical_

- When $\theta$ is at the minimum and $E=U_0$, the axis _steadily precesses_, while $\dot{\chi}$ is also constant

- If $E>U_0$, then the motion of $\theta$ can be treated as _harmonic motion_
- The top _nutates_, meaning $\dot{\chi}$ and $\dot{\phi}$ also oscillate
![[Nutation.png]]

#### The steady case
- Condition: $dU_\text{eff}/d\theta=0$
$$(I_1\cos\theta)\dot{\phi}^2-J_3\dot{\phi}+mgh=0$$
- This gives:
$$\dot{\phi}=\frac{J_3\pm\sqrt{J_3^2-4I_1mgh\cos\theta}}{2I_1\cos\theta}$$

- If $\cos\theta>0$, the physical solution exists if $J_3^2>4I_1mgh\cos\theta$, i.e. the top _must be spinning fast enough for steady precession_
- In the _gyroscopic limit_, $J_3^2>>mghI_1$

- At the gyroscopic limit, the _two possible precession frequencies_ $\dot{\phi}$
- _Slow precession_, $\dot{\phi}^2$ is neglected:
$$\dot{\phi}\approx\frac{mgh}{I_3}$$
- _Fast precession_, $mgh$ couple term is neglected:
$$\dot{\phi}\approx\frac{J_3}{I_1\cos\theta}=\Omega_s$$
	- Since the couple is negligible, it approaches _free precession_, hence $\dot{\phi}\approx \Omega_s$

- For a _horizontal gyroscope_, $\cos\theta=0$, and _only slow precession is seen_

#### Nutation of a horizontal gyroscope
- Nutation where $\cos\theta<<1$, in the _gyroscopic limit_
- Let $\theta=\pi/2+\epsilon$
$$U_\text{eff}(\theta)=\text{const.}+\epsilon\left(\frac{J_3J_z}{I_1}-mgh\right)+\epsilon^2\left(\frac{J_3^2}{2I_1}+\frac{J_z^2}{2I_1}\right)$$
- The _linear term vanishes_ at $\theta_0$
- At the _gyroscopic limit_, one finds that:
$$I_1\ddot{\epsilon}+\frac{J_3^2}{I_1}\epsilon\approx0$$
- Hence, $\epsilon$ _oscillates at the space frequency_ $\Omega_s$
