
# Electrodynamics and Maxwell's Equations

## Fields and charges
- In _free space_, one can define the [[Electromagnetism#The electrostatic force and field|electric field]] $\bm{E}(\bm{r})$ and [[Electromagnetism#The Lorentz Force and the Biot-Savart Law|magnetic flux density]] $\bm{B}(\bm{r})$
- The [[Electromagnetism#The Lorentz Force and the Biot-Savart Law|Lorentz force]] on a _point charge_ $q$ moving with _velocity_ $\bm{v}$:
$$\bm{F}=q(\bm{E}+\bm{v}\times\bm{B})$$
	- $\bm{E}$ gives force _per unit charge_
	- $\bm{B}$ gives force _per unit current_

- In general, there is some _charge distribution_ in space, with _total charge density_ $\rho_T(\bm{r})$
- There can also be some _current distribution_ with _total current density_ $\bm{J}_T(\bm{r})$
- The _conservation of charge_ leads to _continuity_:
$$\displaylines{\int_S \bm{J}_T\cdot d\bm{S}=-\frac{d}{dt}\int_V \rho_T\,\,dV \\ \nabla\cdot\bm{J}_T=-\pd{\rho_T}{t}}$$
- From _experimental observations_, in _vacuum_, the fields obey [[Electromagnetism#Maxwell's equations|Maxwell's Equations]]:
$$\displaylines{\nabla\cdot\bm{E}=\frac{\rho}{\epsilon_0} \\ \nabla\times\bm{E}=-\pd{\bm{B}}{t}\\\nabla\cdot\bm{B}=0\\\nabla\times\bm{B}=\mu_0\bm{J}+\mu_0\epsilon_0\pd{\bm{E}}{t}}$$
- This implies that $\bm{E}$ and $\bm{B}$ are _dependent on each other_
	- The extra terms are the _inductive_ and _displacement_ current terms
## Statics
- In the _electrostatic_ and _magnetostatic_ regimes, $\partial\bm{E}/\partial t=\partial\bm{B}/\partial t=0$
- In _electrostatics_, $\bm{E}$ is _conservative_, as $\nabla\times\bm{E}=0$, hence one can define an _electrostatic potential_:
$$\bm{E}=-\nabla\phi(\bm{r})$$
- In _magnetostatics_, in _regions where_ $\bm{J}_T=0$, one can define a _magnetic scalar potential_:
$$\bm{B}=-\mu_0\nabla\phi_m(\bm{r})$$

- This combined with the other Maxwell's equations give _Poisson's equation_:
$$\nabla^2\phi=\frac{\rho_T}{\epsilon_0}$$
- Similarly for the magnetic scalar potential:
$$\nabla^2\phi_m=0$$
- In the _static regime_, the two fields are _independent_

## Media
- Assumption:
	- Medium is _continuous_
	- Medium is _linear_ and _isotropic_

- In the presence of a _medium_, $\bm{E}$ and $\bm{B}$ can _induce electric/magnetic dipoles_
- Define _dipole moments per unit volume_ $\bm{P}(\bm{r})$ and $\bm{M}(\bm{r})$

- The _electric polarisation_ $\bm{P}$ gives the _surface/volume charge densities_:
$$\sigma_P=\bm{P}\cdot\hat{\bm{n}} \hspace{1.5cm} \rho_P=-\nabla\cdot\bm{P}$$
- If $\bm{P}$ is _time-dependent_, there is an associated _volume current density_:
$$\nabla\cdot\bm{J}_P=-\dot{\rho}_P=\nabla\cdot\dot{\bm{P}}\Longrightarrow \bm{J}_P=\dot{\bm{P}}$$

- Meanwhile, the _magnetisation_ $\bm{M}$ gives _surface/volume current densities_:
$$\bm{J}_M=\nabla\times\bm{M}\hspace{1.5cm}\bm{j}_M=\bm{M}\times\hat{\bm{n}}$$

- The _total charge and current volume distributions_ give:
$$\displaylines{\rho_T=\rho+\rho_P=\rho-\nabla\cdot\bm{P} \\ \bm{J}_T=\bm{J}+\bm{J}_P+\bm{J}_M=\bm{J}+\dot{P}+\nabla\times\bm{M}}$$
- One then defines the _auxiliary fields_:
$$\displaylines{\bm{D}=\epsilon_0\bm{E}+\bm{P} \\ \bm{H}=\frac{1}{\mu_0}\bm{B}-\bm{M}}$$

- In _media_, this gives _another set of Maxwell's equations_:
$$\displaylines{\nabla\cdot\bm{D}=\rho\\\nabla\cdot\bm{B}=0\\\nabla\times\bm{E}=-\pd{\bm{B}}{t}\\\nabla\times\bm{H}=\bm{J}+\pd{\bm{D}}{t}}$$

- In _linear, isotropic media_, one can define the _susceptibilities_:
$$\bm{P}=\epsilon_0\chi_e\bm{E} \hspace{1.5cm}\bm{M}=\chi_m\bm{H}$$
- The assumptions mean that the susceptibilities can be treated as _scalars_
- Defining the _relative permittivity/permeability_:
$$\epsilon=1+\chi\hspace{1.5cm}\mu=1+\chi_m$$
- This gives the _constitutive relations_:
$$\bm{D}=\epsilon\epsilon_0\bm{E}\hspace{1.5cm}\bm{B}=\mu\mu_0\bm{H}$$

## Electromagnetic energy
- The [[Electromagnetism#Energy flow in electromagnetic waves|energy]] $U$ stored in the _fields_ in the volume $V$ bounded by surface $S$:
$$U=\int_V\left(\frac{1}{2}\bm{E}\cdot\bm{D}+\frac{1}{2}\bm{B}\cdot\bm{H}\right)\,dV$$
- From Maxwell's equations, one can show:
$$\frac{dU}{dt}=-\int_S(\bm{E}\times\bm{H})\cdot\,d\bm{S}-\int_V\bm{J}\cdot\bm{E}\,dV$$
- The latter term is _dissipative_ due to _work done_
	- There is _no work done by the Lorentz force_

- One can then define the _energy density_ at a point:
$$u=\frac{1}{2}\bm{E}\cdot\bm{D}+\frac{1}{2}\bm{B}\cdot\bm{H}$$
- The _energy flux_ is given by the _Poynting vector_:
$$\bm{N}=\bm{E}\times\bm{H}$$

## The vector potential
- In the _electrodynamic regime_, when the fields are _not conservative_, one must use a _vector potential_:
$$\bm{B}=\nabla\times\bm{A}$$
- From Maxwell's equations (integrating and adding an _integration constant_ with zero curl):
$$\bm{E}=-\dot{\bm{A}}-\nabla\phi$$

## Boundary conditions
- From converting Maxwell's equations to the _integral forms_, one can define the [[Electromagnetism#Inhomogeneous dielectrics and boundary conditions|boundary conditions in media]]

- $\bm{D}_\perp$ is conserved _in the absence of free charges at the interface_
- $\bm{B}_\perp$ and $\bm{E}_{||}$ are _conserved_
- $\bm{H}_{||}$ is conserved _in the absence of free current at the interface_

## Electromagnetic waves
- In regions with $\rho=0$ and $\bm{J}=0$, by taking curls of Maxwell's equations:
$$\nabla^2\bm{E}=\epsilon\epsilon_0\mu\mu_0\ddot{\bm{E}}\hspace{1.5cm} \nabla^2\bm{B}=\epsilon\epsilon_0\mu\mu_0\ddot{\bm{B}}$$
- Hence, both fields obey _wave equations_, with the speed $v$:
$$v=\frac{1}{\sqrt{\epsilon\epsilon_0\mu\mu_0}}=\frac{c}{\sqrt{\epsilon\mu}}=\frac{c}{n}\hspace{1.5cm}c=\frac{1}{\sqrt{\epsilon_0\mu_0}}$$
- $n$ is the _refractive index_ of the material

- One can then substitute _harmonic solutions_:
$$\bm{E}=\bm{E}_0\exp[i(\bm{k}\cdot\bm{r}-\omega t)]\hspace{1.5cm}\bm{B}=\bm{B}_0\exp[i(\bm{k}\cdot\bm{r}-\omega t)]$$
- $\bm{E}_0$ and $\bm{B}_0$ can be _complex_ to include a _phase difference_
- The wave-vector can also be _complex_ $(\bm{k}+i\bm{\kappa})$ for a _damped wave_
	- The imaginary part takes care of the _damping_
	- Homogeneous/inhomogeneous depending on if $\bm{k}||\bm{\kappa}$

- If there are _no free charges or currents_, from _Maxwell's equations_:
$$\displaylines{\bm{k}\cdot\bm{D}=\bm{k}\cdot\bm{B}=0 \\ \bm{k}\times\bm{E}=\omega\bm{B} \\ \bm{k}\times\bm{H}=-\omega\bm{D}}$$
- For _real_ fields and _real_ $\bm{k}$:
$$\bm{B}\perp\bm{k},\; \bm{B}\perp\bm{E},\; \bm{D}\perp\bm{k},\; \bm{D}\perp\bm{H}$$

- For _isotropic materials_, $\bm{D}||\bm{E}$ and $\bm{B}||\bm{H}$ since $\epsilon$ and $\mu$ are _scalars_
- Then $(\bm{E},\bm{H},\bm{k})$ form a _right-handed set of mutually perpendicular vectors_
- Then $\bm{E}\times\bm{H}=\bm{N}||\bm{k}$, forming a _transverse EM wave_
- The _ratio of strengths_:
$$\frac{|\bm{E}|}{|\bm{H}|}=\frac{c}{n}$$
