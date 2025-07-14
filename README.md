# Poly_Cistronic_Detection

The programs/commands contained within this repo are related to our paper (link) and can be used for the genome-wide identification of polycistronic (PC) RNA's from Nanopore direct RNA-sequencing (DRS) data. This includes the identification of PC loci containing genes in the same orientation, opposite orientations, and PC-like loci containing overlap outside of the annotated genes. 

This repo contains multiple scripts/documents that serve various purposes. The Script1 document contains the necessary R libraries and our custom R function that can be used to identify PC reads and loci. An additional script is provided, Script2, which provides users with an example of how this program can be used. The Script3 document contains the necessarry R libraries and commands to identify the PC-like reads and associated loci. Lastly, the README.md (this document) contains a brief overview of this repo and associated files, an overview of both the PC_Det function and the PC-like detection script, and a discussion of the particular options used in our paper.


## PC_Det
A custom R function has been made with some options to make it easier to detect the full PC loci in the same or opposite oreintations. This function comes with some additional options to allow for greater control over the final output and help with memory issues. 

Before beginning, several input files need to be generated and loaded into R. This includes a BAM file containing the alignments from Nanopore DRS libraries. Sorting is not required but strongly recommended to reduce memory consumption and time. The BAM file can be loaded into R using the readGAlignments() function from the GenomicAlignments package. 
