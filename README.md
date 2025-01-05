# Predicting-Unknown-Music-Genres-Evaluating-Model-Precision-and-Practical-Applications

## Project Overview
This project focuses on building and evaluating a machine learning model to predict music genres. The key steps involve analyzing a dataset, performing dimensionality reduction with PCA, and comparing model performance using precision scores. Finally, the best-performing model is applied to predict missing genres in the dataset.

---

## Table of Contents
- [Project Overview](#project-overview)
- [Dataset Information](#dataset-information)
- [Workflow](#workflow)
- [Key Results](#key-results)
- [Dependencies](#dependencies)
- [Conclusion](#conclusion)

---

## Dataset Information
- **Name**: Modified Music Dataset (`music_dataset_mod.csv`)
- **Size**: Contains data on various tracks, including genre labels and audio features.
- **Missing Data**: Some tracks have missing genre labels, which the project aims to predict.

---

## Workflow
### 1. Data Preprocessing
- Checked for missing values and handled them.
- Encoded categorical target variables (`Genre`) using `LabelEncoder`.
- Scaled numerical features using `StandardScaler`.

### 2. Exploratory Data Analysis
- Visualized the distribution of music genres.
- Created a correlation matrix to analyze relationships between features.

### 3. Dimensionality Reduction
- Applied Principal Component Analysis (PCA) to reduce feature dimensions while retaining at least 80% of variance.

### 4. Model Training and Evaluation
- Trained Logistic Regression models:
  - **With PCA-transformed features**
  - **With original features**
- Compared precision scores for the "Hip-hop" class and overall model accuracy.

### 5. Predicting Missing Genres
- Applied the best-performing model to predict unknown genres in the dataset.
- Validated predictions using track-specific analysis.

---

## Key Results
- **Precision for 'Hip-hop' (With PCA)**: `0.4884`
- **Precision for 'Hip-hop' (Without PCA)**: `0.4490`
- **Best Model**: Logistic Regression trained on original features (slightly higher accuracy).

---

## Dependencies
To run this project, the following libraries are required:

- **Python 3.8+**: A versatile programming language for data analysis and machine learning.
- **pandas**: For data manipulation and analysis.
- **numpy**: For numerical computations and matrix operations.
- **scikit-learn**: For machine learning tasks, including data preprocessing, model training, and evaluation.
- **seaborn**: For statistical data visualization.
- **matplotlib**: For creating static, interactive, and animated visualizations.


## Conclusion

### Key Insights
- **Feature Selection**: Identifying and selecting relevant features improves model performance and interpretability.
- **Dimensionality Reduction**: PCA was used to reduce dimensionality while retaining 80% of the variance in the dataset.
- **Evaluation Metrics**: Comparing precision scores and other metrics helped determine the best-performing model.

### Model Performance
- The logistic regression model trained on **original features** slightly outperformed the model trained on **PCA-transformed features**.
- Precision for the "Hip-hop" genre was used as a key metric, highlighting minor differences between models.

### Practical Application
- The best model was applied to predict missing genres, showcasing its **real-world utility** and robustness.

### Key Takeaways
1. Dimensionality reduction can simplify models but may lead to slight trade-offs in precision for certain classes.
2. A detailed evaluation of precision scores for specific genres (e.g., "Hip-hop") is crucial for addressing imbalances or class-specific challenges.
3. Machine learning pipelines, when designed carefully, can address real-world problems like filling missing values in datasets effectively.

This project illustrates the value of combining **data preprocessing**, **dimensionality reduction**, and **model evaluation** in solving classification challenges with incomplete data.

