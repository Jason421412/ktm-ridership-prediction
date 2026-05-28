# KTM Komuter Ridership Prediction

Regression-based machine learning workflow for hourly KTM Komuter ridership prediction.

## Project Overview

This repository documents a notebook-based ML workflow for forecasting KTM Komuter ridership using temporal, holiday, and station-related features. It is positioned as a reproducible data analytics project, not as a deployed forecasting service.

## Problem

Public transport demand changes by hour, day, station, route, and calendar context. A forecasting workflow can help explore questions such as:

- When are ridership peaks likely to happen?
- Which temporal and station features are useful predictors?
- How do simple baselines compare with more advanced tabular models?
- What limitations appear when dataset availability or licensing is unclear?

## Dataset / Source Note

The repository does not currently include the raw ridership dataset. Dataset files are expected under `data/`, while `data/README.md` documents why large or unclear-license data files are excluded.

TODO/risk note: before publishing data or final metrics, confirm the dataset source, license, schema, and whether redistribution is allowed.

## Preprocessing

The notebook is intended to cover:

- loading ridership records
- parsing date/time fields
- cleaning station and route values
- handling missing or inconsistent values
- preparing tabular features for regression models

## Feature Engineering

Feature groups documented or implied by the notebook setup include:

- hour of day
- day of week
- weekend/weekday indicators
- holiday-related context
- origin/destination or station-related categorical features
- route or direction context where available

## Models Compared

The dependency file supports experimentation with:

- scikit-learn regression models
- XGBoost
- LightGBM
- CatBoost

The README does not claim a winning model because final reproducible metrics and exported result tables are not currently tracked.

## Evaluation Metrics

Recommended metrics for this project:

- MAE
- RMSE
- R2

For time-related ridership data, future evaluation should use a time-aware split to reduce leakage risk.

## Results Summary

No final result table or chart is currently tracked in the repository. Add exported notebook outputs before making claims about model performance.

Suggested evidence to add:

- model comparison table with MAE/RMSE/R2
- actual vs predicted plot
- residual analysis
- feature importance chart
- baseline comparison

## How to Reproduce

Create and activate a virtual environment:

```bash
python -m venv .venv
```

On Windows PowerShell:

```powershell
.venv\Scripts\activate
```

On macOS/Linux:

```bash
source .venv/bin/activate
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Add the dataset files under `data/` according to [data/README.md](data/README.md), then open the notebook:

```bash
jupyter notebook notebooks/ktm_ridership_prediction.ipynb
```

Run the notebook cells from top to bottom after confirming local dataset paths.

## Limitations

- Raw data is not committed.
- Dataset source/license needs clearer documentation before public data sharing.
- The project is currently notebook-based and does not include a training script.
- Final model metrics are not exported to the README.
- Time leakage must be checked carefully before interpreting results.
- This is an analysis workflow, not a production prediction service.

## Future Improvements

- Add dataset source, schema, and license notes.
- Export final charts and metrics from the notebook.
- Add a reproducible `train.py` or `evaluate.py` script.
- Add baseline models before advanced gradient boosting.
- Use time-based validation.
- Add a small model card documenting intended use and limitations.
- Package a trained model only after dataset rights and evaluation are clear.

## Documentation

- [Data README](data/README.md)
- [Project decisions](docs/decisions.md)

## What I Learned

- How to frame transport-demand forecasting as supervised regression.
- Why temporal features and holiday context matter in ridership prediction.
- Why reproducible ML repositories need dataset, metric, and leakage documentation.
- Why public ML claims should be backed by tracked outputs, not notebook memory.
