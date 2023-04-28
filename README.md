# Movie-Recommendation-
     1.User-to-User collaborative filtering:

We used a cosine similarity function to find the most similar user.
Cosine similarity between two vectors u and v: Sim(u,v)=u.v/||u||*||v||
We will find the similarity between target users with all the other users and will eventually find
the most similar user to the targeted user and will recommend the movies which are not
watched by the targeted user and have been rated more than 3 by the most similar user.

    2. Item-to-Item collaborative filtering:
 a. First step: Build the model by finding similarity between all the item pairs. Most
       common method to find similarity between item pairs is by using cosine
       similarity (which we have used).
 b. Formula for cosine similarity:Sim(u,v)=u.v/||u||*||v||

 c. Second step (prediction computation): To execute the recommendation system.
       It uses the items (already rated by the user) that are most similar to the missing
       item to generate ratings. We try to generate predictions based on the ratings of
       similar products. We compute this using the following formula. This formula
       computes the rating of a particular item using a weighted sum of the ratings of
       other similar products.
       rating(U,Ii)= Σj rating(U,Ij)*Sij/Σj Sij
 d. In our case, the item means movie. In the above formula, rating(U , Ii) means
       rating given by user U to ith item 
       (again here item is movie) and sij means the
       similarity between the i
       th and j
       th movie.
