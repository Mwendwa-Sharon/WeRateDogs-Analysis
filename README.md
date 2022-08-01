# WeRateDogs-Analysis
This project involved analyzing tweet data of a Twitter user called WeRateDogs who rates people's dogs with funny comments.

# Dataset: The datasets are in the repo.

Requests library was used to download the image predictions dataset using the following URL(https://d17h27t6h515a5.cloudfront.net/topher/2017/August/599fd2ad_image-predictions/image-predictions.tsv)
Tweet-json was used to get additional data. Use Twitter API to get this data instead.

#Assessing the Data
The dataframes were first assessed visually using Microsoft Excel where a few a few issues such as non-descriptive column headers were spotted.
Programmatic assessment then followed and the following quality and tidiness issues were spotted:

Quality issues
•	incorrect datatypes (in the tweet_id, timestamp columns.)
•	Inconsistent data. (there are rows with retweets and replies information yet we want only the original tweets.)
•	Non-descriptive column header in the timestamp column. It should be changed to a more descriptive header like tweet_Date.
•	Extract the actual source from the source column.
•	Some rating_denominators are not equal to 10
•	Non-descriptive column headers in p1, p1_conf, p1_dog, p2, p2_conf, p2_dog, p3, p3_conf, and p3_dog
•	incorrect datatype in tweet_id
•	The img_num and p1, p2, p3 column should be in categorical variables
•	id should be tweet_id to make it uniform.
•	tweet_id should have string datatype

Tidiness issues
•	Many missing values.
•	One variable has been split into 4 columns (doggo, floofer, puppo, pupper). These columns should be merged to a single column named dog_stage
•	3 datasets have information of the same thing(dogs). The 3 datasets should be merged.
•	Derive ratings column based on the rating_numerator and drating_denominator

Data cleaning followed and the clean data was saved in a CSV file.

Upon analysis the following insights were drawn:
1. The relationship between Retweet_count and Favorite_count is strong. This shows that if a user likes a post on twitter; they will most probably repost it.
2. Pupper was the most tweeted dog_stage
3. Prediction 1 had a better prediction_confidence.
4. Most people use tweeter for iphone
5. Pupper is the most liked and retweeted dog_stage.
6 Ratings affects neither the likes nor the retweets that a dog gets.

# Additional features
Any additional features are welcome.
