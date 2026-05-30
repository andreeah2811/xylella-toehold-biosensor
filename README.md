Xylella fastidiosa Toehold Switch Biosensor
A computational pipeline for the design of toehold switch biosensors targeting Xylella fastidiosa, a quarantine plant pathogen of major biosecurity concern in the UK and EU. This project applies synthetic biology design principles to develop candidate cell-free diagnostic sensors for field-deployable plant health surveillance.
Background
Xylella fastidiosa is a gram-negative, xylem-limited bacterium responsible for serious diseases in grapevine, olive, lavender, and other economically important hosts. It is listed as a priority quarantine organism under UK and EU plant health legislation and is actively monitored by Defra and APHA. Current diagnostic methods rely on laboratory-based PCR and ELISA, which are unsuitable for rapid field deployment.
This project computationally designs toehold switch RNA sensors, following the design framework established by Green et al. (2014) and applied to diagnostics by Pardee et al. (2016), targeting conserved and structurally accessible regions of Xylella fastidiosa RNA. The pipeline produces candidate switch sequences ready for experimental validation in a cell-free expression system.
Pipeline Overview

Notebook 01: Sequence retrieval and conservation analysis
Notebook 02: RNA secondary structure prediction and target site selection
Notebook 03: Toehold switch design and thermodynamic modelling

Dependencies
All dependencies are listed in environment.yml. To recreate the environment:
bashconda env create -f environment.yml
conda activate toehold-env
Tools Used

Biopython for NCBI sequence retrieval
MAFFT v7.526 for multiple sequence alignment
ViennaRNA for RNA secondary structure prediction
NUPACK for toehold switch thermodynamic modelling

References
Green, A.A., Silver, P.A., Collins, J.J. and Yin, P. (2014) Toehold switches: de-novo-designed regulators of gene expression. Cell, 159(5), pp. 925-939.
Pardee, K. et al. (2016) Rapid, low-cost detection of Zika virus using programmable biomolecular components. Cell, 165(5), pp. 1255-1266.
Minsavage, G.V. et al. (1994) Development of a polymerase chain reaction protocol for detection of Xylella fastidiosa in plant tissue. Phytopathology, 84(5), pp. 456-461.
Author
Andreea | BSc Biological Sciences, Middlesex University London

## View notebooks

GitHub sometimes struggles to render Jupyter notebooks directly. Use the 
links below for reliable rendering via nbviewer.

- [Notebook 01: Sequence retrieval and conservation analysis](https://nbviewer.org/github/andreeah2811/xylella-toehold-biosensor/blob/main/notebooks/01_sequence_retrieval.ipynb)
- [Notebook 02: Structure prediction and target site selection](https://nbviewer.org/github/andreeah2811/xylella-toehold-biosensor/blob/main/notebooks/02_structure_prediction.ipynb)
- [Notebook 03: Toehold switch design and thermodynamic evaluation](https://nbviewer.org/github/andreeah2811/xylella-toehold-biosensor/blob/main/notebooks/03_switch_design.ipynb)

## Results summary

Conservation analysis across 117 Xylella fastidiosa strains identified
eight conserved regions in the 16S rRNA gene, of which six were suitable
for toehold switch design. Cross-strain accessibility verification confirmed
three primary candidate target sites in region R4, all showing consistent
accessibility above 0.5 unpaired probability across pauca, multiplex, and
ATCC 35879 reference strains.

Three toehold switch designs were produced and evaluated. The primary
recommended design targets R4 position 236-266.

Trigger RNA:  5'-GUGAAAUGCGUAGAGAUCAGGAGGAACAUC-3'
Switch RNA:   5'-CCUGAUCUCUACGCAUUUCACGAUGUUCCUAAAAGAAGGAGATAAAAUGCUACAAGGAAACCCCTCAAGACCCGUUUGGC-3'
dG RBS-linker: -2.70 kcal/mol
dG switching:  -37.00 kcal/mol
Specificity margin vs Arabidopsis thaliana 18S: +18.80 kcal/mol
Specificity margin vs Xanthomonas campestris 16S: +12.00 kcal/mol

All three designs passed specificity screening against plant host RNA
and related bacterial RNA at margins substantially above the 5 kcal/mol
threshold.
