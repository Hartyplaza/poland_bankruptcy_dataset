# Poland Bankruptcy Prediction Using Random Forest and Gradient Boosting Trees

This project aims to predict bankruptcy in Polish companies using both Random Forest and Gradient Boosting Trees models. The dataset used for this analysis is the Poland Bankruptcy dataset, which is available in ARFF format within a ZIP archive.

## Table of Contents

    Dataset
    Installation
    Usage
    Model
    Resampling
    Results
    Best Performing Model
    Contributing
    License

Dataset

The dataset used for this project is the Poland Bankruptcy dataset. The specific file used is 2year.arff, which contains financial data of Polish companies.
Installation

To get started with this project, clone the repository and install the required dependencies.
Usage

This section demonstrates how to read the ARFF file from the ZIP archive and load it into a Pandas DataFrame.
Model

Two models were used for this project:

    Random Forest: The Random Forest model was chosen for its robustness and ability to handle large datasets with high dimensionality.

    Gradient Boosting Trees: The Gradient Boosting Trees model was also used to compare its performance with the Random Forest model.

Resampling

To address class imbalance in the dataset, the following resampling steps were applied:

    Oversampling the Minority Class: An oversampler object was created targeting 5000 samples for the minority class.

    Creating a New DataFrame from the Resampled Data: A new DataFrame was created from the resampled data, and the oversampled minority class was filtered out.

    Downsampling the Majority Class: The majority class from the original DataFrame was identified and downsampled to match the number of minority class samples.

    Combining the Resampled Data: The newly sampled data was combined into a new DataFrame, balanced_train, and the dataset was shuffled to randomly mix fraud and no_fraud cases.

Results
Random Forest Model

The classification report for the Random Forest model is as follows:

    Precision: 1.00 for class 0, 0.99 for class 1
    Recall: 0.99 for class 0, 1.00 for class 1
    F1-Score: 1.00 for both classes
    Accuracy: 1.00

Gradient Boosting Trees Model

The classification report for the Gradient Boosting Trees model is as follows:

    Precision: 0.94 for class 0, 0.89 for class 1
    Recall: 0.89 for class 0, 0.94 for class 1
    F1-Score: 0.91 for class 0, 0.92 for class 1
    Accuracy: 0.92

Best Performing Model

The best performing model for this project is the Random Forest model. It achieved an accuracy of 1.00 and high precision, recall, and F1-scores for both classes, indicating excellent performance in predicting bankruptcy in Polish companies.
Contributing

Contributions are welcome! Please open an issue or submit a pull request if you have any improvements or bug fixes.
