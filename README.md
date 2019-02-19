# Spring 2019 COSMOS Project
Hot spots of DNA double-strand breaks in human rDNA units are produced in vivo 
Tchurikov, N. A. et al. Hot spots of DNA double-strand breaks in human rDNA units are produced in vivo. Sci. Rep. 6, 25866; doi: 10.1038/srep25866 (2016).
Recently, nine hot spots of double-strand breaks (DSBs) are detected in human rDNA genes inside the intergenic spacer (IGS) in HEK293T cell lines. In this paper, the authors investigated to identify whether these hot spots are generated in vivo or in vitro by comparing the pattern of DSBs and DSBs biomarkers. When phosphorylation on serine 139, H2AX is called γ -H2AX and it is used as a novel biomarker of DNA damage especially in vivo DSBs because it is the first step in recruiting and localizing DNA repair proteins. In this paper, they discovered the pattern of these nine hot spots coincides with the profiles of H2AX or γ -H2AX. Thus, they reported that nine hot spots are generated in vivo only. 
Here is a figure I want to reproduce, Figure 1B
 
Figure 1B is a heatmap indicating the correlation between DSB hot spots, H2AX, and γ -H2AX. To test this correlation, they used three different cells which are CD4+ T lymphocytes (irradiated or not irradiated) and Jurkat (T-cell lymphoma culture cells). The reason why they used T lymphocytes is that they are resting cells and are not prone to replication stress. Thus, only transcriptional stress affects the profiles of H2AX and γ -H2AX. Since it is recently shown that not only γ -H2AX but also H2AX is strongly associated with DSBs, they confirmed that both H2AX and γ -H2AX have a strong positive correlation with DSBs by showing a Pearson’s correlation. Coefficient between 0.53 and 0.64 indicates a strong positive relationship. Based on this heatmap, they reported that both H2AX (dark blue and blue) and γ -H2AX (deep green) can be used as a biomarker of DSBs. Additionally, they showed that the pattern of DSBs and the profiles of H2AX and γ -H2AX are the same in figure 1A. Therefore, they concluded that these nine hot spots are the result of in vivo DNA breakage.
To reproduce this figure,
1.	Make an excel file by inserting all coefficient data
2.	Open the excel file onto R and generate basic heatmap
3.	Generate color range from 0 (blue) to 1 (red) to indicate coefficient
4.	Insert each coefficient value
5.	Compare the figure I reproduce with the original figure
6.	Adjust resolution to get the best figure and output the figure
In addition, they shared all their ChIP-Seq data in NCBI database, I will try to use them to calculate Pearson’s coefficient if I have more time to invest.
Here is the ChIP-Seq data they shared, and I can download all of them from GEO database.
The following ChIP-Seq data were used: 
•	wgEncodeEH002022 (for TCF7L2 in HEK293 cells)
•	wgEncodeEH001779 (for KAP1 in HEK293 cells)
•	GSE25577 (for H2AX and γ-H2AX in CD4+ and Jurkat cells)
•	GSM776558 (for GATA3 in Th1 cells)
•	GSM776557 (for T-bet in Th1 cells)
•	GSE74954 (for PARP1 in HEK293T cells)



