# gender-classification-based-on-twitter-data
Gender classification on twitter data using ensemble techniques

Problem statement:
Finding the most accurate model for gender classification. 

DATASET DESCRIPTION:
The given dataset contains features like _last_judgment_at, gender, ge
nder_confidence, created, description, name, retweet_count, _last_judgment_
at, tweet_id, user_timezone etc
Total of 20050 rows and 26 columns(features). 

Libraries Used:
Sci-kit learn, Pandas, Matplotlib, Numpy, DateTime.

Feature selection:
Selected the following columns: '_last_judgment_at', 'gender',
'gender:confidence', 'created', 'fav_number', 'name','retweet_count',
'tweet_count', 'tweet_created', 'tweet_id', 'tweet_location', 'user_timezone'
As these columns are mostly related to gender.

Data Cleaning:
1. Cleaning gender column: Dropping the categorical values of gender
column having “brand” and “unknown” as labels
2. Handling Null values: Dropping all rows with null values using dropna()
function. 3. Handling columns with datetime values:
(i) changing object dtype to datatime. (ii) extracting month, day, week, etc from the date
(III) adding these values to the dataset.
4. Handling object dtype columns: used labelencoding technique to change
there dtype to int. But for name column used nlp to predict gender based on name used
naviebayesclassification model here. Then applied label encoding for
new column and droped the old column. 

Questions asked on dataset:
Question 1:
which is the 2nd most commonly used description by female?
Ans: Do whatever makes you happy
Question 2
who retweeted the less number of times? male or female. 
Ans: Female


Machine Learning model with their Accuracies:
'AdaBoostClassifier': 58%
'RandomForestClassifier': 60%
'ExtraTreesClassifier': 56%
'GradientBoostingClassifier': 59%
'Logistic RegressionClassifier': 52%
'SVMClassifier': 52%
RandomForestClassifier has given the highest accuracu (58% - 60%).
