
## Census Income (KDD) Prediction

The prediction analysis is done on Census Income data available at http://archive.ics.uci.edu/ml/datasets/Census-Income+(KDD)


### Steps taken to avoid model overfitting.

 To avoid model overfitting I used three steps
 
 1. Imbalance features removals -> Improve model generalization 
 
 2. Balancing dataset -> Resample the training set by using undersampling
 
 3. Cross Validation -> powerful preventative measure against overfitting. CV provides a mechanism to get the MSE test with the current dataset without the need of finding new data to test the model.
 

### Proposed changes to make this modeling process more effective 

To make this modeling process more effective, I suggest to use only a representative sample of data from the dataset for initial data analysis. It is important to fullfill the rule of i.i.d. selected samples from dataset (verification e.g. by using K-S method). 

In this modelling process I did not use Neural Networks models. The reason was that the data was not so diverse and the robust and high quality classifier can be created without NN as well. 

If the data (with 300mil rows) are quite diverse, using excessive data is the way to train a neural network. If there is no much variation in training dataset, then a high amount of data leads to overfitting to the training data.


## Selecting the most promising features without using any ML model (assume that dataset contains many features, and you cannot train a model on all of them). 

There are multiple methods that we can use. At the moment, the most usual process is to train (some) ML model and find out the feature importance out of it. 

However, there are other methods that we can use. 

One of them is to find out **feature correlation** with target (income).

The other method that can be used to perform feature selection without ML models is **Chi-squared test**.

#### Correlation Matrix
Correlation matrix is a table showing correlation coefficients between variables Each cell in the table shows the correlation between two variables.

The correlation coefficient is a statistical measure of the strength of the relationship between the relative movements of two variables. The values range between -1.0 and 1.0. A calculated number greater than 1.0 or less than -1.0 means that there was an error in the correlation measurement. 
- Correlation of -1.0 shows a perfect negative correlation
- Correlation of 1.0 shows a perfect positive correlation
- Correlation of 0.0 shows no linear relationship between the movement of the two variables.

### Should the raw model dataset be randomly distributed to Train/Test before or after identifying the most predictive features?

To prevent some information leakage (which would cause overfitting) I would split dataset to Train/Test first.

I think it's a good practice to **NOT** use test dataset in any stage of model building. That includes feature selection, too.

