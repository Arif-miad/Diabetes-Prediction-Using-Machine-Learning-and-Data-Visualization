

# Diabetes Prediction Dataset

This dataset contains diagnostic measurements collected from female patients to predict the onset of diabetes. It serves as a valuable resource for machine learning practitioners and researchers to explore data preprocessing, visualization, and classification techniques in healthcare analytics.

## Dataset Overview

The dataset consists of **768 records**, with each record characterized by 8 medical attributes and a binary target variable, **Outcome**. The goal is to predict whether a patient has diabetes (`Outcome = 1`) or not (`Outcome = 0`) using the given features.

### Sample Data
| Pregnancies | Glucose | BloodPressure | SkinThickness | Insulin | BMI  | DiabetesPedigreeFunction | Age | Outcome |
|-------------|---------|---------------|---------------|---------|------|--------------------------|-----|---------|
| 6           | 148     | 72            | 35            | 0       | 33.6 | 0.627                    | 50  | 1       |
| 1           | 85      | 66            | 29            | 0       | 26.6 | 0.351                    | 31  | 0       |
| 8           | 183     | 64            | 0             | 0       | 23.3 | 0.672                    | 32  | 1       |
| 1           | 89      | 66            | 23            | 94      | 28.1 | 0.167                    | 21  | 0       |
| 0           | 137     | 40            | 35            | 168     | 43.1 | 2.288                    | 33  | 1       |

---

## Column Descriptions

- **Pregnancies**: Number of times the patient has been pregnant.
- **Glucose**: Plasma glucose concentration after a 2-hour oral glucose tolerance test.
- **BloodPressure**: Diastolic blood pressure (mm Hg).
- **SkinThickness**: Triceps skinfold thickness (mm).
- **Insulin**: 2-hour serum insulin (mu U/ml).
- **BMI**: Body mass index (weight in kg/(height in m)^2).
- **DiabetesPedigreeFunction**: A function that indicates the likelihood of diabetes based on family history.
- **Age**: Age of the patient (years).
- **Outcome**: Binary variable indicating diabetes presence (`1` = yes, `0` = no).

---

## Applications of the Dataset

This dataset can be used for:
1. **Machine Learning Classification**: Build and evaluate models to predict diabetes onset.
2. **Exploratory Data Analysis (EDA)**: Identify trends, correlations, and outliers in medical data.
3. **Feature Engineering**: Create new insights by transforming and selecting key features.
4. **Healthcare Research**: Investigate how medical and lifestyle factors contribute to diabetes.

---

## Project Workflow

### 1. Data Preprocessing
- Handle missing values and outliers in critical columns like `Glucose`, `BloodPressure`, and `Insulin`.
- Scale and normalize the data to ensure consistent ranges across features.

### 2. Exploratory Data Analysis (EDA)
- Perform statistical analysis to understand feature distributions and relationships.
- Visualize data with plots, including:
  - **Histograms and Density Plots**: For feature distribution.
  - **Correlation Heatmaps**: To explore feature interdependence.
  - **Boxplots**: To identify outliers.
```python
plt.figure(figsize=(6, 4))
sns.violinplot(data=data, x='Outcome', y='BMI', palette='muted')
plt.title('Violin Plot for BMI by Outcome')
plt.show()
  ```
![](https://github.com/Arif-miad/Diabetes-Prediction-Using-Machine-Learning-and-Data-Visualization/blob/main/ar1.png)

```python
# 4. Scatter Plot for Age vs Glucose
plt.figure(figsize=(6, 4))
sns.scatterplot(data=data, x='Age', y='Glucose', hue='Outcome', palette='deep')
plt.title('Scatter Plot for Age vs Glucose')
plt.show()
```
![](https://github.com/Arif-miad/Diabetes-Prediction-Using-Machine-Learning-and-Data-Visualization/blob/main/ar2.png)
```python
sns.pairplot(data, hue='Outcome', palette='husl', diag_kind='kde')
plt.suptitle('Pairplot for Continuous Variables', y=1.02)
plt.show()
```
![](https://github.com/Arif-miad/Diabetes-Prediction-Using-Machine-Learning-and-Data-Visualization/blob/main/ar3.png)
```python
plt.figure(figsize=(6, 4))
sns.kdeplot(data=data, x='Glucose', hue='Outcome', fill=True, palette='muted')
plt.title('KDE Plot for Glucose by Outcome')
plt.show()
```
![](https://github.com/Arif-miad/Diabetes-Prediction-Using-Machine-Learning-and-Data-Visualization/blob/main/ar20.png)
### 3. Model Development
- Train machine learning models such as Logistic Regression, Random Forest, and XGBoost.
- Evaluate models using metrics like accuracy, precision, recall, and ROC-AUC.

---

## Getting Started

### 1. Clone the Repository
```bash
git clone https://github.com/your-username/diabetes-dataset.git
cd diabetes-dataset
```

### 2. Install Dependencies
```bash
pip install -r requirements.txt
```

### 3. Run the Analysis
Open and run the provided Jupyter Notebook to explore the dataset and build models:
```bash
jupyter notebook diabetes_analysis.ipynb
```



## Insights
- High glucose levels, BMI, and family history (DiabetesPedigreeFunction) are strong predictors of diabetes.
- Age and pregnancy history also influence diabetes onset.



## Contributing
Contributions are welcome! If you identify issues or have suggestions, feel free to open an issue or submit a pull request.



## License
This project is licensed under the MIT License. See the `LICENSE` file for details.

