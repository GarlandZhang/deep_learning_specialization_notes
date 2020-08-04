## bias (underfit)
- high training cost error
- cross validation cost will be approximately = train cost


## variance (overfit)
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
