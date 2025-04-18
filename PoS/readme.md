
# 📝 Part-of-Speech Tagging using Hidden Markov Model (HMM)

## 📚 Project Overview

This project implements a **Part-of-Speech (PoS) tagger** using a **Hidden Markov Model (HMM)**. It uses the **Viterbi algorithm** for sequence decoding and evaluates the accuracy on real-world text from the NLTK Treebank corpus.

---

## 🗃️ Dataset

- **Corpus:** NLTK Treebank with universal tagset
- **Training Set:** 3000 sentences
- **Test Set:** 750 sentences

Tags are mapped to a simplified universal set (e.g., `NOUN`, `VERB`, `ADJ`, etc.).

---

## 🛠️ Key Components

### 1. `train_hmm()`
- Calculates:
  - **Transition Probabilities:** `P(tag_i | tag_{i-1})`
  - **Emission Probabilities:** `P(word | tag)`
- Applies **Add-1 (Laplace) smoothing**
- Handles **unknown words** using a special `<UNK>` token

### 2. `viterbi()`
- Implements the **Viterbi decoding algorithm**
- Computes the most probable tag sequence for a sentence
- Uses **log-probabilities** for numerical stability

### 3. `evaluate_hmm()`
- Evaluates tagging performance
- Returns overall **accuracy** on the test set

---

## 🧪 Sample Input/Output

**Input Sentence:**
```
["The", "quick", "brown", "fox", "jumps"]
```

**Predicted Tags:**
```
['DET', 'ADJ', 'NOUN', 'NOUN', '.']
```

---

## 📈 Results

- **Test Accuracy:** `88.58%`
- Trained with smoothed HMM, achieves high performance on unseen data

