# Data analysis for &ldquo;Dynamic Lone Pairs and Fluoride-Ion Disorder in Cubic-BaSnF<sub>4</sub>&rdquo;


Authors:
- Bris&eacute;&iuml;s Mercadier (orcid: [0000-0003-2176-8820](https://orcid.org/0000-0003-2176-8820))
- Samuel W. Coles (Wrote workflow) (orcid: [0000-0001-9722-5676](https://orcid.org/0000-0001-9722-5676)) 
- Mathieu Duttine (orcid: [0000-0002-6120-8716](https://orcid.org/0000-0002-6120-8716))
- Christophe Legein (orcid: [0000-0001-7426-8817](https://orcid.org/0000-0001-7426-8817))
- Monique Body (orcid: [0000-0002-5895-3731](https://orcid.org/0000-0002-5895-3731))
- Olaf J. Borkiewicz (orcid: [0000-0003-2370-3393](https://orcid.org/0000-0003-2370-3393))
- Oleg Lebedev
- Benjamin J. Morgan (orcid: [0000-0002-3056-8233](https://orcid.org/0000-0002-3056-8233))
- Christian Masquelier (orcid: [0000-0001-7289-1015](https://orcid.org/0000-0001-7289-1015))
- Damien Dambournet (orcid: [0000-0003-3831-2643](https://orcid.org/0000-0003-3831-2643))

## Summary
This repository contains the analysis and figure-plotting workflow for the manuscript &ldquo;Dynamic Lone Pairs and Fluoride-Ion Disorder in Cubic-BaSnF<sub>4</sub>&rdquo; ([chemRXiv](https://doi.org/10.26434/chemrxiv-2023-m4014-v2)).

The theoretical workflow here contains four main components: `Volume`, `Polarisation`, `Sites`, and `Quenching`, which cover all the analysis of molecular dynamics simulations presented in the main paper as well as the preparatory calculations peformed in order to obtain an appropriate cell volume. Each section consits of one to three annotated Jupyter notebooks that show how the computational analysis in the paper were generated from raw simulation data.

Rerunning this workflow requires the input AIMD trajectory files, which are not included in this repository due to a lack of space. A fully functional version is provided on the Bath University research Archive [awaiting DOI].

A fifth sub-directory (`Experimental`) contains the numerical data plotted in the paper. This data is provided in the form of Excel files, and an index is provided in that section's `README.MD` file.

## Polarisation
The notebooks in `Polarisation` take as input a list of atomic dipoles calculated using wannier90 from snapshots taken from the length of an AIMD simulation. From these dipoles, we calculate the dipole autocorrelation function (in `Autocorrelation.ipynb`), dipole-orientated spatial distribution function, and orientation populations matrix (in `Dipole Correlation.ipynb`).

## Sites
The notebooks in `Sites` take as input the `XDATCAR` and `vasprun.xml` trajectory files taken from the AIMD simulations. The first notebook, `sites.ipynb`, uses the [`site-analysis`](https://github.com/bjmorgan/site-analysis) library to generate figures 7 and 9 in the main paper. The `Density.ipynb` notebook uses the [`revelsMD`](https://github.com/user200000/revelsmd) code to calculate the ion densities presented in figure 6,  which are plotted in `BaSnF4_F_density.ipynb`.

## Quenching
The notebook in `Quenching` takes `POSCAR` files from structures that have been quenched and calculates the structural graphs presented in Figure 5. This notebook also produces the two panels of Fig S4. The quenches taken from the conventional AIMD are analysed in `Structural Characterisation.ipynb` and the AIMD with static fluorine ions in `Stuctural Characterisation Static.ipynb`.

## Volume

This notebook shows the method of fitting the Birch&ndash;Murnaghan equation of state to 600&nbsp;K AIMD simulations of cells of different size. This method is used to get an appropriate volume for the simulated cell, and is shown in `Volume Calculation.ipynb`.

## Experimental

This directory contains excel workbooks of numerical data plotted in the experimental figures in the paper.

## Files in this directory

This directory contains two further files:
- `POTCAR_list` contains a list of the pseudopotentials used for BaSnF<sub>4</sub> in `VASP`.
- `environment.yml` describes the Python environment used for all subsequent analysis.
