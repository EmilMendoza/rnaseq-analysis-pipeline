# RNA-seq Differential Expression Analysis Using DESeq2

## Overview
Analysis of publicly available PRJNA490376 RNA-seq dataset comparing NRDE2 knockdown and control samples using the nf-core/rnaseq pipeline, Salmon, tximport, and DESeq2.

## Objective
The goal of this prroject is to determine how NRDE2 knockdown affects gene expression samples compared with control samples

### Tools used
- R
- Salmon
- tximport
- DESeq2
- apeglm
- ggplot2
- readr

### Input
The analysis requires:
- Salmon qunfitication files('quant.sf')
- Sample metadata ('samplesheet.csv')
- Transcript-to-gene mapping ('tx2gene.tsv')

## Repository Structure

```text
scripts/      R analysis scripts
pipeline/     Nextflow and SLURM execution files
docs/         Analysis report and workflow reports
results/      Figures and output tables
data/         Dataset information
```

## Workflow
1. Import Salmon transcript quantifications.
2. Summarrize transcript-level abundance to gene-level counts usiung tximport.
3. Perform differential expression analysis with DESeq2.
4. Apply log2 fold change shrinkage using aplegm.
5. Generate quality contorl visualizations (PCA, MA plot, dispersion estimates, p-value distribution).
6. Export differential expression results.


# Results
Running the worflow produces:
- Differential exprression results (CSV)
- PCA plot
- MA plot
- Dispersion extimate plot
- P-value histogram

## Skills Demonstrated
RNA-seq differential expression analysis, transcript-to-gene count summarization, statistical analysis of sequenecing data, data visualization in R, and reproducible bioinformatics workflow development.
