# COVID-19-vaccine-Tweets
Sentiment analysis of COVID-19 vaccine Tweets


### Which Domain?
Natural Language Processing (NLP) is a branch of artificial intelligence that enables the machine to read, understand, communicate, and derive meanings from human’s natural languages.[1] Natural languages can be in the form of text or speech. The Semantic (text) analysis aspect of NLP enables the machine to understand the meaning conveyed by a text. It involves applying computer algorithms to understand the meaning and interpretation of words and how sentences are structured. With the combination of NLP and machine learning algorithms, sentiment analysis can be performed, to automatically identify the emotions attached to the communication. Text classification is a division of sentiment analysis to classify people’s opinions as positive, negative, neutral, happy, and sad, etc.
  
### Which Data?
For this project, I will be using tweets about the COVID-19 vaccines used in the entire world.[2] As per the Keggle data contributor, tweets are collected using the tweepy Python package to search Twitter API using relevant search terms. The dataset is continuously updated once a day, during morning hours (GMT). The tweets are about Pfizer/BioNTech, Sinopharm, Sinovac (both Chinese-produced vaccines), Moderna, Oxford/Astra-Zeneca, Covaxin, and Sputnik V vaccines. 
The tweets dataset contains below columns –
•	Id: 		Total 60.3k values
•	User_name: 	60.3k values ,32.6 unique values
•	User_location: 	13.8k missing values
•	User_description: 4158 missing values
•	User_created: 	user creation date.
•	User_followers:	follower count of user
•	User_friends: 	friends count of user.
•	User_favourites
•	User_verified: 	True-6421, False-53.9k
•	Date: 		Tweet date
•	Text: 		Tweet text, 60.3k tweets
•	Hashtags: 	hashtags
•	Source: 	web-31%, phone-29%
•	Retweets: 	retweet count

For the time-series analysis, I will be comparing sentiments trend with COVID-19 vaccination progress.[3] This data is collected from https://ourworldindata.org/ GitHub repository.[4] 


### Research Questions? Benefits? Why analyzes these data?
The year 2020 was full of COVID-19 spread across the world, multiple lockdowns, and burnout of healthcare workers. So far, 2021 has been focused on vaccine distribution. March 11, 2021, was the first anniversary since WHO declared COVID-19 as a global pandemic.[5] As everyone wanted to go back to normal life, people were closely monitoring vaccine developments. Due to the overflowing COVID-19 news and speedy development of a vaccine, people rationally have many questions on vaccines. Some of them are:[6]
-       Do the mRNA vaccines change your DNA? 
-       Did the vaccine clinical trials skip steps to be completed faster? 
-       Can the vaccine give you COVID-19? 
-       Will we need new vaccines if the virus continues to mutate?

Such questions and limited reliable answers lead to confusion and doubts overtaking the vaccine. As per Panacea lab, [7] every day, there are about 4 million tweets a day related to COVID-19. Hence, I planned to utilize tweets to understand people’s sentiments. This analysis will help to understand the difference in sentiments for different vaccines and the change in sentiments over time. 
Applications:
1.	Policy implementations for public awareness.
2.	Biotech companies can utilize this analysis to understanding people’s response to vaccination for future vaccine rollouts. 
3.	Social media monitoring.
4.	Market research.

### What Method?
Sentiment analysis helps governments and businesses to understand people’s opinions. I will be cleaning tweet texts by removing URLs, tokenizing, removing newline characters, removing single quotes, remove punctuation signs, lowercase all text, and detokenize text. Cleaning steps will be utilizing the Python NLTK package.[10] For the text classification, I will be taking a machine learning approach to sentiment analysis. Cleaned text, will be fed to classifier return categories, e.g., positive, negative, and neutral. For the modeling, I will be splitting the dataset to train-test and apply Single LSTM,[8] Bidirectional LSTM, and 1D CNN [9]. Depending upon the accuracy and speed of each model, the best model will be selected, to apply to COVID dataset for sentiment classification.  

### Potential Issues?
Working on the NLTK package is new for me. I might need to first create a framework to execute the analysis step-by-step.

### Concluding Remarks
Its been a long timeframe of sickness, sadness, hopelessness, and distress, but the rollout of COVID-19 vaccination globally has given rise to feelings of relaxation for so many. The information about vaccination, side effects, and efficiency is ongoing and circulating on social platforms. This project will utilize the power of NLP on Twitter data to understand the sentiments of people over-vaccination. Further, the most efficient model will be implemented on the dataset to generate trends.

### References:
1.	Wikipedia contributors. (2021, April 7). Natural language processing. Wikipedia. https://en.wikipedia.org/wiki/Natural_language_processing 
2.	All COVID-19 Vaccines Tweets. (2021, April 15). Kaggle. https://www.kaggle.com/gpreda/all-covid19-vaccines-tweets 
3.	COVID-19 World Vaccination Progress. (2021, April 17). Kaggle. https://www.kaggle.com/gpreda/covid-world-vaccination-progress 
4.	O. (2021). owid/covid-19-data. GitHub. https://github.com/owid/covid-19-data 
5.	Staff, A. (2021). A Timeline of COVID-19 Vaccine Developments in 2021. AJMC. https://www.ajmc.com/view/a-timeline-of-covid-19-vaccine-developments-in-2021 
6.	https://www.ucsf.edu/news/2021/01/419691/covid-19-vaccine-fact-vs-fiction-expert-weighs-common-fears 
7.	PanaceaLab - COVID19 Twitter Dataset Homepage. (2021). Panacea Lab. http://www.panacealab.org/covid19/ 
8.	Sosa, P. M. (2017). Twitter sentiment analysis using combined LSTM-CNN models. Eprint Arxiv, 1-9.
9.	Goularas, D., & Kamis, S. (2019, August). Evaluation of deep learning techniques in sentiment analysis from twitter data. In 2019 International Conference on Deep Learning and Machine Learning in Emerging Applications (Deep-ML) (pp. 12-17). IEEE.
10.	Garg, P., & Bassi, V. G. (2016). Sentiment analysis of twitter data using NLTK in python (Doctoral dissertation).
