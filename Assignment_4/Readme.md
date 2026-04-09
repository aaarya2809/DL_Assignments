# 📩 SMS Spam Detection using NLP & Machine Learning

## 📌 Overview

This project focuses on implementing **Natural Language Processing (NLP)** techniques and building **machine learning models** to classify SMS messages as **Spam** or **Ham (Not Spam)**.

The project covers the complete NLP pipeline — from preprocessing and feature extraction to model building, evaluation, and deep learning.

---

## 🎯 Objectives

* Apply NLP preprocessing techniques (tokenization, stopword removal, stemming, lemmatization)
* Convert text into numerical features using vectorization techniques
* Build and compare multiple classification models
* Evaluate model performance using standard metrics

---

## 📂 Dataset

* Dataset: SMS Spam Collection
* Total messages: 5572
* Spam: 747
* Ham: 4825

---

## 🔧 Technologies Used

* Python 🐍
* Pandas, NumPy
* NLTK, SpaCy
* Scikit-learn
* Gensim (Word2Vec)
* TensorFlow / Keras
* Matplotlib, Seaborn

---

## ⚙️ NLP Pipeline

### 1. Text Preprocessing

* Manual tokenization (from scratch)
* Stopword removal
* Stemming (custom implementation)
* Lemmatization (NLTK with POS tagging)

### 2. Advanced NLP Features

* POS Tagging (manual + NLTK)
* Named Entity Recognition (custom + SpaCy)
* Feature extraction (digits, uppercase, links, etc.)

---

## 🔢 Text Vectorization

* CountVectorizer (Bag of Words)
* TF-IDF Vectorizer
* N-Grams (bigrams & trigrams)

---

## 🧠 Word Embeddings

* Co-occurrence Matrix (from scratch)
* Word2Vec (Gensim)

---

## 📊 Models Implemented

### 🔹 Without Libraries

* Manual Naive Bayes (from scratch)

### 🔹 Using Scikit-learn

* Multinomial Naive Bayes
* Logistic Regression
* Linear SVM

### 🔹 Deep Learning

* Dense Neural Network (Keras)

---

## 📈 Evaluation Metrics

* Accuracy
* F1 Score
* Classification Report
* Confusion Matrix
* Model Comparison Charts

---

## 📊 Results Summary

| Model                    | Vectorizer      | Accuracy | F1 Score |
| ------------------------ | --------------- | -------- | -------- |
| Manual Naive Bayes       | Manual          | 98.12%   | 92.68%   |
| Naive Bayes              | CountVectorizer | 97.85%   | 91.78%   |
| Logistic Regression      | CountVectorizer | 98.12%   | 92.42%   |
| Linear SVM               | CountVectorizer | ⭐ 98.30% | ⭐ 93.33% |
| Deep Learning (Dense NN) | TF-IDF          | 97.94%   | 91.99%   |

👉 **Best Model: Linear SVM with CountVectorizer**

---

## 📌 Key Insights

* Spam messages often contain words like *"free", "win", "call", "prize"*
* Spam messages are generally longer and contain more digits
* Linear models (SVM, Logistic Regression) perform best on text data
* TF-IDF helps reduce the impact of common words
* Deep learning works well but is not always better than simpler models

---

## 🚀 Future Improvements

* Use LSTM / Transformers (BERT)
* Hyperparameter tuning
* Deploy as a web app (Streamlit / Flask)
* Real-time spam detection system

---

## 👨‍💻 Author

**Aarya Malghe**

---

## 📎 Colab Link:

https://colab.research.google.com/drive/1m-arubMwvmFY_16VI1G1BRXRqPlpkMUJ?usp=sharing

---

## ⭐ Conclusion

This project successfully demonstrates the complete NLP workflow, from preprocessing to advanced modeling. It highlights how different techniques impact performance and shows that even simple models can achieve high accuracy with proper text processing.

---
