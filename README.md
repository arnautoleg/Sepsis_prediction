# Sepsis_prediction

ML pipeline (python):
1. Dataset organization. The ony common for all cohort genes as well as sex and aging will be considered for data analysis.
2. RobustScale procedure to reduce the effects of potential outliers.
3. Train/test splitting in relation 80%/20% with shuffling and stratification by outcome.
4. To optimise the computational process we will reduce the number of potential parameters throught multicollinearity procedure, considering Spearman test with threshhold 0.8.
5. [Removing features with low variance](https://scikit-learn.org/stable/modules/feature_selection.html#removing-features-with-low-variance) will be considered for feature selection
6. For outcome prediction we plan to apply Logistic regression, Random Forest, Support Vector Machine, LightGBM, XGBoost [sklearn](https://scikit-learn.org/stable/supervised_learning.html#supervised-learning) library. For each model two options will be considered. First, the model with hyperparameters by default and the model after hyperparameters optimization in greedsearch procedure (cv = 5, the metric for optimization being recall or accuracy).
7. The better model from each pair (default and optimized models) will be considered for [Staking alghorithm](https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.StackingClassifier.html) in default hyperparameters and optimized hyperparameters.
8. Models performans will be estimated considering accuracy, ballanced accuracy, f1-score, recall, precision, recall, ROC-curve and PR-curve.
9. The best model (totally 12 models) will be considered for feature important analysis throught permutation, drop column and shap techniques to find top 20 of features.
  



