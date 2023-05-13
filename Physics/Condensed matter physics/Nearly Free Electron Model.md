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
$$u_k(x)=\sum_{n=-\infty}^\infty C_{k,n}\frac{1}{\sqrt{A}}\exp(inG_1x)$$
- The _overall wave-function_ is then:
$$\Psi_k(x)=\sum_{n=-\infty}^\infty C_{k,n}\frac{1}{\sqrt{A}}\exp[i(k+nG_1)x]$$

- Equivalently:
$$\displaylines{\ket{\Psi_k}=\sum_{n=-\infty}^\infty C_{k,n}\ket{\phi_{k,n}}\\\braket{x|\phi_{k,n}}=\frac{1}{\sqrt{A}}\exp[i(k+nG_1)x]}$$
- $\ket{\phi_{k,n}}$ are the _electron basis states_
- In $k-$space, they are _seprarated by_ $G_1$ along the $k-$axis
- The states are represented by _plane waves_, hence they lie on the _free electron dispersion curve_
- The _overall wave-function_ is given by a _weighted sum_

- If the potential is _weak_, only basis states $\ket{\phi_{k,n}}$ with _energy close to that of the central basis state_ $\ket{\phi_{k,0}}$ will have _significant contributions_ to the overall wavefunction

## Two-state approximation
- For a weak potential, let the _electron wave function_ be a _linear combination_ of two basis states:
$$\ket{\Psi_k}=C_{k,0}\ket{\phi_{k,0}}+C_{k,1}\ket{\phi_{k,1}}$$
- $\ket{\phi_{k,1}}$ and $\ket{\phi_{k,-1}}$ are _both valid choices_

- For a _small value_ of $k$, near the centre, there is a _significant energy difference_ between the two states
- The _additional basis state_ has _little contribution_ to the overall wavefunciton:
$$\ket{\Psi_k}\approx\ket{\phi_{k,0}}$$
- The energy is _close to the free particle energy_

- For a _large value_ of $k$, near the _zone boundary_, the two states have _comparable energy_
- They both have a _significant contribution_ to $\ket{\Psi_k}$
- At $k=G_1/2$, they have _equal contributions_

- When the two states _contribute equally_, they superpose to form _standing waves_
- The $\cos^2$ probability distribution is _higher energy_
DIAGRAMMMMMMMMMMMMMMMMMMMM
- Hence, the _degeneracy of the two states is lifted_

## Solutions to the Schrodinger equation
AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA

## Band structure
- With a more _general_ potential:
$$V(x)=\sum_n V_n\cos(nG_1x)$$
- This will link states at _higher energies_
- There are _gaps_ at

- This leads to a _band structure_, where electron states can only lie in _energy ranges_, or _bands_
- The _Fermi energy_ $\varepsilon_F$ determines how _far up_ the band structure is filled
![[Electron bands.png]]
- The _level_ at which the bands are filled determines the _conductivity_ of the material