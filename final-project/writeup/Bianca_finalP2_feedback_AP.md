I'm just a bit confused on what you are hoping to model here, and wanted to make sure it was a clear goal you had.
Are you simply trying to figure out which of the 6 features you've choosen are important to men and women in the dating world? Or, are you hoping to use those attributes to predict whether a person is likely to be asked on a second date by their partner?

If you are focusing on the 'importance' of features, you can try to use the coefficients assigned to each feature in a logistic regression, or running a tree based model (decision tree, random forest) you can list feature importance through SKLearn.

While observing the top predictive features would be intersting, I think it might be perhaps a bit more interesting for a person to be able to assess what their probability of success might be for securing a second date, before even entering the speed dating event. Just something to consider.