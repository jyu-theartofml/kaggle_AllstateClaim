# kaggle_AllstateClaim
Kaggle competition to predict claim amount.
<p> This python code demonstrats the use of XGBRegressor to predict claim amount using data from Allstate. No domain knowledge is availale because the data provided was encoded to protect confidentiality. </p>
<p>The claim amount (target variable) in the raw data has a skewed distribution. To fix this, a log transformation was used with a shift value of 200 (this is like a hyperparameter and can be tweaked). The categorical data was cleaned up by removing noisy values that only appear in training set OR test set. After the training and test data set was concatenated, the correlation eigenvalues were checked for multicollinearity, and one numerical column was dropped. Gridsearch CV along with XGBRegressor was used by doing a 5-fold cross validation during the parameter grid search. After 6 gridsearch the optimal MAE value was obtained, and the model was used to make prediction on the test set. The feature importance was examined, and it turnes out that all of the important features are the categorical variables. The lack of domain knowledge makes it challenging to perform further feature engineering on these categorical features.</p>

<br>Example plot</br>
<p align='center'><img src="Dashboard 3.png", width="1200" /> </p>
