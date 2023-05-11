- Consider a _dilute monoatomic gas_
	- The _average distance_ between the particles is _much bigger_ than their size
	- There are only _translational_ degrees of freedom
- The gas particles _do not interact_ with each other

- Particles can only _exchange energy_ via _collisions_
- The system remains in _equilibrium_

- Every particle behaves as if it's in equilibrium with a _reservoir_ of temperature $T$
- The reservoir is simply _every other gas particle_
- Hence, one can use results from the [[Statistical thermodynamics#Statistics, density of states, and ensembles|canonical ensemble]], where the _energies_ of each particle obey the [[Statistical thermodynamics#Boltzmann Distribution|Boltzmann Distribution]]

# Distribution of speeds and velocities

## 1 dimensional case
- Each _component_ of velocity behaves _independently_
- Hence, one can _derive the 3D distribution from the 1D distribution_
- It is useful for finding the pressure on a _flat wall_

- Define the _1D velocity distribution function_ $f_{1D}(v_x)$ such that $f_{1D}\,dv_x$ is the _fraction of gas particles_ travelling in velocity range $[v_x,v_x+dv_x]$
- As the states are _equally spaced_ in velocity:
$$f_{1D}(v_x)\propto \exp\left(-\frac{mv_x^2}{2kT}\right)$$
- By _normalising_ the distribution function:
$$\displaylines{\int_{-\infty}^\infty f_{1D}(v_x)\,dv_x=1 \\ f_{1D}(v_x)=\sqrt{\frac{m}{2\pi k_BT}}\exp\left(-\frac{mv_x^2}{2k_BT}\right)}$$

- Since the distribution is _even_:
$$\mean{v_{x}}=0$$
- As for the average of the _magnitude:
$$\mean{|v_x|}=2\int_0^\infty v_x\,f_{1D}(v_x)\,dv_x=\sqrt{\frac{2k_BT}{\pi m}}$$
- One can also find the _root-mean square_:
$$\mean{v_x^2}=\int_{-\infty}^\infty v_x^2\,f_{1D}(v_x)\,dv_x=\frac{k_BT}{m}$$
- This matches the [[Statistical thermodynamics#The classical limit: equipartition|equipartition theorem]]:
$$\frac{1}{2}m\mean{v_x^2}=\frac{1}{2}k_BT$$

## Maxwell-Boltzmann distribution
- As the three coordinates are _independent of each other_, in the 3D case, the _distribution of velocities_ is:
$$f_{1D}(v_x)\,dv_x\,f_{1D}(v_y)\,dv_y\,f_{1D}(v_z)\,dv_z=\left(\frac{m}{2\pi k_BT}\right)^{3/2}\exp\left(-\frac{mv^2}{2k_BT}\right)\,dv_x\,dv_y\,dv_z$$
- The 3D distribution is a _Gaussian_ centred (and _peaked_) at the origin
- The most likely _speed_ depends on corresponding _volume in $v-$space_:
![[MB shell.png]]

- The _number of states_ occupied by particles of _speed_ $v$ are in a _spherical shell_ in $v-$space:
$$f(v)\,dv\propto v^2\exp\left(-\frac{mv^2}{2k_BT}\right)\,dv$$
- By _normalising_, this gives the _Maxwell-Boltzmann distribution of speeds_:
$$\displaylines{\int_0^\infty f(v)\,dv=1 \\ f(v)=\left(\frac{m}{2\pi k_BT}\right)^{3/2}4\pi v^2\exp\left(-\frac{mv^2}{2k_BT}\right)}$$
- _Mass_ dependence:
![[MB distribution mass dependence.png]]

- _Temperature_ dependence:
![[MB distribution temperature dependence.png]]

### Averages and maximums
- The _average speed_ is given by:
$$\mean{v}=\int_0^\infty v\,f(v)\,dv=\sqrt{\frac{8k_BT}{\pi m}}$$
- The _root mean square_ is then given by:
$$\mean{v^2}=\int_0^\infty \,v^2\,f(v)\,dv=\frac{3k_BT}{m}$$
- This matches the _equipartition_ value
- As for the _maximum:
$$\frac{df(v)}{dv}\Bigg|_{v_\text{f max}}=0 \hspace{1cm} v_{f \text{max}}=\sqrt{\frac{2k_BT}{m}}$$
- By considering the _significance of high velocities_ in the distribution:
$$v_{f\text{ max}}<\mean{v}<v_\text{rms}$$
- The ratio is $\sqrt{2}:\sqrt{8/\pi}:\sqrt{3}$
![[MB speeds.png]]

# Pressure