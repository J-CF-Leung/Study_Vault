## Raising yield stress
### Work hardening
- Dislocation intersections
	- Dislocations can combine and form sessile segments 
	   ([[Plastic deformation#Dislocation interactions]])
	- Most dislocations aren't glissle even before stress is applied (forest dislocations)
	- Density of dislocations $\rho=1/L^2$, $L=$ average spacing
	- When dislocations move, they have to intersect and cut each other
		- Each dislocation acquires a step/jog in the dislocation line
		- Jog has length $|\bm{b}|$ of the intersected forest dislocation
		- Jog creation requires energy
	- Created jogs can be sessile, creating further barriers to slip
	- Already plastically deformed metals have much higher dislocation density, raising $\sigma_Y$ significantly
- Both dislocation intersections and combinations contribute to work hardening
### Grain size
- Grain boundaries are obstacles for dislocation movement
- Dislocations will accumulate at grain boundaries and increase stress
	- At some point, the neighbouring grain initiates slip due to the stress
- For yielding, all grains in the metal must initiate slip
- With small grains, fewer dislocations can pile up, required yield stress becomes higher
- Hall-Petch relationship:
$$\sigma_Y=\sigma_0+\frac{k}{\sqrt{d}}$$
### Solution strengthening
- Point defects in a solution: vacancies, substitutional defects, interstitial defects
- Substitutional solute atoms:
	- Stress field is always spherically symmetric, with no shear stress component
	- Interacts exclusively with edge dislocations to minimise strain energy
	- Position of solute atom: depends on if stress is compressive or tensile
	- Combination retards dislocation motion
	- Substitutional atoms are essentially static
	- Effect is weaker as the atoms must be close to active slip plane
- Interstitial solute atoms:
	- Stress fields can be asymmetric, and generate larger strains
	- Interacts with both screw and edge dislocations
	- Interstitials can have high diffusion rates (e.g. $\ce{C}$ in $\ce{Fe}$)
	- Diffusion allows interstitials to accumulate at dislocations
	- Example: carbon steel
		- Carbon atoms diffuse quickly and accumulate at dislocations
		- Formation of Cottrell (carbon) atmospheres, trapping the dislocation
		- Drop in stress required for deformation after initial yield as Cottrell atmospheres are overcome
		- Yield initiates at ends of the sample where stress concentration is highest
		- Luders bands (boundaries of stressed ends) move and meet in the middle
		- Work hardening proceeds as the entire sample plastically deforms
	- Diffusivity of interstitials is heavily reliant on temperature
		- At room temp., previous behaviour is seen (initial drop in yield stress)
		- At high temp., only hardening behaviour is seen as atoms and dislocations move together
		- At an intermediate temperature, atoms and dislocation speeds are similar
			- Carbon can recombine with dislocations that have just escaped the Cottrell atmosphere
			- Repeated pinning and escaping creates serrations in stress-strain curve (Portevin-Le Chatelier Effect)
### Precipitate strengthening
- Small precipitates are often coherent with the matrix and can be sheared/cut by dislocation motion
	- Precipitates are often harder to pass through, providing a strengthening effect
	- $\Delta\tau\propto\sqrt{r}$
- Large precipitates are more likely to be incoherent
	- Dislocations bow around the precipitate (Orowan bowing)
	- Orowan bowing stress $\tau=Gb/L$
- Precipitate size is positively correlated with aging time
- At some size, bowing is more favourable than cutting and $\Delta \tau$ decreases
	- Stronger precipitates increase cutting resistance with no effect on bowing, giving higher peak stress and lower peak radius
	- Greater precipitate fraction increases resistance to both cutting and bowing
- Summary of age hardening
![[Solution strengthening.png|350]]
	- Coherency strengthening: creation of coherency strains that inhibit dislocation motion, with semi-coherency giving the largest strain field
- Example: $\ce{Al-Cu}$ alloys
	- Structure as a function of ageing time: [[Alloys#Al-Cu system]]
	- As $\ce{Cu}$ content increases, strength increases
	- As ageing temperature increases, peak stress increases
	- At peak: both $\theta'$ and $\theta''$ precipitates exist

Treatment | Effect on hardening | Reasons
------------ | ---------- | ---------
Pure $\ce{Al}$ | Low yield strength, little work hardening | Few strengthening mechanisms
Solid solution | Higher yield strength, little work hardening | Solute strain fields
Under-aged | Even higher peak yield strength, stress for continued deformation can drecrease, little work hardening | Dislocations can cut through GP zones
Over-aged | Low yield strength, rapid work hardening | Bowing is dominant, process leaves dislocation debris to inhibit futher dislocation movement
Peak aged | High yield stress, high work hardening rate | Precipitates have a range of sizes

## Other mechanisms
### Partial dislocations
- In fcc metals, a perfect dislocation goes from an A/B/C position to another A/B/C
	- Burgers vector $\bm{b_1}$ is of the type $a/2<110>$
	- Alternative path: B->C->B through 2 partial dislocations $\bm{b_2}$ and $\bm{b_3}$
	- Partials in fcc: type $a/6 <112>$
	- Stacking fault occurs after 1 partial (e..g ABCACABCA)
	- Corrected after passage of second partial
	- Favourability: 
		- Frank's rule always favours decomposition
		- Stress fields cause dislocations to separate, creating a stacking fault region with energetic cost
		- Balance between stacking fault energy and dislocation energy determines stacking fault region size
	- Effect on work hardening
		- Partials have both edge and screw dislocation components
		- They must recombine before cross slipping
		- Low stacking fault energy->large fault region->more work hardening before cross slipping
### Order hardening
- Ordered structures have a higher strength than disordered solid solutions
- Burgers vectors in a typical structure may not equate to lattice vectors
	- Example: $\beta-$brass
		- High temperature: disordered bcc, $\bm{b}=a/2[111]$ is a lattice vector
		- Low temperature: $\ce{CsCl}$ structure, $\bm{b}=a/2[111]$ is not a lattice vector
- Dislocation creates energetically unfavourable like-like bonds 
- Planar defect: anti-phase boundary (APB)
- Shortest lattice vector may be large and unfavourable
- Passage of another dislocation with same $\bm{b}$ restores perfect structure
	- Two dislocations repel to create a bounded region
	- Bounding dislocations and APB: superdislocation
	- Individual dislocations: superpartials
- Balance of (APB) energy and dislocation energy dictates superdislocation size
