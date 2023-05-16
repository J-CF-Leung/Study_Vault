- Phenomena related to _transport via gases_
- Viscosity: _momentum_ transport
- Thermal conductivity: _heat_ transport

- The essential _approximations_:
$$L>>\lambda>>d$$
- $L$: _container size_, so the _scale_ of the flow is much larger than the mean free path
- $d$: _molecule diameter_, to avoid _intermolecular interactions_

# Viscosity
- Viscosity is a measure of the _resistance of a fluid to a deformation under shear stress_
- One considers the _bulk properties_ of a fluid instead of the [[Kinetic Theory of Gases#Maxwell-Boltzmann distribution|velocities of individual particles]]
- The _bulk velocities_ are denoted as a _mean_
![[Shear of a fluid.png]]
- Given two _plates_ of area $A$ and parallel _force_ $F$, the _shear stress_ in the $xz-$plane is:
$$\tau_{xz}=\frac{F}{A}$$
- Given one plate is _moving_ at velocity $u$ while the other is kept _stationary_, there is some _velocity gradient_ $d\mean{u_x}/dz$
	- Boundary conditions _assumed_: the velocities at the boundaries _matches velocities of the plates_
	- Also assume the flow is _laminar_
- The _(dynamic) viscosity_ $\eta$ is then defined as:
$$\tau_{xz}=\eta\frac{d\mean{u_x}}{dz}$$

## Momentum flux
- Consider a case where _mean free path_ of the particles is _larger_ than the plate separation
- As molecules travel in the $+z$ direction, they _move from a layer of lower $\mean{u_x}$ to one of higher $\mean{u_x}$_, hence there is _net momentum transfer_ in the $-x$ direction to the upper layer
	- Similar, one travelling in the $-z$ direction has the opposite effect
- Therefore there is some _momentum flux_ $\Pi$ which is _opposite to the velocity gradient_, with a magnitude equal to $\tau_{xz}$:
$$\Pi=$$

## Viscosity of a gas
- Consider molecules travelling at some angle $\theta$ to the $z-$axis at a particular _plane of interest_:
$$dN=v\cos\theta\,f(v)dv\,\frac{1}{2}\sin\theta d\theta$$
- Since the last collision, the particle has travelled $\lambda\cos\theta$ in the $z-$direction
- The _transfer of momentum_ is then:
$$\Delta p=$$

- The viscosity is _independent of pressure_, as $\lambda\propto 1/n$ at _constant temperature_

- For _gases_, the viscosity _increases with temperature_

# Thermal conductivity
- The _heat flux_ $\bm{J}$ is the _power_ transported across a _unit area_
- The _thermal conductivity_ $\kappa$ in an _isotropic material_ is defined as:
$$\bm{J}=-\kappa\nabla T$$

- The _thermal conductivity_ is then found as:
$$\kappa=\frac{1}{3}nC\mean{v}\lambda=\frac{1}{3}C_V\mean{v}\lambda$$
- Like viscosity, heat transfer is _indpendent of pressure_, and $\propto T^{1/2}$

- One can calculate the _ratio_ between $\eta$ and $\kappa$:
$$\frac{\kappa}{\eta}=\frac{C_V}{m}$$
- This is the _specific heat capacity per unit volume_