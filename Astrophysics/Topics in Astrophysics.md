- Convention for _ideal gas equation of state_:
$$\displaylines{pV=nRT \\ p=\frac{R_{*}}{\mu}\rho T}$$
- Here, $\rho$ is _density_ in $\text{kg m}^{-3}$, and $\mu$ is _molecular mass in_ $\text{kg}$
- $R_{*}=1000R$
	- As te definition of the _mole_ is in $\text{g}$

# Timescales and length scales
- Given some quantity $Q$, the _timescale_ of its change is:
$$\tau=\frac{Q}{|\dot{Q}|}$$
- Likewise, the characteristic _length scale_:
$$L=\frac{Q}{|Q'|}$$
- If a system is observed for some interval $T\ll \tau$, one can consider $Q$ as _static_
- If $T\gg \tau$, one can estimate $Q$ at its _equilibrium_ value

- Example of length scale: atmospheric density
- For some _isothermal atmosphere_, with _speed of sound_ $c$, one gets the density distribution
	- Using the _fluid approximation_, where the mean free path is much _smaller_ than the length scale
$$\rho=\rho_{0}\exp\left( -\frac{gz}{c^{2}} \right)$$
- The _characteristic length scale_ is then $c^{2}/g$
- Once the _mean free path_ $\lambda$ exceeds the length scale, the approximation _breaks down_

- The _stellar discs_ of many galaxies have an _exponential profile_, with differing length scale for each galaxy

- Some systems are _scale-free_
- Consider: 
$$Q=\frac{Q_{0}t_{0}}{t}$$
- One gets $\tau=t$, implying that the time-scale _changes with time_
- This is a _scale-free system_

- Timescale can also be given by _dimensional analysis_

## Different timescales
- Given some _cloud_ of mass $M$ and radius $R$, the _dynamical timescale_ is approximately
$$t_{g}=\left( \frac{R^{3}}{GM} \right)^{1/2}$$
- Examples include _radial infall time_, or some _orbital timescale_

- For _sound crossing_ some medium (hence _propagating changes in pressure_):
$$t_{c_{s}}=\frac{R}{c_{s}}=\frac{R}{\sqrt{ \mathcal{R}_{*}\mathcal{T}/\mu }}$$
- In _magnetised media_, the _magnetic field_ have _wave disturbances_ known as _Alfven waves_, where both _longitudinal and transverse_ waves have speed to the _order_ of:
$$v_{A}\sim \left( \frac{B^{2}}{\rho} \right)^{1/2}\hspace{1cm}t_{A}=\frac{R}{v_{A}}$$

- One can also define a _light speed timescale_ for an object:
$$\tau_{c}=\frac{R}{c}$$
- This is the _delay_ in light crossing an object
- Hence, it is the _minimum timescale_ for _changes in properties_
- Given some timescale $\delta t$, it also _constrains_ the length scale to $c\delta t$

- Reverberation mapping: using _Doppler shift_ and _lag time_ to estimate mass of a black hole (from orbiting _velocities_ of objects)

- If $Q$ is some measure of _energy_, and $\dot{Q}$ is some _thermal/cooling rate_, this gives a _thermal time-scale_
- Typically, $\dot{Q}$ is only for some particular _process_

- For _fluids_, one can define a _collisional timescale_
- Given a _collision cross-section_ $\sigma$, rms speed $v$, and _number density_ $n$, one can define a _mean collision time_ (for a straight line trajectory):
$$\tau=\frac{1}{n\sigma v}$$
- One can define the _opacity_ of an object as the _cross-section per unit mass_:
$$\kappa=\frac{\sigma}{m}$$
- For a _photon_, the mean free path is then:
$$\lambda=\frac{1}{\kappa \rho}$$
- The _optical depth_ of an object is the _number of mean free paths_ in its size $L$:
$$\tau=\frac{L}{\lambda}$$
- The sun is considered a black-body as photons _collide many times_ before they are emitted

- One can define a _diffusional timescale_
- Given a _random walk_ of $N$ steps and mean free path $\lambda$, the _distance travelled_ is:
$$R=\sqrt{ N }\lambda$$
- If the particle speed is $v$, the _average time_ for particles to travel across $R$ is:
$$\tau=\frac{N\lambda}{v}=\frac{R^{2}}{\lambda v}$$
- One can then _estimate the luminosity of the Sun_
- The _time_ the photon takes to escape is:
$$\tau _\text{Sun}=\frac{R_\text{sun}^{2}}{\lambda c}=\frac{R_\text{Sun}^{2}\kappa \rho}{c}$$
- The _energy_ contained is $\sim R_\text{Sun}^{3}\sigma T^{4}$
- This gives the _luminosity_:
$$L=\frac{\sigma cT^{4}R_\text{Sun}}{\kappa \rho}$$
- The _radiant flux_:

- This is _different_ from the _thermal timescale_, as the latter also contains energy from the _matter/gas_ in the Sun (which dominates the thermal energy)
	- The _ratio_ of the two timescales are the ratio of _gas pressure_ to _radiation pressure_

# Distributions
- Given a _probability density function_ $p(q)$, the _probability_ that the quantity is in range $q$ to $q+dq$ is $p(q)\,dq$
	- It is a _linear interval_
- One can define a _probability per logarithmic interval_
	- Constant _fractional width_
$$p(q)\,dq=qp(q)\,d(\ln q)$$
- $qp(q)$ carries information about which part of the distribution _dominates the integrated total_
- Given some _power law distribution_:
$$p(q_\text{min}<q<q_\text{max})\propto q^{-\alpha}$$
- The _integrated total_ is $\propto q^{1-a}$ from $q_\text{min}$ to $q_\text{max}$, matching the expression for $qp(q)$
- The _sign_ of $1-\alpha$ determines _which_ part of the distribution contributes the _most_

- Given the _initial mass function_ (distribution of _stellar mass at birth_)
$$f(m)\,dm\propto m^{-\alpha}\,dm$$
- The _total mass_ is:
$$M=\int f(m)\,dm=m^{2-\alpha}\Big|_{m_\text{min}}^{m_\text{max}} $$
