- Phenomena related to _transport via gases_
- Viscosity: _momentum_ transport
- Thermal conductivity: _heat_ transport
- Diffusion: _particle_ transport

- The essential _approximations_:
$$L>>\lambda>>d$$
- $L$: _container size_, so the _scale_ of the flow is much larger than the mean free path
- $d$: _molecule diameter_, to avoid _intermolecular interactions_

- All formulas are derived _with this set of assumptions_

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
- As molecules _arrive at a layer_ of bulk speed $\mean{u_x}$, they are _thermalised_ to have that speed in the $x-$direction
- As they then travel in the $+z$ direction, they _move from a layer of lower $\mean{u_x}$ to one of higher $\mean{u_x}$_, hence there is _net momentum transfer_ in the $-x$ direction to the upper layer
	- Similar, one travelling in the $-z$ direction has the opposite effect
- Therefore there is some _momentum flux_ $\Pi$ which is _opposite to the velocity gradient_, with a magnitude equal to $\tau_{xz}$:
$$\Pi_z=-\eta\pd{\mean{u_x}}{z}$$

## Viscosity of a gas
- Consider molecules travelling at some angle $\theta$ to the $z-$axis at a particular _plane of interest_:
$$dN=v\cos\theta\,f(v)dv\,\frac{1}{2}\sin\theta d\theta$$
- Since the last collision, the particle has travelled $\lambda\cos\theta$ in the $z-$direction
- The _transfer of momentum_ is then:
$$\Delta p=$$
- Viscosity is then given by:
$$\eta=\frac{1}{3}nm\lambda\mean{v}$$

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

# Particle diffusion
- Consider a _distribution_ of _identical molecules_ in one dimension, with $n(z)$ molecules _per unit volume_
- They will tend to _diffuse_ through the container
- The _flux_ of molecules is given by:
$$\Phi_z=-D\pd{n}{z}$$
- $D$ is known as the _diffusion coefficient_
- In three dimensions, _Fick's First Law_ gives:
$$\bm{\Phi}=-D\nabla n$$
- From KINETIC THEORY PROOF
$$D=\frac{1}{3}\lambda\mean{v}$$

- $D$ is _inversely proportional_ to pressure, and hence also _inversely proportional_ to $n$
- $D$ is proportional to $T^{3/2}$ 

- For a _mixture_ of two molecules, replace $\sigma$, and also use the _reduced mass_ $\mu'$:
$$\sigma=\pi(a_1+a_2)^2 \hspace{1cm} \mu=\frac{2m_1m_2}{(m_1+m_2)^2}$$

# Heat/diffusion equation
- Consider equations obeyed by _heat flux_ $\bm{J}$ and _particle flux_ $\bm{\Phi}$:
$$\displaylines{\bm{J}=-\kappa\nabla T \\ \bm{\Phi}=-D\nabla n}$$
- Considering _particles through a closed surface $S$_, the _total loss of particles_ is:
$$\iint_S\bm{\Phi}\cdot d\bm{S}=-\pd{}{t}\iiint n\,dV$$
- By using the [[Vector calculus in 3-dimensions#Divergence Theorem|Divergence Theorem]]:
$$\pd{}{t}\iiint n\,dV=-\iiint \nabla\cdot\bm{\Phi}\,dV$$
- By substituting Fick's First Law:
$$\pd{n}{t}=D\nabla^2n$$
- Similarly, for _heat_:
$$\displaylines{\pd{T}{t}=D\nabla^2T \\ D=\frac{\kappa}{C}}$$
- [[Partial differential equations|How to solve the damn things]]
- By assuming a _separable solution_:
$$\displaylines{T(\bm{r},t)=P(\bm{r})\tau(t) \\ \nabla^2P=-\frac{\alpha}{D}P \hspace{1cm} \frac{d\tau}{dt}=-\alpha \tau}$$
- By looking for _plane wave solutions_ to $P$, and writing a linear combination of solutions:
$$\displaylines{T(\bm{r},t)=\sum_k P_{0,k} \exp(i\bm{k}\cdot\bm{r})\exp(-k^2Dt) \\ k^2=\frac{\alpha}{D}}$$
- Here, the values of $k$ and $P_{0,k}$ are defined by the _boundary conditions_

- At _longer times_, the solution becomes _dominated_ by the _longest wavelength components_

## Oscillating boundary conditions and the skin depth
- In 1D, look for solutions _periodic in time_ with frequency $\omega$
- Therefore:
$$-k^2D=i\omega \Longrightarrow k=\pm(1+i)\sqrt{\frac{\omega}{2D}}$$
- Hence, the spatial part will _diverge_ in certain limits

- If there is an _oscillating temperature_ at $x=0$, looking for solutions for $x>0$:
$$T(x,t)=\sum_\omega \exp(i\omega t)\exp\left[(i-1)\sqrt{\frac{\omega}{2D}}x\right]$$
- If there is only _one frequency_, let the boundary conditions be:
$$T(0,t)=T_0+\Delta T\cos(\Omega t)$$
$$T(x,t)=T_0+\Delta T\exp(-\frac{x}{\delta})\cos\left(\Omega t-\frac{x}{\delta}\right)$$
- Here, $\delta$ is the _skin depth_, which is _inversely proportional_ to $\sqrt{\Omega}$
- Hence, _higher frequencies cannot penetrate far_
- There is also a _phase shift_ in the spatial oscillations compared to those in time