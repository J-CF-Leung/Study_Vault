## Intrinsic band structure
- The _intrinsic_ property of a conductor are the properties when the material is _pure_

- In a typical [[Nearly Free Electron Model|divalent metal]], there are both _electrons and holes_ even at $T=0$
- They originate from the _Fermi contour_ crossing into the _zone boundary_

- In a _semiconductor_, at $T=0$, the _valence band is full_ and there are _no available charge carriers_
- There is a _small band gap_ between the valence and conduction bands, so electrons can be _thermally excited_ into the latter
- Therefore, a semiconductor has _temperature-dependent conductivity_

- These properties can be modified by introducing _impurities_, making an _extrinsic semiconductor_

## Doping
- Consider _silicon_ $\ce{Si}$, a typical semiconductor with a _full valence band_
- One can _dope_ the material with _phosphorus_ $\ce{P}$, which has an _extra valence electron_

- The _structure_ of the material is unchanged, and there is an _extra electron_
- The extra electron is then subject to the _periodic potential of the nuclei_

- The electron can be _ionised_ (separated from the nucleus), and sit in the _conduction band_
- It can also _remain bound_ and _localised_ at the $\ce{P}$ atom

### Hydrogenic state
- There is an electrostatic potential resulting from _binding energy_ between the electron and the $\ce{P+}$ ion
- The energy sits _below the conduction band_, with _no $k-$dependence_
- Its _energy below the conduction band_ as well as the _radius_ are given by a _hydrogen atom-like formula_ but replacing constants to account for _the effects of the surrounding lattice_
$$\displaylines{\epsilon_0\to\epsilon_r\epsilon_0 \hspace{1cm} m_e\to m_e^*\\ E_n=-\frac{m_e^*e^4}{2\hbar^2(4\pi\epsilon_r\epsilon_0)^2}\frac{1}{n^2} \hspace{1cm} r_n=\frac{\hbar^2}{m_ee^2}(4\pi\epsilon_r\epsilon_0)n^2} $$
- Typical values:
	- Energy _much smaller than hydrogen atom_
	- Radius _much larger than atomic spacing_

- As the electrons are _less tightly bound_, at _higher dopant concentrations_, the wavefunctions can overlap and form an _impurity band_


### n-type and p-type doping
- In _n-type_ doping, _electrons_ are _donated into the conduction band_
- Bound states are formed _below the conduction band_, but the electrons can also be _ionised into the conduction band_ while the dopant atom forms a _cation_
	- The bound state: the excess elctron _bound to_ a _positive ion_
![[n-type doping.png]]

- Doping with a _p-type_ dopant forms a _hole_
- The hole can form _bound states above the valence band_, but holes can also be _ionised_ to give a _hole in the valence band_ while the p-type dopant forms an _anion_
	- The bound state: the _hole_ is _bound to_ a _negative ion_
![[p-type doping.png]]

- Typically, for $\ce{Si}$, typical dopants are:
	- n-type: $\ce{P}$ or $\ce{As}$
	- p-type: $\ce{Al}$ or $\ce{B}$

![[Donor and acceptor states.png]]

- The typical gap energy is _much larger than_ $k_BT$
- When _doped_, at room temperature, there will be _a significant amount of charge carriers_

## Chemical potential
- When $\varepsilon=\mu$, with the Fermi-Dirac distribution:
$$p(\varepsilon=\mu)=\frac{1}{2}$$
- Consider the _chemical potential_ of the _electrons_ as a function of _temperature_

- In an _n-type_ semiconductor:
- At _absolute zero_, as the conduction band is _empty_ while the _donor states_ are full, $\mu$ is _just below the conduction band_
- As electrons from the donor states are _excited_ into the conduction band, the _chemical potential moves down_
![[Moving chemical potential.png]]

- In a _p-type_ semiconductor:
- At _absolute zero_, as the valence band is _full_ while the acceptor states are _empty_, $\mu$ is _just above the valence band_
- As the electrons from the valence band are _excited_ into the acceptor states, the _chemical potential moves up_

- In both cases, the chemical potential _moves towards the middle of the gap_
- At _high temperatures_, electrons can _be excited from the valence band directly to the conduction band_, so donor/acceptor states are _less important_

# Semiconductor devices

## p-n junction

### Neutral behaviour
- Bring _n-type_ and _p-type_ materials into _contact_
	- They are initially _charge neutral_ 
- As electrons and holes _diffuse across the barrier_, there is a _depletion region_ formed at the interface as the electrons and holes _cancel out_, and there are _no charge carriers_

- As there is _charge separation_, there is an _electric field_ which will eventually _stop charge carrier flow_
- There is a _contact potential_ that balances the difference in $\mu$

- Eventually, the _chemical potentials_ will _equalise_ across the system
![[p-n junction contact.png]]

### Forward bias
- A field is applied to _force majority carriers towards the junction_
- This gives _good electrical conductivity_

### Reverse bias
- A field is applied to _force majority carriers away from the junction_
- This gives _very poor electrical conductivity_

### Generation and recombination currents
- With a _forward bias_, the majority carriers _diffuse then recombine_ in order to _maintain equilibrium_
- The diffusion creates a _recombination current_

- With a _reverse bias_, the _minority carriers_ diffuse and recombine instead
- This creates a _generation current_

- The addition of a bias increases $\mu$ to $\mu+eV$:

$$p_V(\varepsilon)\approx p_0(\varepsilon)\exp(eV/k_BT)$$
### I-V Characteristic
- At _zero bias_, the currents _cancel_
- Bias _does not change_ the generation current $I_{0,e}$
- A _forward bias_ will allow _a number of electrons_ $\propto \exp(eV/k_BT)$ to _cross_ the junction, making a _recombination current_
- Hence, the _total current_ varies as:
$$I=I_0\left[\exp\left(\frac{eV}{k_BT}\right)-1\right]$$
![[Diode I-V characteristic.png]]

- Hence, a diode is a _one-way conductor_