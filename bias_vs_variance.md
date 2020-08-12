## bias (underfit)
"Bias is error due to erroneous or overly simplistic assumptions in the learning algorithm you’re using. This can lead to the model underfitting your data, making it hard for it to have high predictive accuracy and for you to generalize your knowledge from the training set to the test set."

- high training cost error
- cross validation cost will be approximately = train cost


## variance (overfit)
"Variance is error due to too much complexity in the learning algorithm you’re using. This leads to the algorithm being highly sensitive to high degrees of variation in your training data, which can lead your model to overfit the data. You’ll be carrying too much noise from your training data for your model to be very useful for your test data."

- low train cost
- cv cost >> train cost


![bv](https://i.gyazo.com/d1a42514aa8fbc5fa421922e2a07f064.png)

## regularization effect on bias and variance

- with large lambda, then theta parametsrs approx = 0 so we cost function will be approx. equal to 00 or a horizontal line
  - therefore high bias (underfit)
  
- small lambda means very complex function therefore overfit
  - therefore high variance (overfit)

![reg](https://i.gyazo.com/0fa2f772c280cead3c3f1333e5264e13.png)

### choosing lambda

![choose_lambda](https://i.gyazo.com/3faf9aaad3a6ea9ae26a7fd8a1fa8881.png)
  - choose model lowest validation error
