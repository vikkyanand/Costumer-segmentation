# Costumer-segmentation
1.	Abstract

Customer segmentation is a crucial aspect of marketing strategies, enabling businesses to better understand their customers and tailor their approaches to meet their needs effectively. This report presents a study on customer segmentation using k-means clustering, a popular unsupervised machine learning algorithm.

2.	Table of Contents

•	Abstract
•	Introduction
•	Existing Method
•	Proposed Method with Architecture
•	Methodology
•	Implementation
•	Conclusion

3.	 Introduction 

The mall industry has become increasingly competitive, necessitating a deeper understanding of customer behavior and preferences. Customer segmentation is a crucial aspect of marketing strategies to offer personalized experiences and targeted promotions. In this report, we explore the utilization of unsupervised learning techniques, specifically the k-means algorithm, to segment mall customers based on their demographic characteristics and shopping patterns. This report aims to present the proposed method, discuss its implementation, and analyze the obtained customer segments to provide actionable insights for mall owners and marketers.



4.	Existing Method

The existing methods for customer segmentation typically involve manual categorization based on demographic, geographic, or psychographic attributes. While these methods can provide some insights, they often lack precision and fail to capture the underlying patterns and relationships within the data. Moreover, manual segmentation can be subjective and time-consuming and not scale well with large datasets. Therefore, there is a need for an improved method that can overcome these limitations and provide more accurate and meaningful customer segments.


5.	 Proposed method with Architecture

Our proposed method utilizes unsupervised learning using k-means algorithm for customer segmentation. The k-means algorithm is chosen due to its simplicity, scalability, and effectiveness in clustering tasks. k-means clustering algorithm automates the process by grouping customers based on similarities in their data attributes. This allows for a more objective and data-driven segmentation approach. The architecture of the proposed method involves several steps: data preparation, feature selection, data scaling, determination of the optimal number of clusters, and applying the k-means algorithm to obtain customer segments. Figure 1 illustrates the flowchart of the proposed method.

6.	Methodology

Data Preprocessing and feature engineering

•	Check missing values- Missing values can lead to errors in your code, and can cause models to fail or be inaccurate
•	Detect and remove outliers- Outliers are data points that have extreme values and they do not conform with the majority of the data. It is important to address this because outliers tend to skew our data towards extremes and can cause inaccurate model predictions. 
•	Skewness Correction- Skewness is a serious issue and may be the reason of bad performance of the model.  We have to reduce or remove Skewness to achieve good accuracy.
•	Scaling- Scaling the data can help to balance the impact of all variables on the distance calculation and can help to improve the performance of the algorithm. 

Determination of Optimal Number of Clusters:

•	To use K-means model, we need to know how many clusters are in the dataset. There are several ways to select the correct number of clusters, they are all based in the amount of insight we get from each cluster. It isn't useful to find a lot of clusters if we cannot interpret them, or gain nothing by separating them into different categories. The number of clusters is an input to the model, but we cannot determine the number of clusters beforehand. So, a good approximation is using use the elbow method and silhouette diagram 

•	Elbow method ->The elbow method involves plotting the within-cluster sum of squares (WCSS) against the number of clusters. The 'elbow' point represents a trade-off between cluster complexity variance explained.

•	Silhouette diagrams ->Silhouette diagrams incorporate more information than the elbow plot. Each "blade" on the diagram represents a separate cluster. Height of blades represents number of samples inside of the cluster and width represents strength of inter-cluster connections. Our goal will be to find clusters of near the same size which are strongly connected.

Training Clustering Models on Dataset

We will use K-Means clustering for customer segmentation.
K-means clustering is an unsupervised machine learning algorithm for clustering ‘n’ observations into ‘k’ clusters where k is predefined or user-defined constant. The main idea is to define k centroids, one for each cluster.

The K-Means algorithm involves:
•	Choosing the number of clusters "k".
•	Randomly assign each point to a cluster
•	Until clusters stop changing, repeat the following:
•	For each cluster, compute the cluster centroid by taking the mean vector of points in the cluster.
•	Assign each data point to the cluster for which the centroid is the closest.
  
7.	 Implementation

The proposed method was implemented using Python programming language (Version- 3.10.12), along with several libraries including Pandas, NumPy, SciPy, and scikit-learn. These libraries provided the necessary functionalities for data manipulation, numerical operations, and the k-means clustering algorithm.

Used libraries and their version

Pandas-> 1.5.3
NumPy -> 1.22.4
Matplotlib -> 3.7.1
Seaborn -> 0.12.2
SciPy -> 1.10.1
Plotly -> 5.13.1
Sklearn -> 1.2.2

The implementation can be outlined as follows:

•	Import the required libraries, including Pandas, NumPy, SciPy, and scikit-learn.
•	Load the customer data into a Pandas DataFrame for further processing and analysis.
•	Preprocess the data by handling missing values, outliers, Skewness Correction, and performing necessary data transformations.
•	Select the relevant features from the dataset that will be used for customer segmentation.
•	Determine the Optimal Number of Clusters using the elbow method and silhouette diagram.
•	Initialize the k-means clustering algorithm from the sklearn library, specifying the desired number of clusters.
•	Fit the customer data to the k-means model using the fit () method, which performs the clustering based on the specified features.
•	Retrieve the cluster assignments for each customer using the predict () method.
•	Interpret the resulting segments based on the cluster characteristics, such as Annual Income and Spending Score.
•	Assign labels to the clusters based on the interpretations.

8.	  Conclusion

In conclusion, the customer segmentation analysis using k-means clustering identified distinct customer segments in the shopping mall dataset. These segments include high-income meagre lifestyle, low-income meagre lifestyle, average-income average lifestyle, high-income lavish lifestyle, and low-income lavish lifestyle. Tailoring marketing strategies to these segments can lead to personalized experiences and increased customer satisfaction, driving business growth in the competitive mall industry. Leveraging k-means clustering and customer segmentation enables to make informed decisions and create meaningful connections with their customers, fostering loyalty and staying ahead in the retail landscape.

