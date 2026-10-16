# Whole Exome Sequencing (WES) Analysis — SRR098401

## Project Overview

This project demonstrates a bioinformatics workflow for Whole Exome Sequencing (WES) data analysis using the sample SRR098401. The workflow covers read quality control, read trimming, alignment, duplicate marking, base quality score recalibration (BQSR), variant calling, variant filtering, and quality assessment of the final variants.

## Objectives

- Assess raw sequencing read quality.
- Trim reads to improve data quality.
- Align sequencing reads to the GRCh38 reference genome.
- Evaluate alignment quality and duplicate metrics.
- Perform variant calling and variant filtering.
- Summarize final SNP and INDEL results.
- Organize quality-control reports for reproducibility.

## Tools and Technologies

- SRA Toolkit
- FastQC
- fastp
- BWA
- SAMtools
- GATK
- Linux / Ubuntu
- Bash scripting

## Analysis Workflow

1. Retrieve sequencing data for SRR098401.
2. Perform quality control on raw reads using FastQC.
3. Trim reads using fastp.
4. Perform quality control on trimmed reads.
5. Prepare the GRCh38 reference genome and indexes.
6. Align reads using BWA.
7. Evaluate alignment statistics using SAMtools.
8. Mark duplicate reads and review duplicate metrics.
9. Apply base quality score recalibration where supported by available resources.
10. Call variants using GATK.
11. Filter SNPs and INDELs.
12. Review final variant statistics and quality-control summaries.

## Key Results

The recorded project metrics include:

- Total reads before trimming: 114,059,565 per read file.
- Reads after trimming: 85,897,923 per read file.
- Alignment rate: 99.93%.
- Properly paired reads: 99.22%.
- Duplicate rate: approximately 6.49%.
- Final PASS SNP records: 1,309,467.
- Final PASS INDEL records: 155,214.
- Total PASS variant records: 1,464,681.

These values are reported from the project's recorded outputs and should be interpreted in the context of the pipeline and its filtering criteria.

## Repository Contents

- `05_fastqc/` — FastQC reports for raw reads.
- `07_trimmed_fastqc/` — FastQC reports for trimmed reads.
- `10_bam_qc/` — Alignment quality statistics.
- `12_markdup_qc/` — Quality statistics after duplicate marking.
- `16_bqsr_qc/` — Recalibration-related quality-control outputs.
- `21_final_qc/` — Statistics for final filtered SNPs and INDELs.
- `22_variant_annotation/` — Small test files used during annotation-related work.
- `23_project_summary/` — Final project summary.
- `.gitignore` — Rules excluding large data files and intermediate outputs.

## Data and File Management

Large sequencing files, reference genome files, alignment files, compressed intermediate files, and large variant files are excluded from this repository to keep it suitable for GitHub.

The repository focuses on documentation and selected quality-control results rather than distributing the full sequencing dataset.

## Limitations and Notes

- Base quality score recalibration depends on suitable known-sites resources and should be interpreted in light of the resources available during this analysis.
- Variant filtering results depend on the selected filtering criteria and the annotations available in the input variant records.
- Functional annotation is not documented as a completed full-scale analysis in this repository.
- Variant counts alone do not establish clinical significance or validate biological findings.

## Reproducibility

The reports in this repository document selected outputs from the analysis. To reproduce the complete workflow, users must obtain the sequencing data and appropriate reference resources separately and configure the required bioinformatics tools.

## Author

Swati Kumari Mishra

## Disclaimer

This project is intended for academic and bioinformatics learning purposes. The reported variants are not clinical interpretations or medical advice.
