# Data analysis for &ldquo;Dynamic Lone Pairs and Fluoride-Ion Disorder in Cubic-BaSnF<sub>4</sub>&rdquo;


Authors:
- Bris&eacute;&iuml;s Mercadier
- Samuel W. Coles (Wrote workflow)
- Mathieu Duttine
- Christophe Legein
- Monique Body 
- Olaf J. Borkiewicz
- Oleg Lebedev
- Benjamin J. Morgan
- Christian Masquelier
- Damien Dambournet

## Summary
This repository contains the analysis workflow for our preprint &ldquo;Dynamic Lone Pairs and Fluoride-Ion Disorder in Cubic-BaSnF<sub>4</sub>&rdquo; now availible on Arxiv.

The workflow here contains two main components: polarisation, sites, and quenching which cover all the analysis of molecular dynamics simulations presented in the main paper. Each section consits of one or two annotated jupyter notebooks which show how all the simulations in the main paper were generated from raw simulation data.

The full simulation data and experimental data will be provided in a data repositiory at time of publication in a peer reviewed journal. Further infromation on this workflow can provided on reasonable request.

## Polarisation
The notebooks in Polarisation take as input a list of atomic dipoles calculted using wannier90 from snapshots taken from the length of an aimd simulation. From these dipoles it calculates the dipole autocorellation function (in Autocorrelation.ipynb), dipole orientated spatial distribution function, and orientation populations matrix (in Dipole Correlation.ipynb).

## Sites
The notebooks in sites take as input the XDATCAR and vasprun trajectory files taken from the aimd simulations. The first book sites.ipynb uses the site analysis library to generate figures 7 and 9 in the main paper. The Density.ipynb notebook uses the revelsMD code to calculate the ion densities presented in figure 6.

## Quenching
The notebook in quenching takes POSCARS from structures which were quenched and calculates the structural graphs presented in Figure 5. And also produces th
