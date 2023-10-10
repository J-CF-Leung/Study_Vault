
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
- In _electrostatics_, $\bm{E}$ is _conservative_, as $\nabla\times\bm{E}=0$, hence one can define an [[Electromagnetism#The electrostatic potential|electrostatic potential]]:
$$\bm{E}=-\nabla\phi(\bm{r})$$
- In _magnetostatics_, in _regions where_ $\bm{J}_T=0$, one can define a [[Electromagnetism#The magnetic scalar potential|magnetic scalar potential]]:
$$\bm{B}=-\mu_0\nabla\phi_m(\bm{r})$$

- This combined with the other Maxwell's equations give [[Electromagnetism#Laplace's and Poisson's equations|Poisson's equation]]:
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

- The [[Electromagnetism#Polarisation and bound charge density|electric polarisation]] $\bm{P}$ gives the _surface/volume charge densities_:
$$\sigma_P=\bm{P}\cdot\hat{\bm{n}} \hspace{1.5cm} \rho_P=-\nabla\cdot\bm{P}$$
- If $\bm{P}$ is _time-dependent_, there is an associated _volume current density_:
$$\nabla\cdot\bm{J}_P=-\dot{\rho}_P=\nabla\cdot\dot{\bm{P}}\Longrightarrow \bm{J}_P=\dot{\bm{P}}$$

- Meanwhile, the [[Electromagnetism#Surface magnetisation currents|magnetisation]] $\bm{M}$ gives _surface/volume current densities_:
$$\bm{J}_M=\nabla\times\bm{M}\hspace{1.5cm}\bm{j}_M=\bm{M}\times\hat{\bm{n}}$$

- The _total charge and current volume distributions_ give:
$$\displaylines{\rho_T=\rho+\rho_P=\rho-\nabla\cdot\bm{P} \\ \bm{J}_T=\bm{J}+\bm{J}_P+\bm{J}_M=\bm{J}+\dot{P}+\nabla\times\bm{M}}$$
- One then defines the _auxiliary fields_:
$$\displaylines{\bm{D}=\epsilon_0\bm{E}+\bm{P} \\ \bm{H}=\frac{1}{\mu_0}\bm{B}-\bm{M}}$$

- In _media_, this gives [[Electromagnetism#Maxwell's equations|Maxwell's equations in media]]:
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
$$\frac{|\bm{E}|}{|\bm{B}|}=\frac{c}{n}$$
- The _characteristic impedance_:
$$\frac{|\bm{E}|}{|\bm{H}|}=\sqrt{\frac{\mu\mu_0}{\epsilon\epsilon_0}}=Z=\sqrt{\frac{\mu}{\epsilon}}Z_0$$

- If there is _free charge_ present, $\nabla\cdot\bm{D}\neq0$, so $\bm{D}$ and $\bm{E}$ can have _longitudinal components_
- For the case of $\epsilon=0$ (e.g. _plasma_ at _plasma frequency_), $\bm{k}||\bm{E}$

## Linear polarisation
- The _polarisation_ of the wave is the _direction_ of $\bm{E}$ in an electromagnetic wave
	- e.g. $\bm{E}_0=(1,0,0), \bm{B}_0=(0,1,0), \bm{k}=(0,0,1),$ this is "$x-$polarised" 
- If it is _constant_, it is _plane-polarised_

- At _interfaces_, the _reflection_ and _transmission_ are dependent on whether or not the polarisation is _in the plane of incidence_
	- $\perp$ to the plane: $s-$polarisation
	- $//$ to the plane: $p-$polarisation
- One can then use _boundary conditions_ to [[Electromagnetism#Fresnel's relations|derive]] reflection and transmission coefficients:
$$\displaylines{r_{p}=\frac{n_2\cos\theta_1-n_1\cos\theta_2}{n_2\cos\theta_1+n_1\cos\theta_2} \hspace{1.5cm} t_{p}=\frac{2n_1\cos\theta_i}{n_2\cos\theta_i+n_1\cos\theta_t} \\ r_s=\frac{n_1\cos\theta_1-n_2\cos\theta_2}{n_1\cos\theta_1+n_2\cos\theta_2} \hspace{1.5cm} t_s=\frac{2n_1\cos\theta_i}{n_1\cos\theta_i+n_2\cos\theta_t}}$$

- At _normal incidence_, where $\theta_1=0$, $r_p=-r_s$ and $t_p=t_s$
- At _grazing incidence_ where $\theta_1\to\pi/2$, $r_p,r_s=1$
- At _Brewster's angle_ where $\theta_1=\tan^{-1}(n_2/n_1)$, $r_p=0$
	- Used in _polarising devices_

# Optics
- Results typically apply to _wide range of frequencies_, including _non-visible_ spectrum
- At optical frequencies, _magnetic properties are negligible_, hence:
$$n=\sqrt{\epsilon\mu}\to\sqrt{\epsilon}$$

## Polarised light
- A _general_ polarisation state is a _superposition of plane wave solutions_
- Consider two _perpendicular_ plane-polarised waves:
$$\bm{E}_1=\bm{i}a_1E_0\exp[i(kz-\omega t)]\hspace{1cm}\bm{E}_2=\bm{j}a_2E_0\exp[i(kz-\omega t)]$$

- For _real_ $a_1$ and $a_2$, the waves are _in-phase_
- It is a _plane-polarised wave_ at angle $\theta=\tan^{-1}(a_2/a_1)$, with amplitude $E_T=E_0\sqrt{a_1^2+a_2^2}$

- Let there be some _phase difference_ $\delta$
- For $a_1=1$ and $a_2=i=\exp(i\pi/2)$, the second wave _lags_ by $\pi/2$:
$$\bm{E}_2=\bm{j}E_0\exp[i(kz-(\omega_t-\pi/2))]$$
- At $z=0$ and taking the _real parts_:
$$\bm{E}_T(z=0)=E_0\bm{i}\cos(\omega t)+E_0\bm{j}\sin(\omega t)$$
- At $t=0$:
$$\bm{E}_T(t=0)=E_0\bm{i}\cos(kz)-E_0\bm{j}\sin(kz)$$
![[anticlockwise circular polarisation.png]]
- This is a _left-hand circularly polarised wave_
- It is _anti-clockwise_ when looking _towards the source_

- For $a_1=1$ and $a_2=-i$, it is a _right-hand circularly polarised wave_

- For $|a_1|\neq|a_2$ and $\delta\neq\pi/2$, it is _elliptically polarised_
- For $a_1=a$ and $a_2=b\exp(i\delta)$:
$$\frac{E_x^2}{a^2}+\frac{E_y^2}{b^2}-2\cos\delta\frac{E_x}{a}\frac{E_y}{b}=\sin^2\delta$$

- The convention to describe polarisation is using the _Jones vectors_:
$$\displaylines{\text{General elliptical polarisation:}\pmatrix{a\\ b\exp(i\delta)} \\ \bm{L}_x=\pmatrix{1\\0}\hspace{1.5cm}\bm{L}_y=\pmatrix{0\\1}\hspace{1.5cm} \bm{L}_\theta=\pmatrix{\cos\theta\\\sin\theta} \\ \bm{C}_R=\frac{1}{\sqrt{2}}\pmatrix{1\\-i}\hspace{1.5cm}\bm{C}_L=\frac{1}{\sqrt{2}}\pmatrix{1\\ i}}$$
- These only apply when the _phase difference is constant_

- One can form _linear combinations_ of the states
- Example: combine _right-handed_ and _left-handed_ polarisations:
$$\frac{1}{\sqrt{2}}\pmatrix{1\\i}+\frac{1}{\sqrt{2}}\pmatrix{1\\-i}=\sqrt{2}\pmatrix{1\\0}$$

## Anisotropic media
- A _dichroic material_ will _absorb_ light polarised in _one direction more than others_
	- A _wire grid_ will absorb electric fields _parallel_ to the wires due to _energy dissipation_
	- Typical _polaroid films_ have _aligned conducting polymeric chains_

- If a device _absorbs light in the_ $y-$direction, one can represent it via a _Jones matrix_:
$$\displaylines{J_x=\pmatrix{1&0\\0&0}\\J_x\pmatrix{1\\0}=\pmatrix{1\\0}\\J_y\pmatrix{0\\1}=\pmatrix{0\\0}}$$
- For a _transmitting axis_ oriented at $\theta$ to the $x-$axis:
$$J_\theta=\pmatrix{\cos^2\theta&\sin\theta\cos\theta\\\sin\theta\cos\theta&\sin^2\theta}$$
- One can prove that $x-$polarised light passing through the polariser has _intensity_:
$$I=I_0\cos^2\theta$$
- This is _Malus's Law_

- For light passing through _multiple optical elements_ $A,B,C$:
$$J=CBA$$
- This _multiplies the Jones vector in the correct order_
- For _crossed polarisers_:
$$J_\theta J_{\theta+\pi/2}=0$$
## Birefringence
- For _isotropic materials_, $\epsilon$, $\mu$, $\chi_m$ are all _scalars_

- However, natural materials can be _anisotropic_
- Here, the permittivity can be a _second-rank tensor_:
$$\bm{D}=\epsilon_0\dunderline{\epsilon}\cdot\bm{E}\hspace{2cm}D_i=\epsilon_0\epsilon_{ij}E_j$$
- From _energy conservation_, $\dunderline{\epsilon}$ must be _Hermitian_:
$$\epsilon_{ij}=\epsilon_{ji}^*$$
- It therefore is _diagonalisable_ and has _real, orthogonal eigenvectors_
- For _lossless media_, it is _real_ and therefore _symmetric_

- It can therefore have _diagonal entries_ $n_i^2$
- If $n_1\neq n_2\neq n_3$, it is _biaxial_
- If $n_1=n_2\neq n_3$, it is _uniaxial_
	- Convention to have $n_1=n_2$
$$\dunderline{\epsilon}=\pmatrix{n_o^2&0&0\\0&n_o^2&0\\0&0&n_e^2}$$
- $o$ denotes the _ordinary_ directions
- $e$ denotes the _extraordinary_ direction, or the _optic axis_

- The _birefringence_ is:
$$\Delta n=n_e-n_0$$
- _Calcite_ has $\Delta n=-0.172$

- $\bm{D}//\bm{E}$ _if and only if_ $\bm{E}$ is _along the optic axis_, or if it is _perpendicular_ to it
- If this does not apply, the _propagation of energy_ may not be in the direction of wave propagation, or $\bm{N}$ is _not parallel_ to $\bm{k}$
## Waves in anisotropic, non-magnetic materials
- As the material is non-magnetic, $\mu\approx 1$ and $\bm{B}//\bm{H}$, and:
$$\bm{B}\perp\bm{k}\text{ and }\bm{E}\hspace{1.5cm}\bm{D}\perp\bm{k}\text{ and }\bm{H}$$
- Therefore, $\bm{D}$, $\bm{B}$ and $\bm{k}$ are _mutually orthogonal_

- If $\bm{D}$ is along a _principal axis_, then $\bm{E}\times\bm{H}=\bm{N}||\bm{k}$
- It is then the _same as an isotropic medium_