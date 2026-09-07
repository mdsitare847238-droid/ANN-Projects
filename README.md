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

# 🍇 Project 01 — Date Fruit ANN Classification

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

# 🧠Project2 — Power Plant Energy ANN Regression

````markdown
# ⚡ Project 02 — Power Plant Energy Prediction using ANN

## 🎯 Problem Statement

The objective of this project is to develop an **Artificial Neural Network (ANN)** capable of predicting the electrical energy output of a power plant based on environmental and operational parameters.

This project is formulated as a **supervised regression problem**, where the model learns the relationship between multiple input variables and the continuous target variable **Produced Energy (`PE`)**.

The goal is to build a neural network that can accurately predict energy output for previously unseen data.

---

# 📊 Dataset

**Dataset:** Power Plant Dataset

**File:** `powerplant_data.csv`

The dataset contains four independent variables that influence the electrical energy output of the power plant.

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

# 🔄 Regression Workflow

The complete machine learning pipeline used in this project is:

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
Prediction on Test Data
     ↓
MSE & R² Evaluation
```

---

# 🧠 Model Architecture

A fully connected **Artificial Neural Network (ANN)** was implemented using **PyTorch**.

The network consists of an input layer, two hidden layers, and a single output neuron for continuous energy prediction.

### Architecture

```text
Input Layer
    │
    ▼
4 Input Features
    │
    ▼
Fully Connected Layer
6 Neurons
    │
   ReLU
    │
    ▼
Fully Connected Layer
6 Neurons
    │
   ReLU
    │
    ▼
Output Layer
1 Neuron
    │
    ▼
Produced Energy (PE)
```

---

# ⚙️ Model Configuration

| Parameter           | Configuration  |
| ------------------- | -------------- |
| Framework           | PyTorch        |
| Problem Type        | Regression     |
| Input Features      | 4              |
| Hidden Layer 1      | 6 Neurons      |
| Hidden Layer 2      | 6 Neurons      |
| Activation Function | ReLU           |
| Output Layer        | 1 Neuron       |
| Loss Function       | MSELoss        |
| Optimizer           | Adam           |
| Learning Rate       | 0.001          |
| Training Epochs     | 100            |
| Train/Test Split    | 80/20          |
| Feature Scaling     | StandardScaler |

---

# 💻 Complete Python Code

## 1. Import Required Libraries

```python
import pandas as pd
import numpy as np
import torch
import torch.nn as nn

from sklearn.model_selection import train_test_split
from sklearn.preprocessing import StandardScaler
from sklearn.metrics import mean_squared_error, r2_score
```

---

## 2. Load Dataset

```python
df = pd.read_csv("powerplant_data.csv")

df.head()
```

---

## 3. Dataset Information

```python
print("Dataset Shape:")
print(df.shape)

print("\nDataset Information:")
print(df.info())

print("\nMissing Values:")
print(df.isnull().sum())
```

---

## 4. Separate Features and Target

The four input features are:

* `AT`
* `V`
* `AP`
* `RH`

The target variable is:

* `PE`

```python
X = df.drop("PE", axis=1)

y = df["PE"]
```

---

## 5. Train-Test Split

The dataset is divided into:

* **80% Training Data**
* **20% Testing Data**

```python
X_train, X_test, y_train, y_test = train_test_split(
    X,
    y,
    test_size=0.20,
    random_state=42
)
```

---

## 6. Feature Scaling

`StandardScaler` is used to standardize the input features.

```python
scaler = StandardScaler()

X_train_scaled = scaler.fit_transform(X_train)

X_test_scaled = scaler.transform(X_test)
```

---

## 7. Convert Data into PyTorch Tensors

```python
X_train_tensor = torch.tensor(
    X_train_scaled,
    dtype=torch.float32
)

X_test_tensor = torch.tensor(
    X_test_scaled,
    dtype=torch.float32
)
```

Convert target values:

```python
y_train_tensor = torch.tensor(
    y_train.values,
    dtype=torch.float32
).reshape(-1, 1)

y_test_tensor = torch.tensor(
    y_test.values,
    dtype=torch.float32
).reshape(-1, 1)
```

---

# 🧠 8. Build ANN Model

The ANN contains:

* Input layer → 4 features
* Hidden layer 1 → 6 neurons
* Hidden layer 2 → 6 neurons
* Output layer → 1 neuron

```python
class ANN(nn.Module):

    def __init__(self):

        super(ANN, self).__init__()

        self.model = nn.Sequential(

            nn.Linear(X_train.shape[1], 6),

            nn.ReLU(),

            nn.Linear(6, 6),

            nn.ReLU(),

            nn.Linear(6, 1)
        )

    def forward(self, x):

        return self.model(x)
```

---

# ⚙️ 9. Initialize Model, Loss Function and Optimizer

```python
model = ANN()

criterion = nn.MSELoss()

optimizer = torch.optim.Adam(
    model.parameters(),
    lr=0.001
)
```

---

# 🚀 10. Train the ANN Model

The model is trained for **100 epochs**.

```python
epochs = 100

train_losses = []

for epoch in range(epochs):

    # Training mode
    model.train()

    # Forward propagation
    predictions = model(X_train_tensor)

    # Calculate loss
    loss = criterion(
        predictions,
        y_train_tensor
    )

    # Clear previous gradients
    optimizer.zero_grad()

    # Backpropagation
    loss.backward()

    # Update weights
    optimizer.step()

    # Store loss
    train_losses.append(loss.item())

    # Display loss
    if (epoch + 1) % 10 == 0:

        print(
            f"Epoch [{epoch + 1}/{epochs}], "
            f"Loss: {loss.item():.4f}"
        )
```

---

# 🔮 11. Make Predictions

After training, the model is evaluated on both training and testing data.

```python
model.eval()

with torch.no_grad():

    train_predictions = model(
        X_train_tensor
    )

    test_predictions = model(
        X_test_tensor
    )
```

---

# 🔄 12. Convert Predictions to NumPy

```python
train_predictions = train_predictions.numpy()

test_predictions = test_predictions.numpy()

y_train_actual = y_train_tensor.numpy()

y_test_actual = y_test_tensor.numpy()
```

---

# 📉 13. Calculate Mean Squared Error

```python
train_mse = mean_squared_error(
    y_train_actual,
    train_predictions
)

test_mse = mean_squared_error(
    y_test_actual,
    test_predictions
)

print("Training MSE:", train_mse)

print("Testing MSE:", test_mse)
```

---

# 📈 14. Calculate R² Score

```python
r2 = r2_score(
    y_test_actual,
    test_predictions
)

print("R² Score:", r2)
```

---

# 📋 15. Compare Actual vs Predicted Values

```python
result = pd.DataFrame({

    "Actual PE":
        y_test_actual.flatten(),

    "Predicted PE":
        test_predictions.flatten()
})

result.head(10)
```

---

# 📌 Complete Code — Single Cell

The complete ANN regression implementation can also be executed as one Python script/cell:

```python
import pandas as pd
import numpy as np
import torch
import torch.nn as nn

from sklearn.model_selection import train_test_split
from sklearn.preprocessing import StandardScaler
from sklearn.metrics import mean_squared_error, r2_score


# Load Dataset
df = pd.read_csv("powerplant_data.csv")

print(df.shape)
print(df.info())
print(df.isnull().sum())


# Features and Target
X = df.drop("PE", axis=1)

y = df["PE"]


# Train-Test Split
X_train, X_test, y_train, y_test = train_test_split(
    X,
    y,
    test_size=0.20,
    random_state=42
)


# Feature Scaling
scaler = StandardScaler()

X_train_scaled = scaler.fit_transform(X_train)

X_test_scaled = scaler.transform(X_test)


# Convert Features to PyTorch Tensor
X_train_tensor = torch.tensor(
    X_train_scaled,
    dtype=torch.float32
)

X_test_tensor = torch.tensor(
    X_test_scaled,
    dtype=torch.float32
)


# Convert Target to PyTorch Tensor
y_train_tensor = torch.tensor(
    y_train.values,
    dtype=torch.float32
).reshape(-1, 1)

y_test_tensor = torch.tensor(
    y_test.values,
    dtype=torch.float32
).reshape(-1, 1)


# ANN Model
class ANN(nn.Module):

    def __init__(self):

        super(ANN, self).__init__()

        self.model = nn.Sequential(

            nn.Linear(X_train.shape[1], 6),

            nn.ReLU(),

            nn.Linear(6, 6),

            nn.ReLU(),

            nn.Linear(6, 1)
        )

    def forward(self, x):

        return self.model(x)


# Create Model
model = ANN()


# Loss Function
criterion = nn.MSELoss()


# Optimizer
optimizer = torch.optim.Adam(
    model.parameters(),
    lr=0.001
)


# Training
epochs = 100

train_losses = []

for epoch in range(epochs):

    model.train()

    predictions = model(X_train_tensor)

    loss = criterion(
        predictions,
        y_train_tensor
    )

    optimizer.zero_grad()

    loss.backward()

    optimizer.step()

    train_losses.append(loss.item())

    if (epoch + 1) % 10 == 0:

        print(
            f"Epoch [{epoch + 1}/{epochs}], "
            f"Loss: {loss.item():.4f}"
        )


# Evaluation
model.eval()

with torch.no_grad():

    train_predictions = model(
        X_train_tensor
    )

    test_predictions = model(
        X_test_tensor
    )


# Convert to NumPy
train_predictions = train_predictions.numpy()

test_predictions = test_predictions.numpy()

y_train_actual = y_train_tensor.numpy()

y_test_actual = y_test_tensor.numpy()


# Calculate MSE
train_mse = mean_squared_error(
    y_train_actual,
    train_predictions
)

test_mse = mean_squared_error(
    y_test_actual,
    test_predictions
)


# Calculate R²
r2 = r2_score(
    y_test_actual,
    test_predictions
)


# Print Results
print("\nModel Performance")

print("Training MSE:", train_mse)

print("Testing MSE:", test_mse)

print("R² Score:", r2)


# Actual vs Predicted
result = pd.DataFrame({

    "Actual PE":
        y_test_actual.flatten(),

    "Predicted PE":
        test_predictions.flatten()
})

print("\nActual vs Predicted:")

print(result.head(10))
```

---

# 📉 Loss Function

Since this is a regression problem, **Mean Squared Error (MSE)** is used as the loss function.

MSE measures the average squared difference between the actual and predicted energy values.

```text
MSE = Average((Actual - Predicted)²)
```

During training, the ANN minimizes this loss using **backpropagation and the Adam optimizer**.

---

# 📈 Model Evaluation

The trained model is evaluated using:

## 1. Mean Squared Error (MSE)

MSE measures the prediction error of the regression model.

A lower MSE generally indicates better prediction performance.

## 2. R² Score

The R² score measures how well the model explains the variation in the target variable.

A value closer to **1.0** indicates stronger predictive performance.

---

# 🏆 Results

The ANN regression model achieved the following results:

| Metric       |     Result |
| ------------ | ---------: |
| Training MSE |  **21.14** |
| Testing MSE  |  **19.59** |
| R² Score     | **0.9315** |

### 📌 Performance Interpretation

The model achieved an **R² score of 0.9315**, indicating that approximately **93.15% of the variance in the produced energy output is explained by the model on the test dataset**.

The testing MSE of **19.59** demonstrates that the model is capable of producing reasonably accurate predictions on unseen data.

---

# 💡 Key Learning Outcomes

Through this project, I gained practical experience in:

* Building ANN regression models using PyTorch
* Preparing numerical datasets for Deep Learning
* Separating independent and dependent variables
* Applying train-test splitting
* Standardizing input features
* Working with PyTorch tensors
* Designing fully connected neural networks
* Using ReLU activation functions
* Implementing MSE loss
* Applying the Adam optimizer
* Performing forward and backward propagation
* Evaluating regression models using MSE and R²
* Interpreting model performance

---

# 🌍 Business / Real-World Relevance

Energy production forecasting is an important problem in the power and energy sector.

Accurate prediction of power output can support:

* ⚡ Energy production planning
* 📊 Operational decision-making
* 🏭 Power plant monitoring
* 📈 Resource optimization
* 🔋 Energy management
* 💰 Improved operational efficiency

This project demonstrates how **Deep Learning techniques can be applied to a real-world numerical prediction problem**.

---

# 🚀 Future Improvements

The model can be further improved by implementing:

* Hyperparameter tuning
* Cross-validation
* Early stopping
* Dropout
* Batch normalization
* Learning-rate scheduling
* Additional hidden layers
* Different activation functions
* Training/validation loss visualization
* Actual vs Predicted visualization
* Model checkpointing
* Hyperparameter experimentation
* Deployment using Flask or FastAPI

---

# 🛠️ Technologies Used

* Python
* PyTorch
* Pandas
* NumPy
* Scikit-learn
* Jupyter Notebook

---

# 📁 Project Structure

```text
ANN-Projects/
│
├── ANN_Classification.ipynb
├── ANN_Regression.ipynb
├── DateFruit_Dataset.csv
├── powerplant_data.csv
└── README.md
```

---

# 📂 Project Files

| File                       | Description                       |
| -------------------------- | --------------------------------- |
| `ANN_Regression.ipynb`     | ANN regression implementation     |
| `powerplant_data.csv`      | Power plant dataset               |
| `ANN_Classification.ipynb` | ANN classification implementation |
| `DateFruit_Dataset.csv`    | Date fruit classification dataset |
| `README.md`                | Project documentation             |

---

# 🎯 Project Highlights

```text
✔ Deep Learning Regression
✔ Artificial Neural Network
✔ PyTorch Implementation
✔ StandardScaler Preprocessing
✔ Adam Optimization
✔ MSE Loss
✔ R² Evaluation
✔ Real-World Power Plant Dataset
✔ End-to-End ML Pipeline
```

---

# ✅ Project Conclusion

This project successfully demonstrates the application of an **Artificial Neural Network to a real-world regression problem**.

The model takes four important power plant parameters — **Ambient Temperature, Exhaust Vacuum, Ambient Pressure, and Relative Humidity** — and learns their relationship with the electrical energy output.

Using **PyTorch, StandardScaler, MSELoss, and the Adam optimizer**, the ANN achieved a **Testing MSE of 19.59** and an **R² score of 0.9315**.

The project provided practical understanding of the complete Deep Learning workflow:

**Data Preparation → Scaling → Tensor Conversion → ANN Design → Training → Optimization → Prediction → Evaluation**

Overall, this project demonstrates the ability to implement a complete **Deep Learning regression solution using PyTorch** and apply ANN techniques to a practical power plant energy prediction problem.

---

# 👨‍💻 Author

**MD SITARE**

Artificial Intelligence & Machine Learning Enthusiast

---
