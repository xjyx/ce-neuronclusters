# Seurat clustering and ploting scrpits used in the article "Combining single-cell RNA-sequencing with a molecular atlas unveils new markers for Caenorhabditis elegans neuron classes".

Authors: Ramiro Lorenzo, Michiho Onizuka,Matthieu Defrance, Patrick Laurent

Datasets used for the analysis are in Datasets folder.

Doublet analysis scripts and results are in DoubletAnalysis folder.

The scripts are organized as the workflow clustering analysis.

1-FirstClusterScreening:
Clustering screening the dataset using Seurat by changing PCA dimensions (between 40 adn 100) and resolution (from 1 to 8) used for louvain clustering.

2-PlotBestFirstClustering:
Plot Tsne space and boxplots corresponding to each cluster using best paramters obtained from 1-FirstClusterScreening

3-SecondIterationClusterScreening:
Second round of clustering on the 64 parent clusters obtained in 2-PlotBestFirstClustering. Single-cell profiles
coming from parent clusters were independently re-clustered. Multiple re-clustering trials were generated for resolution values from 0.1 to 3 and for PCs values from 3 to 92.

4-PlotBestSecondSubClustering:
Single UMAP space plot for each individual clusters and refinement of clusters by manual curation.

5-ThirdIterationClusterScreening:
Third round of clustering on the 8.0, 10.0 and 10.1 parent clusters obtained in 4-PlotBestSecondSubClustering. Single-cell profiles
coming from parent clusters were independently re-clustered. Multiple re-clustering trials were generated for resolution values from 0.1 to 3 and for PCs values from 3 to 92.

6-PlotBestThirdSubClustering:
Single UMAP space plot for each individual clusters and refinement of clusters by manual curation.

7-FinalPlotAndClusteringMarkers:
Final results plots, expression and markers analysis.

8-DoubletAnalysis:
Analysis of cell doublets using DoubletFinder

9-Psudotime:
Psudotime analysis of clusters 0_2, 3, 4 and 42.1-56

10-ClusteringComparison:
Cluster wise comparison against Cao where only cell names were compared and Packer where marker genes were compared between clusters

Datasets:
Folder containing datasets used for the iterative clustering procedures