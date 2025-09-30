Sonar Data Classification with Logistic Regression
Project Overview
This project implements a Logistic Regression model to classify sonar data into two categories: "Rock" (R) and "Mine" (M). The dataset used is sonar data.csv, which contains features extracted from sonar signals. The model is trained and evaluated using scikit-learn, achieving accuracy scores on both training and test datasets.
Table of Contents

Installation
Dataset
Usage
Code Explanation
Results
Contributing
License

Installation
To run this project, ensure you have Python installed along with the required libraries. Follow these steps:

Clone the repository


Navigate to the project directory:cd your-repo-name


Install the required dependencies:pip install numpy pandas scikit-learn



Dataset
The dataset (sonar data.csv) contains 208 rows and 61 columns, with 60 feature columns (numerical) and 1 target column labeled R (indicating "Rock" or "Mine"). The features represent sonar signal characteristics.

Source: User-provided dataset (ensure sonar data.csv is in the project directory).
Features: 60 numerical columns representing sonar signal attributes.
Target: The R column, with values R (Rock) or M (Mine).

Usage

Place the sonar data.csv file in the project directory.
Run the Python script:python sonar_classification.py


The script will:
Load and preprocess the dataset.
Split the data into training (90%) and test (10%) sets.
Train a Logistic Regression model.
Output the accuracy scores for both training and test datasets.



Code Explanation
The code performs the following steps:

Import Libraries:

numpy and pandas for data manipulation.
sklearn.model_selection.train_test_split for splitting data.
sklearn.linear_model.LogisticRegression for the classification model.
sklearn.metrics.accuracy_score for evaluating model performance.


Load and Explore Data:

Loads sonar data.csv into a pandas DataFrame.
Displays the first few rows (df.head()), shape (df.shape), statistical summary (df.describe()), and class distribution (df.value_counts()).
Groups data by the target column (R) to compute mean feature values.


Data Preparation:

Splits features (x) and target (y) by dropping the R column from the DataFrame.
Splits data into training (90%) and test (10%) sets using train_test_split with stratification to maintain class balance.


Model Training:

Initializes and trains a Logistic Regression model on the training data.


Evaluation:

Predicts labels for training and test sets.
Computes and prints accuracy scores for both sets using accuracy_score.



Results

Training Accuracy: Printed as the accuracy of the model on the training data.
Test Accuracy: Printed as the accuracy of the model on the test data.

Example output (values depend on the dataset):
Accuracy: 0.8342245989304813
Accuracy: 0.7619047619047619

Contributing
Contributions are welcome! Please follow these steps:

Fork the repository.
Create a new branch (git checkout -b feature-branch).
Make your changes and commit (git commit -m "Add feature").
Push to the branch (git push origin feature-branch).
Open a pull request.

License
This project is licensed under the MIT License. See the LICENSE file for details.
