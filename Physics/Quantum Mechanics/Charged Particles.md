
- For _electromagnetic_ phenomena in quantum mechanics, assume that the _quantum Hamiltonian_ has the _same form_ as the _classical Hamiltonian_ found in [[Electrodynamics and Optics|Classical Electrodynamics]]
	- From one of the [[Fundamental concepts of quantum mechanics#The fundamental postulates|postulates]]
- Then, the effects of _spin_ are added _by hand_ based on experiment

- In _classical electrodynamics_, the equation of motion is
$$m\ddot{\bm{r}}=q(\bm{E}+\bm{v}\times\bm{B})$$
- The _fields_ are given by:
$$\bm{E}=-\nabla\phi-\pd{\bm{A}}{t}\hspace{1.5cm}\bm{B}=\nabla\times\bm{A}$$
- It can then be shown that the Hamiltonian is:
$$\Ham=\frac{1}{2m}\left|\bm{p}-q\bm{A}(\bm{r},t)\right|^2+q\phi(\bm{r},t)$$
- This suggests the _Hamiltonian operator_:
$$\hat\Ham=\frac{1}{2m}\left|\hat{\bm{p}}-q\bm{A}\right|^2+q\phi$$
- In the _position basis_, the _time-dependent Schrödinger equation_ is:
$$i\hbar\pd{\psi}{t}=\frac{1}{2m}\left|-i\hbar\nabla-q\bm{A}(\bm{r},t)\right|^2\psi+q\phi(\bm{r},t)\psi$$

# Gauge invariance of the Schrödinger equation
- The electric and magnetic fields are known to be _gauge-invariant_:
$$\bm{A}\to\bm{A}'=\bm{A}+\nabla f\hspace{1.5cm}\phi\to\phi'=\phi-\pd{f}{t}$$
- Here, $f(\bm{r},t)$ is any _arbitrary function_, and the above always leaves $\bm{E}$ and $\bm{B}$ _unchanged_

- However, the above _changes the Schrödinger equation_ with _extra terms_
- The only option to recover gauge invariance is to _change $\psi$ as well_:
$$\displaylines{\bm{A}\to\bm{A}'\hspace{1cm}\phi\to\phi'\\\psi(\bm{r},t)\to\psi'(\bm{r},t)=\psi(\bm{r},t)\exp[i\Lambda(\bm{r},t)]}$$
- The phase factor makes sure the _probability density_ is unchanged, hence leaving the physics invariant

- One can prove that with the transformation:
$$\displaylines{\bm{A}\to\bm{A}'=\bm{A}+\nabla f\hspace{1cm}\phi\to\phi'=\phi-\pd{f}{t}\hspace{1cm}\psi\to\psi'=\psi\exp\left[i\frac{q}{\hbar}f\right] \\ i\hbar\pd{\psi'}{t}=\frac{1}{2m}\left|-i\hbar\nabla-q\bm{A}(\bm{r},t)\right|^2\psi'+q\phi(\bm{r},t)\psi'}$$

## The case of zero magnetic field
- For $\bm{B}=0$, the potential $\bm{A}$ can take the form of _the gradient of any function_:
$$\bm{A}=\nabla\chi$$
- Given two points $\bm{r}$ and $\bm{r}_0$:
$$\chi(\bm{r})-\chi(\bm{r}_0)=\int_{\bm{r}_0}^{\bm{r}}\bm{A}(\bm{s})\cdot d\bm{s}$$
- Choosing $f=-\chi$, one can have a _gauge_ where $\bm{A}=0$
- This works as long as the integration path is in a _simply-connected region_

- Denote wave functions such that $\psi_\chi$ in the gauge for $\bm{A}=\nabla\chi$, and $\psi_0$ in the gauge for $\bm{A}=0$:
$$\psi_0(\bm{r})=\psi_\chi(\bm{r})\exp\left[-i\frac{q}{\hbar}\chi\right]$$
- Absorbing a _constant phase factor_, one can rewrite the above:
$$\psi_\chi(\bm{r})=\psi_0(\bm{r})\exp\left[i\frac{q}{\hbar}\int_{\bm{r}_0}^\bm{r}\bm{A}(\bm{s})\cdot d\bm{s}\right]$$

# The Aharanov-Bohm Effect
- In _classical physics_, it is _only the fields_ which have physical significance
- In _quantum mechanics_, the potential $\bm{A}$ has significance

- Suppose there is some _double-slit setup_:
![[Aharonov-Bohm 1.png]]
- The observed _fringe pattern_ will be a result of _interference_:
$$I\propto|\psi_D|^2=|\psi_A+\psi_B|^2$$
- For the gauge where $\bm{A}=0$, $\psi_{D,0}=\psi_{A,0}+\psi_{B,0}$
- For the gauge where $\bm{A}=\nabla\chi$:
$$\psi_{D,\chi}=\psi_{A,0}\exp\left[i\frac{q}{\hbar}\int_A\bm{A}(\bm{s})\cdot d\bm{s}\right]+ \psi_{B,0}\exp\left[i\frac{q}{\hbar}\int_B\bm{A}(\bm{s})\cdot d\bm{s}\right]$$
- When there is _no field anywhere_:
$$\displaylines{\oint\bm{A}\cdot d\bm{s}=\iint_S\bm{B}\cdot d\bm{S}=0\Longrightarrow \int_A\bm{A}(\bm{s})\cdot d\bm{s}=\int_B\bm{A}(\bm{s})\cdot d\bm{s} \\ I\propto |\psi_{A,\chi}+\psi_{B,\chi}|^2=|\psi_{A,0}+\psi_{B,0}|^2}$$

- Then place a _solenoid_ with flux $\Phi$ behind the slits:
![[Aharonov-Bohm 2.png]]
- With a _shielded solenoid_, the flux is _contained_, and $\bm{B}=0$ _along the paths of the electrons_
- However, $\bm{A}$ _cannot be zero along both trajectories_:
$$\oint\bm{A}\cdot d\bm{s}=\iint_S\bm{B}\cdot d\bm{S}=\Phi$$
- In _cylindrical coordinates_ with origin at the centre of the solenoid:
$$\bm{A}=\frac{\Phi}{2\pi\rho}\hat{\phi}=\nabla\left(\frac{\Phi\phi}{2\pi}\right)$$
- As $\chi$ is _multiple-valued_, the entire region is now _multiply-connected_
- As each _path_ is still in a _singly-connected region_:
$$\psi_{D,\chi}=\psi_{A,0}\exp\left[i\frac{q}{\hbar}\int_A\bm{A}(\bm{s})\cdot d\bm{s}\right]+ \psi_{B,0}\exp\left[i\frac{q}{\hbar}\int_B\bm{A}(\bm{s})\cdot d\bm{s}\right]$$
- As $A-B$ is a _loop_ around the solenoid:
$$|\psi_{D,\chi}|^2=\left|\psi_{A,0}\exp\left[i\frac{q\Phi}{\hbar}\right]+\psi_{B,0}\right|^2$$
- This effect on the interference pattern is _detectable_
- Physical reasoning: the potential affects the _phase_ of each beam
- The total _phase difference_ $\delta$:
$$|\delta|=\frac{e\Phi}{\hbar}=2\pi\frac{\Phi}{\Phi_0}\hspace{1.5cm}\Phi_0\equiv\frac{h}{e}\approx 4.1\times 10^{-15}\,\text{T m}^2$$
- $\Phi_0$ is the _flux quantum_

- This proves that there can still be _electromagnetic effects_ in regions where the _field is zero_
- This effect is still _gauge invariant_ as it only depends on the _total enclosed flux_