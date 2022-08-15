# Yotube Recommendation System

![image](https://user-images.githubusercontent.com/25899745/184698408-22beabb2-53c7-4a34-aac7-0061f86e9b26.png)

Recommendations using LDA (Latent Dirichlet Allocation): Latent Dirichlet Allocation
is an unsupervised NLP model used for discovering topics from a document. It is a popular topic
modeling technique that works on a principle similar to clustering on numerical data. LDA is
extremely useful in delineating hidden patterns in a collection of words. In this project, LDA has
been used for recommending videos based on similarity with the given input video. The
following steps have been followed while developing this model:


Step 1- Creating a new dataframe
The original dataframe (without duplicates) is re-constructed by dropping all the remaining
columns except for ‘title’, ‘channel_title’, ‘tags’ and ‘description’ columns.

Further thechannel_title, tags and description columns were grouped together into a a column named
‘overview’. The cleaned data frame now has two columns ; "title" representing the name of the
video and "overview" with all the necessary information pertaining to the video.


Step 2- Text Preprocessing : Preprocessing of textual data has been executed in four stages:
(i) Removing non-english words (ii) Removing Stop words
(iii) Building Bigrams (iv) Lemmatization


Step 3- Initializing LDA Model : LDA has four assumptions:
(i) Each document is a bag of words.
(ii) Stop words do not carry any information about the topic.
(iii) The number of topics(k) are known beforehand.
(iv) Except for the word in question, all other topic assignments are accurate.
By considering these assumptions, the LDA model is initialized and k value is assigned to be 10
(for generating top 10 recommendations). LDA automatically finds the most used keywords in
the ten topics constructed and arranges them according to their probability scores.

Step 4- Building the Recommender System : The recommender system is designed such that it
operates on the basis of the probability scores. When a test title is given as the input, the model
calculates the probability of that title belonging to one of the 10 topics. The system treats it like a
classification problem. The videos with the top 10 highest scores are taken into consideration
and are suggested as recommendations to the user.


![image](https://user-images.githubusercontent.com/25899745/184699344-24ac9010-6972-4129-ba49-7899e0441353.png)




