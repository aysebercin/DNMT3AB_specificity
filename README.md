# So close yet so far apart: Distinct flanking sequence recognition by DNMT3A and DNMT3B

The preprint describing our work: [![DOI:10.1101/2024.02.07.579311](http://img.shields.io/badge/DOI-10.1101/2024.02.07.579311-B31B1B.svg)](https://www.biorxiv.org/content/10.1101/2024.02.07.579311v3)

In mammals, de novo DNA methylation is essential to embryonic development, reprogramming, and gene regulation. The de novo DNA methylation is directed by DNMT3A and DNMT3B enzymes and mainly exerted on CpG islands. Over their enzymatic domains, DNMT3A/B proteins share over 90% of sequence similarity. Even so, DNMT3A predominantly methylates the first cytosine in the CGC and CGT motifs, while DNMT3B prefers the CGG and CGA sequences. To elucidate the mechanistic basis of these selective methylation profiles, we performed extensive molecular dynamics simulations of DNMT3A/B enzymes bound to all possible CGX[C/G/T/A] motifs. For each complex, we performed 2 µs long molecular dynamics (MD) simulations under AMBER parmbsc1 force-field. 

To systematically quantify protein–DNA interactions across different sequence contexts and elucidate sequence-specific recognition mechanisms of DNMT3 enzymes, we developed the Comparative Dynamics Analysis (CDA) framework. CDA integrates base and shape readout analyses into a structured pipeline, enabling parallel evaluation of direct (base-specific) and indirect (shape-dependent) recognition features. This framework was specifically designed to capture dynamic and sequence-dependent recognition features that are not accessible from static structures alone **(Figure 1)**.

![Figure3](https://github.com/user-attachments/assets/d0b51d46-9445-47b6-9a02-6b63e99f14c6)

**Figure 1:** The Comparative Dynamics Analysis (CDA) framework designed to identify DNMT3 base and shape readout rule sets. (A) Base readout. This module quantifies specific hydrogen bond interactions between DNA bases and protein side chains. Step 1: Interaction analysis is performed to detect base-specific hydrogen bonds. The schematic depicts the base-specific hydrogen bonds between DNA base atoms and residue side chain atoms. A heatmap summarizes the average hydrogen bonding intensity between residues and DNA flanking nucleotides at positions +1 to +3. Step 2: The frequency of individual atom-atom hydrogen bonds is visualized through bar plots, representing cumulative interactions over the simulation trajectory. (B) Shape readout. This module captures DNA backbone deformation and associated electrostatic forces, especially at the minor groove where shape recognition is most pronounced. Step 1: DNA deformation is quantified using phosphate root-mean-square deviation (P-RMSD) values relative to ideal B-DNA, representing dynamic shape changes. Step 2: These deformations are correlated with electrostatic distributions at the protein–DNA interface, highlighting sequence-dependent complementarity. Step 3: A pairwise interaction matrix maps residue interactions with upstream DNA flanking nucleotides (–1 to –3) based on base-specific hydrogen bonds and hydrophobic contact intensity.

## Repository Structure

The repository is organized into the following main folders:

***1.	Analysis_scripts:*** This folder contains three subfolders:
-	***CDA_base:*** includes analysis scripts and input datas of Comparative Dynamic Analysis in the order **(i)** residue level flanking nucleotide - amino acid interaction interaction intensity analysis and **(ii)** atom level cumulative h-bond analysis. Jupyter notebooks in each folder can be used directly.
- ***CDA_shape:*** includes analysis scripts and input datas of Comparative Dynamic Analysis in the order **(i)** DNA deformation analysis, **(ii)** electrostatic interaction energy correlation analysis and **(iii)** residue level upstream flanking nucleotide - amino acid interaction intensity analysis. Jupyter notebooks in each folder can be used directly.
-	***supplementary_analysis:*** includes supplementary analysis scripts and input datas as **(i)** DNA minor groove width analysis, **(ii)** cumulative ionic interaction analysis, and **(iii)** cumulative atom-atom interactions of each replica simulations. Jupyter notebooks in each folder can be used directly.

***2.	Gromacs_parameter_files:*** includes .mdp files that defines simulation parameters for each energy minimization step and production run of our MD simulations.

***3. Movies:*** includes movies of MD simulation trajectories of DNMT3A-CGC (cognate) and DNMT3B-CGG (cognate) complexes.
 	
***4.	Starting_structures:*** includes the initial structures of our DNMT3A/B – CGC/G/T/A complexes for MD simulations.

Our MD conformers are deposited at [![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.12545441.svg)](https://doi.org/10.5281/zenodo.12545441)

### ***Important Note:***
At the beginning of the study, we started residue numbering from 1 to allow for direct sequence-based comparison between DNMT3A and DNMT3B constructs. For clarity and consistency with external references, we later adjusted the numbering to match UniProt annotations by adding 629 for DNMT3A and 570 for DNMT3B, and we use these UniProt-based residue numbers throughout the manuscript.

## Contact

If you have any questions related to our repository, please contact us:

- Ayşe Berçin Barlas: aysebercin.barlas@ibg.edu.tr
- Ezgi Karaca: ezgi.karaca@ibg.edu.tr


