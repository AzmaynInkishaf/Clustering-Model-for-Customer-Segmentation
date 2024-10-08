# Clustering Model for Customer Segmentation

## Introduction
The global commerce industry is projected to reach $6.3 trillion and there is substantial competition within the market. Understanding the distinct customer segments is crucial for businesses to tailor their marketing strategies for enhancing customer engagement. Machine learning algorithms plays a pivotal function in this process by enabling the analysis of complex datasets to uncover patterns that traditional methods might overlook. This project focuses on creating a clustering model to segment customers effectively and aiming to provide actionable insights for targeted marketing. The approach involves using a customer instance dataset to visualize patterns and create distinct groups of individuals based on their characteristics.

## Dataset
The dataset utilized in this project is the Customer Information Dataset which is available on the Kaggle Dataset Repository. It comprises 200 customer instances and 5 distinct features representing various individual attributes. Four of these features are numerical variables which are identification, age, income, and spending score. One of the feature is categorical which is gender. This dataset covers a wide range of customers across various age groups, different income brackets and diverse spending habits. Notably, the spending score reflects the relative amount spent rather than their total expenditure of the customer which offers a nuanced perspective of customer behavior and allowing for more detailed segmentation analysis.

## Exploration

<p align="center"><img src="https://github.com/user-attachments/assets/597dacea-3caf-43fe-bec3-544a400bc7f6" alt="1" style="width: 800px; height: 500px;"></p>

The diagram above displays the gender distribution in age group. Targeted advertisement strategies are significantly influenced by the gender and age of the audience. It should be considered that majority of the customers are young adults and there are more females than males.

<p align="center"><img src="https://github.com/user-attachments/assets/b9d040fb-9dc4-4e6d-81d1-7f1c120ca38a" alt="2" style="width: 800px; height: 500px;"></p>

The diagram above displays the outliers values within individual features. Outlier values can cause biased prediction and must be removed before training models. The dataset contains a single outlier in the income feature which is not expected to significantly mislead the results.

<p align="center"><img src="https://github.com/user-attachments/assets/df58dc4e-708f-4518-a778-a405d8761194" alt="3" style="width: 800px; height: 500px;"></p>

The diagram above displays the variable distribution of individual features. Checking the distribution in dataset is crucial for understanding data characteristics, identifying potential bias and ensuring model effectiveness. The features in this dataset are normally distributed.

<p align="center"><img src="https://github.com/user-attachments/assets/2001159e-c6b1-425b-840a-cfd85ff2d23f" alt="4" style="width: 800px; height: 500px;"></p>

The diagram above displays the bivariate analysis of individual features. Bivariate analysis is crucial for understanding the relationship between two variables and can reveal pattern not visible in dataset. There are clear groups that suggest income bracket influence spending habit.

<p align="center"><img src="https://github.com/user-attachments/assets/1ccb9a4b-b8c4-4b34-8caf-649ca7483e7c" alt="5" style="width: 800px; height: 500px;"></p>

The diagram above displays the correlation between the various features. Features with strong relation can cause overfitting and this can be fixed during feature selection. This reveals a negative relationship between age of customer and spending on products.

## Modeling

<p align="center"><img src="https://github.com/user-attachments/assets/8b561aaa-1dad-4d30-89e6-4f808c1377f2" alt="6" style="width: 800px; height: 500px;"></p>

The diagram above represents the elbow method for finding clusters. The elbow method helps find the optimal number of clusters by identifying where the plot of within-cluster variance levels. The inflection point indicating a significant change in the slope occurs at five clusters.

<p align="center"><img src="https://github.com/user-attachments/assets/c7eebc4d-24c6-4aa3-81fc-8c1d4f45ced0" alt="7" style="width: 800px; height: 500px;"></p>

The diagram above represents the silhouette method for finding clusters. The silhouette method assesses clustering quality by comparing how similar points are to their own cluster versus other clusters. The score reaches its maximum at five clusters which suggests this as the optimal number of clusters.

<p align="center"><img src="https://github.com/user-attachments/assets/23e9ff19-e901-4c81-9142-6378819a92ba" alt="8" style="width: 800px; height: 500px;"></p>

The diagram above represents the five clusters of customer groups. Clusters are defined by income versus spending. Group 0 is mid-income mid-spending, Group 1 is high-income high-spending, Group 2 is low-income high-spending, Group 3 is high-income low-spending, and Group 4 is low-income low-spending.

<p align="center"><img src="https://github.com/user-attachments/assets/5810155a-9d3e-4176-b66f-e1e595dd5b4e" alt="9" style="width: 800px; height: 500px;"></p>

The diagram above represents the customer number in each cluster. This assist in visualizing how the observed customer are distributed according to their spending habits. Most of the customer belong to cluster 0 which is the mid-income mid-spending group of people.

<p align="center"><img src="https://github.com/user-attachments/assets/5fbd1027-b63d-46ba-97dd-5d776f0f6232" alt="10" style="width: 800px; height: 500px;"></p>

The diagram above represents the gender count in individual cluster. This allows for a detailed understanding of the customers demographics within each group. There are more females than males in every cluster except cluster 3 which is the high-income low spending group.

## Conclusion

The project demonstrates the effectiveness of machine learning model in customer segmentation for targeted advertisement. Based on the analysis, it is recommended to prioritize targeting customers in Cluster 0, the mid-income mid-spending customers, due to their largest representation. Cluster 1, high-income high-spending customers, should be considered as a secondary target due to their significant purchasing potential. Cluster 3,high-income low-spending customers, warrants further investigation to develop strategies to increase their engagement. For advertising strategies, it is essential to consider that the predominant demographic consists of female customers aged between 20 and 50, which should guide the tailoring of marketing messages to effectively reach this specific group.
