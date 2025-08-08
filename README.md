# Breast-Cancer-Classification-with-Logistic-Regression
This project implements a binary classification model using Logistic Regression to predict whether a tumor is malignant or benign based on the features from the Wisconsin Breast Cancer dataset. The entire analysis, from data preparation to model evaluation and tuning, is documented in the accompanying Jupyter Notebook.

---

## The Dataset

The project uses the **Wisconsin Breast Cancer dataset**, which contains 30 numerical features computed from a digitized image of a fine needle aspirate (FNA) of a breast mass. The goal is to classify tumors into two categories:
- **Malignant (M)**
- **Benign (B)**

---

## Project Workflow

### 1. Data Preprocessing
- **Data Loading**: The dataset was loaded and inspected for quality.
- **Data Cleaning**: Unnecessary columns ('id' and an empty 'Unnamed: 32' column) were dropped.
- **Encoding**: The categorical target variable 'diagnosis' was converted into a numerical format (M=1, B=0).
- **Feature Scaling**: All 30 features were standardized using `StandardScaler` to ensure they have a mean of 0 and a standard deviation of 1. This is crucial for the optimal performance of logistic regression.

### 2. Model Training & Evaluation
A logistic regression model was trained to classify the tumors.
- **Train-Test Split**: The data was split into a training set (70%) and a testing set (30%).
- **Model Training**: The classifier was trained on the scaled training data.
- **Evaluation**: The model's performance on the unseen test data was evaluated using several key metrics:
    - **Accuracy**: Achieved an overall accuracy of **97%**.
    - **Confusion Matrix**: Visualized to understand the model's performance in terms of true positives, true negatives, false positives, and false negatives.
    - **Precision & Recall**: The model showed high precision (98%) and recall (94%) for identifying malignant tumors.
    - **ROC-AUC Score**: Achieved an outstanding ROC-AUC score of **0.9975**, indicating an excellent ability to distinguish between the two classes.

### 3. Threshold Tuning
The project also demonstrates the importance of the classification threshold.
- **The Sigmoid Function**: The core of logistic regression, which outputs a probability between 0 and 1, was explained.
- **Tuning for Recall**: By lowering the default decision threshold from 0.5 to 0.3, we successfully **increased the recall for malignant cases from 94% to 97%**, thereby reducing the number of dangerous False Negatives. This highlights the critical trade-off between precision and recall in a medical diagnosis context.

---

## How to Run the Code
1. Ensure you have Python and Jupyter Notebook installed.
2. Clone this repository to your local machine.
3. Install the required libraries:
   ```bash
   pip install pandas numpy scikit-learn matplotlib seaborn
Open and run the Jupyter Notebook to see the full analysis.

Libraries Used

pandas

numpy

scikit-learn

matplotlib

seaborn
