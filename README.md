## Caesarean Section Classification

### Project Overview

This project aims to classify whether a delivery will require a **Caesarean section** based on various maternal and delivery-related factors. Utilizing features such as age, number of previous deliveries, delivery time, blood pressure, and heart problems, the goal is to develop a machine learning model that can predict the need for a Caesarean section, potentially aiding medical practitioners in prenatal care and delivery planning.

-----

### Technical Highlights

  * **Dataset**: [Kaggle - Caesarean Section Classification Dataset](https://www.kaggle.com/datasets/amir75/caesarean-section-classification)
  * **Size**: 80 entries, 6 columns
  * **Key Features**:
      * Age, Delivery No (number of deliveries), Delivery No (delivery time, e.g., 'Timely', 'Premature'), Blood of Pressure, Heart Problem.
  * **Approach**:
      * Data Cleaning: Standardized 'Caesarian' target column (replaced 'yes' with 'Yes', 'no' with 'No'). No missing values found. Duplicates were present and handled implicitly as LabelEncoder converts all values. A dedicated duplicate drop would be more explicit.
      * Exploratory Data Analysis: Histograms, Boxplots, and Heatmaps were used for visualization.
      * Label Encoding: Applied to all columns, including numerical ones and the target 'Caesarian'.
      * Handling Class Imbalance with `SMOTE` (Synthetic Minority Over-sampling Technique) on the training data. This is important given the original class distribution (42 'Yes', 34 'No', 4 'yes' - combined to 46 'Yes' and 34 'No').
      * Binary Classification: The target variable 'Caesarian' indicates whether a Caesarean section was performed ('Yes' or 'No').
      * Models Used:
          * Logistic Regression, Ridge Classifier, SVC, Random Forest, XGBoost, AdaBoost, Gradient Boosting, Bagging, Decision Tree.
  * **Best Accuracy**:
      * 89.5% with XGBoost Classifier.
      * 84.2% with Logistic Regression, Ridge Classifier, and AdaBoost Classifier.
      * The overall accuracies are decent for a small dataset, with XGBoost performing best.

-----

### Purpose and Applications

  * Assist medical practitioners in **predicting the likelihood of a Caesarean section**, enabling better preparation and patient counseling.
  * Contribute to risk assessment during pregnancy and delivery planning.
  * Potentially improve maternal and infant outcomes by identifying high-risk cases in advance.
  * Serve as a tool for educational purposes in obstetrics and medical data analysis.

-----

### Installation

Clone the repository:

```bash
git clone https://github.com/BhaveshBhakta/Inventory-Classification-Using-ML.git
cd Inventory-Classification-Using-ML
```

Install the necessary libraries:

```bash
pip install pandas numpy seaborn matplotlib scikit-learn imbalanced-learn xgboost
```

-----

### Collaboration

We welcome contributions to improve the project. You can help by:

  * Exploring more robust strategies for handling the very small dataset size, such as more extensive cross-validation techniques.
  * Investigating alternative encoding methods for categorical features and their impact.
  * Adding explainability (e.g., SHAP or LIME) to understand which maternal factors are most influential in predicting Caesarean sections.
  * Collecting a larger and more diverse dataset to enhance model generalization and reliability.
