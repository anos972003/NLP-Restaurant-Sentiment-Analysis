# Sentiment Analysis on Restaurant Reviews

This project performs sentiment analysis on restaurant customer reviews using Natural Language Processing and a Naive Bayes classifier. The dataset contains text reviews labeled with binary sentiment (0 = Negative, 1 = Positive). The goal is to classify new reviews based on their inferred sentiment.

## Dataset
- Source: Kaggle
- File: `Restaurant_Reviews.tsv`
- Text column: `Review`
- Labels: `0` (Negative), `1` (Positive)

## Approach

### Text Preprocessing
The following preprocessing steps were applied to each review:
- Removal of punctuation and non-letter characters
- Conversion to lowercase
- Removal of stopwords using NLTK
- Stemming using Porter Stemmer
- Tokenization and reconstruction into cleaned text form

### Feature Extraction
- Bag-of-Words model created using `CountVectorizer`.

### Model
- Classifier: `GaussianNB` (Naive Bayes)
- Model trained on the transformed feature matrix
- Achieved accuracy: **~73%** on the test set

## Project Structure
project/
│
├── Dataset/
│ └── Restaurant_Reviews.tsv
│
├── Notebook/
│ └── sentiment_analysis.ipynb
│
├── Model/
│ └── GuassianNB.pkl
│
├── requirements.txt
└── README.md


## How to Run
1. Install required dependencies:
   ```bash
   pip install -r requirements.txt
