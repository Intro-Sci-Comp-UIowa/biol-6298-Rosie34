#R script

library(gplots)
df <- data.frame(A = c(0.645, 0.894, 0.956,1), 
                 B=c(0.53, 0.901, 1, 0.956), 
                 C= c(0.585,1,0.901,0.894), 
                 D=c(1,0.585,0.53,0.645))
colnames(df) <- c("H2AXCD4+",   "γH2AX,Jurkat",   "γH2AX,Cd4+,IR",   "DSB")
rownames(df) <- c("DSB",   "γH2AX,Cd4+,IR",   "γH2AX,Jurka",   "H2AXCD4+")
df_matrix <- as.matrix(df)


mat_data<- data.matrix(df[,1:ncol(df)])


#pdf("Heatmap.pdf")

heatmap.2(df_matrix,
          cellnote = mat_data,  # same data set for cell labels
	col=bluered(75),
          main = "COSMOS project", # heat map title
          notecol="black",      # change font color of cell labels to black
          density.info="none",  # turns off density plot inside color legend
          trace="none",         # turns off trace lines inside the heat map
          margins =c(12,9),
          cexCol = 1., 
          cexRow = 1.)     # widens margins around plot

#dev.off()
