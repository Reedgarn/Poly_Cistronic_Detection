# Poly_Cistronic_Detection

The following programs/commands can be used for the genome-wide identification of polycistronic (PC) RNA's from Nanopore direct RNA-sequencing (DRS) data. This includes the identification of PC loci containing genes in the same orientation, opposite orientations, and PC-like loci containing overlap outside of the annotated genes. 

## PC_Det
A custom R function has been made with some options to make it easier to detect the full PC loci in the same or opposite oreintations. This function comes with some additional options to allow for greater control over the final output and help with memory issues. 

Before beginning, several input files need to be generated and loaded into R. This includes a BAM file containing the alignments from Nanopore DRS libraries. Sorting is not required but strongly recommended to reduce memory consumption and time. The BAM file can be loaded into R using the readGAlignments() function from the GenomicAlignments package. 
