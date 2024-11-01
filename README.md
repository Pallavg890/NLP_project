Project Summary

This project focuses on analyzing, visualizing, and experimenting with the PLOW Dataset for Biomedical Named Entity Recognition (NER). The dataset includes tokens with short forms (acronyms) that facilitate text understanding within the biomedical field, such as identifying RNA, DNA, and other cellular components. We apply multiple Natural Language Processing (NLP) methods, including K-Nearest Neighbors (KNN), Support Vector Machines (SVM), and Long Short-Term Memory (LSTM) models, to evaluate performance on the dataset.

Dataset Description

The PLOW dataset, a subset used for NER, is divided into training, testing, and validation datasets, with tags that categorize tokens into four main categories:

B-O: Other tokens not related to abbreviations or long forms.

B-AC: Tokens classified as abbreviations or acronyms.

B-LF: Tokens indicating the beginning of a long form.

I-LF: Tokens inside a long form.

Data Visualization

Histograms: Show the distribution of token lengths across datasets. Observed that the training dataset is skewed with mostly shorter tokens.
Bar Chart: Frequency of each tag, where B-O is the most frequent, leading to an imbalanced dataset.
Heatmap: Co-occurrences of POS and NER tags, identifying that B-O tokens are mostly nouns or punctuation.

Experimentation

Experiment 1: Data Pre-processing Techniques
System 1: Tokenized data with Tfidf Vectorization, followed by KNN.
System 2: Tfidf Vectorization with SVM.
System 3: Tfidf with bigrams in KNN, which significantly improved F1-scores due to the bigram token pairing.

Experiment 2: NLP Algorithms and Techniques
System 1: FastText Vectorization combined with SVM for rare tokens.
System 2: Encoding and applying LSTM for sequence learning.

Experiment 3: Text Encoding and Transformation
Compared Tfidf Vectorization and FastText Vectorization with KNN.

Experiment 4: Hyperparameter Optimization
System 1: SVM with Tfidf Vectorization and optimized kernel parameters.
System 2: KNN with tuned neighbors and Euclidean distance metric.

Results and Analysis
Experiment 1: System 3 (bigram Tfidf with KNN) achieved the best F1 score (0.88) among data preprocessing techniques.
Experiment 2: Both SVM and LSTM models struggled, with F1 scores of 0.23, indicating room for tuning or more epochs.
Experiment 3: FastText Vectorization slightly improved F1 over Tfidf Vectorization.
Experiment 4: Hyperparameter optimization resulted in an F1 score of 0.87 for both KNN and SVM models.
Conclusion
The best-performing models in this project were achieved through hyperparameter optimization, as well as using bigram Tfidf vectorization with KNN. These strategies significantly enhanced the F1 scores and addressed class imbalance. Further improvements could be explored by employing trigrams or advanced vectorization techniques.


