AQIR-ADS

Adaptive Quantum Image Representation with Adaptive Depth Suppression

This repository contains the simulation code, analytically constructed quantum circuits, and experimental results associated with the research work:

AQIR-ADS: A Noise-Aware Adaptive Quantum Image Representation with Reduced Circuit Complexity

All quantum image representations and circuits in this repository are theoretical and simulation-based.
No experiments are performed on physical quantum hardware.

Repository Structure
AQIR-ADS/
│
├── input_datasets/
│   ├── braintumor/
│   ├── mrifnl/
│   └── sar/
│
├── notebooks/
│   ├── aqir_ads_main.ipynb
│   │
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
│   │
│   ├── results/
│   │   ├── *.pdf
│   │   └── *.png
│   │
│   ├── figures/
│   │
│   ├── Table1_Average_Performance.csv
│   ├── Table2_Qualitative_Factors.csv
│   └── Table_Ablation_AQIR_ADS.csv
│
└── README.md

Note:
All generated outputs—including tables, figures, and circuit diagrams—are
intentionally stored under notebooks/ to keep execution, results, and
analysis tightly coupled for reproducibility and reviewer verification.

notebooks/
aqir_ads_main.ipynb

This is the main and only executable notebook used in this work.

It implements the complete simulation pipeline for quantum image
representation and evaluation, including:

Loading and preprocessing grayscale images

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

Noise-aware image reconstruction under NISQ-like assumptions

Quantitative evaluation metrics:

PSNR

SSIM

Gate fidelity

Information loss

Composite performance indicators:

Reconstruction Quality Score (RQS)

Quantum Resource Efficiency (QRE)

Ablation studies for AQIR-ADS variants

Generation of Springer-ready figures, tables, and circuit visualizations

All computations are carried out using classical simulation.
Quantum circuits are constructed analytically and evaluated using theoretical noise models.

notebooks/circuits/

This directory contains theoretical quantum circuit diagrams for all evaluated
quantum image representation techniques, including AQIR-ADS.

Circuits are generated using Qiskit for visualization purposes only

Provided in vector PDF format

Circuits represent analytical constructions, not hardware-executable layouts

No circuit in this repository is executed on real quantum hardware.

notebooks/results/

This directory contains all final experimental figures, including:

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

Visual reconstruction comparisons for MRI and SAR images

All figures are generated at publication-quality resolution (300–600 DPI) and
correspond directly to results reported in the manuscript.

Tables (CSV)

All quantitative result tables are stored directly in the notebooks/ directory:

Table1_Average_Performance.csv
Average PSNR, SSIM, qubit count, gate count, circuit depth, encoding time, and fidelity per QIR technique.

Table2_Qualitative_Factors.csv
Composite qualitative metrics:

Reconstruction Quality Score (RQS)

Quantum Resource Efficiency (QRE)

Table_Ablation_AQIR_ADS.csv
Ablation study results evaluating the impact of gradient weighting, rotation strategy, and circuit depth on AQIR-ADS performance.

Input Datasets

The input_datasets/ directory contains the datasets used for simulation:

input_datasets/
├── braintumor/
├── mrifnl/
└── sar/

Public Dataset Sources

Brain Tumor Dataset (Figshare)
https://figshare.com/articles/dataset/brain_tumor_dataset/1512427

MRI-FNL Dataset (McGill / MNI)
http://nist.mni.mcgill.ca/?page_id=672

Synthetic Aperture Radar (SAR) Dataset (ICEYE)
https://www.iceye.com/resources/datasets

For experimental feasibility and consistency, only a subset of images (up to 200 per dataset) is used during simulation, as described in the manuscript.

Simulation and Reproducibility Notes

All results are obtained via classical simulation

Circuit depth, gate count, and noise effects are analytically modeled

Noise is injected using depth-dependent stochastic perturbations

No physical quantum processor is used

No claims are made regarding hardware-level execution

This repository is provided to support reproducibility, transparency, and
reviewer verification of the reported results.
