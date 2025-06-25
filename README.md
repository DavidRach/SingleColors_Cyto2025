# Single Colors Cyto 2025

<img src="https://github.com/DavidRach/SingleColors_Cyto2025/blob/main/SingleColorsPoster.png" >


This repository is for our '“Well, how bright does it need to be?”: Investigating the interplay of fluorescent signature and brightness in single-color unmixing controls' poster. It contains the data and R code needed to hopefully reproduce our analysis and figures, as well as the .svg files used to create the figures in Inkscape.

## Organization

The .csv files for the respective analyses are stored in the data folder, from which they can be accessed by the code. The code is contained within the Quarto Markdown (.qmd) files named after the respective figure. The .svg files can be opened with Inkscape to access the Figure assembly layout. 

## Luciernaga

Please note, you will need to install [Luciernaga](https://github.com/DavidRach/Luciernaga) to reproduce some of the Figures. The package version utilized for running of the code in this manuscript was the 0.99.4 release. 

## Raw Data

Due to size constraints, this repository only contains the processed data files derrived from our original .fcs files. The actual .fcs files are being uploaded to ImmPort (SDY3080) and will be available at the next release cycle. 

## Abstract

**“Well, how bright does it need to be?”: Investigating the interplay of fluorescent signature and brightness in single-color unmixing controls.**

David Rach1, Kirsten E. Lyke2, Cristiana Cairo3

1 Molecular Microbiology and Immunology Graduate Program, University of Maryland School of Medicine, Baltimore, USA 2 Center for Vaccine Development and Global Health, University of Maryland School of Medicine, Baltimore, USA 3 Department of Microbiology and Immunology, University of Maryland School of Medicine, Baltimore, MD, United States.

Spectral flow cytometry (SFC), with its capacity to resolve similar fluorophores and ability to rapidly acquire large number of events, enables more comprehensive phenotypic and functional analyses than conventional flow cytometry. Unmixing controls (both single-color and unstained) are critical for proper unmixing of high-dimensional panels, as their fluorescence signatures provision the reference matrix. Discrepancies between the fluorescence signatures of unmixing controls and full-stained samples add uncertainty to the unmixing calculations and can lead to loss of resolution for individual fluorophores, (particularly in large panels with broader co-expression of markers) producing batch effects.

These batch effects can affect performance, increase complexity, and impact reproducibility of unsupervised analysis methods that rely on median fluorescent intensity (MFI) for clustering, dimensionality visualization and normalization. While previous efforts at quality control have focused on factors related to instruments and/or full-stained samples, few tools exist to evaluate unmixing controls despite their critical importance. At the same time, the criteria for delineating a good unmixing control and re-using previous controls without affecting the unmixing remain loosely defined.

We therefore set out to quantitatively assess how variation in the fluorescence signature and/or brightness of controls impacts unmixing of full-stained samples. To this end, we have been working on an R package called Luciernaga, which includes a collection of tools for quality control and fluorescence signature profiling of unmixing controls. Leveraging its ability to characterize normalized fluorescence signatures for individual cells, we grouped and quantified, in every unmixing control, cells with similar signatures across 20 experiments. In the process, we identified “variant” signatures indicative of tandem degradation and non-specific binding of decoupled fluorophores associated with specific unmixing issues. We then grouped cells with shared variant signatures in each unmixing control and used them to generate a .fcs file containing a single variant signature. Keeping all unmixing controls but one constant, we swapped in a variant signature at a time, performing iterative unmixing in R with ordinary least squares. This process allowed us to characterize how variations in fluorescence signature, brightness, or both factors impact the unmixing of the full-stained sample. Our work builds on fluorescence signature, brightness, or both factors impact the unmixing of the full-stained sample.

Our work builds on the existing guidelines for good unmixing controls, while providing mechanistic explanations for each. We also highlight advantages of profiling control signatures before performing unmixing as a means to mitigate unmixing issues.
