# General overview
After preprocessing used denoising autoencoder for feature engineering. The model was trained the simple neural network with 5 fold stratified cross validation model with focal loss, Wilcoxon Mann Whitney U statistic  and binary cross entropy with stochastic weight averaging and snapshot ensembling. The final predictions was the mean of the predictions of 3 models. 

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




## Results

loss  | auc(public)|auc(private)
--- | --- | ---
roc approximation | 0.944 | 0.909
focal loss | 0.948 | 0.916
binary crossentropy | 0.934 | 0.902
roc approximation with swa , weight ensemble and snapsort| 0.951 | 0.916
focal loss with swa , weight ensemble and snapsort| 94.9 | 91.7
binary crossentropy with swa , weight ensemble and snapsort| 0.95 | 0.92


## Ensemble Results

 auc(public)|auc(private)
 --- | ---
 0.952 | 0.921
 
 
 ### Correrelaion among predictions of best models.
![alt text](heatmap.png)

## References
- https://www.kaggle.com/c/ieee-fraud-detection/discussion/111476
- https://github.com/tflearn/tflearn/issues/1028
- https://www.kaggle.com/sergeifironov/bowl-stabilize-coefs-cntrs-all5
