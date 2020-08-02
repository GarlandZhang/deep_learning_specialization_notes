## model representation
the simplest learning algorithm we use to model the relationship between input and output (for supervised learning) is **linear regression**.

hypothesis is the function that maps from x to y. learning algorithm is how we improve the hypothesis.
![la=>h](https://i.gyazo.com/05a63aa620f37bf7ad269f6f2179712a.png)

## cost function

"We can measure the accuracy of our hypothesis function by using a cost function."

we just take the average squared difference between our guess and actual output aka **mean squared error**

![cost_fn](https://i.gyazo.com/af049b77793e3ef597822c6c474bc07e.png)


ideally, we try to **minimize** the cost function as that implies the hypothesis is closer to the actual outputs

![cost_fn_contour](https://i.gyazo.com/278eb1dd5e07aebd5bfc611539fe8cf6.png)

notice how hypothesis gets closer to actual outputs when cost function is minimized:

![cost_fn_contour_better](https://i.gyazo.com/20c090baf02438a1314525ab3718e817.png)
