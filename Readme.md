## Dataverse

We present to you a series of hackathons where you will get to work on real-life data science problems, improve your skill set and hack your way to the top of the hackathon leaderboard and win exciting prizes. 

Start your data science hackathon journey today!


## About Hackathon:

**Insurance Claim Prediction**

An insurance policy is an agreement between a company and a customer by which a company undertakes to provide a guarantee of compensation for specified loss, damage or illness in return for the payment of a specified premium. A premium is a sum of money that the customer needs to pay regularly to an insurance company for this guarantee.

For example, you pay a premium of Rs. 3000/- each year for car insurance with a coverage of Rs. 100,000/-. Unfortunately, in case of an accident, the car is severely damaged. In that case, the insurance provider company will bear the cost of damage etc. for up to Rs. 100,000. 

Now if you are wondering how can a company bear such a high cost when it charges a premium of only Rs. 3000/- per year only i.e. where the concept of probability comes into the picture. For example, there might be thousands of customers who would be paying a premium of Rs. 3000 every year just like you, but only a few of them (say 2-3) would have had an accident that year and not everyone. This way everyone shares the risk of everyone else.

Our client is an Insurance company that provides insurance for cars to its customers. In this hackathon, you will be closely working with the insurer in understanding the behaviour of the policyholders.

**RESULTS**

[Link to Competition](https://datahack.analyticsvidhya.com/contest/dataverse/)

Public Rank : 29 <br>
Private Rank : 10

**Steps:**

* EDA: I used the Sweetviz to visualize and for EDA of the data. I found that major of the variables are highly correlated to each other. And ‘MODEL’  alone        actually gives information about the car that other variables give together. 
* Feature Engineering: I created only two new features:
       1. Ratio1: age_of_car/policy_tenure
       2. Ratio2: age_of_policy_holder/policy_tenure
* Feature selection: I used the SHAP values for feature selection.
* Final Feature set:

| Feature 	| Type 	|
|---	|---	|
| age_of_car 	| float64 	|
| age_of_policyholder 	| float64 	|
| area_cluster 	| object 	|
| model 	| object 	|
| fuel_type  	| object 	|
| height 	| float64 	|
| ratio1 	| float64 	|
| ratio2 	| float64 	|

* Models:
I used LightGBM classifiers in a CV setting with 20 folds and the final probability is average of all 20.
Initially I used Catboost models, but my final models are lgbm in a cv setting.
Since the optimal F1 at this setting was correlated with the public score, so I stick to this.
