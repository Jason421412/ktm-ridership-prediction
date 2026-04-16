# KTM Komuter Ridership Prediction

## 📌 Introduction
This project aims to predict the hourly origin-destination ridership of KTM Komuter stations using machine learning techniques. Accurate ridership prediction helps in optimizing train schedules, resource allocation, and overall commuter experience.

## 🎯 Problem Statement
Public transportation services face challenges in matching capacity with demand. Overcrowding during peak hours and underutilization during off-peak hours lead to inefficiencies. This project solves this by treating ridership prediction as a **Regression Problem**, utilizing temporal and holiday features to forecast passenger volume.

## 🛠 Tech Stack
- **Data Manipulation:** `pandas`, `numpy`
- **Visualization:** `matplotlib`, `seaborn`, `plotly`
- **Machine Learning:** `scikit-learn`, `XGBoost`, `LightGBM`, `CatBoost`
- **Feature Engineering:** `holidays`

## 📂 Repository Structure
```text
ktm-ridership-prediction/
├── data/                  # Dataset files (excluded via .gitignore)
├── images/                # Visualizations and project images
├── notebooks/             # Jupyter notebooks
│   └── ktm_ridership_prediction.ipynb
├── .gitignore             # Ignored files
├── README.md              # Project documentation
└── requirements.txt       # Python dependencies
```

## 🚀 Getting Started

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/ktm-ridership-prediction.git
   cd ktm-ridership-prediction
   ```

2. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Run the Notebook**
   Open `notebooks/ktm_ridership_prediction.ipynb` in Jupyter Notebook or Google Colab.
