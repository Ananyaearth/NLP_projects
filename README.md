# 🧠 NLP Projects

Welcome to my curated collection of Natural Language Processing (NLP) projects. Each project showcases a classic NLP task implemented using statistical or machine learning models, and includes visualizations, evaluation, and detailed documentation.

---

## 📁 Project Structure

```
├── Embeddings/
│   ├── Word Embeddings and Semantic Similarity.ipynb
│   ├── readme.md
│   └── download.png (visualization)
│
├── NER/
│   ├── NER using CRF.ipynb
│   ├── readme.md
│
├── PoS/
│   ├── PoS Tagging using HMM.ipynb
│   ├── readme.md
│
├── README.md (← you are here)
```

---

## 🔍 Project Highlights

### 1. 🏷️ Part-of-Speech Tagging (HMM)
Implements a statistical **Hidden Markov Model (HMM)** to tag parts of speech in a sentence using **Viterbi decoding**. Trained on the NLTK Treebank corpus (universal tagset).

- Features: Add-one smoothing, start/end tags, log-probabilities
- Accuracy Achieved: ~88.5%
- 📂 [Explore PoS Project](./PoS)

---

### 2. 🧾 Named Entity Recognition (CRF vs Rule-Based)
Builds a **Conditional Random Field (CRF)** model for NER on the **WNUT-17** dataset. Rich features like word shape, PoS, prefixes/suffixes are used. Compared against **spaCy's** rule-based model.

- Evaluation: Precision, Recall, F1-score (sklearn)
- Visual comparison with rule-based tagging
- 📂 [Explore NER Project](./NER)

---

### 3. 🔍 Word Embeddings and Semantic Similarity
Uses pre-trained **GloVe embeddings** to compute semantic similarity between word pairs and full sentences. Visualizes embeddings with **PCA** and **t-SNE**.

- Tasks: Word & sentence similarity, cosine distance
- Visuals: 2D plots showing clustering of related terms
- 📂 [Explore Embeddings Project](./Embeddings)

---

## 🛠️ Technologies & Libraries

- Python 3.x, Jupyter Notebook  
- Gensim, scikit-learn, matplotlib, numpy  
- spaCy, sklearn-crfsuite, nltk

---

## 💡 Getting Started

Clone the repository:

```bash
git clone https://github.com/your-username/nlp-projects.git
cd nlp-projects
```

Install required packages:

```bash
pip install -r requirements.txt
```

Launch notebooks:

```bash
jupyter notebook
```

---

## 📄 License

These projects are part of my personal learning journey and are shared for educational and demonstration purposes only.

---

Thanks for checking out my work! 😊
```

---
