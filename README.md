# EncinasLab
This is the repository for Encinas' lab code.

*Methods*
To validate the presence of Lpar1 at the transcriptomic level in hippocampal radial glia, equivalently to our study; we re-analysed the single cell RNA-seq published by Hochgerner et al (2018). This article characterized cell type diversity of dentate gyrus in perinatal, juvenile, and adult mice.

We downloaded and imported this dataset to R (v4.1.0), where Seurat (v4.1.0) (Hao et al, 2021) was employed to further analysis, as describe in their vignettes (https://satijalab.org/seurat/). All the code employed is stored in https://github.com/rodrisenovilla/EncinasLab.

In all cases, processing followed Seurat’s default parameters for normalization, variable features (SCTransform) and dimension reduction (PCA, UMAP). Filtering based on poor quality was based on detected genes and mitochondrial percentage (PercentageFeature-Set(pattern= “^MT-”)). Additionally, cell cycle was calculated based on S-phase and G2M-phases specific genes (“cellcycle_genes.csv”) (Li et al, 2019).

An exploratory analysis was carried out of the whole dentate gyrus dataset, but the main displayed analysis (Figure X) was done only with the annotated cells as astrocytes and radial glia, re-processed conveniently. To visualize metadata from original publication, different UMAPs were displayed employing DimPlot() and annotation columns ("characteristics..age" and "characteristics..cell.cluster"). Finally, different gene markers, including Lpar1, of radial glia or/and astrocytes were visualized by FeaturePlot().

*Bibliography*
Cell Cycle (Li et al, 2019)
https://doi.org/10.1242/dev.173476
Seurat (Hao et al, 2021 ; V4)
https://www.sciencedirect.com/science/article/pii/S0092867421005833?via%3Dihub
Hochgerner et al, 2018:
https://www.nature.com/articles/s41593-017-0056-2
