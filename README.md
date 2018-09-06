# A predictive model for Goodreads Book ratings

## Introduction
The goal of this project is to mine the reviews,books and other user data, conduct hypothesis testing, and make prediction about user’s classification, book ratings.

## Data Sources 
To meet the objectives, three sets of data were scrapped from Goodread API.

    - A dataset of 54,000 randomly selected users, which contains public information of users including their name, number of reviews and ratings, numbers of their friends and book lists. 
 
    - A dataset of 71,582 randomly selected reviews and ratings, contains detail information about the content and timestamp of reviews.
    
    - A dataset of 33,478 randomly selected books with book features (id, description, number of pages, etc.) and statistics of book reviews (review counts, average reviews, text review counts)

## Research questions
    - Users: Is there any difference in rating and reviewing behaviors among different demographical subgroups of users? 
    - Reviews: Can we segment reviews based on how they are given by users?
    - Books: What are the major factors that impact the number of reviews and the average rating of a book on Goodreads? Is it possible to classify books based on their description?

## Methodology
I, first, conduct secondary research to gain general understanding about Goodreads platform and its user’s behaviors using online articles and social media posts about Goodreads and its users. I found that the most indicative factor of book sales is it's number of rating and thus, I will use book ratings as the dependent variable in my predictive model. Then, I performed quantitative analysis using data collected from Goodreads API through three major steps:

    •	Exploratory data analysis of users and books on Goodreads. The outcome of this steps is to understand the dataset and define relevant input of my models
    •	Conduct hypothesis testing (T-Test, ANOVA) on the random list of users and books 
    •	Predictive Modeling on Book ratings

## Models
    •	K-mean to cluster users based on numbers of their reviews, friend counts and their book lists
    •	Latent Dirchlet Analysis to cluster topics of books using their descriptions
    •	Regression model to predict rating of a book based on its features

## Challenges
The one major challenge of this project is the quality of the data. While Goodreads API provides several useful information such as location, genders or age, interest of users that could be captured, most of this information is not shared by users. Thus, the Null values are not random. 
Another challenge is that the behavioral data of users such as rating counts,friends are skewed, because a large of Goodreads userbase are non-active users, who have 0 records on most of the features

## Results & Recommendations

The Goodreads data analysis project attempt to perform exploratory analysis on users, reviews and books on Goodreads, to build a model to predict count of ratings on titles. The best estimator of my model is Gradient Boosting Regressor with n_components of 100 and max_depth of 10, giving the value of R square on the test set of .36. In evåaluating our regression model, the residuals on the test set are normally distributed.


**Recommendation**:
- The top 4 features in the importance ranking are "average ratings", "Love Family and Friendship", "number of pages","Series". Thus, to increase the number of ratings, authors should keep the average rating of their books as high as possible, write the descriptions of their books that focus more on love, family and friendships aspect, and extend your book content such as adding more pages or making a series.


- Users are the most active in giving reviews and adding books to their to_read list during lunch and dinner time on Monday, Tuesday, and Wednesday. Therefore, the author should advertise books or interacting with users during these timeframes to optimize their marketing efforts to increase rating reviews.


- Authors should optimize the visibility of their books on Goodreads recommenders because users who are using Goodreads to find new books are more likely to give high ratings compared to the ones who are not using are.


- Authors should put more efforts into advertising their books during Winter/fall as more users are active during this time

