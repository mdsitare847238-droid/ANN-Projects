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
