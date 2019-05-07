# Methods

All FASTQ files (SRX032295, SRX032293, SRX032292, SRX032291, SRX032290, SRX032289, SRX032288) were downloaded. FASTQC was used for quality control and Trim Galore was effectively utilized to remove poor quality portions of the reads. For the alignment, Bowtie2 was used to map reads with the reference genome (U13369). Alignments were converted to BED files by the BamToBed program of the BED Tools package. BED files were opened using GenometriCorr package in R to generate DSB hot spot peak graphs. 

In addition, all ChIP-Seq data sets were analyzed by Perl scripts to calculate the Pearson correlation matrices, and correlation heatmaps and clusters were produced from correlation matrices in packages of R. Since the paper did not share correlation matric files, a csv file was created by inserting all coefficient data, and the file was opened onto R. The heatmap.2 function from gplots was used to create a general basic heatmap. During generation, cell labels, a title, color cell labels, inside plot density, inside the color legend, inside trace lines, margins, and font size were coded. The following ChIP-Seq data were used: GSE25577(for H2AX and γ-H2AX in CD4+ and Jurkat cells); GSE49302(for profiling of DSBs in HEK293T cells).

# GenometriCorr
http://genometricorr.sourceforge.net/galaxy/galaxyintegration.html

# UCSC genome browser
https://genome.ucsc.edu/
