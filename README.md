# 📝 Lab Assignment 4 – NLP Preprocessing and Text Classification
NLP preprocessing and text classification on BBC News dataset (2,225 articles, 5 categories). Implements tokenization, stopword removal, stemming, lemmatization, TF-IDF, CountVectorizer with Naive Bayes, SVM and Logistic Regression. Best accuracy: ~98% (Linear SVM + TF-IDF)

**Student Name:** [Vedant Ingle]
**PRN No. :** [202402040031]
**Course:** Deep Learning / Artificial Intelligence

---

## 📄 Objective

Implement NLP preprocessing techniques and build a text classification model using machine learning on the BBC News dataset. Apply tokenization, stopword removal, stemming, lemmatization, TF-IDF, CountVectorizer and compare multiple classifiers.

---

## 📁 Dataset

| Property | Details |
|---|---|
| **Name** | BBC Full Text Document Classification |
| **Source** | Kaggle – Shivam Kushwaha |
| **Link** | https://www.kaggle.com/datasets/shivamkushwaha/bbc-full-text-document-classification |
| **Total Articles** | 2,225 |
| **Classes** | 5 (Tech, Business, Sport, Entertainment, Politics) |
| **Avg Article Length** | ~380 words |
| **Format** | .txt files organized in category folders |
| **Auto-download** | ✅ Yes — downloads automatically via kagglehub |

### Class Distribution

| Category | Articles |
|---|---|
| Sport | 511 |
| Business | 510 |
| Politics | 417 |
| Tech | 401 |
| Entertainment | 386 |
| **Total** | **2,225** |

---

## 🔧 NLP Preprocessing Pipeline

| Step | Technique | Example |
|---|---|---|
| 1 | **Lowercasing** | `"Running"` → `"running"` |
| 2 | **Remove special characters** | `"hello!"` → `"hello"` |
| 3 | **Tokenization** | `"hello world"` → `["hello", "world"]` |
| 4 | **Stopword Removal** | removes "the", "is", "at", "a"... |
| 5 | **Stemming (Porter)** | `"running"` → `"run"` |
| 6 | **Lemmatization (WordNet)** | `"better"` → `"good"` |

---

## 📊 Text Vectorization

| Method | Description | Features Used |
|---|---|---|
| **CountVectorizer** | Raw word frequency — Bag of Words | 30,000 |
| **TF-IDF Vectorizer** | Word importance × inverse doc frequency | 30,000 |

Both use **unigrams + bigrams** (`ngram_range=(1,2)`)

---

## 🤖 Models Trained

| Model | Description |
|---|---|
| **Multinomial Naive Bayes** | Probabilistic baseline, very fast |
| **Linear SVM** | Best performer for text classification |
| **Logistic Regression** | Interpretable, well-calibrated |

Each model trained on **both TF-IDF and CountVectorizer** → 6 total combinations

---

## 📊 Results

| Model | Vectorizer | Accuracy |
|---|---|---|
| **Linear SVM** | **TF-IDF** | **~98%** ← BEST ✅ |
| Logistic Regression | TF-IDF | ~97.8% |
| Naive Bayes | TF-IDF | ~97.3% |
| Linear SVM | CountVec | ~97.6% |
| Logistic Regression | CountVec | ~97.0% |
| Naive Bayes | CountVec | ~95.1% |

---

## 📈 Evaluation Metrics Used

- ✅ Accuracy
- ✅ Precision
- ✅ Recall
- ✅ F1-Score
- ✅ Confusion Matrix (for all 6 models)
- ✅ Classification Report

---

## 🖼️ Visualizations Generated

- ✅ Class distribution bar chart
- ✅ Text length distribution (KDE plot per category)
- ✅ Word clouds for all 5 categories
- ✅ Top TF-IDF terms per category
- ✅ Model accuracy comparison (horizontal bar chart)
- ✅ Confusion matrix for best model
- ✅ All 6 confusion matrices side by side

---

## 🔍 Key Findings

1. **Linear SVM + TF-IDF** is the best combination with ~98% accuracy ✅
2. **TF-IDF consistently outperforms CountVectorizer** across all models
3. **Naive Bayes** achieves competitive ~95% accuracy with fastest training time
4. **Entertainment & Politics** categories show most confusion due to semantic overlap
5. BBC full-text articles (~380 words avg) provide much richer features than headline-only datasets

---
