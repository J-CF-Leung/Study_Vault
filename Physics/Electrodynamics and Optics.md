
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
- _Effective susceptibilities_

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
- This can only be true for _purely monochromatic waves_

- From _Fourier analysis_, purely monochromatic waves must have _infinite spatial and temporal extent_
- Hence, _real_ sources can only be _quasi-monochromatic_

- The _theory of coherence_ describes _non-monochromatic_ waves _quantitatively_
### Power spectra
- Let there be some _time-dependent function_ $f(t)$
- Take its [[Fourier series and transforms|Fourier transform]]:
$$f(t)=\frac{1}{2\pi}\int_{-\infty}^\infty F(\omega)\exp(i\omega t)\,d\omega \hspace{1cm} F(\omega)=\int_{-\infty}^\infty f(t)\exp(-i\omega t)\,dt$$
- The _power_ in frequency range $\omega$ to $\omega+d\omega$ is the _power spectrum_:
$$P(\omega)\,d\omega=|F(\omega)|^2\,d\omega$$

### Light sources

#### Laser
- Light produced by _stimulated emission_
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
	$$P(\omega)\sim \exp\left(-\frac{m(\omega-\omega_0)^2c^2}{2\omega_0^2 k_BBT}\right)=\exp\left(-\frac{(\omega-\omega_0)^2}{2\sigma^2}\right)$$
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

- Suppose there are two measurements:
	- $f_1$ at $\bm{r}_1$ at time $t$
	- $f_2$ at $\bm{r}_2$ at time $t-\tau$
- Then define the _mutual coherence function_:
$$\Gamma(\bm{r}_1,\bm{r}_2,\tau)=\mean{f_1(\bm{r}_1,t)f_2^*(\bm{r}_2,t-\tau)}$$
- This assumes there is _correlation_ in the behaviour after $\tau$ across time $t$

- By _normalising intensity_, one gets the _degree of mutual coherence_:
$$\displaylines{\gamma(\bm{r}_1,\bm{r}_2,\tau)=\frac{\Gamma(\bm{r}_1,\bm{r}_2,\tau)}{\sqrt{I_1I_2}} \\ I_i=\Gamma(\bm{r}_1,\bm{r}_1,0) \\ 0<\gamma<1}$$

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
- One then observes _fringes_, with _contrast_ $V$:
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

- Define _relative intensity_

- Therefore one can write $P(\omega)$ as:

### Fourier transform spectroscopy
- The _Michelson interferometer_:
![[Michelson interferometer.png]]
- The _compensator plate_ eliminates phase difference due to _optical path in glass_
- Typical _advantages_:
	- Radiation _throughput_ is higher as it is _not limited by slit width_
	- The _signal-to-noise ratio_ is higher as the signal _continuously falls on the detector_
	- The _spectral resolution_ is given by $\lambda/\delta\lambda\approx 2d/\lambda=m$, where $m$ is the _number of fringes recorded_

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

- If the _angular width_ of the source is $\alpha$, then fringes are _offset_ by $\alpha D$
- The _fringe spacing_ is $\lambda D/d$, hence one _loses contrast_ if:
$$\alpha D>\frac{\lambda D}{d}\Longrightarrow d>\frac{\lambda}{\alpha}\approx w_c$$
- It gives _coherence variations across the wavefield_, or _spatial/lateral coherence_
	- _Temporal coherence_ is _along_ the beam, or _longitudinal_
- $w_c$ is known as the _coherence width_

- For the _two rays_:
$$k(\rho_1+r_1-\rho_2-r_2)= kd(\sin\theta+\sin\chi)\approx kd\left(\frac{x}{L}+\frac{y}{D}\right)=2ks$$
- Given some _intensity profile_ at the _source_, the _amplitude_ at $P$ is then:
$$\psi(y)\sim\sqrt{I(x)}\exp[ik(\rho+R)](e^{iks}+e^{-iks})=2\sqrt{I(x)}\exp[ik(\rho+R)]\cos(ks)$$

- If the extended source is _incoherent_ (beams from different points are _uncorrelated_), then the _net intensity as a function of $d$_ is obtained by _summing intensities_:
$$\begin{aligned}I_y(d)&=\int |\psi(y)|^2\,dx=4\int I(x)\cos^2(2ks)\,dx \\ &=2I_0+2\Re\left[\exp(-ikdy/D)\int I(x)\exp(-ikdx/L)\,dx\right]\end{aligned}$$
- Then by _changing variables_, with $x=L\theta$, $y=d\chi$, and $I(x)\,dx=I(\theta)\,d\theta$, with $kd=u$:
$$I_y(u)=2I_0+2I_0\Re[\exp(-iu\chi)\gamma(u)]$$
- Defining $\gamma(u)$, as well as a phase $\beta$:
$$\displaylines{\gamma(u)=\frac{1}{I_0}\int I(\theta)\,\exp(-iu\theta)\,d\theta=\frac{\mathcal{F}[I(\theta)]}{I_0}\equiv|\gamma(u)|\exp(-i\beta) \\ I_y(u)=2I_0+2I_0|\gamma(u)|\cos\left(\beta+\frac{kdy}{D}\right)}$$
- There are $\cos^2$ fringes with _spacing_ determined by $kdy/D$
- $|\gamma(u)|$ defines the _fringe contrast_ at point $y$
- There is some _offset_ $\beta$, determined by the _angular profile_ $I(\theta)$

- For a _symmetric source profile_ (about the axis):
$$\beta=\begin{cases}0&\gamma(u)>0 \\ \pi&\gamma(u)<0\end{cases}$$
- The _visibility_ of the fringes is defined by:
$$V=\gamma(u=kd)$$
- It can be _negative_ (if a minimum occurs where a _maximum_ is expected)

- The visibility gives the _intensity profile_ of the source 
- Define $\gamma(u)$ as the _degree of lateral coherence_
	- The _van Cittert-Zernike theorem_
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
$$\bm{A}=\frac{\mu_0}{4\pi}\int\frac{Id\bm{r}'}{|\bm{r}-\bm{r}'|}$$
- For a _distant loop_, make the approximation:
$$|\bm{r}-\bm{r}'|^{-1}=$$
- "Mathematical jiggery-pokery"

- One gets the expression:
$$\bm{A}(\bm{r})=\frac{\mu_0}{4\pi}\left[\oint_L\frac{I}{2}\bm{r}'\times d\bm{r}'\right]\frac{\bm{r}}{r^3}=\frac{\mu_0}{4\pi}\frac{\bm{m}\times\bm{r}}{r^3}$$
- For a _planar loop_, the integral is $IS\hat{\bm{n}}$, where $S\hat{\bm{n}}$ is the _vector area_:
$$\bm{m}=IS\hat{\bm{n}}$$
- $\bm{m}$ is the _magnetic dipole_
