Email Spam Classifier (NLP + Naive Bayes)

A text classification project that labels emails as spam or not spam using classic NLP preprocessing and a Multinomial Naive Bayes model.

Problem

Spam emails (fake loan offers, prize claims, account alerts) waste time and can be harmful. This project builds a simple model that learns to separate spam from genuine messages.

Dataset
800 labelled email messages (text, label)
Two classes: spam and non-spam, in roughly equal numbers
Approach
Cleaning: tokenization (NLTK), removal of special characters, removal of words shorter than 3 letters
Normalisation: lowercasing and stemming (Porter Stemmer)
Stopword removal: NLTK English stopwords
Feature extraction: TF-IDF vectorizer
Model: Multinomial Naive Bayes, 80/20 train-test split (random_state=42)
Evaluation: accuracy score
Result
Test accuracy: 1.0 on the held-out 20%
Note: the dataset is small and the messages are fairly similar to each other, so a perfect score does not guarantee the same performance on real-world email. Next step is to test on a larger, more varied dataset.
Tools

Python, Pandas, NLTK, scikit-learn, Google Colab

Files
email_spam_classifier.ipynb
What I learned
How text is cleaned and converted into numbers for a model
Why TF-IDF works better than raw word counts for many text tasks
Why a very high score on a small dataset needs to be checked carefully
