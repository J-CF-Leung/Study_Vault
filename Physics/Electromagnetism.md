#IB_Natsci

- The following notes is adapted from Part IB Lectures given by Prof. Oleg Brandt
- Other topics: [[Topics in Electromagnetism]]

## Vector calculus theorems
- [[Vector calculus in 3-dimensions]]

### Stokes' Theorem
$$\oint_{\partial S}d\bm{l}\cdot \bm{A}(\bm{r})=\int_S d\bm{S}\cdot \left[\nabla \times \bm{A}(\bm{r})\right]$$
### Divergence Theorem
$$\oint_{S=\partial V}d\bm{S}\cdot\bm{E}(\bm{r})=\int_VdV\,\nabla\cdot\bm{E}(\bm{r})$$


## Preview: Maxwell's equations
### Variables
- Vector fields:
	- Electric field $\bm{E}$
	- Magnetic flux density $\bm{B}$
	- Electric displacement $\bm{D}$
	- Magnetic field $\bm{H}$
	- Current density $\bm{J}$
- Scalar fields:
	- Charge density $\rho$


### In a vacuum
- Differential forms given, integral forms obtained using the Divergence/Stokes Theorems
$$\begin{aligned}\nabla\cdot\bm{E}&=\frac{\rho}{\epsilon_0} \\ \nabla\times\bm{E}&=-\pd{\bm{B}}{t} \\ \nabla\cdot\bm{B}&=0 \\ \nabla\times\bm{B}&=\mu_0\bm{J}+\mu_0\epsilon_0\pd{\bm{E}}{t} \end{aligned}$$
- Lorentz force law:
$$\bm{F}=q(\bm{E}+\bm{v}\cdot\bm{B})$$
- The continuity of charge:
$$\pd{\rho}{t}+\nabla\cdot\bm{J}=0$$


### In matter
- These forms are _independent of material_
$$\begin{aligned}\nabla\cdot\bm{D}&=\rho_{free} \\ \nabla\times\bm{H} &= \bm{J}_{free}+\pd{\bm{D}}{t}\end{aligned}$$


## Electrostatics
### The electrostatic force and field
- _Coulomb's law_ between 2 point charges
 $$\bm{F}=\frac{1}{4\pi\epsilon_0}\frac{q_1q_2}{r^2}\bm{\hat{r}}$$
- Define a vector field $\bm{E}$ caused by some charge, which causea a force $\bm{F}$ on an infinitesimally small test charge $q$:
$$\bm{F}=q\bm{E}(\bm{r})$$
- The _electric field_ of a charge $q$:
$$\bm{E}(\bm{r})=\frac{1}{4\pi\epsilon_0}\frac{q}{r^2}\bm{\hat{r}}$$

- The superposition principle: electric fields from several charged particles are (vectorially) additive — electrostatics is linear (in a vacuum)

### The electrostatic potential
- The work done to move a charge from $\bm{r}$ to $\bm{r+}d\bm{r}$:
 $$dW=-d\bm{r}\cdot\bm{F}(\bm{r})$$
	 - The work is oone _against_ the force $\bm{F}$
- The electrostatic potential difference:
$$dV=-d\bm{r}\cdot\bm{E}(\bm{r})$$
- The potential difference $V$ between 2 points is the _work required per unit charge_ to move an _infinitesimally small unit charge_ between the 2 points
- The point of zero potential is chosen arbitrarily, often infinity
- The potential difference from $A$ to $B$:
$$V_{BA}=-\int_A^Bd\bm{r}\cdot\bm{E}(\bm{r})$$
- The electrostatic potential $V(\bm{r})$ is a scalar field

- $V(\bm{r})$ is a _path-independent_ field (only the end-points matter) _for an electrostatic system_
	- Consider moving a charge from $A$, to $B$, then back to $A$

- From the definitions of the gradient and $V$:
$$\bm{E}(\bm{r})=-\nabla V(\bm{r})$$
- The physical interpretation of $V$:
	- The electric field $\bm{E}$ points in the direction where $V$ _decreases most rapidly_
	- $|\nabla V(\bm{r})|$ is the maximum rate of change

- $V$ is defined to within a spatially constant offset, as only $\bm{E}$ is physically observable
- The undefined constant is the _gauge_, to make time-varying fields mathematically simpler

- Often simpler to find add potentials using superposition, then use grad to find $\bm{E}$

### The spatial derivatives of an electrostatic field
- Use the fact that the p.d. around a loop is zero
- Consider moving a charge through a loop in a plane, in an _electrostatic system_:
$$\pd{E_i}{x_j}=\pd{E_j}{x_i}$$
- This can be expressed using the curl, and Stokes' theorem:
$$\nabla\times\bm{E}=0$$
### Monopoles
- A monopole is defined as a _single point charge_ $q$
- Using the definition of $V$, its electrostatic potential is:
$$V(\bm{r})=\frac{1}{4\pi\epsilon_0}\frac{q}{r}$$
- Its electric field can be rederived from the potential
	- As the system is spherically symmetric, the field is radial and independent of $\theta$ or $\phi$

- A charge can be regarded as a "source" of field lines

### Dipoles
- A dipole is defined as two point charges $+q$ and $-q$ placed at a _short distance_ $a$ apart
	- No overall net charge
	- _Direction_ of the dipole is from $-q$ to $+q$

- Due to the separation, $\bm{E\neq0}$
- Using the superposition principle for potentials, for $r>>a$:
 $$V(r,\theta)=\frac{1}{4\pi\epsilon_0}\frac{qa\cos\theta}{r^2}$$
	- Falls off _quicker than the monopole_ 
- Define the _dipole moment_ $p\equiv qa$:
$$V(\bm{r})=\frac{1}{4\pi\epsilon_0}\frac{\bm{p\cdot r}}{r^3}=\frac{1}{4\pi\epsilon_0}\frac{\bm{p\cdot\hat{r}}}{r^2}$$
- The electric field is:
 $$\bm{E}(\bm{r})=\frac{1}{4\pi\epsilon_0}\frac{p}{r^3}\left[\bm{\hat{r}}\, 2\cos\theta+\bm{\hat{\theta}}\,\sin\theta\right]=\frac{1}{4\pi\epsilon_0}\frac{p}{r^3}\left[3(\bm{p\cdot \hat{r}})\bm{\hat{r}} -\bm{p}\right]$$
	- As expected, falls off quicker than the monopole
	- As separation decreases, $|\bm{E}|$ tends to zero as expected
	- At $\theta=0$, the field is radial
	- At $\theta=\pi/2$, the field is azimuthal

#### A dipole in a uniform electric field
- The _force and couple_ on a dipole in a uniform field:
	- The charges experience the _same force in opposite directions_
	- The dipole actually experiences a _couple_:
	$$\bm{G=p\times E}$$
	- The couple is zero when the dipole is aligned with the field
	- Equilibrium is alignment

- The _potential energy_ of a dipole in a uniform field:
	- No work needs to be done for displacement
	- Consider work done to _increase the angle_ by $d\theta$
	- Taking $\theta=\pi/2$ as the reference:
	$$U=-\bm{p\cdot E}$$
	- Negative when dipole is more aligned
	- Stable equilibrium when $\theta=0$, unstable equilibrium when $\theta=\pi$


#### A dipole in a non-uniform electric field
 - The force on the dipole:
	 - The electric field at the positive charge can be written as:
	 $$\bm{E^+}=\bm{E^-}+\bm{a\cdot}(\nabla \bm{E})$$
	 - The force on the dipole is:
	 $$F=(\bm{p \cdot \nabla})\bm{E}$$
		 - For a constant dipole moment, $F=\nabla[\bm{p\cdot E}]$
		- It can be written as $F=-\nabla U$
		- $U$ is _rotational_ potential energy
	- For a _fixed, rigid_ (i.e. non-induced) dipole, the dipole will move to a position where it is aligned with the field
	- This calculation assumes the dipole _will not rotate_

### The multipole expansion
- _Expand_ the potential of any charge distribution 
- Monopole - net charge, $V \propto 1/r$
- Dipole: No net charge, net dipole moment, $V\propto 1/r^2$
- Quadrupole: 2 dipoles pointing in opposite directions, $V\propto 1/r^3$

- For any general distribution, many terms will be present simultaneously
- Definition of monopole:
$$Q=\int\,dV\,\rho(\bm{r})$$
- Definition of dipole:
$$\bm{p}=\int\,dV\bm{r}\,\rho(\bm{r})$$
- Quadrupole: tensor

- Any potential can be expeanded with a linear combination of terms

- More mathematical details: [[Topics in Electromagnetism#Multipole expansion|Multipole expansion]]

### Electric flux and Gauss' Law for electrostatics
- Quantify "field line density" using the concept of _electric flux_:
$$\int_S d\bm{S}\cdot\bm{E}(\bm{r})$$
	- Not exactly a "measurable" quantity

- _Charge conservation and continuity_: consider a _current density_ $\bm{J}$ through a closed surface
$$I=\oint_Sd\bm{S}\cdot\bm{J}=-\pd{}{t}\int\,dV\,\rho=\int_V\,dV \,\nabla\cdot\bm{J}$$
- _Continuity_ equation:
$$\pd{\rho}{t}+\nabla\cdot\bm{J}=0$$

- Consider the flux through a closed surface enclosing a _single_ charge:
$$\int_Sd\bm{S}\cdot\bm{E}(\bm{r})=\frac{q}{\epsilon_0}$$
- _Does not matter where_ the charge is within the surface
- Shape can be _arbitrary_

- Assume a continuous charge distribution, and use superposition
- The integral form of the _Gauss Law for Electrostatics_:
$$\oint_{S=\partial V}d\bm{S}\cdot\bm{E}(\bm{r})=\frac{1}{\epsilon_0} \int_VdV\,\rho(\bm{r})$$
- The differential form:
$$\nabla\cdot\bm{E}=\frac{\rho}{\epsilon_0}$$

- The electric _displacement_/electric flux density:
$$\bm{D}(\bm{r})=\epsilon_0\bm{E}(\bm{r})$$
$$\oint_{S=\partial V}d\bm{S}\cdot\bm{D}(\bm{r})=\int_VdV\,\rho(\bm{r})$$
$$\nabla\cdot\bm{D}=\rho$$

### Applying Gauss's Law to charge distributions
- An _infinite, uniform sheet_ of charge: draw a _Gaussian pillbox_
$$\bm{E}=\frac{\sigma}{2\epsilon_0}\bm{\hat{n}}$$
	- Infinite size leads to symmetry and a normal electric field
	- Capacitor: 2 parallel sheets of opposite sign, $\bm{E}=\sigma/\epsilon_0\bm{\hat{n}}$

- An _infinite, uniform line_ of charge: draw a _Gaussian cylinder_
$$\bm{E}=\frac{\lambda}{2\pi\epsilon_0r}\bm{\hat{r}}$$
	- Potential between points at distances $r$ and $r_0$: $V=\lambda/(2\pi\epsilon_0)\ln(r/r_0)$
	- Coaxial cable: two cylinders

### Laplace's and Poisson's equations
- Consider the field at a point, expressed using the potential
- Poisson's equation:
$$-\nabla\cdot\bm{E}=\nabla\cdot(\nabla V)=\nabla^2V=-\frac{\rho}{\epsilon_0}$$
- Laplace operator: measure of curvature (relates curvature to charge density)

- Special case: _charge-free_ region
- Here, one gets Laplace's equation:
$$\nabla^2V=0$$
- [[Poisson and Laplace's equations|How to solve the damn things]]


### Capacitance
- Consider two conducting surfaces with potential difference $V$, holding opposite amounts of charge $Q$, the capacitance $C$ is:
$$C=\frac{Q}{V}$$
- Reference point can be anywhere on the two surfaces

### Electrostatic energy

#### Assembly of charges
- Assemble a system of point charges $q_i$ from infinity
- Adding up the energy from assembling each individual charge:
$$U_N=\sum_{j=1}^N\sum_{i<j}\frac{1}{4\pi\epsilon_0}\frac{q_jq_i}{r_{ij}}$$

- Modifying the sum:
$$U_N=\frac{1}{2}\sum_{j=1}^Nq_j\sum_{i\neq j}\frac{1}{4\pi\epsilon_0}\frac{q_i}{r_{ij}}=\frac{1}{2} \sum_{j=1}^Nq_jV_j$$
	- $V_j$: potential of all charges _except $q_j$_

- For a continuous distribution of charge: $q_i\rightarrow \rho \,d^3\bm{r}$
$$U=\frac{1}{2}\int d^3\bm{r}\,\rho(\bm{r})\,V(\bm{r})$$
	- $V(\bm{r})$ still does not involve the infinitesimal charge element at $\bm{r}$

#### Energy in a capacitor
- Sum over $N$ infinitesimal charges $dQ$ so $Q=NdQ$:
$$U=\frac{1}{2}\frac{Q^2}{C}=\frac{1}{2}QV=\frac{1}{2}CV^2$$

#### Energy stored in the electric field
- Energy can be considered to be stored in the field itself

- By considering a parallel plate capacitor, with area $A$ and distance $d$:
$$U=\frac{1}{2}QV=\frac{1}{2}\epsilon_0|\bm{E}|^2\,(Ad)$$

- This gives an _energy density_ $U_E$:
$$U\equiv\int\,d^3\bm{r}\;U_E(\bm{r})=\int d^3\bm{r}\,\frac{1}{2}\epsilon_0 |\bm{E}(\bm{r})|^2$$

- Considering electric displacement:
$$U=\int d^3\bm{r}\,\bm{D}(\bm{r})\cdot\bm{E}(\bm{r})$$
- _Also valid for dielectrics_

- For _any_ arbitrary charge distribution, over any arbitrary surface:
$$U=\frac{1}{2}\epsilon_0\left[\int d^3\bm{r}\,|\bm{E}(\bm{r})|^2+\int d\bm{S}\cdot[V(\bm{r})\bm{E}(\bm{r})]\right]$$
- The integral must be taken _at infinity_ for the second term to vanish

#### Some nuance
- When dealing with point charges, $\sum \frac{1}{2}qV$ is the energy required to _assemble_ the charges
	- Here, $V$ does not include the potential of the charge itself (since it blows up)
- When dealing with a continuous distribution, $\frac{1}{2}\int \rho V  \,d^3\bm{r}$ is the energy of the _entire system_
	- Here, $V$ is the _full potential_ as the infinitesimal charge has a negligible contribution
- The energy of the whole system is also calculated by $\frac{1}{2} \int \epsilon_0|\bm{E}|^2\,d^3\bm{r}$ over all space
	- One may find that from this, the energy of a point charge is _infinite_

- Conclusion: for point charges, sum; for continuous distributions, integrate

- In the context of electrostatics, the energy is not "stored" anywhere
- In radiation theory and relatvity, the energy is stored _in the field_

>[!quote]
The infinite energy of a point charge is a recurring source of embarrassment for electromagnetic theory, afflicting the quantum version as well as the classical.
>-David J. Griffiths

### Virtual work in electrostatics
- Write down the energy as a function of a displacement of something in the system
	- Account for work done by an external mechanical system
	- Account for energy dissipated or supplied by external circuit components
- Work done on a system to change a distance from $x$ to $x+dx$ is:
$$F\,dx=\pd{U_s}{x}\,dx+\pd{U_d}{x}\,dx$$
	- $U_s$: energy stored in system
	- $U_d$: energy dissipated from system

- Example: force between two _isolated_ (constant charge) ppositely charged parallel plates
	- No energy dissipated, stored energy increases
	- Constant force _independent of distance_, proportional to plate area
	- Can also be calculated by considering charge on one plate experiencing the field of the other

- Example: force between capacitor plates with _constant voltage_ $V$
	- As $x$ increases, $E$ falls due to constant $V$ --> charge falls as current flows between the plates _through a battery_
	- Stored energy _decreases_ with increasing $x$
	- Energy is _dissipated_ as charge moves to the other plate ($dQ<0, dE_d=-VdQ$)
	- Force is proportional to $1/x^2$, still proportional to plate area


### Homogeneous Dielectrics
- Previously: free space and conductors
- Dielectrics: insulating materials
	- No free charge in the material itself, only _bound charges_
	- Overall neutral

- When an external electric field is applied, positive and negative _bound charges separate_, and a dipole moment is induced
- For uniform $\bm{E}_0$ and a homogeneous material, charge only appears on external surfaces
	- Charges inside are _cancelled out_ (they don't move to the surface!)

- _Linear dielectrics_: induced dipole moment is linearly proportional to $\bm{E}_0$
	- Non-linear behaviour emerges for high $\bm{E}_0$
- _Isotropic materials_: magnitude of induced dipole moment is independent of orientation of $\bm{E}_0$ relative to the material

- _Polarisation_ $\bm{P}$: dipole moment _per unit volume_
	$$\bm{P}=\frac{d\bm{p}}{dV}$$
	- Independent of material size and shape

- Consider an infinitesimal cubic volume of polarised dielectric material
- When putting microscopic volumes together in a _uniform_ $\bm{E}_0$, _surface charges cancel_
- Surface bound charge density:
$$\sigma=\bm{P\cdot\hat{n}}$$

- Putting a linear dielectric in a capacitor
	- _Constant potential_: as bound charges are induced, _free charge increases_ to maintain the electric field
	- _Constant free charge_: due to induced charges, total charge decreases and _potential decreases_

- The total charge on a capacitor plate can be written as:
$$Q=\epsilon_0(1+\chi)|\bm{E}|A$$
	- Two contributions: original without dielectric, and extra to offset bound charge
	- $\chi=$ electrical susceptibility, property of the material that gives surface polarisation

- Define the _relative permittivity_ $\epsilon$:
$$\epsilon=1+\chi$$
- Then, the capacitance becomes:
$$C=\frac{Q_f}{V}=\frac{\epsilon_0\epsilon A}{d}$$

- Consider a non-uniform external field
- $\bm{P}$ is also non-uniform, and not all bound charges in the interior are cancelled out
- Consider microscopic volumes put together, one gets a volume bound charge density:
$$\rho=-\nabla\cdot\bm{P}$$
	- Analagous to free charge being a source of the electric field

- Integrating $\rho$ over the volume of the dielectric and applying the divergence theorem:
$$-\int_\mathcal{V}\nabla\cdot\bm{P}\,d^3\bm{r}=\int_{S= \partial\mathcal{V}}\bm{P}\cdot d\bm{S}$$
	- The interior bound charge is equal and opposite to the surface bound charge

- [[Dielectric and magnetic materials|Applications in materials science]]
#### Gauss' Law in dielectrics
- The total charge density is $\rho_f+\rho_b=\epsilon_0\nabla\cdot \bm{E}$
- Define the _electric displacement_ $\bm{D}$:
$$\bm{D}\equiv\epsilon_0\bm{E}+\bm{P}$$
	- Also known as _electric flux density_
- Gauss' Law for dielectrics:
$$\nabla\cdot\bm{D}=\rho_f$$
- For linear dielectrics, using the definition of relative permittivity:
$$\bm{D}=\epsilon\epsilon_0\bm{E}$$
- If $\epsilon$ is constant, $\rho=\nabla\cdot\bm{E}=\rho_f/(\epsilon\epsilon_0)$
	- Total charge density reduced due to bound charge
- This form of Gauss' Law is independent of material properties

#### Remarks about dielectrics
- The induction of a dipole is an _approximation_
- A charge distribution is described by a _hierarchy of terms_
- The dipole is the lowest order term
- The gradient of $\bm{E}$ induces a quadrupole
- The second spatial derivative induces an octopole

- The electric field $\bm{E}$ is more "fundamental", and is an actual measurable quantity

#### Situations involving dielectrics
- _Constant potential_ between a collection of equipotential surfaces:
	- _$\bm{E}$ is determined_ and fixed
	- $\bm{D}$ gives free charge on the surfaces
	- Free charge is dependent on $\epsilon$ as potential is maintained
- _Constant free charge_ between a collection of equipotential surfaces
	- _$\bm{D}$ is determined_ and fixed
	- $\bm{E}$ and $V$ depend on $\epsilon$ as a dielectric is introduced, to maintain free charge

### Inhomogeneous dielectrics and boundary conditions
- Inhomogeneous dielectric: $\epsilon$ varies with position
- Consider a flat boundary where $\epsilon$ has a _discontinuity, with no free charge_

- Draw a Gaussian pillbox across the boundary
- Since there should be no free charge on the surface:
$$\bm{D}_{\perp1}=\bm{D}_{\perp2}$$
- $\bm{E}_\perp$ _must be discontinuous_ due to the discontinuity in $\epsilon$

- As for the parallel component, using Stokes' Theorem:
$$\bm{E}_{||1}=\bm{E}_{||2}$$
- $\bm{D}_{||}$ _must be discontinuous_

- Due to these discontinuities, field lines for $\bm{D}$ and $\bm{E}$ change direction
- $\bm{E}$ field lines can terminate on surface bound charges
- $\bm{D}$  and $\bm{E}$ field lines are parallel

- The direction, parametrised by an angle $\theta$ to the normal:
$$\frac{\cot\theta_2}{\cot\theta_1}=\frac{\epsilon_1}{\epsilon_2}$$
- The magnitudes of $\bm{P}$ and $\bm{E}$ of a dielectric body in an external field is heavily dependent on shape

- Dielectric sphere in a uniform field:
	- Uniform electric field in sphere
	- Sphere is polarised and acts as a dipole
	- From solving Laplace's equation and applying the appropriate boundary conditions:
$$\bm{E}_\text{in}=\frac{3}{\epsilon+2}\bm{E}_0$$

### Energy density in dielectrics
- The same formula for energy from $\rho$ and $V$ applies:
$$U=\frac{1}{2}\int d^3\bm{r}\,\rho(\bm{r})V(\bm{r})$$
- Following a similar derivation as above:
$$U=\frac{1}{2}\int\,d^3\bm{r}\,\bm{D}(\bm{r})\cdot\bm{E}(\bm{r})$$
- Interpretation: bringing in free charge, which _induces bound charge_
	- Work done in inducing bound charges accounted for in $V$
- This is only suitable for _LINEAR dielectrics_

- From the approach of bringing in bits of free charge, a change in energy is:
$$dU=\int(\Delta \bm{D})\cdot\bm{E}\;d^3\bm{r}$$

## Magnetostatics
- Just as charges give rise to electric fields, moving charge gives rise to magnetic fields

- Electrostatics: static charges
- Magnetostatics: constantly moving charges, time-invariant current

- For time-invariant systems, electric and magnetic fields are separate
	- No need to deal with [[Relativity]]

### The Lorentz Force and the Biot-Savart Law
- Let there be a test current element $d\bm{l}$, with its direction defining the current flow
- The _magnetic field_ $\bm{B}$ is defined through the force exerted on the test current:
$$d\bm{F}=Id\bm{l}\wedge\bm{B}$$

- The _Lorentz force_ is the force on a moving charge, accounting for both $\bm{E}$ and $\bm{B}$:
$$\bm{F}=q(\bm{E}+\bm{v}\wedge\bm{B})$$

- The _Biot-Savart law_ described the magnetic field _produced_ by a test current:
$$d\bm{B}=\frac{\mu_0I}{4\pi r^2}d\bm{l}\wedge\bm{\hat{r}}$$
	- $\mu_0$: _permeability_ of free space

- The magnetic field also decreases as an inverse square
- The magnetic field lines _circulate around current_
- There are _no point sources_ (magnetic monopoles)

- The total magnetic field:
$$\bm{B}=\frac{\mu_0}{4\pi}\int d\bm{l}\wedge\bm{\hat{r}}\,\frac{I}{r^2}$$
- The force between two current elements, with displacement $\bm{r}$ from $d\bm{l}_1$ to $d\bm{l}_2$:
$$d\bm{F}_2=\frac{\mu_0}{4\pi}I_1I_2\,d\bm{l}_2\wedge(d\bm{l}_1 \wedge\frac{\bm{\hat{r}}}{r^2})$$
- Maximum when aligned
- Attractive if current flow is in the same direction

### Gauss' Law for magnetic fields
- Like the electric flux, the magnetic flux is given by:
$$\Phi_B=\int_S d\bm{S}\cdot\bm{B}(\bm{r})$$
- This gives the magnetic field $\bm{B}$ another name: the _magnetic flux density_
- Using the properties of the field (no monopoles):
$$\displaylines{\oint_S d\bm{S}\cdot \bm{B}=0\\ \nabla\cdot\bm{B}=0}$$
- This is _Gauss' Law for the magnetic field_

### Magnetic dipoles
- No monopoles: smallest unit is a dipole
- Dipole: infinitesimally small current loop

#### Uniform magnetic field
- Consider an infinitesimal current loop in a uniform magnetic field
- The current loop experienced a couple of forces to produce a torque
- For a large current loop with area elements $d\bm{S}$, the _magnetic dipole moment_ is:
$$\bm{m}=I\int_S d\bm{S}$$
- The couple it experiences is:
$$\bm{G}=\bm{m}\wedge\bm{B}$$

- By considering _work done to rotate the dipole_ by $d\theta$, where $\theta$ is relative to $\bm{B}$:
$$U=-\bm{m}\cdot\bm{B}$$
	- Minimum when aligned with the field
	- For a macroscopic current loop, the energy becomes $-I\Phi$


#### Non-uniform magnetic field
- By considering infinitesimal current loops in the field:
$$\bm{F}=m_j\pd{B_j}{x_i}\bm{e}_i$$
- For a _uniform dipole moment_:
$$\bm{F}(\bm{r})=\nabla[\bm{m}\cdot\bm{B}(\bm{r})]$$
- A _fixed_ dipole tends to move to a position where it can be _aligned with the field_

### The magnetic scalar potential
- Define a _magnetic field strength_ $\bm{H}(\bm{r})$:
$$\bm{B}(\bm{r})=\mu_0\bm{H}(\bm{r})$$
- We would like to describe it in terms of a _magnetic scalar potential_ $\phi_m(\bm{r})$:
$$\displaylines{\bm{H}(\bm{r})=-\nabla\phi_m(\bm{r}) \\ \bm{B}(\bm{r})=-\mu_0\nabla\phi_m(\bm{r})}$$
- As in the case of the electric field, this representation is valid when _the curl is zero_

- The curl is zero _except where there are currents_
- A scalar potential _can be defined for regions far away from currents_

- Physical meaning of $\phi_m$: _unrelated to work_, simply the shape of a landscape to generate $\bm{B}$

#### Magnetic scalar potential of a current loop
- The solid angle $d\Omega$ is defined by an element of surface area $d\bm{S}$ on a sphere of radius $r$:
$$d\Omega=\frac{|d\bm{S}|}{r^2}$$
- If the centre is not at the centre of the sphere, or the surface is not spherical:
$$d\Omega=\frac{|d\bm{S}|}{r^2}\cos\theta=\frac{d\bm{S\cdot r}}{r^3}$$
- $\bm{r}$ points outwards from a closed surface, hence the surface normal points _inwards_
- The infinitesimal dipole moment of a current loop is $d\bm{m}=Id\bm{S}$
- Using the same formula as the [[#Dipoles|electrostatic potential of an electric dipole]]
$$\phi_m(r,\theta)=\frac{|d\bm{m}|\cos\theta}{4\pi r^2}$$
- By inspection and substituting the solid angle
- For a larger loop, simply add up all the $d\bm{m}$

- Hence, the magnetic scalar potential at some point is _proportional to the solid angle $\Omega$subtended by the loop when viewed from the observation point_
$$\phi_m=\frac{I\Omega}{4\pi}$$

### Ampere's Law
- Consider a current loop with current $I$
- Integration path: from one side to the loop, to infinity, circle back to the other side
- $\Omega$ along the path: $2\pi$, $0$, $-2\pi$
- The scalar potential along the path is _not single-valued_
- By considering the integral of $d\phi_m=d\bm{l}\cdot\nabla\phi_m$, one gets _Ampere's Law_:
$$\oint d\bm{l}\cdot\bm{B}=\mu_0I$$
- It can be expressed in terms of _current density_:
$$I=\int d\bm{S}\cdot\bm{J}$$
- Using Stokes' Theorem and the definition of magnetic field strength:
$$\nabla\wedge\bm{H}=\bm{J}$$

### Applying Ampere's Law
#### The infinite wire
- The magnetic field from an infinite wire with current $I$:
$$\bm{B}=\frac{\mu_0I}{2\pi r}\hat{\phi}$$
- By expressing the [[Vector calculus in 3-dimensions#Gradient in orthogonal curvilinear coordinates|gradient in cylindrical coordinates]], one can find the scalar potential:
$$\phi_m=-\frac{I\phi}{2\pi}$$
	- The field points _downhill_
	- The potential is _multi-valued_, and _potential difference cannot describe energy_

#### Two parallel infinite wires
- The _force per unit length_ between two infnite, parallel wires with separation $a$:
$$F=\frac{\mu_0I_1I_2}{2\pi a}$$
	- Attractive if the currents flow in the same direction

- The potential:
	- If the currents are in opposite directions, there is a _discontinuity_ along the line joining the wires
	- Same diection: discontinuity only occurs along a closed path enclosing a current

#### The solenoid
- A long solenoid with $n$ turns per unit length:
	- Consider a loop enclosing a section of the current, extending to infinity
	- Field outside the solenoid is zero
	$$B=\mu_0 nI$$

### The magnetic vector potential
- Define a magnetic vector potential $\bm{A}$:
$$\bm{B=\nabla\wedge A}$$
- Automatically fulfills Gauss' Law

- Scalar potentials are defined to within an arbitrary constant
- Vector potential determined to within a _gauge_ 

- Gauge: vector $\bm{K}$ which satisfies
$$\bm{K}=K_x(x)\bm{e}_x+K_y(y)\bm{e}_y+K_z(z)\bm{e}_z$$
- The divergence of $\bm{A+K}$ _is dependent on_ $\bm{K}$

- The definition of the vector potential _does not constrain the divergence_
- A typical gauge is:
$$\bm{\nabla\cdot A}=0$$

- From Ampere's Law, the Poisson's equation for the magnetic vector potential:
$$-\nabla^2\bm{A}=\mu_0\bm{J}$$
- By _comparing with the electrostatic_ case:
$$\bm{A}(\bm{r})=\frac{\mu_0}{4\pi}\int \frac{\bm{J}(\bm{r'})}{|\bm{r-r'}|}\,d^3\bm{r'}$$

- $\bm{A}$ analagous to $V$, $\rho$ analagous to $\bm{J}$

- Special relativity: the potential 4-vector $(V,\bm{A})$ and the density $(\rho,\bm{J})$
	- Static charge is the source of the electric field
	- Moving charge is the source of the magnetic field
	- When changing the observer, the fields also change

### Current resistivity and conductivity
- Consider a volume of material with surface area $S$, length $l$ and a potential difference of $V$
- The current follows Ohm's Law:
$$V=IR$$
- The current is proportional to $V$, $S$, and $1/l$
- $V=|\bm{E}|/l$, $J=I/S$
- From this, Ohm's Law can be _reformulated to include current_:
$$\bm{J}=\sigma\bm{E}$$
- $\sigma$ is the _conductivity_, equal to $1/\rho$, where $\rho$ is the _resistivity_

### Magnetostatic fields in homogeneous magnetic materials
- Magnetically polarisable materials change how magnetic field lines behave
- Types: _diamagnetic_, _paramagnetic_, _ferromagnetic_
- Properties stem from _magnetic dipole moments of atoms and molecules_
	- Dipole moments: orbital and intrinsic spin angular momenta of electrons

- Diamagnetic materials: _oppose applied external magnetic field_
- Paramagnetic materials: _permanent dipoles align with external magnetic field_
- Ferromagnetic materials: _effect of alignment is enhanced_

#### Volume magnetisation currents
- Magnetisation currents create small dipole moments
- Randomly aligned dipoles produce no net circulating current, and no net dipole moment
- Aligned dipoles produce net circulating current and dipole moment

- _Magnetisation_ $\bm{M}$: _magnetic_ dipole moment _per unit volume_
$$\bm{M}=\frac{d\bm{m}}{dV}$$
- Total dipole moment:
 $$\bm{m}_\text{tot}=\int d^3\bm{r}\,\bm{M}$$
	 - Random alignment leads to a vector sum of zero

- Consider four current loops with a common edge along one Cartesian axis
- One can then find the _magnetisation current density_ $\bm{J}_m$:
$$\bm{J}_m=\nabla\wedge\bm{M}$$
- Magnetisation current is _distinct from moving free charge_
- Analagous to [[#Homogeneous Dielectrics|electrostatic case]]
- Current can be said to be _fictitious_ as it only serves to model atomic dipole moments

- Uniform magnetisation leads to zero bound current as currents around loops sum to zero

#### Surface magnetisation currents
- For a uniform $\bm{M}$, some magnetisation currents must reside on the surface

- Consider a block with uniform magnetisation
- All currents cancel out inside
- On the surface, there is a charge density $\sigma$ flowing
- The current can be described by the _surface current density_ $\bm{K}_m$
$$I=\int \bm{K}_m\cdot d\bm{l}$$
- By considering one surface of the block, the surface current density is:
$$\bm{K}_m=\bm{M}\wedge\bm{\hat{n}}$$
#### Ampere's Law in magnetic materials
- Total current = flow of free charge + magnetisation current
- Magnetisation current _will also produce a force on some test current_
- Modify Ampere's Law accordingly:
$$\nabla\wedge\bm{B}=\mu_0[\bm{J}_\text{free}+\bm{J}_m]$$
- Define the _magnetic field strength_ $\bm{H}$:
$$\mu_0\bm{H}=\bm{B}-\mu_0\bm{M}$$
- Then, Ampere's Law becomes:
$$\nabla\wedge\bm{H}=\bm{J}_\text{free}$$
- Using Stokes' Theorem:
$$\oint \bm{H}\cdot d\bm{l}=I_\text{free}$$
- This form is independent of material properties

#### Magnetic permeability in materials
- To calculate forces, $\bm{B}$ is needed, and $\bm{M}$ is required for that
- For _most materials, in the small-field limit_, $\bm{M}$ is linearly proportional to $\bm{H}$:
$$\bm{M}=\chi_m\bm{H}$$
- $\chi_m$ is the _magnetic permeability_
- The magnetic field is then given by:
$$\bm{B}=\mu_0(1+\chi_m)\bm{H}\equiv\mu_0\mu\bm{H}$$
- $\mu$ is the _relative permeability_

- Non-magnetic materials: $\mu\approx 1$
- Unlike electric susceptibility, magnetic permeability can be _positive or negative_
- Magnetic materials:
	- Diamagnetics - $\chi_m<0$
	- Paramagnetics - $\chi_m>0$
	- Ferromagnetics - $\chi_m>>1$

- Ferromagnetic materials: $\bm{B}$ and $\bm{H}$ _become non-linear_
	- Ferromagnetics can display _hyteresis_
	- Materials can be _permanently magnetised_

- Like the case of dielectrics, susceptibility can be a _tensor_ for anisotropic materials
	- $\bm{B}$ does not need to be parallel to $\bm{H}$

### Inhomogeneous magnetic materials and boundary conditions
- Consider a flat boundary with a discontinuity in $\mu$, with _no free current_

- The perpendicular component of $\bm{B}$: use _Gauss' Law for the magnetic field_
$$\bm{B}_{1\perp}=\bm{B}_{2\perp}$$
- $\bm{H}_\perp$ will then be discontinuous

- The parallel component of $\bm{H}$: use _Ampere's Law_
$$\bm{H}_{1||}=\bm{H}_{2||}$$
- $\bm{B}_{||}$ will then be discontinuous

- The magnetisable sphere:
	- No free current --> consider the [[#The magnetic scalar potential|magnetic scalar potential]]
	- Similar solution to dielectric sphere:
	$$\bm{H}_\text{in}=\frac{3}{\mu+2}\bm{H}_0$$

- Uniformly magnetised cylinder: model for a bar magnet
	- Magnetisation currents flow around the surface, _similar to solenoid_
	- Small-field approximation for $\bm{M}$ _no longer applies
	- From the definition of $\bm{H}$, it _is opposite to $\bm{B}$ inside the magnet_
	- Field lines at cylindrical surface will curve due to edge effects

### Comparing behaviour of electric and magnetic fields
- Fundamental quantities in electrostatics and magnetostatics:
	- $\bm{E}$ gives force on a test charge
	- $\bm{B}$ gives force on a test current

- $\bm{H}=\bm{B}/(\mu_0\mu)$ and $\bm{D}=\epsilon\epsilon_0\bm{E}$ are _derived quantities_ for magnetic materials and dielectrics
	- Free charges are the source of $\bm{D}$
	- Free currents are the source of $\bm{H}$

- In terms of boundary conditions:
	- $\bm{B}$ and $\bm{D}$ are alike
	- $\bm{H}$ and $\bm{E}$ are alike
- Normal components of $\bm{B}$ and $\bm{D}$ are _continuous_, making them _conserved fluxes_

![[Boundary conditions.png|250px]]

### Electromagnets
- Consider a _coil of wire_ wrapped around a _toroidal core_ of magnetisable material
- Assume $N$ turns with current $I$ around a _continuous_ toroidal core
- Core: high permeability $\mu$

- Apply _Ampere's law_ around a closed loop, _inside the core_
- If cross-sectional width is _much smaller_ than radius $r$:
$$\bm{H}_\text{in}=\frac{NI}{2\pi r}\hat{\phi}$$
- The _magnetic field_ is:
$$\bm{B}_\text{in}=\frac{\mu_0\mu NI}{2\pi r}\hat{\phi}$$

- Consider a small _air gap_ of length $l$
- Magnetic field $\bm{B}$ is _continuous across the gap_
$$\bm{B}_\text{gap}=\bm{B}_\text{in}$$
- Applying Ampere's Law again:
$$(2\pi r-l)H_\text{gap}+lH_\text{in}=NI$$
- Across the gap, the field is:
$$\displaylines{H_\text{gap}=\frac{\mu NI}{2\pi r+(\mu-1)l} \\ B_\text{gap}\approx \frac{\mu_0NI}{l}}$$
- Approximation works _for high $\mu$_
- Since $\bm{B}$ is conserved across the loop, $H_\text{gap}>>H_\text{in}$

## Electromagnetic induction
- What happens when fields change with time
- _Not quasi-static changes_
- In electrostatics: static charge gives rise to electric fields
- In magnetostatics: moving charge gives rise to magnetic fields

### Faraday's Law
- Empirical findings: 
	- Changing magnetic flux gives an electromotive force (EMF)
	- EMF magnitude proportional to rate of flux change

- Faraday's Law:
$$\oint d\bm{l}\cdot\bm{E}(\bm{r})=-\frac{d}{dt}\int_S d\bm{S}\cdot \bm{B}(\bm{r})$$
- Left term: electromotive force
- Right term: rate of change of magnetic flux

- EMF: _line integral of $\bm{E}$ around closed loop_, not the same as potential difference
- Work done on a unit charge if it travels around the loop

- _Self-inductance_: a _change in current_ flowing in a coil induces an _emf across its own terminals_
	- Also occurs in lengths of wire

- Lenz's Law: induced EMF always promotes a current flow to produce a magnetic field _opposing the change in flux_

- The differential form of Faraday's Law:
$$\nabla\wedge\bm{E}=-\pd{\bm{B}}{t}$$
- When magnetic field is time-independent, the curl vanishes as in the electrostatic case

### EMF from the Lorentz Force
- An _alternative perspective_ on electromagnetic induction
- Consider the _"work done"_ on a moving charge in a _static magnetic field_
	- From the frame of the charge, it experiences an "electric field" $\bm{E}=\bm{v\wedge B}$

- Consider this applied to a loop moving through a constant magnetic field:
$$\mathcal{E}=\oint d\mathcal{E}=\oint (\bm{v}\wedge \bm{B})\cdot d\bm{l} $$
- By exchanging $\bm{v}$ and $\bm{B}$, and writing $\bm{v}\wedge d\bm{l}$ as $d\bm{S}/dt$:
$$\mathcal{E}=-\frac{d}{dt}\int_\text{loop}\bm{S}\cdot\bm{B}=-\frac{d\Phi}{dt}$$

- Faraday's Law _DOES NOT CARE_ if the field is static and the circuit is changing, or vice versa

### Self-inductance
- The flux _linked back into_ a circuit as a consequence of the current in the same circuit
- Change in current --> change in $\bm{B}$ --> change in flux --> voltage
- Heavily dependent on geometry

- The _self-inductance_ is defined as:
$$L\equiv\frac{\Phi}{I}$$

- Example: a solenoid
	- The flux linked back to the _complete circuit includes all loops_
	- From this, the self-inductance _per unit length_ is:
$$\frac{L}{l}=\mu_0n^2S$$

- For most circuits, _flux within the wires_ is insignificant as _penetration depth_ is very low for higher frequencies

### Inductors and capacitors in circuits
- Consider an _open loop of wire_ with a small gap
	- Electric field is _zero inside the wire_, so it does not contribute to the line integral
$$V_\text{gap}=-\int_\text{gap} d\bm{l}\cdot\bm{E}=+\frac{d\Phi}{dt}=L\frac{dI}{dt}$$
- Consider a [[#Capacitance|capacitor]], the definition of capacitance gives:
$$I=C\frac{dV}{dt}$$
- Consider a circuit with capacitace, resistance and inductance, with no time-dependent $\bm{B}$:
$$V=\frac{q}{C}+IR+L\frac{dI}{dt}$$
- The power delivered by the battery is:
$$VI=\frac{q}{C}I+I^2R+LI\frac{dI}{dt}=I^2R+\frac{d}{dt}\left(\frac{1}{2}\frac{q^2}{C}+\frac{1}{2}LI^2\right)$$
- Therefore, the _energies stored_ in capacitors and inductors are:
$$U_C=\frac{1}{2}CV^2\hspace{1cm}U_L=\frac{1}{2}LI^2$$
- In capacitors, energy is stored in the _electric field_
- In inductors, energy is stored in the _magnetic field
- Resistors only _dissipate_ energy

- Energy storing or dissipating components in physics can be _modelled as equivalent circuits_

### Mutual inductance
- Consider two coils next to each other
- Current $I_1$ in coil 1 produces a flux that links to loop 2, and vice versa
- The _mutual inductance_ $M_{21}$ is defined as:
$$M_{21}=\frac{\Phi_2}{I_1}$$

- Consider a system where $I_1$ is slowly turned on, _followed by_ $I_2$, the energy can be shown to equal:
$$U=\frac{1}{2}L_1I_1^2+\frac{1}{2}L_2I_2^2+M_{12}I_1I_2$$
- This must be _independent_ of which current is switched on first, hence:
$$M_{12}=M_{21}=M$$
- Sign convention of $M$: positive if the currents _produce fluxes in the sam0e direction_

- The mutual inductance can be _combined_ with self-inductance:
$$V_1=L_1I_1+MI_2 \hspace{1.25cm} V_2=L_2I_2+MI_1$$
- Consider two circuits with 2 separate inductors $L_1$ and $L_2$, and mutual inductance $M$:
	- By considering power, the energy is given by the same expression as above

- Rewrite the total energy by completing the square _with respect to_ $I_1$, since the total energy _cannot be negative_, it can be shown that:
$$L_1L_2\geq M^2$$
- We can define a _coupling coefficient_ $k$:
$$M=k\sqrt{L_1L_2}$$
	- $k=0$: No coupling
	- $k=1$: Perfect coupling

- Consider a _doubly wound_ solenoid (wound by 2 _separate_ wires with _different currents and loop density_)
	- For this system, $k=1$

### Transformers
- Consider two coils with number of turns $N_1$ and $N_2$ _coupled by a core of ferromagnetic material_
- Ideality:
	- All flux is _perfectly captured_ by both coils, $k=1$
	- Wires are prerfect conductors, core is linear, no hysteresis

- By considering total flux linkage of the two coils:
$$\frac{V_1}{V_2}=\frac{N_1}{N_2}$$
- Consider a circuit with 2 voltage sources $V_1$ and $V_2$, with currents $I_1$ and $I_2$, the relationship between impedances can be shown to be:
$$Z_1=\frac{j\omega L_1Z_2(N_1/N_2)^2}{j\omega L_1+Z_2(N_1/N_2)^2}\approx Z_2\left(\frac{N_1}{N_2}\right)^2$$

### Energy flow in circuits
- Consider a circuit with resistance $R$, inductance $L$, and capacitor $C$
- With current $I=I_0\cos(\omega t)$, the powers are:
$$P_R(t)=I_0^2R\cos^2\omega t \hspace{1cm} P_L(t)=-\frac{1}{2}I_0^2\omega L\sin2\omega t \hspace{1cm} P_C(t)=\frac{1}{2}I_0^2\frac{1}{\omega C}\sin2\omega t$$
- Energy _always flows into the resistor_ and is dissipated
- Energy is _exchanged between the inductor and capacitor_

- _Resonance_ condition: $P_L+P_C=0$ at all times
	- The same amount of energy is always exchanged between the inductor and capacitor
	- Overall, the only energy supplied is to _compensate for resistive losses_
	- This occurs at the _resonance frequency_ $\omega_0$:
$$\omega_0=\frac{1}{\sqrt{LC}}$$

- $\omega>\omega_0$: $1/\omega C<\omega L$, circuit _looks more like an inductor_ as the capacitor does not store as much energy

- Many electrical systems can be modelled as an $LRC$ circuit


### Magnetic energy
- [[#Electrostatic energy]]: energy _stored in the field_ as _charges are assembled_
- Magnetostatic energy: energy _stored in the field_ as _current loops are assembled_

- By considering a _collection of current loops_, and using the expression for energy [[#Mutual inductance|above]]:
$$U=\sum_\text{loops} \frac{1}{2}\Phi_i I_i$$
- This _includes the energy stored in individual loops_, not just the energy needed to assemble them
	- $\Phi_i$ includes contributions from $M$ and $L$
	- Contributions from $L$: _self-energies_
	- Contributions from $M$: _interaction energies_
	- Energy needed to _assemble_ system: redefine $\Phi_i$ to not include own contribution

- To find a general expression, rewrite the magnetic flux as:
$$\Phi=\int d\bm{S\cdot B}=\oint d\bm{l\cdot A}$$
- Substituting this into the expression above, and using $Id\bm{l}=\bm{J}\,d^3\bm{r}$:
$$U=\frac{1}{2}\int\,d^3\bm{r}\,\bm{J\cdot A}$$

- For _magnetostatic_ problems:
$$U=\frac{1}{2}\int\,d^3\bm{r}\,\bm{A}\cdot(\nabla\wedge\bm{H})=\frac{1}{2}\left[\int d^3\bm{r}\,\bm{H}\cdot\bm{B}-\oint d\bm{S}\cdot(\bm{A\wedge\bm{H}})\right]$$
- Similar to electrostatic energy, by taking the integration surface at infinity:
$$U=\frac{1}{2}\int d^3\bm{r}\,\bm{H}(\bm{r})\cdot B(\bm{r})$$
- The integrand is the _magnetic field energy density_
- This should be compared to the expression for electric field energy density

## Maxwell's equations
- With the Maxwell's equations we have now, _conservation of charge is only satisfied in the steady state_
	- Substitute $\nabla\wedge\bm{H}=\bm{J}$ into the continuity equation

- Maxwell proposed adding a _displacement current_ to Ampere's Law:
$$\nabla\wedge H=\bm{J}+\pd{\bm{D}}{t}$$
- By substituting this into the continuity equation, it can be seen that it is satisfied

- Here, one gets Maxwell's equations _in their full glory_
$$\displaylines{\nabla\cdot\bm{D}=\rho \\ \nabla\wedge E=-\pd{\bm{B}}{t} \\ \nabla\cdot\bm{B}=0 \\ \nabla\wedge H=\bm{J}+\pd{\bm{D}}{t}}$$

>[!quote]
>"All of our cards are now on the table ... now, with Maxwell's equations in their final form, the theory is complete. There are no more laws to be learned, no further generalisations to be considered, and (with perhaps one exception) no lurking inconsistencies to be resolved."
>
>"But in another sense we have just arrived at the starting point. We are at last in possession of a full deck - it's time to deal."
>
>"This is the fun part."
>
>-David J. Griffiths


## Electromagnetic waves

### In free space
- In free space, Maxwell's equations are:
$$\displaylines{\nabla\cdot\bm{E}=0 \\ \nabla\wedge E=-\mu_0\pd{\bm{H}}{t} \\ \nabla\cdot\bm{H}=0 \\ \nabla\wedge H=\epsilon_0\pd{\bm{E}}{t}}$$

- By _taking the curl of the curl of $\bm{E}$_, and using the conditions of free space:
$$\nabla^2\bm{E}=\mu_0\epsilon_0\pd{^2\bm{E}}{t^2}$$
- By using a similar argument:
$$\nabla^2\bm{H}=\mu_0\epsilon_0\pd{^2\bm{H}}{t^2}$$
- In Cartesian coordinates, the Laplacian of the field is:
$$\nabla^2\bm{E}=(\nabla^2 E_x ,\nabla^2 E_y,\nabla^2E_z)$$
- From this, we see that _the fields satisfy the [[Waves#The wave equation|wave equation]]_
- The speed of the wave is:
$$c=\frac{1}{\sqrt{\mu_0\epsilon_0}}=299,792,458 \text{ m s}^{-1}$$
- The speed is _the same for all observers_, leading to Einstein's [[Relativity|special theory of relativity]]

### Plane wave in isotropic medium along the z-direction
- Let the plane wave be propagating along $z$:
$$\pd{\psi(\bm{r},t)}{x}=\pd{\psi(\bm{r},t)}{y}=0$$
- _By considering the curls_, one can see that _longitudinal components are static_
- Hence, EM waves are _transverse waves_

- The _polarisation_ of the wave is defined by the electric field
- The components of $\bm{E}$ and $\bm{H}$ are _linked by Maxwell's equations_

- $x-$polarisation: $E_z$ and $H_y$ propagate _in-phase_ along the $z-$direction at $c$
$$\pd{H_y}{z}=-\epsilon_0\pd{E_x}{t}\hspace{1cm} \pd{E_x}{z}=-\mu_0\pd{H_y}{t}$$

- $y-$polarisation: $E_y$ and $H_x$ propagate _in-phase_ along the $z-$direction at $c$
$$\pd{H_x}{z}=\\\epsilon_0\pd{E_y}{t}\hspace{1cm} \pd{E_y}{z}=\mu_0\pd{H_z}{t}$$

- For linear, isotropic, homogeneous, non-conducting media:
$$v=\frac{1}{\sqrt{\epsilon\epsilon_0\mu\mu_0}}=\frac{c}{n}$$
- $n$ is the _refractive index_:
$$c=\sqrt{\epsilon\mu}$$
- For non-magnetic materials:
$$c\approx\sqrt{\epsilon}$$

- The _form of a travelling wave_ ($x$-polarised), generated by a _sinusoidally oscillating_ current:
$$E_x=\Re\{E_0\exp[i(kz-\omega t)]\}$$
- The dispersion relation is:
$$\frac{\omega}{k}=\frac{1}{\sqrt{\epsilon_0\mu_0}}=c=f\lambda$$
- Applying this to the relation between components:
$$\frac{E_x}{H_y}=\frac{k}{\epsilon_0\omega}=\frac{1}{\epsilon_0c}=\sqrt{\frac{\mu_0}{\epsilon_0}}$$
- This shows that _the fields are locked in phase_
- The magnitudes are related by:
$$Z_0\equiv\sqrt{\frac{\mu_0}{\epsilon_0}}=377\,\Omega$$
	- The _impedance of free space_
	- Does not dissipate power, waves _only transmit power_

>[!quote]
>"'Impedance of free space' is my least favourite term in physics, because it's not impeding anything!"
>-Dr. Oleg Brandt, 2022

- In a linear, isotropic, homogeneous, non-conducting medium, the impedance is:
$$Z=\sqrt{\frac{\mu}{\epsilon}}Z_0$$

- The relationship between the _magnitudes of the $\bm{E}$ and $\bm{B}$ fields_:
$$E_x=cB_y$$
- When the wave is travelling in _negative $z$ direction, or $y$-polarised_, quantities such as impedance _become negative_ but with the same magnitude

- $\bm{E}$, $\bm{H}$, and the propagation direction _always form a right-handed coordinate system_

### General plane waves
- The phase of the field components is, in general (for position vector $\bm{x}$):
$$\bm{k\cdot x}-\omega t$$
- The fields themselves:
$$\displaylines{\bm{E}=\bm{E}_0\exp[i(\bm{k\cdot x}-\omega t)] \\ \bm{H}=\bm{H}_0\exp[i(\bm{k\cdot x}-\omega t)]}$$
- It can be shown that:
$$\displaylines{\nabla\cdot\bm{E}=i\bm{k\cdot E} \\ \nabla\wedge\bm{E}=i\bm{k\wedge E}}$$
- The Maxwell's equations become:
$$\displaylines{\bm{k\cdot E}_0=0 \\ \bm{k\cdot H}_0=0 \\ \bm{k\wedge E}_0=\omega\mu_0\bm{H}_0 \\ \bm{k}\wedge\bm{H}_0=-\omega\epsilon_0\bm{E}_0}$$
- First pair: _The fields are always transverse to the propagation direction_
- Second pair: $\bm{E}_0$, $\bm{H}_0$, and $\bm{k}$ _form a right-handed system_

- By combining the second pair of equations, one finds $\omega^2/k^2=c^2$, as expected
- From the second-last equation:
$$\bm{H}_0=\frac{1}{c\mu_0}\bm{\hat{k}}\wedge\bm{E}_0=\frac{1}{Z_0}\bm{\hat{k}}\wedge\bm{E}_0$$

- _Any field_ can be written as a _linear combination of plane waves_:
$$\bm{E}(\bm{x},t)=\iiiint d^3\bm{k}\,d\omega\,\bm{A}_s(\bm{k},\omega)\, \exp[i(\bm{k\cdot x-\omega t})]$$
- $\bm{A}_s$ is known as the _spectral function_
- The spectral function is the 3-dimensional [[Fourier series and transforms|Fourier transform]] of the field

### Energy flow in electromagnetic waves
- Work done on a charge is calculated by the [[Electromagnetism#The Lorentz Force and the Biot-Savart Law|Lorentz force]]
- As force from the $\bm{B}$ field $\perp \bm{v}$, the _magnetic force does no work_

- For a _continuous charge distribution_, the _rate_ at which the electric field does work is:
$$\int d^3\bm{r}\,\rho\,\bm{E}\cdot\bm{v}=\int\,d^3\bm{r}\,\bm{E}\cdot\bm{J}$$
- Hence, the _work done on charges per unit volume, per unit time_ is $\bm{E}\cdot\bm{J}$

- By _considering the volume integral of_ $\nabla\cdot(\bm{E\cdot H})$, and _Maxwell's equations_:
$$-\oint d\bm{S}\cdot(\bm{E\wedge H})=\int_V\,d^3\bm{r}\left(\pd{}{t}\left[\frac{\mu_0}{2}\bm{H\cdot H}\right]+\pd{}{t}\left[\frac{\epsilon_0}{2}\bm{E\cdot E}\right]+\bm{E\cdot J}\right)$$
- The right hand side is _the rate at which energy is flowing into the volume_

- The integrand on the left hand side is the _Poynting vector_:
$$\bm{N}=\bm{E\wedge H}$$
- The magnitude of $\bm{N}$ represents _power flow per unit area_
- Direction of $\bm{N}$ is _direction of energy flow_

### Pressure and momentum for plane waves
- Using [[Relativity|Einstein's energy-momentum relation]], and the fact that _photons are massless_:
$$E=|\bm{p}|c$$
- The _energy per unit volume_ $U$ is related to _radiation momentum density_ $\bm{g}$ by:
$$U=|\bm{g}|c$$
- By considering _radiation incident normally on a surface_, one gets:
$$\bm{g}=\frac{\bm{N}}{c^2}$$
- By considering the _rate of change of momentum_, one gets the _radiation pressure_:
$$\bm{R}=\frac{\bm{N}}{c}$$
- If the light is _reflected_, the _pressure doubles_

### Complex power in electrical components and waves
#### Electrical components
- Consider some electrical component with voltage and current:
$$\displaylines{V=V_0\cos(\omega t-\phi) \\ I=I_0\cos\omega t}$$
- By expanding the cosines, the _time-averaged power_, or _real power_ becomes:
$$P_r=\frac{1}{2}V_0I_0\cos\phi$$
	- Measures average rate of power dissipation
- There is also an extra term which oscillates as $\sin2\omega t$ and averages to 0, with _peak value_:
$$P_i=\frac{1}{2}V_0I_0\sin\phi$$
	- Measures maximum rate at which power sloshes into and out of the component
	- Also called the _reactive power_

- By replacing the cosines with _complex exponentials_, the _complex power_ is:
$$P=\frac{1}{2}IV^*$$
- $P_r$ and $P_i$ are the _real and imaginary parts_ respectively

- _Power flow_ can be represented by a vector in the complex plane
- When two components are connected, the complex power flow is _the combined sum in the complex plane_ for the two components, _regardless of how they are connected_

#### Waves
- The Poynting vector gives _instantaneous power flow per unit area_ at a given point
- If $\bm{E}$ and $\bm{H}$ are _complex_, the _time-averaged power_ is:
$$P_r=\frac{1}{2}\Re\left[\bm{E}(\bm{r})\wedge\bm{H}(\bm{r})\right]$$
- The _maximum rate at which energy sloshes_ backwards and forwards is:
$$P_i=\frac{1}{2}\Im\left[\bm{E}(\bm{r})\wedge\bm{H}^*(\bm{r})\right]$$
- For _plane waves_, since the fields are in phase, _power is always real_

### Reflection and transmission at interfaces
- Consider a plane wave with wavevector $\bm{k}$, incident on a _plane dielectric boundary_
- Refractive indices in _incident and transmitted regions_ are $n_1$ and $n_2$ respectively
- A _transmitted_ wave, $\bm{k}_t$ and _reflected_ wave $\bm{k}_r$ are produced
- The wavevectors and frequencies _should not be assumed to be identical_ at this point
- The angles $\theta$ are _between plane normal and the wavevectors_

- By using the [[#Inhomogeneous dielectrics and boundary conditions|boundary conditions]] of the electric field, which _must be true for all $x$ and $t$_:
$$\displaylines{\omega_i=\omega_r=\omega_t \\ k_i\sin\theta_i=k_r\sin\theta_r=k_t\sin\theta_t}$$
	- The waves must be _phase-matched_

- The magnitude of the wavevector _depends on the refractive index_ of the two media
- From this, the _law of reflection_, as well as _Snell's Law_ are derived:
$$\displaylines{\theta_i=\theta_r \\ \frac{\sin\theta_t}{\sin\theta_i}=\frac{n_2}{n_1}}$$
### Fresnel's relations
- There are separate relations depending on if the wave is _polarised parallel or normal to the plane of incidence_
- The _reflection and transmission coefficients_ can be derived from _using boundary conditions for the $\bm{E}$ and $\bm{H}$ fields_:
$$\displaylines{r_{||}=\frac{\tan(\theta_i-\theta_t)} {\tan(\theta_i+\theta_t)} \hspace{1.5cm} t_{||}=\frac{2\cos\theta_i}{(n_2/n_1)\cos\theta_i+\cos\theta_t} \\ r_\perp=-\frac{\sin(\theta_i-\theta_t)}{\sin(\theta_i+\theta_t)} \hspace{1.5cm} t_\perp=\frac{2\cos\theta_i}{\cos\theta_i+(n_2/n_1)\cos\theta_t}}$$


- Reflection coefficients _can take negative values_
- The _power reflection and transmission_ coefficients are _proportional_ to the amplitude coefficients _squared_ 
	- Need to scale by refractive index due to difference in wave velocity

- There is also an angle at which $r_{//}=0$, called the _Brewster's angle_ $\theta_B$:
$$\tan\theta_B=\frac{n_2}{n_1}$$
	- In other words, $\theta_i+\theta_t=\pi/2$

- If $n_1>n_2$, there is a _critical angle_ $\theta_c$ such that when $\theta_i>\theta_c$ _all incident power is reflected_
$$\sin\theta_c=\frac{n_2}{n_1}$$
- Occurs regardless of polarisation
- This is _total internal reflection_
- At this angle, $\theta_t=\pi/2$
- There is an _evanescent wave_ in the transmission medium, so _no power is transmitted_

### Waves in plasmas
- Plasmas: _conduction currents are present_, density of atoms is _low_
	- Electrons move coherently, power is _undamped_
- Approximation: the _ions are stationary_ as they are much bigger than electrons
- Approximation: $|\bm{v}|<<c$, _only force from the electric field is significant_

- Suppose a free electron is illuminated by a plane EM wave
- Substituting $\bm{E}$ from the wave into the _equation of motion_, one gets:
$$\bm{r}=\frac{e}{m_e\omega^2}\bm{E}_0\exp[i(kz-\omega t)]$$
- Amplitude _proportional to_ $1/m$ and $1/\omega^2$

- The oscillation gives rise to a _dipole moment_, causing a _polarisation_:
$$\bm{P}=N\bm{p}=-\frac{Ne^2}{m_e\omega^2}\bm{E}$$
- Hence, the _relative permittivity in plasma_ can be written as:
$$\epsilon=1-\frac{\omega_p^2}{\omega^2}$$
- The _plasma frequency_ $\omega_p$ is:
$$\omega_p=\frac{Ne^2}{\epsilon_0m_e}$$

#### Below plasma frequency
- Below $\omega_p$, _refractive index is imaginary_
- A non-propagating, _evanescent wave_ will occur in the transmitted medium:
$$\bm{E}=\bm{E}_0\exp\left[-k_0z\left|1-\frac{\omega_p^2}{\omega^2}\right|^{1/2}\right]\exp(-i\omega t)$$
- Since the refractive index is imaginary, $\bm{E}$ and $\bm{H}$ are _$\pi/2$ out of phase_
- The _time-averaged Poynting vector_ is zero
- There is no net transfer of energy, only "sloshing" of energy
	- Stored in the motion of electrons

#### Above plasma frequency
- The wave is _dispersive_
- The [[Waves#Group velocity|dispersion relation]] is:
$$\omega=\frac{ck}{\sqrt{1-\omega_p^2/\omega^2}}$$
- Phase velocity _can be larger than $c$_
- Group velocity _approaches $c$_ as $\omega$ goes to infinity
- $v_\phi v_g=c^2$

### Waves in conducting media
- Conductors: density of electrons and nuclei is _high_, _scattering is significant_
	- Power is dissipated
- Relevant relations:
$$\displaylines{\bm{D}=\epsilon\epsilon_0\bm{E} \\ \bm{B}=\mu\mu_0\bm{H} \\ \bm{J}=\sigma\bm{E} \\ \nabla\wedge\bm{H}=\sigma\bm{E}+\epsilon\epsilon_0\pd{\bm{E}}{t}}$$
- For solutions:
$$\bm{E}=\bm{E}_0\exp(-i\omega t) \hspace{1.5cm}\bm{H}=\bm{H}_0\exp(i\omega t)$$
- From the equations above, there is an _effective dielectric constant_ $\epsilon'$:
$$\nabla\wedge\bm{H}=-i\omega\epsilon'\epsilon_0\bm{E}\equiv-i\omega\left(1+\frac{i\sigma}{\omega\epsilon_0}\right)\bm{E}$$
- For metals, _the imaginary part dominates_ for typical optical frequencies
- Both the effective dielectric constant _and the refractive index_ are complex:
$$n=\sqrt{\epsilon'\mu}\approx\sqrt{\frac{i\sigma\mu}{\omega\epsilon_0}}=\pm\frac{1+i}{\sqrt{2}}\sqrt{\frac{\sigma\mu}{\omega\epsilon_0}}$$
- By substiuting a [[#General plane waves|plane wave]] solution, and defining the _skin depth_ $\delta$:
$$\displaylines{\delta\equiv\sqrt{\frac{2}{\sigma\omega\mu_0\mu}} \\ \bm{E}=\bm{E}_0\exp\left[-\frac{z}{\delta}\right]\exp\left[i\left(\frac{z}{\delta}-\omega t\right)\right]}$$
- The amplitude of the travelling wave _decays_ with penetration depth $\delta$
- The depth is typically very small

- Using the relations between $\bm{E}$ and $\bm{H}$ again, one can see that they are $\pi/4$ _out of phase_
	- $H_y$ is _behind_ $E_x$
- The Poynting vector can be _instantaneously_ positive _or negative_
- On _average_, energy travels forwards as it is dissipated

#### Skin effect of wires
- Consider a wire carrying a current $I$ oscillating at frequency $\omega$
- As power flows _along_ the wire, the _Poynting vector_ also has a large _component_ along it
- For a metal with finite conductivity, the _electric field is also along the wire_
- From also calculating $\bm{H}$, there is also a _component of the Poynting vector pointing towards the surface_

- For a wire where radius $>>\delta$, _more current flows on the outside_
	- Decays with depth $\delta$ as current goes into the wire
- As frequency increases, the current is _more confined_ and resistance _increases_

## Guided waves
- Due to the skin effect, wires _become lossy at high frequencies_
- If the dimension of the object $d$ is _comparable to or larger than_ $\lambda$, voltage and current _cannot be assumed to be constant_ along the wire
	- $\lambda>>d$: classical circuits
	- $\lambda\approx d$: transmission lines
	- $\lambda<<d$: waveguides

### Transmission lines
#### Parallel wires
- Two parallel wires along the $z-$direction
- The two currents travel in _opposite directions_, with the same magnitude $I(z)$
- There is a voltage $V(z)$ between the wires
- $V$ and $I$ are _functions of both time and position_

- The system has some inductance $L$ and capacitance $C$ _per unit length_
- By considering _infinitesimal changes_ in both $V$ and $I$ across $dz$:
$$\displaylines{\pd{V}{z}=-L\pd{I}{t} \\ \pd{I}{z}=-C\pd{V}{t}}$$
- Differentiating again, one gets the _wave equations_, with phase velocity:
$$v^2=\frac{1}{LC}$$
- Look for solutions of the form:
$$\displaylines{V=V_0\exp[i(kz-\omega t)] \\ I=I_0\exp[i(kz-\omega t)]}$$
- The _characteristic impedance_ of the transmission line is:
$$Z\equiv\frac{V}{I}=\frac{\omega L}{k}=\sqrt{\frac{L}{C}}$$

- $V$ and $I$ are _locked in phase_
- Characteristic impedance if either $V$ or $I$ travel in the opposite drection is $-Z$

- Wires and transmission lines should be thought of as _transmitting electromagnetic energy_ instead of just conducting current

- Consider a _semi-infinite transmission line_, with a voltage generator at one end
- The transmission line can be _swapped for a resistor with resistance $Z$_

- Consider two parallel wires with radius $a$, distance $2D$ apart, where $2D>>a$
- The $\bm{E}$ and $\bm{H}$ fields are _transverse and orthogonal_
- The Poynting vector $\bm{N}$ points in the _same direction as the wire_ (symmetry)
- From previous calculations, the capacitance and inductance _per unit length_ are:
$$C=\frac{\pi\epsilon_0}{\ln(2D/a)} \hspace{1.5cm} L=\frac{\mu_0}{\pi}\ln(2D/a)$$
- The wave _propagates with the speed of light_
- If the wires are embedded _in a dielectric_ with refractive index $n$:
	- Impedance decreases by factor of $n$
	- _Wavelength decreases_ by a factor of $n$

- If the wires are _incompletely embedded_ in the dielectric, the wave _is not transverse_

#### Coaxial cylinders
- Consider coaxial cylinders with a medium of permittivity $\epsilon$ in between
- Inner and outer radii of the dielectric are $a$ and $b$

- The _electric field is radial_, _magnetic field is azimuthal_
- Poynting vector is _along the cylinders_, and the wave is _transverse_
- The capacitance and inductance per unit length are:
$$C=\frac{2\pi\epsilon\epsilon_0}{\ln(b/a)} \hspace{1.5cm} L=\frac{\mu_0}{2\pi}\ln(b/a)$$
- The phase velocity is simply $c/n$

- If it is only partially filled with dielectric, the wave cannot be transverse

#### Strip transmission line
- Consider two flat strips of metal 'sandwiching' a substrate of thickness $d$
- One acts as a _ground plane_, the other is a _conducting strip with length $a$_

- Typically, $d<<a$ and _edge effects can be ignored_
- The capacitance and inductance are:
$$C=\frac{\epsilon\epsilon_0a}{d} \hspace{1.5cm} L=\frac{\mu_0d}{a}$$
- Again, the phase velocity is $c/n$

- Approximation that the wave is transverse _only holds for low frequencies_

#### Power flow in transmission lines
- The energy stored in a transmission line from $z=a$ to $z=b$ is:
$$U=\int_a^b\,dz\left(\frac{1}{2}LI^2+\frac{1}{2}CV^2\right)$$
- This is energy stored _in the fields_, with inductance and capacitance _distributed across the system_

- The rate of change of stored energy can be found to be:
$$\frac{dU}{dt}=[IV]_b-[IV]_a$$

- Considering a _load $R$ at the other end_ of a transmission line from a voltage source
- The source _carries energy away from the source towards the load_

- If $R=Z$, _all power is absorbed_ as $dU/dt=0$, and all power is absorbed
- If $R\neq Z$, _some power must be reflected_ as $dU/dt\neq0$

#### Reflection on transmission lines
- Let there be a terminal load with impedance $Z_t$, from its definition:
$$\frac{V_t}{I_t}=Z_t$$
- The forward and backwards travelling waves are:
$$\displaylines{V_i=V_1\exp[-i(kz-\omega t)]\hspace{1.5cm}I_i=I_1\exp[-i(kz-\omega t)] \\ V_r=V_2\exp[-i(-kz-\omega t)]\hspace{1.5cm}I_r=I_2\exp[-i(-kz-\omega t)]}$$
- Considering _boundary conditions_:
$$V_t=V_i+V_r \hspace{1.5cm} I_t=I_i+I_r$$
- Letting the $z=0$ at the load:
$$r\equiv\frac{V_2}{V_1}=\frac{Z_t-Z}{Z_t+Z} \hspace{1.5cm} t\equiv\frac{V_t}{V_1}=1+r=\frac{2Z_t}{Z_t+Z}$$


#### Input impedances on transmission lines
- Consider the length of the line to be $a$
- Assume the _input impedance_ to be $Z$, matched with the transmission line
- The input and reflected voltages and currents are:
$$\displaylines{V_i=V_1\exp[-i(kz-\omega t)] \hspace{1.5cm} I_i\equiv V_i/Z \\ V_r=rV_1\exp[-i(-kz-\omega t)] \hspace{1.5cm} I_r\equiv -V_r/Z}$$
- The impedance $Z_\text{in}$ is defined as:
$$Z_\text{in}=\frac{V_i+V_r}{I_i+I_r}\Bigg|_{z=-a}=\frac{e^{ika}+re^{-ika}}{e^{ika}-re^{-ika}}Z$$
- From the definition of $r$, one can show that:
$$\frac{Z_\text{in}}{Z}=\frac{Z_t\cos ka+iZ\sin ka}{Z\cos ka+iZ_t\sin ka}$$
- Hence, the _measured impedance_ depends on $a$ and $Z$

- For a _short-circuited_ line, where $Z_t\to0$, $Z_\text{in}/Z=i\tan ka$
	- Imaginary impedance means the load _cannot absorb power_
	- For $0<ka<\pi/2$, the impedance is _inductive_
	- For $\pi/2<ka<\pi$, the impedance is _capacitive_

- For an _open-circuited_ line, where $Z_t\to\infty$, $Z_\text{in}/Z=-i\cot ka$
	- Similar situation as above

- For a _quarter-wavelength line_, $ka=\pi/2$, and $Z_\text{in}=Z^2/Z_t$
	- Used to match impadances

### Waveguides
- More discussion: [[Waves#Guided waves]]

- Transmission lines support _transverse_ EM waves at high frequencies
- At very high frequencies, the _skin effect_ causes significant losses
- _Waveguides_ are often hollow tubes or _optical fibres_
	- Transmission lines are waveguides, but $V$ and $I$ still have some physical meaning
	- For waveguides, $\bm{E}$ and $\bm{H}$ need to be considered

- Consider 2 plane, $y-$polarised waves with wavevectors at angles $\pm\theta$ to the $z-$axis
$$\bm{k}_1=k(\bm{\hat{x}}\sin\theta+\bm{\hat{z}}\cos\theta) \hspace{1.5cm} \bm{k}_2=k(-\bm{\hat{x}}\sin\theta+\bm{\hat{z}}\cos\theta)$$
- It can easily be proven that the combination of the waves is:
$$E_y=2iE_0\exp[i(kz\cos\theta-\omega t)]\sin(kx\sin\theta)$$
- There are _planes of constant $x$_ where the _electric field vanishes_
- The wave _propagates in the $z-$direction while being standing in the $x-$direction_

- The _phase velocity_ is given by:
$$v_\phi=\frac{\omega}{k_\text{eff}}\equiv\frac{\omega}{k\cos\theta}$$
- Phase velocity can be _higher than $c$_
- Group velocity _must be lower than $c$_

- As there are planes where $E_y=0$, they can be _replaced with conductors_
- Hence, a waveguide can be _modelled as two parallel conducting plates_
- Placing one plate at $x=0$ and the other at $x=a$, the constraint on $k$ is:
$$k\sin\theta=\frac{m\pi}{a}$$
- Hence:
$$k_\text{eff}^2=k^2-\frac{m^2\pi^2}{a^2}$$

- It can be shown that _there is no $\bm{H}$ component perpendicular to the plates_
- There can be a component _parallel to the plates_ which goes to zero due to the skin effect

- The electric field has _modes_ with increasing number of nodes at values of $x$
- The modes are formed when _the spacing of the plates is larger than free-space $\lambda$_
- There is a _critical wavelength_, which wavelengths in the waveguide must be _under_
$$\lambda_c=2a$$
#### Rectangular waveguides
- As the field is $y-$polarised, the guide can be _completely closed_ by placing plates in _planes of constant $y$_ so there is no parallel field
- Since $H_y=0$, let any 2 plates be placed at $y=0$ and $y=b$
- As the waveguide is closed, there can be _no voltage difference_ between plates

- Notation for waveguides: $\text{TE}_{mn}$ has mode $m$ in the $x-$direction and $n$ in the $y-$direction
- _Electric field is always transverse_, while the $\bm{H}$ field has _both $x$ and $z$ components
	- $\bm{H}$ field _circulates_, giving rise to _currents in the plates_

#### The general rectangular case
- $\bm{E}$ can vary with _both $x$ and $y$
- The general solution for the $\text{TE}_{mn}$ is:
$$\displaylines{E_x=A_0k_y\cos(k_xx)\sin(k_yy)\cos(k_zz-\omega t) \\ E_y=-A_0k_x\sin(k_xx)\cos(k_yy)\cos(k_zz-\omega t) \\ E_z=0 \\ \bm{k}=\left(\frac{m\pi}{a},\frac{n\pi}{b},k_g\right)}$$
- The _waveguide equation_ is:
$$k_g^2=\frac{\omega^2}{c^2}-\frac{m^2\pi^2}{a^2}-\frac{n^2\pi^2}{b^2}\equiv k_0^2-k_c^2$$
- For propagating waves, $k_g$ _must be positive_, there is a _critical frequency_ that the wave must be above to propagate
- Below the _cutoff_, the wave will be _evanescent_