- Model the _classical reponse_ of charges to electromagnetic fields
- Leads to some predictions in the correct ballpark, but eventually _fails_

# Optical properties of insulators
- The response to a _high-frequency electromagnetic field_
- Wavelength is assumed to be _long compared to inter-atomic spacing_

## Lorentz dipole oscillator model
- An atom is modelled as a _nucleus with an electron cloud_
- An electric field leads to _displacement_ of the cloud
- The restoring force is typically _proportional to displacement_
![[classical atom response to field.png]]

### Finding relative permittivity
- For some _displacement_ $u$:
$$m \ddot{u}+m\gamma\dot{u}+m\omega_{T}^{2}u=qE$$
- $\omega_{T}$ is the _natural frequency_ of the system
	- It is in a _trap_ due to the nucleus
- $\gamma$ gives _damping_
- Consider an _oscillating electric field_ $E=E_{\omega}\exp(-i\omega t)$
- This results in _displacement_ $u=u_{\omega}\exp(ii\omega t)$
- This results in _dipole moment per atom_:
$$p_{\omega}=qu_{\omega}$$
- This gives some _polarisation_ $\boldsymbol{P}$

- For a solid with _number density_ $n_{V}=N/V$, and from the definition of [[Electrodynamics and Optics#Media|electrical susceptibility]]:
$$\chi_{\omega}=n_{V}\frac{q^{2}}{m\epsilon_{0}(\omega_{T}^{2}-\omega^{2}+i\omega\gamma )}$$
- This is typical of a _damped driven harmonic oscillator_

- The _relative permittivity_ $\epsilon_{\omega}\equiv 1+\chi_{\omega}$
![[Insulator permittivity.png|500]]

### Optical response
- From analogy with the [[Oscillations#Power|damped harmonic oscillator]], this leads to the _power absorbed_:
$$P=\frac{1}{2}\omega\epsilon_{0}\left| E_{\omega }^{2} \right| \text{Im}(\epsilon_{0})$$
- There is some _resonant_ frequency where there is a _peak in energy absorbed_
	- Corresponds to an _energy difference_ in [[Atomic transitions|energy transitions]]

- At _low frequencies_:
$$\epsilon(\omega\to 0)=1+n_{V}\frac{q^{2}}{m\epsilon_{0}\omega_{T}}$$
- This means the _static permittivity_ still depends on the _natural frequency_
- This then gives different _reflectivities_:
$$r=\frac{\sqrt{ \epsilon_{1} }-\sqrt{ \epsilon_{2} }}{}\hspace{1.5cm}R=|r|^{2}$$

- In a _solid_, the polarisation fields of _other atoms_ leads to a _different frequency_ from the natural frequency of a single atom

### Quantum mechanical model
- From [[Time-dependent quantum mechanics#Fermi's Golden Rule|time-dependent perturbation theory]]:
$$\chi_{\omega}=(E_{b}-)$$
- The _imaginary part_ gives the [[Atomic transitions|transition rate]], as it represents _energy absorption_
- This can also be written as (with small $\gamma$):
$$\chi_{\omega}\propto \frac{1}{E_{b}-E_{a}-\hbar \omega-i\hbar\gamma/2}$$
- As energy levels _broaden_ and $\gamma$ increases, this becomes similar to the _classical Lorentz model close to resonance_:
$$\chi_{\omega}\propto \approx$$

### Multiple transitions
- One can _superimpose_ multiple spectra of Lorentz oscillators
- There may be _multiple allowed energy transitions_
- One can simply _add frequency responses_:
$$\epsilon(\omega)=1+\sum_{i}\chi_{i}(\omega)$$
![[Lorentz oscillator many frequencies.png|500]]

### Example: silica glass
- One can introduce a _complex refractive index_:
$$\displaylines{\epsilon=(n+ik)^{2} \\ n\approx \sqrt{ \text{Re}(\epsilon) }\hspace{1.5cm} \kappa=\frac{\text{Im}(\epsilon)}{2n}}$$
- Transparent in visible light
- IR: vibrations
- UV: core transitions

- In the _visible region_, due to the "tails" of absorption in IR and UV, $n$ _increases with frequency_
- This leads to _dispersion_

- Given a short _light pulse_ of duration $t_{p}$, there is a _range of frequencies_ $\delta f\approx 1/t_{p}$
- This gives _spreading_ of wave packets due to differencies in group velocities
- The _temporal broadening:
$$\Delta \tau \propto \propto \propto \frac{d^{2}n}{d\lambda^{2}}$$
- From the Lorentz model, $d^{2}n/d\lambda^{2}$ _changes sign_ at the absorption line
- One must _choose_ $dn^{2}/d\lambda^{2}=0$ for sending _optical signals_ to minimise broadening

# Drude model for metals
- Electrons are _no longer bound_ to ions
- However, _core electrons_ will still _contribute to permittivity_ as oscillators
- As for _outer electrons_, the _spring constant_ is effectively zero
- Hence, as $\omega_{T}\to 0$, the _resonance_ is then at $f=0$
- This model of having free electrons is the _Drude model_

- The _bound electrons_ give susceptibility $\chi_{\infty}$
- Hence, the total susceptibility:
$$\chi_{\omega}=\chi_{\infty}-\frac{nq^{2}}{}$$
- This gives the permittivity:
$$\epsilon_{\omega}=\epsilon_{\infty}-\frac{\omega_{p}^{2}}{}\hspace{1.5cm}\omega_{p}$$
- Here, $\omega_{p}$ is the _plasma frequency_
- $|\epsilon_{\omega}|$ _diverges_ as $\omega\to 0$ hence metals are _highly reflective_ at low frequencies
- There is also the _Drude peak_ at

- Crossing zero
- High frequency:
- _Transparent in the ultraviolet_

- Reflectivity
- Plateau at low frequency
- At high frequency, $\propto$
- Background permittivity $>1$

- Experimental results typically have _lower_ reflectivity due to _scattering_, and _interband absorption_
- Example: aluminium

## Plasma oscillations
- Electrons moving in a _positively charged environment_
- Consider an _applied oscillating field_ $\boldsymbol{D}$
	- It is _continuous_ across the interface
$$\boldsymbol{D=}$$

- The _permittivity_:


- In _metals_, $\omega_{p}\gg\gamma=$, and $\epsilon_{\omega}\approx 1$, hence
- One gets _plasma oscillations_

