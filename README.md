# twitter_visualizer
Code for demonstating Natural Language Processing and Data Visualization skills of author. Prepared as submission for Our World In Data job posting: https://ourworldindata.org/data-scientist-2023-q1 

Research question: What Twitter accounts are the OWID team interacting with recently?

Purpose: Develop a data pipeline for visualizing Twitter Interactions of the Our World in Data team. Future NLP tasks includes identifying what in topics that a user mentioned, average sentiment of tweets,identifying most frequent bigrams/trigrams 


#### Skills Demonstrated (research design)
Project should demonstrate applicant proficiency in the following:
- Data collection - scraping Twitter handles from OWID Team page, working with APIs, extracting relevant items from JSON
- Data wrangling - converting semi-raw data into Python Pandas format workable by common Python visualization tasks
- Data visualization - Use of appropriate visualization types, accessible colorschemes, some level of interactiveness (display topics, user, links on hover?)
- Version control - use of git and github for managing code and demonstrating workflow
- Soft skills of author - critical thinking when approaching a technical assignment

- NetworkX package used for creation of network graphs: Can read more about network graphs at: https://networkx.org/documentation/stable/reference/introduction.html#graphs 
- Twitter data is collected using the Tweepy package and the api.user_timeline() function: https://docs.tweepy.org/en/latest/api.html#tweepy.API.user_timeline


#### Functions included: 
- Function to scrape the team twitter data - Names, title, twitter handles, etc
    - output: dataframe containing the team's twitter data
- Function that recieves a Twitter handle, outputs the most recent X tweets from that user
    - Assume that Twitter developer account is set up - recieved access tokens
    - Minimum viable product: most recent 10 tweets from a given user (switch between most popular and most recent?)
    - Output: dataframe of all tweets containing at least the following fields: user, tweet, date of tweet, rts, favs, full_text, and list of interactions between OWID team member and other Twitter accounts
- Function to create network graph images based on Twitter interactions:
    - Nodes: Twitter users
    - Edges: Any interaction between a twitter users (Mentions, retweets, replies)

    
## Final Notes
- Initial ideas to prepare a network graph of interactions between team members was ignored due to visual clutter - more informative to show each OWID team member individually as proof of concept
- Export of data should only include data that is publically available - team page of OWID website, public tweets of OWID team members

