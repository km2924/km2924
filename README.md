  Density Functional Theory, Geometry Optimization, Potential Energy Surface of H2O and H2O2
  This document will be used to provide information on calculations ran, results, and measurments of bond angles/lengths from the          calculations ran



Single Point Energy Caluclations (CP2K)
H2O molecule
Time- H2O energy: 11.669 seconds
--After plotting the total energy of the H2O molecule using CP2K, the graph has an exponential decay and remains stable at the eleventh step, reaching its lowest energy point at the last step, 41. 

H2O2 molecule
Time- H2O2 energy: 17.741 seconds
--




Geometry Optimization (CP2K)
H2O molecule
Time- H2O geom opt: 41.388 seconds
-The geometry optimization calculation was 29.719 seconds longer than the single-point energy calculation
--Plotting the total energy and interpreting the graph, the energy declined dramatically between the first and third optimization step. Around the fifth optimization step, the energy seems to maintain a stable value as the graph appears linear. Comparing the single-point calculation’s energy value (-17.180920022061073) to the Geometry optimization final energy value (-17.205049188439723), the final energy is lower than the energy computed in the single point calculation’s energy value. 

H2O2 molecule
Time- H2O2 geom opt: 118.742 seconds
-The geometry optimization calculation took 101.001 seconds longer than the single-point energy calculation 
--Observing the graph plotted of the total energy, the energy gradually reduces approaching the second optimization step. Between the second and fourth optimization step, the energy appears to have a small peak. The energy then begins to decrease towards the fourth optimization step, and eventually remains stable at the seventh optimization step reaching the local minima of -33.1251478989. 




Visualization (Avogadro)
H2O molecule
bond lengths/angles BEFORE geometry optimization:
_O-H bond length- 0.970 Angstroms 
_HOH angle- 109.5 degrees
bond lengthss angles AFTER geometry optimization:
_O-H bond length- 0.980631 Angstroms
_HOH angle- 109.471 degrees

H2O2 molecule
bond lengths/angles Before geometry optimization:
_O-H bond length- 0.970 Angstroms
_O-O bond length- 1.375 Angstroms
_H-H bond length- 2.727 Angstroms
_dihedral angle- -180.0 degrees
bond lengths/angles AFTER geometry optimization:
_O-H bond length- 0.985 Angstroms
_O-O bond length- 1.488 Angstroms 
_H-H bond length- 2.622 Angstroms
_dihedral angle- -179.333 degrees




Difference between the CP2K input files for the geometry optimization and Single-point Energy Calculation
<  RUN_TYPE ENERGY 
---
>  RUN_TYPE GEO_OPT 
5c5
<  WALLTIME 00:15:00
---
>  WALLTIME 00:25:00
6a7,12
> &MOTION
>  &GEO_OPT
>   OPTIMIZER BFGS #CG
>   MAX_ITER 40
>  &END GEO_OPT
> &END MOTION
11c17
<   POTENTIAL_FILE_NAME ./POTENTIAL
---
>   POTENTIAL_FILE_NAME ./POTENTIAL 
58,60c64,66
< O         -2.77888        1.76816        0.00000
< H         -1.80888        1.76816        0.00000
< H         -3.20855        2.45255        0.83837
---
> O         -1.22146        2.10626        0.00000
> H         -0.25146        2.10626        0.00000
> H         -1.54479        2.59417        0.77350


  
