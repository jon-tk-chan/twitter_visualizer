# twitter_visualizer
Code for collecting Twitter data and performing EDA on tweet text

Prepared as submission for Our World In Data Job posting: https://ourworldindata.org/data-scientist-2023-q1 

## INTRO
Purpose: Develop a data pipeline for analysis of individual user tweets. Interested in topics that a user mentioned, average sentiment of tweets

Research question: What are the topics that OWID team members posting about on Twitter?

#### Skills Demonstrated (research design)
Project should demonstrate applicant proficiency in the following:
- Data collection - scraping Twitter handles from OWID Team page, working with APIs, extracting relevant items from JSON
- Data wrangling - converting semi-raw data into Python Pandas format workable by common Python visualization tasks
- Data visualization - Use of appropriate visualization types, accessible colorschemes, some level of interactiveness (display topics, user, links on hover?)
- Version control - use of git and github for managing code and demonstrating workflow
- Soft skills of author - critical thinking when approaching a technical assignment

OUTPUT: A Streamlit app showing the following:
1. A paragraph introducing the topic
2. NLP VIS 1 - Wordlcloud of the most 
3. NLP VIS 2
4. OUTPUT DATA HEADER (df.head() of one of the dataframes)
5. limitations

## LITERATURE REVIEW:

- Tutorials referenced:
    - Clustering Methods, tf-idf refresher, LDA refresher: https://towardsdatascience.com/a-friendly-introduction-to-text-clustering-fa996bcefd04 
    - Text clustering tutorial: http://brandonrose.org/clustering 
    - Grouping using K-Means clustering, Wordcloud: https://machinelearninggeek.com/text-clustering-clustering-news-articles/#:~:text=Text%20Clustering%20is%20a%20process,in%20different%20clusters%20are%20dissimilar.
- Best practices in data visualization

## METHODOLOGY:

#### Technical Features (kind of data)
- Function that recieves a Twitter handle, outputs the most recent X tweets from that user
    - Assume that Twitter developer account is set up - recieved access tokens
    - Minimum viable product: most recent 10 tweets from a given user (switch between most popular and most recent?)
    - Ignore retweets
    - Output: JSON containing at least the following fields: user, tweet, date of tweet, rts, favs, hashtags, media, URLs
- Function to take in list of JSONS of each user, make pandas dataframe
    - from data columns: user, tweet, date of tweet, rts, favs, hashtags, media, URLs
    - New columns: NER? topics?
- Function to create bar chart of words/topics vs frequency of mentions, grouped by user
    - PLAN THIS DF MORE
