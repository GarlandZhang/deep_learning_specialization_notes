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
