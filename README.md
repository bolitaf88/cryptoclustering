# cryptoclustering



## Cryptocurrency Clustering

### Introduction

Cryptocurrency clustering involves the grouping of digital currencies based on similar characteristics or behaviors. This process aids in identifying patterns, trends, and relationships within the vast and dynamic crypto market. Clustering techniques, such as KMeans and PCA (Principal Component Analysis), help organize cryptocurrencies into meaningful groups, enabling deeper insights and more informed decision-making.

### Elbow Curves: KMeans vs. PCA

The provided code generates composite plots to contrast two essential aspects of clustering analysis:

#### Elbow Curves

```python
elbow_df1.hvplot.line(x='k', y='inertia', xticks=k, title='Elbow Curve 1: KMeans') + elbow_df2.hvplot.line(x='k', y='inertia', xticks=k, title='Elbow Curve 2: PCA')
```

- **Elbow Curve 1 (KMeans):** Demonstrates the inertia (within-cluster sum of squares) for different values of 'k' (number of clusters) in KMeans clustering.
- **Elbow Curve 2 (PCA):** Illustrates a similar curve for PCA, displaying variance explained by different numbers of principal components.
##### Elbow curve 1 and 2 illustration below
[elbowcurves](https://github.com/bolitaf88/cryptoclustering/blob/main/images/elbow.png)
[elobow1](https://github.com/bolitaf88/cryptoclustering/blob/main/images/Screenshot%202023-11-27%20060215.png)
[elbow2](https://github.com/bolitaf88/cryptoclustering/blob/main/images/Screenshot%202023-11-27%20060445.png)
### Contrasting Clusters

#### Scatter Plots

```python
scaled_df_predictions.hvplot.scatter(x='price_change_percentage_24h', y='price_change_percentage_7d', by='k_predictions', hover_cols='coin_id', title='KMeans Scatter Plot') + k_predictions.hvplot.scatter(x='PCA1', y='PCA2', by='k_predictions', hover_cols='coin_id', title='PCA Scatter Plot')
```

- **KMeans Scatter Plot:** Visualizes cryptocurrency clusters based on their 24-hour and 7-day price change percentages, highlighting different clusters identified by the 'k_predictions' label.
- **PCA Scatter Plot:** Depicts clusters generated through PCA transformation (PCA1 and PCA2), showcasing potential groupings based on principal components.
##### scatter plots illustration below
[scatterplots](https://github.com/bolitaf88/cryptoclustering/blob/main/images/scatter.png)
### Conclusion

Cryptocurrency clustering, as demonstrated through these visualizations and techniques, offers a structured approach to understanding the crypto market's complexity. Elbow curves provide insights into the optimal number of clusters, while scatter plots reveal how cryptocurrencies are grouped based on different attributes or transformations.

Through clustering, investors, analysts, and enthusiasts can gain a clearer perspective on crypto behaviors, potential correlations, and distinct market segments, aiding in strategic decision-making within this rapidly evolving landscape.

