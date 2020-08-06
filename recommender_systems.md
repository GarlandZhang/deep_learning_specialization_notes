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

