# AIRLINE CUSTOMERS SEGMENTATION

## Background 
The objective of this project is to segment airline customers based on various existing features. This segmentation can provide valuable insights for various purposes, such as targeted marketing, service customization, or understanding customer behavior.

## Dataset
Disclaimer: This dataset was obtained from Kaggle with the following link: [Customer Segmentation Data](https://www.kaggle.com/competitions/sa-customer-segmentation/data).
Please note that due to the absence of metadata for this dataset, my understanding of the variable descriptions is limited and relies solely on personal assumptions.

## Objective

The primary goal of this project is to employ RFM (Recency, Frequency, Monetary) analysis for customer segmentation. The specific objectives include:

1. **Identifying Clustering Criteria:** Utilizing RFM analysis to define clustering criteria based on the recency of customer activity, the frequency of flights taken, and the monetary value represented by fares spent.

2. **Evaluation with Silhouette Score:** Assessing the quality of the clustering results using the silhouette score as an evaluation metric. The silhouette score provides a measure of how well-defined the clusters are within the dataset.

3. **Tools and Libraries:** Implementing the analysis using Jupyter Notebook and various Python libraries, including pandas, matplotlib, seaborn, scikit-learn, and yellowbrick.

4. **Providing Insights:** Interpreting the clustering results and providing meaningful insights into the identified customer segments, including the characteristics and behaviors associated with each segment.

## Clustering Criteria
RFM (Recency, Frequency, Monetary) analysis is used to determine clustering criteria.
The following variables represent RFM:

- Recency (R): last_to_end - The time elapsed from the last flight to the most recent flight order can represent how recently the customer last made a purchase.
- Frequency (F): flight_count - The number of flights taken by a customer is an indicator of how often they use flight services.
- Monetary (M): fare_sum - The amount of money customers spend in the first and second year after their first flight can reflect how much of a financial impact they have on your business.

## Evaluation Metric
Silhouette score is a metric used to calculate the goodness of a clustering technique. It measures how well-defined the clusters are within the data. The silhouette score ranges from -1 to 1, where a higher score indicates better-defined clusters. Specifically, for each data point, the silhouette score is calculated as (b - a) / max(a, b), where 'a' is the average distance from the data point to other points in the same cluster, and 'b' is the average distance from the data point to points in the nearest cluster. A higher silhouette score suggests that the object is well matched to its own cluster and poorly matched to neighboring clusters.

## Tools
- Jupyter Notebook

## Libraries
- pandas
- matplotlib
- seaborn
- scikit-learn
- yellowbrick

## Clustering Result
### Best Number of Clusters
4 clusters with a silhouette score of 0.48 and a silhouette coefficient above 0.55.

### Cluster Descriptions
1. VIP Tier (Highest Tier): Cluster 0
   - This cluster exhibits a high level of engagement.
   - Takes a significant number of flights.
   - Spends a substantial amount on fares.
   - Has been a member for a long time.
   Therefore, Cluster 0 can be considered as the VIP tier.

2. Premium Tier: Cluster 2
   - This cluster also demonstrates a good level of engagement and activity.
   - While not as high as Cluster 0, they still engage well with the services.
   - Have a decent flight count and spend a considerable amount on fares.
   - Have been members for a moderate duration, making them a strong customer segment.

3. Standard Tier: Cluster 3
   - This cluster shows moderate levels of engagement, flight activity, and spending power.
   - They have a reasonable membership duration but not as long as the VIP and Premium tiers.
   Therefore, Cluster 3 can be considered as the Standard tier.

4. Basic Tier (Lowest Tier): Cluster 1
   - This cluster has the lowest level of engagement, with the longest time since their last flight.
   - They take fewer flights and spend less on fares.
   - Their membership duration is relatively short compared to the other clusters, indicating less active participation.
   Therefore, Cluster 1 can be considered as the Basic tier.
