overfitting

having a higher order function to better fit the model does not generalize well and is therefore a bad predictor. similarly, a low-order function will lead to **underfitting**

2 options to reduce overfitting:

1. reduce number of features
2. regularization:
  - keep all features but reduce magnitude of some parameters
  
## regularization cost function

"If we have overfitting from our hypothesis function, we can reduce the weight that some of the terms in our function carry by increasing their cost."

![cf_reg](https://i.gyazo.com/184feedb3a10ba81992d378f26a755e6.png)
  - 03 and 04 become super small because their contributions are magnified by the 1000x multiplier
 
 ![min_goal](https://i.gyazo.com/46b789746341f32b4aa2f08c7b2741f6.png)
 
- "The λ, or lambda, is the regularization parameter. It determines how much the costs of our theta parameters are inflated."
- the goal to minimizing cost function is twofold: the first component focuses on minimizing error, the second component focuses on minimizing parameter magnitude and therefore "simplify" the model from overfitting.
- note: the 00 is not regularized by convention

## regularized linear regression

![gd](https://i.gyazo.com/d7d58bcad72d4d37d776d50e6990383a.png)

![ne](https://i.gyazo.com/da26f85e887fe9c012826af437f30f9d.png)

## regularized logistic regression

same idea as linear regression where we simply add the lambda component to the cost function. 

![reg_log_reg](https://i.gyazo.com/1a6016d0639e4f7eaf3d349fecc81f6c.png)

In gradient descent, we just add the derivative lambda component (except for the first term 00 of course).

![gd](https://i.gyazo.com/3d0a4789c4e2b5c349925322dca447b8.png)

## l1, l2

see l1vsl2 regulariztaion 

## dropout regularization
  - dropout a subset of nodes in the neural network at random for each iteration 
  - only use for overfitting to prevent relying solely on any single feature 
![dropout](https://i.gyazo.com/d42a0f158c7f04734f65c6f9cc78b85e.png)

### impl
![impl](https://i.gyazo.com/a62c9e828065a8059f274e75e58092e9.png)
  - we keep keep_prob % of nodes in current layer
  - we "remove" nodes by just zeroing out its value (when calculating the Z value for next layer)
  - we must adjust the current activations by dividing by keep_prob % to ensure the magnitude of Z doesn't change cause of dropout
  - at test time, dropout is not activated
  
### intuition
  - ensures we don't rely on any one feature, so have to spread out weights
  
## early stopping
  - prevents weights from becoming too big by stopping iterations at mid-size level
  ![early](https://i.gyazo.com/cd023edebbe86922683f832dc02a9172.png)
  
  
