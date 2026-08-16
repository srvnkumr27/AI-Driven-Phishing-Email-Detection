AI-Driven Phishing Email Detection Using NLP

A machine learning project for automatically classifying emails as Safe Email or Phishing Email using Natural Language Processing (NLP), TF-IDF text features, structural email metadata, and comparative machine learning models.

Project Overview

Phishing emails use social engineering techniques such as urgency, deceptive wording, suspicious URLs, and unusual formatting to trick users into revealing sensitive information or taking harmful actions.

This project builds an end-to-end phishing email detection pipeline:

Raw Emails → Data Cleaning → Feature Engineering → Model Training → Model Comparison → Evaluation → Interpretation

The project combines two types of signals:

Linguistic features: TF-IDF unigrams and bigrams extracted from email text.
Structural features: URL presence/count, exclamation marks, digit count, text length, word count, and uppercase ratio.

The project was developed as part of the Summer Internship Program in AI & ML, 2026 — Indian Institute of Computing and Technology (IICT).

Dataset
18,650 labeled emails
11,322 Safe Emails (60.7%)
7,328 Phishing Emails (39.3%)
16 records with missing email text were removed.
18,629 usable records remained after cleaning.
Methodology
1. Data Preprocessing
Remove HTML tags
Remove embedded URLs
Remove email addresses
Convert text to lowercase
Remove punctuation and digits
Remove redundant whitespace
Remove empty records
2. Feature Engineering

TF-IDF Features

Unigrams + bigrams
English stopword removal
Maximum vocabulary of 5,000 terms
Minimum document frequency of 3

Structural Metadata

has_url
num_urls
num_exclaim
num_digits
text_length
num_words
uppercase_ratio

These metadata features are combined with the TF-IDF representation.

Models Compared
Logistic Regression
Random Forest
Multinomial Naive Bayes
Multi-Layer Perceptron (MLP)
Results
Model	Accuracy	F1-Score
🥇 Neural Network (MLP)	97.05%	0.9755
Logistic Regression	96.89%	0.9742
Random Forest	96.48%	0.9706
Naive Bayes	94.47%	0.9554

The MLP Neural Network achieved the best overall performance.

Evaluation

The project evaluates models using:

Accuracy
Precision
Recall
F1-score
Confusion Matrix
ROC Curve
ROC-AUC
Feature Importance
Key Findings

Phishing predictions were strongly influenced by urgency and monetary language, while structural signals such as uppercase ratio and exclamation count also provided meaningful predictive information.

Future Work
Transformer-based embeddings
BERT-based phishing detection
Sender-domain reputation
Email-header analysis
URL-level analysis
Real-time classification API
Web interface
Continuous model retraining
Project Structure
phishing-email-detection/
│
├── data/
│   ├── Phishing_Email.csv
│   └── Phishing_Email_cleaned.csv
│
├── notebooks/
│   └── project-checkpoint.ipynb
│
├── reports/
│   └── comparative analysis report.pdf
│
├── presentation/
│   └── Phishing_Detection_Presentation.pptx
│
└── README.md
Technologies

Python • Pandas • NumPy • Scikit-learn • NLP • TF-IDF • Logistic Regression • Random Forest • Naive Bayes • MLP

Author

M. Sravan Kumar Varma
B.Tech — Computer Science and Engineering (AI & ML)
CMR Technical Campus, Hyderabad, India

Email: srvnkumr27@gmail.com

GitHub: github.com/srvnkumr27

Acknowledgement

Developed as part of the Summer Internship Program in AI & ML, 2026 at the Indian Institute of Computing and Technology (IICT).
