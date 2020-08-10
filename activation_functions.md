## tanh
  - is just a shifted version of sigmoid (takes on values of -1 to 1 instead)
  - note: tanh almost always better than sigmoid except for output layer
  - disadvantage of both sigmoid and tanh is derivs approx 0 when z is super large or small
  
## relu
  - solves the above problem
  - disadvantage is deriv is 0 when z < 0
  
## Leaky ReLU
  - solves above problem by having a slope value for z < 0
  
  
![summ](https://i.gyazo.com/c253534cfcd2a29a7cc64f4a8c32d7f6.png)

## why do we need non-linear activation functions
  - without it, output is just a linear function of inputs; therefore, no need for hidden layers as its just a linear function
