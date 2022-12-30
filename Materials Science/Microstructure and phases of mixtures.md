### Observing microstructure
- Reflected light microscopy
	- Sample needs to be mounted, ground, polsihed, then etched
	- Grain boundaries appear dark
	- Angle of reflection depends on crystallographic orientation of grain
	- Different phases etch at different rates
- Transmitted light microscopy for thin, transparent samples
- Scanning electron microscopy for conducting materials
- Atomic force microscopy to measure height of sample

## The thermodynamics of mixtures
- Definition of thermodynamic functions: [[Thermodynamics]]
- Gibbs Free Energy $G$ tends to a minimum at equilibrium
- When 2 phases have the same $G$, they are in equilibrium

### Gibbs Free Energy of mixing 2 components
- Enthalpy of mixing $\Delta H=X_AX_B\Psi$
	- $X$: composition, $X_B=1-X_A$
	- $\Psi$: interaction parameter $\propto (2E_{AB}-E_{AA}-E_{BB})$
	- $\Psi<0$: Mixing is more favourable, $\Psi>0$: de-mixing is more favourable
	- $\Delta H$ vs composition has a symmetric parabolic form
- Entropy of mixing $\Delta S=-R(X_A\ln X_A+X_B \ln X_B)$
	- Always positive
	- Curve has infinite gradient at pure substances
- Gibbs Free Energy of mixing $\Delta G=\Delta H-T\Delta S$
	- $\Delta H<0$: mixing is always favourable
	- $\Delta H>0$: shape of $\Delta G$ curve depends on $T$
		- High temperature: solution formed
		- Low temperature: a mixture of 2 phases is formed
- Solvus: boundary of single-phase and 2-phase regions
	- Peak at $X=0.5$, Gibbs Free Energy of that point transitions from maximum to minimum, $\partial^2 G/\partial X^2=0$
- Actual systems: free energy curve will not be symmetrical
- Determination of compositions for equilibrium phases: the common tangent construction
![[Common tangent construction.png]]
	- Composition A: separate into phases B and C given by tangent
	- Proportion of phases: lever rule, proportion of C$=(X_A-X_B)/(X_C-X_B)$

## Phase diagrams of mixtures
### The eutectic system
- Eutectic: incomplete solubility of components in both solid and liquid
![[Eutectic phase diagram.png|400]]
- Transformation at eutectic point: $L\rightarrow \alpha+\beta$, with temperature lower than either melting point
- Details of forming a new phase: [[Phase transitions in materials]]
- As $\alpha$ solidifies, $\beta$ is expelled, and vice versa, forming lamellae (cooperative growth)
- Application: low-temperature solders with well-defined melting point
- Solidification of hyper/hypoeutectoids: formation of pure $\alpha/\beta$ phase with eutectic, 
	- Proportion determined by lever rule
	- Lesser phase forms at grain boundaries of dominant phase
- Cooling curve characteristics:
	- Isothermal arrest occurs at well-defined melting points (pure, eutectic compositions)
	- Slower cooling in mushy phase as latent heat is released
- Solidification in non-equilibrium conditions (e.g. fast cooling)
	- $\alpha/\beta$ atoms have no time to diffuse when the other phase solidifies
	- Coring occurs
- Small perturbations in solid-liquid interface during solidification causes dendrites to form, maximizing area where solute is expelled

### Other transformations
- Eutectoid: similar to eutectic, but all phases involved are solid
- Peritectic: $\alpha+L\rightarrow\beta$
![[Peritectic transformation.png]]

### Control of microstructure by processing
- Cooling: surfaces cool a lot quicker than centres
	- Regions that cool faster experience larger driving force for nucleation, leading to small nuclei
- Casting of metal:
	- Small grains near mould wall
	- Columnar grains approaching centre
	- Large equiaxed grains near centre due to slow cooling
- Metallic glass formation: avoid crystallisation to form an amorphous phase
	- Method: Melt spinning
	- Properties: lack of dislocations makes it brittle, lack of grain boundaries makes it a soft ferromagnetic material
- Cooling of eutectics:
	- Faster cooling rate gives higher driving force to form interfaces between phases, leading to fine lamellar spacing
	- Lower temperature also leads to slower diffusion
- Deformation: Final shapes are often produced using machines