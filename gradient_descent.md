gradient descent is a way to estimate the parameters in the hypothesis.

![gd_visualized](https://i.gyazo.com/efcccbb5d7fa66fab111d7b8e13e81ff.png)

"The way we do this is by taking the derivative (the tangential line to a function) of our cost function. The slope of the tangent is the derivative at that point and it will give us a direction to move towards. We make steps down the cost function in the direction with the steepest descent. The size of each step is determined by the parameter α, which is called the learning rate."

![gd_algo](https://i.gyazo.com/7f4b2119d6b7b736ee3946d826430589.png)

## intuition

Regardless of the slope's sign, cost fn eventually converges to min value.

![gd_intuit](https://i.gyazo.com/b09e4f6c49b165f142fce9e8d5725b39.png)

note: learning rate can impact gradient descent too:

![gd_lr](https://i.gyazo.com/485d5c153bac298fc1108e15ca933f38.png)

![gd_algo_impl](https://i.gyazo.com/7ca689a3f3d7b3b51c3361b5bbdfe1e9.png)
"This method looks at every example in the entire training set on every step, and is called batch gradient descent."


warning: grad desc can converge to local minimum.

## large datasets
- with each gradient calculation, we sum over m training examples; this is computationally expensive if m is very large
- to measure if increasing m leads to better performance, plot m on x axis and error (cost function) on y axis for both the cost function of cv and training:
![large](https://i.gyazo.com/67a33dc2ad647f57abdd154511f2b19b.png)
  - in the first graph, increasing m will reduce cost for cv error but in second graph it wondt do much

## stochastic gradient descent
so far we've been using **batch gradient descent** where we sum over all traiing examples

in stochastic, we update after each training example:

![comp](https://i.gyazo.com/30441c8da3ae6d0592463c57ebd40754.png)

algo:

![algo](https://i.gyazo.com/a2b1da969f9b6336d6e54f0d37fc31ef.png)

note: "The cost function J should go down with every iteration of batch gradient descent (assuming a well-tuned learning rate \alphaα) but not necessarily with stochastic gradient descent."

### checking for convergence

![comp](https://i.gyazo.com/1ef1a9d9a472b45fc15b88512e5408c9.png)
  - learning rate should decay as num iterations increase

## mini-batch gradient descent

so far:
![summ](https://i.gyazo.com/73a45d4ad4c75432f104e7135cdc8556.png)

- allows parallelization
![algo](https://i.gyazo.com/6798d1b892cdf8aba35b9f9e8afcc148.png)




