## Displacive and reconstructive transformations
- Displacive transformations: diffusionless
	- Example: movement of $\ce{Ti^{4+}}$ in $\ce{BaTiO3}$, or formation of martensite
- Reconstructive transformations: structure of the two phases are dissimilar
	- Involves bonds breaking and reforming
	- Sharp phase boundary
	- Thermally activated, metastable states possible
	- Require nucleation and growth (described below)

# Formation and growth
## Kinetics: diffusion
- Types:
	- Interstitial- from one interstitial site to another (typically fast, e.g. $\ce{C}$ in $\ce{Fe}$)
	- Substitutional- from one site to a vacancy
- Flux of solute: Fick's first law
$$J=-D\nabla C$$
	- D: Diffusivity
	- $\nabla C$: concentration gradient, $\partial C/\partial x$ in 1D
	- J: flux
- Diffusion equation:
$$\pd{C}{t}=D\nabla^2C$$
- Approximate solution:
$$x\approx \sqrt{Dt}$$
- Temperature dependence of diffusivity:
$$D=D_0\exp(-\frac{Q}{RT})$$
## The thermodynamics of nucleation
- The driving force: Gibbs Free Energy
	- The Gibbs Free energy of the transformation is $\Delta G=\Delta H-T\Delta S$
	- At equilibrium temperature $T_e$, $\Delta G=0$, therefore $\Delta H=T_e\Delta S$
	- If $\Delta H$ and $\Delta S$ are independent of $T$ ($\Delta C_P=0$), $\Delta G=\Delta S(T_e-T)$
	- At non-equilibrium temperature, there is a driving force
		- Example: solidification $\Delta S<0$, it is thermodyanmically favourable when $T<T_e$
	- Gibbs Free Energy change per volume: $\Delta G_V$
- Work of nucleation:
	- An interface is created and contributes excess energy to the system
	- Energy = $4\pi r^2\gamma$, for a spherical nucleus
- Homogeneous nucleation: nucleation within a uniform phase
	- Work done forming a nucleus:
	$$W_n=\frac{4\pi}{3}r^3 \Delta G_V+4\pi r^2\gamma$$
	- "Force" for nucleation=$dW_n/dr$
	- Critical radius: $dW_n/dr=0$
	$$r^*=-\frac{2\gamma}{\Delta G_V}$$
	- Above the critical radius, the nucleus naturally grows
	- Maximum work $W_n^*\propto 1/{\Delta G_V}^2$, nucleation is impossible at $T_e$
	- Nucleating a solid inside another solid causes strain, with strain energy scaling with volume-->$W_n=V(\Delta G_V+U)+\gamma A$
	- Homogeneous nucleation can often be difficult, resulting in supersaturated solutions
- Heterogeneous nucleation:
	- Nucleation catalysed by presence of defects or particles in the original phase
	- Smaller surface means surface energy contribution is lower
	- Heterogeneous nucleation is much easier to occur, and dominates over homogeneous
	- Sites: grain boundaries, container surfaces, defects
- - Nucleation rate influenced by:
	- Proportion of critcal nuclei $\propto \exp(-W_n^*/kT)$
	- Rate of atomic addition to nucleus $\propto \exp(-Q/kT)$
- Effect of temperature:
	- At $T_e$, there is no nucleation
	- As $T$ is lowered, $\Delta G_V$ increases, rate increases
	- As $T$ is lowered further, diffusion slows and rate drops

## Growth of a new phase
- There is an activation energy barrier for both forward and backward jumps, the driving force gives rise to an asymmetry in energies (forward is more favourable)
- Sketch of growth rate:
![[Phase growth rate.png|250]]
	- Nucleus grows even for very small departures from $T_e$
- During growth, an interface between the 2 phases form
	- Coherent with perfect alignment of lattices
	- Coherent with elastic strain: strain energy increases with growth, becomes semi-coherent
	- Semi-coherent, with formation of dislocations decreasing strain energy
	- Incoherent, with no matching
- Shape of precipitates
	- Some interfaces are more coherent than others
	- Coherent interfaces grow faster, forming discs/needles
- The Widmanstätten microstructure:
	- Plate-like precipitates in crystallographically related orientations
	- Close-packed planes and directions are parallel
	- Body-centred cubic in face-centred cubic:
		- $\{110\}_{bcc}//\{111\}_{fcc}$
		- $<\bar{1}11>_{bcc}//<1\bar{1}0>_{fcc}$
- TTT diagrams: Time $t(y)$ taken to transform a fraction $y$ at a given temperature
	- Time plotted logarithmically
	- "Nose" of curve indicates optimum temperature
	- Critical quench rate to prevent transformation: $\approx \Delta T_{nose}/t_{nose}$
- Diffusionless (displacive) transformations
	- Example: formation of body-centred tetragonal phase in an fcc structure, causes internal strains

# Phase diagrams
- At constant pressure and temperature, the most stable phase has the lowest Gibbs Free Energy (Definition: [[Thermodynamics]])
## Phase boundaries
- The Clausius-Clapeyron equation:
	- Differential of Gibbs Free Energy: $dG=VdP-TdS$
	- For two phases $\alpha$ and $\beta$, $G_\alpha=G_\beta$ at the phase boundary
	- $\Delta(dG)=dG_\alpha-dG_\beta=0$ leads to:
	$$\frac{dP}{dT}=\frac{\Delta S}{\Delta V}$$
	- For solids, $\Delta S$ and $\Delta V$ are approximately constant, making the phase boundary straight
- Direct determination of phase diagram: may require extreme conditions and expensive equipment that also makes observation difficult
- $\Delta V$ measurement: X-ray diffraction
- $\Delta S$: calculation at constant pressure
$$S(T_2)-S(T_1)=\int_{T_1}^{T_2} \frac{C_P\,dT}{T}+\sum_i\frac{\Delta H_i}{T_i}$$
	- Summing continuous variation with temperature and phase transitions
# Melting
- Freezing: nucleation barrier, liquid can be supercooled
- Melting: no nucleation barrier
- Actual melting process:
	- There is some surface melting well below the bulk melting temperature
	- $\gamma_{sv}>\gamma_{ls}+\gamma_{lv}$--> more favourable to form 2 interfaces
	- Thickness of liquid layer increases as temperature approaches $T_m$
- Consider a particle of radius $r$ with some surface melting:
	- Situation analagous to [[#The thermodynamics of nucleation|the nucleation of a new phase in a solid]]
	- Work done in freezing=$(4\pi/3)r^2\Delta G_{V,f}+4\pi r^2\gamma_{ls}$
	- Critical radius:
	$$r^*=-\frac{2\gamma_{ls}}{\Delta S_V(T_m-T)}$$
		- $r>r^*$: the solid phase is stable
	- As temperature gets closer to $T_m$, $r^*$ increases until it exceeds the size of the particle, and the particle melts
	- Therefore, for smaller particles, melting can occur well below $T_m$
- Superheating: suppressing surface melting, heating the interior above surface temp.
	- Prevention of surface melting: coating the crystal in a solid matrix
	- Limit of stability is the onset of liquid nucleation in the interior
	- Nucleation is kinetic, so faster heating (e.g. laser) can superheat the interior to create a metastable solid above $T_m$
# Example: Ice
## Structure
- Most common structure in ambient conditions: ice $I_h$
	- Orientations of water molecules are related via ice rules:
		- Oxygens are covalently bonded to 2 hydrogens, and hydrogen bonded to another 2
		- Only 1 hydrogen per bond
	- Positions of hydrogens have a limited degree of disorder
- All phases of ice have tetrahedrally coordinated oxygen atoms
	- At high pressures, $H-$bond length $\approx$ covalent bond length
		- Distinction between molecules is blurred
	- High density can be achieved while keeping 4-fold coordination with 2 interpenetrating networks
## Properties
- Ice is brittle all the way up to melting point
- Hydrogen disorder disrupts long-range order
- Dislocation movement will cause molecules to violate ice rules
	- Molecules will have to be reoriented
- Glacial ice is typically close to melting point while under its own weight for a long time
	- Ice undergoes creep (glacial flow)
- There is usually significant surface melting on ice
	- Low coefficient of friction
	- High adhesion and ease of compaction
- Regelation: melting of ice $I_h$ reduces volume, giving the boundary a negative slope
	- Ice can melt under pressure then reform when pressure is reduced