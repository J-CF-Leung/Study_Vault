- The _angular momentum_ of a particle is an _observable quantity_, represented by a _vector_
- Therefore, there is a _corresponding operator_, with its own set of eigenfunctions

- The angular momentum resulting from the _"motion"_ of a particle in quantum mechanics is more precisely known as _orbital angular momentum_, denoted $\hat{\bm{L}}$
- Later, it was discovered that a particle also has an _spin angular momentum_, denoted $\hat{\bm{S}}$ which is _intrinsic_, and has _no spatial dependence_

- It is also convenient to define a _total angular momentum_ $\hat{\bm{J}}\equiv\hat{\bm{L}}+\hat{\bm{S}}$

# Orbital angular momentum
- The _orbital_ angular momentum is _analagous to classical angular momentum_:
$$\displaylines{\hat{\bm{L}}=\hat{\bm{X}}\wedge\hat{\bm{P}} \hspace{1cm} \hat{L}_i=\epsilon_{ijk}\hat{X}_j\hat{P}_k}$$
- There is _one operator for each direction_, as well as a _total orbital angular momentum operator_:
$$\hat{\bm{L}}^2=\hat{L}_x^2+\hat{L}_y^2+\hat{L}_z^2$$
- From its definition, _orbital_ angular momentum is found to obey the _commutation relations_:
$$\displaylines{[\hat{L}_i,\hat{L}_j]=i\hbar\epsilon_{ijk}\hat{L}_k \hspace{1cm} \hat{\bm{L}}\wedge\hat{\bm{L}}=i\hbar\hat{\bm{L}} \\ [\hat{L}_i,\hat{L}^2]=0}$$
## In different bases
- In the _Cartesian basis_, the operators can be written as:
$$\displaylines{\hat{L}_i=\epsilon_{ijk}\hat{X}_j\hat{P}_k\xrightarrow{x\text{ basis}}-i\hbar \bm{r}\wedge\nabla=-i\hbar\epsilon_{ijk} x_j\pd{}{x_k} \\ \hat{L}_x\to -i\hbar \left(y\pd{}{z}-z\pd{}{y}\right) \hspace{0.2cm},\hspace{0.2cm} \hat{L}_y\to -i\hbar \left(z\pd{}{x}-x\pd{}{z}\right) \hspace{0.2cm},\hspace{0.2cm} \hat{L}_z\to -i\hbar \left(x\pd{}{y}-y\pd{}{x}\right)}$$
- By expressing $\nabla$ in terms of _spherical coordinates_:
$$\hat{\bm{L}}\xrightarrow{\theta,\phi\text{ basis}}-i\hbar\left( \hat{\phi}\pd{}{\theta}-\hat{\theta} \frac{1}{\sin\theta}\pd{}{\phi}\right)$$
- Of significance is the form of $\hat{L}_z$ in spherical coordinates:
$$\hat{L}_z\xrightarrow{\theta,\phi\text{ basis}}-i\hbar\pd{}{\phi}$$

- From this, the form of the _total orbital angular momentum_ operator is:
$$\hat{L}^2\xrightarrow{\theta,\phi\text{ basis}} -\hbar^2\left[ \frac{1}{\sin\theta}\pd{}{\theta}\left(\sin\theta \pd{}{\theta}\right)+\frac{1}{\sin^2\theta}\pd{^2}{\phi^2}\right]$$
- This is the _angular part of the Laplacian_

## The eigenvalue problem
- The operators $\bm{\hat{L}}^2$ and $\hat{L}_z$ _commute_
- Hence, their eigenvalue problems can be solved _simultaneously_

- Let there be a simultaneous eigenbasis $\ket{\lambda\mu}$
- This eigenvalue problem can be expressed as:
$$L^2\ket{\lambda\mu}=\lambda\ket{\lambda\mu} \hspace{1.5cm}L_z \ket{\lambda\mu}=\mu \ket{\lambda\mu}$$

### Ladder operators
- Like the [[Quantum Harmonic Oscillator|quantum harmonic oscillator]] problem, finding eigenfunctions of angular momentum also involves _ladder operators_
- The ladder operators for angular momentum are defined as:
$$\hat{L}_\pm=L_x\pm iL_y$$
- The ladder operators satisfy the _commutation relations_:
$$[\hat{L_z},\hat{L}_\pm]=\pm\hbar\hat{L}_\pm \hspace{2cm} [\hat{L}^2,\hat{L}_\pm]=0$$
- It is worth noting their form in _spherical coordinates_:
$$\hat{L}_\pm=\hbar\exp(\pm i\phi)\left[\pm\pd{}{\theta}+i\cot\theta\pd{}{\phi}\right]$$

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
- There are $2l+1$ values of $m_l$, which always results in an _odd number_ since $l$ is an integer

- $m_l$ is known as the _magnetic angular momentum quantum number_
- $l$ is known as the _orbital angular momentum quantum number_

- A _measurement of magnitude_ will yield:
$$|\bm{L}|=\hbar\sqrt{l(l+1)}$$
- After deriving these results, one can also find the effect of the _ladder operators_:
$$\hat{L}_\pm\ket{lm_l}=\hbar\sqrt{l(l+1)-m_l(m_l\pm1)}\Ket{l,(m_l\pm1)}$$

### Remarks
- The value of $L^2$ is _always_ larger than the maximum value of $L_z$ as $l(l+1)>l^2$
- Remember that when $L^2$ and $L_z$ are determinate, $L_x$ and $L_y$ are _always indeterminate_
- The values of angular momentum can be pictured as so:
![[Angular momentum eigenstates.png]]
- The _uncertainty relation_ for the other two components of $\bm{L}$:
$$\Delta L_x\Delta L_y\geq \frac{\hbar}{2}|\mean{L_z}|$$
- Special case where _all three components are known_: $L^2=L_x=L_y=L_z=0$

- Given the action of the operators on $\ket{lm_l}$, it is worth knowing the _matrix elements_:
$$\displaylines{\braket{lm_l'|\hat{L}_z|lm_l}=\hbar m_l\delta_{m_l, m_l'} \\ \braket{lm_l'|\hat{L}_\pm|lm_l}=\hbar\sqrt{l(l+1)-m_l(m_l\pm1)}\delta_{m_l',m_l\pm1}}$$


### Eigenfunctions of orbital angular momentum
- By inspecting the DEs resulting from applying $\hat{L}^2$ and $\hat{L}_z$, one can see that the eigenfunctions are the [[Special functions and orthogonal relations#Spherical harmonics|spherical harmonics]] $Y^m_l$
- Or, one can use the operators in spherical coordinates to find some general features:
$$\displaylines{\hat{L}_z\ket{lm_l}=\hbar m_l\ket{lm_l}\to-i\hbar\pd{}{\phi}Y_l^{m_l}(\theta,\phi)=\hbar m_l Y^{m_l}_l(\theta,\phi) \\ Y_l^{m_l}(\theta,\phi)=F_l^{m_l}(\theta)\exp(im_l\phi)}$$
- A _complete rotation_ $\phi\to\phi+2\pi$ must leave the wave function _unchanged_, hence $m_l$ and $l$ must be _integers_

- Consider the state of _maximum $L_z$_:
$$\displaylines{\hat{L}_+\ket{l,l}=0 \to \left(\pd{}{\theta}-l\cot\theta\right)F_l^{l}(\theta)=0 \\ Y_l^l(\theta,\phi)=c_l(\sin\theta)^l\exp(il\phi)}$$
- Then, by _normalising_:
$$\int |Y_l^l(\theta,\phi)|^2\sin\theta\,d\theta\,d\phi=1\longrightarrow c_l=\frac{(-1)^l}{2^ll!}\sqrt{\frac{(2l+1)!}{4\pi}}$$
- Then, the other states can be found by _applying the ladder operators_:
$$\displaylines{\hat{L}_\pm\ket{lm_l}=\hbar\sqrt{l(l+1)-m_l(m_l\pm1)}\Ket{l,(m_l\pm1)} \\ Y_l^{m_l}(\theta,\phi)=\sqrt{\frac{(l-m)!}{(2l)!(l-m)!}}\left(\frac{\hat{L}_-}{\hbar}\right)^{l-m_l}Y_l^l(\theta,\phi)}$$

- It is worth noing what the _parity operator_ does to the eigenfunctions:
$$\hat{P}Y_l^{m_l}(\theta,\phi)=Y_l^{m_l}(\pi-\theta,\pi+\phi)=(-1)^lY_l^{m_l}(\theta,\phi)$$
- Hence, they are _eigenfunctions of the parity operator_

# Spin angular momentum
- From the _Stern-Gerlach_ experiment, it was shown that there is a type of _angular momentum with no spatial dependence_, which was also _quantised_
- A beam of particles known to have a _magnetic dipole moment_ is sent through an _inhomogeneous magnetic field_:
![[Stern-Gerlach experiment.png]]
- From other experiments, it was found that the _degeneracy_ of the angular momentum in one direction can be _even_
- Hence, the analagous quantum number to $l$ can also take _half-integer values_

- Spin angular momentum has _no spatial dependence_, and _no classical analogue_, and hence _cannot be written in terms of other operators_

- The _spin angular momentum operators_ follow the _same commutation relations_ as orbital angular momentum:
$$[\hat{S}_i,\hat{S}_j]=\epsilon_{ijk}i\hbar\hat{S}_k \hspace{1cm} [\hat{S}_i,\hat{S}^2]=0$$


- It also follows the same eigenvalue equations:
$$\displaylines{\hat{S}^2\ket{sm_s}=\hbar^2s(s+1)\ket{sm_s}\hspace{1cm} \hat{S}_z\ket{sm_s}=\hbar m_s\ket{sm_s} \\ \hat{S}_\pm\ket{sm_s}=\hbar\sqrt{s(s+1)-m_s(m_s\pm1)}\ket{s(m_s\pm1)}}$$


- While $l$ can only take integer values, $s$ does not have this constraint:
$$s=0,\frac{1}{2},1,\frac{3}{2}\dots \hspace{1cm} m_s=-s,-s+1,\dots,s-1,s$$

- Particles have _immutable_ values of $s$
	- $\pi$ mesons: $s=0$
	- Electrons: $s=1/2$
	- Photons: $s=1$
	- $\Delta$ baryons: $s=3/2$
	- Gravitons: $s=2$
- This later gives rise to the [[Fundamental concepts of quantum mechanics#Multiple degrees of freedom|spin statistics theorem]]

### Spin 1/2


### Singlet and triplet states
- Consider 2 spin $1/2$ particles
- The addition of the $z$ component is straight-forward:
$$$$

### General addition of spin

# Adding angular momenta
