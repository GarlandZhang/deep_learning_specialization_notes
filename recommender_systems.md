## predicting movie ratings
  - we predict what a user would rate a movie (in the case of the below diagram, based on its movie category) to potentially recommend the movie:
  
![movie](https://i.gyazo.com/4bf0104675d91b76357284952e801331.png)

approaches to building recommender systems:
## content-based recommendations
  - genres (aka content) % of the movie are features
![content](https://i.gyazo.com/905a5de8eebbd897dad40c10027f384e.png)
  - we add extra parameter x0=1 (sort of acts like a bias in NN)

problem formulation:
  - similar to linear regression but we only calculate cost over **rated** movies by the user
  ![cost_fn](https://i.gyazo.com/1a02b92daecbc40f3d8009b4831347d3.png)
  - we tune this cost function a bit:
  
**cost function**

![cfn](https://i.gyazo.com/c68e56b9fd0e74b2cbe4f071f9ebb243.png)

## collaborative filtering
see: https://realpython.com/build-recommendation-engine-collaborative-filtering/#:~:text=Collaborative%20filtering%20is%20a%20family,type%20of%20collaborative%20filtering%20approach.
there are two approaches. The first approach is **memory based**
  - two steps
  1. find similar users
    - use euclidean distance between the points in space or
    - use cosine distance (the smaller the angle between two vectors in space are, the closer they are in similarity; to prevent distance as an issue, normalize the vectors; reason why distance doesn't matter is because some users can be "harder" raters and so generally give lower ratings. So we look at things relatively).
  2. guess rating that user will give to a certain movie
    - take top 5 or 10 similar users and get average rating (or weighted average based on similarity)

the second approach is **model based** where we use the matrix and find the weights of interest to best approximate user ratings.

suppose the category features are not known. we can approximate their values based on the preferences of the users:

![guess](https://i.gyazo.com/929569c1270c750d39792a6283cba4c2.png)
  - we can then use this to approximate unknown user ratings (hence **collaboratie filtering**)!

optimization algo:
![algo](https://i.gyazo.com/5d559a5a8446a399cbe0eae60e5777e1.png)
  - solve for x(i) by determining what values of x(i) minimize the cost where the actual preferences best match the approximations
 
optimization objective:

![obj](https://i.gyazo.com/3e45ae27eac0edfd1172b6f4f38af2d4.png)
  - use both optim. algos to update each set of values simumlatenously to get an overall minimal cost function...
  
collaboritve filterin algo:
![algo](https://i.gyazo.com/ab492cd6f1a616d4219c88051885ae3f.png)
  - the first step is for symmetry breaking so features learn different things (same idea with NN for random init on weights)

### vectorization

![vec](https://i.gyazo.com/b78058d9d77f9f2be8b449e90dfbae16.png)

### finding related movies
  - since we represent movies by their feature vector, x1, we just look for the smallest distance between another instance x2, a related movie
![rel](https://i.gyazo.com/b7b29a842c468b386f387ecd45a3c38c.png)

### users who have not rated movies
  - new user have not rated any movies, therefore even if we run the collaborative filtering algo to predict the user's ratings, it will just be 0s as that minimizes cost:
!{no_rate](https://i.gyazo.com/6ffbd3e9916161d3779c4220cb5e8a22.png)
  - **solution**: mean normalization. basically, the new user is the "average user" and we update our prediction algo:
![mean](https://i.gyazo.com/e579b4204d6769a6375d684f60239b14.png)
  - dont apply **feature scaling** because all movie ratings are already beetween 0 and 5
  
  
