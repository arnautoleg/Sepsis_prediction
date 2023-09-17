# Sepsis_prediction

ML pipeline:
1. Dataset organization. The ony common for all cohort genes as well as sex and aging will be considered for data analysis.
2. RobustScale procedure to reduce the effects of potential outliers.
3. Train/test splitting in relation 80%/20% with shuffling and stratification by outcome.
4. Feature selection (to reduce the number of potential parameters) based on the correlation between genes (multicollinearity), considering Spearman test with threshhold 0.8. 
5. For outcome prediction we plan to apply Logistic regression, Random Forest, Support Vector Machine, ..., ... [sklearn](https://scikit-learn.org/stable/supervised_learning.html#supervised-learning) in condition of hyperparameters by default and using the greedsearch procedure (cv = 5, the metric for optimization being recall or accuracy). The better model from each pair (default and optimized models) will be considered for Staking alghorithm (), 
7.
8. Staking 


This site was built using [GitHub Pages](https://pages.github.com/).
