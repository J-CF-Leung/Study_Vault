
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
>-Richard Feynman

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
$$\pd{\bm{u}}{t}=0$$
- One can _visualise_ the motion of the fluid with _streamlines_, which are _aligned with the velocity_ of the fluid at any point:
$$\displaylines{\frac{d\bm{x}_s}{ds}\wedge\bm{u}(s)=0 \\ \frac{dx_s}{u_x}=\frac{dy_s}{u_y}=\frac{dz_s}{u_z}}$$
- Streamlines are _analagous to electric or magnetic field lines_

- One can also use a _particle path_, which _follows a fluid element_
- A _streakline_ connects _points that go through a particular point in space at all times_

- For a _steady flow_, all three of these lines _coincide_
- Quantities of interest (such as density and temperature) _are also constant at the particular point_

- It is obvious that if one _follows a fluid element_, $\bm{u}$ and other quantities _must change_
- A _rate of change following the fluid_ is the _convective derivative_:
$$\frac{D}{Dt}\equiv\pd{}{t}+\frac{dx_i}{dt}\pd{}{x_i}\equiv\pd{}{t}+\bm{u}\cdot\nabla$$
- The second term can be interpreted as a _rate of change along the streamline_

- Example: _Steady flow with uniform rotation_
$$\displaylines{\bm{u}=(-\Omega y, \Omega x,0) \\\frac{D\bm{u}}{Dt}=(\bm{u}\cdot\nabla)\bm{u}=-\Omega^2(x,y,0)}$$
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
$$\rho\frac{D\bm{u}}{Dt}=-\nabla P+\rho\bm{g}$$
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
- Hence, one obtains _Bernoulli's equation_:
$$\frac{u+P}{\rho}+\frac{1}{2}v^2+\phi=\text{const.}$$
- This is simply a manifestation of _conservation of energy_, with each term representing a different contribution

### Incompressible flow
- Density becomes a _constant_
- Using the identity:
$$(\nabla\wedge\bm{u})\wedge\bm{u}=(\bm{u}\cdot\nabla)\bm{u}-\nabla\left(\frac{1}{2}|\bm{u}|^2\right)$$
- Substituting this into _Euler's equation_, one gets:
$$\displaylines{(\nabla\wedge\bm{u})\wedge\bm{u}=-\nabla H \\ H=P+\rho\phi_g+\frac{1}{2}\rho |\bm{u}|^2}$$
- Like above, each term is a _contribution to energy_
- $\bm{u}H$ is then the _energy flux_

- By dotting with $\bm{u}$ on both sides:
$$(\bm{u}\cdot\nabla)H=0$$
- This is _Bernoulli's equation for incompressible flow_, stating that $H$ is _constant along a streamline_

## Approximations
- _Incompressible flow_ is defined as:
$$\nabla\cdot\bm{v}=0$$
- Most common for _liquids_ and _slow-moving gases_

- _Irrotational flow_ is defined as:
$$\bm{\omega}\equiv\nabla\wedge\bm{v}=0$$
- The _vorticity_ $\bm{\omega}$ is often _generated at boundaries_
- The _bulk_ of a fluid is often irrotational

- If a fluid is _irrotational_, then the velocity can be written using a _scalar potential_:
$$\bm{v}=\nabla\Phi$$

- If a fluid is _both incompressible AND irrotational_, then the flow _satisfies Laplace's Equation_
$$\nabla^2\Psi=0$$
## The Circulation theorem


## Potential flow
