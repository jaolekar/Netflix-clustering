# Netflix-clustering

**PROBLEM STATEMENT**

This dataset consists of tv shows and movies available on Netflix as of 2019. The dataset is collected from Flixable which is a third-party Netflix search engine. In 2018, they released an interesting report which shows that the number of TV shows on Netflix has nearly tripled since 2010. The streaming service's number of movies has decreased by more than 2,000 titles since 2010, while its number of TV shows has nearly tripled. It will be interesting to explore what all other insights can be obtained from the same dataset.

![approach](https://user-images.githubusercontent.com/112775752/210276925-7559024f-e187-4154-b3d6-379680f4b86f.png)

Approaches:-

**Step 1** - Viewing and cleaning data being the initials, we started with importing necessary libraries, mounting drive and storing data in variables for deriving meaningful insights. Next step being data analysis and visualization, where we analyzed our data distribution as univariate, bivariate and multivariate plots. Multicollinearity check was performed.

![total count](https://user-images.githubusercontent.com/112775752/210276954-3e57fb49-788f-4a77-9a73-1597dc3bda07.png)

![rating](https://user-images.githubusercontent.com/112775752/210276992-e33a8b25-d702-47d3-b648-6ed26194f2f0.png)

![year](https://user-images.githubusercontent.com/112775752/210277008-dcc6c881-2497-4ca2-abb1-64954f7bbb28.png)

![heatmap](https://user-images.githubusercontent.com/112775752/210277033-e4b3c839-67b6-4eb5-84b7-dbd7b0b08a48.png)

**Step 2** - We performed 3 hypothesis testing one comparing means for two variavles using T-test , second was asssociation of target age and country using chi_square test, last was asssociation of target age and duration using chi_square test.


**Step 3** - Presence of null values would have created possible errors in the further steps, so we replaced few values with null, few with the word "unknown" few were dropped.


**Step 4** - As a part of feature engineering we have done textual data processing which includes:expand contraction, lower casing, removing punctuations and stopwords, normalization,and vectoriztion. We performed data scaling using standardscalar, and dimensionality reduction using PCA.


**Step 5** - Last step was to perform clustering using different algorithms, we tried K-Means, ElbowCurve, DBSCAN, Dendogram, Agglomerative Clustering. Recommendation system function was also developed.

### Conclusion of EDA:
* Netflix have ~70% of movies and 30% of TV_shows in 2019.
* Comedy is most popular genre in Netflix, across all content.
* Netflix focuses to add new content majorly towards end of current year and start of new year.
* A sudden drop was obserbed after 2020 in count of new content, Which is because of covid pandemic.
* India is on 2nd place as compared to content availability, maximum content is available for United states.
* There are almost ~30% of netflix original movies and ~50 % TV-shows.
* Content category and countries:
  * Maximum adult content is from Spain.
  * Maximum teen content is from India.
  * Maximum older kids content is from Japan.
  * Maximum kids content is from Canada.
* All of this insights will be neccesary for business development and SWOT analysis.


### Conclusion for clustering.
* We tried 5 models for ML i.e.
  * K-means clustering 
  * Elbow curve
  * DBSCAN
  * Hierarchical clustering
  * Agglomerative clustering

* K-means clustering shows that '4' will be optimum no of clusters with the silhoutte score of 0.45. But we selected Optimum cluster number as 6 after Elbow curve cross validation.

* Thus K-means clustering will be best for this data set.
* Cosine based recommender system was working really well.


