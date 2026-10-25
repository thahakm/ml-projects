California Housing Price Prediction (Decision Tree)

A regression project that shows how a Decision Tree overfits, and how pruning improves how well it generalises.

Problem

Predict median house value in California districts from census features, and reduce overfitting in a Decision Tree.

Dataset
scikit-learn California Housing dataset
20,640 records, 8 features: MedInc, HouseAge, AveRooms, AveBedrms, Population, AveOccup, Latitude, Longitude
Target: median house value
Approach
Train/test split 80/20 (random_state=42)
Unpruned Decision Tree Regressor as a baseline
Compare train and test scores to check for overfitting
Pruned tree with max_depth=8 and min_samples_leaf=20
Visualise the first 3 levels of the pruned tree
Results
Model	Train R²	Test R²	Test MSE
Unpruned tree	1.000	0.622	0.495
Pruned tree	0.745	0.682	0.416

The unpruned tree memorised the training data (R² of 1.0 on train, 0.62 on test). Limiting depth and leaf size lowered the training score but improved the test score, which is a sign of better generalisation.

Tools

Python, scikit-learn, Pandas, Matplotlib, Google Colab

Files
california_housing_decision_tree.ipynb
What I learned
How to spot overfitting by comparing train and test scores
How max_depth and min_samples_leaf control tree complexity
How to read a decision tree plot
