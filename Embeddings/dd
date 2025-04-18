# 🔍 Word Embeddings and Semantic Similarity
---

## 📚 Overview

This project explores how word embeddings capture semantic relationships between words and sentences. Using **pre-trained GloVe vectors**, we compute similarity scores, visualize embeddings, and interpret how meanings are embedded in vector space.

---

## ⚙️ Methods Used

### 1. **Pre-trained Embeddings**
- Used GloVe: `glove-wiki-gigaword-100` (100-dimensional)
- Loaded via `gensim.downloader`

### 2. **Word Pair Similarity**
Computed **cosine similarity** between common word pairs:

| Word 1     | Word 2     | Cosine Similarity |
|------------|------------|-------------------|
| car        | automobile | 0.6832            |
| king       | queen      | 0.7508            |
| cat        | dog        | 0.8798            |
| car        | fruit      | 0.2309            |

### 3. **Sentence Similarity**
Sentence vectors were computed by averaging word embeddings:

| Sentence Pair                                     | Cosine Similarity |
|--------------------------------------------------|-------------------|
| cat vs dog sentence                              | 0.9443            |
| cat vs vehicles sentence                         | 0.5911            |
| cars and trucks vs apples and bananas            | 0.6269            |

---

## 📊 Visualization

Used **PCA** and **t-SNE** to project word vectors into 2D space. Words like `car`, `bus`, `train` cluster together, as do `apple`, `banana`, and `fruit`.

![t-SNE Plot](download.png)

---

## 🧠 Interpretation

- High cosine similarity indicates stronger semantic closeness (e.g., `man–woman`, `cat–dog`)
- t-SNE clusters show related concepts grouped together
- GloVe captures relationships in a compact vector form

---

