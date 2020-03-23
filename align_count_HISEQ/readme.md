## Readme for notebooks align_and_count and HISEQ_analysis
Language: Python 2.7

These notebooks perform the first steps of data analysis for the large-scale competition assay, by taking in the raw fastq files of the HISEQ run, performing qc, trimming reads, and then aligning them to reference indexes using bowtie. Index files are provided in this repository, but the raw sequencing data should be downloaded from the NCBI at accession number PRJNA552472.

Notebook 1: make_indexes
This notebook generates bowtie indexes for gRNAs in the library based on the primer indexes used and a table of gRNA sequences. It requires some use of the command line to run the bowtie ulities that build the indexes.

Notebook 2: align_and_count_revised
This notebook uses the previouly generated indexes to generate a raw count table of gRNAs by timepoints. This is also the step where Synthesis error gRNAs (SE gRNAs) are identified and sorted depending on their abundance across the experiment. PLease note that the mutation annotations associated with this table are not the one used in the rest of that analysis, as they were updated in another script.

Notebook 3: 

The important output of these three notebooks is a table associating each gRNA to a lo2-fold change z-score (if detected in the screen). Scores from SE gRNAs are used to generate a null distribution of these scores. This distribution is then used to determine which gRNAs rae significantly depleted (GNEs) at the end of the timecourse experiment. It then ouputs a table with each gRNA and their score.
This notebook also produces Figure 3A as well as Supplementary Figure 7 Panel B and C
