# Recommender-System-for-Amazon-Fine-Foods

Big Data Analytics on Amazon Fine Foods

Problem Amazon is one of the largest cloud computing and eCommerce companies. As a result of that, Amazon relies heavily on recommendation engines that reviews customer ratings and purchase history to recommend items and improve sales. A user should be recommended products that are not purchased by the user yet, based on the previous purchase history. The main objective of this project is to create a recommendation engine based on user preference, the popularity of the items, and the importance of personalization for each user. For the users with no history of feedback, we have come up with a popularity-based recommendation algorithm to address this scenario.

Data The Data consists of the reviews and ratings from amazon's fine foods and was obtained from SNAP by Stanford University. The data span a period of more than 10 years, including 500,000 reviews up to October 2012. Reviews include product and user information, ratings, and a plain text review. It also includes reviews from all other Amazon categories.

The following review characteristics are provided in the dataset.

• ProductId - Unique identifier for the product • UserId - Unique identifier for the user • ProfileName - Profile name of the user • HelpfulnessNumerator - Number of users who found the review helpful • HelpfulnessDenominator - Number of users who indicated whether they found the review helpful or not • Score - Rating between 1 and 5 • Time - Timestamp for the review • Summary – A summary of the review • Text - Text of the review

Techniques We have used Python machine learning framework combined with Spark technology for our project implementation. The PySpark feature in Python is our primary tool. Also, we’ll be using some extensive Python libraries for Data mining like Numpy, Pandas, ScikitLearn for Machine learning, Seaborn for visualization, etc.

User-based Collaborative Filtering
• Using a distance-based approach, User-based collaborative filtering method was used to identify similar items based on the user’s previous ratings. • The distance metric used in this project is Cosine Similarity. • Cosine similarity is a measure of similarity between two non-zero vectors of an inner product space that measures the cosine of the angle between them. • It was found that this method yielded a high RMSE score of around 1.50275.

Alternating Least Squares Method

• The Alternating Least Square Factorization was performed using PySpark’s built-in library. • This method factor implements the Matrix Factorization method huge matrix into a smaller representation of the original matrix through alternating least squares. • It breaks down the huge User- Item matrix into two matrices with User and Item-based latent factors in it. This helps in producing personalized recommendations for a user. • The cold Start problem has been addressed and resolved with the Average of the Prediction method. • By using this algorithm, it was found that the RMSE was slightly less than the Distance-Based Collaborative Filtering method with a value around 1.20466.

 Popularity-based Recommendation systems
• Even though there is no history of ratings for new users, it is important to recommend a few food products to the user. We used a popularity-based recommendation to implement this. • Although it is possible to address the Cold Start problem by using Average of Prediction, we have used the popularity-based recommendation engine which does not make any assumptions. 

Results • For a new user who has neither has a history of purchase nor ratings, the popularity-based recommendation engine is used where the currently popular products are shown on the webpage. • Among the two collaborative filtering approaches, Matrix Factorization using the Alternative Least Square method yields lesser Root Mean Squared Error, Therefore Matrix Factorization with ALS is used as our final recommendation engine. • Therefore, for product “ABQAIIBTTEKVM”, the below-mentioned products are recommended.
