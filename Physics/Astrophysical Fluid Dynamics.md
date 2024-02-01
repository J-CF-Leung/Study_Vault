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

- The _internal energy_ for the ideal gas can be written as:
$$\mathcal{E}=\frac{1}{\gamma-1} \frac{p}{\rho}$$
- Here, $\gamma$ is the _adaibatic constant_, or the _ratio of heat capacities_
## Barotropic fluids
- A _barotropic fluid_ is one where pressure is _purely dependent on density_:
$$p=p(\rho)$$
- Example: _electron degeneracy pressure_ $p\propto \rho^{5/3}$ (e.g. in _white dwarfs_)

- Or, for an _isothermal ideal gas_:
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

# Hydrostatic equilibrium
- [[#Fluid equations|Conservation of mass and momentum]]:
$$\displaylines{\frac{\partial \rho}{\partial t}+\nabla\cdot(\rho \boldsymbol{u})=0 \\ \rho \frac{D\boldsymbol{u}}{Dt}=-\nabla p+\rho \boldsymbol{g}}$$
- [[#Gravitation|Poisson's Equation]]:
$$\nabla^{2}\Psi=4\pi G\rho$$
- The _total energy_ in a fluid:
$$E=\rho\left( \frac{1}{2}u^{2}+\Psi+\mathcal{E} \right)$$
- [[#Conservation of energy]]:
$$\frac{\partial R}{\partial t}+\nabla\cdot[(E+p)\boldsymbol{u}]=\rho \frac{\partial \Psi}{\partial t}-\rho \dot{Q}_\text{cool}$$
- The _equation of stater_ and _internal energy_ for an [[#Barotropic fluids|ideal gas]]:
$$p=\frac{k_{B}}{\mu m_{p}}\rho T\hspace{1.5cm}\mathcal{E}=\frac{1}{\gamma-1} \frac{p}{\rho}$$
## Condition of equilibrium
- A fluid is in _hydrostatic equilibrium_ if:
$$\boldsymbol{u}=0 \hspace{1.5cm}\frac{\partial f}{\partial t}=0\;,\;\forall f$$
- From this, the _continuity equation_ is _automatically satisfied_

- Conservation of momentum gives:
$$\frac{1}{\rho}\nabla p=\boldsymbol{g}=-\nabla \Psi$$
- Example: _isothermal atmosphere_ has $p\propto \rho$, and an _exponential profile_

- If a system is _self-gravitating_ (no external field):
$$\nabla^{2}\Psi=4\pi G\rho$$
- This must be _solved along with_ the equation for hydrostatic equilibrium

## Stars as self-gravitating polytropes
- Consider a _star_ as a _spherically symmetric_, _self-gravitating_ system in _hydrostatic equilibrium_:
$$\frac{dp}{dr}=-\rho \frac{d\Psi}{dr}$$
- This gives:
$$\rho=-\frac{dp}{d\Psi}$$
- As $\rho>0$ for matter in a star, it is a _monotonic function of_ $\Psi$
- One can also _invert_ $p=p(\Psi)$ to get that:
$$p=p(\rho)$$
- Therefore, _non-rotating stars_ are [[#Barotropic fluids|barotropes]]

- A barotropic _equation of state_:
$$p=K\rho^{1+1/n}$$
- In general, $n=n(\rho)$
- For $n$ _constant_, the fluid is _polytropic_, and the star is a _polytrope_
	- Typically a good approximation for stars

- $1+1/n \neq\gamma$, as the star _is not necessarily isentropic_
	- _Convective motions_ means fluid elements are _not thermally isolated_

## Lane-Emden equation
- The equation of hydrostatic equilibrium then gives:
$$-\nabla \Psi=(n+1)\nabla(K\rho^{1/n})\implies \rho=\left( \frac{\Psi_{T}-\Psi}{[n+1]K} \right)^{n}$$
- Here, $\Psi_{T}\equiv \Psi$ on the _surface_, where $\rho=0$

- Let there be a _central density_ $\rho_{c}$ and _central potential_ $\Psi_{c}$:
$$\rho=\rho_{c}\left( \frac{\Psi_{T}-\Psi}{\Psi_{T}-\Psi_{c}} \right)^{n}\equiv \rho_{c}\theta^{n}$$
- Feeding into _Poisson's equation_:
$$\nabla^{2}\theta=\frac{1}{r^{2}} \frac{d}{dr}\left( r^{2} \frac{d\theta}{dr} \right)=-\frac{4\pi G\rho_{c}}{\Psi_{T}-\Psi_{c}}\theta^{n}$$
 - Defining a _scaled radial coordinate_ $\xi=r\sqrt{ (4\pi G\rho_{c})/(\Psi_{T}-\Psi_{c}) }$:
$$\frac{1}{\xi^{2}} \frac{d}{d\xi}\left( \xi^{2} \frac{d\theta}{d\xi} \right)=-\theta^{n}$$
- This is the _Lane-Emden equation_ of index $n$

- Typical boundary conditions have:
$$\theta(\xi\to 0)=1 \hspace{1.5cm} \frac{d\theta}{d\xi}(\xi\to 0)=0$$
- There is _zero force_, and _no enclosed mass_ as $\xi\to 0$

- It can be solved _analytically_ for $n=0,1,5$

### Constant density, incompressible
- The _constant density_, _incompressible_ case corresponds to $n=0$:
$$\frac{1}{\xi^{2}} \frac{d}{d\xi}\left( \xi^{2} \frac{d\theta}{d\xi} \right)=-1$$
- With the _boundary conditions_:
$$\theta=1-\frac{\xi^{2}}{6}$$
## Isothermal sphere
- The _isothermal_ case has $n\to \infty$:
	- The Lane-Emden equation _cannot be applied_
$$p=K\rho\implies \frac{d\Psi}{dr}=-\frac{K}{\rho} \frac{d\rho}{dr}$$
- With the appropriate boundary conditions:
$$\Psi-\Psi_{c}=-K\ln \frac{\rho}{\rho_{c}}$$
- Using _Poisson's equation_:
$$\frac{K}{r^{2}} \frac{d}{dr} \left( r^{2} \frac{1}{\rho} \frac{d\rho}{dr} \right)=-4\pi G\rho$$
- By _defining_ $\Psi_{c}=0$:
$$\rho=\rho_{c}\exp(-\Psi)$$
- Set:
$$r=a\xi \hspace{1cm}a=\sqrt{ \frac{K}{4\pi G\rho_{c}} }$$
- One then gets:
$$\frac{1}{\xi^{2}} \frac{d}{d\xi} \left( \xi^{2} \frac{d\Psi}{d\xi} \right)=\exp(-\Psi) $$
- With the typical boundary conditions $\Psi=d\Psi/d\xi=0$ at $\xi=0$

- At _large radii_, $\rho \propto r^{-2}$ and $M(r)\propto r$
	- Therefore, one cannot have $\Psi(\xi\to \infty)=0$
- _Physical solutions_ must be _truncated_ at a large radius, hence _confined_ by some finite external pressure
- These are known as _Bonnor-Ebert spheres_, with density profile determined by $\xi _\text{cut}$

## Scaling relations
- One can consider _families_ of stars with a given _polytropic index_ $(n)$
- For a _monoatomic ideal gas_, $n=3/2$

### Polytropic stars
- Consider a set of stars sharing index $n$ with given constant $K$
- They then form a _one-parameter family_ characterised by $\rho_{c}$

- Then _relating_ mass and radius with $\rho_{c}$ gives _scaling relations_

- All stars with a _given_ $n$ have the same _profile_ $\theta(\xi)$ as they have the _same solution_ to the Lane-Emden equation

- Relations

- The surface
- The mass:
$$M=\int _{0}^{r_\text{max}}r\pi r^{2}\rho \, dr= $$
- This gives:
$$M\propto \rho_{c}^{(3/n-1)/2}$$
- From the definition of $\xi$:
$$r_{max} \propto \rho_{c}^{(1/n-1)/2}$$
- Eliminating $\rho_{c}$:
$$M\propto R^{(3-n)/(1-n)}$$
- This is the _mass-radius relation for polytropic stars_

- For $n=3/2$, this gives $M \propto R^{-3}$
- So, _larger_ stars are smaller
	- Seen in _smaller white dwarfs_
- For more _massive_ white dwarfs, electrons on the _Fermi surface_ become _relativistic_, so that $p \propto \rho^{4/3}$, and mass is _independent of radius_
	- This is the _Chandrasekar mass_
	- Type-1a supernovae will _collapse at the Chandrasekar mass_

### Main sequence stars
- For most _main sequence_ stars, $M\propto R$
- This is because they _do not have the same_ $K$
- Using the ideal gas law:
$$T_{c}=\frac{\mu K}{\mathcal{R}_{*}}\rho_{c}^{1/n}$$
- _Nuclear reactions_ typically keep the temperature _constant_ regardless of $\rho_{c}$:
	- Stars in the main sequence have _temperature sensitive_ thermonuclear reactions
$$K\propto \rho^{1/n}$$
- Substituting this into the mass relation:
$$M \propto \rho_{c}^{-1/2} \hspace{1cm}R \propto \rho_{c}^{-1/2}\implies M\propto R$$

### Relative timescales
- Whether $K$ or $T_{c}$ are constant depends on the _relative timescales_, as _changes in mass_ causes re-adjustment of nuclear processes
- _Hydrostatic_ equilibrium $(K=\text{const.})$ depends on the _sound-crossing timescale_:
$$\tau _\text{sound}\sim \frac{R}{C_{s}}$$
- The _energy_ of the core typically _re-adjusts_ after the addition of mass, with the _thermal timescale_ (with _luminosity_ $L$)
$$\tau _\text{th}=\frac{GM^{2}}{RL}$$
- For the _Sun_, it approaches $\tau _\text{sound}\approx 1\text{ day}$ and $\tau _\text{th}\approx 30\text{ Myr}$
- Therefore, a _mass loss/gain_ is followed by _rapid hydrostatic equilibriation_ and thermal equilibrium takes a _long time_

### Application: rotating spherical star
- When _non-rotating mass_ is added to a _rotating polytropic star_ with angular velocity $\Omega$, on _less than thermal timescale_, from _conservation_ of angular momentum:
$$\frac{\Delta\Omega}{\Omega}=-\frac{\Delta(MR^{2})}{MR^{2}}$$
- Apply scaling relation

### Application: close binary systems
- Stars in _close binary systems_ can _lose mass_ to companions
- If $\Delta M<0$
- Radius can _increase_ for $1<n<3$
- Then, _runaway mass transfer_ can occur
	- Also depends on _orbital configuration_
	- There is a _critical equipotential_
- Example: X-ray binaries

# Sound waves, supersonic flows, shock waves
- _Disturbances_ often occur in a medium
- They propagate via _waves_

## Sound waves
- Consider a _uniform medium_ with no gravitation

- Start from the fluid equations:
$$\displaylines{\frac{\partial \rho}{\partial t}+\nabla\cdot(\rho \boldsymbol{u})=0 \\ \frac{\partial \boldsymbol{u}}{\partial t}+(\boldsymbol{u}\cdot \nabla)\boldsymbol{u}=-\frac{1}{\rho}\nabla p}$$
- Let there be a _perturbation_ around the state $\rho=\rho_{0}$, $p=p_{0}$, $\boldsymbol{u}=0$:
$$\rho=\rho_{0}+\Delta \rho \hspace{1cm}p=p_{0}+\Delta p \hspace{1cm}\boldsymbol{u}=\Delta \boldsymbol{u}$$
- It is a _Lagrangian perturbation_, as it _follows a fluid element_
- It is related to the _Eulerian_ perturbation $\delta \rho$ by:
	- $\boldsymbol{\xi}$ is the _fluid element displacement_
$$\delta \rho=\Delta p-(\boldsymbol{\xi}\cdot \nabla)\rho_{0}$$
- In this case, there is _no difference_

- Introducing the perturbation into the continuity equation:
$$\frac{\partial}{\partial t} (\Delta \rho)+\rho_{0}\nabla\cdot(\Delta \boldsymbol{u})=0$$
- Similarly, the momentum equation, assuming a _barotropic_ equation of state:
$$\frac{\partial}{\partial t}(\Delta u)=-\frac{dp}{d\rho}\Bigg|_{\rho=\rho_{0}} \frac{\nabla(\Delta \rho)}{\rho_{0}}$$
- Taking a _time derivative_ of the first equation:
$$\frac{\partial^{2}}{\partial t^{2}}(\Delta \rho)=\frac{dp}{d\rho}\Bigg|_{\rho=\rho_{0}}\nabla^{2}(\Delta \rho)$$
- This admits _plane wave solutions_ of the form:
$$\Delta \rho=\Delta \rho_{0}\exp[i(\boldsymbol{k}\cdot \boldsymbol{x}-\omega t)]\hspace{1.5cm}\omega^{2}= \frac{dp}{d\rho}\Bigg|_{\rho=\rho_{0}}k^{2}$$
- The _phase speed_ of the wave:
$$c_{s}=v_{p}=\sqrt{ \frac{dp}{d\rho}\Bigg|_{\rho=\rho_{0}} }$$
- Substituting $\Delta u=\Delta u_{0}\exp[i(\boldsymbol{k}\cdot \boldsymbol{x}-\omega t)]$ into the continuity equation:
$$\Delta u=c_{s}\frac{\Delta \rho}{\rho_{0}}$$
- The disturbances are _in phase_

- Disturbances travel at a _much higher speed than the individual fluid elements_ (for small perturbations):
$$\Delta u\ll c_{s}$$
- The propagation of sound waves is driven by _density perturbations_ giving rise to _pressure gradients_ and _acceleration_, which give rise to _more disturbances_ and propagation continues

- The speed of sound depends on the _linear response_ of _pressure_ to changes in _density_
	- If the material is _stiff_, propagation is _rapid_

- For an _isothermal gas_ and _adiabatic gas_
	- These waves are _non-dispersive_
$$c_{s,I}=\sqrt{ \frac{R_{*}T}{\mu} }\hspace{1.5cm}c_{s,A}=\sqrt{ \frac{\gamma R_{*}T}{\mu} }$$
- This is regarding the structure _of the perturbations_, which is _not necessarily the same as the background_
	- One can have _adiabatic perturbations_ in an _isothermal background_

## Sound waves in a stratified atmosphere
- Consider sound waves in a medium with _background structure_
- An _isothermal atmosphere_ with $\boldsymbol{g}=-g\hat{z}$
- Any _horizontal_ sound waves are _unaffected_ by vertical background structure
- The $z-$dependent terms:
$$\displaylines{\rho}$$
- The _background structure_:
$$\displaylines{\rho_{0}(z)=\tilde{\rho}_{0}\exp\left( -\frac{z}{H} \right) \hspace{1cm} H\equiv \frac{R_{*}T}{g\mu}\\p_{0}(z)=}$$
- Introduce the _perturbations_:
$$\rho=$$
- Relating to Eulerian perturbations:
$$\delta \rho=$$
- The perturbation in velocity:
$$\Delta u=$$
- Substitute into Eulerian continuity equation:
$$\frac{\partial(\Delta \rho)}{\partial t}+\rho_{0}\frac{\partial(\Delta u_{z})}{\partial z}=0$$
- Momentum equation:
$$\frac{\partial}{\partial} \hspace{1cm}c_{u}^{2}\equiv\frac{\partial p}{\partial \rho}\Bigg|_{\rho_{0}}$$
- The wave equation:
$$\frac{\partial^{2}\Delta \rho}{\partial t^{2}}-\rho_{0}\frac{\partial}{\partial z}\left( \frac{c_{u}^{2}}{\rho_{0}}\frac{\partial\Delta \rho}{\partial z} \right)=0$$
- For an _isothermal medium_, $c_{u}$ is _independent of height_, giving:
$$\frac{\partial^{2}\Delta \rho}{\partial t^{2}}-c_{u}^{2}\frac{\partial^{2}\Delta \rho}{\partial z^{2}}+ \frac{c_{u}^{2}}{\rho_{0}}\frac{\partial \rho_{0}}{\partial z} \frac{\partial\Delta \rho}{\partial z}=0$$
- There is an _extra term_ due to the stratification

- For a _plane wave_ $\Delta \rho \propto \exp[i(kz-\omega t)]$:
$$\omega^{2}=c_{u}^{2}\left( k^{2}-\frac{ik}{H} \right)$$
- One can also solve for $k$:
$$k=\frac{i}{2H}\pm \sqrt{ \frac{\omega^{2}}{c_{u}^{2}}-\frac{1}{4H^{2}} }$$
- For $\omega>$
- It is a _travelling wave of decaying amplitude_

- Perturbed velocity and fractional density fluctuation _exponentially increases with height_
- _Without dissipation_, kinetic energy flux thingymajig
- It becomes a _shock wave_

- For $\omega<$
- $k$ is _purely imaginary_, and there is _no travelling wave_
- It is _completely evanescent_, as the properties of the atmosphere _significantly change over one wavelength_
- There are too many _reflections_

## Sound transmission at interfaces
- Consider two _non-dispersive media_ with a _boundary_ at $x=0$
![[Wave at boundary.png|450]]