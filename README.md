![Google Colab](https://img.shields.io/badge/Google%20Colab-%23F9A825.svg?style=for-the-badge&logo=googlecolab&logoColor=white) ![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54) ![Jupyter Notebook](https://img.shields.io/badge/jupyter-%23FA0F00.svg?style=for-the-badge&logo=jupyter&logoColor=white) ![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white) ![scikit-learn](https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=for-the-badge&logo=scikit-learn&logoColor=white) ![Matplotlib](https://img.shields.io/badge/Matplotlib-%23ffffff.svg?style=for-the-badge&logo=Matplotlib&logoColor=black) 

<h1 align="center">⚡ Electricity Theft Detection using Machine Learning</h1>

Electricity theft is a major issue worldwide, especially in regions with rapidly growing energy demands. This project aims to develop a machine learning-based solution to automatically detect instances of electricity theft based on user consumption patterns.

> This work was developed as part of the *Introduction to Machine Learning* course and focuses on data preprocessing, handling class imbalance, training various classifiers, and evaluating performance to build a robust and scalable fraud detection system.

<details>
  <summary><h2>📚 Table of Contents (Click to Expand)</h2></summary>

- [🧩 Problem Statement](#-problem-statement)
- [📂 Dataset Overview](#-dataset-overview)
- [🔍 Approach \& Methodology](#-approach--methodology)
  - [🧼 1. Data Preprocessing](#-1-data-preprocessing)
  - [⚖️ 2. Tackling Class Imbalance](#️-2-tackling-class-imbalance)
  - [🧠 3. Model Development](#-3-model-development)
  - [📈 4. Model Evaluation](#-4-model-evaluation)
- [🥇 Best Results](#-best-results)
- [🧱 Project Structure](#-project-structure)
- [🔧 Tech Stack](#-tech-stack)
- [🚀 Future Enhancements](#-future-enhancements)
- [👨‍💻 Contributors](#-contributors)
- [📜 License](#-license)

</details>

---

## 🧩 Problem Statement

Traditional methods of identifying electricity theft are reactive, manual, and not scalable. With the availability of smart meter data, machine learning offers a proactive approach to detect anomalies and classify theft patterns efficiently.

The goal of this project is to build a supervised classification model that:
- Detects theft based on energy consumption data
- Classifies the type of theft (6 types)
- Handles highly imbalanced datasets effectively

---

## 📂 Dataset Overview

- Contains hourly/daily electricity consumption records from multiple consumer types
- Labeled data includes:
  - `0`: Normal usage
  - `1-6`: Different categories of electricity theft
- Challenges include:
  - High class imbalance (normal consumers far outnumber thieves)
  - Noisy, real-world data

---

## 🔍 Approach & Methodology

### 🧼 1. Data Preprocessing
- Null value handling
- Normalization and scaling
- Feature selection and encoding
- Class relabeling for theft types

### ⚖️ 2. Tackling Class Imbalance
Used the following resampling and weighting techniques:
- **SMOTE** (Synthetic Minority Over-sampling Technique)
<!-- - **ADASYN** (Adaptive Synthetic Sampling) -->
- **Class Weights** (for ANN and tree-based classifiers)

### 🧠 3. Model Development
Trained and tested various models:
- Logistic Regression
- Support Vector Machines
- Decision Trees and Random Forest
- Gradient Boosting and **XGBoost**
- **Artificial Neural Networks (ANN)**
- **Stacking Classifier (Ensemble of best models)**

### 📈 4. Model Evaluation
- Used multiple metrics to evaluate model effectiveness:
  - Accuracy, Precision, Recall, F1-Score
  - ROC-AUC Score
  - Confusion Matrix
- Paid special attention to **Recall** and **F1-score** due to class imbalance

---

## 🥇 Best Results

| Model                | Accuracy | F1-Score | Recall |
|---------------------|----------|----------|--------|
| XGBoost             | ✅ High   | ✅ High   | ✅ High |
| Stacking Ensemble   | ✅ High   | ✅ High   | ✅ Highest |
| ANN (with weights)  | Moderate | Good     | Good   |

📌 **Key Insight**: Ensemble methods like stacking consistently outperformed individual models, especially on minority theft classes.

---

## 🧱 Project Structure

```
📦 Electricity-Theft-ML
├── 📁 MISC/                     # Miscellaneous notebooks or notes
│   └── main.ipynb
├── 📁 src/                      # Core notebooks for model development
│   ├── Ensemble.ipynb
│   ├── eda.ipynb
│   └── hyperparam_tuning.ipynb
├── 📄 .gitignore                # Files/folders to ignore in version control
├── 📄 LICENSE                   # License file
├── 📄 README.md                 # Project overview (this file)
├── 📄 TODO.MD                  # To-do list for the project
├── 📄 dataset-mendley.zip       # Original dataset archive
├── 📄 df.csv                    # Preprocessed dataset
├── 📄 results.ipynb             # Results and evaluation notebook

```


---

## 🔧 Tech Stack

- **Python**
- **scikit-learn**, **imbalanced-learn**
- **XGBoost**, **Keras** 
- **Matplotlib**, **Seaborn** (visualization)
- **Jupyter Notebooks** for experimentation

---

## 🚀 Future Enhancements

- Integrate **Time-Series Models** (LSTM/GRU) for temporal theft pattern learning
- Explore **Anomaly Detection** methods (Isolation Forest, Autoencoders)
- Deploy model as a REST API using Flask or FastAPI
- Integrate into real-time power monitoring systems with alert triggers

---

## 👨‍💻 Contributors

- [Aryan](https://www.linkedin.com/in/aryan-jaljith-64283b240/)
- [Karthik](https://www.linkedin.com/in/karthik-krishnamurthi)
- [Namitha](https://www.linkedin.com/in/namitha-madhu-4934a8276/)
- [Anmol](https://www.linkedin.com/in/anmolkrish/)
---

## 📜 License

This project is licensed under the MIT License – see the [LICENSE](LICENSE) file for details.

---

> ⚠️ Disclaimer: This project is for academic and research purposes. Real-world deployment would require privacy considerations, secure infrastructure, and domain-specific validation.

