Data Mining of Natural Language Text

MSc Data Science and Analytics – Final Project (7COM1039)

📌 Project Overview

This project investigates how stemming algorithms influence the effectiveness of document clustering in natural language text datasets, particularly when the data is imbalanced.

Key objectives:

Compare Porter, Lancaster, and Snowball stemmers in a clustering pipeline.

Evaluate clustering algorithms (K-Means, Agglomerative) on both balanced and imbalanced datasets.

Use internal metrics (Silhouette, Davies–Bouldin) and external validation (Adjusted Rand Index with manual labels).

(Optional) Extend the pipeline to non-English corpora (e.g., Hindi/French).

The outcome provides insight into preprocessing choices for real-world NLP workflows.

🗂️ Repository Contents

DataCreation.ipynb – Scripts for data collection (Wikipedia, BBC, Guardian).

cleaning_processing.ipynb – Preprocessing (cleaning, stopwords removal, stemming).

project_full_code.ipynb – End-to-end pipeline with vectorization, clustering, evaluation.

Final_project_23032450.ipynb – Final integrated notebook for report & viva demo.

combined_corpus.csv – Collected raw dataset (~6,500 documents).

combined_corpus_cleaned.csv – Preprocessed version.

README.md – Project documentation (this file).

⚙️ Methodology
1. Data Collection

Wikipedia API: articles on machine learning, climate change, politics, sports.

RSS feeds: BBC, The Guardian.

Final corpus size: ~6,500 documents (naturally imbalanced).

2. Preprocessing

Lowercasing, punctuation & number removal.

Stopword removal.

Stemming (Porter, Lancaster, Snowball).

Representation: TF-IDF vectors.

3. Manual Labeling

Subset of 500–700 documents manually annotated.

Used as ground truth for external validation (ARI).

4. Clustering

K-Means (centroid-based).

Agglomerative Clustering (hierarchical).

Run separately for each stemmer and dataset version (balanced/imbalanced).

5. Evaluation

Silhouette Score – intra-cluster cohesion.

Davies-Bouldin Index – inter-cluster separation.

Adjusted Rand Index (ARI) – comparison with manual labels

Tools & Libraries

Python 3.10+

Data Handling: pandas, numpy

NLP Preprocessing: NLTK, spaCy

Vectorization: scikit-learn (TF-IDF, CountVectorizer)

Clustering: scikit-learn, scipy

Evaluation: scikit-learn (Silhouette, ARI, DBI)

Visualization: matplotlib, seaborn

Run the following notebooks in order:

DataCreation.ipynb

cleaning_processing.ipynb
