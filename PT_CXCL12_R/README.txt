.Rmd files contain references to Seurat objects by number and iteration name, referring to various stages of analysis, described below. When not explicitly referenced, Seurat object used corresponds to most recently created or loaded Seurat object.


TOTAL:

1) Before QC: saved Seurat object after merging individual GEM lanes (i.e. output from CellRanger count) and adding metadata, before filtering on QC metrics (e.g. percent mito, number of UMIs, etc.). 

2) Filtered: above, post filtering on QC metrics.

3) Processed: PCA, UMAP, cell type assignments, running "NormalizeData" and "ScaleData" (much larger Seurat object)
	
4) Final: added fibtype, immunetype, neurotype/neurotype_general, and ttype from relevant scripts/objects (below)  from sobject.sub.fib_reclustered (2, below x1)

----------------------------------------------------------------------------------------------

FIB: subset to fibroblasts

1) subset - not reclustered

2) reclustered

----------------------------------------------------------------------------------------------

MYELOID: subset to myeloid cells

1) subset - not reclustered

2) reclustered

----------------------------------------------------------------------------------------------

T: subset to T cells

1) subset - not reclustered

2) reclustered

----------------------------------------------------------------------------------------------

Neurons: subset to neurons

1) subset - not reclustered

2) reclustered
