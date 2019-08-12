# Udacity-Data-Analyst-Project-05---Wrangle-And_Analyse-Data

# Introduction

When it comes to dealing with real-world data rarely comes clean. Using Python and its libraries, we gather data from a variety of sources and in a variety of formats, assess its quality and tidiness, then clean it. This is called data wrangling.

The dataset that I'll be wrangling (and analyzing and visualizing) is the tweet archive of Twitter user @dog_rates, also known as WeRateDogs. WeRateDogs is a Twitter account that rates people's dogs with a humorous comment about the dog. These ratings almost always have a denominator of 10. WeRateDogs has over 4 million followers and has received international media coverage.

WeRateDogs downloaded their Twitter archive and sent it to Udacity via email exclusively for me to use in this project. This archive contains basic tweet data (tweet ID, timestamp, text, etc.) for all 5000+ of their tweets as they stood on August 1, 2017.

![alt text]()

#### Python libraries used : 
		1.pandas
		2.NumPy
		3.requests
		4.tweepy
		5.json

#### Data set :
		1.twitter_archive_enhanced.csv
		2.image_predictions.tsv
		3.tweet_json.txt ( created using Twitter API)


# Aim

To wrangle WeRateDogs Twitter data to create interesting and trustworthy analyses and visualizations. The Twitter archive is great, but it only contains very basic tweet information. In addition gathering, then assessing and cleaning is done for generating crutial analyses and visualizations.

# Progress Outline

## Gathering data

The WeRateDogs Twitter archive twitter_archive_enhanced.csv.

Udacity Team : [[The WeRateDogs Twitter archive contains basic tweet data for all 5000+ of their tweets, but not everything. One column the archive does contain though: each tweet's text, which I used to extract rating, dog name, and dog "stage" (i.e. doggo, floofer, pupper, and puppo) to make this Twitter archive "enhanced." Of the 5000+ tweets, I have filtered for tweets with ratings only (there are 2356).]]

The tweet image predictions, i.e., what breed of dog (or other object, animal, etc.) is present in each tweet according to a neural network. This file (image_predictions.tsv) is hosted on Udacity's servers and has been downloaded programmatically using the Requests library.

Each tweet's retweet count and favorite (i.e. "like") count at minimum, and any additional data we find interesting. Using the tweet IDs in the WeRateDogs Twitter archive, query the Twitter API for each tweet's JSON data using Python's Tweepy library and store each tweet's entire set of JSON data in a file called tweet_json.txt file. Each tweet's JSON data has been written to its own line. Then we read this .txt file line by line into a pandas DataFrame with tweet ID, retweet count, and favorite count.
	
## Assessing Data

After gathering each of the above pieces of data, assess them visually and programmatically for quality and tidiness issues. We detect and document eight quality issues and two tidiness issues in wrangle_act.ipynb Jupyter Notebook. 


#### Key Points

To meet specifications, the issues that satisfy the below mentioned Key Points must be assessed.

- We want original ratings (no retweets) that have images. Though there are 5000+ tweets in the dataset, not all are dog ratings and some are retweets.
- Fully assessing and cleaning the entire dataset requires exceptional effort so only a subset of its issues (eight (8) quality issues and two (2) tidiness issues at minimum) need to be assessed and cleaned.
- Cleaning includes merging individual pieces of data according to the rules of tidy data.
- The fact that the rating numerators are greater than the denominators does not need to be cleaned. This unique rating system is a big part of the popularity of WeRateDogs.
- We do not want to gather the tweets beyond August 1st, 2017. You can, but note that you won't be able to gather the image predictions for these tweets since you don't have access to the algorithm used.




## Cleaning Data

- The define, code, and test steps of the cleaning process are clearly documented.
- All issues identified in the assess phase are successfully cleaned.
- A tidy master dataset with all pieces of gathered data is created.


## Storing, Analyzing, and Visualizing Data

Stored the clean DataFrame(s) in a CSV file with the main one named twitter_archive_master.csv.

Analyze and visualize the wrangled data in wrangle_act.ipynb Jupyter Notebook. Three insights and one visualization has be produced.


# Conclusion

Report wrangle_report.pdf has been created that briefly describes the wrangling steps.
Report act_report.pdf communicates the insights and displays the visualizations produced from the wrangled data.


