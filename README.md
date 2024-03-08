# Using K-means and PCA for Geochemical Exploration Targeting 

## Executive Summary
- Southeast Ireland is known for its diverse geology and associated mineral deposits.
- Regional stream sediment sample data is made available by GSI, and can be interrogated to find out potential areas for LCT Pegmatite.
- By utilising K-means, we can cluster the stream sediment sample data to reflect the lithology underneath.
- Granite lithology from previous K-means iterations can then be iterated again to find out where the most fractionated magma in the granite is, in which there where the LCT Pegmatite deposits are usually concentrated.
- To further validate the potential location of anomaly of LCT Pegmatite deposits, Principal Component Analysis (PCA) can be applied using specific enriched elements in this deposits.
- It later discovered that the enriched elements in PCA relates back to the cluster made before in the Clustering analysis.
- These 2 analysis confirm the generation of new prospective areas for LCT Pegmatite, which require more detailed sampling and subsequent exploration techniques.

![Executive Summary](https://github.com/gilangbahana/geochemical-exploration-targeting/assets/89720434/d671f456-e0d1-4ca7-b393-877b69c5adf8)

## Project Workflow

![Project Workflow](https://github.com/gilangbahana/geochemical-exploration-targeting/assets/89720434/80098b29-f0c0-4439-9c5b-ef047c6972b0)

## Study Case
### K-means Clustering
1. The objective of K-means clustering is to group similar data points and to discover underlying patterns or structures in the data.
2. K-mean algorithm works by establishing a centroid point in the middle of clustered data.
3. All data points are then assigned to the nearest cluster based on their statistical similarity (association rules algorithm).

![Kmeans clustering](https://github.com/gilangbahana/geochemical-exploration-targeting/assets/89720434/ba2cb1bb-cce8-498f-83e8-8ca363788173)

### 1st Iteration of Clustering
- Clustering uses all 55 elements in the dataset. Data is transformed to minimise closure effect. 
- There are five possible clusters identified in the analysis. 
- These clusters can be validated against the regional geology to determine if they follow the expected patterns.
- The analysis reveals that the granite lithology corresponds into two separate clusters, labeled as cluster 4 and 5. 
- Further analysis is needed to identify the location of the most fractionated magma within the granite…

![1st iteration of Clustering](https://github.com/gilangbahana/geochemical-exploration-targeting/assets/89720434/49b31dbc-118c-4b13-a3b2-5870596a3ccc)

### 2nd Iteration of Clustering
- The granite cluster from previous iterations clustered again using elements indicative of highly fractionated magma, such as K/Rb, Nb/Ta, Zr/Hf, along with concentrations of Cs, Sn, and W.
- After 2nd iteration of clustering, two possible locations were identified, with the highest likelihood of containing pegmatite.
- Ballouard et al. (2016) outlined that LCT pegmatite is characterised by the ratio of K/Rb < 150, Nb/Ta < 7, Zr/Hf within the range of 28 to 47, Cs concentrations between 12 to 47 ppm, Ta < 7.5 ppm, W < 10 ppm and Sn of up to 50 ppm

![Table Pegmatite png](https://github.com/gilangbahana/geochemical-exploration-targeting/assets/89720434/247f3195-3715-49d4-ac95-b089fec63310)

![2nd Iteration of Clustering](https://github.com/gilangbahana/geochemical-exploration-targeting/assets/89720434/55b5aa86-30af-4b50-8f0c-c82fefd7e693)

### Principal Component Analysis Theory
- Consider a geochemical dataset consisting of 2 elements A and B.
  - _Trends and spatial correlation can be easily determined._
- Consider a geochemical dataset consisting of 2 elements A, B and C.
  - _Trends and spatial correlation can be determined, but not that easily._
- Consider a geochemical dataset consisting of 2 elements A, B, C and D.
  - _Trends and spatial correlation can possibly be determined, but increasingly challenging. Numerical, noise, and irrelevant data trends are introduced._
- Consider a geochemical dataset consisting of 2 elements A, B, C, D, …n:
  - _Trends and spatial correlation are challenging to visually determine as dimensions increase. Numerical, noise, spurious correlations, and irrelevant data trends are significant._
- It is essential to remove the noise, by reducing the dimension of the data, using PCA. A PCA plot converts the correlation (or the lack of) among all cells into a 2d graph.

![PCA png](https://github.com/gilangbahana/geochemical-exploration-targeting/assets/89720434/a32777c5-99a9-497b-86fb-dc37cddb1d90)

### Principal Component Analysis
- PCA uses 9 elements in total and trying to reduction the dimensionality of 9 component into 2 dimension, so it can be displayed in a simple scatter plot.
- Rb, Cs, U, Sn, Ta, and W elements are chosen as common metals enriched in pegmatite. 
- Nb, Hf, and Zr as incompatible and immobile HFSE, frequently found in both granite and pegmatite.
- Scree plot shows that only the first three PCs have eigenvalues above the threshold of one, suggesting only three of them have a significant contribution to the dataset variance.
- Cumulative percentage of influence of each PC on the overall data shows that first three principal components (PC1 to PC3) account for 75.85% of the total variance in the dataset.
- This significant portion of the dataset's variance can be effectively summarised by just these three components, while the variance explained by the remaining six components is not significant and likely due to random processes or noise.

![Scree plot](https://github.com/gilangbahana/geochemical-exploration-targeting/assets/89720434/46763420-e95d-4d10-9f11-4582f432c4a8)

![Eigenvalues table png](https://github.com/gilangbahana/geochemical-exploration-targeting/assets/89720434/106b0401-63e7-4caf-9aa2-ee7638e5e2a9)

- The eigenvector plot provide insights into how each element influences principal components.
- The influence on PC1 appears to be strongly linked to the presence of metals enriched in pegmatite deposits and is low in High Field Strength Elements (HFSE), which are typically associated with granite lithology.
- The RQ Plot combine variable-sample relationships within the context of the principal components. In these plots, samples are depicted as points, and variables are represented as vectors. 
- To put the PCA into previous clustering context, it shows from the graph that the RQ1 - RQ2 plot demonstrates elements such as Cs and Rb are positively correlated along RQ1, associated with pegmatite A cluster.
- Other metals such as Ta, Sn, and U cluster positively along RQ1 but slightly negative along RQ2, indicating pegmatite B cluster.
- HFSE elements are associated with granite characterised by negative RQ1 and RQ2.

![eigenvector plot png](https://github.com/gilangbahana/geochemical-exploration-targeting/assets/89720434/114a5d7f-4ce7-4c7b-9efa-f651d9809f56)

![PC1 PC2 graph](https://github.com/gilangbahana/geochemical-exploration-targeting/assets/89720434/ea47ee6e-813f-4a1a-85d0-2b8504933098)

## Conclusion
- Despite the relatively sparse data density, this study has demonstrated the effectiveness of utilising multi-element and advanced analytical techniques such as K-means and PCA for exploring LCT Pegmatite deposits in the region. 
- K-means and PCA analysis have highlighted areas with significant anomalies that correlate with known mineral deposits and suggest the presence of previously unidentified exploration targets.
- Subsequent detailed sampling and further exploration techniques such as geophysics and drilling are needed to test the anomaly in the area.

![Conclusion](https://github.com/gilangbahana/geochemical-exploration-targeting/assets/89720434/67f5572f-6755-4bba-8c45-9382632783a2)

### Presentation Deck

[Using K-means and PCA for Geochemical Exploration Targeting - Gilang Bahana.pdf](https://github.com/gilangbahana/geochemical-exploration-targeting/files/14543427/Using.K-means.and.PCA.for.Geochemical.Exploration.Targeting.-.Gilang.Bahana.pdf)
