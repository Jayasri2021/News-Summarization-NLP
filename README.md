# News Aggregation System with NER and Summarization

This project introduces a geography-aware news aggregation system that classifies news articles by geographic regions and generates region-specific summaries. It integrates Named Entity Recognition (NER), machine learning classifiers, and both extractive and abstractive summarization techniques to enhance the user experience of personalized news delivery.

## Project Overview

### Objective
Develop a system that:
1. Classifies news articles by geographic regions using NER and machine learning.
2. Generates concise summaries tailored to each region using advanced summarization techniques.

### Steps to Build the Project
1. **Data Collection**:
   - Dataset: [CNN/DailyMail Dataset](https://huggingface.co/datasets/abisee/cnn_dailymail)
   - Contains over 300,000 news articles with corresponding highlights for summarization.

2. **Data Preprocessing**:
   - Tokenized and cleaned text (e.g., removed stopwords, URLs, and punctuation).
   - Utilized `spaCy` for tokenization and stopword filtering.

3. **Named Entity Recognition (NER)**:
   - Extracted geopolitical entities (GPE) using `spaCy`.
   - Mapped entities to predefined regions (e.g., North America, Europe, Asia).

