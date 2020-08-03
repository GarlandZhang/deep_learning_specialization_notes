![hyp](https://i.gyazo.com/49182c6d83bac357164efb5aa1e18a68.png)

![x0](https://i.gyazo.com/caea4b7d9d33b98d604fd482e1a1c729.png)

## gradient descent
![grad_desc](https://i.gyazo.com/4de2997bb4f630e7523c4c4bb42ec0ae.png)

## feature scaling
in general, want to put everything in range of -1 to 1 (e.g.; for images, we do x / 127.5 - 1). We can divide by the range of values (max - min)

## mean normalization

subtract value by average. 

so to apply feature scaling and mean normalization, use:

![fs+mn](https://i.gyazo.com/92222afa92d7b84de396b87afbf98043.png)

## learning rate

if learning rate too big, may overshoot and increase cost function isntead.

if too small, slow convergence

"Debugging gradient descent. Make a plot with number of iterations on the x-axis. Now plot the cost function, J(θ) over the number of iterations of gradient descent. If J(θ) ever increases, then you probably need to decrease α."

"Automatic convergence test. Declare convergence if J(θ) decreases by less than E in one iteration, where E is some small value such as 10^{−3}. However in practice it's difficult to choose this threshold value."
