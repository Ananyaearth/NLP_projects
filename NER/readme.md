# 🧠 Named Entity Recognition using Conditional Random Fields (CRF)
---

## 📚 Overview

This project implements a Named Entity Recognition (NER) system using **Conditional Random Fields (CRF)** and compares its performance to a **rule-based approach** using spaCy. It is built on top of the **WNUT-17 dataset**, which includes noisy, user-generated content like tweets.

---

## 📦 Dataset

**WNUT-17 (Noisy User-generated Text):**
- Specializes in uncommon or emerging named entities
- Includes entity types like `person`, `location`, `organization`, `product`, `creative-work`, and `group`

For demonstration:
- **Training data:** 1000 sentences
- **Testing data:** 200 sentences

---

## ⚙️ Methods

### ✅ 1. Preprocessing
- Load WNUT-17 dataset (via Hugging Face or local `.conll` files)
- Convert numerical NER tags to string labels (e.g., `B-person`)
- Add Part-of-Speech (PoS) tags using **spaCy**

### ✅ 2. Feature Extraction
Each token includes features like:
- Word shape (e.g., lowercase, titlecase)
- Suffixes (last 2/3 letters)
- Digit/capitalization flags
- PoS tag and first 2 letters of the PoS
- Neighboring word/tag features
- Sentence boundary indicators (BOS, EOS)

### ✅ 3. CRF Training
- Using `sklearn-crfsuite`
- Algorithm: `lbfgs`
- Regularization: `c1=0.1`, `c2=0.1`
- Max iterations: 100

### ✅ 4. Rule-Based NER (spaCy)
- spaCy's pre-trained `en_core_web_sm` model is used for comparison.
- Its output is mapped to the same format (e.g., `B-person`, `I-location`) for fair comparison.

---

## 📊 Results

### 🔹 CRF Model Performance:
```
Precision: 0.93 | Recall: 0.97 | F1-score: 0.95 (Micro Avg)
```

- Excellent on non-entity (`O`) class
- Struggles on rare entity types due to data imbalance

### 🔹 Rule-based (spaCy) Performance:
```
Precision: 0.91 | Recall: 0.96 | F1-score: 0.93 (Micro Avg)
```

- Slightly better at picking up some entity types (e.g., organizations, locations)
- Still limited by fixed patterns and pre-trained scope

---

## 🔍 Sample Input/Output

**Input Sentence:**
```python
["@paulwalk", "It", "'s", "the", "view", "from", "where", "I", "'m", "living", "for", "two", "weeks", ".", "Empire", "State", "Building", "=", "ESB", ".", "Pretty", "bad", "storm", "here", "last", "evening", "."]
```

**CRF Predicted Tags:**
```python
['O', 'O', 'O', ..., 'B-product', 'I-product', 'I-product', 'O', ...]
```

---

## 📈 Conclusion

- The CRF model is robust on frequent classes but requires more data or feature enhancements for rare entity tags.
- Rule-based systems like spaCy offer decent performance but lack contextual depth.

### 🔧 Potential Improvements:
- Increase training data
- Use domain-specific gazetteers or Brown clusters
- Try neural models like **BiLSTM-CRF** or **transformers**

---
