
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
