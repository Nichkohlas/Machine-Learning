# Machine Learning

This project explores **three core machine learning tasks** — Unsupervised Learning, Regression, and Classification — using real-world datasets from Kaggle.  
The goal was to **apply appropriate ML techniques**, analyze results, and provide actionable insights where appropriate.

---

## Project Overview

As part of this project, I completed three distinct tasks:

1. **Unsupervised Learning**  
   - **Goal:** Identify homogeneous population groups and/or perform dimension reduction.  
   - **Technique:** Clustering (K-means).
2. **Regression**  
   - **Goal:** Predict a continuous target variable using regression models.  
   - **Techniques:** Linear, Ridge & Lasso Regression.
3. **Classification**  
   - **Goal:** Classify observations into categories based on predictor variables.  
   - **Techniques:** K-Nearest Neighbors (KNN), Support Vector Machine (SVM).

---

## Datasets

- **Dataset 1 (Tasks 1 & 3):** [Link to Kaggle](#)  
  - Size: X rows × Y columns  
  - Key features: [briefly describe key variables]  

- **Dataset 2 (Task 2):** [Link to Kaggle](#)  
  - Size: X rows × Y columns  
  - Key features: [briefly describe key variables]  

---

# Results and Findings

## 1. Unsupervised Learning — Clustering

With the primary objective of **identifying homogeneous subgroups** within the dataset using an unsupervised learning approach, **K-Means clustering** was employed to group individuals based on shared characteristics such as lifestyle factors, demographics, and health information. 

This process aimed to **uncover patterns and hidden structures** in the data without relying on predefined labels.

- **Outlier Handling:**

  - During the initial dataset exploration, some entries were observed to have BMI values in an unrealistic range. While a BMI of 60 is plausible (severe obesity), values greater than 60 are extremely rare and likely due to data entry errors.
  - Because K-Means is **sensitive to outliers**, these individuals were removed from the analysis.

This preprocessing step was essential to maintain clustering robustness and ensure more meaningful population segmentation.

- **Findings**

  - **Diabetes Distribution:**
    - A majority of individuals (>80%) fell under the No Diabetes category.
    - Prediabetes represented <5%, while Diabetes accounted for around 10% of the population.
  - **Binary Variable Distribution:**
    - The presence of high blood pressure was more prevalent among individuals with diabetes and prediabetes compared to those without diabetes.
   
![Diabetes distribution plot](Dbts_Bar.png)  

*Bar charts illustrating the distribution of diabetes across variables*

  - **Optimal Clusters:**
    - The Elbow Curve indicated that K = 3 provided an optimal balance between complexity and explanatory power.

![Elbow plot](Elbow_plot.png)  

*Elbow method for determining the optimal number of clusters.*

  - **Cluster Profiles:**
    - Cluster 1: Highest average BMI (30.5) with lower Education (4.63) and Income (4.50) — representing older individuals with poorer health.
    - Cluster 2: Slightly lower BMI (29.5) with moderate Age (9.10), Education (4.28), and Income (4.67) — moderate health and socioeconomic status.
    - Cluster 3: Healthiest cluster with the lowest BMI (26.9), highest Education (5.62) and Income (7.28) — representing younger, well-educated individuals with minimal health concerns.

![Cluster summary](Cluster_Summ.png)  

*Summary of K-Means clustering results, displaying cluster sizes and key feature averages (BMI, Age, Education, Income).*

  - **Visual Patterns:**
    - The box plot of average BMI showed a decreasing trend across clusters, consistent with cluster health segmentation.
    - The bar plot of general health (GenHlth) distribution revealed a higher proportion of good health in clusters with lower BMI and higher socioeconomic status.
   
![Bar plot](Cluster_Bar.png)  

*Health distributions across clusters*

- **Strategic Recommendations**
Based on the clustering insights, tailored health campaigns are recommended for each subgroup:
   - **Cluster 1 (Priority Group)**
     - Individuals in this group exhibit poorest health indicators (highest BMI, worst mental and general health).
     - **Action:** Implement targeted health campaigns focusing on improving lifestyle habits (dietary guidance, physical activity programs) and increasing access to preventive healthcare at subsidized rates.
      - **Rationale:** Lower income levels in this group indicate that cost-effective and accessible interventions will have the most impact.
   - **Cluster 2 & 3 (Maintenance Group)**
     - These clusters show better overall health and higher education/income levels.
     - **Action:** Encourage routine health checkups, stress management programs, and disease prevention initiatives to maintain or improve current health levels.
    
By tailoring interventions to each cluster’s unique profile, health campaigns can be more impactful and resource-efficient, ultimately improving population health outcomes.

---

## 2. Regression Analysis






  
