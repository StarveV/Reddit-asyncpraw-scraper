# Reddit-asyncpraw-scraper
scrape post on any subreddit with asyncpraw thenexport it a .xlsx file

## Requirements
> Python 3.7+
> openpyxl
> asyncpraw
> asyncio

## Output
The script will scrape data from any designated subreddit (set to r/wallstreeetbet in this python script) for the selected period of time (past 7 days as demon in the script) and save it to an Excel spreadsheet with the current date and time in the filename. The data saved to the spreadsheet includes the date and time of the submission, the title, score, post body, and number of comments.

## Note
The script is set to time out after 30 seconds for a single request and will make a maximum of 10 additional trials if no new submissions are found. These values can be adjusted in the code.

## Instructions
#### change the date or selected timeframe with the following code
```
no_days = 7
end_date = datetime.datetime.now()
start_date = end_date - datetime.timedelta(days=no_days)
```
#### change the reddit client id and secert
```
# Set the reddit client key
client_id='your_client_id'
client_secret='your_secert'
user_agent='your_agent'
```
