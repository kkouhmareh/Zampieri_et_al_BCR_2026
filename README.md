# Single-cell and spatial transcriptomic profiling reveals human breast cancer subtype-specific expression of the urokinase receptor/PLAUR and its association with cancer aggressiveness


## Zampieri et al, 2026 Breast Cancer Research

## Description


This repository contains the code and input files needed to 
reproduce the single-cell RNA sequencing figures in the paper.

## Dependencies
 
| Package | Version |
|---|---|
| Python | 3.10.13 |
| scanpy | 1.11.1 |
| scvi-tools | 1.3.3 |
| anndata | 0.11.4 |
| numpy | 2.1.3 |
| pandas | 2.2.3 |
| scipy | 1.15.2 |
| scikit-learn | 1.5.2 |
| statsmodels | 0.14.4 |
| leidenalg | 0.10.2 |
| celltypist | 1.6.3 |
| infercnvpy | 0.6.0 |
| gseapy | 1.1.8 |

## scRNA-seq Directory Structure

To run the notebooks, place the `.h5ad` files in a `data/` folder in the same directory as the notebook:

```
.
├── README.md
├── [notebook_name].ipynb   # single-cell and spatial analyses
├── data/
│   ├── GSE161529.h5ad
│   ├── GSE176078.h5ad
│   └── GSE246613.h5ad
└── output/
```      

## 10x Visium Directory Structure

To run the notebook, place the `.h5ad` files in a `data/` folder in the same directory as the notebook:

```
.
├── README.md
├── [notebook_name].ipynb
├── data/
│   ├── adata_092a.h5ad
│   ├── adata_092b.h5ad
│   └── ...              # all remaining .h5ad files
└── output/
```

## Data Availability

The processed AnnData (.h5ad) have been deposited on Zenodo, 
one repository per dataset. 

- GSE161529: https://zenodo.org/records/23518046 (scRNA-seq)
- GSE246613: https://zenodo.org/records/23517977 (scRNA-seq)
- GSE176078: https://zenodo.org/records/23518300 (scRNA-seq)
- GSE210616: https://zenodo.org/records/23517586 (Spatial Transcriptomics)


## Source Data
Each dataset name corresponds to its accession number of the Gene Expression Omnibus:

	For each dataset, the following files were downloaded from 
	the source repository:

	*Only untreated samples were utilized in this study, if you 
	wish to use the "scRNA-seq Processing" or "spatial Processing" 
	notebooks to include excluded samples from the source repository, 
	the Supplementary Tables including the metadata for each cohort 
	are available below:

 
## GSE161529: https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE161529

- Source Publication DOI: 10.15252/embj.2020107333
- Cohort Metadata: Supplementary Tables 1-4

- Each sample's barcodes.tsv and matrix.mtx file was downloaded
- The feature file: "GSE161529_features.tsv.gz" is used for all samples and 
available on the GEO repository

| GSM ID | Subtype | Patient |
|---|---|---|
| GSM4909296 | ER+ | 0001 |
| GSM4909297 | ER+ | 0125 |
| GSM4909298 | ER+ | 0360 |
| GSM4909299 | ER+ | 0114 |
| GSM4909300 | ER+ | 0032 |
| GSM4909301 | ER+ | 0042 |
| GSM4909302 | ER+ | 0025 |
| GSM4909303 | ER+ | 0151 |
| GSM4909304 | ER+ | 0163 |
| GSM4909305 | ER+ | 0029-7C |
| GSM4909306 | ER+ | 0029-9C |
| GSM4909307 | ER+ | 0040 |
| GSM4909309 | ER+ | 0043 |
| GSM4909311 | ER+ | 0056 |
| GSM4909313 | ER+ | 0064 |
| GSM4909315 | ER+ | 0167 |
| GSM4909317 | ER+ | 0173 |
| GSM4909319 | ER+ | 0178 |
| GSM4909320 | ER+ | 0068 |
| GSM4909289 | HER2+ | 0308 |
| GSM4909290 | HER2+ | 0337 |
| GSM4909291 | HER2+ | 0031 |
| GSM4909292 | HER2+ | 0069 |
| GSM4909293 | HER2+ | 0161 |
| GSM4909294 | HER2+ | 0176 |
| GSM4909281 | Triple negative | 0126 |
| GSM4909282 | Triple negative | 0135 |
| GSM4909283 | Triple negative | 0106 |
| GSM4909284 | Triple negative | 0114 |
| GSM4909285 | Triple negative (BRCA1) | 4031 |
| GSM4909286 | Triple negative (BRCA1) | 0131 |
| GSM4909287 | Triple negative (BRCA1) | 0554 |
| GSM4909288 | Triple negative (BRCA1) | 0177 |


## GSE246613: https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE246613

- Source Publication DOI: 10.1016/j.ccell.2023.12.012
- Cohort Metadata: Table S1

### Author Provided .h5ad files
- GSE246613_PembroRT_non_immune_cells.h5ad.gz
- GSE246613_PembroRT_immune_R100_final.h5ad.gz

Only Base (Untreated) samples in 'treatment' were used.

## GSE176078: https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE176078

- Source Publication PMID: 34493872
- Cohort Metadata: Supplementary Table 1

| GSM ID | Subtype | Patient |
|---|---|---|
| GSM5354513 |	HER2+ |CID3586
| GSM5354514 |	HER2+  |CID3838
| GSM5354515 |	HER2+  |CID3921
| GSM5354516 |	ER+  |CID3941
| GSM5354517 |	TNBC |CID3946
| GSM5354518 |	ER+ |CID3948
| GSM5354520 |	ER_  |CID4040
| GSM5354522 |	ER+  |CID4067
| GSM5354523 |	ER+ |CID4290A
| GSM5354525 |	TNBC |CID44041
| GSM5354526 |	ER+  |CID4461
| GSM5354527 |	ER+  |CID4463
| GSM5354528 |	TNBC |CID4465
| GSM5354529 |	ER+ |CID4471
| GSM5354530 |	TNBC |CID4495
| GSM5354531 |	TNBC |CID44971
| GSM5354532 |	TNBC |CID44991
| GSM5354534 |	TNBC |CID4515
| GSM5354535 |	HER2+ |CID45171
| GSM5354537 |	ER+ |CID4530N
| GSM5354538 |	ER+ |CID4535

Treated samples were excluded

## GSE210616: https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE210616

- Source Publication DOI: 10.1158/0008-5472.CAN-22-2682
- Cohort Metadata: Supplementary File 1 

For each sample, download the following:

.cloupe.gz
filtered_feature_bc_matrix.h5
scalefactors_json.json
tissue_hires_image.png
tissue_lores_image.png
| GSM ID | Patient |
|---|---|
| GSM6433585 |092A
| GSM6433586 | 092B
| GSM6433587 | 093A
| GSM6433588 | 093B
| GSM6433598 | 117C
| GSM6433603 | 118D
| GSM6433604 | 118E
| GSM6433608 | 119E
| GSM6433609 | 120B
| GSM6433610 | 120C

Both treated samples and untreated samples where PLAU was not an HVG were excluded

## QC and Filtering Parameters

Any quality control or filtering cutoff step has been highlighted if you wish to modify for your analysis. 

## Bulk Transcriptomic Data

Excel files containing patient metadata, along with the data used to generate plots
in Figures 1 and 2 are available in the GitHub repository within the folder
"Bulk_Transcriptomics_Data". 

- BC_Cell2015 DATA.xlsx (Date Accessed: 12/13/2025) https://www.cbioportal.org/study/summary?id=brca_tcga_pub2015
- BC_PanCancerAtlas.xlsx (Date Accessed: 12/13/2025) https://www.cbioportal.org/study/summary?id=brca_tcga_pan_can_atlas_2018
- METABRIC_data.xlsx (Date Accessed: 12/13/2025) https://www.cbioportal.org/study/summary?id=brca_metabric

Parameters used from GEPIA2: (http://gepia2.cancer-pku.cn) 
(Tang et al., *Nucleic Acids Res* 2019; 47(W1):W556–W560)

| Parameter | Value |
|---|---|
| Analysis | Expression DIY → Box plot |
| Gene | PLAUR |
| \|Log2FC\| cutoff | 1 |
| p-value cutoff | 0.01 |
| Dataset | BRCA |
| Log scale | Yes (log2(TPM + 1)) |
| Jitter size | 0.4 |
| Matched normal data | Match TCGA normal and GTEx data |
| Statistical test | One-way ANOVA |
| Sample size | Tumour n = [ ], Normal n = [ ] |
