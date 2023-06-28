![TS](https://github.com/sriram2098/Twitter_Scrapping/blob/main/Twitter-scraping.jpg)


# What is Twitter Scraping?
  Scraping is a technique to get information from Social Network sites. Scraping Twitter can yield many insights into sentiments, opinions and social media trends. Analysing tweets, shares, likes, URLs and interests is a powerful way to derive insight into public conversations.
  It is legal to scrape Twitter or any other SNS(Social Networking Sites) to extract publicly available information, but you should be aware that the data extracted might contain personal data.
  
# How to Scrape the Twitter Data?
  Scraping can be done with the help of many opensource libraries like 
	
  1. Tweepy
  2. Twint
  3. Snscrape
  4. Getoldtweets3
  
  For my project I have used SNSCRAPE library.
   
# Libraries and Modules needed for the project!

 1. snscrape.modules.twitter - (To Scrape the Data from Twitter)
 2. Pandas - (To Create a DataFrame with the scraped data)
 3. Pymongo - (To upload the dataframe to MongoDB database)
 4. Streamlit - (To Create Graphical user Interface)
 5. Datetime - (To get the current date)
	

# Snscrape
  Snscrape allows you to scrape basic information such as a user's profile, tweet content, source, and so on. Snscrape is not limited to Twitter, but can also scrape content from other prominent social media networks like Facebook, Instagram, and others. Its advantages are that there are no limits to the number of tweets you can retrieve or the window of tweets (that is, the date range of tweets). So Snscrape allows you to retrieve old data.

# Streamlit
  Streamlit is an open source app framework in Python language. It helps us create web apps for data science and machine learning in a short time. It is compatible with major Python libraries such as scikit-learn, Keras, PyTorch, SymPy(latex), NumPy, pandas, Matplotlib etc. Streamlit allows you to re-use any Python code you have already written. This can save considerable amounts of time compared to non-Python based tools where all code to create visualizations needs to be re-written.
  
  In my project I've extensively used streamlit API Reference feature for creation of Titles, Images, Headers, Input boxes, Buttons, Checkbox, Download buttons.
 
  To know more about Streamlit do visit the official site- https://docs.streamlit.io/library/api-reference
  
# Workflow
  Lets us see the workflow of the twitter scraping project.  
  
  
  Importing the libraries.
  As I have already mentioned above the list of libraries/modules needed for the project. First we have to import all those libraries. Before that check if the libraries are already installed or not by using the below piece of code.  
	
  If the libraries are already installed then we have to import those into our script by mentioning the below codes.
 
 ## Scraping the tweet

To scrap the data Snscrape python library is used. The TweetSearchScrape() method scrape the Twitter data without Twitter API. The method is passed with a query conating the hashtag to be search and the search dates (From start date to end date)

## Uploading data in MongoDB

Tweets that are scraped using the Snscrape library is inserted into the MongoDB database by establishing the clinet connection. The tweet datas are strored under the twitter db collections.

## Creating the UI

Used Streamlit app for creating the GUI for Twitter Scraping. Used menus for searching, dispalying the tweets and to download. 
 
 **Menu 1 -- Home**  
Home page of the UI conatins title of the app

**Menu 2 -- About**  
Conatins small description about the Twitter Scraping, Snscrape librray, MongoDB and Streamlit framework.

**Menu 3 -- Search**  
Search menu which is used to search the tweet data usng the #hashtag and for given dates. Everytime the search menu deletes the existing datas while searching the new tweet in order to retrive the tweet information correctly.

**Menu 4 -- Display**  
The scraped data from the MongoDB database are dispalyed as a DataFrame

**Menu 5 -- Download**  
The scraped data from the MongoDB database is downloaded as CSV/ JSON file formats as per the requirement. 
  
  
### To view the demo video of my project checkout this link -   [TWITTER SCRAPPING PROJECT](https://www.linkedin.com/posts/sriram-s-2022s2809_project-share-video-activity-7079811490345586688-_8Lm?utm_source=share&utm_medium=member_desktop)
  
  
