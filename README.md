# CSE 158 Assignment 2 - Predicting Workout Duration

Machine Learning project using EndoMondo fitness tracking data to predict total workout duration from early sensor readings.

## Project Overview

This project builds a machine learning pipeline to predict workout duration using:
- **Dataset**: EndoMondo fitness tracking data with sequential heart-rate and speed measurements
- **Task**: Predict total workout duration (minutes) using only the first 5 minutes of sensor data
- **Models**: Linear Regression and Random Forest Regressor

## Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/aaldelaimy/158-assignment-2.git
cd 158-assignment-2
```

### 2. Create Virtual Environment

```bash
python3 -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Set Up Jupyter Kernel

```bash
python -m ipykernel install --user --name=cse158-venv --display-name="Python (CSE 158 venv)"
```

### 5. Add Data Files

The dataset files are **too large for GitHub** (6.1GB and 9.9GB). You need to:

1. Download the EndoMondo dataset files:
   - `endomondoHR.json`
   - `endomondoMeta.json`

2. Place them in the `data/` directory:
   ```
   158-assignment-2/
   └── data/
       ├── endomondoHR.json
       └── endomondoMeta.json
   ```

### 6. Run the Notebook

```bash
jupyter notebook notebook.ipynb
# or
jupyter lab
```

Then select the **"Python (CSE 158 venv)"** kernel and run all cells.

## Project Structure

```
├── data/                    # Dataset directory (files not included in repo)
│   ├── endomondoHR.json    # Heart rate data (6.1GB)
│   └── endomondoMeta.json  # Metadata (9.9GB)
├── venv/                    # Virtual environment (not in repo)
├── notebook.ipynb           # Main analysis notebook
├── requirements.txt         # Python dependencies
├── .gitignore              # Git ignore rules
└── README.md               # This file
```

## Dependencies

- Python 3.13+
- numpy >= 1.26.0
- pandas >= 2.0.0
- matplotlib >= 3.7.0
- seaborn >= 0.13.0
- scikit-learn >= 1.3.0
- jupyter >= 1.0.0
- ipykernel >= 6.25.0

## Key Features

1. **Exploratory Data Analysis**: Distribution of sports and workout durations
2. **Feature Engineering**: Extract statistical features from early-workout sequences
3. **Baseline Models**: Global mean and sport-specific mean predictions
4. **Machine Learning Models**: Linear Regression and Random Forest
5. **Evaluation**: MAE, RMSE, and R² metrics with error analysis by sport

## Results

The Random Forest model achieves the best performance, demonstrating that early heart-rate and speed patterns contain useful predictive information about total workout duration.

## Author

Ayoob Aldelaimy

## Course

CSE 158 - Machine Learning

