# 🧠 Predictive Keyboard using LSTM

This project implements a **predictive keyboard** using a word-level LSTM neural network. It simulates the behavior of modern smart keyboards by suggesting the most likely next word(s) based on a given text prompt.

---

## 🚀 Features

- Tokenizes raw text into word sequences using NLTK.
- Builds a vocabulary with `<UNK>` token support for unseen words.
- Trains an LSTM-based neural network using PyTorch.
- Suggests top-k next word predictions for a user-provided input.
- Simple and modular structure for easy experimentation.

---

## 📦 Tech Stack

- **Language**: Python  
- **Libraries**:
  - [PyTorch](https://pytorch.org/) – Model building and training
  - [NLTK](https://www.nltk.org/) – Word tokenization
  - Jupyter Notebook – Interactive development and experimentation

---

## 🛠 How It Works

1. **Preprocessing**: Input text is tokenized and converted to word sequences.
2. **Vocabulary Creation**: Words are mapped to indices (`word2idx`) with an `<UNK>` token.
3. **Model Architecture**:
   - Embedding Layer
   - LSTM Layer
   - Fully Connected Layer
4. **Training**: Model is trained using CrossEntropyLoss and Adam optimizer.
5. **Prediction**: Given a user prompt (minimum 3 words), the model suggests top-k likely next words.

---

## 📂 Files

- `predictive_Keyboard.ipynb` – Main notebook with model training and inference
- `README.md` – Project overview (this file)

---

## 📈 Example

```python
suggest_next_words(model, "so are we really", top_k=3)
# Output: ['going', 'doing', 'at']

