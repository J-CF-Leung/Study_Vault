>[!quote] Limerick
>There once was a classical theory,
>of which quantum disciples were leery,
>They said "Why spend so long,
>On a theory that's wrong?"
>Well, it works for your everyday query!
>
>-David Morin

# Lagrangian mechanics
## Principle of stationary action 
- Let a particle have a trajectory $q(t)$ linking $q(t_1)$ and $q(t_2)$
- The action of a particle's trajectory $S[q(t)]$:
$$S[q(t)]=\int_{t_1}^{t_2}\Lagr(q,\dot{q},t)\,dt$$
	- $\Lagr=$ Lagrangian
	- $S$: depends on every point in trajectory, functional
- Principle of stationary action: the particle takes a path with stationary/minimum action
- The action is a _functional_, requiring the use of [[Calculus of variations]]

- Consider a particle travelling along a path with minimum action $q(t)$:
	- Let a neighbouring path have path $q(t)+\delta q(t)$, with $\delta q(t_1)=\delta q(t_2)=0$
	- The change in action, $\delta S$ must be 0 if the action is to be minimum:
	$$\delta S=\left[\pd{\Lagr}{\dot{q}}\delta q\right]^{t_2}_{t_1} + \int^{t_2}_{t_1}\left(\pd{\Lagr}{q}-\frac{d}{dt}\pd{\Lagr}{\dot{q}}\right)\,dt=0$$
	
- To achieve this, the particle obeys the Euler-Lagrange equations at all times:
$$\frac{d}{dt}\pd{\Lagr}{\dot{q}_i}=\pd{\Lagr}{q_i}$$
	- $q_i$ is a _generalised coordinate_
		- $x,y,z$ in Cartesian, $r, \theta, \phi$ for polar
>[!quote]
The Lagrangian formalism seems to ascribe to a particle a tremendous amount of foresight: it managaes to calculate ahead of time the action for every possible path linking the endpoints, and takes one with least action.
This, of course, is an illusion. It needs only to obey the Euler-Lagrange equations at each instance in time to minimise the action.
_Our esteem for the particle will sink further_ when we learn the path integral formalism of quantum mechanics. The particle, in a sense, goes along all possible paths, with equal weight to each!
\- Ramamurti Shankar, 1994

- For _velocity-independent_ potentials, $\Lagr=T-V$
- For _velocity dependent_ (but still _conservative_!) forces, $\Lagr$ takes a different form that reproduces the _correct equations of motion_
- Euler-Lagrange equations are _independent of coordinate system_
- Example: Coriolis $(2m\dot{r}\dot{\theta})$, Euler $(mr\ddot{\theta})$ , and centrifugal forces $(mr\dot{\theta}^2)$ arise from polar E-L equations
## Generalised momentum and force conjugates
- _Canonical momentum_ conjugate $p_i$:
$$p_i=\pd{\Lagr}{\dot{q}_i}$$
- _Canonical force_ conjugate $F_i$:
$$F_i=\pd{\Lagr}{q_i}$$
- Polar coordinates: 
	- $p_\theta=mr^2\dot{\theta}$, angular moentum
	- $F_\theta=$ torque
## Cyclic coordinates and conservation of momentum
- If $\Lagr=\Lagr(\dot{q}_i)$,  $F_i=\dot{p}_i=0$
	- Example: If $V=V(r)$, $p_\theta$ is conserved
	- Example: If $V=V(aq_1-bq_2)$, $bp_1+ap_2$ is conserved
- $q_i$ is known as a cyclic coordinate
### The two-body problem
$$\Lagr=\frac{1}{2}m_1|\dot{\bm{r}}_1|^2+ \frac{1}{2}m_2 |\dot{\bm{r}}_2|^2 -V(\bm{r}_2-\bm{r}_1)$$
- Transformation of coordinates: $\bm{r=r_2-r_1}$, $r_{CM}=(m_1\bm{r}_1+m_2\bm{r}_2)/(m_1+m_2)$
$$\Lagr=\frac{1}{2}(m_1+m_2)|\dot{\bm{r}}_{CM}|^2+\frac{1}{2}\frac{m_1m_2}{m_1+m_2}|\dot{\bm{r}}|^2-V(\bm{r})$$

- $\bm{r}_{CM}$ is cyclic (3 coordinates)
	- Centre of mass moves with constant momentum $p_{CM}=(m_1+m_2)\dot{\bm{r}}_{CM}$
- Fictitious particle with reduced mass $\mu=m_1m_2/(m_1+m_2)$ moves under potential $V$
- Shifting the system by a constant displacement $\bm{r}_0$ does not change motion

# Symmetries and Noether's Theorem
- A symmetry is an operation that does not change the functional form of the Lagrangian or Hamiltonian

- Let there be a one-parameter transformation $q_i(t) \rightarrow Q_i(s,t)$, $Q_i(0,t)=q_i(t)$
- Symmetry: $\Lagr$ is invariant in first order of $s$
$$\frac{\partial}{\partial s}\Lagr(Q_i(s,t),\dot{Q}_i(s,t),t)=0$$
>[!info] Noether's Theorem
>For every symmetry of the action of a system, there is a corresponding conserved quantity

- In the case of the one-parameter transformation, the conserved quantity is:
$$\pd{\Lagr}{s}\Bigg{|}_{s=0}=\frac{d}{dt}\left(\sum_i\pd{\Lagr}{Q_i}\pd{Q_i}{s}\Bigg|_{s=0}\right)=0$$
### Example: Translations, homogeneity of space
- Consider a system of $i$ particles, at positions $\bm{r}_i$ translated by vector $\bm{n}$
$$\bm{r}_i(t) \rightarrow \bm{r}_i(t)+s \,\bm{n}$$
- Invariance of $\Lagr$ after translation:
$$\pd{\Lagr}{s}=\frac{d}{dt}\left(\sum_i\bm{p}_i\cdot\bm{n} \right)=0$$
- Total momentum along direction $\bm{n}$ is conserved
- The conservation holds for all $\bm{n}$, therefore total momentum is conserved
	- Example: Two-body system
	- Applying Noether's theorem for all directions --> $\dot{p}_i=0$  $\forall\; i$
### Isotropy of space and rotational invariance
- $\bm{r}_i \rightarrow \bm{r}_i +\alpha\hat{\bm{n}}\times\bm{r}_i$
- Conserved quantity: $\hat{\bm{n}}\cdot \bm{L}$
- $\hat{\bm{n}}$: arbitrary axis, therefore $\bm{L}$ is conserved
### Homogeneity of time
- Time-translation invariance
- Moving the system in time does not affect its evolution
- Lagrangian cannot explicitly depend on time
- Total change in value of Lagrangian:
$$\frac{d\Lagr}{dt}=\frac{d}{dt}\left(\sum_i\pd{\Lagr}{\dot{q}_i}\dot{q}_i\right)+\pd{\Lagr}{t}$$
- Introduce the Hamiltonian:
$$\Ham=\sum_i\left(\pd{\Lagr}{\dot{q}_i}\dot{q}_i\right)-\Lagr$$
$$\frac{d\Ham}{dt}=-\pd{\Lagr}{t}$$
- The Hamiltonian only changes when the Lagrangian depends explicitly on time
- When $\Lagr=T-V$, $\Ham=T+V=E$
- Energy is conserved when Lagrangian does not depend explicitly on time
	- Example: Magnetic field that varies with time

# Hamiltonian formulation
## Hamiltonian as a Legendre transform
- In the Lagrangian formulation, $p_i=\partial\Lagr/\partial \dot{q}_i$
- In the Hamiltonian formulation, $\dot{q}$ _becomes the derived quantity_ from $p$:
$$\dot{q}_i=\pd{\Ham}{p_i}$$
- To find $\Ham$, one can use the _Legendre transform_, giving:
$$\Ham=\sum_i\left(\pd{\Lagr}{\dot{q}_i}\dot{q}_i\right)-\Lagr=\sum_i \dot{q}_ip_i-\Lagr$$
- Considering the total differential of $\Ham$, one gets _Hamilton's equations_:
$$\begin{aligned}\dot{q}_i&=\pd{\Ham}{p_i} \\[8pt] \dot{p}_i&=-\pd{\Ham}{q_i} \\[8pt] \frac{d\Ham}{dt}&=-\pd{\Lagr}{t}\end{aligned}$$
- Cyclic coordinates still exist in the Hamiltonian formulation, with $\dot{p_i}=0$ if $\Ham$ does not depend on $q_i$

## Phase space
- In the Lagrangian formalism, a system's state is described by a _point in $n-$dimensional configuration space_, with a definite velocity
- In the Hamiltonian formalism, a system is described by a single _point in $2n-$dimensional phase space_
- The velocity of a point moving through phase space:
$$\bm{v}_{phase} = \sum_i(\dot{q}_i\hat{q}_i+\dot{p}_i\hat{p}_i)$$
- If energy is conserved, the point stays on a $2n-1$-dimensional _surface of constant energy_
- The collection of all possible trajectories is known as _phase space flow_
- The flow is _divergenceless_:
$$\nabla\cdot\bm{v}_{phase}=\sum_i\left(\pd{\dot{q}_i}{q_i}+\pd{\dot{p}_i}{p_i}\right)=0$$
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
	$$\displaylines {dq_i \rightarrow d\bar{q}_i=dq_i +\pd{\Ham}{p_i}\,dt \\
dp_i \rightarrow d\bar{p}_i=dp_i-\pd{\Ham}{q_i}dt}$$
	- The volume element at time $t+dt$:
	$$d\bar{V}=d\bar{q}_1\cdots d\bar{q}_n d\bar{p}_1\cdots d\bar{p}_n=\left|\pd{(\bar{q},\bar{p})}{(q,p)}\right|\,dV=(\det\mathcal{J})\,dV$$
	- It can be proven that the [[Vector calculus in 3-dimensions#The Jacobian matrix|Jacobian]]  is equal to $1+O(dt^2)$ 
	- Therefore the volume is unchanged
- Liouville's equation: the _number of phase points around a "comoving" volume is unchanged_
	- $\rho$: the [[Fundamental principles of statistical mechanics#The statistical distribution function|statistical distribution function]]
	 $$\frac{d\rho}{dt}=\pd{\rho}{t}+\sum_i \pd{\rho}{q_i}\dot{q}_i+\pd{\rho}{p_i}\dot{p}_i=0$$
	- $d\rho/dt$: along a phase trajectory
	- $\partial\rho/\partial t$: at a particular point
- True for any system with a Hamiltonian $\Ham(q,p,t)$
- For statistical distribution functions $\rho=\rho(\Ham(q,p))$, $\partial\rho/\partial t=0$
	- Example: distributions in [[Fundamental principles of statistical mechanics|statistical mechanics]]


# Comparison between formulations of mechanics
| Newtonian                                                                                           | Lagrangian                                                              | Hamiltonian                                                             |
| --------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------- | ----------------------------------------------------------------------- |
| Vectorial description, trajectory determined "step-by-step" through time                            | Scalar-based/variational description, trajectory determined all at once | Variational description                                                 |
| For $n$ degrees of freedom, state described by $n$ coordinates and $n$ velocities $(q, \dot{q})$    | Same as Newtonian mechanics                                             | For $n$ DOF, state described by $n$ coordinates and $n$ momenta $(q,p)$ |
| State represented by a point moving with definite velocity in $n-$dimensional _configuration space_ | Same as Newtonian mechanics                                             | State described by a point in $2n-$dimensional _phase space_              |
| $n$ coordinates evolve according to $n$ _second-order equations_                                      | Same as Newtonian mechanics                                             | $2n$ coordinates and momenta obey $2n$ _first-order equations_            |
|                                                                                                     |  For a given $\Lagr$, several trajectories can pass through a given point in configuration space depending on $\dot{q}$   | For a given $\Ham$, only one trajectory passes through a given point in phase space |
# Poisson brackets
- _Poisson brackets_ (PBs) are another way to express relations in classical mechanics
$$\PB{\omega}{\lambda}=\sum_i\left(\pd{\omega}{q_i}\pd{\lambda}{p_i}-\pd{\omega}{p_i}\pd{\lambda}{q_i}\right)$$
- The rate of change of a dynamical variable $\omega(x,p,t)$ is simply expressed with PBs:
	 $$\frac{d\omega}{dt}=\PB{\omega}{\Ham}+\pd{\omega}{t}$$
	- Lioville's equation can also be restated in the same way:
$$\pd{\rho}{t}=-\PB{\rho}{\Ham}$$
- As all coordinates and momenta are independent variables, the PBs between them are:
$$\PB{q_i}{q_j}=\PB{p_i}{p_j}=0$$
$$\PB{q_i}{p_j}=\delta_{ij}$$
- Hamilton's equations can be written in terms of PBs:
$$\dot{q}_i = \PB{q_i}{\Ham}\;\;\;\;\dot{p_i} = \PB{p_i}{\Ham}$$
- Anticommutativity, linearity, product rule, Jacobi identity:
$$\begin{aligned}\PB{\omega}{\lambda}&=-\PB{\lambda}{\omega} \\ \PB{\omega}{a\lambda+b\sigma}&= a\PB{\omega}{\lambda}+b\PB{\omega}{\sigma} \\ \PB{\omega}{\lambda\sigma}&=\lambda\PB{\omega}{\sigma}+\PB{\omega}{\lambda}\sigma \end{aligned}$$
$$\PB{\omega}{\PB{\lambda}{\sigma}}+\PB{\sigma}{\PB{\omega}{\lambda}}+\PB{\lambda}{\PB{\sigma}{\omega}}= 0$$
- Taking derivatives with Poisson brackets:
$$\PB{\omega}{q_i}=-\pd{\omega}{p_i}\;\;\;\;\PB{\omega}{p_i}=\pd{\omega}{q_i}$$

# Canonical transformations
- By transforming to another coordinate system, while the _values_ of $\Lagr$ and $\Ham$ do not change, their _functional forms_ will 
## Point transformations
- A point transformation relies on the original coordinates:
$$q_i(t) \rightarrow \bar{q}_i(q,t)$$
- As long as the transformation is invertible, if the EL equations hold for all $q_i$, they also hold for all $\bar{q}_i$:
$$\frac{d}{dt}\pd{\Lagr}{\dot{\bar{q}_i}}-\pd{\Lagr}{\bar{q}_i} = 
\sum_j \pd{q_j}{\bar{q}_i}\left(\frac{d}{dt}\pd{\Lagr}{\dot{q}_i}-\pd{\Lagr}{q_i}\right)$$
- The new conjugate momenta are:
$$\bar{p}_i = \pd{\Lagr}{\dot{\bar{q}}_i} = \sum_j p_j\pd{q_j}{\bar{q}_i}$$
- The Hamiltonian can be defined as a function of $(\bar{q},\bar{p})$:
$$\Ham = \sum_i\dot{\bar{q}}_i\bar{p_i}-\Lagr$$
$$\dot{\bar{q}}_i = \pd{\Ham}{\bar{p}_i}\;\;,\;\;\dot{\bar{p}}_i=-\pd{\Ham}{\bar{q}_i}$$


## Generating functions


# Action-Angle variables

# Adiabatic invariants

# More about the action
- Consider the actual path of a particle $q(t)$, changed by $\delta q(t)$, where only the endpoint is varied:
$$\delta q(t_1)=0 \;\;,\;\; \delta q(t_2)=\delta q$$
- Then, consider the change in action, as the actual path is followed until $t_2$:
$$\delta S=\left[\pd{\Lagr}{\dot{q}}\delta q\right]^{t_2}_{t_1} + \int^{t_2}_{t_1}\left(\pd{\Lagr}{q}-\frac{d}{dt}\pd{\Lagr}{\dot{q}}\right)\,dt=\pd{\Lagr}{\dot{q}}\Bigg|_{t_2} \delta q=p(t_2)\delta q$$
- Therefore, one gets the result, for general number of degrees of freedom:
$$\pd{S}{q_i}=p_i$$
- The action can be regarded as an explicit function of time, with the endpoint being $t_2=t$
- Consider its total derivative with respect to time:
$$\displaylines{\frac{dS}{dt}=\Lagr \\ \frac{dS}{dt}=\pd{S}{t}+\sum_i \pd{S}{q_i}\dot{q}_i=\pd{S}{t}+\sum_ip_i\dot{q}_i}$$
- Using the definition for the Hamiltonian, one gets:
$$\pd{S}{t}=-\Ham$$
# Electromagnetism

# Routhian mechanics

# Hamilton-Jacobi equations

