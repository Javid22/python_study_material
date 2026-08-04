Linear Regression

regression 	
1. Mean Absolute Error (MAE)
	MAE is the average of the absolute errors. It tells us how far the predictions are from the actual values on average. A lower MAE indicates better predictions.

2. Mean Squared Error (MSE)
	MSE is the average of the squared errors. Squaring gives much more weight to larger mistakes.

3. Root Mean Squared Error (RMSE)
	RMSE is the square root of MSE. It measures the average prediction error in the same units as the target variable.
4. R-squared (Coefficient of Determination, R2)
	R² tells us how much of the variation in the target variable is explained by the model.
5. Adjusted R-squared
	Normal R² almost always increases when you add more features, even if those features aren't useful.
	
	Adjusted R² checks whether the new features actually improve the model enough to justify their inclusion.



Logistic Regression

Step 1: Confusion Matrix
1. Accuracy - Out of all predictions, how many were correct?
2. Precision - Whenever my model says "YES", how often is it correct?
3. Recall (Sensitivity) - Out of all actual Positive cases, how many did my model find?
4. F1 Score - One score that balances Precision and Recall.
5. Specificity - Out of all Negative cases, how many did my model correctly identify?
6. ROC-AUC Score - This is a measure of how well the model separates the two classes (Positive and Negative) across different decision thresholds.

Step 1: Confusion Matrix
00 - true negative 01 - true positive 10- false negative 11- false positive
00 - 50,  01-150, 10- 25, 11- 75

accurance is mean by how true negative and true positive predict correctly (TP+TN)/Total
Out of 300 patients, the model correctly predicted 200 patients.

precion - When the model predicts Disease, how often is it correct? TP/(TP+FP)
recall - Did I find all the patients who actually have the disease?TP/(TP+FN)


Decision Tree

The feature that creates the **purest groups** becomes the root node.

There are three common methods used to build decision trees:

Gini Impurity (used by CART - most common in Scikit-learn)
Entropy & Information Gain (used by ID3)
Gain Ratio (used by C4.5)

* **Gini Impurity** → choose the split that creates the purest groups (most common in practice).
* **Entropy & Information Gain** → choose the split that reduces uncertainty the most.
* **Gain Ratio** → similar to Information Gain, but avoids favoring features with many unique values.

It uses one splitting criterion, depending on the algorithm.

Algorithm	Split Criterion
CART (used in Scikit-learn)	Gini Impurity
ID3	Entropy + Information Gain
C4.5	Entropy + Gain Ratio

So if you're using Scikit-learn's DecisionTreeClassifier, it uses Gini by default (or you can choose criterion="entropy").

# Disadvantages

❌ Can overfit if allowed to grow too deep

❌ Small changes in the training data can produce a different tree

❌ A single decision tree may not be as accurate as ensemble methods like **Random Forest** or **XGBoost**


