- Bonding relies heavily on the [[Symmetry in molecules]]

# Qualitative MO Diagrams
- MOs are mainly obtained from the _linear combination of atomic orbitals_ (LCAO) method, based on the [[Molecular quantum mechanics#The Variational Principle|Variational Principle]]
- However, some linear combinations may _not be symmetry allowed_ as they have [[Symmetry in molecules#Overlap integrals|zero overlap]]

- Overall, it is a better strategy to _classify orbitals according to symmetry_, creating _symmetry orbitals_, which then overlap to create MOs

## Basic properties

### Two atomic orbitals
- When two AOs interact, they form a _bonding_ MO which is _lower in energy_ then both of the AOs, airising from _in-phase overlap_
- They also form an _antibonding_ MO which is _higher in energy_ than both AOs, arising from _out of phase overlap_

- The _greater the energy separation_ between the AOs, the _smaller the shift in energy_ between the _lower AO_ and the _bonding MO_, and likewise for the higher energy orbitals

- The _greater contribution_ to the MO is _from the AO closest to it in energy_
![[AOs overlapping.png]]

### More atomic orbitals
- If there are _several AOs_ interacting, the _number of MOs is the same as number of AOs_

- _One_ MO will lie _lower in energy than the lowest energy AO_
- Likewise, _one_ MO will be _higher in energy than the highest energy AO_
- All other MOs will _lie between both extremes_

- The _greatest contribution_ to each MO is still _from the AO closest in energy_
![[Many MOs.png]]

- When _sketching_ MOs, one can _shade_ MOs to indicate _phase_, and use _size_ to indicate _contribution_

## Symmetry orbitals
- A _symmetry orbital_ (SO) is a _linear combination_ of other orbitals, such that it _transforms as a single irreducible representation_

- The method:
1. Find the _point group_ the molecule transforms as
2. Choose a _set of AOs_ to construct SOs from, typically all _from the same type of atom_
3. Find the _representation_ they collectively transform as
4. _Reduce_ the representation
5. _Construct_ orbitals that transform as each _irreducible representation_, based on _analogies with Cartesian functions_
6. _Normalise_ the orbitals

- The reducible representation commonly includes the _totally symmetric IR_, which would involve _all orbitals in phase_

- For _multi-dimensional irreducible representations_, one will need to construct a _set of symmetry orbitals_, each of which transform as one dimension of the IR

### Example: BH3
- Point group: $D_{3h}$
![[D3h character table.png]]
- Start with the _three hydrogen $1s$ orbitals_
![[BH3 hydrogen orbitals.png]]
- It can be found that these three orbitals transform as $A_1'\oplus E'$

- $A_1'$ is the _totally symmetric_ IR, so it involves _all orbitals combined in-phase_
- $E'$ is a _two-dimensional IR_, so it produces _one SO transforming like $x$_, and _one SO transforming like $y$_
- This gives the three orbitals: 
$$\displaylines{\theta_{A_1'}=\frac{1}{\sqrt{3}}(s_A+s_B+s_C) \\ \theta_{E',x}=\frac{1}{\sqrt{2}}(s_B-s_C) \\ \theta_{E',y}=\frac{1}{\sqrt{6}}(2s_A-s_B-s_C)}$$
![[BH3 hydrogen SOs.png|450]]

- Next, there are the $2s$ along with three $2p$ _boron AOs_
- The $2s$ orbital transforms as $A_1'$
- The $2p_z$ transforms as $A_2''$, while $(2p_x,2p_y)$ transforms as $E'$

- Then, _SOs with the same symmetry overlap_ to produce corresponding _bonding and anti-bonding orbitals_
- Meanwhile, as $\text{B } 2p_z$ is the only one with $A_2''$ symmetry, it produces a _non-bonding orbital_
![[BH3 SO overlap.png|600]]

- Overall, the _totally symmetric_ IR gives MOs that give _more overlap_
	- Can be justified with the [[#Hückel Approximations]]
- Then, one can make this _qualitative MO diagram_
![[BH3 MO diagram.png|500]]

### Example: BF3 and local coordinate systems
- Depending on the _symmetry_ of a molecule, instead of a coordinate system applying to all molecules, one can use _local_ coordinates for each atom

- In $\text{BF}_3$, using a universal one, the $2p_x$ and $2p_y$ AOs of different $\text{F}$ atoms _do not transform into each other_
![[BF3 universal coords.png]]

- Instead, classify them into _radial_ and _tangential_ sets:
![[BF3 local coords.png]]

- Constructing symmetry orbitals then proceeds as normal:
![[BF3 example SOs.png]]

## Projection operator
- Symmetry orbitals may not necessarily form an analogy with _Cartesian functions_
- Example: $2p$ orbitals on $\text{BF}_3$
![[BF3 SO.png|350]]

- Let the set of basis orbitals be $\{\phi_i\}$, typically being AOs
- Let the SO transforming as IR $k$ be $\theta^{(k)}$
- The SO can be found by applying the _projection operator_ $\hat{P}^{(k)}$ to a basis function:
$$\displaylines{\theta^{(k)}=\hat{P}^{(k)}\phi_i \\ \hat{P}^{(k)}=\frac{1}{n_R}\sum_R[\chi^{(k)}(R)]\hat{R}}$$
- $\hat{R}$ is a _symmetry operation_ in the group, $n_R$ is the _number of operations_, and $\chi$ is the _character_ of the operation in the representation $k$

- The sum is over _operations_, so operations _in the same class_ must be considered _separately_
- If a basis orbital is _not present in the SO_, then the operator gives _zero_

# Transition metal complexes
- _Transition metals_ can form many _coordination compounds/complexes_
- There is a _central metal atom_ surrounded by a number of _ligands_, which are often _anions_ or _small molecules_
- The ligands have a _ligating atom_ which _interacts directly_ with the metal

- Considering the _central atom_ and the _ligating atoms_, they often have a _high amount of symmetry_

- Common types:
	- _Octahedral_, often with point group $O_h$
	- _Square planar_, often with point group $D_{4h}$
	- _Tetrahedral_, often with point group $T_d$

## Octahedral complexes with $\sigma$ donors
- Consider an _octahedral complex_, where the _central metal ion_ $\text{M}^{n+}$ is surrounded by _six identical ligands_ $\text{L}$, each directing a _$\sigma-$type orbital towards the metal_
- Typically, these orbitals are occupied by _lone pairs_, such as in $\text{NH}_3$ or $\text{H}_2\text{O}$
- In this case, one can _ignore the bonding in the ligand itself_

- Inspect the _character table_ for $O_h$:
	![[Oh character table.png]]
	- There are _four_ $C_3$ axes, each generating 2 rotations, and also doubling as $S_6$ axes
	- The _principal_ $C_4$ axes are _along the ligands_, and are also $S_4$ axes
	- The $C_2$ axes _bisect_ the $\text{L-M-L}$ bond angles
	- The $\sigma_d$ planes contain 2 $\text{M-L}$ bonds and _bisect_ $\text{L-M-L}$
	- The $\sigma_h$ planes contain 4 $\text{M-L}$ bonds

- For _first-row transition metals_, the $3s$ and $3p$ orbitals are _too contracted_ to interact significantly with ligand orbitals
- Instead, the $3d$, $4s$, and $4p$ contribute to bonding
- Their irreducible representations are:
| Cartesian function       | Corresponding orbital(s)      | Irreducible representation     |
| ------------------------ | ----------------------------- | ------------------------------ |
| $(x^2+y^2+z^2)$          | $4s$                          | Totally symmetric IR, $A_{1g}$ |
| $(x,y,z)$                | $4p_x$,$4p_y$,$4p_z$          | $T_{1u}$                       |
| $(xy,yz,xz)$             | $3d_{xy}$,$3d_{yz}$,$3d_{xz}$ | $T_{2g}$                       |
| $(2z^2-x^2-y^2,x^2-y^2)$ | $3d_{z^2}$,$3d_{x^2-y^2}$     | $E_g$                               |

- Meanwhile, the six $\sigma$ orbitals reduce to:
$$A_{1g}\oplus E_g\oplus T_{1u}$$

![[Oh sigma orbitals.png|600]]

- Allowing orbitals of _the same symmetry_ to overlap:
![[Sigma octahedral complex.png]]

- There are _$6$ bonding orbitals_, which are mainly _ligand-derived_
- There are $5$ orbitals, mainly _derived from metal $3d$ orbitals_
- There are $4$ _anti-bonding orbitals_, which have the _greatest contribution from metal_ $4s$ and $4p$ orbitals

- Each ligand is _assumd to donate two electrons each_
- So for first-row transition metal ions, $1t_{2g}$ and $2e_g$ are _filled by electrons originating from the metal $3d$ orbital_

## Ligand field splitting
- The _energy splitting_ between the $1t_{2g}$ and $2e_g$ orbitals is known as the _ligand-field splitting_, denoted $\Delta_o$
	- $o$ stands for _octahedral_, as its nature depends on the shape of the complex
- It is an energy difference between a _non-bonding set_ of MOs and _an anti-bonding set_
- Hence, its magnitude _depends on strength of the bonding interaction_

- Typically, as the $3d$ and $\sigma$ orbitals become _closer in energy_, and the bond strength increases, hence the _splitting increases_
	- This occurs when the _oxidation state of the metal increases_, _contracting the $3d$
	- This can also occur when _moving across the row_ of transition metals, as the _nuclear charge_ contracts the orbitals
- It can also depend on _ligand type_ (See [[#Effect of $ pi$ interactions]])

## High- and low-spin complexes
- As the _bonding_ orbitals have to be completely filled, each orbital contains a _spin singlet_
- If a set of orbitals are _partially occupied_, then each existing _electron pair of the same spin_ will _lower the total energy_ by an [[Molecular quantum mechanics#Coulomb and exchange integrals|exchange term]] $K$

- For the _partially filled_ $1t_{2g}$ and $2e_g$ orbitals, the _spin orientations_ can depend on the _magnitude of splitting_:
![[High spin low spin.png]]

- If the splitting $\Delta_o<3K$, then electrons will be _promoted_ to $2e_g$ to _maximise the number of paired spins_, and achieve _lower energy_
- If the splitting $\Delta_o>3K$, then electrons will _stay at $1t_{2g}$_ to minimise energy
- For all numbers of $d$ electrons:
![[High spin low spin energies.png|600]]

- The magnitude of splitting can be _inferred_ from _electronic spectroscopy_
- Overall, _promoting_ and electron will _alter the energy of all orbitals_ due to changes in repulsion, so more _calculations_ are needed other than the readings themselves

### Magnetic properties
- The overall _magnetic properties_ can easily be _interpreted_ to give whether a complex is _high spin_ or _low spin_
- Any _unpaired electrons_ will lead to the complex being [[Electromagnetism#Magnetic permeability in materials|paramagnetic]]
- The _magnetic susceptibility_ is _proportional_ to the _effective magnetic moment_:
$$\mu_\text{eff}=2\sqrt{S(S+1)}=\sqrt{n(n+2)}$$
- This magnetic moment is measured in terms of _Bohr magnetons_:
$$\mu_B=\frac{e\hbar}{2m_e}$$
- $S$ is the _total spin_, and $n$ is the _number of unpaired electrons_

- A _high spin_ complex will give a _higher degree of paramagnetism_


### Thermodynamic properties
- When plotting _hydration_ and _lattice_ enthalpies, as a function of _number of $d$ electrons_, one will notice a _double dip_:
![[Hydration and lattice enthalpies.png|600]]
- These are interpreted as the _enthalpy of formation of complexes_

- As the _atomic number_ of the metal _increases_, the $3d$ orbital _contracts_, strengthening the bond and _lowering the energy of the bonding electrons_ in the complex
- Let the _energy decrease_ of the bonding electrons be $-E_L$

- However, assuming a _high spin_ complex, increasing the number of $d$ electrons also _increases the number $2e_{g}$ electrons_ $n_{e_\sigma}$
	- This does _not_ occur for _all numbers of_ $d$ electrons 
- Hence, the _overall energy change_ is:
$$-E_L+n_{e_\sigma}E_\sigma$$
- Therefore, the _form_ of the overall hydration/lattice enthalpy is:
![[Hydration enthalpy origin.png]]
- This gives the _double dip_

## Effect of $\pi$ interactions
- Many ligands also have _$\pi$ orbitals_ that may be suitable to _overlap with the metal orbitals_
- Example: For atomic _anions_, there will be $p$ _orbitals perpendicular to the $\text{M}-\text{L}$ axis_
![[Ligand p orbitals.png|200]]

- If there is a _pair_ of $p$ orbitals _perpendicular to the $\text{M}-\text{L}$ axis_, then the 12 orbitals have the _representation_:
$$T_{1g}\oplus T_{2g}\oplus T_{1u}\oplus T_{2u}$$
- In general, there are two types:
	- $\pi$ _donors_, where the $\pi$ orbitals are at a _similar energy_ to the $\sigma$ orbitals
	- $\pi$ _acceptors_, where the $\pi$ orbitals are at a _higher energy_ than the $\sigma$ orbitals

### Donors
- $\pi$ donor ligands often contain _bonding_ $\pi$ orbitals that can overlap with the metal $3d$
	- Example: $\text{Cl}^-$ _anion_
- By considering the effect of _adding_ the $T_{2g}$ orbitals at a _similar energy level_ to the _$\sigma$ orbitals_:
![[Sigma and pi donor.png]]

- Overall, the _lower_ $T_{2g}$ orbitals cause a _weak overlap_
- The $1t_{2g}$ orbitals are _bonding_, and are often _filled_ (depending on the ligand)
- This will cause a _decrease in ligand field splitting_

### Acceptors
- $\pi$ acceptor ligands often contain _antibonding_ $\pi^*$ orbitals that can overlap with the metal $3d$
	- Example: $\text{CO}$ $\pi^*$
- By considering the effect of _adding_ the $T_{2g}$ orbitals at a _higher energy level_ than the _$\sigma$ and the $3d$ orbitals_:
![[Sigma and pi acceptor.png]]

- Overall, the higher energy of the $T_{2g}$ orbitals cause a _weak overlap_
- The _weakly bonding_ $1t_{2g}$ orbital is _partially occupied_ by _metal electrons_
- This causes an _increase in ligand field splitting_

### Spectrochemical series 
- For a _given metal and oxidation state_, changing the _ligand_ changes the magnitude of $\Delta_o$

- The _magnitude_ of $\Delta_o$ _increases_ from left to right along the _spectrochemical series_:
![[Spectrochemical series.png]]

- Generally, a _strong_ $\sigma$ _interaction_ will lead to a large value of $\Delta_o$
	- This means a _higher energy $\sigma$ donor orbital_ to make a _better match_
	- Hence, as _ligating atom_ changes from $\text{N}$ to $\text{O}$ to $\text{C}$, $\Delta_o$ increases

### The 18-electron rule
- For an octahedral complex with $\pi$ _acceptors_, there are _$9$ bonding MOs_
- Hence, when there are $18$ _valence electrons_, this _maximises degree of bonding_

- This leads to an _18-electron "rule"_, where _stable octahedral complexes often have 18 valence electrons_ 
	- This is _not true if there are no $\pi$ acceptors_

## Tetrahedral complexes
- Tetrahedral complexes have the point group $T_d$:
![[Td character table.png]]

- The _metal AOs_ are classified according to:
| Cartesian function       | Corresponding orbital(s)      | Irreducible representation     |
| ------------------------ | ----------------------------- | ------------------------------ |
| $(x^2+y^2+z^2)$          | $4s$                          | Totally symmetric IR, $A_1$ |
| $(x,y,z)$                | $4p_x$,$4p_y$,$4p_z$          | $T_2$                       |
| $(xy,yz,xz)$             | $3d_{xy}$,$3d_{yz}$,$3d_{xz}$ | $T_2$                       |
| $(2z^2-x^2-y^2,x^2-y^2)$ | $3d_{z^2}$,$3d_{x^2-y^2}$     | $E$                               |

- Four $\sigma$ orbitals then transform according to:
$$A_1\oplus T_2$$
- Now, it is the _metal_ $E$ orbitals that are _non-bonding_

- Allowing the relevant orbitals to overlap, and comparing the _metal-based orbitals_ for different complexes:
![[Tetrahedral complex.png]]

- There are _$4$ bonding MOs_, $1a_1$ and $1t_2$

- In this case, the splitting $\Delta_t$ is often _smaller_ than $\Delta_o$ for similar ligands, typically:
$$\Delta_t\approx0.44\Delta_o$$
- In an _octahedral_ complex, the $3d$ orbitals point _directly_ at the ligands
- In a _tetrahedral_ complex, the overlap is _less effective_

- It also means that tetrahedral complexes are typically _high-spin_

## Square planar complexes
- Square planar complexes have the point group $D_{4h}$:
![[D4h character table.png]]

- The _metal AOs_ have symmetries:
| Cartesian function | Corresponding orbital(s) | Irreducible representation     |
| ------------------ | ------------------------ | ------------------------------ |
| $(x^2+y^2+z^2)$    | $4s$                     | Totally symmetric IR, $A_{1g}$ |
| $(x,y)$            | $4p_x$,$4p_y$            | $E_u$                          |
| $(z)$              | $4p_z$                   | $A_{2u}$                       |
| $(xz,yz)$          | $3d_{xz}$,$3d_{yz}$      | $E_g$                          |
| $(xy)$             | $3d_{xy}$                | $B_{2g}$                       |
| $(x^2-y^2)$        | $3d_{x^2-y^2}$           | $B_{1g}$                       |
| $(2z^2-x^2-y^2)$   | $3d_{z^2}$               | $A_{1g}$                               |

- Meanwhile, the four $\sigma$ orbitals transform as:
$$A_{1g}\oplus B_{1g}\oplus E_u$$

- Hence, the overlap creates:
![[Square planar complex.png]]

- Calculations show that the $b_{1g}$ orbitals give _stronger overlap_
- There are _$4$ bonding MOs_, $1a_{1g}$, $1b_{1g}$, and $1e_u$

- The $1e_g$ and $1b_{2g}$ orbitals are _non-bonding_ and _degenerate_
	- If there are $\pi$ interactions, they can _separate_, with $1b_{2g}$ moving _higher_

# Linear molecules
- Requires [[Symmetry in molecules#Infinite groups|infinite groups]]
- Consider _diatomics_

## Symmetry orbitals
- Construct $\sigma$ and $\pi$ _symmetry orbitals_ from $s$ and $p$ AOs
- For many atoms, _$s-p$ mixing_ will also need to be considered

- Homonuclear diatomics belong to the $D_{\infty h}$ point group
- Heteronuclear diatomics belong to the $C_{\infty v}$ point group

### Simplest case: hydrogen gas
- The simplest homonuclear diatomic is $\text{H}_2$, with _two $1s$ orbitals_, $1s_A$ and $1s_B$
- By inspection, the symmetry orbitals are the _sum and difference_ of the orbitals:
![[H2 SOs.png]]

- Since they are of _different symmetries_, there is _no overlap_, and they form the _molecular orbitals_

### Second period homonuclear diatomics
- In the second period, the $1s$ orbitals are _too contracted_ to interact
- The $2s$ orbitals behave _similarly to $1s$ orbitals_ in the first period
- Meanwhile, the $2p_z$ orbitals also _form degenerate $\sigma$ SOs_:
![[2pz sigma.png]]

- As for the $2p_x$ and $2p_y$ orbitals, consider $(x_A,y_A,x_B,y_B)$, which transforms as $\Pi_u\oplus\Pi_g$:
![[2px 2py pi.png]]

- From this, one can construct the MO diagram by overlapping appropriate SOs:
	- The $2p$ orbitals are _higher energy_ due to _shielding_, but all are originally _degenerate_
![[Homonuclear diatomic MOs.png]]

- By selecting overlap due to symmetry, one can account for the effects of $s-p$ _mixing_:
	![[sp mixing.png]]
	- The extent depends on the _energy separation_
	- For $\text{O}$ and $\text{F}$, $2\sigma_g^+$ is _below_ $1\pi_u$
- The mixing makes $1\sigma_g^+$ _more bonding_, while $2\sigma_g^+$ becomes _less bonding_
- Meanwhile, $1\sigma_u^+$ becomes _less antibonding_

### Heteronuclear diatomics
- For heteronuclear diatomics, the point group is $C_{\infty v}$
- The $2s$ and $2p_z$ MOs transform as $\Sigma^+$, while $2p_x$ and $2p_y$ transform as $\Pi$
- Hence, _more orbitals match symmetry and overlap_:
![[Heteronuclear MO diagram.png]]

- Hence, $2\sigma^+$ and $3\sigma^+$ are now _further apart_

## Molecular term symbols
- Analagous to [[Molecular quantum mechanics#Energy levels and term symbols|atomic term symbols]]
- For each _configuration_, it is split into _terms_ based on $L$ and $S$, which are then split into _levels_ based on $J$

- _Molecular_ term symbols also specify total $L$, $S$, and $J$, as well as adding _symmetry labels_

- The _lowest energy_ level still follows [[Molecular quantum mechanics#Hund's rules|Hund's rules]]

### Angular momentum
- For spin, due to the [[Molecular quantum mechanics#Pauli Principle|Pauli Principle]], a _filled shell_ has _zero spin_
- Otherwise, spins in _separate orbitals_ will _add_

- For _orbital angular momentum_ in _diatomics_, only the _component along the inter-nuclear axis_ is defined
	- There is now a "_preferred direction_"
- The total component is obtained from _adding contributions from separate orbitals_
- 1D $\Sigma$ IRs have $\lambda=0$,while 2D $\Pi$ IRs have $\lambda=\pm1$
- The _total orbital angular momentum component_ is denoted $\Lambda$:
| $\Lambda$ | $0$      | $1$   | $2$ |
| --------- | -------- | ----- | --- |
| Letter    | $\Sigma$ | $\Pi$ | $\Delta$    |

### Symmetry labels
- The _overall_ symmetry of a level is found by _combining_ the symmetry of _orbitals occupied by individual electrons_, via a _direct product_
- When taking _inversion symmetry_ into account:
$$g\otimes g=u\otimes u=g \hspace{1cm} g\otimes u=u\otimes g=u$$
- When _only $\sigma$ orbitals_ are occupied, the $\pm$ labels for _reflection symmetry_ follow:
$$+\otimes +=-\otimes -=+ \hspace{1cm} +\otimes -=-\otimes +=-$$

### Term symbol without degenerate orbitals
- Overall, the term symbol is denoted:
$$^{2S+1}\Lambda_{g/u}^\pm$$
- The left _superscript_ is the _spin multiplicity_
- The right _subscript_ is the _inversion symmetry_, for _homonuclear diatomics_
- The right _superscript_ is the _reflection symmetry_, only for $\Sigma$ levels
	- For other levels, _interchanging_ electrons will _interchange wave-functions_, giving no meaning to a $\pm$ label

- For _heteronuclear diatomics_, the term symbol _only has multiplicity and $\Lambda$_

- From symmetry arguments above, if a set of _degenerate orbitals_ are _completely filled_, it contributes:
$$^1\Sigma_g^+$$
- Therefore, one _only needs to consider partially filled orbitals_

- From Hund's rules, the _lowest energy_ level has the _maximum spin multiplicity_

### Partially filled degenerate orbitals
- For partially filled degenerate orbitals, there are _multiple ways to fill them_
- They form _components_ of _triplet_ or _singlet_ states

- Example: _Oxygen_ $\text{O}_2$ has a $(1\pi_g)^2$ configuration, which gives possible terms:
$$1\Delta_g, ^1\Sigma_g,^3\Sigma_g$$
- Due to Hund's rules, the _latter has the lowest energy_

- However, the latter two have _reflection symmetry_, which must be determined by _considering the spatial wave function_
- The respective spatial wave functions are:
$$\displaylines{^1\Sigma_g\to\Psi_+=\frac{1}{\sqrt{2}}\left[\psi_+(1)\psi_-(2)+\psi_+(1)\psi_-(2)\right] \\ ^3\Sigma_g\to\Psi-=\frac{1}{\sqrt{2}}\left[\psi_+(1)\psi_-(2)-\psi_+(1)\psi_-(2)\right]}$$
- The $\pm$ signs indicate $\pm1$ _angular momentum along the internuclear axis_
- Hence, the wave functions transform as $\exp(\pm i\phi)$, leading to:
$$\displaylines{\Psi_+\propto\cos(\phi_1-\phi_2) \\ \Psi_-\propto\sin(\phi_1-\phi_2)}$$
- Reflection symmetry _inverts the signs of angles_, hence the terms available are:
$$1\Delta_g, ^1\Sigma_g^+,^3\Sigma_g^-$$
- It is _not the general case_ that singlet and triplet terms have _different signs_
	- Example: $(1\sigma^+_g)^1(2\sigma^+_u)^1$ has levels $^1\Sigma_u^+$ and $^3\Sigma_u^+$

### Direct products for symmetry labels
- If there are _non-equivalent electrons_, then their _electronic wave function_ is simply a _product_
- Hence, the term symboil, _excluding multiplicity_, can be given by _direct products_

- This gives another reasoning for why _fully filled orbitals_ contribute $^1\Sigma_g^+$, as it is the _totally symmetric IR_
- Example: _Excited state_ of $\text{N}_2$
	$$\dots(3\sigma_g^+)^1(1\pi_g)^1\to \Sigma_g^+\otimes \Pi_g=\Pi_g$$
	- This then gives rise to _separate triplet and singlet terms_

### Notation for electronic states
- The _ground state_ is sometimes given the additional label $X$
- Example: ground state of $\text{N}_2$ has term $\text{X}\,^1\Sigma_g^+$
- For excited states with the _same multiplicity_, they are labelled $\text{A},\text{B},\dots$
- For excited states with _different multiplicity_, they are labelled $a,b,\dots$

# Hückel Approximations
- Approximations to calculate _energies of molecular orbitals_, applicable for _simple molecules_

## LCAO method and secular equations
- The simplest method for _computing molecular orbitals_ is the [[Molecular quantum mechanics#Linear combination of atomic orbitals for diatomics|Linear Combination of Atomic Orbitals]] method, based on the Variational Principle
- Let the _basis of atomic orbitals_ be $\{\phi_i\}$, any _molecular orbital_ is then written as:
$$\psi=\sum_i c_i\phi_i$$
- Then, using the Variational Principle and _minimising energy_:
$$E\geq\frac{\braket{\psi|\hat{\Ham}|\psi}}{\braket{\psi|\psi}} \hspace{1cm} \pd{E}{c_k}=0$$
- Introducing the notation for _matrix elements_ for the Hamiltonian and identity:
$$\Ham_{ij}=\braket{\phi_i|\hat{\Ham}|\phi_j} \hspace{1cm} S_{ij}=\braket{\phi_i|\phi_j}$$
- Then, one obtains the _secular equations_:
$$\sum_j \left(\Ham_{ij}-ES_{ij}\right)c_j=0$$
- This can be put into _matrix form_:
$$\left[\begin{pmatrix}\Ham_{11} & \Ham_{12} & \dots & \Ham_{1N} \\ \Ham_{21} & \Ham_{22} & \dots & \Ham_{2N} \\ \vdots & \vdots & \ddots & \vdots \\ \Ham_{N1} & \Ham_{N2} & \dots & \Ham_{NN} \end{pmatrix} -E \begin{pmatrix}S_{11} & S_{12} & \dots & S_{1N} \\ S_{21} & S_{22} & \dots & S_{2N} \\ \vdots & \vdots & \ddots & \vdots \\ S_{N1} & S_{N2} & \dots & S_{NN} \end{pmatrix}\right] \begin{pmatrix} c_1 \\ c_2 \\ \vdots  \\ c_N\end{pmatrix} = \begin{pmatrix} 0 \\ 0 \\ \vdots  \\ 0\end{pmatrix}$$

## The approximations
- The Hückel approximations consist of several steps
- Assume the _basis functions are normalised_, and that _overlap between wavefunctions of different atoms is zero_: $$S_{ij}=\delta_{ij}$$	- Accounting for the overlap integral usually results in _minor shifts in energies_

- Next, let the _matrix elements_ of the Hamiltonian be _defined as_:
$$\displaylines{\Ham_{ii}=\alpha_i \\ \Ham_{ij}=\beta_{ij} \text{ for }i\neq j}$$
- $\alpha$ can be interpreted as the _energy of the atomic orbital_ $\phi_i$
- Meanwhile, $\beta$ can be interpreted as _energy resulting from overlap between_ $\phi_i$ and $\phi_j$
- They are both _negative_
- Since the Hamiltonian is _Hermitian_, and $\beta$ is real: $$\beta_{ij}=\beta_{ji}$$
- Finally, apply the _tight-binding approximation_, where $\beta_{ij}$ is _only non-zero if $\phi_i$ and $\phi_j$ are on adjacent atoms_
- The secular equations then become: $$\begin{pmatrix}\alpha_{11}-E & \beta_{12} & \dots & \beta_{1N} \\ \beta_{21} & \alpha_{22}-E & \dots & \beta_{2N} \\ \vdots & \vdots & \ddots & \vdots \\ \beta_{N1} & \beta_{N2} & \dots & \alpha_{NN}-E \end{pmatrix}\begin{pmatrix} c_1 \\ c_2 \\ \vdots  \\ c_N\end{pmatrix} = \begin{pmatrix} 0 \\ 0 \\ \vdots  \\ 0\end{pmatrix}$$
- Solving this for $E$, then $\{c_i\}$ gives the _energies of all molecular orbitals_, as well as their _coefficients for atomic orbitals_

- Ocassionally, _further approximations_ are needed
- Example: in _carboxylate_, $\alpha_\text{O}=\alpha_\text{C}+\beta$
	- Crude approximation, but takes into account that _oxygen orbitals are lower in energy_

## Properties of results
- By setting the _overlap matrix equal to the identity_, a result is that _the sum of energies is invariant_
	- The problem becomes equivalent to _expressing $\hat{\Ham}$ in its eigenbasis_

- For some $\pi$ systems, it can be found that by _letting electrons delocalise across many atoms_, the _overall energy is lowered_
- The _delocalisation energy_ is the _difference_ between _total $\pi$ electron energy_, and the _localised electron energy_ obtained from a _model with separated $\pi$ bonds_
- For delocalisation to be _favourable_, the energy must be _negative_
	- $k\beta$, where $k>0$
- This is especially relevant for [[#Rings|cyclic molecules]] and _aromaticity_

## Exploiting symmetry

### Example: Cyclobutadiene

# Rings

# Chains

