# **House Price Prediction Using Ensemble Techniques**

## **Overview**
This project predicts house prices using various machine learning models and ensembling techniques to achieve high accuracy and generalization. It explores multiple ensembling strategies such as bagging, boosting, stacking, voting, and weighted averaging. The dataset used is the [House Prices - Advanced Regression Techniques](https://www.kaggle.com/c/house-prices-advanced-regression-techniques) from Kaggle.

---

## **Ensembling Techniques Explained**

### 1. **Bagging (Bootstrap Aggregating)**
   - **Description**: Reduces variance by training multiple models on different random subsets of the dataset (with replacement) and aggregating their predictions.
   - **Example**: Random Forest is a classic bagging-based algorithm.
   - **Advantage**: Handles overfitting in high-variance models.

### 2. **Boosting**
   - **Description**: Models are trained sequentially, with each model correcting errors from the previous one. Focuses more on difficult-to-predict samples.
   - **Examples**: Gradient Boosting.
   - **Advantage**: Reduces bias and improves performance on complex datasets.

### 3. **Stacking**
   - **Description**: Combines multiple models by using their predictions as input features to a meta-model (e.g., Ridge Regression or Gradient Boosting).
   - **Advantage**: Exploits the strengths of diverse models for better generalization.

### 4. **Voting**
   - **Description**: Aggregates predictions from multiple models using:
     - **Hard Voting**: Majority voting for classification.
     - **Soft Voting**: Weighted average of predicted probabilities.
   - **Advantage**: Simple and interpretable ensemble technique.

### 5. **Weighted Averaging**
   - **Description**: Combines predictions by assigning weights based on model performance.
   - **Advantage**: Ensures the best-performing models contribute more to the final prediction.

---

## **Project Workflow**

### **1. Data Preparation**
- **Exploratory Data Analysis (EDA)**:
  - Handling missing values.
  - Analyzing numerical and categorical features.
  - Outlier detection and treatment.
- **Feature Engineering**:
  - Encoding categorical features.
  - Normalizing numerical features.
  - Creating interaction terms.
- **Feature Selection**:
  - Used Lasso Regression to select the most relevant features.

### **2. Models Trained**
- **Base Models**:
  - Linear Regression.
  - Random Forest.
  - Gradient Boosting.
  - XGBoost.
  - LightGBM.
- **Ensembling Techniques**:
  - Bagging: Random Forest.
  - Boosting: Gradient Boosting.
  - Stacking: Combination of base models with a Ridge meta-model.
  - Voting: Hard and Soft Voting with multiple base models.
  - Weighted Averaging: Weighted combination of base model predictions.

### **3. Evaluation Metrics**
- **Root Mean Squared Error (RMSE)**:
  - A lower RMSE indicates better model performance.
- **Comparison Table**:
  | **Technique**         | **RMSE** |
  |------------------------|----------|
  | Random Forest (Bagging)|    0.12260344620934514      |
  | Gradient Boosting      |    0.12662487427252478      |
  | Stacking               |    0.1231576901660913       |
  | Voting                 |    0.11924395629680816      |
  | Weighted Averaging     |    0.11896408092027111      |

---

## **Insights**
- Ensemble models outperformed individual models due to their ability to generalize better.
- Boosting techniques like Gradient Boosting and XGBoost achieved high accuracy but required careful hyperparameter tuning.
- Stacking effectively combined diverse models and leveraged their strengths for improved performance.
- Weighted Averaging provided flexibility by assigning importance to better-performing models.

---
