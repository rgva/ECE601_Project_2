# ECE601: Project 2 - Analyzing UFC Fight Trends
## Phase 1(a): Twitter API Tool Tests
### '0-authentication'
This script is the authentication script used in every following python notebook implementing a few of the different tools of interest for Project 2. 
### '1-list_tweets'
In this script, I am playing around with the functionality of listing tweets from a users timeline. Implenting pandas dataframes, I was able to create a list of tweets, replies, and reference IDs exported as a .csv file 'tweetslist'. This particular test involved my own account, and the .csv file was successfully generated. 
### '2-interacttweets'
In this script, I am using the twitter API to interact with a singular tweet. This can then be used to pull analytics from the tweet - such as number of likes, retweets, etc. but I am currently limited by the access level of the API in doing so.
### '3-automatefollows'
Similarly to the second script, this script is not able to be performed at the current access level. However, it automates following users which the @UFC account follows, given the parameter of greater than 300 friends, and greater than 300 followers to limit the amount of bot accounts followed.

### 'UFC-araujo-grasso_tweets'
This script performs a search of recent tweets relating to the upcoming UFC Fight Night: Araujo v Grasso, storing them in pandas. The implementation for sentiment analysis is fairly simple in this script - mainly pulling the last 1000 tweets relating to both 'Viviane Araujo' and 'Alexa Grasso', and analyzing the overall sentiment of these tweets. Further implementations will give a more detailed review of positive (such as proportions of positive/neutral/negative, etc. You may see that in these tests, both queries for both fighters turn out mostly negative sentiments in the last 1000 tweets for each (unsurprising given the nature of Twitter). 

### 'singlebot-UFC'
This is a very basic test of the funcionality of the Botometer library. In theory, the function should take the the input string '@UFC' and verify if it is a bot or not using criteria defined by the Botometer. However, when run, the output raises 'Not authorized' - after much troubleshooting, and changing the subscription on RapidAPI to 'Botometer Pro' this is still not rectified, and I will have to verify with my instructor to see why. 

## Phase 1(b): Google NLP

## 'google_nlp'
The Google Cloud uses an interactive version of Python in the cloud shell with the NLP libraries pre-installed. Given the difficulty of exporting these results as a legible .ipynb (since authentication is not a simple process outside of the cloud development environment), I have attached the file 'google_nlp' including the results s I obtained on the Cloud Terminal. Please note this is not able to run on any outside IDE. For sentiment analysis, the Google NLP is very adept at recognizing positive and negative sentiments. The phrase: "Alexa Grasso is a terrible fighter!" scored -70.0% (indicating substantial negative sentiment), and likewise, the phrase: "Viviane Araujo is a great fighter!" scored 90.0% (indicating overwhelmingly positive sentiment). 

## Phase 2(a): User Stories
### User Stories
Cory Sandhagen (Bantamweight Div., UFC): "Wow, I'm really torn between these two fighters - I'm not sure who I should support publicly in order to safeguard my reputation!"

Jimmy Random (Someville, Ohio): "I'm just getting into UFC, and I don't have a favorite fighter yet. I'd love to see who the favorites are so I can start looking up their clips and rooting for them, but I don't know where to start!"

Joe Rogan (Podcast Host): "I wish there was a way I could pad my UFC Fight Night talks with statistics that will make me sound smart!" 

In general, the users for this application will be fans, fighters, and commentators, all of whom have different interests in accessing this data.

MVP: 
The product should do these things at a minimum:
- Pull thousands of tweets relating to a certain fighter.
- Perform sentiment analysis, identify what the overhwelming sentiment is toward that fighter, and provide a limited set of examples from the tweets.
- Classify the number of positive to negative tweets.

## References
YouTube: CodingEntrepreneurs - '30 Days of Python - Day 21 - Twitter API with Tweepy - Python TUTORIAL'

Samuel Diaz, Data Scientist - 'Twitter Sentiment Analysis & Botometer — Part 2' via medium.com

Google Developer Codelabs - Using Natural Language API with Python
