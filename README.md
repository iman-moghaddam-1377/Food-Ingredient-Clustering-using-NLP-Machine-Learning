# 🍽️ Food Ingredient Clustering using NLP & Machine Learning

![Python](https://img.shields.io/badge/Python-3.9+-blue.svg)
![NLP](https://img.shields.io/badge/NLP-Word2Vec-orange.svg)
![ML](https://img.shields.io/badge/MachineLearning-KMeans-red.svg)
![Status](https://img.shields.io/badge/Status-Completed-success.svg)

---

## 📌 Project Overview

This project focuses on **clustering foods based on their ingredients** using Natural Language Processing (NLP) and Machine Learning techniques.

The main idea is to extract ingredients from recipes, represent them numerically, and group similar foods together based on their ingredient composition.

---

## 📊 Dataset

* Input: Recipe dataset containing food instructions and ingredients
* Goal: Extract and analyze ingredient lists
* Output: Clustered groups of similar foods

---

## 🧹 Preprocessing

Each recipe is processed using standard NLP techniques:

* Convert text to lowercase
* Remove punctuation
* Remove stopwords
* Normalize words (e.g., removing plural forms like *s/es*)
* Tokenize ingredients

---

## 🔢 Feature Engineering

### 1. One-Hot Encoding

* Extract all unique ingredients
* Create a **one-hot vector** for each ingredient
* Represent each recipe as a combination of ingredient vectors

Example:

```
       A  B  C  D
Rec1   1  0  0  1
Rec2   0  0  1  0
```

---

### 2. Word2Vec Embedding

* Train or use pretrained Word2Vec embeddings
* Generate vector representation for each ingredient
* Compute **average embedding per recipe**

---

## 🤖 Clustering

Clustering is performed using **K-Means**:

### 🔹 Approach 1:

* Input: One-hot encoded vectors

### 🔹 Approach 2:

* Input: Averaged Word2Vec vectors

### 📉 Optimal Clusters

* Use the **Elbow Method** to determine the optimal number of clusters

---

## 📊 Results

### ✅ Evaluation Strategy

* Compare clusters qualitatively
* Identify differences in ingredient distributions
* Analyze top ingredients per cluster

### 🔍 Insights

* Similar cuisines/recipes tend to cluster together
* Word2Vec-based clustering captures **semantic similarity** better
* One-hot encoding captures **exact ingredient overlap**




