# Spring 2019 COSMOS Project
# My paper
Hot spots of DNA double-strand breaks in human rDNA units are produced in vivo 
Tchurikov, N. A. et al. Hot spots of DNA double-strand breaks in human rDNA units are produced in vivo. Sci. Rep. 6, 25866; doi: 10.1038/srep25866 (2016).
# Introduction
DNA hotspots are narrow regions of the genome that have higher recombination rates, which overlap with DNA double-strand break (DSB) regions. Recently, nine hotspots of DSBs are detected in human rDNA genes inside the intergenic spacer (IGS) in HEK293T cell lines. In this paper, the authors investigated to identify whether these hotspots are generated in vivo or in vitro by comparing the pattern of DSBs and DSB biomarkers such as H2AX and γ -H2AX. 
When DSBs are induced by endogenous or exogenous factors, H2AX becomes γ -H2AX through phosphorylation on serine 139. γ -H2AX is also used as a novel biomarker of in vivo DSBs because producing it is the very first step in recruiting and localizing DNA repair proteins. 
To investigate the nature of DSB hotspots, they used the irradiation to induce DSBs and compared profiles of DSBs, H2AX, and γ -H2AX in CD4+ resting cells and γ -H2AX in Jurkat (T-cell lymphoma culture cells). The reason why they used T lymphocytes is that they are resting cells and are not prone to replication stress. Thus, only transcriptional stress affects the profiles of H2AX and γ -H2AX. 
In figure1A, they discovered all four profiles practically coincide. Therefore, they reported active transcription is sufficient for such distribution of both H2AX and γ -H2AX marks and concluded that nine hotspots are generated in vivo only. 

# My figure

Here is a figure I want to reproduce, Figure 1B
![](https://github.com/Rosie34/COSMOS/blob/master/1.png)

Figure1B is a heatmap representing the correlation between DSB hotspots, H2AX and γ -H2AX. To test this correlation, they analyzed ChIP-Seq data sets from CD4+ T lymphocytes (irradiated or not irradiated) and Jurkat and calculated Pearson’s correlation coefficient. They confirmed that both H2AX and γ -H2AX have a strong positive correlation with DSBs. Coefficient between 0.53 and 0.64 indicates a strong positive relationship. Therefore, they reported that both H2AX (dark blue and blue) and γ -H2AX (deep green) can be used as a biomarker of DSBs.

# Methods
In this paper, all ChIP-Seq data sets were analyzed by Perl scripts to calculate the Pearson correlation matrices, and correlation heatmaps and clusters were produced from correlation matrices in packages of R. Since the paper did not share correlation matric files, a csv file was created by inserting all coefficient data, and the file was opened onto R. The heatmap.2 function from gplots was used to create a general basic heatmap. During generation, cell labels, a title, color cell labels, inside plot density, inside color legend, inside trace lines, margins, and font size were coded. The created heatmap was compared with the original figure and adjusted resolution to get the best figure. The following ChIP-Seq data were used: GSE25577(for H2AX and γ-H2AX in CD4+ and Jurkat cells); GSE49302(for profiling of DSBs in HEK293T cells). 

# Next step
I have almost done with reproducing the heatmap in R, but I still need to adjust the color key because the original figure uses more than four colors, which is difficult to reproduce. In addition, I need to output the figure as an independent PDF file. Since I am almost done with reproducing the heatmap, now I am trying to calculate Pearson correlation matrices from ChIP-Seq data sets by using Perl scripts. I am not sure whether I could use Perl scripts, but I would like to try it. I also found that Galaxy is a good tool to calculate and generate a heatmap by using ChIP-Seq data, so I will also try to use it if I have troubles to navigate the Perl scripts.



