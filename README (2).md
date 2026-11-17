# Mushroom Classification (Edible vs Poisonous)

A machine learning project that predicts whether a mushroom is **edible or poisonous** using the UCI Mushroom dataset. I compared three classification models and evaluated them with accuracy, precision, recall and a confusion matrix.

## Problem
Eating the wrong mushroom can be dangerous, so a model that rarely misses a poisonous mushroom is important. In this project, **recall for the poisonous class** is the most important metric.

## Dataset
- **Source:** [UCI Machine Learning Repository: Mushroom](https://archive.ics.uci.edu/dataset/73/mushroom)
- **Size:** 8,124 rows, 22 categorical features (cap shape, odor, gill size, etc.)
- **Target:** `edible` (e) or `poisonous` (p)

## Tools
Python, pandas, NumPy, scikit-learn, matplotlib, seaborn, Jupyter Notebook

## Steps
1. Loaded the data and checked class balance and missing values
2. Exploratory data analysis (class balance, odor vs class)
3. Encoded categorical features with One-Hot Encoding
4. Split the data into train and test sets (80/20, stratified)
5. Trained Logistic Regression, Decision Tree and Random Forest
6. Evaluated the models and compared the results

## Results

| Model | Accuracy | Precision | Recall |
|---|---|---|---|
| Logistic Regression | 99.94% | 100% | 99.87% |
| Decision Tree | 100% | 100% | 100% |
| Random Forest | 100% | 100% | 100% |

*Recall and precision are for the poisonous class.*

### Confusion Matrix (Random Forest)
![Confusion Matrix](images/confusion_matrix.png)

### Top 10 Important Features (Random Forest)
![Feature Importance](images/feature_importance.png)

## Key Learnings
- **Best model:** Decision Tree and Random Forest both scored 100%. I prefer Random Forest because it combines many trees and is more stable than a single tree.
- **Most important features:** `odor_n` (no odor) and `odor_f` (foul odor) ranked highest, followed by gill size and spore print color.
- **Why recall matters:** A poisonous mushroom predicted as edible could cause serious harm, so recall for the poisonous class matters more than overall accuracy.
- **Why accuracy is so high:** The features, especially odor, separate the two classes very clearly. This does not mean the model would perform as well on messy real-world data.

## How to Run
```bash
git clone https://github.com/Shashini-fernando08/mushroom-classification-ml.git
cd mushroom-classification-ml
pip install pandas numpy scikit-learn matplotlib seaborn jupyter
jupyter notebook mushroom_classification.ipynb
```

## Author
**Shashini** | BSc (Hons) in Information Technology, SLIIT
[GitHub](https://github.com/Shashini-fernando08)