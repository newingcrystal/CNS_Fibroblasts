# CNS_Fibroblasts
Code used for RNAseq analysis in "Dynamic fibroblast-immune interactions shape wound healing after brain injury," Ewing-Crystal et al.

-------------------------------------------------
See corresponding folder for R markdown file containing code to analyze indicated dataset, including:
  
  	Visium_R: analysis of spatial transcriptomics experiment (Fig. 1, Extended Data Fig. 2,6)
  
  	PT_Timecourse_R: analysis of first single nuclear RNA sequencing experiment (Fig. 2,3, Extended Data Fig. 3,5,6)

  	Marmoset_R, TBI_R, GBM_R: analysis of published single nuclear/cell RNA sequencing data from non-human primate or human CNS injury (Extended Data Fig. 3)
  
 	PT_TGFb_R: analysis of second single nuclear RNA sequencing experiment (Fig. 4, Extended Data Fig. 9)
   
 	PT_CXCL12_R: analysis of third single nuclear RNA sequencing experiment (FIg. 5, Extended Data Fig. 10)

Source data available in GEO at time of publication. Code run using R in RStudio.

-------------------------------------------------
System requirements:

R version 4.3.2

RStudio v2023.03.1

Seurat version 4.2.1, 5.0.1, or 5.2.1

R Packages: Presto (v1.0.0), EnhancedVolcano (v1.20.0), Nebulosa (v1.12.0), ScCustomize (v2.0.1), clusterProfiler (v4.10.0), nichenetr (v2.0.5), spacexr (v2.2.1), monocle3 (v1.3.4), DESeq2 (v1.42.0), dplyr (v1.1.4), ply (v1.8.9), ape (v5.7-1), cowplot (v1.1.2), Matrix (v1.6-4), variancePartition (v1.32.2), MAST (v1.28.0), HGNChelper (v0.8.1), openxlsx (v4.2.5.2), RColorBrewer (v1.1-3), gridExtra (v2.3), ggpubr (v0.6.0), ComplexHeatmap (v2.18.0), tidyverse (v2.0.0), tibble (v3.2.1), biomaRt (v2.58.0), data.table (v1.14.10), glmGamPoi (v1.14.0), SeuratWrappers (v0.3.2), patchwork (v1.1.3), magrittr (v2.0.3), s2 (v1.1.6), gplots (v3.1.3), stringr (v1.5.1), ggnewscale (v0.4.9), coin (v1.4-3), and dunn.test (v1.3.6).

CellPhoneDB (cellphonedb package v4.1.0) utilized Python v3.11.0 in Jupyter Notebook.
