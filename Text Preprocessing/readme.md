# 🧠 Text Preprocessing and Classification – NLP Lab Assignment

This project focuses on implementing advanced text preprocessing and classification techniques as part of an NLP lab assignment. The workflow includes data cleaning, tokenization, embedding techniques, and text classification using various machine learning models.

---

## 📚 Objective

- Implement and compare various text preprocessing techniques.
- Apply different text vectorization strategies like one-hot encoding, TF-IDF, Word2Vec, FastText, and GloVe.
- Perform sentiment analysis and spam detection using classical ML classifiers.

---

## 🧰 Technologies & Libraries Used

- **Text Preprocessing:** NLTK, spaCy, regex, BeautifulSoup
- **Machine Learning:** Scikit-learn, XGBoost
- **Word Embeddings:** Gensim (Word2Vec, FastText), GloVe
- **Visualization:** Matplotlib, Seaborn
- **Other Tools:** Transformers (for subword tokenization)

---

## 📊 Features Implemented

### 1️⃣ Basic Preprocessing

- Word, sentence, and subword tokenization (NLTK, spaCy, BERT)
- Stemming and lemmatization
- Stopword removal, punctuation cleanup
- Lowercasing and whitespace normalization

### 2️⃣ Context-Aware Preprocessing

- Sentence segmentation
- Out-of-vocabulary (OOV) handling with WordPiece
- Named entity detection and anonymization using spaCy

### 3️⃣ Text Representation Techniques

- One-hot encoding
- TF-IDF vectorization
- Word2Vec embeddings
- FastText embeddings
- GloVe embeddings (converted and loaded)

### 4️⃣ Text Classification

Performed on sentiment/spam samples using:

- Naive Bayes
- Support Vector Machines (SVM)
- Logistic Regression
- Decision Trees

Each model is evaluated using precision, recall, F1-score, and accuracy.

---

## ✅ Results Summary

Example results from classification reports:

| Model                 | Accuracy |
|----------------------|----------|
| Naive Bayes          | 81%      |
| SVM                  | 81%      |
| Logistic Regression  | 82%      |
| Decision Tree        | 64%      |

---

