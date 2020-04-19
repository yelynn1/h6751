## H6751 In-class Kaggle Competition Summary

Our in-class kaggle competition: stackoverflow answer ratings classification is over. Thank all students very much for their efforts! What is important, we were happy to see some students that were new to the Kaggle platform finished their first data science match. In this binary text classification competition, similar to other data science competitions, XGBoost, LightGBM, Deep Learning, CatBoost and other state-of-arts NLP tools have been explored among the works. However, powerful models alone are not enough, a strong understanding and intuition of the classification task and evaluation metric can be crucial for success. To win the competition, there are three key factors:

1. Careful Pre-processing and Feature Engineering

2. Proper Validation Framework and Regularization to Prevent Overfit

3. Effective Ensemble of **Uncorrelated** Models

In the following, I would like to share my own insights on the first factor: how to conduct pre-processing and feature engineering. After checking the data, it can be easily seen that some answers contain not only plain text, but also **code**. And code in the answer should be discriminative information for our targets (we usually vote for answers with correct code). It should be one important characteristic of the data. Based on the above observation, it may not be appropriate to remove punctuations or even stop-words even they are common text pre-processing steps. In addition, using a range of ngrams in sklearn tfvectorizer may be the optimal approach because it would result in both words and characters that enable the downstream machine learning model to learn both code and words. You may check the [solution](topsubmission/NgramChar_LRModel.html) based on the above idea (Yup, talk is cheap). This solution is not among the top submissions. But the reported testing accuracy is around 72.5% (public+private) under a very basic model, i.e., logistic regression model. Therefore it should be considered as a decent solution. Fully understanding data and task will allow you to most accurately encode the hidden information behind the data and finally create the best machine learning model. And what is more, we have several outstanding submissions from your peers. Here, the winning submission （ranked first place in private leaderboard) have been selected. Congratulations to Thant Htoo Zin! And pls take a look at his submission. 

**Name** |	**Submissions** 
:----:  | ------- 
Thant Htoo Zin | [Notebook](topsubmission/notebook.zip);  [Report](topsubmission/G1801166F.pdf)

