# C-13 NMR
## Chemical shifts
- Scale: 0-200 ppm
Chemical shift/ppm | Carbon environment 
------------ | -----------
0-50 | sp$^3$
50-100 | sp$^3$ bonded to oxygen or fluorine atoms/sp
100-150 | sp$^2$
150-200 | sp$^2$ with very electron withdrawing groups
- When proton decoupled, quaternary carbons (C with no protons attached) have particularly weak signal
### Specific environments
Ketone: $\delta\approx 206$ ppm
End of double bond conjugated with ketone: $\delta\approx 140$ ppm
Aldehyde: $\delta\approx 195$ ppm
Acid derivatives: $\delta\approx 160-170$ ppm

## Coupling
- Signal spltting is seen when there is an atom with non-zero spin is nearby
	- Total number of signal lines$=2nI+1$ ($n=$number of equivaent nuclei, $I$=nuclear spin)
	- For C-13 NMR, only coupling to atoms with spin=1/2 is seen due to rapid interconversion of atoms with spin>1/2
- In C-13 NMR, coupling will not be through more than 1-2 bonds
- Unseen splitting:
	-  C-H coupling is not seen unless proton coupled
	- C-C coupling is not seen due to low relative abundance (unless enriched)
	- No splitting from equivalent nuclei
- Coupling constant $^xJ_{\ce{Y-Z}}$ is measured in Hz instead of ppm
	- $x$ = number of bonds, Y and Z are coupled atoms
- For coupling to more than one nucleus, order of splitting does not matter
- Splitting pattern and intensities: tree diagram, Pascal's triangle
- Satellites: from elements with isotopes that have non-zero spin (e.g. $^{15}N$)
	- Doublet superimposed over singlet, intensity proportional to abundance
- Spectrum can be proton coupled for more information, but with significant noise
- APT NMR: signals attached to even number of protons is on one side, signals attached to odd numbers are on the other

# Proton NMR
- Area under peaks proportional to number of protons
- Intensities of split signals may be affected by roofing
## Chemical shifts of protons connected to carbon
- Scale: 0-14ppm
Environment (underlined proton) | Chemical shift/ppm
------- | -----------
Terminal $\ce{-C\underline{H}_3}$ | 1-1.5
 $\ce{-C\underline{H}_2-}$ | 1.5-2.5
  $\ce{=CH-C\underline{H}_2 -}$ | 2.5-3.5
 $\ce{-CO-C\underline{H}_2 -}$ | 2-3.5
 $\ce{Ph-C\underline{H}_2}$ | 2.5-3
 $\ce{-NR-C\underline{H}_2 -}$| 2-2.5
  $\ce{-CO-NR-C\underline{H}_2 -}$ | 3-3.5
  $\ce{-O-C\underline{H}_2 -}$ | 3.5-4
  $\ce{-CO-O-C\underline{H}_2}$ | 4-4.5
  $\ce{Cl-C\underline{H}_2 -}$ | 3.5-4
  $\ce{-C#C\underline{H}}$ | 2-2.5
  $\ce{-C=CR-\underline{H}}$ | 4.5-6
  $\ce{Ph-\underline{H}}$ | 6-9
 $\ce{-O-CO-H}$ | 8
 $\ce{-CH2-CO-H}$ | 9.5-10.5
- Shifts of proton in methyl groups: 0.5ppm less than alkyl protons
- Protons on carbons connected to double bonds: around 2.5ppm
- Three-membered rings: unusually low, around 0.5ppm
- Protons on carbons bonded to $\ce{O}$: 1ppm greater than those on carbons bonded to $\ce{N}$
- Conjugation of $\ce{O}$ or $\ce{N}$ with carbonyls: further increases shift by $\approx 1$
- Shift of aldehyde proton > shift of formate ester proton
- Aromatic rings and terminal alkynes: higher/lower than expected due to ring currents generating magnetic field

## Signals of protons connected to O and N
- Hydrogen bonding leads to large range of chemical shifts
- Leads to very broad signal
- A $\ce{D2O}$ shake leads to $\ce{H-D}$ exchange, removes signal
- No coupling is seen due to rapid swapping, except when solvent is extremely dry
      
## Coupling
- Coupling can be seen over 3-4 bonds 
	- As it is a through-bond effect, the bond angle significantly affects $J$
 Coupling environment | Coupling constant 
 ---------- | ---------------
Over 3 freely rotating bonds (vicinal) | $^3J_{Ha-Hb}\approx 7$Hz
2 protons attached to an sp$^2$ carbon | $^2J_{Ha-Hb}\approx0-3$ Hz
2 protons on the cis-side of a double bond | $^3J_{Ha-Hb, cis}\approx 8$Hz ($0<\,^3J<12$)
2 protons on different sides of a double bond | $^3J_{Ha-Hb, trans}\approx 15$Hz ($12<\,^3J<18$)
2 protons attached to an sp$^3$ carbon (geminal) | $^2J_{Ha-Hb}\approx 13$Hz ($8<\,^3J<18$)
- Coupling to atoms with spin>1/2:
	- Some atoms relax slow enough for coupling to be seen
	- Number of lines$=2nI+1$, $n=$ number of nuclei, $I=$nuclear spin
	- Deuterium: $I=1$, one $D$ atom leads to 3 equal split signals
	- Intensities obtained via tree diagram/modified Pascal's triangle
	- Chlorine: relaxes too quickly



# IR spectroscopy
- Wavenumber of absorbed IR wave is correlated to bond oscillation angular frequency
- Oscillation of more complex molecules can be broken down into normal modes with different frequencies
IR wavenumber region | Bond 
-------- | ---------
500-1500 cm$^{-1}$ (fingerprint) | X-Y single bonds, non-stretching modes
1500-2000 cm$^{-1}$ | Double bonds
2000-2500 cm$^{-1}$ | Triple bonds
2500-4000 cm$^{-1}$ | X-H single bonds
- Strength of absorption depends on dipole moment of molecule
	- Non-dipoles are too weak for IR, and require Raman spectroscopy
## X-H region
Group | Wavenumber | Note
------ | -------- | --------
Tetrahedral $\ce{C-H}$ | 2900-3000 cm$^{-1}$ | Sharp
Trigonal $\ce{C-H}$ | 3000-3200 cm$^{-1}$ | Sharp
 $\ce{R-C#C-H}$ | 3300 cm$^{-1}$ | Strong, sharp
 $\ce{N-H}$ | 3300 cm $^{-1}$ | Sharp
 $\ce{NH2}$ symmetric| 3300 cm$^{-1}$  | Strong, sharp
 $\ce{NH2}$ anti-symmetric | 3400 cm$^{-1}$ | Strong, sharp
 $\ce{RO-H}$, H-bonding present |2900-3500 cm$^{-1}$ | Broad and U-shaped 
 $\ce{O-H}$, no H-bonding | 3500-3600 cm$^{-1}$ | Sharp
 $\ce{RCOO-H}$ | 2500-3500 cm$^{-1}$ | Very broad 

## Triple bond region
Group | Wavenumber | Note
---- | ------- | -----
 $\ce{RC#N}$ | 2250 cm$^{-1}$ | Strong
 $\ce{C#C}$ | 2100-2250cm$^{-1}$ | Weak
## Double bond region
Group | Wavenumber | Note
----- | -------- | -----
 $\ce{C=C}$ | 1635-1690cm$^{-1}$ | Weak
 Benzene ring | 1450-1625cm$^{-1}$ | Two or three sharp absorptions
 $\ce{-NO2}$ symmetric | 1350cm$^{-1}$ | Sharp
 $\ce{-NO2}$ antisymmetric | 1530cm$^{-1}$ | Sharp
 

## Carbonyls
- Starting reference: Ketone, 1715cm$^{-1}$
- Increase: electron-withdrawing groups (density towards $\ce{C=O}$ bond)
- Decrease: electron-donating groups
Group | Wavenumber
---- | -----
Ketone | 1715cm$^{-1}$
Aldehyde | 1730cm$^{-1}$
Acid chloride | 1750-1820cm$^{-1}$
Amide | 1640-1690cm$^{-1}$
Carboxylic acid | 1730cm$^{-1}$
Ester | 1745cm$^{-1}$
Acid anhydride symmetric | 1820cm$^{-1}$
Acid anhydride antisymmetric | 1750cm$^{-1}$
- Conjugation: lowers by 20-30cm$^{-1}$
- 6-member to 5-member ring: increases by 30cm$^{-1}$
- 5-member to 4-member/4 to 3: increases by 35cm$^{-1}$
	- Resistance from compression of ring during stretching



