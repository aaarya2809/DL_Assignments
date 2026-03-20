<img width="661" height="127" alt="image" src="https://github.com/user-attachments/assets/a78c72f1-0b27-4ff6-9cce-3429b4db4bc5" /># 📌 Assignment 1: Neural Network for Cooling Load Prediction

## 👨‍🎓 Student Details
- **Name:** Aarya Malghe  
- **PRN:** 202301100061  
- **Batch:** PEC4  

---

## 📖 Problem Statement
This assignment focuses on implementing a Neural Network from scratch to predict Cooling Load using the Energy Efficiency dataset.

---

## 📊 Dataset Information
- **Dataset:** Energy Efficiency Dataset  
- **File Used:** ENB2012_data 4.xlsx  

### 🔢 Features
- Relative Compactness  
- Surface Area  
- Wall Area  
- Roof Area  
- Overall Height  
- Orientation  
- Glazing Area  
- Glazing Area Distribution  

### 🎯 Target
- Cooling Load  

---

## 🎯 Objective
- Build a neural network model from scratch  
- Apply optimization techniques  
- Compare performance of different optimizers  

---

## 🧠 Methodology

### 1. Data Preprocessing
- Loaded dataset using pandas  
- Renamed columns  
- Checked missing values and duplicates  
- Standardized features  
- Split into training and testing  

### 2. Neural Network Architecture
- Input Layer: 8 neurons  
- Hidden Layer: 5 neurons  
- Output Layer: 1 neuron  
- Activation: Sigmoid  
- Loss: Mean Squared Error  

---

## ⚙️ Optimization Techniques
- Batch Gradient Descent  
- Stochastic Gradient Descent (SGD)  
- Mini-Batch Gradient Descent  

### Momentum
- Classical Momentum  
- Nesterov Momentum  

### Learning Rate Strategies
- Constant  
- Time Decay  
- Step Decay  
- Exponential Decay  

### Adaptive Optimizers
- AdaGrad  
- RMSProp  

---

## 📈 Results
- Mini-Batch performed better than Batch and SGD  
- Momentum improved convergence  
- Nesterov Momentum gave best performance  

---

## 📂 Files
- DL_lab_1.ipynb  
- dl_lab_1.py  
- ENB2012_data 4.xlsx  
- README.md  

---

## ▶️ How to Run

### Jupyter Notebook
```bash
Open DL_lab_1.ipynb and run all cells
