## Readme
Language: Python 3

This directory contains the scripts and data used to analyse the base editing timecourse deep sequencing results and generate the associated figures in the manuscript. Most files are provided directly in this repository, but the raw sequencing data should be downloaded from the NCBI at accession number PRJNA552472. It is recommended that the placeholder files used to preserve the directory sturcture on github be removed before running the notebooks.

BE_NGS_needle_align:
This notebook takes in the raw sequencing data, performs demultiplexing using the two levels of barcoding (barcodes are aligned with bowtie) and then splits the reads into multiple subfiles. The reads are then merged with PANDA-Seq and aligned to the target gene using the Needle alignment tool of the EMBOSS suite. Please note that some parts of the notebook require the use of the command line, in particular to run trimmomatic. It also performs some of the data analysis, and imports some results from the other notebook to generate Supplementary Figures 4, 5, 6. When you reach this point of the notebook, please switch to the other one and run it to generate the required intermediate files.

target_co_editing:
Performs most of the analysis that generate Figure 1. Requires intermediate results from the previous script to work. Also contributes some files that are used to generate the Supplementary figrues in the first notebook.
