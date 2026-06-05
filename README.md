# Single-Cell RNA Sequencing Analysis Pipeline

## Project Overview

This repository contains a complete single-cell RNA sequencing (scRNA-seq) analysis workflow developed using Python and Scanpy.

The project demonstrates essential bioinformatics skills including:

* Quality Control (QC)
* Cell and gene filtering
* Data normalization
* Dimensionality reduction
* Clustering
* Data visualization
* Biological interpretation of single-cell transcriptomic data

The analysis was performed as part of a bioinformatics coursework project and highlights reproducible computational approaches commonly used in modern genomics research.

---

## Objectives

The main objectives of this project were:

1. Perform quality control and filtering of raw scRNA-seq data.
2. Justify filtering thresholds based on data distributions.
3. Apply normalization techniques to reduce technical variability.
4. Explore cellular heterogeneity using dimensionality reduction methods.
5. Generate interpretable visualizations for downstream biological analysis.

---

## Dataset

The dataset consists of multiple patient-derived samples containing normal and disease-associated tissues.

Samples included:

* P2_normal
* P2_cSCC
* P3_normal
* P3_cSCC1
* P3_cSCC2
* P4_normal
* P4_cSCC1
* P4_cSCC2
* P5_normal
* P5_cSCC

---

## Methods

### 1. Quality Control

Quality control metrics were calculated for:

* Number of detected genes per cell
* Total UMI counts per cell
* Percentage of mitochondrial genes

Cells with abnormal characteristics were removed to reduce technical noise and low-quality observations.

### 2. Filtering

Filtering thresholds were selected after inspecting QC metric distributions.

The filtering strategy aimed to:

* Remove likely empty droplets
* Remove damaged cells
* Reduce doublets
* Improve downstream clustering performance

### 3. Normalization

Library-size normalization was applied to account for sequencing depth differences across cells.

Log-transformation was then used to stabilize variance and improve comparability across samples.

### 4. Dimensionality Reduction

The following methods were applied:

* Principal Component Analysis (PCA)
* UMAP

These approaches were used to visualize transcriptional heterogeneity across cells.

### 5. Clustering

Cell populations were identified using graph-based clustering approaches implemented in Scanpy.

---

## Software

* Python 3.10
* Scanpy
* Pandas
* NumPy
* Matplotlib
* Seaborn

---

## Key Skills Demonstrated

### Bioinformatics

* Single-cell RNA-seq analysis
* Transcriptomics
* Quality control
* Data normalization
* Exploratory data analysis

### Programming

* Python
* Data visualization
* Reproducible computational workflows

### Data Science

* High-dimensional data analysis
* Statistical preprocessing
* Biological data interpretation

---

## Reproducibility

Install dependencies:

```bash
pip install -r requirements.txt
```

Run notebooks:

```bash
jupyter notebook
```

---

## Future Improvements

Potential extensions include:

* Differential expression analysis
* Cell type annotation
* Trajectory inference
* Batch correction
* Integration of multiple datasets
* Nextflow workflow implementation
* Docker containerization

