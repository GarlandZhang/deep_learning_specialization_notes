![comp](https://i.gyazo.com/3f9363073d342b7263b2c72a1132001a.png)
  - graph organizes flow of operations from left to right; this is foreward propagation
  
![deriv](https://i.gyazo.com/552d47ba37f9a8e7a26916f433f67eb4.png)
![deriv2](https://i.gyazo.com/e3abcfd77f5baf9622f515faf65b72da.png)
  - when calculating derivates, we go from right to left (aka calculate all drivs for J in respect to prev inputs, then go to previous node and calculate all derivs for v in respect to prev inputs, and etc.)
    - use chain rule for all intermeddiate derivatives (aka not J derivs)
  - can calculate derivs by adding a small number, 0.001, and see how that affects the value
  
## logistic regression derivates

![log_reg](https://i.gyazo.com/f47b94e1b1057459770b7784c9ff1063.png)

## grad desc

![grad](https://i.gyazo.com/aca0563d7da8cb824be38201479837db.png)
  - once we calculate derivates w.r.t inputs, then we cana update the weights and bias with the learning rate * derivs

## vectorization

  - for loop over m exapmles to calc grad desc is inefficient

### foreward propagation
![vec](https://i.gyazo.com/81d3620a0cc91f8cb4eb8308cb6f7053.png)
  - explanation: we want to calculate Z (the raw output value from applying weights to input values). we can do that by multiplying the weights with each x input (note how w does not depend on m). Then we add the biases
  
### gradient computation
![vec](https://i.gyazo.com/a22f5bf52e6f5f88eff890729355bf74.png)
  - rhs is th vectorized impl
  - this is for two layer NN
  - compared to gradient descent before, the dw's are the triangles and dz's is the 8's
