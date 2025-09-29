# Single-Cell RNA Sequencing Data Preprocessing with Scanpy

This notebook demonstrates a basic workflow for preprocessing single-cell RNA sequencing data using the Scanpy library in Python. The steps covered are essential for preparing 10x Genomics data for downstream analysis such as dimensionality reduction, clustering, and differential expression.

## 📖 Overview

The notebook walks through:

1.  **Loading 10x Genomics Data:** Reading raw count data, gene information, and cell barcodes into an AnnData object.
2.  **Initial Data Inspection:** Examining the structure and dimensions of the AnnData object (`.X`, `.obs`, `.var`).
3.  **Basic Quality Control (QC):**
    *   Filtering out low-quality cells based on minimum detected genes.
    *   Filtering out genes expressed in very few cells.
    *   Calculating QC metrics such as total counts per cell and the percentage of mitochondrial reads.
    *   Visualizing QC metrics using violin plots and scatter plots to identify potential outliers.
    *   Filtering cells based on outlier values for gene counts and mitochondrial percentage using quantiles.
4.  **Normalization:** Normalizing total counts per cell to a common scale (e.g., 10,000 UMI).
5.  **Log Transformation:** Applying a log1p transformation to stabilize variance and make data more suitable for downstream analysis.
6.  **Visualizing Transformation Effect:** Demonstrating the effect of the log1p transformation on the distribution of total counts.

## Prerequisites

*   Python 3.7+
*   Scanpy
*   Anndata
*   Numpy
*   Pandas
*   Matplotlib
*   Seaborn
*   Leidenalg
*   Louvain

These libraries can be installed using pip as shown in the notebook.

## 📂 Dataset
This notebook assumes the use of data in the 10x Genomics Cell Ranger output format, consisting of `matrix.mtx`, `barcodes.tsv`, and `features.tsv` (or `genes.tsv`). These files are typically found in the 'filtered_feature_bc_matrix' directory after running Cell Ranger.

1.  Ensure you have your 10x Genomics output files (`matrix.mtx.gz`, `barcodes.tsv.gz`, `features.tsv.gz`) in a directory accessible by the notebook.
2.  Update the file path in the `sc.read_10x_mtx()` command to point to your data directory.
3.  Run the cells sequentially to perform the preprocessing steps.
4.  Adjust QC thresholds and parameters as needed based on your specific dataset.

## Next Steps

After completing the preprocessing steps in this notebook, you can proceed with further analysis, including:

*   Identifying highly variable genes
*   Dimensionality reduction (PCA, UMAP, t-SNE)
*   Clustering cells
*   Visualizing cell populations
*   Differential gene expression analysis