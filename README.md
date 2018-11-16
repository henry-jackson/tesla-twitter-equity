# <p align="center"> Code Louisville 2018 Python Project - Henry Jackson </p>

## To Install
```
git clone https://github.com/henry-jackson/tesla-twitter-equity.git
```

## You will need the following dependencies/programs
1. Anaconda - https://www.anaconda.com/download
2. Jupyter Notebook - http://jupyter.org/install

## To Run
1. Open your terminal
2. Change directory to the cloned folder
3. Create conda environment from spec-file.txt
```
conda create --name teslatwitter --file spec-file.txt
```
4. Install conda environment to get all package dependencies
```
conda install --name teslatwitter --file spec-file.txt
```
5. Run Jupyter Notebook by running below script in your terminal
```
jupyter notebook
```
6. Open the file tesla-twitter-notebook.ipynb in your browser
7. Select 'Kernel' and then 'Restart and Run All'

## Data Dictionary
```
    TWEET - a posting made on the social media website Twitter. The maximum character length is 280 characters as of late 2017
    HIGH - the highest price the stock was traded for on a particular day
    LOW - the lowest price the stock was traded for on a particular day
    OPENING PRICE - the price at which a security first trades upon the opening of an exchange on a trading day; for example, the New York Stock Exchange opens at precisely 9:30 a.m. EST
    CLOSING PRICE - the final price at which a security is traded on a given trading day. The closing price represents the most up-to-date valuation of a security until trading commences again on the next trading day; for example, the New York Stock Exchange closes at precisely 4:00 p.m. EST
    TIMESTAMP - a digital record of the time of occurrence of a particular event
```

## How does Elon Musk's activity on Twitter impact Tesla's stock price?

<b>Introduction:</b>
Due to a tweet Elon Musk sent out the summer before I started my Code
Louisville cohort, which sent the price of TSLA stock shooting upwards, I was curious as to how much his tweets, on average, affect the stock price of his company. Should he stay off of Twitter, increase his number of Tweets, or does it not matter when viewing the data on aggregate? 

<b>Hypothesis:</b>
My best guess before starting this project was that he probably decreases his
company's stock in correlation to how much he tweets.

<b>Procedure:</b>
I downloaded as many of his most recent tweets that I could with a free Twitter
API account and the twarc python script that can be found on github. This was
stored in a json file. Next, I went to NASDAQ's website and downloaded
a spreadsheet of Tesla stock data for a similar time frame. Data was loaded
into pandas dataframes, graphed separately for their own analysis, and then
compared with a numpy correlation function. The data was also compared on
a scatter plot. Units of comparison were the number of tweets per month, and
the average daily change in price per month (close price - open price).

<b>Results:</b>
Run the notebook to view my results and see how I queried the SQL databases and
graphed everything!

<b>Conclusions:</b>
There was virtually no correlation between the two datasets. It can be
concluded that tweet quantity did not affect the daily price change in Tesla
stock when considering one month of trading days per sample.

<b>Ways to Take This Further:</b>
- Make graphs more aesthetically pleasing
- Publish on my portfolio instead of a jupyter notebook
- Graph/identify outliers
