This directory creates the figures plotted which present lone pair polarisation it consists of two sub notebooks:
- Autocorrelation which calculates both autocorrelation functions presented in Fig 11.
- Dipole correlation which calculates structural information about the dipole, it both plots Fig. 10 and generates the ASCII file hexamin_loc which is used by the notebook `Sites/Site_based_analysis.ipynb`.

In the bath archive version of this dataset this directory contains two subdirectories:
- dipoles
- static_dipoles
Within each of these directories are sub directories containing the results and inputs for wannierisation

Each subdirectory contains:
- dipoles.out	: The final list of molecular dipoles used to calculate autocorrelation functions
- wannier90.eig	: Final wannier eigenfucntion output
- wannier90.wout : Output of final wannierisation run for this structure
- wannier2dipoles_new.py: The python script used to convert centres to dipoles
- wannier90.win	: Input file for wannier90 for this structure
- wannier90_centres.xyz : Locations of wannier centres in xyz format
- POSCAR : The structure that was wannierised in POSCAR format

Due to the large number of wannierisations which had to be performed and the large amount of data produced files other than these could not be retained.
