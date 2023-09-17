# Sepsis prediction

ML pipeline (python):
1. Dataset organization. Aging, sex as well as common for all cohort genes will be considered for data analysis.
2. Train/test splitting in relation 80%/20% with shuffling and stratification by outcome.
3. As preprocessing the [robust scale procedure](https://scikit-learn.org/stable/modules/generated/sklearn.preprocessing.RobustScaler.html) to reduce the effects of potential outliers. It will be applied after the train/test splitting to avoid data leakage.
4. To optimise the computational process  the number of potential parameters will reduced after correlational analysis (Spearman test), the threshhold for genes elimination being 0.8.
5. [Removing features with low variance](https://scikit-learn.org/stable/modules/feature_selection.html#removing-features-with-low-variance) will be considered for feature selection.
6. For outcome prediction we plan to apply Logistic regression, Random Forest, Support Vector Machine, LightGBM, XGBoost form [sklearn](https://scikit-learn.org/stable/supervised_learning.html#supervised-learning) library. For each model two options will be considered. First, the model with hyperparameters by default and the model after hyperparameters optimization in greedsearch procedure (cv = 5, the metric for optimization being recall or accuracy).
7. The better model from each pair will be a part of [Staking alghorithm](https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.StackingClassifier.html) in default hyperparameters and optimized hyperparameters variants.
8. Models performans will be estimated considering accuracy, ballanced accuracy, f1-score, recall, precision, recall, ROC-curve and PR-curve.
9. The best model from 12 proposed models will be considered for feature important analysis throught permutation, drop column and shap techniques to find the top 20 features.
  



