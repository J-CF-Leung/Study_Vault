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

- A correct description has electrons as a [[#Sommerfeld model|Fermi gas]]

# Sommerfeld model
- Typically, in _insulators_, electronic energy levels are of the order $\text{eV}$, corresponding to a _temperature_ of $\sim 10,000\text{ K}$
- Hence, _electronic specific heat_ is only significant in very high temperatures

- In _metals_, one can have _low energy excitations_ for a _small fraction of electrons_
- Conduction electrons form a [[Advanced statistical mechanics#The Fermi gas|degenerate Fermi gas]]
- A _fraction_ $\sim k_{B}T/E_{F}$ are close enough to $\mu$ to contribute to _heat capacity_

- For electrons on the _Fermi surface_, most travel at _very high speeds_
- Without external field, the _drift velocity_ $\left<v\right>$ is $0$

## Free electron gas and the Fermi sphere
- The _free electron gas_:
$$-\frac{\hbar^{2}}{2m}\nabla^{2}\psi(\boldsymbol{r})=E\psi(\boldsymbol{r})$$
- Introduce _eigenstates_
$$\psi(\boldsymbol{r})$$

- With _periodic boundary conditions_, the _allowed values_ of $\boldsymbol{k}$ are _discrete_:
$$\boldsymbol{k}=$$
- $n_i$ are _positive or negative integers_

- At _zero temperature_, the _Fermi sphere_ is filled up to Fermi energy $E_{F}$
- Each _triplet_ of $n_{i}$ corresponds to _2 states_ due to _spin degeneracy_
- The _volume_ of a $\boldsymbol{k}-$state is $(2\pi/L)^{3}$

- Writing out the _volume_ of the Fermi sphere in terms of $k_{F}$, one gets:
$$N=2 \left( \frac{4}{3}\pi k_{F}^{3} \right)\left( \frac{2\pi}{L} \right)^{-3}\implies k_{F}=(3\pi^{2}n)^{1/3}$$
- One then gets $E_{F}\propto n^{2/3}$

- Define a _density of states_ w.r.t. $E_{F}$:
$$g(E_{F})\equiv \frac{dn}{dE_{F}}=\frac{3}{2} \frac{n}{E_{F}}$$
- The _density of states_ w.r.t. energy:
$$g(E)\,dE=\frac{2(4\pi k^{2}\,dk)}{8\pi^{3}/V}$$
- It is _proportional to volume_
- One can define $g_{V}(E)$ as _number of states per energy per unit volume_ to remove the normalisation factor $V$:
$$g_{V}(E)=\frac{1}{V}g(E)$$

## Thermodynamic properties
- The [[Advanced statistical mechanics#The Fermi gas|Fermi distribution]]:
$$f(E)=\frac{1}{\exp[(E-\mu)/k_{B}T]+1}$$
- At _zero temperature_, the _chemical potential_ $\mu=E_{F}$
	- The distribution is a _step function_
- At finite temperature, there is some _smearing_ $\sim k_{B}T$
- At _room temperature_, $k_{B}T\approx 26 \text{ meV}$
- For _metals_, $E_{F}\approx 1-10\,\text{eV}\gg k_{B}T_\text{room}$

- The _number density_:
$$n=\frac{1}{V}\sum_\text{states} f(E_{i})=\int  g(E)f(E) \, dE $$
- The _internal energy density_:
$$u=\frac{U}{V}=\int E\,g(E)\,f(E) \, dE $$
- The _heat capacity at constant volume_:
$$c_{V}=\frac{\partial u}{\partial T}\Bigg|_{V}=\int E \,g(E)\,\frac{\partial f(E)}{\partial T} \, dE $$
- The derivative is _sharply peaked_ at the _chemical potential_ $\mu$
- Hence, the _contributions_ are mainly from states _around_ $k_{B}T$ of $\mu$
- Each state has specific heat $\sim k_{B}$, giving total specific heat:
$$c_{V}\approx n \frac{k_{B}T}{E_{F}}k_{B}$$
- One gets a more exact answer from the [[Advanced statistical mechanics#Away from absolute zero|Sommerfeld expansion]]:
	- It is a _leading order term_ from the expansion of $\mu$ in powers of $(k_{B}T/E_{F})^{2}$
$$c_{V}=\frac{\pi^{2}}{3}k_{B}^{2}Tg(E_{F})$$
- Defining the _Fermi temperature_ $T_{F}=E_{F}/k_{B}$
$$c_{V}=\frac{\pi^{2}}{2}\frac{T}{T_{F}}nk_{B}$$

- Typically in _solids_, this is much smaller than the _lattice specific heat_ due to [[Phonons]]
- It is more achieveable with a _mixture_ of $\ce{ ^{3}He }$ and $\ce{ ^{4}He }$ (Fermi gas of atoms)

## Electrostatic screening
- Consider adding some _positive charge_ to a solid
- In a _metal_, _classically_, electrons can _move freely_, and _screen_ the positive charge, _cancelling out_ the electric field
	- In a _dielectric_, the potential is _reduced_ by the dielectric constant $\epsilon$

- _Quantum mechanically_, electrons are _waves_ and hence the electrons _cannot be aribitrarily close to the charge_
	- Electrons _minimise_ the _potential and kinetic energies_
- There is a _length scale_ over which the external charge is _screened_

### Peturbing potential
- The _charge density response_ of a free-electron gas to some _potential_ $V_{0}(\boldsymbol{r})$
$$\nabla^{2}V_{0}(\boldsymbol{r})=-\frac{\rho_{0}(\boldsymbol{r})}{\epsilon_{0}}$$
- Consider the _"jellium"_ model where the electron gas _balances the positive background charge_. such that $\rho_{0}(\boldsymbol{r})=0$
	- Not including charges set up for the perturbing potential

- In the presence of a _perturbing potential_ $V_\text{ext}(\boldsymbol{r})$, the _charge density redistributes_ to $\rho(\boldsymbol{r})=\rho_{0}(\boldsymbol{r})+\delta \rho(\boldsymbol{r})$
- This then _changes the potential_ to $V(\boldsymbol{r})=V_{0}(\boldsymbol{r})+\delta V(\boldsymbol{r})$:
	- The correction $\delta \rho$ is _independent_ of the _external_ charges which obey $\nabla^{2}V_\text{ext}=-\rho _\text{ext}/\epsilon_{0}$
$$\nabla^{2}\delta V(\boldsymbol{r})=-\frac{\delta \rho(\boldsymbol{r})}{\epsilon_{0}}$$
- Electrons experience the _total potential_ $V_\text{tot}=V_\text{ext}+\delta V$:
$$-\frac{\hbar^{2}}{2m}\nabla^{2}\psi(\boldsymbol{r})+(-e)[\delta V(\boldsymbol{r})+V_\text{ext}(\boldsymbol{r})]\psi(\boldsymbol{r})=E\psi(\boldsymbol{r})$$

### Thomas-Fermi approximation
- Assume the perturbing potential is _slowly varying_, affecting _free energy levels_ as:
	- It varies on a _lengthscale larger than_ $k_{F}$
	- Equivalent to considering a _spatially varying Fermi energy_
$$E(\boldsymbol{k},\boldsymbol{r})=\frac{\hbar^{2}k^{2}}{2m}-eV_\text{tot}(\boldsymbol{r})$$
- The electrons are _filled up to constant chemical potential_ $\mu$
- Therefore, the _local Fermi energy_ must be adjusted:
$$\mu=E_{F}(\boldsymbol{r})-eV_\text{tot}(\boldsymbol{r})$$
![[Fermi approximation shift.png]]
- A shift in the _local_ Fermi energy leads to a _change in local electron number density_ $n$:
	- Density of state is _normalised by volume_
$$\delta n=g_{V}(E_{F})\delta E_{F}=eg_{V}(E_{F})V_\text{tot}=\frac{\delta \rho}{e}$$
- Substitute back into _Poisson's equation_:
$$\nabla^{2}\delta V(\boldsymbol{r})=\frac{e}{\epsilon_{0}}g_{V}(E_{F})(\delta V(\boldsymbol{r})+V_\text{ext}(\boldsymbol{r}))$$
- Then using _Fourier decomposition_ with wave-vector $\boldsymbol{q}$, and defining the _Fermi wave-vector_:
$$\displaylines{q_\text{TF}\equiv \sqrt{\frac{e}{\epsilon_{0}}g_{V}(E_{F})} \\ \delta V(\boldsymbol{q})=-\frac{q_\text{TF}^{2}}{q^{2}+q_\text{TF}^{2}}V_\text{ext}(\boldsymbol{q})}$$
### Free electron gas
- For the _3D free electron gas_:
$$g_{V}(E)=\frac{1}{2\pi^{2}}\left( \frac{2m}{\hbar^{2}} \right)^{3/2}E^{1/2}\implies g_{V}(E_{F})=\frac{m}{\pi^{2}\hbar^{2}}k_{F}$$
- This gives:
$$q_{TF}^{2}=\frac{1}{\pi^{2}} \left( \frac{me^{2}}{\epsilon_{0}\hbar^{2}} \right)k_{F}=\frac{4}{\pi} \frac{k_{F}}{a_{0}}$$
- Here, $a_{0}$ is the _Bohr radius_ $4\pi \hbar^{2}\epsilon_{0}/(me^{2})\approx 0.53\text{ Å}$
- The _Thomas-Fermi screening length_ is $q_\text{TF}^{-1}$
	- For copper, $n=8.5\times 10^{22}\text{ cm}^{-3}$, and $1/q_\text{TF}=0.055\text{ nm}$
- Often comparable to the _Wigner-Seitz radius_ $r_{S}$:
$$\frac{4\pi}{3}r_{s}^{3}=n^{-1}=\frac{3\pi^{2}}{k_{F}^{3}}$$

- The _induced electron number density_, with a given $V_\text{ext}(\boldsymbol{q})$:
$$n_\text{ind}(\boldsymbol{q})=\delta n(\boldsymbol{q})=\frac{\epsilon_{0}}{e}V_\text{ext}(\boldsymbol{q})\left( \frac{q^{2}}{q^{2}/q_\text{TF}^{2}+1} \right)$$
### Thomas-Fermi dielectric function
- The wave-vector dependent _dielectric function_ $\epsilon(\boldsymbol{q})$ relates the _electric displacement_ $\boldsymbol{D}$ and _electric field_ $\boldsymbol{E}$ by:
$$\boldsymbol{D}(\boldsymbol{q})=\epsilon(\boldsymbol{q})\epsilon_{0}\boldsymbol{E}(\boldsymbol{q})$$
- Given $\nabla V_\text{ext}=-\boldsymbol{D}/\epsilon_{0}$ and $\nabla V_\text{tot}=-\boldsymbol{E}$:
$$V_\text{ext}(\boldsymbol{q})=\epsilon(\boldsymbol{q})V_\text{tot}(\boldsymbol{q})$$
- One then gets the _Thomas-Fermi dielectric function_:
$$\epsilon^\text{TF}(\boldsymbol{q})=1+\frac{q_\text{TF}^{2}}{q^{2}}$$
### Thomas-Fermi screening
- For _small_ $q$ (long distances), $\epsilon^{\text{TF}}\propto 1/q^{2}$
- The _long range_ part of the _Coulomb potential_ is then  _exactly cancelled_

- In _real space_, for a _long range Coulombic perturbing potential_:
$$V_\text{ext}=\frac{Q}{r}$$
- The _screened potential_, or the _Yukawa potential_ is then:
$$V(r)=\frac{Q}{r}\exp(-q_\text{TF}r)$$
- The exponential factor _reduces range_ of the Coulomb potential
	- Screened over distances _comparable_ to inter-perticle spacing
	- Metals: $r_{s}/a_{0}\sim 2-6$
- A _mobile electron gas_ is _highly effective_ at _screening_ external charges
	- Applies to the _resistivity_ of alloys, as _substitutional atoms_ can _add excess charge_
- _Foreign_ atoms scatter _conduction electrons_ with interaction given by the _screened Coulomb potential_, hence scattering contributes to an _increase in resistivity_