## Properties at high pressure
- High pressure leads to high packing densities and changes in bonding
- In molecular solids. bond lengths may become similar to intermolecular distance
	- Loss of molecular identity can lead to polymer formation (Example: nitrogen, $\ce{CO2}$)
	- Electron delocalisation can lead to the solid becoming a metal (Example: iodine)
- Phase transitions in high pressure are typically [[Phase transitions in materials#Displacive and reconstructive transformations|reconstructive]]
- Example: $\ce{NaCl}$ and $\ce{MgO}$ adopt the $\ce{CsCl}$ structure at high pressure
- Example: In the Earth's mantle, $\ce{(Mg,Fe)2SiO4}$ can transform from olivine to spinel
	- Large kinetic barrier, can be in metastable phase
	- Once transformation occurs, significant volume contraction can cause earthquakes
- Example: graphite to diamond
	- Complete reconstruction required, with high activation energy
	- Diamond becomes more thermodynamically stable at high pressures
- Example: hexagonal to cubic $\ce{BN}$
	- Cubic structure similar to diamond
## Creep
- Time-dependent permanent deformation at stresses well below yield stress
- For alloys and ceramics, occurs at homologous temperature ($T/T_m$)$>0.4$
- Three phases: 
	- Primary: high strain rate, material work hardens
	- Secondary/steady-state: near-constant strain rate, lasts the longest
	- Tertiary: necking and failure
- Equation for steady-state creep:
$$\frac{d\epsilon}{dt}\equiv \dot{\epsilon}=A\sigma^n$$
	- $A$ depends on temperature
- Dislocation/power-law creep: high stress, $3<n<10$, involves dislocation motion
- Diffusion/linear creep: low stress, $n\approx 1$, involves diffusion
### Dislocation creep
- Below $\sigma_Y$, dislocations encounter obstacles such as precipitates and sessile segments
- Dislocation creep occurs when dislocations start migrating onto other slip planes
- Migration occurs via a diffusive process called climb
- A limited segment of the dislocation line moves to another plane
- At high enough temperatures, bulk diffusion occurs
	- Atoms in the bulk lattice can diffuse into/out of dislocation core
- At lower temperatures, core diffusion occurs
	- The only significant diffusion is along the dislocation cores
- Temperature dependence of dislocation creep is derived from diffusivity:
$$\dot{\epsilon}=A'D_0\sigma^n\exp(-\frac{Q}{RT})=A''\sigma^n\exp(-\frac{Q}{RT})$$
	- $A'$ and $A''$ are temperature-independent
### Diffusion creep
- When under stress, atomic diffusion direction is biased, and grains elongate
- At higher temperatures, Nabarro-Herring creep occurs
	- Diffusion within bulk of the lattice is dominant
- At lower temperatures, Coble creep occurs
	- Diffusion is predominantly among grain boundaries
- Strain rate depends on average grain diameter $d$:
$$\dot{\epsilon}=B\frac{D\sigma}{d^2}=\frac{B'\sigma}{d^2}\exp(-\frac{Q}{RT})$$
- Summary of deformation mechanisms:
![[Deformation mechanisms.png|450]]
### Creep resistance
- Minimisation of creep rate:
	- High melting point to reduce homologous temperature
	- Minimal dislocation motion
		- Example: superalloys with order hardening
	- Coherent, stable, small precipitates to increase yield strength
	- Large grains
	- Pinned grain boundaries with controlled orientation to prevent sliding
## Jet engines
- Efficiency of a [[Thermodynamics|thermodynamic heat engine]] is higher with higher temperatures
	- Carnot cycle: $W/Q_{in}=1-T_c/T_H$
	- Brayton cycle for jet engines: $W/Q_in=1-T_1/T_2$
		- Start and end temperatures for adiabatic compression of air
- Conditions for turbine blades:
	- Temperature of blade exceeds $0.75T_m$
	- High angular velocity leads to high centrifugal stress
	- Long lifetime
- Requirements: strength, creeo resistance, toughness, oxidation resistance
- Blades kept cool using internal channels that pass cold air
### Turbine blade superalloy
- Requirements:
	- No polymorphism (no phase changes in temperature range)
	- Low diffusivity (ccp is lowest, followed by hcp and bcc)
	- Ductile
	- Low density (density can increase centrifugal forces)
	- Oxidation resistance
	- Relatively cheap
- Choice of main constituent metal: Nickel
- Alloying additions in nickel-based superalloy:
	- Chromium for corrosion resistance ($\ce{Cr2O3}$)
	- Cobalt and tungsten for solution strengthening
	- Aluminium, titanium, tantalum to form precipitates and provide [[Strengthening mechanisms in metals|order hardening]]
- Phases present:
	- $\gamma$ phase: ccp-based solid solution, average composition for each lattice point
	- $\gamma'$ phase: fully ordered precipitate phase, mainly $\ce{Ni3Al}$ ($\ce{Al}$ at lattice points)
	- Lattice parameters of the phases are matched to provide coherent interfaces
	- Incoherent interfaces cause precipitates to coarsen
- Blades are single crystal to prevent diffusion creep
	- Grown along long axis of blade
- Order hardening: lattice vector in $\gamma$ is not lattice vector in $\gamma'$
	- A dislocation entering $\gamma'$ creates an anti-phase boundary and encounters resistance
	- First dislocation line has arc shapes due to drags
	- Second dislocation line restores favourable arrangement and is smooth
### Thermal barrier coating
- Blades protected from high temperatures by cold air and thermal barrier coatings
- Coatings need to have low thermal conductivity, high $T_m$ and adequate strength
- Main component: Yittria-stabilised zicronia ($\ce{Y2O3}-\ce{ZrO2}$)
	- Yittria stops transformation from cubic phase to monoclinic
- The ceramic adheres to the turbine blade via an alloy bond coat
- Oxygen can diffuse through YSZ ([[Solid ionic conductors|ionic conduction]])
	- Layer of $\ce{Al2O3}$ is added to block oxygen
- Zicronia layer is grown with a columnar structure to allow it to expand instead of crack
## Radiation
- Irradiation of materials changes physical, chemical, and mechanical properties
- Common environment for irradiation: nuclear reactor
	- Fuel rods: typically $\ce{UO2}$, absorbs neutrons to undergo fission
	- Cladding (austenitic steel/zicronium alloy) protects fuel from water corrosion and brittle fracture
	- Control rods absorb neutrons to control chain reaction
	- Coolant removes heat from fission to produce steam
### Displacement cascade
1. An energetic particle such as a fast neutron strikes an atom in the lattice
2. Transfer of energy displaces the atom, making it a primary knock-on atom (PKA)
3. PKA moves through lattice to make further knock-on atoms
4. Knock-on atoms leave behind vacancies
5. Eventually, all knock-on atoms come to rest as interstitial atoms
![[Displacement cascade.png|300]]
- Results in vacancies in the core, with surrounding interstitials
- After the cascade, vacancies and interstitials diffuse, making recombination rare
- Each atom has a minimum energy $E_d$ for it to be displaced
	- Maximum energy transferrable from neutron with energy $E_n$:
	$$E_{max}=\frac{4A}{(1+A)^2}E_n$$
		- Average energy transferred=$E_{max}/2$
- Average number of atoms per PKA=$E_{max}/(2E_d)$
- Rate of PKA creation depends on incident neutron flux
- Effects on microstructure:
	- Dissolution of precipitates
	- Change in morphology
	- Appearance of non-equilibrium phases
### Effects of displacement cascade on lattice
- Vacancies and interstitials are too far apart to recombine
	- Interstitial atoms are more mobile and disappear at dislocations and grain boundaries
	- There is an esxcess of vacancies
- At lower temperatures ($T<0.2T_m$):
	- Interstitials and vacancies form interstitial/vacancy loops in close-packed planes
	- Results in stacking fault
	- Dislocation loop is sessile as Burgers vector is normal to close-packed plane
	- Increase in dislocation density analagous to work hardening
	- As material is annealed due to heating, a steady-state dislocation density is reached
- At higher temperatures ($T>0.2T_m$):
	- Vacancies nucleate into voids that grow as irradiation continues
	- Void formation leads to swelling
	- At lower temperatures, there is a large driving force to nucleate many small voids
	- At higher temperatures, much larger voids can form
	- Swelling and distortion causes hardening, embrittlement, and shortens creep life