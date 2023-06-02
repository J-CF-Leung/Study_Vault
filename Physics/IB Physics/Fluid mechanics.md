
# Buoyancy
- In a fluid, pressure _increases linearly with depth_
$$P=\rho gz$$
- Due to this, a body _immersed in fluid_ will experience _upthrust_
- The net force for a cylindrical body with height $\Delta z$ is:
$$F=\rho gA\Delta z = \rho gV$$
- This can be extended to _any arbitrary shape_
	- Consider an _arbitrary shape_ filled with the displaced fluid, which _must be in equilibrium_
- _Archimedes' Principle_ states that _buoyancy_ is _equal to the weight of the displaced fluid_

- The upthrust acts through the _centre of buoyancy_, which is the _geometrical centre of the fluid-displaced volume_


# Basic characteristics of Newtonian fluid flow
>[!quote]
>"The flow of dry water."
>-Feynman Lectures, Volume 2, Lecture 40

- Fluid: _continuous_ medium
	- Any 'infinitely' small volume element still contains a _large number of molecules_
	- The _mean free path_ is small compared to scale of interest
- _Locally_, a volume element is in equilibrium but _macroscopic quantities_ like $P$ and $\rho$ can still be defined, and vary with position
- Relevant quantities:
	- Flow velocity $\bm{v}(x,y,z,t)$
	- Pressure $P(x,y,z,t)$
	- Density $\rho(x,y,z,t)$

- These quantities can change _discontinuously_ at _shock fronts_, which are not considered
- The effects of _surface tension_ are also ignored

## Newtonian fluid
- Newtonian fluids _cannot maintain a shear stress_ as the molecules _move past each other_
- Any imposed (normal or shear) stress, _unless maintained, rapidly decays_

- The _viscosity_ $\eta$ is defined by the _ratio between shear stress and rate of shear_:
$$\tau_{xy}=2\eta\dot{e}_{xy}$$
- The _time-scale_ at which shear stress _decays_, $t_s$, is related by:
$$\eta=G t_s$$
- For _Newtonian_ fluids, the only stresses are _isotropic_:
$$\tau_1=\tau_2=\tau_3=-P$$

## Following the fluid
- Often, one is looking at a _steady flow_, where the _velocity_ of the fluid is _constant at a point fixed in space_:
$$\pd{\bm{v}}{t}=0$$
- One can _visualise_ the motion of the fluid with _streamlines_, which are _aligned with the velocity_ of the fluid at any point:
$$\displaylines{\frac{d\bm{x}_s}{ds}\wedge\bm{v}(s)=0 \\ \frac{dx_s}{u_x}=\frac{dy_s}{u_y}=\frac{dz_s}{u_z}}$$
- Streamlines are _analagous to electric or magnetic field lines_

- One can also use a _particle path_, which _follows a fluid element_
- A _streakline_ connects _points that go through a particular point in space at all times_

- For a _steady flow_, all three of these lines _coincide_
- Quantities of interest (such as density and temperature) _are also constant at the particular point_

- It is obvious that if one _follows a fluid element_, $\bm{v}$ and other quantities _must change_
- A _rate of change following the fluid_ is the _convective derivative_:
$$\frac{D}{Dt}\equiv\pd{}{t}+\frac{dx_i}{dt}\pd{}{x_i}\equiv\pd{}{t}+\bm{v}\cdot\nabla$$
- The second term can be interpreted as a _rate of change along the streamline_

- Example: _Steady flow with uniform rotation_
$$\displaylines{\bm{v}=(-\Omega y, \Omega x,0) \\\frac{D\bm{v}}{Dt}=(\bm{v}\cdot\nabla)\bm{v}=-\Omega^2(x,y,0)}$$
- This represents a _centrifugal acceleration_, as expected

## Continuity
- $\bm{j}=\rho\bm{v}$: mass flux density
- Decrease in mass of fluid inside specified volume:
$$-\int\pd{\rho}{t}\, dV$$
- Flow out of closed volume:
$$\oint \bm{j}\cdot \,d\bm{S}=\oint \nabla\cdot(\rho\bm{v})\,dV$$
- Continuity equation:
$$\pd{\rho}{t}+\nabla\cdot(\rho\bm{v})=0$$
- If the flow is _incompressible_:
$$\nabla\cdot\bm{v}=0$$

## Euler's equation
- Calculate the _acceleration of a particular fluid element_

- Account for the presence of gravity, with a _force per unit volume_:
$$\rho \bm{g}=-\rho\nabla\phi_g$$
- By considering _variations in pressure on the sides of the element_:
$$\rho\frac{D\bm{v}}{Dt}=-\nabla P+\rho\bm{g}$$
- This is effectively the _equation of motion_ for a fluid element

## Bernoulli's equation

### Compressible flow
- Consider the _conservation of energy along a streamline_:
![[Bernoulli derivation.png]]
- The energy flows _in or out_ can be written as:
$$Av\left(\rho\phi+\frac{1}{2}\rho v^2+u\right)$$
- Here, $u$ is the _internal energy density_
- The _mass flow rate_ must be constant:
$$A\rho v=\text{const.}$$
- At each end, the pressure also does _work_ at rate:
$$W_P=APv$$
- Hence, one obtains _Bernoulli's equation_:
$$\frac{u+P}{\rho}+\frac{1}{2}v^2+\phi=\text{const.}$$

- This is simply a manifestation of _conservation of energy_, with each term representing a different contribution

- $u+P$ is the [[Classical Thermodynamics#Thermodynamic potentials|specific enthalpy]] $H/V$ of the fluid
- For a _perfect gas_:
$$u+P=\frac{\gamma}{\gamma-1}P$$

### Incompressible flow
- Density becomes a _constant_
- _Incompressibility_ means $\gamma\to\infty$, $u\to0$
	- Incompressibility leads to $C_p\to\infty$

- Using the identity:
$$(\nabla\wedge\bm{v})\wedge\bm{v}=(\bm{v}\cdot\nabla)\bm{v}-\nabla\left(\frac{1}{2}|\bm{v}|^2\right)$$
- Substituting this into _Euler's equation_, one gets:
$$\displaylines{(\nabla\wedge\bm{v})\wedge\bm{v}=-\nabla H \\ H=P+\rho\phi_g+\frac{1}{2}\rho |\bm{v}|^2}$$
- Like above, each term is a _contribution to energy_
- $\bm{v}H$ is then the _energy flux_

- By dotting with $\bm{v}$ on both sides:
$$(\bm{v}\cdot\nabla)H=0$$
- This is _Bernoulli's equation for incompressible flow_, stating that $H$ is _constant along a streamline_
	- Can also be derived from multiplying the result above with $\rho$
- If the flow is _steady and irrotational_, then it is _constant everywhere_
	- Hence, the _enthalpy flow_ of a body of fluid is constant

## Approximations
- _Incompressible flow_ is defined as:
$$\nabla\cdot\bm{v}=0$$
- Most common for _liquids_ and _slow-moving gases_

- _Irrotational flow_ is defined as:
$$\bm{\omega}\equiv\nabla\wedge\bm{v}=0$$
- The _vorticity_ $\bm{\omega}$ is often generated at the _boundary layer_
- The _bulk_ of a fluid is often irrotational
- The curve _tangent to $\bm{\omega}$_ is known as the _vortex line_

- If a fluid is _irrotational_, then the velocity can be written using a _scalar potential_:
$$\bm{v}=\nabla\Phi$$

- If a fluid is _both incompressible AND irrotational_, then the flow _satisfies Laplace's Equation_
$$\nabla^2\Psi=0$$

## The Circulation theorem
- The _circulation_ $K$ around a loop $\Gamma$ is defined as:
$$K=\oint_\Gamma\bm{v}\cdot\,d\bm{l}$$
- Using Stokes' Theorem:
$$K=\int\bm{\omega}\cdot\,d\bm{S}$$
- By _applying the convective derivative to both sides_, and using _Euler's equation_:
$$\frac{DK}{Dt}=\oint \nabla\left(-\frac{P}{\rho}-\phi_g+\frac{1}{2}u^2\right)\cdot d\bm{l}=0$$
	- The derivative also applies to $d\bm{l}$
- Hence, _vortex lines are conserved_, and _moves with the fluid_
	- For an _ideal fluid_

## Potential flow of an irrotational fluid
- Often applies to _bulk fluid_
- Solving for velocity $\bm{v}=\nabla\Phi$ is equivalent to solving [[Poisson and Laplace's equations|Laplace's equation]]:
$$\nabla^2\Phi=0$$
- A _source or sink_ of fluid is _analagous to an electric charge_

- Example: A source next to a _rigid plate_
	- _Boundary condition_: No flow _normal_ to the plate
	- Place an _image source_
	- Radial velocity _decreases with distance from source_
	- Applying Bernoulli, there is a _pressure deficit_, which _attracts the plate to the source_
- Consequence: _two sources attract, a source and a sink repel_


- Example: Potential flow _past a sphere_ of radius $a$
![[Sphere potential flow.png]]
	- Boundary condition: $u_r(r=a)=0$
	- At _large distances_, $\Phi=V_0z=V_0r\cos\theta$
	- From solving Laplace's Equation:
	$$\Phi=V_0\cos\theta\left(r+\frac{a^3}{2r^2}\right)$$
	- From applying _Bernoulli's theorem_, the _pressure on the sphere_ is:
	$$P(\theta)=P_0+\frac{1}{2}\rho V_0^2-\frac{9}{8}V_0^2\sin^2\theta$$
	- There is _no net force_ (implies _no drag_)
	- At $\theta=0$ and $\theta=\pi$, there are _equal and opposite high pressures_
	- For a _high enough speed_, $P(\theta=\pi/2)<0$, causing _cavitation_, forming _bubbles_
- _Real flow_:
	- The fluid _cannot freely slip past surface_
	- There is a _boundary shear layer_, causing a _drag force_

- Example: flow _past a cylinder_ of radius $a$
	- There is a _similar solution to the sphere_ by solving Laplace's solution:
	$$\Phi=V_0\cos\theta\left(r+\frac{a^2}{r}\right)$$
	- A _separate solution_ for irrotational flow is the _vortex_:
	$$\bm{v}=\frac{\kappa}{2\pi r}\hat{\bm{e}}_\theta$$
	- Any _circulation_ around a loop _not containing the cylinder_ is _zero_
	- Hence, _everywhere in the fluid_, the flow is _irrotational_
	- The vortex is said to have _strength_ $\kappa$
	- This leads to a _multi-valued potential_ $\kappa\theta/(2\pi)$
	- Let the cylinder _rotate_ at $\omega=\kappa/(2\pi a^2)$ to _match boundary conditions_
	- _Add the two potentials together_:
	$$\Phi=V_0\cos\theta\left(r+\frac{a^2}{r}\right)+\frac{\kappa\theta}{2\pi}$$
	![[Cylinder potential flow.png]]
	- Using Bernoulli's equation, one finds an _asymmetrical term_ in pressure
	- This gives a _net vertical force per unit length_:
	$$F_\text{vertical}=\rho V_0\kappa$$
	- This is the _Magnus force_, which can be written as:
	$$\bm{F}_\text{Magnus}=\rho\bm{V}_0\wedge\bm{\kappa}$$

## Vortex lines and rings

### Lines
- Create circulation in a _bulk fluid_ without additional elements (such as a cylinder)
- If $\bm{v}=\kappa/(2\pi r)\hat{\bm{r}}_\theta$ like above, there will be a _singularity_ at $r=0$

- Instead, the fluid can form a _Helmholtz vortex_
- It is said to have a _core_ of radius $r_c$, with vorticity $\bm{\Omega}=\nabla\wedge\bm{v}$
- The velocities are:
$$\displaylines{\kappa=\pi r_c^2\Omega\\\bm{v}=\begin{cases}\frac{\kappa r}{2\pi r_c^2}\hat{\bm{e}}_\theta & r<r_c \\ \frac{\kappa}{2\pi r} \hat{\bm{e}}_\theta&r>r_c\end{cases}}$$
- The solid core has _angular speed_ $\Omega/2$
- Analagous to _uniform current in a wire_

- [[#The Circulation theorem]] states that vortex lines are _conserved and move with the fluid_

- From this, two _vortex lines of opposite sign_ will _move in the same direction_, perpendicular to the line between them
	- In a frame where the vortices are _at rest_, there are two _equal and opposite Magnus forces_, one from _surrounding fluid flow_ and the other from the _vortex_
- Two vortex lines of the _same sign_ will circle around each other

### Rings
- It is also possible to make a _vortex ring_
- A ring of _radius_ $a$ with _core size_ $r_c$ has a _drift velocity_:
$$u_D=\frac{\kappa}{4\pi a}\ln\left(\frac{a}{r_c}\right)$$

# Viscous fluids
>[!quote]
>"The flow of wet water."
>-Feynman Lectures, Volume 2, Lecture 41
- A sudden _shear_ $e_{xy}$ produces a stress $\tau_{xy}=2Ge_{xy}$ which _decays_
- To _maintain_ the stress, the fluid must be _continually sheared_
- The _proportionality constant_ is known as the _viscosity_ $\eta$:
$$\tau_{xy}=2\eta\frac{de_{xy}}{dt}$$

- Consider _steady shear flow_ between two _flat plates_ at $y=0$ and $y=d$
- The upper plate moves at speed $V$
- By equilibrium of a fluid element, the _velocity gradient must be constant_:
$$\tau_{xy}=\eta\pd{v_x}{y}=\eta\frac{V}{d}$$

- By considering the _variation of stresses across a volume element_:
$$\frac{F_i}{\delta V}=\sum_j\pd{\tau_{ij}}{x_j}=\eta\sum_j\left(\pd{^2 v_i}{x_j\partial x_j}+\pd{^2v_j}{x_i\partial x_j}\right)$$
- Therefore, for an _incompressible fluid_, where $\nabla\cdot\bm{v}=0$
$$\rho\frac{D\bm{v}}{Dt}=-\nabla P+\rho\bm{g}+\eta\nabla^2\bm{v}$$
- This is the _Navier-Stokes equation_

- Example: _Poiseuille flow_
	- The boundary condition is _zero velocity at a boundary_
	- Draining plate: Uniform pressure, viscous force _balances_ gravity
	- Pipe: Pressure gradient _balances_ viscous force
	- The flow profile is _parabolic_

## Microscopic processes
- Viscosity and thermal conductivity are determined by _collisional processes_
- Let there be some quantity $Q$ (thermal conductivity or viscosity)
- The molecules move at $v_T$ with _mean free path_ $\lambda_c$
- This leads to a _diffusion equation_ w.r.t. the fluid element:
$$\frac{1}{3}\lambda_cv_T\nabla^2Q=\frac{DQ}{Dt}$$
	- Factor of $1/3$: 3 degrees of freedom
	- Can be derived from the [[Kinetic Theory of Gases]]
- The _kinematic viscosity_ is defined as:
$$\nu\equiv\frac{\eta}{\rho}=\frac{1}{3}\lambda_cv_T$$

## Boundary layers
- Boundary condition for _surface of solid body_: No slip, hence $v$ matches the body
- There must be a _boundary layer_ with a _velocity gradient_
- This region must have some _vorticity_
![[Boundary layer.png]]
- This can lead to _vortex shedding_

## Reynolds number and drag force
- A viscous fluid flowing at speed $v$ will experience _intertial stress_ $\sim\rho v^2$ and _viscous stress_ $\eta v/L$, where $L$ is a _characteristic length scale_
- Define the _Reynolds number_ $N_R$:
$$N_R=\frac{\rho vL}{\eta}$$
- For a _low Reynolds number flow_