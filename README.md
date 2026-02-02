# Maroon 5 comment section

## Dataset Overview
Our dataset on our project contains 499 rows and 21 columns, which is more than the 200 rows needed for the project. The data comes from a YouTube video and shows how people interact with each other online.

The dataset includes three types of information: numbers, categories, and true/false
values. This will allows us to understands the data in different ways and create chart to know the patterns.

**Number columns** include like count, reply count, and how many characters are in each comment. These numbers shows us how much people engage with the comments. For example, more likes or replies means to people who are more interested in what was posted.

**Category columns** include the ID number, author name, and parent ID. These help us identify each row and show which replies connect to which original posts.

**True/False columns** tells us whether something is a reply or an original post. This helps us separate regular posts from conversations between users.

We chose this dataset because it's good for analysing how people interact online. Having many rows (499) gives us reliable results, and having several number columns means we can do calculations and create charts. The data helps us spot trends in what gets the most likes and responses.

The dataset works well for our project because we can use it for descriptive statistics, create visual charts, and apply basic machine learning. All the data is public and does not contain personal information, making it ethical to use.

## Data Cleaning Summary
Fixing problems in the data beforehand improves our analysis. First, we reviewed the dataset to check for missing information, incorrect formats, and duplicate entries. 

**Missing Information:** Some cells were empty, especially in the parent ID and unnamed columns. Parent ID are blank because most posts are original, not replies. The unnamed columns were almost entirely empty, so we removed them. 

**Correct Formats:** We verified the numbers (likes, replies, character length) were formatted properly for calculations and charts. 

**Unusual Values:** We found some extremely high numbers, like posts with many likes or very long text. These represent real user behavior, not errors, so we kept them to maintain accuracy. 

This process ensures our statistics and visualisations are based on quality information. 



# Chose machine learning model (regression). Our ML model will predict the number of likes a Youtube Comment Gets.

# machine learning report: Introduction 
This report investigates if it is possible to predict the number of likes a Youtube comment gets using a simple Machine Learning (ML)  model. The likes represent a form of user engagement. Understanding what influences them can provide an insight into user behavior. As the target variable is likes, this makes it numeric. So we chose a linear regression machine learning model.

Data preparation
The data collected was a subset of Youtube Comments, timestamps, reply information and engagement metrics. Several preprocessing steps were taken before the model was made. 
-	The removal of rows that were unnecessary and not in use of our project. 
-	Converted is_reply to a numeric value ( 0 or 1)
-	Username length and reply information were used as information for features.
-	Training and testing was split into 80/20. 80% being training and 20% being testing.

Featured used: 
-	Username length 
-	Is reply (0 or 1)
-	The number of replies 
-	The category of like labels ( 0 likes, 1-5 likes, 6+ likes)
These features were selected as they are simple to work with. They are also Available in the data set and are related to engagement activity.
Model training 

A linear Regression model was trained to predict like_count. The model attempted to learn a relationship of
likes=𝛽0+𝛽1(username length)+𝛽2(is reply)+𝛽3(reply count)+𝜖
The model was trained on a sample subset and then evaluated on the test subset.
We expected the model too predict a low like count for most comments. We believed the model would penalize replies and reward comments with more replies. We also expected the model too favor shorter usernames and fail too accurately predict high engagement comments.
Model evaluation 
The models performance Would be assessed as follows:
-	R2 score- this will measure how much variation in likes there is 
-	RMSE- this is an average prediction error in terms of likes 
-	MAE- an average absolute difference between predicted and actual likes 
Observations:
-	The majority of comments have 0 likes and make predicting hard.
-	Very few comments have high like counts (20-70) these act as outliers
-	The model performed well on typical comments but struggled with popular and viral ones.

Results and evaluation 

The model showed some meaningful patterns:
-	Reply comments receive less likes than top level comments 
-	Comments with lots of replies had more likes
-	Short usernames showed a slight increase in predicted lines 
-	Most of the predictions fell between 0 and 2 likes. This matches the data sets skew.
-	The high engaging comments are under predicted. This was expected.
These results match close too our original hypothesis.
Conclusion 
This machine learning task demonstrated that simple data can provide useful insights YouTube engagement. The linear regression model could not perfectly predict the number of likes. Especially for viral comments. However, it did successfully identify consistent patterns such as low engagement is normal and reply comments receive fewer likes. Overall, the model helped show that even basic features can aid in explaining engagement on YouTube comments. 

 
