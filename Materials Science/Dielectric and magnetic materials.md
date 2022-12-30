## Dielectrics
### Polarisation of materials
- Polarisation mechanisms:
	- Electronic: electron cloud distortion
	- Ionic: eleastic distortion of ionic bonds
	- Molecular: rotation of pre-existing dipole moments
- Definition of displacement and polarisation vectors:
	- [[Electromagnetism#Homogeneous Dielectrics]]
### Capacitors
- Empty parallel plate capacitor
$$C_0=\frac{Q}{V}=\frac{\sigma A}{El}=\frac{\epsilon_0 A}{l}$$
- Parallel plate capacitor with dielectric inserted
$$C'=\frac{\sigma_f A}{El}=\kappa \frac{\epsilon_0A}{l}$$
	Notation- $\kappa=\epsilon_r$=relative permittivity/dielectric constant

### Materials with dielectric properties
- Centrosymmetry: possessing an inversion centrecentre of symmetry
- Some non-centrosymmetric crystals: contain a unique direction not repeated by symmetry
	- Example of unique direction: $\ce{ZnS}$ with wurtzite structure: $[001]$
- Material with unique direction: polar due to charge separation
- Centrosymmetric: always non-polar, non-centrosymmetric not necessarily polar
#### Piezoelectricity
- Has to be non-centrosymmetric (e.g. $\ce{SiO2}$, quartz)
- Initially non-polar, application of stress leads to shape change and polarity
	- Reason for shape change: equalisation of bond lengths
	- Shape change can also be a response to electric field
- Change in polarisation:
$$P=d\sigma$$
	- $d=$piezoelectric coefficient, $\sigma=$stress
- Voltage across piezoelectric subject to stress against 2 parallel sides:
$$V=\frac{d\sigma l}{\kappa \epsilon_0}$$
- Generator effect: stress applied, voltage induced
- Motor effect: electric field applied, movement induced

#### Pyroelectricity
- In polar materials with unique direction (example: $\ce{ZnS}$ with wurtzite structure)
- Temperature change leads to relative movement of charges
- Change in polarisation with temperature
$$\Delta P=p\Delta T$$
	$p=$pyroelectric coefficient, $\Delta T=$change in temperature
- Change in voltage:
$$\Delta V=\frac{p\Delta Tl}{\kappa \epsilon_0}$$
- Uses: IR detector in burglar alarm, thermal imaging cameras
#### Ferroelectricity
- Permanent polarisation after applying electric field, polarised direction can be reversed
- Example: barium titanite $\ce{BaTiO3}$ with perovskite structure
- Below the Curie Temperature $T_c$, the unit cell is spontaneously polarised due to low symmetry
- Example- displacement of $\ce{Ti^{4+}}$ ion in $\ce{BaTiO3}$ at different temperatures
	- [[Phase transitions in materials#Displacive and reconstructive transformations|Displacive]] phase transition
	- From low to high temperature: rhombohedral->orthorombic->tetragonal->cubic
	- Ion in the crystal is in a double-well potential, the field can make one end more favourable
- Dielectric constant depends on electric field (non-linear)
#### Domains in ferroelectric materials
- All cells in a domain have the same polarisation direction as dipoles tend to line up
- A material with differently oriented domains ends up having 0 net polarisation
- Energetic balance of domain formation:
	- Domain wall energy from dipoles having different orientations
	- Stray field energy from surface charges in regions with high anisotropy
- Angles between domains depends on symmetry of the crystal
- Ferroelectrics held in a field become poled as dipoles line up in a crystallographic direction closest to field direction
#### Ferroelectric hysteresis
![[Ferroelectric hysteresis loop.png]]
	- Domains with favourable orientations grow to align with $E$
	- Dipoles remain aligned after field is removed
	- $E_c$: coercive field, depends on pinning of domain wall motion by defects/grain boundaries
	- $P_r$: remnant polatisation as some domains switch direction to reduce stray fields
	- Area of loop proportional to energy required for switching
## Magnetic materials
- Origin of magnetism: unpaired valence electrons acting as magnetic dipoles
- Magnetisation of a material $M=$ magnetic moment per unit volume
$$M=\chi H$$
	- $\chi=$ magnetic susceptibility
- Detailed explanation of $M$ and $H$: 
	- [[Electromagnetism#Magnetostatic fields in homogeneous magnetic materials]]
- Types of magnetism:
Type | $\chi$ | Origin
---------| ------------ | ----
Diamagnetism | $-10^{-5}$ | No unpaired electrons, but moments exist to oppose the applied field
Paramagnetism | $10^{-5}$ | Some unpaired electrons, isolated, random dipoles exist and can align with applied field
Ferromagnetism | $10^3-10^5$ | Many unpaired electrons with aligned dipoles due to exchange interaction, can have permanent magnetisation
Antiferromagnetism | 0 | Lowest energy state has anti-parallel moments (e.g. $\ce{Cr}$)
Ferrimagnetism | $10^{-1}$ | Atoms with magnetic properties in two different sub-lattices with unequal moments (e.g. $\ce{Fe3O4}$ with spinel structure)
### Ferromagnetic materials
- Thermal motion competes with exchange interaction at high temperature
- Unlike ferroelectricity, dipoles can be aligned along multiple possible crystallographic axes, but there is a preferred "easy" axis due to interaction of crystal structure with the dipole
#### Domains in ferromagnetic materials
- Ferromagnetic materials also form domains
	- Shape can affect domain orientation (reduction of stray fields, magnetisation tends to lie along elongated direction)
- Magnetistion can lead to strain, and vice versa
- Domain wall width determined by:
	- Exchange interaction energy- encouraging dipoles to align with each other (widens domain wall due to gradual change in alignment)
	- Anisotropy energy- encouraging dipoles to align with easy axis (leads to abrupt change)
- Small particles do not always form domains
	- Domain wall energy $\propto r^2$
	- Stray field energy $\propto r^3$
#### Ferromagnetic hysteresis
![[Ferromagnetic hysteresis loop.png|400]]
	- Increasing $H$:
		- Initially, moments are aligned along easy axes with domains cancelling out
		- Domains grow by irreversible wall motion as they are pinned by imperfections
		- Then, whole sample is aligned along easy axis
		- Finally, sample is aligned along external field
	- Like [[#Ferroelectric hysteresis]], there is remnant magnetisation to reduce stray fields
	- $H_c$ also influenced by grain boundaries and imperfections
	- Area proportional to energy of switching
		- Permanent magnets: large $M_r$ and $H_c$
		- Memory devices: well defined $H_c$
		- Transformer cores: small loop area, low $H_c$, high $M_{sat}$