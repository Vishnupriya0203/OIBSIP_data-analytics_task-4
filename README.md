# OIBSIP_data-analytics_task-4
Twitter Sentiment Analysis using Machine Learning
---

# Twitter Sentiment Analysis using Machine Learning

## Project Overview

This project focuses on **Sentiment Analysis of Twitter data** using **Machine Learning techniques**. The goal is to analyze tweets and classify them into **Positive, Negative, or Neutral sentiments**.

The project uses **Natural Language Processing (NLP)** techniques to clean the text data and convert it into numerical features using **TF-IDF vectorization**. Two machine learning models — **Multinomial Naive Bayes** and **Support Vector Machine (SVM)** — are trained and evaluated to predict sentiment.

---

## Objectives

* To preprocess and clean Twitter text data
* To perform sentiment classification using machine learning models
* To convert text data into numerical format using **TF-IDF Vectorization**
* To compare the performance of **Naive Bayes** and **SVM** models
* To visualize model performance using **confusion matrices**

---

## Technologies Used

* **Python**
* **Jupyter Notebook**
* **Pandas** – Data manipulation
* **NumPy** – Numerical operations
* **Matplotlib** – Data visualization
* **Seaborn** – Statistical visualization
* **Scikit-learn** – Machine learning models

---

## Dataset

The dataset used is **Twitter_Data.csv**, which contains:

* **clean_text** – Preprocessed tweet text
* **category** – Sentiment label (-1, 0, 1)

Sentiment labels represent:

* **-1 → Negative**
* **0 → Neutral**
* **1 → Positive**

---

# Project Workflow

## 1. Importing Libraries

Necessary libraries were imported for **data processing, visualization, and machine learning**.

Libraries used include:

* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn

---

## 2. Loading the Dataset

The dataset was loaded using Pandas.

```python
df = pd.read_csv("Twitter_Data.csv")
```

Basic dataset exploration was done using:

* `df.head()`
* `df.info()`
* `df.isnull().sum()`

---

## 3. Data Cleaning

Missing values were removed to ensure clean data.

```python
df.dropna(inplace=True)
```

Column names were renamed for easier usage:

* `clean_text` → **text**
* `category` → **sentiment**

---

## 4. Data Visualization

A **count plot** was used to visualize the distribution of sentiments in the dataset.

This helps understand whether the dataset is balanced between **positive, negative, and neutral tweets**.

---

## 5. Text Preprocessing

A custom function was created to clean the tweet text.

The following steps were performed:

* Convert text to **lowercase**
* Remove **URLs**
* Remove **user mentions**
* Remove **hashtags**
* Remove **punctuation**
* Remove **numbers**

This ensures that the text is standardized before machine learning processing.

---

## 6. Train-Test Split

The dataset was divided into **training and testing data**.

* **80% Training Data**
* **20% Testing Data**

This helps evaluate the model’s performance on unseen data.

---

## 7. Text Vectorization

Text data was converted into numerical format using **TF-IDF Vectorizer**.

TF-IDF helps measure the importance of words in a document relative to the entire dataset.

Key parameters used:

* `stop_words = 'english'`
* `max_features = 5000`

---

## 8. Naive Bayes Model

The **Multinomial Naive Bayes** classifier was trained using the TF-IDF features.

Model evaluation includes:

* **Accuracy Score**
* **Classification Report**
* **Confusion Matrix**

A confusion matrix heatmap was generated to visualize prediction results.

---

## 9. Support Vector Machine (SVM)

A **Linear Support Vector Machine (SVM)** model was trained and tested on the dataset.

Performance metrics evaluated include:

* **Accuracy Score**
* **Precision**
* **Recall**
* **F1 Score**

A confusion matrix was also visualized using a heatmap.

---

## 10. Sentiment Prediction

The trained model can predict sentiment for new tweets.

Example:

```
Input Tweet:
"Modi government has done excellent work"
```

The model processes the text and predicts whether the sentiment is **Positive, Neutral, or Negative**.

---

# Key Insights

* Text preprocessing significantly improves model performance.
* TF-IDF effectively converts textual data into numerical features.
* Both **Naive Bayes and SVM** can classify tweet sentiments effectively.
* SVM generally performs better for text classification tasks.

---

# Conclusion

This project demonstrates how **Natural Language Processing and Machine Learning** can be used to analyze public sentiment from social media data. Sentiment analysis helps organizations and governments understand public opinion and improve decision-making.

---

# Author

**Kaviya N**
Data Analytics Intern – Oasis Infobyte

---
