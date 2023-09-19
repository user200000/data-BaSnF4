This subdirectory handles site- and density-based analysis. It contains three Jupyter notebooks:

- `Density Calculation.ipynb` - This calculates the three-dimensional density using [`revelsMD`](https://github.com/user200000/revelsmd).
- `BaSnF4_F_density.ipynb` - This creates Figure 6 from the cube file created in Density Calculation.ipynb
- `Site_based_analyis` - This notebook is larger than the other theoretical contributions to the data set and handles all site based anaylysis. It plots Figs. 7, 9 and 12 and generates the related occupancy tables presented in the SI.

The trajectories are stored in the trajectories folder included in the full version of this dataset, available from the University of Bath Research Data Archive.
Each run is stored in a number `r` subdirectory and contains the following files:

- `OUTCAR`
- `POSCAR` (starting structure)
- `CONTCAR` (final structure)
- `vasprun.xml`
- `INCAR`
- `XDATCAR`
