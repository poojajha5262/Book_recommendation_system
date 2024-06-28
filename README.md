# Book_recommendation_system
In this project we use three different datasets to come up with a book recommendation system for different users based on how they and others have rated previously purchased books.
Dataset 1: Users Data Dataset 2: Ratings Data Dataset 3: Books Data
Project Summary:
Recommender systems go hand in hand with the bussinesses that have established their presence on the internet. With the huge amount of products and services available online to customers, it becomes imperative for the bussinesses to boil down the total available items to a select group of items that might be of interest to a customer. This will not only enhance the customer's shopping experience and reduce the efforts which go into making a satisfying purchase but it will also have a tremendous impact on the performance of the bussiness.

In this particular project we were put against three datasets each having a specific information about different aspects that go into a purchase. Users dataset carried information about the customers location and Age. Ratings dataset gave us information about how each customer had rated his/her multiple book purchases on a scale from 1-10 and how a good chunk of customers prefered to act lazy in rating their purchases. These Latter customers' ratings for such purchases were taken to be 0 which stood for an implicit rating in favour of such books.

Our Approach towards this project:

Data cleaning and EDA:

We began our project by performing a primary inspection of all the three datasets. We checked and handled outliers null values and duplicacies in various columns. Once we were assured of a clean set of dataframes we merged them together into a single dataframe to carry our EDA.

Next, we perfomed Exploratory analysis on our dataframe to come up with insights about Authors, Publications, Titles and about different age categories of customers. We also build an interactive dataframe which could provide popularity based recommendation to a new customer and these popularities could be based upon average rating an author, a book, or a publisher had received from previous cutomers.

Model building using KNN:

We then moved on to build a memory based recommender for explicit rating case (1-10) using a Nearest Neighbour approach. Customers who had rated a certain book on good scale would be getting recommendations based on other customers who also had rated that particular book on a good scale.

Model building using SVD:

The next big step was to build a model based collaborative recommender system which could very well be evaluated in realtime. For this purpose we chose a very frequently used model namely Matrix Factorization using SVD. In this approach what we broadly do is set forth a pivot table with Customers and Items as columns and rows, and values for each customer-Item mapping is either a zero or an explicit rating for that particular customer-item pair. This matrix is then decomposed into factors using SVD and the individual element of decomposition is multiplied back into a complete matrix to finally generate recommendations.

Model building for implicit case using KNN:

After we had dealt with the explicit ratings, we started working on implicit ratings case. Firstly, we developed a model based on KNN where in Age of customers was taken as a relevance factor to recommend books. In this recommender, a customer who had previously purchased a certain book, would be recommended books based on other customers' buying patterns who were most nearest to him in terms of age.

Model building for implicit case using content based approach:

Our dataset lacked any description for the books that there in the data. Our next step was to fetch description of as many books as we could using Google's API. Once we had successfully fetched the descriptions for a sufficient number of books, we developed a content based model using TFIDF vectorizer. Once this model was built, we could recommend books based on the similarity of content in the books a customer had purchased with the other books that were there in the corpus.

Creating a dummy web page for generating recommendations:

Finally we also developed and tested a web page which could take our models in the backend and produce recommendations to a given input item. Conclusion of the Project:- It is very important to deal with implicit and explicit user ratings, separately. For dealing with explicit ratings, we can build simple models based on ratings, and we can also use certain comprehensive models based on Collaborative Filtering approach. For dealing with implicit ratings, we can build KNN based models , and we can also use content based models, which utilize the similarity of different contents, to make recommendations. It is crucial to be precise about user preferences, otherwise repetitive recommendations can cause nuisance to the user.

Conclusion of the Project
It is very important to deal with implicit and explicit user ratings, separately. For dealing with explicit ratings, we can build simple models based on ratings, and we can also use certain comprehensive models based on Collaborative Filtering approach. For dealing with implicit ratings, we can build KNN based models , and we can also use content based models, which utilize the similarity of different contents, to make recommendations. It is crucial to be precise about user preferences, otherwise repetitive recommendations can cause nuisance to the user.
