AUTOENC:created features using denoising autoencoder and selected top 100 features by training 50000 samples increasing iteratively and predicting next 50000 samples
ENSEMBLE:ensembled lgbm and neural net model
FINDING_MAGIC_FEATURE:for a particular customer D4 is the cumulative sum of D3 so iteratively grouped by different columns and difference between D3 and D4(after rolling by 1 and subtracting )
RAW:Dropped V columns since they were causing overfitting filled numerical columns with their mean and categorical columns with nan, created unique id using columns found calculated mean and std of numerical columns after grouping by unique id added dummies for top 5 most common categories in categorical columns,since C and D columns are time varient normalized and standerized on basis of week,day,month
FOCAL_LOSS: used bayesian optimization to find optimal values for focal loss

