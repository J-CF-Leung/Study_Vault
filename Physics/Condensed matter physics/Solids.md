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
- This results in _displacement_ $u=u_{\omega}\exp(-i\omega t)$
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
- This can also be written as (with small $\gamma$):Calculate the  
difference in the refractive index of the do
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

- When one applies both _electric and magnetic fields_, $\boldsymbol{f}=q(\boldsymbol{E}+\boldsymbol{v}\times \boldsymbol{B})$, and the equation of motion is:
$$\frac{d\boldsymbol{p}(t)}{dt}=-\frac{\boldsymbol{p}(t)}{\tau}+q(\boldsymbol{E}+\boldsymbol{v}\times \boldsymbol{B})$$

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

## Transport with magnetic fields and the Hall effect
- In the _relaxation time approximation_:
$$\frac{d\boldsymbol{j}(t)}{dt}=-\frac{\boldsymbol{j}(t)}{\tau}+ \frac{nq^{2}}{m}\boldsymbol{E}+\frac{q}{m}(\boldsymbol{j}\times \boldsymbol{B})$$

- wlog, take $\boldsymbol{B}=B\hat{z}$
- In the _steady state_ $d\boldsymbol{j}/dt=0$:
	- The dimensionless constant $\beta=qB\tau/m=\omega_{c}\tau$, where $\omega_{c}$ is the _cyclotron frequency_
$$\begin{align}
j_{x}&=qn\left( \frac{q\tau}{m}E_{x}+\beta v_{y} \right) \\ j_{y}&=qn\left( \frac{q\tau}{m}E_{y}-\beta v_{x} \right) \\ j_{z}&=\frac{nq^{2}\tau}{m}E_{z}
\end{align}$$

- Eventually, for a material with _finite extent_, there is a _charge build-up_, leading to a _transverse field_ and _confining_ the current to the $x-$direction ($v_{y}=0$):
$$\boldsymbol{E}=-\boldsymbol{v}\times \boldsymbol{B}$$
- This is the _Hall effect_, with a measurable _Hall voltage_

- The _Hall coefficient_:
$$R_{H}=\frac{E_{y}}{j_{x}B}=\frac{1}{nq}$$
- This gives _carrier density_, and the _sign of charge_

- Drude theory predicts that $R_{H}$ is _independent_ of $B$ and $\tau$
- However, _experiments_ confirm that it can vary with both
- $R_{H}$ can also _change sign_

- Scanning Hall probe microscopy: using a _Hall bar_ to measure _local magnetic field_

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

- Typically in _solids_, this is much smaller than the _lattice specific heat_ due to [[Phonons (IB)]]
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
$$\nabla^{2}\delta V(\boldsymbol{r})=\frac{e^{2}}{\epsilon_{0}}g_{V}(E_{F})(\delta V(\boldsymbol{r})+V_\text{ext}(\boldsymbol{r}))$$
- Then using _Fourier decomposition_ with wave-vector $\boldsymbol{q}$, and defining the _Fermi wave-vector_:
$$\displaylines{q_\text{TF}\equiv \sqrt{\frac{e^{2}}{\epsilon_{0}}g_{V}(E_{F})} \\ \delta V(\boldsymbol{q})=-\frac{q_\text{TF}^{2}}{q^{2}+q_\text{TF}^{2}}V_\text{ext}(\boldsymbol{q})}$$
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

# Bonding mechanisms
- _Cohesion_ in a medium is due to _interactions_ between _electrons and nuclei_, such that there is an _effective potential_ for movement of _atoms_

- Bonding potential depends on the _electron configurations_ of the constituent atoms

## van der Waals
- Typical in _inert gases_
	- With _filled electron shells_, leading to _large ionisation energies_
- Between _neutral atoms_, which give _weak interactions_

- Apart from $\ce{ He }$, inert gases form _close-packed face-centred cubic solids_

### Force between induced dipoles
- Consider an atom as an _oscillator_, as electrons _fluctuate_ around the _nucleus_
- Fluctuations give a _dipole moment_ $p_{1}$, which causes an _electric field_:
$$E_{1} \propto \frac{p_{1}}{R^{3}}$$
- This then _induces_ a dipole on the second atom (with _polarisability_ $\alpha$):
$$p_{2} \propto \frac{\alpha p_{1}}{R^{3}}$$
- This then _induces_ another electric field at the first atom:
$$E_{1} \propto \frac{p_{2}}{R^{3}}\propto \frac{\alpha p_{1}}{R^{6}}$$
- The _energy_ of the system changes by:
$$\Delta U=-\langle \boldsymbol{p_{1}}\cdot \boldsymbol{E}_{1} \rangle\propto -\frac{\alpha \left<p_{1}^{2}\right>}{R^{6}} $$
- The force is always _attractive_
	- $\left<p_{1}\right>^{2}=0$, and $\left<p_{1}^{2}\right>\neq 0$

### Overall potential
- If the _electron charge distributions_ of atoms _overlap_, they start to _repel_ each other
	- Contributions from _electrostatic_ forces, and _Pauli exclusion_
- This gives a _short range potential_
- The _Lennard-Jones_ potential:
	- Purely _empirical_
$$V(r)=4\varepsilon\left[ \left( \frac{\sigma}{r} \right)^{12}-\left( \frac{\sigma}{r} \right)^{6} \right]=\epsilon\left[ \left( \frac{R_\text{min}}{r} \right)^{12}-2\left( \frac{R_\text{min}}{r} \right)^{6} \right]$$
![[Lennard-Jones potential.png|400]]
- $\sigma$ and $\varepsilon$ are parameters _depending on the atoms_

- _Layers_ of 2D materials are also held together by van der Waals forces:
![[2D materials.png]]
## Ionic bonding
- For atoms with _electronic configuration close to a filled shell_, they will _gain or lose electrons_ to have a filled shell

- An atom with _excess electrons_ will _ionise_ with _ionisation energy_ $I$ in the _gas phase_:
$$\ce{ M } \xrightarrow{I} \ce{ M+ +e- }$$
- An atom with _insufficient electrons_ can _gain_ an electron with _electron affinity_ $A$:
$$\ce{ X +e- }\xrightarrow{A}\ce{ X- }$$

- An _ionic structure_ forms if the _electrostatic binding energy_ is _stronger_ than the _energetic cost_ $I+A$
- The binding energy as the _sum of pair Coulomb interactions_:
$$U=\frac{1}{2}\sum_{i}\sum_{j\neq i}U_{ij}=\frac{1}{2}\sum_{i}\sum_{i\neq j} \frac{1}{4\pi\epsilon_{0}} \frac{\pm_{ij}q^{2}}{R_{ij}}$$
- Depending on the nature of $i$ and $j$, the interaction can be _attractive_ or _repulsive_

- For a _regular lattice_ with some constant $R$:
$$U=-\frac{\alpha_{M}q^{2}}{4\pi\epsilon_{0}R}$$
- Here, $\alpha_{M}$ is the _Madelung constant_, which is _dependent on the structure_

- One must also account for a _short range repulsive force_
	- Influenced by the _size of ions_

- Most ionic structures have _coordination number_ around $6-8$

## Covalent bonding
- A _covalent bond_ is an _electron pair_ which _hold atoms together_
- The _overlapping orbitals_ on neighbouring atoms _hybridise_ to form new orbitals
- The overall Hamiltonian must be _symmetric_ about the point _between equivalent nuclei_, hence eigenstates must have _odd or even parity_ about that point

### Hydrogen molecule
- The _toy model_ is the _hydrogen molecule_
- With a _basis_ of atomic states $\phi(\boldsymbol{r}-\boldsymbol{R})$, where the _nucleus_ is at $\boldsymbol{R}$, one gets two states, of _even_ and _odd_ parity:
$$\psi_{\pm}(r)=\phi(\boldsymbol{r}-\boldsymbol{R}_{a})\pm \phi(\boldsymbol{r}-\boldsymbol{R}_{b})$$
- $\psi_{+}$ is _non-zero_ between the nuclei, while $\psi_{-}$ has a _node_ there

- For an _attractive potential_, $E_{+}<E_{-}$ and two electrons of _opposite spin_ occupy the _lower (bonding) state_ $\psi_{+}$
- The _antibonding state_ is separated from the bonding state by $E_{g}=E_{-}-E_{+}$ and becomes _unfilled_
![[Hydrogen atom states.png]]

### Calculation of energies
- _Ignores electron repulsion_ and _spin effects_
	- Effectively the [[Atomic and molecular physics#The H2+ ion|H2+ ion]]
	- With repulsion and spin, [[Atomic and molecular physics#The H2 molecule|numerical methods]] are required 

- Denote the states by:
$$\ket{a}=\phi(\boldsymbol{r}-\boldsymbol{R}_{a}) \hspace{1.5cm}\ket{b}=\phi(\boldsymbol{r}-\boldsymbol{R}_{b})  $$
- Find energy eigenfunctions in the subspace _spanned_ by basis functions:
	- Assume that they are _orthonormal_
$$\ket{\psi}=\alpha \ket{a}+\beta \ket{b}   $$
- By taking the inner product with $\braket{ a}$ and $\bra{b}$, and denoting the matrix elements of the _Hamiltonian_ as $H_{aa}, H_{bb}, H_{ab}, H_{ba}=H_{ab}^{*}$
$\begin{vmatrix}H_{aa}-E&H_{ab} \\ H_{ab}^{*}&H_{bb}-E\end{vmatrix}=0$

- The _energy eigenvalues_:
$$\displaylines{E=\frac{H_{aa}+H_{bb}}{2}\pm \frac{\Delta E}{2} \\ \frac{\Delta E}{2}=\sqrt{ \left( \frac{H_{aa}-H_{bb}}{2} \right)^{2}+ | H_{ab}|^{2}  }}$$
- If $H_{aa}\approx H_{bb}$, then $\Delta E/2=|H_{ab}|$, and there is _covalent bonding_

- If $H_{aa}\gg H_{bb}$ or vice versa, $E=H_{aa}$ or $H_{bb}$, and $H_{ab}$ is _irrelevant_, giving _ionic bonding_
	- The electrons are _localised_

## Covalent and ionic semiconductors
- With the $s$ electrons, _molecules_ are formed first to then give a _weakly (covalently) bound molecular solid_
	- $s$ orbitals are _spherical_
- With $p$ and $d$ electrons, bonds are _directional_
	- Example: $sp^{3}$ in carbon gives _tetrahedral bonding_, as the hybrids point along $(111),(\bar{1}\bar{1}1),(\bar{1}1\bar{1}),(1\bar{1}\bar{1})$

- _Binary compounds_: GaAs and ZnS
- _Zinc blende_ structure: tetrahedral with alternating atoms
- Partly ionic, partly covalent

- Hexagonal structure with ocal tetrahedral network: _wurtzite_

## Metals
- _Bands_ form from _atomic orbitals_
- They are typically _partially filled_ and _lowers_ energy in general
	- A _generalisation_ of the covalent bond to a _giant structure_
	- It is _isotropic_, like the van der Waals force
![[Covalent vs metallic.png]]
- Electrons are _delocalised_ to minimise kinetic energy
	- Gives _high conductivity_

- Atoms are _close packed_ to _maximise_ electron wave-function overlap while also _reducing Coulomb repulsion_ by keeping the _atomic cores_ far apart
	- Closed packed structures: _hexagonal_ close packing or _face-centred cubic_
	- Giving _high coordination numbers_ $\approx 10-12$

- [[#Electrostatic screening|Screening]] by conduction electrons have order of $\approx 1\text{ Å}$

- Within a _row_ in the periodic table, as the _ion core potential_ grows and _density_ increases, structures _cross over_ to covalent semiconductors, then _insulating_ molecular structures
- For _transition metals_, $d$ electrons are more localised, and give _spin polarised_ materials, leading to _magnetism_

# Lattices
- An _ideal crystal_ consists of an _infinite repetition_ of some structural _unit_ in _space_
- The _repeating structure_ is known as the _lattice_

- The _group_ of atoms repeated is the _basis_
	- Can be a _single atom_, or some _group_ of atoms, or some _polymer_

- A lattice is defined by the _primitive translation vectors_ $\boldsymbol{a}_{i}, i=1,2,3$
- Form an arbitrary _lattice translation_:
$$\boldsymbol{T}=\sum$$
 - The _atomic arrangement_ looks the _same_ from _equivalent points_ in the crystal:
$$\boldsymbol{r}_{i}$$

- Bravais lattice
- Unit cell

- The _Wigner-Seitz cell_ is the _region in real space_ around some _lattice point_, which is _closer to that point than any other lattice point_
	- _Smallest volume_ enclosed by _perpendicular bisectors_ to all other neighbours

- The _first Brillouin zone_ is the _Wigner-Seitz cell_ of the _reciprocal lattice_

- The _symmetry operations_ that map a lattice _onto itself_ form a _space group_
- Symmetry operations that _keeps one point fixed_ give a _point group_
	- Reflections, inversions, rotations
- There are _seven point groups, and 14 space groups_ for Bravais lattices

- General crystal structure

## Crystal planes
- _Planes_ are labelled by the _coordinates where it cut the axes_:
$$\{\boldsymbol{r}_{i}\}=$$
- $(hkl)$ denotes planes that _cut_ the axes at
- Therefore, $xh=yk=zl=$
- A _zero_ indicates that the plane is _parallel_ to that axis

- $(hkl)$ is known as the _index_ of the plane
- A _set_ of planes equivalent _by symmetry_ are denoted by $\{hkl\}$
	- Example: $\{100\}$ for a cubic crystal has planes $(100),(010),(001),(\bar{1}00),(0\bar{1}0),(00\bar{1})$

# The reciprocal lattice
- Arises from the _scattering_ of waves by crystals
	- _Generalise_ Fraunhofer diffraction from a grating
- Consider the scattering of a _plane wave_ off a _basis_

## Scattering from a lattice
- The _incoming wave_ $\boldsymbol{k}_{0}$ incident on a _potential_ centred on $\boldsymbol{R}_{i}$
- For _large distances_, the scattered wave is _circular_
- The _scalar field_:
$$\psi \propto \exp[i\boldsymbol{k}_{0}\cdot(\boldsymbol{r}-\boldsymbol{R}_{i})]+cf_{0} \frac{\exp[ik_{0}|\boldsymbol{r}-\boldsymbol{R}_{i}]}{}$$
- The _angular dependence_ from the _basis_ is determined by the _form factor_ $f_{0}$
	- Depends on scattering _angle_, type of atom, and their arrangement
- The _total scattered intensity_ determined by $c$ is assumed _small_

- At a _large distance_ from the scattering centre:
$$k_{0}\left| \boldsymbol{r}- \right| $$
- Here, $\boldsymbol{k}$ is the _scattered wave-vector_ $\boldsymbol{k}\equiv k_{0}\boldsymbol{r}/r$
- The _momentum transferred_ is $\boldsymbol{q}=\boldsymbol{k}-\boldsymbol{k}_{0}$
- The wave-form is then:
$$\psi \propto \exp[-i]\left[  \right]  $$
- The _effective scattering amplitude_ is:
$$f(\theta)=cf_{0}\exp(-i\boldsymbol{q}\cdot \boldsymbol{R}_{i})$$
- _Sum over all identical lattice sites_ gives the _scattering amplitude of the lattice_
	- _Multiply_ each term by the _phase of the incoming wave_ $\exp$
	- _Cancels out_ the pre-factor
- The [[Scattering#Differential cross-section|differential cross-section]]:
$$\frac{d\sigma}{d\Omega}=|f(\theta)|^{2}=\left| cf_{0}\sum_{i}  \right|^{2} $$
- The addition _cancels out all phases_, unless the _Bragg condition_ is satisfied:
$$\boldsymbol{q}\cdot \boldsymbol{R}_{i}=2\pi m_{i}$$
- In this case, all the scattered waves _constructively interfere_ to give a clear diffracted beam

## Diffraction conditions
- The vectors $\boldsymbol{q}\equiv\boldsymbol{G}$ satisfying the Bragg condition form a _reciprocal lattice_:
	$$\boldsymbol{G}\cdot \boldsymbol{R}_{i}=2\pi m_{i}$$
	- A _linear combination_ leads to another vector satisfying the Bragg condition

- The _primitive vectors_ of the reciprocal lattice, in terms of _real space_ lattice vectors:
$$\boldsymbol{b}_{1}=2\pi \frac{\boldsymbol{a}_{2}\times \boldsymbol{a}_{3}}{\boldsymbol{a}_{1}\cdot(\boldsymbol{a}_{2}\times \boldsymbol{a}_{3})}$$

- For _elastic scattering_, $|\boldsymbol{k}|=|\boldsymbol{k}_{0}|$
- This, combined with the _Bragg condition_, dictates:
$$\boldsymbol{k}_{0}\cdot \frac{\boldsymbol{G}}{2}=\left( \frac{\boldsymbol{G}}{2} \right)^{2}$$
- This defines a _plane_ perpendicular to $\boldsymbol{G}$ which _intersects_ $\boldsymbol{G}$ at its _midpoint_, or its _perpendicular bisectors_

- The _set of all such planes_ defines the incident wave-vectors $\boldsymbol{k}_{0}$ that _satisfy the Bragg condition_
- The _Ewald construction_ in reciprocal space:
![[Ewald construction.png]]
- For a _given_ $\boldsymbol{k}_{0}$, give it an origin $a$ such that it _ends on a reciprocal lattice_
- Draw a _sphere_ of radius $|\boldsymbol{k}_{0}|$ about $a$
- If the sphere _intersects_ any _other_ reciprocal lattice point, a _diffracted beam forms_ with $\boldsymbol{k}$ going from $a$ to the intersection
- $a$ lies on the _perpendicular bisector_ of $\boldsymbol{G}$

- $\theta$ is the _Bragg angle_, giving:
$$2|\boldsymbol{k}|\sin\theta=|\boldsymbol{G}|$$
- This is the _von Laue condition_

- The _spacing between parallel lattice planes_ in _real space_, perpendicular to $\boldsymbol{G}=$, is given by:
$$d(hkl)=\frac{2\pi}{|\boldsymbol{G}|}$$
- Then given $|\boldsymbol{k}|=2\pi/\lambda$:
$$2d(hkl)\sin\theta=\lambda$$
- Here, $\theta$ is the _angle_ between the _incident beam_ and the _crystal planes_, being _half_ the angle of deflection
- The _indices_ defining a crystal plane may contain a _common factor_ $n$, generalising the equation to:
$$2d\sin\theta=n\lambda$$

- For a film of _thickness_ $t$ on some _substrate_, the _angular spacing_ between diffraction peaks $\Delta\theta$ is given by:
$$2t\cos\theta \Delta\theta=\lambda$$

## Diffraction and Brillouin zones
- The _set_ of reciprocal space planes _satisfying the Bragg condition_ (Bragg planes) can be _constructed_ from the _perpendicular bisectors_ of $\boldsymbol{G}$
- These planes will _divide_ reciprocal space up into _cells_
	- Voronoi decomposition
- The cell _closest to origin_ is the _first Brillouin zone_
- The $n$th Brillouin zone consists of all fragments _exterior_ to the $(n-1)$th planes and _interior_ to the $n$th planes

- The _first Brillouin zone_ is deduced to be the _Wigner-Seitz cell of the reciprocal lattice_
- The _volume_ of each Brillouin zone is equal to the _volume of the primitive unit cell_ of the _reciprocal lattice_
- Given the _real space volume_ $\Omega _\text{cell}$ of the primitive unit cell, the BZ volume is:
$$V_\text{BZ}=\frac{(2\pi)^{3}}{\Omega _\text{cell}}$$

- Example: fcc lattice
	- Left: real space with primitive lattice vectors
	- Right: reciprocal space with 1st BZ
![[fcc lattice.png]]

## Born-von Karman boundary conditions
- Any _wave function_ describing particles in lattices should reflect the _translational symmetry_ of the lattice
- This is covered by _Born-von Karman boundary conditions_

- Consider a _volume_ with $N_{j}$ _primitive unit cells_ in the $j-$th direction, with $N=N_{1}N_{2}N_{3}$ cells in _total_
- For a _plane wave_:
$$\psi(\boldsymbol{r})=\exp[i(\boldsymbol{k}\cdot \boldsymbol{r}-\omega t)]$$
- This should be subject to the oundary condition:
$$\psi(\boldsymbol{r}+N_{j}\boldsymbol{a}_{j})=\psi(\boldsymbol{r})$$
- From the boundary condition, the _allowed wave-vectors_ are:
$$\boldsymbol{k}=\sum_{j=1}^{3}\frac{m_{j}}{N_{j}}\boldsymbol{b}_{j}$$
- The _k-space volume_ occupied by _one state_ is:
$$\frac{1}{N}\boldsymbol{b}_{1}\cdot(\boldsymbol{b}_{2}\times \boldsymbol{b}_{3})$$
- Hence, each _Brillouin zone_ contains $N$ $k-$states

# One-dimensional models of phonons

## Identical atoms
- Simplest model: row of _identical atoms_
	![[Identical atoms phonons.png]]
	- Inter-atomic spacing $a$
	- Atomic mass $m$
	- Spring constant $K$

- Displacement of the $n$th atom $u_{n}$ obeys:
$$m\frac{\partial^{2}u_{n}}{\partial t^{2}}=K(u_{n+1}-u_{n})-K(u_{n}-u_{n-1})$$
- _Harmonic solution_ of wave-vector $q$:
$$u_{n}(t)=u_{0}\cos(qr_{n}-\omega(q)t)$$
- This gives:
$$\omega(q)=2\sqrt{ \frac{K}{m} }\left| \sin\left( \frac{qa}{2} \right) \right| $$
- It is _periodic_ in $q$ with period $2\pi/a$
![[Monoatomic chain dispersion.png]]

- The _long wavelength modes_ $q\to 0$ gives _linear dispersion_
	- Same for a _wire_ with tension $Ka$ and _density_ $m/a$
	- They are _compressive waves_ with group and phase velocity $\sqrt{ K/m }$ 

- These waves behave as _sound waves_, and are an _acoustic mode_

- For $qa=0$ and $qa=2\pi$, neighbouring atoms are _in phase_
	- Wavelength is effectively $a$
- For $qa=\pi$, they move in _antiphase_

- One can consider only the _range_:
$$-\frac{\pi}{a}<q<\frac{\pi}{a}$$
- Values _outside_ are equivalent to the value at $q-2n\pi$
	- Analagous to _aliasing_
- This corresponds to the _first Brillouin zone_
![[Phonon aliasing.png]]

## Two types of atoms
- Consider _two different types_ of atoms in a unit cell, giving different masses and spring constants:
![[Diatomic chain.png]]
- The equations of motion:
$$\begin{align} m_{A}\frac{\partial^{2}u_{n,A}}{\partial t^{2}}&= K(u_{n,B}-u_{n,A})-K'(u_{n,A}-u_{n-1,B}) \\ m_{B} \frac{\partial^{2}u_{n,B}}{\partial t^{2}}&=K'(u_{n+1,A}-u_{n,B})-K(u_{n,B}-u_{n,A})\end{align}$$

### Diatomic molecules
- The limit of _same mass_ $(m_{A}=m_{B})$, with $K\gg K'$, simulating a _chain of strongly bound diatomics_
	- Let the spacing _between molecules_ be $a_{2}$

- Then each molecule has a mode where _each atom oscillates out of phase_
	- The coordinate $u_\text{opt}(q=0)=u_{A}-u_{B}$ undergoes oscillation

- _Branches_ to the dispersion curve
	- Acoustic branch: for low frequency, it vanishes _linearly_ with $q$
	- Optical branch: finite frequency as $q\to 0$, often _interacts with light_
- The optical branch frequency is _largely independent of_ $q$
![[Diatomic dispersion curve.png|500]]
### Same springs, different masses
- In the limit of the _same spring constant_
- With lattice constant $a$, travelling wave solutions lead to:
$$\begin{align}u_{n,A}&= \\ u_{n,B}&=\end{align}$$

- Limiting results:
![[Acoustic optical phonons.png|500]]
- The branches _split_ such that there are _no solutions_ between $\sqrt{ 2K/m_{A} }$ or $\sqrt{ 2K/m_{B} }$
- Atomic displacements:
![[Acoustic optical displacements.png]]

# Real phonons

## 3 dimensions
- 3 dimensions: _transverse_ and _longitudinal_ modes
- For a solid with $m$ atoms per unit cell:
	- $3$ acoustic modes (2 transverse, 3 longitudinal)
	- $3(m-1)$ optical modes

- Plot along a _path in reciprocal space_
![[Ge phonon dispersion.png|600]]

## Inelastic neutron scattering
- Inelastic neutron scattering: neutron _transfers_ energy and momentum _to phonons_
$$\boldsymbol{Q}=\boldsymbol{k}'-\boldsymbol{k}+\boldsymbol{G}$$
- Here, $\boldsymbol{G}$ is _any reciprocal lattice vector_
- Measurement: outgoing neutron energy:
$$E(\boldsymbol{Q})=\varepsilon(\boldsymbol{k}')-\varepsilon(\boldsymbol{k})$$

![[Inelastic neutron scattering.png]]

## Density of states and heat capacity
- For a _1D chain_ of $N$ atoms, there must be $N$ _modes_
- The allowed _density of states_, with _periodic boundary conditions_, are then:
	- There is a _maximum momentum_ on the _Brullouin zone boundary_ (due to the _discreteness_ of the atomic chain)
$$k_{n}=\frac{2\pi}{L}n \hspace{1cm}n=\left(-\frac{N}{2}+1,-\frac{N}{2}+2,\dots,\frac{N}{2}\right]$$
- Here, $a=L/N$ and $-\pi/a<k<\pi/a$
- In 3 dimensions, each _branch_ has $N=L^{3}/\Omega _\text{cell}$ states
- The volume for each $k-$state is $(2\pi)^{3}/L^{3}$

### Einstein and Debye models
- The _Einstein model_ assumes a _flat dispersion_ $\omega(\boldsymbol{k})=\omega_{0}$
- The _density of states_ per branch is then:
$$D_{E}(\omega)=N\delta(\omega-\omega_{0})$$
- This is suitable for _optical branches_

- For _acoustic modes_, with _linear dispersion_, use $\omega=vk$
- The density of states in the _Debye model_:
$$D_{D}(\omega)=\frac{4\pi k^{2}}{(2\pi/L)^{3}} \frac{dk}{d\omega}=\frac{V\omega^{2}}{2\pi^{2}v^{3}}$$
- This _fails at the zone boundary_, hence implement a _cut off_ at the Debye frequency
- _Count_ the number of states and cut off at $N$:
$$\int _{0}^{\omega_{D}}D_{D}(\omega) \, d\omega=N \implies \omega_{D}^{3}=6\pi^{2}v^{3} \frac{N}{V}$$
- _Replacing_ the Brillouin zone with a _sphere_ of radius $k_{D}=\omega_{D}/v$

### Lattice specific heat
- Phonons obey the [[Advanced statistical mechanics#The Bose gas|Bose-Einstein distribution]]
- As their _number is not conserved_, $\mu=0$:
$$n(\omega)=\frac{1}{\exp(\hbar\omega/k_{B}T)-1}$$
- For $k_{B}T<\hbar\omega$, $n(\omega) \to \exp(-\hbar\omega/k_{B}T)$
- For $k_{B}T>\hbar\omega$, $n(\omega)\to k_{B}T/\hbar\omega$

- The _internal energy_ in the _Einstein_ model:
$$U_{E}=\int  D_{E}(\omega)n(\omega)\hbar\omega \, d\omega =\frac{\hbar\omega_{0}}{\exp(\hbar\omega_{0}/k_{B}T)-1}$$
- The _heat capacity_:
$$C_{V}=\left( \frac{\partial U}{\partial T} \right)_{V}=Nk_{B}\left( \frac{\hbar\omega_{0}}{k_{B}T} \right)^{2} \frac{\exp(\hbar\omega_{0}/k_{B}T)}{[\exp(\hbar\omega_{0}/k_{B}T)-1]^{2}}$$
- At _low temperatures_, this varies as $\exp(-\hbar\omega_{0}/k_{B}T)$
- It _saturates_ above the _characteristic temperature_ $\theta_{E}=\hbar\omega_{0}/k_{B}$
- It satisfies the _Dulong-Petit law_ such that $C_{V}(T>\theta_{E}) \to Nk_{B}$

- At _low temperatures_, the contribution of _optical modes_ is _small_
- In the _Debye model_:
$$U_{D}=\int D_{D}(\omega)n(\omega)\hbar\omega \, d\omega=\int _{0}^{\omega_{D}} \frac{V\omega^{2}}{2\pi^{2}v^{3}} \frac{\hbar\omega}{\exp(\hbar\omega/k_{B}T)-1} \, d\omega  $$
- Define the _Debye temperature_:
$$\theta_{D}=\frac{\hbar\omega_{D}}{k_{B}}$$

- Debye temperature
- Substitution: $x=\hbar\omega/k_{B}T$
- Factor of $3$ for different modes

- Internal energy:
$$U_{D}=$$
- Heat capacity:
$$C_{V}=$$
- For $T\gg\theta_{D}$, $x\to 0$, giving $C_{V}=3Nk_{B}$
- Low temperature: $\propto T^{3}$

- Phonons and electrons:
$$C_{V}=$$
- Straight line plot

- At _low temperatures_, it is difficult to _thermally excite_ optical modes, giving the _Einstein model_ a _low heat capacity_
- Real density of states
	- _Branches_ of the phonon spectrum
	- van Hove singularities: the dispersion is _flat_, giving an _infinite_ density of states

# Heat capacity and conductivity
- For _heat flux_ $\boldsymbol{J}_{q}$ (energy per unit area per unit time)
$$\boldsymbol{J}_{q}=-\kappa \nabla T$$
- Kinetic theory:
$$\kappa=\frac{1}{3}C_{B}lv=\frac{1}{3}C_{V}v^{2}\tau$$
- $v$: phonon velocity
- $l=v\tau$: mean free path
- $\tau$: scattering time

- $v$ is the _speed of sound_, which is _almost constant_
- Scattering processes:
	- Normal and Umklapp scattering
	- Point defects
	- Sample boundaries
	- Crystal dislocations
$$\tau^{-1}=\sum \tau^{-1}=$$
- Low temperature: large $l$, $\tau$ given by _sample boundaries_ (constant w.r.t. $\tau$), giving $\kappa \propto T^{3}$
- Middle range: $\kappa$ often _peaks_, dominated by _impurity scattering_
- Beyond $\theta_{D}$, phonon _numbers_ increase, Umklapp scattering becomes important, $\kappa$ _decreases_ rapidly

![[Thermal conductivities.png]]

# Bloch's Theorem
- Electrons experience a _periodic potential_ in a lattice
- Find a set of _plane wave solutions_ for electron wave-functions, satisfying _periodic boundary conditions_
- Hamiltonian with a _periodic potential_
$$\hat{H}\ket{\psi}=\left( \frac{\hat{p}^{2}}{2m}+V \right)\ket{\psi }=\ket{\psi}   $$

## Fourier expansion of the potential
- $V(\boldsymbol{r})$ has the periodicity _of the lattice_:
$$V(\boldsymbol{r})=\sum_{\boldsymbol{G}}V_{\boldsymbol{G}}\exp(i\boldsymbol{G}\cdot \boldsymbol{r})$$
- _Fourier components_:
$$V_{\boldsymbol{G}}=\frac{1}{V_\text{cell}}\int _\text{cell}V(\boldsymbol{r})\exp(-i\boldsymbol{G}\cdot \boldsymbol{r}) \, d^{3}\boldsymbol{r} $$
- As the potential is _real_:
$$V_{\boldsymbol{G}}^{*}=V_{-\boldsymbol{G}}$$
- For $\boldsymbol{G}=0$, the Fourier component is the _average of the potential_, which can be set to _zero_
- The eigenstate can be _constructed by plane wave states_:
$$\ket{\psi}=\sum_{\boldsymbol{k}}c_{\boldsymbol{k}}\ket{\boldsymbol{k}}=\sum_{\boldsymbol{k}}c_{\boldsymbol{k}}\exp(i\boldsymbol{k}\cdot \boldsymbol{r})  $$
- Substituting into the Schrodinger equation:
	- $E_{k}^{0}$ is the _free particle energy_ $\hbar^{2}k^{2}/(2m)$
$$\sum_{\boldsymbol{k}}E_{\boldsymbol{k}}^{0}c_{\boldsymbol{k}}\exp(i\boldsymbol{k}\cdot \boldsymbol{r})+\sum_{\boldsymbol{G}}\sum_{\boldsymbol{k}}V_{\boldsymbol{G}}c_{\boldsymbol{k}}\exp[i(\boldsymbol{k}+\boldsymbol{G})\cdot \boldsymbol{r}]=E\sum_{\boldsymbol{k}}c_{\boldsymbol{k}}\exp(i\boldsymbol{k}\cdot \boldsymbol{r})$$
- The _double sum_ in the potential term, with _relabelling_ the sum:
$$V(\boldsymbol{r})\ket{\psi}= \sum_{\boldsymbol{G}}\sum_{\boldsymbol{k}}V_{\boldsymbol{G}}c_{\boldsymbol{k}-\boldsymbol{G}}\exp(i\boldsymbol{k}\cdot \boldsymbol{r})$$

- As the eigenfunctions are _orthogonal_, the eigenvalue equation is:
$$(E_{\boldsymbol{k}}^{0}-E)c_{\boldsymbol{k}}+\sum_{\boldsymbol{G}}V_{\boldsymbol{G}}c_{\boldsymbol{k}-\boldsymbol{G}}=0$$
- $\boldsymbol{k}$ is _anywhere in the reciprocal lattice_
- Write wavevector $\boldsymbol{q}\equiv \boldsymbol{k}+\boldsymbol{G}'$, such that it is _in the first Brillouin zone_
- Then writing $\boldsymbol{G}''=\boldsymbol{G}+\boldsymbol{G}'$:
$$\left[ \frac{\hbar^{2}}{2m}(\boldsymbol{q}-\boldsymbol{G}')^{2}-E \right]c_{\boldsymbol{q}-\boldsymbol{G}'}+\sum_{\boldsymbol{G}''}V_{\boldsymbol{G}''-\boldsymbol{G}'}c_{\boldsymbol{q}-\boldsymbol{G}''}=0 $$
- This _specifies_ the set of coefficients $c_{\boldsymbol{k}}$

- Hence, for _each distinct value_ of $\boldsymbol{q}$ in the 1st BZ, there is a _corresponding wave-function_
$$\psi_{\boldsymbol{q}}(\boldsymbol{r})=\sum_{\boldsymbol{G}}c_{\boldsymbol{q}-\boldsymbol{G}}\exp[i(\boldsymbol{q}-\boldsymbol{G})\cdot \boldsymbol{r}] $$
- _Bloch's Theorem_:
$$\psi_{\boldsymbol{q}}(\boldsymbol{r})=\exp(i\boldsymbol{q}\cdot \boldsymbol{r})\sum_{\boldsymbol{G}}c_{\boldsymbol{q}-\boldsymbol{G}}\exp(-i\boldsymbol{G}\cdot \boldsymbol{r})\equiv \exp(i\boldsymbol{q}\cdot \boldsymbol{r})u_{j,\boldsymbol{q}}(\boldsymbol{r})$$
- Here, $u$ _has the same periodicity as the lattice_
- $j$ is the _band index_

- In a solid, _eigenstates of the one-electron Hamiltonian_ can be written as a _plane wave_ multiplied by a _function_ with the _periodicity of the Bravais lattice_

## From symmetry
- Consider the _translation operator_:
$$\hat{T}_{\boldsymbol{R}}f(\boldsymbol{r})=f(\boldsymbol{r}+\boldsymbol{R})$$
- As the Hamiltonian is _also periodic_, it _commutes_ with $\hat{T}_{\boldsymbol{R}}$:
$$\left[ \hat{T}_{\boldsymbol{R}},\hat{H} \right]=0$$
- Therefore, there must be _simultaneous eigenstates_

- The eigenstates of $\hat{T}$ are the _plane wave states_ $\ket{\boldsymbol{k}}$ with eigenvalue $\exp(i\boldsymbol{k}\cdot \boldsymbol{a})$
- The _common eigenstates_ are:
$$\psi(\boldsymbol{r}+\boldsymbol{a})=\exp(i\boldsymbol{k}\cdot \boldsymbol{a})\psi(\boldsymbol{r})$$
- This is an _equivalent form_ of Bloch's Theorem
## Bloch states
- Energy eigenstates obey:
$$\hat{H}\psi=\left[ -\frac{\hbar^{2}}{2m}\nabla^{2}+V \right]\psi=E\psi$$
- Periodic potential obeys $V(\boldsymbol{r}+\boldsymbol{R})=V(\boldsymbol{r})$ for all _lattice vectors_ $\boldsymbol{R}$

- Choose wavefunction $\psi_{\boldsymbol{k}}^{(n)}$ such that
$$\psi_{\boldsymbol{k}}^{(n)}(\boldsymbol{r})=\exp(i\boldsymbol{k}\cdot \boldsymbol{r})u_{\boldsymbol{k}}^{(n)}(\boldsymbol{r}) \hspace{1.5cm}u_{\boldsymbol{k}}^{(n)}(\boldsymbol{r}+\boldsymbol{R})=u_{\boldsymbol{k}}^{(n)}(\boldsymbol{r})$$
- Here, $n$ is the _band index_, as there may be _several distict eigenstates_ of $\hat{H}$ with the _same symmetry label_ $\boldsymbol{k}$

- Evaluating the wave function at _two different lattice points_:
$$\psi_{\boldsymbol{k}}^{(n)}(\boldsymbol{r}+\boldsymbol{R})$$
- If $\boldsymbol{k}\to \boldsymbol{k}+\boldsymbol{G}$, one gets the _same wave-function_
- $\boldsymbol{k}$ can always be _mapped back to the 1st BZ_

- From the _periodicity_ of $u$, _relabel_ a Bloch state $\boldsymbol{k}$ with the wave-vector $\boldsymbol{k}-\boldsymbol{g}$, introducing a _different periodic function_:
$$\displaylines{u_{\boldsymbol{k}-\boldsymbol{g}}^{(n)}=\exp(i\boldsymbol{g}\cdot \boldsymbol{r})u_{\boldsymbol{k}}^{(m)} \\ \psi_{\boldsymbol{k}}^{(n)}(\boldsymbol{r})=\psi_{\boldsymbol{k}-\boldsymbol{g}}^{(m)}(\boldsymbol{r})}$$
- $n$ and $m$ label different _bands_
- There are _two different states_ labelled with the _same_ $\boldsymbol{k}$ but belonging to _different bands_:
$$\psi_{\boldsymbol{k}}^{(m)}(\boldsymbol{r})=\exp(-i\boldsymbol{g}\cdot \boldsymbol{r})\psi_{\boldsymbol{k}}^{(n)}(\boldsymbol{r})$$
- For every state labelled with a $\boldsymbol{k}$ _outside the 1st BZ_, there is an _identical state_ with $\boldsymbol{q}=\boldsymbol{k}-\boldsymbol{G}$ which is _inside_

- As a _corollary_, _any_ function that relies on the wave-function are _also periodic_

# Nearly-free electron approximation
- Find _approximate_ single-electron states in a _periodic potential_ by _hybridising nearly degenerate plane wave states_
- Plane wave expansion (from [[#Fourier expansion of the potential|derivation of Bloch's Theorem]])
$$\ket{\psi_{\boldsymbol{k}}}=\sum_{\boldsymbol{G}}c_{\boldsymbol{k}-\boldsymbol{G}}\ket{\boldsymbol{k}-\boldsymbol{G}}  $$
- If the lattice potential is _weak_ compared to kinetic energy, the eigenstates are simply _constructed_ from $\boldsymbol{k}$ with a _small contribution_ from states $\ket{\boldsymbol{k}-\boldsymbol{G}}$

- Use [[Time-Independent Approximation Methods#Second-order perturbation theory|second order perturbation theory]] to calculate the _degree of mixture_ of the harmonic states
- Both the _energy shift_ $\Delta E_{\boldsymbol{k}}$ and the _admixture of states_ are dominated by _nearly degenerate states_:
$$\Delta E_{\boldsymbol{k}}=\frac{|V_{\boldsymbol{G}}|^{2}}{E_{\boldsymbol{k}}^{0}-E_{\boldsymbol{k}-\boldsymbol{G}}^{0}}$$
- From eigenvalue equation:
$$(E_{\boldsymbol{k}}^{0}-E)c_{\boldsymbol{k}}+\sum_{\boldsymbol{G}}V_{\boldsymbol{G}}c_{\boldsymbol{k}-\boldsymbol{G}}=0$$
- This _restricts_ the choice of nearly degenerate states to:
$$E_{\boldsymbol{k}}^{0}\approx E_{\boldsymbol{k}-\boldsymbol{G}}^{0}$$
## 1D chain
- Nearest state

- Hermitian operator

- Set $V_{0}=0$
$$\begin{pmatrix}E_{\boldsymbol{k}}^{0}-E & V_{\boldsymbol{G}} \\ V_{-\boldsymbol{G}} & E_{\boldsymbol{k}-\boldsymbol{G}}^{0}-E\end{pmatrix}\begin{pmatrix}c_{\boldsymbol{k}} \\ c_{\boldsymbol{k}-\boldsymbol{G}}\end{pmatrix}=\begin{pmatrix}
0\\0\end{pmatrix}$$
- Solution:
$$E\approx \frac{1}{2}(E_{\boldsymbol{k}}^{0}+E_{\boldsymbol{k}-\boldsymbol{G}}^{0})\pm |V_{\boldsymbol{G}}|$$
- There is a _symmetrical splitting_ of levels about the _free-electron value_, where the two bands _cross_ close to the BZ boundary
- The degeneracy is _broken_ due to the _perturbation_ of $V_{\boldsymbol{G}}$

- At the boundary, they are formed by the _sum/difference_ of the unperturbed states $\ket{\boldsymbol{k}}$ and $\ket{\boldsymbol{k}-\boldsymbol{G}}$

- If the potential is zero:
$$E_{\boldsymbol{k}}^{0}=\frac{\hbar^{2}}{2m}|\boldsymbol{k}|^{2}$$
- At the _BZ boundary_, $\partial E/\partial k=0$
	- Makes it such that there is _no discontinuity_ in the _gradient_ of the energy
	- In general, $\nabla_{\boldsymbol{k}}E$ is _parallel to the Bragg plane_
	- So, _constant energy_ surfaces are always _perpendicular_ to the BZ boundary
	- There, the _hybridisation_ and _band distortions_ are the _strongest_

- For a purely _sinosoidal_ potential

- $s-$type and $p-$type
![[s p type Bloch waves.png|500]]


- In 3D, energy contours are _spherical_ but begin to _distort_ near the BZ boundary

- Add more figures

# Tight binding method
- It is the technique of _linear combination of atomic orbitals_

## Diatomic molecule
- Use a basis of _one orbital per atom_
- For _identical atoms_, the full Hamiltonian is:
$$\hat{H}=\hat{T}+\hat{V}_{a}+\hat{V}_{b}$$
- The _basis set_ consists of the _atomic orbitals_ $\ket{a}$ and $\ket{b}$:
$$\displaylines{\ket{\psi}=\alpha \ket{a}+\beta \ket{b} \\ \left( \hat{T}+\hat{V}_{a} \right)\ket{a}=E_{0}\ket{a}\hspace{1.5cm}\left( \hat{T}+\hat{V}_{b} \right)\ket{b}=E_{0}\ket{b}    }$$
- One then gets the _simultaneous equations_
	- _Ignore_ the overlap $\braket{ a | b }$
$$\begin{pmatrix}\tilde{E}_{0}-E & t \\ t^{*} & \tilde{E}_{0}-E\end{pmatrix}\begin{pmatrix}
\alpha \\ \beta\end{pmatrix}=\begin{pmatrix}
0\\0\end{pmatrix}$$
- The _shift in energy_ due to the _crystal field_ of the other atom:
$$\tilde{E}_{0}=H_{aa}=\braket{ a|\hat{T}+\hat{V}_{a}+\hat{V}_{b} | a }=E_{0}+ \braket{ a|\hat{V}_{b} | a }  $$
- $t$ is the _hopping element_ of the molecule:
$$t=H_{ab}=\braket{ a| \hat{T}+\hat{V}_{a}+\hat{V}_{b} | b } $$

- For $t<0$, the new eigenstates are the _constructive_ and _destructive_ combinations:
$$\ket{\psi}=\frac{1}{\sqrt{ 2 }}[\ket{a}\pm \ket{b}  ]\hspace{1cm} E=\tilde{E}_{0}\mp |t| $$
- For the _lower energy_ (bonding) state, there is _higher electron density_ between the atoms
- For the _higher energy_ (antibonding) state, there is a _node_ between the atoms

- The _sign_ of $t$ depends on the _symmetry_ of the orbitals
	- For $s$ states, with an _attractive potential_, $t<0$
## Linear chain
- Generalise to a _chain_ of atoms, with _periodic boundary conditions_
- Similar behaviour to diatomics, where _initially degenerate_ energy levels start to _split apart_ as energy levels get closer
![[20 atom ring energy levels.png|450]]
- From Bloch's theorem, only allowing _one orbital per unit cell_, the wavefunction must be of the form:
$$\ket{\psi}=\sum_{n}\exp(i\boldsymbol{k}\cdot \boldsymbol{R}_{n})\ket{n}  $$
- Here, $\boldsymbol{R}_{n}$ is the _position_ of atom $n$, and $\ket{n}$ is its wavefunction:
$$\braket{ \boldsymbol{r} | n }=\phi(\boldsymbol{r}-\boldsymbol{R}_{n}) $$

- Single atom vs full Hamiltonian

- Check that it _obeys Bloch's Theorem_

- _Neglect_ matrix elements which are _not from neighbouring orbitals_
- The remaining matrix elements:
$$\tilde{E}_{0}=\braket{ n|H | n }\hspace{1.5cm} t=t^{*}=\braket{ n|H |n+1  }  $$

- Derivation
$$E_{k}=\tilde{E}_{0}+2t\cos(ka)$$
- As there is only _one orbital per site_, there is a _single band_
	- Due to the _periodic boundary conditions_, the quantised wavenumbers give a _conserved number_ of orbitals

## Generalised LCAO method
- Extend the sum to _over all atoms in the 3D solid_:
$$\ket{\psi}=\sum_{n}\exp(i\boldsymbol{k}\cdot \boldsymbol{R}_{n})\ket{n}  $$
- Contributions to _hopping processes_ from _all directions_
- Example: the _simple cubic_ lattice
$$E_{\boldsymbol{k}}=\tilde{E}_{0}+2t\cos(k_{x}a)+2t\cos(k_{y}a)+2t\cos(k_{z}a)$$

### Multiple bands

## Comparison with nearly free electron model


## Psuedopotentials
- The nearly free electron and tight-binding models can have _parameters fit to experiment_

- _Semiconductors_ often have small band gaps
- Only a _few_ Fourier components are sufficient to determine _scattering_ of electrons from the atom
	- The _effective scattering potential_ is much _smaller_ than the _full atomic potential_
- This is known as the _pseudopotential_

- The _full_ Schrodinger equation gives both the _valence_ states are _core_ states
- The pseudopotential has the _valence states_ as the _lowest energy eigenstates_, completely _ignoring core states_

- The _true_ potential $V(r)$ matches the _true wavefunction_ $\Phi(r)$
	- True wavefunction tends to _oscillate_ near the core
- The _pseudopotential_ $V_{s}(r)$ has a matching _pseudo-wavefunction_ $\Phi_{s}(r)$
- When _far_ from the core, the pseudo-quantities match the _true result_
![[Pseudopotential.png|400]]

# General band structures
- Bloch's theorem, the NFE (Nearly Free Electron) model, and tight binding theory give _general features_ applicable to all crystalline materials

## Band gaps
- In the [[#Nearly-free electron approximation|NFE]], band _gaps_ arise due to _interference_ between _degenerate plane waves_
- It is a _splitting_ of the degeneracy due to scattering from the relevant _Fourier component_

- Requiring $E_{0}(\boldsymbol{k})=E_{0}(\boldsymbol{k}-\boldsymbol{G})$ for a _given_ $\boldsymbol{G}$:
$$|\boldsymbol{k}|^{2}=|\boldsymbol{k}-\boldsymbol{G}|^{2} \implies \boldsymbol{k}\cdot \frac{\boldsymbol{G}}{2}=\left|\frac{\boldsymbol{G}}{2}\right|^{2}$$
- This is simply the _Bragg condition_, describing the _boundary of a Brillouin zone_
	- Planes which _bisect_ $\boldsymbol{G}$

- Energy eigenstates form _discrete bands_ $E_{n}(\boldsymbol{k})$
	- _Continuous_ functions of $\boldsymbol{k}$ and labelled by band index $n$
	- _Periodic_ in the reciprocal lattice
- Bloch's theorem: eigenstates are always in the _form_:
$$\psi_{n\boldsymbol{k}}(\boldsymbol{r})=\exp(i\boldsymbol{k}\cdot \boldsymbol{r})u_{n\boldsymbol{k}}(\boldsymbol{r})$$

- $\hbar \boldsymbol{k}$ is the _crystal momentum_
- It enters _conservation laws_ for _scattering processes_
- It is a _label_ for electron momentum, not necessarily related to _actual momentum_
	- Can be related to physical momentum by adding $\boldsymbol{G}$
- Bloch states labelled by $\boldsymbol{k}$ are _not momentum eigenstates_

- Volume associated with each $\boldsymbol{k}$ state is simply $(2\pi)^{3}/V_\text{cell}$
- Within _each_ BZ, the number of $\boldsymbol{k}-$states allowed by periodic boundary conditions is the _number of unit cells_ in the crystal
	- Practically _continuous_
- Each $\boldsymbol{k}-$point has _two electrons_ due to spin

- One electron per unit cell: only _half_ the states are filled
- Two electrons per unit cell: first BZ is _filled_
- In general: 
	- if Fermi energy is in a _band gap_, the material is an _insulator_
	- if Fermi energy is in a _band_, the material is a _metal_

- If bands _overlap_, there are two or more _partially filled_ bands, and the material is a _metal_
- When energy due to _Coulomb repulsion_ between electrons is _larger than bandwidth_, the material is a _Mott insulator_
	- Spin-polarised band theory

## Metals
- For an _odd number_ of electrons per primitive cell, Fermi energy is _within a band_
- Therefore, _low-energy excitations_ are possible, and the solid is a _metal_

- For simple metals, the Fermi surface is _close to a free electron sphere_
	- Example: $\ce{ Na,Al }$
- In other cases, the Fermi surface can _meet the Brillouin zone boundary_
	- Example: $\ce{ Cu }$
![[Copper Fermi surface.png|400]]
- In some cases, bands are _cut_ by the Fermi energy, leading to a non-trivial _topology_

- Even with enough electrons to fill bands, bands can _overlap_
- The Fermi surface can then _intersect more than one band_
- It makes a pocket of electrons in one band, and makes _holes_ in another band
	- Example: $\ce{ Ca,Mg }$ are metals
	- _Semimetals_

- Example: $\ce{ Al }$
- FCC structure
- First BZ is _full_, valence electrons _spread_ into 2nd, 3rd, 4th BZ
![[Aluminium band structure.png]]
- This determines [[#Optical properties of insulators|reflectivity]] of the metal
- Optical transitions are _vertical_, and [[Time-dependent quantum mechanics#Fermi's Golden Rule|Fermi's Golden Rule]] states that both _initial_ and _final_ density of states influence the transition rate
- Reflectivity _dips_ for $1.5\,\text{eV}$ due to transitions between _parallel bands_
- Transitions above $1.5\,\text{eV}$ are possible, but _not parallel_, leading to a higher plateau in reflectivity

- Example: $\ce{ Cu }$
- The $3d$ bands are _tightly bound_, have high density of states, and are _full_
- The $4s$ bands are _free electron-like_, have lower density of states, and is _broader_ and _partially filled_
- Fermi surface is in the $4s$ band, completely above $3d$ band
- _Transitions_ are possible from $3d$ to $4s$
- _Threshold_ for transitions above $2\,\text{eV}$
- Keads to the _colour_ of the metal

## Semiconductors
- For an even number of electrons per unit cell, bands can be _filled_
- There is an _energy gap_ to the next empty states
- The system is a _semiconductor_ or _insulator_

- Example: $\ce{ Si }$ and $\ce{ GaAs }$
- Direct/indirect band gaps:

# Semiclassical electron dynamics
- Particles are treated as _wave packets_
- Given _band energy_ $\varepsilon(\boldsymbol{k})$, the time-dependent wave-function is:
$$\psi_{\boldsymbol{k}}\exp\left( -\frac{i\varepsilon(\boldsymbol{k})}{\hbar}t \right)$$

## Wavepackets and equations of motion
- Model electrons as _wave packets_ with group and phase velocity

### Group velocity and effective mass
- As it is a wavepacket, it moves with _group velocity_:
$$\dot{\boldsymbol{r}}=\boldsymbol{v}_{g}=\frac{1}{\hbar}\nabla_{\boldsymbol{k}}\varepsilon(\boldsymbol{k})$$
- The _rate of doing work_ is:
$$\frac{d\varepsilon}{dt}=\dot{\boldsymbol{k}}\cdot \nabla_{\boldsymbol{k}}\varepsilon=\hbar \dot{k}\cdot \boldsymbol{v}_{g}$$
- From this, the _force on the electron_ $\boldsymbol{F}$ is equal to $\hbar \,d\boldsymbol{k}/dt$
- This leads to the _equation of motion in an electromagnetic field_:
$$\hbar \dot{\boldsymbol{k}}=\boldsymbol{F}=-e(\boldsymbol{E}+\boldsymbol{v}_{g}\times \boldsymbol{B})=-e(\boldsymbol{E}+ \hbar^{-1}\nabla_{k}\varepsilon \times \boldsymbol{B})$$
- The _electric field_ will _shift_ the crystal momentum _towards the field direction_
- The _magnetic field_ moves $\boldsymbol{k}$ on a _surface of constant energy_

- From this, one gets that _all filled bands are inert_
	- Total current is obtained by _integrating_ $v_{g}$ over the BZ, giving 0 if the band is _filled_

- Consider the rate of chanege of velocity:
$$\frac{d\boldsymbol{v}_{g}}{dt}=\frac{1}{\hbar} \frac{d^{2}E}{dkdt}=\frac{1}{\hbar} \frac{d^{2}E}{dk^{2}} \frac{dk}{dt}=\frac{1}{\hbar^{2}} \frac{d^{2}E}{dk^{2}}\boldsymbol{F}$$
- From this, the _effective mass_ is:
$$m^{*}=\frac{\hbar^{2}}{d^{2}E/dk^{2}}$$

- In an _energy extremum_, one can _expand_ energy as:
$$E(\boldsymbol{k})\approx E_{0}+ \frac{\hbar^{2}}{2m^{*}}(\boldsymbol{k}-\boldsymbol{k}_{0})^{2}$$

- Linear tight-binding dispersion:
![[Group velocity and effective mass.png]]
- The effective mass can _diverge_ and _change sign_ near _turning points_

### Bloch oscillations
- For a 1D bandstructure, consider applying a _constant electric field_
	- Applied using a _DC voltage_
- Consider the [[#Linear chain|linear tight binding]] dispersion:
$$E=E_{0}-2t\cos(ka)$$
- The group velocity and effective mass:
$$v_{g}=\frac{2ta}{\hbar}\sin(ka)\hspace{1.5cm}m^{*}=\frac{\hbar^{2}}{2ta^{2}} \frac{1}{\cos(ka)}$$

- Start the state at the _energy minimum_ $k=0$, the wavenumber _evolves linearly_:
$$k(t)=-\frac{eE}{\hbar}t$$
- This gives _Bloch oscillations_:
$$v_{g}=-\frac{2ta}{\hbar}\sin\left( \frac{eEa}{\hbar}t \right)\hspace{1.5cm}m^{*}=\frac{\hbar^{2}}{2ta^{2}} \frac{1}{\cos(eEat/\hbar)}$$
- Typically, _scattering_ prevents Bloch oscillations from being observed
	- The momentum $\pi/a$ is _too high_ to accelerate to without scattering
	- One canu use an _artificial potential_ (Wannier-Stark ladder)

### Density of states
- Near the _maxima_ and _minima_, the dispersion is _quadratic_
- Define effective mass _w.r.t. Cartesian coordinates_:
$$m_{\alpha}^{*}=\hbar^{2}\left[ \frac{\partial^{2}E}{\partial k_{\alpha}^{2}} \Bigg|_{\boldsymbol{k}_\text{min}} \right]^{-1} $$
- With quadratic dispersion, the _density of states_ can be written as:
$$g(E \gtrsim E_\text{min})=\frac{Vm^{*}}{\pi^{2}\hbar^{2}} \left[ \frac{2m^{*}(E-E_\text{min})}{\hbar^{2}} \right]^{1/2} $$
- The _effective mass_ is _averaged_ across three directions
	- The _average curvature_
$$m^{*}=(m_{x}^{*}m_{y}^{*}m_{z}^{*})^{1/3}$$
- Similarly:
$$g(E\lesssim E_\text{max})=\frac{Vm^{*}}{\pi^{2}\hbar^{2}} \left[ \frac{2m^{*}(E_\text{max}-E)}{\hbar^{2}} \right]^{1/2}$$
- The _flatter_ the band, the larger $m^{*}$, and the _larger the density of states_ is
- The band structure can also have _saddle points_ where curvature can have _opposite signs for different directions_
	- Later, it can be proven that it gives rise to _singularities_

- For any form of $E(\boldsymbol{k})$, taking different _bands_ into account:
$$g(E)=\sum_{n} g_{n}(E)=\sum_{n} \int  \, \frac{d^{3}\boldsymbol{k}}{4\pi^{3}} \delta(E-E_{n}(\boldsymbol{k}))$$
- From the delta function, this is an _integral over a surface_ $S_{n}(E)$
	- $S_{n}(E_{F})$ is the _Fermi surface_
- Separate into a _2D surface integral over the surface_, and a _perpendicular component_:
	- Using $\delta(f(x)-f(x_{0}))=\delta(x-x_{0})/|f'(x_{0})|$
	- The gradient is _in the normal direction_
$$\begin{align}
g_{n}(E)&= \int _{S_{n}(E)} \, \frac{dS}{4\pi^{3}} \int  \, dk_{\perp}(\boldsymbol{k}) \delta(E-E_{n}(\boldsymbol{k})) \\ &=\int _{S_{n}(E)} \, \frac{dS}{4\pi^{3}} \frac{1}{\left| \nabla_{\perp} E_{n}(\boldsymbol{k})  \right| } 
\end{align}$$
![[Constant energy surface.png|400]]
- The gradient must _vanish at the edge of the band_
	- Such that there is _no discontinuity_ in the _derivative_
- It also _vanishes at saddle points_

- All stationary points are described by dispersion (relative to stationary point):
$$E(\boldsymbol{k})=E_{0}\pm \frac{\hbar^{2}}{2m_{x}^{*}}k_{x}^{2}\pm \frac{\hbar^{2}}{2m_{y}^{*}} k_{y}^{2} \pm \frac{\hbar^{2}}{2m_{z}^{*}} k_{z}^{2}$$
- If the signs are _all positive/negative_, it is a _minimum/maximum_
- If the signs are _mixed_, it is a _saddle point_

- Near these stationary points, one gets _van Hove singularities_
	- 2D: a _logarithmically singular_ density of states
	- 3D: a _discontinuity_ in the derivative

## Electrons and holes
- Consider _removing electrons_ from a _filled band_
	- Example: _absorption_ of a photon with energy _exceeding_ that of the band gap
- The removal of an electron gives a _hole_
	- Like the removed electron, it is a _fermion_
![[Electron-hole pair.png]]
- Photons give _vertical transitions_, adding _no momentum_ to the system
- From momentum conservation:
$$\boldsymbol{k}_{h}=-\boldsymbol{k}_{e}$$
- Measuring energy _from the top of the band_, from energy conservation:
$$\varepsilon_{h}(\boldsymbol{k}_{h})=-\varepsilon_{e}(\boldsymbol{k}_{e})$$
- The _hole velocity_, from the relations above:
$$v_{h}=\boldsymbol{v}_{e}$$
- Assuming a _parabolic dispersion_, the _effective mass_ is then:
$$m^{*}_{h}=-m^{*}_{e}$$
- Taking the [[#Wavepackets and equations of motion|equation of motion]] for an electron and flipping signs:
$$\hbar \frac{d\boldsymbol{k}_{e}}{dt}=+e(\boldsymbol{E}+\boldsymbol{v}_{h}\times \boldsymbol{B})$$
- The _current_ carried by the hole must be the _same_ as the missing current from the electron
- The _effective charge_ is $+e$
	- Consider the motion of the _valence electrons_ in moving the hole, under an electric field


# Experimental probes of Fermi surface

## Photon absorption
- The photon _excites_ an electron from an occupied state to an _empty state_
- As $E=\hbar kc$, the transition is _nearly vertical_

- In a _direct band gap_ conductor (e.g. $\ce{ GaAs }$), the _lowest energy available_ is at the _same wave-vector_, so the transition is _vertical_
- For an _indirect band gap_ semiconductor (e.g. $\ce{ Si }$), the valence band maximum is at a _different wave-vector_ to the conduction band minimum
	- A _phonon_ must be excited as the photon is absorbed
	- A _second order_ process which is _much less likely_ than a direct transition

![[Direct vs indirect band gaps 1.png|500]]

- The initial and final electron states are related by:
$$\epsilon_{f}=\epsilon_{i}+\hbar\omega$$
- The _minimum_ for $\hbar\omega$ is $E_{g}$, above which there is a _spectrum of available transitions_

### Form of transition rate
- The _optical absorption coefficient_ is determined by a _quantum mechanical transition rate_, for _exciting_ the electron from $\psi_{i}$ to $\psi_{f}$ by absorption of $\hbar\omega$
- From [[Time-dependent quantum mechanics#Fermi's Golden Rule|Fermi's Golden Rule]]:
$$W_{i\to f}=\frac{2\pi}{\hbar}|M|^{2}g(\hbar\omega)$$
- $g(\hbar\omega)$ is a _joint density of states_ as there can be _multiple_ transitions of $\hbar\omega$ at _different energies_

- Matrix element: perturbation due to _electric dipole formation_
	- $\boldsymbol{p}_{e}=-e\boldsymbol{r}$
$$M=\braket{ \psi_{f}|\hat{H}' | \psi_{i} }  \hspace{1cm} \hat{H}'=-\boldsymbol{p}_{e}\cdot \boldsymbol{E}_{0}\exp(i\boldsymbol{k}\cdot \boldsymbol{r})$$
- Electron states are [[#Bloch states|Bloch wave-functions]]
$$\psi_{i/f}=\frac{1}{\sqrt{ V }} u_{i/f}\exp(i\boldsymbol{k}_{i/f}\cdot \boldsymbol{r})$$
- The matrix element is then:
$$M=\frac{e}{V} \int  \, dx $$
- The _phase factor_ must be zero:
$$\hbar(\boldsymbol{k}_{f}-\boldsymbol{k}_{i})=\hbar \boldsymbol{k}$$
- $u_{f}$ and $u_{i}$ have the _periodicity of the lattice_, so the integral becomes a _sum over identical unit cells_:
$$|M| \propto \int _\text{unit cell} u_{i}^{*}(\boldsymbol{r}) x u_{f}(\boldsymbol{r}) \, d^{3}\boldsymbol{r} $$
- Assume the light is _polarised_ along the $x-$axos

- The precise forms of $u$ depend on the _band_ and the material

- Let $\boldsymbol{k}_{f}=\boldsymbol{k}_{i}$, valid for optical transitions

### Example: GaAs
- Direct band gap
- $3$ valence bands, corresponding to $p$ bonding orbitals
- Single conduction band due to $s$ antibonding orbitals
	- Description strictly valid only at _zone centre_ $\Gamma$, as _atomic character_ tends to change away from $\Gamma$
- There is then _one electron band_, and _three hole bands_
![[GaAs band structure.png]]
### Joint density of states
- $g(\hbar\omega)$ is the _joint density of states_, as both initial and final states are in _continuous bands_
- Take the example of $\ce{ GaAs }$, with _conduction, heavy-hole, light-hole, split-off hole_ bands
![[GaAs bands.png|350]]

- Quadratic dispersions:

- In a _heavy or light hole transition_:
$$\hbar \omega=E_{g}+\frac{\hbar^{2}k^{2}}{2m^{*}_{e}}+\frac{\hbar^{2}k^{2}}{2m^{*}_{h}}$$
- Write the _reduced electron-hole mass_:
$$\frac{1}{\mu}=\frac{1}{m_{e}^{*}}+\frac{1}{m_{h}^{*}}\implies \hbar\omega=E_{g}+\frac{\hbar^{2}k^{2}}{2\mu}$$
- Joint density of states:
$$\hbar\omega>E_{g}: g(\hbar\omega)=\dots \sqrt{ \hbar\omega-E_{g} }$$

### Experimental results
- In a material of _finite size_, the absorption follows _Beer's law_:
$$I=I_{0}\exp(-\alpha z)$$
- $\alpha$ is the _fraction of intensity absorbed per unit length_

- For $\hbar\omega>E_{g}$, one expects $\alpha \propto \sqrt{ \hbar\omega -E_{g} }$
	- Plot as $\alpha^{2} \propto \hbar\omega-E_{g}$
- As $g(\hbar\omega) \propto \mu^{3/2}$, transitions with _larger reduced masses_ give rise to _stronger absorption_

- This is only followed _approximately_
- The electrons and holes have _Coulomb attraction_
- They can form a _bound pair_, known as an _exciton_
- These effects become more significant for _large band gap_, and _lower temperature_

- Crystals may include _impurities_ and _defects_ with energies _within the band gap_
- This gives _additional absorption_

- The _parabolic_ approximation is only valid near $k=0$
	- Joint DoS moves away from $\sqrt{ \hbar\omega-E_{g} }$
	- The _full band structure_ must be calculated
![[GaAs optical spectrum.png]]

### Indirect semiconductor
- Transition must involve a _phonon_ to conserve momentum

- Consider an indirect transition from $(\epsilon_{1},k_{1})$ to $(\epsilon_{2},k_{2})$
- Photon energy $\hbar\omega$, phonon energy $\hbar\Omega$

- Conservation:
$$\epsilon_{f}=\epsilon_{i}+\hbar\omega \pm \hbar\Omega \hspace{1.5cm} \hbar \boldsymbol{k}_{f}\approx \hbar \boldsymbol{k}_{i}+\hbar \boldsymbol{q}$$
- Phonons can be _absorbed_ or _emitted_
	- The former is only possible at _higher temperatures_

- The absorption is _weaker_ due to it being a _second order process_
![[Direct vs indirect absorption.png|400]]

- A QM derivation gives $\alpha(\hbar\omega) \propto (\hbar\omega-E_{g} \mp \hbar\Omega)^{2}$
- Frequency dependence _different from direct band gap conductors_

- The _threshold_ is dependent on whether the phonon is _emitted or absorbed_
	- There are often _contributions from both_, but the latter is only possible for _higher temperatures_

### Excitons
- There is often a _peak_ in the spectrum at _low temperatures_
- An exciton is a _bound pair_ of electron and hole with _reduced mass_
$$\frac{1}{\mu}=\frac{1}{m_{e}^{*}}+\frac{1}{m_{h}^{*}}$$
- Modify equation for _energy of a hydrogen atom_:
	- Change both _mass_, and _relative permittivity_
$$E_{n}=-\frac{\mu^{*}}{m_{e}\epsilon^{2} } \frac{13.6\,\text{eV}}{n^{2}}\equiv -\frac{R_{x}}{n^{2}}$$
- The energy of the exciton is equal to _energy required to create a pair_, _minus the binding energy_:
$$\epsilon_{n}=E_{g}-\frac{R_{x}}{n^{2}}$$

- Typically on the order of $\text{meV}$

## Photoemission
- Photons are _incident_ on a sample, electrons are then _excited_

- The excited electron _leaves_ the crystal

- The incident photon has _very little momentum_, so the momentum of the electron _parallel_ to the surface is approximately that of its _original state_ in the solid
	- The _perpendicular_ momentum is not conserved as the electron _escapes_
![[Electron photoemission.png|250]]
- Relating energies:
	- $E_{F}$ is relative to the _vacuum_ state, $E_{i}$ is relative to the _Fermi energy_
$$E_{f}=\frac{\hbar^{2}k_{f}^{2}}{2m}=E_{i}+\hbar\omega-\phi \hspace{1cm}k_{i, ||}=k_{f, ||}$$

- Use _detector angle_ to find $k_{||}$
	- If the sample is _rough_

- Can only be used to probe _occupied states_
- Typically easiest to interpret when there is _little dispersion_ perpendicular to the surface
	- _Anisotropic_ layered materials
- There is often _thermal broadening_ 
## Quantum oscillations
- Many material properties tend to _oscillate_ with magnetic field
- The _form_ of the oscillations can be used to infer the Fermi surface

- Use a _semiclassical treatment_ using the _Bohr-Sommerfeld quantisation condition_ for electron orbits:
$$\oint \boldsymbol{p}\cdot d\boldsymbol{r}=\left( n+\frac{1}{2} \right)2\pi \hbar$$
- $\boldsymbol{p}$ is the _canonical momentum_:
$$\boldsymbol{p}=\hbar \boldsymbol{k}+q\boldsymbol{A}$$
- The Lorentz force:
$$m\dot{\boldsymbol{v}}=q \dot{\boldsymbol{r}}\times \boldsymbol{B} \implies m\boldsymbol{v}_{\perp}=q\boldsymbol{r}\times \boldsymbol{B}$$
- Around a _loop_, the integral of $\boldsymbol{v}_{||}\cdot d\boldsymbol{r}$ is zero
- Using _Stokes theorem_, and the fact that the integral of $\boldsymbol{r}\cdot d\boldsymbol{r}$ is twice the area:
$$\oint\boldsymbol{p}\cdot d\boldsymbol{r}=-q\Phi=\left( n+\frac{1}{2} \right)2\pi \hbar$$
- Hence, electron orbits must _enclose a quantised flux_:
$$\Phi_{n}=A_{r}^{n}B=\left( n+\frac{1}{2} \right) \frac{h}{e}$$
- From the de Broglie relation:
$$\hbar \boldsymbol{k}_{\perp}=q\boldsymbol{r}\times \boldsymbol{B}$$
- The $k-$space orbit is _stretched_ by factor $Bq/\hbar$, and is _rotated_ by $90^{\circ}$
- The _area enclosed_ in $k-$space is:
$$A_{k}=\left( \frac{eB}{\hbar} \right)^{2}A_{r}^{n}= \frac{2\pi e}{\hbar}B\left( n+\frac{1}{2} \right)$$
- Hence, orbits in $k-$space are _quantised_

- In a magnetic field, the _allowed_ $k-$states _no longer form a lattice_
- They live in _Landau tubes_, which _cut_ the Fermi surface
![[Landau tubews.png]]

- A _slice_ $\perp \boldsymbol{B}$, with area $A$, through Fermi surface only contributes to $g(E_{F})$ only if it _matches the Landau tube_
- Consider _varying_ $\boldsymbol{B}$ for this slice, then the _contribution_ to $g(E_{F})$ will _oscillate_
- Field values where the considition is _satisfied_ follow the Osanger relation:
$$\Delta\left( \frac{1}{B} \right)=\frac{2\pi e}{\hbar} \frac{1}{A_{k}}$$
- It links the _period of quantum oscillations_ to the area of the Fermi slice

- The energy of the band electrons are quantised into [[Charged Particles#Landau levels|Landau levels]] perpendicular to $\boldsymbol{B}$
	- Motion _parallel_ is unconstrained
- Hence, each Landau level has a $1D$ _density of states_ superimposed on it
- _Sharp peaks_ in the DoS move _through_ the chemical potential, such that there is a _modulation_ in density of states and 

## Tunnelling (incomplete)
- Through a _potential barrier_
- Maintain _electrical bias_

$$I= \int _{\mu+eV}^{\mu} g_{1}(\omega)g_{2}(\omega)T(\omega) \, d\omega $$

- _Differential conductivity_

- STM
	- Tunnelling probability is an _exponential function_ of barrier thickness
	- Spatial resolution
	- Constant current

## Cyclotron resonance
- _Direct measurement_ of the cyclotron resonance frequency:
$$\omega_{c}=\frac{eB}{m^{*}}$$
- Measurement of the _effective mass_ by exciting _transitions between Landau levels_
- For _semiconductors_, with _lower carrier density_, the radiation _easily penetrates samples_

- Measurements made by _transmission_, and radiation is detected using a _bolometer_
- _Linewidth_ gives information about the _scattering rate_
- In _lightly doped_ samples, carriers

![[Cyclotron resonances.png]]

# Transport properties

## Scattering in metals
- Consider the effect of scattering in a metal with _isotropic bands_, characterised by $m^{*}$ and a _spherical Fermi surface_
- In the _relaxation time approximation_:
$$\sigma=\frac{ne^{2}\tau_{\sigma}}{m^{*}}$$
- The _thermal conductivity_ $\kappa$, defined by the _heat flux_
$$\boldsymbol{J}_{q}=-\kappa \nabla T$$
- From kinetic theory:
$$\kappa=\frac{1}{3}\langle v^{2} \rangle \tau_{\kappa}C_\text{el} $$
- $C_\text{el}$ is the _electronic heat capacity_:
$$C_\text{el}=\frac{1}{2}n\pi^{2} \frac{k_{B}T}{E_{F}}$$
- Assume that they move at the _Fermi velocity_, and assuming $E_{F}=m^{*}v_{F}^{2}/2$:
$$L=\frac{\kappa}{\sigma T}=\frac{\pi^{2}k_{B}^{2}}{3e^{2}} \frac{\tau_{\kappa}}{\tau_{\sigma}}$$
- If one _assumes_ $\tau_{\kappa}=\tau_{\sigma}$, one gets the _Wiedemann-Franz Law_
- $L_{0}$ is the _ideal Lorenz number_:
$$L_{0}=\frac{\pi^{2}k_{B}^{2}}{3e^{2}}$$
- Therefore, one can _estimate_ $\kappa$ from $\sigma$

- For _lower temperatures_, $\tau_{\kappa}\approx \tau_{\sigma}$ _no longer holds_

### Electron transport in metals
- Electron velocities are _perpendicular_ to surfaces of constant energy:
$$\boldsymbol{v}_{g}=\frac{1}{\hbar}\nabla_{\boldsymbol{k}}E(\boldsymbol{k})$$
- When an _electric field_ is applied, the Fermi surface is _shifted_ by a small amount:
$$\delta k=\frac{1}{\hbar}m^{*}v_{d}$$
- $v_{d}$ is the _drift velocity_, with $v_{d}\ll v_{F}$
- $\tau_{\sigma}$ is the time taken to _randomise_ an electron's velocity, as they get _scattered_

### Thermal transport in metals
- When there is a _temperature gradient_, molecules travelling in one direction will have _more energy_ than molecules travelling in the other
- The Fermi-Dirac distribution will be more _smeared_ in one direction

- At _low temperatures_, scattering will only affect _thermal conduction_ as it _cannot change_ the _direction_ of electrons (imsufficient energy)
- At _high temperatures_, it will affect _both electrical and thermal conduction_

### Matthiessen's rule
- Scattering rates are _additive_:
$$\frac{1}{\tau}=\frac{1}{\tau_{1}}+\frac{1}{\tau_{2}}+\frac{1}{\tau_{3}}+\dots$$
- Scattering processes with the _shortest scattering time_ will _dominate_
- There are _ranges of temperature_ where only _one scattering process_ dominates
	- At _high temperature_, _phonon_ scattering dominates

- Matthiessen's rule _fails_ when scattering rate is _direction-dependent_, or when _scattering processes interfere with each other_

## Phonon emission and absorption
- Phonons can _scatter off electrons_ either _elastically_ or _inelastically_
	- Elastic: both particles _change momentum and energy_, constrained by the conservation of both
	- Inelastic: the phonon is _emitted or absorbed by the electron_
- This results as _mobile electrons can distort the lattice_

### Room temperature
- Phonons behave as _massless bosons_, similar to _photons_
- They have a _black-body distribution_ with $\hbar\omega \sim k_{B}T$
- Hence, scattered electrons are distributed within $\pm k_{B}T$ of the _Fermi energy_
	- Must be scattered into an _unoccupied state_, so only $\sim k_{B}T$ of energy can be emitted in the form of phonons

- The _most energetic phonons_ have energy of roughly $\hbar\omega \sim k_{B}\theta_{D}$
- They have wave-vectors _comparable_ to the width of the BZ $q\sim k_{F}$
- Therefore, phonons can _scatter an electron to the other side_ of the Fermi surface
- At room temperature, $\tau_{\sigma}\approx \tau_{\kappa}$, and are _proportional_ to the number of phonons with $\hbar\omega \sim k_{B}T$

### Low temperatures
- At _low temperatures_ $T\ll\theta_{D}$, phonons have energies $k_{B}T\ll k_{B}\theta_{D}$, so $q\ll k_{F}$
- _Inelastic scattering_ changes electron energy by $k_{B}T$, so the _thermal scattering rate_ $\tau_{\kappa}^{-1} \propto T^{3}$
	- From _Debye theory_, that gives number of phonons with $\hbar\omega\sim k_{B}T$
- Weighting factor for $\tau_{\sigma}$, to account for the _small angle_ by which $\boldsymbol{k}$ can change along the Fermi surface:
$$1-\cos\theta\sim \frac{\theta^{2}}{2}\propto \frac{q^{2}}{k_{F}^{2}}\propto T^{2}$$
- Therefore:
$$\tau_{\sigma}^{-1} \propto T^{5},\tau_{\kappa}^{-1} \propto T^{3} \implies \tau_{\sigma}^{-1}\ll \tau_{\kappa}^{-1}$$

- Fermi surface close to BZ boundary: _Umklapp scattering_ occurs
- $\boldsymbol{k}$ is scattered into an _adjacent BZ_

- For _very low temperatures_: _impurity_ and _defect_ scattering
- They can cause _large angle scattering_, such that $\tau_{\kappa}\approx \tau_{\sigma}$, and Wiedemann-Franz law holds
![[Metal conductivities.png]]
## Electron-electron scattering
- For both _energy and momentum_ to be conserved, electron-electron scattering _within the Fermi surface_ is typically unlikely for _simple Fermi surfaces_
	- e.g. A _roughly spherical_ Fermi surface has very few electron-electron scattering events
- For more complicated Fermi surfaces, and _high initial and final density of states_ (high $m^{*}$), it becomes more important

- For a _filled Fermi sphere_ with a _single excited electron_ of $\epsilon_{1}>E_{F}$
- It must _scatter_ with an electron of $\epsilon_{2}<E_{F}$ to give electrons of $\epsilon_{3},\epsilon_{4}$ (all _within_ $k_{B}T$)
- From energy conservation, $\epsilon_{1}+\epsilon_{2}=\epsilon_{3}+\epsilon_{4}$
- If $\epsilon_{1}=E_{F}$, then $\epsilon_{2}=\epsilon_{3}=\epsilon_{4}=E_{F}$, giving _zero_ allowed $k-$space volume, and an _infinite scattering lifetime_ at $T=0$

- When $\epsilon_{1}\neq E_{F}$, there is _finite phase space available_ within a shell of thickness $|\epsilon_{1}-E_{F}|$
- The scattering rate $\propto(\epsilon_{1}-E_{F})^{2}$
	- There is _no freedom_ for $\epsilon_{4}$ due to conservation
- Due to the _thermal distribution_, there is _additional choice in energy_, leading to the _total scattering rate_:
$$\tau^{-1}=\alpha(\epsilon_{1}-E_{F})^{2}+\beta(k_{B}T)^{2}$$
- At _finite temperature_, $\epsilon_{1}-E_{F} \propto k_{B}T$, hence $\tau \propto T^{-2}$

# Semiconductors
- In semiconductors, the _band gap_ becomes _small_ enough that _thermal excitation_ of carriers is significant
- The _chemical potential_ is typically _mid-gap_

- The _conduction band_:
$$\varepsilon_{c}(k)=\varepsilon_{c}+\frac{\hbar^{2}k^{2}}{2m_{e}^{*}} \hspace{1.5cm}g_{e}(\varepsilon)=\frac{1}{2\pi^{2}}\left( \frac{2m_{e}^{*}}{\hbar^{2}} \right)^{3/2}\sqrt{ \varepsilon-\varepsilon_{c} }$$
- The _valence band_, occupied by _holes_:
$$\varepsilon_{v}(k)=\varepsilon_{v}-\frac{\hbar^{2}k^{2}}{2m_{h}^{*}} \hspace{1.5cm}g_{e}(\varepsilon)=\frac{1}{2\pi^{2}}\left( \frac{2m_{h}^{*}}{\hbar^{2}} \right)^{3/2}\sqrt{ \varepsilon_{v}-\varepsilon }$$

## Carrier density
- For a known $\mu$, the _carrier density_ in the conduction band:
$$n=\int _{\epsilon_{c}}^{\infty}g_{e}(\epsilon)f(\epsilon) \, d\epsilon $$
- Here, $f(\epsilon)$ is the _Fermi-Dirac distribution_
- For a _non-degenerate gas_, make the approximation $\epsilon-\mu\gg k_{B}T$:
$$f(\epsilon)\approx \exp\left[ -\frac{\epsilon-\mu}{k_{B}T} \right]$$
- From this, the _electron density_:
$$n=2\left( \frac{m_{e}^{*}k_{B}T}{2\pi \hbar^{2}} \right)^{3/2}\exp\left[ -\frac{\epsilon_{c}-\mu}{k_{B}T} \right]$$
- Similarly, the _hole density_:
$$p\approx 2\left( \frac{m_{h}^{*}k_{B}T}{2\pi \hbar^{2}} \right)^{3/2}\exp\left[ -\frac{\mu-\epsilon_{v}}{k_{B}T} \right]$$
- Define _temperature-dependent concentrations_ for the number of states within $k_{B}T$ of the band edge:
$$\displaylines{n_{c}(T)=2\left( \frac{m_{e}^{*}k_{B}T}{2\pi \hbar^{2}} \right)^{3/2} \hspace{1.5cm}p_{v}(T)= 2\left( \frac{m_{h}^{*}k_{B}T}{2\pi \hbar^{2}} \right)^{3/2}\\ n=n_{c}(T)\exp\left[ -\frac{\varepsilon_{c}-\mu}{k_{B}T} \right]\hspace{1.5cm}p=p_{v}(T)\exp\left[ -\frac{\mu-\varepsilon_{v}}{k_{B}T} \right]}$$
### Law of mass action
- From this, get that $np$ is _only dependent on temperature_
$$np=n_{c}(T)n_{p}(T)\exp\left( -\frac{\epsilon_{g}}{k_{B}T} \right)\hspace{1cm}\epsilon_{g}=\epsilon_{c}-\epsilon_{v}$$
- $\epsilon_{g}$ is the _band gap_
- This is the _law of mass action_
	- Independent of $\mu$

- This applies for _all carriers_, including _extrinsic_ ones (impurities, dopants)

- This can be argued thermodynamically:
	- Suppose the equilibrium population is maintained by _blackbody radiation_
	- Photons generate _electron-hole pairs_ at rate $A(T)$
	- The rate of _recombination_ is $B(T)np$
	- At _equilibrium_, $np=A(T)/B(T)$

- If one introduces _impurities_, $n$ or $p$ may _increase_, then as $np$ is _constant_, the other intrinsic carrier has _lower concentration_
- One can then _reduce_ the _total carrier concentration_ $n+p$ in an impure crystal

### Intrinsic semiconductors
- In an _intrinsic semiconductor_, holes come from unoccupied electron levels, hence:
$$n_{i}=p_{i}=\sqrt{ n_{c}(T)n_{v}(T) }\exp\left( -\frac{\epsilon_{g}}{2k_{B}T} \right)$$
- As the creation of an electron also creates a _hole_, the "gap" is $\epsilon_{g}/2$

- If one substitutes the formulae for $n_{c}(T)$ and $n_{p}(T)$, and setting $n=p$:
$$\mu=\epsilon_{v}+\frac{1}{2}\epsilon_{g}+\frac{3}{4}k_{B}T\ln\left( \frac{m_{h}^{*}}{m_{e}^{*}} \right)$$
- If $m_{h}^{*}=m_{e}^{*}$, or $T=0$. then $\mu$ lies in the _middle of the bandgap_
- Otherwise, it _drifts_ in the direction of _higher effective mass_

## Doped semiconductors
- When _impurity atoms_ are added, this produces _extrinsic carriers_

### Donor and acceptor levels
- Example: replace the $\ce{ Ga }$ in $\ce{ GaAs }$ with $\ce{ Si }$, which is an _electron donor_
- The _donated electron_ is still _attracted_ to $\ce{ Si }$
- The _donor energy levels_ are approximately [[The hydrogen atom|hydrogenic]]
	- Account for _screening_ in the dielectric constant
	- Use the _effective mass_
$$\Delta_{d}=\frac{m_{e}^{*}}{m_{e}} \frac{1}{\epsilon^{2}} \frac{13.6\,\text{eV}}{n^{2}}$$
- For $\ce{ GaAs }$, $\Delta_{d}(\text{1s})= 5.3\,\text{meV}$, compared to the _band gap_ of $1.4\,\text{eV}$

- At _room temperature_, all donors are likely to be _ionised_
- This gives a _constant carrier density_

- The energy is _relative to the bottom of the conduction band_
- When ionised, the donor electrons go _into the conduction band_
![[Donor levels.png]]

- Similarly, impurities can _accept_ electrons, adding a _hole_
- The _acceptor levels_ are also _hydrogenic_, and _sit above the valence band maximum_ (the holes are _ionised_ into the valence band)
- The _chemical potentials_ for doped semiconductors lie _between_ the donor/acceptor levels, and the conduction/valence bands
![[Physics/Zimages/Donor and acceptor levels.png|400]]
### Carrier densities
- Even for _low densities_, the low donor/acceptor energies mean that _impurities are the main source of carriers_, even in _room temperature_
- If _donors_ dominate, the material is _n-type_
- If _acceptors_ dominate, the material is _p-type_

- Materials can have _both_ types of purities
	- In $\ce{ GaAs }$, $\ce{ Si }$ can be both donor and acceptor based on the _site_
- Dominant carrier probed by _Hall effect_

- The law of mass action _holds as long as_ donor/acceptor concentration are _low_ enough such that $\mu$ is _in the band gap_
- Given $N_{D}$ and $N_{A}$, use the law of mass action, and $n-p=N_{D}-N_{A}$ to find $n,p$

![[Carrier density.png]]
- At _intermediate temperature_, all donors are _ionised_, in the _saturation range_ where $n$ is _constant_
	- The _intrinsic contribution_ is negligible
- At _low temperature_, extrinsic electrrons _freeze out_, and gradient is _dependent on saturation energy_
- At _high temperature_, the _intrinsic contribution_ becomes larger, with gradient _dependent on band gap_

### Electrical conductivity
- Electrical conductivity is a _sum of contributions from carrier tyoes_:
	- Typically dominated by _electrons and havy holes_
$$\sigma=ne\mu_{e}+pe\mu_{hh}$$
- The mobilities:
$$\mu_{e}=\frac{e \tau_{e}}{m_{e}^{*}} \hspace{1.5cm}\mu_{hh}=\frac{e \tau_{hh}}{m_{hh}^{*}}$$
- _Temperature dependence_ is dependent on _scattering times_ of different processes
- Impurity scattering: _cross-section_ varies as $\epsilon^{-2} \propto T^{-2}$, so $\lambda \propto T^{2}$
- The _carrier speed_ $v \propto \epsilon^{1/2}\propto T^{1/2}$, such that $\tau _\text{imp}=\lambda/v\propto T^{3/2}$

- Phonon scattering: the _number of phonons_ $\propto T$, hence $\lambda \propto T^{-1}$ and $\tau _\text{pho}\propto T^{-3/2}$

- At _low temperatures_, impurity scattering dominates
- At _high temperatures_, phonon scattering dominates
- There is a _peak in mobility_ at an intermediate temperature

### Hall effect with two carrier types
- [[#Relaxation time approximation]]:
$$\frac{d\boldsymbol{j}}{dt}=-\frac{1}{\tau}\boldsymbol{j} +\frac{ne^{2}}{m}(\boldsymbol{E}+\boldsymbol{v}\times \boldsymbol{B})$$
- In the _steady state_, for electrons, using [[#Relaxation time approximation|mobility]] $\mu_{e}=e \tau/m$
$$\boldsymbol{j}=n_{e}e\mu_{e}(\boldsymbol{E}+\boldsymbol{v}_{e}\times \boldsymbol{B})$$
- If there are both _electrons and holes_:
$$\boldsymbol{j}=ne\mu_{e}(\boldsymbol{E}+\boldsymbol{v}_{e}\times \boldsymbol{B})+pe\mu_{h}(\boldsymbol{E}+\boldsymbol{v}_{h}\times \boldsymbol{B})$$

- After the charge build-up, let the current be _confined_ in the $x-$direction, with $\boldsymbol{B}=B\hat{z}$
- Then, $v_{h}^{x}$ and $v_{e}^{x}$ have _opposite directions_
- Using $\mu=v/E$:
$$\displaylines{j_{x}=eE_{x}(n\mu_{e}+p\mu_{h}) \\ 0=eE_{y}(n\mu_{e}+p\mu_{h})-eBE_{x}(n\mu_{e}^{2}-p\mu_{h}^{2})}$$
- From this: 
$$\displaylines{E_{y}=\frac{j_{x}B(n\mu_{e}^{2}-p\mu_{h}^{2})}{e(n\mu_{e}+p\mu_{h})^{2}} \\R_{H}=\frac{E_{y}}{j_{x}B}=\frac{n\mu_{e}^{2}-p\mu_{h}^{2}}{e(n\mu_{e}+p\mu_{h})^{2}}}$$
- In the $p\to 0$ limit, $R_{H}\to -1/ne$
- For _high mobility_, a _minority carrier_ can determine the _sign_ of $R_{H}$
![[InSb Hall effect.png]]
- Example: $\ce{ InSb }$ with $\mu_{e}/\mu_{h}\sim 100$
- At _high temperature_, the _intrinsic carriers dominate_, and the _slope_ of the graph can be used to determine the _band gap_
	- $R_{H}\approx -1/ne$ remains _negative_
- At _low temperatures_, the _intrinsic carriers freeze out_
	- With donors: $R_{H}$ remains constant, dependent on _extrinsic electron concentration_
	- With acceptors: $R_{H}$ _changes sign_, as _holes_ begin to dominate
# Semiconductor devices
- _Inhomogenous_ systems of semiconductors
- Dependent on the _interfaces_ between semiconductors

- A _semiclassical treatment_ of electrons:
$$H=E_{n}(\boldsymbol{k})-e\phi(\boldsymbol{r})$$
- They have momentum $\boldsymbol{p}=\hbar \boldsymbol{k}$ and experience electrostatic potential $\phi(\boldsymbol{r})$
- The potential can arise from _external fields_, _doping_, or changes in _composition_

- For an _isolated solid_, the difference between $\mu$ and the _vacuum level_ (free space) is the _work function_ $\Phi$
- Two _isolated materials_ with different $\Phi$ have different $\mu$
- This must _equalise_ when _placed in contact_
	- Electrons _flow towards_ the more _electronegative_ material to equalise $\mu$
	- This generates _internal inhomogenous electric fields_

## Metal-semiconductor contact
![[Metal semiconductor contact.png]]
- Consider an _ideal metal_ in contact with an _n-type semiconductor_
	- Known as a _Schottky diode_
- The chemical potentials must then be _equalised_ as electrons _go into the metal_, producing the potential $\phi(x)$
	- _Deep inside_ the semiconductor, $\phi(x)\to 0$
	- The _electro-chemical_ potential: $\mu+e\phi(x)$
- Relative to $\mu$, the bands in the semi-conductor _bend upwards_
- The _donor levels near the interface_ are _emptied_, leaving a _depletion region_

- The _Schottsky barrier_ $\Phi_{b}$ will _inhibit current flow_ between metal and semiconductor
	- An electron must _tunnel through_ (common for low $T$), or be _thermally excited_ (thermionic emission) into the _conduction band_
- With a large enough bias, the junction acts as a _rectifier_ as the _chemical potentials_ of the two materials _shift_ 

- With a _+ve bias to the metal_ , the barrier is _lowered_ and current flows more freely
	- For a large enough bias, the barrier _disappears_
- With a _-ve bias to the metal_, the barrier is _raised_ as the _depletion region grows in width_, and current remains small
	- Eventually, _breakdown_ occurs
## p-n junctions
- A _p-n junction_ is formed when [[#Doped semiconductors|p-type and n-type semiconductors]] come into _contact_
	- An _inhomogeneous doping_ of the material
![[Physics/Zimages/p-n junction.png]]
- _Electrons flow from n-type to p-type_ in order to fill the holes, until $\mu$ is _equalised_
	- _Deep inside_ the semiconductors, the $\mu$ must lie _close to_ the conduction/valence bands (between donor/acceptor levels and the bands)
- This creates a _depletion region_ with no carriers, where there is also an _electric field_

- Relative to $\mu$, the bands _bend_ according to $\phi(z)$, determined by _Poisson's equation_:
$$\nabla^{2}\phi=\frac{\partial^{2}\phi}{\partial z^{2}}=-\frac{\rho}{\epsilon\epsilon_{0}}$$
- The _junction potential_ $\phi_{j}$ is defined by:
$$e\phi_{j}=E_{g}=\mu_{n}-\mu_{p}$$
- Given _donor/acceptor densities_ $N_{D/A}$, and _widths of depletion regions_ $w_{n/p}$, overall _charge neutrality_ of the system dictates:
$$N_{D}w_{n}=N_{A}w_{p}$$
- In 1D, when there is _net charge_, $\phi$ (and the bands) will _curve_
- When there is _no net charge_ in 1D, $\phi$ is either _linear_ or _constant_:
$$\displaylines{\phi_{j}=\frac{e}{2\epsilon\epsilon_{0}}(N_{A}w_{p}^{2}+N_{D}w_{n}^{2}) \\ N_{(A,D)}w_{(p,n)}=\sqrt{ \frac{2\epsilon\epsilon_{0}\phi_{j}}{e} \frac{N_{A}N_{D}}{N_{A}+N_{D}}} \\ w_{n}+w_{p}=\sqrt{ \frac{2\epsilon\epsilon_{0}\phi_{j}}{e} \frac{N_{A}+N_{D}}{N_{A}N_{D}}}}$$
- On both sides, there are both _majority_ and _minority carriers_ from the [[#Law of mass action]]
![[p-n junction contact.png]]
### Rectification
- A $p-n$ junction behaves as a _diode_, allowing current to _flow much more readily in one direction_ than the other
- Let there be some _electrical bias_, where a _positive voltage_ corresponds to applying towards the p-side
![[p-n junction bias.png|400]]
- A charge _experiences_ the potential $\phi_{j}-V$ _across the depletion layer_

- With _no voltage bias_, there will be _no net current flow_ across the diode
- The _minority carriers_ tend to get _swept by the in-junction electric field_ into the other side, making a _generation current_ $-J^\text{gen}$ from $n$ to $p$
	- Minority carriers are continuously _thermally generated_
	- The current is _independent of bias_, only depending on $E_g$ and $T$
- The _majority carriers_ may be _thermally excited up_ the potential barrier, then _recombine_, creating a _recombination current_ $J^{\text{rec}}$ from $p$ to $n$
	- The _activation energy_ is dependent on $V$:
$$J^\text{rec}\propto \exp\left[ -\frac{e(\phi_{b}-V)}{k_{B}T} \right]$$

![[Drift and generation current.png]]
- Considering that there is _no current at zero bias_, the current takes the form:
$$I=I_\text{sat}\left[ \exp\left( \frac{eV}{k_{B}T} \right)-1 \right]$$
- The saturation current is the combination of _generation currents_ from minority carriers, proportional to $n_{i}^{2}/N_{D}$, and hence _activated_ by $\exp(-E_{g}/k_{B}T)$
- If _reverse bias_ is too large, the _majority carriers tunnel across_ the depletion region, and _breakdown_ occurs
![[Diode I-V.png]]

## LEDs
- _Recombination_ of electrons and holes can be used to _generate light_
- With a _bias_, electrons (holes) can be _injected_ into the n(p)-type region to _continuously_ generate photons
- The process is _not efficient_ for _indirect band gap_ materials
![[LED operation.png|400]]

## Photovoltaic cells
- If _light_ shines on a p-n junction (wihout bias), an _electron-hole pair_ can be created
- The _carriers_ will _diffuse towards_ the junction, and are pulled in _opposite directions_ by the electric field
	- Must be _fast enough_ to reach the junction _before recombining_
- This results in a current _in the same direction as the generation current_ ($n\to p$)
- The _separation of charges_ generates its own _electrical bias_
	- Analagous to a _capacitor_
- The _photo-voltaic effect_ described above can be used to make _power cells_
![[Solar cell.png|420]]

- It can be modelled as a _diode_ in _parallel_ with a _current source_
- For _zero load_ resistance and _infinite load_ resistance, there is _zero power extracted_
	- Zero load resistance: $V=0$
	- Infinite load resistance: $I_\text{load}=0$
![[Solar cell equivalent circuit.png|450]]
- The _open circuit_ $V_{d}$ has an _upper limit_ $E_{g}$
	- If $V_{d}>\phi_{j}$, the _junction field vanishes_, and there is _no photo-generated current_
- There is a _dark current_ $I(V_\text{load})$, with _photo-current_ $I_\text{ph}$ for a certain amount of light
- The _maximum power_ extracted is then $\sim I_\text{ph}E_{g}/e$

### Shockley-Queisser limit
- The _optimisation_ of solar cells by _tuning_ the bandgap
- Involves _matching_ the _bandgap_ with the _intensity spectrum_ of sunlight
- Only photons with _energy_ $\hbar\omega>E_{g}$ can be _captured_
	- Power _extracted_ in the current is then $E_{g}$
	- Carriers in _excited states_ away from band edges then _lose energy_ by _decaying_ to lower lying states
- For _intensity spectrum_ $I(\omega)$, the efficiency is:
$$\frac{\int_{E_{g}}^{\infty} I(\omega)E_{g}\,d\omega}{\int_{0}^{\infty} I(\omega)\hbar\omega \, d\omega } $$
- The typical _optimum efficiency_ is $33\%$ for a band-gap of $1.2\,\text{eV}$
## Field-effect transistors
- Transistors _manipulate carrier density_ in a _channel between two electrodes_, using a _controlling voltage_ applied to a third electrode
	- Controlling electrode: the _gate_
	- The carriers travel from the _source_ electrode to the _drain_ electrode

### Junction field-effect transistor (JFET)
- $p-n$ junctions are used to control the _width_ of a _conducting channel_
- There is an $n-$type conductor _between source and drain_, with _high conductivity_
- Adding $p-$type regions connected to _gate electrodes_ allow control over the _depletion region widths_, adjusting _conducting width_
	- A _positive gate voltage_ will _shrink the depletion region_, and _increase current_
	- A _negative gate voltage_ then _reduces the current_
	- There is always some _small current across_ the depletion region
![[JFET operation.png]]
- With _increasing_ source-drain voltage $V_{DS}$, the _drain-source current_ $I_{D}$ will initially _rise linearly_
	- _Rate_ of increase determined by _gate-source_ voltage $V_{GS}$
- Eventually, the _depletion regions meet_ at some _pinch-off voltage_ $V_{DS}=V_{P}$, and increases in $V_{DS}$ are counterbalanced by the _depletion regions expanding towards the drain_
- This is the _saturation region_, where $I_{D}$ _does not increase_
- If $V_{DS}$ is too high, the _breakdown region_ is entered, and $I_{D}$ increases _rapidly_

- The _value_ of _saturation_ $I_{D}$ is _controlled_ by $V_{GS}$
	- JFET acts as an _amplifier_, as saturation current is _constant for a range of_ $V_{DS}$
- JFETs have _high gain and high input impedance_ compared to the MOSFET
	- Used in low-noise op-amps
![[JFET I-V.png]]
### Metal oxide semiconductor field-effect transistor (MOSFET)
- The _width_ of the conducting channel is controlled by an _electric field_ using the _gate electrode_
- The _gate_ is _separated_ from the rest of the device by an _insulating layer_, ensuring _no current flow from the gate electrode_ (unlike the JFET)
![[MOSFET structure.png]]

- Applying a voltage will _pull electrons into the depleted region_ to create a _conducting channel_ between source and drain
- Changing $V_{GS}$ will _vary resistance_ of the channel
![[MOSFET operation.png]]
- Left: _enhancement_ mode, _positive_ voltage _pulls minority carriers towards surface_, to form a high conductivity _inversion layer channel_
	- Right: I-V characteristic, still with _pinch-off_ at high $V_{DS}$
- Middle: _depletion-enhancement_ mode, a _negative_ voltage _depletes the channel_ to _increase resistance_
	- Similarly, _positive_ voltage will _enhance_ the channel and _decrease resistance_

#### Inversion layer
- Applying a _positive voltage_ to the gate will create an _electric field across the oxide layer_
- The field will _penetrate into_ the semiconductor
- This causes [[#Metal-semiconductor contact|band bending]]

- If the band bending is _larger_ than the band-gap $E_{g}$, the _conduction band edge falls below $\mu$_, forming an _inversion layer_
- The _width_ of the inversion layer is _controlled_ by $V_{GS}$
	- Typically _narrow_ enough so _quantisation_ is observed

## Bandstructure engineering
- The _confinement_ of electrons can be achieved by _spatial control_ of band structure
- Crystal growth techniques: molecular-beam epitaxy (MBE) and metal-organic chemical vapour deposition (MOCVD), to grow _monolayers_ one by one
	 - Allows layer-by-layer control of _heterostructures_
	 - _High purity_ materials must be used
	 - Electron beam lithography: length-scale of $20-100\,\text{nm}$
	- _Heating_ the substrate allows _lateral motion_ of atoms before incorporation, leading to smoother layers

- The _surface structures_ of a growing crytal can be monitored using _reflection high-energy electron diffraction_ (RHEED), or _transmission electron microscopy_ (TEM)
![[RHEED.png]]

### Two-dimensional electron gas (2DEG)
- The manufacture of a _two-dimensional electron gas_ (2DEG)
	- _Spacers_ prevent positive carriers from scattering with the 2DEG
![[2DEG.png|700]]
- Electrons inhabit a _potential well_ in the $z-$direction, and hence the wave-functions are of the form:
$$\Phi(\boldsymbol{r},z)=\phi_{n}(z)\exp(i\boldsymbol{k}\cdot \boldsymbol{r})$$
- Where $\boldsymbol{k}$ and $\boldsymbol{r}$ are _two-dimensional_
- States in the $z$ direction are _sub-bands_

### 2DEG in a magnetic field
- With a _perpendicular magnetic field_, the density of states splits into _spin-split pairs_ of [[Charged Particles#Landau levels|Landau levels]]
$$E_{i}=\left( i+\frac{1}{2} \right)\hbar\omega_{c} \hspace{1.5cm}\omega_{c}=\omega_{L}=\frac{eB}{m}$$
- The _spin splitting_ is determined by the $g-$factor:
$$\Delta E_{s}=g\mu_{B}B$$
- The original states will _condense_ into nearest Landau level
	- As $B$ increases, the highest Landau levels become _depopulated_

- Each Landau level has the _same degeneracy_
- Let the _occupancy_ of a Landau level _per unit area per spin_ be $n_{L}$
- The _average density of states_ must be _equal_ to the one in the $B\to 0$ case
	- In 2D, $g(E)=\frac{m}{\pi \hbar^{2}}$
- Therefore, the _degeneracy of a single Landau level per unit area_ is:
$$g(E)=\frac{2n_{L}}{\hbar\omega_{c}} \implies n_{L}=\frac{m\omega_{c}}{2\pi \hbar}=\frac{eB}{h}$$

- _Alternatively_, consider that each $h/e$ of flux _enclosed_ gives _one state_ (the [[Charged Particles#The Aharanov-Bohm Effect|Aharonov-Bohm Effect]]), then the number of states per unit area is $BA$ divided by $Ah/e$:
$$n_{L}=\frac{eB}{h}$$

- For $\nu$ occupied Landau levels at $B_{1}$:
$$n_{e}=\frac{\nu eB_{1}}{h}$$
### Shubnikov-de Haas effect
- If the field is _increased_, the highest level can be _depopulated_, so that electrons are _redistributed_
$$n_{e}=\frac{e}{h}\left( \frac{1}{B_{1}}-\frac{1}{B_{2}} \right)^{-1}$$
- The depopulation of Landau levels is _periodic_ in $1/B$
	- Similar to the [[#Quantum oscillations|de Haas van Alphen effect]]

- If the Fermi level is _inside_ a Landau level, the 2DEG behaves as a _conductor_ 
	- Electrons can _backscatter_
- If the Fermi level is inside a _gap_, the 2DEG behaves as an _insulator_ in the _bulk_
	- Except for _edge states_
- At _low temperatures_ $k_{B}T\ll \hbar\omega_{c}$, depopulation affects the _resistance_, making it _oscillate_
	- The Shubnikov-de Haas effect
![[Shubnikov-de Haas.png|400]]

### Quantum Hall effect
- Measuring the _Hall effect_ for Shubnikov-de Haas oscillations:
$$R_{H}=\frac{V}{I}=\frac{B}{n_{e}e}$$
- The Hall voltage forms _plateaus_ when there are _full Landau levels_
![[Quantum Hall effect.png|500]]
- This is the _integer quantum Hall effect_
$$G=\frac{dI}{dV}=\frac{\nu e^{2}}{h}\hspace{1.5cm}\nu \in\mathbb{N}$$
- Electrons travel in _edge states_ within bulk gaps:
![[IQHE edge states.png]]

### Fractional quantum Hall effect
![[Fractional quantum Hall effect.png]]
- Electrons form _composite fermions_ as _quasi-particles_ with a _fractional effective magnetic field_
	- Example: two flux quanta $h/e$ captured by each electron, so effectively $\nu=1/2$
- Observed for _very high mobility_ samples

## Quantum semiconductor devices
### Creation: lithography
![[Lithography.png]]
- Metals are coated with a _polymer "resist"_
	- Polymer is broken into _shorter units_ using UV light
- Metal is _deposited_ on the surface after evaporation
- The resist is _dissolved_ so the metal on it _lifts off_

- Can be used to create _1D channels_ from split gates, as the _negative voltage_ on metal gates can be used to _repel electrons_
	- _Arbitrary patterns_ are possible
![[Split gate.png|500]]
### 1D quantum wires
- Like waveguides, _standing waves_ tend to form across the wire, with _quantised energies_
- There are _sub-bands_ for each energy as the electron is a _free particle along the wire_
	- The $z-$direction is already quantised
	- The gate voltage can be made more _steep_ to "squeeze" the sub-bands and _increase energy spacing_
![[Sub-band squeezing.png]]
- Each sub-band has the _same conductance_
	- There is _no scattering_ between each sub-band
- This creates a _quantised conductance_
- Using the _density of states_ in 1D $n=$
![[1D quantised conductance.png]]
$$\Delta I= \int  \, dx $$
- For $\nu$ sub-bands, and 2 _spin orientations_:
$$G=\frac{2\nu e^{2}}{h}$$
### Anti-dots
- A _potential hill_ (anti-dot) in the middle has _circulating edge states_
![[Anti-dot.png]]
- _Each trajectory_ has a set of _standing waves_ with its own energy levels
	- From the [[Charged Particles#The Aharanov-Bohm Effect|Aharonov-Bohm effect]], states must enclose _multiples_ of $e/h$ in magnetic flux
![[Antidot oscillations.png|400]]
- Resistance will _oscillate_ as there is an _additional phase_ of $2\pi$ around the loop

### 0D quantum dots
- Confine a _fixed number_ of electrons _between tunnel barriers_
- Due to the confinement, there are _quantised energies_
- The energy required to _charge up_ the dot is typically large $(\gg k_{B}T)$
![[Quantum dot.png|400]]

- For a _small voltage_, current only flows when the _net charge_ on the dot is $\pm e/2$
- The conductance _peaks_ as electrons are loaded into the dot
	- _Coulomb blockade_ oscillations
![[Coulomb blockade.png]]

### Single electron pump
- A _pump_ can _transfer one electron per cycle_
- Can make a _quantised current_
![[Single electron pump.png|400]]
- Mechanism: raising barriers
![[Electron pump mechanism.png]]
- There will be some _tunneling rate_ back to the source
- The _quantised energy levels_ can be made so there is a _large separation in tunneling rates_

### Single photon sources
- An _electron-hole pair_ (exciton) using a _self-assembled quantum dot_
	- Made from $\ce{ GaAs }$ and $\ce{ InAs }$, by molecular-beam epitaxy
	- Electrons and holes are _trapped_ in the band gap
 ![[Single photon source.png|500]]
 ![[Single photon source structure.png|500]]
 - It can be tested using a [[Identical particles and second quantisation#Hanbury Brown and Twiss effect|Hanbury Brown and Twiss]] setup for _photon pair correlation_
![[Single photon HBT.png|500]]
- There can be _polarisation entangled_ pair photon sources

### Quantum cascade lasers
- Semiconductor lasers: _forward biased p-n junctions_, such that _electrons recombine with holes_
- Quantum cascade laser: _inter-subband transitions_ in _quantum wells_
- Pumping: by electrical _biasing_
![[Quantum cascade laser.png|350]]
- The _lowest level_ of one well is the _highest level_ of the next, such that electrons can _tunnel between wells_
- The transition from $\ket{1}$ to $\ket{0}$ is _phonon assisted_, making it _faster_ than $\ket{2}$ to $\ket{1}$ which _emits_ the photon
- Each electron emits up to $\sim 80$ photons
	- Conventional diode lasers: 1 photon per electron
- Wavelength: $\sim 1\,\mu\text{m}$ (infrared)

- The _terahertz_ regime: between infrared and visible light, done using cascade lasers

# Collective phenomena
- Accounting for _interactions_ between particles, including _summing over_ interactions between _all pairs of electrons and ions_
	- Order of magnitude: $\sim 10^{23}$ particles
	- _Approximations_ have to be made

- Interactions give rise to _collective phenomena_
- _Symmetry breaking_ will give _quasi-particles_
	- Crystal structure breaks _translational invariance_, giving _phonons_
	- Electrons and holes: Fermi liquids
	- Composite fermions: [[#Fractional quantum Hall effect]]
	- Spin waves: _magnetism_
	- Cooper pairs: _super-conductivity_

## Electronic instabilities
- Most solids have complicated structures
- _Close-packed_ structures are relatively _rare_

- Typically, chemical potential is in a _gap_
	- Occupied states are _lowered_ in energy, unoccupied states go up
- Like in the [[#Nearly-free electron approximation]], this occurs at _BZ boundaries_

- The _Peierls transition_ occurs for a _1D chain of atoms_
- Lattice constant $a$, with $k_{F}$ in the middle of a band
- It becomes an _insulator_ when an _external potential_ is applied, with periodicity $2\pi/Q$ where $Q=2k_{F}$, as there is an _energy gap_ on the Fermi surface

- The _same effect_ occurs with a _periodic lattice distortion_ with the same periodicity:
	- Assume the _amplitude_ $u_{0}\ll a$
$$R_{n}=na+u_{0}\cos(Qna)$$
- The generated _Fourier component_:
	- $g_{Q}$ is an _electron-phonon coupling_ constant
$$V_{Q}=g_{Q}u_{0}$$

- Overall, there is an _energy lowering_
$$E_\text{elec}=$$
![[Peierls distortion.png|500]]
- This results in an _electric charge modulation_, known as a _charge density wave_
- For total energy, model interactions as _springs_:
$$E_\text{tot}=$$
- There is a _minimum_ at non-zero displacement, so the system _lowers energy_

- This is a [[Classical Field Theory#Symmetry breaking|spontaneous symmetry breaking]]

- Metals with _strongly anisotropic structures_ are prone to forming charge density waves
- Transition occurs at _lower temperatures_
- Can be measured with _Bragg scattering_
	- _Widely spaced_ peaks from unit cell
	- Less intense peaks from charge density waves
- The two periods are _unrelated_ (determined by $a$ vs $k_{F}$)

- Onset can be determined using _phonon spectra_
- There will be an _acoustic branch_ that has _zero stiffness at_ $q=2k_{F}$
	- Takes _no energy_ to distort lattice (already distorted)

## Magnetism
- _Classically_, materials _cannot be magnetic at thermal equilibrium_
	- Bohr-van Leeuwen theorem
- Materials are magnetic due to _discrete orbital/spin angular momenta_ in particles
- Materials can be _diamagnetic, paramagnetic, or magnetically ordered_

- Diamagnetic: $\chi<0$, induced magnetism is _opposite to applied field_, $|\chi| \sim 10^{-5}$ 
	- _Superconductors_ are _perfect diamagnets_ with $\chi=-1$
	- Diamagnets can be _levitated_ in a stable equilibrium

- Paramagnetic: $\chi>0$, induced magnetism _aligns with applied field_, $10^{-6}<\chi<10^{-1}$
- Below a _critical temperature_, magnetic dipoles will be _aligned_

- Ferromagnetic: dipoles _aligned_ to give a _permanent magnetic field_
- Anti-ferromagnetic: dipoles _anti-aligned_

![[Magnetism types.png]]
### Paramagnetism

#### Semiclassical case
- A _semiclassical description_: _no discrete states_
- Let a magnetic moment $\boldsymbol{\mu}$ be at an angle $\theta$ relative to the applied field
$$E=-\boldsymbol{\mu}\cdot \boldsymbol{B}=-\mu B\cos \theta$$
- The _probability_ of it being in angle $\theta\to\theta+d\theta$
$$P(\theta)d\theta \propto\exp\left( \frac{\mu B\cos\theta}{k_{B}T} \right) \frac{2\pi \sin\theta\,d\theta}{4\pi}$$
- _Normalising_, the _average magnetic moment_ is given by the _Langevin function_:
	- $y=\mu B/k_{B}T$
$$\frac{\langle \mu_{z} \rangle}{\mu}=\coth y-\frac{1}{y}=\frac{M}{M_{s}}$$
- There is a _saturation magnetisation_ $n\mu$ where $n$ is the number of dipoles
- Magnetisation as $y\gg 1$

- As $y\to 0$, $M/M_{s} \to y/3$
- From this:
$$\chi=\frac{n\mu_{0}\mu^{2}}{k_{B}T}$$
- The _Curie law_: proportional to _inverse temperature_

#### Quantum case
- Quantum system: $J=1/2$
- Magnetic moments $\pm \mu_{B}$
$$\langle g\mu_{B}m_{J} \rangle = \mu_{B}\tanh\left( \frac{\mu_{B}B}{k_{B}T} \right) \implies \frac{M}{M_{s}}=$$
- For _small fields_

#### General solution
- The _Brillouin function_:
$$\frac{M}{M_{s}}=B_{J}(y)=$$
- Can be used to _measure_ $J$

### Magnetism in materials
- Typically, there is _finite magnetism_ when applied fields are absent
- Interaction energy between _two dipoles_:
$$U_\text{dipole}\approx \frac{\mu_{0}m^{2}}{4\pi r^{3}}$$
- A typical value for $a\approx 0.2\,\text{nm}$ and $m=\mu_{B}$ gives $40\,\mu \text{eV}$, corresponding to $T<1\,\text{K}$
- _Real materials_ have much higher $T$
- Explanation comes from _Pauli exclusion_

### Role of exchange interaction
- Consider two electrons in _orthogonal orbitals_ $\ket{a},\ket{b}$
- They are _indistinguishable_, and are fermions:
$$\Psi(\boldsymbol{r}_{1},\boldsymbol{r}_{2})=-\Psi(\boldsymbol{r}_{2},\boldsymbol{r}_{1})$$
- Either:
	- _Symmetric_ spatial function with spin _singlet_
	- _Anti-symmetric_ spatial function with spin _triplet_
- The electron _Hamiltonian_, with _interaction part_ $H_{1,2}=V(\boldsymbol{r}_{1}-\boldsymbol{r}_2)$
$$H=H_{0}+H_{1,2}$$
- Denoting energies as:
$$\displaylines{E_{0}=\braket{ ab | H|ab } =E_{a}+E_{b}+E_\text{Coul} \\ E_\text{Coul}=\braket{ ab|H_{12} | ab }\hspace{1.6cm} E_\text{ex}=\braket{ ba|H_{12} | ab } }$$
- $E_\text{ex}$ is the _exchange term_
- For _short range interactions_ $V\to \delta(\boldsymbol{r}_{1}-\boldsymbol{r}_{2})$, $E_\text{Coul}\to E_\text{Ex}$
- The _singlet_ and _triplet_ energies:
$$\displaylines{E_{s}=\frac{1}{2}\braket{ ab+ba|H | ab+ba }=E_{0}+E_\text{ex} \\ E_{t}=\frac{1}{2}\braket{ ab-ba|H | ab-ba }=E_{0}-E_\text{ex} } $$

- For $n$ particles, the _anti-symmetric_ spatial wave-function has _nodes_ when $\boldsymbol{r}_{i}=\boldsymbol{r}_{j}$
- On _average_, the particles are _further apart_ from each other, hence experience _less repulsion_, and are _lower in energy_

- When orbitals are _orthogonal_, $E_\text{ex}>0$, so the _triplet_ is lower in energy
- If the orbitals are _not orthogonal_, $E_\text{ex}$ _can be negative_, so the _singlet_ is lower in energy
	- Not orthogonal when they belong to _different atoms_ (e.g. molecular hydrogen)

- This means _higher ordering temperatures_ in ferromagnetism

### Heisenberg Hamiltonian
- The _spin interaction_ between two electrons can be written as $\boldsymbol{S}_{1}\cdot \boldsymbol{S}_{2}$:
$$\displaylines{\boldsymbol{S}_{1}\cdot \boldsymbol{S}_{2}=\frac{1}{2}(S^{2}-S_{1}^{2}-S_{2}^{2})=\frac{1}{2}S^{2}-\frac{3}{4}\hbar^{2} \\ (\boldsymbol{S}_{1}\cdot \boldsymbol{S}_{2})_{s}=-\frac{3}{4}\hbar^{2}\hspace{1.5cm}(\boldsymbol{S}_{1}\cdot \boldsymbol{S}_{2})_{t}=\frac{1}{4}\hbar^{2}}$$
- The _spin Hamiltonian_ can be written as:
$$H_\text{spin}=\frac{1}{4}(E_{s}+3E_{t})-(E_{s}-E_{t}) \frac{\boldsymbol{S}_{1}\cdot \boldsymbol{S}_{2}}{\hbar^{2}}$$
- Defining $J=(E_{s}-E_{t})/2$, and shifting the _zero_ of energy:
$$H_{2}=-2J \frac{\boldsymbol{S}_{1}\cdot \boldsymbol{S}_{2}}{\hbar^{2}}$$
- It favours _parallel spins_ for $J>0$, and _antiparallel spins_ for $J<0$

- Extending to a _collection of spins_, summing over _nearest neighbours_ $\braket{  i,j  }$
$$H_\text{Heisenberg}=-\sum_{\braket{  i,j  } }J_{ij} \frac{\boldsymbol{S}_{i}\cdot \boldsymbol{S}_{j}}{\hbar^{2}}$$
- This only depends on the _relative orientation_ of the spins
	- Unless there is coupling to _orbital angular momentum_

### Super-exchange
- Let the magnetic moments in a solid be _separated_ by insulator ions
	- Example: $\ce{ MnO }$, with $\ce{ O^{2-} }$ being the _insulator_

- Explanation
- Favouring _anti-alignments_
![[Superexchange.png]]
- From _second order perturbation theory_, the exchange is of order
$$J\sim -\frac{t^{2}}{U}<0$$
- $t$ is the _hopping element_ between the magnetic and non-magnetic ions
- $U$ is the _Coulomb repulsion energy_ for the moment

- On a _lattice_, it favours an _anti-ferromagnetic_ state
- Magnitude: $10^{0}-10^{2}\,\text{K}$
- There can be a _phase transition_ from ordered states to a _paramagnetic disordered_ state
![[MnO transition.png]]
- When spins are _anti-aligned_, there is a _magnetic unit cell_ which is _twice the size_ of the crystal unit cell
- This is _detectable_ with _neutron diffraction_
	- The _neutron magnetic moments_ can _couple_ to atomic magnetic moments

### Band magnetism
- Electron _bands_ can respond to magnetic fields (_Pauli paramagnetism_)
- Let there be a _Fermi gas_ with dispersion $\epsilon_{\boldsymbol{k}}$ in a magnetic field $B_{a}=\mu_{0}H$
- The _spin-up_ and _spin-down_ electrons will be split by [[Atomic and molecular physics#Zeeman effect|Zeeman energy]] with $g_{s}=2$
$$\epsilon_{\boldsymbol{k}\uparrow}=\epsilon_{\boldsymbol{k}}-\mu_{B}B_{a}\hspace{1.5cm}$$
- The _chemical potential_ is the _same_ for both spins, so there is a _transfer of carriers_ between bands
- There is a _population imbalance_:
	- $g_{V}$ is for _both spins_
	- Assume the splitting is _small_ so the DoS is _constant_
$$n_{\uparrow}-n_{\downarrow}=2\mu_{B}B_{a}\left( \frac{1}{2}g_{V}(E_{F}) \right)=\mu_{B}B_{a}g_{V}(E_{F})$$
- The _magnetisation_ $M$ is given by:
$$M=\mu_{B}(n_{\uparrow}-n_{\downarrow})$$
- This gives the _spin susceptibility_:
$$\frac{M}{H}=\chi_{\sigma}=\mu_{0}\mu_{B}^{2}g_{V}(E_{F})$$
- Unlike the [[#Semiclassical case|Curie law]], it is _temperature-independent_
	- For _higher temperatures_, the _broadening_ of the Fermi distribution starts to be significant
- Energy scales:
### Band magnetism with interactions
- Consider the _Stoner-Hubbard model_, where there is an _energy penalty_ for lattice sites which are _doubly occupied_ (with both up and down electrons)
$$H_\text{int}=\sum_{i}Un_{i\uparrow}n_{i\downarrow}$$
- Let there be _average occupancies per atom_ $\bar{n}_{i\uparrow}$ and $\bar{n}_{i\downarrow}$
- With the _mean-field approximation_:
$$\epsilon_{\boldsymbol{k}\uparrow}=\epsilon_{\boldsymbol{k}}+U\bar{n}_{\downarrow}-\mu_{0}\mu_{B}H\hspace{1.5cm}$$
- It is _analagous to a magnetic field_, known as an _exchange field_
	- "Book-keeping" to account for _Coulomb interactions_

- The average spin density:
$$\frac{N}{V}(\bar{n}_{\uparrow}-\bar{n}_{\downarrow})=[U(\bar{n}_{\uparrow}-\bar{n}_{\downarrow})+]$$
- Using the _density of states oer atom_ $g_{V}=(N/V)g$:
$$\chi_{\sigma}=$$
- The susceptibility will _diverge_ if the _Stoner criterion_ is satisfied:
	- Onset of _ferro-magnetism_
$$\frac{Ug(E_{F})}{2}>1$$
- The density of states is of order $E_{F}$
- Kinetic energy

### Local moment magnetism
- $d-$ or $f-$band metals
- There are _localised electrons_ from the _tightly-bound_ orbitals, with _itinerant/delocalised_ electrons from the $sp$ bands
- The itinerant bands are _weakly spin-polarised_ due to _large kinetic energies_
- They have an _induced spin polarisation_ due to interaction with _core spins_
- This is then _transmitted_ to other ions which will attempt to _align_

- This creates _Friedel oscillations_ in _spin density_, which _decay in distance_ and _oscillate_ with period $\pi/k_{F}$
	- The _RKKY interaction_

### Magnetic order and the Weiss exchange field
- A _phenomenological equation of state_:
	- _Ignore_ the _vector nature_ of the fields
$$H=aM+bM^{3}$$
- $a$ is the _inverse susceptibility_
$$a=\chi^{-1}=$$
- $b$ ensures magnetisation _tends towards saturation_ for high fields

- A _ferro-magnetic_ interaction needs a _non-zero_ $M$ for _zero_ $H$
- Only possible for _negative_ $a$

# Fermi liquid theory
- The above treatment of _conduction electrons_ treats them as a _degenerate_ [[Advanced statistical mechanics#The Fermi gas|Fermi gas]]
- The many-particle problem is _separated_ into _single-particle_ states, as the wave-function is written as a _Slater determinant_ of single-particle wavefunctions
- This _ignores electron-electron correlations_
- i.e. it is assumed that $\langle \boldsymbol{r}_{1} \boldsymbol{r}_{2}\rangle = \langle \boldsymbol{r}_{1} \rangle\langle \boldsymbol{r}_{2} \rangle$

## Problems with the Fermi gas
- With _strong electron-electron interactions_, the electron motion must be _correlated_
	- Example: [[#Thomas-Fermi screening]], where electrons move to _screen_ charged impurities
- For any given electron, _other electrons must execute a correlated screening motion_, which _reduces_ the particle density _near the first electron_
- Thia also _reduces_ the effective range of the _Coulomb potential_, implying _correlated motions_ between electrons
- Becomes significant in _extreme conditions_ (Example: $\ce{ ^{3}He }$)

- In most cases, _single particle theories_ (e.g. band structures) are still _successful_
### Helium 3
- $\ce{ ^{3}He }$ is a _fermionic particle_ which _does not solidify at zero temperature_ at _atmospheric_ pressure
	- _Low mass_ of the particles boosts _zero-point_ motion, to a point that the _weak inter-atomic interactions_ cannot cause freezing
- An _uncharged analogue_ of electrons in solids as a _quantum fluid_
- Due to _hard core repulsion_ and _weak van der Waals interaction_, helium atoms at _low temperature_ act as a _close-packed array_ of hard spheres
- _Not solid_, but atoms are _strongly correlated_

- _Heat capacity per mole_ [[Advanced statistical mechanics#Away from absolute zero|at low temperatures]] behaves as:
$$\frac{C_{m}}{T}\approx \frac{\pi^{2}}{2} \frac{R}{T_{F}}\hspace{1.5cm} T_{F}=\frac{E_{F}}{k_{B}}=\frac{\hbar^{2}}{2mk_{B}}(3\pi^{2}n)^{2/3}$$
- There is a _predicted increase_ in $T_{F}$ as _pressure rises_
- For $\ce{ ^{3}He }$, $C_{m}/T$ is still _constant w.r.t._ $T$ is a _reduction_ in $T_{F}$
![[3He heat cap.png|300]]
- This is due to a _rise in effective mass_, due to _stronger interactions_ as pressure rises
- _Fermi gas relations hold_, but with a _renormalisation of parameters_

## Collective excitations and the Fermi liquid
- Consider _deviations_ of a many-particle system from the _ground state_
- Example: _phonons_ as _collective deformations_ of a lattice, forming a _Bose gas_
	- _Normal modes_ labelled with $\boldsymbol{k}$ with corresponding $\omega(\boldsymbol{k})$
	- _Harmonic oscillations_ can be [[Quantum Harmonic Oscillator|created and annihilated]]
	- $a,a^{\dagger}$ for phonons follow _Bose statistics_, so there can be _multiple excitations_ of the same $\boldsymbol{k}$ state
	- A _collection_ of atoms (fermions or bosons) will form a _Bose gas_

- Analagous to phonons, the _collective excitations_ in a _liquid_ of _strongly interacting fermions_ will behave like a _weakly interacting Fermi gas_
- Hence, the _single particle description_ still _applies_, but requires _modifications_ for collective fermionic excitations

### Adiabatic continuity
- Let there be a collection of _non-interacting electrons_, forming a _Fermi gas_, and at its _ground state_ (filled up to the Fermi surface)
- _Interactions_ are _gradually_ turned on
- _Adiabatic continuity_ dictates that the _energy eigenstates_ can still retain their original _labels_
	- Assuming _no energy crossings_
- Therefore, _excitations_ in the Fermi liquid _follow the same laws as the Fermi gas_
![[Adiabatic continuity.png|400]]
- The _one-to-one_ correspondence between the two systems guarantees that the _volume of the Fermi surface is unchanged_ (Luttinger's Theorem)
- The theorem _fails_ if _energy levels do not cross_

- _Not all_ interacting Fermi systems can be treated as _Fermi liquids_

### Landau Fermi liquid
- Label _excited states_ of the _interacting_ system using _quantum numbers of the non-interacting system_ ($\boldsymbol{k}$, spin, band index, etc.)
- This is referred to as a _quasi-particle_
- It resides _outside the Fermi surface_, leaving behind _quasi-holes inside_ the Fermi surface 
- The _total energy_ of the interacting system can be expressed as a _functional_ of the occupation numbers of all states
- At _low temperatures_ with few excitations, this can be _approximated_:
$$E[n_{\boldsymbol{k}}]=\sum_{\boldsymbol{k}}n(\boldsymbol{k})\epsilon(\boldsymbol{k})+\frac{1}{2}\sum_{\boldsymbol{k},\boldsymbol{k}'}f(\boldsymbol{k},\boldsymbol{k}')n(\boldsymbol{k})n(\boldsymbol{k}')$$
- $\epsilon(\boldsymbol{k})$ is the _energy of quasiparticles_ for wavenumber $\boldsymbol{k}$
- $f(\boldsymbol{k},\boldsymbol{k}')$ is the _interaction function_

## Quasi-particle scattering
- Quasi-particles _outside_ the Fermi surface can _scatter_ by creating an _electron-hole pair_
![[Quasi-particle scattering.png]]
- From _Pauli's exclusion principle_, $\epsilon_{1},\epsilon_{2}>0$
- The energy required to _excite_ the hole is $-\epsilon_{3}>0$
	- Measured _downwards from_ $E_{F}$
- By _conservation of energy_:
$$\epsilon=\epsilon_{1}+\epsilon_{2}-\epsilon_{3}$$
- $\epsilon_{1}$ and $\epsilon_{2}$ are _chosen freely_ from $0$ to $\epsilon$, which fixes $\epsilon_{3}$
- The number of _available final states_ is then $\propto\epsilon^{2}$, so the _scattering rate_ $\Gamma$:
$$\Gamma \propto\epsilon^{2}$$

- Therefore, _quasi-particles close to the Fermi surface_ $(\epsilon\to 0)$ will _scatter extremely rarely_, and be able to travel _long distances_
	- Despite _strong interactions_ with other particles
	- _Protection_ by Pauli exclusion (very few empty states to scatter to)
- Example: _high mean free path_ in low temperature copper
	- _Current_ is carried by a _collective mode_ of the Fermi system
	- The quasi-particle is a _dressed excitation_, involving a _correlated motion_ of the added electron in a _many-particle background_

- When $\Gamma > \epsilon/\hbar$, quasi-particles are _no longer well-defined_, as they _scatter before_ the wave-function undergoes a _full oscillation_
- They are _over-damped_
- Fermi liquid theory is only for _low-energy excitations_, and $k_{B}T\ll E_{F}$
	- Typically, $E_{F}/k_{B}\sim 10^{3}\,\text{K}$

### Near the Fermi surface
- _Fermi liquid quasiparticles_ only defined _close to the Fermi surface_, where they have a _large enough lifetime_
- The quasiparticles are _labelled_ by $\boldsymbol{k}$
- There is a _vacuum ground state_, where low energy excitations are _fermionic particles and holes_, on _either side_ of a boundary surface in $\boldsymbol{k}-$space
	- Comparison to _Fermi gas_, which has a _filled Fermi sphere_
![[Fermi gas vs liquid.png|420]]

### Quasiparticle spectral function
- Consider the _response_ of the addition/removal of a quasi-particle

- In a _non-interacting system_, for a particle in _eigenstate_ $\epsilon(\boldsymbol{k})$, the wave-function is:
$$\psi_{\boldsymbol{k}}(\boldsymbol{r},t)=\psi_{\boldsymbol{k}}(\boldsymbol{r})\exp\left( -\frac{i\epsilon_{\boldsymbol{k}}t}{\hbar} \right)$$
- $\psi_{\boldsymbol{k}}$ is the _Bloch wavefunction_, with _time-dependent factor_ $\exp(-i\omega_{\boldsymbol{k}}t)$
- In _Fourier space_:
$$\psi_{\boldsymbol{k}}(\boldsymbol{r},\omega)=2\pi \psi_{\boldsymbol{k}}(\boldsymbol{r})\delta(\omega-\epsilon_{\boldsymbol{k}}/\hbar)$$
- It has _non-zero spectral weight_ at $\omega=\epsilon_{\boldsymbol{k}}/\hbar$, given by the _electron spectral function_:
$$A(\boldsymbol{k},\omega)=\delta(\omega-\epsilon_{\boldsymbol{k}}/\hbar)$$

- In an _interacting system_, _scattering_ will cause $A(\boldsymbol{k},\omega)$ to _spread out_ in energy
- Due to interactions, _replace_ $\epsilon_{\boldsymbol{k}}$ to a _renormalised_ $\tilde{\epsilon}_{\boldsymbol{k}}$
- _Mass renormalisation_:
$$\frac{m^{*}}{m}=\frac{\epsilon_{\boldsymbol{k}}}{\tilde{\epsilon}_{\boldsymbol{k}}}$$
- _Quasi-particles_ can _scatter_ from other quasi-particles, or create _electron-hole pairs_
- The _probability amplitude_ of finding a quasi-particle of momentum $\boldsymbol{k}$ at time $t$ will then _decay exponentially_ with $\Gamma_{\boldsymbol{k}}$
$$\displaylines{\psi_{\boldsymbol{k}}(\boldsymbol{r},t)=\psi_{\boldsymbol{k}}(\boldsymbol{r})\exp\left( -\frac{i\tilde{\epsilon}_{\boldsymbol{k}}t}{\hbar}-\Gamma_{\boldsymbol{k}}t \right) \\ A(\boldsymbol{k},\omega)=-\frac{1}{\pi}\mathrm{Im}\left[ \frac{1}{\omega-\tilde{\epsilon}_{\boldsymbol{k}}/\hbar+i\Gamma_{\boldsymbol{k}}} \right]=\frac{1}{\pi} \frac{\Gamma_{\boldsymbol{k}}}{(\omega-\tilde{\epsilon}_{\boldsymbol{k}}/\hbar)^{2}+\Gamma_{\boldsymbol{k}}^{2}}}$$
- This is the _quasi-particle spectral function_ with _dispersion relation_ $\tilde{\epsilon}_{\boldsymbol{k}}$ and _decay rate_ $\Gamma_{\boldsymbol{k}}$
	- For _long lifetime_ $\Gamma_{\boldsymbol{k}}\to 0$, $A(\boldsymbol{k},\omega) \to \delta(\boldsymbol{\omega}-\epsilon_{\boldsymbol{k}}/\hbar)$

- Let there be a _chemical potential_ $\mu$
- In _equilibrium_ (or $T=0$), one _cannot add fermionic excitations_ at energy $\hbar\omega<\mu$
- For $\hbar\omega>\mu$, $A(\boldsymbol{k},\omega)$ is for _particle-like_ excitations
- For $\hbar\omega<\mu$, $A(\boldsymbol{k},\omega)$ is for _hole-like_ excitations
![[Quasi-particle spectrum.png]]
- For small $\Gamma_{\boldsymbol{k}}$, a _quasi-particle resonance_ at $\hbar\omega=\tilde{\epsilon}_{\boldsymbol{k}}$ has _peak width_ $2\Gamma_{\boldsymbol{k}}$
	- They are _well-defined_ when near the _central frequency_
- There is a _quality factor_ $\tilde{\epsilon}_{\boldsymbol{k}}/\Gamma _\boldsymbol{k}\propto 1/\tilde{\epsilon}_{\boldsymbol{k}}$
	- _Diverges_ as $\epsilon\to 0$
- Quasi-particles are _over-damped_ at high energies

### Tunability of the quasiparticle interaction
- The _interaction term_ causes _change_ in quasi-particle properties w.r.t. the _free electron_
$$\frac{1}{2}\sum_{\boldsymbol{k},\boldsymbol{k}'}f(\boldsymbol{k},\boldsymbol{k}')n(\boldsymbol{k})n(\boldsymbol{k}')$$
- The _effective mass_ $m^{*}$ can be _orders of magnitude_ larger than $m$
- It is _not necessarily_ only Coulomb repulsion
	- Can be _spin-dependent_

- An example of _tunability_ of correlated electron systems
- The effective interaction can be _tuned_ over a wide range by _doping_, or using _electromagnetic fields_

## Heavy fermions
- _Strong interactions_ cause a _high effective mass_
- _Heavy fermion materials_ suggest a high effective mass via coefficients in [[#Heat capacity|heat capacity]], or [[#Magnetism|magnetic susceptibility]], as predicted by Fermi liquid theory
- Typically, $m^{*}\sim 10^{3}m$
- Usual heavy atoms: $\ce{ Ce,Yb, U }$ with _partially filled_ $f$ _orbitals_
- The $f$ states are more _localised_ compared to the other _valence orbitals_, leading to very _narrow bands_
- _Coulomb_ repilsion will _prevent double occupancy_ of the states

- Example: $\ce{ CeCu_{6} }$ heat capacity
![[CeCu6.png|350]]
- Comparing to _copper_, the _low-temperature heat capacity_ is boosted by $\approx 150$
- Consider the _density of states_:
$$g(E_{F}) \propto \frac{1}{v_{F}}\hspace{1.5cm}m^{*}v_{F}=\hbar k_{F}$$
- Increase in $m^{*}$ reflects increase in $g(E_{F})$
- The _heavy fermion state_ only develops at _low temperatures_

- Example: $\ce{ UPt_{3} }$ magnetic susceptibility
![[UPt3.png|350]]
- At _high temperatures_, the susceptibility roughly follows _Curie's law_, as the $f$ electrons act as _local magnetic moments_
- At _low temperatures_, Curie susceptibility tends to a _constant value_
	- _Free spins_ bind to conduction electrons to make heavy fermions

### Renormalised bands
- Consider the _hybridisation_ of $f$ bands with the $s,p,d$ bands, which are more _extended_
	- $f$ orbitals lie _inside_ the $s,p,d$ orbitals
- There is _little_ $f-f$ hybridisation, resulting in a _flat band_

- In the _single electron_ scheme, the $f$ orbitals are _completely full_, and there would be _no heavy fermion behaviour_
![[f bands.png|400]]
- Typically, due to _Coulomb repulsion_, only _one electron_ occupies the $f$ band
- Energy is _re-normalised_, with an _anti-crossing_ once hybridisation is considered
- $dE/dk$ is _much flatter_ at $k_{F}$ to give a _higher effective mass_
- $k_{F}$ also becomes _larger_ than without hybridisation

### Detection by de Haas-van Alphen
- There are different _Fermi surface sheets_, with different _contributions_ to heat capacity
- _Volume_ enclosed by the sheets is used to determine if the electrons act as a Fermi liquid
- _Temperature dependence_ of the _amplitude_ of de Haas-van Alphen measurements will give the _effective mass_ and its contribution to heat capacity
![[Heavy fermion surface sheets.png|400]]
### Tuning the interaction
- The _effective_ interaction can be _tuned_ to determine interactions at _low temperatures_
	- Except the _Coulomb_ interaction
- This gives rise to different _phases_ depending on the ground state
- The ground states can be tuned to be _magnetic_ or _superconducting_
![[Heavy fermion phases.png]]
