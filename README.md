# Netflix-Movies-and-TV-Shows-Clustering
📖 Introduction

This project aims to cluster the video content available on Netflix based on the company’s site data. Apart from aiding in the development of an efficient recommendation system, clustering the video content would also provide information about the type of content the company is interested in listing on its site. Thus giving an insight to content creators and filmmakers on the type of video content in demand.

2. EDA Summary:

The notable observations identified during EDA were:

Movies and TV Shows on Netflix are in ratio 7/3. And TV Shows have long way to catch upto the number of Movies.
Most content on Netflix is from United States followed by India and United Kingdom.
Raul Campos and Jan Suter together directed 18 movies. We can observe some other great names such as Jay Chapman, Martin Scorsese and Steven Spielberg in top 20 directors list.
International movies is the top genre followed by Dramas and Comedies.
Most movies are of length ~100 mins while most TV Shows have only one season.
Most content o Netflix is rated for mature audience only.
Love,Christmas, World, Man, Story are the top 5 most occurring words from the complete vocabulary of description.
From October to January, maximum number of movies and TV shows were added on the platform.

3. Clustering Summary:

Clusters were built on the attributes: Director, Cast, Country, Rating, Listed in (genres), Description Steps involved in preprosessing:Tokenize the corpus, Remove non-ascii characters, Convert all words to lowercase, Remove punctuation marks, Replace all numbers with its respective textual representation, Stemming and Lemmatization Text corpus was vectorized using TFIDF vectorizer, and 20000 attributes were generated. More than 80% of the variance is explained just by 4000 components. Hence to handle the curse of dimensionality, only the top 4000 components were taken, which will still be able to capture more than 80% of variance in the data.

    3.1. K Means Clustering: The optimal number of clusters were built after visualizing the elbow curve and the Silhouette score. Suing which the number of clusters for k-means clustering was taken as 4.
    3.2. Hierarchical Clustering: Clusters were built using the Agglomerative clustering algorithm, and the optimal number of clusters were built after visualizing the     dendogram. From the dendogram 6 clusters can be built. Hence the number of clusters were taken as 12. Algorithm: Agglomerative clustering Distance: Euclidean     Linkage: Ward
    
    
4. Content Based Recommender system using Cosine Similarity:

We can build a simple content based recommender system based on the similarity of the shows. If a person has watched a show on Netflix, the recommender system must be able to recommend a list of similar shows that s/he likes. To get the similarity score of the shows, we can use cosine similarity. The similarity between two vectors (A and B) is calculated by taking the dot product of the two vectors and dividing it by the magnitude. We can simply say that the CS score of two vectors increases as the angle between them decreases.

Conclusion:

In conclusion, tailored recommendations can be made based on information about movies and TV shows. In addition, similar models can be developed to provide valuable recommendations to consumers in other domains. It will solve for improved movie and TV-Show selection times with a considerable growth in satisfaction of the content being consumed leading to more user engagement and greater trust in Netflix recommendations.
