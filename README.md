# Myntra Reviews Analysis Using NLP

A Natural Language Processing project that analyzes customer reviews from **Myntra** — India's leading fashion e-commerce platform. The project extracts meaningful insights from raw customer feedback using text preprocessing, sentiment classification, word frequency analysis, and TF-IDF techniques.

---

## 📖 Project Overview

Customer reviews are a goldmine of information for e-commerce businesses. This project applies **NLP techniques** to Myntra customer reviews to uncover sentiment trends, identify frequently discussed topics, and extract key terms that can guide product and service improvements. The pipeline covers the complete text analytics workflow — from raw text cleaning to visual insights and sentiment classification.

---

## 📂 Repository Structure

```
myntra-reviews-analysis/
│
├── dataset/                          # Myntra customer reviews dataset
│   └── myntra_reviews.csv
│
├── notebooks/                        # Jupyter Notebooks
│   └── myntra_reviews_analysis.ipynb
│
├── outputs/                          # Generated visualizations
│   ├── wordcloud.png                 # Word Cloud image
│   └── sentiment_distribution.png   # Sentiment analysis chart
│
├── README.md                         # Project overview and instructions
└── requirements.txt                  # Python dependencies
```

---

## 🔍 Dataset

The dataset consists of Myntra customer reviews with the following key columns:

| Column | Description |
|--------|-------------|
| `Review Text` | Raw customer review in text format |
| `Rating` | Numeric rating given by the customer (e.g., 1–5) |
| `Sentiment Label` | Sentiment category — Positive, Negative, or Neutral |

---

## 📊 Key Features

| Feature | Description |
|---------|-------------|
| **Word Cloud Visualization** | Highlights the most frequently occurring words across all reviews |
| **Term-Document Matrix (TDM)** | Represents word frequency across the entire review corpus |
| **TF-IDF Analysis** | Identifies the most informative and unique terms per review |
| **Sentiment Analysis** | Classifies each review as Positive, Negative, or Neutral |
| **Data Preprocessing** | Full text cleaning pipeline — stopword removal, tokenization, and normalization |

---

## 🛠️ Technologies Used

| Category | Tools / Libraries |
|----------|-------------------|
| **Language** | Python 3.x |
| **Data Processing** | Pandas, NumPy |
| **NLP** | NLTK, Scikit-learn |
| **Visualization** | Matplotlib, Seaborn, WordCloud |

**Key NLP modules used:**
- `nltk.corpus.stopwords` — Stopword removal
- `nltk.tokenize` — Text tokenization
- `sklearn.feature_extraction.text.TfidfVectorizer` — TF-IDF computation
- `sklearn.feature_extraction.text.CountVectorizer` — Term-Document Matrix
- `wordcloud.WordCloud` — Word Cloud generation

---

## 🚀 Implementation Steps

### 1. Data Loading & Preprocessing
- Load the Myntra reviews dataset using Pandas
- Handle missing and null values in review text
- Convert text to lowercase
- Remove special characters, punctuation, and numbers
- Remove **stopwords** using NLTK
- Perform **tokenization** to split text into individual words
- Apply **stemming/lemmatization** for word normalization

### 2. Word Cloud Generation
- Combine all cleaned review text into a single corpus
- Generate a **Word Cloud** to visually highlight the most frequently used words
- Larger words = higher frequency in the reviews

### 3. Term-Document Matrix (TDM) & TF-IDF Computation
- Build a **Term-Document Matrix** using `CountVectorizer` to capture raw word frequencies
- Apply **TF-IDF (Term Frequency-Inverse Document Frequency)** using `TfidfVectorizer` to identify the most meaningful terms
- TF-IDF down-weights common words and elevates unique, informative terms

### 4. Sentiment Analysis
- Classify each review into one of three sentiment categories:

| Sentiment | Meaning |
|-----------|---------|
| **Positive** | Customer is satisfied with the product/service |
| **Negative** | Customer is dissatisfied or has complaints |
| **Neutral** | Customer has a mixed or indifferent opinion |

- Visualize sentiment distribution using bar charts and pie charts

---

## 📊 Results & Insights

- **Word Cloud** reveals the most common themes in customer feedback — such as product quality, delivery, sizing, and fabric
- **TF-IDF analysis** surfaces key distinguishing terms that appear prominently in specific reviews, useful for identifying niche pain points
- **Sentiment distribution** provides a high-level view of overall customer satisfaction levels
- Insights from this analysis can directly inform:
  - Product quality improvements
  - Better size and fit communication
  - Delivery and logistics enhancements
  - Targeted marketing based on positive review themes

---

## 🏁 Getting Started

1. **Clone the repository**
   ```bash
   git clone https://github.com/shreyaa-1702/myntra-reviews-analysis.git
   ```

2. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Download NLTK resources**
   ```python
   import nltk
   nltk.download('stopwords')
   nltk.download('punkt')
   nltk.download('wordnet')
   ```

4. **Run the Jupyter Notebook**
   ```bash
   jupyter notebook notebooks/myntra_reviews_analysis.ipynb
   ```

---

## ⚙️ Requirements

```
pandas
numpy
nltk
scikit-learn
matplotlib
seaborn
wordcloud
```

Install all at once:
```bash
pip install pandas numpy nltk scikit-learn matplotlib seaborn wordcloud
```

---

## 💡 Key Insights

- **Positive reviews** tend to dominate Myntra feedback, reflecting generally high customer satisfaction in fashion e-commerce
- **Negative reviews** frequently mention sizing inconsistencies and delivery delays — common pain points in online fashion retail
- **TF-IDF** is more powerful than raw word frequency for identifying truly meaningful terms, as it filters out common filler words
- **Word Clouds** provide an intuitive, at-a-glance summary of review themes that are easy to communicate to non-technical stakeholders

---

## 📄 License

This project is licensed under the terms specified in the [LICENSE](LICENSE) file.

---

## 🙋 Contributing

Contributions and suggestions are welcome. Feel free to open an issue or submit a pull request for any improvements or enhancements.
