# Methodology

This project follows a focused cSCC single-cell RNA-seq workflow comparing patient-derived normal skin-associated samples with cutaneous squamous cell carcinoma samples.

The active analysis is contained in `notebooks/01_qc_filtering_normalization.ipynb` and is intended to cover:

1. Loading normal and cSCC sample-level AnnData objects
2. Adding patient, sample, and condition metadata
3. Calculating cell-level quality control metrics
4. Filtering low-quality cells, stressed cells, and likely outliers
5. Normalizing total counts and applying log transformation
6. Selecting highly variable genes
7. Running PCA, neighborhood graph construction, UMAP, and Leiden clustering
8. Comparing integrated and non-integrated embeddings where supported by dependencies
9. Identifying marker genes for cluster interpretation
10. Comparing cell type composition between normal and cSCC samples

An unrelated mouse hematopoiesis trajectory notebook has been archived and is not part of this cSCC methodology.

This document can be expanded with cSCC-specific dataset provenance, parameter choices, filtering rationale, marker evidence, and interpretation as the repository is refined.
