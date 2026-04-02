# 📊 Visualizations and Results

This project includes multiple visualizations to understand data preprocessing, model learning, and performance evaluation.

---

## 🖼️ 1. Original vs Gaussian Blurred Images

**Description:**
This visualization compares original images with their Gaussian low-pass filtered versions.

**Purpose:**

* Demonstrates the effect of removing high-frequency noise
* Validates the research paper concept

**Observation:**

* Blurred images have reduced noise
* Important object structures are still preserved

*(Shown in notebook – Step 12)*

---

## 📈 2. Training vs Validation Accuracy

**Description:**
Line graph showing model accuracy over epochs for training and validation datasets.

**Purpose:**

* Tracks learning progress
* Detects overfitting

**Observation (from graph on page 10 & 19):**

* Training accuracy increases steadily
* Validation accuracy remains close → good generalization

---

## 📉 3. Training vs Validation Loss

**Description:**
Line graph showing loss values across epochs.

**Purpose:**

* Measures model error
* Helps evaluate convergence

**Observation (from graph on page 10 & 19):**

* Loss decreases consistently
* No major divergence → stable training

---

## 🔍 4. Feature Map Visualization

**Description:**
Feature maps extracted from early layers of MobileNetV2.

**Purpose:**

* Understand what CNN learns
* Visualize edge detection & patterns

**Observation (page 14):**

* Early layers detect edges and shapes
* Deeper layers capture complex patterns

---

## 📊 5. Confusion Matrix

**Description:**
Heatmap showing prediction results vs actual labels.

**Purpose:**

* Evaluate classification performance
* Identify misclassifications

**Values (from page 18):**

* True Airplane predicted correctly: **438**
* Airplane misclassified: **49**
* Truck misclassified: **2**
* True Truck predicted correctly: **511**

**Observation:**

* Very high correct predictions
* Minimal misclassification

---

## 📋 6. Performance Metrics Table

**Description:**
Tabular representation of model evaluation metrics.

**Metrics:**

* Accuracy: **94.9%**
* Precision: **91.25%**
* Recall: **99.61%**
* F1 Score: **95.24%**

**Purpose:**

* Summarize model performance in one place

---

## 📦 7. Class Distribution

**Description:**
Counts of each class in training dataset.

**Values (page 6):**

* Airplane: **2012**
* Truck: **1988**

**Purpose:**

* Check dataset balance

**Observation:**

* Dataset is well balanced

---

## 📊 8. Dataset Visualization (Batch Check)

**Description:**
Prints shape of training batches.

**Purpose:**

* Verify data pipeline correctness

**Output:**

* Batch shape: (32, 224, 224, 3)
* Labels shape: (32,)

---

## 🧠 9. Model Learning Curves

**Description:**
Combined visualization of:

* Accuracy Curve
* Loss Curve

**Purpose:**

* Evaluate training stability
* Ensure no overfitting

---

## 📌 Summary of Visual Insights

* Gaussian filtering improves robustness
* Model learns effectively with transfer learning
* No major overfitting observed
* High classification accuracy achieved
* Feature maps confirm meaningful feature extraction

---

## 📷 Screenshots Included

✔ Original vs Blurred Images
✔ Accuracy Graph
✔ Loss Graph
✔ Feature Maps
✔ Confusion Matrix
✔ Performance Table

---
