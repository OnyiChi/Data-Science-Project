# Breast Cancer Classification

This repository contains code for analyzing and reporting on breast cancer data. The goal is to provide insights into breast cancer incidence, risk factors, and survival rates based on the dataset.

## Introduction

Breast cancer is a significant health concern worldwide. Early detection and classification of breast cancer tumors are crucial for effective treatment. In this report, we explore the classification of breast cancer using logistic regression. Logistic regression is a powerful statistical technique commonly used for binary classification tasks.

## Dataset

The dataset used in this project is the Breast Cancer Wisconsin (Diagnostic) dataset from scikit-learn's built-in datasets. This dataset contains 569 instances and 30 features extracted from breast mass images, along with the corresponding binary labels indicating malignant or benign tumors.  The dataset includes the following columns:

- ID: Unique identifier for each patient.
- Diagnosis: Indicates whether the tumor is malignant (M) or benign (B).
- Other features: Attributes describing characteristics of the tumor, such as radius, texture, perimeter, area, smoothness, compactness, concavity, concave points, symmetry, and fractal dimension.
  

## Dependencies

To run the code in this repository, you'll need the following libraries:
- numpy
- pandas
- matplotlib
- seaborn
- scikit-learn

You can install these libraries using pip:
```
pip install numpy pandas matplotlib seaborn scikit-learn
```

## Data Preprocessing

The data preprocessing steps include:
1. Importing the dataset.
2. Renaming columns for consistency.
3. Checking for missing values.

## Data Visualization

Various plots are created to understand the distribution of different attributes and their relationships.

### Distribution Plots

![image](https://github.com/OnyiChi/Data-Science-Project/assets/144718639/6d9226ef-3324-4c4e-953f-c71e29f9c385)

357 benign cases ---> 1

212 malignant cases ---> 0

###  Correlation Heatmap

![image](https://github.com/OnyiChi/Data-Science-Project/assets/144718639/14b0c479-c11b-4370-8f94-861ad96564ae)


### Pair Plot

![image](https://github.com/OnyiChi/Data-Science-Project/assets/144718639/55ff0c15-3a05-4f69-89ee-05a6974f5d49)


## Analysis

### Exploratory Data Analysis (EDA)

EDA techniques are applied to uncover insights into breast cancer data, such as identifying patterns, correlations, and potential risk factors.

### Model Building

Machine learning models may be constructed to predict breast cancer diagnosis or survival rates based on patient features.

### Model Training and Evaluation

The dataset is split into training and testing sets using a 70-30 ratio. Then, a logistic regression model is instantiated and train on the training data. After training, the model's performance is evaluated using several metrics:

- Accuracy Score: It measures the proportion of correctly classified instances out of the total instances. In this case, the accuracy score is 95.32%.

- Confusion Matrix: It provides a summary of correct and incorrect predictions, showing true positives, true negatives, false positives, and false negatives.

- Precision: Precision measures the ratio of correctly predicted positive observations to the total predicted positives. It reflects the model's ability to avoid false positives. For this model, precision is 96.92%.

- Recall (Sensitivity): Recall calculates the ratio of correctly predicted positive observations to all actual positives. It indicates the model's ability to detect positive instances. Here, recall is 94.44%.

- F1 Score: The F1 score is the harmonic mean of precision and recall, providing a balance between the two metrics. It is 95.66% in this model.

These evaluation metrics collectively demonstrate that our logistic regression model performs well in classifying breast cancer tumors, with high accuracy, precision, recall, and F1 score.

The dataset into training and testing sets, train a logistic regression model on the training data, and evaluate its performance using various metrics such as accuracy, precision, recall, F1-score, and confusion matrix.

## Conclusion

In conclusion, this report highlights the application of logistic regression in breast cancer classification. By leveraging machine learning techniques, we can aid medical professionals in diagnosing breast cancer with high accuracy, thus facilitating timely interventions and improving patient outcomes. Further refinements and optimizations could be explored to enhance the model's performance and generalizability.



