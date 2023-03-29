## Orbital angular momentum
- [[Operators, uncertainties and symmetries#The angular momentum operators|Definition of angular momentum operators]]
- The operators $\bm{\hat{L}}^2$ and $\hat{L}_z$ _commute_
- Hence, their eigenvalue problems can be solved _simultaneously_

- Let there be a simultaneous eigenbasis $\ket{\lambda\mu}$
- This eigenvalue problem can be expressed as:
$$L^2\ket{\lambda\mu}=\lambda\ket{\lambda\mu} \hspace{1.5cm}L_z \ket{\lambda\mu}=\mu \ket{\lambda\mu}$$

### Ladder operators
- Like the [[Quantum Harmonic Oscillator|quantum harmonic oscillator]] problem, finding eigenfunctions of angular momentum also involves _ladder operators_
- The ladder operators for angular momentum are defined as:
$$\hat{L}_\pm=L_x\pm iL_y$$
- The ladder operators satisfy the commutation relations:
$$[\hat{L_z},\hat{L}_\pm]=\pm\hbar\hat{L}_\pm \hspace{2cm} [\hat{L}^2,\hat{L}_\pm]=0$$

- Combining the two ladder operators also yields the following relation:
$$\hat{L}^2=\hat{L}_\pm\hat{L}_\mp+\hat{L}_z^2\mp\hbar\hat{L}_z$$

- If $\ket{\lambda\mu}$ is an eigenket of $\hat{L_z}$ and $\hat{L}^2$, then $\hat{L}_\pm\ket{\lambda\mu}$ is _also an eigenket_:
$$\hat{L}^2(\hat{L}_\pm\ket{\lambda\mu})=\hat{L}_\pm(\hat{L}^2\ket{\lambda\mu})=\lambda(\hat{L}_\pm\ket{\lambda\mu})$$
$$\hat{L}_z(\hat{L}_\pm\ket{\lambda\mu})=(\mu\pm\hbar)(\hat{L}_\pm\ket{\lambda\mu})$$
- Hence, the ladder operators _raise or lower the eigenvalue of $\hat{L}_z$ by $\hbar$ while not affecting the eigenvalue of $\hat{L}^2$_

- Since $\braket{\hat{L}_z^2}\leq \braket{\hat{L}^2}$, there must be a "top rung" and "bottom rung" where:
$$\displaylines{\hat{L}_+\ket{\lambda\mu_t}=\ket{0} \hspace{1cm} \hat{L}_z\ket{\lambda\mu_t}=\hbar l\ket{\lambda\mu_t} \hspace{1cm} \hat{L}^2\ket{\lambda\mu_t}=\lambda\ket{\lambda\mu_t} \\ 
\hat{L}_-\ket{\lambda\mu_b}=\ket{0} \hspace{1cm} \hat{L}_z\ket{\lambda\mu_b}=\hbar \bar{l}\ket{\lambda\mu_b} \hspace{1cm} \hat{L}^2\ket{\lambda\mu_b}=\lambda\ket{\lambda\mu_b}}$$
	- Here, $l$ and $\bar{l}$ are numbers indicating the _magnitude of the maximum and minimum_ $L_z$

- Using the above relations, one gets $\bar{l}=-l$

- Hence, for a given value of $l$, angular momenta can take values of $m\hbar$, where $m$  has $2l+1$ values, going from $-l$ to $l$ _in integer steps_
- As $-l$ has to go to $l$ in integer steps, it can _only be an integer or half-integer_
- From finding the [[#Eigenfunctions of orbital angular momentum|eigenfunctions]], one finds that the orbital angular momentum only allows _integer values_, hence:
$$\displaylines{\hat{L}^2\ket{lm_l}=\hbar^2l(l+1)\ket{lm_l} \hspace{1cm}\hat{L}_z\ket{lm_l}=\hbar m_l\ket{lm_l} \\ l=0, 1, 2,\dots \hspace{1cm} m_l=-l,-l+1,\dots,l-1,l}$$
- A _measurement of magnitude_ will yield:
$$|\bm{L}|=\hbar\sqrt{l(l+1)}$$

### Remarks
- The value of $L^2$ is _always_ larger than the maximum value of $L_z$ as $l(l+1)>l^2$
- Remember that when $L^2$ and $L_z$ are determinate, $L_x$ and $L_y$ are _always indeterminate_
- After deriving these results, one can also find the effect of the ladder operators:
$$\hat{L}_\pm\ket{lm_l}=\hbar\sqrt{l(l+1)-m_l(m_l\pm1)}\ket{l(m_l\pm1)}$$
- The values of angular momentum can be pictured as so:
![[Angular momentum eigenstates.png]]
- The _uncertainty relation_ for the other two components of $\bm{L}$:
$$\Delta L_x\Delta L_y\geq \frac{\hbar}{2}|\mean{L_z}|$$
- Special case where all three components are known: $L^2=L_x=L_y=L_z=0$

### The operators in spherical coordinates
- Before finding the eigenfunctions, it is helpful to rewrite the operators in spherical coordinates
- The total angular momentum vector operator:
$$\hat{\bm{L}}=-i\hbar\left( \hat{\phi}\pd{}{\theta}-\hat{\theta} \frac{1}{\sin\theta}\pd{}{\phi}\right)$$
- The ladder operators:
$$\hat{L}_\pm=\pm\hbar\exp(\pm i\phi)\left(\pd{}{\theta}\pm i\cot\theta\pd{}{\phi}\right)$$
- Square of total angular momentum:
$$\hat{L}^2=-\hbar^2\left[\frac{1}{\sin\theta}\pd{}{\theta} \left(\sin\theta\pd{}{\theta}\right) +\frac{1}{\sin^2\theta}\pd{^2}{\phi^2}\right]$$
- Angular momentum along $z-$direction:
$$\hat{L}_z=-i\hbar\pd{}{\phi}$$

### Eigenfunctions of orbital angular momentum
- By inspecting the DEs resulting from applying $\hat{L}^2$ and $\hat{L}_z$, one can see that the eigenfunctions are the [[Special functions and orthogonal relations#Spherical harmonics|spherical harmonics]] $Y^m_l$

- For spherical harmonics, $l$ _only takes on integer values_

## Spin angular momentum
- In quantum mechanics, there is a fundamental difference between _orbital_ and _spin_ angular momentum, where the latter is an _intrinsic property of the particle_

- They follow the same commutation relations as orbital angular momentum:
$$[\hat{S}_i,\hat{S}_j]=\epsilon_{ijk}i\hbar\hat{S}_k$$
- It also follows the same eigenvalue equations:
$$\displaylines{\hat{S}^2\ket{sm_s}=\hbar^2s(s+1)\ket{sm_s}\hspace{1cm} \hat{S}_z\ket{sm_s}=\hbar m_s\ket{sm_s} \\ \hat{S}_\pm\ket{sm_s}=\hbar\sqrt{s(s+1)-m_s(m_s\pm1)}\ket{s(m_s\pm1)}}$$
- Here, the spin ladder operators have the same definition as the ones for angular momentum.

- While $l$ can only take integer values, $s$ does not have this constraint:
$$s=0,\frac{1}{2},1,\frac{3}{2}\dots \hspace{1cm} m_s=-s,-s+1,\dots,s-1,s$$

- Particles have _immutable_ values of $s$
	- $\pi$ mesons: $s=0$
	- electrons: $s=1/2$
	- Photons: $s=1$
	- $\Delta$ baryons: $s=3/2$
	- Gravitons: $s=2$

### Spin 1/2


### Singlet and triplet states
- Consider 2 spin $1/2$ particles
- The addition of the $z$ component is straight-forward:
$$$$

### General addition of spin

# Total angular momentum
