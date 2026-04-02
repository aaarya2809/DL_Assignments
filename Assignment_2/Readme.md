# 📌 Practical No. 02: Transfer Learning for Image Classification

---

## 👨‍🎓 Student Details

* **Name:** Aarya Malghe
* **PRN:** 202301100061
* **Batch:** PEC4

---

## 📄 Research Paper

**Title:** Low-Pass Image Filtering to Achieve Adversarial Robustness
**Authors:** Vadim Ziyadinov, Maxim Tereshonok
**Year:** 2023

### 🔍 Summary

The research paper focuses on improving the robustness of Convolutional Neural Networks (CNNs) against adversarial attacks. It proposes the use of **Gaussian Low-Pass Filtering** to remove high-frequency noise from images, thereby improving classification performance.

---

## 📂 Dataset

* **Dataset Used:** CIFAR-10
* **Link:** https://www.cs.toronto.edu/~kriz/cifar.html or https://www.kaggle.com/datasets/ayush1220/cifar10?utm_source=chatgpt.com

### 📊 Dataset Description

* 60,000 RGB images
* 10 classes (airplane, automobile, bird, cat, deer, dog, frog, horse, ship, truck)
* Image size: 32×32

### 🧪 Selected Classes

For this project:

* **Airplane (0)**
* **Truck (9)**

(Binary classification problem)

---

## ⚙️ Task 1: Dataset Preparation

### ✔ Steps Performed

* Loaded CIFAR-10 dataset using TensorFlow

* Selected two classes (Airplane & Truck)

* Normalized pixel values (0–1 range)

* Resized images to 224×224

* Converted labels to binary format

* Applied **Data Augmentation**:

  * Rotation
  * Horizontal Flip
  * Zoom

* Applied **Gaussian Low-Pass Filtering** (as per research paper)

* Split dataset into:

  * Training (80%)
  * Validation (20%)
  * Testing

---

## 🤖 Task 2: Model Implementation and Fine-Tuning

### ✔ Model Used

* Pre-trained model: **MobileNetV2**

### ✔ Architecture

* Base model (pre-trained on ImageNet)
* Frozen initial layers
* Added:

  * Global Average Pooling
  * Dense layer (ReLU)
  * Output layer (Sigmoid)

### ✔ Hyperparameters

* Learning Rate: 0.001
* Batch Size: 32
* Epochs: 5
* Loss Function: Binary Crossentropy

---

## ⚙️ Optimizer Comparison

The model was trained using multiple optimizers:

* SGD
* SGD + Momentum
* RMSProp
* Adam

### 🏆 Best Optimizer:

* **Adam** showed the best performance in terms of convergence speed and accuracy.

---

## 📊 Task 3: Model Evaluation

### ✔ Performance Metrics

| Metric    | Value  |
| --------- | ------ |
| Accuracy  | 94.9%  |
| Precision | 91.25% |
| Recall    | 99.61% |
| F1 Score  | 95.24% |

---

## 📉 Visualizations

The following visualizations are included:

* Training vs Validation Accuracy
* Training vs Validation Loss
* Confusion Matrix
* Optimizer Comparisons
* Learning Rate Analysis
* Gaussian Filtering Effects

---

## 📊 Comparison with Research Paper

| Aspect               | Research Paper     | Our Model     |
| -------------------- | ------------------ | ------------- |
| Dataset              | CIFAR-10           | CIFAR-10      |
| Technique            | Low-pass filtering | Gaussian Blur |
| Accuracy Improvement | High               | Achieved      |
| Robustness           | Improved           | Improved      |

---

## ⚠️ Limitations

* Reduced dataset size (due to RAM constraints)
* Limited epochs (5)
* No adversarial attack testing (FGSM not implemented)

---

## 🚀 Future Improvements

* Implement adversarial attacks (FGSM)
* Train on full dataset
* Use advanced models (EfficientNet)
* Increase epochs for better accuracy

---

## 📁 Files Included

* `DL_Lab_2.ipynb` – Main notebook
* `README.md` – Project documentation
* Visualizations folder (graphs & results)

---

## 🔗 GitHub Repository

(Add your GitHub repo link here)

---

## ✅ Conclusion

This project successfully demonstrates the use of **Transfer Learning** combined with **Gaussian Low-Pass Filtering** to improve CNN performance and robustness. The results align with the research paper findings.

---
