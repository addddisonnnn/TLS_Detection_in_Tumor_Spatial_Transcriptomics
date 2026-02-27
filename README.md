# Spatial Tumor Microstructure: TLS Detection Project

### Project Goal
Characterize structures,  especially Tertiary Lymphoid Structures (TLS),  in tumor tissue using spatial transcriptomics by:

1. Processing a scRNA-seq reference to identify and annotate immune and tumor cell types
2. Processing 10x Visium spatial data from matched tumor tissue
3. Deconvoluting spatial spots using the scRNA-seq reference (figuring out what mix of cell types is at each location)
4. Scoring TLS gene signatures per spot and identifying TLS-enriched regions on the tissue

### Repository Structure
```text
spatial-tumor-tls/
├── README.md
├── environment.yml  
├── data/
├── notebooks/
├── results/
└── src/
```

### Data

### Setup

### Biology Background
Tertiary Lymphoid Structures are organized immune aggregates that form inside tumors, acting like mini lymph nodes. They contain:
- B-cell follicles (sometimes with germinal centers — sign of active immune response)
- T-cell zones
- Follicular Dendritic Cells
- High Endothelial Venules (HEVs)
Their presence in tumors is one of the strongest known predictors of good patient outcomes and better response to immunotherapy.

#### Key Cell Type Markers
|     Cell Type    |       Key Genes       |        Why they matter for TLS       |
|:----------------:|:---------------------:|:------------------------------------:|
| B cells          | MS4A1, CD79A, IGHM    | Core TLS component                   |
| T cells (CD8+)   | CD3D, CD8A, GZMB      | Cytotoxic — kills tumor cells        |
| T cells (CD4+)   | CD3D, CD4, IL7R       | Helper — coordinates immune response |
| Regulatory T     | CD3D, FOXP3           | Suppresses immune response           |
| Dendritic cells  | CLEC9A, LAMP3, FCER1A | TLS organizer cells                  |
| Plasma cells     | MZB1, IGHG1           | Mature B cells, make antibodies      |
| NK cells         | NKG7, GNLY            | Innate immune killers                |
| Macrophages      | CD68, CSF1R           | Tumor-infiltrating myeloid           |
| Tumor/Epithelial | EPCAM, KRT8           | Cancer cells                         |

### References
