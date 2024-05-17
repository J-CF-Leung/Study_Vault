- [ ] Antennae ⏫📅 2024-03-22 
- [x] Wtf is spatial coherence anyway ⏫ 📅 2024-03-22 ✅ 2024-03-23
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
$$\nabla^2\phi=-\frac{\rho_T}{\epsilon_0}$$
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

## Polarised light and the Jones representation
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
![[Elliptical polarisation.png]]
$$\tan2\alpha=\frac{2ab\cos\delta}{a^2-b^2}$$

- The convention to describe polarisation is using the _Jones vectors_:
$$\displaylines{\text{General elliptical polarisation:}\pmatrix{a\\ b\exp(i\delta)} \\ \bm{L}_x=\pmatrix{1\\0}\hspace{1.5cm}\bm{L}_y=\pmatrix{0\\1}\hspace{1.5cm} \bm{L}_\theta=\pmatrix{\cos\theta\\\sin\theta} \\ \bm{C}_R=\frac{1}{\sqrt{2}}\pmatrix{1\\-i}\hspace{1.5cm}\bm{C}_L=\frac{1}{\sqrt{2}}\pmatrix{1\\ i}}$$
- These only apply when the _phase difference is constant_

- One can form _linear combinations_ of the states
- Example: combine _right-handed_ and _left-handed_ polarisations:
$$\frac{1}{\sqrt{2}}\pmatrix{1\\i}+\frac{1}{\sqrt{2}}\pmatrix{1\\-i}=\sqrt{2}\pmatrix{1\\0}$$

## Anisotropic media and Jones matrices
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

- If $\bm{D}$ is along _any principal axis_, then $\bm{E}\times\bm{H}=\bm{N}||\bm{k}$
- It is then the _same as an isotropic medium_ but with $n$ depending on the axis

- For a _uniaxial material_:
$$\pmatrix{D_x\\D_y\\D_z}=\epsilon_0\pmatrix{\epsilon_1&0&0\\0&\epsilon_1&0\\0&0&\epsilon_3}\pmatrix{E_x\\E_y\\E_z}$$
- As long as $\bm{D}$ is in the $\hat{\bm{e}}_1-\hat{\bm{e}}_2$ _plane_ (meaning $\perp\hat{\bm{e}}_3$), $\bm{D}||\bm{E}$
- Otherwise, $\bm{N}$ is _not necessarily parallel_ to $\bm{k}$

### A geometric approach to wave propagation
- The _energy density_ is proportional to $\bm{D}\cdot\bm{E}$
- For some _fixed_ energy density:
$$\epsilon_0\bm{D}\cdot\bm{E}=\bm{D}\epsilon^{-1}\bm{D}=1$$
- As $\epsilon$ is _diagonalised_, this defines an _ellipsoid_, the _optical indicatrix_:
$$\frac{D_x^2}{\epsilon_1}+\frac{D_y^2}{\epsilon_2}+\frac{D_z^2}{\epsilon_3}=1$$

- For a given $\bm{D}$, the corresponding $\bm{E}$ can be shown to be _normal to the ellipsoid surface_ at the tip of $\bm{D}$

- From Maxwell's equations, $\bm{k}\times\bm{k}\times\bm{E}=-\mu_0\omega^2\bm{D}$
- Letting the angle between $\bm{E}$ and the plane _perpendicular to_ $\bm{k}$ be $\alpha$, $|\bm{k}\times\bm{k}\times\bm{E}|=k^2E\cos\alpha$, and $\epsilon_0ED\cos\alpha=\epsilon_0\bm{E}\cdot\bm{D}=1$
- From this, calculate the _refractive index_:
$$n^2=c^2\frac{k^2}{\omega^2}=\frac{c^2}{\omega^2}\frac{\mu_0\omega^2D}{E\cos\alpha}\epsilon_0ED\cos\alpha=|\bm{D}|^2$$
- Hence, the _radius vector of the ellipsoid_ in direction of $\bm{D}$ is the _refractive index_

- One can represent this in terms of _Huygens wavelets_

- For $\bm{D}\perp\hat{\bm{e}}_3$, $v=c/n_o$, making a _spherical wavelet_, independent of direction in the plane
- For _other polarisations_, for some $\bm{D}$ with angle $\theta$ to $\hat{\bm{e}}_3$, it travels with _effective refractive index_ $n_b$:
$$\frac{(n_b\cos\theta)^2}{n_o^2}+\frac{(n_b\sin\theta)^2}{n_e^2}=1$$
- These form _extraordinary wavelets_, which are _ellipsoidal_
	- It has _azimuthal symmetry_ around $\hat{\bm{e}}_3$

### Double refraction
![[Double refraction.png]]
- Let some wave _enter_ a _uniaxial crystal_ with $\bm{k}_\text{inc}$ _normal_ to the surface, making some angle $\theta$ to the _optic axis_

- If $\bm{D}\perp\hat{\bm{e}}_3$, $\bm{D}||\bm{E}$, and _spherical wavelets_ are formed
- This is an _ordinary ray_

- If $\bm{D}$ has some _component_ parallel to $\hat{\bm{e}}_3$, the wavelets are _ellipsoidal_
- This creates an _extraordinary ray_, which is _laterally shifted_ before exiting the crystal

### Waveplates
- Consider a _plane-polarised wave normally incident_ on a material
![[Waveplate.png]]
- Let the _fast axis_ be along $x$, with $n_f<n_s$

- Depending on the _orientation_ of $\bm{E}$, components experience _different optical thicknesses_
- The _Jones matrix_ for this case:
$$\pmatrix{\exp(i\omega n_fd/c)&0\\0&\exp(i\omega n_sd/c)}\propto\pmatrix{\exp(-i\Delta\phi/2)&0\\0&\exp(i\Delta\phi/2)}$$
- The _phase difference_ $\Delta\phi$ is defined as:
$$\Delta\phi=\omega\frac{(n_s-n_f)d}{c}$$

- This creates a _quarter-wave_ plate or a _half-wave_ plate
	- $\Delta\phi = \pi/2$: a _quarter-wave_ plate
	- $\Delta\phi=\pi$: a _half-wave_ plate
- For a _quarter-wave_ plate with fast axis along $x$:
$$\dunderline{J}_{\lambda/4,x}=\exp(-i\pi/4)\pmatrix{1&0\\0&i}$$
- For a _half-wave_ plate with fast axis along $x$:
$$\dunderline{J}_{\lambda/2,x}=\exp(i\pi/2)\pmatrix{1&0\\0&-1}$$
- For a _general plane-polarised wave_:
$$\dunderline{J}\underline{L}=\pmatrix{\exp(-i\Delta\phi/2)\cos\theta \\ \exp(i\Delta\phi/2)\sin\theta}$$
- For $\Delta\phi=\pi/2$ (_quarter-wave_ plate), $\dunderline{J}\underline{L}=\pmatrix{\cos\theta&i\sin\theta}^T$
	- This is an _elliptically polarised_ wave, with $\alpha=0$, with $\cos\theta$ and $\sin\theta$ as the _semi-major and minor axes_
	- For $\theta=0$ or $\pi/2$, it is _linearly polarised_
	- For $\theta=\pi/4$, it is a _left-handed circularly polarised_
- For $\Delta\phi=\pi$ (_half-wave_ plate), $\dunderline{J}\underline{L}=\pmatrix{\cos\theta&-\sin\theta}^T$
	- This is _plane-polarised_, directed at angle $-\theta$ relative to the $x-$axis
	- It is _rotated_
	- If $\theta=\pi/4$, it is _perpendicular_ to the original
- If $\theta=0$ or $\theta=\pi/2$, it is _completely unaffected_ by the waveplate as $\bm{E}$ is _along one of the principal axis_
### Induced birefringence
- Optical anisotropy can be _induced_ in originally _isotropic_ materials

- When an isotropic, _photoelastic_ material is subjected to _stress_, one induces _stress birefringence_
- The stress causes a distortion at the _molecular level_ to make the dielectric tensor _anisotropic_
- _Experimentally_, when an _isotropic_ material is placed between _crossed polars_, _no light passes through_
- When a stress is applied, the _stress pattern_ can be _visualised_ by seeing how different _stressed sections_ affect the _polarisation_

- When an _external electric field_ $\bm{E}_0$ is applied, an isotropic material can _become uniaxially birefringent_, with the _optic axis_ along $\bm{E}_0$
- This comes from the _alignment_ of polar molecules in _fluids_
- The birefringence _cannot depend on the sign_ of $E_0$, hence one gets:
$$\Delta n=\lambda_0KE_0^2$$
- $K$ is the _Kerr constant_ of the material
- The _Kerr cell_:
![[Kerr Effect.png]]


- In _solids_, $\bm{E}$ can _lower the crystal symmetry_ of the material
- If there is _no inversion symmetry_, it can often _differentiate between field directions_
- This is the _Pockels effect_, and _linear field dependence_ is possible

### Optical activity
- Some materials have _chirality_ at the _molecular level_
	- The _mirror image_ is _unable to be superimposed_ onto the original molecule
- The material is _optically active_, or _circularly birefringent_
- It _responds differently_ to _left and right-handed circularly polarised waves_
	- Circular polarised waves are said to be the _characteristic waves_
- It has _different refractive indices_ for the waves, denoted $n_L$ and $n_R$
	- Effectively a [[#Waveplates|waveplate]] but for circularly polarised waves

- Consider the fact that a _linearly_ polarised wave is a _sum_ of two circularly polarised waves:
$$\bm{L}_x=\pmatrix{1\\0}=\frac{\bm{C}_L+\bm{C}_R}{\sqrt{2}}$$
- The chiral plate of thickness $d$ then gives _additional phases_ of $\exp(i\omega n_{L/R}d/c)$
- Defining $\Delta\phi=\omega(n_L-n_R)d/c$:
$$\bm{L}_x\longrightarrow\pmatrix{\cos(\Delta\phi/2)\\-\sin(\Delta\phi/2)}$$
- This gives _another plane-polarised wave_, but rotated _clockwise_ 
	- Looking _towards_ the source
- The _specific rotatory power_ is the _rotation per unit length_:
$$\alpha=\frac{\Delta\phi}{2d}=\frac{\omega}{2c}(n_L-n_R)$$
- If $n_L>n_R,\;\alpha>0$, the medium is _dextrorotatory (d-rotatory)_
	- The wave rotates _clockwise_
- If $n_L<n_R,\;\alpha<0$, the medium is _levorotatory (l-rotatory)_
	- The wave rotates _anti-clockwise_

### The Faraday Effect 
- _Electric field_ can induce _birefringence_
- Similarly, a _magnetic field_ can induce _chirality_
- An example is an [[Electromagnetism#Waves in plasmas|EM wave in plasma]], with $\bm{B}_0||\bm{k}$ (known as the _Faraday geometry_)
- The _equation of motion_ of _electrons_ in plasma:
$$m\ddot{\bm{r}}=-e(\bm{E}+\dot{\bm{r}}\times\bm{B}_0)$$
- Have _harmonic solutions_:
$$\bm{E}=\pmatrix{E_x\\E_y}\exp(-i\omega t) \hspace{1.5cm}\bm{r}=\pmatrix{x_0\\y_0}\exp(-i\omega t)$$
- The amplitudes are _not necessarily real_, to account for _phase difference_
- Define the _cyclotron frequency_ of the system:
$$\omega_c=\frac{eB_0}{m}$$
- Then to find the _response to circularly polarised wave_:
$$\displaylines{-\omega^2(x_0+iy_0)=-\frac{e}{m}(E_x+iE_y)+\omega\omega_c(x_0+iy_0) \\ -\omega^2(x_0-iy_0)=-\frac{e}{m}(E_x-iE_y)+\omega\omega_c(x_0-iy_0)}$$
- For $E_x=E_y=|\bm{E}|$, they correspond to _LCP_ and _RCP_, with some _displacement_ $a\pmatrix{1&i}^T$ as the _response_
- With some _electron number density_ $n$, the _circular polarisation field_:
$$P_L=-ena\pmatrix{1\\i}=\epsilon_0\chi_LE\pmatrix{1\\i}$$
- The _effective susceptibility_ is then:
$$\chi_L=-\frac{ne^2}{m\epsilon_0}\frac{1}{\omega^2-\omega\omega_c}=-\frac{\omega_p^2}{\omega^2-\omega\omega_c}$$

- One finds that the _effective dielectric constants_ are:
$$\epsilon_\frac{L}{R}(\omega)=1-\frac{\omega_p^2}{\omega(\omega\mp\omega_c)}$$
- The _angle of rotation_ $\theta$ is then, in the limit of a _weak field_:
$$\theta=\frac{\Delta\phi}{2}=\frac{\omega(n_L-n_R)d}{c}\approx-\frac{\omega_p^2\omega_cd}{2c\omega^2\sqrt{1-\omega_p
^2/\omega^2}}$$
- Define the _Verdet coefficient_ as:
$$\theta=VB_0d\Longrightarrow V=-\frac{e\omega_p^2}{2mc\omega^2\sqrt{1-\omega_p^2/\omega^2}}$$

- Any $z-$component of $\bm{E}$ is always _unaffected_ as $z-$motion is _unaffected_ by $\bm{B}_0$
- If one _solves_ for $x_0$ and $y_0$:
$$\dunderline{\epsilon}=1+\dunderline{\chi}=\pmatrix{1-\frac{\omega_p^2}{\omega^2-\omega_c^2}&\frac{i\omega_c\omega_p^2}{\omega(\omega^2-\omega_c^2)}&0\\\frac{-i\omega_c\omega_p^2}{\omega(\omega^2-\omega_c^2)}&1-\frac{\omega_p^2}{\omega^2-\omega_c^2}&0\\0&0&1-\frac{\omega_p^2}{\omega^2}}$$
- As expected, the matrix is _Hermitian_
- When $\bm{B}\to0$, one regains an _isotropic plasma_

## Interference and partial polarisation
- When considering EM waves, the interference must be in _vector_ form

### Perpendicular plane-polarised waves
- Consider the superposition of _two waves_ along the $z-$axis, _perpendicularly plane polarised_, with some _phase difference_ $\delta$
- The _Poynting vector_ is then:
$$\begin{aligned}\bm{N}=\bm{E}\times\bm{H}&=\begin{pmatrix}E_{1x}\cos(\omega t)\\E_{2y}\cos(\omega t+\delta)\\0\end{pmatrix} \times\begin{pmatrix}-H_{2x}\cos(\omega t+\delta) \\ H_{1y}\cos(\omega t) \\ 0\end{pmatrix} \\ &= \begin{pmatrix}0 \\ 0 \\ E_{1x}H_{1y}\cos^2(\omega t)+E_{2y}H_{2x} \cos^2(\omega t+\delta) \end{pmatrix}\end{aligned}$$
- This is _identical_ to the energy propagation for _two independent waves_
- The _intensity at a point_ from two _superimposed perpendicularly plane-polarised waves_ is the _sum_ of the intensity of two waves
- In other words, _perpendicular plane-polarised waves do not interfere_

### Unpolarised and partially polarised light
- Many natural sources have the _direction_ of $\bm{E}$ changing _randomly_ in time and space
- It is said to be _unpolarised_
- The $x$ and $y$ components of $\bm{E}$ are _unpolarised_
- Plane-polarised beams produced by passing the _same unpolarised beam_ through $x$ and $y$ polarisers will be _mutually incoherent_
	- There is _no well-defined phase difference_, hence they _cannot interfere_

- A beam with both _polarised and unpolarised_ light with intensities $I_\text{pol}$ and $I_\text{unpol}$, is said to be _partially polarised_
- The _degree of polarisation_ is defined as:
$$\alpha=\frac{I_\text{pol}}{I_\text{pol}+I_\text{unpol}}$$
### The Fresnel-Arago Laws
- The conclusions above can be _summarised_ as:
1. Two _coherent_ beams, plane polarised _parallel_, will _interfere_
2. Two _coherent_ beams, plane polarised _perpendicularly_, _cannot interfere_
3. Two _plane-polarised_ beams (no matter the orientation), _derived_ from components of _unpolarised light_, are _mutually incoherent_ and hence _cannot interfere_

## Coherence
- For simplicity, consider _scalar_ waves
- Interference relies on a _well-defined phase difference_ between the wavelets, such that there is a well-defined sum
	- Then given $f(\boldsymbol{r}_{1},t_{1})$, one can _deduce_ $f(\boldsymbol{r}_{2},t_{2})$ given the wave is _coherent_ in that region
- This can only be true for _purely monochromatic waves_

- From _Fourier analysis_, purely monochromatic waves must have _infinite spatial and temporal extent_
- Hence, _real_ sources can only be _quasi-monochromatic_

- The _theory of coherence_ describes _non-monochromatic_ waves _quantitatively_
- It quantifies the _correlation_ between the values of a wave in two positions and times
### Power spectra
- Let there be some _time-dependent function_ $f(t)$
- Take its [[Fourier series and transforms|Fourier transform]]:
$$f(t)=\frac{1}{2\pi}\int_{-\infty}^\infty F(\omega)\exp(i\omega t)\,d\omega \hspace{1cm} F(\omega)=\int_{-\infty}^\infty f(t)\exp(-i\omega t)\,dt$$
- The _power_ in frequency range $\omega$ to $\omega+d\omega$ is the _power spectrum_:
$$P(\omega)\,d\omega=|F(\omega)|^2\,d\omega$$

### Light sources

#### Laser
- Light produced by [[Lasers|stimulated emission]]
- It is (almost) a _pure harmonic wave_:
$$\displaylines{f(t)\sim \cos(\omega t+\alpha) \\ F(\omega)\propto \exp(i\alpha)\delta(\omega-\omega_0)+\exp(-i\alpha)\delta(\omega+\omega_0)}$$
- It is a _pair_ of delta functions at $\pm\omega_0$

#### Spectral lines
- Example: _gas discharge_ lamps
- There are _several broadening mechanisms_

- _Lifetime_ broadening:
	- Unstimulated emission from an _isolated, stationary atom_ can be characterised by a _decaying harmonic wave_, with some _lifetime_ $\tau_s$, and _frequency_ $\omega_s=1/\tau_s$
	$$\displaylines{f(t)=\exp(-\omega_st)\exp(i\omega_0t) \\ F(\omega)=\frac{1}{\omega-\omega_0-i\omega_s} \\ P(\omega)\sim \frac{1}{(\omega-\omega_0)^2+\omega_s^2}}$$
	- It is a _Lorentzian_ power spectrum, _centred_ on $\omega_0$ with _linewidth_ (full-width half maximum) $2\omega_s$
	![[Lifetime broadening.png]]

- _Thermal_ broadening:
	- Radiation from atoms _moving in the line of sight_ (at $v_x$) will be _Doppler shifted_
	$$\omega-\omega_0=\frac{\omega_0 v_x}{c}$$
	- From kinetic theory, the _distribution of velocities_ is _Gaussian_
	- The _power spectrum_ is then:
	$$P(\omega)\sim \exp\left(-\frac{m(\omega-\omega_0)^2c^2}{2\omega_0^2 k_BT}\right)=\exp\left(-\frac{(\omega-\omega_0)^2}{2\sigma^2}\right)$$
	- The _full-width half maximum_ is then given by:
	$$2.36\sigma=2.36\,\omega_0\left(\frac{k_BT}{mc^2}\right)^{1/2}$$
	- The _width scales with temperature_

- _Pressire_ broadening:
	- Atoms are subject to _collisions_ with other atoms
	- This _perturbs_ the _phase correlation_
	- The _mean time_ $\tau_1$ is:
	$$\tau_1=\frac{1}{4N\mean{v}A}=\frac{b\sqrt{T}}{p}$$
	- This produces another _Lorentzian_ profile:
	$$P(\omega)\sim\frac{1}{(\omega-\omega_0)^2+1/\tau_1^2}$$

- A gas discharge lamp has an output of a _superposition_ of large numbers of _independent photons_ from _similar atoms_
- Overall, one gets a _convolution_ of the different broadening profiles
- The _quasi-monochromatic waveform_:
![[Quasi-monochromatic.png]]

#### White light
- A _large number_ of atoms with _different emission frequencies_, or atoms on a _black body_, results in _white light_ with a _broad power spectrum_
![[White light.png]]
### Interference and coherence
- One must be able to calculate _interference with partially coherent light_
- A _partially coherent_ wavefield:
![[Partial coherence.png]]
- _Phase registration_ is _lost_ over $l_c=c\tau_c$
- $\tau_c$ is the _temporal coherence length_, which is _along the direction of propagation_
- $w_c$ is the _spatial coherence width_, which is _perpendicular to the direction of propagation_

- To _measure_ these lengths, let there be _ideal, identical lossless optical fibres_ which _sample_ points on a wavefield, and let them _interfere_
![[Optical stethoscope.png]]

- The _time average_ of a function $g(t)$ is defined as:
$$\mean{g(t)}=\lim_{T\to\infty}\int_{-\infty}^\infty g(t)\,dt$$
- The _resultant intensity_ of the interference pattern:
$$I\sim \mean{(A_1+A_2)(A_1^*+A_2^*)}=\mean{|A_1|^2}+\mean{|A_2|^2}+\mean{A_1A_2^*}+\mean{A_1^*A_2}$$
- The _cross terms_ determine _interference effects_
	- If the sources at $A_1$ and $A_2$ are _perfectly coherent_, this gives _distinct fringes_
	- If the sources are _incoherent_, there are _no fringes_
- The _visibility_ of the fringes $V=(I_\text{max}-I_\text{min})/(I_\text{max}+I_\text{min})$ then quantifies the _mutual coherence_ of the points

### Mutual coherence function
- Suppose there are two measurements:
	- $f_1$ at $\bm{r}_1$ at time $t$
	- $f_2$ at $\bm{r}_2$ at time $t-\tau$
- Then define the _mutual coherence function_:
$$\Gamma(\bm{r}_1,\bm{r}_2,\tau)=\mean{f_1(\bm{r}_1,t)f_2^*(\bm{r}_2,t-\tau)}$$
- This assumes there is _correlation_ in the behaviour after $\tau$ across time $t$

- By _normalising intensity_, one gets the _degree of mutual coherence_:
$$\displaylines{\gamma(\bm{r}_1,\bm{r}_2,\tau)=\frac{\Gamma(\bm{r}_1,\bm{r}_2,\tau)}{\sqrt{I_1I_2}} \\ I_i=\Gamma(\bm{r}_i,\bm{r}_i,0) \\ 0<\gamma<1}$$

- This determines how _effectively_ the source waves can _interfere_
- If $|\gamma|\sim 1$, this means $I$ can go _down to zero_ due to the _interference terms_, giving _good fringe contrast_
	- If $I_1=I_2$, then the resultant intensity can go back to _zero_

- Examining the wavefield _along direction of propagation_ compares $f(t)$ at the _same point in the wavefront_, $\bm{r}_1=\bm{r}_2$, at _different times_, $t$ and $t-\tau$
- This investigates _temporal coherence_

- Examining the wavefield _along the wavefront_ compares $f(t)$ at the _same time_, $\tau=0$, at _different points along the wavefront_, $\bm{r}_1\neq\bm{r}_2$
- This investigates _spatial coherence_

## Temporal coherence
- The _temporal coherence_ of a source gives information on the _spectral content_

- Potential setup to investigate temporal coherence:
![[Temporal coherence stethoscope.png]]
- The _time delay_ $\tau=2d/c$ can be altered _spatially_
- This is _amplitude division_, so $\bm{r}_1\equiv\bm{r}_2$
- Take the divided amplitudes to be _equal_, $A_1=f(t)$, and $A_2=f(t-\tau)$

- The output intensity:
$$\displaylines{I(\tau)=\mean{(A_1+A_2)(A_1^*+A_2^*)}=2I_0+2\Re{[(\Gamma(\tau)]} \\ \Gamma(\tau)=\mean{f(t)f^*(t-\tau)}}$$
- $\Gamma$ in this is the _temporal coherence function_, _quantified_ by $I$

- Write $\Gamma$ as $|\Gamma(\tau)|\exp[i\Delta(\tau)]$
- This gives intensity:
$$I(\tau)=2I_0+2|\Gamma(\tau)|\cos[\Delta(\tau)]$$
- For a _quasi-monochromatic_ waveform $f(t)\approx \exp(-i\omega_0t)$:
$$\Gamma(\tau)=\mean{f(t)f^*(t-\tau)}\approx \exp(-i\omega_0\tau)=\exp(-2ik_0d)$$
- The phase term _oscillates_ with change in $d$, on the _order of the wavelength_
	- _Rapidly_ compared to variation in _amplitude_ (light is quasi-monochromatic)

- One then observes _fringes_, with _visibility/contrast_ $V$:
$$V(\tau)=\frac{I_\text{max}-I_\text{min}}{I_\text{max}+I_\text{min}}=\frac{|\Gamma(\tau)|}{I_0}=|\gamma(\tau)|$$
- $\gamma(\tau)$ is the _degree of temporal coherence_
	- The _normalised_ temporal coherence function
- One can check that $\Gamma(0)=I_0$ and $V(0)=1$
- As $\tau$ increases, any element of _decorrelation_ in $f(\tau)$ causes $V$ to _decrease_

### Auto-correlation
- For some _irregular normalised waveform_ $f(t)$, its [[Fourier series and transforms#Correlations|auto-correlation]] $h(\tau)$:
$$h(\tau)=\int_{-\infty}^\infty f(t)f^*(t-\tau)\,dt$$
- For some _quasi-random function_, it is _unity_ at $\tau=0$ then _quickly drops off_
	- For a truly random function, it approaches a _delta function_

- One can prove that the _Fourier transform_ of $h(\tau)$ is:
$$\mathcal{F}[h(\tau)]=H(\omega)=F(\omega)F^*(\omega)=|F(\omega)|^2$$
- This is the _Wiener-Khinchine Theorem_

- As $h(\tau)\sim \gamma(\tau)$, one shows that the _power spectrum_ is given by the Fourier transform of the _fringe visibility_:
$$P(\omega)=\mathcal{F}[\gamma(\tau)\equiv V(\tau)]$$

- Define _relative intensity_ $I_r(\tau)$:
$$I_r(\tau)=\frac{I(\tau)}{2I_0}=1+\Re[\gamma(\tau)]$$

- Letting $f(t)$ and therefore $\gamma$ be _real_, one can write $P(\omega)$ as:
$$P(\omega)=\mathcal{F}[I_r(\tau)-1]$$

### Fourier transform spectroscopy
- The _Michelson interferometer_:
![[Michelson interferometer.png]]
- The _compensator plate_ eliminates phase difference due to _optical path in glass_
- Typical _advantages_:
	- Radiation _throughput_ is higher as it is _not limited by slit width_
	- The _signal-to-noise ratio_ is higher as the signal _continuously falls on the detector_
	- The _spectral resolution_ is given by $\lambda/\delta\lambda\approx 2d/\lambda=m$, where $m$ is the _number of fringes recorded_

### Summary
- Given a _source_ outputting $f(t)$
- Interfering sources with outputs $f(t)$ and $f(t-\tau)$, _divided_ from the _same point on the wavefront_ (division of amplitude)
- If the division is achieved using _mirrors_ separated at distance $d$:
$$\tau=\frac{2d}{c}$$

- The _temporal coherence function_:
$$\Gamma(\tau)=\langle f(t)f^{*}(t-\tau) \rangle $$
- The _degree of mutual coherence_:
$$\gamma(\tau)=\frac{\Gamma(\tau)}{I_{0}}$$
- The _measured intensity_ given $\tau$, _averaged_ over $t$ is:
$$I(\tau)=2I_{0}+2\mathrm{Re}[\Gamma(\tau)]$$
- This gives _fringes_, which have _visibility_:
$$V(\tau)=\frac{I_\text{max}-I_\text{min}}{I_\text{max}+I_\text{min}}=|\gamma(\tau)|$$
- Then from the [[#Auto-correlation|Wiener-Kinchine Theorem]], the _power spectrum_:
$$P(\omega)=\text{FT}[\gamma(\tau))]$$

### Gaussian power spectrum
- Suppose the power spectrum is _Gaussian_ due to [[#Spectral lines|broadening]]
$$P(\omega)=C\exp\left(-\frac{(\omega-\omega_0)^2}{2\sigma^2}\right)$$
- Find the temporal coherence function:
$$\Gamma(\tau)=\mathcal{F}^{-1}[P(\omega)]=\exp(i\omega_0\tau)\exp\left(-\frac{\tau^2}{2(1/\sigma^2)}\right)$$
- The _relative intensity_ is then:
$$I_r(\tau=2d/c)=1+\exp\left(-\frac{\sigma^2\tau^2}{2}\right)\cos(\omega_0\tau)$$
- The _visibility_ is then:
$$V(\tau)=\exp\left(-\frac{\sigma^2\tau^2}{2}\right)$$
![[Michelson broadened spectral line.png]]
- The _spacing_ of the fringes is related to _central frequency_
- The _modulation_ of the fringes gives the _broadening_
- As $d$ increases, the beams become _gradually less coherent_

### Coherence length and time
- Define the _coherence length_ $l_c$ as the _path difference_ $2d$ where $V(\tau)=1/e$
- This determines the _frequency bandwidth_ $\delta\omega\sim\sigma$
- From the expression for $V(\tau)$:
$$l_c=\frac{c\sqrt{2}}{\sigma}\sim\frac{\lambda^2}{2\delta\lambda}$$
- This is really a measure of _coherence time_:
$$\tau_c=\frac{l_c}{c}\propto\sigma^{-1}$$
- Example for $\text{Kr}^{84}$, $l_c\approx 0.78\,\text{m}$

- For a _spatial observation_ of temporal coherence, use _double slits_ with the broadened source:
![[Temporal coherence slits.png]]
- The _differing path lengths_ mean that the beams become _less mutually coherent_ as $l$ increases, such that _fringe visibility decreases_

## Spatial coherence
- Let there be a _perfectly monochromatic_, but _incoherent_ source
	- Different _spatial locations_ in the source are _uncorrelated_
![[Spatial coherence stethoscope.png]]
- Slits are illuminated by _beams_ of wavelength $\lambda$ and with _finite angular width_
- The _intensity variation in the source plane_ is $I(x)$

- Each _beam_ produces its own _fringes_, which are _offset from each other_
- The _fringe contrast_ is then _degraded_

### Coherence width
- If the _angular width_ of the source is $\alpha$, then fringes are _offset_ by $\alpha D$
- The _fringe spacing_ is $\lambda D/d$, hence one _loses contrast_ if:
$$\alpha D>\frac{\lambda D}{d}\Longrightarrow d>\frac{\lambda}{\alpha}\approx w_c$$
- It gives _coherence variations across the wavefield_, or _spatial/lateral coherence_
	- _Temporal coherence_ is _along_ the beam, or _longitudinal_
- $w_c$ is known as the _coherence width_

### Intensity profile
- For the _two rays_:
$$k(\rho_1+r_1-\rho_2-r_2)= kd(\sin\theta+\sin\chi)\approx kd\left(\frac{x}{L}+\frac{y}{D}\right)=2ks$$
- Given some _intensity profile_ $I(x)$ at the _source_, the _amplitude_ at $P$ is then:
$$\psi(y)\sim\sqrt{I(x)}\exp[ik(\rho+R)](e^{iks}+e^{-iks})=2\sqrt{I(x)}\exp[ik(\rho+R)]\cos(ks)$$

- If the extended source is _incoherent_ (beams from different points are _uncorrelated_), then the _net intensity as a function of $d$_ is obtained by _summing intensities_:
$$\begin{aligned}I_y(d)&=\int |\psi(y)|^2\,dx=4\int I(x)\cos^2(ks)\,dx \\ &=2I_0+2\Re\left[\exp(-ikdy/D)\int I(x)\exp(-ikdx/L)\,dx\right]\end{aligned}$$
- This is similar to the form from [[#Temporal coherence|division of amplitude]] for investigating temporal coherence

- Then by _changing variables_, with $x=L\theta$, $y=d\chi$, and $I(x)\,dx=I(\theta)\,d\theta$, with $kd=u$:
$$I_y(u)=2I_0+2I_0\Re[\exp(-iu\chi)\gamma(u)]$$
- Defining $\gamma(u)$, as well as a phase $\beta$, using the _Fourier transform of the intensity profile_:
$$\displaylines{\gamma(u)=\frac{1}{I_0}\int I(\theta)\,\exp(-iu\theta)\,d\theta=\frac{\mathcal{F}[I(\theta)]}{I_0}\equiv|\gamma(u)|\exp(-i\beta) \\ I_y(u)=2I_0+2I_0|\gamma(u)|\cos\left(\beta+\frac{kdy}{D}\right)}$$
- There are $\cos^2$ fringes with _spacing_ determined by $kdy/D$
- $|\gamma(u)|$ defines the _fringe contrast_ at point $y$
- There is some _offset_ $\beta$, determined by the _angular profile_ $I(\theta)$


- For a _symmetric source profile_ (about the axis), $\gamma (u)$ is _real_ and:
$$\beta=\begin{cases}0&\gamma(u)>0 \\ \pi&\gamma(u)<0\end{cases}$$
- The _visibility_ of the fringes is then:
$$V=\gamma(u\equiv kd)$$
- It can be _negative_ (if a minimum occurs where a _maximum_ is expected)

### Degree of lateral coherence
- The visibility gives the _intensity profile_ of the source 
- Define $\gamma(u)$ as the _degree of lateral coherence_:
$$\gamma(u)\equiv\gamma(kd)=\frac{\mathcal{F}[I(\theta)]}{I_{0}}$$
- The _van Cittert-Zernike theorem_ states that the degree of lateral coherence is the _normalised Fourier transform of the intensity profile_

- $\gamma(u)$ is determined by the _slit separation_ $d$, and can be used to define a _coherence width_

### Examples
- Given a _distant, uniform line source_ with _angular width_ $\alpha$:
$$\gamma(u)=\frac{1}{I_0}\int_{-\alpha/2}^{\alpha/2}J\exp(-iu\theta)\,d\theta=\sinc\left(\frac{u\alpha}{2}\right)$$
- The _fringe contrast_ will _fall to zero_ at:
$$\frac{u\alpha}{2}=\pi\longrightarrow w_c\sim d=\frac{\lambda}{\alpha}$$
- Beyond which, $V$ becomes _negative_

- For a uniform _disc source_ of _angular diameter_ $\alpha$ illuminating the pinholes of separation $d$:
$$\gamma(u)=\frac{2J_1(u\alpha/2)}{u\alpha/2}\longrightarrow w_c=\frac{1.22\lambda}{\alpha}\sim\frac{\lambda}{\alpha}$$
- In general, the _broader the source_, the _narrower the coherence width_

- For a _fixed source width_, and _increasing slit separation_:
![[Spatial coherence comparison.png]]
- $V$ goes _through zero_ then rises again
- When there is a _central minimum_, that indicates $\gamma(u)<0$

- For an _increasing source width_, and _fixed slit separation_:
![[Spatial coherence comparison 2.png]]

### Coherence area and volume
- For a _2D source_, there is some _coherence area_
- When combined with [[#Temporal coherence]] effects, one can find a [[#Fourier transform spectroscopy|coherence length]]
- This gives a _coherence volume_

- For _sunlight_, $\lambda\approx 500\,\text{nm}$, $\delta\lambda\approx500\,\text{nm}$, $\alpha\sim 0.5^o\sim0.01\,\text{rad}$:
$$w_c\sim\frac{\lambda}{\alpha}\sim5\times 10^{-5}\,\text{m}\hspace{1.5cm} l_c\sim\frac{\lambda^2}{\delta\lambda}\sim 500\,\text{nm}$$
- These are _very small scales_ when compared to every day objects
- Hence, one needs _filtered light_ to make measurements

### Michelson interferometer

# Electrodynamics
- A _conservative field_, such as the _electrostatic_ one, is described by a _scalar potential_ $\phi$:
$$\bm{E}=-\nabla\phi$$
- In _general_, $\bm{E}$ is _time-dependent_, and _non-conservative_ from _Faraday's Law_:
$$\oint\bm{E}\cdot d\bm{l}=-\int\dot{\bm{B}}\cdot d\bm{S}$$
- Similarly:
$$\oint \bm{H}\cdot d\bm{l}=\int(\bm{J}+\dot{\bm{D}})\cdot d\bm{S}$$
- The _magnetic scalar potential_ $\phi_m$ can only be defined for _static_ circumstances and in _current-free regions_

## The magnetic vector potential
- Since $\nabla\cdot{\bm{B}}=0$ _at all times_, one can define the _magnetic vector potential_ $\bm{A}$:
$$\bm{B}(\bm{r})=\nabla\times\bm{A}(\bm{r})$$
- Given some _loop_ $L$, for _any surface_ $S$ bounded by $L$:
$$\Phi_S=\int\bm{B}\cdot d\bm{S}=\oint_L \bm{A}\cdot d\bm{l}$$
- The _flux_ through the surface is only determined by $\bm{A}$ _along the bounding path_
	- Expected from $\nabla\cdot\bm{B}=0$

- One can then find the corresponding _electric field_:
$$\bm{E}=-\nabla\phi-\pd{\bm{A}}{t}$$
- For _static situations_, it reduces to the electrostatic potential

### Gauge transformations
- $\bm{B}=\nabla\times\bm{A}$ _does not completely specify_ $\bm{A}$
- One can get the _same vector field_ with:
$$\bm{A}\to\bm{A}+\nabla\chi$$
- One must then make a _corresponding change to potential_:
$$\phi\to\phi-\pd{\chi}{t}$$
- $\chi$ can be _any scalar function_ of $\bm{x}$ and $t$
- It is called the _gauge_
- All physical laws are _gauge invariant_

- One often chooses the _divergence_ of $\bm{A}$ as $\nabla^2\chi$ is arbitrary

- The _Coulomb gauge_:
$$\nabla\cdot\bm{A}=0$$
- The _Lorenz gauge_:
$$\nabla\cdot\bm{A}+\frac{1}{c^2}\pd{\phi}{t}=0$$

## Poisson's equation for the vector potential
- From substituting the definition of $\bm{A}$, for the _Coulomb gauge_:
$$\nabla^2\bm{A}=-\mu_0\bm{J}$$
- This is simply _Poisson's equation_ again
	- Each _component_ must obey its own Poisson's equation
$$\bm{A}(\bm{r})=\frac{\mu_0}{4\pi}\int_\text{all space}\frac{\bm{J}(\bm{r}')}{|\bm{r}-\bm{r}'|}\,d^3\bm{r}'$$
- For some _line element_, $\bm{J}(\bm{r}')\to Idl'$, with $d\bm{A}||d\bm{l}'$
- One can also recover the _Biot-Savart law_ by taking the curl

- One can _find_ $\bm{A}$ by:
	- Direct integration of the current distribution
	- Integration of a _known_ $\bm{B}$ field
	- Equating the _line integral_ to the _flux_ through any open surface bounded by the path

- Example: for a _long, straight wire_, $B_\phi=\mu_0I/2\pi r$
	- From the _symmetry_ of the integral, one gets that $\bm{A}$ is _parallel_ to the wire
	![[Long straight wire B.png]]
	- One then gets $A_z=-\mu_0I/(2\pi)\ln r$

- Example: for a _solenoid_, $B_z=\mu_0 nI$ _inside_, and is _zero outside_
	- Equate the _line integral_ of $\bm{A}$ to the _enclosed flux_
	- _Inside_, $A_\phi=\mu_0nIr/2$
	- _Outside_, $A_\phi=\mu_0nIa^2/2r$
	- The _experimental effects_ of the $\bm{A}$ _outside_ can be seen in the [[Charged Particles#The Aharanov-Bohm Effect|Aharonov-Bohm Effect]]
### The distant current loop and magnetic dipole
- For a _current loop_:
$$\bm{A}=\frac{\mu_0}{4\pi}\oint\frac{Id\bm{r}'}{|\bm{r}-\bm{r}'|}$$
- For a _distant loop_, make the approximation:
$$|\bm{r}-\bm{r}'|^{-1}=\frac{1}{\sqrt{r^2+r'^2-2\bm{r}\cdot\bm{r}'}}\approx\frac{1}{r}\left(1-\frac{\bm{r}\cdot\bm{r}'}{r^2}+\dots\right)$$
- Substitute into the integral:
$$\bm{A}=\frac{\mu_0}{4\pi}\left[\frac{1}{r}\oint d\bm{r}' -\frac{1}{r^3}\oint (\bm{r}\cdot\bm{r}')\,d\bm{r}'+\dots\right]$$
- The _first term is zero_
- For the second term, one can prove:
$$d\bm{r}'(\bm{r}\cdot\bm{r}')=\frac{1}{2}d[\bm{r}'(\bm{r}\cdot\bm{r}')]+\frac{1}{2}(\bm{r}'\times d\bm{r}')\times\bm{r}$$
- The _perfect differential vanishes when integrated_

- One gets the expression:
$$\bm{A}(\bm{r})=\frac{\mu_0}{4\pi}\left[\oint_L\frac{I}{2}\bm{r}'\times d\bm{r}'\right]\frac{\bm{r}}{r^3}=\frac{\mu_0}{4\pi}\frac{\bm{m}\times\bm{r}}{r^3}$$
- For a _planar loop_, the integral is $IS\hat{\bm{n}}$, where $S\hat{\bm{n}}$ is the _vector area_:
$$\bm{m}=IS\hat{\bm{n}}$$
- $\bm{m}$ is the _magnetic dipole_

## Maxwell's equations in terms of potentials
- Maxwell's equations feature _redundancy_:
$$\displaylines{\div(\curl\bm{E})=-\div\dot{\bm{B}}=0}$$
- This is already given by $\div\bm{B}=0$

- They contain _8 independent unknowns_
	- 4 _independent components of fields_
	- The _current and charge densities_
 
- Writing the fields _in terms of potentials_:
$$\mu\mu_0\bm{H}=\curl\bm{A}\hspace{1.5cm}\frac{\bm{D}}{\epsilon\epsilon_0}=-\dot{\bm{A}}-\grad\phi$$
$$\div\bm{E}=-\pd{}{t}\div\bm{A}-\nabla^2\phi=\frac{\rho}{\epsilon\epsilon_0}$$
$$\grad\left(\div\bm{A}+\epsilon\epsilon_0\mu\mu_0\dot{\phi}\right)-\nabla^2\bm{A}=\mu\mu_0\bm{J}-\epsilon\epsilon_0\mu\mu_0\ddot{\bm{A}}$$
- Then choose the [[#Gauge transformations|Lorenz gauge]]:
$$\div\bm{A}+\epsilon\mu\frac{\dot{\phi}}{c^2}=0$$
- This then gives two _wave equations_, with _source terms_
$$\displaylines{\frac{\epsilon\mu}{c^2}\ddot{\phi}-\nabla^2\phi=\frac{\rho}{\epsilon\epsilon_0} \\ \frac{\epsilon\mu}{c^2}\ddot{\bm{A}}-\nabla^2\bm{A}=\mu\mu_0\bm{J}}$$
- This contains the _same information as Maxwell's equations_
- For _static fields_, they reduce to _Poisson's equation_, and the _Coulomb gauge_ also applies

## Solving for the potentials
- For simplicity, assume $\epsilon=\mu=1$
- Both $\rho$ and $\bm{J}$ can _vary in time_
- As the equations are _wave equations_, one expects equations of the form $f(t\pm r/c)$

- Consider some _time-varying charge_ at the origin $q(r=0,t)$
- The solution must be _spherically symmetric_, and go like an _inverse square_:
$$\phi\sim\frac{1}{r}g\left(t-\frac{r}{c}\right)$$
- This corresponds to an _outgoing wave_
	- The solution at $(r,t)$ depends on the _charge at a time earlier_ by the _retarded time_ $r/c$
	- This gives the notion of _causality_, hinting at [[Special Relativity|special relativity]]

- If the charge _varies over timescale_ $\tau$, and $r\ll c\tau$, the solution _must be like the static case_
- This gives the solution:
$$\phi(r,t)=\frac{1}{4\pi\epsilon_0}\frac{q(t-r/c)}{r}$$

- For a source term with some _charge distribution_ $\rho(\bm{r},t)$, _superimpose_ the solutions:
$$\phi(r,t)=\frac{1}{4\pi\epsilon_0}\int_\text{all space}\frac{\rho(\bm{r}',t-|\bm{r}-\bm{r}'|/c)}{|\bm{r}-\bm{r}'|}\,dV$$

### Evaluating quantities at retarded time
- The _retarded scalar potential_ allows for the _propagation of information_ at a _finite speed_ $c$
- Denote _evaluating at retarded time_:
$$\displaylines{\rho\left(\bm{r}',t-\frac{|\bm{r}-\bm{r}'|}{c}\right)\equiv[\rho(\bm{r}',\bm{r},t)]\equiv[\rho] \\ \phi=\frac{1}{4\pi\epsilon_0}\int_\text{all space}\frac{[\rho]}{|\bm{r}-\bm{r}'|}\,dV'}$$

- Similarly, the _retarded vector potential_:
$$\bm{A}=\frac{\mu_0}{4\pi}\int\frac{[\bm{J}]\,dV'}{|\bm{r}-\bm{r}'|}$$

- The _differential_ of retarded quantities:
$$\pd{}{r}[F]=\frac{\partial}{\partial r}F\left( t-\frac{r}{c} \right)=-\frac{1}{c}[F']\hspace{1.5cm}\pd{}{t}[F]=[F']$$

# Dipole radiation
- _Moving charges_ will cause _time-varying fields_
	- For a charge at _constant velocity_, one can _transform_ into a frame where the charge is _stationary_, and _cannot lose energy_
- Therefore, only _accelerating charges radiate_

- Consider a _time-varying dipole_ in free space:
![[Time-varying dipole.png]]
- If the dipole suddenly _flips direction_, the field at $X$ _does not flip direction until_ time $r/c$ _later_ due to retardation effects
- If the dipole _oscillates_ with phase $\omega t$, then $\bm{E}$ must also oscillate but _shifted in phase_ due to the retardation, therefore having phase $\omega(t-r/c$)
- The oscillating charge also involves a _current_, giving a _magnetic field_

## The Hertzian electric dipole
- There are _two opposite charges_, separated by distance $d$, giving a _current_
- The _dipole moment_ is then:
$$\bm{p}=(0,0,p_0\exp(-i\omega t))\hspace{1.5cm} I=-i\omega\frac{p_0}{d}\exp(-i\omega t)$$
- The _physical size_ of the dipole is taken as _small_ compared to the radiation wavelength $\lambda=2\pi c/\omega$
- At some _distant point_ $P$ at $\bm{r}=(r,\theta,\phi)$ is given by the _retarded potential_ with $r\gg d$

- Let $d\ll r$, such that _variations_ in $|\bm{r}-\bm{r}'|$ is _ignored_

### Magnetic field
- The magnetic potential:
$$\bm{A}(r,t)=\frac{\mu_0}{4\pi r}\int[\bm{J}]\,dV'$$
- where the _retarded current density_ gives:
$$\int[\bm{J}]\,dV'=\dot{q}(t-r/c)d\,\hat{\bm{z}}=[\dot{\bm{p}}]$$
- This gives the potential:
$$\bm{A}(\bm{r},t)=\frac{\mu_0}{4\pi r}[\dot{\bm{p}}]=A\hat{z}$$
- Decomposing $\bm{A}$ into _components in polar coordinates_, and using $\bm{B}=\nabla\times\bm{A}$:
$$\displaylines{B_r=B_\phi=0 \\ B_\phi=-\sin\theta\pd{A}{r}=\frac{\mu_0}{4\pi}\sin\theta\left(\frac{[\dot{p}]}{r^2}+\frac{[\ddot{p}]}{rc}\right)}$$
### Electric field
- The _scalar potential_:
$$\begin{aligned}\phi&=\frac{1}{4\pi\epsilon_0}\left[\frac{q(t-r_+/c)}{r_+}-\frac{q(t-r_-/c)}{r_-}\right] \\ &=\frac{1}{4\pi\epsilon_0}(r_+-r_-)\pd{}{r}\left[\frac{q(t-r/c)}{r}\right]\end{aligned}$$
- Writing the distance $r_+-r_-$ as $d\cos\theta$ and doing the derivative:
$$\phi=\frac{\cos\theta}{4\pi\epsilon_0}\left\{\frac{[p]}{r^2}+\frac{[\dot{p}]}{rc}\right\}$$
- Calculating the _components_ by $\bm{E}=-\dot{\bm{A}}-\grad\phi$:
$$\displaylines{E_\phi=0\\ E_r=\frac{2\cos\theta}{4\pi\epsilon_0}\left\{\frac{[p]}{r^{3}}+\frac{[\dot{p}]}{r^{2}c}\right\} \\ E_\theta=\frac{\sin\theta}{4\pi\epsilon_0}\left\{\frac{[p]}{r^{3}}+\frac{[\dot{p}]}{r^{2}c}+\frac{[\ddot{p}]}{rc^{2}}\right\}}$$
### Behaviour of the field
- The _non-zero components_:
$$\begin{aligned}B_\phi&= {\mu_0}{4\pi}\sin\theta\left(\frac{[\dot{p}]}{r^2}+\frac{[\ddot{p}]}{rc}\right)\\ E_\theta&=\frac{\sin\theta}{4\pi\epsilon_0}\left\{\frac{[p]}{r^{3}}+\frac{[\dot{p}]}{r^{2}c}+\frac{[\ddot{p}]}{rc^{2}}\right\} \\ E_r&=\frac{2\cos\theta}{4\pi\epsilon_0}\left\{\frac{[p]}{r^{3}}+\frac{[\dot{p}]}{r^{2}c}\right\}\end{aligned}$$
- The terms varying as $1/r^3$ correspond to a _static dipole_, but according to the _retarded dipole moment_

- The _dipole term_ $\propto1/r^3$ will _dominate for small distances_ $r\ll\lambda$
- The _induction term_ $\propto 1/r^2$ never dominates
- The _radiation term_ $\propto1/r$ will _dominate for large distances_ $r\gg\lambda\gg d$

![[Dipole field.png]]
- The electric field _starts to form closed loops_ as they are _pinched off_
	- They circulate in _different directions_

- In the _far field region_, only the _radiation fields_ remain:
$$E_{\theta}=\frac{\sin\theta}{4\pi\epsilon_{0}} \frac{[\ddot{p}]}{rc^{2}}\hspace{1.5cm}B_{\phi}=\frac{\mu_{0}\sin\theta}{4\pi} \frac{[\ddot{p}]}{rc}$$
	- The fields are _in phase_ with one another (with $[\ddot{p}]$)
	- The field components are _proportional_ to each other as $E_\theta=cB_\phi$, as expected for _electromagnetic waves_
	- The fields are _orthogonal in space_
	- There is a _radially outward Poynting flux_
	- The radiation is _polarised_

### Power radiated
- One can typically ignore the _induction fields_
	- It is _not purely radial_
	- It goes as $1/r^4$, which _does not correspond to a net outward energy flux_
	- The flux _redistributes energy_ close to the dipole instead
- In the _far field_:
$$N=\frac{1}{\mu_0}E_\theta B_\phi=\frac{\mu_0}{16\pi^2 c}\sin^2\theta\frac{[\ddot{p}]^2}{r^2}$$
- It goes as $1/r^2$ as expected

- The _angular distribution_ is
$$G(\theta,\phi)\propto\sin^2\theta$$
- It has _cylindrical symmetry_, with the _maximum radiated power_ in the _equatorial plane_, and _zero along the polar axes_

- The _instantaneous total radiated power_:
$$P-\int\bm{N}\cdot d\bm{S}=\frac{\mu_0}{6\pi c}[\ddot{p}]^2$$
- It is _independent of $r$_, so there is _no accumulation in energy_
	- All energy is simply _radiated outwards_

- Taking _time averages_:
$$\displaylines{\mean{N(r,\theta,\phi)}=\frac{\mu_0\omega^4p_0^2}{32\pi^2c}\frac{\sin^2\theta}{r^2} \\ \mean{P}=\frac{\mu_0\omega^4p_0^2}{12\pi c}=\frac{\omega^4p_0^2}{12\pi\epsilon_0c^3}}$$

## Multipole expansion
- Let there be some _system_ of _charges and currents sinusoidally varying in time_:
$$\rho(\boldsymbol{r},t)=\rho(\boldsymbol{r})\exp(-i\omega t)\hspace{1cm}\bm{J}(\boldsymbol{r},t)=\boldsymbol{J}(\boldsymbol{r})\exp(-i\omega t)$$

- In the _far field_:
$$\bm{A}(\bm{r}.t)=\frac{\mu_{0}}{4\pi}\int \frac{[\boldsymbol{J}]\,dV'}{|\boldsymbol{r}-\boldsymbol{r}'|} \equiv \boldsymbol{A}(\boldsymbol{r})\exp(-i\omega t) $$
- Writing $|\bm{r}-\bm{r}'|\approx r-\bm{n}\cdot\bm{r}'$, where $\bm{n}$ is _in the direction of $\bm{r}$_:
$$\bm{A}(\bm{r})=\frac{\mu_0}{4\pi}\frac{\exp(ikr)}{r} \int \boldsymbol{J}(\boldsymbol{r}') \exp(-ik\boldsymbol{n}\cdot \boldsymbol{r}')\, dV' $$

- Then, expand in _powers of_ $m$:
$$\bm{A}(\bm{r})=\frac{\mu_{0}}{4\pi} \frac{\exp(ikr)}{r} \sum_{m}  \frac{(-ik)^{m}}{m!} \int \boldsymbol{J}(\boldsymbol{r}')(\boldsymbol{n}\cdot \boldsymbol{r}')^{m} \, dV' $$
- If the _source dimension_ $d$ is _small compared to wavelength_ $(kd\ll1)$, then terms with $m>1$ will _fall off rapidly_

### Electrical dipole radiation term
- Using _integration by parts_:
$$\boldsymbol{A}(\boldsymbol{r})=\frac{\mu_{0}}{4\pi} \frac{\exp(ikr)}{r} \int \boldsymbol{J}(\boldsymbol{r}') \, dV'=-\frac{\mu_{0}}{4\pi} \frac{\exp(ikr)}{r} \int \boldsymbol{r}' (\nabla'\cdot \boldsymbol{J})\, dV'  $$

- Using _continuity_ $\nabla\cdot \boldsymbol{J}=i\omega \rho$
$$\bm{A}(\bm{r})=\frac{i\omega \mu_{0}}{4\pi} \frac{\exp(ikr)}{r} \int \boldsymbol{r}'\rho(\boldsymbol{r}') \, dV' =- \frac{i\omega \mu_{0}}{4\pi} \frac{\exp(ikr)}{r}\boldsymbol{p}$$
- This corresponds to the _electric dipole radiation_
### Magnetic dipole radiation term
- This can be _split_ into contributions, which are _symmetric_ and _antisymmetric_ in $\boldsymbol{J}$ and $\boldsymbol{r}'$
$$(\bm{n}\cdot\bm{r}')\bm{J}=\frac{1}{2}[(\boldsymbol{n}\cdot \boldsymbol{r}')\boldsymbol{J}+(\boldsymbol{n}\cdot \boldsymbol{J})\boldsymbol{r}']+\frac{1}{2}(\boldsymbol{r}'\times \boldsymbol{J})\times \boldsymbol{n}$$
- The _antisymmetric term_ is dependent on the _magnetic dipole moment_:
$$\displaylines{\bm{m}=\frac{1}{2}\int (\boldsymbol{r}\times \boldsymbol{J}) \, dV  \\ \bm{A}(\bm{r})=\frac{ik\mu_{0}}{4\pi}(\boldsymbol{n}\times \boldsymbol{m}) \frac{\exp(ikr)}{r}}$$
- This is the _magnetic dipole radiation term_

- $\bm{A}$ of a _magnetic dipole_ is _proportional to_ the [[#Magnetic field|magnetic field of an electric dipole]]
	- Follow from _Maxwell's equations_
	- Substitute $c\bm{p}\to\bm{m}$
- The _electric and magnetic fields_ are then:
$$\begin{aligned}\bm{B}(\bm{r})&=\frac{\mu_{0}k^{2}}{4\pi} [(\boldsymbol{n}\times \boldsymbol{m})\times \boldsymbol{n}] \frac{\exp(ikr)}{r} \\ \bm{E}(\bm{r})&=-\frac{Z_{0}k^{2}}{4\pi}(\boldsymbol{n}\times \boldsymbol{m}) \frac{\exp(ikr)}{r}\end{aligned}$$

- The _time-averaged total power radiated_
	- Analagous to the [[#Power radiated|electric dipole]]
$$\left<P^{\text{MD}}\right> = \frac{\mu_{0}\omega^{4}m_{0}^{2}}{12\pi c^{3}}$$

- If the electric and magnetic dipoles carry _similar currents_, with _similar sizes_:
$$\displaylines{p_{0} \sim \frac{I_{0}a}{\omega}\hspace{1.5cm}m_{0}\sim I_{0}a^{2} \\ \frac{\left<P^{\text{MD}}\right>}{\left<P^{\text{ED}}\right> }=\frac{m_{0}^{2}}{c^{2}p_{0}^{2}} \sim \left( \frac{2\pi a}{\lambda} \right)^{2}\ll 1}$$

- Therefore, _small magnetic dipoles are much less efficient_ than the _electric dipole_

### Quadrupole term
- Consider the _symmetric term_ of the $m=1$ contribution
- Using _integration by parts_:
$$\displaylines{\int \frac{1}{2}[(\boldsymbol{n}\cdot \boldsymbol{r}')\boldsymbol{J}+(\boldsymbol{n}\cdot \boldsymbol{J})\boldsymbol{r}'] \, dV'=-\frac{i\omega}{2} \int \boldsymbol{r}'(\boldsymbol{n}\cdot \boldsymbol{r}')\rho(\boldsymbol{r}') \, dV' \\ \boldsymbol{A}(\boldsymbol{r})= -\frac{\mu_{0}ck^{2}}{8\pi} \frac{\exp(ikr)}{r} \int \boldsymbol{r}'(\boldsymbol{n}\cdot \boldsymbol{r}')\rho(\boldsymbol{r}') \, dV' }  $$
- The fields are:
$$\begin{align}
\boldsymbol{B} &= ik\boldsymbol{n}\times \boldsymbol{A}=-\frac{ick^{3}\mu_{0}}{24\pi} \frac{\exp(ikr)}{r} \boldsymbol{n}\times \boldsymbol{Q}(\boldsymbol{n}) \\ \boldsymbol{E}&= \frac{ikZ_{0}}{\mu_{0}}(\boldsymbol{n}\times \boldsymbol{A})\times \boldsymbol{n}
\end{align}$$
- $\bm{Q}(\bm{n})$ is a _contraction_ of the _quadrupole moment tensor_:
$$\displaylines{\boldsymbol{Q}(\boldsymbol{n})=3\int \boldsymbol{r}'(\boldsymbol{n}\cdot \boldsymbol{r}')\rho(\boldsymbol{r}') \, dV'\\ Q_{\alpha}=Q_{\alpha\beta}n_{\beta} \\ Q_{\alpha\beta}=\int (3x_{\alpha}x_{\beta}-r^{2}\delta_{\alpha\beta}) \rho(\boldsymbol{r}')\,dV  }$$

- The _angular distribution_:
$$N(r,\theta,\phi)=\frac{\mu_{0}\omega^{6}}{1152\pi^{2}c^{3}} \frac{1}{r^{2}} \left| (\boldsymbol{n}\times \boldsymbol{Q}(\boldsymbol{n}))\times \boldsymbol{n} \right|^{2} $$
- The _total instantaneous power radiated_:
$$\left<P\right>^{\text{EQ}}=\frac{\mu_{0}\omega^{6}}{1440\pi c^{3}} \sum_{\alpha\beta}|Q_{\alpha\beta}|^{2}$$
- The quadrupole is a _very ineffective radiator_ than the corresponding _electric_ dipole with $ka\ll 1$
- It also has a _different power law dependence_ to $\omega$

- The _oscillating lateral quadrupole_
- The power distribution is _no longer cylindrically symmetric_
- There is _no power emitted along_ 

# Antennas
- Antennas are devices designed to _emit or receive EM waves_
	- Transmitting energy: electric/magnetic dipoles. quadrupoles

## As radiators
- Any antenna will _lose energy_ from whatever circuit it is _drawing power_ from
- This is reflected as a _radiation resistance_ $R_r$
$$R_r\equiv\mean{P}/\mean{I^2}=\mean{V^2}/\mean{P}$$
- For [[#Power radiated|the Hertzian electric dipole]] with $\dot{p}=Id$
$$\displaylines{\mean{P}=\frac{\mu_0\omega^4p_0^2}{12\pi c}=\frac{\mu_{0}\omega^{2}\langle \dot{p}^{2} \rangle}{6\pi c}  \\ R_r=\frac{\mu_{0}\omega^{2}}{6\pi c}d^{2}=\frac{2\pi}{c}Z_{0}\left( \frac{d}{\lambda} \right)^{2}}$$
- This is valid for $d\ll\lambda$ (approximation usually made for Hertzian dipole)

- The _power gain_ $G(\theta,\phi)$ quantifies the _directionality_ of the emitted radiation:
$$G(\theta,\phi)=\frac{N(\theta,\phi)}{(4\pi)^{-1}\int N \, d\Omega }$$

- For the Hertzian dipole:
$$G^{\text{ED}}(\theta,\phi)=\frac{3}{2}\sin^{2}\theta$$
## As receivers
- When there is an _incident EM wave_, it induces a _voltage_
- It can be treated as a _generator_ with voltage $V$ and _internal resistance_ $R_r$
![[Antenna receiver circuit.png]]
- Its _performance_ is quantified by the _power delivered to the load_ $R_\text{load}$
$$\displaylines{\mean{P}_\text{tot}=(R_{r}+R_\text{load})\langle I^{2} \rangle  \\ \mean{P}_\text{load}}$$
- $\mean{P}_\text{load}$ is maximised for a _matched load_ $R_\text{load}=R_r$

- The _effective area_ of the antenna, or the _absorption cross-section_ is:
$$A_\text{eff}(\theta,\phi)=$$
- One should then pick the _polarisation best-suited for reception_

- For the _Hertzian dipole_
- The _open circuit voltage_ is $V=Ed\sin\theta$

- This is the _same angular dependence as the power gain_
- It is also _independent of dipole size_
	- It is _much larger than the actual geometrical area_

- As the antenna _radiates_, a portion of the _incident power is re-radiated_

- The _incident_ and _re-radiated_ fields can _interfere_, so the _Poynting flux turns back towards the antenna_, increasing its effective area

## Relation between effective area and power gain
- From the results for the Hertzian dipole above:
$$A_\text{eff}(\theta,\phi)=\frac{\lambda^2}{4\pi}G(\theta,\phi)$$
- This is _true for any antenna_

- Consider _any antenna_ with a _matched load_ $R_r$, all in _thermal equilibrium_ at temperature $T$, in a _black-body_ environment with radiation _energy density_ $U(\nu)$
- For $h\nu\ll k_BT$, it is given by the [[Thermal Radiation|Rayleigh-Jeans formula]]
- The antenna only responds to _one polarisation_

- The _effective incident energy flux_

- The _power dissipated_ is

- Thermal equilibrium requires that there is a _compensating backflow_ of _power_ into space
	- Must apply for _all directions_
- This arises from _Johnson noise_, given by the _Nyquist formula_

- Equating the powers:

- This gives:
$$A_\text{eff}(\theta,\phi)=\frac{\lambda^2}{4\pi}G(\theta,\phi)$$
- This is _independent of antenna construction_
- A high _radiative efficiency_ will give a high _detection sensitivity_

## Centre-fed linear antenna
- A _practical antenna_ has _finite size_

- Example: an _open-ended_ transmission line, driven by an _oscillating voltage_
- There are then _current nodes/voltage antinodes_ at the _end_ of the line

- In the _far-field_ case, $r\gg L$:
$$\mean{N(r,\theta)}=$$
- As expected, there is _no $\phi$ dependence_

- It has _resonant_ behaviour with $L$
- The _half-wave_ antenna has $L=\lambda/2$, with gain:
$$G_{\lambda/2}(\theta)=$$
- It is _maximal_ in the _equatorial plane_, but is more _confined_
- It has a bigger _radiation resistance_ than the Hertzian dipole
	- More _efficient_, and more easily _matched_

## Antenna arrays
- Consider an _array of dipole antennas_, _oriented_ parallel to the $z-$axis and _arranged regularly_ along the $y-$axis with spacing $a$
- They are driven _in phase_ at frequency $\omega$

- The total $\bm{E}$ on the $xy-$plane $(\theta=\pi/2)$ is then affected by the _phase difference_ $ka\sin\phi$:
$$\bm{E}\sim\sum_{j=1}^\infty \exp[-ika\sin\phi(j-1)]=\frac{1-\exp[-iNka\sin\phi]}{1-\exp[-ika\sin\phi]}$$

- The Poynting flux has an _extra $\phi-$dependent factor_, similar to [[Optics#Diffraction|N-slit diffraction]]
- The array produces _directed beams_
	- The _width decreases_ as the _number of dipoles increases_
	- The direction can be _controlled_ by modifying the _spacing_

- As $A_\text{eff}(\theta,\phi)\sim G(\theta.\phi)$, they also act as _directional receivers_

- Directional antennas can also be acheived with a _single dipole_ using a _conductive reflector_, and _spaced director elements_ (passive dipoles, _absorbing and re-emitting_ radiation)
- This achieves a _highly directional output_
- There is a _forward lobe_, much _stronger_ than the backward lobe

# Light scattering
- If electromagnetic radiation is incident on a _particle_, it is _scattered_ in different directions

- Consider a _small particle_ with $a\ll\lambda$ so phase variations _across_ the particle are negligible
- If it is _polarisable_, then it [[#Electrical dipole radiation term|radiates]] with power:
$$\mean{P}=\frac{\mu_0\mean{\ddot{p}^2}}{6\pi c}$$
- The _cross-section_ is the _ratio_ of $\mean{P}$ to the _incident flux_:
$$\sigma=\frac{\mean{P}}{E_0^2/(2\mu_0c)}=\frac{\mu_0^2\mean{\ddot{p}^2}}{3\pi E_0^2}$$
- It is typically _independent_ of $E_0$

## Polarisation of scattered waves
- When light is scattered, the _polarisation is altered_

- Consider radiation _in the scattering plane_
![[Scattering plane.png]]
$$N_1=\frac{}{}\sin^2(\pi/2-\alpha)=\frac{}{}\cos^2(\alpha)$$

- Then consider polarisation _perpendicular to the scattering plane_
![[Scattering perpendicular.png]]
$$N_2=\frac{}{}$$
- For _unpolarised incoming radiation_ (an _incoherent equal superposition_):
$$\mean{\ddot{p}_x^2}=\mean{\ddot{p}_z^2}=\frac{\mean{\ddot{\bm{p}}^2}}{2}$$

- Write $N_2$ as $N_1+(N_2-N_1)$, as it is larger than $N_1$
	- There are _two mutually incoherent fluxes_ of magnitude $N_1$, corresponding to one _unpolarised beam_ of intensity $2N_1$
	- There is remaining _polarised flux_ of $N_2-N_1$
- For _unpolarised light_, the _degree of polarisation_ after scattering:
$$P=\frac{I_\text{pol}}{I_\text{tot}}=\frac{N_2-N_1}{N_2+N_1}=\frac{1-\cos^2\alpha}{1+\cos^2\alpha}$$

- There is _no scattered flux parallel to the induced dipole moment_
- This gives the [[#Boundary conditions|Brewster condition]], where the _reflected and refracted beams are perpendicular_

## Rayleigh scattering
- Rayleigh scattering comes from _small neutral particles_
- For each particle, the dipole moment has _amplitude_ $p_0=\alpha E_0$
- The scattering cross-section is:
$$\sigma=\frac{\mu_0\omega^4p_o^2/(12\pi c)}{c\epsilon_0E_0^2/2}=\frac{\mu_0^2\omega^4\alpha^2}{6\pi}=\frac{8\pi^3}{3}\mu_0^2c^4\alpha^2\frac{1}{\lambda^4}$$
- The $\lambda^{-4}$ dependence gives _stronger scattering for short wavelengths_

## Thomson scattering
- Consider $z-$polarised EM radiation incident on a _free electron_
	- The _Lorentz force_ is typically much _weaker_ and is ignored
- The equation of motion:
$$\displaylines{\ddot{z}=-\frac{e}{m_e}E_0\exp(-i\omega t) \\ \ddot{p}=-e\ddot{z}=\frac{e^2}{m_e}E_0\exp(-i\omega t)=-\omega^2p_0\exp(-i\omega t)}$$
- The _time-averaged scattered power_:
$$\mean{P}=$$
- The _Thomson cross-section_ is then:

- For _high-frequency light_, one must consider _photon momentum_, leading to _Compton scattering_

- Consider a _classical electron radius_ $r_e$ where the _electrical self-energy_ is equivalent to the _rest mass energy_:
$$\frac{e^2}{4\pi\epsilon_0r_e}=m_ec^2$$
- The Thompson scattering cross-section:
$$\sigma_T=\frac{8\pi}{3}r_e^2$$

## Dense media
- Consider when _many scatterers are present_

- Light scattered by one particle can then be _incoherently scattered by another particle_
- For a medium where particles have cross-section $\sigma$, mean _separation_ $d$, with _linear dimension_ $L$
- The chance of a _single scattering event_:
$$\frac{N\sigma}{L}\sim\frac{\sigma L}{d^3}$$
- When $\sigma L/d^3\ll1$, one can _ignore multiple scattering_

- Let there be $N$ _identical scatterers_ at positions $\{\bm{r}_j\}$
- Let it be illuminated by a _coherent_ wave with wavevector $\bm{k}_i$, with _resultant wavevector_ $\bm{k}_s$
![[Scattering many particles.png]]
- Define some _origin_, where the observed field is $\tilde{\bm{E}}\exp(-i\omega t)$
- The _additional phase from each particle_ is $(\bm{k}_i-\bm{k}_s)\cdot\bm{r}_j$

- Defining the _scattering wave-vector_ $\bm{q}$:
$$\displaylines{\bm{q}\equiv\bm{k}_i-\bm{k}_s \\ \tilde{\bm{E}}_\text{tot}=\tilde{\bm{E}}\exp(-i\omega t)\sum_{j=1}^N\exp(i\bm{q}\cdot\bm{r}_j)}$$
- The _total time-averaged radiated power_:
$$\displaylines{P_\text{tot}=\frac{1}{2Z_0}|\tilde{\bm{E}}_\text{tot}|^2=P_1(\bm{q})\left|\sum_{j=1}^N\exp(i\bm{q}\cdot\bm{r}_j)\right|^2 \\ P_1(\bm{q})\equiv|\tilde{\bm{E}}^2|/(2Z_0)}$$
- $P_1(\bm{q})$ is the _form factor_, the power resulting from a _single scatterer_ in the direction $\bm{k}_s=\bm{k}_i-\bm{q}$

- Define $\mathcal{F}(\bm{q})$, the _structure factor_:
$$\mathcal{F}(\bm{q})\equiv\left|\sum_{j=1}^N\exp(i\bm{q}\cdot\bm{r}_j)\right|^2\equiv\left|\text{FT}\left[\sum_{j=1}^N \delta(\bm{r}-\bm{r}_j)\right]\right|^2=\left|\text{FT}[n(\bm{r})]\right|^2=|\tilde{n}(\bm{q})|^2$$
- Here, $n(\bm{r})$ is the _particle density_ of the scatterers
- $\mathcal{F}(\bm{q})$ is the _Fourier transform squared_ of $n$
	- It is said to depend on _positional correlations_
	- Treat each term $\exp(i\bm{q}\cdot\bm{r}_j)$ as a _phasor_

- For an _ideal gas_, there is _no correlation_ between positions:
$$\mathcal{F}(\bm{q})=N\hspace{1.5cm}P_\text{tot}=NP_1$$
- There are _no interference effects_, as the intensities simply _add_

- For some spatial correlation (e.g. a _1D lattice_):
$$n(r)=\sum_{j=-\infty}^\infty\delta(r-jL)\Longrightarrow \tilde{n}(q)=\sum_{j=-\infty}^\infty \delta\left(q-j\frac{2\pi}{L}\right)$$
- One gets _strong scattering_ at $q=2\pi j/L$

- Scattering is typically _strongest_ from _density variations_ on lengthscales _comparable to incident wavelength_

- For a _general lattice_, the strongest peaks are given by $\bm{q}=\bm{G}$, the _reciprocal lattice vectors_, giving _Bragg's Law_:
$$\bm{k}_s=\bm{k}_i-\bm{G}$$

- For _transparent substances_, scattering can occur from _defects_ and _density fluctuations_
	- They typically appear in _liquids_ close to _phase separation_
	- For _phase separating liquids_, the _large density fluctuations_ lead to changes in _local refractive index_, which leads to _scattering_ and making the liquid appear _cloudy_

# Relativistic electrodynamics
- [[Special Relativity|Foundations of special relativity]]

- The _4-divergence_ and _Laplacian/d'Alembertian_:
$$\begin{aligned}\partial_\alpha A^\alpha&=\pd{A^0}{x^0}+\nabla\cdot\bm{A}  \\ \Box^2\equiv\partial_\alpha\partial^\alpha&=\pd{^2}{x_0^2}-\nabla^2\end{aligned}$$

## The 4-current
- From experiment, the _total charge_ in some _region_ of space-time is _Lorentz invariant_
- Given some region, with _charge density_ $\rho_0$ in its _instantaneous rest frame_

- Define the _4-current_:
$$\vec{J}=(c\rho,\bm{J})=\rho_0\frac{d}{d\tau}(ct,\bm{r})$$
- The _continuity equation_:
$$\partial_\alpha J^\alpha=\pd{\rho}{t}+\div\bm{J}=0$$
- Applying a _Lorentz transformation_:
$$\begin{aligned}c\rho'&=\gamma(c\rho-\beta J_x) \\ J_x'&=\gamma(J_x-\beta c\rho) \\ J_y'&=J_y \\ J_z'&=J_z\end{aligned}$$

- Writing components _parallel and perpendicular to the boost_:
$$c\rho'=\gamma(c\rho-\beta\cdot\bm{J})\hspace{1.5cm}\bm{J}'=\gamma(\bm{J}_{||}-c\rho\bm{\beta})+\bm{J}_\perp$$
## Maxwell's equations
- Consider [[#Maxwell's equations in terms of potentials]]:
$$\Box^2\phi=\frac{\rho}{\epsilon_0}\hspace{1.5cm}\Box^2\bm{A}=\mu_0\bm{J}$$
- Then define the _4-potential_ $\vec{A}$ such that:
$$\displaylines{\vec{A}=\left(\frac{\phi}{c},\bm{A}\right) \\ \Box^2\vec{A}=\mu_0\vec{J}}$$
- $\Box^2$ is _Lorentz invariant_ and $\vec{J}$ is a 4-vector, hence $\vec{A}$ must be a _4-vector_

- Introduce the _anti-symmetric field-strength tensor_:
$$\displaylines{F^{\alpha\beta}=\partial^\alpha A^\beta-\partial^\beta A^\alpha \\ F^{i0}=E^i \hspace{1cm} F^{ij}=-\epsilon^{ijk}B^k \\ F^{\alpha\beta}=\pmatrix{0&-E_x/c&-E_y/c&-E_z/c \\ E_x/c&0&-B_z&B_y \\ E_y/c&B_z&0&-B_x \\ E_z/c&B_y&B_z&0}}$$

- Maxwell's equations then become:
$$\begin{aligned}\partial_\alpha F_{\beta\gamma}+\partial_\beta F_{\gamma\alpha}+\partial_\gamma F_{\alpha\beta}&=0 \\ \partial_\alpha F^{\alpha\beta}&=\mu_0 J^\beta\end{aligned}$$

## Lorentz force law
- Given _4-momentum_ $\vec{p}$, and _4-velocity_ $\vec{U}$, the _Lorentz force law_ is:
$$\frac{dp^\alpha}{d\tau}=m\frac{dU^\alpha}{d\tau}=qF^{\alpha\beta}U_\beta$$

## Gauge invariance
- As the field tensor is a _physical quantity_, it must be _gauge invariant_:
$$\displaylines{A_\alpha\to A_\alpha+\partial_\alpha \lambda(x) \\ F_{\alpha\beta}\to F_{\alpha\beta}}$$
- The _divergence_ of the 4-potential must be _Lorentz invariant_
- The _Lorenz gauge_ will _zero_ the _4-divergence_:
$$\partial_\alpha A^\alpha=\frac{1}{c^2}\pd{\phi}{t}+\div\bm{A}=0$$

## Transformations of fields
- _Transforming_ the field strength tensor:
$$\displaylines{F'^{\alpha\beta}=\tenscom{\Lambda}{\alpha}{\gamma}\tenscom{\Lambda}{\beta}{\delta}F^{\gamma\delta} \\ \tenscom{\Lambda}{\alpha}{\gamma}=\pmatrix{\gamma&-\beta\gamma&0
&0\\-\beta\gamma&\gamma&0&0\\0&0&1&0\\0&0&0&1}}$$
- One gets that the _fields along the boost direction_ are _unchanged_
$$\begin{aligned}E_x'&=E_x\hspace{3.5cm}B_x'=B_x \\ E_y'&=\gamma(E_y-vB_z)\hspace{1.55cm}B_y'=\gamma(B_y+\frac{v}{c^2}E_z) \\ E_z'&=\gamma(E_z+vB_y)\hspace{1.55cm}B_z'=\gamma(B_z-\frac{v}{c^2}E_y) \end{aligned}$$
- Writing in terms of _parallel and perpendicular components_:
$$\begin{aligned}\bm{E}_{||}'&=\bm{E}_{||} \hspace{3.5cm} \bm{B}_{||}'=\bm{B}_{||} \\ \bm{E}_\perp'&=\gamma(\bm{E}_\perp+\bm{v}\times\bm{B}_\perp)\hspace{0.6cm}\bm{B}'_\perp=\gamma\left(\bm{B}_\perp-\frac{1}{c^2}\bm{v}\times\bm{E}_\perp\right)\end{aligned}$$
- This reveals that the _electric and magnetic fields_ are part of the _same phenomenon_, depending on the _inertial frame_
## Magnetism as a relativistic effect
- Consider a _wire_ carrying a _current_, wjhere the _charge carriers_ are moving at speed $V$
- There is a _charge_ $q$ moving at speed $u$ _parallel_ to the wire
![[Wire.png]]
- The _positive charges_ give the _electrostatic force_:
$$f_y^+=\frac{q}{2\pi\epsilon_0}\frac{neA}{r}$$
- In the _instantaneous rest frame_ of the charges, $\rho_x'=\rho_x/\gamma_v$:
- Force from the _negative charges_:
$$(f_y^-)'=-\frac{1}{\gamma_v}\frac{q}{2\pi\epsilon_0}\frac{neA}{r}$$
- Carrying a [[Special Relativity#Lorentz transformations|Lorentz transformation]]:
$$f_y^-=\gamma_v\left(1-\frac{vu}{c^2}\right)(f_y^-)'$$
- _Adding_ the forces:
$$f_y=f_y^++f_y^-=-\frac{\mu_0I}{2\pi r}u$$
- This is the Lorentz force given by _Ampere's law_

- _Lorentz transformed electrostatic forces_ give a _magnetic_ force 

### Spin-orbit coupling
- Consider in an _atom_:
$$\bm{B}'_\perp=\gamma\left(\bm{B}_\perp-\frac{1}{c^2}\bm{v}\times\bm{E}_\perp\right)$$
- In the _rest frame_ of the _nucleus_, there is only an _electric field_
- This generates a _magnetic field_ in the _electron frame_, which interacts with the _spin_

- The [[The hydrogen atom#Spin-orbit correction|spin-orbit Hamiltonian]]:
$$\displaylines{\bm{E}=-\frac{\bm{r}}{r}\frac{d\Phi}{dr} \\ \hat{H}_{SO}=-\frac{1}{2}\frac{g_Se}{2m}\hat{\bm{S}}\cdot\hat{\bm{B}}'=-\frac{g_Se}{4mc^2}\hat{\bm{S}}\cdot(\hat{\bm{v}}\times\frac{\hat{\bm{r}}}{r})\frac{d\Phi}{dr}=-\frac{g_Se}{4m^2c^2}\hat{\bm{S}}\cdot\hat{\bm{L}}\frac{1}{r}\frac{d\Phi}{dr}}$$
- _Approximation_: $\gamma\approx 1$
- Factor of $1/2$: _Thomas precession_ (Rotation of electron rest frame)

# Radiation

## A uniformly moving charge
![[Uniformly moving charge.png]]
- In the frame $S'$, the field is _static_:
$$\bm{E}'=\frac{q}{4\pi\epsilon_0}\left(\frac{x'}{r^3},\frac{y'}{r^3},0\right)\hspace{1.5cm}\boldsymbol{B}=(0,0,0)$$
- Carrying out the [[#Transformations of fields|Lorentz transformation]]
$$\displaylines{E_{x}=\frac{q}{4\pi\epsilon_{0}}\frac{x'}{r'^{3}}\hspace{1.5cm}E_{y}=\frac{q}{4\pi\epsilon_{0}}\frac{\gamma y'}{r'^{3}}\hspace{1.5cm}E_{z}=0 \\ B_{x}=0\hspace{1.5cm}B_{y}=0\hspace{1.5cm}B_{z}=\frac{\gamma v}{c^{2}}E_{y}'}$$

- Taking the $x-$axis as the _polar axis_, with $x'=\gamma x$ and $y'=y$, _at_ $t=t'=0$
$$r'^{2}=x'^{2}+y'^{2}=\gamma^{2}r^{2}\left( 1-\frac{v^{2}}{c^{2}}\sin^{2}\theta \right)$$
- This gives the fields:
$$\displaylines{E_{x}=\frac{1}{4\pi\epsilon_{0}}\frac{\cos\theta}{\gamma^{2}r^{2}(1-v^{2}\sin^{2}\theta/c^{2})^{3/2}}\hspace{1.5cm}E_{y}=\frac{1}{4\pi\epsilon_{0}}\frac{\sin\theta}{\gamma^{2}r^{2}(1-v^{2}\sin^{2}\theta/c^{2})^{3/2}} \\ B_{z}=\frac{v}{c^{2}}E_{y}}$$
- With this geometry, $E_{x}$ is _parallel_ $(E_{//})$, $E_{y}$ is _perpendicular_ $(E_{\perp})$, and $\boldsymbol{B}$ is _azimuthal_

- $\bm{E}$ has a $1/r^2$ dependence, hence the _Poynting flux_ $\bm{N}\sim 1/r^4$

- $\bm{E}$ is _purely radial_, hence the field is _always directed away from the origin_
	- $E_\perp/E_{||}=\sin\theta/\cos\theta$
	- The _magnitude_ has an _angular dependence_
	- It is evaluated at _retarded time_, but the _Lorentz transformation_ makes it less apparent

- For $\gamma\sim 1$, it reduces to the _non-relativistic result_, where the field is _isotropic_
- For $\gamma\gg1$, the field is _flattened_ to the plane _perpendicular to motion_:
$$E_{||}\sim\frac{1}{\gamma^2}\frac{q}{4\pi\epsilon_0r^2}\hspace{1.5cm}E_\perp\sim\frac{\gamma q}{4\pi\epsilon_0r^2}$$
![[Field of moving charge.png]]
- $\bm{N}$ is _tangentially oriented_
	- _Maximum_ at $\theta=\pi/2$, and _zero_ for $\theta=0$
- As $\bm{N}\sim 1/r^4$, the charge _does not radiate_, and simply _moves energy along the charge_

## Cherenkov radiation
- In a _medium_ of refractive index $n=\sqrt{\epsilon(\omega)}$, it is possible for the _velocity of the charge to exceed the speed of light_:
$$v>\frac{c}{n}$$
- The medium is _moving_ in $S'$

- The _solutions_ to Maxwell's equations are given using [[#Solving for the potentials|retarded potentials]]
$$[\phi]=\phi\left(t-\frac{|\bm{r}-\bm{r}'|}{c/n}\right)$$

- It is moving _faster than the propagation of information_
- There is a region where the _potentials are zero_
- There is a _growing cone_ of _non-zero field_, hence there must be _energy transfer_
- The Huygens construction:
![[Cherenkov radiation.png]]

- The radiation is propagating in the _Cherenkov angle_:
$$\cos\theta_C=\frac{cT/n}{vT}=\frac{c}{nv}=\frac{1}{\beta n}$$
- Assume that the _rate of energy loss of the particle_ is _small_, hence the angle is _constant_
- As $n=n(\omega)$, different _frequencies_ radiate in _different angles_

### The fields
- Solve for potentials using _Fourier transforms_:
$$F(\bm{r},t)=\frac{1}{(2\pi)^2}\int\int \tilde{F}(\bm{k},\omega)\,d\bm{k}\,d\omega$$

- The _plane wave solutions_

- Arriving from _source terms_:

- Maxwell's equations then become:
$$\begin{aligned}\left(k^2-\epsilon(\omega)\frac{\omega^2}{c^2}\right)\tilde{\phi}(\bm{k},\omega)&=\frac{1}{\epsilon(\omega)\epsilon_0}\tilde{\rho}(\bm{k},\omega) \\ (\tilde{\bm{A}})&=\end{aligned}$$
- The fields are then obtained by:

- _Radiation_ is only emitted when $\epsilon(\omega)$ is real, and $\beta^2\epsilon(\omega)>1$, hence:
$$v>\frac{c}{\sqrt{\epsilon(\omega)}}$$
- For most materials, this _restricts_ radiation to a _high optical frequency band_
- It is typically _blue_

## A general accelerating charge
- A _uniformly moving charge_ can _never radiate in vacuum_
	- Not in vacuum: Cherenkov condition
- An _accelerating_ charge can radiate in _vacuum_

- A _sudden deceleration_:
![[Decelerating charge radiation.png]]
- Electric field lines are _always continuous_ in a charge-free region

- When the charge _abruptly decelerates_, for an observer _far away_, one still experiences _field as if from a uniformly moving charge_, from the position where it _would have been_
- For a _near observer_, it emanates from the _true position_
- Therefore, the field has a _transverse kink_

- There is some _characteristic time_ $T=|\bm{u}|/|\bm{a}|$
- This sets the _characteristic wavelength_ $\lambda\sim c|\bm{u}|/|\bm{a}|$

### The Lienart-Wirchert potentials
- Potentials from 4-current, evaluated at [[#Solving for the potentials|retarded time]]:
$$\begin{align}
\phi(r,t)&=\frac{1}{4\pi\epsilon_0}\int_\text{all space}\frac{\rho(\bm{r}',t-|\bm{r}-\bm{r}'|/c)}{|\bm{r}-\bm{r}'|}\,dV \\ \boldsymbol{A}(r,t)&=\frac{\mu_{0}}{4\pi}\int_\text{all space}\frac{\boldsymbol{J}(\bm{r}',t-|\bm{r}-\bm{r}'|/c)}{|\bm{r}-\bm{r}'|}\,dV
\end{align}$$
- Evaluation at retarded time can also be written in _covariant form_:
$$A^{\alpha}(x^{\mu})= \frac{\mu_{0}}{4\pi} \int \frac{\theta(x_{0}-x_{0}')}{|\boldsymbol{r}-\boldsymbol{r}'|} \delta(x_{0}-x_{0}'-|\boldsymbol{r}-\boldsymbol{r}'|)J^{\alpha}(x'^{\mu}) \, d^{4}x' $$

- The _solutions_ to the 4-potential are the _Lienard-Wiechert potentials_:
$$A^\alpha(x^\mu)=\frac{\mu_0ec}{4\pi}\left[\frac{V^\alpha(\tau)}{V^\nu[x_\nu-r_\nu(\tau)]}\right]_{\tau=\tau_0}$$
- The _light-cone condition_ implies:
$$\displaylines{x_0-}$$
- The potetials can then be written as:

### The fields
$$\begin{aligned}\bm{E}(\bm{x},t)&= \\ \bm{B}(\bm{x},t)&=\end{aligned}$$
- The first term for the fields gives the _velocity fields_, which are _dependent on acceleration_
- They are _static_, and _do not radiate_
- For a charge with _uniform velocity_, it reproduces the field for [[#A uniformly moving charge]]

- The second term gives the _acceleration fields_, which drop off as $R^{-1}$, and are responsible for _radiation_

### Larmor and Lienart formulae
- Consider an _accelerating_ charge in the _non-relativistic_ limit, the _acceleration field_ is:
$$\bm{E}_a=$$
- The _power radiated per solid angle_:

- The _total radiated power_ is then given by the _Larmor formula_:
$$P=\frac{\mu_0e^2}{6\pi c}|\dot{\bm{v}}|^2$$
- This can be interpreted as an _electric dipole_ with $p=ez$

- In some _general frame_, where the charge is _relativistic_
- The power radiated is a _Lorentz invariant_
	- In the _instantaneous rest frame_, one expects a $\sin^2\theta$ dependence so there is _no net 3-momentum_, yet there is lost _4-momentum_ $dP'^\mu=(dE'/c,0,0,0)$
	- Transforming to the _lab frame_, $dE=\gamma dE'$ and $dt=\gamma dt'$, hence _power loss is the same in all inertial frames_
- Working in the instantaneous rest frame, the _4-acceleration_ is $(0,\bm{\alpha})$, where $\bm{\alpha}$ is the _proper acceleration_
- From invariance of the inner product, $-\alpha^2=A^\mu A_\mu$
- The _relativistic Larmor formula/Lienart formula_ is then:
$$P=\frac{\mu_0e^2}{6\pi c}|\alpha|^2$$

## Circular motion
- Consider a particle moving in a _unifrm magnetic field_:
$$\frac{d\bm{p}}{dt}=\frac{d(\gamma_um\bm{u})}{dt}=e(\bm{u}\times\bm{B})$$
- The particle's _energy_ is _constant_
- However, it must _radiate energy_
	- Assume it is _small relative to kinetic energy_, or it is _maintained_ (e.g. particle accelerator)

- Taking $u_z=0$, one finds:
$$\omega_B=\frac{eB}{\gamma m}$$
- With _radial acceleration_:
$$a_\perp=\frac{evB}{\gamma m}$$
- Substituting into the Lienard formula:
$$P=\frac{\mu_0e^4\gamma^2B^2v^2}{6\pi cm^2}$$
- The radiation is _not necessarily harmonic_
	- Dependent on _wavelength_ and _orbital radius_

### Cyclotron motion
- For $v\ll c$, $\gamma\to1$, and the motion is _non-relativistic circular motion_:
$$\lambda=\frac{2\pi c}{\omega_B}\gg\frac{v}{\omega_B}=R$$
- Therefore, the [[#The Hertzian electric dipole|dipole approximation]] _applies_
- It can be considered a _superposition of two perpendicular Hertzian dipoles_:
$$\bm{p}(t)=$$
- One expects _monochromatic_ radiation at angular frequency $\omega_B$

- As they are _quadrature in phase_, the _time-averaged Poynting fluxes add_:
$$\mean{P}=$$

- The _polarisation_ of the radiation depeneds on the _direction of emission_
	- In the _equatorial plane_, only

### Synchotron radiation
- For $v\to c$, $\gamma\gg1$, the motion is _highly relativistic_

- The _characteristic wavelength_ is _much smaller_ than $R$, hence the _dipole approximation does not apply_
- There is  _continuous chear_ in the field lines, hence there is a _continuum_ of frequencies

- The _instantaneous_ radiated power is still given by the Lienard formula

- The $Oz$ axis is now taken as the _direction of the speed of the particle_:
![[synchotron geometry.png]]
- The _angular distribution_ can be written as:
$$G(\theta',\phi')=1-\sin^2\theta'\cos^2\phi'$$
- Maths

- The _power radiated per unit angle_, in the _particle frame_:
$$\frac{dP(t')}{d\Omega}=$$
- The angular distribution is _dependent on the relative orientations_ of $\bm{\beta}$ and $\dot{\bm{\beta}}$
- The _denominator_ results in a _strong forward focusing_ of the radiation in direction $\bm{n}||\bm{\beta}$

- For _circular motion_, where $\bm{\beta}\perp\dot{\bm{\beta}}$ the formula above becomes:
$$\frac{dP(t')}{d\Omega}=$$
![[Synchotron radiation distribution.png]]

- As $\beta$ increases, the power becomes _more confined in the forward direction_
	- The _rearward lobe_ becomes _weaker_
- The _angle_ separating the lobes is $\sim 1/\gamma$
	- A stationary observer only receives radiation when the line of sight is _almost tangential_ to the circular path
![[Synchotron radiation pulse.png]]
- The _duration_ of the pulse is:
$$\Delta t=\frac{2R}{\gamma v}+\frac{1}{c}\left[d-\frac{R}{\gamma}-\left(d+\frac{R}{\gamma}\right)\right]\approx\frac{1}{\gamma^3\omega_B}$$
- The radiation is then _spectrally broad_:
$$\nu_s\sim\gamma^3\omega_B \hspace{1.5cm}\lambda_s\sim \frac{R}{\gamma^3}\ll R$$
- Typical spectrum:
![[synchotron spectrum.png]]