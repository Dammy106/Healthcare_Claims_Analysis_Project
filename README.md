# Healthcare Claims Analysis Project
Using Unsupervised Learning to analyze healthcare claims data
## Project Overview
This project focuses on analyzing healthcare claims data to uncover trends and patterns related to healthcare costs and demographic factors. It includes exploratory data analysis (EDA), feature engineering, and customer segmentation using clustering techniques like K-means. The analysis provides insights into how various factors like smoking, BMI, and age impact claim amounts.

## Dataset
The dataset used for this analysis contains demographic and health-related information such as age, gender, BMI, smoker status, and regional data. It also includes claims amounts, which serve as the primary variable of interest.

- **Features include:**
  - `age`, `bmi`, `children`, `smoker`, `gender`, `region`
  - Closest Target variable: `log_claim` (log-transformed claim amounts)

## Analysis Process
### 1. Exploratory Data Analysis (EDA)
Explored the dataset with the following techniques:
- **Scatter plots** and **trend lines** to investigate relationships (e.g., BMI vs. Claims).
- **Countplots** for gender, diabetes status, and smoking prevalence.

### 2. Feature Engineering
Several new features were created to enhance the model’s predictive power:
- **Age Groups**: Grouped into categories like `Young`, `Middle-Aged`, and `Senior`.
- **BMI Groups**: Classified into `Normal`, `Overweight`, and `Obese`.
- Log-transformation of `claim` amounts to reduce skewness.

### 3. Clustering
K-means clustering was performed on the data to segment customers based on their claim patterns. We used the **elbow method** to determine the optimal number of clusters (4 clusters).

### 4. Insights from Clustering
- Cluster 3 has the highest average claim amounts, and it is heavily populated by smokers.
- Cluster 1 includes individuals with children but has the second-lowest claim amounts.
- Non-smokers tend to have lower claims but exhibit higher variability.

## Key Findings
- **Smoking status** plays a significant role in healthcare costs, with smokers having higher average claim amounts.
- **BMI** and **age** also correlate with claim amounts, with higher BMIs leading to higher claims.
- Clustering analysis revealed distinct groups of individuals with varying healthcare claim behaviors.

## How to Run the Project
### Prerequisites
To run this analysis, you need the following libraries:
- `pandas`
- `numpy`
- `matplotlib`
- `seaborn`
- `scikit-learn`

## Visualizations
- Scatter plots showing the relationship between BMI and claim amounts.
- Box plots for claim distribution across smokers and non-smokers.
- Clustering visualizations to highlight customer segments.

## Conclusion
This analysis sheds light on the impact of smoking, BMI, and age on healthcare costs. Clustering helped identify different customer segments, providing a foundation for more targeted healthcare policies or interventions.
