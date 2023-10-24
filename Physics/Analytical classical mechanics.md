>[!quote] Limerick
>There once was a classical theory,
>of which quantum disciples were leery,
>They said "Why spend so long,
>On a theory that's wrong?"
>Well, it works for your everyday query!
>
>-David Morin


- In mechanics, $\exists$ _coordinates_ $\{x_i\}$ and _time_ in some _inertial frame_
	- There is a _map_ from $\mathbb{R}$ (time) to $\mathbb{R}^3$ (space)
- In _Newtonian mechanics_, $\{x_i\}$ obey the _second law_:
$$m\frac{d^2x_i}{dt^2}=F_i$$
- For every _force_ $\bm{F}$, there is some _reaction_ $-\bm{F}$

- These laws are completely _deterministic_
- One can define a _centre of mass_ $X_i$ and _total mass_ $M$, such that for _external forces_ $F_\text{ext}$:
$$M\frac{d^2X_i}{dt^2}=F_{\text{ext},i}$$
- This seems to be a _result_ of Newtonian mechanics, instead of a _principle_
- This is a principle of _locality_, or that _far away_, one can ignore the _internal structure_ of an object

- _However_, Newtonian mechanics _does not specify_ the necessary frame in which to measure $t$
- It does not explain the _physical origins_ of $\bm{F}$
- It is sometimes _unable to deal with constraints_
- It does not specify _what inertial frame_ to write laws in, as one can simply make a _map to another frame_ $x_i\mapsto \rho_{ij}x_j+\alpha_i+\beta_it$
	- This implies there is some _symmetry_, implying a connection to _groups_
	- This should be regarded as a _principle of physics_

- This leads to the creation of _Lagrangian mechanics_
# Lagrangian mechanics
## Hamilton's Principle of Stationary Action 
- Let there be a _map_ from $\mathbb{R}$ to $\mathbb{R}^3$
	- Typically from _time_ to _configuration space_
- Fix the _initial_ and _final_ times $t_i$ and $t_f$
- There are _many possible maps_ fixing $t_i$ and $t_f$

- _Hamilton's Principle_ states that there is some _function_ $L$ known as the _Lagrangian_:
$$L(\text{path, tangent along path, time})$$
- One can then _integrate_ $L\,dt$ from $t_i$ to $t_f$, to form a function known as the _action_ $S$
- The _classical trajectory(ies)_ is/are then the path(s) of _extreme_ action
	- There is no _first order change_ when there is some _small change_ in the path

- Denote the _coordinates_ as $q_i$
- The action of a particle's trajectory $S[q(t)]$:
$$S[q(t)]=\int_{t_1}^{t_2}L(q,\dot{q},t)\,dt$$
- This depends on every point in trajectory, functional
- The action is a _functional_, requiring the use of [[Calculus of variations]]

- Consider a particle travelling along a path with _minimum action_ $q(t)$:
	- Let a neighbouring path have path $q(t)+\delta q(t)$, with $\delta q(t_1)=\delta q(t_2)=0$
	- The change in action, $\delta S$ must be 0 if the action is to be minimum:
	$$\delta S=\left[\pd{L}{\dot{q}}\delta q\right]^{t_2}_{t_1} + \int^{t_2}_{t_1}\left(\pd{L}{q}-\frac{d}{dt}\pd{L}{\dot{q}}\right)\,dt=0$$

- To achieve this, the particle obeys the _Euler-Lagrange equations_ at all times:
	$$\frac{d}{dt}\pd{L}{\dot{q}_i}=\pd{L}{q_i}$$
	- $q_i$ is a _generalised coordinate_
		- $x,y,z$ in Cartesian, $r, \theta, \phi$ for polar
	- This applies for _any frame/coordinate system_

>[!quote]
The Lagrangian formalism seems to ascribe to a particle a tremendous amount of foresight: it managaes to calculate ahead of time the action for every possible path linking the endpoints, and takes one with least action.
This, of course, is an illusion. It needs only to obey the Euler-Lagrange equations at each instance in time to minimise the action.
_Our esteem for the particle will sink further_ when we learn the path integral formalism of quantum mechanics. The particle, in a sense, goes along all possible paths, with equal weight to each!
\- Ramamurti Shankar, 1994

- For _velocity-independent_ potentials:
$$L=T-V=\frac{1}{2}m\dot{x}_i^2-V(x_i)$$
- This reproduces _Newton's second law_:
$$m\ddot{x}_i=-\pd{V}{x_i}$$
- This _only applies to conservative forces_
	- _Not dissipative_

- For _velocity dependent_ (but still _conservative_!) forces, $L$ takes a different form that reproduces the _correct equations of motion_
- Example: Coriolis $(2m\dot{r}\dot{\theta})$, Euler $(mr\ddot{\theta})$ , and centrifugal forces $(mr\dot{\theta}^2)$ arise from polar E-L equations

- One can also apply _constraints_ using _Lagrange multipliers_ (as long as they are _holonomic_)
- One can also easily spot _symmetries_ in the system
## Generalised momentum and force conjugates
- _Canonical momentum_ conjugate $p_i$:
$$p_i=\pd{L}{\dot{q}_i}$$

- _Canonical force_ conjugate $F_i$:
$$F_i=\pd{L}{q_i}$$
- Polar coordinates: 
	- $p_\theta=mr^2\dot{\theta}$, angular momentum
	- $F_\theta=$ torque
## Cyclic coordinates and conservation of momentum
- If $L=L(\dot{q}_i)$,  $F_i=\dot{p}_i=0$
	- Example: If $V=V(r)$, $p_\theta$ is conserved
	- Example: If $V=V(aq_1-bq_2)$, $bp_1+ap_2$ is conserved
- $q_i$ is known as a cyclic coordinate
### The two-body problem
$$L=\frac{1}{2}m_1|\dot{\bm{r}}_1|^2+ \frac{1}{2}m_2 |\dot{\bm{r}}_2|^2 -V(\bm{r}_2-\bm{r}_1)$$
- Transformation of coordinates: $\bm{r=r_2-r_1}$, $r_{CM}=(m_1\bm{r}_1+m_2\bm{r}_2)/(m_1+m_2)$
$$L=\frac{1}{2}(m_1+m_2)|\dot{\bm{r}}_{CM}|^2+\frac{1}{2}\frac{m_1m_2}{m_1+m_2}|\dot{\bm{r}}|^2-V(\bm{r})$$

- $\bm{r}_{CM}$ is cyclic (3 coordinates)
	- _Centre of mass moves with constant momentum_ $p_{CM}=(m_1+m_2)\dot{\bm{r}}_{CM}$
- Fictitious particle with reduced mass $\mu=m_1m_2/(m_1+m_2)$ moves under potential $V$
- Shifting the system by a constant displacement $\bm{r}_0$ does not change motion

## Holonomic constraints
- In many system, there is a _constraint_ on the movement of a body
- This _reduces the number of degrees of freedom by one_

- This can also occur since there is a _conserved quantity_

- A _holonomic constraint_ is in the form:
$$f(q_i,t)=0$$
- This can be incorporated as a _Lagrange multiplier_
- Or, one can make a _coordinate transformation_ to take advantage of the constraint
# Symmetries and Noether's Theorem
- A symmetry is an operation that does not change the functional form of the Lagrangian or Hamiltonian

- Let there be a one-parameter transformation $q_i(t) \rightarrow Q_i(s,t)$, $Q_i(0,t)=q_i(t)$
- Symmetry: $L$ is invariant in first order of $s$
$$\frac{\partial}{\partial s}L(Q_i(s,t),\dot{Q}_i(s,t),t)=0$$
>[!info] Noether's Theorem
>For every symmetry of the action of a system, there is a corresponding conserved quantity

- In the case of the one-parameter transformation, the conserved quantity is:
$$\pd{L}{s}\Bigg{|}_{s=0}=\frac{d}{dt}\left(\sum_i\pd{L}{Q_i}\pd{Q_i}{s}\Bigg|_{s=0}\right)=0$$
### Example: Translations, homogeneity of space
- Consider a system of $i$ particles, at positions $\bm{r}_i$ translated by vector $\bm{n}$
$$\bm{r}_i(t) \rightarrow \bm{r}_i(t)+s \,\bm{n}$$
- If $L$ is _invariant_ after translation:
$$\pd{L}{s}=\frac{d}{dt}\left(\sum_i\bm{p}_i\cdot\bm{n} \right)=0$$
- _Total momentum along_ direction $\bm{n}$ is conserved
- The conservation holds for all $\bm{n}$, therefore _total momentum is conserved_
	- Example: Two-body system
	- Applying Noether's theorem for all directions --> $\dot{p}_i=0$  $\forall\; i$
### Isotropy of space and rotational invariance
- $\bm{r}_i \rightarrow \bm{r}_i +\alpha\hat{\bm{n}}\times\bm{r}_i$
- Conserved quantity: $\hat{\bm{n}}\cdot \bm{L}$
- $\hat{\bm{n}}$: arbitrary axis, therefore $\bm{L}$ is conserved
### Homogeneity of time
- _Time-translation_ invariance
- Moving the system in _time_ does not affect its evolution
- Lagrangian _cannot explicitly depend on time_
- Total change in value of Lagrangian:
$$\frac{dL}{dt}=\frac{d}{dt}\left(\sum_i\pd{L}{\dot{q}_i}\dot{q}_i\right)+\pd{L}{t}$$
- Introduce the _Hamiltonian_:
$$H=\sum_i\left(\pd{L}{\dot{q}_i}\dot{q}_i\right)-L$$
$$\frac{dH}{dt}=-\pd{L}{t}$$
- The Hamiltonian _only changes when the Lagrangian depends explicitly on time_
- When $L=T-V$, $H=T+V=E$
- Energy is conserved when Lagrangian does not depend explicitly on time
	- Example: Magnetic field that varies with time

### In equations of motion
- If there is a _conserved quantity_, it _cannot be substituted into the Lagrangian_
- The Euler-Lagrange Equations are _derived while assuming all variables are independent_

- Instead, conserved quantities such as $J$ _can only be substituted into equations of motion_

# Hamiltonian formulation
## Hamiltonian as a Legendre transform
- In the Lagrangian formulation, $p_i=\partial L/\partial \dot{q}_i$
- In the Hamiltonian formulation, $\dot{q}$ _becomes the derived quantity_ from $p$:
$$\dot{q}_i=\pd{H}{p_i}$$
- To find $H$, one can use the _Legendre transform_, giving:
$$H=\sum_i\left(\pd{L}{\dot{q}_i}\dot{q}_i\right)-L=\sum_i \dot{q}_ip_i-L$$
- Considering the total differential of $H$, one gets _Hamilton's equations_:
$$\begin{aligned}\dot{q}_i&=\pd{H}{p_i} \\[8pt] \dot{p}_i&=-\pd{H}{q_i} \\[8pt] \frac{dH}{dt}&=-\pd{L}{t}\end{aligned}$$
- _Cyclic coordinates_ still exist in the Hamiltonian formulation, with $\dot{p_i}=0$ if $H$ does not depend on $q_i$
- The _minus sign_ hints at a _symplectic structure_ of the coordinate system

## Phase space
- In the Lagrangian formalism, a system's state is described by a _point in $n-$dimensional configuration space_, with a _definite velocity_
	- For a _given point_ $q$, one must also give $\dot{q}$ to determine the trajectory
	- Due to the fact that the E-L equation is _second-order_
- In the Hamiltonian formalism, a system is described by a single _point in $2n-$dimensional phase space_
	- For a _given point_ $(q,p)$, there is _only one trajectory_ passing through that point
	- Due to the fact that Hamilton's equations are _first-order_

- The velocity of a point moving through phase space:
$$\bm{v}_{phase} = \sum_i(\dot{q}_i\hat{q}_i+\dot{p}_i\hat{p}_i)$$
- If energy is conserved, the point stays on a $2n-1$-dimensional _surface of constant energy_
- The collection of all possible trajectories is known as _phase space flow_
- The flow is _divergenceless_:
$$\nabla\cdot\bm{v}_{phase}=\sum_i\left(\pd{\dot{q}_i}{q_i}+\pd{\dot{p}_i}{p_i}\right)=0$$
- This corresponds to the fact that _only one trajectory_ passes through every point

- Example of phase space flow: 1-dimensional harmonic oscillator
	- Phase space: 2-dimensional
	$$\frac{x^2}{2E/k}+\frac{p^2}{2mE}=1$$
	- The fluid rotates about the origin in fixed _ellipses_
## Liouville's Theorem
>[!INFO] Liouville's Theorem
For a small, closed region of phase space, its shape will change over time, but the total volume will not
In other words, the distribution function along a phase space trajectory is constant in time

- Proof of unchanging volume
	- Volume element at time $t$: $dV=dq_1dq_2\cdots dq_ndp_1dp_2 \cdots dp_n$
	- After time $dt$:
	$$\displaylines {dq_i \rightarrow d\bar{q}_i=dq_i +\pd{H}{p_i}\,dt \\
dp_i \rightarrow d\bar{p}_i=dp_i-\pd{H}{q_i}dt}$$
	- The volume element at time $t+dt$:
	$$d\bar{V}=d\bar{q}_1\cdots d\bar{q}_n d\bar{p}_1\cdots d\bar{p}_n=\left|\pd{(\bar{q},\bar{p})}{(q,p)}\right|\,dV=(\det\mathcal{J})\,dV$$
	- It can be proven that the [[Vector calculus in 3-dimensions#The Jacobian matrix|Jacobian]] is equal to $1+O(dt^2)$ 
	- Therefore the volume is unchanged

- Or, given some volume $V$ in the phase space, compute the _flux_ through the outer surface, and use the fact that the _flow is divergenceless_:
$$\frac{dV}{dt}=\int_S\bm{v}\cdot\,d\bm{S}=\int_V\nabla\cdot\bm{v}\,dV=0$$
- If the system is _dissipative_ (and cannot be described by $L$ or $H$), the volume _shrinks_

- Liouville's equation: the _number of phase points around a "comoving" volume is unchanged_
	- $\rho$: the [[Fundamental principles of statistical mechanics#The statistical distribution function|statistical distribution function]]
	 $$\frac{d\rho}{dt}=\pd{\rho}{t}+\sum_i \pd{\rho}{q_i}\dot{q}_i+\pd{\rho}{p_i}\dot{p}_i=0$$
	- $d\rho/dt$: along a phase trajectory
	- $\partial\rho/\partial t$: at a particular point
- True for any system with a Hamiltonian $H(q,p,t)$
- For statistical distribution functions $\rho=\rho(H(q,p))$, $\partial\rho/\partial t=0$
	- Example: distributions in [[Fundamental principles of statistical mechanics|statistical mechanics]]

# Comparison between formulations of mechanics
| Newtonian                                                                                           | Lagrangian                                                                                                         | Hamiltonian                                                                         |
| --------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------ | ----------------------------------------------------------------------------------- |
| Vectorial description, trajectory determined "step-by-step" through time                            | Scalar-based/variational description, trajectory determined all at once                                            | Variational description                                                             |
| For $n$ degrees of freedom, state described by $n$ coordinates and $n$ velocities $(q, \dot{q})$    | Same as Newtonian mechanics                                                                                        | For $n$ DOF, state described by $n$ coordinates and $n$ momenta $(q,p)$             |
| State represented by a point moving with definite velocity in $n-$dimensional _configuration space_ | Same as Newtonian mechanics                                                                                        | State described by a point in $2n-$dimensional _phase space_                        |
| $n$ coordinates evolve according to $n$ _second-order equations_                                    | Same as Newtonian mechanics                                                                                        | $2n$ coordinates and momenta obey $2n$ _first-order equations_                      |
|                                                                                                     | For a given $L$, several trajectories can pass through a given point in configuration space _depending on_ $\dot{q}$ | For a given $H$, _only one_ trajectory passes through a given point in phase space |
# Poisson brackets
- _Poisson brackets_ (PBs) are another way to express relations in classical mechanics
$$\PB{\omega}{\lambda}=\sum_i\left(\pd{\omega}{q_i}\pd{\lambda}{p_i}-\pd{\omega}{p_i}\pd{\lambda}{q_i}\right)$$
- The _rate of change in time_ of a dynamical variable $\omega(x,p,t)$ is simply expressed with PBs:
	 $$\frac{d\omega}{dt}=\PB{\omega}{H}+\pd{\omega}{t}$$
	- Lioville's equation can also be restated in the same way:
$$\pd{\rho}{t}=-\PB{\rho}{H}$$
- Therefore, if an observable _does not depend explicitly on time_, and the PB _vanishes_, it is a _conserved quantity_

- If $H$ _does not depend_ on one of the coordinates, $\PB{p}{H}=0$, hence one derives the _conservation of canonical momentum_

- As all coordinates and momenta are _independent variables_, the PBs between them are:
$$\PB{q_i}{q_j}=\PB{p_i}{p_j}=0$$
$$\PB{q_i}{p_j}=\delta_{ij}$$
- Hamilton's equations can be written in terms of PBs:
$$\dot{q}_i = \PB{q_i}{H}\;\;\;\;\dot{p_i} = \PB{p_i}{H}$$

- Anticommutativity, linearity, product rule, Jacobi identity:
$$\begin{aligned}\PB{\omega}{\lambda}&=-\PB{\lambda}{\omega} \\ \PB{\omega}{a\lambda+b\sigma}&= a\PB{\omega}{\lambda}+b\PB{\omega}{\sigma} \\ \PB{\omega}{\lambda\sigma}&=\lambda\PB{\omega}{\sigma}+\PB{\omega}{\lambda}\sigma \end{aligned}$$
$$\PB{\omega}{\PB{\lambda}{\sigma}}+\PB{\sigma}{\PB{\omega}{\lambda}}+\PB{\lambda}{\PB{\sigma}{\omega}}= 0$$
- Taking _derivatives_ with Poisson brackets:
$$\PB{\omega}{q_i}=-\pd{\omega}{p_i}\;\;\;\;\PB{\omega}{p_i}=\pd{\omega}{q_i}$$

- These properties are similar to that of the _commutators in quantum mechanics_
- Take [[Fundamental concepts of quantum mechanics#Ehrenfest's Theorem|Ehrenfest's Theorem]]:
$$\frac{d\mean{\hat{O}}}{dt}=\mean{\pd{\hat{O}}{t}}+\mean{[\hat{O},\hat{H}]}$$
- This suggests the relation between them to be:
$$\PB{A}{B}\longleftrightarrow\frac{1}{i\hbar}[\hat{A},\hat{B}]$$
# Transformations
- By transforming to another coordinate system, while the _values_ of $L$ and $H$ do not change, their _functional forms_ will 
## Point transformations
- A point transformation relies on the original coordinates:
$$q_i(t) \rightarrow \bar{q}_i(q,t)$$
- As long as the transformation is invertible, if the EL equations hold for all $q_i$, they also hold for all $\bar{q}_i$:
$$\frac{d}{dt}\pd{L}{\dot{\bar{q}_i}}-\pd{L}{\bar{q}_i} = 
\sum_j \pd{q_j}{\bar{q}_i}\left(\frac{d}{dt}\pd{L}{\dot{q}_i}-\pd{L}{q_i}\right)$$
- The new conjugate momenta are:
$$\bar{p}_i = \pd{L}{\dot{\bar{q}}_i} = \sum_j p_j\pd{q_j}{\bar{q}_i}$$
- The Hamiltonian can be defined as a function of $(\bar{q},\bar{p})$:
$$H = \sum_i\dot{\bar{q}}_i\bar{p_i}-L$$
$$\dot{\bar{q}}_i = \pd{H}{\bar{p}_i}\;\;,\;\;\dot{\bar{p}}_i=-\pd{H}{\bar{q}_i}$$

## Canonical transformations
- Consider the transformation $q\to p$ and $p\to q$, this preserves the _structure of Hamilton's equations_
	- Said to preserve the _symplectic structure_
- Clearly, this transformation is somehow _"canonical"_

- Let there be some _general transformation_:
$$q\to Q(q,p)\hspace{1.5cm}p\to P(q,p)$$
- One can then _rewrite_ $H$ as $H(Q,P)$

- For _Hamilton's equations to hold_ in this new coordinate system:
$$\PB{Q_i}{P_j}=\delta_{ij}$$
- If this holds, the transformation is _canonical_

## Generating functions


# Action-Angle variables

# Adiabatic invariants

# More about the action
- Consider the actual path of a particle $q(t)$, changed by $\delta q(t)$, where only the endpoint is varied:
$$\delta q(t_1)=0 \;\;,\;\; \delta q(t_2)=\delta q$$
- Then, consider the change in action, as the actual path is followed until $t_2$:
$$\delta S=\left[\pd{L}{\dot{q}}\delta q\right]^{t_2}_{t_1} + \int^{t_2}_{t_1}\left(\pd{L}{q}-\frac{d}{dt}\pd{L}{\dot{q}}\right)\,dt=\pd{L}{\dot{q}}\Bigg|_{t_2} \delta q=p(t_2)\delta q$$
- Therefore, one gets the result, for general number of degrees of freedom:
$$\pd{S}{q_i}=p_i$$
- The action can be regarded as an explicit function of time, with the endpoint being $t_2=t$
- Consider its total derivative with respect to time:
$$\displaylines{\frac{dS}{dt}=L \\ \frac{dS}{dt}=\pd{S}{t}+\sum_i \pd{S}{q_i}\dot{q}_i=\pd{S}{t}+\sum_ip_i\dot{q}_i}$$
- Using the definition for the Hamiltonian, one gets:
$$\pd{S}{t}=-H$$

- Also consider:
$$\frac{S}{\hbar}=\frac{1}{\hbar}\int L\,dt=\frac{1}{\hbar}\int (p\dot{q}-H)\,dt=\int k\,dq-\omega\,dt$$
- This corresponds to the _phase_ of a wave
- From _Hamilton's principle_, this must be _extremised along the classical path_
- This is similar to the trajectory from _wave optics_ to _geometrical optics_

# Electromagnetism

## Reproducing the Lorentz force
- Let there be some particle with _charge_ $q$, in _electric_ and _magnetic fields_ $\bm{E}$ and $\bm{B}$ 
- In _Newtonian_ mechanics, it is under some _Lorentz force_:
$$m\dot{\bm{v}}=e(\bm{E}+\bm{v}\times\bm{B})$$
- The _Lagrangian_ and _Hamiltonian_ must _reproduce_ this result
- To reproduce the _electric_ force, one must incorporate the _electrostatic potential_ $\phi$

- To reproduce the _magnetic_ force, let there be a term in the potential varying _linearly_ with the velocity:
$$V(\bm{x},\dot{\bm{x}},t)=e\phi(\bm{x})-e\dot{x}_jA_j(\bm{x},t)$$
- This is in fact the _most general form_ of $V$ which is _linear in velocity_
- The corresponding _Lagrangian_:
$$L(\bm{x},\dot{\bm{x}},t)=\frac{1}{2}m|\dot{\bm{x}}|^2-e(\phi-\dot{\bm{x}}\cdot\bm{A})$$

- The derivative with respect to _position_:
$$\pd{L}{x_i}=-e\pd{\phi}{x_i}+e\dot x_j\pd{A_j}{x_i}$$
- The corresponding _canonical momentum_ then becomes:
$$p_i=m\dot x_i+eA_i$$
- Hence, _mechanical momentum does not equal the canonical one_
- Then using the _E-L Equation_:
$$\displaylines{\dot p_i=m\ddot{x}_i+e\frac{dA_i}{dt}=m\ddot{x}_i+e\dot{x}_j\pd{A_i}{x_j}+\pd{A_i}{t}=\pd{L}{x_i} \\ m\ddot{x}_i=e\left(-\pd{\phi}{x_i}+\dot x_j\pd{A_j}{x_i}-\dot{x}_j\pd{A_i}{x_j}-\pd{A_i}{t}\right)=e\left(-\pd{\phi}{x_i}-\pd{A_i}{t}+\left(\dot{\bm{x}}\times\nabla\times\bm{A}\right)_i\right)}$$

- This gives:
$$m\ddot{\bm{x}}=q[\bm{E}+\bm{v}\times\bm{B}]$$
- Where:
$$\bm{E}=-\nabla\phi-\pd{\bm{A}}{t}\hspace{1.5cm}\bm{B}=\nabla\times\bm{A}$$
- Therefore, the Lagrangian above _correctly reproduces the Lorentz force law_
	- From the _most general_ Lagrangian possible that is _linear to velocity_

- To write down the _Hamiltonian_:
$$H=\bm{p}\cdot\dot{\bm{q}}-L=\frac{1}{2}m|\dot{\bm{x}}|^2+e\phi=\frac{1}{2m}|\bm{p}-e\bm{A}|^2+e\phi$$
- The Hamiltonian (and the corresponding equations) _must not be written in terms of $m\dot{\bm{x}}$_, but _in the actual canonical momentum_ $\bm{p}=m\dot{\bm{x}}+e\bm{A}$

- If there is _translational invariance_ in the magnetic field, it is _canonical momentum_ that is conserved instead of mechanical momentum
	- Example: _cyclotron_ motion
## Gauge symmetry
- Let there be a _transformation_ where $f$ is _any function_ $f(\bm{x},t)$
$$\phi\to\phi-\pd{f}{t}\hspace{1.5cm}\bm{A}\to\bm{A}+\nabla f$$
- One can check that this leaves $\bm{E}$ and $\bm{B}$ _invariant_
- It _shifts_ the Lagrangian, but _not the equations of motion_
- This is known as a _gauge symmetry_

- There can exist only _one condition_ (the arbitrary $f$) for the gauge
	- $\phi=0$ is allowed but $\bm{A}=0$ is not, as it governs three _components_
- One can choose an _axial gauge_:
$$\bm{n}\cdot\bm{A}=0$$
- Due to the arbitrary gradient, one can also choose a _Coulomb gauge_:
$$\nabla\cdot\bm{A}=0$$
- Or the _Lorenz gauge_:
$$\pd{\phi}{t}+\nabla\cdot\bm{A}=0$$
- The latter still has some _ambiguity_ as one can use any $f$ that satisfies:
$$\pd{^2f}{t^2}-\nabla^2f=0$$

- One can motivate the _form of the Lagrangian_ by requiring that it is _gauge invariant_
$$V=e(\phi-\dot{x}_iA_i)=e\left(\frac{dt}{dt}\phi-\frac{dx_i}{dt}A_i\right)$$
- One can see that the Lagrangian is also _Lorentz invariant_
# Relativistic particle dynamics

- Minkowski spacetime
## 4-vectors
- A _Lorentz transformation_ is a transformation between _frames_ in _Minkowski spacetime_
- _4-vectors_ are _Lorentz invariant_ objects
	- Its components are not Lorentz invariant

- Define a _contravariant 4-vector_ $x^\mu$, with $\mu=0,1,2,3$
	- $0$ is the _time_ component
	- $1,2,3$ are the _space_ components
	- Set $c=1$
- The _position contravariant 4-vector_
$$x^\mu=(x^0,x^1,x^2,x^3)=(t,x,y,z)$$
- Then define a _covariant vector_ $x_\mu$ 
$$x_\mu=(x_0,x_1,x_2,x_3)=(t,-x,-y,-z)$$

- The _inner product_ of the vectors:
$$x^\mu x_\mu=t^2-x^2-y^2-z^2$$
- This produces a _Lorentz invariant quantity_

- Let there be some _field_ $\phi(x^\mu)$, then consider its _differential_:
$$d\phi=\pd{\phi}{x^\mu}dx^\mu$$
- $d\phi$ is _Lorentz invariant_, hence $\partial\phi/\partial x^\mu$ is a _covariant 4-vector_:
$$\pd{\phi}{x^\mu}=\partial_\mu\phi$$
- Similarly, the corresponding _contravariant 4-vector_ is $\partial\phi/\partial x_\mu=\partial^\mu\phi$

- One can _raise and lower indices_ using the _metric tensor_:
$$\displaylines{g_{\mu\nu}=g^{\mu\nu}=\text{diag}(1,-1,-1,-1)=\pmatrix{1&0&0&0\\0&-1&0&0\\0&0&-1&0\\0&0&0&-1} \\ x_\mu=x^\nu g_{\mu\nu}}$$
- This corresponds to converting between a _column vector_ and a _row vector_

- To _preserve innner products_, a _Lorentz transformation_ must _obey_:
$$g_{\alpha\beta}={L^\bar\mu}_\alpha {L^\bar\nu}_\beta \,g_{\bar\mu\bar\nu}\hspace{1.5cm} g_{\bar\mu\bar\nu}={L^\alpha}_\bar\mu {L^\beta}_\bar\nu \,g_{\alpha\beta}$$
## The relativistic free particle Lagrangian
- The _action must be Lorentz invariant_
- Hence, for a _free particle_, define the _action_ as the _proper time elapsed_:
$$S=-mc^2\int d\tau=-mc\int\sqrt{dx_\mu dx^\mu}=-mc^2\int\sqrt{1-\frac{\dot{x}_i\dot{x}^i}{c^2}}\,dt$$
- Then one gets the _Lagrangian_:
$$L=-mc^2\sqrt{1-\frac{\dot{x}_i\dot{x}^i}{c^2}}$$
- For $\dot{x}_i\dot{x}^i<<c^2$, one can take the _non-relativistic limit_:
$$L\approx-mc^2+\frac{1}{2}mv^2$$
- The Lagrangian is _not Lorentz invariant_, but the _action_ is due to $\int\,dt$
- For the action to remain _real_, $\dot{x}_i\dot{x}^i<c^2$

- One can then find the _canonical momentum_:
$$p_i=\gamma m\dot{x}_i$$
- The _Hamiltonian_:
$$H=\gamma mc^2$$

- From the _symmetry w.r.t. translation_ of $L$:
$$p_i=\text{const.}\Longrightarrow v_i=\text{const.}$$

- The above formulation takes _time_ as the _independent variable_
- From the point of relativity, this _compromises the symmetry_ of spacetime

- Let there be a _parameter_ $\lambda$ parametrising _all components_ $x^\mu$
- The _action_ is then written as:
$$S=-mc\int\sqrt{\frac{dx_\mu}{d\lambda}\frac{dx^\mu}{d\lambda}}\,d\lambda$$
- This is _independent of parametrisation_
- This reveals the _gauge symmetry_ of the action, as it is _invariant_ under the transformation:
$$\lambda\to\lambda'(\lambda)$$

## The relativistic electromagnetic Lagrangian
- Define a _contrvariant 4-vector_ such that:
$$A^\mu=\left(\frac{\phi}{c},A^i\right)$$
- From electrodynamics, it can be proven that this is _Lorentz invariant_
- Then let its contribution to the _Lagrangian_ be:
$$-e\frac{dx_\mu}{dt}A^\mu$$


# Routhian mechanics

# Hamilton-Jacobi equations

