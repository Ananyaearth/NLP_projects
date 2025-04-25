# IMDb Sentiment Analysis using BERT Embeddings

This project demonstrates sentiment classification on the IMDb movie reviews dataset using pre-trained BERT embeddings and a Logistic Regression classifier.

---

## 📚 Overview

- **Objective**: Classify movie reviews into Positive or Negative sentiment.
- **Embedding Model**: `bert-base-uncased` from Hugging Face Transformers.
- **Classifier**: Scikit-learn Logistic Regression.
- **Dataset**: IMDb movie reviews from Hugging Face `datasets` library.

---

## 🛠️ Project Steps

1. **Load IMDb Dataset**  
   Sampled 1000 training reviews and 300 test reviews after shuffling.
   
2. **Embedding Extraction**  
   Used the `[CLS]` token from `bert-base-uncased` to generate a 768-dimensional vector for each review.
   
3. **Model Training**  
   Trained Logistic Regression on extracted BERT embeddings (300 iterations).

4. **Evaluation**  
   Evaluated using precision, recall, F1-score, and accuracy metrics.

---

## 🧪 Results

### 📈 Classification Report:
   precision    recall  f1-score   support

negative       0.77      0.79      0.78       150
positive       0.78      0.77      0.77       150

accuracy                           0.78       300
macro avg 0.78 0.78 0.78 300 weighted avg 0.78 0.78 0.78 300



### 📄 Sample Predictions:

| Sentence | Predicted Sentiment |
|:---|:---|
| The battery lasts for two days without charging. | Negative |
| The camera produces blurry photos. | Negative |
| The screen is bright and vibrant. | Positive |
| The sound quality is terrible. | Negative |
| The latest update improved performance a lot. | Positive |
| The movie was an absolute masterpiece! | Positive |
| I hated every second of that film. | Negative |

---

## 🔥 How to Run

1. Install required libraries:

```bash
pip install transformers datasets scikit-learn
Run the Jupyter Notebook or Python script:

Extract BERT embeddings for sentences

Train Logistic Regression

Predict sentiment on test set or custom sentences

🧠 Future Improvements
Train on full IMDb dataset (50,000 samples) for higher accuracy.

Fine-tune BERT model instead of using frozen embeddings.

Try other transformer models (RoBERTa, DistilBERT).

Deploy as a simple web app (e.g., using Streamlit or Flask).

