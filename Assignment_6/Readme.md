# Encoder–Decoder Models with and without Attention

## 📌 Overview
This project implements and compares two sequence-to-sequence models:

- Baseline Encoder–Decoder (without attention)
- BiLSTM Encoder + Luong Attention Decoder

The goal is to demonstrate how attention improves translation quality.

---

## 📊 Key Results

| Metric | Without Attention | With Attention |
|--------|------------------|---------------|
| Loss | Higher | Lower |
| BLEU Score | Lower | Higher |
| Output Quality | Poor | Better |
| Training Time | Faster | Slower |

---

## 🧠 Architecture

### Without Attention
Encoder (LSTM) → Decoder (LSTM)

### With Attention
BiLSTM Encoder → Attention → LSTM Decoder

---

## 🚀 How to Run

```bash
pip install -r requirements.txt
python main.py
