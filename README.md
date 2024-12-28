# Machine Learning Final Project: CommonLit - Evaluating Student Summaries

## Overview

This repository contains the final project for a Machine Learning course, focused on evaluating student summaries using the **CommonLit - Evaluate Student Summaries** dataset from Kaggle. The project involves extensive exploratory data analysis (EDA), feature engineering, and predictive modeling to assess the quality of student summaries based on content and wording scores.

---

## Project Components

### 1. Exploratory Data Analysis (EDA)
- **Dataset Description:**
  - Features include student summaries, prompts, and associated scores for content and wording.
  - Data preprocessing steps include mining numerical features (e.g., word counts, syllables, readability scores) and calculating commonality metrics between summaries and prompts.
- **Visualization Techniques:**
  - Histograms for score distributions.
  - Scatter plots for feature correlations.
  - Heatmaps and pair plots for identifying linear and non-linear relationships.
  - Log-odds ratio analysis to determine word associations with good or bad summaries.

### 2. Key Insights
- **Score Correlations:**
  - Content and wording scores exhibit a linear relationship.
  - Wording scores are multimodal, indicating subgroup influences, while content scores are unimodal.
- **Feature Correlations:**
  - Strong correlation (\(r = 0.71\)) between readability scores and average word length, with a logarithmic trend.
- **Prompt Analysis:**
  - Most prompts have low scores, except "The Third Wave," which scored exceptionally high.

### 3. Predictive Modeling
Three models were developed to predict content and wording scores:
1. **Model 0:** Linear regression with five features, no normalization.
   - MSE: Content = 0.3089, Wording = 0.4820
2. **Model 1:** Linear regression with all features and normalization using `StandardScaler`.
   - MSE: Content = 0.2952, Wording = 0.4541
3. **Model 2:** Random forest regression with all normalized features.
   - MSE: Content = 0.2034, Wording = 0.3748
- **Observations:**
  - Random forest significantly outperformed linear regression models, reducing MSE by 0.0918 (content) and 0.0794 (wording).

---

## Key Methods and Tools
- **Feature Engineering:** 
  - Extracted features include word counts, sentence counts, readability scores, and commonality metrics.
- **Modeling Techniques:** 
  - Linear regression for baseline comparisons.
  - Random forest for handling non-linear relationships and avoiding overfitting.
- **Libraries Used:**
  - `scikit-learn`
  - `pandas`
  - `matplotlib`
  - `seaborn`

---

## Notebooks and Documentation
1. **`final_project_template.ipynb`**: Code and results for EDA and modeling.
2. **`ML_Writeup.pdf`**: Detailed analysis and discussion of the project outcomes.

---

## Conclusion
This project demonstrates the application of machine learning techniques to evaluate student summaries effectively. By leveraging advanced preprocessing and predictive modeling, significant insights were gained into the dataset, and random forest regression was identified as the best approach for predicting content and wording scores.

---

## Questions?
For further information or inquiries, feel free to reach out.
