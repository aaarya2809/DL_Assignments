# 🧠 Deep Learning Lab Assignments

## 👩‍🎓 Student Details

* **Name:** Aarya Balumalghe
* **PRN:** 202301100061
* **Batch:** PEC4
* **Subject:** Deep Learning

---

## 📋 Assignment Overview

| # | Assignment | Topic | Due Date |
|---|-----------|-------|----------|
| 1 | Lab Assignment 1 | Neural Network from Scratch | 
| 2 | Lab Assignment 2 | Transfer Learning (Pretrained Model) | 
| 3 | Lab Assignment 3 | Multi-Task YOLO Vision System | 
| 4 | Lab Assignment 4 | NLP — SMS Spam Detection | 

---

---

# 📌 Lab Assignment 1 — Neural Network from Scratch

## 📄 Problem Statement

Build a Neural Network from scratch (without deep learning libraries) to predict Cooling Load using the Energy Efficiency dataset.

## 📂 Dataset

* **Dataset:** Energy Efficiency Dataset
* **File:** ENB2012_data.xlsx
* **Features:** Relative Compactness, Surface Area, Wall Area, Roof Area, Overall Height, Orientation, Glazing Area, Glazing Area Distribution
* **Target:** Cooling Load

## 🧠 Neural Network Architecture

* Input Layer: 8 neurons
* Hidden Layer: 5 neurons
* Output Layer: 1 neuron
* Activation: Sigmoid
* Loss: Mean Squared Error

## ⚙️ Optimization Techniques

### Gradient Descent Variants
* Batch Gradient Descent
* Stochastic Gradient Descent (SGD)
* Mini-Batch Gradient Descent

### Momentum
* Classical Momentum
* Nesterov Momentum

### Learning Rate Strategies
* Constant
* Time Decay
* Step Decay
* Exponential Decay

### Adaptive Optimizers
* AdaGrad
* RMSProp

## 📈 Results

* Mini-Batch performed better than Batch and SGD
* Momentum improved convergence
* Nesterov Momentum gave best overall performance

## 📁 Files

* `DL_lab_1.ipynb` — Main notebook
* `dl_lab_1.py` — Python script
* `ENB2012_data.xlsx` — Dataset
* `README.md` — Documentation

## 🔗 Links

* **Colab Notebook:** https://colab.research.google.com/drive/1-nyWfC4k5fh6tHqs_wgtJzOzwdxL1HMG?usp=sharing
* **GitHub Folder:** https://github.com/aaarya2809/DL_Assignments/tree/main/Assignment_1

---

---

# 📌 Lab Assignment 2 — Transfer Learning for Image Classification

## 📄 Research Paper

* **Title:** Low-Pass Image Filtering to Achieve Adversarial Robustness
* **Authors:** Vadim Ziyadinov, Maxim Tereshonok
* **Year:** 2023

## 📂 Dataset

* **Dataset:** CIFAR-10
* **Total Images:** 60,000 RGB images (32×32)
* **Classes:** 10 (airplane, automobile, bird, cat, deer, dog, frog, horse, ship, truck)
* **Selected Classes:** Airplane (0) and Truck (9) — Binary Classification
* **Link:** https://www.cs.toronto.edu/~kriz/cifar.html

## 🤖 Model

* **Base Model:** MobileNetV2 (pretrained on ImageNet)
* Frozen initial layers
* Added: Global Average Pooling → Dense (ReLU) → Output (Sigmoid)

## ⚙️ Hyperparameters

| Parameter | Value |
|-----------|-------|
| Learning Rate | 0.001 |
| Batch Size | 32 |
| Epochs | 5 |
| Loss Function | Binary Crossentropy |

## ⚙️ Optimizer Comparison

* SGD
* SGD + Momentum
* RMSProp
* Adam ⭐ (Best — fastest convergence)

## 📊 Results

| Metric | Value |
|--------|-------|
| Accuracy | 94.9% |
| Precision | 91.25% |
| Recall | 99.61% |
| F1 Score | 95.24% |

## 📁 Files

* `DL_Lab_2.ipynb` — Main notebook
* `README.md` — Documentation

## 🔗 Links

* **Colab Notebook:** https://colab.research.google.com/drive/1m-arubMwvmFY_16VI1G1BRXRqPlpkMUJ?usp=sharing
* **Colab Template:** https://colab.research.google.com/drive/1wE3qFcSdnNvexqdgCW_9BlAB7CmiJvyC?usp=sharing
* **Reference Paper:** https://www.frontiersin.org/journals/human-neuroscience/articles/10.3389/fnhum.2023.1150120/full
* **GitHub Folder:** https://github.com/aaarya2809/DL_Assignments/tree/main/Assignment_2

---

---

# 📌 Lab Assignment 3 — Multi-Task YOLO Vision System

## 📄 Overview

Design and implement a Multi-Task Computer Vision System using YOLOv8 to perform Object Detection, Image Classification, Pose Estimation, and Oriented Bounding Box detection — all trained locally on a MacBook Air Apple M4 with no cloud platforms used.

## 💻 System Configuration

* **Device:** MacBook Air — Apple M4
* **RAM:** 16 GB Unified Memory
* **GPU:** Apple M4 MPS (Metal Performance Shaders)
* **Python:** 3.11.13
* **PyTorch:** 2.11.0 (MPS backend)
* **Ultralytics:** 8.4.36
* **No cloud platforms used** ✅

## 📂 Datasets

All datasets sourced from **Roboflow Universe** — exported in YOLOv8-compatible format.

| Part | Dataset | Images | Classes | Format |
|------|---------|--------|---------|--------|
| A | Vehicles v1i | 9,324 | 4 vehicle types | YOLOv8 Detection |
| B | Plant Disease v1i | 3,676 | 3 (Healthy, Powdery, Rust) | Folder Classification |
| C | Human Pose v1i | 1,808 | 2 + 17 COCO keypoints | YOLOv8 Pose |
| D | Text Detection v1i | 4,762 | 3 (Text, Blur_text, None Text) | YOLOv8 OBB |

## 🏋️ Training Configuration

| Part | Model | ImgSz | Batch | Epochs | Device |
|------|-------|-------|-------|--------|--------|
| A | yolov8n.pt | 640 | 16 | 20 | MPS |
| B | yolov8n-cls.pt | 224 | 32 | 20 | MPS |
| C | yolov8n-pose.pt | 640 | 8 | 20 | MPS |
| D | yolov8n-obb.pt | 640 | 8 | 20 | MPS |

## 📊 Results Summary

| Part | Task | Model | Key Metric | Result |
|------|------|-------|-----------|--------|
| A | Vehicle Detection | yolov8n | mAP50 | 0.009 * |
| B | Plant Disease Classification | yolov8n-cls | Top-1 Accuracy | ⭐ 100.0% |
| C | Human Pose Estimation | yolov8n-pose | Box mAP50 | ⭐ 0.955 |
| D | Text Detection OBB | yolov8n-obb | mAP50 | ⭐ 0.819 |

> \* Detection mAP is low due to label class mismatch in Roboflow dataset export. Training completed fully across all 20 epochs.

## 🗂️ Project Structure
yolo_multitask/
├── datasets/
│   ├── detection/vehicles/
│   ├── classification/plant_disease/
│   ├── pose/human_pose/
│   └── obb/text_detection_obb/
├── models/
│   ├── detect_best.pt    (6.0 MB)
│   ├── classify_best.pt  (2.8 MB)
│   ├── pose_best.pt      (6.5 MB)
│   └── obb_best.pt       (6.3 MB)
├── deployment/
│   └── app.py
├── train_detection.py
├── train_classification.py
├── train_pose.py
├── train_obb.py
├── run_all_tasks.py
├── app_streamlit.py
├── requirements.txt
└── README.md

## 🚀 Setup

```bash
git clone https://github.com/aaarya2809/yolo-multitask-vision.git
cd yolo-multitask-vision
python3.11 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
```

## 🏋️ Train

```bash
python train_detection.py
python train_classification.py
python train_pose.py
python train_obb.py
```

## 🔍 Inference

```bash
python run_all_tasks.py
```

## 🌐 Run App

```bash
# Streamlit
streamlit run app_streamlit.py
# Open: http://localhost:8501

# Flask
cd deployment && python app.py
# Open: http://127.0.0.1:5000
```

## 🔗 Links

* 🚀 **Deployed App:** https://yolo-multitask-vision.streamlit.app/
* 💻 **GitHub Repo:** https://github.com/aaarya2809/yolo-multitask-vision
* 🎥 **Screen Recording:** https://drive.google.com/drive/u/0/folders/1ymjPfqKIDwFIkcch4VWKTRkP1M53Pwsk

---

---

# 📌 Lab Assignment 4 — NLP: SMS Spam Detection

## 📄 Overview

Implement NLP techniques and machine learning models to classify SMS messages as Spam or Ham (Not Spam) — covering the complete NLP pipeline from preprocessing to deep learning.

## 📂 Dataset

* **Dataset:** SMS Spam Collection
* **Total Messages:** 5,572
* **Spam:** 747
* **Ham:** 4,825

## 🔧 Technologies Used

* Python, Pandas, NumPy
* NLTK, SpaCy
* Scikit-learn
* Gensim (Word2Vec)
* TensorFlow / Keras
* Matplotlib, Seaborn

## ⚙️ NLP Pipeline

### 1. Text Preprocessing
* Manual tokenization from scratch
* Stopword removal
* Stemming (custom implementation)
* Lemmatization (NLTK with POS tagging)

### 2. Advanced NLP Features
* POS Tagging (manual + NLTK)
* Named Entity Recognition (custom + SpaCy)
* Feature extraction (digits, uppercase, links)

### 3. Text Vectorization
* CountVectorizer (Bag of Words)
* TF-IDF Vectorizer
* N-Grams (bigrams and trigrams)

### 4. Word Embeddings
* Co-occurrence Matrix from scratch
* Word2Vec (Gensim)

## 🧠 Models Implemented

### Without Libraries
* Manual Naive Bayes from scratch

### Using Scikit-learn
* Multinomial Naive Bayes
* Logistic Regression
* Linear SVM

### Deep Learning
* Dense Neural Network (Keras)

## 📊 Results Summary

| Model | Vectorizer | Accuracy | F1 Score |
|-------|-----------|----------|----------|
| Manual Naive Bayes | Manual | 98.12% | 92.68% |
| Naive Bayes | CountVectorizer | 97.85% | 91.78% |
| Logistic Regression | CountVectorizer | 98.12% | 92.42% |
| Linear SVM | CountVectorizer | ⭐ 98.30% | ⭐ 93.33% |
| Dense Neural Network | TF-IDF | 97.94% | 91.99% |

👉 **Best Model: Linear SVM with CountVectorizer**

## 📌 Key Insights

* Spam messages often contain words like "free", "win", "call", "prize"
* Spam messages are generally longer and contain more digits
* Linear models (SVM, Logistic Regression) perform best on text data
* TF-IDF helps reduce the impact of common words
* Deep learning works well but is not always better than simpler models

## 🔗 Links

* **Colab Notebook:** https://colab.research.google.com/drive/1m-arubMwvmFY_16VI1G1BRXRqPlpkMUJ?usp=sharing

---

---

## 🔗 All Links at a Glance

| Assignment | Link |
|-----------|------|
| Assignment 1 — Colab | https://colab.research.google.com/drive/1-nyWfC4k5fh6tHqs_wgtJzOzwdxL1HMG?usp=sharing |
| Assignment 2 — Colab | https://colab.research.google.com/drive/1m-arubMwvmFY_16VI1G1BRXRqPlpkMUJ?usp=sharing |
| Assignment 3 — Streamlit App | https://yolo-multitask-vision.streamlit.app/ |
| Assignment 3 — GitHub Repo | https://github.com/aaarya2809/yolo-multitask-vision |
| Assignment 3 — Screen Recording | https://drive.google.com/drive/u/0/folders/1ymjPfqKIDwFIkcch4VWKTRkP1M53Pwsk |
| Assignment 4 — Colab | https://colab.research.google.com/drive/1m-arubMwvmFY_16VI1G1BRXRqPlpkMUJ?usp=sharing |

---

## 🚀 Future Improvements

* Use LSTM / Transformers (BERT) for NLP tasks
* Use YOLOv11 for better vision accuracy
* Add instance segmentation as a 5th YOLO task
* Deploy NLP model as a web app
* Implement adversarial attack testing (FGSM)

---

## ✅ Conclusion

This repository contains all four Deep Learning Lab Assignments — covering neural networks from scratch, transfer learning with MobileNetV2, multi-task computer vision with YOLOv8, and NLP for spam detection. Each assignment demonstrates a different area of deep learning with practical implementation, evaluation, and deployment.

---

*Aarya Balu Malghe | PRN: 202301100061 | Batch: PEC4 | April 2026*
