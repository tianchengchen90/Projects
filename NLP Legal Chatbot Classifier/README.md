## Problem Statement

The use of chatbots and other bots are increasingly prevalent in modern times. Corporations, and government bodies alike make use of these bots to handle repetitive tasks. Some of the chatbots rely on automated responses, while others are using Machine Learning to enable better responses that are closer to human interaction. In order to make the interaction more immersive, there has been a trend towards machine learning models for such chatbot. 

With this growing trend, legal implications to organisations may arise, since there has been several instances of such chatbots misbehaving and giving harmful replies, ranging from defamation, to telling people to kill their parents. Machine Learning models may inadvertantly dish out legal advices that makes the company which owns the chatbot liable if they do not work out.

In light of this trend, it may be beneficial for Machine Learning model to classify what is a query that is asking for legal advice and what is a query that is not legal advice. The response when a legal query is received can be to direct it to the relevant authorities, caveat and protect the owner of the bot before answering, or just not responding to those types of queries.

I have opted to use `r/NoStupidQuestions` to mimic real life questions, where users from all walks of life ask any questions they want, while `r/legaladvice` to mimic real life legal queries and questions that have legal implications. This project will look at how successful I will be able to correctly classify posts from the two subreddits.

It is interesting to note that `r/NoStupidQuestions` contains questions that have no boundaries, since all questions are welcome. The result is a melting pot of questions which mimics the borderline nonsensical questions that many asks chatbots out of leisurely purposes, as well as serious and insightful questions.


## Executive Summary
A data science approach was used to guide the process. The problem statement was defined as building a classifier model which has high accuracy is predicting what is a legal query and what is a general query

Data was scrapped off Reddit, with twelve thousand submissions from each subreddit. Data was imported as a dataframe and cleaned before merging. An exploratory data analysis was to evaluate and understand key trends, and top used words before coming up with the areas which will be visualized. 

Inferences are made at each visualisation and exploratory data analysis stage, and external reasons were made to give insights. Similarly at the error analysis phase, logical reasoning was used to give insight to why false positive and false negatives occur.

Lastly, TF-IDF Vectorizer with Logistic Regression was chosen with 93.44% accuracy score on test data, and 93.15% sensitivity. Random Forest was not suitable as it takes too long to fit and optimise. Multinomial Naive Bayes models simply was not as accurate. Lastly, CountVectorizer gave rise to higher instances of false negatives.

## Error analysis
- 1) On several recurring topics, it becomes difficult for the model to distinguish if it belongs to `r/legaladvice` or `r/NoStupidQuestions`. Due to the scope of the project, the stopwords had to include subreddit names in it. Legal being used as a stopword is a severe handicap to the model, especially when it comes to short posts in r/legaladvice, where people can ask "is doing topic X legal?"

- 2) Sexual assault, sex, relationship advices, tax, property, management and matters that the police are handling are some common themes.

- 3) There are irreducible error within the model due to some legal queries being posted in `r/NoStupidQuestions` and non legal queries posted in `r/legaladvice`.

## Limitations and future works
#### Misclassifications of questions in subreddit, wrong spellings in posts
As observed from the misclassified datapoints, there are a number of submissions that are posted in `r/legaladvice` that are badly crafted and do not look like they have legal implications. Similarly, there are a number of submissions posted in `r/NoStupidQuestions` that are legal queries in nature, since all questions are welcomed in that subreddit. This creates confusion for the model, but for now, this works out as a proxy for real life questions and legal queries. 

Also, there were several instances of use of shortforms and spelling errors in the data.

To improve on the data, should an organisation want to proceed further, logging in new data with high integrity would be helpful. This is to prevent the situation of garbage in garbarge out.

#### Law terms are different across all countries
A challenge when implementing the classifier is that legal jargons can be very different across different countries. There must be a sizable number of data to train the model to become more accurate. Thus, the current model would take time to be implemented across different countries.

#### Differences in language and slangs
Word choices can be different across different cultures. Even amidst the english language, the British, Americans and Australians for example will have their own colloquial ways of writing.

Furthermore, the model is built on existing data from Reddit based on the english language. There will be a limitation of language as such. 

#### Hyperparameters tuning for Random Forest
In my process, I have opted to run RandomizedSearch instead of GridSearch for the two Random Forest models. Perhaps the accuracy rates could have been improved further, and if organisation have the capability and investment to process the model quick enough, they may get a different model choice compared to me.

#### Merely one step in the correct direction
Other classifier related to suicide, depression, and defamation can also be paired with this legal query classifier. My classifier alone will not be sufficient to cover all liabilities legally.





