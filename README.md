# Titanic Survival Prediction

## Project Overview

This project predicts whether a passenger survived the Titanic disaster using machine learning.

The project includes:

- Data preprocessing
- Feature engineering
- Missing value handling
- Categorical encoding
- Random Forest classification
- Feature importance and SHAP explainability
- Model saving using Joblib

---

## Dataset

Dataset used:

Titanic Survival Dataset

Main columns:

- PassengerId
- Survived
- Pclass
- Name
- Sex
- Age
- SibSp
- Parch
- Ticket
- Fare
- Cabin
- Embarked

Place the dataset file:

```bash
Titanic-Dataset.csv
```

inside the project folder.

---

## Features Created

The following new features were generated:

### 1. Title Extraction

Titles were extracted from passenger names.

Examples:

- Mr
- Mrs
- Miss
- Master

### 2. FamilySize

```python
FamilySize = SibSp + Parch + 1
```

### 3. CabinPresent

Checks whether cabin information exists.

```python
1 = Cabin available
0 = Cabin missing
```

---

## Missing Value Handling

| Column | Method Used |
|---|---|
| Age | Median Value |
| Cabin | Filled with "Unknown" |
| Embarked | Mode Value |

---

## Packages Used

| Package | Version |
|---|---|
| Python | 3.11 |
| pandas | 2.2.2 |
| scikit-learn | 1.5.1 |
| matplotlib | 3.9.2 |
| shap | 0.46.0 |
| joblib | 1.4.2 |

---

## Install Requirements

Run:

```bash
pip install pandas==2.2.2 scikit-learn==1.5.1 matplotlib==3.9.2 shap==0.46.0 joblib==1.4.2
```

---

## Run the Project

Open Jupyter Notebook:

```bash
jupyter notebook
```

Open:

```bash
Titanic_Survival_Prediction.ipynb
```

Run all notebook cells sequentially.

---

## Machine Learning Model

Model used:

```bash
RandomForestClassifier
```

Train-test split:

```bash
80% Training
20% Testing
```

---

## Model Explainability

The project includes:

- Feature Importance
- SHAP Summary Plot

These help explain which features most influence survival prediction.

---

## Evaluation Metrics

The following metrics are used:

- Accuracy Score
- Precision
- Recall
- F1-Score
- Classification Report

---

## Saved Model

The trained model is saved as:

```bash
titanic_model.joblib
```

---

## Inference Example

```python
import joblib

model = joblib.load("titanic_model.joblib")

sample = [[3,1,22,7.25,2,10,2,0]]

prediction = model.predict(sample)

print("Prediction:", prediction[0])
```

---

## Project Structure

```bash
├── Titanic-Dataset.csv
├── Titanic_Survival_Prediction.ipynb
├── titanic_model.joblib
├── README.md
```

---

## Conclusion

The project successfully predicts Titanic passenger survival using machine learning techniques with feature engineering and explainable AI methods.