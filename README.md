# Spring 2019 COSMOS Project
# My paper
Hot spots of DNA double-strand breaks in human rDNA units are produced in vivo 
Tchurikov, N. A. et al. Hot spots of DNA double-strand breaks in human rDNA units are produced in vivo. Sci. Rep. 6, 25866; doi: 10.1038/srep25866 (2016).
# Introduction
DNA hotspots are narrow regions of the genome that have higher recombination rates, which overlap with DNA double-strand break (DSB) regions. Recently, nine hotspots of DSBs are detected in human rDNA genes in HEK293T cell lines. When DSBs are induced by endogenous or exogenous factors, H2AX becomes γ -H2AX through phosphorylation on serine 139. Thus, γ -H2AX is widely used as a novel biomarker of in vivo DSBs because this histone modification is the very first step in recruiting and localizing DNA repair proteins. 
In this paper, the authors investigated to identify whether these hotspots are generated in vivo or in vitro by comparing the pattern of DSBs and DSB biomarkers such as H2AX and γ -H2AX. To investigate the nature of DSB hotspots, they used the irradiation (IR) to induce DSBs and compared profiles of DSBs, H2AX, and γ -H2AX in CD4+ resting cells and γ -H2AX in Jurkat (T-cell lymphoma culture cells). The reason why they used T lymphocytes is that they are resting cells and are not prone to replication stress. Thus, only transcriptional stress affects the profiles of H2AX and γ -H2AX. 


# My figure

Here is a figure I want to reproduce, Figure 1B
![](https://github.com/Rosie34/COSMOS/blob/master/1.png)

Figure1B is a heatmap representing the correlation between DSB hotspots, H2AX and γ -H2AX. To test this correlation, they analyzed ChIP-Seq data sets from CD4+ T lymphocytes (irradiated or not irradiated) and Jurkat and calculated Pearson’s correlation coefficient. They confirmed that both H2AX and γ -H2AX have a strong positive correlation with DSBs. Coefficient between 0.53 and 0.64 indicates a strong positive relationship. Therefore, they reported that both H2AX (dark blue and blue) and γ -H2AX (deep green) can be used as a biomarker of DSBs.

# Methods
All FASTQ files (SRX032295, SRX032293, SRX032292, SRX032291, SRX032290, SRX032289, SRX032288) were downloaded. FASTQC was used for quality control and Trim Galore was effectively utilized to remove poor quality portions of the reads. For the alignment, Bowtie2 was used to map reads with the reference genome (U13369). Alignments were converted to BED files by the BamToBed program of the BED Tools package. BED files were opened using GenometriCorr package in R to generate DSB hot spot peak graphs. 

In addition, all ChIP-Seq data sets were analyzed by Perl scripts to calculate the Pearson correlation matrices, and correlation heatmaps and clusters were produced from correlation matrices in packages of R. Since the paper did not share correlation matric files, a csv file was created by inserting all coefficient data, and the file was opened onto R. The heatmap.2 function from gplots was used to create a general basic heatmap. During generation, cell labels, a title, color cell labels, inside plot density, inside the color legend, inside trace lines, margins, and font size were coded. The following ChIP-Seq data were used: GSE25577(for H2AX and γ-H2AX in CD4+ and Jurkat cells); GSE49302(for profiling of DSBs in HEK293T cells).



