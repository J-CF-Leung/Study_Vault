## Dislocations and plastic deformation
- Initial "block slip" model of plastic deformation: $\tau_{crit}=Gb/(2\pi h)$, overestimate
- Actual estimation: movement of dislocations (line defects)
- Vectors describing dislocations:
	- Line vector $\bm{l}$: separation between unslipped and slipped plane
	- Burgers vector $\bm{b}$: magnitude and direction of lattice displacement
		- Make a closed loop (orientation: right hand rule with $\bm{l}$) around dislocation core, $\bm{b}$ links the start and end points when the loop is applied in a perfect crystal
### Dislocation types
- Edge dislocations
	- Extra terminating plane of atoms
	- $\bm{l \perp b}$
- Screw dislocations
	- Part of the crystal is sheared
	- $\bm{l} \parallel \bm{b}$
- Real dislocations: can be combinations of edge and screw dislocations\
	- Example: dislocation loop: $\bm{l}$ forms a loop, constant $\bm{b}$
### Dislocation motion
- Dislocations move by small relative shifts of atoms
	- After passage, original crystal structure is restored
- Movement under application of stress $\bm{\tau}$:
![[Dislocation movement.png]]
	- Directional condition: $\bm{b \parallel \tau}$
	- Slip direction $\parallel \bm{\tau}$
	- Direction of dislocation propagation $\parallel (\bm{l \times n})$
	- For slip to occur, slip plane $\bm{n=l \times b}$
	- Edge: only one plane possible, screw can have infinite slip planes
- Example of motion: dislocation loop
	- $\bm{l}$ is in a loop, and the propagation of each segment is perpendicular to $\bm{l}$
	- If $\bm{\tau\parallel b}$, the loop expands or contracts
- Stress required to move a dislocation: Peierls-Nabarro stress
$$\tau_P\approx 3G\exp(-\frac{2\pi w}{b})$$
	- $w$: width of dislocation, typically around $|\bm{b}|/4$
- Force per unit length to move a dislocation $F/L=\tau|\bm{b}|$
- Strain energy per unit length for a screw dislocation $\Lambda=Gb^2/2$
### Slip in real crystals
- For a crystal to be restored after dislocation passage, $\bm{b}$=lattice vector
	- Along close-packed directions, required stress is much lower
	- Dislocation width is higher for close-packed planes
Structure | Dominant slip system | Number of possible slip systems
------ | ---------- | ------ 
bcc | $\{110\}<\bar{1}11>$ | 12 (6 planes, 2 directions)
fcc | $\{111\}<\bar{1}10>$ | 12 (4 planes, 3 directions)
hcp | $\{001\}$<100> | 3 (1 plane, 3 directions)
- Only dislocations in allowed slip system will move, and the Burgers vector has to align with shear stress
- Stress at arbitrary angle: stress resolved along $\bm{b}$, area resolved along $\bm{n}$
- Resolved stress:
$$\tau_R=\frac{F}{A}\cos{\phi}\cos{\lambda}=\sigma_Y\cos{\phi}\cos{\lambda}$$
	- $\phi$: between slip plane normal and force
	- $\lambda$: between force and slip direction
	- $\cos{\phi}\cos{\lambda}$: Schmid factor, maximum value of $0.5$
	- Schmid's law: Slip system with highest Schmid factor will operate first
- Identifying highest Schmid factor for cubic metals: OILS rule (provided in IA data book)
- As slip continues, direction of stress relative to slip direction changes\
	- New tensile direction = old tensile direction + $n$$[\text{slip direction}]$
	- Continues until two slip systems start to operate
### Deformation of metals
- hcp metals: Only one slip system operates
	- Schmid factor will decrease overall, can either monotonically decrease or initially increase
	- Stress required to continue plastic deformation will increase overall
- fcc metals: multiple slip systems can operate
	- Initial: easy glide, one slip system operates, $\tau_R$ remains constant
	- Second stage: duplex slip (2 slip systems operate), dislocations interfere with each other and increases $\tau_R$, work hardening occurs
	- Final stage: other slip systems operate, dislocations bypass obstacles, $\tau_R$ increases more slowly
	- Duration of work hardening has negative correlation with stacking fault energy
		- Origin of stacking fault: [[Strengthening mechanisms in metals#Partial dislocations]]
		- Partial dislocations must recombine before cross slipping
- Polycrystalline metals
	- All grains have different Schmid factors
	- Each grain initiates work hardening at different times, easy glide does not occur
	- Continuous work hardening
	- Much higher yield stress than single crystals as all grains must initiate multiple slip at the same time

### Dislocation interactions
- Each dislocation generates tensile, compressive, and shear stress fields
- Dislocations with opposite signs attract each other to minimise strain energy
- Dislocation interactions: intersection or combination
- Intersection: [[Strengthening mechanisms in metals]]
- Combination: 
	- $\bm{b_3=b_1+b_2}$
	- New line vector is intersection of slip planes: $\bm{l_3=n_1\times n_2}$
	- New slip plane $\bm{n_3=b_3 \times l_3}$
	- If new slip plane is not a viable slip system, the dislocation is sessile (static)
	- Favourability of combination: reduction in stress energy, $|\bm{b_3}|^2<|\bm{b_1}|^2+|\bm{b_2}|^2$
- Combination of intersection and combination: work hardening
- Generation:
	- Continued plastic deformation requires source of new dislocations
		- Sources: Free surfaces, grain boundaries
	- Frank-Read source: dislocation pinned at both ends
		1. Without shear stress, dislocation lies in a straight line
		2. Under shear stress, dislocation experiences a force normal to the line, and bows outwards due to pinned ends
		3. Straight line->semicircle->expanded curve->spiral
		4. When two spiral arms touch, they annihilate and create a dislocation loop
- Migration to other slip planes
	- Climb of edge dislocations
		- For edge dislocations, glide is confined to a single plane
		- Dislocations can move to other parallel planes to avoid obstacles
		- Vacancies or atoms in the crystal can diffuse to the dislocation core and move it upwards/downwards
		- The climb allows the dislocation to avoid obstacles
		- Diffusion is thermally activated
	- Cross slip of screw dislocations
		- Screw dislocations can glide on a family of planes
		- If dislocation movement is impeded, stress required for deformation increases until the dislocation glides on a new plane (cross slip)
		- Once past the obstruction, the dislocation can double cross slip back to the original plane

### Deformation without dislocations: cooperative shear
- Alternative deformation mechanism
- Deformation twinning: structure remains the same, with different orientation
	- Structures on either side of twin boundary are mirror images
- Twinning planes and directions: analagous to slip plane and direction
Structure | Twinning plane | Twinning direction
------- | ------------- | --------------
bcc | $\{112\}$ | $<11\bar{1}>$
bct | $\{011\}.\{102\}$ etc. | $<100>,<\bar{2}01>$ etc.
fcc | $\{111\}$ | $<11\bar{2}>$
- Example: Twinning in fcc metal
	- Shear: A to B, B to C etc
	- Movement of atom: similar to partial dislocation, vector $\bm{\delta}=a/6[11\bar{2}]$
	- Successive planes shear simultaneously:
![[Cooperative shear.png|400]]
	- Twinning shear $\gamma=|\bm{\delta}|/d_{111}=1/\sqrt{2}$
- In some cases, deformation twinning becomes the dominant deformation mechanism
	- At high strain rates, twinning is dominant as it propagates faster
	- Also favoured at low temperatures as twinning does not require thermal activation
- Deformation twins have a lens-like shape to be compatible with grain boundaries
	- Unlike annealing twins with straight boundaries
- Martensitic phase transition: change in structure via cooperative shear
	- Example: ccp to hcp
		- ABCABCABC->ABCACACA
		- Two planes shear together (BC->CA, AB->CA)