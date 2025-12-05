# CS210 Homework #2 – Penguin Health Classification

This notebook was completed as part of **CS210: Introduction to Data Science**. The assignment involved building a decision tree classifier to predict penguin health status using audio features from a modified version of the Palmer Penguins dataset.

---

## Objective

The goal was to apply the **machine learning experimental pipeline** by:
- Preprocessing real-world tabular data
- Training and tuning a **Decision Tree Classifier**
- Evaluating the model using accuracy, confusion matrix, and feature correlations
- Practicing AI-assisted coding via ChatGPT prompts

---

## Dataset Source

The dataset was derived from:  
🔗 https://www.kaggle.com/datasets/samybaladram/palmers-penguin-dataset-extended/data  
A custom static CSV version named `cs210_hw2_dataset.csv` was provided via SuCourse.

It includes columns like:
- Categorical: `species`, `island`, `sex`, `diet`, `life_stage`, `health_metrics` (target)
- Numerical: `bill_length_mm`, `bill_depth_mm`, `flipper_length_mm`, `body_mass_g`, `year`

---

## Tools and Libraries Used

- `pandas` – data loading & wrangling  
- `numpy` – numerical operations  
- `scikit-learn` – model building, evaluation, hyperparameter tuning  
- `seaborn`, `matplotlib` – visualization (heatmaps, decision tree plot)  

---

## Method

- **Step 1:** Imported and explored dataset using `.info()`, `.head()`, `.shape()`
- **Step 2:** Filled missing values with mode
- **Step 3:** Mapped categorical variables to numerical values
- **Step 4:** Split into train/test (80/20) with `train_test_split`
- **Step 5:** Visualized feature correlations & selected key predictors
- **Step 6:** Tuned `max_depth` and `min_samples_split` with `GridSearchCV`
- **Step 7:** Trained and visualized final Decision Tree
- **Step 8:** Evaluated model with accuracy and confusion matrix
- **Step 9:** Calculated **information gain** using entropy formula

---

## Key Observations

- **Accuracy:** Achieved ~84% accuracy on test set  
- **Strongest Correlation:** `energy` ↔ `loudness` (r ≈ 0.76)  
- **Common Mistake:** Model most frequently mistakes *overweight* for *healthy*  
- **Info Gain (1st split):** `-0.7219`  
- **Moderate Predictors:** `diet`, `life_stage` moderately correlate with health status

---

## Files

- `Beyza-Balota-CS210-HW2.ipynb`: Jupyter Notebook with code and outputs  
- `README.md`: Project overview (this file)

---

## Notes

This assignment focused on:
- Applying the **end-to-end ML workflow** using decision trees
- Working with real-world data imperfections (missing values, categorical mappings)
- Using **AI tools (ChatGPT)** effectively through prompt engineering

No external APIs or advanced ML models were used.
