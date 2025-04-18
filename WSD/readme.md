# 🧠 Word Sense Disambiguation (WSD)

This project implements **Word Sense Disambiguation (WSD)** using the classical **Lesk algorithm** with enhancements. The goal is to determine the correct sense of an ambiguous word within a sentence using contextual overlap with WordNet definitions.

---

## 📌 Objective

To build a simple yet interpretable WSD system using dictionary-based semantic overlap, and evaluate its performance on real-world examples. This task is part of the NLP Lab series and focuses on understanding ambiguity and semantic relationships in language.

---

## ⚙️ Methodology

We use the **Lesk algorithm**, which selects the most appropriate WordNet sense of a word by calculating the maximum overlap between:

- The **sentence context** (after tokenization and lemmatization)
- The **WordNet synset signature**, which includes:
  - Gloss (definition)
  - Usage examples
  - Hypernyms (parent concepts)

> The implementation also includes lemmatization for improved matching, and provides both verbose and clean output modes.

---

## 🧪 Sample Sentences Used

| Sentence                                                   | Target Word |
|------------------------------------------------------------|-------------|
| He sat on the bank of the river.                           | bank        |
| She deposited the money at the bank.                       | bank        |
| The crane is flying over the construction site.            | crane       |
| He couldn't bear the pain any longer.                      | bear        |
| The cell was locked for the night.                         | cell        |

---

## ✅ Final Predicted Senses

```text
🔹 Sentence: He sat on the bank of the river.
👉 Predicted Sense: bank.n.01
   Meaning: sloping land (especially the slope beside a body of water)

🔹 Sentence: The cell was locked for the night.
👉 Predicted Sense: cell.n.01
   Meaning: any small compartment
