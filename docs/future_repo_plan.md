# Future Repository Plan

## Proposed Repository

`single-cell-hematopoiesis-analysis`

## Dataset

- GEO accession: `GSE107727`
- Organism: mouse (`Mus musculus`)
- Biological system: bone marrow hematopoietic stem and progenitor cells
- Project type: exploratory single-cell RNA-seq clustering, marker analysis, lineage trajectory, PAGA, and DPT pseudotime analysis

## Description

The archived notebook represents a separate mouse hematopoiesis project, not a cSCC skin cancer analysis. It uses GEO samples `GSM2877127` through `GSM2877134` and explores hematopoietic populations such as HSC, myeloid, erythroid, and lymphoid cells using clustering, marker gene visualization, and trajectory-style analysis.

The biological question is closer to:

> How can single-cell RNA-seq resolve hematopoietic progenitor populations and inferred lineage structure in mouse bone marrow?

## Files To Move Later

- `archive/02_downstream_analysis_mouse_hematopoiesis.ipynb`
- `reports/02_Downstream_Analysis.html`, if regenerated or retained as a report for that analysis
- Any local input files matching `GSM2877127_SIGAB1.h5ad` through `GSM2877134_SIGAH8.h5ad`
- Any future figures, tables, environment files, or metadata documentation specific to `GSE107727`

## Migration Notes

The future repository should document GEO provenance, download steps, sample metadata, expected filenames, checksums, and environment setup before the notebook is presented as reproducible.
