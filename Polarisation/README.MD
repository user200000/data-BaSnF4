This directory creates the figures showing analysis of lone pair polarisation. It consists of two sub notebooks:

- `Autocorrelation.ipynb`, which calculates both autocorrelation functions presented in Fig 11.
- `Dipole correlation.ipynb`, which calculates structural information about the dipole. This notebook plots Fig. 10 and generates the ASCII file `hexamin_loc`, which is used by the notebook `Sites/Site_based_analysis.ipynb`.

The complete version of this dataset, available from the University of Bath Research Data Archive, contains two additional subdirectories:
- `dipoles`
- `static_dipoles`
Within each of these directories are sub directories containing the results and inputs for wannierisation.

Each subdirectory contains:

- `dipoles.out`: The final list of molecular dipoles used to calculate autocorrelation functions
- `wannier90.eig`: Final wannier eigenfucntion output
- `wannier90.wout`: Output of final wannierisation run for this structure
- `wannier2dipoles_new.py`: The Python script used to convert centres to dipoles
- `wannier90.win`: Input file for wannier90 for this structure
- `wannier90_centres.xyz`: Locations of Wannier centres in `xyz` format
- `POSCAR `: The structure that was wannierised in `POSCAR` format

Due to the large number of wannierisations which had to be performed and the large amount of data produced, files other than these could not be retained.
