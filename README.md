# 🧠 Artificial Neural Network Projects

<p align="center">
  <b>End-to-End Deep Learning Projects using PyTorch</b>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.x-blue?logo=python">
  <img src="https://img.shields.io/badge/PyTorch-Deep%20Learning-ee4c2c?logo=pytorch">
  <img src="https://img.shields.io/badge/Scikit--learn-Machine%20Learning-orange?logo=scikit-learn">
  <img src="https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter">
  <img src="https://img.shields.io/badge/Status-Completed-success">
</p>

---

## 🚀 About This Repository

This repository contains two practical **Artificial Neural Network (ANN)** projects developed using **Python and PyTorch**.

The projects demonstrate how neural networks can be applied to two fundamental Machine Learning problems:

- 🍇 **Classification** — identifying different varieties of dates
- ⚡ **Regression** — predicting electrical energy output from a power plant

Both projects follow an end-to-end Machine Learning workflow:

**Data → Preprocessing → Feature Scaling → Train/Test Split → ANN Architecture → Training → Evaluation → Performance Analysis**

---

# 📌 Projects Overview

| Project | Problem Type | Dataset | Target | Performance |
|---|---|---|---|---|
| 🍇 Date Fruit Classification | Classification | Date Fruit Dataset | `Class` | **93.89% Accuracy** |
| ⚡ Power Plant Prediction | Regression | Power Plant Dataset | `PE` | **R² = 0.9315** |

---

# 🍇 Project 01 — Date Fruit Classification

## 🎯 Problem Statement

The objective of this project is to build an Artificial Neural Network capable of classifying different varieties of dates based on their numerical characteristics.

The model learns patterns from the input features and predicts the corresponding date variety.

## 📊 Dataset

**Dataset:** Date Fruit Dataset

**File:** `DateFruit_Dataset.csv`

- 34 numerical input features
- 7 target classes
- Multiclass classification problem

### Classes

- BERHI
- DEGLET
- DOKOL
- IRAQI
- ROTANA
- SAFAVI
- SOGAY

## 🧠 Model

A fully connected **Artificial Neural Network (ANN)** was implemented using **PyTorch**.

### Training Pipeline

```text
Raw Dataset
     ↓
Data Preprocessing
     ↓
Feature / Target Separation
     ↓
Train-Test Split
     ↓
Feature Scaling
     ↓
PyTorch Tensor Conversion
     ↓
Artificial Neural Network
     ↓
Model Training
     ↓
Prediction
     ↓
Performance Evaluation


````markdown
# ⚡ Project 02 — Power Plant Energy Prediction

## 🎯 Problem Statement

The objective of this project is to develop an **Artificial Neural Network (ANN)** capable of predicting the electrical energy output of a power plant based on environmental and operational parameters.

This project is formulated as a **supervised regression problem**, where the model learns the relationship between multiple input variables and the continuous target variable **Produced Energy (`PE`)**.

The goal is to build a neural network that can accurately predict energy output for previously unseen data.

---

## 📊 Dataset

**Dataset:** Power Plant Dataset

**File:** `powerplant_data.csv`

The dataset contains four input features that influence the electrical energy output of the power plant.

### Input Features

| Feature | Description |
|---|---|
| `AT` | Ambient Temperature |
| `V` | Exhaust Vacuum |
| `AP` | Ambient Pressure |
| `RH` | Relative Humidity |

### Target Variable

```text
PE → Produced Energy
````

---

## 🔄 Regression Workflow

The complete Machine Learning workflow used in this project:

```text
Raw Dataset
     ↓
Data Preprocessing
     ↓
Feature / Target Separation
     ↓
Train-Test Split (80/20)
     ↓
Feature Scaling using StandardScaler
     ↓
PyTorch Tensor Conversion
     ↓
Artificial Neural Network
     ↓
Forward Propagation
     ↓
MSE Loss Calculation
     ↓
Backpropagation
     ↓
Adam Optimization
     ↓
Model Training
     ↓
Prediction
     ↓
MSE & R² Evaluation
```

---

## 🧠 Model

A fully connected **Artificial Neural Network (ANN)** was implemented using **PyTorch**.

The network consists of an input layer, two hidden layers, and one output neuron for continuous energy prediction.

### Architecture

```text
Input Layer
   │
   ▼
4 Input Features
   │
   ▼
6 Neurons
   │
  ReLU
   │
   ▼
6 Neurons
   │
  ReLU
   │
   ▼
1 Output Neuron
   │
   ▼
Produced Energy (PE)
```

---

## ⚙️ Training Configuration

| Parameter           | Value          |
| ------------------- | -------------- |
| Framework           | PyTorch        |
| Problem Type        | Regression     |
| Input Features      | 4              |
| Hidden Layer 1      | 6 Neurons      |
| Hidden Layer 2      | 6 Neurons      |
| Activation Function | ReLU           |
| Output Neurons      | 1              |
| Loss Function       | MSELoss        |
| Optimizer           | Adam           |
| Learning Rate       | 0.001          |
| Epochs              | 100            |
| Train/Test Split    | 80/20          |
| Feature Scaling     | StandardScaler |

---

## 📉 Loss Function

Since this project is a regression problem, **Mean Squared Error (MSE)** is used as the loss function.

MSE measures the average squared difference between the actual and predicted values.

```text
MSE = Average((Actual - Predicted)²)
```

During training, the model minimizes the MSE loss using **backpropagation and the Adam optimizer**.

---

## 📈 Model Evaluation

The trained ANN model is evaluated using two important regression metrics.

### 1. Mean Squared Error (MSE)

MSE measures the prediction error between actual and predicted energy output.

A lower MSE indicates better prediction performance.

### 2. R² Score

R² measures how well the model explains the variation in the target variable.

A value closer to **1.0** indicates stronger predictive performance.

---

## 🏆 Results

The trained ANN regression model achieved the following performance:

| Metric       |     Result |
| ------------ | ---------: |
| Training MSE |  **21.14** |
| Testing MSE  |  **19.59** |
| R² Score     | **0.9315** |

### 📌 Performance Interpretation

The model achieved an **R² score of 0.9315**, indicating that approximately **93.15% of the variance in the produced energy output is explained by the model on the test dataset**.

The testing MSE of **19.59** demonstrates that the model is capable of producing reasonably accurate predictions on unseen data.

---

## 💡 Key Learning Outcomes

Through this project, I gained practical experience in:

* Building ANN regression models using PyTorch
* Preparing numerical datasets for Deep Learning
* Separating features and target variables
* Applying train-test splitting
* Standardizing input features
* Converting data into PyTorch tensors
* Designing fully connected neural networks
* Using ReLU activation functions
* Implementing MSE loss
* Applying the Adam optimizer
* Performing forward and backward propagation
* Evaluating regression models using MSE and R²
* Interpreting model performance

---

## 🌍 Real-World Relevance

Energy production forecasting is an important application in the **power and energy sector**.

Accurate prediction of power output can support:

* ⚡ Energy production planning
* 🏭 Power plant monitoring
* 📊 Operational decision-making
* 📈 Resource optimization
* 🔋 Energy management
* 💰 Improved operational efficiency

This project demonstrates how **Deep Learning can be applied to a real-world numerical prediction problem**.

---

## 🚀 Future Improvements

The current model can be further improved using:

* Hyperparameter tuning
* Cross-validation
* Early stopping
* Dropout regularization
* Batch normalization
* Learning-rate scheduling
* Different ANN architectures
* Additional hidden layers
* Training and validation loss visualization
* Actual vs Predicted visualization
* Model checkpointing
* Hyperparameter experimentation
* Model deployment using Flask or FastAPI

---

## 🛠️ Technologies Used

* **Python**
* **PyTorch**
* **Pandas**
* **NumPy**
* **Scikit-learn**
* **Jupyter Notebook**

---

## 📁 Project File

```text
ANN_Regression.ipynb
powerplant_data.csv
```

---

## ✅ Conclusion

This project successfully demonstrates the application of an **Artificial Neural Network to a real-world regression problem**.

The model uses **Ambient Temperature (`AT`), Exhaust Vacuum (`V`), Ambient Pressure (`AP`), and Relative Humidity (`RH`)** to predict the electrical energy output (`PE`) of a power plant.

By using **PyTorch, StandardScaler, MSELoss, and the Adam optimizer**, the model achieved a **Testing MSE of 19.59** and an **R² score of 0.9315**.

The project provided practical experience in the complete Deep Learning workflow:

**Data → Preprocessing → Scaling → Tensor Conversion → ANN Design → Training → Optimization → Prediction → Evaluation**

Overall, this project demonstrates the ability to implement a complete **ANN-based regression solution using PyTorch**, while applying Deep Learning concepts to a practical energy prediction problem.

```






