### AQIR-ADS

### Adaptive Quantum Image Representation with Adaptive Depth Suppression

This repository contains the complete simulation code, analytically constructed
quantum circuits, and experimental results for the research work:

### AQIR-ADS: A Noise-Aware Adaptive Quantum Image Representation with Reduced Circuit Complexity

All quantum image representations and circuits provided in this repository are
purely theoretical and simulation-based.
No experiments are conducted on physical quantum hardware.
```
Repository Structure
AQIR-ADS/
├── input_datasets/
│   ├── braintumor/
│   ├── mrifnl/
│   └── sar/
├── notebooks/
│   ├── aqir_ads_main.ipynb
│   ├── circuits/
│   │   ├── FRQI_Circuit.pdf
│   │   ├── EFRQI_Circuit.pdf
│   │   ├── NEQR_Circuit.pdf
│   │   ├── IQIR_Circuit.pdf
│   │   ├── 2D-QSNA_Circuit.pdf
│   │   ├── NASS_Circuit.pdf
│   │   ├── GQIR_Circuit.pdf
│   │   ├── QRMW_Circuit.pdf
│   │   ├── MCQI_Circuit.pdf
│   │   ├── QUALPI_Circuit.pdf
│   │   └── AQIR-ADS_Circuit.pdf
│   ├── results/
│   │   ├── *.pdf
│   │   └── *.png
│   ├── Table1_Average_Performance.csv
│   ├── Table2_Qualitative_Factors.csv
│   └── Table_Ablation_AQIR_ADS.csv
└── README.md
```
### notebooks/aqir_ads_main.ipynb

This is the main and only executable notebook used in this work.

It implements the complete quantum image processing simulation pipeline,
including:

Loading and preprocessing grayscale image datasets

Analytical modeling of quantum image representation (QIR) techniques:

FRQI

EFRQI

NEQR

IQIR

2D-QSNA

NASS

GQIR

QRMW

MCQI

QUALPI

Proposed AQIR-ADS

Analytical estimation of:

Qubit count

Gate count

Circuit depth

Noise-aware image reconstruction under NISQ-like constraints

Quantitative evaluation metrics:

PSNR

SSIM

Gate fidelity

Information loss

Composite performance measures:

Reconstruction Quality Score (RQS)

Quantum Resource Efficiency (QRE)

Ablation studies for AQIR-ADS variants

Automatic generation of Springer-ready figures and tables

### All simulations are performed using classical computation.
Quantum circuits are analytically constructed and simulated using theoretical
noise models.

notebooks/circuits/

This directory contains theoretical quantum circuit diagrams for all evaluated
quantum image representation techniques.

Circuits are generated using Qiskit for visualization purposes only

Provided in vector PDF format

Circuits represent analytical constructions, not hardware-executable layouts

No circuit in this repository is executed on real quantum hardware.

### notebooks/results/

This directory contains all final experimental outputs, including:

Performance comparison plots:

Qubit count

Gate count

Circuit depth

Encoding time

Gate fidelity

PSNR

SSIM

Information loss

Composite metric plots:

Reconstruction Quality Score (RQS)

Quantum Resource Efficiency (QRE)

Visual reconstruction comparisons for MRI and SAR datasets

All figures are generated at publication-quality resolution (300–600 DPI) and
correspond directly to the results reported in the manuscript.

Tables (CSV Files)

### All quantitative result tables are stored directly in the notebooks/ directory:

Table1_Average_Performance.csv
Average performance metrics across all QIR techniques.

Table2_Qualitative_Factors.csv
Composite qualitative indicators (RQS and QRE).

Table_Ablation_AQIR_ADS.csv
Ablation study results evaluating the impact of adaptive encoding components
in AQIR-ADS.

### Input Datasets (Not Included in Repository)

### Important Note:
Due to their large storage size, the input datasets used in this study are not included in this GitHub repository. As a result, the input_datasets/ directory is not provided in the repository snapshot.

The notebook assumes the following local directory structure when executed:
```
input_datasets/
├── braintumor/
├── mrifnl/
└── sar/
```
Users who wish to reproduce the experiments should manually download the datasets from the public sources listed below and place them in the corresponding directories.

### Public Dataset Sources

Brain Tumor Dataset (Figshare)
https://figshare.com/articles/dataset/brain_tumor_dataset/1512427

MRI-FNL Dataset (McGill / MNI)
http://nist.mni.mcgill.ca/?page_id=672

Synthetic Aperture Radar (SAR) Dataset (ICEYE)
https://www.iceye.com/resources/datasets

For experimental feasibility and consistency with the manuscript, only a subset of images (up to 200 per dataset) is used during simulation.
