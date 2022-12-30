## Structure of solid ionic conducting materials
- Charge carriers: defects
	- Pairs of vacancies in anion and cation sites (Shottky defect)
	- Ion moves from site to interstice, leaving a vacancy behind (Frenkel defect)
	- Migration: swapping positions with other ions, enhanced by vacancies
- Factors affecting ion current
	- Availability of vacancies -> concentration gradient
	- Energy barrier between lattice sites
	- External electric field -> drift current
- Diffusion current from concentration gradient:
	- Fick's first law gives current density as:
	$$j=-qD\frac{\partial n}{\partial x}$$
	- Diffusivity $D$ has Arrhenius behaviour:
	$$D=D_0\exp(-\frac{Q}{RT})$$
	- Number of ions with a particular potential follows Boltzmann statistics:
	$$n=n_0\exp{(-\frac{qV}{kT})}$$
- Drift current:
$$j=-\sigma\frac{\partial V}{\partial x}$$
	- $\sigma=$ conductivity
- At equilibrium, both current densities are equal and opposite, leading to the Nernst-Einstein equation:
$$\frac{\sigma}{D}=\frac{nq^2}{kT}$$
- For small electric field where $\exp(qV/kT)\approx 1$:
$$\ln\sigma\approx\ln\sigma_0-(\frac{Q}{k})\frac{1}{T}$$

### Example of solid ionic conductor: Yttrium stabilised zicronia (YSZ)
- Zicronia $\ce{ZrO2}$ has a fluorite structure: fcc with anions in all tetrahedral interstices
- Doped with yttria $\ce{Y2O3}$, replacing $\ce{Zr^{4+}}$ with $\ce{Y^{3+}}$ 
- Oxygen vacancies are created to maintain charge neutrality, becoming charge carriers