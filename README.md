# RNA-seq Differential Expression Analysis Using DESeq2
Analysis of the publicly available **PRJNA490376** RNA-seq dataset comparing **NRDE2 knockdown** and **control** samples using the **nf-core/rnaseq** workflow, **Salmon**, **tximport**, and **DESeq2**.
This project demonstrates an end-to-end RNA-seq analysis workflow, from transcript quantification to differential gene expression analysis and downstream visualization.
## Overview
Analysis of publicly available PRJNA490376 RNA-seq dataset comparing NRDE2 knockdown and control samples using the nf-core/rnaseq pipeline, Salmon, tximport, and DESeq2.

## Objective

The goal of this project is to identify genes that are differentially expressed between NRDE2 knockdown and control samples using an RNA-seq differential expression workflow.

## Tools Used

**Programming**
- R

**RNA-seq Analysis**
- Salmon
- tximport
- DESeq2
- apeglm

**Visualization**
- ggplot2

**Data Import**
- readr

**Workflow**
- nf-core/rnaseq
- Nextflow
- SLURM

## Input

The analysis requires the following input files:

- Salmon transcript quantification files (`quant.sf`)
- Sample metadata (`samplesheet.csv`)
- Transcript-to-gene mapping (`tx2gene.tsv`)

## Repository Structure

```text
scripts/      R analysis scripts
pipeline/     Nextflow and SLURM execution files
docs/         Analysis report and workflow reports
results/      Figures and output tables
data/         Dataset information
environment/  Session information and package versions
```

## Workflow

1. Import Salmon transcript quantifications.
2. Summarize transcript-level abundance to gene-level counts using tximport.
3. Perform differential expression analysis with DESeq2.
4. Apply log2 fold change shrinkage using apeglm.
5. Generate quality-control visualizations.
6. Export differential expression results.

## Results

Running the workflow generates:

- Differential expression results (.csv)
- PCA plot
- MA plot
- Dispersion estimate plot
- P-value histogram

## Skills Demonstrated

- RNA-seq differential expression analysis
- Transcript quantification with Salmon
- Gene-level count summarization using tximport
- Differential expression analysis with DESeq2
- Log2 fold change shrinkage with apeglm
- Statistical analysis of sequencing data
- RNA-seq quality assessment
- Data visualization in R
- Reproducible bioinformatics workflow development
