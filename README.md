# IMDB Movie Revenue Prediction

A simple machine learning project that predicts a movie's box office revenue using **Linear Regression**, built on the IMDB movies dataset.

## 📌 Project Overview

This project walks through a complete regression workflow:

1. Load and explore the IMDB movie dataset
2. Clean the data (handle missing values)
3. Apply a **log transform** to Revenue (since revenue is right-skewed — a few blockbusters, many small films)
4. **Standardize** the input features so coefficients are comparable
5. Train a Linear Regression model
6. Evaluate performance (MSE, RMSE, R²) on both log and original scale
7. Visualize Actual vs Predicted revenue

## 🗂 Dataset

* **Source:** [IMDB 5000 Movie Dataset / IMDB Movies (Kaggle)](https://www.kaggle.com/datasets) — replace this link with the exact dataset you used
* **File used:** `imdb\_movie\_dataset.csv`
* Columns used: `Title, Genre, Director, Actors, Rating, Votes, Runtime (Minutes), Metascore, Revenue (Millions)`

> Note: The dataset CSV is not included in this repo (check the dataset's license before redistributing). Download it from the source above and place it in the project root before running the notebook.

## ⚙️ Features Used

|Feature|Description|
|-|-|
|Rating|IMDB user rating|
|Votes|Number of user votes|
|Runtime (Minutes)|Movie duration|
|Metascore|Critic score|

**Target:** `Revenue (Millions)` (log-transformed during training)

## 📊 Results

|Metric|Value|
|-|-|
|R² Score|\~0.45 (baseline)|
|RMSE|\~80.0 (baseline, original scale)|

> Update these numbers after running the modified notebook with log-transform + scaling.

## 🛠 Tech Stack

* Python
* pandas, numpy
* scikit-learn
* matplotlib, seaborn

## 🚀 How to Run

1. Clone the repository

```bash
   git clone https://github.com/<your-username>/imdb-revenue-prediction.git
   cd imdb-revenue-prediction
   ```

2. Install dependencies

```bash
   pip install -r requirements.txt
   ```

3. Add the dataset

   * Download `imdb\_movie\_dataset.csv` and place it in the project root
4. Run the notebook

```bash
   jupyter notebook Untitled1\_modified.ipynb
   ```

## 📈 Sample Output

The notebook produces:

* A distribution plot of Revenue before/after log transform
* Model coefficients (standardized, so magnitudes are comparable)
* An Actual vs Predicted scatter plot

## 🔮 Future Improvements

* Try Ridge/Lasso regression to handle multicollinearity
* Try tree-based models (Random Forest, XGBoost) for comparison
* Add cross-validation instead of a single train/test split
* Feature engineering (e.g., extract release year effects, genre one-hot encoding)

## 📄 License

This project is open source under the [MIT License](LICENSE).

