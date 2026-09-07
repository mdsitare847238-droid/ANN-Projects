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


# 🧠 ANN Regression — Power Plant Energy Prediction

## 📌 Project Overview

This project implements an **Artificial Neural Network (ANN) Regression model** using **PyTorch** to predict the electrical energy output of a power plant.

The model learns the relationship between environmental conditions and the amount of electrical energy produced by the power plant.

---

## 🎯 Objective

The main objective of this project is to build an ANN-based regression model that can predict **Power Plant Energy Output (PE)** using different environmental and operational parameters.

The project covers the complete machine learning workflow, from data preprocessing to model evaluation.

---

## 📊 Dataset

The project uses the **Combined Cycle Power Plant dataset** stored in:

**`powerplant_data.csv`**

The dataset contains environmental conditions recorded from a power plant along with the corresponding electrical energy output.

---

## 📥 Input Features

| Feature | Description         |
| ------- | ------------------- |
| **AT**  | Ambient Temperature |
| **V**   | Exhaust Vacuum      |
| **AP**  | Ambient Pressure    |
| **RH**  | Relative Humidity   |

---

## 🎯 Target Variable

| Target | Description                |
| ------ | -------------------------- |
| **PE** | Produced Electrical Energy |

The ANN model predicts the value of **PE** based on the four input features.

---

## 🧠 What is ANN Regression?

**Artificial Neural Network Regression** is a deep learning approach used to predict continuous numerical values.

In this project, the ANN learns complex relationships between:

**Ambient Conditions → Power Plant Energy Output**

The network consists of an input layer, hidden layers, and an output layer.

---

## 🔄 Project Workflow

The project follows these steps:

1. Dataset Loading
2. Dataset Exploration
3. Data Preprocessing
4. Feature and Target Selection
5. Train-Test Split
6. Feature Scaling
7. Conversion into PyTorch Tensors
8. ANN Model Construction
9. Loss Function Definition
10. Optimizer Selection
11. Model Training
12. Prediction
13. Model Evaluation

---

## 🏗️ ANN Architecture

The regression model consists of:

* **Input Layer:** 4 neurons
* **Hidden Layer 1:** 6 neurons
* **Activation:** ReLU
* **Hidden Layer 2:** 6 neurons
* **Activation:** ReLU
* **Output Layer:** 1 neuron

### Architecture

**4 Input Features → 6 Neurons → 6 Neurons → 1 Output**

---

## ⚙️ Model Configuration

| Parameter                | Value              |
| ------------------------ | ------------------ |
| Framework                | PyTorch            |
| Problem Type             | Regression         |
| Input Features           | 4                  |
| Hidden Layers            | 2                  |
| Neurons per Hidden Layer | 6                  |
| Activation Function      | ReLU               |
| Loss Function            | Mean Squared Error |
| Optimizer                | Adam               |
| Learning Rate            | 0.001              |
| Epochs                   | 100                |
| Train-Test Split         | 80:20              |
| Feature Scaling          | StandardScaler     |

---

## 📏 Data Preprocessing

### Feature Scaling

The input features are standardized using **StandardScaler**.

Feature scaling helps the neural network train more effectively when different input features have different numerical ranges.

### Train-Test Split

The dataset is divided into:

* **80% Training Data**
* **20% Testing Data**

The training data is used to learn patterns, while the testing data is used to evaluate the model on unseen data.

---

## 📉 Loss Function

The model uses **Mean Squared Error (MSE)** as the loss function.

MSE measures the average squared difference between the actual and predicted energy values.

A lower MSE indicates better prediction performance.

---

## ⚡ Optimizer

The **Adam Optimizer** is used to update the weights and biases of the neural network during training.

### Learning Rate

**0.001**

Adam helps the model efficiently minimize the loss during the training process.

---

## 🏋️ Model Training

The ANN model is trained for **100 epochs**.

During training, the following process is repeated:

**Forward Propagation → Loss Calculation → Backpropagation → Weight Update**

As training progresses, the model learns the relationship between the input environmental parameters and power generation.

---

## 📊 Model Evaluation

The regression model is evaluated using:

### Mean Squared Error (MSE)

Measures the average squared difference between actual and predicted values.

### R² Score

Measures how well the model explains the variation in the target variable.

An R² value closer to **1.0** indicates stronger predictive performance.

---

## 📈 Results

| Evaluation Metric | Result |
| ----------------- | -----: |
| **Training MSE**  |  21.14 |
| **Testing MSE**   |  19.59 |
| **R² Score**      | 0.9315 |

### Performance Summary

The model achieved an **R² Score of 0.9315**, indicating that the ANN is able to explain approximately **93.15% of the variation** in power plant energy output on the test data.

---

## 💡 Key Learning Outcomes

Through this project, the following concepts were implemented:

* Artificial Neural Network Regression
* PyTorch
* Neural Network Architecture
* ReLU Activation
* Forward Propagation
* Backpropagation
* Gradient-Based Optimization
* Adam Optimizer
* Mean Squared Error
* R² Score
* Feature Scaling
* Train-Test Split
* PyTorch Tensors
* Regression Model Evaluation

---

## 🌍 Real-World Applications

ANN-based energy prediction can be useful for:

* Power generation forecasting
* Energy management
* Plant operation planning
* Resource optimization
* Power plant efficiency analysis
* Predictive maintenance systems
* Smart energy management

---

## 🚀 Future Improvements

The model can be further improved using:

* Hyperparameter tuning
* Additional hidden layers
* Dropout
* Batch Normalization
* Early Stopping
* Learning Rate Scheduling
* Cross-Validation
* Hyperparameter optimization
* Model deployment using Flask or FastAPI
* Web-based prediction interface

---

## 🛠️ Technologies Used

* **Python**
* **PyTorch**
* **Pandas**
* **NumPy**
* **Scikit-learn**
* **Jupyter Notebook**
* **Matplotlib**

---

## 📁 Project Structure

```text
ANN-Projects/
│
├── ANN_Regression.ipynb
├── powerplant_data.csv
└── README.md
```

---

## 📂 Project Files

### `ANN_Regression.ipynb`

Jupyter Notebook containing the complete ANN Regression implementation and model evaluation.

### `powerplant_data.csv`

Dataset containing power plant environmental parameters and produced electrical energy.

### `README.md`

Project documentation containing the project overview, methodology, architecture, results, and technologies used.

---

## ⭐ Project Highlights

* ANN Regression using PyTorch
* Real-world Power Plant dataset
* Feature scaling using StandardScaler
* Two hidden layers
* ReLU activation
* Adam optimization
* MSE-based training
* R²-based evaluation
* Complete machine learning workflow

---

## 📌 Conclusion

This project demonstrates the practical implementation of an **Artificial Neural Network for Regression** using PyTorch.

The model successfully learns the relationship between environmental conditions and power plant energy output, achieving an **R² Score of 0.9315** on the test data.

The project provides hands-on experience with **deep learning, ANN architecture, regression, PyTorch, data preprocessing, model training, and performance evaluation**.

---

## 👨‍💻 Author

**MD SITARE**

*Aspiring Data Scientist | Machine Learning Enthusiast | Python Developer*
