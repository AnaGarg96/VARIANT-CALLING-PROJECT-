# E. coli Variant Calling Workflow (Galaxy)

## Overview

This project documents a variant calling pipeline performed on *Escherichia coli* whole‑genome sequencing data using the Galaxy platform. The main purpose of the project was to understand and implement the standard steps involved in variant calling and to organize them into a usable workflow.

## Objectives

* Assess the quality of raw sequencing reads
* Align sequencing reads to the *E. coli* reference genome
* Identify genomic variants such as SNPs and small insertions/deletions
* Filter variants to retain reliable, high‑quality calls
* Save the complete analysis as a Galaxy workflow

## Data Used

* **Organism:** *Escherichia coli*
* **Type:** Whole‑genome sequencing (paired‑end reads)
* **Source:** Publicly available example dataset accessed within Galaxy

## Tools Used (Galaxy)

* **FastQC:** to check the quality of raw sequencing reads
* **BWA‑MEM:** to align reads to the reference genome
* **FreeBayes:** to perform variant calling
* **VCFtools (Filter):** to filter variants based on quality

## Workflow Description

1. Raw FASTQ files were first checked using FastQC to assess overall read quality.
2. The reads were then aligned to the *E. coli* reference genome using BWA‑MEM, producing an alignment (BAM) file.
3. Variants were called from the aligned reads using tools, generating a VCF file.
4. The VCF file was filtered using VCFtools to keep high‑confidence variants (QUAL ≥ 30).
5. All successful steps were extracted from the Galaxy history and saved as a reusable workflow.

## Outputs
* FastQC quality report
* BAM alignment file
* Raw VCF file containing variant calls
* Filtered VCF file with high‑quality variants
* Saved Galaxy workflow

## Conclusion

This project provides a straightforward implementation of a bacterial variant calling pipeline using Galaxy. It helped build practical understanding of NGS data processing and the importance of reproducible workflows.

## Author

Ana Garg
