# Data-Analysis-NanoDegree-project-4-5
Data wrangle and act
The wrangling process is broken down to three main parts:
Gather
Download the WeRateDogs Twitter archive file manually into the project folder and save as twitter_archive_enhanced.csv
Read this .csv file into a pandas dataframe as  𝑡𝑤𝑡𝑎𝑟𝑐ℎ
t
w
t
a
r
c
h
 
Download image_predictions.tsv programmatically using the Requests library and the provided URL on Udacity's servers
Check for encoding - make sure it is UTF-8
Read this .tsv file into a pandas dataframe as  𝑖𝑚𝑔𝑝𝑟𝑒𝑑
i
m
g
p
r
e
d
 
Using the tweet IDs in the WeRateDogs Twitter archive, query the Twitter API for each tweet's JSON data using Python's Tweepy library and store each tweet's entire set of JSON data in a file called tweet_json.txt file.
Read this .txt file line by line into a pandas DataFrame as  𝑡𝑤𝑡𝑑𝑎𝑡𝑎
t
w
t
d
a
t
a
 
Assess
Read in the dataframes and inspect multiple sample rows at random to see if there are any quality / tidiness issues
The issues found are:
There are 78 entries that are in reply to a status or a user - these should be removed together with the columns;
There are 181 entries that are retweets - these should be removed together with the columns;
The rating value columns are probably not accurate in the first place so need to be read in from text to double check;
There are a total of 14 rows that have multiple choices of Dogtionary, and these need to be corrected;
There are 324 rows where none of the predicted breed is a dog's, and so need to drop these rows;
The three breed predictions along with the conf level and whether the breed is a dog need to be combined into one most likely dog breed;
The  𝑡𝑤𝑒𝑒𝑡_𝑖𝑑
t
w
e
e
t
_
i
d
  column in archive dataframe should be object (string) type;
The  𝑡𝑖𝑚𝑒𝑠𝑡𝑎𝑚𝑝
t
i
m
e
s
t
a
m
p
  column should be of datatime type;
The four Dogtionary columns in archive dataframe can be merged into one;
The  𝑡𝑤𝑒𝑒𝑡_𝑖𝑑
t
w
e
e
t
_
i
d
  column in predictions dataframe should be Object (string) type;
There are fewer tweet IDs (2075 records) in predictions dataframe than there are (2356 records, pre-cleaning) in the archive dataframe;
For the purpose of the study all dataframes should be merged together.
Clean
Leverage various pandas methods to address the issues listed above;
Test the effectiveness of data cleaning by intermittently inspecting the dataframes.
