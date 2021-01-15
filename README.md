# Youtube Comments Sentiment Analysis
The study aims to review sentiments and opinions towards a YouTuber's channel based on the following article: - https://gantlaborde.medium.com/siraj-rival-no-thanks-fe23092ecd20

- Scraped over 1,000 YouTube comments using Python and Youtube Data API
- Engineered polarity and subjectivity features based on user's opinions on the targeted Youtube video
- The YouTube channel received a lot more negative and neutral sentiments from 17.23% to 1.42% in average sentiment polarity after the public backlash.


## Resources Used
**Programming language:** Python 3.7

**Packages:** pandas, numpy, spacy, texthero, seaborn, matplotlib, re, json, pickle, urllib

**Scraper Article:** https://towardsdatascience.com/how-to-build-your-own-dataset-of-youtube-comments-39a1e57aade

## YouTube Comments Scraping
Scraped the following data points from YouTube API:
- comment
- comment_id
- author_url
- author_name
- reply_count
- like_count
- date
- vidid
- total_reply_counts
- vid_title
- just_date

### Steps: 
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

## Data Cleaning
- Preprocessed data with a custom function using the Texthero library:
  - Changed text to lowercase
  - Removed digits
  - Removed punctuations
  - Removed diacritics
  - Removed stopwords
  - Removed whitespace
  - Removed HTML tags
  
## Exploratory Data Analysis

### Video 1
<p float="left">
  <img src="https://github.com/PannaD8ta/YT_Comments_Sentiment_Analysis/blob/main/Sentiment_Analysis_plot_1.png" alt="Video 1" width="350" height="300"/>
  <img src="https://github.com/PannaD8ta/YT_Comments_Sentiment_Analysis/blob/main/Word_Cloud_1.png" alt="Video 1" width="450" height="300" />
</p>

### Video 2
<p float="left">
  <img src="https://github.com/PannaD8ta/YT_Comments_Sentiment_Analysis/blob/main/Sentiment_Analysis_plot_2.png" alt="Video 1" width="350" height="300"/>
  <img src="https://github.com/PannaD8ta/YT_Comments_Sentiment_Analysis/blob/main/Word_Cloud_2.png" alt="Video 1" width="450" height="300" />
</p>


