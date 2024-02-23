# Single-cell-RNA-seq-data-integration-and-analysis
Welcome to the scRNA-seq Integration and Analysis repository! This repository contains R code for integrating single-cell RNA sequencing (scRNA-seq) datasets using six different approaches, as well as conducting evaluation and downstream analyses. The dataset utilized in this repository was sourced from the NCBI GEO data repository.

# Dataset Information
The dataset used in this project is GSE162631, which consists of 4 samples of each tumor and normal endothelial cells of the brain. Two samples of tumor and normal cells were used for analysis. This dataset provides a valuable resource for studying the gene expression profiles of endothelial cells in both tumor and normal conditions. Seurat object was created for each sample and cells containing high mitochondrial transcripts were removed before the integration. 

# Approach
Integration Methods
1) Seurat
2) LIGER
3) Harmony
4) Reciprocal PCA
5) scVI
6) Scanorama

# Evaluation
Evaluation metrics used for assessing integration performance:
1) kBET: Test for assessing batch effects correction. (https://github.com/theislab/kBET)
2) Silhouette score: Quantifies clustering quality of similar cell-types in single-cell data. (https://www.rdocumentation.org/packages/cluster/versions/2.1.6/topics/silhouette)
3) Mixing metric: Evaluates the degree of mixing of similar cell types from different datasets. (https://satijalab.org/seurat/reference/mixingmetric)
4) Local Inverse Simpson's Index (LISI): Asseses the dominance of cell-type within a cluster. The test used is cLISI or cell-type LISI. (https://www.nature.com/articles/s41592-019-0619-0)
5) Local Structure Preservation: Assesses how effectively the original dataset structure is preserved post-integration.(https://satijalab.org/seurat/reference/localstruct)

# Downstream Analyses
The optimally integrated object was saved and different analyses were conducted on this object to gain deeper insights about the gene expression profiles under normal and tumor conditions:
1) Differential Expression Analysis: Used for Identifying biomarkers closely associated with distinct cell types/conditions.
2) Gene Coexpression Analysis: Helps in establishing co-expression networks associated with specific cell-types/conditions across various Gene Ontologies.
3) Pseudotemporal ordering: Helps in identifying cell development trajectories.

# Dependencies
R version 4.2.2



