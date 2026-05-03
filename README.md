# Multilingual Public Discourse NLP Analytics Pipeline

**Author:** Rafael Angelo S. Tibayan  
**Course:** CSCI 161 - Social Computing  
**Institution:** Ateneo de Manila University  

---

## Data Availability Note

Some original source URLs may no longer be active or viewable. However, the processed datasets, metadata, and analysis outputs used for this project are preserved in the repository for reproducibility.

---

## 1. Project Overview

This repository contains an end-to-end NLP analytics pipeline for analyzing multilingual public discourse from online comments and news articles.

The project demonstrates data collection, text preprocessing, topic modeling, sentiment classification, network analysis, and visualization. It was originally developed as a Social Computing final project and uses Philippine public discourse data as the case study.

**Objective:** To identify major discussion themes, sentiment patterns, and platform-level differences across online text data.

**Methodology:**
- **Data Cleaning and Preprocessing:** Structured raw text into reusable cleaned datasets and analysis-ready artifacts.
- **Topic Modeling (LDA):** Identified recurring themes and discussion clusters in the corpus.
- **Sentiment Analysis (XLM-RoBERTa):** Classified multilingual sentiment patterns across platforms.
- **Network Analysis:** Built bigram co-occurrence networks to surface important terms and relationships.
- **Data Visualization:** Generated figures and summary outputs for interpretation and reporting.

---

## 2. Skills Demonstrated

- Python-based data cleaning and preprocessing
- Natural language processing on mixed online discourse
- Topic modeling using LDA
- Sentiment analysis using XLM-RoBERTa
- Social network analysis through bigram co-occurrence
- Data visualization and interpretation
- Research writing and presentation

---

## 3. Technologies Used

- Python
- Jupyter Notebook
- Pandas
- Parquet / CSV
- LDA topic modeling
- XLM-RoBERTa sentiment classification
- Network analysis
- Matplotlib / data visualization

---

## 4. Key Deliverables

**[Tibayan_FinalPaper_CSCI161.pdf](./Tibayan_FinalPaper_CSCI161.pdf)** - The final research paper.

**[Tibayan_FinalProjectPresentation.pdf](./Tibayan_FinalProjectPresentation.pdf)** - The presentation slides.

---

## 5. How to Run the Code

The analysis is divided into sequential Jupyter Notebooks found in the `notebooks/` folder. Run them in this order:

1. **`01_NLP_Data_Collection_Flood.ipynb`** - Data ingestion and formatting.
2. **`02_Preprocessing_and_EDA_Flood.ipynb`** - Cleaning, tokenization, and exploratory analysis.
3. **`03_topic_modeling_aggregated.ipynb`** - LDA topic modeling on the full corpus.
   - Optional: **`03B_topic_modeling_balanced.ipynb`** - Balanced modeling experiment.
4. **`04_sentiment_analysis.ipynb`** - XLM-RoBERTa sentiment classification.
5. **`05_Final_Merge_Interpretation.ipynb`** - Merging outputs, network analysis, and final visualizations.

### Installation

To install the required dependencies:

```bash
pip install -r requirements.txt
```

---

## 6. Repository Structure

```text
│   README.md
│   requirements.txt
│   Tibayan_FinalPaper_CSCI161.pdf
│   Tibayan_FinalProjectPresentation.pdf
│
├───configs
│       Basic Stopwords.txt
│       Domain-Specific Stopwords.txt
│       tagalog_stopwords.txt
│
├───data
│   ├───processed
│   │       bigram_freq.csv
│   │       clean_tokens.parquet
│   │       docs_agg_map.csv
│   │       docs_balanced_index.csv
│   │       doc_topic_matrix_agg.csv
│   │       doc_topic_matrix_balanced.csv
│   │       lda_visualization_agg.html
│   │       sentiment_by_platform.csv
│   │       sentiment_by_topic.csv
│   │       sentiment_scored_full.csv
│   │       topic_strengths.csv
│   │       topic_term_matrix_agg.csv
│   │       topic_term_matrix_balanced.csv
│   │       topic_top_terms.txt
│   │       topic_top_terms_agg.csv
│   │       topic_top_terms_balanced.csv
│   │       topic_top_terms_balanced.txt
│   │       unigram_freq.csv
│   │       unigram_freq_by_platform.csv
│   │
│   └───raw
│           cleaned_corpus.csv
│           cleaned_corpus.xlsx
│           rappler_corpus.csv
│           rappler_corpus.xlsx
│           youtube_corpus.csv
│           youtube_corpus.xlsx
│
├───figures
│   │   len_hist_rappler.png
│   │   len_hist_youtube.png
│   │   likes_vs_length_by_sentiment.png
│   │   platform_share.png
│   │   sna_top_75_bigrams.png
│   │   topic_terms_balanced_T0.png
│   │   topic_terms_balanced_T1.png
│   │   topic_terms_balanced_T2.png
│   │   topic_terms_balanced_T3.png
│   │   topic_terms_balanced_T4.png
│   │   topic_terms_balanced_T5.png
│   │   topic_terms_balanced_T6.png
│   │   topic_terms_T0.png
│   │   topic_terms_T1.png
│   │   topic_terms_T2.png
│   │   topic_terms_T3.png
│   │   topic_terms_T4.png
│   │   topic_terms_T5.png
│   │   topic_terms_T6.png
│   │   top_10_comments_by_likes.png
│   │   top_unigrams.png
│   │   top_unigrams_by_platform.png
│   │   word_cloud_topic_0.png
│   │   word_cloud_topic_1.png
│   │   word_cloud_topic_2.png
│   │   word_cloud_topic_3.png
│   │   word_cloud_topic_4.png
│   │   word_cloud_topic_5.png
│   │   word_cloud_topic_6.png
│   │   word_cloud_unigrams.png
│   │
│   └───sentiment
│           overall_sentiment.png
│           sentiment_by_platform.png
│           sentiment_by_topic_stacked.png
│
└───notebooks
        01_NLP_Data_Collection_Flood.ipynb
        02_Preprocessing_and_EDA_Flood.ipynb
        03B_topic_modeling_balanced.ipynb
        03_topic_modeling_aggregated.ipynb
        04_sentiment_analysis.ipynb
        05_Final_Merge_Interpretation.ipynb
```
