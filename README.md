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
This repository contains the analysis workflow for our preprint &ldquo;Dynamic Lone Pairs and Fluoride-Ion Disorder in Cubic-BaSnF<sub>4</sub> &rdquo; [which is availible on chemRXiv](https://s3.eu-west-1.amazonaws.com/assets.prod.orp.cambridge.org/0a/aa6285dade45ffa977031e4ff7f1cc.pdf?AWSAccessKeyId=ASIA5XANBN3JD2TC4RMI&Expires=1693823175&Signature=Th62XnPK%2FIh8Pnqfy6rIQRr4PJs%3D&response-cache-control=no-store&response-content-disposition=inline%3B%20filename%20%3D%22dynamic-lone-pairs-and-fluoride-ion-disorder-in-cubic-ba-sn-f4.pdf%22&response-content-type=application%2Fpdf&x-amz-security-token=FwoGZXIvYXdzEHwaDCh2Qcc5wa3mgjX50iKtASoxVvDXN4qAI5PxDYkVksl%2BaOHO02wMdOIvpTRnOiJXxf%2BwUE3eMUnDLYXU%2BxopT%2BX%2FN3Aq5bZky59Dk1xbUtLMRPqvpaH1bViTpsSANewrG1Xyu1O4dy5uOxcntgjnJknIPiEH081l%2FY1rJF9Yq%2BQc9B3CyTb03S9wBnJN5hZvHo6TdS5n8dqUPqv2GsaFhhHDC3V2ZCQma%2BKOKGA5tGUQh066fXvS3TDBexqQKJPf1qcGMi3qXoenN6XleM1Ob8xaBTFpfx8FjUKojIucRa18RQvRbpQ6JiEP0eANZktl2Ag%3D).

The theoretical workflow here contains three main components: polarisation, sites, and quenching which cover all the analysis of molecular dynamics simulations presented in the main paper. Each section consits of one to three annotated jupyter notebooks which show how all the simulations in the main paper were generated from raw simulation data.

This workflow is non operational due to the lack of trajectory files. A fully functional version is provided on the Bath University research Archive.

A fourth sub directory (Experimental) contains the numerical data plotted in the paper. This data is provided in the form of excel files, an index is provided in that section's README.MD file.

## Polarisation
The notebooks in Polarisation take as input a list of atomic dipoles calculted using wannier90 from snapshots taken from the length of an aimd simulation. From these dipoles it calculates the dipole autocorellation function (in Autocorrelation.ipynb), dipole orientated spatial distribution function, and orientation populations matrix (in Dipole Correlation.ipynb).

## Sites
The notebooks in sites take as input the XDATCAR and vasprun trajectory files taken from the aimd simulations. The first book sites.ipynb uses the site analysis library to generate figures 7 and 9 in the main paper. The Density.ipynb notebook uses the revelsMD code to calculate the ion densities presented in figure 6.

## Quenching
The notebook in quenching takes POSCARS from structures which were quenched and calculates the structural graphs presented in Figure 5. And also produces th
