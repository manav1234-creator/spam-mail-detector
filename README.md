# 📧 Spam Mail Detection using Machine Learning

## 📌 Project Overview

This project uses **Machine Learning and Natural Language Processing (NLP)** to classify text messages as **Spam** or **Ham (Not Spam)**.

The model analyzes the content of a message, converts the text into numerical features using **TF-IDF**, and predicts whether the message is spam or legitimate.

---

## 🎯 Objectives

* Detect spam messages automatically
* Clean and preprocess text data
* Convert text into numerical features using TF-IDF
* Train a Machine Learning classification model
* Evaluate model performance using standard classification metrics
* Test the model on new/unseen messages

---

## 🛠️ Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Regular Expressions
* NLP
* Scikit-learn
* TF-IDF Vectorization
* Multinomial Naive Bayes
* Google Colab

---

## 📂 Dataset

The project uses a labeled message dataset containing two classes:

| Label  | Meaning            |
| ------ | ------------------ |
| `ham`  | Legitimate message |
| `spam` | Spam message       |

The practice dataset contains **1,000 messages**:

* 500 Ham messages
* 500 Spam messages

The original dataset is based on the SMS spam classification problem. The dataset used in this repository is a **synthetic practice dataset** prepared for this project.

---

## 🔄 Project Workflow

```text
                 ┌─────────────────────┐
                 │     Input Dataset   │
                 │  Spam / Ham Messages│
                 └──────────┬──────────┘
                            │
                            ▼
                 ┌─────────────────────┐
                 │   Data Exploration  │
                 │ Shape, Missing Data │
                 │ Duplicates, Labels  │
                 └──────────┬──────────┘
                            │
                            ▼
                 ┌─────────────────────┐
                 │    Text Cleaning    │
                 │ Lowercase           │
                 │ Remove URLs         │
                 │ Remove punctuation  │
                 │ Remove numbers      │
                 └──────────┬──────────┘
                            │
                            ▼
                 ┌─────────────────────┐
                 │   Label Encoding    │
                 │ Ham  → 0            │
                 │ Spam → 1            │
                 └──────────┬──────────┘
                            │
                            ▼
                 ┌─────────────────────┐
                 │ Train / Test Split  │
                 │      80% / 20%      │
                 └──────────┬──────────┘
                            │
                            ▼
                 ┌─────────────────────┐
                 │   TF-IDF Vectorizer │
                 │ Text → Numerical    │
                 │ Features            │
                 └──────────┬──────────┘
                            │
                            ▼
                 ┌─────────────────────┐
                 │ Multinomial Naive   │
                 │ Bayes Classifier    │
                 └──────────┬──────────┘
                            │
                            ▼
                 ┌─────────────────────┐
                 │    Evaluation       │
                 │ Accuracy            │
                 │ Precision           │
                 │ Recall              │
                 │ F1-Score            │
                 │ Confusion Matrix    │
                 └──────────┬──────────┘
                            │
                            ▼
                 ┌─────────────────────┐
                 │ New Message         │
                 │ Spam / Ham          │
                 │ Prediction          │
                 └─────────────────────┘
```

---

## 🧹 Data Preprocessing

The text data is cleaned before training the model.

Main preprocessing steps:

1. Convert text to lowercase
2. Remove URLs
3. Remove punctuation
4. Remove numbers
5. Remove extra spaces
6. Encode labels into numerical values

---

## 🔢 Feature Extraction — TF-IDF

Machine Learning models cannot directly understand raw text.

Therefore, **TF-IDF (Term Frequency-Inverse Document Frequency)** is used to convert text messages into numerical feature vectors.

```text
Text Message
     ↓
Text Cleaning
     ↓
TF-IDF Vectorization
     ↓
Numerical Feature Vector
     ↓
Machine Learning Model
```

---

## 🤖 Machine Learning Model

### Multinomial Naive Bayes

The project uses **Multinomial Naive Bayes**, which is commonly used for text classification problems.

It learns patterns from the training messages and predicts whether a new message belongs to the `spam` or `ham` class.

---

## 📊 Model Evaluation

The model is evaluated using:

* Accuracy
* Precision
* Recall
* F1-Score
* Confusion Matrix

Example evaluation structure:

```text
                    Predicted
                 Ham       Spam
Actual Ham       TN         FP
Actual Spam      FN         TP
```

The notebook also generates visualizations for class distribution, confusion matrix, and model performance.

---

## 🧪 Example Predictions

The trained model can classify new messages such as:

```text
"Congratulations! You have won a cash prize. Claim now."
```

Prediction:

```text
SPAM
```

Example legitimate message:

```text
"Can you send me the notes from today's lecture?"
```

Prediction:

```text
HAM
```

---

## 📁 Project Structure

```text
spam-mail-detector/
│
├── spam_mail_detector.ipynb
├── processed_spam_dataset.csv
└── README.md
```

### Files

**`spam_mail_detector.ipynb`**

Complete Google Colab notebook containing data preprocessing, EDA, model training, evaluation, and prediction.

**`processed_spam_dataset.csv`**

Processed dataset generated during the project.

**`README.md`**

Project documentation.

---

## 🚀 How to Run the Project

### 1. Open the notebook

Open:

```text
spam_mail_detector.ipynb
```

using Google Colab.

### 2. Upload the dataset

The original raw dataset is not stored in this GitHub repository.

Upload the required CSV file in Colab when prompted.

### 3. Run all cells

Run the notebook from top to bottom.

The notebook will:

```text
Load Data
    ↓
Clean Text
    ↓
Perform EDA
    ↓
Split Dataset
    ↓
Apply TF-IDF
    ↓
Train Model
    ↓
Evaluate Model
    ↓
Predict New Messages
```

---

## 💡 Key Learning Outcomes

Through this project, I learned:

* Text data preprocessing
* Basic NLP concepts
* Exploratory Data Analysis
* TF-IDF feature extraction
* Train-test splitting
* Naive Bayes classification
* Model evaluation
* Confusion matrix interpretation
* Building a simple text classification system

---

## 🔮 Future Improvements

The project can be further improved by:

* Testing Logistic Regression and SVM
* Using Word2Vec or modern embeddings
* Implementing deep learning models
* Building a Streamlit web application
* Adding an email/message input interface
* Deploying the model online
* Comparing multiple ML algorithms

---

## 👨‍💻 Author

**Manav Verma**

B.Tech CSE (AI)

GitHub: Add your GitHub profile link here

LinkedIn: Add your LinkedIn profile link here

---

## ⭐ Conclusion

This project demonstrates how **Machine Learning and NLP** can be used to automatically identify spam messages.

The complete pipeline covers **data preprocessing → NLP feature extraction → model training → evaluation → prediction**, making it a practical beginner-level Machine Learning project.
