- Main sources:
	-  Floquet Engineer's Handbook (Rudner and Lidner)
	- Introduction to Loquet Theory (Viebahn)

- A system governed by a _time-periodic Hamiltonian_:
$$\displaylines{i\hbar \frac{d}{dt}\ket{\psi}=H(t)\ket{\psi}   \\ H(t+T)=H(t)}$$
- This is analagous to [[Solids#Bloch's Theorem|Bloch's Theorem]] in solids
- Define _Floquet states_ that satisfy:
$$\ket{\psi_{n}(t)}=\exp\left( -\frac{i\varepsilon_{n}t}{\hbar} \right)\ket{\Phi_{n}(t)}\qquad \ket{\Phi_{n}(t+T)}=\ket{\Phi_{n}(t)}    $$
- One can _Fourier decompose_ $\ket{\Phi_{n}(t)}$
$$\ket{\Phi_{n}(t)}=\sum_{m}\exp(-im\omega t)\ket{\phi_{n}^{(m)}}  $$
- 