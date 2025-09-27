# 🧥👟 Fashion-MNIST Classifier (MLP & CNN)

A clean, professional PyTorch pipeline for training and evaluating **MLP** and **CNN** models on the [Fashion-MNIST](https://github.com/zalandoresearch/fashion-mnist) dataset.  
Includes **stratified dataset split (80/10/10)**, **proper normalization**, **augmentation**, **advanced optimizers/schedulers**, and **rich visualizations** (confusion matrices, per-class metrics, learning curves, misclassifications, etc.).

---

## 📌 Features
- ✅ Dataset audit + class distribution plots  
- ✅ Stratified **80/10/10 split** (Train/Val/Test)  
- ✅ **Normalization from train only** (no leakage)  
- ✅ Configurable models: **MLP** and **CNN**  
- ✅ Training tricks:
  - Label smoothing  
  - AdamW + OneCycleLR  
  - Gradient clipping  
  - Dropout + BatchNorm  
- ✅ Metrics: Accuracy + Macro-F1  
- ✅ Visualizations:
  - Confusion matrices  
  - Per-class Precision/Recall/F1 (bar plots)  
  - Learning curves & LR schedule  
  - Misclassified examples grid  
  - Confidence distributions  

---

## 🗂️ Dataset
**Fashion-MNIST**: 70,000 grayscale images (28×28) across 10 categories:

| ID | Label        | Example |
|----|--------------|---------|
| 0  | T-shirt/top  | 👕 |
| 1  | Trouser      | 👖 |
| 2  | Pullover     | 🧥 |
| 3  | Dress        | 👗 |
| 4  | Coat         | 🧥 |
| 5  | Sandal       | 🩴 |
| 6  | Shirt        | 👔 |
| 7  | Sneaker      | 👟 |
| 8  | Bag          | 👜 |
| 9  | Ankle boot   | 👢 |

We split the dataset as:
- **80% train**
- **10% validation**
- **10% test**

---

## 🏗️ Models

### 🔹 MLP
- Flatten 28×28 → [512, 256] hidden layers
- ReLU + Dropout
- Output: 10 classes

### 🔹 CNN
- Conv layers: 32 → 64 → 128 filters
- BatchNorm + ReLU + MaxPooling
- Dropout regularization
- Dense head: 256 → 10

---

## 🚀 Training Setup
- **Loss**: CrossEntropy (with optional label smoothing)  
- **Optimizer**: AdamW  
- **Scheduler**: OneCycleLR  
- **Regularization**: Dropout, Gradient clipping  
- **Metrics**: Accuracy, Macro-F1  
- **Early Stopping** on validation F1  

---

## 🔬 Visualizations
The notebook/Colab includes:

- 📉 Training curves: loss, accuracy, F1  
- 📈 LR schedule (OneCycleLR)  
- 🔍 Confusion matrices (Val/Test)  
- 📊 Per-class Precision/Recall/F1  
- 🖼️ Misclassified examples grid  
- 📦 Class confidence distributions  

---

## ⚡ Getting Started

### 🔹 Run in Google Colab
1. Open the notebook in Colab  
2. Select **GPU runtime** (`Runtime > Change runtime type > GPU`)  
3. Run all cells  

