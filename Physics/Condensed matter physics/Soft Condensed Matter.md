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
- This typically gives a _strain along perpendicular directions_
- Define _Poisson's ratio_:
$$\nu=-\frac{\epsilon_{yy}}{\epsilon_{x x}}$$
- It is typically _positive_, but can be _negative_ (auxetic materials)

- The _volumetric deformation_ of a material:
$$\epsilon_{x x}+\epsilon_{yy}+\epsilon_{zz}=\text{Tr}(\epsilon)$$
- For an isotropic _pressure_:
$$-p=\text{Tr}(\sigma)$$
- The _bulk modulus_:
$$B=-\frac{p}{\text{Tr}(\epsilon)}$$
- This can be written as:
$$B=\frac{E}{3(1-2\nu)}$$
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
- In _analogy_ with the general case without potentiak:
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

## The ideal chain
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

### Differences to real chains
- Typically, _real chains_ have $\nu>1/2$
	- The _excluded volume_ of the polymer causes it to _swell_

- $R$ also scales with some _natural length scale_
- It is _not necessarily the size of a monomer_
- For real chains, it is known as the _Kuhn length_ $b$

## Freely jointed chain
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
- The _scaling_ $\nu=1/2$ is retained, but the _effective length_ is now:
$$b=b_{0}\sqrt{ \frac{1+\cos\theta}{1-\cos\theta} }$$