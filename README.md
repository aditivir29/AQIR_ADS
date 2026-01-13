# AQIR-ADS: Adaptive Quantum Image Representation with Angle-Dependent Sampling

This repository contains the complete experimental pipeline for **Quantum Image Representation (QIR)** techniques, with a focus on the proposed **AQIR-ADS** method. The framework provides a **comparative, simulation-based evaluation** of multiple classical QIR models using image reconstruction quality, quantum resource metrics, qualitative scoring, and circuit-level visualization.

The implementation is designed for **reproducible academic experimentation** and aligns with evaluation standards used in quantum image processing literature.



##  Implemented QIR Techniques

The following quantum image representation models are implemented and evaluated:

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
- **AQIR-ADS (Proposed)**

AQIR-ADS introduces **gradient-aware angle modulation** and **adaptive depth control** to improve reconstruction quality while reducing quantum resource usage.

---

## Core Contributions

- Unified simulation pipeline for **multiple QIR techniques**
- Adaptive reconstruction model (AQIR-ADS)
- Quantitative evaluation using:
  - PSNR
  - SSIM
  - Information Loss
  - Gate Fidelity
- Composite qualitative scoring:
  - Reconstruction Quality Score (RQS)
  - Quantum Resource Efficiency (QRE)
- Visual comparison across **medical (MRI, brain tumor)** and **remote sensing (SAR)** datasets
- Qiskit-based **quantum circuit visualization**

---

## Dataset Structure


Datasets are expected to be stored locally as:
dataset/
├── brain_tumor/
│ └── original/
│ ├── image1.jpg
│ ├── image2.png
│ └── ...
├── mri/
│ └── original/
│ ├── image1.mat
│ └── ...
└── sar/
└── original/
├── image1.tif
├── image2.png
└── ...

Supported formats:
- `.jpg`, `.png`, `.jpeg`
- `.tif`, `.tiff`
- `.mat` (MATLAB arrays)

---

##  Pipeline Overview

### 1. Image Loading
- Automatic grayscale conversion
- Robust `.mat` and SAR image handling
- Safe normalization and resizing

### 2. Quantum Encoding Simulation
- Each QIR technique is mapped to:
  - Qubit count
  - Gate count
  - Circuit depth
- Encoding time is measured analytically

### 3. Reconstruction Simulation
- Existing methods: noise modeled from gate count and depth
- AQIR-ADS:
  - Sobel gradient extraction
  - Gradient-weighted angle encoding
  - Adaptive depth-based noise modeling

### 4. Metric Computation
- PSNR
- SSIM (custom implementation)
- Gate fidelity (exponential depth decay)
- Information loss

### 5. Result Aggregation
- CSV output for:
  - Per-image results
  - Technique-wise averages
  - Qualitative factor tables

---

##  Generated Result Tables

### Table 1: Average Performance Metrics
Saved as:

Table1_Average_Performance.csv


Includes:
- Qubits
- Gates
- Circuit Depth
- Encoding Time
- PSNR
- SSIM
- Gate Fidelity
- Information Loss

---

### Table 2: Qualitative Factors
Saved as:


Table2_Qualitative_Factors.csv


Computed using min–max normalization:
- **Reconstruction Quality Score**
- **Quantum Resource Efficiency**

---

## Visual Comparisons

Visual reconstructions are generated for:
- Brain tumor images
- MRI images
- SAR images

Comparisons include:
- Original image
- Best existing method (2D-QSNA)
- Proposed AQIR-ADS

All visualizations are resolution-consistent with experimental settings.

---

##  Gradient-Aware Angle Mapping (AQIR-ADS)

AQIR-ADS uses:
- Sobel-based gradient magnitude
- Gradient-normalized angle range
- Angle modulation proportional to structural complexity

This mechanism preserves high-frequency regions while suppressing unnecessary noise in smooth regions.

---

##  Quantum Circuit Visualization

Quantum circuits are generated using **Qiskit** and saved as `.png` files.

Each circuit reflects:
- Actual qubit count
- Logical gate structure
- Encoding pattern per QIR technique

Output directory:


QIR_CIRCUITS/
├── FRQI_Circuit.png
├── 2D-QSNA_Circuit.png
├── AQIR-ADS_Circuit.png
└── ...


---

##  Graphical Analysis

The repository generates plots for:
- Qubit requirements
- Gate count
- Circuit depth
- Encoding time
- PSNR
- SSIM
- Gate fidelity
- Information loss
- Qualitative score comparison
- Quality vs. resource trade-off scatter plot

---

##  Dependencies

- Python ≥ 3.9
- OpenCV
- NumPy
- Pandas
- Matplotlib
- SciPy
- scikit-image
- Qiskit
- Rasterio (for SAR images)

---

##  How to Run

1. Place datasets in the required folder structure
2. Run the main pipeline script to generate CSV results
3. Run visualization scripts for:
   - Image comparisons
   - Graphs
   - Quantum circuits
4. Use generated tables directly for paper figures

---

##  Notes

- This is a **simulation-based comparative study**
- No physical quantum hardware is assumed
- All noise and fidelity models are analytical
- The framework is extensible to additional QIR methods

---

##  Intended Use

- Academic research
- Journal and conference submissions
- Quantum image representation benchmarking
- Teaching and experimentation

---

##  Author

Developed as part of a structured research study in **Quantum Image Processing**, with emphasis on **adaptive encoding and resource-aware design**.
