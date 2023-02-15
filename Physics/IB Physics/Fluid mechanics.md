
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