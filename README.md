# EduPulse · Student Success Analytics

An interactive data-science assignment project exploring student performance with two supervised-learning tasks:

- **Regression:** predict a numeric final grade (G3).
- **Binary classification:** estimate pass likelihood, where a grade at or above the configurable threshold (10 by default) is labelled Pass.

The sample uses 395 mathematics records from the UCI Student Performance dataset. It includes earlier-period grades (G1, G2), study time, previous failures and absences. The app compares Linear Regression, Decision Tree, Random Forest and KNN for regression; Logistic Regression, Decision Tree, Random Forest and KNN for classification.

## Run the project

Open `edupulse_lab.html` in a modern browser. No build step, package installation or server is required. The app and its machine-learning implementations run locally; uploaded CSV data is not sent to a server. Google Fonts are an optional external stylesheet.

Keep `edupulse_lab.html`, `edupulse_lab.css` and `edupulse_lab.js` together in the same folder.

## Evaluation

Models are trained on the training partition and scored on held-out records. The supplied sample has a saved 80/20 split; uploaded data uses a random split. Classification uses a stratified random split for uploaded data.

For grade regression, compare **RMSE** (primary; lower is better), MAE (grade-point error; lower is better) and R² (higher is better). For pass/fail classification, compare **F1** (primary; balances precision and recall), accuracy, precision, recall and the confusion matrix. The highlighted model is the best on the current split and selected primary metric; its ranking can change with the data, settings or split.

## Interpretation and limitations

This is an educational demonstration, not a validated student-risk tool. The dataset is small and specific to secondary-school mathematics in Portugal. G1 and G2 are prior grades, so the model assumes they are available when estimating G3. Predictions show associations, not causes; they should not be used to label students or make high-stakes decisions.

Dataset source: [UCI Machine Learning Repository · Student Performance](https://archive.ics.uci.edu/dataset/320/student+performance).

> Cortez, P. & Silva, A. (2008). *Using Data Mining to Predict Secondary School Student Performance.* 5th Future Business Technology Conference (FUBUTEC).
