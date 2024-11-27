- Main sources:
	-  Floquet Engineer's Handbook (Rudner and Lidner)
	- Introduction to Floquet Theory (Viebahn)

- A system governed by a _time-periodic Hamiltonian_:
$$\displaylines{i\hbar \frac{d}{dt}\ket{\psi}=H(t)\ket{\psi}   \\ H(t+T)=H(t)}$$

# Floquet Theorem
- This is analagous to [[Solids#Bloch's Theorem|Bloch's Theorem]] in solids
- Define _Floquet states_ that satisfy:
$$\ket{\psi_{n}(t)}=\exp\left( -\frac{i\varepsilon_{n}t}{\hbar} \right)\ket{\Phi_{n}(t)}\qquad \ket{\Phi_{n}(t+T)}=\ket{\Phi_{n}(t)}    $$
- $\varepsilon_{n}$ is the _quasi-energy_, which is _analagous to quasi-momentum_

- One can _Fourier decompose_ $\ket{\Phi_{n}(t)}$ and $H(t)$, with $\omega=2\pi/T$:
$$\displaylines{\ket{\Phi_{n}(t)}=\sum_{m}\exp(-im\omega t)\ket{\phi_{n}^{(m)}}  \\
H(t)=\sum_{m}\exp(-im\omega t)H^{(m)}}$$
- One gets the time-dependent Schrodinger equation in the forms:
$$\begin{align}
\left( \varepsilon_{n}+i\hbar \frac{d}{dt} \right)\ket{\Phi_{n}(t)}&=H(t)\ket{\Phi_{n}(t)}   \\
(\varepsilon_{n}+m\hbar\omega)\ket{\phi_{n}^{(m)}}&=\sum_{m'}H^{(m-m')}\ket{\phi_{n}^{(m')}}  
\end{align}$$
- The eigenvalue equation can be written using the _block matrix_:
$$\displaylines{\mathcal{H}\boldsymbol{\varphi}_{n}=\varepsilon_{n}\boldsymbol{\varphi}_{n} \\
\mathcal{H}=\pmatrix{\ddots & H^{(-1)}& H^{(-2)}& \\
H^{(1)}&H^{(0)}-m\hbar\omega & H^{(-1)}& H^{(-2)} \\ H^{(2)}&H^{(1)}&H^{(0)}-(m+1)\hbar\omega &H^{(-1)} \\ & H^{(2)} & H^{(1)} &\ddots} \qquad \boldsymbol{\varphi}_{n}=\pmatrix{\vdots \\ \ket{\phi ^{(m)}} \\ \ket{\phi^{(m+1)}}\\ \vdots }}$$
- The matrix is in _blocks_ of $d\times d$, where $d$ is the _dimension_ of $H(t)$
- There are _infinite_ blocks as $m$ runs over an _infinite range_

- Let there then be a _rectangular matrix_ of phase factors:
$$P_{\omega}(t)=\pmatrix{\dots &\exp(-im\omega t)\mathbb{I}_{d\times d}& \exp(-i(m+1)\omega t)\mathbb{I}_{d\times d}&\dots}$$
- Such that one can _map_ between the _extended matrix_ from the eigenvalue equation, and the _physical Hilbert space_, by _contracting_:
$$P_{\omega}(t)\boldsymbol{\varphi}_{n}=\ket{\Phi_{n}(t)} $$
# The Floquet Brillouin zone
- The _extended space_ is _redundant_, as the _physical solutions_ are _repeated_ across the space
- One can _add_ an _interger multiple_ of $\hbar\omega$ to the _quasi-energy_ while _leaving the physical wavefunction unchanged_
$$\begin{align}
\ket{\psi_{n}}&=\exp\left[ -\frac{i(\varepsilon_{n}+m'\hbar\omega)t}{\hbar} \right]\sum_{m}\exp[-i(m-m')\omega t]\ket{\phi_{n}^{(m)}}  \\
&=\exp\left[ -\frac{i\tilde{\varepsilon}_{n}t}{\hbar} \right]\sum_{m} \exp(-im\omega t)\ket{\tilde{\phi}_{n}^{(m)}} 
\end{align}$$

- The _spectrum_ of the system will _repeat_, with periodicity of the _Floquet Brillouin zone_ of width $\hbar\omega$

- Physical meaning: the _absorption_ or _emission_ of $\hbar\omega$
	- Example: a _light-driven_ system, with _photon absorption/emission_

