# DEG-analysis
Limma &amp; PCA analysis of GSE15852, GSE109169 for tumor vs normal  GSE129551, GSE20685 for early vs late stage 


Datasets and comparisons:
  GSE15852  (GPL96,  Tumor vs Normal)        - limma, |logFC| > 1,   n sig DEGs: 1658
  GSE109169 (GPL5175, Tumor vs Normal)       - limma, |logFC| > 1,   n sig DEGs: 849
  GSE129551 (GPL96,  Late vs Early Stage)    - limma, |logFC| > 0.5, n sig DEGs: 79
  GSE20685  (GPL570, Late vs Early Stage)    - limma, |logFC| > 0.5, n sig DEGs: 12

Notes:
  - All analyses genome-wide (all probes on each array), no gene list restriction.
  - Significance: adj.P.Val < 0.05 (BH-adjusted) for all thresholds above.
  - logFC cutoff differs between tumor-vs-normal (1.0) and stage (0.5) comparisons
    because early-vs-late stage transcriptional differences are subtler in magnitude.
  - GSE109169 is an exon array (GPL5175); ~8% of probes (1560/19076) lack a mapped
    gene symbol and are excluded from filtered/top-DEG tables (but not from the DE test itself).
  - _filtered.csv files: all probes with adj.P.Val < 0.5 and a valid gene symbol (broader
    reference list beyond the strict significance cutoff).
  - _topDEGs files: top 25 by adjusted p-value at the dataset-specific logFC cutoff.
  - _top10_up/downregulated files: top 10 by logFC magnitude among significant genes.
