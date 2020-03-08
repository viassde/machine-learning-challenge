# machine-learning-challenge

### Summary of work and findings (by Daniel Viassolo)

* The original problem was converted into a 2-class classification problem by mapping: CANDIDATE or CONFIRMED =TruePositives; FALSE POSITIVE =FalsePositive

* Two different classifiers were applied: 
(1) Random Forest - see notebook `RF_model.ipynb` 
(2) Logistic Regression - see notebook `LogReg_gmodel.ipynb` 


* The 6 most relevant features were identified - using `.feature_importances_` for RF and `.coef_` for LogReg    
1- Top 6 for RF: `koi_fpflag_co, koi_fpflag_nt, koi_fpflag_ss, koi_prad, koi_fpflag_ec, koi_prad_err1`
2- Top 6 for LogReg: `koi_fpflag_nt, koi_fpflag_ss, koi_fpflag_co, koi_impact, koi_duration_err1, koi_depth`


* Both models were tuned using `GridSearchCV` in scikit-learn

* Testing accuracy for LogReg: 0.9776728209531989

* Testing accuracy for RF: 0.9875483039931301


 