

# IEEE-CIS-Fraud
Autoeencoder : Used Denoising Autoencoder to find hidden features.Used 10% noise in each column in each batch.Projected the 
feature sapce into 100 columns.


ensemble : used cross validation to find perfect weights then used weighted average to calculate final predictions.


finding_magic_feature : For a given user id V4 is the cumulative sum of V3 thus grouped by different columns and cumsum of V3 
then used this to compared this to V4 to calculate a loss for these columns.


focal_loss : Used previously selected parameters form bayesian optimization to optimize focal loss and used it them for predictions.
Also used deep factorization machine for higher order interactions between categorical features.


raw_preparation : filled numerical columns with mean and categorical columns with 'nan'. Dropped V columns since they are causing overfit.
Calculated mean and standard deviation of numerical columns afetr grouping by id column. Also created dummies of categorical columns for 
top 5 most frequuent levels. Normalized and standerized numerical columns w.r.t transaction days(daily,weekly,monthly).


time_vald : fitted lgbm model on earliest 50,000 columns and predicted on next 50,000 columns the number of rows in fitted increased
by 40,000 upto 590,000 for each increase calculated roc_auc score for fitted rows and test rows.Selected columns which were best for 
validation rows.
