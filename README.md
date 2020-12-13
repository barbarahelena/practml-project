# Predicting movement quality - practical ML course project
In this project for the practical ML course (Coursera), the goal was to use data from accelerometers on the belt, forearm, arm, and dumbell of 6 participants. They were asked to perform an unilateral dumbbell biceps curl lifts correctly and incorrectly in 5 different ways with 10 repetitions: A) according to specification, B) throwing elbows to front, C) lifting only halfway, D) lowering only halfway, E) throwing the hips to the front. Read more on this page: http:/groupware.les.inf.puc-rio.br/har#ixzz4TjprBEIK.

In these analyses, I first removed all variables that were not of interest (date, timestamp), and the ones with missing variables. I assessed the predictor variables using dimension reduction with a PCA for every participant separately, since the difference between participants was larger than the difference between classes.

I divided the training dataset in a train and test set (75 vs 25%), and I trained a gradient boosted model on the train partition to predict the class of the movement (variable: classe). I also plotted the most important features for this model. I assessed the model's performance on the test partition. Finally, I predicted the movement classes within the actual test data set. The data for this project come from this source: http://web.archive.org/web/20161224072740/http:/groupware.les.inf.puc-rio.br/har.

The model had an accuracy of 96.5% (CI 96.0-97.1%), with variables "roll belt", "pitch forearm", and "yaw belt", as top 3 predictors. The complete analysis and results are presented in the markdown document in this repository.