# Classification of Alzheimer’s Disease using Handwriting Analysis

This project focuses on leveraging machine learning and handwriting analysis to address the urgent need for early and accurate diagnosis of Alzheimer's disease. By utilizing the DARWIN dataset, the project develops and evaluates machine learning models to distinguish between healthy individuals and Alzheimer's patients. The results demonstrate the potential of handwriting analysis as a non-invasive and cost-effective diagnostic tool.

---

## Table of Contents
1. [Usage](#usage)
2. [Introduction](#introduction)
3. [Motivation](#motivation)
4. [Objectives](#objectives)
5. [Methodology](#methodology)
6. [Results](#results)
7. [Visualizations](#visualizations)

---

## Usage
To reproduce the results, follow these steps:

1. Clone the repository:
   ```bash
   git clone https://github.com/nobir/predictions-of-alzheimers-disease-using-handwriting-analysis.git
2. Install the required dependencies:

   ```bash
   pip install -r requirements.txt
   Run the Jupyter notebook:
   ```
3. Run the Jupyter notebook:
   ```bash
   jupyter notebook main.ipynb
   ```

---

## Introduction
Neurodegenerative diseases (NDs), such as Alzheimer's and Parkinson's, pose significant challenges to healthcare systems worldwide. These diseases progressively impair nerve cells, leading to severe cognitive and motor deficits. Traditional diagnostic methods often fail to provide timely and accurate identification, hindering effective treatment and intervention. This project explores the use of machine learning and handwriting analysis to bridge this diagnostic gap. By analyzing handwriting dynamics, we aim to develop a predictive tool for the early diagnosis of Alzheimer's disease.

---

## Motivation
The motivation behind this project stems from the increasing prevalence of neurodegenerative diseases and the limitations of traditional diagnostic methods. Handwriting, as a complex integration of motor and cognitive processes, serves as a valuable indicator of disease progression. By leveraging machine learning, we aim to create a non-invasive and cost-effective diagnostic tool that can enhance early detection and improve patient outcomes.

---

## Objectives
The primary objectives of this project are:
1. **Develop Machine Learning Models**: Utilize the DARWIN dataset to design and train machine learning classifiers capable of distinguishing between healthy individuals and Alzheimer's patients.
2. **Validate Model Performance**: Assess the models using performance metrics such as accuracy, precision, recall, and F1-score.
3. **Contribute to Healthcare**: Provide medical practitioners with an accessible and timely diagnostic tool for neurodegenerative diseases.
4. **Advance Research**: Foster collaboration and expertise in machine learning and neurodegenerative disease research.

---

## Methodology
The project follows a structured methodology, as illustrated below:

### Data Collection
The dataset used in this project is the DARWIN dataset, obtained from the UCI Machine Learning Repository. It contains handwriting data from 174 participants (89 Alzheimer's patients and 85 healthy individuals) and includes 451 features.

### Data Preprocessing
- Dropped the 'ID' column.
- Checked for missing values (none found).
- Scaled the features for normalization.
- Split the data into independent (X) and dependent (y) variables.

### Feature Selection
- Used Random Forest Classifier to calculate feature importance.
- Dropped features with an importance score of zero.
- Split the remaining features into subsets for further analysis.

### Model Development
- Trained models using `LazyPredict` to identify the best-performing baseline models.
- Selected the LightGBM (LGBM) model for further tuning.
- Tuned the LGBM model using GridSearchCV to optimize hyperparameters.

### Model Evaluation
- Evaluated the model using metrics such as accuracy, precision, recall, F1-score, and ROC-AUC.
- Compared the performance of the baseline and tuned models.

---

## Results
The tuned LightGBM model achieved the following results:
- **Accuracy**: 88%
- **Precision**: 0.67 (Class 1)
- **Recall**: 0.73 (Class 1)
- **F1-score**: 0.70 (Class 1)
- **ROC-AUC**: 0.78

The model demonstrated strong performance in distinguishing between healthy individuals and Alzheimer's patients, although the accuracy of the tuned model was slightly lower than the baseline due to cross-validation during hyperparameter tuning.

---

## Visualizations
Below are key visualizations from the project:

### Feature Importance
![Feature Importance](image/Feature%20Importances.png)
*Description: This plot shows the importance of each feature as determined by the Random Forest Classifier.*

### Model Comparison
![Model Comparison](image/Compare%20Lazypredict%20Model%20vs%20Tuning%20Model.png)
*Description: Comparison of the baseline Lazypredict model and the tuned LightGBM model.*

### Precision-Recall Curve
![Precision-Recall Curve](image/Precision-Recall%20Curve%20(Tuning%20LGBM).png)
*Description: The precision-recall curve for the tuned LightGBM model.*

### ROC Curve
![ROC Curve](image/Receiver%20Operating%20Characteristic%20(ROC)%20Curve%20(Tuning%20Model).png)
*Description: The ROC curve for the tuned LightGBM model, showing an AUC of 0.78.*

### Confusion Matrix
![Confusion Matrix](image/Confusion%20Matrix%20(Tuning%20LGBM).png)
*Description: The confusion matrix for the tuned LightGBM model, showing true positives, true negatives, false positives, and false negatives.*

### F1-score Curve
![F1-score Curve](image/F1-score%20Curve%20(Tuning%20LGBM).png)
*Description: The F1-score curve for the tuned LightGBM model.*

---
