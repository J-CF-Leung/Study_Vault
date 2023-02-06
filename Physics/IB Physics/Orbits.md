
- Consider a particle moving in a _central force field_:
$$\displaylines{U=U(r) \\ \bm{F}=-\nabla U=-\pd{U}{r}\hat{\bm{r}}}$$
- Due to the lack of a torque:
$$J=mr^2\dot{\phi}=\text{constant}$$
- The motion _remains in the plane defined by $\bm{r}$ and $\bm{v}$_

- Conservation of energy:
$$E=U(r)+\frac{1}{2}m(\dot{r}^2+r^2\dot{\phi}^2)=\frac{1}{2} m\dot{r}^2+U(r)+\frac{J^2}{2mr^2}$$
- Therefore, there is an _effective potential_ $U_\text{eff}$:
$$U_\text{eff}(r)=U(r)+\frac{J^2}{2mr^2}$$
- This includes a _centrifugal term_ which decreases with $r$

## Power law force
- Consider a force of the form:
$$F=-Ar^n$$
- The effective potential is:
$$U_\text{eff}(r)=\frac{Ar^{n+1}}{n+1}+\frac{J^2}{2mr^2}$$
	- Exception: $n=-1$

- Define the equilibrium distance $r_0$ such that:
$$\frac{dU_\text{eff}}{dr}\Bigg|_{r=r_0}=0$$
- The potential behaves differently for different values of $n$:
| Condition on $n$ | Stability at $r_0$ | Boundedness                          | $r\to\infty$            | $r\to0$                 |
| ---------------- | ------------------ | ------------------------------------ | ----------------------- | ----------------------- |
| $n\geq-1$        | Stable             | Bound                                | $U_\text{eff}\to\infty$ | $U_\text{eff}\to\infty$ |
| $-3<n<-1$        | Stable             | Can be bound or unbound              | $U_\text{eff}\to0$      | $U_\text{eff}\to\infty$ |
| $n\leq -3$       | Unstable           | Goes to either $r=0$ or $r\to\infty$ | $U_\text{eff}\to0$      | $U_\text{eff}\to-\infty$                        |

![[Power law force effective potentials.png]]

- Consider _small perturbations_ from the crcular orbit
- By _Taylor expanding_ the potential and using the definition of $r_0$:
$$U_\text{eff}\approx U_0+\frac{1}{2}\frac{dU^2}{dr}\Bigg|_{r=r_0}(r-r_0)^2=U_0+\frac{(n+3)J^2}{mr_0^4}(r-r_0)^2$$
- This is a _harmonic potential_, thus the equation of motion for $r$ can be written as:
$$\displaylines{\epsilon=r-r_0 \\ m\ddot{\epsilon}+\omega_p^2\epsilon=0 \\ \omega_p=\sqrt{n+3}\frac{J}{mr_0^2}}$$
- The angular frequency of _radial oscillations_ $\omega_p$ is _proportional_ to angular frequency of _rotation_:
$$\omega_p=\sqrt{n+3}\,\dot{\phi}=\sqrt{n+3}\omega_c$$
![[Orbit cases.png]]

## Elliptical orbits and Kepler's Laws
- Let there be an _attractive force_ obeying the _inverse square law_:
$$\bm{F}=-\frac{A}{r^2}\hat{\bm{r}}$$
- For _gravity_, $A=GMm$

- _First Law_: Planetary orbits are _ellipses with the Sun at one focus_
- _Second Law_: The line _joining the planet and the Sun_ sweeps out _an equal amount of area in equal times_
	- Due to the conservation of angular momentum
- _Third Law_: The _square of the period_ of the planet around the sun is _proportional the cubed of the semi-major axis_ of the orbit

- Using _conservation of angular momentum and energy_, and making a _substitution_:
$$\displaylines{u=\frac{1}{r} \\ \left(\frac{du}{d\phi}\right)^2=\frac{e^2}{r_0^2}-\left(u-\frac{1}{r_0}\right)^2 \\ \frac{e^2}{r_0^2}=\frac{2mE}{J^2}+\frac{1}{r_0^2}}$$
- By _integrating $du$_, one finds:
$$r=\frac{r_0}{1+e\cos\phi}$$
- This is the equation of the _conic section_
- Hence, it is shown that $e$ _is the eccentricity of the conic section_
- For a _repulsive_ potential, $r_0=r(e\cos\phi-1)$

| Eccentricity | Shape of orbit |
| ------------ | -------------- |
| $e=0$        | Circle         |
| $0<e<1$      | Ellipse        |
| $e=1$        | Parabola       |
| $e>1$        | Hyperbola               |

- Assume the orbit is an ellipse, hence $0<e<1$
- The centre of attraction _is one focus of the ellipse_
- $r_0$ is the _semi-latus rectum_
- The _minimum and maximum_ distances are:
$$\displaylines{r_\text{min}=\frac{r_0}{1+e} \\ r_\text{max}=\frac{r_0}{1-e}}$$
- The _semi-major and semi-minor axes_ of the ellipse satisfy:
$$\displaylines{a=\frac{r_\text{min}+r_\text{max}}{2}=\frac{r_0}{1-e^2} \\ r_\text{min, max}=a(1\pm e) \\ b=\frac{r_0}{\sqrt{1-e^2}} \\ }$$
- The _area_ of the ellipse is:
$$\pi ab=\frac{\pi r_0^2}{(1-e^2)^{3/2}}$$
- The _rate of sweeping out area_ is:
$$\frac{1}{2}r^2\dot{\phi}=\frac{J}{2m}=\text{constant}$$
- The period is _time taken to sweep out the whole area_
$$\displaylines{T=\frac{2\pi r_0^2m}{J(1-e^2)^{3/2}}=2\pi\sqrt{\frac{ma^3}{A}} \\ T^2=\frac{4\pi^2m}{A}a^3}$$


### An alternative derivation
- The vectors $\bm{J}=mr^2\dot{\phi}\hat{z}$, $\dot{\bm{v}}=-A/(mr^2)\hat{\bm{r}}$ and $\dot{\bm{e}}_r=\dot{\phi}\bm{e}_\phi$ are _mutually perpendicular_:
$$\bm{J}\wedge\dot{\bm{v}}=-A\dot{\bm{e}}_r$$
- Since $\bm{J}$ is a constant, the equation can be _integrated_:
$$\bm{J}\wedge\bm{v}+A(\hat{\bm{e}}_r+\bm{e})=0$$
	- where $\bm{e}$ is an integration constant

- Taking a _dot product with $\bm{r}$ on both sides_:
$$\displaylines{-\frac{J^2}{m}+A(r+\bm{e}\cdot\bm{r})=0 \\ r(1+\bm{e}\cdot\bm{e}_r)=r(1+e\cos\phi)=\frac{J^2}{mA}=r_0}$$
### Energy
- By taking the scalar product of $A\bm{e}=-(\bm{J}\wedge\bm{v}+A\bm{e}_r)$ _with itself_, one obtains:
$$\displaylines{A^2(e^2-1)=J^2\left(v^2-\frac{2A}{mr}\right)=\frac{2EJ^2}{m}=2AEr_0}$$
- From this, the energy is found to be:
$$E=-\frac{A}{2a}$$
- Energy is _independent of eccentricity_

- The _time-averaged energies_ are:
$$\mean{T}=-\mean{E}=-\frac{1}{2}\mean{U}$$

### A summary
- Orbit:
$$r=\frac{r_0}{1+e\cos\phi}$$
- Characteristic distances:
$$\displaylines{r_\text{min}=\frac{r_0}{1+e}\hspace{1cm}r_\text{max}=\frac{r_0}{1+e} \\ a=\frac{r_0}{1-e^2} \hspace{1cm} b=\frac{r_0}{\sqrt{1-e^2}}}$$
- From all of this, it can be seen that _the semi-major axis determines energy and period_:
$$E=-\frac{A}{2a} \hspace{1cm} T=\frac{2\pi}{\omega} \hspace{1cm} \omega^2=\frac{A}{ma^3}$$

- The semi-latus rectum determines _angular momentum_:
$$J^2=Amr_0$$
## Non-elliptical orbits
- From above, eccentricity can be expressed in terms of _energy and angular momentum_:
$$e^2=1+\frac{2EJ^2}{mA^2}$$
| Eccentricity | Orbit      | Energy              |
| ------------ | ---------- | ------------------- |
| $e=0$        | Circular   | $-mA^2/(2J^2)$ |
| $0<e<1$      | Elliptical | Negative            |
| $e=1$        | Parabola   | $0$                 |
| $e>1$        | Hyperbola  | Positive            |

### Parabolic orbit
- The _focal length_ of the parabola is $r_0/2$, equal to $r_\text{min}$
	- Like the ellipse, the _focus_ is at the origin
- Equation with the attracting body as origin:
$$y^2=4f(f-x)$$

### Hyperbolic orbit
- If $e>1$, energy is positive and $a$ is _negative_
![[Hyperbolic orbit.png]]
- The _impact parameter_ $b$ and the _speed at infinity_ $v_\infty$ determine angular momentum:
$$J=mbv_\infty \hspace{1cm} E=\frac{1}{2}mv_\infty^2$$
- The _asymptotes_ are given with $\phi_\infty$:
$$\displaylines{\cos\phi_\infty=-1/e \hspace{1cm} \tan^2\phi_\infty=e^2-1=\frac{m^2v_\infty^4b^2}{A^2} \\ \cot(\chi/2)=|\tan\phi_\infty|=\frac{mv_\infty^2b^2}{A}}$$
- Since it is a hyperbola, $\pi/2<\phi_\infty<\pi$

- $\chi$ is the _angle of deflection_ $2\phi_\infty-\pi$

- With the attractive body at the origin, the equation in Cartesian coordinates are:
$$\displaylines{\frac{(x-x_c)^2}{X^2}-\frac{y^2}{Y^2}=1 \\ X=\frac{r_0}{e^2-1} \hspace{1cm}Y=\frac{r_0}{\sqrt{e^2-1}} \hspace{1cm} x_c=eX}$$

- The _distance of closest approach_ is:
$$x_c-X=|a|(e-1)$$
- The equation for the _asymptotes_ is:
$$y=\pm\frac{Y}{X}x=\pm\sqrt{e^2-1}x$$
### Repulsive potential/Rutherford scattering
- The _repulsive force_ is $F=B/r^2$
- The angular momentum and orbit are:
	- The solution for $r$ is the _negative branch_ of the conic section
$$J^2=BMr_0 \hspace{1cm} r=\frac{r_0}{e\cos\phi-1}$$
- The _angle of deflection_ $\chi$ is now defined to be _negative_
- The angle of the asymptote is:
$$\cot(\chi/2)=|\tan\phi_\infty|=\frac{mv_\infty b}{B}$$
- The _impact parameter_ can be found by looking at the _change in momentum along one asymptotic direction_
	- Here, $\theta$ is _instantaneous angular position_ starting from asymptote
$$\begin{align}\Delta p&=mv_\infty(\cos\chi-1)=\int F_d\,dt=-\int\frac{B}{r^2}\cos\theta\,dt \\ &=-\int\frac{B}{r^2}\cos\theta\frac{d\theta}{\dot{\theta}}=-\int\frac{mB}{J}\cos\theta\,d\theta\end{align}$$

### Hohmann Transfer
![[Hohmann Transfer.png]]
- The _Hohmann transfer_ is a _half-elliptical trajectory_ connecting _2 circular orbits_
- In a circular orbit:
$$T=-E=-\frac{1}{2}U$$
- The _initial conditions_ are:
$$E_1=-\frac{GMm}{2a_1}\hspace{1cm} v_1=\sqrt{\frac{GM}{a_1}}$$
- The energy of the _transfer orbit_ is:
$$E=-\frac{GMm}{a_1+a_2}$$
- From _energy conservation_, the $\Delta v$ required to go into the orbit is:
$$\Delta v=\sqrt{\frac{2GMa_2}{a_1(a_1+a_2)}}-\sqrt{\frac{GM}{a_1}}$$
- To enter the _larger circular orbit_, a _further velocity change_ is required

- The Hohmann transfer is _the most fuel-efficient orbit_
	- Exception: Gravitational slingshot, or _bi-elliptic transfer_ in some cases

### Gravitational slingshot
- Using a _large object_ to _increase kinetic energy_ or _change direction_
	- The _loss of kinetic energy_ of the large object is _negligible_
- Best understood using a _frame transformation_
![[Gravitational slingshot.png]]
- Consider the case of a slingshot _along the original direction_:
	- Let the ship's original velocity be $v$, and Jupiter's speed be $V$
	- The final velocity of the ship is $2V-v$
- Only viable for a _small impact parameter_
	- Jupiter's gravity is _dominant_ in this region

## The two-body problem
- Let there be 2 masses $M_1$ and $M_2$, of _comparable size_
- Let their positions be $\bm{r}_1$ and $\bm{r}_2$

- The _reduced mass_ $\mu$ is defined as:
$$\displaylines{\frac{1}{\mu}=\frac{1}{M_1}+\frac{1}{M_2} \\ \mu=\frac{M_1M_2}{M_1+M_2}}$$

- The centre of mass must _stay in place relative to the masses_
- The two masses and the COM form a _straight line_
- The masses _orbit around the COM_

- Let the coordinate $\bm{r}\equiv\bm{r}_1-\bm{r}_2$

- It can be shown that the _kinetic energy in the COM frame_ is:
$$T=\frac{1}{2}\mu|\dot{\bm{r}}|^2$$
- The _angular momentum_ in the frame is:
$$\bm{J}=\mu\bm{r}\wedge\dot{\bm{r}}$$
- The _equation of motion_ for $\bm{r}$ is:
$$\ddot{\bm{r}}=\frac{1}{\mu}\bm{F}_{12}=\frac{M_1}{\mu}\ddot{\bm{r}}_1$$
- Hence, the two-body problem with _no external forces_ is _equivalent to a one-body problem_

## The three-body problem
- Example: Sun, Earth, Moon
- Real, stable cases are often _co-planar_

- General behaviour: 
	- With arbitrary initial conditions, the bodies often start to spin to conserve $\bm{J}$
	- The bodies attract, speed up and interact strongly
	- A _close binary_ is formed, releasing energy
	- The final body may _reach escape velocity_

## Gravitational potential and tidal forces
- The _zero is arbitrary_, but often chosen to be _infinity_
- Hence, the potential for a _point mass_ $M$ is:
$$\phi_g(\bm{r})=-\frac{GM}{R}$$
- The _gravitational field_ $\bm{g}$ is the _negative gradient_:
$$\bm{g}=-\nabla\phi_g$$
- For a _point mass_:
$$\bm{g}=-\frac{GM}{R^2}\hat{\bm{e}}_r$$
- The gravitational _tidal field_ $\bm{R}$ is a _difference in gravitational field between points_ offset by some displacement $\bm{a}$
$$\bm{T}(\bm{a})=(\bm{a}\cdot\nabla)\bm{g}$$
- Since the field varies as $1/r^2$, the tidal field varies as $1/r^3$

- If $\bm{a}=a\bm{e}_r$, it can be shown either from _binomial expansion_ or differentiation that:
$$\displaylines{\bm{T}(a\hat{\bm{e}}_r)=\frac{2aGM}{R^3}\hat{\bm{e}}_r \\ \bm{T}(\hat{\bm{e}}_r)=\frac{2GM}{R^3}\hat{\bm{e}}_r}$$

- If $\bm{a}=a\hat{\bm{e}}_\theta$, this brings a small _change in angle_ $a/R$, hence it can be shown that:
$$\bm{T}(\hat{\bm{e}}_\theta)=-\frac{GM}{R^3}\hat{\bm{e}}_\theta$$
- Hence, an object in the field of a point mass experiences a _radial stretching_ and a _compression in a plane_ perpendicular to the radial vector

- In the case where the object is _co-rotating_ with the orbit, there is contribution from the _centrifugal force_
- The _sideways tidal force is cancelled out_
- The sum gives a _radial stretch_ of $3GM/R^3$ _per unit length_, and a _compression perpendicular to the rotating plane_ of $-GM/R^3$ per unit length

### The tides on Earth
![[Earth tides.png]]
- The Earth _rotates relative to the tidal bulge_, which is oriented _towards the moon_
- This gives a _tidal acceleration_ $2GM_Mz/r^3$ at $A$ and $-GM_Mz/r^3$ at $B$
- This gives a _potential difference_ $3GM_Mz/r^3$, equivalent to $gh$, where $h$ is the _height of the tides_
- Complications: Geography, the Sun
