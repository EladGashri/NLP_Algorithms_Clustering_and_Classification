The aim of the project is to compare the difference between 2 known Natural Language Processing (NLP) algorithms in regards to analyzing medical textual data. The 2 NLP algorithms are: Word2vec and TF-IDF. The data are over 3,000 medical notes from visits to medical professionals.

For each one of the 2 NLP algorithms there are 2 tasks, in the fields of unsupervised learning and supervised learning:
1. Unsupervised learning: Cluster the texts to clusters using K-means.
2. Supervised learning: Classify each text to the correct diagnosis. In the Word2vec algorithm a RNN (Recurrent Neural Network) algorithm preforms the classification and in the TF-IDF algorithm a Random forest algorithm does.

A database in MongoDB stores the texts and details about the final K-means clusters for each algorithm.

The algorithms were deployed as a REST API with multiprocessing with Python and Flask. The API receives from a request an unknown medical text and returns one of the following:
1. Most common labels and closest sentences in the cluster assigned to the text according to the Word2vec & K-means algorithm or the TF-IDF & K-means algorithm.
2. Predicted diagnosis for the condition described in the text according to the Word2vec & RNN algorithm or the TF-IDF & Random forest algorithm.

Technologies used in the project: Python,  Flask, MongoDB, PyTorch, Gensim, Scikit-learn.
