# **Sentiment Analysis of IMDb Movie Reviews for Film Junky Union**

## **Introduction**
The Film Junky Union, a community for classic movie lovers, aims to create a sentiment analysis system to filter and categorize movie reviews. By leveraging IMDb movie reviews, this project develops machine learning models to classify review sentiments (positive or negative) with an F1 score target of at least **0.85**. Through iterative experimentation with various text preprocessing techniques and models, this project identifies the best-performing solution for reliable sentiment detection.

---

## **Project Goal**
The primary goal is to build a robust machine learning model that classifies IMDb movie reviews into positive or negative sentiments with a minimum F1 score of **0.85**. This system will enable Film Junky Union to automatically detect and address negative feedback.

---

## **Table of Contents**
- [Introduction](#introduction)
- [Project Goal](#project-goal)
- [Tools and Libraries](#tools-and-libraries)
- [Workflow and Methodologies](#workflow-and-methodologies)
  - [1. Data Preparation](#1-data-preparation)
  - [2. Exploratory Data Analysis (EDA)](#2-exploratory-data-analysis-eda)
  - [3. Model Development](#3-model-development)
  - [4. Model Evaluation](#4-model-evaluation)
  - [5. Advanced Modeling](#5-advanced-modeling)
  - [6. Model Comparison](#6-model-comparison)
- [Results](#results)
- [Conclusions and Key Insights](#conclusions-and-key-insights)
- [Future Improvements](#future-improvements)
- [How to Run](#how-to-run)
- [Contact](#contact)

---

## **Tools and Libraries**
- **Programming Language**: Python
- **Libraries**:
  - **Data Handling**: pandas, numpy
  - **Visualizations**: seaborn, matplotlib
  - **Natural Language Processing**: nltk, spaCy, transformers
  - **Machine Learning**: scikit-learn, LightGBM
  - **Pretrained Models**: BERT (transformers library)

---

## **Workflow and Methodologies**

### **1. Data Preparation**
- **Dataset**: IMDb movie reviews labeled with positive (1) and negative (0) sentiments.
- **Preprocessing Steps**:
  - Removed duplicates and missing values.
  - Normalized text (lowercased, removed punctuation).
  - Split data into training and test sets.

### **2. Exploratory Data Analysis (EDA)**
- **Insights**:
  - Sentiment labels were balanced (50% positive, 50% negative).
  - Reviews showed polarized ratings, with most ratings at the extreme ends (1 and 10).
  - Temporal trends revealed increasing review frequency over the years.

### **3. Model Development**
- **Baseline Model**:
  - **DummyClassifier**: Predicted the most frequent class (accuracy = 50%, F1 = 0.0).
- **Advanced Models**:
  - Logistic Regression with TF-IDF vectorization.
  - LightGBM Classifier.
  - Transformer-based embeddings (BERT).

### **4. Model Evaluation**
- Metrics:
  - **F1 Score**: Measures the balance between precision and recall.
  - **Accuracy**: Proportion of correct predictions.
  - **ROC AUC**: Discriminative ability across thresholds.
  - **APS (Average Precision Score)**: Precision-recall balance.

### **5. Advanced Modeling**
- **spaCy Preprocessing**:
  - Applied lemmatization and stopword removal for cleaner text.
- **BERT Embeddings**:
  - Leveraged pretrained transformer-based embeddings for rich semantic representation.
- **LightGBM**:
  - Trained a gradient boosting model for efficient text classification.

### **6. Model Comparison**
| **Model**         | **Preprocessing**         | **F1 Score (Test)** | **ROC AUC** | **Accuracy** |
|--------------------|---------------------------|----------------------|-------------|--------------|
| Dummy Classifier   | None                     | 0.0                  | 0.50        | 50%          |
| Logistic Regression| TF-IDF                   | 0.88                 | 0.95        | 88%          |
| Logistic Regression| TF-IDF + spaCy           | 0.87                 | 0.95        | 87%          |
| LightGBM           | TF-IDF + spaCy           | 0.86                 | 0.93        | 85%          |
| BERT + Logistic    | BERT Embeddings          | 0.89 (sampled data)  | 0.94        | 90%          |

---

## **Results**
- The **BERT-based model** demonstrated the best semantic understanding, outperforming simpler models in F1 score and interpretability.
- **Logistic Regression with TF-IDF and spaCy** preprocessing offered a strong trade-off between performance and computational efficiency.

---

## **Conclusions and Key Insights**
1. **Preprocessing Matters**: Lemmatization and stopword removal improved performance by standardizing text input.
2. **BERT Embeddings**: Captured deep contextual meaning, significantly enhancing sentiment classification.
3. **Model Performance**:
   - Baseline models performed poorly, highlighting the necessity for advanced preprocessing and algorithms.
   - Logistic Regression with TF-IDF offered simplicity with strong results.
   - BERT embeddings paired with Logistic Regression achieved the highest accuracy and F1 score on sampled data.

---

## **Future Improvements**
1. **Full Dataset BERT Training**:
   - Use GPUs to train on the entire dataset for further performance gains.
2. **Hyperparameter Tuning**:
   - Experiment with LightGBM and BERT hyperparameters to optimize performance.
3. **Real-Time Prediction**:
   - Deploy the best-performing model for live review sentiment classification.
4. **Incorporate Sentiment Trends**:
   - Analyze temporal sentiment trends to better understand audience preferences.

---

## **How to Run**
1. Clone the repository:
   ```bash
   git clone https://github.com/navarroal95/Data-projects-TripleTen.git
   cd Data-projects-TripleTen/IMDb-Sentiment-Analysis

