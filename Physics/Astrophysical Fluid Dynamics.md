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
- Examples include _stars in a galaxy_, or dark matter
	- _Intracluster medium_ (ICM) is typically an _edge case_

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
- It comes from _random thermal motion_

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
	- It can _strip gaess from galaxies_, which affects _stellar evolution_ in that galaxy
- Example: a flow _only in the $y-$direction_ will only ram a surface normal to $y$:
$$\sigma_{ij}=\begin{pmatrix}p&0&0\\0&p+\rho u^{2}&0\\0&0&p\end{pmatrix}$$

- The _thermal pressure_ is _isotropic_ due to the _random motions_ of the molecules

- The general equation of motion, given a stress tensor:
$$\displaylines{\partial_{t}(\rho \underline{\boldsymbol{u}})=-\nabla\cdot \underline{\underline{\boldsymbol{\sigma}}}+\rho \underline{\boldsymbol{g}} \\ \partial_{t}(\rho u_{i})=-\partial_{j}(\sigma_{ij})+\rho g_{i}}$$

# Gravitation
- One can define a _gravitational potential_ $\Psi$ such that the _gravitational acceleration_ $\boldsymbol{g}$ is:
$$\boldsymbol{g}=-\nabla \Psi$$
- As it is a _gradient_, the force is _conservative_, and the _work done around a closed loop vanishes_
- The _work done against gravity_ in taking _a unit mass_ from $\boldsymbol{r}_{a}$ to $\boldsymbol{r}_{b}$ is:
$$W(\boldsymbol{r}_{a}\to \boldsymbol{r}_{b})-\int _{a}^{b} \boldsymbol{g}\cdot d\boldsymbol{r}= \Psi(\boldsymbol{r}_{b})-\Psi(\boldsymbol{r}_{a})$$

- The gravitational potential of a _point mass_ $M$ in position $\boldsymbol{r}'$ is:
$$\Psi(\boldsymbol{r})=-\frac{GM}{\left| \boldsymbol{r}-\boldsymbol{r}' \right| }$$
- For a _system of point masses_:
$$\Psi(\boldsymbol{r})=-\sum_{i}\frac{GM_{i}}{\left| \boldsymbol{r}-\boldsymbol{r}'_{i} \right| }\implies \boldsymbol{g}(\boldsymbol{r})=-\sum_{i}GM_{i} \frac{\boldsymbol{r}-\boldsymbol{r}'}{|\boldsymbol{r}-\boldsymbol{r}'|^{3}}$$

## Poisson's equation
- For some _continuous mass distribution_:
$$\boldsymbol{g}(\boldsymbol{r})=-G\int \rho(\boldsymbol{r}') \frac{\boldsymbol{r}-\boldsymbol{r}'}{|\boldsymbol{r}-\boldsymbol{r}'|^{3}} \, dV' $$
- Taking the _divergence_ of both sides:
$$\nabla_{\boldsymbol{r}}\cdot \boldsymbol{g}=-G\int \rho(\boldsymbol{r}')\nabla_{\boldsymbol{r}}\cdot\left( \frac{1}{|\boldsymbol{r}-\boldsymbol{r}|^{2}} \right) \, dx $$
- This gives a _delta function_

- This then gives _Poisson's equation_:
$$\nabla\cdot \boldsymbol{g}=-\nabla^{2}\Psi=-4\pi G\rho$$
- In the _integral form_, using the divergence theorem:
$$\int \boldsymbol{g}\cdot \, d\boldsymbol{S}=-4\pi GM $$
- For a _spherically symmetric mass distribution_, where the _mass enclosed_ at radius $r$ is $M(r)$:
$$\boldsymbol{g}(r)=-\frac{GM(r)}{r^{2}}\hat{\boldsymbol{r}}$$
- In _galaxies_, from measuring velocity from _Doppler shift_, one can infer the _mass distribution_
	- Discovery of _dark matter_

## Potential of a spherically symmetric system
$$\boldsymbol{g}(r)=-\frac{G}{r^{2}}\int _{0}^{r}4\pi r'^{2}\rho(r') \, dr' =-\frac{d\Psi}{dr}$$
- Assuming $\Psi(r\to \infty)=0$, this gives:
$$\Psi(r)=\int_{\infty}^{r} \frac{G}{r''^{2}} \left[\int_{0}^{r''} 4\pi r'^{2}\rho(r') \, dr'\right]\,  dr'' $$
- The integrating _by parts_, given $M(r)/r\to 0$ as $r\to \infty$
$$\Psi(r)=-\frac{GM(r)}{r}+\int _{\infty}^{r}4\pi Gr'\rho(r') \, dr' $$
- Hence, the potential _is also influenced by matter outside_ $r$
	- The potential between two points _inside_ $r$ is still the _same_
- Having material _outside_ means it takes _more work_ to _remove_ a mass to _infinity_
	- Second term is _negative_

## Gravitational potential energy
- The _gravitational potential energy_ of a system is the energy required to _take all particles apart to_ $\infty$
- This is given by:
$$\Omega=-\frac{1}{2}\sum_{j\neq i}\sum_{i}\frac{GM_{i}M_{j}}{\left| \boldsymbol{r}_{i}-\boldsymbol{r}_{j} \right| }=\frac{1}{2}\sum_{j}M_{j}\Psi_{j}$$
- The factor of $1/2$ _avoids double counting_

- For a _continuous mass distribution_, this gives:
$$\Omega=\frac{1}{2}\int \rho(\boldsymbol{r}) \Psi(\boldsymbol{r})\, dV $$

- For a _spherically symmetric case_:
$$\Omega=\frac{1}{2}\int_{0}^{\infty} 4\pi r^{2}\rho(r)\Psi(r) \, dr=\frac{1}{2}\int_{0}^{\infty} \Psi(r) \, dM $$
- Integrating by parts, both _boundary terms vanish_:
$$\Omega=-\frac{1}{2}\int_{0}^{\infty}M(r) \frac{d\Psi}{dr} \, dr $$
- Using the formula for a _spherically symmetric gravitational force_, then _integrating by parts again_:
$$\Omega=-G\int _{0}^{\infty}\frac{M(r)}{r} \, dM $$
- This corresponds to _peeling_ the system in _shells_

## Virial theorem
- Consider a gravitating system of _many particles_, where each particle experiences _force_:
$$m_{i} \frac{d^{2}\boldsymbol{r}_{i}}{dt^{2}}=\boldsymbol{F}_{i}$$
- Consider the _second time derivative_ of the _moment of inertia_:
$$\frac{1}{2}\frac{d^{2}}{dt^{2}}(m_{i}r_{i}^{2})=\boldsymbol{r}_{i}\cdot \boldsymbol{F}_{i}+m_{i}\left( \frac{d\boldsymbol{r}_{i}}{dt} \right)^{2}$$
- By _summing over all masses_:
$$\frac{1}{2}\frac{d^{2}I}{dt^{2}}=2T+\sum_{i}(\boldsymbol{r}_{i}\cdot \boldsymbol{F}_{i})$$
- The sum is known as the _virial_

 - In the absence of _external forces_, the force on a particle $\boldsymbol{F}_{i}$ is the _sum_ of forces from _all other particles_ $\boldsymbol{F}_{ij}$
 - From Newton's 3rd law:
$$\boldsymbol{F}_{ji}=-\boldsymbol{F}_{ij}$$
- The _virial_ is then:
$$\sum_{i}(\boldsymbol{r}_{i}\cdot \boldsymbol{F}_{i})=\sum_{i}\sum_{j>i}\boldsymbol{F}_{ij}\cdot(\boldsymbol{r}_{i}-\boldsymbol{r}_{j}) $$
- If there are _only gravitational interactions_, the virial is _equivalent_ to the _total gravitational potential energy_
$$\sum_{i}(\boldsymbol{r}_{i}\cdot \boldsymbol{F}_{i})=-\sum_{i}\sum_{j>i}\frac{Gm_{i}m_{j}}{r_{ij}}=\Omega$$
- Therefore:
$$\frac{1}{2} \frac{d^{2}I}{dt^{2}}=2T+\Omega$$
- If the system is in a _steady state_:
$$2T+\Omega=0$$

- The kinetic energy is determined by _temperature_ and _local fluid flows_
- Hence, the _gravitational potential_ will _determine temperature and velocity dispersion of the system_

- The _total energy_ of a system:
$$E_\text{tot}=T+\Omega=-T$$
- As a system _loses energy_, it can tend to become _hotter_

# Equations of state and energy
- The conservations of [[#Conservation of mass|mass]] and [[#Conservation of momentum|momentum]] solve for 4 _degrees of freedom_ given a set of boundary conditions:
$$\displaylines{\frac{\partial \rho}{\partial t}+\nabla\cdot(\rho \boldsymbol{u})=0  \\ \rho \frac{D\boldsymbol{u}}{Dt}=-\nabla p-\rho \nabla \Psi}$$

- In order to solve for _density_ $\rho(\boldsymbol{r},t)$, _pressure_ $p(\boldsymbol{r},t)$, and _velocity distribution_ $\boldsymbol{u}(\boldsymbol{r},t)$, there must be another equation to _solve for_ these degrees of freedom
	- The _gravitational potential_ $\Psi$ is already given by [[#Poisson's equation]] $\nabla^{2}\Psi=-4\pi G\rho$

- This is the _equation of state_

- For an _ideal gas_:
$$p=p(\rho,T)=nk_{B}T=\frac{k_{B}}{\mu m_{p}}\rho T$$
- Here, $\mu$ is the _mean molecular mass_ in terms of proton mass
- This introduces an _extra degree of freedom_ in the form of scalar field $T(\boldsymbol{r},t)$

## Barotropic fluids
- A _barotropic fluid_ is one where pressure is _purely dependent on density_:
$$p=p(\rho)$$
- Example: _electron degeneracy pressure_ $p\propto \rho^{5/3}$ (e.g. in _white dwarfs_)

- Or, if a system is _isothermal_:
$$p=\frac{k_{B}T}{\mu m_{p}}\rho=\text{const.}$$
- Valid when a system has _strong heating and cooling processes_ keeping temperature in balance

- Or, for some [[Classical Thermodynamics#Adiabatic expansion|adiabatic system]] (where all thermodynamic changes are _reversible_):
$$p=K\rho^{\gamma}$$
- Here $K$ is some constant based on _initial conditions_
- A fluid is _isentropic_ if _all fluid elements_ obey the above with the _same value_ of $K$

## Conservation of energy
- Consider the [[Classical Thermodynamics#The first law, internal energy, and heat|first law of thermodynamics]], applied to a _fluid element_:
$$d\hspace{-0.04em}\bar{}\hspace{0.1em}Q=d\mathcal{E}+pdV$$
- Here, $\mathcal{E}$ is the _internal energy_, and $W\equiv-pdV$ is the _work done_ on the gas
- Let all quantities be _per unit mass_

- Rates of change _in the fluid element_:
$$\frac{D\mathcal{E}}{Dt}=\frac{DW}{Dt}+\frac{d\hspace{-0.04em}\bar{}\hspace{0.1em}Q}{dt}$$
- Express $DW/Dt$ in terms of $p$ and $\rho$:
$$\frac{DW}{Dt}=-p\frac{D}{Dt}\left( \frac{1}{\rho} \right)=\frac{p}{\rho^{2}}\frac{D\rho}{Dt}$$
- Let there be a _cooling rate per unit mass_ $\dot{Q}_\text{cool}$:
$$\frac{d\hspace{-0.04em}\bar{}\hspace{0.1em}Q}{dt}=-\dot{Q}_\text{cool}$$
- The first law is then:
$$\frac{D\mathcal{E}}{Dt}=\frac{p}{\rho^{2}}\frac{D\rho}{Dt}-\dot{Q}_\text{cool}$$
- The _total energy per unit volume_ is:
$$E=\rho\left( \frac{1}{2}|\boldsymbol{u}|^{2}+\Psi+ \mathcal{E}\right)$$
- From applying the above:
$$\frac{DE}{Dt}=-(E+p)\nabla\cdot \boldsymbol{u}-(\boldsymbol{u}\cdot \nabla)p+\rho \frac{\partial \Psi}{\partial t}-\rho \dot{Q}_\text{cool}$$
- Expanding the convective derivative:
$$\frac{\partial E}{\partial t}+\nabla\cdot [(E+p)\boldsymbol{u}]=\rho \frac{\partial \Psi}{\partial t}-\rho \dot{Q}_\text{cool}$$
- In most cases, $\Psi$ is only a _function of position_
- If there is also _no cooling_, the _changes in energy density_ are given by the divergence of _enthalpy flux_ $(E+p)\boldsymbol{u}$

## Heating and cooling processes
- The $\dot{Q}_\text{cool}$ term describes _local heating $(\dot{Q}_\text{cool}<0)$ or cooling $(\dot{Q}_\text{cool}>0)$ processes_
### Cooling by radiation
- Energy is carried away from the fluid by _photons_

- This can arise from _recombination_ of ionised gases
- Or, the gas can undergo _free-free emission_, as _free electrons_ are _accelerated_ in the electric fields of ions:
	- A case of Bremsstrahlung
$$L_\text{ff}\propto n_{e}n_{p}T^{1/2}$$
- _Collisions_ between electrons and atoms in the _ground state_ can produce an _excited atomic state_ that _emits_ a photon of energy $\chi$:
	- Hydrogen cannot be excited, so this typically happens through _trace species_
$$L_\text{c}\propto n_{e}n_\text{ion}\exp\left( -\frac{\chi}{k_{B}T} \right)\frac{\chi}{\sqrt{ T }}$$

- These are all _two-body interactions_, with $L\propto \rho^{2}f(T)$ (per _unit volume_)
- Hence, the rate _per unit mass_ $\dot{Q}_\text{cool}\propto \rho f(T)$

- In both processes, $f(T)$ follows a _power law_ $T^{\alpha}$
### Heating by cosmic rays
- _Cosmic rays_ bring in _external, high-energy_ (relativistic) _particles_
- These particles _diffusing_ through the fluid will _heat_ the fluid and facilitate _energy transport_
- They _ionise_ atoms in fluid, with _excess energy_ in the electrons which then end up _heating_ the fluid locally
- The ionisation rate _per unit volume_ is $\propto$ $H\rho$
- $H$ is the _cosmic ray flux_

- Combined with radiation cooling, this gives $\dot{Q}_\text{cool}$:
$$\dot{Q}_\text{cool}=A\rho T^{\alpha}-H$$

- Heating can also be _internal_, due to _energy dissipation_ in _shocks_ or _viscosity_
## Energy transport processes
- Transport processes _move energy through the fluid_

- _Thermal conduction_ is facilitated by fast-travelling particles travelling from hotter to cooler regions
- Typically facilitated by _electrons_
	- Conduction by _ions_ is typically _smaller_ as they are more _massive_
	- The ion flux is _smaller_ by $\sqrt{ m_\text{ion}/m_\text{e} }\sim 40$

- The _energy flux_ per unit area is given by:
$$\boldsymbol{F}_\text{cond}=-\kappa \nabla T$$
- The rate of change of _energy density per unit volume_:
$$-\nabla\cdot \boldsymbol{F}_\text{cond}=\kappa \nabla^{2}T$$
- This is typically relevant in the _interior_ of white dwarfs, _supernova shock fronts_, and ICM (intracluster medium) _plasma_

- _Convection_ is transport due to _circulating flows_ due to an _entropy gradient_
- Typically relevant in _cores of massive stars_, or _planet interiors_

- _Radiation transport_ is relevant in _optically thick_ systems (where the _photon mean free path_ is much _shorter_ than the characteristic length scale)
- If _scattering opacity_ is large, then one gets _radiative diffusion_
- Given _radiation density_ $\epsilon _\text{rad}$, the _radiative flux_ is:
$$\boldsymbol{F}_\text{rad}\propto-\nabla\epsilon _\text{rad}$$
![[star energy transport zones.png|400]]