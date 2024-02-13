- _Scattering_ is a common phenomenon, where particles _approach each other from infinity_, _interact_ in close proximity, then _continue in an altered trajectory_
	- [[Phonons#Phonon-phonon scattering|Phonon scattering]] is responsible for properties in solids
	- [[Electrodynamics and Optics#Light scattering|Light scattering]] affects optical properties
	- Also occurs in [[Quantum scattering theory|quantum systems]]

- They are also used as an _experimental probe_ (Neutron/X-ray scattering)

![[Scattering.png]]

- Typically, in a _scattering experiment_, one measures _particle flux_ at a _detector_
	- The incoming beam has a _spread of particle energies_
	- The incoming _particle flux varies_ with _transverse position_ across the beam
	- The target may have an _irregular shape_
	- The detector covers a _finite spread_ of scattering angles $(\theta,\phi)$

# Scattering cross-sections

## Differential cross-section
- Let there be a _single scattering target_ (test particle)
- It is illuminated with a _mono-energetic_ beam of _infinite transverse extent_, and _uniform flux_ (a _plane wave_)
- Consider scattered particles directed to an infinitesimal _solid angle element_ $d\Omega$, in the _direction_ $(\theta,\phi)$
![[Scattering target.png|500]]

- The _incident flux_ $j$  is the _number of incoming particles, per unit time per unit transverse area_

- The scattering _rate_ as a function of _angle_ is quantified by the _differential scattering cross-section_, defined _per target particle_:
$$\frac{d\sigma}{d\Omega}\equiv \frac{\text{no. of particles scattered/unit time into }d\Omega}{\text{incident flux}\times d\Omega}$$

- It is _dependent_ on:
	- The _nature_ of both the _incoming_ and _target_ particles
	- The _beam energy_
	- The _scattering angles_ $(\theta,\phi)$
- It is _independent_ of targert density/geometry, or beam _intensity_ or profile

- It is often written in terms of the _scattering amplitude_ $f(\theta,\phi)$
$$\frac{d\sigma}{d\Omega}=|f(\theta,\Omega)|^{2}$$
- This is often _useful_ to understand the reaction
	- Example: [[Atomic transitions#Angular distribution of spontaneous decay|angular momentum conservation in spontaneous decay]]

## Total scattering cross-section
- The _total scattering cross-section_ $\sigma$ characterises scattering rate _across all angles_
- It is defined _per unit particle_:
$$\sigma\equiv \frac{\text{no. of particles scattered/unit time}}{\text{incident flux}}$$

- It is a _single quantity_, which is _independent of_ $(\theta,\phi)$
$$\sigma=\int \frac{d\sigma}{d\Omega}\,d\Omega=\int _{0}^{2\pi}\int _{-1}^{1} \frac{d\sigma}{d\Omega}\,d\cos\theta  \,d\phi  $$
- It has dimensions of _area_

## Measuring the cross-section
- Let there be a _small, homogeneous target_ with $N_T$ particles, covering area $A$ 
- It is illuminated by a _wide, uniform, monoenergetic beam_, which has $N_\text{in}$ particles _incident_ within time $T$
- Let the target be _thin_ enough that particles only scatter _once_

- The _total number of scattered particles_ in time $T$ is $N_\text{scatt}$
- The _fraction of scattered particles_:
$$f_\text{scatt}=\frac{N_\text{scatt}}{N_\text{in}}$$

- The _total scattering cross-section_ is:
$$\sigma=\frac{N_\text{scatt}/T}{N_{T}N_\text{in}/(TA)}=f_\text{scatt}\frac{A}{N_{T}}$$

- For a _uniform foil_ of density $\rho$, of mass $m$, $A/N_T=m/\rho$, depending on the _nature_ of the target instead of the _geometry_

- If the _detector_ covers solid angle $\Delta\Omega$ in direction $(\theta,\phi)$, measuring number of particles $N_\text{scatt}^{\Delta\Omega}$ the differential cross-section measured:
$$\frac{d\sigma}{d\Omega}(\theta.\phi)=\frac{N_\text{scatt}^{\Delta\Omega}}{N_\text{in}}\frac{A}{N_{T}}\frac{1}{\Delta\Omega}$$

## Interpreting the cross-section
- The _total cross-section_ $\sigma$ has dimensions of _area_
- It is an _effective transverse area_ of each _scattering particle_

- The _effective area_ of the target, where each particle has _effective area_ $\sigma _\text{eff}$
$$A_\text{eff}=N_{T}\sigma _\text{eff}$$

- If the _physical area_ of the target is $A$:
$$f_\text{scatt}=\frac{A_\text{eff}}{A}=\frac{N_{T}\sigma}{A}$$
- One then gets:
$$\sigma=\sigma _\text{eff}$$

# Classical scattering
- Consider scattering in some _central potential_ $V(r)$
- Classical particles follow a _well-defined trajectory_
![[Classical scattering.png]]

- The _impact parameter_ $b$ has a _one-to-one correspondence_ with $\theta$:
$$b=b(\theta)$$
- _Incoming_ particles between $b$ and $b+db$ are _scattered_ into solid angle $d\Omega=2\pi(d\cos\theta)$
- One gets the cross-section:
$$\frac{d\sigma}{d\Omega}=\frac{j(2\pi b\,db)}{j(d\Omega)}=b(\theta)\left|\frac{db}{d(\cos\theta)}\right|$$

## Hard sphere scattering
- In the case of a _hard sphere_:
![[Hard sphere scattering.png]]
- The impact parameter:
$$b=R\sin\alpha=R\sin\frac{\theta}{2}$$
- One then gets the cross-section:
$$\frac{d\sigma}{d\Omega}=b(\theta)\left|\frac{db}{d(\cos\theta)}\right|=\frac{1}{4}R^{2}$$
- It is _independent_ of $\theta$

- The _total scattering cross-section_:
$$\sigma=\int \frac{d\sigma}{d\Omega} \, d\Omega=\pi R^{2} $$
- It is the _projected/transverse area_ of the sphere

## Coulomb scattering
- Consider _classical_ [[Orbits#Repulsive potential/Rutherford scattering|Coulomb/Rutherford scattering]]
$$V(r)=\frac{C}{r}\hspace{1.5cm}C=\frac{Z_{1}Z_{2}e^{2}}{4\pi\epsilon_{0}}$$
![[Coulomb scattering.png]]
- One can find the _impact parameter_:
$$b=\frac{|C|}{2E}\cot\frac{\theta}{2}$$
- This leads to the _Rutherford formula_:
$$\frac{d\sigma}{d\Omega}=\frac{C^{2}}{16E^{2}}\frac{1}{\sin^{4}(\theta/2)}$$