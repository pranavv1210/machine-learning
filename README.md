# Machine Learning — A Practical Study Path

This repository is a step-by-step study resource for learning classical Machine Learning with Python. It is designed to teach both **what to do** and **why each step works**.

The existing 31 numbered chapters and their original datasets are retained. The notebooks are intended to be read in order, executed from top to bottom, and revisited while solving the exercises.

## How to study each notebook

1. Read the learning goals and the introduction before running code.
2. Look up every new technical term in the chapter glossary or the inline explanation.
3. Run the code cells in order. Do not skip a cell just because its output looks familiar.
4. Compare the output with the explanation immediately below it. Ask: what did the code receive, what did it calculate, and what does the result tell me?
5. Change one value or parameter and run the cell again. Predict the result first.
6. Complete the exercises without looking at the solution immediately.
7. Explain the concept aloud in your own words. If you cannot explain why a method is used, revisit its intuition and assumptions.

## Learning roadmap

| Stage | Chapters | What you learn |
|---|---|---|
| Python and data foundations | 01–04 | Python skills, NumPy arrays, Pandas tables, visualizations |
| Data preparation | 05–08 | Cleaning, exploratory analysis, feature engineering, safe data splitting |
| Supervised learning | 09–17 | Regression and classification algorithms |
| Unsupervised learning | 18–20 | Clustering and dimensionality reduction |
| Model reliability | 21–25 | Regularization, validation, tuning, metrics, imbalanced data |
| Ensembles and practical ML | 26–31 | Combining models, boosting, XGBoost, model persistence, complete workflows |

## Chapter index

1. Python for ML
2. NumPy
3. Pandas
4. Matplotlib and Seaborn
5. Data Cleaning
6. Exploratory Data Analysis
7. Feature Engineering
8. Train-Test Split
9. Linear Regression
10. Multiple Linear Regression
11. Polynomial Regression
12. Logistic Regression
13. Decision Tree
14. Random Forest
15. Support Vector Machine
16. K-Nearest Neighbors
17. Naive Bayes
18. K-Means Clustering
19. Hierarchical Clustering
20. Principal Component Analysis
21. Regularization
22. Cross Validation
23. Hyperparameter Tuning
24. Model Evaluation Metrics
25. Imbalanced Data Handling
26. Ensemble Learning
27. Bagging and Boosting
28. Gradient Boosting
29. XGBoost
30. Model Saving and Loading
31. End-to-End ML Projects

## Essential ideas to understand

- **Feature:** an input measurement the model uses, such as house area or a patient's age.
- **Target / label:** the value the model is asked to predict.
- **Training:** the process of adjusting a model using examples.
- **Inference:** using a trained model to make predictions on new data.
- **Loss:** a numerical measure of how wrong a model's predictions are during learning.
- **Metric:** a measure used to evaluate model performance, such as MAE or precision.
- **Generalization:** how well a model works on examples it did not train on.
- **Overfitting:** learning training examples too specifically, including noise, so performance on new data suffers.
- **Data leakage:** allowing information into training that would not legitimately be available when predicting in the real world.
- **Hyperparameter:** a configuration chosen before or around training, such as tree depth or learning rate.

## Setup

Use Python 3.10 or 3.11 for a predictable learning environment unless a particular library's current installation guide recommends otherwise.

```bash
python -m venv .venv
# Windows PowerShell:
.venv\Scripts\Activate.ps1
# macOS / Linux:
source .venv/bin/activate
python -m pip install --upgrade pip
pip install -r requirements.txt
jupyter notebook
```

Open a notebook and run its cells from top to bottom. Many notebook datasets use paths relative to their chapter folder, so start Jupyter from the repository root and check the notebook's dataset path if your environment reports a file-not-found error.

## Important study habits

- Keep the existing dataset and notebook outputs as the reference for the examples.
- A printed metric is not automatically good or bad: interpret it in the context of the target, dataset and baseline.
- Never fit preprocessing steps using the test set. Fit them on training data and apply the learned transformation to validation/test data.
- For classification, do not rely on accuracy alone when classes are imbalanced.
- Set random seeds when supported so that experiments are easier to reproduce.

## Additional resources

- [Google Machine Learning Crash Course](https://developers.google.com/machine-learning/crash-course)
- [scikit-learn User Guide](https://scikit-learn.org/stable/user_guide.html)
- [NumPy documentation](https://numpy.org/doc/stable/)
- [Pandas documentation](https://pandas.pydata.org/docs/)
- [GeeksforGeeks Machine Learning](https://www.geeksforgeeks.org/machine-learning/)
- [StatQuest](https://statquest.org/)

These resources supplement the repository; the notebooks should remain understandable without having to follow an external tutorial for every step.

## Study tracker

Open `study-tracker.html` in a browser to record chapter progress. Progress is stored by the tracker in the browser you use.
