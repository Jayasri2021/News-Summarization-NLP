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

4. **Classification**:
   - Vectorized text using TF-IDF.
   - Applied machine learning classifiers:
     - **Logistic Regression (Baseline)**
     - **Support Vector Machines (SVM)**
     - **XGBoost (Best Performance with 83% Accuracy)**

5. **Summarization**:
   - **Extractive**: TextRank, LexRank, BERTSum.
   - **Abstractive**: BART, T5, PEGASUS.
   - Evaluation metrics: ROUGE, BLEU.

6. **Integration**:
   - Combined classification outputs with summarization tasks to ensure region-specific summaries.

### Results
- **Classification**:
  - Best accuracy achieved: **83%** (XGBoost).
- **Summarization**:
  - Best extractive model: **BERTSum**.
  - Best abstractive model: **BART**.

## Tools and Technologies
- **Programming Language**: Python
- **Libraries**: `spaCy`, `scikit-learn`, `XGBoost`, `Hugging Face Transformers`
- **Platform**: [Google Colab](https://colab.research.google.com/)

## Resources
- **Dataset**: [CNN/DailyMail](https://huggingface.co/datasets/abisee/cnn_dailymail)
- **NER Tool**: [spaCy](https://spacy.io/)
- **Summarization Models**: [Hugging Face Transformers](https://huggingface.co/transformers/)

## Future Work
- Implement multi-label classification for articles spanning multiple regions.
- Explore topic-based grouping within each region for more focused summaries.
- Enhance abstractive summarization models for better fluency and coherence.