# Recommender System: Collaborative filtering
 
# Project Objective
The objective of the project is to build a recommendation system that recommends items to users. The project is run in the style of a data science contest, where there is an open leaderboard for students. To achieve high positions on the leaderboard, participants are required to select appropriate models and tune the necessary hyper-parameters for the best performance. 

# Datasets
The data provided includes 2 subsets of data: Training data and Probing data. 
Each subset contains three data fields: User ID, Item ID and Rating of users to items. 
•	In the training dataset, there are 147.244 ratings from 46.612 users for 21.820 items. 
•	In the probing dataset, there are 79.118 ratings from 46.061 users for 18.230 items.

#	Methodology

1. Raw Data
Data processing and cleaning was not necessary as the data sets are provided in the UIR format that is compatibe to Cornac models. The data types of all fields are in correct formats.

2.	Data Preparation and Exploration
Data preparation and analysis were performed to detect null values, duplicates and other data abnormalities. No data abnormalities were detected. 

3.	Model Selection 
The 4 following models were explored during experiments:
   -	Matrix Factorization (MF)
   -	Non-negative Matrix Factorization (NMF)
   -	Weighted Matrix Factorization (WMF)
   -	Bayesian Personalized Ranking (BPR)

All models were built by using Cornac library. The evaluation methods used include Ratio Split and Base method. When Ratio Split is used, only Training dataset is provided for training and testing, with the ratio of 80:20, respectively. When Base method is used, the Training dataset is utilized to train models and the Probing dataset is used for model testing.

# Parameter Tuning
Depending on the model in usage, the hyper parameters that were optimized include the followings:

•	Number of factors (k)
•	Maximum Iteration (max_iter)
•	Learning Rate (learning_rate)
•	Lambda Regression (lambda_reg)
•	User Bias (user_bias): only applied to MF
•	Lambda U (lambda_u): only applied to WMF
•	Lambda V (lambda_v): only applied to WMF

# Model Evaluation
F1@50, Training Time, AUC, NDCG@50, Precision@50 and Recall@50 

# Credits

Cornac: A comparative framework for multimodal recommender systems (https://cornac.preferred.ai/)


