
# Amazon Alexa Sentiment Analysis

This project uses machine learning to classify customer sentiment from verified Amazon Alexa reviews. It applies natural language processing and Random Forest classification to predict whether a review is positive or negative.

## Dataset

- Source: `amazon_alexa.tsv`
- Contains 3,150 verified reviews with metadata and binary feedback labels.

## Methodology

- Data cleaning and one-hot encoding
- Text vectorization using `CountVectorizer`
- Model training with `RandomForestClassifier`
- Evaluation using confusion matrix and classification report
- Feature importance analysis
- Deployment-ready prediction function

## Performance

- Accuracy: **96%**
- Precision and recall: High for both classes
- Top features: “love”, “great”, “easy”, “disappointed”

## How to Run

## How to Run
1. Open `C12_Assignment10.ipynb` in Google Colab.
2. Run all cells sequentially.
3. Ensure internet access to load the Mall Customer dataset from GitHub.

## Requirements
- Python 3
- pandas, numpy, matplotlib, seaborn
- scikit-learn, scipy
