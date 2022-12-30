## Thermodynamics of mixing
- Mixing of two elements $A$ and $B$ in a lattice
- Quantity to minimise: [[Thermodynamics|Free Energy]] $F$
- Free energy change in mixing:
	- Entropy change of mixing
	$$\Delta S=-k_BM\left[\Phi\ln\Phi+(1-\Phi)\ln(1-\Phi)\right]$$
		- $M$: Number of lattice sites
		- $\Phi$: Volume fraction of polymer
	- Change in interaction energy upon mixing, using mean-field approximation:
	$$\Delta U=\chi Mk_BT\Phi(1-\Phi)$$
	$$\chi\equiv\frac{z}{2}\frac{2\epsilon_{AB}-\epsilon_{AA}-\epsilon_{BB}}{k_BT}$$
		- $\chi$: Parameter, $\epsilon=$ interaction energies
		- $z$: coordination number
	- Free energy density of mixing
	$$f=\frac{\Delta F}{M}=\frac{\Delta U-T\Delta S}{M}=k_BT\left[\Phi\ln\Phi+(1-\Phi)\ln(1-\Phi)+\chi\Phi(1-\Phi)\right]$$
![[Free energy of mixing.png|400]]
- Temperature or $\chi$ dependence:
	- At low temperature/high $\chi$, intermediate concentrations are unstable, phase separation is favourable
	- At high temperature/low $\chi$, intermediate concentration is stable
- Binodal: the curve describing which 2 phases can co-exist
	- Two phases have equal chemical potential $\mu=\partial F/\partial N$
	- Inside binodal, phase separation is favourable but requires nucleation
- Spinodal decomposition: at central range, $\partial^2F/\partial\Psi^2<0$, phase separation occurs spontaneously
![[Binodal and spinodal.png|250]]

### Flory-Huggins model
- Flory-Huggins model: Behaviour of polymer in a solvent
- Segments of a polymer are adjacent to each other, reducing its entropy by a factor of $N$
$$\Delta S_{FH}=-k_BM\left[\frac{\Phi}{N}\ln\Phi+(1-\Phi)\ln(1-\Phi)\right]$$
- The free energy density of mixing becomes:
$$f=k_BT\left[\frac{\Phi}{N}\ln\Phi+(1-\Phi)\ln(1-\Phi)+\chi\Phi(1-\Phi)\right]$$
- The free energy density curve, the spinodal and the binodal become asymmetric