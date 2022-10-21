# We rate dogs wrangling project 
## Dataset Introduction
This project involves gathering data from variety of sources and variety of formats
## Wrangling
The first file twitter_archived_enhanced has been provided for as csv. I downloaded the file and loaded it to jupyter notebook workspace, this only required the pandas library to be imported. The twitter_archived_enhanced has 2356 rows and 17 columns. I went ahead and cleaned the dataset and merged with the rest of the datasets.
 
The second file is the tweet_image_predictions. The file is hosted on udacity's servers. i downloaded the file programatically from the udacity servers using the request library, this involved installing the request library using conda in the terminal then importing the request library in the jupyter notebook workspace. The url for the file was provided. I created  a file called image_predictions.tsv and wrote the contents of the requests to it. I read the image_predictions.tsv file to the jupyter notebook workspace using pandas_read_csv and using the sep as \t. I continued to clean the dataset and merged it to the rest other two datasets.

the third file is data from twitter API.First i installed tweepy and json in the annaconda prompt since both libraries are required for this dataset. This data from twitter required authorization before use and so i had to setup a twitter developer account with level as elevated. The steps for developer account setup are quite strightforward. Once you fill a questionaire and create an account succesfully,you can the generate the  api key, api key secret, access toeken and access token secret. This keys are used for authorization and access of the twitter data. The data is stored in json format by twitter. I querryied the json data using the tweet_id earlier provided in the image_predictions file and also using the tweepy library.The columns that were required in the we_rate_dogs data was the tweet_id, retweet_count and fovourite_count. I stored the data in a file called tweet_json.txt. i wrote JSON data  to its own line, then read this .txt file line by line and appended into a list. i converted the list to dataframe with the required columns(tweet_id, retweet_count and fovourite_count). The wrangling part of the project was quite mind breaking and required each individual to look beyond the normal scope.
## Reporting

After wrangling of the data from various sources and cleaning the data, i was tasked with deducing insights and creating visualizations from the data.To deduce my insights, i grouped the data by dog_stage and used the means of retweet count, favorite count and rating numerator. some of the insights i brought to light are as:
 1. dog stage floofer has the highest retweet count with a mean of 6773.666667 retweets and the dog stage with the least retweet count is pupper with a mean of 1879.576037 retweet counts.    

2. dog_stage puppo has the highest mean favorite_count and pupper as the lowest mean favorite count

3. floofer has the highest rating numerator

When deducing my insights, i specifically used the dog_stage. i grouped the data by dog_stage and used the means of favorite count, retweet count and rating numerator.
The first insight was that the dog_stage floofer received the most retweets, i also looked at the favorite count and i found out that the dog stage puppo was leading with the most favorite counts.I also deduced that the dog_stage floofer had the highest rating numerator.

I went ahead and visualized with a bar chart the dog_stage and the rating numerator and the visualization was as follows:

![image.png](attachment:image.png)

The title of the visualization is dog_stage by mean rating numerator and xlabel and ylabel was dog_stage and rating numerator respectively.
I also used a pie chart to visualize the dog_stage and the mean fovorite count. The visualization is as follows:
![image-2.png](attachment:image-2.png)



