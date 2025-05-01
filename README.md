# 🧠 Income Classification and Clustering Using Machine Learning

This project explores both **supervised** and **unsupervised** machine learning methods to analyze income classification using the **UCI Census Income Dataset**. The goal was to understand patterns in demographic and employment data that influence whether an individual's income exceeds $50K.

## 📊 Dataset
- **Source**: [UCI Machine Learning Repository – Census Income Data](https://archive.ics.uci.edu/ml/datasets/census+income)
- The dataset includes features like age, workclass, education, occupation, relationship, race, sex, hours-per-week, and native country.
- The target variable is **income**, classified as `<=50K` or `>50K`.

## 🧪 Methods Used

### 1. **Supervised Learning**
- **Model**: Random Forest Classifier
- **Preprocessing**:
  - Handled missing values by replacing `'?'` with `NaN` and dropping incomplete rows.
  - Encoded categorical features using `LabelEncoder`.
  - Split data into training and test sets (80/20 split).
- **Evaluation**:
  - Used `classification_report` and `accuracy_score` to assess performance.
  - Reported metrics include precision, recall, F1-score, and accuracy.

### 2. **Unsupervised Learning**
- **Model**: K-Means Clustering
- **Preprocessing**:
  - Scaled all features using `StandardScaler`.
- **Clustering**:
  - Applied K-Means with `n_clusters=2`, based on the binary nature of the income variable.
  - Assigned a cluster label to each sample and compared it to actual income labels.
- **Visualization**:
  - Created a seaborn countplot to compare how well clustering aligns with income classes.

## 🔍 Key Insights
- The Random Forest classifier provided strong performance in predicting income level based on demographic and occupational features.
- K-Means clustering showed some separation between income groups, although it was not perfectly aligned—highlighting the challenge of unsupervised learning on complex socioeconomic data.

## 🧰 Technologies Used
- Python
- Jupyter Notebook
- Scikit-learn
- Pandas
- Seaborn & Matplotlib
- UCI ML Repo API (`ucimlrepo`)