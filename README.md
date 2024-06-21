# Sentiment Analysis on Amazon Fine Food Reviews

## Overview
This project performs sentiment analysis on the Amazon Fine Food Reviews dataset using two different techniques:

1. **VADER (Valence Aware Dictionary and Sentiment Reasoner)** - A rule-based sentiment analysis tool tailored for social media texts.
2. **Roberta (from Huggingface)** - A state-of-the-art pretrained transformer model for natural language processing tasks.

The goal is to compare the performance and insights provided by these two methods on the same dataset.

## Dataset
The dataset used in this project is the Amazon Fine Food Reviews, which contains 568,454 food reviews from Amazon. Each review includes information such as the product ID, user ID, profile name, helpfulness rating, score (rating), time, summary, and text of the review.

## Methodology
The project is divided into several sections, each focusing on a different aspect of the analysis:

### 1. Loading and Exploring the Dataset
- The dataset is loaded into a Pandas DataFrame.
- Basic exploratory data analysis (EDA) is performed to understand the structure and content of the data.
- Steps include checking for missing values, examining the distribution of ratings, and viewing sample reviews.

### 2. Data Preprocessing
- **Handling Missing Values:** Rows with missing text data are removed.
- **Tokenization:** Text is split into individual words or tokens.
- **Removing Stop Words:** Common words that do not contribute to sentiment are removed.
- These preprocessing steps help improve the accuracy and efficiency of the sentiment analysis models.

### 3. Sentiment Analysis with VADER
- VADER (Valence Aware Dictionary and Sentiment Reasoner) is introduced and explained.
- The VADER sentiment analyzer is initialized.
- Sentiment scores for each review are calculated using VADER.
- The compound score, ranging from -1 (extremely negative) to +1 (extremely positive), is interpreted.

### 4. Sentiment Analysis with Roberta
- Roberta (A Robustly Optimized BERT Pretraining Approach) is introduced as a transformer model developed by Huggingface.
- The pretrained Roberta model is loaded using the Huggingface pipeline.
- Sentiment labels and scores for each review are predicted using Roberta.
- The model provides a label (e.g., pos, neu or neg).

### 5. Comparing Results
- The results from VADER and Roberta are compared to understand their performance and differences.
- Visualizations of sentiment score distributions from both methods are created.
- Overall sentiment predictions (positive, negative, neutral) from each model are compared.

## Findings
- **VADER** provides a quick and interpretable sentiment score based on predefined rules and a lexicon. It is effective for social media texts and quick analyses.
- **Roberta** leverages deep learning to capture more nuanced sentiment patterns, offering high accuracy but requiring more computational resources.

## Future Work
- Experiment with other sentiment analysis models and techniques.
- Fine-tune the Roberta model on a specific subset of the data.
- Apply these methods to different datasets for broader insights.

## Conclusion
This project demonstrates the application of two different sentiment analysis techniques on the same dataset, highlighting their respective advantages and limitations. The insights gained can guide the choice of method based on the specific needs of a sentiment analysis task.


## Acknowledgements
- The dataset is sourced from [Kaggle](https://www.kaggle.com/snap/amazon-fine-food-reviews).
- VADER sentiment analysis tool is developed by C.J. Hutto and Eric Gilbert.
- Roberta model is developed by Huggingface.
