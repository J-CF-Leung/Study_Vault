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
$$\chi_{\omega}=n_{V}\frac{q^{2}}{m\epsilon_{0}(\omega_{T}^{2}-\omega^{2}-i\omega\gamma )}$$
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
$$r=\frac{\sqrt{ \epsilon_{1} }-\sqrt{ \epsilon_{2} }}{\sqrt{ \epsilon_{1} }+\sqrt{ \epsilon_{2} }}\hspace{1.5cm}R=|r|^{2}$$

- In a _solid_, the polarisation fields of _other atoms_ leads to a _different frequency_ from the natural frequency of a single atom

### Quantum mechanical model
- From [[Time-dependent quantum mechanics#Fermi's Golden Rule|time-dependent perturbation theory]]:
$$\chi_{\omega}=(E_{b}-E_{a}-\hbar\omega)^{-1}+i\delta(E_{b}-E_{a}-\hbar\omega)$$
- The _imaginary part_ gives the [[Atomic transitions|transition rate]], as it represents _energy absorption_
- This can also be written as (with small $\gamma$):
$$\chi_{\omega}\propto \frac{1}{E_{b}-E_{a}-\hbar \omega-i\hbar\gamma/2}$$
- As energy levels _broaden_ and $\gamma$ increases, this becomes similar to the _classical Lorentz model close to resonance_:
$$\chi_{\omega}\propto \frac{\omega_{T}+\omega}{\omega_{T}^{2}-\omega^{2}-i(\omega_{T}+\omega)\gamma/2}\approx \frac{2\omega_{T}}{\omega_{T}^{2}-\omega^{2}-i\omega\gamma}$$

### Multiple transitions
- One can _superimpose_ multiple spectra of Lorentz oscillators
- There may be _multiple allowed energy transitions_
- One can simply _add frequency responses_:
$$\epsilon(\omega)=1+\sum_{i}\chi_{i}(\omega)$$
![[Lorentz oscillator many frequencies.png|500]]

### Example: silica glass
- One can introduce a _complex refractive index_:
$$\displaylines{\epsilon=(n+ik)^{2} \\ n\approx \sqrt{ \text{Re}(\epsilon) }\hspace{1.5cm} \kappa=\frac{\text{Im}(\epsilon)}{2n}}$$
- It is a _weakly absorbing medium_, with _extinction coefficient_ $\kappa$

- Glass is _transparent in visible light_
- The _IR absorption_ is from _molecular vibrations_
- The _UV absorption_ is from _transitions of core electrons_
![[Silica glass refractive index.png|500]]

- In the _visible region_, due to the "tails" of absorption in IR and UV, $n$ _increases with frequency_
- This leads to _dispersion_

- Given a short _light pulse_ of duration $t_{p}$, there is a _range of frequencies_ $\delta f\approx 1/t_{p}$
- This gives _spreading_ of wave packets due to differencies in group velocities
- The _temporal broadening:
$$\Delta \tau \propto \frac{d^{2}\omega}{dk^{2}} \propto \frac{d^{2}n}{dk^{2}}\propto \frac{d^{2}n}{d\lambda^{2}}$$
- From the Lorentz model, $d^{2}n/d\lambda^{2}$ _changes sign_ at the absorption line
- One must _choose_ $dn^{2}/d\lambda^{2}=0$ for sending _optical signals_ to minimise broadening

# Drude model for metals
- Electrons are _no longer bound_ to ions
- However, _core electrons_ will still _contribute to permittivity_ as oscillators
- As for _outer electrons_, the _spring constant_ is effectively zero

- Hence, as $\omega_{T}\to 0$, the _resonance_ is then at $f=0$
- This model of having free electrons is the _Drude model_

## Optical properties
- The _bound electrons_ give susceptibility $\chi_{\infty}$
- Hence, the total susceptibility:
$$\chi_{\omega}=\chi_{\infty}-\frac{nq^{2}}{m\epsilon_{0}(\omega^{2}+i\omega\gamma)}$$
- This gives the permittivity:
$$\epsilon_{\omega}=\epsilon_{\infty}-\frac{\omega_{p}^{2}}{\omega^{2}+i\omega\gamma}\hspace{1.5cm}\omega_{p}^{2}=\frac{nq^{2}}{m\epsilon_{0}}$$
- Here, $\omega_{p}$ is the _plasma frequency_
- $|\epsilon_{\omega}|$ _diverges_ as $\omega\to 0$ hence metals are _highly reflective_ at low frequencies
- There is also the _Drude peak_ for absorption at _low_ $\epsilon$
![[Metal permittivity.png|500]]

- At $\omega_{p}^{*}$, there is _zero permittivity_
- At _high frequency_, $\epsilon(\omega)\to 1$, and the metal becomes _transparent in the ultraviolet_

- Consider _reflectivity_ $R=|r|^{2}$
![[Metal reflectivity.png|500]]
- At _low frequency_, the reflectivity _plateaus_
	- Related to the _conductivity_
- At high frequency, $R\propto 1/\omega^{4}$
- If the _core electrons_ are _more polarisable_, and $\epsilon_{\infty}$ is large enough, reflectivity can _go to zero_

- Experimental results typically have _lower_ reflectivity due to _scattering_, and _interband absorption_
- Example: aluminium
![[Aluminium reflectivity.png|500]]

## Plasma oscillations
- Electrons moving in a _positively charged environment_
- Consider an _applied oscillating field_ $\boldsymbol{D}$
	- It is _continuous_ across the interface
$$\boldsymbol{D}=\epsilon_{0}\boldsymbol{E}+\boldsymbol{P}\implies \boldsymbol{P}=\frac{\boldsymbol{D}}{1-\epsilon_{\omega}^{-1}}$$

- The _permittivity_ (assuming $\epsilon_{\infty}\approx 1$):
$$\epsilon_{\omega}^{-1}=\frac{\omega^{2}+i\omega\gamma}{\omega^{2}-\omega_{p}^{2}+i\omega\gamma}$$

- In _metals_, $\omega_{p}\gg\gamma=\tau^{-1}$, and $\epsilon_{\infty}\approx 1$, hence $\epsilon_{\omega_{p}}\approx0$

- In the _general case_, as $\epsilon_{\omega}\to 0$ at $\omega=\omega_{p}^{*}\equiv\omega_{p}\sqrt{ \epsilon_{\infty} }$, one gets _plasma oscillations_
- _Polarisation_ causes a _build-up_ of _surface charge_, generating a _restoring force_ and hence causing _oscillation_ of charges

- The _energy_ of the plasma oscillations can be obtained from EELS (Electron energy-loss spectroscopy)

## Electrical conductivity
- The _gas_ of electrons are _scattered_ by positive ion cores
- Between collisions, they _do not interact with each other_
- Collisions are _instantaneous_
- The _probability_ an electron has a collision in unit time is $\tau^{-1}$, the _scattering rate_
- Through these collisions, electrons achieve _equilibrium_


- Setting $\omega_{T}\to 0$ gives an _arbitrary offset_ in displacement as they _no longer oscillate_
- _Scattering_ also means that electrons _do not all have the same velocity_
	- They follow a _statistical distribution_

- In the equation of motion, consider velocity $\boldsymbol{v}$ as the variable
- _Average_ over all electrons to give a _"drift" velocity_

### Relating permittivity to conductivity
- With _displacement_ $\boldsymbol{u}$:
	- _Current density_: $\boldsymbol{j}=nq\dot{\boldsymbol{u}}$
	- _Polarisation_: $\boldsymbol{P}=nq\boldsymbol{u}$ for the _conduction electrons_

- Adding polarisation of the _core electrons_:
$$\dot{\boldsymbol{P}}=\boldsymbol{j}+\chi_{\infty}\epsilon_{0}\dot{\boldsymbol{E}}$$
- Substituting harmonic solutions:
$$\boldsymbol{E}=\boldsymbol{E}_{\omega}\exp(-i\omega t)\hspace{1cm}\boldsymbol{j}=\boldsymbol{j}_{\omega}\exp(-i\omega t)$$

- Ohm's law: $\boldsymbol{j}_{\omega}=\sigma_{\omega}\boldsymbol{E}_{\omega}$
- This gives permittivity:
$$\epsilon_{\omega}=\epsilon_{\infty}+\frac{i\sigma_{\omega}}{\epsilon_{0}\omega}$$
- This relates the _AC conductivity_ to the _imaginary part of the permittivity_
	- Therefore, _conductivity_ can be measured by _optical measurements_
- One can often approximate $\epsilon_{\infty}=1$

### Relaxation time approximation
- The _current density_ due to the _drift velocity_ $\boldsymbol{v}$:
$$\boldsymbol{j}=-ne\boldsymbol{v}=-\frac{ne}{m}\boldsymbol{p}$$
- The _probability_ that there is a _collision_ in time $\delta t$ is $\delta t/\tau$
- Given that there is an _external force_ $\boldsymbol{f}(t)$, only electrons that _have not collided_ will be affected
	- The fraction of electrons that _have_ collided is of the order $\delta t$, hence their change in momentum due to $\boldsymbol{f}(t)$ is _negligible_
$$\boldsymbol{p}(t+\delta t)=\left( 1-\frac{\delta t}{\tau} \right)(\boldsymbol{p}(t)+\boldsymbol{f}(t)\delta t)$$
- This gives the _differential equation_:
$$\frac{d\boldsymbol{p}(t)}{dt}=-\frac{\boldsymbol{p}(t)}{\tau}+\boldsymbol{f}(t)$$
- Collisions give a _frictional damping_
	- This is the _relaxation time approximation_

- Applying a _constant electric field_ $\boldsymbol{E}$, in the _steady state_, one gets:
$$\sigma=\frac{ne^{2}\tau}{m}$$

- When one applies both _electric and magnetic fields_, $\boldsymbol{f}=q(\boldsymbol{E}+\boldsymbol{v}\times \boldsymbol{B})$

- If $\boldsymbol{E}=\boldsymbol{E}_{\omega}\exp(-i\omega t)$ and $\boldsymbol{B}=0$, producing an _oscillating current_, the _conductivity is dependent on frequency_:
$$\sigma_{\omega}=\frac{nq^{2}\tau}{m(1-i\omega \tau)}=\frac{\epsilon_{0}\omega_{p}^{2}\tau}{1-i\omega \tau}$$
- Here, $\omega_{p}$ is the [[#Optical properties|plasma frequency]]
- $\omega \tau$ gives an _estimate of the number of collision events in a period_

- At _low frequencies_ $\omega \tau\ll 1$:
$$\sigma_{0}=\frac{ne^{2}\tau}{m}=ne\mu \hspace{1cm}\mu\equiv \frac{e \tau}{m}$$

- $\mu$, the _carrier mobility_, quantifies how well carriers _respond to an electric field_:
$$\mu=\frac{e \tau}{m}=\frac{\left| \boldsymbol{v} \right|}{|\boldsymbol{E}|} $$
- Using the formula for _permittivity_:
$$\epsilon_{\omega}=\epsilon_{\infty}+\frac{i\sigma_\omega}{\epsilon_{0}\omega}=\epsilon_{\infty}-\frac{\omega_{p}^{2}}{\omega^{2}+i\omega/\tau}$$
- This _recovers_ the expression from the [[#Optical properties|Lorentz oscillator]] with $\omega_{\tau}=0$, with $\gamma=\tau^{-1}$

## Flaws in the Drude model
- Assuming that collisions _completely randomise momentum_

- Fermi sphere
- Scattering: at the _Fermi surface_

- Scattering: other particles (phonons, lattice defects)
	- Scattering _between electrons_: the _total electron momentum_ is conserved, to give _little effect on conductivity_

## Transport in electric and magnetic fields
- wlog, take $\boldsymbol{B}=B\hat{z}$
- In the _steady state_ $d\boldsymbol{j}/dt=0$

- Eventually, for a material with _finite extent_, there is a _charge build-up_, leading to a _transverse field_ and _confining_ the current to the $x-$direction

- The _Hall coefficient_:
$$R_{H}=\frac{E_{y}}{j_{x}B}=\frac{1}{nq}$$
- This gives _carrier density_, and the _sign of charge_

- _Cyclotron frequency_

- Drude theory predicts that $R_{H}$ is _independent_ of $B$ and $\tau$
- However, _experiments_ confirm that

- $R_{H}$ can also _change sign_

- Scanning Hall probe microscopy

## Incorrect predictions of Drude theory
- The Drude model predicts _heat capacity_ to be constant at $3nk_{B}/2$
	- It is _independent_ of temperature
	- Given by the _equipartition theorem_
- The _measured_ heat capacity is _dependent_ on temperature and falls _below_ $3nk_{B}/2$

- While the _oscillator model_ gives correct predictions of _optical properties_, it fails to predict _thermodynamic properties_ (as the equipartition theorem is applied again)

- At _low temperatures_, electron motion is typically _frozen_ as thermal energy is _not enough_ to excite them to higher energy states
	- A _quantum_ effect

- A correct description has electrons as a [[Sommerfeld model|Fermi gas]]