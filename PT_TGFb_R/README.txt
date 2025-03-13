.Rmd files contain references to Seurat objects by number and iteration name, referring to various stages of analysis, described below. When not explicitly referenced, Seurat object used corresponds to most recently created or loaded Seurat object.


TOTAL:

1) Before QC: saved Seurat object after merging individual GEM lanes (i.e. output from CellRanger count) and adding metadata, before filtering on QC metrics (e.g. percent mito, number of UMIs, etc.). 

2) Filtered: above, post filtering on QC metrics.

3) Processed: PCA, UMAP, cell type assignments, running "NormalizeData" and "ScaleData" (much larger Seurat object)
	
4) Final_withfibtype: added fib type from sobject.sub.fib_reclustered (2, below x1)

5) Final_withfibtype_withimmunetype: added immune type from sobject.sub.immune.reclustered (2, below x2)

6) Final_withfibtype_withimmunetype_withttype: added t type from sobject.sub.t.reclustered (2, below x3)

7) Final_withfibtype_withimmunetype_withttype_nodoublets: removed *fibroblast* doublet clusters 1, 3 (neurons, macrophages)

----------------------------------------------------------------------------------------------

FIB: subset to fibroblasts

1) subset - not reclustered

2) reclustered

3) final - minus doublet clusters 1, 3 (neurons, macrophages)

----------------------------------------------------------------------------------------------

MYELOID: subset to myeloid cells

1) subset - not reclustered

2) reclustered

----------------------------------------------------------------------------------------------

T: subset to T cells (including NK, ILC, etc.)

1) subset - not reclustered

2) reclustered
