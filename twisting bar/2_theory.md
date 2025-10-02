# Design Basis Report: Phase-Field Simulation of a Torsion Test on a Soda-Lime Glass Tube

## Abstract

This report provides a comprehensive Design Basis Report (DBR) for the numerical simulation of a torsion test on a thin-walled soda-lime glass tube. The objective is to replicate the fracture behavior using a phase-field model. The report outlines the specimen’s geometry, the material properties of soda-lime glass, boundary and loading conditions, and the governing equations for stress and strain. Additionally, it specifies the solver parameters, meshing strategy, fracture model parameters, and the expected outputs for both 2D and 3D plots. The tube has an initial length of 5 mm, an inner radius of 2.85 mm, and an outer radius of 3 mm. The simulation aims to predict the stress-strain response and the crack nucleation pattern, with results benchmarked against provided reference data. Keywords: Torsion Test, Soda-Lime Glass, Phase-Field Model, Fracture Mechanics, Finite Element Analysis, Thin-Walled Tube

1.  Objective
		The primary objective of this report is to provide a clear and comprehensive framework for simulating a torsion test on a thin-walled soda-lime glass tube. It details all the nec- essary parameters needed to accurately replicate the simu- lation, which aims to predict the stress-strain response and fracture behavior of the tube using a phase-field modeling approach.
2. Geometry and Dimensions
		The test specimen is a thin-walled circular tube. The ge- ometric parameters are specified in Table 1 and visualized in Figure 1 ![cylinder1]().![[cylinder 1.png]]   
   
		
		
		The wall thickness is t = B − A = 0.15 mm.


		| Parameters | Symbol  | Value | Units |
        | -------- | -------- | -------- | -------- |
		| Initial Length| L   | 5.00     | mm       |
		| Inner Radius   | A     | 2.85     | mm     |
		| uter Radius    | B     | 3.00     | mm     |
		


3.  Material Properties: Soda-Lime Glass 

	The tube is fabricated from soda-lime glass. The me- chanical properties used for the linear elastic and fracture simulation are detailed in Table 2. The Shear Modulus (G) is derived from Young’s Modulus (E) and Poisson’s Ratio (ν) via the relation G = E/(2(1 + ν)).
	

		| Property | Symbol |Value  | Units |
		| -------- | -------- | -------- | -------- |
		| Young’s Modulus   | E    | 70    | GPa     |
		| Poisson’s Ratio     | ν      | 0.22     | GPa     |
		| Shear Modulus     | G    | 28.69    | MPa    |
		| Shear Strength  | Sss     | 58     | GPa     |


4.  Boundary and Loading Conditions

	* Fixed End: One end of the tube is fully constrained, preventing all translations and rotations. 
	*  Twisted End: The opposite end is subjected to a prescribed small angle of twist, α, around the tube’s central axis (z-axis). This loading induces a state of nearly uniform shear stress throughout the thin wall.

5.  Formulation and Governing Equations

	Due to the tube’s thin wall, the stress and strain are considered approximately uniform.


