- The _angular momentum_ of a particle is an _observable quantity_, represented by a _vector_
- Therefore, there is a _corresponding operator_, with its own set of eigenfunctions

- The angular momentum resulting from the _"motion"_ of a particle in quantum mechanics is more precisely known as _orbital angular momentum_, denoted $\hat{\bm{L}}$
- Later, it was discovered that a particle also has an _spin angular momentum_, denoted $\hat{\bm{S}}$ which is _intrinsic_, and has _no spatial dependence_

- It is also convenient to define a _total angular momentum_ $\hat{\bm{J}}\equiv\hat{\bm{L}}+\hat{\bm{S}}$

- [x] Start addition of angular momentum ⏫ 📅 2023-10-10 ✅ 2023-10-11
# Orbital angular momentum
- The _orbital_ angular momentum is _analagous to classical angular momentum_:
$$\displaylines{\hat{\bm{L}}=\hat{\bm{X}}\wedge\hat{\bm{P}} \hspace{1cm} \hat{L}_i=\epsilon_{ijk}\hat{X}_j\hat{P}_k}$$
- There is _one operator for each direction_, as well as a _total orbital angular momentum operator_:
$$\hat{\bm{L}}^2=\hat{L}_x^2+\hat{L}_y^2+\hat{L}_z^2$$
- From its definition, _orbital_ angular momentum is found to obey the _commutation relations_:
$$\displaylines{[\hat{L}_i,\hat{L}_j]=i\hbar\epsilon_{ijk}\hat{L}_k \hspace{1cm} \hat{\bm{L}}\wedge\hat{\bm{L}}=i\hbar\hat{\bm{L}} \\ [\hat{L}_i,\hat{r}_j]=i\hbar\epsilon_{ijk}\hat{r}_k\hspace{1cm}[\hat{L}_i,\hat{p}_j]=i\hbar\epsilon_{ijk}\hat{p}_k \\ [\hat{L}_i,\hat{L}^2]=[\hat{L}_i,\hat{r}^2] = [\hat{L}_i,\hat{p}^2]=0}$$
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

- From this, one can see that for any _radial function_ $f(r)$:
$$[f(r),\hat{L}]=0$$

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
- Note that they are _Hermitian conjugates_ of each other, as $\hat{L}_\pm^\dagger=\hat{L}_\mp$

- The ladder operators satisfy the _commutation relations_:
$$[\hat{L_z},\hat{L}_\pm]=\pm\hbar\hat{L}_\pm \hspace{1cm} [\hat{L}^2,\hat{L}_\pm]=0\hspace{1cm}[\hat{L}_+,\hat{L}_-]=2\hbar\hat{L}_z$$
- It is worth noting their form in _spherical coordinates_:
$$\hat{L}_\pm=\hbar\exp(\pm i\phi)\left[\pm\pd{}{\theta}+i\cot\theta\pd{}{\phi}\right]$$

- _Combining_ the two ladder operators also yields the following relation:
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

- Appearance of the spherical harmonics:
![[Spherical harmonics.png]]
- An _equal mix_ of $m$'s is _isotropic_:
$$\sum_{m=-l}^{+l}=\text{const.}$$

# Spin angular momentum
- From the _Stern-Gerlach_ experiment, it was shown that there is a type of _angular momentum with no spatial dependence_, which was also _quantised_
- A beam of particles known to have a _magnetic dipole moment_ is sent through an _inhomogeneous magnetic field_:
![[Stern-Gerlach experiment.png]]
- From other experiments, it was found that the _degeneracy_ of the angular momentum in one direction can be _even_
- Hence, the analagous quantum number to $l$ can also take _half-integer values_

- Spin angular momentum has _no spatial dependence_, and _no classical analogue_, and hence _cannot be written in terms of other operators_

- The _spin angular momentum operators_ follow the _same commutation relations_ as orbital angular momentum:
$$[\hat{S}_i,\hat{S}_j]=\epsilon_{ijk}i\hbar\hat{S}_k \hspace{1cm} [\hat{S}_i,\hat{S}^2]=0$$

- One can still define the _ladder operators_:
$$\hat{S}_\pm=S_x\pm iS_y$$
- Since these operators have the _same algebraic structure_, they obey _the same eigenvalue equations_:
$$\displaylines{\hat{S}^2\ket{sm_s}=\hbar^2s(s+1)\ket{sm_s}\hspace{1cm} \hat{S}_z\ket{sm_s}=\hbar m_s\ket{sm_s} \\ \hat{S}_\pm\ket{sm_s}=\hbar\sqrt{s(s+1)-m_s(m_s\pm1)}\ket{s(m_s\pm1)}}$$

- While $l$ can only take integer values, $s$ does not have this constraint:
$$s=0,\frac{1}{2},1,\frac{3}{2}\dots \hspace{1cm} m_s=-s,-s+1,\dots,s-1,s$$

- Particles have _immutable_ values of $s$
	- $\pi$ mesons: $s=0$
	- Electrons: $s=1/2$
	- Photons: $s=1$
	- $\Delta$ baryons: $s=3/2$
	- Gravitons: $s=2$
- This later gives rise to the [[Principles of quantum mechanics#Bosons and Fermions|spin-statistics theorem]], where spin determines the _exchange symmetry of the wave-function_

### Spin 1/2
- For $s=1/2$, there are only _two possible orientations_, $\ket{m_s=+1/2}$ and $\ket{m_s=-1/2}$
- Denote these as $\ket{\uparrow}$ and $\ket{\downarrow}$ respectively

- One can express the _spin wave function_ as a _spinor_:
$$\displaylines{\wv=\Psi_\uparrow\ket{\uparrow}+\Psi_\downarrow\ket{\downarrow}\\ \Psi\longrightarrow\pmatrix{\Psi_\uparrow\\\Psi_\downarrow}}$$

- In this basis, the _matrix elements_ of the operators are:
$$\displaylines{\hat{S}^2=\frac{3\hbar^2}{4}\pmatrix{1&0\\0&1}\hspace{1.5cm}\hat{S}_z=\frac{\hbar}{2}\pmatrix{1&0\\0&-1}\\\hat{S}_+=\hbar\pmatrix{0&1\\0&0}\hspace{1.5cm}\hat{S}_-=\hbar\pmatrix{0&0\\1&0} \\ \hat{S}_x=\frac{\hbar}{2}\pmatrix{0&1\\1&0}\hspace{1.5cm}\hat{S}_y=\frac{\hbar}{2}\pmatrix{0&-i\\i&0}}$$

- The introduction of spin $1/2$ _doubles_ the dimensionality of the Hilbert space
- One introduces a basis $\ket{xyzs_z}$ which diagonalise the operators $\hat{X},\hat{Y},\hat{Z},\hat{S}_z$
- The state vector in this basis becomes:
$$\braket{xyzs_z|\psi}=\pmatrix{\psi(x,y,z,\hbar/2)\\ \psi(x,y,z,-\hbar/2)}$$
	- where $\psi(x,y,z,\pm\hbar/2)$ are each an _infinite-dimensional_ vector with the values of $\psi$ as a function of position

- Introduce the _Pauli matrices_ $\bm{\sigma}$:
$$\sigma_x=\pmatrix{0&1\\1&0}\hspace{1.5cm}\sigma_y=\pmatrix{0&-i\\i&0}\hspace{1.5cm} \sigma_z=\pmatrix{1&0\\0&-1}$$
- They _anticommute_:
$$[\sigma_i,\sigma_j]_+=0$$
- They follow:
$$\sigma_i\sigma_j=i\epsilon_{ijk}\sigma_k$$
- They are _traceless_:
$$\text{Tr }\sigma_i=0$$
- The _square_ of any Pauli matrix is $I$:
$$\sigma_i^2=I$$
# General angular momenta

## The operators
- The existence of different _types_ of angular momenta, and considering the dynamics of _multiple particles_, motivates the introdution of _general angular momentum operator_:
$$\hat{\bm{J}}=(\hat{J}_x,\hat{J}_y,\hat{J}_z)=(\hat{J}_1,\hat{J}_2,\hat{J}_3)$$
- They must still satisfy the _commutation relations_:
$$[\hat{J}_i,\hat{J}_j]=i\hbar\epsilon_{ijk}\hat{J}_k$$
- The eigenstates are still characterised by _quantum numbers_ $j$ and $m$, which can be _integer/half-integer_:
$$\displaylines{\hat{J}^2\ket{jm}=\hbar^2j(j+1)\ket{jm}\hspace{1cm} \hat{J}_z\ket{jm}=\hbar m\ket{jm}\\\braket{j'm'|jm}=\delta_{jj'}\delta_{mm'} \\ j=0,\frac{1}{2},1,\frac{3}{2}\dots \hspace{1cm} m=-j,-j+1,\dots,j-1,j}$$
- For _orbital_ angular momentum, $j=l$ which only takes _integer_ values
	- Invariance after spatial rotation of $2\pi$
- One can still define _ladder operators_:
$$\displaylines{\hat{J}_\pm=\hat{J_x}\pm i\hat{J}_y\\\hat{J}_\pm\ket{jm}=\hbar\sqrt{j(j+1)-m(m\pm1)}\ket{j(m\pm1)}}$$
- Again, at the _top or bottom_ of the ladder, $\hat{J}_\pm$ simply _annihilates_ the states:
$$\hat{J}_+\ket{jj}=\hat{J}_-\ket{j,-j}=\ket{0}$$

## Matrix elements
- From the _orthonormality_ of the eigenstates, obtain the _matrix elements_:
$$\displaylines{\braket{j'm'|\hat{J}_\pm|jm}=\hbar\sqrt{j(j+1)-m(m\pm1)}\delta_{jj'}\delta_{m',m\pm1}\\ \braket{j'm'|\hat{J}^2|jm}=\hbar^2j(j+1)\delta_{jj'}\delta_{mm'}\\\braket{j'm'|\hat{J}_z|jm}=m\hbar\delta_{jj'}\delta_{mm'}}$$
- One can obtain the matrix elements for $\hat{J}_x$ and $\hat{J}_y$ via:
$$\hat{J}_x=\frac{\hat{J}_++\hat{J}_-}{2}\hspace{1.5cm}\hat{J}_y=\frac{\hat{J}_+-\hat{J}_-}{2i}$$
- As the matrix elements _vanish unless_ $j=j'$, one can consider the matrix as being made of _block diagonals_, with each block corresponding to a value of $j$

- For example, for $j=1/2$:
$$\displaylines{\hat{J}_z=\pmatrix{\braket{\uparrow|\hat{J}_z|\uparrow}&\braket{\uparrow|\hat{J}_z|\downarrow}\\\braket{\downarrow|\hat{J}_z|\uparrow}&\braket{\downarrow|\hat{J}_z|\downarrow}}=\frac{\hbar}{2}\pmatrix{1&0\\0&-1}\\ 
\hat{J}_+=\hbar\pmatrix{0&1\\0&0}\hspace{2cm}\hat{J}_-=\hbar\pmatrix{0&0\\1&0} \\ \hat{J}_x=\frac{\hbar}{2}\pmatrix{0&1\\1&0}\hspace{2cm}\hat{J}_y=\frac{\hbar}{2i}\pmatrix{0&-i\\i&0}}$$
- One then obtains the _Pauli matrices_:
$$\displaylines{\hat{\bm{J}}=\frac{\hbar}{2}\bm{\sigma} \\ \sigma_x=\pmatrix{0&1\\1&0}\hspace{1cm}\sigma_y=\pmatrix{0&-i\\i&0}\hspace{1cm}\sigma_z=\pmatrix{1&0\\0&-1}}$$

## Measurements and uncertainty
- The _uncertainty relation_ for $\hat{J}_x$ and $\hat{J}_y$:
$$\Delta J_x\Delta J_y\geq \frac{\hbar}{2}|\mean{J_z}|$$
- For the _eigenstate_ $\ket{jm}$, $\Delta J_z=0$, and as _possible measured values_ of $\hat{J}_x$ and $\hat{J}_y$ are _evenly distributed_:
$$\mean{\hat{\bm{J}}}=\left(0,0,m\hbar\right)$$
# Addition of angular momenta
- One may want to _add_ different angular momenta in a system
	- _Total angular momentum_ of one particle $\hat{\bm{J}}=\hat{\bm{L}}+\hat{\bm{S}}$
	- _Total spin_ of two particles $\hat{\bm{S}}=\hat{\bm{S}}_1+\hat{\bm{S}}_2$

## Finding the eigenstates
- Let there be an operator comprised of _two generic angular momentum operators_ added:
$$\hat{\bm{J}}=\hat{\bm{J}}'+\hat{\bm{J}}''$$
- It can be represented by a $(2j'+1)(2j''+1)-$dimensional matrix
	- Like before, it is _block-diagonal_
- It follows the _same commutation relations_ as a _general_ angular momentum operator

- It must then itself have _a set of angular momentum eigenstates_:
$$\displaylines{\hat{J}^2\ket{jm}=\hbar^2j(j+1)\ket{jm}\hspace{1cm} \hat{J}_z\ket{jm}=\hbar m\ket{jm}\\\braket{j'm'|jm}=\delta_{jj'}\delta_{mm'} \\ j=0,\frac{1}{2},1,\frac{3}{2}\dots \hspace{1cm} m=-j,-j+1,\dots,j-1,j}$$
- One can see that the _product state_ $\ket{jm}=\ket{j'm'}\otimes\ket{j''m''}$ is an eigenstate of $\hat{J}_z$, but _in general_ is _not_ an eigenstate of $\hat{J}^2$
$$\displaylines{(\hat{J}_z'+\hat{J}_z'')\ket{jm}=(m'+m'')\hbar\ket{jm}\\ m=m'+m''}$$
- In _general_, the eigenstate should b e written as a _linear combination_ of the original eigenstates:
$$\ket{jm}=\sum_{m',m''}\left[\ket{j'm'}\otimes\ket{j''m''}\right]\braket{j'm';j''m''|jm}$$
- The sum is over valus of $m'$ and $m''$ such that $m'+m''=m$
	- Or one can treat the inner products as _zero_
- The inner products are known as the _Clebsh-Gordan coefficients_, and give the _overlap_ between the states
- The _matrix_ of coefficients is a _block-diagonal, unitary_ matrix
	- It is not just unitary, but _orthogonal_ as the coefficients are _real_

- For a _given_ $j'$ and $j''$, one can show that $j$ takes the values:
$$j=j'+j'',j'+j''-1,\dots,|j'-j''|+1,|j'-j''|$$
- Intuitively, from the angular momentum vectors being _parallel_ to _anti-parallel_
- The _maximum_ values of $m'$ and $m''$ are simply $j'$ and $j''$ respectively
- Hence, the maximum possible value of $m$ is simply $j'+j''$, as expected

- Typically, $j'$ and $j''$ are _given_ but one can also specify the state as $\ket{jmj'j''}$

- For a _given_ $j'$ and $j''$, start with the state $j=j'+j''$ with the _maximum_ $m$:
$$\ket{j=j'+j'', m=j'+j''}=\ket{j'j'}\otimes\ket{j''j''}$$
- One can then apply the _ladder operator_:
$$\displaylines{\hat{J}_\pm=\hat{J}_\pm'+\hat{J}_\pm''\\\hat{J}_\pm\ket{jm}=\left(\hat{J}'_\pm\ket{j'm'}\right)\otimes\ket{j''m''}+\ket{j'm'}\otimes\left(\hat{J}_\pm''\ket{j''m''}\right)}$$
- To obtain states of _other_ $j$ but _same_ $m$, use the fact that the states are _orthogonal_:
$$\braket{j_1m|j_2m}=0$$

![[Clebsch-Gordan coefficients.png]]

- For $j_1=j_2$, the _resultant_ eigenstate is either _symmetric or antisymmetric_ w.r.t. _particle exchange_:
$$\ket{j_2m_2j_1m_1}=(-1)^{j-(j_1+j_2)}\ket{j_1m_1j_2m_2}$$
## Two spin-1/2 particles
- For $s'=s''=1/2$, start from the state:
$$\ket{11}=\ket{\uparrow}\ket{\uparrow}$$
- Applying the operator $\hat{S}_-=\hat{S}'_-+\hat{S}''_-$:
$$\ket{10}=\frac{1}{\sqrt{2}}\left(\ket{\uparrow}\ket{\downarrow}+\ket{\downarrow}\ket{\uparrow}\right)$$
- The state with $s=1$ and $m_s=-1$ is obvious:
$$\ket{1,-1}=\ket{\downarrow}\ket{\downarrow}$$
- Then from the fact that $\braket{10|00}=0$:
$$\ket{00}=\frac{1}{\sqrt{2}}\left(\ket{\uparrow}\ket{\downarrow}-\ket{\downarrow}\ket{\uparrow}\right)$$

- The $s=1$ ladder is known as the _triplet_ state
- The $s=0$ ladder is known as the _singlet_ state

- This is significant when studying the electron wave-function of the [[Molecular quantum mechanics#The Helium atom|helium atom]]

## The trivial case
- Consider the combination $0\otimes j$
- The total angular momentum states are then:
$$\ket{jm}=\ket{00}\otimes\ket{jm}$$
- This correspods to Clebsch-Gordan coefficients:
$$\braket{00;jm|j'm'}=\delta_{jj'}\delta_{mm'}$$