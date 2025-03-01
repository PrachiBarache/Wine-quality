# Wine Quality Prediction Using Machine Learning

## Project Overview
This project explores different machine learning algorithms to predict wine quality based on physicochemical properties. Traditional wine quality assessment is an expensive and time-consuming process that requires human expertise. This project aims to develop a data-driven approach that is both cost-effective and accurate.

The model achieved a maximum accuracy of **94.65%** using the Random Forest classifier, demonstrating the effectiveness of machine learning in predicting wine quality.

## Dataset
The analysis uses the [Wine Quality Dataset](https://archive.ics.uci.edu/ml/datasets/wine+quality) from UCI, which consists of variants of Portuguese "vinho verde" wine. The dataset includes:
- 4,896 instances
- 11 input features (physicochemical properties)
- Quality ratings ranging from 3 (very bad) to 8 (excellent)

### Features
- Fixed acidity
- Volatile acidity
- Citric acid
- Residual sugar
- Chlorides
- Free sulfur dioxide
- Total sulfur dioxide
- Density
- pH
- Sulphates
- Alcohol percentage

## Analytical Questions
The project addresses the following key questions:
1. Which chemical characteristics are the strongest predictors of wine quality?
2. How accurately can machine learning models predict wine quality, and which model performs best?
3. What are the differences in model performance when predicting high-quality versus low-quality wines?
4. Is there a significant difference in prediction performance for different quality levels (good vs. bad) in the wine dataset?

## Methodology
1. **Data Preprocessing**
   - Data cleaning and validation
   - Feature exploration and correlation analysis
   - Binarization of the target variable (quality > 7 = "high quality", quality <= 7 = "low quality")
   - Dataset split (70% training, 30% testing)

2. **Model Development**
   - Baseline model: DummyClassifier
   - Logistic Regression
   - Decision Tree
   - Random Forest

3. **Model Evaluation**
   - Accuracy, precision, recall, and F1 score
   - Confusion matrices
   - ROC curves and AUC scores
   - Precision-Recall curves
   - Cross-validation

## Key Findings
- **Feature Importance**: Alcohol content and sulphates are the most significant predictors of wine quality. Higher alcohol levels strongly correlate with better quality wines, while higher volatile acidity negatively impacts wine quality.

- **Model Performance**:
  | Model | Accuracy |
  |-------------|---------|
  | DummyClassifier | 49.35 |
  | Logistic Regression | 82.78% |
  | Decision Tree | 89.87%|
  | Random Forest | 94.65%|

- **Class Prediction**: The Random Forest model demonstrated balanced performance in predicting both high-quality and low-quality wines, maintaining high precision, recall, and F1 scores across both classes.

- **Quality Levels**: There is a significant difference in prediction performance across different quality levels. Simpler models struggle with the minority class (high-quality wines), while the Random Forest model effectively minimizes this performance gap.

## Requirements
- Python 3.8+
- scikit-learn
- pandas
- numpy
- matplotlib
- seaborn

## References
1. Laughter, A., Omari, S. (2020). A Study of Modeling Techniques for Prediction of Wine Quality.
2. Chhikara, S., Bansal, P., Malik, K. (2023). Wine Quality Prediction Using Machine Learning Techniques.
3. G. Hu, T. Xi, F. Mohammed and H. Miao (2016). Classification of wine quality with imbalanced data.
4. Mahima, Gupta, U., Patidar, Y., Agarwal, A., Singh, K.P. (2020). Wine Quality Analysis Using Machine Learning Algorithms.
