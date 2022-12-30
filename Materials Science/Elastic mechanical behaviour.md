## Stress and strain
- Tensile load: force normal to surface
	- Tensile/compressive stress $\sigma=F/A_0$
	- Tensile/compressive strain $\epsilon=\delta l/l_0$
	- Approximations: constant area
- Stress-strain behaviour: independent of object geometry
![[Stress-strain.png|300]]
	- $\sigma\propto\epsilon$: elastic region, fully reversible
	- Small required stress for large strain: plastic region, non-reversible
	- Yield point $\sigma_Y$: end of elastic region
	- Tensile stress $\sigma_U$: peak stress
	- End of graph: mechanical failure
- Shear load: force parallel to surface
	- Shear stress $\tau=F/A_0$
	- Shear strain $\gamma=\delta y_0/x_0=\tan\phi$
- Poisson's ratio $\nu$: ratio of lateral contraction to axial elongation
	-  Elongation in $z-$direction: $\epsilon_x=\epsilon_y=-\nu\epsilon_z$
	- Typical values: $0.2-0.5$

## Elastic behaviour
### Moduli of materials
- Young's modulus $E$:
$$\sigma=E\epsilon$$
- Shear modulus $G$:
$$\tau=G\gamma$$
- Relation between moduli:
$$E=2G(1+\nu)$$
- Some materials: anisotropic, Young's modulus along different axes change
- Energy density (work done per unit volume) of materials under stress:
$$\frac{W}{V}=\frac{1}{2}E\epsilon^2$$
$$\frac{W}{V}=\frac{1}{2}G\gamma^2$$
- Atomic basis: forces between atoms approximated by Lennard-Jones potential
$$U_{LJ}=U_{min}[\left(\frac{r_0}{r}\right)^{12}-2\left(\frac{r_0}{r}\right)^6]$$
	- Small deviations from $r_0$: $F=dU/dr$ is approximately linear
	$$E=\frac{1}{r_0}\frac{d^2U}{dr^2}\Big|_{r=r_0}$$
- Composite materials: fibres ($f$) embedded in a matrix ($m$), each with volume fraction $V_i$
	- Loaded axially: equal strains, $E=E_mV_m+E_fV_f$
	- Loaded in transverse direction: equal stress assumption, $E^{-1}=V_fE_f^{-1}+V_mE_m^{-1}$
- Thermal expansion:
	- Extent of expansion depends on width of potential well
	- $\epsilon_T=\alpha\Delta T$
	- $\alpha$: coefficient of thermal expansion

### Beam deformation
- Bending of a beam: one side in tension, other side in compression
- Neutral axis: mid-height, undeformed, length $l$
- Radius of curvature: $R=l/\theta$, curvature $\kappa=1/R$
- Distance of beam mass element from neutral axis: $h$
$$\sigma_{axial}=E\epsilon_{axial}=\frac{Eh}{R}$$
- Moment on mass element $dM=hdF=h\sigma dA=h\sigma w(h) dh$
	- Width $w$ can be a function of $h$
- Total moment $M$:
$$M=\frac{E}{R}\int h^2w(h)dh=\kappa EI$$
	- $I$: second moment of area
	- $EI$: beam stiffness
- Example: cantilever of length $L$ loaded at the end with force $F$
	- Deflection at point $x=y(x)$
	- Moment as a function of $x$: $M=F(L-x)$
	- Curvature $\kappa\approx d\theta/dx\approx d^2y/dx^2$
	- Boundary conditions: $y(0)=y'(0)=0$
	- Solving the equation for $y$: $y=Fx^2(3L-x)/(6EI)$
	- Maximum deflection: end of beam, $x=L$
