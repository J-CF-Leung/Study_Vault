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
$$\sigma(t)=\int_{0}^{t} \, d\sigma(t')=\int G(t-t') \, d\epsilon(t')=\int G(t-t') \frac{d\epsilon(t')}{dt'}\, dt' $$
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
- The model _does not exhibit stress relaxation_
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
	- In the case of [[#Stokes drag force on a sphere|Stokes flow]], $\gamma=6\pi \eta r$

- For _random motion_, as there is _no preferred direction_:
$$\langle \boldsymbol{\xi}(t) \rangle=0 $$
- As the motion is _uncorrelated_ at different times (_relaxation times_ are practically instantaneous):
$$\langle \boldsymbol{\xi}(t)\cdot \boldsymbol{\xi}(t') \rangle=G\delta (t-t') $$
- The [[Advanced statistical mechanics#Formal solution and fluctuation-dissipation theorem|formal solution]] to the Langevin equation:
$$\displaylines{\boldsymbol{v}=\boldsymbol{v}_{0}\exp\left( -\frac{\gamma}{m}t \right)+ \int _{0}^{t} \frac{\boldsymbol{\xi}(t')}{m}\exp\left[ -\frac{\gamma}{m}(t-t') \right] \, dt'  \\ \langle \boldsymbol{v}(t) \rangle=\boldsymbol{v}_{0}\exp\left( -\frac{\gamma}{m}t \right) }$$
- One can also derive:
$$\langle v^{2}(t) \rangle=v_{0}^{2}\exp\left( -\frac{2\gamma}{m}t \right)+\frac{c}{2m\gamma}\left[ 1-\exp\left( -\frac{2\gamma}{m}t \right) \right] $$

### Overdamped limit
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
	- The [[Advanced statistical mechanics#Fokker-Planck from random walks|Fokker-Planck equation]]
	- In the context of diffusion, it is also known as the _Smoluchowski equation_
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

- A _homopolymer_ has $N$ _identical monomers_
- The _degree of polymerisation_ is defined as $N$
- The _molar mass_ of the polymer is:
$$M=NM_\text{mono}$$

- A sample often has a _molar mass distribution_ $n(M)$
- The _number average_ and _mass average_:
$$\displaylines{\langle M \rangle_{n}=\frac{ \int Mn(M) \, dM}{\int n(M) \, dM } \hspace{1.5cm}\langle M \rangle_{w}=\frac{ \int M^{2}n(M) \, dM}{\int Mn(M) \, dM } \\\langle M \rangle_{n}\leq \langle M \rangle_{w}  }$$
- The equality is only satisfied when the polymer is _monodispersed_
- Otherwise, it is _poly-dispersed_
## Ideal, non-interacting chains
- Ideal chains _have no volume_, and monomers _do not interact with other monomers_
### The freely jointed chain
- Let the chain have $N$ _monomers_
- Let the _length_ of a monomer (lattice cell size) be $b$

- Consider the _end-to-end displacement_ $\boldsymbol{R}$
- On _average_, as the walk is _completely random_:
	- Average: _ensemble average_
$$\left<\boldsymbol{R}\right>=0$$
- Let the vector for the $i-$th step be $\boldsymbol{U}_{i}$
- As they are _random_, they are _uncorrelated_
$$\boldsymbol{R}=\sum_{i=1}^{N}\boldsymbol{U}_{i}\hspace{1.5cm}\left<\boldsymbol{U}_{i}\cdot \boldsymbol{U}_{j}\right>=b^{2}\delta_{ij}$$
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

### Freely rotating chain
- Let monomers have a _fixed step size_ $b_{0}$, but also be able to _freely rotate_ around some _axis_
- The axis is _fixed_ as there is a characteristic _bond angle_ $\theta$
- The average end-to-end distance:
$$\left<R^{2}\right>=\sum_{i=1}^{N}|\boldsymbol{U}_{i}|^{2}+2\sum_{i=1}^{N}\sum_{j=i+1}^{N}\left<\boldsymbol{U}_{i}\cdot \boldsymbol{U}_{j}\right>$$
- To consider the second term, _project_ $\boldsymbol{U}_{i}$ along $\boldsymbol{U}_{i+1}$:
$$\boldsymbol{U}_{i}=\frac{\boldsymbol{U}_{i}\cdot \boldsymbol{U}_{i+1}}{b_{0}^{2}}\boldsymbol{U}_{i+1}+\boldsymbol{U}_{i,\perp}=\cos\theta \boldsymbol{U}_{i+1}+\boldsymbol{U}_{i,\perp}$$
- Then consider the _correlation_ to a monomer _two links away_:
$$\left<\boldsymbol{U}_{i}\cdot \boldsymbol{U}_{i+2}\right>=\cos\theta \left<\boldsymbol{U}_{i+1}\cdot \boldsymbol{U}_{i+2}\right>+\left<\boldsymbol{U}_{i,\perp}\cdot \boldsymbol{U}_{i+2}\right>=b^{2}_{0}\cos^{2}\theta$$
- The second term _vanishes_ due to free rotation of the second link w.r.t. $i$
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
$$\int  \, d^{3}\boldsymbol{r}_{1}\exp[-\alpha|\boldsymbol{r}_{0}-\boldsymbol{r}_{1}|^{2}-\alpha|\boldsymbol{r}_{1}-\boldsymbol{r}_{2}|^{2}]=\sqrt{ \frac{\pi}{2\alpha} }\exp\left( -\frac{\alpha}{2}|\boldsymbol{r}_{0}-\boldsymbol{r}_{2}|^{2} \right) $$
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
$$G(\boldsymbol{r}_{m}-\boldsymbol{r}_{n},m-n)=\left[ \frac{3}{2\pi|m-n|b^{2}} \right]^{3/2}\exp\left[ -\frac{3}{2} \frac{|\boldsymbol{r}_{m}-\boldsymbol{r}_{n}|^{2}}{|m-n|b^{2}} \right]$$
- It is the _probability density_ for $\boldsymbol{r}_{n}$ for a _given_ $\boldsymbol{r}_{m}$
- As expected, it _convolves_, indicating the _joining_ of two chains
$$\int G(\boldsymbol{r}_{m}-\boldsymbol{r}_{k},m-k)G(\boldsymbol{r}_{k}-\boldsymbol{r}_{n},k-n) \, d^{3}\boldsymbol{r}_{k}=G(\boldsymbol{r}_{m}-\boldsymbol{r}_{n},m-n) $$

- The form of $G$ is _identical_ to the solution to a _diffusion equation_
	- The _random walk_ of a polymer can be modelled as _diffusion_, with $n$ acting as _time_ and $b^{2}/6$ as the _effective diffusion constant_
$$\left( \partial_{n}-\frac{b_{0}^{2}}{6}\nabla^{2} \right)G(\boldsymbol{r}_{m}-\boldsymbol{r}_{n},m-n)=\delta(\boldsymbol{r}_{m}-\boldsymbol{r}_{n})\delta_{mn}$$
### Worm-like chain and persistence length

#### Persistence length
- Let the polymer of _fixed length_ $l$ be described by some _curve_, with some _tangent angle_ $\theta$ at each point
- The chain is said to retain _memory_ of how it bent before, up to a significant _persistence length_, defined as the _mean value_ of $\boldsymbol{R}$ over the _first segment_
	- From later analysis, it is _half_ the Kuhn length
$$l_{p}\equiv \left\langle  \boldsymbol{R}\cdot \frac{\boldsymbol{u}_{0}}{b_{0}} \right\rangle =b_{0}\sum(\cos\theta)^{i}=\frac{b_{0}}{1-\cos\theta}\approx \frac{2b_{0}}{\theta^{2}}$$
- The _correlation_ between different segments $s_{1}$ and $s_{2}$ is then:
$$\displaylines{(\cos\theta)^{m}\approx \left( 1-\frac{\theta^{2}}{2} \right)^{m}\approx \exp\left( -\frac{m\theta^{2}}{2} \right)\approx \exp\left( -\frac{mb_{0}}{l_{p}} \right) \\ \langle \boldsymbol{t}(s_{1})\cdot \boldsymbol{t}(s_{2}) \rangle\approx \exp\left( -\frac{|s_{1}-s_{2}|}{l_{p}} \right) }$$
#### Energy of the worm-like chain
- Account for the _stiffness_ of joints, for some _small bending_
- Label points on the chain by $s$, with a _quadratic potential_ to penalise _bending_:
$$U=\frac{C_{B}}{2}\int _{0}^{l}[\partial_{s}\theta(s)]^{2} \, ds $$
- $C_{B}$ quantifies _rigidity_ of the polymer
- Suitable for modelling polymers where the _bending length scale_ is on the order of the _chain size_ (e.g. DNA)

- The _equipartition theorem_ yields:
	- For a _short polymer_ so the approximation of $d\theta/ds \sim \theta/b_{0}$ applies
$$\left<\left( \frac{d\theta}{ds} \right)^{2}\right>=\frac{2k_{B}T}{C_{B}b_{0}}$$
- The _persistence length_ is the _characteristic length scale_ of the system, dependent on _temperature_:
$$l_{p}=\frac{C_{B}}{k_{B}T}$$

#### Relating to Kuhn length
- The _end-to-end distance_, introducing $s$ as the _contour length_:
$$\begin{align}
\left<R^{2}\right>&=\left<\int_{0}^{l}  \, \frac{d\boldsymbol{r}}{ds}ds\cdot \int _{0}^{l} \frac{d\boldsymbol{r}}{ds'} \, ds'\right> =\int _{0}^{l} \, ds \int _{0}^{l} \, ds' \langle \boldsymbol{t}(s)\cdot \boldsymbol{t}(s') \rangle  \\   &=\int _{0}^{l} \, ds \int _{0}^{l} \, ds' \exp\left( -\frac{|s-s'|}{l_{p}} \right) 
\end{align}$$
- By letting $s>s'$, with the _limit_ of the second integral changed:
$$\langle R^{2} \rangle = 2\int _{0}^{l} \, ds \int _{0}^{s} \, ds' \exp\left( -\frac{s-s'}{l_{p}} \right)   $$
- With the _total contour length_ $L$:
$$\langle R^{2} \rangle =2l_{p}^{2}\left[ \exp\left( -\frac{L}{l_{p}} \right)-1+\frac{L}{l_{p}} \right] $$
- For $L\gg l_{p}$
$$\langle R^{2} \rangle =2l_{p}L  $$
- The _effective Kuhn length_ is $2l_{p}$
	- Effective _number of segments_ is $L/2l_{p}$
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

- Entropy is _higher_ for _lower_ $R^{2}$ as it is _more likely_ for the chain to be more coiled up

### Lattice random walk
- For a polymer on a _1D lattice_, let it undergo _steps_ to the left and right, with $N_{-}$ and $N_{+}$ steps respectively
- The _length_ $x$ is given by $(N_{+}-N_{-})b_{0}=\Delta Nb_{0}$

- The entropy is:
$$S=k_{B}\ln W=k_{B}\ln \begin{pmatrix}N\\N_{+}\end{pmatrix}\approx N\ln 2-\frac{(\Delta N)^{2}}{2N}$$
- This gives the probability:
$$P \propto \exp\left[ -\frac{(\Delta N)^{2}}{2N} \right]\propto \exp\left[ -\frac{x^{2}}{2Nb_{0}^{2}} \right]$$
- In 3D, this recreates the formula from the [[#Bead-spring model|partition function]]
## Polymer interactions
- _interactions_ of the chain with _itself_

- For a random walk, it may _self-intersect_
- As lattice sites can only be singly occupied, this leads to a _repulsive_ effect

- The polymer can be modelled as being in a _solvent_
- A _repulsion_ from itself can be considered as being _attractive_ to the solvent
### Excluded volume interaction and swelling
- Polymers _cannot self intersect_
- This is the _excluded volume interaction_
- It is an _entropic effect_ as there are _fewer sites available_

#### Scaling
- The repulsion term goes like $V\Phi^{2} \propto N^{2}/V$
	- Typically _stronger_ when there is a smaller [[#Semi-flexible polymers|persistence length]]
- The free energy:
$$\frac{F}{k_{B}T}\sim \nu \frac{N^{2}}{V}+\frac{R^{2}}{Nb_{0}^{2}}\sim \nu \frac{N^{2}}{R^{3}}+ \frac{R^{2}}{Nb_{0}^{2}}$$
- Finding the _minimum_:
$$R^{5} \sim \nu b_{0}^{2}N^{3}$$
- For an excluded volume interaction, $\nu\sim b_{0}^{3}$, giving:
$$R \sim b_{0}N^{3/5}$$
- This gives the scaling relation for the _swollen chain_

#### Reduction in entropy
- The _excluded volume effect_ will lead to a _decrease in number of available configurations_

- Let there be a _lattice_ where each cell has the volume of a solute, $v$
	- With _no excluded volume_, number of states $W_\text{id}=(V/v)^{N}/N!$
	- With excluded volume, $W_\text{ex}=\pmatrix{V/v \\ N}$ 
- Then comparing $S_\text{id}$ and $S_\text{ex}$:
$$S_\text{ex}-S_\text{id}=-k_{B} \frac{N^{2}v}{V}$$
- This then leads to the expression seen in the previous section

### Coil-to-globule transition
- The _swollen chain_ occurs when the _excluded volume parameter_ $v>0$
- For an _attractive potential_ $\Phi_{ij}$, the total attractive energy is:
	- $n(\boldsymbol{r})$ is the _local density_
$$U=\frac{1}{2}\int  \, d^{3}r\,d^{3}r'\,n(\boldsymbol{r})n(\boldsymbol{r}')\Phi(\boldsymbol{r}-\boldsymbol{r}') $$
- Within a _mean field_ theory, $n\approx N/R^{3}$
$$U=\frac{1}{2}\left( \frac{N}{R^{3}} \right)^{2}\int  \, d^{3}(\boldsymbol{r}-\boldsymbol{r}')\,d^{3}\boldsymbol{r}\,\Phi(\boldsymbol{r}-\boldsymbol{r'})=-Van^{2} $$
- $a$ is a _parameter_ determining the strength of the interaction

- Also including the _excluded volume_ interaction:
$$\displaylines{\frac{F_\text{int}}{V}=k_{B}Tv(T)n^{2} \\ v(T)=v_{0}-\frac{a}{k_{B}T}}$$
- Introduce the _Flory parameter_:
$$\displaylines{\chi(T)=\frac{1}{2}\left( 1- \frac{v(T)}{v_{0}} \right) \\ \frac{F_\text{int}}{V}=k_{B}Tv_{0}(1-2\chi(T))n^{2}}$$

- At some _temperature_ $\theta=a/(v_{0}k_{B})$, the excluded volume interaction is _cancelled out_, and _ideal scaling_ $R\sim \sqrt{ N }$ is regained
- Both $v_{0}$ and $a$ can be temperature-dependent, but often
$$\chi\sim T^{-1}$$

- For a _high temperature_ $(\chi<1/2)$, the polymer is _swollen_ and is said to be in a _good solvent_, with $R \sim N^{3/5}$
- For a _low temperature_ $(\chi>1/2)$, the polymer is _collapsed_ into a _globule_, and is said to be in a _bad solvent_
- As the polymer _collapses together_, $V\sim N$, hence $R\sim N^{1/3}$

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

- The _free energy per lattice site upon mixing_ is then:
	- Effectively the same as the formula for [[Advanced statistical mechanics#The binary mixture|binary mixtures]] but accounting for _polymerisation_
$$f_\text{mix}=\frac{F}{M}=k_{B}T\left[ \frac{\Phi}{N}\ln \Phi+(1-\Phi)\ln(1-\Phi)+\chi \Phi (1-\Phi) \right]$$
- For _small_ $\Phi$:
$$f\approx k_{B}T\left[ \frac{\Phi}{N}\ln \Phi+(\chi-1)\Phi+\frac{1}{2}\Phi^{2}(1-2\chi)+\frac{\Phi^{3}}{6} \right]$$
- The second term acts as a [[Advanced statistical mechanics#Virial expansion|second virial coefficient]]
- The last term ensures _stability_

### Variation of Flory parameter
- Typically, the Flory parameter _increases with temperature_
$$\chi\sim T^{-1}$$
- At high temperature, there tends to be a _coil in solution_
	- The _high entropy case_
- The _coil to globule transition_ happens for a _decreasing temperature_

- There are _temperature-responsive poiymers_, with _sharp coil-to-globule transitions_ at _high temperatures_

### Osmotic pressure and chemical potential
- The free energy above is _per lattice site_, with _volume fraction_ $\Phi=N_{A}/M$
	- $M$: _number of_ lattice sites
- The _osmotic pressure_, from changing the _volume of the system_:
	- The $N_{A}$ constraint makes $M(\partial/\partial M)=-\Phi(\partial/\partial \Phi)$
$$\Pi=- \frac{\partial F}{\partial V}\Bigg|_{N_{A}}=-\frac{1}{b_{0}^{3}} \frac{\partial(Mf)}{\partial M}=-\frac{1}{b_{0}^{3}}\left( f+M\frac{\partial f}{\partial M} \right)=-\frac{1}{b_{0}^{3}}\left( f-\Phi \frac{\partial f}{\partial \Phi} \right)$$
- Using the _polynomial expansion_ of $f$:
$$\Pi=\frac{k_{B}T}{b_{0}^{3}}\left[ \frac{\Phi}{N}+ \frac{1}{2}(1-2\chi)\Phi^{2} \right]$$

- The _chemical potential_ is given by:
$$\mu=\frac{\partial F}{\partial N_{A}}=M\frac{\partial f}{\partial(M\Phi)}=\frac{\partial f}{\partial \Phi}$$
- The osmotic pressure can then be written as:
$$\Pi=-\frac{f-\Phi \mu}{b_{0}^{3}}$$
### Virial expansion
- In $\Pi$, the first term obeys the _ideal gas law_, while the latter term is the _second term_ of the [[Advanced statistical mechanics#Virial equation of state|virial expansion]]
$$B_{2}=\frac{1}{2}(1-2\chi)$$

- When $\chi=1/2$, the chain has _ideal behaviour_
- The _excluded volume parameter_ can also be written as:
$$v(T)=b_{0}^{3}(1-2\chi)$$
- This resembles the parameter when considering [[#Coil-to-globule transition|polymer interactions]]
- If $1-2\chi<0$, there is an _attractive force_, and there is a _coil to globule transition_, and:
$$R \sim N^{1/3}$$
- If $1-2\chi=0$ (the $\theta$ point), it is an _ideal chain_:
$$R \sim N^{1/2}$$
- If $1-2\chi>0$, there is a _swollen chain_ (the chain tends to be attracted to the _solvent_)
$$R \sim N^{3/5}$$

### Polymer melt
- Let the _solvent_ be another polymer of _identical polymer_, with different _degree of polymerisation_
- This _reduces_ the _translational entropy of the solvent_:
$$\displaylines{\Delta S=k_{B}M\left[ \frac{\Phi}{N}\ln \Phi+\frac{1-\Phi}{N_{2}}\ln(1-\Phi) \right] \\ f\approx k_{B}T\left[ \frac{\Phi}{N}\ln \Phi+\frac{1}{2}\Phi^{2}\left( \frac{1}{N_{2}}-2\chi \right)+\frac{\Phi^{3}}{6} \right] \\ v=b_{0}^{3}\left( \frac{1}{N_{2}}-2\chi \right)}$$
- As they are the _same polymer_, $\chi=0$

- There is simply an _extra entropic term_ $v=b_{0}^{3}/N_{2}$, which _vanishes_ in the limit of a _long chain solvent_ $(N_{2}\gg 0)$

- The $\theta$ point is then _always reached for long-chain polymer melts_
- As there is _no relative interaction_ between chain and "solvent", the excluded volume interaction is "screened"
	- The polymer _cannot distinguish_ between contacts with _itself_ and contacts with _surrounding chains_

### Semi-dilute solutions
- For _low-concentration_ solutions, chains typically _do not overlap_
	- They have an _effective radius_ which is _smaller_ than average distance between chains
- At some concentration $c^{*}$, there is an _onset_ where chains start to _overlap_
- This is a _semi-dilute solution_
![[Polymer overlap.png]]
- At the onset of _overlap_, the _overall concentration_ is roughly equal to _concentration of segments in a single polymer_ (in a good solvent):
$$\Phi^{*}\sim \frac{Nb_{0}^{3}}{(\sqrt{ R^{2} })^{3}}\sim N^{-4/5}$$
### Phase diagram for polymers
- Flory-Huggins free energy:
$$f=\frac{F}{M}=k_{B}T\left[ \frac{\Phi}{N}\ln \Phi+(1-\Phi)\ln(1-\Phi)+\chi \Phi (1-\Phi) \right]$$
- Investigate its _stability_ w.r.t. _phase separation_ into phases $\Phi'=\Phi+\delta \Phi$ and $\Phi''=\Phi-\delta \Phi$
- Let both phases occupy _half_ of the lattice:
$$\Delta F=M\left[ \frac{f(\Phi+\delta \Phi,\chi)+f(\Phi-\delta \Phi ,\chi)}{2}-f(\Phi,\chi) \right]$$
- For some small change $\delta \Phi$, this yields:
$$\Delta F=\frac{M}{2} \frac{\partial^{2}f(\Phi,\chi)}{\partial \Phi^{2}}\delta \Phi^{2}$$
- For a _homogeneous solution_ to be _stable_, $\partial_{\Phi}^{2}f>0$

- The _spinodal curve_ separates regions of _stability_, with the curve defined by:
$$\frac{\partial^{2}f}{\partial \Phi^{2}}=0\implies \chi^{*}(\Phi)=\frac{1}{2}\left( \frac{1}{N\Phi}+\frac{1}{1-\Phi} \right)$$
- For $\chi>\chi^{*}$, the solution is _unstable_, and the polymer _phase separates_
	- It is a _bad solvent_ at that concentration
	- Corresponds to _low temperature_

- The spinodal has a _minimum_ in the $(\Phi,\chi)$ plane where _instability first emerges_ with increasing $\chi$
- By minimising $\chi^{*}(\Phi)$:
$$\Phi_{c}=\frac{1}{\sqrt{ N }+1}\hspace{1.5cm}\chi_{c}=\frac{1}{2}+\frac{1}{\sqrt{ N }}+\frac{1}{2N}\approx \frac{1}{2}+\frac{1}{\sqrt{ N }}$$
- $T_{c}$ is the corresponding _critical temperature_
- Depending on the _sign_ of the [[#Coil-to-globule transition|interaction parameter]], either _high_ or _low_ temperatures can be stable
	- For most polymers, _high temperatures_ yield stable homogeneous solutions

## Polymer applications
- Polymers can be _adsorbed_ onto surfaces
	- A _temperature-dependent_ process

### Brushes
- Let a surface be _grafted_ with polymers a spacing $D$ apart
- The _grafting density_ is $\sigma=1/D^{2}$

- The _mushroom_ regime has $D\gg R$, and they _barely interact_
- If $D\sim R$, they start to _overlap_ and act roughly as in a _solution_, $D\sim R\sim b_{0}N^{3/5}$

- For $D\ll R$, the chains interact, and are _stretched_, making a polymer _brush_
- Let it be of height $h$
- The [[#Entropy of the ideal chain|entropic]] part of the free energy scales as $h^{2}/(Nb_{0})$
	- Due to _stretching_ of the polymer
- From [[#Excluded volume interaction and swelling|excluded volume]], free energy scales as $b_{0}^{3}N^{2}/V=b_{0}^{3}N^{2}\sigma/h$
- The _total free energy_:
$$\displaylines{F=k_{B}T \frac{h^{2}}{b_{0}N}+k_{B}T \frac{b_{0}^{3}N^{2}\sigma}{h} \\ \frac{\partial F}{\partial h}=0 \implies \langle h \rangle  \sim (b_{0}^{5}\sigma)^{1/3}N}$$
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
$$\gamma\frac{d\boldsymbol{R}_{n}}{dt}=\kappa(\boldsymbol{R}_{n+1}+\boldsymbol{R}_{n-1}-2\boldsymbol{R}_{n})+\boldsymbol{\xi}(n,t)$$
- $\kappa=3k_{B}T/b_{0}^{2}$ is the [[#Bead-spring model|spring constant]] of the Gaussian chain
- Random noise, from the [[#Langevin equation|fluctuation-dissipation theorem]]:
$$\langle \xi_{i}(n,t)\xi_{j}(m,t') \rangle =2\gamma k_{B}T\delta_{mn}\delta(t-t')\delta_{ij} $$
- Applicable for _low Reynolds numbers_
- Ignores _hydrodynamics_, or _solvent interactions_
- Works for _dense polymer solutions_

- In the _continuum limit_, the _Rouse equation_ gives:
$$\gamma\frac{ d\boldsymbol{R}_{n}}{dt}=\kappa \frac{\partial^{2}\boldsymbol{R}}{\partial n^{2}}+\boldsymbol{\xi}(n,t)$$

### Motion of normal modes
- _Fourier transform_ into _modes_:
$$\displaylines{\boldsymbol{R}_{n}=\boldsymbol{X}_{0}(t)+2\sum_{p=1}^{\infty}\boldsymbol{X}_{p}(t)\cos\left( \frac{p\pi n}{N} \right) \\ \boldsymbol{X}_{p}(t)=\frac{1}{N}\int_{0}^{N} \boldsymbol{R}(n,t)\cos\left( \frac{p\pi n}{N} \right) \, dn }$$
- Only _cosine modes_, due to the boundary conditions:
$$\frac{\partial R}{\partial n}\Bigg|_{n=0}=\frac{\partial R}{\partial n}\Bigg|_{n=N}=0$$

- The _cnetre of mass_ undergoes _diffusion_:
$$N\gamma \frac{dX_{0}}{dt}=\boldsymbol{\xi}_{0}(t)$$
- The effective _diffusion constant_ is
$$D_\text{eff}=\frac{k_{B}T}{\gamma N}$$

- The equation of motion for each mode $p\geq 1$:
$$\displaylines{2N\gamma \frac{d\boldsymbol{X}_{p}}{dt}=-k_{p}\boldsymbol{X}_{p}+\boldsymbol{\xi}_{p}(t) \\ k_{p}=\frac{6k_{B}T\pi^{2}p^{2}}{Nb_{0}^{2}}}$$

- Define a _relaxation time_ for each mode, which is _shorter_ for _higher modes_
$$\tau_{p}=\frac{N\gamma}{k_{p}}=\frac{\gamma N^{2}b_{0}^{2}}{6\pi^{2}k_{B}T} \frac{1}{p^{2}}$$
- The _slowest relaxation time_ is the _Rouse time_ $\tau_{1}$
- It is time for relaxation of the _overall shape_ of the molecule

- The _correlation_ between mode amplitudes:
$$\left<X_{q}^{i}(t)X_{q'}^{j}(t)\right>= \frac{k_{B}T}{k_{p}} \delta_{qq'} \delta_{ij} \exp\left[ - \frac{|t-t'|}{\tau_{p}} \right]$$

### Viscoelastic behaviour
- Compute the _stress tensor_ to get viscoelastic behaviour
- Consider a _cube_ of polymer with length $L$, with _concentration_ $c=\Phi/b_{0}^{3}$ of segments

- For _sub-chains_ of length $\tilde{N}$, there are $(c/\tilde{N})L^{3}$ within the cube
- The _probability_ that the end-to-end vector $\boldsymbol{R}$ _cuts_ the $j-$plane in the cube is $R_{j}/L$
- The $i-$component of _force_ transmitted by the chain across the plane is $F_{i}=\kappa R_{i}/\tilde{N}$
- Combining the above:
$$\sigma_{ij}=\frac{3k_{B}Tc}{\tilde{N}^{2}b_{0}^{2}}\langle R_{i}R_{j} \rangle = \frac{3k_{B}Tc}{b_{0}^{2}} \left\langle  \frac{\partial R_{i}}{\partial n} \frac{\partial R_{j}}{\partial n}  \right\rangle  $$
- From the Rouse model:
$$\sigma_{ij}=\frac{c}{N}\sum_{p}k_{p}\langle X_{p}^{i}X_{p}^{j} \rangle $$
- Apply a _shear strain_ such that:
$$X_{p}^{x}(t)=X_{p}^{x}(0)+\epsilon X_{p}^{y}(0)$$
- The stress component $\sigma_{xy}$ is then:
$$\sigma_{xy}=\frac{\epsilon c}{N}\sum_{p}k_{p} \left<X_{p}^{x}(t)X_{p}^{y}(0)\right> \sim \frac{\epsilon c}{N} \sum_{p} k_{p}T \exp\left( -\frac{t}{\tau_{p}} \right)=G(t)\epsilon$$

- The shear modulus can be written as:
$$G(t)=c \frac{k_{B}T}{N} \sum_{p} \exp\left( -\frac{p^{2}t}{\tau_{1}} \right)$$
- Each _un-relaxed_ mode then contributes $ck_{B}T$ to the modulus, behaving like a Maxwell fluid

- For _long timescales_, it behaves as a [[#Maxwell fluid]]
$$G(t)\approx c \frac{k_{B}T}{N} \exp\left( -\frac{t}{\tau_{1}} \right)$$
- For _short timescales_:
$$G \sim \int \exp\left( -\frac{p^{2}t}{\tau_{1}} \right) \, dp\sim \sqrt{ \frac{\tau_{1}}{t} } $$
## Helix to coil transition
- Many polymers can undergo a transition from a _disordered globule_ to an _ordered helical state_
	- Driving force includes _hydrogen bonding_
- Model it as a _two-state system_, where each _segment_ can be in either the helical or coil state
- There may be varying degrees of _cooperativity_, as each segment has a different _tendency_ to be in a given state _depending on the state of its neighbours_

- Let the helical state have some _energy_ $-\epsilon$

### Non-cooperative model
- Each segment as a _two-state system_:
$$Z_{1}=1+\exp(-\beta\epsilon)$$
- For a polymer of $N$ segments:
$$Z=z_{1}^{N}$$
- The _proportion of the chain in a helical state_:
$$f_\text{helix}=\frac{\langle i \rangle}{N}=-\frac{1}{N} \frac{\partial \ln Z}{\partial\beta}=\frac{s}{1+s} \hspace{1cm}s\equiv \exp(-\beta\epsilon) $$
- It is a _gradual transition_ with temperature

### Fully cooperative model
- Alternatively, consider an _on-off model_:
$$Z=1+ \exp(-\beta N\epsilon) \implies f_\text{helix}= \frac{\exp(-\beta N\epsilon)}{1+ \exp(-\beta N\epsilon)}$$
- This gives a much _sharper_ transition for large $N$

### Zimm-Bragg model
- The _nearest neighbour_ interactions are parametrised with $\sigma$
- Statistical weights of each case:
	- Coil $(C)$ with $C$ neighbour: $1$
	- Helix $(H)$ with $H$ neighbour: $s$
	- $H$ following $C$: $\sigma s$
	- $C$ following $H$: $1$
	- $H$ is the first unit: $\sigma s$

- The weights for the first segment can be written as a _vector_:
$$\boldsymbol{q}_{1}=\pmatrix{1\\\sigma s} \hspace{1.5cm}Z_{1}=\pmatrix{1&1}\pmatrix{1\\\sigma s}$$
- The _second segment_:
$$\boldsymbol{q}_{2}=\pmatrix{C-C&C-H\\H-C&H-H}\boldsymbol{q}_{1}=G\boldsymbol{q}_{1}$$
- $G$ is the _transfer matrix_

- For $N$ segments:
$$Z_{N}=\pmatrix{1&1}G^{N-1}\pmatrix{1\\\sigma s}$$
- The partition function is a _linear combination_ of the two _eigenvalues_ of $G$:
$$\lambda_{\pm}=\frac{1+s\pm\alpha}{2} \hspace{1.5cm}\alpha=\sqrt{ (1-s)^{2}+4\sigma s }$$
- For $N\gg 1$, the _larger eigenvalue_ will dominate:
$$Z_{N}\approx \lambda_{+}^{N-1}$$
- From this, one gets:
$$f_\text{helix}= \frac{1}{2}\left( 1+ \frac{s-1}{\sqrt{ (1-s)^{2}+4\sigma s }} \right)$$
- For $\sigma=1$, the result of the _non-cooperative model_ is regained

# Molecular self-assembly
- The formation of _structures_ from purely _inter-molecular forces_
- Molecules can assemble into _different structures_, such as _spherical/cylindrical micelles_, or _lamellae_
	- Can be quantified using _shape/packing parameters_
- Proteins (biopolymers) can self-assemble into _filaments_ and _microtubules_

## Forces
- _Hydrogen bonding_, where _dipole moments_ in molecules interact

- _Hydrophobicity_, where an _entropic force_ makes hydrophobic/phillic parts of molecules stick to each other
	- _Amphiphillic_ molecules have _hydrophilic_ and _hydrophobic_ parts

- The _hydrogen bond network_ of water molecules _around hydrophobic molecules_ will end up _decreasing_ entropy of an even solution
- This leads to the entropic force making _hydrophobic_ parts stick together
- For a _higher temperature_ solution, hydrogen bonding interactions matter _less_

- _Electrostatics_, where charged parts of molecules interact
	- From _screening_, it typically _decays exponentially_
	- The length scale is typically _short_

## Critical concentration
- Often, there is a _critical concentration_ above which the molecules will self-assemble
- _At_ the critical concentration, for a _cluster_ of size $\alpha$ made out of monomer $I$:
$$\mu_{\alpha}=\mu_{I}$$
- Let there be a solution of $N_{T}$ molecules, forming $n_{\alpha}$ _clusters_ of $\alpha$ monomers, such that there are $N_{\alpha}$ molecules used to construct those clusters:
$$N_{\alpha}=\alpha n_{\alpha}\hspace{1.5cm}\sum_{\alpha=1}^{N}N_{\alpha}=N_{T}$$
### Chemical potential of a cluster
- Assume the clusters _do not interact with each other_
	- Valid for _low concentration_
- The partition function for all clusters is then:
$$Z= \prod_{\alpha=1}^{\infty} \frac{1}{n_{\alpha}!} \left( \frac{Vz_{\alpha}}{\Lambda_{\alpha}^{3}} \right)^{n_{\alpha}}$$
- This is the [[Advanced statistical mechanics#The ideal gas in the canonical ensemble|partition function for the ideal gas]], with some characteristic length scale $\Lambda_{\alpha}$
- The _internal degrees of freedom_ are represented by $z_{\alpha}$

- Working out free energy and chemical potential:
$$\displaylines{F=-k_{B}T\ln Z \\ \mu_{a}= \frac{k_{B}T}{\alpha}\ln \frac{n_{\alpha}\Lambda_{\alpha}^{3}}{V} + \frac{f_{\alpha}}{\alpha}}$$
- $f_{\alpha}$ is the _internal free energy per monomer_ belonging to an aggregate of size $\alpha$

- Write in terms of the _mass concentration_:
$$c_{\alpha}=\frac{N_{\alpha}}{V}=\frac{n_{\alpha}\alpha}{V}$$
- Then write the chemical potential as:
	- $\epsilon_{\alpha}=f_{\alpha}/\alpha+(k_{B}T/\alpha)\ln(\Lambda_{\alpha}^{3})$
$$\mu_{\alpha}=\frac{k_{B}T}{\alpha}\ln\left( \frac{c_{\alpha}}{\alpha} \right)+\epsilon_{\alpha}$$

### Cluster formation
- Equilibrium:
$$\frac{k_{B}T}{\alpha}\ln\left( \frac{c_{\alpha}}{\alpha} \right)+\epsilon_{\alpha}=k_{B}T\ln c_{1}+\epsilon_{1}$$
- Here, $c_{1}$ and $\epsilon_{1}$ characterise a system of _monomers_

- The concentration then evolves as:
$$c_{\alpha}=\alpha \left[ c_{1}\exp\left( \frac{\epsilon_{1}-\epsilon_{\alpha}}{k_{B}T} \right) \right]^{\alpha}$$
- If $\epsilon_{\alpha}>\epsilon_{1}$, then there is _no micelle formation_
- If $\epsilon_{\alpha}<\epsilon_{1}$, then _most monomers_ will form into a _micelle_

- There is often an _optimum number_ $\alpha^{*}$ for the size of a micelle
$$c_{\alpha^{*}}=\alpha^{*}\left[ c_{1}\exp\left( -\frac{\Delta\epsilon}{k_{B}T} \right) \right]^{\alpha^{*}}\hspace{1cm}\Delta\epsilon=\epsilon_{\alpha}^{*}-\epsilon_{1}$$
- If $c_{1}<\exp(\Delta\epsilon/k_{B}T)$, then _micellar concentration_ becomes very _small_
- Above the _critical micellar concentration_, most new amphiphiles are _integrated into micelles_
## Micelles
- One form of self-assembly is the organisation of _surfactant molecules_ into _micelles_

### Surfactants
- _Surfactants_ are _asymmetric molecules_ with a _hydrophobic_ and a _hydrophilic_ part
- It is an _amphiphile_
 
- The _hydrophobic_ parts tend to phase separate, while the _hydrophilic_ parts prefer to _stay in solution_
- _Microscopic_ phase separation occurs

- The hydrophilic head is typically a _charged group_, which can be _cationic, anionic, or zwitterionic_
![[Head groups.png]]
- The _hydrophobic tail_ is typically a _hydrocarbon chain_

### Micellar shape
- For a _spherical micelle_ formed from $\alpha$ surfactant molecules:
$$V_{\alpha}=\alpha v=\frac{4}{3}\pi R^{3} \hspace{1.5cm}A_{\alpha}=\alpha a_{0}=4\pi R^{2}$$
- The _packing parameter_

- For a _cylindrical micelle_:

![[Micellar shapes.png]]

## Polymer filament self-assembly
- The _polymerisation_ of _identical protein molecules_ into _filaments_
- Examples: microtubules, actin fibrils

- Consider _linear polymerisation_:
$$\ce{ m + X_{n} <=> X_{n+1}   }$$
- For all values of $n$, the _equilibrium constant_ is $K$

- Let $c_{i}$ denote the _concentration_ of a filament with $i$ monomers
- There is a _total concentration_ $c_\text{tot}$
- From this:
$$\displaylines{c_{i}=K^{-1}(Kc_{1})^{i} \\ c_\text{tot}=\sum_{i=1}^{\infty} ic_{i}=\frac{c_{1}}{(1-Kc_{1})^{2}}}$$
- For a given $c_\text{tot}$, the _free monomer concentration_ is:
$$c_{1}=\frac{1+2Kc_\text{tot}-\sqrt{ 4Kc_\text{tot}+1 }}{2K^{2}c_\text{tot}}$$

- For a _small_ $c_\text{tot}$, $c_{1}\approx c_\text{tot}$, and most proteins _remain as monomers_
- For $c_\text{tot}>K^{-1}$, the concentration of monomers is _approximately constant_, and most proteins exist as _filaments_
- $K^{-1}$ is analagous to the _critical micellar concentration_
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

### Forces, energy, and effective area
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
- This is the _optimal head group area_

- One can then write the energy as:
$$\varepsilon_{N}=2\gamma a_{0}+\frac{\gamma}{a}(a-a_{0})^{2}$$

### Shape of aggregates
- Assume the _hydrophobic tails_ remain _fluid_ and _incompressible_
	- Both the _head group_ and _tails_ will influence the shape
- Let the lipids have _optimal head group area_ $a_{0}$, with _volume_ $v$
- Let the _critical chain length_ (where the molecule is _fully extended_) be $l_{c}$

- Due to _entropy_, the system favours _smaller aggregates_

- Example: _spherical micelles_ of radius $R$
- From _area_, the _number of lipids_ $M$ is:
	- Assuming _dense packing_
$$M=\frac{4\pi R^{2}}{a_{0}}=\frac{4\pi R^{3}}{3v} \implies R=\frac{3v}{a_{0}}$$
- In order to form the micelle:
$$R\leq l_{c} \implies \frac{v}{a_{0}l_{c}}\leq \frac{1}{3}$$

- Lipids with _different_ $a_{0},l_{c},v$ will form _different aggregates_
	- The _microscopic_ effect of the lipids affecting the _macroscopic_ structure

- Consider _cylinders_:
$$\frac{1}{3}\leq \frac{v}{l_{c}a_{0}}\leq \frac{1}{2}$$
- Consider _bilayers_:
$$ \frac{v}{l_{c}a_{0}}> \frac{1}{2}$$
- Bilayers are typically _planar_ on the _length scale of the lipids_
	- Formed for a _large volume_ and _small critical length_
	- Possible to be _gently curved_ as well at an energetic cost
	- Forms if the _water-lipid ratio_ is _divergent_
![[Lipid aggregate shapes.png|650]]

- They can also _pack_ to form _crystals_
![[Micelle phase diagram.png|500]]

## Phase transitions in planar lipid bilayers
- _Phase transitions_ can occur between aggregate structures, at certain _temperatures_
- Typically from a _fluidic_ membrane, where lipids can _move around_, into _quasi-crystalline phases_, where the lipids are _frozen_
![[Bilayer phases.png|400]]

- It indicates a _loss in chain and lattice order_:
![[Loss of lipid bilayer order.png|500]]


- Typically investigated using _differential scanning calorimetry_ (DSC)
	- A _buffer solution_, with a _low concentration_ (forming bilayers), is put into a _sample cell_, compared to a _reference cell_ of only water
	- At [[Advanced statistical mechanics#Phase equilibria and transitions|phase transitions]], the _heat capacity_ experiences a _discontinuity_
	- Hence, _heat capacities_ of both cells are measured
	- As the cells are _open_, it is $\Delta C_{p}$ that is measured

![[DSC results.png|400]]
- The peaks indicate _melting temperature_ $T_{m}$, where the _phase transition_ occurs
	- Temperature rise: from _crystalline_ to _fluidic_

- From DSC results, $T_{m}$ must depend on $l_{c}$, as well as the _head group_
![[Chain length DSC.png|600]]
- For some chain lengths, there may also be _no phase transition at all_

- One can also often identify _pre-transitions_, and a _ripple phase_
![[DSC phases.png|500]]
### Thermodynamic quantities
- As the phase transition takes place at _constant pressure_, consider the _Gibbs Free Energy_
$$G=H-TS=U+pV-TS\hspace{1cm}dG=dH-T\,dS-S\,dT$$

- As there are _multiple components_:
$$dH=T\,dS+V\,dp+\sum_{j=1}^{m}\mu_{j}\,dN_{j}$$
- In _equilibrium_, assume $p,T,N_{j}$ are all _constant_
	- For DSC, heating must be _slow_
- This then gives $dH=T\,dS$

- As $dH$ is the _heat for constant pressure_, given $\Delta C_{p}(T)$:
$$\Delta H=\int _{T_{0}}^{T_{1}} \Delta C_{p}\, dT \hspace{1.5cm} \Delta S=\int _{T_{0}}^{T_{1}} \frac{\Delta C_{p}}{T}\, dT $$
- For _sharp transitions_, $\Delta C_{p}(T)$ is a _delta function_:
$$\Delta S=\frac{\Delta H}{T_{m}}$$
- $\Delta C_{p}$ can be _linked to microscopic properties_ of the bilayer

### Compressibility of the bilayer
- For a _sharp transition_, taking place at _pressure_ $p_{0}$:
$$T_{m}=\frac{\Delta H_{0}}{\Delta S}=\frac{\Delta E+p_{0}\Delta V}{\Delta S}$$
- Let there be a _change in pressure_ $\Delta p$:
$$\Delta(\Delta H)=\Delta p\,\Delta V$$
- This gives a _change in melting temperature_:
$$\frac{\Delta T_{m}}{T_{m}}=\frac{\Delta p\Delta V}{\Delta H_{0}}$$
- This can be rewritten as:
$$\Delta V=\frac{\Delta T_{m}}{T_{m}}\,\frac{\Delta H_{0}}{\Delta p}$$
- This gives a way to _experimentally measure_ $\Delta V$
- Typical value: $\Delta V \sim 1\%$ (_almost incompressible_)

## Soft membranes
- Lipid bilayers are often seen to _fluctuate_, and can be considered _soft_
- _Cells_ often have phospholipid bilayers as barriers
	- _Organelles_ also have membranes
	- _Plants_ have _cell walls_ for additional stability
	- They often contain _many types of phospholipids_

- Membrane stiffness plays roles in:
	- _Cell motion_ through membrane deformation
	- _Material transport_ as vesicles fuse with other cells
	- _Macrophages_ taking up ("eating") blood cells

- Let a soft membrane have length/width $L\gg d$, where $d$ is the _thickness_
	- $L \sim \mu \text{m}$, $d\sim \text{nm}$
- It undergoes _fluctuations_ of energy $\sim k_{B}T$
- This includes _stretching_, controlled by modulus $\sigma$, and _bending_, with modulus $\kappa$
	- Typically quite difficult to _measure directly_ (due to disruption of the membrane in said measurement)
### Membrane stretching
- Assume the membrane is a _quasi-2D liquid_, with a _vanishing shear modulus_, and _finite shear viscosity_
- Assume _bending/stretching_ is the dominant deformation, and _does not induce a phase change_ (far away from $T_{m}$)

- The lipids stay _close_ such that $a_{0}$ is _constant_
- They remain _incompressible_ ($v$ is constant)
- Thus, the stretching comes from the _tilting_ and _splaying_ of the lipids themselves
	- _Holes_ in the membrane are _not allowed_

![[Membrane curvature.png]]
- The _area_ of the membrane is $A=L^{2}$
- Let the _curvature_ along $x$ and $y$ be $c_{1}$ and $c_{2}$
- Let $h=h(x,y)$ with $h_{x}=\partial h/\partial x$

- Let there be a _point_ $P$, with neighbouring points $P_{x}$ and $P_{y}$, which are $dx$ and $dy$ away
$$\vec{PP_{x}}= \pmatrix{1\\0\\h_{x}}\,dx\hspace{1.5cm}\vec{PP_{y}}= \pmatrix{0\\1\\h_{y}}\,dy$$
- The _infinitesimal area_ (small $\Delta h$)
$$dA=\vec{PP_{x}}\times \vec{PP_{y}}=\left( 1+ \frac{1}{2}(\nabla h)^{2} \right)\,dx\,dy$$
- The _actual increase in area_:
$$dA-dx\,dy=\frac{1}{2}(\nabla h)^{2}dx\,dy$$

### Membrane bending
- The _curvature_ $H$ in 1D is defined by the reciprocal of the _radius of curvature_: 
$$H=\frac{1}{r}=\frac{f''(x)}{[1+f'(x)^{2}]^{3/2}}=\left[ \frac{f'}{\sqrt{ 1+f'^{2} }} \right]'\approx f''(x)$$
- Generalise to 2D:
	- Formally, one needs to consider _mean_ and _Gaussian_ curvature along 2 directions
	- 2 directions: normal of plane, normal of curve
$$H=\frac{1}{2}\nabla\cdot\left( \frac{\nabla h}{\sqrt{ 1+|\nabla h|^{2} }} \right)\approx \frac{1}{2}\nabla^{2}h$$
### Spectrum of deformations
- The _energy_ has contributions from _stretching_ and _bending_:
	- Characterised by $\sigma$ and $\kappa$ respectively
$$\delta E=\frac{1}{2}\sigma \int |\nabla h|^{2} \, dx\,dy+\frac{1}{2}\kappa \int (\nabla^{2}h)^{2} \, dx\,dy  $$

- Go to _Fourier space_:
$$h(x,y)=L^{2} \int  \, \frac{d^{2}q}{(2\pi)^{2}} \tilde{h}(q) \exp(i\boldsymbol{q}\cdot \boldsymbol{r}) $$
- Substitute the above into the formula for energy, and using that $h(\boldsymbol{q})=h^{*}(-\boldsymbol{q})$ 
	- $h(\boldsymbol{r})$ is _real_
$$\delta E=\frac{L^{2}}{2(2\pi)^{2}}\int  d^{2}q \,(\sigma q^{2}+\kappa q^{4})\tilde{h}(q)^{2}$$

- Use _equipartition_ for each $q$ mode
	- Each mode gets $k_{B}T/2$, as it only depends on the _modulus_ of $q$ (one DOF)
$$\langle \tilde{h} (q)^{2}\rangle = \frac{k_{B}T}{A} \frac{1}{\sigma q^{2}+\kappa q^{4}} $$
- For _large_ $q$ (small wavelength), _bending_ dominates
- For _small_ $q$, _stretching_ dominates
- One can define $q_\text{crossover}=\sqrt{ \sigma/\kappa }$

- The _minimum_ and _maximum_ $q$ are given by the _dimensions_ of the membrane:
$$q_\text{min}=\frac{2\pi}{L}\hspace{1.5cm}q_\text{max}=\frac{2\pi}{d}$$
- _Sum over_ individual modes:
$$\begin{align}
\langle h^{2} \rangle &= \frac{k_{B}T}{A} \int  2\pi q\, dq \, \frac{1}{\sigma q^{2}+\kappa q^{4}} \\ &= \frac{k_{B}T}{4\pi\sigma} \,\ln\left( \frac{q^{2}}{\sigma+\kappa q^{2}} \right)\Bigg|_{q_\text{min}}^{q_\text{max}} \\ &\xrightarrow{\sigma\to0} \frac{k_{B}T}{16\pi^{3}\kappa}A
\end{align}$$
- A _typical value_ of $\kappa$ is $20k_{B}T$, leading to a _fluctuation_ $\sqrt{ \langle h^{2} \rangle }$ of $L/100$

## Other self-assembled structures
- _Viruses_ contain an _outer coat_ of _proteins_ (the _capsid_)
- It can be _reversibly self-assembled_

- _DNA_ is also a _self-assembled_ structure from its bases

# Surface Energy
- There are _van der Waals_ interactions between _molecules of the same species_
	- They are typically _attractive_
- Interactions between molecules of _different species_ can be _unfavourable_
	- Example: _water and oil_ are _immiscible_ and form an _interface_

- The creation of an _interface_ between immiscible liquids leads to an _energy penalty_
	- When in the _bulk_, molecules have more _favourable interactions_ with surroundings
	- Hence, liquids will _minimise surface area_ if possible
	- This usually leads to _spherical droplets_

- To form an _additional surface area_ $\delta A$ gives a penalty of $\delta E$ given _surface tension_ $\gamma$
$$\delta E=\gamma\delta A$$
- $\gamma$ is determined by _the materials in contact_
	- Water-air: $72\times 10^{-3}\,\text{N/m}$
	- Water-oil: $30\times 10^{-3}\,\text{N/m}$

- Surface tension can be _reduced_ via the addition of _surfactants_, such as _amphiphilic molecules_
	- The amphiphilic molecules create a _2D film between the unlike molecules_
	- It will also naturally be quite low when there are _similar co-existing compositions_ (e.g. near phase transitions)
- It can be _measured_ by _measuring forces near moving interfaces_

- Thermodynamic variables accounting for surface energy:
$$\displaylines{dU=T\,dS-p\,dV+\sum_{i}\mu_{i}\,dN_{i}+\gamma\,dA \\ \gamma=\left( \frac{\partial U}{\partial A} \right)_{S,V,N_{i}}=\left( \frac{\partial F}{\partial A} \right)_{T,V,N_{i}}=\left( \frac{\partial G}{\partial A} \right)_{T,p,N_{i}}}$$
## Geometries

### 2D films
- Consider an applied force $f$ to change the _area_ of a 2D film
![[2D film surface tension.png]]
$$f\,dx=\gamma\,dA=\gamma L\,dx \implies \gamma=\frac{f}{L}$$
- It is a _force per unit length_

- Measurement: depends on measuring the _tension_ as a function of the _surface area_
![[Surface tension measurement.png]]
- As the _number of lipids_ increases, the surface tension increases _faster_

### Link to van der Waals interactions
- $\gamma$ can be linked to _van der Waals interactions_

- Let there be a _slab_ of liquid be _split_ with separation $h$
- The force _between the halves_:
$$f(h)=\frac{A}{6\pi h^{3}}$$
- $A$ is the [[#Dipole interactions|Hamaker constant]]
	- Typical values: $A\sim 10^{-20}\,\text{J}$
- Calculating surface energy per unit area, given $a$ as _half the average distance between molecules_
$$\gamma=\frac{1}{2}\int _{a}^{\infty} f(h) \, dh=\frac{A}{24\pi a^{2}} $$

- This operates on the assumption that the system is _static_
- However, $A$ is _frequency dependent_
	- As it is an _electromagnetic_ interaction, it is mediated by _photons_ which will _radiate_

### Bubbles and droplets
- Let a _droplet_ of radius $R$ have _pressure difference_ $\Delta p$ across the surface
![[Droplet surface.png]]
- _Work done_ by $\Delta p$ is used to expand the surface:
$$\gamma\,\Delta A=\gamma(8\pi R\Delta R)=\Delta p(4\pi R^{2}\Delta R)$$
- The pressure difference due to _surface tension_:
$$\Delta p=\frac{2\gamma}{R}$$
- It is _positive_ due to _higher internal pressure_

- In a _bubble_, there are both _inner_ and _outer surfaces_:
$$\Delta p=\frac{4\gamma}{R}$$

- For _non-spherical drops_, two radii must be taken into account:
$$\Delta p=\gamma\left( \frac{1}{R_{1}}+\frac{1}{R_{2}} \right)$$
### Capillary rise
- The _rise_ of a water column in a capillary leads to _increased pressure_ at the _meniscus_:
![[Capillary rise.png|150]]
- The additional _hydrostatic pressure_ must _balance_ the pressure from _surface tension_:
$$\rho gh=\gamma\left( \frac{1}{R_{1}}+\frac{1}{R_{2}} \right)$$
- For a _rotationally symmetrical meniscus_:
$$\gamma=\frac{\rho ghR}{2}$$
- It is valid for _uniform curvature_, for a liquid with _low viscosity_
- Assume _complete wetting_, independent of _wetting angle_

- The _capillary length_ to compare surface tension and gravitational force:
$$l_{c}=\sqrt{ \frac{\gamma}{\rho g} }$$
- For water, $l_{c}\approx 2.7\,\text{mm}$
- Droplets with $R<l_{c}$ adopt a _near-spherical shape_, which is _not influenced by gravity_
- For _small capillaries_, gravity _does not change the shape_ of the meniscus, and the formula for $\gamma$ holds

## Amphiphiles
- Amphiphiles have both _hydrophilic_ and _hydrophobic_ groups
- They are attracted to _water/oil_ or _water/air_ interfaces

- Amphiphiles can be _permanently adsorbed_ to a surface, and be _insoluble_
	- Concentration on the _surface_ can be _uncorrelated with bulk concentration_
	- There can also be _zero bulk concentration_

### Insoluble surfactants
- The surfactants are treated as _molecules_ of size $a$ _confined to a plane_ of area $A$
- The plane has _pure surface tension_ (no surfactants) $\gamma_{0}$
- The _energy gain_ by moving a surfactant _from bulk to interface_ is $u_{0}$

- The _free energy per site_ from the above, plus excluded volume, similar to the [[#Flory-Huggins free energy]]
$$f=k_{B}T(\phi \ln \phi+(1-\phi)\ln(1-\phi))+(\gamma_{0}a^{2}-u_{0}\phi)$$
- The _area fraction_ is $\phi=A_\text{surfactant}/A$
- There are a total of $A/a^{2}$ sites

- The surface tension is then:
$$\gamma=\frac{\partial F}{\partial A}=\gamma_{0}+k_{B}T\ln(1-\phi)$$

- For a _low surfactant average_, the _reduction_ in surface tension is the _ideal gas pressure of a 2D gas_
	- The dilute molecules have an _osmotic pressure_ same as that of a 2D gas
	- Can be considered a _correction_ to the ideal gas law in 2D
- The _degree of hydrophobicity_ determined $u_{0}$, which in turn has _no role_ in surface tension

### Soluble surfactants
- For _soluble_ surfactants, the _adsorbed concentration_ will be in _equilibrium_ with the _bulk concentration_
- The _Gibbs Free Energy_ for the whole system:
$$dG=V\,dP-S\,dT+\sum_{i}\mu_{i}\,dN_{i}+\gamma \,dA$$
- In _equilibrium_, $dP=dT=0$, using the [[Advanced statistical mechanics#Scaling and Gibbs-Duhem relation|Gibbs-Duhem relation]]: 
$$\sum_{i}N_{i}\,d\mu_{i}+A\,d\gamma=0$$
- Let there be 2 species (1: solvent, 2: solute)
$$-d\gamma=\frac{n_{1}}{A}d\mu_{1}+\frac{n_{2}}{A}d\mu_{2}$$
- $n_{i}/A$ are the _surface excess quantities_, and $n_{1}/A$ can be set to zero
- The bulk [[Advanced statistical mechanics#Chemical reactions|chemical potential]] in terms of concentration $c$, for a _bulk dilute solution_:
$$\mu_{2}=\mu_{0}+k_{B}T\ln c$$
- This leads to:
$$\frac{n}{A}=-\frac{1}{k_{B}T} \frac{d\gamma}{d(\ln c)}$$
- This is the _Gibbs adsorption isotherm_
- It is derived from the _balance_ of _bulk entropy_ and _surface energy_

- It holds _up to_ the [[#Critical concentration|critical micelle concentration]] (CMC)
	- Above this concentration, _monomer concentration does not increase_, which _stops reducing surface tension_
	- A way to _measure_ the CMC

![[Surface tension measurements.png|450]]

## Wetting and contact angle
- The _composition_ of a surface determines the _interactions with water_
- The _surface and its energies_ influence the _shape_ of the surface
![[Pasted image 20240427184402.png]]
- The relevant surface energies: _liquid-vapour_, _liquid-surface_, _surface-vapour_
- The _balance_ of forces gives _Young's equation_
![[Young's equation.png]]
$$\gamma_{SV}=\gamma_{SL}+\gamma_{LV}\cos\Theta$$
- One can define a _wetting parameter_:
$$S=\gamma_{SV}-(\gamma_{SL}+\gamma_{LV})$$
- For $S>0$, there is _complete wetting_ as it lowers energy
$$\cos\Theta=\frac{\gamma_{SV}-\gamma_{SL}}{\gamma_{LV}}$$
- For $-1<\cos\Theta<1$, there is _partial wetting_ at some angle
- For $\cos\Theta<-1$, a _completely spherical droplet_ forms

- Typically, _aqueous_ liquids _spead_ on _highly polarisable_ surfaces
- Otherwise, it depends on _relative polarisability_ of the liquid and surface
- _Contamination_ of a surface can change wetting to have a _range_ of contact angles

- Contact angle may be determined by _surface structure_
	- The presence of _pillars_ on plants will _increase_ contact angle, as water is _far_ from the surface and _cannot reduce energy_ by wetting
![[Hydrophobic surfaces.png|500]]
# Colloids
- A colloid consists of particles within size range of $10^{-3}-10^{-7}\,\text{cm}$
	- _Larger_ than ordinary molecules, but still _invisible to naked eye_
	- They may exist as _dispersions_ of one substance in another
- Colloids are typically _stabilised_ by van der Waals interactions

- Examples: 
	- _Suspensions_ formed from silica, metals, or polymers
	- _Viruses_
- They can have _many shapes_, such as spheres or rods

- In a _suspension_, the _distribution_ is Boltzmann-like due to _gravity_:
$$P(h)\propto\exp\left( -\frac{mgh}{k_{B}T} \right) $$
- In a colloid, $\langle h \rangle$ is _larger than the particle size_
- For a spherical particle:
$$\langle h \rangle = \frac{k_{B}T}{4\pi R^{3}\rho g/3} \sim R$$
- For a typical colloidal particle, $R\approx 1\,\mu\text{m}$

- Typically, colloids will _[[#Diffusion|diffuse]] over an experimental time-scale_ $2Dt_\text{exp} \sim R^{2}$
- A particle with $R\sim 1 \,\mu \text{m}$ will diffuse in water over $1\,\text{s}$

- Colloids are typically understood _without details about atomic constitution_

![[Colloid interactions.png|350]]
- Relevant interactions:
	- _Excluded volume_ (no overlap)
	- _Dispersion forces_ (van der Waals interactions)
	- _Coulomb interactions_ (for charged particles)
	- _Depletion interactions_ (non point-like particles)
	- _Steric repulsion_ (if coated in polymers to prevent aggregation)

## Excluded volume interaction
- One model is the _hard sphere potential_
- Let $r$ be the separation between particles of radius $a$
$$V(r)=\begin{cases}
0&r<2a \\ \infty &r>2a
\end{cases}$$
## Dispersion forces
- Interactions between _uncharged_ particles
	- They generally _repel_ when they are close, and _attract_ each other at intermediate distances
	- There is an _equilibrium distance_

### Pair potential and length scales
- Let there be a _pair potential_ $u(r)$, where $r$ is separation
$$F(r)=-\frac{du(r)}{dr}$$
- If $u(r) \sim r^{-1}$, it is _long ranged_
	- Example: Coulomb between point charges, gravity
- Van der Waals forces are _short ranged_ with $r^{-6}$
	- Can be modelled as _hard spheres_

![[pair interactio.png|450]]

- Coulomb interactions can become _short-ranged_ with more complex charge distributions such as _dipoles_ formed from _polarisable molecules_

### Dipole interactions
- For a particle with _polarisability_ $\alpha$, the _induced dipole moment_ is
$$\mu=\alpha E$$
- Force _experienced by a dipole_:
$$F(r)=-q\left[ E\left( r-\frac{\Delta r}{2} \right)-E\left( r+\frac{\Delta r}{2} \right) \right]\approx q\Delta r \frac{dE}{dr}=\mu \frac{dE}{dr}$$
- If the electric field is caused by a _charged molecule_ $Q$:
$$\displaylines{F(r)=-2\alpha\left( \frac{Q}{4\pi\epsilon_{0}\epsilon_{r}} \right)^{2} \frac{1}{r^{5}} \\ u(r)=-\frac{\alpha}{2}\left( \frac{Q}{4\pi\epsilon_{0}\epsilon_{r}} \right)^{2} \frac{1}{r^{4}} }$$
- These interactions are _always attractive_, and is very _short ranged_
	- Also _proportional_ to $\alpha$

- Between _two polarisable atoms_:
$$V_\text{atom-atom}(r)=-\frac{B}{r^{6}}$$
- Here, $B$ is the _interaction parameter_
	- Typically, $B>0$, making an _attractive_ potential
- It can be derived [[Time-Independent Approximation Methods#Van der Waals interaction|quantum mechanically]] for two atoms with characteristic frequency $\nu$
$$V_\text{two dipoles}(r)=-\frac{2\alpha^{2}h\nu}{(4\pi\epsilon_{0})^{2}} \frac{1}{r^{6}}$$

- For larger bodies, one can _approximate_ by summing over _interaction potentials between all pairs_, which _increases_ the range of interaction
![[vdW wit solids.png|500]]
$$\begin{align}
V_\text{atom-solid}(r)&=-\frac{\pi B\rho}{6r^{3}} \\ V_\text{solid-solid}(h)&=-\frac{A}{12\pi h^{2}}\text{ per unit area} \\ V_\text{sphere-sphere}(r)&=-\frac{\pi^{2}B\rho^{2}R}{12r}\;,\;r\ll R
\end{align}$$
- $\rho$ is the _density of atoms_
- $A(B,\rho)$ is the [[#Surface tension in 2D films|Hamaker constant]]

- Dispersion interactions are almost always _attractive_, leading to _aggregation_ and _destabilisation_ of the colloidal system
	- Tends to _weaken_ when the _solvent_ has the _same polarisability_ as the colloid
![[vdW gellation.png|600]]

- In cases where $A<0$, atoms _maximise interactions with the environment_
	- Example: liquid helium

## Coulomb interactions preventing aggregation
- In _dilute electrolyte solutions_, the presence of _charged surfaces_ can prevent aggregation
	- Electrolytes: ion solutions
- The ions are _surrounded_ by solvent molecules which provide _electrostatic screening_
- _Charge neutrality_ dictates that for a collection of ions with charge $z_{i}e$ and density $n_{i}$
$$\sum z_{i}n_{i}=0$$

### Bjerrum length
- _Thermal energy_ dictates a _length-scale_ known as the _Bjerrum length_ when _Coulomb interactions_ are present:
$$\frac{z_{i}z_{j}e^{2}}{4\pi\epsilon_{0}\epsilon_{r}} \frac{1}{l_{B}}=k_{B}T\hspace{1cm}l_{B}=\frac{z_{i}z_{j}e^{2}}{4\pi\epsilon_{0}\epsilon_{r}}$$
- At _room temperature water_, $l_{B}\sim0.7\,\text{nm}$
- If molecules aggregate _closer_ than the Bjerrum length, they start to _fall out of solution_
- $l_{B}$ is _only dependent on the solution itself_

### Charged surfaces and the Poisson-Boltzmann equation
- Consider a _charged surface_, with _counter-ions_ of opposite charge
	- There are also _co-ions_ with the same charge as the surface
- The counter-ions provide _screening_

- The _distribution_ of counter-ions is determined by the _Poisson equation_:
$$\nabla^{2} \phi(\boldsymbol{r})=\frac{\rho(\boldsymbol{r})}{\epsilon_{0}\epsilon_{r}}\hspace{1.5cm}\rho(\boldsymbol{r})=\sum_{i}ez_{i}n_{i}(\boldsymbol{r})$$
- The ions also follow a _Boltzmann distribution_:
	- For $\boldsymbol{r}\to \infty$ in the _bulk_, $n_{i}=n_{0}$
$$n_{i}(\boldsymbol{r})=n_{i0}\exp\left( -\frac{z_{i}e\phi(\boldsymbol{r})}{k_{B}T} \right)$$
- For an _infinite plane_, it is a 1D problem:
$$\frac{\partial^{2}}{\partial x^{2}}\phi(x)=-\frac{e}{\epsilon_{0}\epsilon_{r}}\sum_{i}z_{i}n_{i0}\exp\left( -\frac{ez_{i}\phi(x)}{k_{B}T} \right)$$
- This is the _Poisson-Boltzmann equation_
	- It is _non-linear_

### Debye-Huckel approximation and potential
- For $\phi(x)\ll k_{B}T$, the equation can be _linearised_ to get the _Debye-Huckel equation_:
	- The constant term from the exponential _cancels out_ due to _charge neutrality_
$$\begin{align}
\frac{\partial^{2}}{\partial x^{2}}\phi(x)&\approx \sum_{i} \frac{e^{2}z_{i}^{2}n_{i0}}{\epsilon_{0}\epsilon_{r}k_{B}T}\phi(x) \\ &=\kappa^{2}\phi(x)
\end{align}$$
- $1/\kappa\equiv\lambda_{D}$ is the _Debye screening length_:
	- Unlike $l_{B}$, it is _dependent_ on the _bulk distribution_ of ions
$$\kappa^{2}=\frac{e^{2}}{\epsilon_{0}\epsilon_{r}k_{B}T}\sum_{i}z_{i}^{2}n_{i0} \hspace{1.5cm}l_{D}=\lambda_{D}\equiv \frac{1}{\kappa}$$
![[Screening layer.png]]
- Solution to the Debye-Huckel equation:
$$\phi(x)=\phi(0)\exp(-\kappa x)$$
- From _boundary conditions_ due to surface charge density $\sigma$:
$$-\kappa \phi(0)=-\frac{\sigma}{\epsilon_{0}\epsilon_{r}}$$
- This gives the solution:
$$\phi(x)=\frac{\lambda_{D}\sigma}{\epsilon_{0}\epsilon_{r}}\exp\left( -\frac{x}{\lambda_{D}} \right)$$
- The _surface potential_ $\phi(0)$ is _dependent on ion concentrations_

### Charge density
- The ion concentrations:
$$n_{i}(x)=n_{i0}\exp\left( -\frac{z_{i}e\phi(x)}{k_{B}T} \right)$$
- In the _linear_ regime:
$$n_{i}(x)=n_{i0}\left[ 1-\frac{z_{i}e}{k_{B}T}\phi_{0}\exp\left( -\frac{x}{\lambda_{D}} \right) \right]$$
- Monovalent ions:
$$n_{\pm}(x)=n_{0}\left[ 1\mp \frac{e}{k_{B}T}\phi_{0}\exp\left( -\frac{x}{\lambda_{D}} \right) \right]$$
- There is a _counter-ion accumulation_ around the surface to screen the charge
- At the same time, there is a _co-ion depletion_
- This forms an _electric double layer_ at the surface
	- Typical thickness: $\lambda_{D} \approx 0.5\,\text{nm}$
	- The potential of the double layer is the _$\zeta-$potential_

- The _net charge density_ in the layer, using the above:
	- _Integrating_ gives the _charge of the original layer_, as expected from neutrality
$$\rho(x)=-\frac{\sigma}{\lambda_{D}}\exp\left( -\frac{x}{\lambda_{D}} \right)$$
### Other geometries
- Let there be a _spherical colloidal particle_ with charge $Q$ and radius $a$:
- In spherical polars, the Debye-Huckel equation:
$$\frac{1}{r^{2}} \frac{\partial}{\partial r}\left( r^{2}\frac{\partial \phi}{\partial r} \right)=\frac{1}{r} \frac{\partial^{2}}{\partial r^{2}}(r\phi)=\kappa^{2}\phi(r)$$
- With boundary conditions, this gives the solution:
$$\phi(r)=\frac{Q}{4\pi\epsilon_{r}\epsilon_{0}r(1+\kappa a)}\exp[-\kappa(r-a)]$$
- As expected, the _surface charge_ is _screened_

- Let there be _two spherical charged particles_ a distance $d$ apart
	- Size: $a\approx 500\,\text{nm}$
	- Typical $\lambda_{D}\approx 1\,\text{nm}$
- As $\lambda_{D}\ll a$, the _curvature_ can be neglected

- Let $d\ll a$, so the system can be treated as _two semi-infinite parallel plates_
- The _osmotic pressure_ of the counter-ions tend to _push the particles apart_
	- The counter-ions _accumulate_ to be _more concentrated than the bulk_
- Charge density:
$$\displaylines{n(x)=\sum_{i}n_{i}\exp\left( -\frac{z_{i}e\phi(x)}{k_{B}T} \right) \\ \frac{\partial n}{\partial x}=-\frac{\epsilon_{0}}{k_{B}T}\frac{\partial^{2}\phi}{\partial x^{2}} \frac{\partial \phi}{\partial x}=\frac{\epsilon_{0}}{2k_{B}T}\frac{\partial}{\partial x}\left( \frac{\partial \phi}{\partial x} \right)^{2}}$$
- _Integrating_, recognising $E(x)=-\partial \phi/\partial x$, and multiplying by $k_{B}T$
$$k_{B}T\,n(x)-\frac{1}{2}\epsilon_{0}[E(x)]^{2}=\text{const.}\,k_{B}T$$
- The two terms represent _pressure_ on the plates
$$\Pi _\text{wall}=k_{B}T\left[ n\left( x=\frac{d}{2} \right)-n_{0} \right]$$
- _Excess counter-ions_ will create _osmotic pressure_
	- If $n(x=d/2)=n_{0}$, there is _no pressure_

- From the solution to the Debye-Huckel equation:
$$\Pi _\text{wall}=\frac{\sigma^{2}}{\epsilon_{r}\epsilon_{0}}\exp\left( -\frac{d}{\lambda_{D}} \right)$$
### High surface charge
- The _full_ Poisson-Boltzmann equation, for a _high charge density_:
$$\frac{d^{2}\phi}{dx^{2}}=\frac{2en_{0}}{\epsilon_{w}}\sinh\left( \frac{e\phi}{k_{B}T} \right)$$

- For a _semi-infinite geometry_:
$$\phi(x)=\frac{2k_{B}T}{e}\ln\left( \frac{1+\gamma \exp(-x/\lambda)}{1-\gamma \exp(-x/\lambda)} \right)$$
- Here, introducing the _Gouy-Chapman length_ $\lambda _\text{GC}$:
$$\lambda _\text{GC}=\frac{2k_{B}T\epsilon_{w}}{e|\sigma|}\hspace{1.5cm}\gamma=-\frac{\lambda _\text{GC}}{\lambda}+\sqrt{ 1+\left( \frac{\lambda _\text{GC}}{\lambda} \right)^{2} }$$
- For low values of $\sigma$, the Debye-Huckel result is recovered
![[High surface charge screening.png|500]]
- For large $\sigma$, the potential _far from the surface_ becomes _independent_ of $\sigma$
- All _additional screening charge_ is located _close to the charged surface_

- _Screening_ a _highly charged_ surface:
	- There is a _diffuse layer_ a few Debye lengths wide, with _symmetric distributions_ of excess counter-ions and missing co-ions
	- A more _compact layer_ of mostly _counter-ions_

## DLVO Theory
- The description of _interactions between charged particles in colloids_ by Derjaguin, Landau, Verwey and Overbeek
	- _Attraction_ due to van der Waals forces
	- _Repulsion_ due to electrostatics

![[DLVO potential.png|450]]
- The _functional forms_ of interactions in DLVO theory, for particles of radius $R$ and charge $Q$, a distance $r$ apart:
	- $U_{e}$ is _repulsive_ and $U_\text{vdW}$ is _attractive_
	- Ignoring hard core potential for _longer distances_
$$\displaylines{U(r)=U_{e}+U_\text{vdW} \\ U_{e}=\left( \frac{Q\exp(\kappa R)}{1+\kappa R} \right)^{2}\frac{\exp(-\kappa r)}{\epsilon_{0}\epsilon_{r}r} \\ U_\text{vdW}=-\frac{\mathcal{B}}{6}\left[ \frac{2R^{2}}{r^{2}-4R^{2}}+\frac{2R^{2}}{r^{2}}+\ln\left( \frac{r^{2}-4R^{2}}{r^{2}} \right) \right]}$$
- $\mathcal{B}$ is analagous to the [[#Dipole interactions|Hamaker constant]]
- $U_\text{vdW}$ is the more accurate form for $r>R$
	- The _Hamaker summation_
	- For $r=2R+h$, with $h\ll R$, reduces to $\propto h^{-1}$ as [[#Dipole interactions|expected]]

- The _decay_ of $U_\text{vdW}$ is _slower_ than two semi-infinite planes $(h^{-2})$ 
	- For spheres, changes in separation matter _less_

- There are some conditions under which $U(r)$ is _repulsive overall_, which _prevents aggregation_
	- High _surface charge_
	- Low _bulk ionic strength_ or _colloid concentration_
- There may also be _metastable minima at large distances_
	- Gives rise to _Bragg scattering_ and _self-assembling photonic crystals_

- Typically, for _long time-scales_ and _finite concentrations_, aggregation is _most favourable_
	- Example: gold nanoparticles coated with charge
## Other interactions
- DLVO: accounts for _dispersion, Coulomb, hard core repulsion_ interactions

### Steric interactions
- Colloids can be _coated_ in [[#Brushes|polymer brushes]] to enhance _steric interactions_
	- There is _osmotic pressure_ from _pressing_ the polymer layer
	- The brush can be _extended_ into regions where _dispersion_ is negligible
	- The brush itself is [[#Excluded volume interaction and swelling|swollen]] and dilute, hence _does not contribute to dispersion_
- Example: _casein_ layer outside _fat_ in milk

### Depletion interaction
- _Entropic_ in origin, for solutions with _small particles_ between _larger objects_
- If there is a _small gap_ between the large objects, there are _fewer small particles_, and are _depleted_ from the gapped region
- The large objects are subject to an _osmotic pressure_ from the outside, and hence are _attracted to each other_

- The _range_ is the _diameter_ of the small particles
	- Most effective when there are _no small particles at all_ in the gap
- Interaction _potential_ is set by the _osmotic pressure_, which depends on _concentration_
- Effectively, a _square well potential_, with a _depth_ of $k_{B}T$

- For a _dilute solution_ of _non-interacting_ particles or _polymers_, the _osmotic pressure_ is given by the _ideal gas law_, with $N$ polymers and _total solution volume_ $V$
$$P_\text{osm}=\frac{N}{V}k_{B}T$$
- The _interaction potential_ is then:
$$U_\text{dep}=-P_\text{osm}V_\text{dep}$$
- $V_\text{dep}$ is the _exclusion volume_
- For two particles of _radius_ $a$ and _separation_ $r$, given a _depletion layer thickness_:
$$V_\text{dep}=\frac{4\pi}{3}(a+L)^{2}\left[ 1-\frac{3r}{4(a+L)}+\frac{r^{3}}{16(a+L)^{3}} \right]$$

- An _increase_ in _number density_ will increase the _attraction_, leading to _aggregation_

## Phase diagram of colloidal suspensions

![[Colloid phase diagram.png]]
- There are _ordered_ and _disordered_ phases
# Electrokinetic phenomena
- Pulling a system _out of equilibrium_ using _electric fields_

- Electro-osmosis and electro-phoresis: opposites
- Streaming potential: _pressure-driven_
![[EKP.png]]
## Electro-osmotic flow
- The _movement_ of a liquid _over an immobilised_ (semi-infinite) _charged surface_, with a _parallel electric field_
![[EOF.png]]
- The profile of _ion concentration perpendicular_ to the surface is given by the [[#Charged surfaces|Poisson-Boltzmann equation]]
- The motion _parallel_ to the surface is given by the [[#Navier-Stokes equation]]
- The system is _separable_ along the two directions
### Movement of ions
- Let there be a _constant electric field_ $\boldsymbol{E}=E\hat{x}$
- The _force_ on ions:
$$F_\text{el}=z_{i}eE=-z_{i}e \frac{\partial \psi}{\partial x}$$

- At _low_ [[#Reynolds number]], there is _no inertia_, and $F_\text{el}$ is _balanced_ by _drag_
$$F_\text{el}+F_\text{drag}=z_{i}eE-\xi v=0 \implies v_\text{ion}=\frac{F_\text{el}}{\xi}$$
- Model it as _Stokes drag_, where $\xi=6\pi \eta a$, with $\eta$ being the _viscosity_

- The ions will _transfer momentum_ to water, leading to bulk _water flow_
- The [[#Charged surfaces|Debye-Huckel length]] for _monovalent ions_ of density $n$:
	- In water: $\epsilon_{w}=\epsilon_{r}\epsilon_{0}$
	- Applies for $e\phi(x)\ll k_{B}T$
$$\lambda _{D}=\sqrt{ \frac{\epsilon_{w}k_{B}T}{2e^{2}n} }$$
- Solution for potential, along with the electric field:
$$\displaylines{\phi(x,y)=\frac{\lambda_{D}\sigma}{\epsilon_{0}\epsilon_{r}}\exp\left( -\frac{y}{\lambda_{D}} \right)-Ex \\ \rho=-\frac{1}{\epsilon_{w}}\nabla^{2}\phi=\rho(y)}$$
### Velocity profile
- Let the fluid be _incompressible_, hence the Navier-Stokes equation becomes:
$$\rho(\boldsymbol{r})\boldsymbol{E}+\eta \nabla^{2}\boldsymbol{v}=0$$
- Parallel flow:
$$\displaylines{\boldsymbol{v}=v_{x}(y)\hat{x} \\ -\epsilon_{w}\frac{\partial^{2}\phi}{\partial y^{2}}E+\eta \frac{\partial^{2}v_{x}}{\partial y^{2}}=0}$$
- Integrating twice, with the _no-slip_ boundary condition:
$$v_{x}(y=0)=0$$
- Also assume _far away_ from the plate (_thin Debye layer_ limit), where 
$$\frac{\partial \phi}{\partial y}\Bigg|_{y\gg\lambda_{D}}=0$$
- The full solution:
$$v_{x}(y)=\frac{\epsilon_{w}}{\eta }[\phi(y)-\phi_{0}]E$$

- _Helmholtz-Smoluchowski equation_ for _counter-ions_ in the centre:
$$v_\text{eo}=-\frac{\epsilon_{w}}{\eta}\zeta E$$
- $\zeta=\phi_{0}$ is the _zeta-potential_ at the plate
- One can define the _electrophoretic mobility_ of the ions:
$$\mu _\text{eo}=-\frac{\epsilon_{w}}{\eta}\zeta$$
- In this limit, counter-ions and co-ions have _equal and opposite velocities_

- This does not take the _surface conduction_ close to the surface, or the _polarisation_ of the electric double layer into account

### Testing the Helmholtz-Smoluchowski equation
- A _single colloidal particle_ in an _optical trap_
![[Optical tweezers.png|450]]
- The _optical tweezers_ can exert a _restoring force_ $-\kappa\Delta x$
- The _electrophoretic mobility_ $\mu$ can be measured by:
	- The particle is taken to be in _equilibrium_ at all times as it is in the _low Reynolds number_ regime
$$v_\text{eff}(t)=-\frac{\kappa\Delta x(t)}{6\pi \eta r}+u_{e}E(t)$$
- If $E(t)$ _oscillates_ with frequency $f$, and the _maximum amplitude_ is $\Delta X$, the _average_ velocity over a period is $4\Delta Xf$, and one can _measure_ $|u_{e}|$
$$|u_{e}|=\frac{4\Delta Xf}{E}+\frac{\kappa\Delta X}{6\pi \eta rE}$$
- The _zeta-potential_ can also be _extracted_ as:
$$\zeta=\frac{\eta}{\epsilon_{w}}u_{e}$$
## Streaming potential
- Using a _pressure gradient_ to drive flow in a _charged channel_
- This leads to _charge separation_ and hence a _current_
- It can be used to _generate power_

- Total current through a _cross-section_ of width $w$ and height $h$:
	- Ignoring _sidewall_ effects as $w\gg h$
$$I_\text{str}=w\int _{h/2}^{h/2} \rho(x)v(x) \, dx $$
- Typical flow profile: [[#Pressure-driven flow in a channel|Poiseuille flow]] with no-slip conditions
- Expected to increase _linearly_ with pressure

![[EOF vs pressure.png]]
![[EOF vs streaming.png|350]]
## Zeta-potential and the atomic double layer
- The $\zeta-$potential denotes the potential at the _no-slip plane_ $d^{\text{ek}}$ from the surface with _surface charge_ $\sigma_{0}$ and _surface potential_ $\Psi^{0}$
- The $\zeta-$potential is always _smaller than the bare surface potential_
- Assumptions:
	- There is a _thin layer without charges_ due to an _absorbed water layer_, known as the _inner Helmholtz plane_ (IHP), with potential $\Psi^{i}<\Psi^{0}$
	- The potential is _further reduced_ by the _adsorbed ions_ in the _outer Helmholtz plane_ with $\Psi^{d}<\Psi^{i}$
	- There is then another _charge-free layer_, hence $\zeta<\Phi^{d}$, at the _no-slip plane_
	- Further than $d^{ek}$, the water and ions are _in motion_

- The IHP and OHP are collectively known as the _Stern layer_
![[EDL.png|450]]
- The exact _position_ of the no-slip plane is often _not known_, depending on the _type and valency_ of counter-ions, salt _concentrations_, and the _geometry_ of the system
	- _Defined_ by the fluid motion, and details of measurements
![[EDL molecules.png|450]]
### Double layer capacitance
- The _split charges_ in the double layer lead to a _measurable capacitance_, and is used to _probe the thickness of Helmholtz planes_
	- In the limit of _high salt concentrations_ where the Debye length is _short_
- The _differential capacitance_, given some _AC voltage_ $V(t)$
$$C_\text{diff}=\frac{dQ}{dV}$$
- The _current_ through the capacitor:
$$I_{C}=C_\text{diff}\,\frac{dV}{dt}$$
- The EDL can be approximated as a _double plate capacitor_
- For a _Debye length_ of $\approx 0.2\,\text{nm}$, $\epsilon\epsilon_{0}/d\approx 350\,\mu \text{F cm}^{-2}$, which is an _over-estimation_ compared to the _experimental value_ by a factor of $\approx7$
- There is practically a _reduction_ in $\epsilon$ as the water molecules are _frozen_ on the surface and _less polarisable_

- It can be modelled as _two capacitors in series_, as $\epsilon$ _changes across the layer_
- Model as a layer of _dipoles_, along with the IHP-OHP
	- $a$: diameters of _water molecules_ and _counter-ions_ respectively
	- Valid for _Debye length close to_ width of IHP/OHP 
$$\frac{1}{C_\text{Stern}}=\frac{1}{C_\text{dipole}}+\frac{1}{C_\text{IHP-OHP}}=\frac{a_\ce{ H_{2}O }}{\epsilon_\text{dipole}}+\frac{a/2}{\epsilon _\text{IHP}}$$
- For a _thick Debye screening layer_, there needs to be a _third term_

## Gel electrophoresis
- Driving charged molecules through a _dense network of cross-linked polymers_, using an _electric field_
- Factors include _polymer dynamics_, _electro-osmosis_, and interactions between the _DNA and the gel matrix_

- Long DNA is treated as _free-draining_, as solvent molecules can _fow past_ each segment
- It behaves as a _solid particle_ rather than a _colloid_
	- The particle radius is the _radius of gyration_
	- They themselves can be described by a $\zeta-$potential depending on charge density
	- Therefore, mobility is _independent_ from their length
- Therefore, _separation of free-draining polymers by length_ is impossible in a solvent

- Separation is accomplished using a _gel matrix_, as _interactions_ between gel and DNA is dependent on the length of the latter
- Similar to a _concentrated polymer solution_, with _electrophoretic mobility_ controlled by the _effective pore diameter_ of the gel
- Typically, _agarose_ is used for the gel
	- Easy to control _pore diameter_
![[Agarose gel.png|500]]

### Rouse model for diffusion
- Use the [[#Rouse model of polymer dynamics|Rouse model]]
	- Each monomer also has a _friction coefficient_ $\gamma$ independent of position in the chain
	- There are _no hydrodynamic interactions_, hence the polymer is _free-draining_
- The _centre of mass diffusion coefficient_:
$$D_{R}=\frac{k_{B}T}{N\gamma}$$
- Define the _Rouse time_ $\tau_{R}$, where the polymer _diffuses its end-to-end distance_
- For the _ideal chain_:
$$\tau_{R}=\frac{R_{N}^{2}}{D_{R}}=\frac{\gamma b_{0}^{2}}{k_{B}T}N^{1+2\nu}=\tau_{0}N^{2}$$
- $\tau_{0}$ is the time taken for a _monomer_ to diffuse if _not linked_ to the chain

- _Approximate_ $\gamma\approx \eta b_{0}$:
$$\tau_{R}=\left( \frac{\eta b_{0}^{3}}{k_{B}T} \right)N^{2}$$
- For $t\ll \tau_{0}$, the polymer chain appears _static_ and responds _elastically_
- For $t\gg \tau_{R}$, the polymer _diffuses_
- In the  _intermediate_ regime, it behaves _visco-elastically_

### Zimm model of polymer hydrodynamics
- The Zimm model defines a _no-slip condition_ on the chain, hence it is _not free-draining_
- A more _realistic_ model of hydro-dynamic interactions, especially in _dilute solutions_
- The _Zimm diffusion coefficient_:
	- $R$ is the _radius of gyration_
$$D_{Z}=\frac{k_{B}T}{\eta R}=\frac{k_{B}T}{\eta bN^{\nu}}$$
- The _Zimm relaxation time_:
$$\tau_{Z}=\frac{R^{2}}{D_{Z}}=\frac{\eta b^{3}}{k_{B}T}N^{3\nu}\equiv \tau_{0}N^{3\nu}$$
- It has a _weaker_ $N$ dependence compared to $\tau_{R}\sim N^{2}$

### Reptation
- In the Zimm and Rouse models, chain segments still _move independently_ from one another
- For polymer _melts_, there are entangled chains which _overlap_ and _cannot cross_

- The _reptation model_ assumes that the chain moves in a _tube_ defined by the surrounding chains
- The _diameter_ of the tube is given by $r_{t}\approx b\sqrt{ N_{e} }$
	- $N_{e}$ is the _average number of monomers between two entanglements_
	- The diameter is also known as the _entanglement length_

- The _coarse-grained chain length_ is $R_{0}=r_{t}\sqrt{ N/N_{e} }=b\sqrt{ N }$
- There is also a _coarse-grained contour length_
$$\langle L \rangle \approx r_{t} \frac{N}{N_{e}}=\frac{bN}{\sqrt{ N_{e} }}$$

- _Diffusive motion_ in the tube is known as _reptation_, with the _Rouse diffusion coefficient_
$$D_{c}=\frac{k_{B}T}{N\gamma}$$

- The _reptation time_ is the time taken to _diffuse along the tube length_
$$\tau _\text{rep}=\frac{\langle L \rangle^{2}}{D_{c}}=\frac{\gamma b_{0}^{2}N^{3}}{k_{B}TN_{e}} =\frac{\gamma b_{0}^{2}}{k_{B}T}N_{e}^{2}\left( \frac{N}{N_{e}} \right)^{3} $$
- The _lower limit_ has $N=N_{e}$

- It can be shown that through reptation, given a _force per Kuhn segment_ $f$, for a polymer with $N$ Kuhn segments, the _drift velocity_ $v_{d}$ is:
$$v_{d}=\frac{f}{\eta bN}$$
### Tether force