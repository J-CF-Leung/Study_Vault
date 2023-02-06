# Newtonian dynamics
- Newtonian mechanics is _non-relativistic_, i.e. $v<<c$
- It is _classical_, i.e. $Et>>\hbar$

- Assumptions:
1. Mass is _independent of velocity, time, or frame of reference_
2. Measurements of length and time are _independent of frame of reference_
3. All parameters can be known _precisely_

- Newton's Laws of motion-
- 1st Law: If no force is applied on a body, there is no acceleration
- 3rd Law: If one body exerts a force on a second body, the second body exerts an _equal and opposite_ force on the first
- 2nd Law: Force is rate of change of _momentum_
$$\bm{F}=\frac{d\bm{p}}{dt}$$
## Simple harmonic motion
- Force is _proportional to_, and _opposite_ displacement
$$F=m\ddot{x}=-kx$$
- General solution:
$$x=\Re\{Ce^{i\omega t}\}=A\cos(\omega t)+B\sin(\omega t)$$
	- Where $\omega^2=k/m$
- Integrating the equation, one discovers _the conservation of energy_:
$$\frac{1}{2}m\dot{x}^2+\frac{1}{2}kx^2=E=\text{const.}$$
- The energy is also known as the _Hamiltonian_

## Energy
- If energy is conserved, one can always _derive the equations of motion_
- Works as $\dot{x}$ is _generally non-zero_
- _Work-energy theorem_: work done on particle = change in kinetic energy

## Many-particle systems
- Let there be $N$ particles, the $i$th particle of mass $m_i$ is at position $\bm{r}_i$ with velocity $\bm{v}_i$
- It is acted on by external force $\bm{F}_{i0}$ and internal forces $\bm{F}_{ij}$ from particles $j$
- Let the _total mass_ be $M=\sum m_i$
- The position of the _centre of mass_ $\bm{R}$ is defined as:
$$\bm{R}\equiv\frac{1}{M}\sum_im_i\bm{r}_i$$
- Other useful quantities:
	- Total momentum $\bm{P}$
	- Total angular momentum $\bm{J}$
	- Total external force $\bm{F}_0$
	- Total external torque $\bm{G}_0$
	- Kinetic, potential, and total energies $T$, $U$. $E$

### Momenta
- The external force and torque affect _total_ momentum and angular momentum:
$$\bm{F}_0=\frac{d\bm{P}}{dt} \hspace{1.5cm} \bm{G}_0=\frac{d\bm{J}}{dt}$$
	- Can be derived by considering all external and internal forces + Newton's 3rd Law

- Let $S'$ the _centre of mass frame/zero-momentum frame_
- The _intrinsic angular momentum_ is $\bm{J}'$, the angular momentum in the ZMF
	- Property of system, independent of origin

### Kinetic and potential energy
- The _change in KE_ of a system can be written, using the work-energy theorem, as:
$$dT=\sum_i\bm{F}_i\cdot d\bm{r}_i+\sum_i\sum_{j<i}\bm{F}_{ij}\cdot$$

## Constant translation of frame of reference
- Let the origin be displaced by _constant_ $\bm{a}$ from the CM, thus $\bm{r}=\bm{r}'+\bm{a}$
- Since the displacement is constant, _linear momenta are unaffected_
- As for the angular momenta:
$$\bm{J}=\bm{J}'+\sum_i\bm{a}\wedge\bm{p}_i=\bm{J}'+\bm{a}\wedge\bm{P}$$
- In general, $\bm{J}$ depends on $\bm{P}$ ($\bm{J}=\bm{J}'$ in the ZMF)
- Taking the time derivative:
$$\bm{G}=\bm{G}'+\bm{a}\wedge\bm{F}$$
## Galilean transformation
- Let $\bm{r}=\bm{r}'+\bm{V}t$, with $t=t'$
- Momenta:
$$\bm{p}=\bm{p}'+m\bm{V}\hspace{1.5cm}\bm{P}=\bm{P}'+m\bm{V}$$
- Angular momenta:
$$\bm{J}=\sum_i(\bm{r}'_a+\bm{V}t)\wedge(\bm{p}'_i+m_i\bm{V})=\bm{J'}+\bm{V}t\wedge\bm{P}'+M\bm{R}'\wedge\bm{V}$$
- If $S'$ is the _zero-momentum frame_:
$$\bm{J}=\bm{J}_\text{CM}+M\bm{R}'\wedge\bm{V}$$
	- $\bm{J}_\text{CM}$ is the angular momentum measured in the ZMF, also denoted $\bm{J}'$
- Kinetic energy:
$$T=T'+\sum_im_i\bm{v}'_i\cdot\bm{V}+\frac{1}{2}MV^2$$
- In the _zero-momentum frame_:
$$T=T_\text{CM}+\frac{1}{2}MV^2$$
	- $T_\text{CM}$ is the kinetic energy measured in the ZMF
	- KE of _linear motion of CM_ + KE of the whole system rotating about CM

## Motion in polar coordinate system
- [[Vector calculus in 3-dimensions#Definition of curvilinear coordinates|Curvilinear coordinates]]
- Care has to be taken since _unit vectors are dependent on position_

- Consider _cylindrical polar coordinates in 2 dimensions_
- Since the magnitude of a unit vector cannot change, its change _has to be orthogonal_:
$$\frac{d}{dt}\hat{\bm{e}}_\rho=\dot{\phi}\hat{\bm{e}}_\phi \hspace{1.5cm} \frac{d}{dt}\hat{\bm{e}}_\phi=-\dot{\phi}\hat{\bm{e}}_\rho$$
- From simple geometry, or the above relations:
$$\bm{\dot{r}}=\dot{\rho}\hat{\bm{e}}_\rho+\rho\dot{\phi}\hat{\bm{e}}_\phi$$
- The acceleration is:
$$\bm{\ddot{r}}=(\ddot{\rho}-\rho\dot{\phi}^2)\hat{\bm{e}}_\rho+(2\dot{\rho}\dot{\phi}+\rho\ddot{\phi})\hat{\bm{e}}_\phi$$
- The _radial_ acceleration has a _centripetal term_ required to keep $\rho$ constant
- The _transverse_ acceleration can be written a different way:
$$2\dot{\rho}\dot{\phi}+\rho\ddot{\phi}=\frac{1}{\rho}\frac{d}{dt}\left(\frac{1}{2}\rho^2\dot{\phi}\right)$$
	- The term in the brackets is _angular momentum per unit mass_

## Non-inertial frame
- Let there be an _inertial frame_ $S_0$, where a particle experiences a force $\bm{F}$
	- The force should be _generated from known physical causes_
- Suppose in moving frame $S$, $\bm{r}=\bm{r}_0-\bm{R}(t)$
- For the special case $\ddot{\bm{R}}=0$, the Galilean transformation is regained
- However, in general:
$$m\ddot{\bm{r}}=\bm{F}-m\ddot{\bm{R}}$$
- The term $-m\ddot{\bm{R}}$ is a _fictitious force_

### Rotating frame
- Let an observer rotate with _constant angular velocity_ $\bm{\omega}$
- Given _any_ vector $\bm{A}$, the rates of change in _inertial_ frame $S_0$ and _rotating_ frame $S$ are related by:
$$\left[\frac{d\bm{A}}{dt}\right]_{S_0}=\left[\frac{d\bm{A}}{dt}\right]_S+\bm{\omega}\wedge\bm{A}$$
- Define $\bm{r}$, $\bm{v}$ and $\bm{a}$ to be measured _in the rotating frame_
- By _applying the operator twice_, the accelerations of the 2 frames are related by:
$$\displaylines{m\ddot{\bm{r}_0}=\bm{F}=m\bm{a}+2m(\bm{\omega}\wedge\bm{v}) +m\bm{\omega}\wedge(\bm{\omega}\wedge \bm{r}) \\ m\bm{a}=\bm{F}-2m(\bm{\omega}\wedge\bm{v}) -m\bm{\omega}\wedge(\bm{\omega}\wedge \bm{r})}$$
- There are _two distinct fictitious forces_
- $-2m(\bm{\omega}\wedge\bm{v})$ is the _Coriolis force_
- $-m\bm{\omega}\wedge(\bm{\omega}\wedge\bm{r})$ is the _centrifugal force_

- For a _general rotating frame_, for an observer moving at $\bm{R}(t)$, rotating at $\bm{\omega}(t)$:
$$m\bm{a}=\bm{F}-2m(\bm{\omega}\wedge\bm{v}) -m\bm{\omega}\wedge(\bm{\omega}\wedge \bm{r}) -m\ddot{\bm{R}}-m\dot{\bm{\omega}}\wedge\bm{r}$$
- The latter term is the _Euler force_

- The centrifugal force can be written as:
$$F_\text{centrifugal}=m\omega^2(\bm{r}-(\bm{r}\cdot\hat{\bm{\omega}})\hat{\bm{\omega}})=m\omega^2\rho\hat{\bm{\rho}}$$
- It is _outwards_, perpendicular to $\hat{\bm{\omega}}$
- To _maintain radius_, there must be some _inward (centripetal) force_

- The Coriolis force is _perpendiular to both the rotation axis and velocity_
- Effects of the Coriolis force are _taken into account by angular momentum conservation_
