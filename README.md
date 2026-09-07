# 🧠 Artificial Neural Network Projects

Welcome to my **Artificial Neural Network (ANN) Projects** repository.

This repository contains two end-to-end Deep Learning projects implemented using **Python, PyTorch, Pandas, NumPy, Scikit-learn, and Jupyter Notebook**.

The projects demonstrate the application of Artificial Neural Networks for both **Classification** and **Regression** problems.

---

## 📌 Projects Overview

| Project | Type | Dataset | Target | Result |
|--------|------|---------|--------|--------|
| 🍇 ANN Classification | Classification | Date Fruit Dataset | Class | **93.89% Accuracy** |
| ⚡ ANN Regression | Regression | Power Plant Dataset | PE | **R² = 0.9315** |

---

# 🍇 1. ANN Classification

### 📖 Description

This project uses an **Artificial Neural Network (ANN)** to classify different types of dates based on their extracted features.

The dataset contains **34 numerical features** and a categorical target variable named `Class`. The classification task contains **7 different classes**.

### 📊 Dataset

**Dataset:** Date Fruit Dataset

**File:** `DateFruit_Dataset.csv`

**Input:** 34 numerical features

**Target:** `Class`

### 🎯 Classes

The model classifies the date fruits into the following categories:

- BERHI
- DEGLET
- DOKOL
- IRAQI
- ROTANA
- SAFAVI
- SOGAY

### 🤖 Model

An Artificial Neural Network is implemented using **PyTorch**.

The model is trained for **100 epochs** using mini-batch training.

### 📈 Performance

**Classification Accuracy: 93.89%**

The model demonstrates strong performance in distinguishing between the different date fruit classes.

---

# ⚡ 2. ANN Regression

### 📖 Description

This project uses an **Artificial Neural Network (ANN)** to predict the electrical energy output of a power plant.

The model predicts **Power Plant Energy (PE)** using environmental and operational parameters.

### 📊 Dataset

**Dataset:** Power Plant Dataset

**File:** `powerplant_data.csv`

### 🔢 Features

The dataset contains the following input features:

- **AT** – Ambient Temperature
- **V** – Vacuum
- **AP** – Ambient Pressure
- **RH** – Relative Humidity

### 🎯 Target

- **PE** – Produced Energy

### 🤖 Model

An Artificial Neural Network is implemented using **PyTorch**.

The data is standardized using **StandardScaler** before training.

The dataset is divided into training and testing sets using an **80:20 split**.

### 📉 Loss Function

**Mean Squared Error (MSE)** is used as the regression loss function.

### 📈 Performance

- **Training MSE:** 21.14
- **Testing MSE:** 19.59
- **R² Score:** 0.9315

The model also compares predicted values with actual values to evaluate regression performance.

---

# 🛠️ Technologies Used

- 🐍 Python
- 🔥 PyTorch
- 🐼 Pandas
- 🔢 NumPy
- 📊 Scikit-learn
- 📈 Matplotlib
- 📓 Jupyter Notebook

---

# 📁 Repository Structure

```text
ANN-Projects/
│
├── ANN_Classification (1).ipynb
├── ANN_Regression (1).ipynb
├── DateFruit_Dataset.csv
└── powerplant_data.csv
