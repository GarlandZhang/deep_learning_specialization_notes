## bias

a high bias (underfitting) model:

![bias](https://i.gyazo.com/cad2adcf594fecff9abf430cd5023173.png)
  - more data will cause training error to increase but eventually plateaus as each new point has less effect on average error. same idea with cv error. 
    - in fact they converge to same error so **getting more data will not do much**
  - train error approx same as cv error

a high variance (overfitting) model:

![var](https://i.gyazo.com/53aa3426c5acfc7abb0af74eb55d1c26.png)
  - doesn't plateau, therefore extrapolating from graph suggests solution is to **get more data**
  - observe cross validation is high but decreases as we get a better model to predict the data (little data makes it hard to make a good generalized model)
  
  
**note**: it doesn't matter if training set error goes up as we really only care about test set error (generalized error)
