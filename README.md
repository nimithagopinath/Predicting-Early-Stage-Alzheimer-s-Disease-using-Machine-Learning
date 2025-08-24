# Predicting-Early-Stage-Alzheimer-s-Disease-using-Machine-Learning

Alzheimer’s disease (AD) is a prevalent neurodegenerative
disorder that primarily affects older adults and leads to
dementia. Early prediction and treatment of AD are crucial for
maximizing efficacy and minimizing damage. Magnetic resonance
imaging (MRI) provides valuable insights into AD through the
visualization of brain tissue shrinkage. However, MRI analysis
encounters challenges such as complexity, subjectivity, and interrater
variability.
To address these limitations, various machine learning models,
including Decision Tree, Random Forest, Support Vector Machine,
logistic regression, and AdaBoost, have been employed
to identify the optimal model for AD prediction. Performance
evaluation measures, such as Precision, Recall, and Accuracy,
are utilized to assess the models, with the Random Forest model
emerging as the most effective classifier, delivering exceptional
performance with an accuracy of 86.84%, a recall of 80%, and
an impressive AUC of 87.22%. This model demonstrated its
robustness in accurately identifying cases of Alzheimer’s disease.
Moreover, the study introduces additional metrics, including
the Mini-Mental State Examination (MMSE) and education level,
to enhance the model’s ability to differentiate between normal
healthy adults and individuals with Alzheimer’s. MMSE, a gold
standard for dementia determination, proves to be an indispensable
feature to include. Through the proficient utilization
of advanced machine learning techniques, this research aims to
enhance diagnostic accuracy and make substantial contributions
to the understanding and management of AD.


Dataset:

OASIS longitudinal dataset (first visit only, ~150 patients).

Features: demographics (Age, Gender, Education, SES), cognitive scores (MMSE), and MRI-derived measures (eTIV, nWBV, ASF).

Target: Demented (1) vs Nondemented (0).

Preprocessing & EDA:

Encoded categorical variables, handled missing SES values with conditional median imputation by education level.

Explored feature distributions using KDE plots: MMSE and nWBV showed clear separation between classes → strong predictors.

Examined SES vs Education with scatter plots + regression line → justified imputation strategy.

Modeling:

Applied Logistic Regression (probabilistic model) with cross-validation to tune regularization (C).

Compared with SVM, Decision Tree, Random Forest, and AdaBoost.

Used MinMax scaling, train/test splits, and k-fold CV for fair evaluation.

Evaluation:

Metrics: Accuracy, Recall (important for medical screening), ROC curves, and AUC.

Logistic regression coefficients & tree-based feature importance consistently highlighted MMSE and nWBV as top predictors, Age moderate, SES/Education weaker.

Takeaway:

Strong integration of probability and statistics: distribution analysis, logistic regression probabilities, ROC/AUC, recall.

Showed that cognitive (MMSE) and brain volume (nWBV) measures are statistically robust predictors of dementia.
