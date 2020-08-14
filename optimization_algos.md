## expoenntially weighted average

## grad desc with momentum

## rmsprop
  - similar to momentum
  - note: in practice, the space is high dimensional, but its simplified to illustrate the bias in the vertical dimension, and the weights in the horizontal dimension:
  
![impl](https://i.gyazo.com/99aa8bed7f7406c39bbc40d67acda0b7.png)
  
## adam
  - cmobined momentum (again) and rmsprop  
![impl](https://i.gyazo.com/cf22d34e56c7a4b74129f347fc89e39c.png)

### hyperparameters

![hyper_params](https://i.gyazo.com/826b03f5d033ea092d42bf11491dd123.png)


## learning_rate decay
  - slowly reduce alpha
  - can be done manually if training a single model and takes long time 
  
## saddle point
  - is like a local optima except not in all directions
  
  ![giddyup](https://i.gyazo.com/7fee5040d7f9ad18256be1ba4f9372e0.png)
  
## plateaus
  - make learning slow
  ![plat](https://i.gyazo.com/7ecf4c0b8b6a9fb8867c2409f1c732aa.png)
  
  
