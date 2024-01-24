Fibroblast cluster correspondence (code uses working names based on representative DEG):
	*working name* = *figure name*
	Prolif = Prolif
	Fn1 = Myofibroblast
	Cd80 = Lymphocyte interactive
	Ghr = Late myofibroblast
	Lama1 = Pial
	Ptgds = Arachnoid
	Tmeff2 = altered dural

Myeloid cell cluster correspondence (code uses working names based on representative DEG):
	*working name* = *figure name*
	Macrophage_ECM = ECM_Mac
	Macrophage_CD206 = PVM/BAM
	Macrophage_Ldlrad3 = SAM
	DAM = DAM
	Microglia = Microglia
	Monocyte_DC = Mono/DC

---------------------------------------------------------------------------------------------

.Rmd files contain references to Seurat objects by number and iteration name, referring to various stages of analysis, described below. When not explicitly referenced, Seurat object used corresponds to most recently created or loaded Seurat object.


TOTAL:

1) Before QC: saved Seurat object after merging individual GEM lanes (i.e. output from CellRanger multi) and adding metadata, before filtering on QC metrics (e.g. percent mito, number of UMIs, etc.). NOTE - "organ" metadata incorrectly lists 1_rest_parenchyma as "meninges" (fixed later)

2) Filtered: above, post filtering on QC metrics. NOTE - "organ" metadata incorrectly lists 1_rest_parenchyma as "meninges" (fixed later)

3) Processed: PCA, UMAP, cell type assignments, etc.

4) Scaled: after running "NormalizeData" and "ScaleData" (much larger Seurat object)
	
5) Final: excluded 21dpi cKO (wrong genotypes + clog); renamed certain clusters

#Below from "6_integrate_visium_fib.Rmd"

6) Final_fib_no710: included fibtype and fibtypecluster variables, excluded cluster 7/10, as in Fib/3) below

7) Final_fib_no710_nomen_wt: excluded meninges (by cluster and microanatomy, as Fib/5-6), below

#Below from 8_integrate_visium_immune.Rmd

8) Final_immune: starting from 6 (final_fib_no7no10), included immunetype and immunetypecluster variables

9) Final_immune_nomen_wt: excluded meninges (by microanatomy), subset to WT

#Below from 10_integrate_visium_astrocyte.Rmd

10) Final_astro: starting from 8 (final_immune), included astrotype and astrotypecluster variables

11) Final_astro_nomen_wt: excluded meninges (by microanatomy), subset to WT

12) final_fib-immune-astro-subset: starting from 10 (final_astro), integrate fibtype/immunetype/astrotype into "celltype_subest" (and celltype_subsetcluster) metadata column


----------------------------------------------------------------------------------------------

IMMUNE: subset to clusters 1, 13, 17 (T-cells + myeloid)

1) not reclustered - just subset, as above

2) reclustered

3) macrophages: subset "DAMs", "Macrophage_Ldlrad3", "Macrophage_CD206", "Macrophage_ECM", "Monocytes/DCs", "Microglia"

4) immune_reclustered_7dpi: starting from 2 (reclustered), isolate 7dpi (all genotypes)

----------------------------------------------------------------------------------------------

ASTRO: subset to clusters 7, 20 (astrocytes)

1) not reclustered - just subset

2) reclustered

3) WT only

----------------------------------------------------------------------------------------------

FIB: subset to clusters 2, 5, 6, 8, 16, 24 (fibroblasts)

1) not reclustered - just subset, as above

2) reclustered

3) v2: remove cluster 7 (myeloid, likely doublets) and 10 (neuron, likely doublets)

4) wt-all: remove cluster 7/10, then subset to only wild type

5) wt: remove cluster 7/10, meninges, then subset to only wildtype

6) 7dpi: remove cluster 7/10, meninges, then subset to only 7dpi

#Old (res=0.25, vs. new res=0.5)
	
3) v2: remove cluster 6 (myeloid, likely doublets)

4) wt-all: remove cluster 6, then subset to only wild type

5) wt: remove cluster 6, meninges, and mural cells, then subset to only wildtype

6) 7dpi: remove cluster 6, meninges, and mural cells, then subset to only 7dpi
