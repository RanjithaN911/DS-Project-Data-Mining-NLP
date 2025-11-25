**Data Mining of Natural Language Text**

**MSc Data Science and Analytics – Final Project (7COM1039)**

** **Project Overview****

This project investigates how stemming algorithms influence the effectiveness of document clustering in natural language text datasets, particularly when the data is imbalanced.

**Key objectives:**

Compare Porter, Lancaster, and Snowball stemmers in a clustering pipeline.

Evaluate clustering algorithms (K-Means, Agglomerative) on both balanced and imbalanced datasets.

Use internal metrics (Silhouette, Davies–Bouldin) and external validation (Adjusted Rand Index with manual labels).

The outcome provides insight into preprocessing choices for real-world NLP workflows.

 **Repository Contents**

DataCreation.ipynb – Scripts for data collection (Wikipedia, BBC, Guardian).

23032450-project.ipynb – Final integrated notebook.

combined_dataset_New.csv – Collected raw dataset (~8577 documents).


 **Methodology**
 
**1. Data Collection**

Wikipedia API: articles on machine learning, climate change, politics, sports.

RSS feeds: BBC, The Guardian.

Final corpus size: 8577 documents (naturally imbalanced).

**2. Preprocessing**

Lowercasing, punctuation & number removal.

Stopword removal.

Stemming (Porter, Lancaster, Snowball).

Representation: TF-IDF vectors.

**3. Manual Labeling**

Subset of 700 documents manually annotated.

Used as ground truth for external validation (ARI).

**4. Clustering**

K-Means (centroid-based).

Agglomerative Clustering (hierarchical).

Run separately for each stemmer and dataset version (balanced/imbalanced).

**5. Evaluation**

Silhouette Score – intra-cluster cohesion.

Davies-Bouldin Index – inter-cluster separation.

Adjusted Rand Index (ARI) – comparison with manual labels

**Tools & Libraries**

Python 3.10+

Data Handling: pandas, numpy

NLP Preprocessing: NLTK, spaCy

Vectorization: scikit-learn (TF-IDF, CountVectorizer)

Clustering: scikit-learn, scipy

Evaluation: scikit-learn (Silhouette, ARI, DBI)

Visualization: matplotlib, 

**Run the following notebooks in order:**

DataCreation.ipynb

23032450-project.ipynb
