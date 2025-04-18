# 🧠 Tokenization Techniques in NLP

This project explores various tokenization techniques, including basic implementations, NLTK, spaCy, and subword tokenization using BERT-based tokenizers.

## 📌 Objectives

- Implement basic tokenizers using Python.
- Compare tokenization approaches from different libraries: NLTK, spaCy, HuggingFace.
- Understand how preprocessing affects tokenization (e.g., punctuation, casing).
- Explore subword tokenization using Byte Pair Encoding (BPE).

---

## 🧪 Sample Text Used

```
"Tokenization is the first step in NLP. It involves splitting text into meaningful units."
```

---

## 1️⃣ Basic Tokenization (Custom Python)

- **Whitespace Tokenization**: Uses `str.split()`
- **Regex Tokenization**: Uses `re.split()` to split on punctuation.

### 🔍 Insights

- Whitespace tokenizer is naive — cannot handle punctuation or contractions.
- Regex-based tokenization improves by removing punctuations and special chars.

---

## 2️⃣ Tokenization with NLTK

- **Word Tokenization**: `nltk.word_tokenize()`
- **Sentence Tokenization**: `nltk.sent_tokenize()`

### 🔍 Observations

- Handles punctuation and quotes well.
- Tokenizes contractions and possessives properly.
- Requires downloading `punkt`.

---

## 3️⃣ Tokenization with spaCy

- **Model**: `en_core_web_sm`
- Automatically handles:
  - Punctuation
  - Lemmatization
  - Special characters

### 🛠 Preprocessing

- Implemented stopword removal and lowercasing.
- SpaCy offers better consistency across sentence structures.

---

## 4️⃣ Subword Tokenization (BPE - Byte Pair Encoding)

- **Model**: `bert-base-uncased` from HuggingFace
- **Tokenizer**: `AutoTokenizer`

### 🔍 BPE Tokenization Example

```python
['tokenization', 'is', 'an', 'essential', 'part', 'of', 'nl', '##p', '.']
```

- Splits unknown or rare words into subwords (e.g., `nlp` → `nl`, `##p`)
- Excellent for generalization and transfer learning

---

## 🧾 Summary

| Method       | Handles Punctuation | Case Norm | Subwords | Pre-Trained |
|--------------|---------------------|-----------|----------|-------------|
| Whitespace   | ❌                  | ❌        | ❌       | ❌          |
| Regex        | ✅                  | ❌        | ❌       | ❌          |
| NLTK         | ✅                  | ❌        | ❌       | ❌          |
| spaCy        | ✅                  | ✅        | ❌       | ✅          |
| BERT (BPE)   | ✅                  | ✅        | ✅       | ✅          |

---

## 📚 Requirements

```bash
pip install nltk spacy transformers sentencepiece
python -m spacy download en_core_web_sm
```

---

