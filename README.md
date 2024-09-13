# Protein Analysis Machine Learning project

Overview

This project involves working with multimodal single-cell RNA sequencing (scRNA-seq) data. The goal is to predict protein abundance based on gene expression data.
Data Description

    Organs and Cells: The data is related to cells from organs such as the pancreas, including cell types specific to the organ (e.g., alpha and beta cells) and those related to vascular and immune systems.
    Data Types: The dataset consists of RNA transcript counts (gene expression) and surface protein abundance for cells.
    Data Source: The data is derived from bone marrow samples of human donors, predominantly immune system cells.

Data Files

    X_train.csv and X_test.csv: Contain RNA expression matrices where each row represents a cell, each column a gene, and values are expression levels.
    y_train.csv: Contains surface protein abundance data corresponding to the cells in X_train.csv.

Tasks
1. Exploration

    Data Inspection: Examine the number of observations and variables, and check data types. Convert types if necessary and ensure data completeness.
    Descriptive Statistics: Analyze the distribution of the target variable with basic statistics and visualizations like histograms.
    Correlation Analysis: Identify the 250 most correlated features with the target variable. Compute and visualize correlations using a heatmap.

2. ElasticNet Model

    Model Overview: Explain the ElasticNet model, including the parameters, the objective function, and the hyperparameters. Discuss how ElasticNet includes ridge regression and lasso as special cases.
    Hyperparameter Tuning: Define a grid of hyperparameters, ensuring it covers ridge regression and lasso. Use cross-validation to select the best hyperparameters.
    Performance Metrics: Report training and validation errors averaged across cross-validation folds.

3. Random Forest Model

    Model Training: Train a Random Forest model and compare it to the ElasticNet model.
    Hyperparameter Tuning: Select three hyperparameters and define a 3D grid of combinations. Use cross-validation to find the best values.
    Comparison: Summarize and compare results from cross-validation for both models and a basic reference model that predicts the mean of the target variable.

4. Test Data Prediction

    Model Application: Apply the chosen model to predict values on the test dataset.
    Submission: Provide a file with predictions including observation IDs and predicted values. The quality of predictions will be evaluated based on RMSE (Root Mean Squared Error).
