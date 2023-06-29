- The [[Free Electron Model]] is able to explain observations such as _electrical and thermal conductivity_, and _heat capacity_
- However, there are large discrepancies in the [[Free Electron Model#Hall Effect|Hall coefficient]] of metals

- The _Nearly Free Electron Model_ takes the _periodic potential_ of nuclei and ions into account
- In order to account for [[Crystal structure and diffraction|lattice periodicity]], one needs to use the _reduced zone scheme_
- The _dispersion curve_ of electrons must be _"folded"_ into the _1st Brillouin zone_
![[Electron dispersion reduced zone.png]]

- One can later show that the periodic potential _lifts the degeneracy at the zone boundary_

- The weak periodic potential can be represented as a _Fourier series_ using [[Crystal structure and diffraction#The reciprocal lattice|reciprocal lattice vectors]]
- The _form_ of the electron wave function can be established using Bloch's theorem
- The subsequent _electron basis states_ can be written as a _Fourier series_

- Then use the basis states to solve the _Schrodinger equation_ using the matrix approach

- If the periodic potential is _weak_, then the electron can be represented using only _a few basis states_
	- A _completely free_ electron is simply a _plane wave_
- Ignore _electron-electron interactions_

# The electron wave function

## Bloch's Theorem
- Let there be a _periodic lattice in 1D_
![[1D potential.png]]
- The potential can then be written as a _Fourier series_:
$$V(x)=\sum_{p=-\infty}^\infty V_p\cos(pG_1x) \hspace{1cm} G_1=\frac{2\pi}{a}$$
- As the lattice has some _translational symmetry_, the _electron probability density_ $|\Psi|^2$ must _reflect the symmetry of the lattice_

- Therefore, _between sites_, the probability density must only change by a _phase factor_:
$$\Psi(x+a)=\Psi(x)\exp(i\delta)$$
- The phase difference can then be written as $ka$, where $-\pi/a<k<\pi/a$:
$$\Psi(x+a)=\Psi(x)\exp(ika)$$
- Given this form, the function can be _re-written_ as:
$$\Psi(x)=u_k(x)\exp(ikx)$$

- In general, _Bloch's theorem_ states that _solutions of the Schrodinger equation for a periodic potential_ must have the form:
$$\Psi_\bm{k}(\bm{r})=u_\bm{k}(\bm{r})\exp(i\bm{k}\cdot\bm{r})$$
- $u_k(\bm{r})$ must _reflect the periodicity of the potential_:
$$\displaylines{u_\bm{k}(\bm{r}+\bm{R})=u_\bm{k}(\bm{r}) \\ u_k(x)=\sum_{n=-\infty}^\infty C_{k,n}\frac{1}{\sqrt{A}}\exp(inG_1x)}$$
- The _overall wave-function_ is then:
$$\Psi_k(x)=\sum_{n=-\infty}^\infty C_{k,n}\frac{1}{\sqrt{A}}\exp[i(k+nG_1)x]$$

- Equivalently:
$$\displaylines{\ket{\Psi_k}=\sum_{n=-\infty}^\infty C_{k,n}\ket{\phi_{k,n}}\\\braket{x|\phi_{k,n}}=\frac{1}{\sqrt{A}}\exp[i(k+nG_1)x]}$$
- $\ket{\phi_{k,n}}$ are the _electron basis states_ for wave-vector $k$
	- The $1/\sqrt{A}$ is a _normalising factor_
- In $k-$space, they are _seprarated by_ $G_1$ along the $k-$axis starting from $k$
- The states are represented by _plane waves_, hence they lie on the _free electron dispersion curve_:
![[Electron basis states.png]]
- The _overall wave-function_ $\Psi_k$ is given by a _weighted sum_ of the basis states
 
- If the potential is _weak_, only basis states $\ket{\phi_{k,n}}$ with _energy close to that of the central basis state_ $\ket{\phi_{k,0}}$ will have _significant contributions_ to the overall wavefunction

## Matrix elements of the Hamiltonian
- The _Hamiltonian_ of the crystal in the position basis:
$$\hat{\Ham}\xrightarrow{x\text{ basis}}-\frac{\hbar^2}{2m}\frac{d^2}{dx^2}+\sum_{p=-\infty}^\infty \cos(pG_1x)$$
- The _matrix elements_ of the Hamiltonian can then be calculated:
$$\braket{\phi_{k,m}|\hat{\Ham}|\phi_{k,n}}=\frac{\hbar^2}{2m_e}(k+mG_1)^2\delta_{m,n}+\sum_p\frac{V_p}{2}(\delta_{n,m+p}+\delta_{n,m-p})$$

## Two-state approximation
- For a weak potential, let the _electron wave function_ be a _linear combination_ of two basis states:
$$\ket{\Psi_k}=C_{k,0}\ket{\phi_{k,0}}+C_{k,-1}\ket{\phi_{k,-1}}$$
- $\ket{\phi_{k,1}}$ and $\ket{\phi_{k,-1}}$ are _both valid choices_

- For _limiting behaviour_, one can guess the behaviour of the function at small and large $k$:
![[NFE small and large k.png]]

### Small k
- For a _small value_ of $k$, near the centre, there is a _significant energy difference_ between the two states
- Hence, the _additional basis state_ has _little contribution_ to the overall wavefunciton:
$$\ket{\Psi_k}\approx\ket{\phi_{k,0}}$$
- The energy is _close to the free particle energy_

### Large k
- For a _large value_ of $k$, near the _zone boundary_, the two states have _comparable energy_
- They both have a _significant contribution_ to $\ket{\Psi_k}$
- At $k=G_1/2$, they have _equal contributions_

- When the two states _contribute equally_, they superpose to form _standing waves_:
$$\displaylines{\Psi_+(x)=\frac{1}{2}[\phi_{G_1/2}(x)+\phi_{-G_1/2}(x)]\propto\cos\left(\frac{\pi x}{a}\right)\\ \Psi_-(x)=\frac{1}{2}[\phi_{G_1/2}(x)-\phi_{-G_1/2}(x)]\propto\sin\left(\frac{\pi x}{a}\right)}$$
- The two wave-functions have _different energies_, as they have _different values_ at points of _high and low potential_
![[Lifting degeneracy.png]]
- Hence, the _degeneracy of the two states is lifted_

## Solutions to the Schrodinger equation
- Only using two states as a basis, find the _energies as a function of $k$_ by finding the _eigenvalues of the Hamiltonian_:
$$\hat{\Ham}\ket{\Psi_k}=E_k\ket{\Psi_k}$$
- To do this, one needs to find the [[#Matrix elements of the Hamiltonian|matrix elements]]:
$$\displaylines{H_{00}=E_{k,0}=\frac{\hbar^2}{2m_e}k^2 \\ H_{0\bar{1}}= H_{\bar{1}0}=\frac{V_1}{2} \\ H_{\bar{1}\bar{1}}=E_{k,-1}=\frac{\hbar^2}{2m_e}(k-G_1)^2}$$

- This gives energies as a function of $k$:
$$E_k=\frac{1}{2}\left(E_{k,-1}+E_{k,0}\right)\pm\sqrt{\frac{1}{4}(E_{k,-1}-E_{k,0})^2+\left(\frac{V_1}{2}\right)^2}$$
- The wavefunction is a _superposition of two states_

![[Two state energies.png]]
- The interaction of the basis states with the potential leads to an _avoided crossing_ of the two original dispersion curves
- This leads to the formation of _bands_, with a _gap_ of $V_1$ at $k=\pm G_1/2$

## Band structure
- With a more _general_ potential:
$$V(x)=\sum_n V_n\cos(nG_1x)$$
- This will link states at _higher energies_
- There are _gaps_ of $V_n$ at $nG_1/2$
	- Consider the interaction between $\Psi_+$ and $\Psi_-$ for the $n$th Fourier component

- This leads to a _band structure_, where electron states can only lie in _energy ranges_, or _bands_
- The _Fermi energy_ $\varepsilon_F$ determines how _far up_ the band structure is filled
![[Electron bands.png]]
- The _level_ at which the bands are filled determines the [[#Electrical conductivity]] of the material

## Electron motion and effective mass
- Model the electrons using a _semiclassical approximation_
- They are considered as _wavepackets_ with _group velocity_:
$$\bm{v}(\bm{k})=\frac{d\omega}{d\bm{k}}=\frac{1}{\hbar}\frac{dE_k}{d\bar{k}}$$
- This is a _non-vanishing velocity_ (unless $E_k$ is stationary), and is _purely due to the lattice potential itself_, determining the _position of the electron_
- The quantity $\hbar\bm{k}$ is known as _crystal momentum_
	- The Hamiltonian and momentum operators _do not have simultaneous eigenstates_
- If any _external force_ is applied, this would _change the momentum of the electron itself_

- Define the _effective mass_ $m^*$ such that:
$$m^*\frac{dv}{dt}=\hbar\frac{dk}{dt}$$
- Substitute the formula for group velocity:
$$m^*\frac{d}{dt}\left(\frac{d\omega}{dk}\right)=\frac{m^*}{\hbar}\frac{d^2\varepsilon}{dk^2}\frac{dk}{dt}$$
- From this, the formula for effective mass is:
$$m^*=\hbar^2\left(\frac{d^2\varepsilon}{dk^2}\right)^{-1}$$
- This is analagous to:
$$\varepsilon=\frac{\hbar^2k^2}{2m^*}\Longrightarrow m^*=\hbar^2\left(\frac{d^2\varepsilon}{dk^2}\right)^{-1}$$
- Therefore, depending on the _band structure_ or the _band_ itself, $m^*$ is _dependent on $k$_
- Depending on the position of $\varepsilon_F$, _more than one effective mass_ can be present at the Fermi level

- The _time evolution_ of the electron wave-vector is dependent on _external forces_:
$$\hbar\frac{d\bm{k}}{dt}=-e\left[\bm{E}+\bm{v}\wedge\bm{B}\right]$$

## Electrical conductivity
- Similar to the [[Free Electron Model#Electrical conductivity|free electron model]], an _applied electric field_ will _shift_ the Fermi sphere and cause a _drift velocity_, allowing the material to _conduct_ electricity
	- There is a _non-zero average crystal momentum_ for the electrons
- However for the sphere to move, one requires _nearby empty $k-$states_

- In $k-$space, one can map out the _bands and band gaps_
- If a band is _completely filled_, the Fermi sphere _cannot move_ without a _large jump in electron energy_, and the material is an _insulator_
- If a band is _partially filled_, the Fermi sphere is easily _displaced_, and the material is a _conductor_
![[Conductor vs insulator.png]]

### 1 dimensional model
- In _1 dimension_, the _separation of $k-$states_ is $2\pi/L$
- The _size_ of the first Brillouin zone is $2\pi/a$, hence the _number of states_ is $L/a=n$
- As the electrons have _two spin states_, each _band_ can accommodate $2n$ electrons

- If there is an _odd number of electrons per atom_, the material is an _insulator_
	- The topmost band is _full_
- if there is an _even number of electrons per atom_, the material is a _conductor_
	- The topmost band is _half full_
- This _does not match observations_ (e.g. Group 2 metals)
![[1D model band filling.png]]

### 2D model for a divalent metal
- In the _free electron model_, the energy is a _paraboloid_ in $k-$space
- As states are filled _up to the Fermi energy_, this forms a _circular contour_:
![[Free electron Fermi contour.png|400]]

- With a _weak potential_, there is a _small energy gap at the zone boundary_
- There is an _energy overlap_ between the 1st and 2nd bands
- At the _band gap_, energies _vary with position_, hence the _Fermi energy contour crosses_ into the 2nd Brillouin zone
- At the gap, there tends to _bulges_ in the Fermi surface at the band gap
- Hence, as _both bands_ are _partially filled_ at the Fermi level, the material is a _conductor_:
![[Divalent metal weak potential.png]]

- With a _strong potential_, the energy gap is _much larger_
- There is _no overlap in energies_
- The Fermi surface follows the _shape of the 1st Brillouin zone_
- As only the first band is _full_, the material is an _insulator_
![[Divalent metal insulator.png]]
- Variation in the Fermi surface:
![[Divalent Fermi surfaces.png]]

### Conduction
- With _no electric field_, the Fermi surface is _symmetric_
- There are _equal numbers_ of electrons moving _forwards and backwards_

- With an electric field:
$$-e\bm{E}=\hbar\frac{d\bm{k}}{dt}$$
- The electrons move towards _higher $k-$states_
- Phonons and defects will _scatter_ the electrons into _empty states_
![[Nearly free conduction.png]]
- There is a _net group velocity_ opposite the field

### Bloch oscillations
- If the electric field is _strong_, and the scattering processes are _weak_, the occupied states will _move continuously through $k-$space_
- They can _cross into the 2nd Brillouin zone_
- The _observed group velocity_ is _reversed_
![[Bloch oscillations.png]]
- The _backfolding_ of zones means the process is _continuous_
- Overall, the _electron group velocity oscillates_, and an _AC current_ is generated from a _DC electric field_
- This is known as the _Bloch oscillation_

- For a _band structure_:
$$\varepsilon=-V_0\cos(ka)$$
- This gives rise to Bloch oscillations:
$$\displaylines{\hbar\frac{dk}{dt}=-eE \\ v(k)=\frac{V_0a}{\hbar}\sin(ka)=-\frac{V_0a}{\hbar}\sin\left(\frac{eEa}{\hbar}t\right)}$$
- Due to the requirement of _very little scattering_, this typically only happens for _pure metals at very low temperatures_

## Holes
- Consider a band that has _few empty states near the top_
- These are at the region _close to the zone boundary_
- It is easier to _offset_ the reduced zone scheme
![[Offset reduced zone scheme.png]]

- The _lower_, almost full band is the _valence band_
- The _upper_, almost empty band is the _conduction band_

- Consider the _promotion_ of an electron from the valence band _to the conduction band_:
![[Electron promotion 1.png]]

- It is convenient to model this as a __completely filled valence band__, along with a particle known as a __"hole" in a separate hole band__, and the _electron in the conduction band_
![[Hole band.png]]

- Consider that in a _completely filled band_:
$$\sum_\text{band}\bm{k}=0$$
- The hole model must still _conserve energy and momentum_
	- Measure energy from the _top of the valence band_, such that the electrons in the _valence band_ have _negative energy_, and the _hole band has positive energy_
- Therefore, define the _energy and momentum of holes_:
$$\varepsilon_h=-\varepsilon_e \hspace{1cm} k_h=-k_e$$
- Ways of looking at momentum:
	- A _completely filled valence band_ with zero momentum, plus the _hole in the hole band_ with momentum $\hbar k_h=-\hbar k_e$
	- A valence band with _one electron missing_, with net momentum due to the electron on the _other side_, with momentum $-\hbar k_e$

- As the _electron effective mass_ at the top of the valence band is _negative_, it is much easier to imagine a _hole_ moving in an _opposite direction to the electron_ with a _positive effective mass_: $$m_h^*=-m_e^*>0$$
- The _conventions_ for a hole are:
$$q=+|e| \hspace{1cm} m_h>0 \hspace{1cm} E=+\frac{\hbar^2k_h^2}{2m_h}$$
### Dynamics of a hole
- When a field is applied, the _empty state in the valence band moves with the filled states_
- As the _empty states moves opposite_ to the field, this can be modelled as a _hole moving in the direction of the field_
	- As the hole model has a _completely filled valence band_, the momentum _only comes from the hole band_
$$\bm{k}_h=-\bm{k}_e \hspace{1cm} \frac{d\bm{k}_h}{dt}=-\frac{d\bm{k}_e}{dt}$$
![[Hole movement.png]]
![[Hole vs eletron movement.png]]

### Return to the divalent metal
- In the 2D divalent metal, there are _holes_ in the 1st Brillouin zone, with _electrons_ in the 2nd Brillouin zone
- They have _different effective masses_ due to different curvatures
![[Divalent metal charge carriers.png]]

## Observation

### Hall Effect

### Cyclotron resonance

