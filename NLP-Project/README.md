# The Obsessions of the Wise Minds: Topic Modeling of Over 2500 Years of Philosophical Texts

### Abstract

In this project, initial topic modeling and assessment were performed on philosophical published texts as a pilot for more general modeling purposes (for any type of published texts). The topic model created by this project along with similar topic models in other fields can be used in a wide variety of downstream models, from clustering models to recommendation systems. Nine distinct topics coded in the raw data were described in this work, using dimensionality reduction algorithms and topic evaluation and interpretation.

### Data

The dataset contains over 300,000 sentences from over 50 texts spanning 10 major schools of philosophy over the course of 2500 years, from Plato to Wittgenstein. Texts were taken either from Project Gutenberg or from the original author of the dataset personal library of pdfs (https://www.kaggle.com/kouroshalizadeh/history-of-philosophy).

### Methodology

The texts were pre-processed using Python Regular Expression (RE) and String libraries, punctuations, numbers, special characters, etc. were removed. Cleaned text excerpts were then vectorized using SKLearn TFIDF and CountVectorizer packages. The term-document matrices underwent dimensionality reduction using Non-negative Matrix Factorization (NMF) or Latent Semantic Analysis (LAS, Truncated SVD) algorithms from SKLearn. After the selection of the final vectorizer and topic modeler, the raw topics were evaluated and interpreted using exploratory data analysis (EDA) and domain knowledge.

### Results

Amon the combinations of topic modeler and vectorizer examined, NMF with 10 topics (PCs) combined with CountVectorizer and a costume stop-word list, resulted in the most reasonable raw topics:

<img width="921" alt="download" src="https://user-images.githubusercontent.com/84594280/142655816-259c19f7-9a56-492a-8d66-c241200b42e2.png">

In order to evaluate and interpret these raw topics, the PCA dataframe were used and each topic were tagged based on two criteria:

1) The average of each PC (topic) values for each author<br>
2) The share of each author of the top 1000 philosophers with the highest score for that topic (normalized)<br>

Using EDA based on these two criteria and domain knowledge, topic evaluation and interpretation were performed on the raw topics and they have been tagged as follow:

Topic 0: __German Idealism__<br>
Topic 1: __Feminism__<br>
Topic 2 & 7: __Rationalism__<br>
Topic 3: __Ethics__<br>
Topic 4: __Marxism/Capitalism__<br>
Topic 5: __Kantism__<br>
Topic 6: __Continental__<br>
Topic 8: __Empiricism/Idealism__<br>
Topic 9: __Analytic__<br>
