# Functions

PCA
#library(DESeq2)

plotPCA(DESeqTransform object, intgroup = "condition", ntop = 500, returnData = FALSE)
#object--> DESeqTransform object, with data in assay(x), produced for example by either rlog or varianceStabilizingTransformation.


library( pcaExplorer)
pcaplot(DESeqTransform object,intgroup = "condition", ntop = 500,
        pcX = 1, pcY = 3, title = " ",text_labels = FALSE, point_size = 2, ellipse = FALSE )

pcaplot3d(DESeqTransform object,intgroup = "condition",ntop = 1000,
          pcX = 1, pcY = 2, pcZ = 3, text_labels = FALSE, point_size = 2)
          



#Counts plot of gene + condition

library(DESeq2)
plotCounts( object DESeqDataSets, gene="", intgroup = "condition"))
geneCounts <- plotCounts(MatrixDESeqData, gene = "MAPK15", intgroup = c("cond"), returnData = TRUE)
ggplot(geneCounts, aes(x =  cond, y = count, color = cond)) +
scale_y_log10() + geom_jitter()+ labs(x= "MAPK15", y="Normalized Count") + guides(color=guide_legend("MAPK15 Alteration"))

