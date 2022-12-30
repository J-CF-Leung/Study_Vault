## Elastic behaviour
- Most manmade solids: linear, time-independent response to stress
	- $\sigma=E\epsilon$
- Biomaterials: Time dependent, more like liquids, shows viscoelastic behaviour
- Viscosity:
$$\sigma=\eta\frac{d\epsilon}{dt}$$
	- Modeled by dashpot
- Maxwell model: spring and dashpot in series
$$\dot{\epsilon}=\dot{\epsilon_d}+\dot{\epsilon_s}=\frac{\sigma}{\eta}+\frac{\sigma}{k}$$
	- With an oscillating stress $\sigma=\sigma_0\exp(i\omega t)$:
	$$E=Re\left(\frac{\sigma}{\epsilon}\right)=\frac{k\omega^2t_R^2}{1+\omega^2t_R^2}\;\;,\;t_R=\frac{\eta}{k}$$
	- At high frequencies, viscous flow is negligible, only elastic response is significant
	- At low frequencies, viscous flow is dominant, stress and strain are $\pi/2$ out of phase
- Voigt model: spring and dashpot in parallel, better for constant stress
	- At high frequency, dashpot has no time to extend, leading to high stiffness (flaw)
	- At low frequency, behaviour tends to that of a spring
- High frequencies: linear solid model
	- Spring + dashpot combination, and pure spring in parallel

## Material selection
- Choosing a material to maximise/minimise a characteristic (e.g. mass, yield stress)
- Equate free variable using 2 expressions, find merit index to maximise/minimise
- Straight lines on Ashby diagrams

## Biopolymers
### Rubber
- Natural rubber: monomers of cis-isoprene (5 carbon atoms)
- Chain is coiled up, predicted by random walk model with Kuhn length
- trans-isoprene will prefer a more linear arrangement, leading to crystalline regions
- Rubber can undergo large elastic extensions (elastomer)
	- Large strain comes from the uncoiling of chains
	- Uncoiling is thermally activated, and chains cannot flow past their neighbours
	- Increasing elasticity: vulcanisation, creating sulphur cross links
	- Uncoiling: decrease in entropy
### Proteins
- Formed from condensation polymerisation of amino acids
- Protein rubbers:
	- Coiled protein with cross links
	- Example: resilin in invertebrates, elastin in vertebrates
	- Example of resilin: insect wing hinges
- Folded structures: $\alpha-$helices (right-handed) and $\beta-$sheets
	- Transition between packing arrangements: breaking and remaking hydrogen bonds
	- Example: Keratin
		- In hair: in alpha form when dry, unwinds to form sheets when wet
		- In nails and hooves: heavily cross-linked, more strong and stiff
	- Example: types of spider silk
		- Dragline/frame silk: stiff, has crystalline regions with $\beta-$sheets
		- Viscid/capture silk: extensible, low coefficient of restitution
- Collagen: family of protein fibres in animals, with a hierarchal structure
	- Left handed coils
	- 3 coils wrap around each other to make a molecule
	- Molecules bunch into fibrils with covalent cross links
	- Ends of fibrils are staggered
	- Fibrils can pack together into bunches in tendons
- Skin: stiff collagen fibres in an elastin matrix
	- Collagen fibres are short and somewhat aligned, to make skin anisotropic
## Energy storage
- In linear elastic materials, energy density=$E\epsilon^2/2$
- Biomaterials: non-linear stress-strain curves
	- Skin: stiffer when stretched, energy density$\leq E\epsilon^2/2$
		- Storing less energy makes it less susceptible to fracture
	- Tendons: stores more energy, energy density $\geq E\epsilon^2/2$
- Elastic hysteresis: viscoelastic behaviour, dissipation of energy
	- Area of stress-strain hysteresis loop=dissipated energy density
	- Upon stress, helices unravel into sheets
	- Helices reform upon release, absorbing energy
	- Energy absorption gives enhanced toughness
- Coefficient of restitution=fraction of energy input returned elastically
	- Repeated loading and unloading: high coefficient of restitution (e.g. insect wings)
	- Viscid spider silk: low coefficient of restitution
## Polysaccharides
### Wood
- Anisotropy: strongest in vertical direction, much less strong in radial direction, weak tangentially
- Cell arrangement: most cells ($90-95\%$) are elongated and vertical, the rest are radial
- Softwood vs hardwood:
	- In softwood, vertical cells have thin cell walls and wide channel for conduction, radial cells store nutrients
	- In hardwood, vertical cells are thick-walled, there are specialised vessels in the wood
- Microstructure of wood: hierarchal
	- Basic fibre: cellulose chains
	- Chains pack together to form crystalline regions
	- Fibrils are formed from crystalline regions within amorphous lignin (1:1 ratio)
- Cell wall structure: layered arrangements of microfibrils
	- Thin primary wall: random arrangement
	- Secondary wall:
		- outer layer with microfibrils wound in 2 opposite, tilted spirals
		- middle layer with a single spiral
		- thin inner layer with 2 opposite spirals
![[Wood cell wall.png]]
- Structure of cell wall and cell arrangement lead to directional anisotropy of stiffness
- Wood stiffness is different for tension and compression
	- When under compression, cell walls buckle
	- Creases become cracks when wood is in tension
	- Trees pre-stress outer layers to withstand bending
- Water weakens wood by disrupting hydrogen bonding
- Wood has high touhness as fibres have to pull out, and layers have to separate
### Chitin
- Collagen and chitin are the main tension-bearing matertials in animals
- Chitin is also found in plants, fungi, and exoskeletons of insects and crustaceans
- Chitin is a chain of a glucose amide derivative
- Often mixed with proteins and arranged in layers to increase stiffness
- Similarly stiff as biominerals but with energetic cost
## Biominerals
- Examples: bone, shell, lenses, compasses, pathological minerals
- Strong and hard, with a lower energetic cost
- Generally brittle
- Component of tough composite materials
### Non-structural minerals
- Magnetotacticity: magnetic ferrous minerals in bacteria
	- Size, shape and orientation controlled by protein growth templates
	- Each crystal has a single domain
	- Helps bacteria orient themselves
- Calcite: assists with balance in inner ear
### Structural mineral: calcium carbonate
- $\ce{CaCO3}$ based shells are often substituted with up to  $30\,mol\%\,\ce{Mg}$
	- Achieved via ion transport
- Phases of $\ce{CaCO3}$: calcite, aragonite, and an amorphous phase
	- Calcite is more thermodynamically stable
	- Magnesium substitution prefers calcite
- Either crystalline phase can be made to precipitate using a template in an organic matrix
- Natural materials typically have a preferred crystallographic texture
	- Grain direction is controlled
	- Eggshells have a columnar growth geometry
	- Size and shape of crystals can be determined by organic matrices and pre-defined vesicles
- Example: nacre
	- Organic protein matrix with aragonite component
	- Organic material is in sheets, stacked between aragonite blocks
	- Layers are nucleated by pores in the sheets, resulting in a "brick wall" or "coin stack"
	- Nacre is exceptionally tough
		- When a crack forms, it is deflected along the weak organic layers
		- New surface area requires substantial energy

## Biomedical materials
### Bone
- Composite of collagen and hydroxyapatite (HA) $\ce{Ca10(PO4)6(OH)2}$
- Cortical bone has a hierarchal structure
	- Collagen molecule -> fibrils wrapped around HA crystals -> fibres -> lamellae -> osteons
	- Crystal's crystallographic $c-$axis is aligned parallel to the fibres
	- Fibres are bunched and wrapped into concentric sheets around blood vessel
	- Tubes (osteons) are bundled into a load-bearing structure
- Cortical bone has high tensile strength and stiffness, comparable to wood
- Bone has specialist cells that make and dissolve the structure according to mechanical requirements
### Hip joint replacements
- A stem replaces the upper part of the femur
	- Ceramics are too brittle, a biocompatible, inert metal ($\ce{Ti}$) is chosen
	- Titanium is sintered to match the typical stiffness of bone
- A ball and cup are used for moving contacts
	- Low friction is required to reduce wear
	- Metal particles can be distributed around the body
- Stem has to be bonded to the bone via a coating
	- Typical material for coating: hydroxyapatite
	- Mismatch in thermal expansion coeffcients can make the coating flake off
	- Titanium is alloyed to match thermal expansion of HA
### Arteries
- Arterial wall: collagen and elastin
- Material has to have a J-shaped curve to avoid aneurysms (local swelling)
	- Swelling caused by 2 co-existing stable radii

## Phase transformations
- Significance: cytosol (intracellular fluid) can undergo transformations
	- Dehydration and freezing can cause formation of fatal crystals
- Water-sugar systems have a eutectic phase diagram ([[Microstructure and phases of mixtures]])
	- There is virtually no solid solubility
- Phase transformations can be caused by changes in temperature or composition
- Sugar crystallisation is kinetically difficult
	- The liquid can be supercooled or dehydrated to form a viscous, glassy state
	- Glass: viscosity $\geq 10^{12} Pa\,s$
	- Glass transition has no obvious volume change
- Cell metabolism heavily relies on cytosol composition
- Crystal formation can cause ruptures
### Dehydration
- Dehydration causes formation of sharp mineral crystals, and changes ionic ratios
- Dehydration can be avoided with a higher concentration of heavy sugars in cytosol
	- Makes glass transition more likely
	- Example: resurrection plants
### Freezing
- Ice formation increases salt concentration in the cytosol, causing osmotic swelling
- Strategy 1: avoiding ice formation
	- Preventing heterogeneous nucleation makes it possible to supercool water
	- Achieved by dispersing many water droplets in oil
	- If droplets are small enough, most will not contain nucleants
	- In woods: water is subdivided within cellular structure
	- Subdivision is not possible for circulatory fluids
		- Anti-freeze proteins cause crystals to bind in favourable growth sites
		- Inhibits growth for small supercoolings
- Strategy 2: tolerating ice formation
	- For large supercoolings, organisms ensure ice is formed in extra-cellular space
		- Example: mountain plants use a central vessel for water
		- Release of latent heat protects cells for a short period
	- Higher salt concentration outside the cell draws water outside by osmosis
		- Cytosol forms a glass
		- Frogs: Intercellular regions contain ice-nucleating agents
			- Ice nucleating agents are flat protein sheets with favourable growth sites
			- Radius of protein sheet=minimum radius of curvature of ice
			- Large radius ensures ice crystals will grow
				- Favourability of supercooling: [[Phase transitions in materials]]