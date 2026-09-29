# 🌸 Iris Flower Species Classification using Artificial Neural Network

An end-to-end Machine Learning project that uses an **Artificial Neural Network (ANN)** to classify Iris flowers into three species based on their physical measurements.

The project covers the complete workflow from data validation and exploratory data analysis to feature engineering, ANN model training, evaluation, and deployment through a Gradio interface.

---

## 📌 Project Overview

The objective of this project is to build an Artificial Neural Network capable of classifying Iris flowers into:

- Iris-setosa
- Iris-versicolor
- Iris-virginica

The project uses two provided data sources:

- `Iris.csv`
- SQLite database containing the Iris dataset

Instead of combining the two sources and creating duplicate records, both sources are independently validated for consistency. The validated CSV data is then used for model development.

---

## 🎯 Objectives

- Understand and validate the Iris dataset from multiple sources
- Perform data cleaning and exploratory data analysis (EDA)
- Analyze feature distributions and relationships
- Create additional engineered features
- Prepare the data for Artificial Neural Network training
- Build and train a multiclass ANN classifier
- Evaluate the model using multiple classification metrics
- Test the model on a new flower sample
- Save the trained model and preprocessing objects
- Provide an interactive prediction interface using Gradio

---

## 📊 Dataset

The dataset contains **150 Iris flower samples** with the following original features:

| Feature | Description |
|---|---|
| `SepalLengthCm` | Length of the sepal in centimeters |
| `SepalWidthCm` | Width of the sepal in centimeters |
| `PetalLengthCm` | Length of the petal in centimeters |
| `PetalWidthCm` | Width of the petal in centimeters |
| `Species` | Target flower species |

An `Id` column is also present in the original dataset and is not used as a predictive feature.

### Target Classes

The model predicts one of three classes:

1. Iris-setosa
2. Iris-versicolor
3. Iris-virginica

---

## 🔍 Exploratory Data Analysis

The project performs several EDA steps to understand the dataset:

- Dataset shape and structure
- Missing-value analysis
- Duplicate-row detection
- Species distribution
- Numerical feature distributions
- Boxplots for detecting feature spread and potential outliers
- Feature comparison across species
- Scatter plots
- Pair plots
- Correlation analysis
- Correlation heatmap

These visualizations help understand how the flower measurements differ across species.

---

## ⚙️ Feature Engineering

In addition to the four original numerical measurements, four new features are created.

### 1. Petal Area

```text
PetalArea = PetalLengthCm × PetalWidthCm
