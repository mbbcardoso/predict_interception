# predict_interception
In this project I attempt to build a classification model to predict the occurrence of one of the most crucial plays in American Football: the interception or pick. It happens when the team attacking attempts to pass the ball and it ends up being caught by someone from the defending team. Using play-by-play data of previous plays, plus some information that can be known about the play itself prior to it taking place, the model outputs a probability of an interception happening as a result of the play. To train and test the model, a public dataset from Kaggle is used, containing play-by-play data from 10 NFL seasons.

## Language:
* Python

## Libraries:
* pandas
* numpy
* matplotlib
* seaborn
* xgboost
* imblearn
* sklearn
* datetime
* time
* boostaroota
* scipy

## Files:
* predict_interception.ipynb
	* Notebook containing the Python code used in every step of the modelling
* Predicting likelihood of interception in NFL games.pdf
	* Paper describing the project
* feat_desc.txt
	* A description of all the features present in the original dataset
* log.txt
	* File containing data logged during modelling
* CSV files in data folder
	* The dataset partioned by year and month of the game
	
The dataset was obtained at:
https://www.kaggle.com/maxhorowitz/nflplaybyplay2009to2016#NFL%20Play%20by%20Play%202009-2018%20(v5).csv

File name:
NFL Play by Play 2009-2018 (v5).csv

## Summary:
These were the steps included in building the model:
* The problem to solve was defined by browsing public datasets in Kaggle
* The relevant dataset was obtained in CSV format
* A benchmark model was found to evaluate results
* The dataset was loaded and preprocessed
* Classifiers were trained on the resulting dataset iteratively, adding steps to improve performance (rebalancing, feature selection, cross-validation)
* The best model was then evaluated, with comparison to the benchmark model using the same metrics (FDR and TPR at a chosen decision threshold)

The final metrics of the benchmark model were a FDR of 8.3% and a TPR of 38.1%. In turn, the ones regarding this project’s final model were 83.7% and 17.2%. That means that both metrics were inferior to the ones of the benchmark model, especially the FDR which was ten times worse.

## Conclusion:

This project’s model did not improve upon the benchmark model and it could have only limited practical use. A predicted probability of interception higher than 80% would mean that there is approximately a 16% chance of there being an interception, which is much higher than the base probability of close to 2%, so the model could still serve as an auxiliary, limited information source for coaches, sports bettors, or anyone else interested in anticipating interceptions.

## References:
[1] https://en.wikipedia.org/wiki/National_Football_League

[2] Jozsa, Frank P. (2004). Sports Capitalism: The Foreign Business of American Professional Leagues. Ashgate Publishing. p. 270. ISBN 978-0-7546-4185-8. Since 1922, [the NFL] has been the top professional sports league in the world with respect to American football

[3] Harris, Nick (January 31, 2010). "Elite clubs on Uefa gravy train as Super Bowl knocked off perch". The Independent. London. Retrieved November 28, 2012.

[4] https://operations.nfl.com/the-rules/2018-nfl-rulebook/

[5]
https://thepowerrank.com/2014/01/31/how-to-predict-interceptions-in-the-nfl-backed-by-surprisin
g-science/

[6] https://en.wikipedia.org/wiki/Precision_and_recall#Recall

[7]
https://stats.stackexchange.com/questions/336455/fpr-false-positive-rate-vs-fdr-false-discovery-r
ate

[8] https://github.com/dmlc/xgboost

[9] https://machinelearningmastery.com/gentle-introduction-xgboost-applied-machine-learning/

[10] https://medium.com/mlreview/gradient-boosting-from-scratch-1e317ae4587d

[11]
https://www.analyticsvidhya.com/blog/2016/03/complete-guide-parameter-tuning-xgboost-with-c
odes-python/

[12] Bock, J.: Empirical Prediction of Turnovers in NFL Football (2017)

[13]
https://github.com/udacity/machine-learning/blob/master/projects/capstone/capstone_report_te
mplate.md

[14]
https://www.analyticsvidhya.com/blog/2016/03/complete-guide-parameter-tuning-xgboost-with-c
odes-python/

[15] https://github.com/chasedehan/BoostARoota

[16] https://pypi.org/project/imblearn/

[17] https://github.com/dmlc/xgboost/issues/2621

[18] https://nextgenstats.nfl.com/
