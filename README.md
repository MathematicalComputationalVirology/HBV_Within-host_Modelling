# HBV_Within-host_Modelling

HBV_Intercellular_Model.f90 is a Fortran code that is used for the simulation of the age-structured intrecellular HBV infection, corresponding to
the paper submitted to Scientific Reports. This model uses dde_solver_m.f90 algorithm (see http://www.radford.edu/~thompson/ffddes/index.html for more detail).
The code is written in Fortran 90 and can be compiled using gfortran. The -O4 flag should be used to optimise the executable output.
This code as currently configured the treatment-free control case. The results are written to the file "HBVIntercellularModel.dat"

On a desktop computer (~2Ghz processor) the code should take around 3mins to run and uses <1Gb of RAM.

Data_fitting_asa047.f90 uses Nelder-Mead algorithm (see "R ONeill, Algorithm AS 47: Function Minimization Using a Simplex Procedure, Applied Statistics,
Volume 20, Number 3, 1971, pages 338-345" for more detail) to fit the intercellular model to patient data.
