# AQIR-ADS  
Adaptive Quantum Image Representation with Adaptive Depth Suppression

This repository contains the simulation code, analytical circuit constructions,
and experimental results for the research work:

**AQIR-ADS: A Noise-Aware Adaptive Quantum Image Representation with Reduced Circuit Complexity**

All quantum image representations and circuits in this repository are
**theoretical and simulation-based**.  
No experiments are performed on physical quantum hardware.

---

## Repository Structure

AQIR-ADS/
- notebooks/
  - aqir_ads_main.ipynb
- results/
  - *.pdf
  - *.png
- circuits/
  - *.png
  - *.pdf
- README.md



---

## notebooks/

### aqir_ads_main.ipynb

This is the **main and only executable notebook** used in this work.

It implements the complete **simulation pipeline** for quantum image
representation and evaluation, including:

- Loading and preprocessing grayscale images
- Analytical modeling of multiple QIR techniques:
  - FRQI  
  - EFRQI  
  - NEQR  
  - IQIR  
  - 2D-QSNA  
  - NASS  
  - GQIR  
  - QRMW  
  - MCQI  
  - QUALPI  
  - **Proposed AQIR-ADS**
- Analytical estimation of:
  - Qubit count  
  - Gate count  
  - Circuit depth
- Noise-aware image reconstruction under NISQ-like assumptions
- Evaluation metrics:
  - PSNR  
  - SSIM  
  - Gate fidelity  
  - Information loss
- Composite performance measures:
  - Reconstruction Quality Score (RQS)  
  - Quantum Resource Efficiency (QRE)
- Ablation studies for AQIR-ADS variants
- Generation of Springer-ready figures and tables (PDF and PNG)

All simulations are performed using **classical computation**.
Quantum circuits are **constructed theoretically** and **simulated using local
statevector and analytical noise models**.

---

## results/

This folder contains **all final outputs** generated from the notebook, including:

- Quantitative result tables
- Performance comparison plots (PSNR, SSIM, gate count, depth, fidelity)
- Composite metric plots (RQS, QRE)
- Springer-formatted visual comparisons (PDF and PNG)

All figures are produced at publication-quality resolution
(300–600 DPI) and correspond directly to results reported in the manuscript.

---

## circuits/

This folder contains **theoretical quantum circuit diagrams** for all evaluated
quantum image representation techniques, including AQIR-ADS.

- Circuits are generated using Qiskit for visualization purposes only
- PNG and vector PDF formats are provided
- Circuits represent **analytical constructions**, not executable hardware layouts

**No circuit in this repository is executed on real quantum hardware.**

---

## Input Datasets (Not Included)

Input datasets are **not included** in this repository due to their large size.

The notebook assumes the following local directory structure:

input_datasets/
- braintumor/
- mrifnl/
- sar/


### Public Dataset Sources

- Brain Tumor Dataset (Figshare):  
  https://figshare.com/articles/dataset/brain_tumor_dataset/1512427

- MRI-FNL Dataset (McGill / MNI):  
  http://nist.mni.mcgill.ca/?page_id=672

- Synthetic Aperture Radar (SAR) Dataset (ICEYE):  
  https://www.iceye.com/resources/datasets

For experimental consistency, only a **subset of images (up to 200 per dataset)**
is used during simulation, as described in the paper.

---

## Simulation and Reproducibility Notes

- All results are obtained via **classical simulation**
- Circuit depth, gate count, and noise effects are **analytically modeled**
- Noise is injected using depth-dependent stochastic perturbations
- No physical quantum processor is used
- No claims are made regarding hardware-level execution

This repository is provided to support **reproducibility, transparency, and
reviewer verification** of the reported results.

---
