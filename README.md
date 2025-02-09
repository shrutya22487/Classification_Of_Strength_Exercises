# 🏋️ Strength Exercise Classification and Repetition Counting

## 📌 Overview

This project leverages wearable sensor data and machine learning to classify strength exercises and count repetitions accurately. Using MetaMotion sensors, we analyze accelerometer and gyroscope data to develop supervised learning models capable of recognizing different exercises and tracking repetitions.

## 📂 Repository Structure

```
├── 📜 LICENSE
├── ⚙️ Makefile           <- Commands for data processing and model training.
├── 📖 README.md          <- Project documentation.
├── 📂 data
│   ├── 🌍 external       <- Third-party data sources.
│   ├── 🛠️ interim        <- Intermediate transformed data.
│   ├── 📊 processed      <- Final datasets used for modeling.
│   └── 🗄️ raw            <- Original unprocessed data.
│
├── 📄 docs               <- Documentation and Sphinx files.
│
├── 🤖 models             <- Trained models and their predictions.
│
├── 📓 notebooks          <- Jupyter notebooks for analysis and visualization.
│
├── 📚 references         <- Manuals and explanatory materials.
│
├── 📑 reports            <- Generated analysis, including figures and summaries.
│   └── 📉 figures        <- Visual results.
│
├── 📋 requirements.txt   <- Dependencies required for the project.
│
├── 🏗️ setup.py           <- Installation script for the project.
├── 📁 src                <- Source code.
│   ├── 🛠️ __init__.py    <- Makes src a module.
│   ├── 📥 data           <- Scripts for data acquisition and processing.
│   ├── 🎯 features       <- Feature extraction scripts.
│   ├── 🔬 models         <- Training and prediction scripts.
│   └── 📊 visualization  <- Visualization scripts.
│
└── 🧪 tox.ini            <- Configuration for testing.
```

## 📊 Dataset

- **📌 Source:** Data collected via MetaMotion sensors over 20 days from five participants.
- **📈 Features:** Includes accelerometer (acc\_x, acc\_y, acc\_z) and gyroscope (gyr\_x, gyr\_y, gyr\_z) readings.
- **🛠️ Preprocessing:**
  - 🔄 Data aggregated into 0.2-second intervals.
  - 🚨 Outliers removed using Chauvenet’s Criterion.
  - 📝 Missing values handled via interpolation.
  - 🎛️ Noise reduced using a Butterworth low-pass filter.
  - 🔽 Dimensionality reduction via PCA.

## 🏗️ Methodology

1. **📊 Exploratory Data Analysis (EDA)**
   - 📉 Heatmaps, box plots, and correlation matrices for insights.
2. **🛠️ Feature Engineering**
   - 🔍 Aggregated, temporal, and frequency-based features.
   - 🎼 Fourier transformations and clustering applied.
3. **🔬 Modeling**
   - 🏆 Models tested: Random Forest, Neural Network, KNN, Decision Tree, Naïve Bayes.
   - 🏅 Best model: Random Forest (98.51% accuracy after hyperparameter tuning).
4. **🔢 Repetition Counting**
   - 📈 Custom algorithm using peak detection in sensor data.

## 📊 Results

- **🏆 Model Accuracy:**
  - 🌲 Random Forest: 98.51%
  - 🧠 Neural Network: 96.29%
  - 🌳 Decision Tree: 96.87%
- **🔢 Repetition Counting:** Achieved a mean absolute error of 0.88 repetitions per set.

## ⚙️ Installation

### 📌 Prerequisites

- 🐍 Python 3.8+
- Install dependencies:
  ```bash
  pip install -r requirements.txt
  ```
- Run setup:
  ```bash
  python setup.py install
  ```

## 🚀 Usage

- To preprocess data:
  ```bash
  python src/data/make_dataset.py
  ```
- To extract features:
  ```bash
  python src/features/build_features.py
  ```
- To train a model:
  ```bash
  python src/models/train_model.py
  ```
- To make predictions:
  ```bash
  python src/models/predict_model.py
  ```
- To visualize results:
  ```bash
  python src/visualization/visualize.py
  ```

## 👨‍💻 Contributors

- **Grishma Bellani** - 📊 Data Visualization, Feature Engineering, Neural Network.
- **Riya Gupta** - 📡 Data Collection, 🌲 Random Forest, 🔢 Repetition Counting Algorithm.
- **Shreyansh Srivastav** - 🛠️ Data Preprocessing, 🔬 Predictive Modeling.
- **Shrutya Chawla** - 🎼 Fourier Transformation, 🔍 Clustering, 🔬 Predictive Modeling.
- **Vimansh Mahajan** - 📡 Data Collection, 🎼 Fourier Transformation, 🔢 Repetition Counting.

## 📚 References

- [📡 MetaMotion Sensors](https://mbientlab.com/metamotions/)
- [🧠 Machine Learning for Strength Exercises](https://ieeexplore.ieee.org/document/8526202)

