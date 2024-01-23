- A fluid is a _flowing continuous medium_
- It has well-defined _macroscopic properties_:
$$\boldsymbol{v}(\boldsymbol{r},t),\rho(\boldsymbol{r},t),p(\boldsymbol{r},t)$$

- Fluids are present in _interstellar medium_, _stars_, and giant _planets_ (e.g. Jupiter)

# Fluid elements
- One can consider a _fluid element_
- It must be _small enough_, that _macroscopic properties_ $q$ are _approximately constant_:
$$l_\text{region}\ll l_\text{scale}\sim \frac{q}{|\nabla q|}$$
- It must also be _large_ enough to contain a _large number of particles_:
$$nl_\text{region}^{3}\gg 1$$
- With these satisfied, the fluid can be considered a _continuum_
	- Otherwise, it must be considered _particle by particle_

## Collisional and collisionless fluids
- Particles have some _mean free path_ $\lambda$, the typical distance _traveled_ by a particle _between collisions_
- In a _collisional fluid_, $l_\text{scale}\gg\lambda$
- Particles have a _velocity distribution_ that _maximises entropy_
- Hence, there are _well-defined properties_
- One can define an _equation of state_:
$$p=p(\rho,T)$$

- In a _collisionless fluid_, $l_\text{scale}\ll\lambda$
- Velocity distribution is _not determined locally_
- It depends on _initial and non-local conditions_
- Examples include _stars in a galaxy_, dark matter, or _interstellar medium_ in galaxy clusters

## Eulerian and Lagrangian descriptions
- One can follow an _Eulerian description_, which defines properties as a _function of time in a fixed spatial reference frame_:
$$\rho(\boldsymbol{r},t),p(\boldsymbol{r},t),T(\boldsymbol{r},t)\dots$$

- One can also follow a _Lagrangian description_, which considers properties _of a fixed fluid element_, as a function of _time_
	- _Position_ is a function of both _time_, and the _label of the fluid element_

- The Lagrangian approach is important if the path of an _individual element_ is important
	- e.g. tracing a _parcel with particular composition_

- The Eulerian approach is useful for _steady flows_, where $\partial q/\partial t=0$ for all physical quantities $q$

## The convective derivative
- One can _relate the rates of change_ in the two descriptions
- An _Eulerian time derivative_ is $\partial Q/\partial t$

- In the Lagrangian description, consider _rate of change_ of a quantity $Q$ _in a moving fluid element_, denoted $DQ/Dt$
$$\frac{DQ}{Dt}=\lim_{ \delta t \to \infty }\left[ \frac{Q(\boldsymbol{r}+\delta \boldsymbol{r},t+\delta t)-Q(\boldsymbol{r},t)}{\delta t} \right] $$
- This becomes:
$$\frac{DQ}{Dt}=\frac{\partial Q}{\partial t}+(\boldsymbol{u}\cdot \nabla )Q$$
- The derivative in the Lagrangian derivative adds a _convective term_ $(\boldsymbol{u}\cdot \nabla )Q$, which accounts for _movement of the fluid element_

## Kinematics of a fluid
- One can define _streamlines_, a family of curves _instantaneously tangent to the velocity vector_ $u(\boldsymbol{r},t)$:
$$\displaylines{\frac{d\boldsymbol{r}}{ds}=\left( \frac{dx}{ds},\frac{dy}{ds},\frac{dz}{ds} \right) \\ \frac{d\boldsymbol{r}}{ds}\times \boldsymbol{u}=0 \implies \frac{dx}{u_{x}}=\frac{dy}{u_{y}}=\frac{dz}{u_{z}}}$$
- In _non-Cartesian coordinates_, the form is different (e.g. spherical polars):
$$\frac{dr}{u_{r}}=\frac{r\, d\theta}{u_{\theta}}=\frac{r\sin\theta \,d\phi}{u_\phi}$$

- One can also consider _particle paths_, which are paths _followed by individual particles_:
$$\frac{d\boldsymbol{r}}{dt}=\boldsymbol{u}(\boldsymbol{r},t)$$
- The _integration constant_ becomes a _label_ for the particle

- One can also consider _streaklines_, which _joins the instantaneous positions of all particles that have ever passed some point_ $\boldsymbol{r}_{0}$
- i.e. $\boldsymbol{r}(\boldsymbol{a},0)$ for _all particles_ $\boldsymbol{a}$ such that $\boldsymbol{r}(\boldsymbol{a},t_{0})=\boldsymbol{r}_{0}$

- In _steady flow_, they all _coincide_:
$$\frac{\partial \boldsymbol{u}}{\partial t}=0$$
- Every particle passing through a _given point_ will all _follow the same path_

- Example: $\boldsymbol{u}(t<0)=(u,0,0)$, $\boldsymbol{u}(t>0)=(0,u,0)$
	- Streamlines, particle paths, streaklines
![[stream path streak.png|500]]
# Fluid equations
- Equations _governing the flow of fluid_
## Conservation of mass
![[mass fluid element.png]]
- Consider a _fixed arbitrary volume_ $V$
- The _change in mass_ must correspond to some _flow across the surface_:
$$\frac{\partial }{\partial t}\int_{V} \rho \, dV=-\int_{S} \rho \boldsymbol{u}\cdot \, d\boldsymbol{S}  $$
- Using the _divergence theorem_, and as it must be _true for all volumes_, one gets _continuity in the Eulerian description_:
$$\frac{\partial \rho}{\partial t}+\nabla\cdot(\rho \boldsymbol{u})=0$$
- Using the Lagrangian time derivative:
$$\frac{D\rho}{Dt}+\rho \nabla\cdot \boldsymbol{u}=0$$
- In an _incompressible flow_, all _fluid elements_ must have _constant density_, and one gets:
$$\frac{D\rho}{Dt}=0\implies\nabla\cdot \boldsymbol{u}=0$$

## Conservation of momentum
- Consider some _fluid element_ of volume $V$ subject to _pressure_, as well as an _external gravitational field_ $\boldsymbol{g}$
- _Project_ the pressure along some _arbitrary direction_ $\hat{\boldsymbol{n}}$:
$$\boldsymbol{F}_{p}\cdot \hat{\boldsymbol{n}}=-\int _{S}p \hat{\boldsymbol{n}}\cdot \, d\boldsymbol{S}=-\int _{V}\hat{\boldsymbol{n}}\cdot \nabla p \, dV  $$
- Then consider the _rate of change of momentum_ in the fluid element, due to both _pressure_ and external force:
$$\left( \frac{D}{Dt}\int _{V}\rho \boldsymbol{u} \, dV  \right)\cdot \hat{\boldsymbol{n}}=-\int \hat{\boldsymbol{n}}\cdot \nabla p \, dV+\int \rho \boldsymbol{g} \, dV  $$
- Take the _limit_ to a _fluid element_, with _infinitesimal volume_ $\delta V$

- By _mass conservation of the fluid element_, $D(\rho\delta V)/Dt=0$

- One then gets the _Lagrangian equation of motion_:
$$\rho \frac{D\boldsymbol{u}}{Dt}=-\nabla p+\rho \boldsymbol{g}$$
- One can convert to an Eulerian description using the convective derivative:
$$\rho \frac{\partial \boldsymbol{u}}{\partial t}+\rho(\boldsymbol{u}\cdot \nabla)\boldsymbol{u}=-\nabla p+\rho \boldsymbol{g}$$

## Stress tensor and ram pressure
- Fluid elements can undergo _pressure_, but also _viscous stresses_
- Hence one must use a _tensorial relation_:
$$dF_{i}=\sigma_{ij}dS_{j}$$
- An _isotropic pressure_ corresponds to $\sigma_{ij}=p\delta_{ij}$

- _Expand_ the Eulerian equation of motion to get _components of stress_ in different directions

- Using the equation above, one gets
$$\partial_{t}(\rho u_{i})=-\partial_{j}(p\delta_{ij}+\rho u_{i}u_{j})+\rho g_{i}$$

- One can then define the _stress tensor_:
$$\sigma_{ij}=p\delta_{ij}+\rho u_{i}u_{j}$$
- This combines the effects of _pressure_ with _bulk motion_
- In _component-free_ language:
$$\underline{\underline{\boldsymbol{\sigma}}}=p\underline{\underline{I}}+\rho \underline{\boldsymbol{u}}\otimes \underline{\boldsymbol{u}}$$
- It is _symmetric_

- The bulk term gives the $x_{i}-$_directional momentum flux per second_, through a _surface of constant_ (normal to) $x_{j}$
- It is also known as the _ram pressure_

- The _thermal pressure_ is _isotropic_ due to the _random motions_ of the molecules

- The general equation of motion, given a stress tensor:
$$\displaylines{\partial_{t}(\rho \underline{\boldsymbol{u}})=-\nabla\cdot \underline{\underline{\boldsymbol{\sigma}}}+\rho \underline{\boldsymbol{g}} \\ \partial_{t}(\rho u_{i})=-\partial_{j}(\sigma_{ij})+\rho g_{i}}$$
