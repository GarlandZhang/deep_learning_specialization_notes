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

