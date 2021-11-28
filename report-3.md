# Data Understanding

## Gathering data

We don’t need to gather our own data as we are using pre-made datasets. 
### Data Requirements
We require our data to have news headlines as well as accurate dates. We also need stock market information within the range of dates that our news articles were written in (circa 2008-2017).
### Verify data availability
The data is usable. 
### Define selection criteria
We are going to use the whole reddit worldnews dataset. Stocks data is spread into separate files. We aren’t certain yet whether or not we will need all of it. We most probably won’t get use out of the author and over_18 fields of the reddit dataset. Similarly the time_created field is redundant since we have the date_created field.
On the stocks dataset we won’t exclude any fields for now.

The data was acquired from 2 seperate Kaggle datasets. Since we’re using pre-made datasets, they are already formatted for us and there were no problems in reading the data into pandas dataframes.
## Describing data
### Stock data
The stock data is firstly separated into ETFs and Stocks. For the dates(string), earliest and latest vary between stocks.. Each row of data encompasses a single day. Open(float) and Close(float) being the value of the stock when the market was opened and closed on that day. The High(float) and Close(float) signify the highest and lowest value of the stock on that day. Volume (int) is the number of stocks that were traded on the day.

### Headline data
Each row of the reddit worldnews dataset is a single headline. Time_created(int) is the unix timestamp of when the post was created. Date_created(string) is the date formatted like %Y-%m-%d. Up_votes(int) and down_votes(int) are the amount of times the given post was upvoted or downvoted. The title(string) is the title of the post. Over_18(bool) whether or not the post is restricted to accounts whose owners are 18 years or older. Author(string) the reddit account name of the poster. Subreddit(string) the subreddit this post was made on.

Most important to us will be to see whether or not there is a correlation between the dates of certain articles being posted and the stock price fluctuating, this we can do as we have dates for both datasets.
## Exploring data
The data doesn’t seem to have quality problems. We are considering classifying stocks based on their industry, to see if some industries' stocks are affected by headlines more than others.
## Verifying data quality
The data is good enough to support our goals. Only possible problem we might have is that we might or might not need to classify stocks by industry depending on if we can detect any correlation without classifying stocks. 
