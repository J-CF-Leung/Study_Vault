- Soft matter is matter that is often _deformed_ by _thermal fluctuations and mechanical stresses_

- The tendency to deform is determined by $E$, the _elastic modulus_
- Given _pressure_ $p=F/A$ and _strain_ $\delta L/L$:
$$E=\frac{p}{\delta L/L}$$
- Deformation under _atomospheric pressure_ $10^{5}\,\text{Pa}$
	- _Diamond_ has $E=1.2\times 10^{11}\,\text{Pa}$, which gives _strain_ $8\times 10^{-7}$
	- _Rubber_ has $E\sim 10^{7}\,\text{Pa}$, which gives strain $1\times 10^{-2}$
	- _Gelatin_ has $E\sim 10^{3}\text{Pa}$, which gives strain $100$
		- The strain is _no longer small_, hence the _elastic regime breaks down_

- The elastic modulus can be thought of _characteristic energy per characteristic volume_
- The characteristic energy is the _binding energy per atom_
- The characteristic volume is the _volume per atom_

- Given _thermal fluctuations_ $\sim k_{B}T$, the relevant _length scale_ $(k_{B}T/E)^{1/3}$ is typically _much larger than atomic spacing_
- Hence, _quantum effects are irrelevant_, and _all fluctuations are thermal_

- The _scaling behaviour_ of polymers are typically _independent of atomic composition_
- They also have both _viscous_ and _elastic_ properties
- They can also _self-assemble_ into structures

# Fluids
- A _fluid_ is a collection of _particles_ each with their own mass $m_{i}$, position $\boldsymbol{r}_{i}$ and velocity $\boldsymbol{v}_{i}$
- In some _continuum desciption_, one can take a _small region of space_ and _average over_ the number of particles to obtain the _coarse-grained quantities_ $\rho(\boldsymbol{r})$, $\boldsymbol{v}(\boldsymbol{r})$, etc.

- The fluid obeys _conservation laws_

- A _Newtonian fluid_ has _does not maintain shear_, but has _viscosity_, which is _constant_ and _independent of flow rate_

## Conservation laws
- The _total mass_ within some volume $V$:
$$M_{V}(t)=\int_{V} \, d^{3}\boldsymbol{r} \,\rho(\boldsymbol{r},t) $$
- The _total momentum_ within the volume:
$$\boldsymbol{P}_{V}(t)=\int_{V} \, d^{3}\boldsymbol{r}\,\rho(\boldsymbol{r},t)\boldsymbol{v}(\boldsymbol{r},t) $$
- $\rho \boldsymbol{v}$ is the _momentum density_

### Conservation of mass
- Any _change in mass_ must correspond to some _change in density_, as well as some _in/outflow_:
$$\frac{dM_{V}}{dt}=\int _{V} \, d^{3}\boldsymbol{r}\left( \frac{\partial \rho}{\partial t}\right)=-\int _{S}\rho \boldsymbol{v}\cdot \, d\boldsymbol{S}  $$
- Using the _divergence theorem_, and using the fact that this must be true for _arbitrary volumes_:
$$\frac{\partial \rho}{\partial t}+\nabla\cdot (\rho \boldsymbol{v})=0$$
- For an _incompressible_ fluid where $\rho(\boldsymbol{r},t)=\rho_{0}$:
$$\nabla\cdot \boldsymbol{v}=0$$

### Conservation of momentum
- The _change in momentum_ in some volume of fluid:
$$\frac{\partial P_{i}}{\partial t}=\int \, d^3 \boldsymbol{r} \frac{\partial}{\partial t}(\rho v_{i})$$

- This must take into account all the _contributing forces_, as well as the _momentum convection out of the volume_:
$$\partial_{t}P_{i}=\partial_{t}P_{i}^{\text{conv}}+\partial_{t}P_{i}^{\text{p}}+\partial_{t}P_{i}^{\text{visc}}+\partial_{t}P_{i}^{\text{body}}$$

- Define a _momentum flux density tensor_:
$$\Pi_{ij}=\rho v_{i}v_{j}$$
- The _momentum outflow_:
$$\partial_{t}P_{i}^{\text{conv}}=-\int  \, d^3\boldsymbol{r}\partial_{j}(\rho v_{i}v_{j})=-\int _{S} \Pi_{ij} n_{j}dS$$

### Force terms
- _Pressure_ from the fluid is _isotropic_:
$$\partial_{t}P_{i}^{\text{p}}=-\int_{S} pn_{i} \, dS=-\int _{S}p\delta_{ij} n_{j}\, dS  $$

- One can get _stresses_ in the fluid that are _tangential_
- Tensorial relation for force:
$$dF_{i}^{\text{visc}}=\sigma_{ij}n_{j}\,dS$$

- The _Newtonian viscous stress tensor_:
	- Equilibrium demands that the stress tensor be _symmetric_
	- One term _vanishes_ in the _surface integral_ as the fluid is _incompressible_
$$\sigma_{ij}^{\text{v}}=\eta(\partial_{i}v_{j}+\partial_{j}v_{i})$$
- For some fluids, it must be specified using a _fourth rank tensor_

- Along with _pressure_, this gives the _stress tensor_:
$$\sigma_{ij}=\sigma_{ij}^{\text{v}}-p\delta_{ij}$$
$$\partial_{t}(P_{i}^{\text{visc}}+P_{i}^{\text{p}})=\int \sigma_{ij}n_{j} \, dS=\int (\sigma_{ij}^{\text{v}}-p\delta_{ij})n_{j} \, dS  $$

- There are also _body forces_ $f_{i}$ such as _gravity_ or _electrostatic_ forces:
$$\partial_{t}P_{i}^{\text{body}}=\int _{V} f_{i}\, d^{3}\boldsymbol{r} $$

## Material derivative
- One can describe fluids by labelling _particles_ instead of _position_
- Let there be a _collection_ of particles occupying a _small volume_, known as a _fluid element_

- One can define a _material derivative_, for quantity $f$, which _follows the fluid_:
$$\frac{Df}{Dt}=D_{t}f=\frac{d}{dt}f[x(t),y(t),z(t),t]$$
- Applying the chain rule:
$$D_{t}=\partial_{t}+\boldsymbol{v}\cdot \nabla$$
- This accounts for the rate of change _along a streamline_

## Navier-Stokes equation
- Combing all of the above, for a _Newtonian incompressible fluid_, one gets the _Navier-Stokes equation_
$$\rho \frac{D\boldsymbol{v}}{Dt}=\rho[\partial_{t}\boldsymbol{v}+(\boldsymbol{v}\cdot \nabla)\boldsymbol{v}]=-\nabla p+\eta \nabla ^{2}\boldsymbol{v}+\boldsymbol{f}$$
- The left side is the _inertial term_, accounting for _change of momentum in a fluid element_
	- Consequence of _Newton's second law_
	- Using $\partial_{t}\boldsymbol{v}$ _does not describe particles_, so the second law cannot be used
- The right side gives the _force densities_, which involves a _pressure gradient_, _viscous force_, and the _applied force density_

- For a _conservative force_ (such as gravity):
$$\boldsymbol{f}=\nabla V$$

- The $(\boldsymbol{v}\cdot \nabla)\boldsymbol{v}$ term is _non-linear_
## Reynolds number
- Given a _characteristic length scale_ $L_{0}$, _velocity_ $u_{0}$
- One can define _time scale_ $T_{0}=L_{0}/u_{0}$, and _pressure_ $p_{0}=\eta u_{0}/L_{0}$

- Define the _Reynolds number_, which is _dimensionless_
$$\text{Re}=\frac{\rho u_{0}L_{0}}{\eta}$$
- _Rescale_ the Navier Stokes equation such that all quantities $(\tilde{p},\tilde{\boldsymbol{v}},\tilde{\partial}\dots)$ are all _dimensionless_:
	- With _no external driving force_
$$\text{Re}(\tilde{\partial}_{t}\tilde{\boldsymbol{v}}+(\tilde{\boldsymbol{v}}\cdot \tilde{\nabla})\tilde{\boldsymbol{v}})=-\tilde{\nabla}\tilde{p}+\tilde{\nabla}^{2}\tilde{\boldsymbol{v}}$$
- Flows of the _same Reynolds number_ will _behave similarly_
![[Reynolds number flows.png]]

- For _large_ Reynolds number $\text{Re}\gg 1$, the _inertial term_ $(\boldsymbol{v}\cdot \nabla)\boldsymbol{v}$ _dominates_
	- Viscosity is _negligible_
	- Flow typically becomes _turbulent_

### Stokes flow and the scallop theorem
- For _small_ Reynolds number $\text{Re}\ll 1$, the _viscous term_ $\nabla^{2}v$ _dominates_
	- Conditions: _viscous_, _small length and velocity scale_
- It is known as _Stokes flow_

- There is _much less turbulent_ as the fluid had _very little inertia_
- The Navier-Stokes equation becomes _linear_:
	- Allows for the use of _superposition_
	- Known as the _Stokes equation_
$$0=-\nabla p+\eta \nabla^{2}\boldsymbol{v}$$
- For an _external driving force_, the time derivative is determined by the _external driving force_, and is not negligible
	- Typically due to _boundary conditions_
	- Known as the _time-dependent Stokes equation_ (linear)
$$\rho\partial_t\boldsymbol{v}= -\nabla p-\eta \nabla^{2}\boldsymbol{v}$$

- _Without_ an external force, there is _no timescale_ associated with the fluid motion, hence it acts _instantaneously_
	- As there is _no inertia_
	- It is also much _less turbulent_
- If one _increases pressure_, the _flow pattern_ is unchanged, only the _flow velocity_

- Taking the _divergence_ of the Stokes equation also gives:
$$\nabla^{2}p=0$$
- Pressure obeys the _Laplace equation_

- If the _spatial direction_ is reversed, the _flow velocity_ and _pressure gradient_ change sign, making the Stokes equation _symmetric under spatial reversal_
	- Kinematic reversibility
	- _Flow lines_ do not contain enough information to deduce flow direction
	- Not the same as _thermodynamic_ reversibility as there is _energy dissipation_

![[Typical Re values.png]]
- _Micro-organisms and nanomachines_ in small scales, with a _reversible, periodic locomotion mechanism_, are _unable to translate_
	- Motion undergone in the _first half_ of the cycle will be _reversed_ in the second half
- This is the _scallop theorem_
- The mechanism must be _fast_ to _escape the low_ $\text{Re}$ regime
	- Much more difficult for smaller objects

- Therefore, propulsion at low $\text{Re}$ must require _breaking time-reversal symmetry_
	- Example: _flagella_, or _circular motion_
## Vorticity
- The _vorticity_ of a fluid is a _local angular rate of rotation_
- It is a _pseudo-vector_ field:
$$\boldsymbol{\omega}=\nabla\times \boldsymbol{v}$$
### Vorticity diffusion in Stokes flow
- For _Stokes flow_:
$$\rho\partial_{t}\boldsymbol{v}=-\nabla p+\eta \nabla^{2}\boldsymbol{v}$$
- Taking the _curl_:
$$\partial_{t}\boldsymbol{\omega}=\frac{\eta}{\rho}\nabla^{2}\boldsymbol{\omega}$$
- This is a _diffusion equation_ for $\boldsymbol{\omega}$
- Therefore, at _low Reynolds number_, vorticity _diffuses_
- The _kinematic viscosity_ $\eta/\rho$ is the _effective diffusion coefficient_

### General vorticity transport
- Use the vector identity:
$$\frac{1}{2}\nabla(|\boldsymbol{v}|^{2})=(\boldsymbol{v}\cdot \nabla)\boldsymbol{v}+\boldsymbol{v}\times(\nabla\times \boldsymbol{v})$$
- One can then take the _curl_ of the [[#Navier-Stokes equation]]:
$$\frac{D\boldsymbol{\omega}}{Dt}-(\boldsymbol{\omega}\cdot \nabla)\boldsymbol{v}=\frac{\eta}{\rho}\nabla^{2}\boldsymbol{\omega}$$
- This is the _general vorticity transport equation_

- For _two dimensional flow_, as vorticity is _out of the plane_, $(\boldsymbol{\omega}\cdot \nabla)\boldsymbol{v}$ _vanishes_
- This gives a _conservation of vorticity_
## Special cases of flow

### Mechanical equilibrium in gravity
- Let there be a _viscous fluid_, which is _at rest_ relative to the container ($\boldsymbol{v}=0$)
	- Otherwise, the fluid _loses energy_
- The Stokes equation is then:
$$\nabla p=-\rho g\hat{z}$$
- This can be integrated to obtain:
$$p(z)=p(0)-\rho gz$$
- Letting $p(0)=0$, this gives a _hydrostatic pressure_ $p_\text{hs}=-\rho gz$
- The _pressure gradient_ then _cancels out_ the gravitational body force:
$$-\nabla p_\text{hs}+\rho\boldsymbol{g}=0$$

### Steady couette flow
- Flow _induced through the relative movement_ of _walls_ in a container
	- Example: two _concentric cylinders_ rotating w.r.t. each other

- Let the flow be _steady state_
	- The system has _relaxed_ from the effect of the initial movement of the walls
$$\frac{\partial \boldsymbol{v}}{\partial t}=0$$
#### Planar Couette flow
- For a _planar geometry_, let a plate at $z=0$ be _stationary_ and have the _top plate_ at $z=h$ have velocity $v_{0}\hat{x}$
- Let there be _no external pressure gradient_ in $x-y$ either
- The system is _infinite_ in the $x-y$ plane and therefore be _translationally invariant_ in those directions, hence:
$$\boldsymbol{v}=\boldsymbol{v}(z)=v_{x}(z)\hat{x}$$
- From this, the _non-linear term_ $(\boldsymbol{v}\cdot \nabla)\boldsymbol{v}=0$
- This leaves:
$$\partial_{z}^{2}v_{x}(z)=0$$
- Let there be a _no-slip condition_:
$$v_{x}(z=0)=0 \hspace{1.5cm} v_{z}(z=h)=v_{0}$$
- This gives a _linear velocity profile_:
$$v_{x}(z)=v_{0} \frac{z}{h}$$
- One can then determine the _horizontal force_ required to _maintain velocity_:
$$F_{z}=\sigma'_{xz}A=\eta\frac{v_{0}A}{h}$$
- This can be used to _measure_ the viscosity of a fluid

- The _vorticity_ of the fluid:
$$\boldsymbol{\omega}=\frac{v_{0}}{h}\hat{y}$$
#### Circular couette flow
- Steady state flow: $\partial \boldsymbol{v}/\partial t=0$
- The flow is _along the surface_ of a cylinder:
$$\boldsymbol{v}=v_{\theta}(r)\hat{\theta}$$

- The _non-linear term_:
$$(\boldsymbol{v}\cdot \nabla)\boldsymbol{v}=\frac{v_{\theta}}{r}\frac{\partial}{\partial\theta}\left( v_{\theta}\hat{\theta} \right)=-\frac{v_{\theta}^{2}}{r}\hat{r}$$
- The _pressure gradient_ due to _centripetal force_:
$$\frac{dp}{dr}=\frac{\rho v_{\theta}^{2}}{r}$$
- The _vector Laplacian_:
$$\nabla^{2}\left( v_{\theta}(r)\hat{\theta} \right)=\left( \nabla^{2}v_{\theta}-\frac{v_{\theta}}{r^{2}} \right)\hat{\theta}$$
- From this, the _radial terms cancel out_, and the _azimuthal term vanishes_:
$$\frac{d^{2}v_{\theta}}{dr^{2}}+\frac{1}{r} \frac{dv_{\theta}}{dr}-\frac{v_{\theta}}{r^{2}}=0$$
- This gives the _solution_:
$$v_{\theta}=Ar+\frac{B}{r}$$
- The _constants_ depend on the _angular velocities_ of the cylindrical walls (no slip condition)

### Pressure-driven flow in a channel
- Have a _planar geometry_, where _neither plate is moving_
- There is a _pressure difference_ $\Delta p$ across the channel in the $x-$direction
	- Known as _Poiseuille flow_
- Similar to the Couette flow, $\boldsymbol{v}=v_{x}(z)\hat{x}$

- Assume a _linear pressure gradient_:
$$\frac{dp}{dx}=-\frac{\Delta p}{L}=\eta\frac{d^{2}v_{x}}{dz^{2}}$$
- This then gives a _parabolic_ velocity profile:
$$v_{x}=\frac{\Delta p}{2\eta L}(h-z)z$$
- For a _width_ $w$, this gives the _net flow rate_:
$$Q=\int \, dy\,dz\,v_{x} =\frac{wh^{3}}{12\eta L}\Delta p$$

- Similarly, for a _circular channel_ with radius $a$:
$$v_{x}(r)=\frac{\Delta p}{4\eta L}(a^{2}-r^{2}) \hspace{1.5cm}Q=\frac{\pi a^{4}}{8\eta L}\Delta p$$

- This is _analagous to Ohm's Law_, where a _flow rate_ is _proportional to_ the _driving force_
	- One can define the _hydraulic resistance_ $\Delta p/Q$
	- For _fluid storage_, one can also define a _capacitance/compliance_
![[Fluid law.png]]

### Momentum diffusion in boundary layer
- Consider an _infinite plane_ in the $x$ and $y$ directions, in contact with a fluid and _initially at rest_
- At $t=0$, one wall begins to have velocity $v\hat{x}$, with equation of motion:
$$\rho \partial_{t}v_{x}=\eta\partial_{z}^{2}v_{x}$$
- This is a _diffusion equation_ for transverse flow velocity $v_{T}=v_{x}$
- The _diffusion coefficient_ is
	- Same as the [[#Vorticity diffusion in Stokes flow|diffusion of vorticity]]
$$\nu\equiv\frac{\eta}{\rho}$$
- It is the _kinematic viscosity_

- There is a _characteristic length scale_:
$$\delta\sim\sqrt{ \frac{\eta}{\rho}t }$$
- This is the _thickness of the boundary layer_
	- The change in velocity _propagates_, until _steady state is achieved_ (Pouiseuille flow)
### Oscillatory flow near a surface
- Let there be an _oscillatory driving force_ on a boundary
- Assume the _planar geometry_, with $\boldsymbol{v}=v_{x}(z)\hat{x}$
- Time-dependent Stokes equation:
$$\rho\partial_{t}v_{x}=\eta\partial_{z}^{2}v_{x}$$

- Let the fluid be in _contact_ with a single surface at $z=0$, with oscillating frequency $\omega$
- The velocity is then:
$$v_{x}(z)=\tilde{v}_{x}(z)\exp(i\omega t)$$
- This has a _travelling wave solution_:
$$\displaylines{v_{x}=C\exp[i(\omega t-kz)] \\ k=\pm(1-i)\sqrt{ \frac{\omega \rho}{2\eta} }=\pm \frac{1-i}{\delta}}$$
- The _response_ is _out of phase_ with the driving
- $\delta$ is the _decay length_

- The _stress_ on the moving surface due to viscous forces:
$$\frac{F}{A}=\eta\partial_{z}v_{x}(z=0)=Re\left[(-1+i) \frac{\eta v}{\delta}\right]$$
- There is both an _in phase_ and an _out of phase_ component

## Stokes drag force on a sphere
- Consider a _spherical body_ of radius $a$ moving at velocity $\boldsymbol{v}$ through an _overall stationary fluid_
- It creates a _temporary disturbance_ in the flow field wherever it goes
- Work in the _low Reynolds number regime_ $(\text{Re}=\rho va/\eta\ll 1)$

- The _exact drag force_ experienced by the sphere is:
$$\boldsymbol{F}=6\pi \eta a\boldsymbol{v}$$
### Scaling argument
- _Ignoring_ the pressure gradient, for the _transverse velocity_:
$$\nabla^{2}v_{T}=0$$
- The _solution_:
$$v_T\sim \frac{v_{0}a}{r}$$
- This gives the _stress_:
$$F\sim \int \eta(\partial_{r} v_{T}) \, dS \sim 4\pi \eta av_0 $$
- This gives the correct _functional dependence_ for Stokes law

- In the _exact solution_:
$$\boldsymbol{F}_\text{viscous}=4\pi \eta a\boldsymbol{v}_{0}\hspace{1.5cm}\boldsymbol{F}_\text{pressure}=2\pi \eta a\boldsymbol{v}_{0}$$

# Elasticity
- _Hookean solids_ respond _immediately_ to stresses and change shape _without dissipating energy_

## Elastic strain tensor
- Denote a point in some body as $\boldsymbol{x}$
	- The _initial/reference state_
- When the object is _deformed_, the point is _moved_ to $\boldsymbol{x}'$
	- The _target state_
- Define the _displacement vector_:
$$\boldsymbol{u}=\boldsymbol{x}'-\boldsymbol{x}$$

- The _forces_ in the object _cannot_ depend on the _absolute displacement_
	- A _constantly displaced_ object cannot have elastic forces
- Only the _relative displacement_ matters

- Consider the _distance_ between two points initially _infinitesimally_ close together:
$$\displaylines{d\boldsymbol{x}=\boldsymbol{x}_{2}-\boldsymbol{x}_{1} \hspace{1cm} d\boldsymbol{u}=\boldsymbol{u}_{2}-\boldsymbol{u}_{1} \hspace{1cm}d\boldsymbol{x}'=d\boldsymbol{x}+d\boldsymbol{u} \\ dl^{2}=dx_{i}dx_{i} \longrightarrow dl'^{2}=dx_{i}'dx_{i}'}$$

- Expanding to _first order_, one gets:
$$dl'^{2}=dl^{2}+2\partial_{k}u_{i}dx_{i}dx_{k}$$
- One can identify the _strain tensor_:
$$d\boldsymbol{u}=\epsilon_{ik}dx_{k} \implies dl'^{2}=dl^{2}+2\epsilon_{ik}dx_{i}dx_{k}$$
- This gives the definition:
$$\epsilon_{ik}=\frac{1}{2}(\partial_{i}u_{k}+\partial_{k}u_{i})$$
- An _antisymmetric_ combination gives _rotation_, which _does not change the shape_ of the object and does not require force
	- Components of $\nabla\times \boldsymbol{u}$

- The _diagonal_ terms indicate a _deformation along an axis_
- The _off-diagonal_ terms indicate a _shear_
![[Shear vs rotation.png|400]]

- Common types of deformation:
![[Deformation types.png|600]]

- The strain can be _diagonalised_ for some point $\boldsymbol{x}$:
$$\displaylines{\underline{\underline{\epsilon}}=\begin{pmatrix}\epsilon_{11}&0&0 \\ 0&\epsilon_{22}&0 \\ 0&0&\epsilon_{33}\end{pmatrix} \\ dx_{i}'=(1+\epsilon_{ii})\,dx_{i}}$$
- The _volume change_, using only _linear terms_:
$$dV'=dx_{1}'dx_{2}'dx_{3}'\approx dV(1+\epsilon_{ii})$$
- Therefore, the _relative volume change_:
$$\frac{dV'-dV}{dV}=\epsilon_{ii}=\text{Tr}(\underline{\underline{\epsilon}})=\nabla\cdot \boldsymbol{u}$$

## Hooke's Law
- One can relate the _force_ $F_{i}$ to the _stress tensor_ $\sigma_{ij}$:
$$dF_{i}=\sigma_{ij}dS_{j}$$

- The most _general_ relation, given by _Hooke's Law_:
$$\sigma_{ij}=C_{ijkl}\epsilon_{kl}$$
- $C$ is the _stiffness tensor_

- The _minor symmetries_ of stress and strain:
$$\sigma_{ij}=\sigma_{ji} \hspace{1.5cm} \epsilon_{ij}=\epsilon_{ji}$$
- The _energy density_ of the material:
$$\frac{U}{V}=\frac{1}{2}\sigma_{ij}\epsilon_{ij}=\frac{1}{2}C_{ijkl}\epsilon_{ij}\epsilon_{kl}$$
- This gives the _major symmetry_:
$$C_{ijkl}=C_{klij}$$
- In 3 dimensions, this gives 18 _independent components_

## Elastic moduli
- For a _uniaxial deformation_:
$$\sigma_{x x}=E\epsilon_{x x}$$
- $E$ is the _Young's modulus_

### Poisson's ratio
- This typically gives a _strain along perpendicular directions_
- Define _Poisson's ratio_:
$$\nu=-\frac{\epsilon_{yy}}{\epsilon_{x x}}$$
- It is typically _positive_, but can be _negative_ (auxetic materials)
- In the case of _uniaxial deformation_:
$$E\epsilon_{x x}=\sigma_{x x}\hspace{1cm}E\epsilon_{yy}=-\nu\sigma_{x x}\hspace{1cm}E\epsilon_{zz}=-\nu \sigma_{x x}$$
- For a _general deformation_:
$$\begin{align}E\epsilon_{x x}&=+\sigma_{x x}-\nu\sigma_{yy}-\nu\sigma_{zz} \\ E\epsilon_{yy}&=-\nu\sigma_{x x}+\sigma_{yy}-\nu\sigma_{zz} \\ E\epsilon_{zz}&=-\nu\sigma_{xx}-\nu\sigma_{yy}+\sigma_{zz}\end{align}$$
- This can be _solved_ to get:
$$\sigma_{x x}=\frac{E}{(1+\nu)(1-2\nu)}[(1-\nu)\epsilon_{x x}+\nu\epsilon_{yy}+\nu\epsilon_{zz}]$$

### Bulk modulus
- The _volumetric deformation_ of a material:
$$\epsilon_{x x}+\epsilon_{yy}+\epsilon_{zz}=\text{Tr}(\epsilon)$$
- For an isotropic _pressure_:
$$-p=\text{Tr}(\sigma)$$
- The _bulk modulus_:
$$B=-\frac{p}{\text{Tr}(\epsilon)}$$
- This can be written as:
$$B=\frac{E}{3(1-2\nu)}$$
### Shear modulus
- The _shear modulus_:
$$\sigma_{xy}=2G\epsilon_{xy}$$
- Can be written as:
$$G=\frac{E}{2(1+\nu)}$$

## Physical constraints
- For $\nu\to 1/2$, the material is _incompressible_ as $B\to \infty$
	- Accurate for many _fluids_
- For $\nu\to-1$, the material is _maximally auxetic_ as $G\to \infty$

- One can show:
$$\sigma_{ik}=\left( B-\frac{2}{3}G \right)\epsilon_{l l}\delta_{ik}+2G\epsilon_{ik}$$

# Viscoelastic materials
- Many materials act both like a _fluid_, and as an _elastic solid_
- They are _viscoelastic_

- For _incompressible materials_, all deformations are _shear_
- The deformation leads to the material _storing energy_
- Once the material _flows_, the viscosity leads to _energy dissipation_

- _Viscosity_ can depend on _speed of flow_
- Leads to shear _thickening/thinning_ ($\eta$ increasing/decreasing) as the _strain rate_ $\partial_{t}\epsilon$ increases
	- Ketchup: shear thinning (due to disentanglement of polymer)
	- Cornstarch: shear thickening (creation of structures when sheared)
![[Viscoelastic behaviour.png]]

- Bheaviour of the material is tested using _time-dependent stress and strains_
![[Creep and stress relaxation.png]]

## Complex modulus
- The _viscoelastic behaviour_ of the solid is quantified by the _complex modulus_:
$$G(\omega)=G'(\omega)+iG''(\omega)$$
- where $G'$ and $G''$ are _real_

- The stress and strain are functions of the _history_ of the material
- It is a superposition of all _stress and strain increments_ from its history
$$\sigma(t)=\int_{0}^{t} \, d\sigma(t')=\int G(t-t') \, dt'=\int G(t-t') \frac{d\epsilon(t)}{dt}\, dt $$
- Due to _time translation invariance_, only the _interval_ $t-t'$ matters

- For a _Hookean solid_:
$$G(t-t')=G_{0}\implies \sigma(t)=G_{0}\epsilon(t)$$
- For a _Newtonian fluid_:
$$G(t-t')=\eta\,\delta(t-t')\implies \sigma(t)=\eta\,\dot{\epsilon}(t)$$

- For a _constant strain rate_ $\dot{\epsilon}$:
$$\sigma(t)=\dot{\epsilon}\int G(t-t') \, dt' $$
- There is an _effective viscosity_ 

- Consider an _oscillatory strain rate_:
$$\epsilon(t)=\epsilon_{0}\exp(i\omega t)$$
- Making the substitution $\tau=t-t'$, one gets:
$$\sigma(t)=i\omega\epsilon_{0}\exp(i\omega t)\int_{0}^{\infty} G(\tau)\exp(-i\omega \tau) \, d\tau $$
- Define:
$$\displaylines{G^{*}(\omega)=i\omega \int _{0}^{\infty}G(\tau)\exp(-i\omega \tau) \, d\tau \\ \sigma(t)=\epsilon(t)G^{*}(\omega)} $$
- From inspecting behaviour of the Hookean solid and Newtonian fluid:
	- $\mathrm{Re}(G^{*})$ is an _effective modulus_
	- $\mathrm{Im}(G^{*})/\omega$ is an _effective viscosity_

## Models of viscoelasticity

### Maxwell fluid
- Consider a _spring_ and _dashpot_ in _series_, with stresses and strains $\sigma_{S},\epsilon_{S}$ and $\sigma_{D},\epsilon_{D}$ respectively
- As they are connected in _series_:
$$\sigma_{S}=\sigma_{D}=\sigma \hspace{1.5cm}\epsilon_{S}+\epsilon_{D}=\epsilon$$
- The spring and dashpot behave as _Hookean solid_ and _Newtonian fluid_ respectively:
$$\sigma=G_{0}\epsilon_{S} \hspace{1.5cm}\sigma_{D}=\eta\dot{\epsilon}_{D}$$
- Using the above relations:
$$\dot{\epsilon}=\frac{\dot{\sigma}}{G_{0}}+\frac{\sigma}{\eta}$$
- Doing a _Fourier transform_:
$$\sigma(\omega)=\frac{i\omega\epsilon_{0}\eta}{G_{0}+i\omega \eta}\epsilon(\omega)=G^{*}(\omega)\epsilon(\omega)$$
- Rewrite as:

$$G^{*}(\omega)=\frac{i\omega G_{0}}{G_{0}/\eta+i\omega}\epsilon(\omega)$$
- Define the _relaxation time_ $\tau=\eta/G_{0}$
- For timescales $t\ll \tau$, it behaves as a _Hookean solid_ with $G^{*}(\omega)\to G_{0}$
- For timescales $t\gg \tau$, it behaces as a _Newtonian fluid_ with $G^{*}(\omega)\to i\omega \eta$

- For a _constant strain_:
$$\dot{\epsilon}=0 \implies \sigma=\sigma_{0}\exp\left( -\frac{t}{\tau} \right)$$
- This is _stress relaxation_

### Kelvin-Voigt solid
- Have the spring and dashpot in _parallel_:
$$\epsilon_{S}=\epsilon_{D}=\epsilon \hspace{1.5cm}\sigma_{S}+\sigma_{D}=\sigma$$
- This gives:
$$\sigma(\omega)=(G_{0}+i\omega \eta)\epsilon(\omega)$$
- For $t\ll \tau$, it behaves as a _Newtonian fluid_
- For $t\gg \tau$, it behaves as a _Hookean solid_

- For a _constant stress_:
$$\dot{\sigma}=0 \implies \epsilon=\frac{\sigma_{0}}{G_{0}}\left( 1-\exp\left( -\frac{t}{\tau} \right) \right)$$

### Zener model/standard linear solid
- Consider a _Maxwell fluid_ and a _Hookean solid_ in _parallel_
	- Maxwell fluid has elastic modulus $G_{2}$
	- The elastic solid has elastic modulus $G_{1}$
- There are _two timescales_:
$$\tau_{\sigma}=\frac{\eta}{G_{2}}\hspace{1.5cm}\tau_{\epsilon}=\eta \left( \frac{1}{G_{2}}+\frac{1}{G_{1}} \right)$$
- Combining the stresses:
$$\sigma(\omega)=\sigma _\text{solid}+\sigma _\text{Maxwell}=G_{1}\frac{1+i\omega \tau_{\epsilon}}{1+i\omega \tau_{\sigma}}\epsilon(\omega)$$
- For $\omega\to 0$, it approaches the _elastic solid_ with $G_{1}$
- For $\omega\gg \tau_{\sigma}^{-1}$, it approaches $G_{1}+G_{2}$

- One gets the same result for an _elastic solid_ and _Kelvin-Voigt solid_ in _series_

## Brownian motion
- Viscoelastic behaviour arises from _random motions_ of particles

- For a particle in some solution to _undergo Brownian motion_, the _thermal motion_ must be sufficient to _overcome_ the _gravitational energy_:
$$\frac{P(h)}{P_{0}}=\exp\left( -\frac{m_{b}h}{k_{B}T} \right)=\exp\left( -\frac{h}{\langle h \rangle } \right)$$
- Here, $\langle h \rangle$ is the _average height_
- Accounting for the Buoyant force, the _effective mass_ in the solution is:
	- $\Delta \rho$ is the _density difference_ between the particle and the solvent
$$m_{b}=\frac{4\pi}{3}r^{3}\Delta \rho$$
- The particle is _suspended_ if $\langle h \rangle>r$, as it _does not stay in the bottom_ of a container
- Example: _pollen_ in air, or _colloidal_ particles of micron width

## Langevin equation
- To account for the [[Advanced statistical mechanics#Stochastic physics|stochastic motion]] of the particle:
$$m \frac{d\boldsymbol{v}}{dt}=-\gamma \boldsymbol{v}+\boldsymbol{\xi}(t)$$
- $\gamma$ is the _drag coefficient_
	- In the case of [[#Stokes drag force on a sphere|Stokes flow]], $\gamma=6\pi \eta v$

- For _random motion_, as there is _no preferred direction_:
$$\langle \boldsymbol{\xi}(t) \rangle=0 $$
- As the motion is _uncorrelated_ at different times (_relaxation times_ are practically instantaneous):
$$\langle \boldsymbol{\xi}(t)\cdot \boldsymbol{\xi}(t') \rangle=G\delta (t-t') $$
- The [[Advanced statistical mechanics#Formal solution and fluctuation-dissipation theorem|formal solution]] to the Langevin equation:
$$\displaylines{\boldsymbol{v}=\boldsymbol{v}_{0}\exp\left( -\frac{\gamma}{m}t \right)+ \int _{0}^{t} \frac{\boldsymbol{\xi}(t')}{m}\exp\left[ -\frac{\gamma}{m}(t-t') \right] \, dt'  \\ \langle \boldsymbol{v}(t) \rangle=\boldsymbol{v}_{0}\exp\left( -\frac{\gamma}{m}t \right) }$$
- One can also derive:
$$\langle v^{2}(t) \rangle=v_{0}^{2}\exp\left( -\frac{2\gamma}{m}t \right)+\frac{c}{2m\gamma}\left[ 1-\exp\left( -\frac{2\gamma}{m}t \right) \right] $$

## Overdamped limit
- The dimension of $\eta$ is such that $\eta \sim \gamma/L$, where $L$ is some _length scale_
- Then by dimensional analysis, the _overdamped limit_ $\gamma t/m \to \infty$ corresponds to a _low_ [[#Reynolds number]]
$$\left<v^{2}(t)\right> \approx \frac{c}{2m\gamma}=\frac{3k_{B}T}{m}$$
- The latter comes from _equipartition_, giving:
$$c=6\gamma k_{B}T$$
- The damping is _independent of mass_, as expected (no inertial motion)
- The _dissipation_ from $\gamma$ is linked to the _fluctuation_ $c$:
$$\left<\boldsymbol{\xi}(t)\cdot \boldsymbol{\xi}(t')\right> = 6k_{B}T\gamma\delta(t-t')$$
- This is the [[Advanced statistical mechanics#Formal solution and fluctuation-dissipation theorem|fluctuation-dissipation theorem]]

- In the overdamped limit, the Langevin equation becomes:
$$\gamma \boldsymbol{v}=\gamma \dot{\boldsymbol{x}}=\boldsymbol{\xi}(t)$$
- One then gets:
	- Can be given by integrating the _full solution_, then taking the limit in the solution
$$\langle x^{2} \rangle=\frac{6k_{B}T}{\gamma}t \equiv 6Dt$$
- The _diffusion constant_ (Einstein relation)
$$D=\frac{k_{B}T}{\gamma}$$
- Factor of 6 in solution from consideration of _diffusion equation_

- The _Stokes-Einstein relation_, using formula for Stokes drag force:
$$D=\frac{k_{B}T}{6\pi \eta r}$$

- Define a _characteristic time_ for particles to diffuse distance $r$:
$$\tau=\frac{r^{2}}{D}$$
## Diffusion
- Diffusion equation:
$$\partial_{t}c=D\nabla^{2}c$$

- One can have a _diffusion-limited processes_

### Diffusion-limited cluster growth
- Consider particles _attaching_ themselves to a _cluster_ of radius $a$
	- The potential is _purely attractive_
- $a$ is taken as a _constant_ as it changes on a _timescale much larger than diffusion time_
- In the _steady state_, $\partial_{t}c=0$, giving _Laplace's equation_
- Boundary condition $c(r=a)=0$:
$$c=c_{\infty}\left( 1-\frac{a}{r} \right)$$
- The spatial part of the diffusion equation can be written as a _flux_:
$$\partial_{t}c=-\nabla\cdot \boldsymbol{J} \implies \boldsymbol{J}=-D\nabla c$$
- In this case:
$$\boldsymbol{J}=-Dc_{\infty} \frac{a}{r^{2}}\hat{r}$$
- Then the _change in number of particles in the cluster_:
$$\frac{dN}{dt}=-J(r=a)4\pi a^{2}=4\pi Dc_{\infty}a \sim \frac{d(a^{3})}{dt}$$
- Therefore:
$$a \sim \sqrt{ t }$$
- This _ignores the structure of the cluster_

## Diffusion in an external potential
- In the _overdamped limit_, with some _external potential_:
$$\gamma \boldsymbol{v}=-\nabla V+\boldsymbol{\xi}=-k\boldsymbol{x}+\boldsymbol{\xi}$$
- In _analogy_ with the general case without potential:
$$\left<x^{2}\right>_{k}=x_{0}^{2}\exp\left( -\frac{2k}{\gamma}t \right)+\frac{3k_{B}T}{k}\left( 1-\exp\left( -\frac{2k}{\gamma}t \right) \right)$$
- The new _relaxation time_:
$$\tau_{k}=\frac{\gamma}{k}$$
- Over the relaxation time:
$$\frac{1}{2}k\left<x^{2}\right> = \frac{3k_{B}T}{2}$$

- From the consideration of a [[Advanced statistical mechanics#Markov chains|Markov process]], the general _diffusion equation_:
$$\partial_{t}c=D\nabla^{2}c+\frac{1}{\gamma}\nabla\cdot(c\nabla U)=-\nabla\cdot \boldsymbol{J}$$
### 1-dimensional potential barrier
- Consider a system which is _metastable_ at $x=A$, separated by a barrier that _peaks_ at $P$, leading to _true equilibrium_ at $x=B$
- In the _steady state_, $\partial_{t}c=\partial_{x}J=0$:
$$J=-D\partial_{x}P-\frac{\partial_{x}U}{\gamma}P=-D\exp(-\beta U)\partial_{x}[\exp(\beta U)P]$$
- The second equality is from the [[#Diffusion|Einstein relation]]
- Then multiplying both sides by $\exp(\beta U)$ and _integrating_:
$$J\int _{A}^{B}\exp(\beta U) \, dx=-D[\exp(\beta U)P]_{A}^{B} $$
- For a _deep_ potential well, the RHS is $DP(A)$
- From the method of _steepest descent_, the _dominant contribution_ is from where $U$ is _maximum_:
$$U\approx U_{P}-\frac{1}{2}k(x-x_{P})^{2}$$
- Combining this gives:
$$J=D\exp(-\beta U_{P})\sqrt{ \frac{k}{2\pi k_{B}T} }P(A)\propto \exp(-\beta U_{P})$$
- It is _proportional_ to the negative exponential of the _barrier height_
- This is the _Arrhenius relation_

### Reaction controlled processes
- Let there be a _potential barrier_ for particles attaching to a [[#Diffusion-limited cluster growth|cluster]]
- Write the _radial current_ as:
$$J=\frac{\dot{N}}{4\pi r^{2}}=-D\left(  \frac{d}{dr} \frac{U}{k_{B}T}+\frac{d}{dr} \right)c(r)$$
- Write the concentration as:
$$c(r)=\Phi(r)\exp(-\beta U) \implies J=D\exp(-\beta U) \frac{d\Phi}{dr}$$
- Then by _integrating_:
$$\Phi(\infty)-\Phi(a)=\frac{\dot{N}}{4\pi D}\int _{a}^{\infty} \frac{\exp(\beta U)}{r^{2}} \, dr \equiv \frac{\dot{N}}{4\pi D\lambda} $$
- Here, $\lambda$ is the _length scale_ of the process

- This gives:
$$c(a)=c_{\infty}\exp(-\beta U)\left( 1-\frac{k}{4\pi D\lambda } \right)$$
- Defining the _reaction constant_:
$$\dot{N}=kc_{\infty}$$
- For a _purely diffusion controlled process_, $U=0$ and $\lambda=a$, hence $c(a)=0$
- Adding the _reaction constants_:
$$k^{-1}=k_\text{diff}^{-1}+k_\text{reac}^{-1}$$

## Microrheology
- _Tracer particle_ in a _viscoelastic fluid_

- If it is in a _purely viscous fluid_, from the _Langevin_ equation:
$$\left<x^{2}\right> = \frac{k_{B}T}{\pi \eta v}t$$
- For a _purely elastic_ fluid:
$$\left<x^{2}\right> =\frac{3k_{B}T}{k}$$
- For a _time-dependent viscosity_, consider the _generalised Langevin equation_:
$$m \frac{dv}{dt}=-\gamma \int _{0}^{\tau} \gamma(t-\tau)v(\tau) \, d\tau +\xi(t)$$
- Consider the _Laplace transform_:
$$\mathcal{L}[f]=\int _{0}^{\infty}f(t)\exp(-st) \, dt $$
- From the _convolution theorem_ for $\mathcal{L}$:
$$ms\hat{v}(s)-m\hat{v}(0)=-\gamma(s)v(s)+\xi(s)$$
- Correlation:
$$\left<\hat{v}(s)v(0)\right>$$
- Mean square displacement:
$$\mathcal{L}(\left<x^{2}\right>)=\frac{6k_{B}T}{s^{2}\hat{\gamma}(s)}$$
- This is the _generalised Einstein relation_
# Polymers
- _Polymers_ make up a large variety of materials
	- They can be _naturally occuring_ or _synthetic_

- They are often modelled as being on a _lattice_
- Each _link_ on a lattice can represent a _monomer_ in the chain
- The chain follows a _random walk_

## Chains
### The ideal chain
- Let the chain have $N$ _monomers_
- Let the _length_ of a monomer (lattice cell size) be $b$

- Consider the _end-to-end displacement_ $\boldsymbol{R}$
- On _average_, as the walk is _completely random_:
$$\left<\boldsymbol{R}\right>=0$$
- Let the vector for the $i-$th step be $\boldsymbol{U}_{i}$
- As they are _random_, they are _uncorrelated_
$$\boldsymbol{R}=\sum_{i=1}^{N}\boldsymbol{U}_{i}\hspace{1.5cm}\left<\boldsymbol{U}_{i}\cdot \boldsymbol{U}_{j}\right>=0$$
- From this:
$$\left<R^{2}\right>=Nb^{2}\implies R=\sqrt{ N }b\propto N^{1/2}$$
- Analagous to _diffusion_, with $N$ in the role of _time_

- Define the _exponent_ $\nu$:
$$R\propto N^{\nu}$$
- For the _ideal chain_, $\nu=1/2$

### Real chains and Kuhn length
- Typically, _real chains_ have $\nu>1/2$
	- The _excluded volume_ of the polymer causes it to _swell_

- $R$ also scales with some _natural length scale_
- It is _not necessarily the size of a monomer_
- For real chains, it is known as the _Kuhn length_ $b$

### Freely jointed chain
- Let monomers have a _fixed step size_ $b_{0}$, but also be able to _freely rotate_ around some _axis_
- The axis is _fixed_ as there is a characteristic _bond angle_ $\theta$
- The average end-to-end distance:
$$\left<R^{2}\right>=\sum_{i=1}^{N}|\boldsymbol{U}_{i}|^{2}+2\sum_{i=1}^{N}\sum_{j=1}^{N}\left<\boldsymbol{U}_{i}\cdot \boldsymbol{U}_{j}\right>$$
- To consider the second term, _project_ $\boldsymbol{U}_{i}$ along $\boldsymbol{U}_{i+1}$:
$$\boldsymbol{U}_{i}=\frac{\boldsymbol{U}_{i}\cdot \boldsymbol{U}_{i+1}}{b_{0}^{2}}\boldsymbol{U}_{i+1}+\boldsymbol{U}_{i,\perp}=\cos\theta \boldsymbol{U}_{i+1}+\boldsymbol{U}_{i,\perp}$$
- Then consider the _correlation_ to a monomer _two links away_:
$$\left<\boldsymbol{U}_{i}\cdot \boldsymbol{U}_{i+2}\right>=\cos\theta \left<\boldsymbol{U}_{i+1}\cdot \boldsymbol{U}_{i_{+1}}\right>+\left<\boldsymbol{U}_{i,\perp}\cdot \boldsymbol{U}_{i+2}\right>=b^{2}_{0}\cos^{2}\theta$$
- The second term _vanishes_ due to free rotation
- From _recursion_:
$$\left<\boldsymbol{U}_{i}\cdot \boldsymbol{U}_{j}\right>=b_{0}^{2}(\cos\theta)^{|j-i|}$$
- Therefore, approximating $N$ as _infinity_:
$$\left<R^{2}\right>=Nb_{0}^{2} \frac{1+\cos\theta}{1-\cos\theta}$$
- The _scaling_ $\nu=1/2$ is retained, but the _Kuhn length_ is now:
$$b=b_{0}\sqrt{ \frac{1+\cos\theta}{1-\cos\theta} }$$
### Bead-spring model
- A model which lends itself to _statistical analysis_
- Describe a chain as a _series of beads_, connected by _springs_ with spring constant $\kappa$
- Let the _natural lengths_ be zero
	- Good model for _high temperatures_

- The potential of the chain:
$$U=\sum_{i=1}^{N-1} \frac{1}{2}\kappa \left| \boldsymbol{r}_{i+1}-\boldsymbol{r}_{i} \right|^{2} $$
- The [[Advanced statistical mechanics#Canonical ensemble and the partition function|partition function]]:
$$Z(R)=\prod_{i=1}^{N-1}\int\, d^{3}\boldsymbol{r}_{i} \exp\left[ -\frac{\kappa}{2k_{B}T}\left(|\boldsymbol{r}_{0}-\boldsymbol{r}_{1}|^{2}+\dots|\boldsymbol{r}_{N-1}-\boldsymbol{r}_{N}|^{2} \right)  \right]$$
- Integrating over an _intermediate degree of freedom_:
$$\int  \, d^{3}\boldsymbol{r}_{1}\exp[-\alpha|\boldsymbol{r}_{0}-\boldsymbol{r}_{1}|^{2}-\alpha|\boldsymbol{r}_{1}-\boldsymbol{r}_{2}|^{2}]=\sqrt{ \frac{\pi}{2\alpha} }\exp(-\alpha|\boldsymbol{r}_{0}-\boldsymbol{r}_{2}|^{2}) $$
- From this:
$$\displaylines{Z(R)\propto \exp\left( -\frac{\kappa R^{2}}{2k_{B}TN} \right) \\ \left<R^{2}\right>= \frac{\int Z(R)R^{2} \, d^{3}R}{\int Z(R) \, d^{3}R } =\frac{3k_{B}T}{\kappa}N}$$
- The _effective Kuhn length_ is now a _thermodynamic quantity_:
$$b^{2}=\frac{3k_{B}T}{\kappa}$$

- The _end-to-end distance_ in the chain then follows _Gaussian statistics_:
$$P(R)=G(\boldsymbol{R},N)=\left( \frac{3}{2\pi Nb^{2}} \right)^{3/2}\exp\left[ -\frac{3}{2} \frac{|\boldsymbol{r}_{0}-\boldsymbol{r}_{N}|^{2}}{Nb^{2}} \right]$$
- Here, $G$ is the _correlation function_ of the entire _chain_
### Segment correlation in an ideal chain
- Two random beads _within_ a polymer are typically _correlated as if they are the two ends_ of a shorter polymer
- Define a _correlation function_ using the _Gaussian statistics_ of the ideal chain:
$$G(\boldsymbol{r}_{m}-\boldsymbol{r}_{n},m-n)=\left[ \frac{3}{2\pi|m-n|b^{2}} \right]^{3/2}\exp\left[ -\frac{3}{2} \frac{|\boldsymbol{r}_{0}-\boldsymbol{r}_{N}|^{2}}{|m-n|b^{2}} \right]$$
- It is the _probability density_ for $\boldsymbol{r}_{n}$ for a _given_ $\boldsymbol{r}_{m}$
- As expected, it _convolves_, indicating the _joining_ of two chains
$$\int G(\boldsymbol{r}_{m}-\boldsymbol{r}_{k},m-k)G(\boldsymbol{r}_{k}-\boldsymbol{r}_{n},k-n) \, d^{3}\boldsymbol{r}_{k}=G(\boldsymbol{r}_{m}-\boldsymbol{r}_{n},m-n) $$

- The form of $G$ is _identical_ to the solution to a _diffusion equation_
	- The _random walk_ of a polymer can be modelled as _diffusion_, with $n$ acting as _time_ and $b^{2}/6$ as the _effective diffusion constant_
$$\left( \partial_{n}-\frac{b_{0}^{2}}{6}\nabla^{2} \right)G(\boldsymbol{r}_{m}-\boldsymbol{r}_{n},m-n)=\delta(\boldsymbol{r}_{m}-\boldsymbol{r}_{n})\delta_{mn}$$
### Semi-flexible polymers
- Account for the _stiffness_ of joints
- Let the polymer of _fixed length_ $l$ be described by some _curve_, with some _tangent angle_ $\theta$ at each point

- Label points on the chain by $s$, with a _quadratic potential_ to penalise _bending_:
$$U=\frac{C_{B}}{2}\int _{0}^{l}[\partial_{s}\theta(s)]^{2} \, ds $$
- $C_{B}$ quantifies _rigidity_ of the polymer
- Suitable for modelling polymers where the _bending length scale_ is on the order of the _chain size_ (e.g. DNA)

- The _equipartition theorem_ yields:
	- For a _short polymer_ so the approximation of $d\theta/ds \sim \theta/b_{0}$ applies
$$\left<\left( \frac{d\theta}{ds} \right)^{2}\right>=\frac{2k_{B}T}{C_{B}b_{0}}$$
- The _persistence length_ is the _characteristic length scale_ of the system:
$$l_{p}=\frac{C_{B}}{k_{B}T}=\frac{b_{0}}{2}$$
- The _end-to-end distance_:
$$\left<R^{2}\right>=\left<\int_{0}^{l}  \, \frac{d\boldsymbol{r}}{ds}ds\cdot \int _{0}^{l} \frac{d\boldsymbol{r}}{ds'} \, ds'\right> =  $$
### Entropy of the ideal chain
- The probability distribution for the ideal chain:
$$P(\boldsymbol{R},N)=\left[ \frac{3}{2\pi Nb_{0}^{2}} \right]^{3/2}\exp\left( -\frac{3R^{2}}{2Nb_{0}^{2}} \right)$$
- The _entropy_ of the chain:
$$S=k_{B}\ln\Omega=-k_{B} \frac{3}{2}\frac{R^{2}}{Nb_{0}^{2}}+S(0)$$
- The _free energy_:
	- There is _zero_ internal energy as the monomers _do not interact_ with each other
$$F=U-TS=k_{B}T \frac{3}{2} \frac{R^{2}}{Nb_{0}^{2}}+F(0)$$
- As expected for a _Hookean spring_
- The _spring constant_ is _proportional to temperature_

- Entropy is _higher_ for _lower_ $R^{2}$ as it is _more likely_

### Lattice random walk
- For a polymer on a _1D lattice_, let it undergo _steps_ to the left and right, with $N_{-}$ and $N_{+}$ steps respectively
- The _length_ $x$ is given by $(N_{+}-N_{-})b_{0}=\Delta Nb_{0}$

- The entropy is:
$$S=k_{B}\ln W=k_{B}\ln \begin{pmatrix}N\\N_{+}\end{pmatrix}\approx N\ln 2-\frac{(\Delta N)^{2}}{2N}$$
- This gives the probability:
$$P \propto \exp\left[ -\frac{(\Delta N)^{2}}{2N} \right]\propto \exp\left[ -\frac{x^{2}}{2Nb_{0}^{2}} \right]$$

## Polymer interactions
- _interactions_ of the chain with _itself_

- For a random walk, it may _self-intersect_
- As lattice sites can only be singly occupied, this leads to a _repulsive_ effect

- The polymer can be modelled as being in a _solvent_
- A _repulsion_ from itself can be considered as being _attractive_ to the solvent

### Flory-Huggins free energy
- Let the _monomer fraction_ in the solution be $\Phi_{A}$, with $\Phi_{B}=1-\Phi_{A}$
- Let the _total number of sites_ be $M$
- The entropy of the solution is then:
$$S_{S}=k_{B}\ln W=k_{B}\ln \frac{M!}{N_{A}!N_{B}!}=-k_{B}M[\Phi_{A}\ln \Phi_{A}+\Phi_{B}\ln \Phi_{B}]$$
- Ignoring _additive constants_:
$$S_{P}=-k_{B}M \left[ \frac{\Phi}{N}\ln \Phi+(1-\Phi)\ln(1-\Phi) \right]$$
- The factor of $1/N$ corresponds to _reduced translational entropy_ as monomers occupy adjacent sites
- The second term corresponds to contributions from the _solvent_

- The _internal energy_, accounting for _monomer-monomer interactions_ $\chi_{MM}$, _monomer-solvent_ interactions $\chi_{MS}$, and _solvent-solvent interactions_ $\chi_{SS}$:
$$\frac{E}{Mk_{B}}=\frac{T}{2}\chi_{MM}(T)\Phi^{2}+T\chi_{MS}\Phi(1-\Phi)+\frac{T}{2}\chi_{SS}(1-\Phi)^{2}$$
- Thsi can be written as:
$$\displaylines{\frac{E}{M}=\chi k_{B}T\Phi(1-\Phi) \\ \chi=\chi_{MS}-\frac{1}{2}(\chi_{MM}+\chi_{SS})}$$
- $\chi$ is known as the _Flory parameter_

- The _free energy upon mixing_ is then:
$$f=\frac{F}{M}=k_{B}T\left[ \frac{\Phi}{N}\ln \Phi+(1-\Phi)\ln(1-\Phi)+\chi \Phi (1-\Phi) \right]$$
- For _small_ $\Phi$:
$$f\approx k_{B}T\left[ \frac{\Phi}{N}\ln \Phi+\frac{1}{2}\Phi^{2}(1-2\chi)+\frac{\Phi^{3}}{6} \right]$$
- The second term acts as a [[Advanced statistical mechanics#Virial expansion|second virial coefficient]]

- If $1-2\chi<0$, there is an _attractive force_, and there is a _coil to globule transition_, and:
$$R \sim N^{1/3}$$
- If $1-2\chi=0$ (the $\theta$ point), it is an _ideal chain_:
$$R \sim N^{1/2}$$
- If $1-2\chi>0$, there is a _swollen chain_ (the chain tends to be attracted to the _solvent_)
$$R \sim N^{3/5}$$
### Excluded volume interaction and swelling
- The free energy can also be written in terms of a _repulsive term_ and the _entropic term_
- The repulsion term goes like $V\Phi^{2} \propto N^{2}/V$
- The free energy:
$$\frac{F}{k_{B}T}\sim \nu \frac{N^{2}}{V}+\frac{R^{2}}{Nb_{0}^{2}}\sim \nu \frac{N^{2}}{R^{3}}+ \frac{R^{2}}{Nb_{0}^{2}}$$
- Finding the _minimum_:
$$R^{5} \sim \nu b_{0}^{2}N^{3}$$
- For an excluded volume interaction, $\nu\sim b_{0}^{3}$, giving:
$$R \sim b_{0}N^{3/5}$$
- This gives the scaling relation for the _swollen chain_

### Osmotic pressure
- The _osmotic pressure_:
$$\Pi=- \frac{\partial F}{\partial V}\Bigg|_{N_{A}}=\frac{k_{B}T}{b_{0}^{3}}\left[ \frac{\Phi}{N}+ \frac{1}{2}(1-2\chi)\Phi^{2} \right]$$
### Polymer melt
- Let the _solvent_ be another polymer of _identical polymer_, with different _degree of polymerisation_
$$f\approx k_{B}T\left[ \frac{\Phi}{N}\ln \Phi+\frac{1}{2}\Phi^{2}\left( \frac{1}{N_{2}}-2\chi \right)+\frac{\Phi^{3}}{6} \right]$$
- For _high_ $N_{2}$, and since they are the _same polymer_, $\chi\to 0$, the _second virial coefficient vanishes_
- The $\theta$ point is _always reached_
- As there is _no relative interaction_ between chain and "solvent", the excluded volume interaction is "screened"

### Variation of Flory parameter
- Typically, the Flory parameter _increases with temperature_
- At high temperature, there tends to be a _coil in solution_
	- The _high entropy case_
- The _coil to globule transition_ happens for a _decreasing temperature_

- There are _temperature-responsive poiymers_, with _sharp coil-to-globule transitions_ at _high temperatures_

### Semi-dilute solutions
- For _low-concentration_ solutions, chains typically _do not overlap_
	- They have an _effective radius_ which is _smaller_ than average distance between chains
- At some concentration $c^{*}$, there is an _onset_ where chains start to _overlap_
- Above that concentration, there is a _semi-diulute_ solution where chains start to _interact with each other_

- At the onset, the _overall concentration_ is roughly equal to _concentration of segments in a single polymer_ (in a good solvent):
$$\Phi^{*}\sim \frac{Nb_{0}^{3}}{(\sqrt{ R^{2} })^{3}}\sim N^{-4/5}$$

## Polymer applications

### Brushes
- Let a surface be _grafted_ with polymers a spacing $D$ apart
- The _grafting density_ is $\sigma=1/D^{2}$

- The _mushroom_ regime has $D\gg R$, and they barely interact
- If $D\sim R$, they start to _overlap_ and act roughly as in a _solution_, $D\sim R\sim b_{0}N^{3/5}$

- For $D\ll R$, it is a polymer _brush_
- Let it be of height $h$
- The [[#Entropy of the ideal chain|entropic]] part of the free energy scales as $h^{2}/(Nb_{0})$
	- Due to _stretching_ of the polymer
- From [[#Excluded volume interaction and swelling|excluded volume]], free energy scales as $b_{0}^{3}N^{2}/V=b_{0}^{3}N^{2}\sigma/h$
- The _total free energy_:
$$\displaylines{F=k_{B}T \frac{h^{2}}{b_{0}N}+k_{B}T \frac{b_{0}^{3}N^{2}\sigma}{h} \\ \frac{\partial F}{\partial h}=0 \implies h \sim (b_{0}^{5}\sigma)^{1/3}N}$$
- The polymers are _fully stretched_, compared to in solution

- Grafted polymers can be used in _colloidal suspensions_
- They can also be used to _reduce friction_ as long as the timescale of the motion is _slower than relaxation time_

### Rubber elasticity
- Rubbers can be modelled as a _dense polymer melt_, with _cross-linking_ between polymers
- Let there be a _number density_ of crosslinks $n/V$

- Assume the _affine network model_, where there is _uniform shear_ of the polymers
- Let the _original_ end-to-end distances in each direction be $R^{0}_{x,y,z}$
- The _shear_:
$$R_{x,y,z}=\lambda_{x,y,z}R^{0}_{x,y,z}$$
- The [[#Entropy of the ideal chain|free energy]] difference when _stretching_:
$$\frac{\Delta F}{n}=\frac{3k_{B}T}{2Nb_{0}^{2}}\sum_{x,y,z}(R_{i}^{0})^{2}(\lambda_{i}^{2}-1)$$
- For the _ideal chain_:
$$(R^{0}_{x})^{2}=(R^{0}_{y})^{2}=(R^{0}_{z})^{2}=\frac{Nb_{0}^{2}}{3}$$
- This gives:
$$\Delta F=\frac{nk_{B}T}{2}(\lambda_{x}^{2}+\lambda_{y}^{2}+\lambda_{z}^{2}-3)$$

- Let there be a _uniaxial stretch_, for an _incompressible rubber_:
$$\lambda_{x}\lambda_{y}\lambda_{z}=1 \implies \lambda_{y}=\lambda_{z}=\frac{1}{\sqrt{ \lambda_{x} }}\equiv \frac{1}{\sqrt{ \lambda }}$$
- The difference in free energy:
$$\Delta{F}=\frac{nk_{B}T}{2}\left( \lambda^{2}+\frac{2}{\lambda }-3 \right)$$
- The _force_ required is $f_{x}=\partial(\Delta F)/\partial(\lambda_{x}L_{0})$
- The _stress_ is then:
$$\sigma_{x}=\frac{f_{x}}{\lambda_{y}\lambda_{z}L_{0}^{2}}=\frac{nk_{B}T}{V}\lambda\left( \lambda-\frac{1}{\lambda^{2}} \right)$$
- The elasticity is _non-linear_
- Assuming $\lambda$ is _small_, such that $\lambda=1+\epsilon_{x}$:
$$\sigma_{x}=3 \frac{n}{V}k_{B}T\epsilon_{x}=E\epsilon_{x x}$$
- This gives the _Young's modulus_:
$$E=3 \frac{n}{V}k_{B}T$$
- Given the material is _incompressible_, $\nu=1/2$, and $G=E/3$
- The _shear modulus_ is:
$$G=\frac{n}{V} k_{B}T$$
- The rubber becomes _stiffer_ as temperature _increases_
	- Also increases _linearly_ with crosslink density
- The elasticity is _entropic_
	- Corresponds to the [[#Entropy of the ideal chain|entropy of the chain]] itself due to stretching

## Rouse model of polymer dynamics
- Use [[#Overdamped limit|overdamped Langevin dynamics]] for the Gaussian chain
$$\gamma\frac{d\boldsymbol{R}_{n}}{dt}=\kappa(\boldsymbol{R}_{n+1}+\boldsymbol{R}_{n-1}-2\boldsymbol{R}_{n})+\boldsymbol{\xi}_{n}(t)$$
- Applicable for _low Reynolds numbers_
- Ignores _hydrodynamics_, or _solvent interactions_
- Works for _dense polymer solutions_

- In the _continuum limit_:
$$\gamma\frac{ d\boldsymbol{R}}{dt}=u \frac{\partial^{2}\boldsymbol{R}}{\partial \eta^{2}}+\boldsymbol{\xi}(t)$$
- _Fourier transform_

- The _cnetre of mass_ undergoes _diffusion_:
$$N\gamma \frac{dX_{0}}{dt}=\boldsymbol{\xi}_{0}(t)$$
- The effective _diffusion constant_ is
$$D_\text{eff}=\frac{k_{B}T}{\gamma N}$$
- The other Fourier modes:
$$2N\gamma \frac{d\boldsymbol{X}_{p}}{dt}=-k_{p}X_{p}+\xi_{p}(t)$$
- The _spring constant in Fourier space_:
$$k_{p}=$$
- Define a _relaxation time_:
$$\tau_{p}=\frac{N\gamma}{k_{p}}$$
- The _slowest relaxation time_ is the _Rouse time_ $\tau_{1}$

- The _correlation_:
$$\left<X_{q}^{i}(t)X_{q'}^{j}(t)\right>= \frac{k_{B}T}{k_{p}} \delta_{qq'} \delta_{ij} \exp\left[ - \frac{|t-t'|}{\tau_{p}} \right]$$
- The _stress_ from this is:
$$\sigma_{ij}=\frac{\epsilon c}{N}\sum_{p}k_{p} \left<X_{p}^{i}X_{p}^{j}\right> \sim \frac{\epsilon c}{N} \sum_{p} k_{p}T \exp\left( -\frac{t}{\tau_{p}} \right)=G(t)\epsilon$$
- $c$ is the _chain concentration_
- The shear modulus can be written as:
$$G(t)=c \frac{k_{B}T}{N} \sum_{p} \exp\left( -\frac{p^{2}t}{\tau_{1}} \right)$$
- For _long timescales_, it behaves as a [[#Maxwell fluid]]
$$G(t)\approx c \frac{k_{B}T}{N} \exp\left( -\frac{t}{\tau_{1}} \right)$$
- For _short timescales_:
$$G \sim \int \exp\left( -\frac{p^{2}t}{\tau_{1}} \right) \, dp\sim \sqrt{ \frac{\tau_{1}}{t} } $$
## Helix to coil transition
- Many polymers can undergo a transition from a _disordered globule_ to a _helical state_
	- Driving force includes _hydrogen bonding_
- Let the helical state have some _energy_ $-\epsilon$

- Model it as a _two-state system_:
$$Z_{1}=1+\exp(-\beta\epsilon) \implies f_\text{helix}= \frac{\exp(-\beta\epsilon)}{1+\exp(-\beta\epsilon)}$$
- It is a _gradual transition_

- Alternatively, consider an _on-off model_:
$$Z_{1}=1+ \exp(-\beta N\epsilon) \implies f_\text{helix}= \frac{\exp(-\beta N\epsilon)}{1+ \exp(-\beta N\epsilon)}$$
- This gives a much _sharper_ transition

- Or, the _Zimm-Bragg model_
- The _nearest neighbour_ interactions are parametrised with $\sigma$

$$f_\text{helix}= \frac{1}{2}\left( 1+ \frac{s-1}{\sqrt{ (1-s)^{2}+4\sigma s }} \right)$$
# Molecular self-assembly
- The formation of _structures_ from purely _inter-molecular forces_
- Molecules can assemble into _different structutes_, such as _spherical/cylindrical micelles_, or _lamellae_
	- Can be quantified using _shape/packing parameters_
- Proteins (biopolymers) can self-assemble into _filaments_ and _microtubules_

## Forces
- _Hydrogen bonding_, where _dipole moments_ in molecules interact
- _Hydrophobicity_, where an _entropic force_ makes hydrophobic/phillic parts of molecules stick to each other
	- _Amphiphillic_ molecules have _hydrophilic_ and _hydrophobic_ parts
- _Electrostatics_, where charged parts of molecules interact
	- From _screening_, it typically _decays exponentially_
	- The length scale is typically _short_

## Critical concentration
- Often, there is a _critical concentration_ above which the molecules will self-assemble
- _At_ the critical concentration, for a _cluister_ of size $\alpha$ made out of monomer $I$:
$$\mu_{\alpha}=\mu_{I}$$
- Assume the clusters _do not interact with each other_

- The partition function is then:
$$Z= \prod_{\alpha=1}^{\infty} \frac{1}{n_{\alpha}!} \left( \frac{Vz_{\alpha}}{\Lambda_{\alpha}^{3}} \right)^{n_{\alpha}}$$
- This is the [[Advanced statistical mechanics#The ideal gas in the canonical ensemble|partition function for the ideal gas]], with some characteristic length scale $\Lambda_{\alpha}$
- The _internal degrees of freedom_ are represented by $z_{\alpha}$

- Working out free energy and chemical potential:
$$\displaylines{F=-k_{B}T\ln Z \\ \mu_{a}= \frac{k_{B}T}{\alpha}\ln \frac{n_{\alpha}\Lambda_{\alpha}^{3}}{V} + \frac{f_{\alpha}}{\alpha}}$$

- For a _spherical micelle_ of radius $R$ from molecules of volume $v$:
$$\displaylines{\alpha^{*}= \frac{4\pi}{3} \frac{R^{3}}{v} \\ \mu_{\alpha}= \frac{k_{B}T}{\alpha}\ln\left( \frac{c_{\alpha}}{\alpha} \right)+
\epsilon_{\alpha}=k_{B}T\ln c_{1}+\epsilon_{1}}$$
- Here, $c_{1}$ and $\epsilon_{1}$ characterise a system of _monomers_

- The concentration then evolves as:
$$c_{\alpha}=\alpha^{*} \left[ c_{1}\exp\left( \frac{\epsilon_{1}-\epsilon_{\alpha^{*}}}{k_{B}T} \right) \right]^{\alpha^{*}}$$
- If $\epsilon_{\alpha}>\epsilon_{1}$, then there is _no micelle formation_

## Micellar shape
- For a _spherical micelle_:
$$V_{\alpha}=\alpha v=\frac{4}{3}\pi R^{3} \hspace{1.5cm}A_{\alpha}=\alpha a_{0}=4\pi R^{2}$$
- The _packing parameter_

- For a _cylindrical micelle_:

![[Micellar shapes.png]]

## Polymer filament self-assembly
- Consider _linear polymerisation_:
$$\ce{ m + X_{n} <=> X_{n+1}   }$$
- For all values of $n$, the _equilibrium constant_ is $K$

- From this:
$$\displaylines{c_{i}=K^{-1}(Kc_{1})^{i} \\ c_\text{tot}=\sum_{i=1}^{\infty} ic_{i}=\frac{c_{1}}{(1-Kc_{1})^{2}}}$$

# Self-assembled structures

## Membranes and lipid bilayers
- One of the most common self-assembled structures is the _lipid membrane_
- It acts as a _barrier_ surrounding a cell
- The _membrane composition_ controls its properties

- A _lipid bilayer_ is made of _amphiphilic molecules_
- There is a _hydrophilic head group_, and a _hydrophobic tail_
	- The head group is usually _polar_ due to _charged atoms_
	- There is typically a _range_ of head groups, tail length, shape, and chemical composition

- They form due to the _entropic hydrophobic force_ in water
### Membrane shape
- Lipid bilayers can have _phases_ dependeing on water content
	- Shapes with increasing water content:
	- _Hexagonal_: low water content $(\sim 1\%)$
	- _Layer, cubic_: medium water content
	- _Vesicles_: high water content $(\sim 99\%)$
![[Lipid bilayer shapes.png]]

- The _geometry_ of amphiphillic molecules:
	- _Effective_ area $a_{0}$ given by _head group interactions_
	- _Length_ of the hydrophobic tail $l_{c}$
	- _Volume_ of the lipid $v$

- _Shapes_:
	- Cone
	- Truncated (inverted) cone
	- Cylindrical

### Forces
- The can be _attractive forces_ at an interface
	- Hydrophobic effect, leads to _tight packing_
- The hydrophobic effect also leads to _interfacial energy_:
	- $a$ is the effective head group area
	- $\gamma$ is the _surface tension_
$$E \sim \gamma a$$
- The head groups can also lead to _electrostatic repulsion_
- _Size_ of the head groups also give _steric effects_ $\sim a^{-1}$

- The _phenomenological model_ of interfacial energy:
$$\varepsilon=\gamma a+\frac{K}{a}$$
- The _minimum_ is at:
$$a_{0}=\sqrt{ \frac{K}{\gamma} }$$