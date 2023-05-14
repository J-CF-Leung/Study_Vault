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
- The _collisions_ of gas molecules on a wall produces a _net force_, and thus a _pressure_

## Collisions on a wall
- Consider particles with velocity $u_x$ _perpendicular_ to a wall of _area_ $A$, in a box of volume $V$
- Let there be $N$ particles with mass $m$
- The _impulse per collision_ is $2mu_x$, with _collision rate_ $Au_xN/2V$
- Therefore, the _average pressure_ is:
$$p=m\mean{u_x^2}\frac{N}{V}$$
- As $\mean{u_x^2}=\mean{u^2}/3$:
$$pV=\frac{1}{3}Nm\mean{u}^2=nRT$$
- The second equality comes from the [[Classical Thermodynamics#Ideal gases|ideal gas law]]
- Therefore, the energy is the [[Statistical thermodynamics#The classical limit: equipartition|equipartition]] value:
$$U=\frac{3}{2}nRT$$

## From the Maxwell-Boltzmann distribution
- Let the _number of molecules per unit volume_ with speed between $v$ and $v+dv$ be:
$$n\,f(v)\,dv$$
- The _fraction_ of molecules in a trajectory covering _solid angle_ $d\Omega$:
	$$\frac{d\Omega}{4\pi}=\frac{2\pi\sin\theta\,d\theta}{4\pi}=\frac{1}{2}\sin\theta\,d\theta$$
	- The solid angle is that of an _annulus_:
	![[Kinetic theory annulus.png]]

- Hence, the _number of molecules per unit volume_, with _speed_ in interval $[v,v+dv]$, with trajectory of angle $[\theta,\theta+d\theta]$:
$$\frac{1}{2}nf(v)\sin\theta\,d\theta\,dv$$
- In a time interval $dt$, the particles travelling at angle $\theta$ _normal_ to the wall sweep a volume $Av\cos\theta\,dt$
- Therefore, the number of molecules _hitting_ the wall in the above conditions:
$$dN=nAv\cos\theta\,dt\,f(v)\,dv\,\frac{1}{2}\sin\theta\,d\theta$$
- As the molecules have _momentum change_ $2mv\cos\theta$:
$$p=\int2mv\cos\theta\,\frac{dN}{dt}=mn\int_0^\infty\,dv\,v^2f(v)\int_0^{\pi/2}\cos^2\theta\sin\theta\,d\theta$$
- Therefore, the _pressure_ is:
$$\displaylines{p=\frac{1}{3}mn\mean{v^2} \\ pV=\frac{1}{3}mN\mean{v^2}=Nk_BT}$$
- Where the second equality comes from [[Statistical thermodynamics#The classical limit: equipartition|equipartition]]

## Dalton's law
- In a _mixture of gases_, the _total pressure_ is the _sum of partial pressures_ of the separate components:
$$\displaylines{p=nk_BT \hspace{1cm} n=\sum_i n_i \\ p=\sum_i n_ik_BT=\sum_i p_i}$$

# Effusion and flux
- _Effusion_ is a process where a gas _escapes from a hole_, which is _small_, so molecules can _pass through without colliding with each other_
- The _rate of effusion_ is:
$$nAv_\text{rms}\propto nA\sqrt{\frac{T}{m}}$$
- It is often _limited_ by the _mean free path_ of collisions between the particles

- The _molecular flux_ through a surface is the _number of molecules_ hitting a _unit area_, _per unit time_, with units of $\text{m}^{-2}\,\text{s}^{-1}$

- The _number of particles_ hitting a _unit area of a wall per unit time_ with speed in range $v$ to $v+dv$, at angles between $\theta$ and $\theta+d\theta$:
$$dN=nv\cos\theta f(v)\,dv\frac{1}{2}\sin\theta\,d\theta$$

- Therefore the _flux_ is:
$$\Phi=\frac{1}{4}n\mean{v}$$
- Substituting the result from [[#Averages and maximums|the Maxwell-Boltzmann distribution]]:
$$\Phi=\frac{p}{\sqrt{2\pi mk_BT}}$$

## Graham's law
- At _equal pressure_, the _effusion speed_ of different gases is _inversely proportional_ to the _square root of their densities_
- This agrees with the expression for _flux_

- The _effusion rate_ is defined as the _number of molecules_ hitting a hole of area $A$:
$$\text{Effusion rate}\;=\;\Phi A$$
- A _practical use_ is to _measure the vapour pressure_ of a liquid by measuring _rate of mass loss_ from effusion

- _Effusion_ is inherently a _speed-selective process_
- The _number of molecules_ passing through the hole is proportional to:
$$Av\,dt\cos\theta\,nf(v)\,dv\frac{1}{2}\sin\theta\,d\theta\propto vf(v)\,dv$$
- Therefore, the _speed distribution of effused molecules_ is:
$$f_\text{Effusion}(v)\propto v^3\exp(-mv^2/2k_BT)$$

# Collisions
- For a _dilute gas_, one can treat molecules as _classical particles_, or _hard spheres_
- One can also approximate that a collision _randomises molecular velocities_
- Therefore, one can derive a _mean free path_ of particles

## The statistics of collisions
- Let some volume have a _number density_ of $n$
- Assume _all gas molecules are stationary_, except for _one_, moving at _speed_ $v$
- Let the molecule have _collision cross-section_ $\sigma$
- Then in some time $\delta t$, the particle _sweeps out_ volume $\sigma v\delta t$
- A _collision_ occurs if _another molecule_ lies inside this volume

- The _chance_ which this collision occurs in this time is $n\sigma v\delta t$

- Let $P(t)$ be the _probability_ where the molecule _survives without colliding_ for time $t$
- The _fraction_ $P(t+\delta t)/P(t)$ is then the probability that the molecule survives until $t+\delta t$, _given_ that it survived until $t$:
$$\frac{P(t+\delta t)}{P(t)}=1-n\sigma v\delta t$$
- By _integrating_:
$$P(t)=\exp(-n\sigma vt)$$
- From its definition, $P(t=0)=1$

- The probability of a particle _surviving_ until time $t$, then _colliding_ after time $dt$:
$$\exp(-n\sigma vt)n\sigma v\,dt$$
- This probability is already _normalised_
	- Integrate w.r.t. $t$ from 0 to infinity

- Then, one can find the _mean collision time_:
$$\tau=\int_0^\infty t\exp(-n\sigma vt)\,n\sigma v\,dt=\frac{1}{n\sigma v}$$

## Collision cross-section
- Consider two _spheres_ of radius $a_1$ and $a_2$
- Let there be a _hard-sphere potental_, as a function of the _distance between them_:
$$V(r)=\begin{cases} \infty &{r\leq a_1+a_2} \\ 0 &r\geq a_1+a_2\end{cases}$$
![[Hard sphere potential.png]]

- Define $b$ as the _impact parameter_ between two moving molecules, as the _distance of closest approach_ that would result if the trajectories were _undeflected_
- For hard-sphere potentials:
$$b<a_1+a_2$$
- A collision takes place when the _centres of the molecules_ lie within a _tube_ of radius $a_1+a_2$
![[Impact parameter tube.png|600]]
- This area is known as the _collision cross-section_:
$$\sigma=\pi(a_1+a_2)^2$$

## Mean free path
- The expression for _mean free path_ $\lambda$ is then:
$$\lambda=\mean{v}\tau=\frac{\mean{v}}{n\sigma\mean{v_r}}$$
- Here, $\mean{v_r}$ is the _mean relative speed_ of molecules:
$$\displaylines{\bm{v}_r=\bm{v}_1-\bm{v}_2 \\ \mean{v_r^2}=\mean{v_1^2}+\mean{v_2^2}-2\mean{\bm{v}_1\cdot\bm{v}_2}=2\mean{v^2}}$$
- Approximating:
$$\mean{v_r}\approx \sqrt{2}\mean{v}$$
- From this, the _mean free path_ is:
$$\lambda=\frac{1}{\sqrt{2}n\sigma}=\frac{k_BT}{\sqrt{2}p\sigma}$$
- In _air_, at _atmospheric pressure_, $\lambda\approx 68\,\text{nm}$
