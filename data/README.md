# Data

Raw and processed data files are not committed to this repository.

Before this project can be described as fully reproducible, the dataset source, accession identifiers, download instructions, expected file names, and preprocessing assumptions should be documented here.

Large single-cell data files such as `.h5ad`, `.h5`, `.loom`, and `.rds` should remain outside Git history unless there is a specific reason to include a small example dataset.

## Expected Local Layout

The active cSCC notebook reads input data from the `CSCC_DATA_ROOT` environment variable. If that variable is not set, it falls back to:

```text
data/raw/cscc/
```

The expected local directory layout is:

```text
data/raw/cscc/
├── P2_normal/
│   └── filtered_feature_bc_matrix.h5ad
├── P2_cSCC/
│   └── filtered_feature_bc_matrix.h5ad
├── P3_normal/
│   └── filtered_feature_bc_matrix.h5ad
├── P3_cSCC1/
│   └── filtered_feature_bc_matrix.h5ad
├── P3_cSCC2/
│   └── filtered_feature_bc_matrix.h5ad
├── P4_normal/
│   └── filtered_feature_bc_matrix.h5ad
├── P4_cSCC1/
│   └── filtered_feature_bc_matrix.h5ad
├── P4_cSCC2/
│   └── filtered_feature_bc_matrix.h5ad
├── P5_normal/
│   └── filtered_feature_bc_matrix.h5ad
└── P5_cSCC/
    └── filtered_feature_bc_matrix.h5ad
```

`data/raw/` is intentionally ignored by Git. Do not commit the `.h5ad` files.

## Discovered Local Mapping

During local inspection, matching input files were found under Downloads:

```text
P2_normal -> /Users/emily/Downloads/Assignment_1_1/P2_normal/filtered_feature_bc_matrix.h5ad
P2_cSCC   -> /Users/emily/Downloads/Assignment_1_2/P2_cSCC/filtered_feature_bc_matrix.h5ad
P3_normal -> /Users/emily/Downloads/Assignment_1_1/P3_normal/filtered_feature_bc_matrix.h5ad
P3_cSCC1  -> /Users/emily/Downloads/Assignment_1_1/P3_cSCC1/filtered_feature_bc_matrix.h5ad
P3_cSCC2  -> /Users/emily/Downloads/Assignment_1_1/P3_cSCC2/filtered_feature_bc_matrix.h5ad
P4_normal -> /Users/emily/Downloads/Assignment_1_4/P4_normal/filtered_feature_bc_matrix.h5ad
P4_cSCC1  -> /Users/emily/Downloads/Assignment_1_3/P4_cSCC1/filtered_feature_bc_matrix.h5ad
P4_cSCC2  -> /Users/emily/Downloads/Assignment_1_4/P4_cSCC2/filtered_feature_bc_matrix.h5ad
P5_normal -> /Users/emily/Downloads/Assignment_1_3/P5_normal/filtered_feature_bc_matrix.h5ad
P5_cSCC   -> /Users/emily/Downloads/Assignment_1_2/P5_cSCC/filtered_feature_bc_matrix.h5ad
```

Because the files are currently spread across multiple `Assignment_1_*` folders, the safest reproducible setup is to create an ignored local `data/raw/cscc/` directory or set `CSCC_DATA_ROOT` to a local directory that contains the expected sample folders.
