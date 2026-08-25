EasyVisa – Visa Approval Prediction

Project Overview

This project develops a machine learning classification model to help predict visa certification outcomes based on applicant and employment characteristics.

The objective is not only to achieve strong predictive performance, but also to identify the factors that contribute most to the model’s predictions and translate the results into actionable business insights.

Business Problem

Visa application processing involves evaluating multiple applicant and employment characteristics. A predictive model can help organizations identify applications that are more likely to receive certification and support more efficient case review and resource allocation.

For this project, recall was prioritized as an important evaluation metric because the goal was to minimize missed positive certification cases.

Project Workflow

The analysis followed an end-to-end machine learning workflow:

1. Data exploration and preprocessing
2. Exploratory Data Analysis (EDA)
3. Feature engineering and encoding
4. Train, validation, and test splitting
5. Model development and comparison
6. Hyperparameter tuning using GridSearchCV and RandomizedSearchCV
7. Final model selection based on validation performance
8. Evaluation on unseen test data
9. Feature importance analysis
10. Business insights and recommendations

Models Evaluated

Several classification and ensemble models were explored during the project. The strongest candidates were further tuned and compared using:

* Gradient Boosting
* AdaBoost
* Random Forest
* GridSearchCV
* RandomizedSearchCV

Recall was used as the primary metric during model selection, while precision, F1-score, accuracy, and the difference between training and validation performance were also considered.

Final Model

The final selected model was:

AdaBoost tuned with GridSearchCV

### Test Performance

|Metric   |	Score |
|---|---:|
|Accuracy |71.41%|
|Recall	  |94.49%|
|Precision|71.43%|
|F1-score |81.36%|

The model achieved 94.49% recall on unseen test data, successfully identifying most observations belonging to the positive certification class.

The trade-off is a higher number of false positives, reflected in the model’s 71.43% precision. This is acceptable for a recall-focused screening use case where minimizing missed positive cases is particularly important.

Key Predictive Features

Feature importance from the final AdaBoost model showed that the strongest predictive information came from:

* Education level
* Previous job experience
* Applicant continent
* Annual wage
* Region of employment

Education and previous job experience were particularly influential in the final model.

Feature importance represents predictive importance rather than causality. Therefore, these results should not be interpreted as evidence that any individual characteristic directly causes a visa certification decision.

Business Recommendations

1. Use the model as an early-screening tool

With a test recall of 94.49%, the model can help identify a high proportion of potential positive certification cases and support more efficient prioritization of application reviews.

2. Maintain professional review of model predictions

Because precision is approximately 71%, some applications predicted as positive will still receive a negative outcome. Model predictions should therefore support, rather than replace, professional case review.

3. Pay close attention to important application information

Education, work experience, wage information, and employment characteristics provide useful predictive information. Organizations should ensure that these fields are complete and accurately documented during application preparation.

4. Monitor model performance over time

Visa patterns, labor-market conditions, and immigration policies can change. Model performance should therefore be monitored and the model retrained as newer application data becomes available.

Tools and Technologies

* Python
* Pandas
* NumPy
* Scikit-learn
* Matplotlib
* Seaborn
* Jupyter / Google Colab
* Ensemble Machine Learning
* GridSearchCV
* RandomizedSearchCV

Skills Demonstrated

* Exploratory Data Analysis
* Data preprocessing
* Classification modeling
* Ensemble learning
* Hyperparameter tuning
* Model comparison and selection
* Recall-focused model evaluation
* Feature importance interpretation
* Translating machine learning results into business recommendations

Notebook

The complete analysis, modeling workflow, evaluation, and recommendations are available in:

EasyVisa_Chen_final_edition.ipynb
