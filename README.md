# Machine Learning
Summary
This multiclass classification project for predicting football match outcomes employed a variety of approaches and models. Below is a detailed summary of the steps, methods, and reasoning behind each decision:

Models Used
XGBoost

Model: XGBClassifier

Why it was used: Efficient for multiclass classification, provides overfitting control, and is optimized for large-scale datasets.

CatBoost

Model: CatBoostClassifier

Why it was used: Handles categorical variables natively without requiring manual encoding such as one-hot encoding. Also performs well on imbalanced datasets.

Random Forest

Model: RandomForestClassifier

Why it was used: Robust against overfitting due to the use of multiple decision trees and can capture complex interactions between variables.

Logistic Regression

Model: LogisticRegression

Why it was used: A simple linear model used as a baseline to compare with more complex models.

Support Vector Machine (SVM)

Model: LinearSVC

Why it was used: Efficient classifier for linearly separable problems, with built-in regularization to avoid overfitting.

Decision Tree

Model: DecisionTreeClassifier

Why it was used: An interpretable model that creates data splits based on features, used as a baseline for comparison with more sophisticated models.

Neural Network (MLP - Multilayer Perceptron)

Model: Sequential (Keras)

Why it was used: Designed to capture complex patterns in data through multiple dense layers. Dropout and L1/L2 regularization were applied to prevent overfitting.

Evaluation Techniques Used
ROC Curve (Receiver Operating Characteristic)

Why it was used: The ROC curve evaluates classifier performance in terms of sensitivity (true positive rate) vs. specificity (false positive rate).

Method applied: ROC curves were used to visualize multiclass classification performance, with AUC (Area Under the Curve) calculated for each class.

Confusion Matrix

Why it was used: Provides a detailed view of how the model correctly or incorrectly classifies each class. Displays true positives, false positives, true negatives, and false negatives.

Method applied: The confusion_matrix function was used to compute the matrix, and ConfusionMatrixDisplay was applied for visualization, helping to better understand model performance per class.

Auxiliary Techniques
Cross-Validation (K-Fold)

Why it was used: K-Fold cross-validation ensures the model is evaluated across different data splits, offering a better sense of its generalization ability.

Method applied: KFold was used to split the dataset into multiple folds and compute average accuracy, aiding in identifying overfitting or underfitting.

Manual Hyperparameter Search

Why it was used: Hyperparameter tuning is essential to improve model performance, adjusting values such as neuron counts, dropout rates, and learning rates.

Method applied: A manual search was conducted to test several parameter combinations, aiming to maximize the model’s accuracy.

Conclusion
This project combined machine learning techniques, neural networks, and robust evaluation strategies. Models like XGBoost, CatBoost, and Neural Networks were assessed using ROC Curves and Confusion Matrices, while Decision Trees and Random Forests provided interpretable baselines. Cross-validation and hyperparameter tuning ensured that models were well-fitted and properly validated, resulting in a complete approach to football match outcome prediction.

