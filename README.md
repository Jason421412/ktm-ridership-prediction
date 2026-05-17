# KTM Komuter Ridership Prediction

A notebook-based machine learning project for predicting hourly KTM Komuter ridership using temporal, holiday, and station-related features.

## Why I Built This

Public transport demand changes by hour, day, station, and calendar context. Better ridership prediction can support planning decisions such as capacity allocation, timetable review, and identifying peak-demand patterns. This project treats ridership forecasting as a supervised regression problem and documents the modeling workflow in a Jupyter notebook.

## Features

- Notebook workflow for ridership prediction.
- Data preprocessing with pandas and NumPy.
- Exploratory visualization with Matplotlib, Seaborn, and Plotly.
- Temporal and holiday-related feature engineering.
- Regression modeling with scikit-learn and gradient-boosting libraries.
- Dependency file for reproducible local setup.
- Dataset folder documented separately because data files are excluded from the repository.

## Tech Stack

- **Language:** Python
- **Notebook:** Jupyter Notebook
- **Data:** pandas, NumPy
- **Visualization:** Matplotlib, Seaborn, Plotly
- **Machine learning:** scikit-learn, XGBoost, LightGBM, CatBoost
- **Feature engineering:** holidays, SciPy

## Architecture / System Design

```text
data/
  README.md

notebooks/
  ktm_ridership_prediction.ipynb

requirements.txt
```

- **Data layer:** Raw dataset files are expected under `data/`, but are not committed to the repository.
- **Modeling workflow:** The notebook handles loading, cleaning, feature engineering, model training, and evaluation.
- **Experimentation:** The dependency list supports several regression model families so results can be compared.
- **Deployment:** This is an analysis notebook, not a deployed prediction service.

## My Contributions

- Structured the project as a reproducible notebook-based ML workflow.
- Prepared dependency documentation through `requirements.txt`.
- Worked on preprocessing and feature engineering for ridership prediction.
- Explored regression models suitable for tabular transport-demand forecasting.
- Documented the current project scope and limitations honestly.

## What I Learned

- How transport forecasting problems can be framed as supervised regression tasks.
- Why temporal features and holiday context matter in demand prediction.
- How to compare multiple tabular ML models without treating one library as a guaranteed answer.
- Why public ML repositories should clearly explain missing datasets and reproducibility limits.

## Screenshots / Demo

No screenshots are currently tracked in this repository.

Evidence to add later:

- Notebook output charts exported as images.
- Model comparison table with MAE, RMSE, and R2.
- Feature-importance chart for the best-performing model.
- Dataset source and license notes, if the data can be shared publicly.

## Setup

1. Clone the repository.

   ```bash
   git clone https://github.com/Jason421412/ktm-ridership-prediction.git
   cd ktm-ridership-prediction
   ```

2. Create and activate a virtual environment.

   ```bash
   python -m venv .venv
   .venv\Scripts\activate
   ```

   On macOS/Linux:

   ```bash
   source .venv/bin/activate
   ```

3. Install dependencies.

   ```bash
   pip install -r requirements.txt
   ```

4. Add the dataset files under `data/` according to `data/README.md`.

5. Open the notebook.

   ```bash
   jupyter notebook notebooks/ktm_ridership_prediction.ipynb
   ```

## Future Improvements

- Add a clear dataset source, schema, and license note.
- Export final charts and model metrics into the README.
- Add a train/evaluation script outside the notebook.
- Add baseline models before advanced gradient-boosting models.
- Add time-based validation to avoid leakage.
- Package the best model behind a small FastAPI endpoint.
