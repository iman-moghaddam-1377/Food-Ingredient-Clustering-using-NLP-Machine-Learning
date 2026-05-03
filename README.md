# 🍽️ Food Ingredient Clustering using NLP, PySpark & Machine Learning

![Python](https://img.shields.io/badge/Python-3.9+-blue.svg)
![PySpark](https://img.shields.io/badge/PySpark-BigData-orange.svg)
![NLP](https://img.shields.io/badge/NLP-Word2Vec-yellow.svg)
![ML](https://img.shields.io/badge/MachineLearning-KMeans-red.svg)
![Status](https://img.shields.io/badge/Status-Completed-success.svg)

---

## 📌 Project Overview

This project focuses on **clustering foods based on their ingredients** using **PySpark, NLP, and Machine Learning**.

The pipeline processes large-scale recipe data using **PySpark** for distributed computation, then applies feature extraction and clustering techniques to group similar foods.

---

## ⚡ Tech Stack

* **PySpark (Apache Spark)** for distributed data processing
* **Python**
* **NLP techniques** (tokenization, normalization)
* **Word2Vec (Spark MLlib)**
* **K-Means Clustering (Spark MLlib)**

---

## 📊 Dataset

* Recipe dataset containing ingredients and cooking instructions
* Processed in a distributed manner using **PySpark DataFrames**

---

## 🧹 Preprocessing (PySpark)

All preprocessing is implemented using **PySpark transformations**:

* Convert text to lowercase
* Remove punctuation
* Remove stopwords
* Normalize tokens (e.g., plural → singular)
* Tokenize ingredient lists

---

## 🔢 Feature Engineering

### 1. One-Hot Encoding (Spark)

* Extract all unique ingredients
* Generate **sparse vectors** using PySpark
* Represent each recipe as a feature vector

---

### 2. Word2Vec (PySpark MLlib)

* Train Word2Vec model using Spark
* Generate vector embeddings for ingredients
* Compute **average vector per recipe**

---

## 🤖 Clustering (PySpark MLlib)

Clustering is performed using **K-Means in PySpark**:

### 🔹 Approach 1:

* Input: One-hot encoded vectors

### 🔹 Approach 2:

* Input: Averaged Word2Vec vectors

### 📉 Optimal Clusters

* Determined using the **Elbow Method**

---

## 📊 Results

### ✅ Evaluation

* Cluster comparison based on ingredient similarity
* Identification of dominant ingredients per cluster
* Analysis of cluster coherence

### 🔍 Key Findings

* One-hot encoding captures **exact ingredient overlap**
* Word2Vec captures **semantic similarity between ingredients**
* PySpark enables efficient processing of large datasets


