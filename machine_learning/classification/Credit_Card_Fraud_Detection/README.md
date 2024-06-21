# Credit Card Fraud Detection

This report outlines the process and findings from a project aimed at detecting fraudulent transactions in credit card data. The project leverages machine learning techniques, particularly Logistic Regression, to distinguish between legitimate and fraudulent transactions.

## Introduction

Credit card fraud is a significant concern in the financial industry, leading to substantial losses each year. Detecting fraudulent transactions early can prevent financial loss and protect cardholders. In this report, we explore the detection of fraudulent credit card transactions using logistic regression, a robust statistical technique commonly used for binary classification tasks.

## Dataset

The dataset used in this project is the Credit Card Transactions dataset. This dataset contains transactions made by credit cards, with each transaction labeled as either legitimate (0) or fraudulent (1). The dataset includes various features such as transaction amount and anonymized variables resulting from a PCA transformation.

- Class: Indicates whether the transaction is legitimate (0) or fraudulen(1).
- Amount: The transaction amount.
- Other features: Various anonymized attributes derived from PCA. 

  

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
1. Importing the dataset: : Loaded the dataset into a Pandas DataFrame.
2. Checking dataset structure: Displayed the first and last 5 rows, and checked for missing values.
3. Class distribution analysis: Identified the imbalance in the dataset with a higher number of legitimate transactions compared to fraudulent ones.


## Data Visualization

### Class Distribution
The dataset is highly imbalanced:

- 0: Normal Transaction
- 1: Fraudulent Transaction

Distribution of transactions:

- Legitimate transactions: 284,315
- Fraudulent transactions: 492


## Analysis

### Exploratory Data Analysis (EDA)

EDA techniques were applied to uncover insights into the credit card transaction data, such as identifying patterns and statistical differences between legitimate and fraudulent transactions.

### Data Balancing
To address the class imbalance, under-sampling was performed:

- Created a balanced dataset by sampling 492 legitimate transactions to match the number of fraudulent transactions.
- Concatenated the sampled legitimate transactions with all fraudulent transactions.

### Model Building

Machine learning models may be constructed to predict breast cancer diagnosis or survival rates based on patient features.

### Model Training and Evaluation

1. Splitting the data:

- Features (X): All columns except 'Class'.
- Target (Y): 'Class' column.
- Split the data into training (80%) and testing (20%) sets.

2. Training the Model:

- Trained a Logistic Regression model using the training data.

3. Evaluating the Model:

- Calculated the accuracy score for both training and testing data.

## Results

- Training Data Accuracy: The model showed high accuracy on the training data, indicating a good fit.

- Testing Data Accuracy: The accuracy on the testing data confirmed the model's ability to generalize to unseen data.

## Conclusion

In conclusion, this report highlights the successful implementation of logistic regression for detecting fraudulent credit card transactions. Despite the initial class imbalance, under-sampling allowed for a balanced training set, improving the model's performance. The logistic regression model demonstrated high accuracy in distinguishing between legitimate and fraudulent transactions, providing a reliable tool for early fraud detection.

