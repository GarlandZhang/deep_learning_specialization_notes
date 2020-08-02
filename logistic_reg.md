in classification, we expect output ot be 0 or 1. Since linear reg's hypothesis fn can have values outside of [0, 1], then we apply logistic function to th linear reg hypothesis function.

![log_reg](https://i.gyazo.com/88aeab01637a6d37bc6f6eaf4c43ed39.png)
  - the new hypothesis fn represents the probability the output is 1.
  - we can also say: 0^Tx >= 0 => y = 1 and 0^Tx < 0 => y = 0
  
## decision boundary
the line that separates the area where y = 0 and y = 1 and is created by the hypothesis function

![dec_bound](https://i.gyazo.com/15de132e73a4677cf0d8d4968d4070fa.png)

## cost fn

the cost function used in linear regression can lead to a **non-convex** cost function (multuiple local minima) especially if the hypothesis is complicated. ideally we want a **convex** cost function.

![cost_fn](https://i.gyazo.com/9b08db9804087af13ea3a06b7d1f4f95.png)
- penalize incorrect guesses heavily 

simplified cost function:

![simpl_cost_fn](https://i.gyazo.com/9dcaa5ed22d2d05e11a35d3e3060c93c.png)

## gradient descent

like linear reg, we use gradient descent to improve the parameters.

![gd](https://i.gyazo.com/cdee4a6cd6167e278329dfbc84fddb90.png)

## advanced optimization

e.g.; conjugate gradient, BFGS, L-BFGS
  - faster than gradient descent
  - no need to pick learning rate
  
![adv_ops](https://i.gyazo.com/00b7080189ea48d92024572f67572c4f.png)

## multiclassification

for each class, set instances to 1 and all other class instances to 0 
  - train classifier on each of the classes
  - choose the class for an input x with highest hypothesis output
