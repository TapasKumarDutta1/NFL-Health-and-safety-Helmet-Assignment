# General overview
After preprocessing used denoising autoencoder for feature engineering. The model was trained the simple neural network with 5 fold stratified cross validation model with focal loss, whitmann's approximation of roc and binary cross entropy with stochastic weight averaging and snapshot ensembling. The final predictions was the mean of the predictions of 3 models. 

## cleaning_preprocessing_and adding_columns
data preprocessing

## magic_feature
created the magic feature

## cleaning_preprocessing_and adding_columns_with_id
data preprocessing along with creating uid columns

## autoenc_prep_without_id 
created features using denoising autoencoder and selected 256 features without using the uid column

## autoenc_prep_with_id
created features using denoising autoencoder and selected 256 features using the uid column

## final_submission
submission of 3 different models using roc,focal and binary cross entropy loss scoring 94.5 on public leaderboard kaggle

## simple_model_with_uid_embeddings
createn neural network using uid columns features extracted from autoencoder and uid columns with binary cross entropy

## simple_model_roc_auc_with_uid_embeddings
createn neural network using uid columns features extracted from autoencoder and uid columns with Wilcoxon-Mann-Whitney U statistic.

## simple_model_focal_loss_with_uid_embeddings
createn neural network using uid columns features extracted from autoencoder and uid columns with focal loss





model | type of validationy | auc
--- | --- | ---
*Still* | `renders` | **nicely**
1 | 2 | 3
