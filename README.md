# predicting the sale price of bulldozers using machine learning

in this notebook, we're going to go through an example machine learning project with the goal of predicting the sale price of bulldozers

 # 1. problem definition
> how well can we predict the future sale price of a bulldozer, given its characteristics and previous examples of how much similar bulldozers have been sold for?
# 2. data
> https://www.kaggle.com/c/bluebook-for-bulldozers/data
> For this competition, you are predicting the sale price of bulldozers sold at auctions.

> The data for this competition is split into three parts:

1. Train.csv is the training set, which contains data through the end of 2011.
2. Valid.csv is the validation set, which contains data from January 1, 2012 - April 30, 2012 You make predictions on this set throughout the majority of the competition. Your score on this set is used to create the public leaderboard.
3. Test.csv is the test set, which won't be released until the last week of the competition. It contains data from May 1, 2012 - November 2012. Your score on the test set determines your final rank for the competition.
> The key fields are in train.csv are:

1. SalesID: the uniue identifier of the sale
2. MachineID: the unique identifier of a machine.  A machine can be sold multiple times
3. saleprice: what the machine sold for at auction (only provided in train.csv)
4. saledate: the date of the sale
> There are several fields towards the end of the file on the different options a machine can have.  The descriptions all start with "machine configuration" in the data dictionary.  Some product types do not have a particular option, so all the records for that option variable will be null for that product type.  Also, some sources do not provide good option and/or hours data.
The machine_appendix.csv file contains the correct year manufactured for a given machine along with the make, model, and product class details. There is one machine id for every machine in all the competition datasets (training, evaluation, etc.).
# 3. evaluation
> The evaluation metric for this competition is the RMSLE (root mean squared log error) between the actual and predicted auction prices.

**Note:** the goal for most regression evaluation metrics is to minimize the error. For example, our goal for this project will be to build a ML model which minimises RMSLE.
# 4. features
We provide a data dictionary detailing all the features of the dataset
