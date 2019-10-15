# A Review of Text Classification Methods

## I. Introduction

This repository is an effort to illustrate and review different text classification techniques. This project is not about showcasing and comparing different machine learning algorithms per se, but it is more concerned with the different approaches and representations one can use when attempting to solve a text classification task.

## II. Approaches

There are generally two classes of models to solve a text classification problem : Bag of Words like models, which represent a text document as an unordered set of words, and assigns a score to each one of them, and Sequence models, which leverage the sequential nature of text data and represent it as a set of successive words. We will present two approaches in each of these classes.

### 1. Bag Of Words

The first technique starts by building a vocabulary of words from all available documents, then proceeds to convert each text document into a vector of values, each corresponding to a vocabulary term. The result is usually referred to as the **Document-Term Matrix** where each row represents a different document, and each column represents a specific word from the vocabulary. The values of the matrix can be one of several available scoring metrics : either a simple count of occurences (how many times **word<sub>j</sub>** appears in **document<sub>i</sub>**) or a more elaborate measure such as the TF-IDF (Term Frequency Inverse Document Frequency). As such, we end up with a numeric matrix that can be fed directly to a classification model to learn the mapping between this bag of words document representation and the corresponding labels. In this case all standard classifiers can be applied, but it is usually best to make use of Linear Classifiers such as Logistic Regression, Naive Bayes (usually) or Linear SVM, as opposed to highly non linear ones such as Decision Tree-based algorithms. In this notebook, we use Logistic Regression.

Despite its simplicity, the standard Bag Of Words approach works really well for text classification problems, and is also arguably the fastest in terms of training. The reason being that the information necessary to distinguish between different classes of text is more dependent on the presence of certain words and the absence of others, rather than their order of appearance of these words. This means that discarding the order doesn't hinder the performance of our classifiers,quite the opposite, it simplifies the representation of the problem for fast and accurate results.

### 2. Word Embeddings and Document Quantization

TODO.


### 3. Word Embeddings and Neural Networks

TODO.

### 4. Language Models

TODO.