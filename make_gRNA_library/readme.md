## readme
Language: Python 2.7
This notebook generates the gRNA library from info on known gRNAs in the yeast genome, essential gene information, fitness effect information fromt the yeast deletion collection, information on yeast introns, and a set of unannotated yeast putative non-functionnal peptides.

All files required to run the notebook are in the directory, with exception of no_nag_targets.fasta, which can be generated from the supplementary material of DiCarlo et al 2013 (NAR): https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3627607/
Simply generate a fasta file from the csv table provided as supplementary material that only include gRNAs for which no NAG alternative PAM sites were detected in the yeast genome.

This notebook outputs the gRNA library file and Supplementary Figure 1
