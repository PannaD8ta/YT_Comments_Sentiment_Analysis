# Youtube Comments Sentiment Analysis
The study of sentiments and opinions towards the YouTuber's videos was made based on the following article: - https://gantlaborde.medium.com/siraj-rival-no-thanks-fe23092ecd20

- Scraped over 1,000 YouTube comments using Python and Youtube Data API
- Engineered polarity and subjectivity features based on user's opinions on the targeted Youtube video

1. Firstly, let's get on a virtual environment (venv). "comments_collector" is the name of your venv, and it can be any name of your liking
```
python3 -m venv comments_collector
```
2. Activate your venv 
```
source comments_collector/bin/activate
```
3. Install all the required libraries
```
pip3 install requirements.txt
```
4. Obtain your YouTube Data API from the link below. Credits & tutorial link: https://bit.ly/2Ljdk4s
```
https://console.developers.google.com/ 
```
5. Next, run the command below to collect the comments and store it in a tabular data format (.csv) 
```
python3 cleaned_get_youtube_comments_backup.py --order time --csv_filename MrBeast_comments --apikey path/to/apikey.json
```
6. Run the newly mined .csv files on the YT_Comments_SentimentAnalysis.ipynb
