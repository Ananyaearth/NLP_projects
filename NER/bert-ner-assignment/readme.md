# Named Entity Recognition with BERT 

This repository demonstrates how to fine-tune a pre-trained BERT model for Named Entity Recognition (NER) using the CoNLL-2003 dataset.

## 📌 Objective

To fine-tune BERT for identifying named entities such as persons, organizations, and locations from text using the Hugging Face Transformers library.

## 🧰 Tools Used

- Hugging Face Transformers
- Hugging Face Datasets
- PyTorch
- spaCy
- Matplotlib
- Google Colab (for training)

## 🚀 How to Run

1. Open the notebook `BERT_NER_Assignment.ipynb`.
2. Run all cells step-by-step:
   - Loads and tokenizes the CoNLL-2003 dataset
   - Fine-tunes the `dslim/bert-base-NER` model
   - Evaluates the model
   - Saves the model and tokenizer for later use

3. Use the saved model for inference:

```python
from transformers import pipeline, AutoModelForTokenClassification, AutoTokenizer

model = AutoModelForTokenClassification.from_pretrained("model/bert-ner-conll2003")
tokenizer = AutoTokenizer.from_pretrained("model/bert-ner-conll2003")
ner_pipeline = pipeline("ner", model=model, tokenizer=tokenizer, aggregation_strategy="simple")

sentence = "Elon Musk is the CEO of Tesla, founded in California."
entities = ner_pipeline(sentence)

for ent in entities:
    print(f"{ent['word']} → {ent['entity_group']} ({ent['score']:.2f})")
```

## 📊 Sample Output

```
Elon Musk → MISC
Tesla → PER
California → ORG
```

## 📄 Evaluation Metrics

```json
{
  "eval_loss": 0.0969,
  "eval_runtime": 36.15,
  "epoch": 1.0
}


