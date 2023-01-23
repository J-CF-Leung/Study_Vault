Insert good/inspirational/silly quote here

# The birth of quantum mechanics

## The photoelectric effect
![[Photoelectric effect.png]]
- Let there be monochromatic light _incident on some electrode_ (the cathode)
- The light _gives energy to the electrons_, allowing them to escape
- By result, there will be a _photocurrent_ travelling between electrodes

- The energy needed to _release_ an electron is the _work function_ $W$
- After escaping the metal, there is still some _kinetic energy_

- One can apply an _external voltage_ to either _accelerate or decelerate_ the electrons
- At some voltage $-V_0$, known as the _stopping voltage_, the _photocurrent vanishes_

![[Photoelectric effect behaviour.png]]
- The photocurrent is _dependent on intensity and frequency_
- If intensity is increased, _number of electrons emitted does not change_
	- Hence, _energy of each electron is independent of intensity_

- However, if light frequency is increased, _kinetic energy of the electrons increases_

- Conservation of energy:
$$\displaylines{\frac{1}{2}mv^2=eV_0=h\nu-W \\ V_0=\frac{h\nu}{e}-\frac{W}{e}}$$
- The _slope_ of the graph is _universal for all materials_

- From this, the conclusion was:
- Energy _can only be extracted in packets_
- The energy of each packet is _proportional to frequency_:
$$E=hf=\hbar\omega$$
- Here, $h$ is _Planck's constant_
- $\hbar$ is the _reduced Planck's constant_, given by $h/(2\pi)$

## Blackbody radiation
- A _perfect blackbody absorbs all radiation_, with no reflections 

- The _energy density_ of the radiation is given by the _density of states_ multiplies by the _energy of each state_
- Consider the _number of states_ with frequency range between $\nu$ and $\nu+d\nu$:
$$dn=N(\nu)\,d\nu=\frac{8\pi\nu^2}{c^3}d\nu$$
- From classical thermodynamics, the energy of each state is given by $k_BT$
- Hence, the _Rayleigh-Jeans Law_ gives:
$$\rho_E(\nu,T)\,d\nu=\frac{8\pi\nu^2}{c^3}k_BT\,d\nu$$
- From this, as _frequency increases_, _energy density increases without bound_
- This is known as the _ultraviolet catastrophe_
![[Blackbody radiation.png]]

- From this, Planck suggested that the energy is _quantised_ in intervals of $h\nu$
- These levels follow the _Boltzman distribution_
- Hence, the _average energy_ at frequency $\nu$ is:
$$\overline{\epsilon}=\frac{\sum_{n=0}^\infty nh\nu\exp(-nh\nu/k_BT)}{\sum_{n=0}^\infty\exp(-nh\nu/k_BT)}=\frac{h\nu}{\exp(-h\nu/k_BT)-1}$$
- Therefore, _high frequency states are relatively unoccupied_

- Hence:
$$\rho(\nu,T)=\frac{8h\pi\nu^3}{c^3}\frac{1}{\exp(-h\nu/k_BT)-1}$$
- This is _Planck's Law_
- It matched spectral measurements

- In the _low-frequency limit_, or if $h\to0$, the _Rayleigh-Jeans Law is regained_
- Hence, classical behaviour exists as some _limit_, this is known as the _Correspondence Principle_

## Quantisation and de Broglie's hypothesis
- From classical electromagnetism, light exists _as a continuous wave_
- From the above two experiments, it was concluded that electromagnetic radiation is _quantised_ in the form of _photons_, which are _wave packets_

- The _quantised energy_ $E=nh\nu$ is a property _of the photons_ (not the electrons in the photoelectric effect)

- The _de Broglie hypothesis_ states that _individual particles have wave-like properties_
- If the particle has momentum $\bm{p}$, it has the wavevector $\bm{k}$ related by:
$$\displaylines{p=h/\lambda \\\bm{p}=\hbar\bm{k}}$$

## Bohr's hydrogen atom
- According to classical electromagnetism, if _charged particles accelerate_, they _emit radiation and lose energy_
- Hence, if an electron is _orbiting around a nucleus_, they _must lose energy and the atom collapses_

- Bohr proposed that the electron can exist in _discrete, stable orbits_
- In order for an orbit with radius $r_n$ to be stable, it must satisfy:
$$2\pi r_n=n\lambda_n=nh/p_n$$
- Any mode not satisfying this will _destructively interfere_

- Therefore, the _angular momentum is quantised_:
$$L_n=n\hbar$$
- One can calculate the _total energy_:
$$E_n=-\frac{e^2}{8\pi\epsilon_0 r_n}=-\frac{m_ee^4}{8\epsilon_0^2h^2}\frac{1}{n^2}=-\frac{hcR}{n^2}$$
- Here, $R$ is the _Rydberg constant_:
$$R\equiv\frac{m_ee^4}{8\epsilon_0^2h^3c}$$

- Therefore, the _atomic emission lines_ are discrete
- The emission line representing a transition from level $n$ to $m$:
$$\Delta E=hcR\left(\frac{1}{n^2}-\frac{1}{m^2}\right)$$